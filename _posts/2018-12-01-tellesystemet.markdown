---
title: Tellesystemet (1. desember 2018)
author: Patricia Aas
layout: post
date: 2018-12-01
description:
---

Min foreløpige forståelse

Maskinell stemmetelling i Norge blir gjort av windows maskiner koblet til vanlige dokumentskannere via USB. Det finnes to forskjellige installasjoner av dette systemet, såkalt liten eller stor installasjon. I liten installasjon vil alle deler av systemet kjøre på en PC. I stor installasjon vil dette være et lokalt distribuert system som består av flere maskiner med forskjellige roller (se mer senere). Systemet består av tre deler, alle med brukergrensesnitt, en skanning applikasjon, en verifiserings applikasjon og en “jobbstyrings” applikasjon.

Et valg er definert gjennom et XML dokument som definerer hva denne sentralen skal telle. I en stor installasjon kjøres det flere maskiner med skanning applikasjonen, hver med sin dokumentskanner. Bildene av stemmesedlene sendes ukryptert (mulig det er andre muligheter her) over det lokale nettet til en PC med Microsoft SQL Server, hvor bildene av stemmesedlene blir lagret. Bildene blir så analysert av et Optical Character Recognition (OCR) bibliotek, som fram til 2017 var levert av ReadSoft, et nå kinesisk eid selskap. De bildene biblioteket markerer som tvetydige, blir sendt videre til verifiserings applikasjonen hvor en person skal tyde den. Metadata og bilde blir lagret i databasen. Denne databasen blir så brukt til å lage resultat filen som så blir signert med en Buypass brikke. Brukerne av systemene logger seg på applikasjonene med MinID.

Alle maskinene er koblet til internett, all kommunikasjon over internett blir gjort over https. Ingen sletting av maskiner eller database blir rutinemessig gjort i ettertid, mulig databasen burde lagres etter arkivloven, men ingen gjør det.

Man kan bruke de datamaskinene man har, med de oppdateringer og applikasjoner (evt malware) som de har fra før. Disse og programvaren fra Valgdirektoratet kan settes opp av en av tre godkjente leverandører, en av disse er norske. Man må anta at maskinene og nettverket er mulig å ta seg inn på. Man må anta at man kan komme seg imellom skanner og applikasjon og mellom klient og database. En angrepsvinkel for en fremmed makt ville være å infiltrere en “skanning leverandør”. En annen mulighet er over nett, enten lokalt eller remote. En siste er fysisk tilgang. Disse rommene gjøres klare lang tid i forveien og finnes over hele landet, gjerne i kommune-bygninger. 

Det er også et spørsmål hva som telles. Det ville være en annen angrepsmulighet å lage stemmesedler med ett parti men med strekkoden til et annet. Hvis det er slik at det som avgjør partitilhørighet er en strekkode så ville dette være mulig å gjøre i stemmelokalet. Dette har man foreløpig ikke spurt om.

I liten installasjon så finnes alle disse applikasjonene på samme maskin, og man vil da ikke trenge tilgang til nettet hvis man har fått tilgang til maskinen.

Visstnok kan man ha passord og brukernavn til databasen i klartekst i en fil på disk.
Mye av det over kan være feil, men så lenge man ikke får svar så for man trekke slutninger.
Hvis man har hatt manuell og maskinell telling og disse ikke stemmer overens med hverandre, så har man pleid å telle på nytt med de samme maskinene. Litt under halvparten av alle stemmer ved forrige valg skulle bare telles med maskiner uten noen kontrollmekanismer. 10 dager før valget bestemte KMD at alle måtte telle manuelt minst en gang, men fortsatt finnes ingen rutiner for hvordan man skal reagere og kontrollere hvis tellingene ikke stemmer overens. Vi har ikke greid å få en oversikt over nasjoneal manuell vs maskinell tellings resultat. Valgdirektoratet svarer i media, noe mer til akademia og har nektet å svare på innsynsbegjæringer, som man så har måttet klage på i mange omganger.

Denne holdningen om å ikke svare eller la seg se i kortene, lover ikke godt for valgsikkerhet i Norge.
