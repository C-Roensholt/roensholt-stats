---
layout: post
published: true
title: Guide til fodboldstatistikker
subtitle: >-
    Statistikker i fodbold er eksploderet i de seneste år og det er svært at holde styr på dem. I dette indlæg vil jeg give et overblik over de nye statistikker som bliver brugt i dag.
date: '2021-02-22'
readtime: true
thumbnail-img: /img/advanced_metrics/thumbnail.png
---

Jeg vil give et overblik over de forskellige de nye, mere avancerede, statistikker som er kommet til fodboldverdenen i de seneste år. Yderligere vil jeg give kontekst til de forskellige statistikker og hvordan de kan bruges til at analysere spillere eller hold.

## Kontekstualisering af statistikker

Det vigtigste med statistikker er at sætte dem i kontekst. _"Tallene lyver aldrig"_ er en velkendt formulering, hvilket er rigtigt. Men nogle gange fortæller de ikke den fulde sandhed.
\
Glenn Murray lavede f.eks. 14 mål i 27 kampe for Brighton i 2018, mens at Karim Benzema lavede 12 mål i 37 for Real Madrid. Dette fortæller os dog ikke hvem der er den bedste angriber af dem to. Der er mange faktorer som spiller ind på en angribers antal mål, minutter spillet, styrken af modstanderne, holdets taktik, osv. Det er derfor utrolig vigtigt at give det fulde billede når man udlægger statistikker og nogle gange er den bedste statistik øjnene som ser kampen.

_Det er vigtigt at pointere at introduktionen af de nye mere avancerede statistikker ikke betyder at de mere brugte statistikker, som f.eks. skud på mål, antal afleveringer, osv., ikke kan bruges længere. De nye statistikker giver ikke den endegyldige analyse af spillerens eller holdets præstation. De er udelukkende introducerede i et forsøg på at forbedre og give et mere komplet billede af fortællingen om spilleren, holdet eller kampen._

# Indhold

1. Expected Goals (xG)
2. Expected Points (xP)
3. Expected Assist (xA)
4. PPDA
5. Possession adjusted defensive aktioner
6. Field Tilt

## Expected Goals (xG)

