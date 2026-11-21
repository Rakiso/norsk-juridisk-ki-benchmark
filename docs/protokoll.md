# Evalueringsprotokoll

**Versjon:** 0.1-utkast · **Dato:** 21. november 2026  
**Status:** Forslag til metode. Ingen tjenester er evaluert, og ingen resultater eller rangeringer er publisert.

## 1. Formål og avgrensning

Prosjektet skal undersøke hva norske juridiske KI-tjenester leverer i avgrensede brukeroppgaver: juridisk riktighet, etterprøvbare kilder, håndtering av usikkerhet og praktisk brukbarhet. Det er en evaluering av observerbar tjenesteatferd. Svar og kildehenvisninger gir ikke grunnlag for å fastslå hvilken modell, database eller søketeknologi leverandøren bruker.

Piloten foreslås avgrenset til **to rettsområder som ennå ikke er valgt**. Områdene velges etter en dokumentert kartlegging av tjenestenes målgrupper og støttede oppgaver, før testsaker eller leverandørresultater påvirker valget. Protokollen gir ingen sertifisering eller garanti for en tjenestes generelle kvalitet.

## 2. Tre separate evalueringsspor

| Spor | Oppsett | Hva resultatet kan belyse |
|---|---|---|
| Tjenestens ordinære produkt | Oppgaven løses med tjenestens tilgjengelige kilder og funksjoner | Samlet kvalitet i den aktuelle produktmodusen |
| Felles dokumentgrunnlag | Tjenestene får identiske, tillatte dokumenter og samme oppgave | Analyse og dokumentforståelse med likt tilført grunnlag |
| Brukeropplevelse | Forhåndsdefinerte handlinger utføres og dokumenteres | Hvor lett brukeren kan forstå, kontrollere og bruke resultatet |

Sporene rapporteres hver for seg. Felles dokumenter isolerer ikke språkmodellen fullstendig. God presentasjon kompenserer ikke for juridiske feil. Manglende kilder i et svar betyr at kildestøtten ikke er dokumentert i svaret; det beviser ikke at tjenesten mangler kilden internt.

## 3. Planlagt pilot: 48 sakspakker

| Hovedtype | Antall | Sentrale observasjoner |
|---|---:|---|
| Daterte regler, beløp og frister | 10 | Riktig regel eller verdi på oppgitt rettsdato |
| Rettslig anvendelse på faktum | 12 | Vilkår, relevante fakta, motargumenter og konklusjon |
| Finne og kontrollere kilder | 8 | Kildens eksistens, støtte og korrekt gjengivelse |
| Dokumentanalyse | 10 | Sporbare funn, motstrid og manglende opplysninger |
| Dialog og endrede fakta | 8 | Relevante avklaringer og oppdatert vurdering |
| **Sum** | **48** | **Foreløpig fordeling, uten ferdige saker** |

Én sak kan vurderes på flere dimensjoner, men har én hovedtype. Juristvaliderte språkpar på bokmål og nynorsk og varianter av samme faktum merkes som samme sakfamilie. De er ikke uavhengige observasjoner. Den endelige fordelingen mellom rettsområder, språk og spor fryses før evalueringen.

Før hovedkjøringen prøves opplegg og rubrikk på separate utviklingssaker. Disse inngår ikke i sammenligningsresultatene. Piloten skal avdekke konkrete feil og forbedre metoden; 48 strategisk valgte saker dokumenterer ikke en generell feilrate for norsk juss.

## 4. Krav til hver sakspakke

En pakke skal ha en stabil identifikator, versjon, hovedtype, rettsområde og eventuelt sakfamilie. Den skal inneholde:

- Brukeroppgave, faktum, målgruppe og eventuelle vedlegg.
- **Rettsdato:** tidspunktet rettstilstanden skal vurderes for, inkludert relevante overgangsregler.
- Kontrollert kildegrunnlag med dokumentversjon, relevante avsnitt og dokumentert adgang til bruk.
- Vurderingspunkter, akseptable alternative konklusjoner og forhåndsdefinerte alvorlige feil.
- Standardiserte opplysninger som gis dersom tjenesten stiller relevante avklaringsspørsmål.
- Regler for modus, oppfølging, tidsbudsjett og fullføring.

