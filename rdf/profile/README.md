# Toepassingsprofiel RDANL in RDF

Het toepassingsprofiel RDANL is een op RDA gebaseerde ontologie in RDF-vorm. 

Zie: [`rdanl.ttl`](rdanl.ttl).

Het profiel is opgesteld aan de hand van de volgende principes:

* De URI's van de klassen en kenmerken zijn ontworpen voor bruikbaarheid door mensen. Daartoe zijn ze gebaseerd op de zogenaamde lexical aliasses van RDA.
* De URI's zijn gedefinieerd in één namespace,  `http://data.bibliotheken.nl/rdanl#`, bij voorkeur met `rdanl` als de namespace prefix.
* Klassen zijn in RDANL gedefinieerd via `rdfs:subClassOf` van de overeenkomstige klasse in RDA.
* Kenmerken zijn in RDANL gedefinieerd via `rdfs:subPropertyOf` van het overeenkomstige kenmerk in RDA.
* Ter ondersteuning van de Persona-benadering is kenmerk `rdanl:relatedPersonaOfWork` toegevoegd, een `rdfs:subPropertyOf` van `rdanl:relatedNomenOfWork`.



