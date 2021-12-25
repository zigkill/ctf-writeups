# PSTs julekalender 2021

PSTs julekalender for 2021 brukte [DASS](https://dass.p26e.dev/), som er samme adresse som for 2020. I *DASS* kommer oppgavene i et slags e-post-program kalt *Snabel-A*.

## Velkommen! (1. desember 08.00)

>Velkommen til NPST zigkill, hyggelig å endelig ha deg på plass!
>
>Jeg er dessverre litt opptatt i dag, men HR tar kontakt med deg kl 18:00 i kveld, så snakkes vi igjen i morgen. På din etterspørsel om mer fritid i denne hektiske førjulsperioden har jeg valgt å gi deg fri på mandager, så kan du få senket skuldrene litt. Håper du blir fornøyd med dette.
>
>Vi ber om at alle løsninger til arbeidsoppgaver leveres i dette formatet: pst{eksempel} (som regel er formatet gitt ut av kontekst, men noen ganger ikke).
>
>Dersom du skulle snuble over verdifull informasjon som ikke hører til arbeidsoppgavene du får utlevert, så send det på en epost til en av oss. Denne informasjonen skal også leveres i formatet beskrevet ovenfor.
>
>Mvh Mellomleder

Jeg tror ikke det var noe poeng å hente fra denne meldingen.

## Velkommen til DASS! (Oppgave 1, 1. desember 18.00)

>Velkommen zigkill!
>
>Veldig hyggelig å ha deg ombord og fint å se at du har funnet veien inn til DASS. For at du skal finne deg mer til rette anbefaler jeg deg å sette ditt eget preg på systemet! Dette kan du gjøre ved å velge «Mal» fra startmenyen, mal din egen skrivebordsbakgrunn og velg Fil -> Sett som skrivebordsbakgrunn. Her er det bare kreativiteten som setter begrensninger, men i tilfelle du trenger litt starthjelp, legger jeg ved et eksempelbilde.
>
>Spent på å følge deg videre, lykke til!
>
>Hilsen HR
>
>📎eksempel_bakgrunnsbilde.png

Jeg lastet opp bildet [her](https://stegonline.georgeom.net/extract) og tok extract av RGB i Layer 0, der flagget lå.

Flagg: `PST{HelloDASS}==`

>Bra jobba zigkill! Mellomleder tar kontakt med deg i morgen med mer konkret informasjon angående hva du skal jobbe med.

Jeg testet først å se på bit planes i RGB, deretter strings i ulike verktøy og det var litt tilfeldig at jeg fant flagget. En bedre tilnærming hadde vært

    `zsteg -a eksempel_bakgrunnsbilde.png | grep -i pst{`.

## Huskelapp (2. desember 18.00)

>Velkommen til teamet zigkill!
>
>Vi går rett på sak. I fjor rakk ikke julenissen å dele ut pakker til alle som hadde gjort seg fortjent. For å komme til bunns i årsaken ble det satt ned et utvalg med mandat til å utnevne en kommisjon som skulle starte arbeidet med opprettelsen av en granskningskommité. Da granskningskommiteen kom med sin utredelse viste det seg at mulighetsrommet for å utøve slemme handlinger ble betraktelig redusert ved nedstenging og isolasjon. Det hadde rett og slett blitt for mange snille barn.
>
>Da nedstenging og isolasjon delvis har vedvart, har det høy prioritet i år å finne en ny, mer optimal rute.
>
>Julenissen fant i går en huskelapp som han tror kan være relevant, men han klarer ikke å finne ut av hva han skulle huske. Kunne du hjulpet han med det?
>
>Mvh Mellomleder
>
>📎huskelapp_til_2021.txt

Huskelappen så ut til å inneholde koordinater, og jeg importerte disse på Google Maps. Punktene viste flagget direkte.

>Selvfølgelig, det gir mening! Jaja, det visste han jo allerede.

## Mistenkelig julekort (3. desember 18.00)

>God fredag. Det Nordpolare Postkontor har oppdaget et julekort som er på vei til Antarktis. Etterretning viser at pingvinene i Antarktis ikke alltid har ren snø i skuffa. Det er derfor ønskelig at en alvebetjent gjennomfører en rutinemessig kontroll, og undersøker julekortets bakside og framside. Rapporter tilbake et eventuelt funn innpakket i pst{}.
>
>📎 julekort_baksiden.jpg
>📎 julekort_framsiden.jpg
>
>Mvh Mellomleder

Begge sidene av julekortet inneholdt symboler som jeg fant ut kalles [Pigpen Cipher](https://en.wikipedia.org/wiki/Pigpen_cipher). Forsiden hadde fire symboler som stavet ut «PILA» mot klokken. Baksiden av kortet måtte snus opp ned for at cipheret skulle gi mening.

Flagg: `pst{julenissenerteit}`

>Vel vel. Tilsynelatende ikke noe muffens her, så julekortet blir sendt videre til Antarktis.

Jeg klarte ikke denne oppgaven helt uten hjelp. Jeg kom fram til cipheret, men skjønte ikke hintet fra forsiden og forsøkte finne en måte å ordne bokstavene på eller bruke varianter av cipheret.

En annen deltaker ga meg hint om at «noe må gjøres med tekstsiden» og det var tilstrekkelig.

## Krøll på verkstedet (4. desember 18.00)

>HMS-ansvarlig var innom verkstedet i går og var helt forskrekket over rotet vi har etterlatt oss der. Jeg er litt opptatt med møter i dag, kan du ta deg tid til å rydde litt? Oversikt over hva vi har på verkstedet ligger vedlagt.
>
>Mvh Mellomleder
>
>📎verksted_npst.txt

Tabellen inneholdt en kolonne der verdiene lå innenfor [ASCII-tabellen](https://en.wikipedia.org/wiki/ASCII) og jeg la inn disse og sorterte på en annen kolonne og da kom flagget fram.

Flagg: `PST{DetBlirFortRot}`

>Takk zigkill, la oss prøve å holde litt bedre orden der fremover.

Selv om jeg ganske tidlig la merke til at to av verdiene i kolonnen var 7b og 7d, som representerer «{» og «}» i ASCII og jeg hadde begynt med riktig løsning, rotet jeg meg bort til jeg fikk en bekreftelse fra en annen deltaker.

## Digitalt varelager (5. desember 18.00)

>NPST har digitalisert varelageret sitt og flyttet det til skyen! For øyeblikket er det fortsatt i oppstartsfasen og trenger litt kvalitetssjekking.
>
>Har du mulighet til å se om Varelager v1 funker som det skal og at det ikke skjuler seg noen feil i systemet?
>
>Varelageret finner du her, og bruk programmeringsgrensesnittnøkkel v1_pgmsqxmddz.
>
>Mvh Mellomleder

Jeg brukte litt tid først på å identifisere databasen (PostgreSQL), men deretter var det ganske raskt å finne data i basen:

`xxx' UNION (select NULL,TABLE_NAME,NULL,NULL,TABLE_SCHEMA,NULL FROM information_schema.tables WHERE TABLE_SCHEMA='v1');--`

Denne SQL-en lister tabeller i schema v1 og viste at det har var en tabell `ting`.

`xxx' UNION (SELECT NULL,COLUMN_NAME,NULL,NULL,NULL,NULL FROM INFORMATION_SCHEMA.COLUMNS WHERE TABLE_NAME='ting');-- -`

Denne SQL-en lister kolonnene i `ting` og viste at det var en kolonne `flagg`.

`xxx' UNION (SELECT NULL,FLAGG,NULL,NULL,NULL,NULL FROM v1.ting);-- -`

Flagg: `PST{5Q1_1nj€Ⓒt10n}`

>Bra jobba zigkill! Jeg syntes det virket som om det var noe muffins i systemet. Forhåpentligvis funker alt bedre i neste oppdatering.

## Ukens ansatt (6. desember 18.00)

>Vi vil takke dere alle for strålende innsats i første uke som alvebetjenter!
>
>Og samtidig annonsere at Peter er ukens ansatt! Gratulerer!
>
>Takk for godt samarbeid, vi ser frem til fortsettelsen.

Hviledag. Jeg tror ikke det var noe poeng å hente fra denne meldingen.

## Kryptert melding (7. desember 18.00)

>Godt å se at du er klar for en ny arbeidsuke! Arbeidsoppgavene står i kø, så det er best å sette i gang umiddelbart:
>
>Det er fanget opp en kryptert melding som Etterretningsalvdelingen har grunn til å tro at inneholder noe av interesse. Meldingen skiller seg ut fordi det ser ut til at mottaker er lokalisert i sydpolare strøk. For andre gang på under en uke! E-alvene er temmelig overbevist om at det er brukt temmelig sikker krypto her, fordi de ikke klarer å knekke meldingen. Og det sier litt, siden e-alvene våre er eksperter på knekking.
>
>Uansett, kan du ta en titt? E-alvene mener det er en umulig oppgave siden de ikke klarer det, men jeg håper at du kanskje har litt nyansattflaks.
>
>Her er meldingen:
>
>Y2MPyYU4kblEXrEfExry4AIRAjqdke+JyQQN50Uj5GuCu5rE66lEzQXB5bE VOlNGRoU06Ny4vh/gzSPFV0mHUrxaaAVt1BwN1WN1HFT7baIejtR5KyG6 JK8yC70CpuPZV610coCiWzdFICcgEtAdQaesScLrg495kxofzG3EGvA=
>
>Mellomleder

Denne viste seg kanskje å være ekstra vanskelig, og oppgaven fikk to oppdateringer (20.00 og 21.45):

>Etterretningsalvdelingen informerer om at mottaker av den krypterte meldingen heter Chili Willy. Kanskje det kan være til hjelp for å dekryptere meldingen?
>
>Mellomleder

og

>en Alvebetjent gjorde meg oppmerksom på at det kan ha foregått En nøkkelutveksling tidligere i desember, kanSkje det kan hjelpe i oppklaringen?
>
>Mellomleder

Fram til den siste meldingen var jeg ikke i nærheten av noe som helst, men der kom det fram både at det finnes et passord (åpenbart `julenissenerteit`) og en algoritme (fra store bokstaver i meldingen, `AES`).
Jeg la inn recipe From Base64->AES Decrypt (med passordet) i [CyberChef](https://gchq.github.io/CyberChef/) og fikk ut meldingen `NPST skal endre paa pakkefordelingsruta i aar. Det gir mulighet for aa sabotere. XOXO M. PS Ikke god jul. PS pst{nootnoot}`.

Flagg: `pst{nootnoot}`

>Konfidensiell informasjon er lekket! Det er uansett verdifullt for oss å vite om det, så takk for innsatsen. Kan det være vår uvenn Pen Gwyn som bedriver kvalme i år igjen? Uansett, jeg rapporterer dette videre til Julenissen, så blir det nok satt i gang strengere sikkerhetstiltak.
>
>Mellomleder

## Egg

## Verktøy

## Hjelp

