---
layout: post
published: true
title: Expected Goals - Hvad er Expected Goals?
subtitle: >-
  Hvad er Expected Goals (xG)?
date: '2020-07-08'
readtime: true
---
## Expected Goals - Fodbold analysens grundsten

Expected Goals (xG) betegner starten på den store analytiske tilgang til fodboldspillet, som vi har set i de seneste 5 år. Jeg vil derfor give en introduktion til begrebet i denne artikel.

#### Den simple xG model
xG er baseret på skud, hvor man har fundet ud af at lokationen af skudet og vinkel til målet har størst inflydelse på skudets xG. Så et skud tættere på mål med en bred vinkel til målet (f.eks. fra straffesparkspletten) vil have en større xG end et skud langt fra mål og/eller med en smal vinkel til målet (f.eks. et skud fra mållinjen eller midtercirklen).
Så tommelfingerreglen er at jo tættere på mål skudet kommer fra dets større er chanchen (xG) for at skudet ender med at mål. Derudover vil et skud der er udført med hovedet have en lavere xG end et skud med foden, da et hovedstød intuitivt er sværere at konvertere til et mål. 
> _Note_: En lille 'pet peeve' er dog om et skuds xG skal betsemmes af angriberens valg af skud form. For chancen for at score bliver vel ikke lavere bare fordi Giroud laver et skorpions spark, fremfor bare at flugte til bolden. Men det vil jeg ikke komme ind på i denne artikel.

Disse tre egenskaber ved et skud, distance til mål, vinkel til mål og hvilken kropsdel skudet kommer fra, er meget deskriptive for skudets xG og vil derfor danne et godt grundlag som _'features'_ for at kunne træne en model til at forudsige om et skud ender med et mål eller ikke. En xG model kunne derfor se således ud:

__Features__:
- Distance til mål
- Vinkel til mål
- Kropsdel

__Target__:
- Mål (1) eller ikke mål (0)

Dette er en meget simpel model der er nem at analyse og evaluere, men du tænker nok at der er flere egenskaber ved et skud eller opspillet til målet som har indflydelse på om det ender med mål?

#### Den komplekse xG model

Ja, der er flere egenskaber ved et skud og opspillet til skudet, som har indflydelse på om skudet ender med et mål. For et skud er væsenligt svære at score på hvis bolden kommer 2 meter over jorden og væsentligt nemmere at score på hvis målmanden er totalt misplaceret. Dette er noget som StatsBomb for nyligt har implmenteret i deres meget [avancerede xG model](https://statsbomb.com/2020/07/statsbomb-release-expected-goals-with-shot-impact-height/). En sådan xG model vil derfor være mere præcis en den simple model vi har diskuteret ovenfor. Men der vel flere _features_ ved et skud med indflydelse på dets udfald, f.eks. kunne minuttallet og stillingen i kampen have indflydelse på dets udfald (en angriber vil være under større i 90. minut med stillingen 1-1 end i 10. minut med stillingen 3-0).

En xG model kan dog meget hurtigt blive utrolig kompleks og dermed svær at analyse og evaluere. For en xG model kan blive utrolig præcis hvis den bliver fodret med mange _features_ der har indflydelse på skudet. Men hvis modellen tager _features_ som trænerens beklædning, tid på dagen, spillerens morgenmad osv. i betragting, kan det være utrolig svært at analyse og evaluere til spilleren hvorfor han skal drible til en bestemt position med højere xG end den position han skød fra.



