# Over de voorbeelden

In deze map staan voorbeeldbestanden die het gebruik van het RDA-toepassingsprofiel voor het publiceren van linked data (RDF) illustreren.

Bij het maken van de voorbeeld-RDF zijn de volgende principes gehanteerd:

* Alle entiteiten zijn expliciet van een klasse-aanduiding voorzien. Dit verhoogt de begrijpelijkheid van de RDF en maakt het mogelijk om alleen generieke relaties toe te passen.
* De properties zijn zo generiek mogelijk gekozen. Doordat alle entiteiten van  een klasse-aanduiding voorzien zijn doet dit geen afbraak aan de semantische rijkdom. Het bevragen van de data, bijvoorbeeld met SPARQL, wordt hierdoor ook vereenvoudigd.
* Voor taalcodes is IETF BCP 47 gebruikt. Het gebruik van URI’s heeft hier geen meerwaarde.
* Op vergelijkbare wijze is voor landencodes gebruik gemaakt van literals volgens ISO 3166-1 alpha-2 .
* Bij de plaats van publicatie is een geneste constructie gebruikt voor plaatsnaam en land.
* Timespans zijn ingevuld als literals volgens ISO- 8601, zonder datatype-aanduiding.
* De RDF volgt de in het toepassingsprofiel voorgestelde Persona-aanpak.
* Eigenschappen zoals languageOfRepresentativeExpression worden hier op het meest specifieke niveau aangeduid, dus in dit voorbeeld als eigenschap van de representatieveExpression, niet als eigenschap van het Work (wat uiteraard alleen mogelijk is als er ook een representativeExpression aangewezen kan worden).

De voorbeeld-RDF komt in twee varianten:

* [example_rda.ttl](example_rda.ttl): waarin direct gebruik gemaakt wordt van de officiële RDA-klassen en kenmerken,
* [example_rdanl.ttl](example_rdanl.ttl): waarin klassen en kenmerken gebruikt worden uit de afgeleide [rdanl-ontologie](../profile/rdanl.ttl).