Expected Goals (xG) ses af mange som starten dataens indtog i fodbold efter at [Sam Green introducerede konceptet i en artikel i 2012](https://www.statsperform.com/resource/expected-goals-in-context/). Det er ligeledes den nymoderne fodboldstatistik som her vundet størst indpas i den almene fodboldsnak.

I den simple form er xG sandsynligheden for at et skud bliver til et mål givet omstændighederne omkring skuddet. Faktorer som har indflydelse på omstændighederne er f.eks:

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

Danny Ings   | Roberto Firmino
:-----------:|:-------------------:
![Alt Text](/img/advanced_metrics/Ings_shotMap_1.png) | ![Alt Text](/img/advanced_metrics/Firmino_shotMap_1.png)

Her kan man se hvordan Ings har scoret flere mål end det forventede, mens at Firmino ikke har formået at konvertere hans store chancer til mål. Det kan indikere at Ings har bedre afslutningsevner og/eller bedre held med hans afslutninger end Firmino, som har misset mange skud med høj xG værdi.

I denne forbindelse er det vigtigt at pointere at xG ikke tager hensyn til hvilken spiller der tager skuddet. Hvis Messi og Phil Bardsley stod i samme skudposition vil en xG model tildele den samme sandsynlighed for at skuddet vil blive konverteret til mål. xG tager ligeledes heller ikke hensyn til om det er Alisson eller Adrian som skuddet er imod. Det er illusteret ved at Messi har [overpræsteret xG igennem flere sæsoner](https://www.infogol.net/en/blog/analysis/hit-or-miss-the-most-clinical-finishers-in-europe-142020), hvilket kan tildeles hans afslutningsevner som ligger over gennemsnittet.

![Alt Text](/img/advanced_metrics/Messi_shotMap_4.png)
_I de seneste 4 sæsoner har Messi scoret flere mål end hans xG_

Mange mener at dette skal kunne inkluderes i en xG model, men det, ifølge mig, er ikke meningen med xG. xG estimere ud fra tusindvis datapunkter sandsynligheden for at _enhver_ spiller vil score fra den givne position i de givne omstændigheder. Hvis en spiller, som f.eks. Messi, er en ekstraordinær afslutter og overpræsterer xG er det helt fint, da det fortæller os noget spillerens evner og ikke manglerne af vores model. Spillernes og holdenes evner er i sidste evne det vi vil blive klogere på.


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

Vi tager nu et kig på xG's lillesøster, [Expected Assist (xA).](https://www.statsperform.com/resource/expected-assists-in-context-2/)
\
En assist er den sidste aflevering som fører til et mål. Det betyder at spilleren som spiller afleveringen er afhængig af at angriberen kan konvertere afleveringen til mål. Assist er derfor ikke en endegyldig god indikator af en spillers egenskab til at sætte sine medspillere op til chancer, da assist er direkte afhængig af medspillernes evner til at afslutte.
\
En spiller kan i løbet af en kamp lave flere gode offensive afleveringer, hvor ingen af dem resulterer i mål. Mens en anden spiller får en assist ved at lave en aflevering til en medspiller som dribler fra midten, som f.eks. Messi eller Maradona.

Det kan Expected Assist (xA) være med til at adressere. xA kan blive beregnet på to måder, den første, mest simple og naive metode, er at den xG værdi som tilfalder skuddet bliver til xA for spilleren med afleveringen til skuddet. F.eks. hvis Sterlings skud nedenfor havde en xG værdi på 0.85 vil det svare til at Kyle Walker vil få 0.85 xA for afleveringen. Men hvad nu hvis Sterling havde misset bolden og ikke lavet en afslutningen? Kyle Walkers gode aflevering ville dermed få en xA værdi på 0, som ikke virker rigtigt.

![Alt Text](/img/advanced_metrics/sterling_miss.gif)
*Sterling brænder en stor chance og Kyle Walker får ikke assisten*

Derfor findes der en mere sofistikeret xA model. Denne model beregner sandsynligheden for at enhver aflevering vil resultere i en assist. I xA er, ligesom xG modellen, inkluderet omstændighederne omkring afleveringen, afleverings lokation, antal modspillere afleveringen passerer, osv. Alle afleveringer som bliver lavet i en kamp har dermed en xA værdi associeret med sig. Det betyder at Sergio Busquets assist nedenfor ikke vil have en høj xA værdi, da hans aflevering ikke har en stor chance for at resultere i et mål. På den anden side vil Mané's aflevering, som skærer forsvaret åbent, have en høj xA værdi. 
\
Shaqiri kommer i en position hvor han vil have en stor chance for at score, og afleveringen har derfor en høj xA værdi. Hvis Shaqiri havde afleveret bolden på tværs til Salah, som så havde scoret, ville Mané stadigvæk ifølge denne model få tildelt samme xA værdi. Det ville ikke være tilfældet i den simple og naive xA model.

Mané assist  | Sergio Busquets assist
:-----------:|:-------------------:
![Alt Text](/img/advanced_metrics/mane_assist.gif) | ![Alt Text](https://i.imgur.com/BzyPDZX.gif)

xA kan dermed være med til at evaluere kreative spillere på et bedre grundlag, hvor de ikke er afhængige af deres medspilleres afslutningsevner. Det ses f.eks. ved at Rodrigo de Paul har akkumuleret 7,77 xA, hvilket er mest i Serie A efter 23. spillerrunde, men kun har lavet to assist, hvilket er uden for top 50 for assist i ligaen.
\
xA kan visualiseres og bruges til analyse hvor et hold eller spiller skaber sine målfarlige chancer fra, hvilket Benoit Pimpaud har gjort i [denne artikel](https://medium.com/nightingale/beyond-the-goal-visualizing-expected-assists-in-soccer-28df81dafe09).

## PPDA

Presspillet er blevet en stor del af fodbold i de seneste år. PPDA (Passes Allowed Per Defensive Action) gør det muligt at måle et holds presintensiet, og dermed sammenligne intensiteten af presset mellem hold. Konceptet blev introduceret af Colin Trainor i [denne StatsBomb artikel](https://statsbomb.com/2014/07/defensive-metrics-measuring-the-intensity-of-a-high-press/)

PPDA for et hold er defineret ved: PPDA = Antal af afleveringer af modstanderholdet / Antal af defensive aktioner.
\
De defensive aktioner inkluderer:
- Tacklinger (både tabte og vundne)
- Erobringer
- Blokeringer
- Begået frispark

Både antallet af afleveringer og defensive aktioner bliver målt på modstandernes sidste 60% af banen. Det er en meget vigtig observation ved PPDA, som nogle gange ikke bliver kommunikeret ordentligt. Denne observation følger godt logikken, da presintensiteten vil stige eksponentielt når modstanderholdet kommer tættere på holdets mål.

PPDA for Premier League holdene i 2020/2021 efter 24. spillerunde er illustreret nedenfor.
\
Marcelo Bielsa's Leeds er det helt suverænt mest aggressive hold i deres presspil, mens at Newcastle meget mere dybt i deres defensive organisation. Denne rangering følger godt intuitionen om hvilke hold der presser højt og hvilke hold der er mere defensive i deres organisation.

![Alt Text](/img/advanced_metrics/ppda_table.png)

Det er vigtigt at notere at PPDA kan måle intensiteten af et holds pres og gør det muligt at sammenligne og rangere hold. Men PPDA måler ikke hvor succesfulde holdene er i deres aktioner og er dermed ikke et mål for hvor godt et hold er defensivt, men mere en indikation på deres defensive profil. Leeds er f.eks. et offensivt pressende hold, men at Newcastle står med en lavere defensiv linje og ikke presser højt.

## Possession adjusted tacklinger og erobringer

Et af flere problemer med defensive statistikker er at de hold som har bolden mere end deres modstandere vil have færre defensive aktioner som tacklinger og erobringer. Spillere på hold med lav boldbesiddelse, som f.eks. under Sam Allardyce, vil have flere muligheder for at lave tacklinger og erobringer end spillere under f.eks. Pep Guardiola. Spillere hold med lav boldbesiddelse ligger derfor øverst på defensive aktioner, men ved at justere for boldbesiddelse (possession adjusted, PAdj) kan man kreditere alle spillere, uanset hold, på samme præmis.

Helt konkret så justeres defensive aktioner ved at starte med 50% boldbesiddelse som divideres med boldbesiddelsen for modstander holdet. Dette tal bliver så ganget med antallet af tacklinger eller erobringer som spilleren lavede. Så hvis et hold havde 60% boldbesiddelse og spilleren lavede 10 tacklinger, så vil spilleren have lavet (50/40 * 10 = 12.5) 12.5  PAdj tacklinger.
\
Dette er altså ikke længere det _"rigtige"_ antal tacklinger eller erobringer en spiller lavede i kampen. Men derimod, som [StatsBomb nævner i deres artikel](https://statsbomb.com/2014/06/introducing-possession-adjusted-player-stats/), kan man tænke dette tal som antal defensive point spilleren fik i løbet kampen. Ved at justere for boldbesiddelse kan man altså vurdere spillernes defensive output på lige vilkår. Lad os se på et eksempel fra Premier League 2019/2020 sæsonen.

![Alt Text](/img/advanced_metrics/padj_tackles_pl.png)

Her er top 10 for tacklinger per 90 min. i Premier League sæsonen 2019/2020 både justeret for boldbesiddelse og ikke justeret.
\
Her kan man se spillere som João Cancelo og Fabinho, som spiller på hold med høj boldbesiddelse, bliver krediteret for deres defensive aktioner når man justerer for boldbesiddelsen.

## Field Tilt

Field tilt er en ny måde at måle boldbesiddelse på. Ved udelukkende [kun at bruge boldbesiddelse](https://theathletic.com/2352067/2021/01/29/possession-the-most-dangerous-statistic-in-football/) kan interessante og vigtige informationer om kampen eller holdet blive skjult.
\
Et hold med 80% boldbesiddelse vurderes til at have domineret en kamp. Men hvis 60% af afleveringerne foregik på egen tredje del og holdet ikke skabte nogle chancer, vil dominansen ikke være stor. Det handler om hvor boldbesiddelse tager plads. Ligeledes kan et hold med lav boldbesiddelse, såsom Leicester 2015/2016 sæsonen, have en dyb struktureret defensiv, og lave hurtige kontraangreb som skaber farlige afslutninger.

Fielt tilt er ikke den endegyldige løsning, men det kan give et bedre billede af hvorhenne boldbesiddelsen for de to hold tog plads. Field tilt måler andelen af boldbesiddelse, hvis man kun tager berøringer og afleveringer på den sidste tredje del af banen i betragtning.
\
Hvis f.eks. Manchester City havde 80 afleveringer på sidste tredje del, mens at Stoke kun havde 20 afleveringer på sidste tredje del, vil Manchester City have et field tilt på 80%.

Som nævnt er field tilt ikke den endegyldige løsning, da det ikke måler hvor mange eller kvaliteten af chancer som holdet skabte. Her kan man bruge xG til at kvantificere kvaliteten af holdets chancer, og dermed skabe et bedre billede af kampen.


_Dette indlæg vil løbende bliver opdateret med nye statistikker._

_Kommende opdateringer: **[Expected Threat (xT)](https://karun.in/blog/expected-threat.html)**, **[Possession Value (PV)](https://www.statsperform.com/resource/evolving-our-possession-value-framework/)**_

