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

## Resultat

Pull requester til default-branchen må nå ha grønne statussjekker og være oppdatert mot branchen før de kan merges.
