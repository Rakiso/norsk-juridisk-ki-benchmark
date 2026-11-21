# Norsk juridisk KI-benchmark

**Et åpent prosjekt for etterprøvbar evaluering av norske juridiske KI-tjenester.**

Målet er å undersøke hvor godt tjenestene løser realistiske juridiske oppgaver, hvilket kildegrunnlag svarene har, og hvor lett resultatene er å kontrollere og bruke.

> **Status: metodeutkast v0.1 · 21. november 2026.** Ingen tjenester er evaluert, ingen juridiske fasiter er godkjent, og ingen rangering er publisert. De to eksemplene i dette repoet er offentlige utviklingseksempler som trenger faglig gjennomgang.

## Start her

| Dokument | Innhold |
| --- | --- |
| [Testprotokoll](docs/protokoll.md) | Forslag til omfang, oppgaver, gjennomføring og rapportering |
| [Vurderingsrubrikk](docs/vurderingsrubrikk.md) | Juridisk kvalitet, kilder, usikkerhet og separat UX-vurdering |
| [Kilder og eksisterende initiativer](docs/kilder.md) | Etterprøvbart researchgrunnlag og avgrensninger |
| [Saksmal](templates/sak.md) | Mal for oppgaver, kilder, avklaringer og faglig godkjenning |
| [Eksempel: avklaring](examples/DEV-001-avklaring.md) | En fiktiv situasjon med manglende opplysninger |
| [Eksempel: dokumentanalyse](examples/DEV-002-dokumentanalyse.md) | Motstridende frister i en helt fiktiv avtale |
| [Veikart](ROADMAP.md) | Arbeidet frem mot en avgrenset pilot |
| [Bidra](CONTRIBUTING.md) | Hvordan foreslå endringer, oppgaver og faglig vurdering |
| [Åpenhet og styring](GOVERNANCE.md) | Roller, interesser, vurdering og publisering |

## Hva vi vil måle

Tre spor skal rapporteres separat:

1. **Vanlig tjenestebruk:** Hva produktet leverer med sine egne tilgjengelige kilder og funksjoner.
2. **Felles dokumentgrunnlag:** Hvordan tjenestene behandler identiske, kontrollerte dokumenter.
3. **UI/UX og arbeidsflyt:** Hvordan brukeren finner, kontrollerer, redigerer og bruker resultatet.

Juridisk riktighet, alvorlige feil, kildestøtte, fullstendighet og håndtering av usikkerhet skal fremgå hver for seg. Et bestemt abonnement, produktmodus og testtidspunkt er del av resultatet. Svarene alene gir ikke innsyn i leverandørens database eller interne arkitektur.

## Forslag til første pilot

Protokollen foreslår **48 sakspakker i to rettsområder**, valgt etter en kartlegging av produktene: 10 daterte regelspørsmål, 12 vurderinger av faktum, 8 kildeoppgaver, 10 dokumentanalyser og 8 dialogoppgaver. Dette er en plan; oppgavesettet er ikke ferdig laget.

Før piloten utvikles 8–12 åpne saker for å prøve ut rubrikker og arbeidsflyt. Disse skal holdes utenfor den senere sammenligningens evalueringssett. Bokmål og nynorsk inngår i planleggingen, og språkvarianter av samme sak behandles som sammenhengende observasjoner.

## Hva som er åpent

Metode, rubrikker, offentlige utviklingseksempler og endringshistorikk deles her. Et fremtidig skjult evalueringssett må oppbevares utenfor dette repoet og dets git-historikk. En privat mappe eller `.gitignore` er ikke en tilgangskontroll.

Det er foreløpig ingen automatisk testkjører eller koblinger til leverandørtjenester. Første fase prioriterer faglig etterprøvbare oppgaver og en praktisk gjennomføringsmåte.

## Hvem kan bidra?

Jurister, forskere, utviklere, brukere og leverandører kan bidra med metodekritikk, oppgaveforslag, kildekontroll og vurdering av brukeropplevelse. Se [bidragsveiledningen](CONTRIBUTING.md). Å bidra eller bli omtalt som kilde innebærer ikke at man har godkjent prosjektet eller resultatene.

Initiativtaker og foreløpig vedlikeholder er [Thor Langfeldt / Rakiso](https://github.com/Rakiso). Prosjektet er i oppstart og har ikke etablert et uavhengig fagpanel. Roller og relevante interesser er beskrevet i [GOVERNANCE.md](GOVERNANCE.md).

## Lisens

Prosjektets eget materiale er tilgjengelig under [MIT-lisensen](LICENSE). Eksterne datasett, rettskilder og leverandørsvar beholder sine egne vilkår og er ikke omfattet av en ny lisens bare fordi de omtales her. Foreløpig lenker repoet til eksterne kilder uten å distribuere datasettene.

## English summary

An open, early-stage initiative to evaluate complete Norwegian legal AI services. The proposed methodology separates legal quality, source support and user experience. This repository contains draft methods and public development examples; it does not yet contain validated legal answer keys, product evaluations or a leaderboard. Contributions in Norwegian or English are welcome.
