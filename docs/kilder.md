# Kilder og eksisterende initiativer

**Sist kontrollert: 21. november 2026.**

Dette er et kildegrunnlag for prosjektets metode og avgrensning. Omtale av forskere, institusjoner og leverandører innebærer ikke samarbeid, tilslutning eller godkjenning. Vi har kontrollert publiserte beskrivelser og deler av evalueringskoden, men har ikke gjentatt studiene. Dokumentet inneholder ikke kopier av datasett, fasiter eller rettskildesamlinger.

## Nor-CaseHOLD: setningsekstraksjon

Bendik Eeg-Henriksens [Nor-CaseHOLD](https://github.com/Bendik-Eeg-Henriksen/Nor-CaseHOLD) inneholder **1 244 dokumenter**: 627 Høyesterettsavgjørelser og 617 bindende forhåndsuttalelser fra Skatteetaten. Det publiserte testsettet har **233 dokumenter**. Oppgaven velger fem setninger fra hvert dokument og sammenligner uttrekket med det offisielle sammendraget ved hjelp av ROUGE. [Datasettkortet](https://huggingface.co/datasets/bendik-eeg-henriksen/nor-casehold) oppgir CC BY 4.0; repositoriet oppgir Apache 2.0 for kode og modell.

[Evalueringskoden](https://github.com/Bendik-Eeg-Henriksen/Nor-CaseHOLD/blob/main/evaluate.py) bruker det offisielle sammendraget som søkespørring for både ordsøk og dense-modeller. Søket skjer innenfor ett allerede valgt dokument. BM25 og TF-IDF oppnår høyere ROUGE enn de undersøkte encoderne, men dette dokumenterer ikke at ordsøk generelt slår moderne embeddings i juridisk RAG. Oppgaven, modellutvalget og metrikken begrenser hva resultatene sier om komplette tjenester.

Prosjektets bruk: en mulig komponenttest og metodeinspirasjon. Et eget oppsett må teste om tjenesten finner riktig dokument fra et vanlig brukerspørsmål, og om svaret anvender rettskildene riktig.

## norregel: daterte tallverdier

Eirik Botten Nicolaysens [norregel-artikkel, versjon 2](https://arxiv.org/html/2610.29207v2), revidert 2. november 2026, beskriver **916 oppgaver**, hvorav **880** inngår i hovedanalysen etter eksklusjoner. Verdier og historikk er hentet mekanisk fra Lovdatas åpne data. Svar klassifiseres som korrekte, utdaterte, feil eller ufortolkbare.

Dette er **ikke et åpent oppgavesett**. Spørsmål og fasiter holdes tilbake for å begrense treningsforurensning. Artikkelen oppgir at kode, resultater og skårklasser deles på [Zenodo](https://doi.org/10.5281/zenodo.23422302), mens nye evalueringer kan avtales med EcoDeco AS.

Artikkelen konkluderer ikke robust med at utdaterte svar blir vanligere etter modellens kunnskapsgrense: den relevante sensitivitetsanalysen S8 svekker hovedfunnet. Et feil tall utenfor den registrerte historikken beviser heller ikke at tallet aldri har vært gyldig. «Feil» skal derfor ikke automatisk omtales som «sikkert hallusinert».

Prosjektets bruk: inspirasjon til daterte fasiter, historikk og separate feilkategorier. Vi må lage egne kontrollerte oppgaver eller avklare tilgang; antallet publiserte oppgaver skal ikke presenteres som fritt tilgjengelige testdata.

## Lovdata: regelverk og gjenbruk

Lovdatas [kunngjøring 3. november 2025](https://lovdata.no/artikkel/lovdata_tilrettelegger_for_bruk_tilpasset_var_ki-hverdag_gjor_api_av_oppdatert_regelverk_gratis_tilgjengelig_for_alle/5277) åpner gratis API-tilgang til gjeldende lover og sentrale forskrifter under NLOD 2.0. Dette bekreftes i [Lovdatas API-hjelp](https://lovdata.helpscoutdocs.com/article/440-hva-er-lovdata-api).

Åpningen er ikke dokumentasjon på fri tilgang til all rettspraksis, alle historiske versjoner eller redaksjonelt bearbeidede kilder. For hvert materiale må prosjektet registrere kilde, versjon, hentetidspunkt og konkret gjenbruksgrunnlag. [NLOD 2.0-vilkårene](https://data.norge.no/nlod/no/2.0) krever blant annet korrekt navngivelse uten å antyde at lisensgiver anbefaler bruken. Ingen av disse datakildene er innlemmet i dette repositoriet gjennom dette dokumentet.

## Andre norske målinger

[Wammers Juss-Bench v0.1](https://wammer.ai/benchmarks/juss-bench) beskriver 612 oppgaver per spor, med og uten kildeoppslag, og fem rettsområder. Siden merker resultatene som foreløpige interne kjøringer og anonymiserer flere sammenligningsmodeller.

[Attorlys kvalitetsmålinger](https://attorly.ai/en/benchmarks) beskriver blant annet kildegjenfinning, kildekontroll og kontraktsredigering. Leverandøren opplyser selv at oppgavene og vurderingen er interne, og at de ikke utgjør en uavhengig evaluering.

Begge er relevante for kartleggingen. Opplysningene behandles her som leverandørenes egne publiserte beskrivelser og foreløpige kvalitetsbelegg, ikke som uavhengig kvalitetssikrede resultater. De viser også hvorfor en påstand om at det «ikke finnes norske benchmarks» blir for kategorisk.

## Internasjonale metodereferanser

[VLAIR – Legal Research](https://www.vals.ai/industry-reports/vlair-10-14-25), datert 14. oktober 2025, sammenligner produkter på 200 amerikanske juridiske spørsmål og vurderer blant annet korrekthet, kildegrunnlag og anvendelighet.

Studien [Hallucination-Free?](https://arxiv.org/abs/2405.20362) undersøker kommersielle juridiske søkeverktøy gjennom en forhåndsregistrert evaluering og skiller mellom korrekthet, kildeforankring og ufullstendige svar.

Disse arbeidene gir metodeinspirasjon for tjenestetesting. Resultater fra amerikansk rett gir ingen dokumentert rangering i norsk rett, og prosenttall skal ikke sammenstilles uten samme oppgaver, tilgang, skåring og testbetingelser. Før dette prosjektet publiserer egne resultater, må det dokumentere både testoppsettet og hvilke konklusjoner materialet faktisk kan bære.
