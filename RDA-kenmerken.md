# Toe te passen RDA-kenmerken

Toe te passen RDA-kenmerken voor monografieën:

* [voor `Works`](Work-kenmerken.md)
* [voor `Expressions`](Expression-kenmerken.md)
* [voor `Manifestations`](Manifestation-kenmerken.md)
* [voor `Items`](Item-kenmerken.md)

## Leeswijzer

De tabellen met kenmerken zijn opgebouwd uit de volgende kolommen:

* **uri**: Linkt naar de officiële RDA-URI van het element, toont de element-naam met *namespace prefix*.
* **naam**: Toont de Engelstalige *lexical alias*, die ook overeen komt met de naam van het equivalente element in de [`rdanl`-ontologie](rdf/profile).
* **opm.**: Aanvullende informatie over de toepassing van het element, zie ook de definitie en richtlijnen van RDA. In sommige  gevallen wordt aangeraden een zo specifiek mogelijk sub-element te gebruiken. Zie voor hiervoor (als RDF) ook [`rdanl.ttl`](rdf/profile/rdanl.ttl).
* **range**: Aanduiding van de klasse van de entiteit waar het kenmerk naar verwijst. **Let op:** het betreft hier **niet** de `rdf:range` (zie ook [RDA als linked data](rdf/RDA_als_linkeddata.md) ).
* **vastlegging**: De wijze van vastlegging (*recording method*). Bij een verwijzing naar een WEMI-entiteit of `Agent` (of subklasse daarvan), geldt dat gebruik van een IRI of anders een ingang van een geautoriseerde bron de voorkeur verdient. Denk hierbij bijvoorbeeld aan de Nederlandse Thesaurus van Auteursnamen[^1] of de Brinkman-thesaurus[^2].
* **verpl.?**: Is het gebruik van dit element *verplicht* (**M** = *mandatory*), *verplicht indien van toepassing* (**MA** = *mandatatory if applicable*) of *optioneel* (**O**).
* **max.**: Is het element herhaalbaar?
* **waarde**: Richtlijnen ten aanzien van de waarde van het element. Verwijst naar een gecontroleerde waardelijst ('VES', zoals de [RDA Carrier Type](http://www.rdaregistry.info/termList/RDACarrierType/)), een standaard voor structurering van tekenreeksen ('SES', zoals de ISO 639.2-taalcodes) of geeft (tussen " " ) een voorbeeld van een geschikte waarde.

## Achtergrond

De overzichten van de toe te passen kenmerken zijn gebaseerd op de richtlijnen van RDA ten aanzien van de e**isen van effectieve beschrijving** [^3].

* Het voldoet aan de eisen van een **coherente beschrijving**[^4] van een bron 
* En ten minste één van zijn entiteiten voldoet aan de **minimumbeschrijving** gesteld binnen RDA 
* Andere elementen kunnen toegevoegd worden aan de beschrijving van één of meer entiteiten die nuttig worden geacht voor de identificatie of toegang. 
* Beschrijving van andere entiteiten kunnen toegevoegd worden aan de coherente beschrijving van een resource die nuttig geacht worden voor de identificatie of toegang. 

## Zie ook

TODO: oa. voorbeeld Sita


[^1]: Zie [Nederlandse Thesaurus van Auteurnamen](http://data.bibliotheken.nl/id/dataset/persons). Hoewel deze nu nog niet naar RDA klassen omgezet is kan deze gebruikt voor `Persons` (op indirecte wijze) of (direct) voor de centrale `Nomen` van een [Persona](Persona_in_RDA.md).
[^2]: Zie [Brinkman-thesaurus](http://data.bibliotheken.nl/id/dataset/brinkman).
[^3]: Zie [RDA Toolkit - Effective description](https://access.rdatoolkit.org/Guidance/Index).
[^4]: {coherente bescvhrijving}
