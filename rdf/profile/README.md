# Toepassingsprofiel RDANL in RDF

Toepassingsprofiel RDANL is een op RDA gebaseerde ontologie in RDF-vorm. 

Zie [`rdanl.ttl`](rdanl.ttl).

Doel van dit toepassingsprofiel is om de hoogdrempeligheid van het gebruik van RDA te verlagen voor toepassingen in een RDF-context, zonder daarbij de semantische zeggingskracht van RDA aan te tasten. 

Een uitgangspunt hierbij is dat de veelheid van naar *range* en *domain* gedifferentieerde kenmerken die RDA biedt geen semantische meerwaarde opleveren in een context waarin alle entiteiten expliciet van een klasse-aanduiding voorzien zijn. Onder deze voorwaarde wordt een groot deel van de kenmerken van RDA overbodig.

RDF is er niet alleen voor machines maar ook voor mensen. Binnen dit profiel is daarom nadrukkelijk gekozen voor door mensen leesbare, begrijpelijke URI's. Hiertoe worden de element-namen van de Engelstalige *lexical aliasses* van RDA gebruikt.

Het profiel is een **extensie van RDA** en kan daarom, waar relevant of zinvol, gecombineerd worden met reguliere RDA.

## Meer in detail

* De URI's van RDANL zijn uit het oogpunt van gebruiksgemak gedefinieerd in één *namespace*, te weten  `http://data.bibliotheken.nl/rdanl#`, bij voorkeur met `rdanl` als *namespace prefix.*
* De klassen zijn in RDANL gedefinieerd als een `rdfs:subClassOf` van de overeenkomstige klasse in RDA.
* Kenmerken zijn in RDANL gedefinieerd als een `rdfs:subPropertyOf` van het overeenkomstige kenmerk in RDA.
* Ter ondersteuning van de Persona-benadering is kenmerk `rdanl:relatedPersonaOfWork` toegevoegd, een `rdfs:subPropertyOf` van `rdanl:relatedNomenOfWork`. 
* Een kracht van RDA ligt onder andere bij de grote rijkdom aan kenmerken die rollen aanduiden. Vanuit de genoemde vereenvoudigingsprincipes worden alleen rollen die betrekking hebben op een `rdanl:Agent`.
* De hierarchie in kenmerken binnen RDANL volgt impliciet die van RDA (door de `rdfs:subPropertyOf`-relatie). Uit oogpunt van leesbaarheid zijn deze relaties waar zinvol geacht ook expliciet opgenomen in RDANL.

## Work in progress

RDANL is *work in progress*. Aandacht verdient onder andere:

* Nog niet alle kenmerken uit het spreadsheet van het toepassingsprofiel waar deze RDF variant als bijzondering toe behoord zijn opgenomen.
* Streven is ook alle inverse relaties expliciet op te nemen.
* Aandacht verdient nog welke rol-definierende relaties opgenomen zouden moeten worden.

