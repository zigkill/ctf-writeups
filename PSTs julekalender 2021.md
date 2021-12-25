# PSTs julekalender 2021

PSTs julekalender for 2021 brukte [DASS](https://dass.p26e.dev/), som var samme adresse som for 2020. I *DASS* kommer oppgavene i et slags e-post-program kalt *Snabel-A*.

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

## Velkommen til DASS! (1. desember 18.00)

>Velkommen zigkill!
>
>Veldig hyggelig å ha deg ombord og fint å se at du har funnet veien inn til DASS. For at du skal finne deg mer til rette anbefaler jeg deg å sette ditt eget preg på systemet! Dette kan du gjøre ved å velge «Mal» fra startmenyen, mal din egen skrivebordsbakgrunn og velg Fil -> Sett som skrivebordsbakgrunn. Her er det bare kreativiteten som setter begrensninger, men i tilfelle du trenger litt starthjelp, legger jeg ved et eksempelbilde.
>
>Spent på å følge deg videre, lykke til!
>
>Hilsen HR
>
>📎eksempel_bakgrunnsbilde.png

![eksempel_bakgrunnsbilde.png](/assets/images/npst-2021/eksempel_bakgrunnsbilde.png)

Jeg lastet opp bildet [på Stegonline](https://stegonline.georgeom.net/extract) og tok extract av RGB i Layer 0, der flagget lå.

Flagg: `PST{HelloDASS}==`

>Bra jobba zigkill! Mellomleder tar kontakt med deg i morgen med mer konkret informasjon angående hva du skal jobbe med.

Jeg testet først å se på bit planes i RGB, deretter strings i ulike verktøy og det var litt tilfeldig at jeg fant flagget. En bedre tilnærming hadde vært å bruke zsteg.

    zsteg -a eksempel_bakgrunnsbilde.png | grep -i pst{

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

Flagg: `PST{MANGE SNILLE BARN I VERDEN}`

>Selvfølgelig, det gir mening! Jaja, det visste han jo allerede.

## Mistenkelig julekort (3. desember 18.00)

>God fredag. Det Nordpolare Postkontor har oppdaget et julekort som er på vei til Antarktis. Etterretning viser at pingvinene i Antarktis ikke alltid har ren snø i skuffa. Det er derfor ønskelig at en alvebetjent gjennomfører en rutinemessig kontroll, og undersøker julekortets bakside og framside. Rapporter tilbake et eventuelt funn innpakket i pst{}.
>
>📎 julekort_baksiden.jpg
>📎 julekort_framsiden.jpg
>
>Mvh Mellomleder

![julekort_baksiden.jpg](/assets/images/npst-2021/julekort_baksiden.jpg)
![julekort_framsiden.jpg](/assets/images/npst-2021/julekort_framsiden.jpg)

Begge sidene av julekortet inneholdt symboler som jeg fant ut kalles [Pigpen Cipher](https://en.wikipedia.org/wiki/Pigpen_cipher). Forsiden hadde fire symboler som kanskje stavet ut «PILA» mot klokken. Baksiden av kortet måtte snus opp ned for at cipheret skulle gi mening.

Flagg: `pst{julenissenerteit}`

>Vel vel. Tilsynelatende ikke noe muffens her, så julekortet blir sendt videre til Antarktis.

Jeg klarte ikke denne oppgaven helt uten hjelp. Jeg kom fram til cipheret, men skjønte ikke hintet fra forsiden og forsøkte forgjeves å finne en måte å ordne bokstavene på eller bruke varianter av cipheret som kunne gi mer mening.  
En annen deltaker ga meg hint om at «noe må gjøres med tekstsiden» og det var tilstrekkelig. Det slo meg at en mottaker på Sydpolen ville lese kortet opp-ned.

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

Hviledag.

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

Denne viste seg kanskje å være ekstra vanskelig, og oppgaven fikk to oppdateringer samme kveld (20.00 og 21.45):

>Etterretningsalvdelingen informerer om at mottaker av den krypterte meldingen heter Chili Willy. Kanskje det kan være til hjelp for å dekryptere meldingen?
>
>Mellomleder

og

>en Alvebetjent gjorde meg oppmerksom på at det kan ha foregått En nøkkelutveksling tidligere i desember, kanSkje det kan hjelpe i oppklaringen?
>
>Mellomleder

Fram til den siste meldingen var jeg ikke i nærheten av noe som helst, men der kom det fram både at det finnes et passord (det måtte være `julenissenerteit`) og en algoritme (fra store bokstaver i meldingen, `AES`).
Jeg la inn oppskrift From Base64->AES Decrypt (med passordet) i [CyberChef](https://gchq.github.io/CyberChef/) og fikk ut meldingen «NPST skal endre paa pakkefordelingsruta i aar. Det gir mulighet for aa sabotere. XOXO M. PS Ikke god jul. PS pst{nootnoot}».

Flagg: `pst{nootnoot}`

>Konfidensiell informasjon er lekket! Det er uansett verdifullt for oss å vite om det, så takk for innsatsen. Kan det være vår uvenn Pen Gwyn som bedriver kvalme i år igjen? Uansett, jeg rapporterer dette videre til Julenissen, så blir det nok satt i gang strengere sikkerhetstiltak.
>
>Mellomleder

## Frimerke (8. desember 18.00)

>En av alvebetjentene fant et løst frimerke i postmottaket. Initielle undersøkelser viser at det ikke kan ha sittet på julekortet som kom den 3. desember, da fiberne som sitter igjen i limet ikke er av samme type som julekortet. Fiberne kan minne om setetrekket fra en reinsdyrslede klasse 8.
>
>Motivet på frimerket er av en slik karakter at det må undersøkes nærmere. Kan du ta en titt?
>
>frimerke.png
>
>Mellomleder

Bildet viste en snegle i en slede mot en bakgrunn av noe som liknet på Tetris-figurer.

Jeg lastet opp bildet til Stegonline og fant informasjon i bitplanes Red 0 og Blue 0. Den første viste noe som så ut til å være en operasjon med data fra B0 med S8(«Frimerke\x00...»). I R0 var det kompilert s8-kode for [Slede8](https://slede8.p26e.dev/), som ble mye brukt i CTF-en i 2020, mens bitplane B0 viste deler av en QR-kode. Jeg kjørte s8-koden med hex for «Frimerke» som føde (input) og oppgulp (output) ble en hex-code. Fra B0 i bildet ekstraherte jeg data som input til CyberChef med oppskrift: XOR (output fra s8 som Hex)->Generate Image (Bits, 256 pixels per row)->Parse QR Code.

Flagg: `PST{R3m3mb3r_m3?_W3_h4d_SO_MUCH_FUN_t0g3th3r!_:D}`

>Supert, takk skal du ha! Da var magefølelsen min riktig, her var det noe slimete!
>
>Mellomleder

Også på denne måtte jeg få hjelp en annen deltaker. Jeg trodde jeg skulle bruke bildene til å få fram en QR-kode som kanskje skulle sende meg videre til Slede 8, men jeg fikk hint om å se etter s8-koden og gå videre med den først. Dessuten rotet jeg mye med input og operasjoner i CyberChef og brukte blant annet feil data som input. Jeg trodde jeg kunne bruke View Bit Plane (Blue 0) på `frimerke.png`.
Jeg brukte også mye tid på først å forsøke tolke s8-koden, i stedet for å bare legge den inn direkte. Dessuten fikk jeg problemer med kjøretiden og måtte øke antall sykler via `localStorage.setItem("🚲", <ønsket grense>)` (settes i console i browser).

Oppgaven må ha vært veldig vanskelig for de som evt. ikke deltok i 2020, da Slede 8 ble brukt i stadig mer krevende oppgaver.

## Nettverkstrafikk (9. desember 18.00)

>Hei,
>
>Fikk tilsendt denne filen fra IT-avdelingen i går, de har TAPpet filen ut av nettverket. Har du mulighet til å se på den? Mulig den gir oss litt mer informasjon angående lekkasjen vi hadde ut til SPST. Husk, dette forblir mellom oss, i tilfelle det viser seg å være en av våre egne.
>
>Mvh Mellomleder
>
>📎npst_02_12_21_18_00.pcap

Jeg brukte Wireshark og tcpdump til å se på trafikken, som kun var TCP. De store bokstavene `TAP` viser til [Tap code](https://en.wikipedia.org/wiki/Tap_code) og payload i trafikken kunne dekodes. Her var det mange repeterende meldinger mellom parter, men en melding skilte seg ut, `PST{F'JEG SNACCER MED DEG FRA {SOURCEIP}'}`. Source på denne meldingen var `43.44.45.15`, som etter koden parser til `stue`.

Flagg: `pst{jegsnakkermeddegfrastue}`

> Oj, det var spennende. Takk for hjelpen zigkill!

Jeg visste ikke om Tap code før etter at jeg hadde løst oppgaven, det var dataene som tydet på at det var mulighet for å oversette til tekst, og etter litt testing kom jeg fram til koden. Det var ikke opplagt at sourceip også skulle oversettes.

## Oppdatering av varelageret (10. desember 18.00)

>Alvebetjent Eline har oppgradert varelageret til v2 etter at det ble oppdaget litt muffins i versjon 1. Som en del av videreutviklingen har hun slått sammen v2 med resten av bruker-systemene til NPST, slik at det ikke trengs mange ulike databaser oppe i skyene.
>
>Har du mulighet til å sjekke at alt funker som det skal etter Elines oppgradering?
>
>Varelageret finner du som vanlig her, og bruk programmeringsgrensesnittnøkkel v2_vr7n0p1tf7.
>
>Mvh Mellomleder

Dette var tilsvarende operasjoner som i Digitalt varelager fra 5. desember og her var det SQL-en

`xxx' UNION (SELECT  NULL,cast(b.id as varchar),NULL,NULL,b.passord,NULL FROM v2.brukere b, v2.ting t);-- -`

som listet ut alle passordene. Her var det Elines passord som var flagget.

Flagg: `PST{c3ce11494e56a8897b6f80d1ca3dbe}`

>Oii, det var ikke bra at alle brukerne lå så lett tilgjengelig! Vi skal få fiksa opp i det ASAP.

På denne oppgaven brukte jeg en del tid på å se etter data som skulle peke seg ut på en eller annen måte, og det var først etter gjenlesning av oppgaven der Eline er identifisert at jeg forsøkte med hennes passord.

## Muffens i filsystemet (11. desember 18.00)

>Beklager for å forstyrre deg på en lørdag zigkill, men det haster.
>
>En av terminalene på julenissens kontor har utvist rar oppførsel de siste dagene. AlveCERT har sikret data fra hjemmeområdet, finner du noe muffens?
>
>Mvh Mellomleder
>
>📎sikring.tar.gz

Filen inneholdt et JFFS2-image, og jeg mountet opp dette ved hjelp av informasjonen [her](https://github.com/Dvd848/CTFs/blob/master/2018_35C3_Junior/rare_mount.md). Etter mount fant jeg flere bildefiler og en `flag.txt`, men det var ikke flagget. En `.sys` inneholdt et CramFS-system som jeg fikk pakket ut med `fsck.cramfs --extract=this .sys` og der var det nok en bildefil. Den inneholdt teksten `CFG{WhyrYnzn}` som jeg brukte rot13 på.

Flagg: `PST{JuleLama}`

>Bra jobbet zigkill, takk for hjelpen!

Den første delen av oppgaven gikk ganske greit, men jeg brukte litt tid på å forsøke montere opp CramFS før jeg fant kommandoen for å heller pakke det ut.

## Ugler i grøten (12. desember 18.00)

>God søndag! Det er fanget opp tO krypterte meldinger som ble sendt under lunsjgrøTen i dag. Det vekker mistanke, siden alle alvebetjenter elsker grøt og aldri vil gå gliPp av en lunsjgrøt. Se de krypterte meldingene nederst i mailen. En dyktig alvebetjent har allerede funnet noen biter av klarteksten til melding 1:
>```
>"- - - k r o e l l - - - - - - - - - - - - - - - - - - - - - - - k r o e l l - - - - - - - -"
>```
>og noen biter av klarteksten til melding 2:
>```
>"- - - - - - - - - - - - - - - - p e n g w y n - - a - - o l - n - - - - - - - - - - - - - -"
>```
>Kan du se om du klarer å finne resten av klarteksten til begge meldingene? Legger også ved en tabell over ascii-verdier, kanskje du får bruk for den.
>
>Melding 1:
>```
>00010101 00010100 00010011 00000000 00011101 00000011 00001010 00000010 00011100 00000011 00010101 00011001 00010111 00000001 00010001 00001001 00011111 00010010 00000100 00000000 00001001 00000111 00011010 00000000 00000001 00001110 00000000 00010101 00001011 00011111 00010000 00011000 00000000 00000000 00000000 00000000 00000000 00000000 00000000 00000000 00000000 00000000 00000000 00000000 00000000 00000000
>```
>Melding 2:
>```
>00010110 00001100 00000110 00000111 00001000 00000101 00001101 00001011 00000011 00011000 00011110 00001110 00010110 00001001 00010111 00001101 00011100 00010101 00001111 00010101 00010010 00010111 00011010 00001010 00011110 00000100 00000110 00000111 00001010 00000000 00010000 00000100 00011000 00011001 00000110 00001011 00000010 00001001 00000010 00001000 00011111 00001010 00011100 00010011 00000000 00011101
>```
>📎 ascii.pdf

Meldingsteksten inneholdt OTP i store bokstaver, og jeg antok at det viste til [One-time pad](https://en.wikipedia.org/wiki/One-time_pad), som er sårbare dersom samme kode brukes flere ganger. Her skulle det være mulig å benytte noe som heter Crib Drag (e.g., [denne](https://toolbox.lotusfa.com/crib_drag/)), men jeg løste den for hånd, noe som tok litt tid. Den første meldingen var `pstkroellparentesberlinerkranserkroellparentes` og den andre `skalgibeskjedfrapengwynomatsolenskinnerimorgen`.

Flagg: `pst{berlinerkranser}`

>Ikke dårlig! Det er da strengt tatt ikke nødvendig å kryptere værmeldingen.. Men siden Pen Gwyn ble nevnt, så kan det jo faktisk være noe underfundig på gang. Best å holde øyne og alveører åpne!

## Har du tid? (13. desember 08.00)

>Hei, zigkill!
>
>Jeg vet at du har fri i dag, men om du har tid så kan du gjerne ta en titt på dette.
>
>Vi har gjort observasjoner av to (2) personer med tilknytning til Utlandia på ulike lokasjoner på Vestlandet. Personene oppholdt seg ved flere vannkraftverk i perioden 4-10. november, før de forlot landet.
>
>Basert på våre observasjoner og rapportering fra Etterretningstjenesten er personene trolig agenter fra Utlandia. Det mistenkes at agentene er medvirkende i en sabotasjeoperasjon mot et vannkraftverk i Norge.
>
>Gjennom koordinering gjennomfører Etterretningstjenesten innhenting av informasjon på de utenlandske agentene og deres intensjoner, da dette er utenfor vår jurisdiksjon.
>
>Følg situasjonen videre på deres platform ctf.cybertalent.no.
>
>Rapporter tilbake innhentet informasjon om aktørens planer mot norske mål, dersom du finner noe.

Hviledag. Fra meldingen hintes det sterkt om at det finnes et ekstra flagg på [Cybertalent](ctf.cybertalent.no), men oppgavene der har jeg bare løst noen få av de innledende av. Det ble også bekreftet på Discord at flere har fått flagget etter å ha gjennomført oppgaven.

## Ukens ansatt! (13. desember 18.00)

>Kjære alle sammen,
>
>Takk for enda en uke med strålende prestasjoner!
>
>Denne uken har vi gleden av å berømme Carixo som ukens ansatt!
>
>Vi gratulerer, og takker for den gode jobben.
>
>Ha en fin dag, alle betjenter. :)

Hviledag (fortsatt).

## Reinsdyr på villspor (14. desember 18.00)

>Fire av Julenissens favorittreinsdyr ble sluppet løs fra basen på Svalbard i går. Heldigvis er det sporing på reinsdyrene, så en av alvene i NPST har funnet en datamaskin og lastet ned sporingsdataen. Han klarer dessverre ikke å finne ut hvordan man får tak i GPS-filene.
>
>Kan du hjelpe han?
>
>Nb: Hvis du skulle finne noe mistenkelig i dataen, så rapporter tilbake med hva du fant, omkranset av PST{ og }.
>
>Mvh Mellomleder
>
>📎 sporing.zip

Filen inneholdt en KML-fil som jeg lastet opp til Google Maps. Sporene inneholdt noen små forstyrrelser som kunne minne om morse og jeg leste ut flagget.

Flagg: `pst{runforestrun}`

>Bra jobba zigkill! Julenissen hilser og sier takk for at du reddet reinsdyrene hans.
>
>Mellomleder

## Kameraopptak gir klarhet (15. desember 18.00)

>Etter gårsdagens reinsdyrflukt bestemmer alvebetjent M. Nist seg for å sjekke kameraloggen. Dessverre ser det ut som om det bare eR blått og grØnt støy Der... Klarer du å finne ut noe mer fra opptaket?
>
>Mvh Mellomleder
>
>📎 opptak.gif

Navnet M. Nist viser til [MNIST-databasen](https://en.wikipedia.org/wiki/MNIST_database), som brukes til maskinlæring for tallgjenkjenning. Bokstavene `RØD` i teksten tolket jeg som at jeg skulle finne noe i røde lag i bildet. Bildet var en GIF med 110 bilder som jeg ekstraherte med ImageMagick. I rød kanal framkom i hvert bilde tall fra MNIST-databasen oppe til venstre og jeg oversatte koden fra bildene til bokstaver fra ASCII-tabellen.

Flagg: `PST{HerVarDetIkkeMyeÅSeGitt...}`

>Takk for meldingen zigkill. Bra jobba!

Denne oppgaven klarte jeg ikke uten hjelp. Jeg brukte mye tid på å forsøke fjerne grønt og blått fra bildet (med ImageMagick) og kanskje få et sett av stort sett transparente bilder som skulle kombineres, eller noe slikt, men det var et feilspor, og jeg fikk et hint om å bare se på fargekanelene. Det hadde jeg nok allerede gjort, men uten å legge merke til tegnet oppe til venstre i bilder som stort sett var støy i alle kanaler.

## Ødelagt julesang (16. desember 18.00)

>Alvene på verkstedet klager over dårlig kvalitet på noen av julesangene som spilles over høyttalerne. Særlig denne sangen, "Rudolph, the Red-Nosed Reindeer", har mottatt mange klager. Kan du se om du finner ut hva som er galt?
>
>📎 rudolf.wav
>
>Det spilles et bredt spekter av julesanger på verkstedet, men denne sangen er egentlig en favoritt blant alvene. Da er det jo ekstra synd at lydkvaliteten er dårlig.
>
>Mellomleder

I meldingen var det et hint om spekter. Jeg åpnet filen i [Audacity](https://www.audacityteam.org/) og med visning av spektrogram og tilstrekkelig zoom kunne flagget leses ut i den delen av filen der det var støy.

Flagg: `PST{H4KKIPL4PL4T4}`

>Så flott at du fant ut av det. Da er det kanskje på tide å kjøpe nye plater.
>
>Mellomleder

Selv om oppgaven var ganske enkel, var det bare flaks at jeg så teksten i spekteret. Jeg forsto ikke hintet i oppgaven før etterpå.

## Klokt trasévalg (17. desember 18.00)

>Hei,
>
>nå Er det jo baRe en uke igjen til jul så vi må begynne å få på plass den nye pakkefordelingSruta. avdelingen for optimalisering og ruteplanlegging har jobbet hardt med å finne en trasé, og ga meg i går en Cd Hvor den foreløpige ruten er lagrEt. de fortalte meg at de hadde en baktanke med trasén, men ville ikke fortelle meg høyt hva dette var (i frykt for avlytting), så dette skulle komme frem fra fiLen. jeG sliteR med å tolke hvA de har tenkt. kunne du hjulPet meg?
>
>mvH mellomleder
>
>📎trasé.txt

Meldingen inneholdt `HERSCHELGRAPH` i store bokstaver. Tekstfilen inneholdt koordinater som jeg plottet i Google Maps og fant at hvert punkt lå i en by, 11 stykker totalt.

Oppgaven var åpenbart krevende, og det kom en oppdatering dagen etter:

>Oppdatering angående gårsdagens Mail. En alvebetjent har funnet alle koordinatene på kartet og hentet ut de tilhørende byene. Kan dette være til hjelp?
>
>[-11.725769, -61.778000] = Rolim de moura
>[20.145221,-75.215909] = Guantanamo
>[52.300000,76.95000] = Pavlodar
>[23.101397,88.393575] = Ektapur
>[-34.417148,19.248128]} = Hermanus
>[-15.4825, 128.122778] = Wyndham
>[78.216667,15.633333] = Longerbyen
>[5.041066,7.919476] = Uyo
>[45.424722,-75.695000] = Ottawa
>[21.150000,79.083333] = Nagpu
>{[17.083333,-96.750000] = Oaxaca
>
>Mellomleder

Første bokstav i byene med ROT-4 og miks av bokstavene ga flagget.

Flagg: `PST{SKYRIVAL}`

>Takk zigkill! Sky rival, det er smart. Ingen grunn til å legge trasén forbi Sydpolen.

Denne oppgaven klarte jeg ikke på egenhånd, og jeg løste den først etter hint fra to andre deltakere, og det var først det siste hintet om at forbokstavene på byene skulle danne svaret (noe jeg hadde forsøkt å få til, også med ROT-*n*) som gjorde at jeg klarte å komme fram til det. Jeg vet ikke hva poenget med Herschel-graf er i denne oppgaven og hintet fra dagen etter, hvor byene delvis er gjengitt feil, forsto jeg heller ikke poenget med.

## Grønne firkanter (18. desember 18.00)

>Hei,
>
>Alvdelingen for nettverksoperasjoner har utført en hemmelig nettverksoperasjon mot SPST. De har snublet over et "git repository", men de synes det er noe merksnodig med det. Alv en eller annen grunn så mener Alvdelingen for tekniske undersøkelser at det kan ha noe med "grønne firkanter" å gjøre, hva nå enn det betyr.
>
>Kan du sjekke det ut?
>
>📎groenne-firkanter.zip
>
>Om du trenger hjelp så kunne du kanskje spurt alvdelingen for åpne kilder - de tar sikkert en titt på Github profilen til personen som "comitter" i repoet, kanskje det ligger et hint der.
>
>Mvh
>
>Mellomleder

zip-filen inneholdt et git-repo og på profilen til [underleder](https://github.com/underleder), som var den som hadde commitet alle versjonene, var det et hint (teksten «HINT HINT») i den grafiske framstillingen av bidrag.

![underleders profil](/assets/images/npst-2021/underleder.png)

Tilsvarende plottet commit-historikken i repoet flagget.

Flagg: `pst{get_clean_go_green!}`

>Jasså ja! Det var det de mente med grønne firkanter. Bra jobba!
>
>Mellomleder

Denne oppgaven tok masse tid, da jeg løste også denne *for hånd*. Det var også litt tilfeldig at jeg oppdaget at commit-ene i repoet var samlet på datoer, men til samme tid hver dag.

## ChimneyChopper (19. desember 2021)

>Hei zigkill!
>
>Nissen forsøker å være mer produktiv i år, og unngå å gå ned i feil pipe. For å sørge for spe-serialisert levering har alvene ordnet en helt ny leveransemetode for denne pakkeleveringen.
>
>Nå handler det bare om å finne riktig pipe! Og hva var det han ønsket seg igjen...?
>
>📎Chimney_Chopper.ps1
>
>📎Chimney_Client.ps1

Den vesentlige delen av koden var disse linjene fra Chopper (server):

```
try {
    $Encrypted_Flag = "76492d..."
    $key = [byte[]]($addressLookup[0..15] -join "").ToCharArray()
    $ss = ConvertTo-SecureString \
        -String $Encrypted_Flag \
        -Key $key
    $way = [System.Runtime.InteropServices.Marshal]::SecureStringToGlobalAllocUnicode($ss)
    $decoded = [System.Runtime.InteropServices.Marshal]::PtrToStringUni($way)
    Write-Host "Korrekt adresse funnet! Deploy julegaver " \
        -ForegroundColor Magenta
    Write-Host $decoded \
        -ForegroundColor Yellow
}
```

Jeg endret først en test i klienten slik at skriptet ikke avsluttet og deretter la jeg inn en loop i server som testet alle muligheter (tall) i addressLookup i stedet for den adressen (pid) som ble sendt fra klient:
```
$i = 0
while($i -lt 65536) {
    $i++
    $Loadstring = "$i"
    $addressLookup = \
    (Get-FileHash \
        -InputStream ([IO.MemoryStream]::new([byte[]][char[]]$Loadstring)) \
        -Algorithm SHA384).hash
    try {
```

Flagget ble da skrevet ut.

Flagg: `PST{Nissen_i_pipa}`

>Helt supert, zigkill!
>
>Nå fikk pipen en annen lyd, eller hva? He, he.

Dette var antakelig også en vanskelig oppgave for mange, for dagen etter kom det et hint:

>Hei igjen, zigkill !
>
>Vi har fått ny informasjon som kan kaste lys over pipevalget. Alvene sier at all relevant informasjon er å finne i Chopper, men kanskje du må prøve et par adresser før du får lastet riktig adresse.

I den første kjøringen av server og klient kom det en feilmelding (som står kodet i klienten) med et hint om å lage egen klient, i.e., å endre på klient-koden. Derfor tok det litt tid før jeg la inn brute-force i server-delen. Jeg leste derfor i stedet på de metodene som ble benyttet i skriptene for å se om det kunne være sårbarheter i disse.

## Påminnelse om gjeldende regler (20. desember 11.15)

>Kjære alle alvebetjenter!
>
>Her i NPST verdsetter vi integritet.
>
>Over helgen har noen ansatte valgt å opptre uærlig for å tilegne seg informasjon i form av flagg.
>
>Slik oppførsel gjenspeiles i tjenesten og er ikke i tråd med våre retningslinjer.
>
>Jeg forventer ordentlig oppførsel fra alle ansatte, og det vil få konsekvenser for de som alikevel velger å oppføre seg uærlig.
>
>I ytterste konsekvens mister man nisseklareringen sin.
>
>Minner om at i tillegg til reglene for kveldsarbeidet, så gjelder også alminnelige lover og regler forøvrig.
>
>Med ønske om fortsatt godt samarbeid frem mot jul,
>
>Mellomleder

Hviledag. Det ble varslet på Discord om at noen hadde satt opp en [Cryptobin](https://cryptobin.co/)-klone for å fiske flagg. Jeg har sett på noen av løsningene som har blitt postet på Cryptobin, men tror ikke jeg har vært utsatt for dette.

## Ukens ansatt! (20. desember 18.00)

>Kjære alle alvebetjenter!
>
>Denne uken har vi gleden av å annonsere at Røllik Münch er ukens ansatt!
>
>Vi takker for strålende arbeid, og ser frem til fortsettelsen.
>
>Med ønske om fortsatt god førjulstid,
>
>HR

Hviledag (fortsatt). Røllik var den som varslet om jukset og det var antakelig en bevisst gest av Julenissen å gi en oppmerksomhet om dette.

## Mulig lekkasje (21. desember 18.00)

>NPST's sikkerhetssystemer er satt til øverste beredskap nå som jula nærmer seg, og den ene alvebetjenten oppdaget en melding som noen prøver å skjule. Kan du ta en nærmere titt på denne?
>
>Mvh Mellomleder
>
>brev.txt

Vedlegget `brev.txt` inneholdt `NULLBREDDETEGN` med store bokstaver. Filen inneholdt to tegn med null bredde og ved å sette disse til 0 og 1 fikk jeg ut binærkode som konvertert til bokstaver fra ASCII-tabellen ga flagget.

Flagg: `PST{ReadingBetweenTheLetters}`

>Bra jobba zigkill! Det er viktig at vi fortsetter å stå på siste dagene frem mot jul.

## Mistenkelig rute (22. desember 18.00)

>Hei zigkill,
>
>Som du sikkert er klar over har de ansatte hos oss mulighet til å trene to timer i arbeidstiden i løpet av uken. Dette er et tilbud mange benytter seg av, spesielt etter at vi startet med utlån av GPS klokker til alle ansatte. De mest ivrige tar tar også med seg klokkene hjem i helgene. Ofte er dette ansatte med stor glede av sosiale medier, som liker å dele opplevelser med andre. Vi har spesielt lagt merke til et økt bruk av Instagram i arbeidstid.
>
>Da en oppmerksom alvebetjent tok imot en klokke i går, fant hun en rute hun syns var veldig mistenkelig og rapporterte den inn. Det mistenktes at personen som lånte denne klokka kan ha hatt kontakt med en pingvin vi holder ekstra øye med. Legger ved både rute som ble funnet på klokka og nylige bevegelser gjort av pingvinen. Kan du ta en tit å se om det har skjedd noe mistenkelig?
>
>Mellomleder
>
>📎aktivitet_pingvin.kml 📎klokke_7_18_12_21.kml

Jeg lastet opp KML-filene til Google Maps og så at sporene sammenfalt omtrent ved frølageret på Svalbard. På Instagram fant jeg profilen @chilliwilly1234 og der var flagget i profilbeskrivelsen.

![chilliwilly1234](/assets/images/npst-2021/chilliwilly1234.png)

Flagg: `pst{utpaaturaldrisur123}`

>Takk for hjelpen zigkill, dette var jo veldig mistenkelig.

Det tok litt tid å finne Instagramprofilen, men jeg overså først flagget og holdt også på en stund med analyse av det ene bildet som var postet der.

## Sabotasje (23. desember 18.00)

>Alvene i sledegarasjen rapporterer om at noen har tuklet med julegaveruta som er lagt inn i slede-GPSen. Det er kritisk fordi det ikke er mulig å overstyre sledens GPS-kurs under flyturen. Det har visst blitt lagt til et stopp på Antarktis, rett utenfor SPST sitt hovedkvarter, og jeg (Julenissen) er redd for at SPST planlegger å rappe alle gavene fra sleden på selveste julaften.
>
>I slede-GPS-loggen er det lagt igjen en kort beskjed: "Ikke god jul, hilsen M".
>
>Det er derfor høy prioritet å finne ut hvem "M" er, før "M" klarer å utrette mer ugagn. Mellomleder har skrytt av din innsats denne førjulstiden, så jeg vil derfor betro denne viktige oppgaven til nettopp deg. Jeg personlig har ikke tid, for jeg skal først på gløggsmaking og så skal jeg se Grevinnen og Hovmesteren. Du blir gitt tilgang til kontoret mitt i kveld for å lete gjennom papirer og se om du klarer å finne ut hvem rakkeren er. Navnet rapporteres tilbake til meg (du må selv pakke navnet inn i formatet pst{}).
>
>Dette oppdraget er gradert "Temmelig Hemmelig", så ikke fortell om dine funn til noen andre enn meg personlig.
>
>📎 Julenissens_kontor.png
>
>Hoho, Julenissen

Jeg brukte binwalk til å ekstrahere filer fra png-filen. En av filene var `note_to_elf.txt` som inneholdt hint.

>En alvebetjent kom innom kontoret nettopp, og delte sin hypotese om hvem
som kan stå bak de uheldige hendelsene denne førjulstiden. Jeg skriver det ned
slik at jeg husker det til senere, for nå må jeg straks løpe for å rekke
lunsjgrøten. Alvebetjenten tror at den skyldige har et navn på M, fordi
vedkommende kaller seg for "M". Videre mente alvebetjenten at den skyldige må
være ansatt i NPST, av flere grunner. Først og fremst fordi vedkommende lekket
konfidensiell informasjon om pakkefordelingsruta tidlig i desember. Men også
fordi vedkommende kommuniserte med SPST fra vår stue.
>
>Spørsmålet er da hvorfor en NPST-ansatt vil snu ryggen til julen og samarbeide
med SPST. Alle NPST-ansatte er "snille", og ikke "slemme". Hvis en alv skulle
hoppe over til "slem"-listen, så mister alven umiddelbart alvtorisasjonen og
dermed også jobben. Så hva kan være grunnen til at en "snill" alvebetjent ønsker
å sabotere årets julegavedistribusjon?
Det klarte ingen av oss å svare på.

I filen `snille_og_slemme.pdf` la jeg merke til at kun én av de som var snille og ansatt i NPST som *ikke* hadde mottatt gave i 2020.

Flagg: `PST{Maximilian}`

>Å glitrende julekule, godt jobbet! Endelig har vi funnet rakkeren.
>
>Maximilian innrømmer å ha båret nag over å ikke ha mottatt julegave i fjor, selv om han hadde gjort seg fortjent. Dette naget gikk gradvis over til hemningsløs arghet. Maximilian ville at andre skal føle smerten han har slitt med gjennom det siste året, og ønsket derfor å sabotere årets jul. For å lykkes med dette allierte han seg med agenter hos SPST.
>
>For å hindre denne sabotasjen må vi rette opp i GPS-instillingene, men det får vente til i morgen tidlig kl. 9.
>
>Hoho, Julenissen

## REDD JULA! (24. desember 09.00)

>Selv om vi har funnet den ansvarlige må vi fortsatt fikse opp i ruta som er blitt tukla med, men Julenissen har glemt passordet til slede-GPSen.
>
>Før du kan ta fri må du fikse en siste liten oppgave for Julenissen! Det er å finne ut av passordet til Julenissen med Julenisse-passordgjenopprettings-verktøyet, mens han gjør ferdig de siste forberedelsene til jul! Kanskje det ligger noe info på kontoret hans du kan bruke, eller har du hørt noe nyttig informasjon tidligere?
>
>Det er viktig at du løser dette så fort som mulig slik at vi får reddet julen før det er for sent. Lykke til!
>
>Rapporter tilbake med julenissens passord omkranset av PST{ og }, og bruk gjenopprettingsnøkkel hohoho_god_jul.
>
>Mvh Mellomleder

Jeg løste ikke denne oppgaven og vet fortsatt ikke hvor jeg skal begynne.

## Egg

Det var klart fra poenggivningen at det antakelig kom flagg 10. desember (noen fikk et ekstra poeng i tillegg til de ti poengene som hver oppgave ga), 12. desember (noen hadde to poeng), 14. desember (Cybertalent-lenken), 16. desember (noen hadde nå fire poeng) og 23. desember (hvor jeg kom over flagget selv). Det er ingen som per 25. desember har flere enn fem ekstrapoeng, så jeg antar at det ikke er flere flagg.

### Første egg

I oppgaven for 23. desember så jeg at en av filene som ble ekstrahert, `julekort.png`, hadde en kode i B0: `PST{Egg_`. Jeg ekstraherte data fra R0 («tikk takk tikk takk»), B0 («lang kort lang kort»), R1 («hvor peker klokka mon tro») og G1 («ikke tall men antall streker langs klokka»). Bildet viste to klokker som pekte på 15:05 og 16:06, og i rekkefølge ble det ut fra dataene 5-15-6-20.

Flagg: `PST{EGG_515620}`

>Takk for at du fant egget mitt!
>
>- Juleharen 🐣

### Andre egg

Jeg gikk tilbake til varelageret for å se etter andre flagg og oppdaget da at det i tillegg til logoen på websiden også ble lastet en fil med navn `Logo_egg.jpg`. Denne hadde jeg oversett, men den hadde flagget avbildet.

Flagg: `PST{EGG_StRpiITbqyEsBJM}`

>Takk for at du fant egget mitt!
>
>- Juleharen 🐣

### Øvrige egg

På de øvrige flaggene hadde jeg ingenting, selv om jeg brukte ekstra tid på de dagene for å forsøke finne noe som pekte seg ut.

## Hjelp

Jeg klarte oppgavene 1., 2., 5., 7., 9., 10., 11., 12., 14., 16., 18., 19., 20., 21., 22. og 23. desember og eggene fra 10. og 23. desember uten hint fra andre. På noen av de andre oppgavene var jeg veldig nære løsningen på egenhånd (og hadde delvis rotet meg bort), mens jeg også på noen fikk gode hint som ledet meg til riktig løsning.

## Oppsummering

Dette er den fjerde CTF-en til PST jeg har forsøkt meg på. Den første var påsken 2020, deretter advent 2020 og påske 2021. I hovedsak er oppgavene underholdende og passe vanskelige. I noen tilfeller er det litt vanskelig å finne riktig tilnærming og det er lett å gå seg bort i irrelevant informasjon.