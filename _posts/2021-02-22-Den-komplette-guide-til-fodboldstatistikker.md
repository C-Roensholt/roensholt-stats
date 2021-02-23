---
layout: post
published: true
title: Den komplette guide til fodboldstatistikker
subtitle: >-
Statisitkker i fodbold er eksploderet i de seneste år og det er svært at holde styr på dem alle sammen. I dette indlæg vil jeg give et overblik over de avancerede statistikker som bliver brugt i fodbold.
date: '2021-02-22'
readtime: true
---

Fodbold er i de seneste år blevet en 

Jeg vil derfor give et overblik over de forskellige "avancerede" statistikker som er kommet til fodboldverdenen de seneste år. Yderligere vil jeg give kontekst til de forskellige statistikker og hvordan de kan bruges til at analysere og måle præstation for en spiller eller et hold.

# Indhold

1. [Expected Goals (xG)](##Expected-Goals)
2. [Expected Points (xP)](##Expected-Points)2. 
3. [Expected Assist (xA)](##Expected-Assist)
4. [Expected Threat (xT)](##Expected-Threat)
5. [Chance skabende aktioner](##Chance-skabende-aktioner-(SCA-&-GCA))
6. [Skud assist aktioner (SCA)](##Skud-assist-aktioner)
7. [Bold progression](##Bold-progression) 
8. [PPDA](##PPDA)
9. [Possession adjusted tacklinger og erobringer](##Possession-adjusted-tacklinger-og-erobringer)
10. [Revideret tackle procent](##True-Tackle-procent)
11. [Field Tilt](##Field-Tilt)

## Expected Goals

Vi starter med den statistik som har vundet størst indpas i den almene fodboldsnak, Expected Goals (xG).

I den simple form er xG sandsynligheden for at et givet skud bliver til et mål givet omstændighederne omkring skuddet. Faktorer som har indflydelse på omstændighederne er f.eks:

- **Lokationen af skuddet:** Distance til målet og vinklen på skuddet.
- **Modspillernes position:** Hvor mange forsvarsspillere var der mellem bolden og målet? Hvordan stod målmanden placeret?
- **Typen af assist:** Kom skuddet efter en aflevering i dybden, et indlæg eller et frispark osv.
- **Opbygning til målet:** Kom bolden fra en _rebound_? I et etableret opspil mod et dybt stående forsvar eller i et kontraangreb mod et forsvar ude af balance?

Flere tusinde skud er taget i betragtning for at beregne hvor meget hver enkel faktor influerer sandsynligheden for af skuddet bliver til mål. En xG på 0.5 betyder at det forventes at 5 ud af 10 spillere vil score på den chance, mens en xG på 1 indikerer et garanteret mål.
\
Alle udbydere af xG bruger ikke de samme faktorer i deres beregning af xG. Som nævnt i mit tidligere indlæg så er [StatsBomb de første til at lave en xG model som tager højden på skuddet i betragtning](https://statsbomb.com/2020/07/statsbomb-release-expected-goals-with-shot-impact-height/), hvilket er noget som f.eks. Opta's xG model ikke tager hensyn til.

En  udbygning af xG er **Post Shot xG (PSxG)**. PSxG tager udelukkende skud som ender inden for målrammen i betragtning. Alle skud som ikke er inden for målrammen vil have en PSxG på nul, da der er 0% chance for at skuddet til et mål. Det bliver bl.a. brugt når man skal beregne en målmands præstation i forhold til den xG holdet har tilladt imod ham, hvilket jeg har inkluderet [i min analyse af Premier League målmændenes præstationer midt i 2019/2020 sæsonen](http://roensholt-stats.com/2020-02-16-GoalkeepersSoFar-1-af-3/).

**Hvad kan man bruge xG til?**
Man kan bruge xG til at evaluere en spillers skud egenskaber. Ved at summere alle xG for de skud en spiller har haft, kan man se om spilleren scorer flere mål end hans xG indikerer. En spiller med bedre afslutningsevner end det forventede (gennemsnitlige), eller mere held i sine afslutninger, vil score flere mål end hans xG.
\
Et eksempel på dette er illustreret nedenfor hvor jeg har illustreret Danny Ings og Roberto Firmino's skud i Premier League sæsonen 2019/2020.

:![Alt Text](/img/advanced_metrics/Ings_shotMap_1.png) :|: ![Alt Text](/img/advanced_metrics/RobertoFirmino_shotMap_1.png):

Her kan man se hvordan Ings har scoret flere mål end det forventede, mens at Firmino ikke har formået at konvertere hans store chancer til mål. Det kan indikere at Ings har bedre afslutningsevner og/eller bedre held med hans afslutninger end Firmino, som har misset mange skud med høj xG værdi.

I denne forbindelse er det vigtigt at pointere at xG ikke tager hensyn til hvilken spiller der tager skuddet. Hvis Messi og Phil Bardsley stod i samme skudposition vil en xG model tildele den samme sandsynlighed for at skuddet vil blive konverteret til mål. xG tager ligeledes heller ikke hensyn til om det er Alisson eller Adrian som skuddet er imod. Det er illusteret ved at Messi har [overpræsteret xG igennem flere sæsoner](https://www.infogol.net/en/blog/analysis/hit-or-miss-the-most-clinical-finishers-in-europe-142020), hvilket kan tildeles hans afslutningsevner som ligger over gennemsnittet.

![Alt Text](/img/advanced_metrics/Messi_shotMap_4.png)
_I de seneste 4 sæsoner har Messi scoret flere mål end hans xG_

Yderligere kan xG bruges til at indikere hvordan et hold egentlig burde præstere. Her kigger man på forskellen mellem xG for og imod holdet (xG - xG imod). En positiv xG forskel indikerer et hold som laver flere målscorende chancer end sine modstandere, mens en negativ xG forskel indikere et hold som skaber færre målscorende chancer.
Ligesom med spillerne kan man sammenligne et holds egentlige målforskel med xG forskellen. Det kan så fortælle om holdet har haft uheld i deres afslutninger og/eller har afslutningsevner under det gennemsnitlige.

![Alt Text](/img/advanced_metrics/)
*Liverpools gennemsnitlige xG forskel over 10 kampe under Jürgen Klopp. Her ses det at Liverpool generelt har skabt flere målscorende chancer end deres modstandere, men i løbet af 2020/2021 ikke er på samme niveau."*

Det er dog vigtigt at forstå at xG ikke er en ultimativ beregning af om en holds sejr i en specifik kamp var fortjent eller ufortjent. Der er mange faktorer gældende i en enkelt fodboldkamp (held, antal spillere på banen, stillingen af kampen, tid tilbage), så xG skal i højere grad bruges til at måle et holds eller spillers præstation over en række kampe. David Sumpter, som er Professor of Applied Mathematics, har skrevet bogen [Soccermatics](https://www.saxo.com/dk/soccermatics_paperback_9781472924148) og arbejder i den svenske klub Hammerby, har skrevet [dette indlæg](https://soccermatics.medium.com/should-you-write-about-real-goals-or-expected-goals-a-guide-for-journalists-2cf0c7ec6bb6), hvor denne pointe bliver forklaret.

## Expected Points

Man kan yderligere konvertere xG for og imod et hold til expected points (xP). Dette gøres ved at simulere kampen flere tusinde gange, og se hvilket hold der vinder den største andel af disse simulationer, baseret på de chancer (xG) holdene har skabt. Denne metode har vundet indpas i dansk fodbold gennem FC Midtjylland og deres "Table of Justice".

"Table of justice" kan udregnes ved at tage hver enkel kamp og vurdere hver enkelt skud som et møntkast. Skuddet er vægtet afhængig af hvor stor xG chancen er tildelt, og et skud med xG på 0.5 vil være en regulær mønt, som lander krone halvdelen af tiden. Hvorimod det tidligere eksempel på et straffespark med en xG på 0.76, vil lande på krone cirka tre ud af fire gange. Hvis man nu forestiller sig at hvis mønten lander på krone så scorer holdet. Ved at lave et møntkast for hvert skud i kampen, vægtet af skuddets xG værdi, kan man dermed simulere hvor mange mål hvert hold i gennemsnit vil have scoret i kampen.
\
Hvis vi tager 0-2 kampen mellem Atletico Madrid og Levante nedenfor, som er illusteret ved et xG race chart som stiger efter hvert skud afhængigt af skuddets xG værdi. I den kamp skabte Levante skud med xG værdier på 0.4, 0.04, 0.04, 0.13, 0.08 og 0.07, hvilket samlet giver Levante en xG værdi på 0.77 xG. I gennemsnit vil vi dermed ikke forvente at Levante rammer krone, og dermed mål, særligt ofte. På den anden side skabte Atl. Madrid en samlet 2.09 xG for alle deres skud.
\
Kampen bliver spillet og Atl. Madrid og Levante laver et møntkast for hvert af deres skud i kampen, og vinderen af kampen er det hold hvor krone kom op flest gange. Ved at simulere denne "møntkast konkurrence" flere tusinde kan man finde den andel af "møntkast konkurrencer" som hvert hold vinder, og bestemme det hold der har fortjent at vinde kampen baseret på de chancer holdet skabte og deres evne til at holde modstanderen fra chancer.

![Alt Text](/img/advanced_metrics/atl_madrid_levante_xg_flow.png)
*En lige kamp mellem Liverpool og Leicester, som hvis simuleret 1000 gange ville resultere i en uafgjort eller mere lige resultat*

Race chartet mellem Atletico Madrid og Levante viser også at denne metode for at udregne sandsynligheden for at et hold vinder ikke tager hensyn til kampens stilling.
\
Levante skaber nærmest ingen xG efter deres første mål, da de ikke har nogen grund til at satse på offensive aktioner. Derimod står de længere tilbage på banen og tillader Atletico Madrid flere skud og dermed en højere xG for kampen. Hvis Levante ikke havde fået det tidlige mål kunne kampen have set anderledes ud.

Expected points kan altså se udover aktuelle point, scorede og indkasserede mål, og vurdere et holds evner til at skabe chancer der kan føre til mål, og holdets evne til at holde modstanderen fra chancer. Men som nævnt ovenfor er xP ikke en endegyldig måleenhed for holdendes præstation, da xP, ligesom aktuelle point, er influeret af flere faktorer.

## Expected Assist

Vi tager nu et kig på xG's lillesøster, Expected Assist (xA).
\
En assist er den sidste aflevering som fører til et mål. Det betyder at spilleren som spiller afleveringen er afhængig af at angriberen kan konvertere afleveringen til mål. Assist er derfor ikke en endegyldig god indikator af en spillers egenskab til at sætte sine medspillere op til chancer, da assist er direkte afhængig af medspillernes evner til at afslutte.
\
En spiller kan i løbet af en kamp lave flere gode offensive afleveringer, man ingen af dem resultere i mål. Mens en anden spiller laver en får en assist for at lave en aflevering til en spiller som scorer på en meget usandsynlig chance.
\
![Alt Text](/img/advanced_metrics/sterling_miss.gif)
*Sterling brænder en stor chance og Kyle Walker får ikke assisten*

Det kan Expected Assist (xA) være med til at adressere. xA kan blive beregnet på to måder, den første, mest simple og naive metode er at den xG værdi som tilfalder et skud bliver til xA for spilleren med afleveringen til skuddet. Hvis Sterlings skud ovenfor havde en xG værdi på 0.85 vil det svare til at Kyle Walker vil få 0.85 xA for afleveringen. Men hvad nu hvis Sterling havde misset bolden og ikke lavet en afslutningen? Kyle Walkers gode aflevering ville få en xA værdi på 0, hvilket ikke føles rigtigt.
\
Derfor findes der en mere sofistikeret xA model der beregner sandsynligheden for at hver afleveringen vil resultere i en assist. Denne model kigger, ligesom xG modellen, på faktorer omkring afleveringen, f.eks. afleverings lokation, modspillere aflevering passerer, osv. Dvs. altså sige at alle afleveringer som bliver lavet i en kamp har en xA værdi associeret med sig. Det betyder at Sergio Busquets assist nedenfor ikke vil have en høj xA værdi, da hans aflevering ikke har en stor chance for at resultere i et mål. På den anden side vil Mané's aflevering, som skærer forsvaret åbent, have en høj xA værdi. Shaqiri kommer i en position hvor han vil have en stor chance for at score, og afleveringen har derfor en høj xA værdi associeret ved sig. Hvis Shaqiri havde afleveret bolden på tværs til Salah, som så havde scoret, ville Mané stadigvæk ifølge denne model få tildelt samme xA værdi. Hvilket ikke ville have været tilfældet i den simple og naive xA model.

Mané assist  | Sergio Busquets assist
:-----------:|:-------------------:
![Alt Text](/img/advanced_metrics/mane_assist.gif) | ![Alt Text](https://i.imgur.com/BzyPDZX.gif)

xA kan visualiseres og bruges til analyse hvor et hold eller spiller skaber sine målfarlige chancer fra, hvilket Benoit Pimpaud har gjort i [denne gode artikel](https://medium.com/nightingale/beyond-the-goal-visualizing-expected-assists-in-soccer-28df81dafe09).

## Expected Threat

(Hvis Özil co-assist)

## Chance skabende aktioner (SCA & GCA)

Der er flere forskellige avancerede modeller, f.eks. xT og xA, til at kvantificere spillernes evner til at skabe målscorende chancer. En mere simpel metode er at kigge på aktioner som fører til mål assisterende - og skud assisterende aktioner.
\
Denne metode tager et skridt tilbage fra xT og xA, og vurderer de to offensive aktioner som leder til hendholdsvis et skud eller mål.

## Bold progression

Fremadrettede afleveringer og 






## PPDA

(Hvis tabel af PPDA med Leeds top)


## Possession adjusted tacklinger og erobringer

(Hvis revised tabel)


## True tackle procent

## Field Tilt

## Kontekstualisering af statistikker

Det vigtigste med statistikker er at sætte dem i kontekst

Jeg bestræber mig meget på det, men endelig "call me out" hvis jeg ikke efterfølger mine egne principper.


