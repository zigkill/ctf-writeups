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

Flagg: ==PST{HelloDASS}==

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

Begge sidene av julekortet inneholdt symboler som jeg fant ut kalles (Pigpen Cipher)[https://en.wikipedia.org/wiki/Pigpen_cipher]. Forsiden hadde fire symboler som stavet ut «PILA» mot klokken. Baksiden av kortet måtte snus opp ned for at cipheret skulle gi mening.

## Egg

## Verktøy

## Hjelp

