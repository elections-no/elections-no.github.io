---
title: Tilsvar til Valgdir
author: Patricia Aas
layout: post
date: 2017-08-09
description:
image: "/images/norway-island-2075451_640.jpg"
image_alt: Norway Island Rocky Sunset Lighthouse Architecture
---

I VG 8. august svarer Bjørn Berg, direktør Valgdirektoratet, på min kronikk (29. juli, VG). Min kronikk inneholdt en rekke spørsmål rundt IT sikkerheten i norske valg, spesielt rundt telling av stemmer. Disse ble til en viss grad besvart av Berg, og de som er interesserte kan finne både spørsmålene mine og svaret hans på profilen min på Twitter. I stedet for å gå igjennom svaret til Berg vil jeg prøve å illustrere hvorfor jeg stilte disse spørsmålene, og hvorfor de ikke bør avfeies med “gode ord”.

Hans beskrivelse av tellingen gir meg følgende inntrykk: PCene hvor “telleprogrammet” kjører er “private”, koblet til internett og ikke under kontroll av Valgdirektoratet. En valgmedarbeider laster ned et program til en PC og kobler til en skanner.

Jeg skal beskrive en angrepsarkitektur mot et slikt system, ikke nødvendigvis den optimale arkitekturen (og kanskje litt vel ambisiøs), men den gir et høynivå inntrykk av hvordan noe slikt kan se ut. Det er rimelig å anta at jeg har store ressurser og jobber for en fremmed makt eller et pengesterkt privat selskap. Det jeg ønsker er å manipulere valgresultatet til min fordel, uten at det oppdages. Jeg skal prøve å gjøre dette ved å angripe PCene som teller stemmesedlene.

Arkitekturen vil ligne på et såkalt “botnet”, siden jeg gjerne vil fjernstyre dette. For å få dette til, er det en del forskjellige biter som må på plass: jeg må ha kontrollservere for å styre nettet mitt, en måte å distribuere koden, en måte å få den til å kjøre på PCene og jeg må lage koden som skal manipulere tellingen. De fleste av disse bitene er “hyllevare” for Windows PCer, enda greiere hvis maskinene ikke har blitt oppdatert nylig. Hvis jeg ikke har det jeg trenger, så kan de fleste av disse tingene kjøpes av både private selskaper og kriminelle på nettet.

Jeg ønsker meg en effektiv spredning, gjerne ved bruk av kjente Windows sårbarheter og helst noe liknende WannaCry (ransomware) sin spredning i våres. For selve manipuleringen av tellingen er jeg inspirert av Jon Lech Johansen (“DVD-Jon”) og vil prøve å bytte ut bildet som sendes fra skanneren til det bildet jeg ønsker. Siden dette er stemmesedler, og hvordan de ser ut er begrenset, så burde dette være greit å få til. PCene antas å være standard Windows maskiner og skannere, så dette kan jeg utvikle i fred og ro på kontoret. Fordelene er at jeg bare trenger å angripe maskinen i tellelokalet og kan bruke kjente sårbarheter. Jeg ønsker å gjøre et angrep på flere maskiner, helst over nettet, kanskje strategisk utvalgte eller kanskje jeg vil prøve å infisere så mange som mulig.

Dette er et litt overambisiøst prosjekt, og det kan godt hende at rutinene i Valgdirektoratet kunne ha avverget akkurat dette angrepet. Det som er poenget mitt er at denne problemstillingen ikke kan avfeies med betryggende ord. Datasystemer som avgjør valg må behandles som andre samfunnskritiske systemer, og runde formuleringer gir ikke trygghet. Dette er 2017 og storpolitikk involverer å distribuere malware.

(Lagt ut på Medium 29. August 2017)