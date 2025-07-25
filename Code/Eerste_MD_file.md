## Quiz: Hoe interpreteer jij waarschijnlijkheid?

We starten met een korte quiz (gebaseerd op @johnson2022bayes) met vier vragen om te ontdekken hoe jij naar waarschijnlijkheid kijkt.

**Instructies voor deelnemers**

- Lees iedere vraag zorgvuldig.
- Bespreek je antwoorden kort met je buurvrouw of man.
- Noteer je antwoorden (A, B of C) op papier.
- We bespreken de antwoorden en de achterliggende gedachten plenair na de quiz.

## Vraag 1

Bij het opgooien van een eerlijke munt zeggen we dat de kans op ‘kop’ 0,5 is. Hoe interpreteer jij deze kans?

A) Als ik de munt heel vaak opgooi, komt ongeveer 50% kop.  
B) Kop en munt zijn nu even plausibel.  
C) Beide interpretaties (A en B) zijn logisch.

**notes**

Deze vraag laat mooi het verschil zien tussen de Frequentistische en Bayesiaanse interpretatie:

- A geeft de Frequentistische uitleg: kans als lange termijn frequentie.
- B past beter bij de Bayesiaanse uitleg: kans als plausibiliteit gegeven de kennis nu.
- C laat zien dat je beide benaderingen logisch vindt.

Later gebruiken we deze interpretaties om de verschillende manieren van omgaan met onzekerheid uit te leggen.


## Vraag 2

Elf dagen voor de verkiezingen gaf FiveThirtyEight Trump een kans van 51% om te winnen. Hoe interpreteer jij deze kans?

A) Als we de verkiezingen 100 keer zouden houden, wint Trump 51 keer.  
B) Trump heeft iets meer kans om te winnen dan om te verliezen.  
C) Dit slaat nergens op: Trump wint of verliest, de kans is 0 of 1.

**notes** 

Deze vraag laat zien waarom een Frequentistische interpretatie soms onnatuurlijk aanvoelt:

- A is Frequentistisch gedacht: kans als herhaalbaar experiment.
- B is typisch Bayesiaans: kans als mate van overtuiging.
- C wijst kansdenken helemaal af, vanuit een deterministische blik.


## Vraag 3 


We laten 2 statements zien:

1. Tessa zegt dat ze elk liedje van Taylor Swift binnen een paar tonen kan herkennen. Ze wordt getest: 7 liedjes, 7 keer goed.

2. Paul de Octopus voorspelde in 2010 de uitslag van alle 7 WK-wedstrijden van Duitsland correct.

Wat denk jij?

A) Ik vertrouw meer op Tessa’s claim dan op die van Paul.  
B) Het bewijs voor Tessa en Paul is even sterk.


**notes**
Frequentistisch kijk je alleen naar het succespercentage: beiden 7 uit 7. Bayesiaans weeg je ook mee wat je vooraf gelooft: mensen herkennen liedjes best vaak, maar een octopus die voetbalwedstrijden voorspelt? Onwaarschijnlijk.

Deze vraag laat zien waarom ‘priors’ belangrijk zijn in Bayesiaans redeneren.


## Vraag 4

Een arts zegt dat je positief hebt getest op een zeldzame ziekte. Wat is de belangrijkste vraag om te stellen?

A) Wat is de kans dat ik écht ziek ben?  
B) Wat is de kans dat ik een positieve test krijg als ik níet ziek ben?

**notes**

Hier draait het om een klassiek probleem in medische statistiek:

- A vraagt naar de *"post test kans"* — de kans dat je echt ziek bent gegeven de positieve test (positieve predictieve waarde).
- B vraagt naar het *vals-positiefpercentage* — kans op een fout-positieve test bij gezonde mensen.

