# Oppskrift: Slik aktiverer du merge queue

Denne oppskriften viser hvordan du slår på merge queue for et repo på GitHub.

## 1. Tillat auto-merge

1. Gå til repoet på GitHub.
2. Åpne **Settings**.
3. Under **General** → **Pull Requests**, huk av for **Allow auto-merge**.

## 2. Opprett et branch-ruleset

1. Gå til **Settings** → **Rules** → **Rulesets**.
2. Velg **New ruleset** → **New branch ruleset**.
3. Fyll inn:
   - **Ruleset name**: et beskrivende navn, f.eks. `merge-queue`.
   - **Enforcement status**: sett til **Active**.
   - **Target branches**: velg **Add target** → **Include default branch**.
4. Under **Branch rules**, velg **Require status checks to pass**:
   - Klikk **Add checks** og legg til de sjekkene som må være grønne før merge (f.eks. bygg og test).
   - Huk av for **Require branches to be up to date before merging**.
5. Klikk **Create**.

## 3. Aktiver merge queue

1. Åpne rulesettet fra forrige steg.
2. Under **Branch rules**, huk av for **Require merge queue**.
3. Klikk **Save changes**.

## 4. Slå på merge queue i Dependabot-automerge

Hvis repoet bruker `dependabot-automerge.yaml` fra [tms-deploy](https://github.com/navikt/tms-deploy) (som igjen bruker `navikt/automerge-dependabot`), må du sette inputen `merge-queue` i kallerens `with`. Merge queue er opt-in, og standardverdien er `"false"` (merger direkte).

| Verdi | Oppførsel |
| --- | --- |
| `"false"` (standard) | Merger alltid direkte. |
| `"auto"` | Legger PR-en i kø hvis målbranchen har en `merge_queue`-regel, ellers merges den direkte. |
| `"true"` | Legger alltid i kø. |

Repoer som aktiverer merge queue bør bruke `"auto"` (eller `"true"`):

```yaml
jobs:
  dependabot-automerge:
    uses: navikt/tms-deploy/.github/workflows/dependabot-automerge.yaml@v1
    with:
      merge-queue: "auto"
    secrets:
      APP_ID: ${{ secrets.APP_ID }}
      PRIVATE_KEY: ${{ secrets.PRIVATE_KEY }}
```

Merk:

- Workflows med påkrevde sjekker må også trigges på `merge_group`:

  ```yaml
  on:
    pull_request:
    merge_group:
  ```

- Jobben har outputene `merged-pr-count` og `queued-pr-count`. PR-er i kø telles ikke som merget.

## Resultat

Pull requester til default-branchen må nå ha grønne statussjekker og være oppdatert mot branchen før de kan merges. Med merge queue aktivert legges de i kø, og Dependabot-PR-er håndteres av `merge-queue`-inputen.
