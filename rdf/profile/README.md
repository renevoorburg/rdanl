# Toepassingsprofiel RDANL in RDF

Toepassingsprofiel RDANL is een op RDA gebaseerde ontologie in RDF-vorm. 

Zie [`rdanl.ttl`](rdanl.ttl).

Doel van dit toepassingsprofiel is om de hoogdrempeligheid van het gebruik van RDA te verlagen voor toepassingen in een RDF-context, zonder daarbij de semantische zeggingskracht van RDA aan te tasten. Het vormt een verbijzondering van een generieker RDA-toepassingsprofiel voor monografieën. 

Een uitgangspunt hierbij is dat de veelheid van naar *range* en *domain* gedifferentieerde kenmerken die RDA biedt, geen semantische meerwaarde opleveren in een context waarbij alle entiteiten expliciet van een klasse-aanduiding voorzien zijn. Onder deze voorwaarde wordt een groot deel van de kenmerken van RDA overbodig.

RDF is er niet alleen om gelezen te worden door machines, maar ook door mensen. Daarom is er binnen dit profiel nadrukkelijk gekozen voor door mensen leesbare, begrijpelijke URI's. Hiertoe worden de element-namen van de Engelstalige *lexical aliasses* van RDA gebruikt.

Het profiel is minder uitgebreid dan RDA, zeker als het gaat om kenmerken die rollen aanduiden, maar omdat het een **extensie van RDA** is, kan het gecombineerd worden met reguliere RDA als RDF.

## Meer in detail

* De URI's van RDANL zijn uit het oogpunt van gebruiksgemak gedefinieerd binnen één *namespace*, te weten  `http://data.bibliotheken.nl/rdanl#`, bij voorkeur te gebruiken met `rdanl` als *namespace prefix.*
* Klassen binnen RDANL zijn gedefinieerd als een `rdfs:subClassOf` van de overeenkomstige klasse in RDA.
* Kenmerken zijn in RDANL gedefinieerd als een `rdfs:subPropertyOf` van het overeenkomstige kenmerk in RDA.
* Als verbijzondering van een RDA-toepassingsprofiel voor monografieën kunnen kenmerken relevant voor andere materiaalsoorten ontbreken.
* Ter ondersteuning van de Persona-benadering is kenmerk `rdanl:relatedPersonaOfWork` toegevoegd, een `rdfs:subPropertyOf` van `rdanl:relatedNomenOfWork`. 
* Een kracht van RDA is de grote rijkdom aan kenmerken die **rollen** aanduiden. Vanuit de genoemde vereenvoudigingsprincipes is er een voorkeur voor rollen die betrekking hebben op instanties van de `rdanl:Agent`-klasse.
* De hierarchie in kenmerken binnen RDANL volgt impliciet die van RDA (door de `rdfs:subPropertyOf`-relatie). Uit oogpunt van leesbaarheid zijn deze relaties waar zinvol geacht ook expliciet opgenomen.

## Work in progress

RDANL is *work in progress*. Aandacht verdient onder andere:

* Nog niet alle kenmerken uit het spreadsheet van het toepassingsprofiel, waar deze RDF variant als verbijzondering toe behoort, zijn opgenomen.
* Streven is ook alle inverse relaties expliciet op te nemen.
* Aandacht verdient nog welke rol-definierende relaties opgenomen zouden moeten worden.

