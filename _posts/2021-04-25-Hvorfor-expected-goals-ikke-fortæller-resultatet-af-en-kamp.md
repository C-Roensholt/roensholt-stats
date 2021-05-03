---
layout: post
published: true
title: Hvorfor extected goals ikke fortæller resultatet en kamp
image: /img/xG_infographic/Leeds_vs_Liverpool_xG_infographic_gw32.png
date: '2021-04-25'
readtime: true
---

Expected goals (xG) bliver ofte brugt som en rettesnor for hvilket hold der "fortjente" at vinde en kamp. Ligeledes at 4 xG betyder at en spiller eller et hold "fortjente" eller "skulle have" scoret 4 mål, men det betyder faktisk at 4 mål var det mest **sandsynlige resultat** af alle skud. I dette blog indlæg vil give en bedre fortolkning af xG på enkelte kampe, og lave en visualisering som repræsentere sandsynlighed og usikkerheden ved xG på en enkelt kamp.

![alt text](/img/xG_infographic/Leeds_vs_Liverpool_xG_racechart_gw32.png)
_Det traditionelle xG visualisering i en kamp mellem Leeds og Liverpool_

## Sandsynlighedsfordeling af xG

Fodbold er i sin natur en _uforudsigelig_ sport, derfor en rigtig god idé at kigge på fodbold gennem sandsynlighed beregninger. Da fodbold er en uforudsigelig sport kan mål blive scoret ud af ingenting, altså uden sammenhæng til tidligere mål, holdene eller andre faktorer. I statistik kan dette fænomen blive beskrevet gennen __poisson fordelingen__, som kan finde sandsynligheder af tilfældige og uafhængige hændelser i en given tidsramme.

**Poisson-fordeling**
Poisson fordelingen beskriver sandsynligheden for et bestemt antal hændelser sker i en bestemt tidsramme, f.eks. antal fødsler fra 10-11 på om lørdagen i Faxe, antal telefonsælger opkald på din telefon i uge 32 eller antal mål Brøndby scorer på 90 minutter. Sandsynlighederne bliver udregnet gennem en parameter λ, som beskriver det antal mål vi forventer i de 90 minutter.

Den matematiske formel ser således ud:
![alt text](/img/xG_infographic/poisson.png)

Når vi kigger på en enkelt kamp kan vi bruge expected goals som det forventede antal mål, og dermed udskifte parameteren λ med expected goals værdien for holdet og _x_ med det antal mål vi vil udregne sandsynligheden for. F.eks. hvis Liverpool genererer 1.60 xG i en kamp kan vi udregne sandsynligheden for at de scorer 1 mål være 32%.

![alt text](/img/xG_infographic/poisson_calculated.png)

Hvis vi igen kigger på Leeds (2.62 xG) mod Liverpool (1.60 xG) kan denne udregning gentages for at begge hold scorer 0, 1, 2, 3 osv. mål. Sandsynlighederne for at begge hold scorer 0 til 9 er dermed:

![alt text](/img/xG_infographic/goal_probabilities_viz.png)

Når vi har udregnet sandsynligheden for at begge hold scorer mellem 0 og 9 mål kan vi nu udregne sandsynligheden for resultatet af kampen, f.eks. vil sandsynligheden for 1-1 være (0.19*0.32 = 0.0608) 6,05%, mens at sandsynligheden for at Leeds vinder 2-1 er (0.25*0.32 = 0.0807) 8,07%.
Udregningen kan så gentages for alle mulige resultater, og ved at lægge alle resultater hvor Liverpool vinder (0-1, 1-2, osv.), Leeds vinder (1-0, 2-1 osv.) og uagjorte resultater sammen kan sandsynligheden for sejr, nederlag og ufgjort blive udregnet. Disse sandsynligheder i kampen er fordelt således:

![alt text](/img/xG_infographic/win_probability_viz.png)

## Den komplette xG grafik

De forskellige grafikker kan sammensættes i en enkel visualisering. Denne visualisering giver, sammenlignet til den traditionelle grafik, en bedre forståelse af hvordan expected goals på enkelte kampe ikke fortæller resultatet. 

![alt text](/img/xG_infographic/Leeds_vs_Liverpool_xG_infographic_gw32.png)

Fodbold er en udforudsigelig sport og man kan, som vist, gennem sandsynlighedsregning få en bedre intuitiv forståelse uforudsigeligheden og variansen af mål og enkelstående resultater i fodbold.

Tak for at læse med, hvis du er interesseret kan koden for beregningerne og visualiseringerne findes [her](https://github.com/C-Roensholt/Improving-Match-xG-Infographics)