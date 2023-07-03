# Work



| uri | naam | opm. | range | vastlegging [^1] | verpl.? [^2] | max. | waarde |
| --- | --- | --- | --- | --- | --- | --- | --- |
||||||||| 
|| *Appellation:* | *elementen om de entiteit te benoemen:* ||| M | >1 ||
| [rdaw:P10088](http://rdaregistry.info/Elements/w/P10088) | 	**titleOfWork** | oorspronkelijke titel | `Nomen` | U | M | 1 |
| [rdaw:P10223](http://rdaregistry.info/Elements/w/P10223)	 | 	**preferredTitleOfWork** | meest bekende titel, alleen indien anders dan **titleOfWork** | `Nomen` | U | MA | 1 |
| [rdaw:P10086](http://rdaregistry.info/Elements/w/P10086) | **variantTitleOfWork** || `Nomen` | U| MA | >1 | 
||
|| *Coherence:* | *primaire relaties tussen entiteiten:* ||| M | >1 |
| [rdaw:P10078](http://rdaregistry.info/Elements/w/P10078) | 	**expressionOfWork**	|| `Expression` |  S / Id / IRI | M | >1 |
| [rdaw:P10072](http://rdaregistry.info/Elements/w/P10072) | **manifestationOfWork** || `Manifestation` | S / Id / IRI | O | >1 |
||
|| *General description:*	| *algemene beschrijving (basistoepassingsprofiel):* |
| [rdaw:P10004](http://rdaregistry.info/Elements/w/P10004) | **categoryOfWork**	| voor o.a. genre | - | U / S / Id / IRI | M | >1 | bijvoorbeeld:<br>Brinkman Trefwoorden thesaurus [^3] <br>Thema [^4] |
| [rdaw:P10365](http://rdaregistry.info/Elements/w/P10365)	| **extensionPlan** || - | S / Id / IRI | M | 1 | bijvoorbeeld: "static plan",<br>zie RDA Extension Plan [^5] | 
| [rdaw:P10330](http://rdaregistry.info/Elements/w/P10330)	 | 	**noteOnWork**	|| 	- | U | O | >1 |
| [rdaw:P10256](http://rdaregistry.info/Elements/w/P10256)	 | **subject**	 | 	gebruik waar nodig subproperties met een specifieke range, als Person en Place ||| O	| >1 | bijvoorbeeld: <br>Brinkman Trefwoorden Thesaurus [^3] |
| [rdaw:P10353](http://rdaregistry.info/Elements/w/10353)	 | 	**languageOfRepresentativeExpression** | oorspronkelijke taal (bij vertalingen), gebruik als representatieve expressie niet aanwijsbaar || S | O | >1 | ISO 639-2 |
||
| | *General relationships:* | *algemene elementen om relaties van de entiteit te beschrijven (basistoepassingsprofiel):* |
| [rdaw:P10219](http://rdaregistry.info/Elements/w/P10219)	 | 	**dateOfWork** || `Timespan` |  U / S / Id / IRI | O | 1 | ISO 8601-1:2019 | 
| [rdaw:P10065](http://rdaregistry.info/Elements/w/P10065)	 | 	**creatorAgentOfWork** | gebruik een zo specifiek mogelijke narrow element. Zie tabblad Agent. | `Agent` | S / Id / IRI | M | >1 || NTA, NACO, Corporatiethesaurus | 
| [rdaw:P10198](http://rdaregistry.info/Elements/w/P10198)	 | 	**relatedWorkOfWork**	| gebruik een zo specifiek mogelijke narrow element | `Work` | S / Id / IRI	 | O | >1 |
| [rdaw:P10346](http://rdaregistry.info/Elements/w/P10346)	 | 	**representativeExpression** || `Expression` | S / Id / IRI | O | >1 | 


[^1]: Vastlegging / *Recording method*, volgens <br>**U**: "unstructured"<br>**S**: "structured"<br>**Id**: "identifier" <br>**IRI**: IRI.
[^2]: Verplicht veld?, volgens <br>**M**: "*Must* / Verplicht"<br>**MA**: "*Must if applicable* / Verplicht indien van toepassing"<br>**O**: "*Optional* / Optioneel" 
[^3]: Zie [Brinkman Trefwoorden Thesaurus](http://data.bibliotheken.nl/id/dataset/brinkman).
[^4]: Zie [Thema](https://ns.editeur.org/thema/nl).
[^5]: Zie [RDA Extension Plan](http://www.rdaregistry.info/termList/RDAExtensionPlan/). 