Beide perspectieven zijn belangrijk, maar A is de vraag die je écht wil stellen. Hier biedt de formule van Bayes het antwoord: we updaten onze overtuiging op basis van de test (data) en de zeldzaamheid van de ziekte (prior.

We kunnen dit eventueel visueel laten zien? [zoiets?](https://www.youtube.com/watch?v=HZGCoVF3YvM)

## Tellen van je score 


Tel je punten op:

| Vraag  | A (punten) | B (punten) | C (punten) |
|-------|------------|------------|------------|
| 1     | 1          | 3          | 2          |
| 2     | 1          | 3          | 1          |
| 3     | 3          | 1          |            |
| 4     | 3          | 1          |            |

**Interpretatie van je score**

- 4–5 punten: Je denkt nu vooral Frequentistisch.
- 6–8 punten: Je ziet sterke kanten in beide benaderingen.
- 9–12 punten: Je neigt sterk naar het Bayesiaanse denken.




## Frequentistisch versus Bayesiaans: de belangrijkste verschillen

| Aspect             | Frequentistisch                | Bayesiaans                       |
|--------------------|---------------------------------|-----------------------------------|
| Kans (P)            | Lange termijn frequentie       | Geloofsgraad / plausibiliteit     |
| Focus               | Variabiliteit van data         | Onzekerheid over uitkomsten       |
| Informatiebron      | Data                           | Data + voorkennis (‘priors’)      |
| Wat je berekent     | $P(\text{data | hypothese})$    | $P(\text{hypothese | data})$      |

**Uitleg van de tabel**:

- **Kans (P)**:
    - Frequentisten zien kans als herhaalde uitkomsten in de lange termijn.
    - Bayesians zien kans als een maat van hoe plausibel iets is, gegeven wat je weet.

- **Focus**:
    - Frequentisten kijken naar de spreiding (variabiliteit) van data.
    - Bayesians kijken naar onzekerheid en passen kennis aan na nieuwe data.

- **Informatiebron**:
    - Frequentisten baseren zich puur op data.
    - Bayesians combineren data met bestaande kennis 

- **Wat je berekent**:
    - Frequentisten berekenen: hoe waarschijnlijk is deze data als de hypothese klopt?
    - Bayesians berekenen: hoe waarschijnlijk is de hypothese gezien de data die we hebben?

## We kunnen nog een mooie visualisatie maken met prior + data = nieuwe prior
nieuwe prior + data = nieuwere prior


## In de praktijk: onzekerheid over beleidsanalyse

- de onzekerheid over de schatting van coefficienten vertaalt zich in onzekerheid van beleidsrelevante keuzes
- een voorbeeld:
  - de overheid wil een publiek goed van 18k (per capita) financieren met inkomensbelasting
  - er is belasting systeem met 3 schuiven en een oplopende marginale belasting tarief
  - wij schatten de (Pareto) verdeling van inkomens
  - de onzekerheid van de schatting van deze parameters bepaalt of het lukt om het publieke goed te financieren
  - dit is een niet lineare transformatie van de onzekerheid, frequentisme is hier niet goed in

## Simulatie

- we hebben sample gegenereerd van een Pareto inkomens verdeling
- met sample hebben we de parameters van deze verdeling geschat

![verdeling inkomens in sample](../figures/income_distribution.png)


## Onzekerheid

- deze geschatte parameters $\alpha, m$ hebben een verdeling gegeven de data
- posterior verdeling: $p(\alpha,m|data)$
- het algoritme sampled van deze verdeling: er zijn 4000 $\alpha$ and $m$ (4 keer 1000 samples)
- voor een geven $\alpha, m$, is er een belasting opbrengst (met de niet lineare belasting functie)
- voor 4000 $\alpha, m$ is er een verdeling van deze belasting opbrengt

## Verdeling van belasting opbrengsten

![verdeling belasting opbrengst](../figures/average_tax_income_distribution.png)

## Significantie

- stel de verwachte belasting opbrengst is 17k (per capita)
- is dit significant verschil met benchmark 18k?
- is helemaal niet relevant voor beleidsanalyse
- Bayesiaan: verwachte belasting opbrengst is 19875
- kans dat de threshold niet gehaald wordt is 40%

## Wat is een goede keuze voor het top marginal tarief

![kans dat de benchmark gehaald wordt](../figure/probabilities.png)


## andere voorbeelden

- arbeidsaanbod elasticteit: totale belasting opbrengsten als functie van marginal tarief inkomsten belasting
- eigen risico elasticeit: total zorg uitgaven
- vraagelasticiteit NS: prijzen treinkaartjes, hoeveel autos op de weg
- efficientie winsten van een fusie: leidt fusie tot welvaartsverhoging
- onzekerheid over de schattingen die niet triviaal vertaald in onzekerheid over beleidsuitkomsten
- geintegreerde schattingsmethod en scenario analyse
