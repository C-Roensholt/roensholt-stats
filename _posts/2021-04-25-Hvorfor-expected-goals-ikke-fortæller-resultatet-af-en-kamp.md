---
layout: post
published: true
title: Hvorfor xG ikke er resultatet af kampen - Om sandsynlighed og uforudsigelighed i foldbold
image: /img/xG_infographic/Leeds_vs_Liverpool_xG_infographic_gw32.png
date: '2021-04-25'
readtime: true
---

Expected goals (xG) bliver ofte brugt som en rettesnor for hvilket hold der "fortjente" at vinde en kamp. Ligeledes at 4 xG betyder at en spiller eller et hold "fortjente" eller "skulle have" scoret 4 mål, men det betyder faktisk at 4 mål var det mest **sandsynlige resultat** af alle skud. I dette blog indlæg vil give en bedre fortolkning af xG på enkelte kampe, og lave en visualisering som repræsentere sandsynlighed og usikkerheden ved xG på en enkelt kamp.

Jeg vil bruge 1-1 kampen mellem Leeds og Liverpool som eksempel, og den traditionelle xG grafik vil typisk minde om denne: 
![alt text](/img/xG_infographic/Leeds_vs_Liverpool_xG_racechart_gw32.png)
_Det traditionelle xG visualisering i en kamp mellem Leeds og Liverpool_

#### Fodbold - En uforudsigelig og tilfældig sport

Fodbold er i sin natur en _uforudsigelig_ sport, og det er derfor nærliggende at se fodbold gennem sandsynligheder. Da fodbold er en uforudsigelig sport kan mål blive scoret ud af ingenting, altså uden sammenhæng til tidligere mål, holdene eller andre faktorer. I statistik kan dette fænomen blive beskrevet gennem poisson-fordelingen.

**Poisson-fordeling**

Poisson fordelingen beskriver sandsynligheden for at et bestemt antal hændelser sker i en bestemt tidsinterval, f.eks. antal fødsler fra kl. 10 til kl. 11 på om lørdagen i Faxe, antal telefonsælger opkald på din telefon i uge 32 eller antal mål Liverpool scorer på 90 minutter. Disse sandsynligheder bliver udregnet ved en parameter λ (lambda), som beskriver det antal mål vi forventer i de 90 minutter.

Rent matematisk ser det således ud:
![alt text](/img/xG_infographic/poisson.png)

Hvis vi kigger på en enkelt kamp kan vi bruge expected goals som det forventede antal mål. Man kan dermed udskifte parameteren λ med expected goals værdien for holdet og _x_ med det antal mål vi vil udregne sandsynligheden for. F.eks. hvis Liverpool genererer 1.60 xG i en kamp kan vi udregne sandsynligheden for at de scorer 1 mål til at være ~32%.

![alt text](/img/xG_infographic/poisson_calculated.png)

Hvis vi igen kigger på Leeds (2.62 xG) mod Liverpool (1.60 xG) kan denne udregning gentages for at begge hold scorer 0, 1, 2, 3... mål. Sandsynlighederne for at begge hold scorer 0 til 9 i denne kamp vil være:

![alt text](/img/xG_infographic/goal_probabilities_viz.png)

Når vi har udregnet sandsynligheden for at begge hold scorer mellem 0 og 9 mål kan vi udregne sandsynligheden for resultatet af kampen. Sandsynligheden for resultatet 1-1 vil være (0.19*0.32 = 0.0608) 6,08%, mens at sandsynligheden for at Leeds vinder 2-1 er (0.25*0.32 = 0.0807) 8,07%.
Udregningen kan så gentages for alle mulige resultater, og ved at lægge alle resultater hvor Liverpool vinder (0-1, 1-2, osv.), Leeds vinder (1-0, 2-1, osv.) og uagjorte resultater (0-0, 1-1, osv.) sammen kan sandsynligheden for sejr, nederlag og ufgjort blive udregnet. Disse sandsynligheder i kampen er fordelt således:

![alt text](/img/xG_infographic/win_probability_viz.png)

##### Den samlede xG grafik

De forskellige grafikker kan sammensættes i en enkel visualisering. Denne visualisering giver, sammenlignet til den traditionelle grafik, en bedre forståelse af hvordan expected goals på enkelte kampe ikke fortæller resultatet. 

![alt text](/img/xG_infographic/Leeds_vs_Liverpool_xG_infographic_gw32.png)

Fodbold er en udforudsigelig sport og man kan, som vist, gennem sandsynlighedsregning få en bedre intuitiv forståelse af uforudsigeligheden og variansen af mål og enkelstående resultater i fodbold.

Tak for at læse med, hvis du er interesseret kan koden for beregningerne og visualiseringerne kan det findes [her](https://github.com/C-Roensholt/Improving-Match-xG-Infographics)