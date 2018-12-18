---
title: Høringssvar til KMD forslag til endringer i Valgforskriften
author: M.Sc. Patricia Aas, TurtleSec
layout: post
date: 2018-12-13
description: Høringsvar fra TurtleSec
image: "/images/opera-3838030_640.jpg"
image_alt: Opera Oslo Architecture Norway Building Visitoslo
---
## Bakgrunn
Høsten og sensommeren 2017 skrev jeg på Twitter, i aviser og senere snakket på TV og radio om valgsikkerhet. Denne interessen har jeg hatt siden jeg i 2005 skrev masteroppgave i informatikk om valgsystemet i Norge. Et “valgsystem” er et bredt begrep og favner alt som gjøres under et valg, alt fra manuelle til maskinelle prosesser og kontrollmekanismer. I denne høringsuttalelsen vil jeg snakke mest om de delene av valgsystemet i Norge som omhandler telling av stemmesedler.

## Valgsikkerhet
Valgsikkerhet er et overraskende komplekst område innenfor sikkerhet, likevel er det et område som har vokst fram under et kontinuerlig trusselbilde over mange hundre år, lenge før vi introduserte datamaskiner. Det kan høres selvfølgelig ut, men målet i alle valgsystemer er å sikre at valgresultatet er riktig. Valgresultatet skal reflektere det folket har stemt. Dette utsagnet kan igjen virke utrolig naivt, men det definerer noen grenser som er viktige; målet er ikke at alt skal være feilfritt, målet er at eventuelle feil enten ikke påvirker resultatet eller blir oppdaget. 

## Oppdage feil
Å oppdage feil og/eller valgfusk er helt sentralt i et valgsystem, for hvis man oppdager feil/valgfusk som har påvirket valgresultatet, så har valgsystemet mulighet til å rette dette opp: slike muligheter inkluderer alt fra lokale og nasjonale omtellinger helt til annullering av valget. Disse mekanismene utløses bare hvis man kan påvise feil/fusk som er på en slik skala at resultatet kan ha blitt påvirket.

Denne påvisningen er helt sentral, man må oppdage feil og fusk, og man må evaluere hvorvidt hendelsen er av betydning for valgresultatet. Altså, det er ikke nødvendig at man har null feil, det er nødvendig at man oppdager feil. For å kunne gjøre dette må man ha kontrollmekanismer på plass.

Her kommer dette forslaget om endring i forskriften inn, som jeg støtter:

> Forslaget er: § 37a Foreløpig opptelling av stemmesedler (1) Den foreløpige opptellingen av stemmesedler etter valgloven § 10-4 femte ledd og § 10-5 skal skje ved manuell telling.

Jeg skal begrunne dette gjennom et scenarie. Anta følgende metode, i valglokalet går frivillige sammen i par eller grupper, og sorterer stemmesedler etter parti. Hver bunke vil inneholde (innenfor en viss risikomargin) bare stemmesedler for ett parti. Hver bunke telles deretter og antall stemmesedler skrives ned og sendes med bunken. I det sentrale “tellesenteret” vil en slik bunke sendes gjennom en skanner, et dataprogram, over et nettverk og videre til en database. Alle disse leddene kan ha feil og kan inneholde skadevare som kan prøve å endre valgresultatet. Poenget er at så lenge maskinen kommer fram til det samme tallet som man kom fram til i valglokalet, så er det unødvendig å bekymre seg over sikkerheten i dette IT-systemet. Tallene stemte. Problemet oppstår bare hvis tallene ikke stemmer.

Her kommer et annet forslag til endring i forskriften inn, som i min mening gir lite hjelp til å løse dette problemet:

> Forslag til ny § 37a (2) er: Ved avvik mellom en foreløpig og en endelig opptelling som er foretatt maskinelt, skal opptelling foretas på nytt. Ny maskinell opptelling kan
ikke foretas av de samme personer som foretok endelig opptelling første gang.

Gitt at man gjorde det over, men tallet fra maskinen og tallet på lappen som fulgte med bunken stemmer ikke overens. Hvordan skal man løse dette? Her er det viktig å tenke over risikomodellen og trusselmodellen som valgsystemer er bygd på.

## Evaluering av sikkerheten til manuell telling
Manuell telling er distribuert, gjøres av mange vanlige borgere og gjøres i felleskap med andre. Dette er gjort for å beskytte mot valgfusk. For å kunne begå valgfusk i et slikt system så er man nødt til å ha en konspirasjon, og en stor konspirasjon. Mange mennesker på mange steder må samarbeide for å kunne greie å bevege valgresultatet. Dette er helt sentralt. Målsetningen til valgsikkerhet handler om å sikre at valgresultatet er riktig, ikke at prosessen var feilfri. En slik massiv konspirasjon, som involverer dusinvis, kanskje hundrevis av mennesker er vanskelig å skjule. Spesielt siden den må foregå i valglokalene, der mange andre mennesker også oppholder seg. I valgsikkerhet antar man at en slik konspirasjon har høy risiko for å bli oppdaget og man er da kan bruke de midlene man har til å korrigere valgresultatet, for eksempel omtelling eller omvalg.