Et referansesvar er et hjelpemiddel; fasiten består av juridiske vurderingspunkter og kildegrunnlag. Vi krever ikke én ordlyd eller én konklusjon der flere er forsvarlige. Saksforfatter og juridiske kontrollører dokumenteres internt. **Ingen sak brukes til offentlig scoring før kvalifiserte jurister har validert faktum, kilder og rubrikk.** Uavklarte saker holdes utenfor.

## 5. Sammenlignbare og tillatte kjøringer

Hver evaluert konfigurasjon registreres med produkt, abonnement, funksjonsmodus, kjente innstillinger og synlig versjon. Gratis og betalt tilgang rapporteres som forskjellige konfigurasjoner. Ukjent modellversjon oppgis som ukjent.

Testene bruker ordinær, tillatt evalueringsadgang. Gjeldende vilkår og eventuell tillatelse til automatisering dokumenteres før kjøring. Tilgangsbegrensninger omgås ikke. Bruk syntetiske saker eller dokumenter med avklart grunnlag for bruk, uten reelle personopplysninger som ikke trengs for testen.

En felles kjernetest dekker sammenlignbare oppgaver. Særfunksjoner får egne moduler. Oppgaver utenfor tjenestens dokumenterte støtte registreres som manglende dekning; de fjernes ikke lydløst fra resultatene. Juridisk feil, avslag, teknisk feil og manglende funksjon holdes atskilt.

Alle kjøringer starter i ny samtale uten tidligere sakskontekst. Prompt, vedlegg og oppfølgingsregler er like innen hver sammenligning. Produktets relevante ordinære arbeidsflyt kan brukes når den er forhåndsdefinert. Man velger ikke den beste av flere skjulte forsøk.

**Kjøredato** registreres separat fra rettsdato, med klokkeslett og tidssone. Lagre full dialog, svar, synlige kilder, feil, tidsbruk og nødvendige skjermbilder. Gjentakelser og regler for tekniske omkjøringer fastsettes på forhånd og gjelder likt for alle.

## 6. Bedømmelse og rapportering

To jurister vurderer svarene uavhengig etter [vurderingsrubrikken](vurderingsrubrikk.md). Leverandørnavn skjules og svarrekkefølge randomiseres så langt praktisk mulig, uten å fjerne nødvendig kildemateriale. Mulige avslørende kjennetegn dokumenteres. Uenighet og avgjørelse bevares, ikke bare sluttpoeng.

Rapporten viser hver kvalitetsdimensjon, alvorlige feil, fullføring og dekning med tydelige nevnere. Brukeropplevelse rapporteres separat. Ingen samlet rangering inngår i v0.1. LLM-støttet uttrekk kan hjelpe bedømmerne, men erstatter ikke juridisk kontroll.

Usikkerhetsmål må ta hensyn til at de samme sakene brukes på flere tjenester, og at varianter og gjentakelser hører sammen. Eventuelle statistiske analyser forhåndsdefineres. Et lite, strategisk valgt utvalg skal ikke presenteres som representativt for alle juridiske oppgaver.

## 7. Offentlighet, versjoner og uavhengighet

Offentlig repo kan inneholde metode, rubrikker, kode, syntetiske demonstrasjoner og dokumenterte rettelser. **Det skjulte evalueringssettet og tilhørende fasiter, samt tilgangsbegrenset materiale, lagres utenfor offentlig Git og Git-historikk.** En skjult mappe eller en gren i samme offentlige repo gir ikke beskyttelse.

Protokoll, sakversjoner og rubrikk fryses før hver evaluering. Lovendringer gir nye versjoner; tidligere resultater beholder sitt opprinnelige grunnlag. Finansiering, leverandørtilknytning og hvem som utformer og bedømmer sakene oppgis. Åpen kode alene gjør ikke evalueringen uavhengig.

## Metodisk bakgrunn

Dette dokumentet beskriver prosjektets eget forslag, ikke en publisert eller validert standard. Eksisterende produktstudier gir relevant metodebakgrunn:

- Magesh mfl., *Hallucination-Free? Assessing the Reliability of Leading AI Legal Research Tools*: <https://arxiv.org/abs/2405.20362>
- Vals AI, *Vals Legal AI Report*, februar 2025: <https://www.vals.ai/industry-reports/vlair-2-27-25>
- Vals AI, *VLAIR – Legal Research*, oktober 2025: <https://www.vals.ai/industry-reports/vlair-10-14-25>

Studiene gjelder andre oppgaver og markeder. Resultatene deres overføres ikke til norske tjenester.
