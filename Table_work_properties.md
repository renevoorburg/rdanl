# Work


| uri | label | opm. | range | recording method | verpl.? | max. | VES/SES | voorbeeld |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **Appellation:** | **elementen die worden gebruikt om de entiteit te identificeren (benoemen)** |||| M | >1 ||| 
| rdaw:P10088	 | 	"*title of work*" | oorspronkelijke titel | `Nomen` | unstructured| M | 1 | | | 
| rdaw:P10223	 | 	"*preferred title of work*" | meest bekende titel, indien gelijk aan "*title of work*" dan alleen "*title of work*" | `Nomen` | unstructured | MA | 1 ||| 
| rdaw:P10086 | "*variant title of work*" || `Nomen` | unstructured| MA | >1 ||| 
|||||||||| 
| 	**Coherence:**	 | 	**het koppelen van de  resource entiteiten van een enkele informatie resource met behulp van "primaire" relaties** |||| M | >1	 ||| 
| rdaw:P10078 | 	"*expression of work*"	|| `Expression` | structured/identifier/iri | M | >1 ||| 
| rdaw:P10072 | "*manifestation of work*" || `Manifestation` | structured/identifier/iri | O | >1 ||| 
|||||||||| 
| **General description:**	| **algemene elementen om de entiteit te beschrijven [basistoepassingsprofiel]** |||||||| 
| rdaw:P10004 | "*category of work*"	| voor o.a. genre | - | unstructured/structured/identifier/iri | M | >1 | Brinkman Trefwoorden thesaurus, Thema [^1] || 
| rdaw:P10365	| "*extension plan*" ||| structured/identifier/iri | M | 1 | RDA Extension Plan http://www.rdaregistry.info/termList/RDAExtensionPlan/?language=nl || 
| rdaw:P10330	 | 	"*note on work*"	|| 	- | unstructured | O | >1 ||| 
| rdaw:P10256	 | "*subject*"	 | 	gebruik waar nodig subproperties met een specifieke range, als Person en Place ||| O	| >1 ||| 
| rdaw:P10353	 | 	"*language of representative expression*" | 	oorspronkelijke taal bij vertalingen, gebruik dit element als niet duidelijk is wat de representatieve expressie is en wel daarover iets wil vastleggen || structured | O | >1 | ISO 639-2 || 
|||||||||| 
| **General relationships:** | 	Algemene elementen die worden gebruikt om relaties van de entiteit te beschrijven [basistoepassingsprofiel]. |||||||| 
| rdaw:P10219	 | 	"*date of work*" || `Timespan` | unstructured/structured/identifier/iri | O | 1	| ISO 8601-1:2019 || 
| rdaw:P10065	 | 	"creator agent of work"	 | gebruik een zo specifiek mogelijke narrow element. Zie tabblad Agent. | `Agent` | structured/identifier/iri | 	M | >1	|| 	NTA, NACO, Corporatiethesaurus | 
| rdaw:P10198	 | 	"related work of work"	| Gebruik een zo specifiek mogelijke narrow element.	 || structured/identifier/iri	 | 	O | >1 ||| 
| rdaw:P10346	 | 	"representative expression" || `Expression` | structured/identifier/iri | O | >1 ||| 


[^1:] [Thema](https://ns.editeur.org/thema/nl)