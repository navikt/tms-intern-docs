# Frontend-applikasjoner – Team Minside

Oversikt over frontend-repoer eid av team **min-side** (`navikt/min-side`) – *"Team Minside jobber med innloggede sider på nav.no."*

## Kjerne-frontendapper for min-side

| Repo | Stack | Beskrivelse |
|---|---|---|
| [tms-min-side](https://github.com/navikt/tms-min-side) | Astro | Hovedapplikasjonen (container) for innlogget Min side på nav.no |
| [tms-dokumentarkiv-frontend](https://github.com/navikt/tms-dokumentarkiv-frontend) | Astro | Frontend for dokumentarkivet på Min side |
| [tms-utbetalingsoversikt-frontend](https://github.com/navikt/tms-utbetalingsoversikt-frontend) | Astro | Frontend for utbetalingsoversikt på Min side |
| [tms-utkast-frontend](https://github.com/navikt/tms-utkast-frontend) | Astro | Frontend for visning av utkast (påbegynte søknader) på Min side |
| [tms-varsler-frontend](https://github.com/navikt/tms-varsler-frontend) | Astro | Frontend for visning av varsler på Min side |
| [personopplysninger](https://github.com/navikt/personopplysninger) | Astro | Visning av personopplysninger i henhold til GDPR |
| [tms-min-side-demo](https://github.com/navikt/tms-min-side-demo) | Astro | Demo-container som setter sammen mikrofrontends for Min side |
| [tms-test-producer-frontend](https://github.com/navikt/tms-test-producer-frontend) | Astro | Frontend for å opprette testeventer (utkast og varsler) for gjeldende bruker |

## Mikrofrontender (rendres inne i min-side)

| Repo | Stack | Beskrivelse |
|---|---|---|
| [aap-min-side-microfrontend](https://github.com/navikt/aap-min-side-microfrontend) | Astro | AAP-mikrofrontend for Min side |
| [aia-min-side-ssr](https://github.com/navikt/aia-min-side-ssr) | Astro | Arbeidsflate for innlogget arbeidssøker |
| [ao-min-side-microfrontend-ssr](https://github.com/navikt/ao-min-side-microfrontend-ssr) | Astro | Mikrofrontend for arbeidsoppfølging (ao) på Min side |
| [aktivitetspenger-innsyn-mikrofrontend-ssr](https://github.com/navikt/aktivitetspenger-innsyn-mikrofrontend-ssr) | Astro | Mikrofrontend for innsyn i aktivitetspenger |
| [esyfo-mikrofrontends](https://github.com/navikt/esyfo-mikrofrontends) | Astro | Mikrofrontender for digital sykefraværsoppfølging (esyfo) |
| [familie-ba-minside-mikrofrontend](https://github.com/navikt/familie-ba-minside-mikrofrontend) | Astro | Mikrofrontend for barnetrygd (familie-ba) på Min side |
| [familie-ef-mikrofrontend-minside](https://github.com/navikt/familie-ef-mikrofrontend-minside) | Astro | Mikrofrontend for enslig forsørger – overgangsstønad, barnetilsyn og skolepenger |
| [jobbmuligheter-mikrofrontend](https://github.com/navikt/jobbmuligheter-mikrofrontend) | Astro | Mikrofrontend som lenker til direktemeldte stillingsannonser for brukere under oppfølging |
| [k9-innsyn-dine-pleiepenger-mikrofrontend-ssr](https://github.com/navikt/k9-innsyn-dine-pleiepenger-mikrofrontend-ssr) | Astro | Mikrofrontend for innsyn i pleiepenger for sykt barn (K9) |
| [meldekort-mikrofrontend](https://github.com/navikt/meldekort-mikrofrontend) | Astro | Mikrofrontend for meldekort på Min side |
| [mine-klager-microfrontend](https://github.com/navikt/mine-klager-microfrontend) | Go | Mikrofrontend for innsyn i egne klager |
| [pam-min-side-microfrontend](https://github.com/navikt/pam-min-side-microfrontend) | Astro | Mikrofrontend fra Team PAM (arbeidsmarked) på Min side |
| [pensjonskalkulator-microfrontend-ssr](https://github.com/navikt/pensjonskalkulator-microfrontend-ssr) | Astro | Mikrofrontend for pensjonskalkulator på Min side |
| [tiltakspenger-meldekort-microfrontend](https://github.com/navikt/tiltakspenger-meldekort-microfrontend) | Astro | Mikrofrontend for meldekortløsningen til tiltakspenger |
| [ungdomsprogramytelse-innsyn-mikrofrontend-ssr](https://github.com/navikt/ungdomsprogramytelse-innsyn-mikrofrontend-ssr) | Astro | Mikrofrontend for innsyn i ungdomsprogramytelse |

## Maler (templates)

| Repo | Stack | Beskrivelse |
|---|---|---|
| [tms-astro-template](https://github.com/navikt/tms-astro-template) | Astro | AstroJS-frontendmal med IdPorten-autentisering for eksterne brukere |
| [tms-astro-template-azure](https://github.com/navikt/tms-astro-template-azure) | Astro | AstroJS-frontendmal med Azure-autentisering for interne brukere |
| [tms-microfrontend-template-ssr](https://github.com/navikt/tms-microfrontend-template-ssr) | Astro | Mal for å opprette nye server-side-rendrede mikrofrontends til Min side |

## Biblioteker / verktøy

| Repo | Stack | Beskrivelse |
|---|---|---|
| [tms-astro-auth](https://github.com/navikt/tms-astro-auth) | TypeScript | Astro-middleware for autentisering via Wonderwall/Nais |
| [tms-astro-logger](https://github.com/navikt/tms-astro-logger) | TypeScript | Egendefinert Astro-logger med strukturerte JSON-logger for Nav/Grafana |
| [tms-astro-mocks](https://github.com/navikt/tms-astro-mocks) | TypeScript | Astro-integrasjon som serverer mock-HTTP-endepunkter under utvikling |
| [tms-deploy](https://github.com/navikt/tms-deploy) | Python / GitHub Actions | Workflows for deploy av Min side-frontender |
| [tms-shared-dependencies](https://github.com/navikt/tms-shared-dependencies) | JavaScript | Delte avhengigheter (bl.a. React/React-DOM) som brukes i mikrofrontendene og Min side |

## Øvrige (docs, redirect, prototype, test)

Frontend-stack-repoer som ikke er egne applikasjoner, men tatt med for fullstendighet.

| Repo | Stack | Merknad | Beskrivelse |
|---|---|---|---|
| [tms-docs](https://github.com/navikt/tms-docs) | Astro | Dokumentasjonsside | Dokumentasjonssiden til Team Min side (tms-docs.nav.no) |
| [tms-dokumentarkiv-redirect](https://github.com/navikt/tms-dokumentarkiv-redirect) | JavaScript | Redirect-tjeneste | Node.js-tjeneste som videresender gamle Mine saker-lenker til dokumentarkivet |
| [tms-produktside-prototype](https://github.com/navikt/tms-produktside-prototype) | Astro | Prototype | Prototype for en produktside |
| [tms-microfrontend-do-test](https://github.com/navikt/tms-microfrontend-do-test) | Astro | Test-repo | Test-repo basert på mikrofrontend-malen |
