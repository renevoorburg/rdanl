# Toe te passen RDA-kenmerken voor `Manifestation`-entiteiten

Zie ook overzicht [RDA-kenmerken](RDA-kenmerken.md).


| uri | naam | opm. | range | vastlegging [^1] | verpl.? [^2] | max. | waarde |
| --- | --- | --- | --- | --- | --- | --- | --- |
|| 
|| *Appellation:* | *elementen om de entiteit te benoemen:* ||| M | >1 |
| rdam:P30156 |	**titleProper** | letterijk overnemen uit de bron zoals het er staat, ook eventuele tikfouten<br>vastleggen als een zin<br>hoofdlettergebruik zoals in de taal van de titel gebruikelijk is<br>bij fouten de gecorrigeerde titel opnemen als **variantTitleOfManifestation** | `Nomen` | U | M | 1 |
| rdam:P30128	 | **variantTitleOfManifestation** | zie bij **titleProper** | `Nomen` |	U | O | >1	|
| rdam:P30004 | **identifierForManifestation** | systeemonafhankelijke identifier, indien mogelijk persistent, dit is niet de identifier van het metadata record | `Nomen` | identifier	|	MA	|	>1	| "ISBN: 9025499678" |
||
|| *Coherence:* | *primaire relaties tussen entiteiten:* ||| M | >1 |
| rdam:P30139 | **expressionManifested** || `Expression` | S / Id / IRI | M | >1 |
| rdam:P30135 | **workManifested** || `Work` | S / Id / IRI | O | 1 |
| rdam:P30103	|	**exemplarOfManifestation** || `Item` | S / Id / IRI | M | >1 |
||
||	*General description:*	| *algemene beschrijving (basistoepassingsprofiel):* |
| rdam:P30002	|	media type	|		|		|	structured/iri	|	M	|	1	|	RDA Media Type http://www.rdaregistry.info/termList/RDAMediaType/?language=nl	|
|	rdam:P30003	|	mode of issuance	|		|		|	structured/iri	|	M	|	1	|	RDA Mode of Issuance http://www.rdaregistry.info/termList/ModeIssue/?language=nl	|
|	rdam:P30335	|	category of manifestation	|	Gebruik zoveel mogelijk een gecontroleerde waardelijst.	|		|	unstructured/structured/identifier/iri	|	O	|	1	|	Brinkman Trefwoorden thesaurus, Thema (https://ns.editeur.org/thema/nl)	|
|	rdam:P30142	|	other title information	|		|		|	unstructured	|	O	|	>1	|	ondertitel	|
|	rdam:P30105	|	statement of responsibility relating to title proper	|	Overnemen uit de resource.	|		|	unstructured	|	MA	|	1	|		|
|	rdam:P30280	|	manifestation copyright statement	|	Overnemen uit de resource. Datum en bij wie de copyright berust. Als alleen een datum bekend is, gebruik dan copyright date.	|		|	unstructured	|	MA	|	1	|		|
|	rdam:P30007	|	copyright date	|	"Overnemen uit de resource. Datum copyright "	|		|	unstructured	|	MA	|	1	|	ISO 8601-1:2019	|
|	rdam:P30107	|		|	Dit element wordt samengesteld uit de volgende subelementen: rdam:P30133, rdam:P30132, rdam:P30121, rdam:P30118. Als deze elementen apart genoteerd kunnen worden en van toepassing zijn, gebruik deze elementen. Indien de informatie als geheel wordt opgenomen, gebruik dan dit superelement.	|		|		|		|		|		|
|	rdam:P30133	|	designation of edition	|	Overnemen uit de resource.	|		|	unstructured	|	MA	|	>1	|		|
|	rdam:P30132	|	designation of named revision of edition	|		|		|	unstructured	|	MA	|	>1	|		|
|	rdam:P30121	|	statement of responsibility relating to edition	|		|		|	unstructured	|	MA	|	1	|		|
|	rdam:P30118	|	statement of responsibility relating to named revision of edition	|		|		|	unstructured	|	MA	|	1	|		|
|		|		|		|		|		|		|		|		|
|	rdam:P30001	|	carrier type	|		|		|	structured/iri	|	M	|	1	|	RDA Carrier Type http://www.rdaregistry.info/termList/RDACarrierType/	|
|	rdam:P30182	|	extent of manifestation	|	o.a. aantal pagina's	|		|	structured	|	M	|		|		|
|	rdam:P30169	|	dimensions	|	Neem in dit element wat nodig is voor het magazijn van fysieke resources. Noteer de maten in cm. Indien de hoogte kleiner is dan 10 centimeter, gebruik dan mm om de maten aan te geven.	|		|	unstructured	|	MA	|	>1	|		|
|	rdam:P30137	|	note on manifestation	|		|		|	unstructured	|	O	|	>1	|		|
|	rdam:P30453	|	illustrative content	|		|		|	structured/iri	|	MA	|	>1	|	RDA Illustrative Content http://www.rdaregistry.info/termList/IllusContent/?language=nl	|
|	rdam:P30309	|	type of binding	|		|		|	structured/iri	|	O	|	>1	|	RDA Type of Binding http://www.rdaregistry.info/termList/RDATypeOfBinding/?language=nl	|
|	rdam:P30160	|	term of availability	|	o.a. prijs	|		|	unstructured	|	O	|	>1	|		|
|		|		|		|		|		|		|		|		|
|		|		|		|		|		|		|		|		|
|	rdam:P30111	|		|	Dit elemement wordt samengesteld uit de volgende subelementen: place of publication, name of publisher, date of publication. Als deze elementen apart genoteerd kunnen worden en van toepassing zijn, gebruik deze elementen. Indien de informatie als geheel wordt opgenomen, gebruik dan dit superelement.	|		|	structured	|	O	|	1	|	Spijkenisse : Hageboek, 1998	|
|		|		|		|		|		|		|		|		|
|	General relationships	|	Algemene elementen die worden gebruikt om relaties van de entiteit te beschrijven [basistoepassingsprofiel].	|		|		|		|		|		|		|
|		|		|		|		|		|		|		|		|
|	rdam:P30088	|	place of publication	|	Neem over zoals opgenomen in de resource. Indien niet bekend, geef het volgende aan: "Plaats van uitgave niet vastgesteld" in een element 'note of manifestation'. Zet een plaats tussen vierkante haken als de bron van de informatie niet de Manifestation zelf is. Indien mogelijk herhaal dit element om een identifier of iri van een plaats te geven. Herhaal dit element om een land van uitgave te vermelden, het liefst gestructureerd, met identifier of iri. Indien de identifier van een plaats het land duidelijk aangeeft, dan is een land van uitgave niet nodig.	|	place	|	unstructured/identifier/iri	|	MA	|	>1	|		|
|	rdam:P30083	|	publisher agent	|	Overnemen uit de resource.	|	nomen	|	unstructured	|	MA	|	>1	|		|
|	rdam:P30011	|	date of publication	|	Indien onbekend, geef een datum of jaar range wanneer het werk kan zijn ontstaan.	|	timespan	|	unstructured/structured/identifier/iri	|	M	|	1	|	ISO 8601-1:2019	|
|	rdam:P30321	|	contributorAgentOfStillImage	|	Gebruik zoveel mogelijk de ingang van een authority record.	|	agent	|	unstructured/structured/identifier/iri	|	O	|	>1	|	NTA, NACO, Corporatiethesaurus	|
|	rdam:P30328	|	contributorAgentOfText	|	Gebruik zoveel mogelijk de ingang van een authority record.	|	agent	|	unstructured/structured/identifier/iri	|	O	|	>1	|	NTA, NACO, Corporatiethesaurus	|
|	rdam:P30157	|	title of series	|	Inhoudelijk overnemen uit de resource zoals het er staat. Titel vastleggen zoals een zin. Hoofdlettergebruik zoals in de taal van de titel gebruikelijk is. De relatie 	|	nomen	|	unstructured	|	MA	|	>1	|		|
|	rdam:P30048	|	related manifestation of manifestation	|		|	manifestation	|	unstructured/structured/identifier/iri	|	O	|	>1	|		|
|		|		|		|		|		|		|		|		|
|	Special description	|		|		|		|		|		|		|		|
|	rdam:P30096	|	encodingFormat	|		|		|	structured	|	M	|	>1	|		|
|	rdam:P30018	|	fileType	|		|		|	structured	|	O	|	1	|		|
|	rdam:P30183	|	file size	|		|		|	unstructured	|	O	|	1	|		|
|	rdam:P30165	|	numbering of sequence	|	Overnemen uit de resource.	|		|	unstructured	|	MA	|	1	|		|
|	rdam:P30454	|	sound content	|	In 2025 wordt de wet m.b.t. digitale toegankelijkheid van kracht. Uitgevers worden geacht gegevens daarover aan te leveren. Het is van belang deze op te nemen in de metadata.	|		|	unstructured	|	MA	|	>1	|		|
|	rdam:P30456	|	colour content	|	In 2025 wordt de wet m.b.t. digitale toegankelijkheid van kracht. Uitgevers worden geacht gegevens daarover aan te leveren. Het is van belang deze op te nemen in de metadata.	|		|	unstructured	|	MA	|	>1	|		|
|	rdam:P30452	|	accessibility content	|	In 2025 wordt de wet m.b.t. digitale toegankelijkheid van kracht. Uitgevers worden geacht gegevens daarover aan te leveren. Het is van belang deze op te nemen in de metadata.	|		|	unstructured	|	MA	|	>1	|		|
