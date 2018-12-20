---
title: Svar på spørsmål om EVA Skanning (Svar på mail)
author: Valgdirektoratet
layout: post
date: 2018-12-20
description: Svar på henvendelse om EVA Skanning
image: "/images/norway-2144066_640.jpg"
image_alt: Norway Coast Mountain Scandinavia Sea Landscape
---

Det følgende er sitat fra [dette svaret](/docs/2018-12-20-HenvendelseOmEVASkanning-Valgdir.pdf) fra Valgdirektoratet (utheving er lagt til)

"Spørsmål og svar:
1) Fantes det i 2017 et oppsett av stor installasjon som innebar at brukernavn og passord til SQL
Serveren ble lagret i klartekst på disk?

Oppsettet av EVA Skanning ble gjort av kommuner og fylkeskommuner med eller uten bistand fra
skanningleverandørene. Valgdirektoratet har inngått en rammeavtale med leverandørene av teknisk
bistand på vegne av landets kommuner og fylkeskommuner, og disse velger selv om de benytter denne
type bistand. Valgdirektoratet har ikke en fullstendig oversikt over konfigurasjonene som er gjort i
fylkeskommunene og kommunene. __Installasjonsveiledningen beskriver kort kryptering av passord ved
hjelp av Integrated Security/Active Directory.
Til valgene i 2019 vil brukernavn og passord være kryptert i standardoppsett ved hjelp av Data
protection API (innebygget i Windows).__

2) Stemmer det at kommunikasjonen mellom maskinene i stor installasjon ikke er kryptert?

Som nevnt i svaret over, ble oppsettet av EVA Skanning gjort av kommuner og fylkeskommuner. Noen
benyttet bistand fra ekstern leverandør. Valgdirektoratet har ikke en fullstendig oversikt over
konfigurasjonene som er gjort i fylkeskommunene og kommunene.
Det som sendes fra klienten til databasen (Microsoft SQL Server) er stemmeseddelbilder og metadata
over TCP/IP eller «named pipes» avhengig av oppsettet gjennom «stored procedures». Dette er
standardiserte og etablerte protokoller som direktoratet benytter. __Selv om direktoratet ikke har noen
instruksjonsrett overfor kommuner og fylkeskommuner, anbefaler vi brukerne av EVA Skanning å
kryptere denne kommunikasjonen ved TLS og sertifikat.__

3) Stemmer det at parti tolkes ut ifra stemmeseddel nummeret og ikke teksten på stemmeseddelen?

__Fram til nå har det vært slik at identifisering av parti skjer ved hjelp av stemmeseddelnummeret på
seddelen. Til valgene i 2019 vil også tekstfelt for partinavn leses og kontrolleres.__

4) Stemmer det at det er metadataen i databasen som er grunnlaget for tellingen og ikke bildene?

Ved skanning vil bildene tolkes og metadata utledes. Bilder og metadata sendes så til databasen som
grunnlag for telling.

5) Stemmer det at det ikke finnes noen nasjonal arkivering av disse databasene?

__Det finnes ingen nasjonal arkivering av databasene fra valgene i Norge.__ Det er kommunene og
fylkeskommunene som eier dataene, og Valgdirektoratet kan ikke sette noe krav til at kommuner og fylkeskommuner skal ta vare på databasen for EVA Skanning etter valget. Vi anbefaler kommunene og
fylkeskommunene å ta vare på dataene fra valget med backup av MSSQL- databasen. Kommunene er
forpliktet til å ta vare på de fysiske stemmesedlene i fire år.

6) Stemmer det at det ikke finnes noen revisjon av om metadata og bilde i databasene stemmer
overens?

Det finnes ingen generell revisjon av om bilder og metadata stemmer overens i databasen.
Det finnes imidlertid en revisjonsmekanisme i skanningprosessen som alltid vil føre til at et antall sedler
inspiseres av mennesker. __I de tilfeller en stemmeseddel er endret og endringen ikke kan tolkes entydig
av maskinen, vil disse være gjenstand for menneskelig verifisering. Et avvik mellom metadata og bilde
vil da bli oppdaget for disse sedlene.__

7) Finnes det noen prosedyre for å passe på at maskinene har de aller siste patcher på valgdagen?

__Sikkerhetsveilederne inneholder en anbefaling om å oppdatere programvare, men det er kommunens og
fylkeskommunenes ansvar å utforme en prosedyre som sikrer at de alltid har siste versjon av
programvare.__

8) Har dere noen statistikk fra valget i 2017 over forskjeller mellom manuell og maskinell telling -
for hele landet?

__Informasjon om foreløpig og endelig opptelling vil framkomme i den enkelte kommunes protokoller fra
valget.__

9) Vil dere utføre fysisk penetrasjonstest av en installasjon av EVA Skanning før valget i 2019?

__Ja, vi planlegger å gjennomføre penetrasjonstester før valget i 2019.__

10) Har dere utført noen fysisk inntrengningstest (ved bruk av social engineering mv) av en EVA
Skanning tellesentral?

__NSM gjennomførte i juni en sikkerhetstest av EVA Skanning installert hos en av landets kommuner
med påfølgende avviksrapportering.__

11) Vil dere tillate sikkerhetsforskere å undersøke et oppsett av EVA Skanning slik det ble brukt i
2017 og slik det vil bli brukt i 2019?

Vi har tett samarbeid med andre myndighet som utfører sikkerhetstester, og som gir anbefalinger til
konkrete tiltak for å gjøre den til enhver tid gjeldene versjon av løsningen enda sikrere.
__Det er utført koderevisjon av en ekstern aktør med fokus på å avdekke kvalitets- og
sikkerhetsutfordringer.__ Revisjonen peker på aktuelle tiltak som sikrer løsningen ytterligere, og som gir
et system som er godt rustet.

12) Når vil dere slippe koden som ble brukt i 2017 som Bjørn Berg lovet på NRK at skulle slippes i
August 2017?

Vi vil publisere systemdokumentasjon og kildekode for valgsystemene i 2019 når systemene går i
produksjon (januar, april og juni). __Vi vil i forbindelse med dette også vurdere om vi skal publisere
kildekoden fra 2017.__

13) Vil dere anskaffe en person eller team til å være liaison mellom sikkerhets researchere og
valgdirektoratet?

__Det er ikke noen sikkerhets-liason mellom offentligheten og Valgdirektoratet.__ For å komme i kontakt med sikkerhetsteamet, besøk vår nettside der dette er beskrevet: https://valg.no/.well-known/security.txt. Man vil naturlig nok også bli sendt til rett sted om man tar kontakt med oss gjennom vårt postmottak (post@valg.no)."