Videre kan vi se på feil, rett og slett tellefeil. Det er ikke nødvendig å anta, tellefeil vil forekomme i en manuell telling. Det er da viktig å se på tellefeil som vesensforskjellig fra valgfusk, ved uskyldig tellefeil prøver ingen bevisst å endre valgresultatet. Når vi da ser på tellefeil, så vil de distribuere seg over alle partiene. Dette kan vi illustrere best gjennom denne modellen: Anta at av 1000 stemmer talt pleier det å være et avvik på 5, dette er uavhengig av parti for dette er uskyldige tellefeil. Disse feilene vil skalere med parti, slik at man prosent-/promille-messig vil rammes like hardt om man er et lite eller stort parti. Rent antallsmessig så vil store partier ha flere feil og små partier ha få, bare fordi antall stemmer er forskjellig. I valgsikkerhet antar man ofte at dette ikke vil medvirke til å betydelig endre resultatet, fordi feilene distribuerer seg proporsjonalt over alle partiene. 

Det finnes et unntak her, og det gjelder små marginer. Ved små marginer (eksempelvis utjevningsmandater eller partier på sperregrensen) kan feilmarginer som vanligvis ville være uproblematiske, bli veldig viktige. I disse tilfellene pleier man ofte å anbefale lokal manuell omtelling. Lovgivning på dette området varierer stort fra land til land.

Summert så anser man at rene manuelle tellefeil vil distribuere seg over partier og vil vanligvis ikke påvirke valgresultatet, unntak er i situasjoner med små marginer.

## Evaluering av sikkerheten til maskinell telling
Når det gjelder maskinell opptelling er risikomodellen helt annerledes, og dette er utrolig viktig å forstå. Selv uskyldige feil i programvare eller oppsett, selv feil under trykking av stemmesedler, kan ha store konsekvenser. Datamaskiner er ikke ufeilbarlige, og selv i Norge har vi hatt flere feilsituasjoner på valgdagen med skanning systemer. Det er to ting som er viktig når man evaluerer risikoen ved maskinell opptelling:

Ett system: Disse systemene installeres sentralt og deles av mange valglokaler, det betyr at feil eller fusk her vil påvirke veldig mange stemmer.
Umulig å verifisere: Det finnes ingen måte for vanlige mennesker å sjekke hva som skjer inne i datamaskinene eller i nettverket

Ved manuell telling sjekkes tellingen kontinuerlig av de andre som teller med deg, ved maskinell telling har man ingen slik sjekk. I tillegg er det stor mulighet for å påvirke valgresultatet, på grunn av mengden med stemmer.

Tilbake til scenariet, vi står nå med en bunke som i følge lappen skal inneholde 1000 Høyre stemmer, maskinen sier at det er 998, hva kan man gjøre?

En ting som har blitt gjort er å veie bunken, man vet ganske nøyaktig hva en viss mengde med stemmesedler veier, og siden både maskinell og manuell telling er enige om parti, så kan dette gi en bekreftelse den ene eller andre veien.

Det som er sentralt er å ikke stole på maskinen. Man må ha en uavhengig måte å sjekke resultatet. I løpet av det siste året har jeg vært veileder for en student ved NTNU,  Vilde Amundsen, som skriver sin masteroppgave ved Institutt for informasjonssikkerhet og kommunikasjonsteknologi om å oppdage og korrigere feiltelling i valg. Hun fremlegger et forslag om å bruke en teknikk fra valgsikkerhet som heter Risk Limiting Audits. Denne setter stikkprøvekontroll i et statistisk system hvor man tar nok stikkprøver til at man klarer å statistisk bekrefte valgresultatet, disse stikkprøvene telles manuelt. Dette kan innebære at man må ta flere og flere stikkprøver, hvis man ikke klarer å bekrefte resultatet, og kan i siste instans føre til en full manuell omtelling.

Datamaskiner, programvare og nettverk kan ha feil og kan manipuleres til å gjøre feil. Siden disse systemene er sentralt plassert og den samme programvaren er distribuert over hele landet, så vil selv små feil kunne bevege valgresultatet, uavhengig av om feilene har blitt gjort med vilje eller ei. Dette gjør at risikomodellen for disse er vesensforskjellig fra manuell telling og kan ikke egentlig sammenlignes.

Hvis man bruker datamaskinener til å gjøre dobbeltsjekking og omtelling, så vil det manuelle resultatet i stor grad miste sin verdi. Innen valgsikkerhet, som beskrevet over, så anser man et manuelt resultat som sikrere enn et maskinelt, selv om det manuelle inneholder uskyldige tellefeil.

## Konklusjon
Å forhindre feil er ikke hovedfunksjonen til et valgsystem, og derfor ikke primæroppgaven til valgsikkerhet. Valgsystemer, altså hele prosessen man har for å foreta valg, har blitt utviklet over hundrevis av år for å oppdage feil og fusk som kan påvirke valgresultatet. Hvis man oppdager noe slikt, så kan man ta i bruk de lovmessige verktøyene man har for å forhindre at noen kommer til makten som ikke har blitt stemt inn.

Min anbefaling er å bruke andre verktøy en datamaskiner for å finne ut av uoverensstemmelser mellom manuelt og maskinelt resultat. Blant disse verktøyene er å sortere og sende stemmesedler sortert på parti, veie bunker, Risk Limiting Audits og manuell omtelling av en bunke.

Mer generelt er det nødvendig å åpne opp datasystemer som blir brukt i valg i Norge for at vi som borgere skal ha muligheten til i en viss grad å undersøke disse. Allikevel vil innsyn aldri bli nok, vi kan ikke vite hva som skjer inne i datamaskinen på valgdagen, vi er nødt til å ha andre kontrollmekanismer.

[Høringssvar](https://www.regjeringen.no/no/dokumenter/horing---endringer-i-valgforskriften-og-forskrift-om-direkte-valg-til-kommunedelsutvalg/id2617660/?uid=957f57af-ec17-4eda-a860-3d4eae73a75c)