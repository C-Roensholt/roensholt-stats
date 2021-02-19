---
layout: post
published: true
title: Forklaring af avancerede fodbold statistikker
subtitle: >-
  Hvordan kan man bruge passing networks til at analyse en fodboldkamp?
date: '2021-02-28'
readtime: true
---

Fodbold er i de seneste år blevet en  

Jeg vil derfor give et overblik over de forskellige "avancerede" statistikker som er kommet til fodboldverdenen de seneste år. Yderligere vil jeg give kontekst til de forskellige statistikker og hvordan de kan bruges til at analysere og måle præstation for en spiller eller et hold. 

# Indhold
1. [Expected Goals (xG)](#Expected-Goals)
2. [Expected Assist (xA)](#Expected-Assist)
3. [Expected Points (xP)](#Expected-Points)
4. [Målscorende aktioner (GCA)](#Målscorende-aktioner)
5. [Skud assist aktioner (SCA)](#Skud-assist-aktioner)
6. [Bold progression](#Bold-progression)
7. [Expected Threat (xT)](#Expected-Threat)
8. [PPDA](#PPDA)
9. [Possession adjusted tacklinger og erobringer](#Possession-adjusted-tacklinger-og-erobringer)
10. [Revideret tackle procent](#True-Tackle-procent)
11. [Field Tilt](#Field-Tilt)

## Expected Goals
(Vis en shot map af underperformer og overperformer, ligeledes rolling xG for Liverpool)

Vi starter med den statistik som har vundet størst indpas i den almene fodboldsnak nemlig Expected Goals (xG)
\
Jeg har lavet to indlæg omkring xG, som kan ses [her](http://roensholt-stats.com/2020-07-08-Hvad-er-Expected-Goals/) og [her](http://roensholt-stats.com/2020-08-14-Hvordan-laver-man-en-xG-model/). Derfor vil jeg ikke gå i dybden, men give en overordnet beskrivelse.

I den simple form er xG sandsynligheden for at et givet skud bliver til et mål. En xG på 0.5 betyder dermed at det forventes at 5 ud af 10 spillere vil score på den chance. Den mest simple eksempel af xG er straffesparket, som har en fikset xG værdi på 0.76.
\
I analysen af denne sandsynlighed bliver der taget en række faktorer i betragtning, hvor de mest basale er:

- **Lokationen af skuddet:** Distance til målet og vinklen på skuddet.
- **Modspillernes position:** Hvor mange forsvarsspillere var der mellem bolden og målet? Hvordan stod målmanden placeret?
- **Typen af assist:** Kom skuddet efter en aflevering i dybden, et indlæg eller et frispark osv.
- **Opbygning til målet:** Kom bolden fra en _rebound_? I et etableret opspil mod et dybt stående forsvar eller i et kontraangreb mod et forsvar ude af balance?

Flere tusinde skud er taget i betragtning for at beregne hvor meget hver enkel parameter influere sandsynligheden for af skuddet bliver til mål. Alle udbydere af xG bruger ikke de samme parametre, som nævnt i mit tidligere indlæg, så er [StatsBomb de første til at lave en xG model som tager højden på skuddet i betragtning](https://statsbomb.com/2020/07/statsbomb-release-expected-goals-with-shot-impact-height/), hvilket er noget som Opta's xG model ikke tager hensyn til.
\
En lille udbygning af xG er **Post Shot xG (PSxG)**, som kun tager skud som ender inden for målrammen i betragtning. Dermed vil alle skud som ikke er inden for målrammen have en PSxG på nul, da der er 0% chance for at skuddet til til et mål. Dette bliver bl.a. brugt når man skal beregne en målmands præstation i forhold til den xG holdet har tilladt imod ham, hvilket jeg har inkluderet [i min analyse af Premier League målmændenes præstationer midt i 2019/2020 sæsonen](http://roensholt-stats.com/2020-02-16-GoalkeepersSoFar-1-af-3/).


Man kan f.eks. bruge xG til at evaluere en spillers skud egenskaber. Ved at summere alle xG for skuddene af spilleren kan man analysere se om spilleren konsekvent scorer flere mål end hans xG indikerer en spiller med bedre afslutningsevner end forventet eller mere held i sine afslutninger.
\
Et eksempel på dette er illustreret nedenfor hvor alle Mohamed Salah's og Roberto Firmino's skud er vist.

![Alt Text](/img/advanced_metrics/Mohamed-Salah_shotMap_1.png)
![Alt Text](/img/advanced_metrics/Roberto-Firmino_shotMap_1.png)

Her kan man se hvordan Salah har scoret flere mål en det var forventet, mens at Firmino ikke har formået at konvertere hans store skud muligheder til mål.
![Alt Text](/img/advanced_metrics/Roberto Firmino_shotMap_1.png)
![Alt Text](/img/advanced_metrics/Mohamed Salah_shotMap_1)

\
Dette tydeliggør også en af ulemperne ved xG, fordi xG tager nemlig ikke hensyn til hvilken spiller der tager skuddet. Man har set at Messi igennem flere sæsoner har [overpræsteret hans xG](https://www.infogol.net/en/blog/analysis/hit-or-miss-the-most-clinical-finishers-in-europe-142020), simpelthen fordi at han er en så meget bedre afslutter en den gennemsnitlige spiller.


En angriber der kommer i gode skud situationer, men ikke får konverterede disse chancer til mål vil have en høj xG. Denne underpræstation på xG I løbet af en hel sæson kan man forvente at angriberen vil  
Hvis vi kigger på Mohamed Salah

Det samme koncept gør sig gældende hvis vi kigger på et holds xG, hvor man kan kigge på forskellen mellem xG for og imod holdet. Ved at kigge xG forskellen for holdet kan man 

\
Det er dog vigtigt at forstå at xG ikke er en ultimativ beregning af om en holds sejr var fortjent eller ufortjent.
Game state impact on xG
\


## Expected Assist

https://www.youtube.com/watch?v=H4kNa1cUvZM

Vi tager nu et kig på xG's lillesøster, Expected Assist (xA).
\
Assist er den sidste aflevering som fører til et mål, hvilket betyder at spilleren er afhængig af at angriberen kan konvertere afleveringen mål. Assist er derfor ikke en god indikator af en spillers egenskab til at skabe chancer, da 

![Alt Text](/img/sterling_miss.gif)
*Sterling brænder en stor chance og Kyle Walker får ikke assisten*

 xA kan blive målt på to forskellige måder nemlig 

Mané assist | Sergio Busquets assist
-----------:|:-------------------:
![Alt Text](/img/mane_assist.gif) | ![Alt Text](https://i.imgur.com/BzyPDZX.gif)






## Expected Points
(Hvis en Expected Point tabel)

Ovenfor kiggede vi på xG for og imod et hold

## Målscorende aktioner

## Skud assist aktioner

## Bold progression

Fremadrettede afleveringer og 

## Expected Threat

(Hvis Özil co-assist)




## PPDA

(Hvis tabel af PPDA med Leeds top)


## Possession adjusted tacklinger og erobringer

(Hvis revised tabel)


## True tackle procent

## Field Tilt

## Kontekstualisering af statistikker

Det vigtigste med statistikker er at sætte dem i kontekst

Jeg bestræber mig meget på det, men endelig "call me out" hvis jeg ikke efterfølger mine egne principper.


