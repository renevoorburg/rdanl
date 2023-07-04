# Toe te passen RDA-kenmerken voor `Manifestation`-entiteiten

Zie ook overzicht [RDA-kenmerken](RDA-kenmerken.md).


| uri | naam | opm. | range | vastlegging [^1] | verpl.? [^2] | max. | waarde |
| --- | --- | --- | --- | --- | --- | --- | --- |
||
|| *Appellation:* | *elementen om de entiteit te benoemen:* ||| M | >1 |
| rdam:P30156 |	**titleProper** | letterijk overnemen uit de bron zoals het er staat, ook eventuele tikfouten<br>vastleggen als een zin<br>hoofdlettergebruik zoals in de taal van de titel gebruikelijk is<br>bij fouten de gecorrigeerde titel opnemen als **variantTitleOfManifestation** | `Nomen` | U | M | 1 |
| rdam:P30128	 | **variantTitleOfManifestation** | zie bij **titleProper** | `Nomen` | U | O | >1 |
| rdam:P30004 | **identifierForManifestation** | systeemonafhankelijke identifier, indien mogelijk persistent, dit is niet de identifier van het metadata record | `Nomen` | Id |	MA | >1 | "ISBN: 9025499678" |
||
|| *Coherence:* | *primaire relaties tussen entiteiten:* ||| M | >1 |
| rdam:P30139 | **expressionManifested** || `Expression` | S / Id / IRI | M | >1 |
| rdam:P30135 | **workManifested** || `Work` | S / Id / IRI | O | 1 |
| rdam:P30103	|	**exemplarOfManifestation** || `Item` | S / Id / IRI | M | >1 |
||
||	*General description:*	| *algemene beschrijving (basistoepassingsprofiel):* |
| rdam:P30002	| **mediaType** |	||	S / IRI | M | 1 | RDA Media Type [^3] |
| rdam:P30003	| **modeOfIssuance** ||| S / IRI | M | 1 | RDA Mode of Issuance [^4] |
| rdam:P30335	| **categoryOfManifestation** | TODO: zijn dit de vormtrefwoorden? || U / S / Id / IRI | O | 1 | Brinkman Trefwoorden thesaurus, Thema (https://ns.editeur.org/thema/nl) |
| rdam:P30142	| **otherTitleInformation** | gebruik voor ondertitel || U | O | >1 |
| rdam:P30105	| **statementOfResponsibilityRelatingToTitleProper** | TODO waarvoor? / overnemen uit de resource  || U | MA | 1 |
| rdam:P30280 | **manifestationCopyrightStatement** | datum en bij wie de copyright berust, overnemen uit de bron<br>als alleen een datum bekend is, gebruik dan **copyrightDate** || U | MA | 1 |
| rdam:P30007 | **copyrightDate**	| datum copyright zoals vermeld in de bron || U | MA | 1 | ISO 8601-1:2019 |
||
| rdam:P30107 | **editionStatement** |	een vermelding die een editie identificeert waartoe een manifestatie behoort<br>wordt samengesteld uit de volgende elementen: **designationOfEdition**, **designationOfNamedRevisionOfEdition**, **statementOfResponsibilityRelatingToEdition**, **statementOfResponsibilityRelatingToNamedRevisionOfEdition**, als deze elementen apart genoteerd kunnen worden en van toepassing zijn, gebruik deze elementen, indien de informatie als geheel wordt opgenomen, gebruik dan dit element |
| rdam:P30133 | **designationOfEdition** | overnemen uit de bron || U | MA | >1 |
| rdam:P30132 | **designationOfNamedRevisionOfEdition** ||| U | MA | >1 |
| rdam:P30121 | **statementOfResponsibilityRelatingToEdition** ||| U | MA | 1 |
| rdam:P30118 | **statementOfResponsibilityRelatingToNamedRevisionOfEdition** ||| U | MA | 1 |
||
| rdam:P30001 | **carrierType** |	||	S / Id / IRI | M | 1 | RDA Carrier Type [^5] |
| rdam:P30182 | **extentOfManifestation** | o.a. aantal pagina's ||S| M | 1 |
| rdam:P30169	 | **dimensions** |	neem op wat nodig is voor het magazijn van fysieke bronnen,  maten in cm., tenzij hoogte < 10 cm, dan in mm. || U / S (?) | MA | >1 |
| rdam:P30137 | **noteOnManifestation** ||| U | O | >1 |
| rdam:P30453 | **illustrativeContent**	 | een indicatie van de soorten expressies van beeldcontent die de hoofd-expressies aanvullen || S / IRI | MA | >1 | RDA Illustrative Content [^6] |
| rdam:P30309 | **typeOfBinding** ||| S / IRI | O | >1 | RDA Type of Binding [^7] |
| rdam:P30160 | **termOfAvailability** | o.a. prijs || U | O | >1 |
| rdam:P30111 | **publicationStatement** | wordt samengesteld uit de volgende subelementen: **placeOfPublication**, name of publisher, date of publication. Als deze elementen apart genoteerd kunnen worden en van toepassing zijn, gebruik deze elementen. Indien de informatie als geheel wordt opgenomen, gebruik dan dit superelement || S | O | 1 | "Spijkenisse : Hageboek, 1998" |
||
|| *General relationships:* | *algemene elementen om relaties van de entiteit te beschrijven (basistoepassingsprofiel):* |
| rdam:P30088 | **placeOfPublication**	| zoals vermeld in de bron. Indien niet bekend, geef aan: "Plaats van uitgave niet vastgesteld" in element **noteOnManifestation**.<br>Zet een plaats tussen vierkante haken als de bron van de informatie niet de `Manifestation` zelf is. [ TODO: willen we dit wel? -> Indien mogelijk herhaal dit element om een identifier of iri van een plaats te geven. Herhaal dit element om een land van uitgave te vermelden, het liefst gestructureerd, met identifier of iri. Indien de identifier van een plaats het land duidelijk aangeeft, dan is een land van uitgave niet nodig] | `Place` | U / Id / IRI | MA | >1 |
| rdam:P30083 | **publisherAgent** | overnemen uit de bron | `Agent` | U / Id / IRI | MA | >1 |
| rdam:P30011 | **dateOfPublication** | indien onbekend, geen datum, jaar of periode wanneer publicatie kan hebben plaatsgevonden | `Timespan` | U / S / Id / IRI | M | 1 | ISO 8601-1:2019 |
| rdam:P30321 | **contributorAgentOfStillImage** || `Agent` | U / S / Id / IRI | O | >1 | NTA [^8] , NACO [^9] , Corporatiethesaurus [^10] |
| rdam:P30328 | **contributorAgentOfText** || `Agent` | U / S / Id / IRI | O | >1 | NTA [^8] , NACO [^9] , Corporatiethesaurus [^10] |
| rdam:P30157 |	**titleOfSeries** | letterlijk overnemen uit de bron, vastleggen als een zin<br> Hoofdlettergebruik zoals in de taal van de titel gebruikelijk is. |`Nomen` | U | MA | >1 |
| rdam:P30048	 | **relatedManifestationOfManifestation** || `Manifestation` | U / S / Id / IRI | O | >1 |
||
||	*Special description:* | *Gespecialiseerde elementen om de entiteit te beschrijven:* |
| rdam:P30096 | **encodingFormat** | wijze waarop digitale inhoud gecodeerd is || U / S / IRI | MA | >1 | "html" |
| rdam:P30018 | **fileType** ||| U / S / IRI  | O | 1 | RDA File Type [^11] |
| rdam:P30183 | **fileSize** |||	U | O | 1 |
| rdam:P30165 | **numberingOfSequence**	| overnemen uit de bron || U | MA | 1 |
| rdam:P30454	 | **soundContent** | indicatie van de aanwezigheid of afwezigheid van geluid [^12] || U | MA | >1 |
| rdam:P30456 | **colourContent** | indicatie van de aanwezigheid van kleur of grijsschakeringen [^12] || U | MA | >1 |
| rdam:P30452 |	**accessibilityContent** | indicatie van de soorten expressies die alternatieve zintuiglijke modi bieden om de hoofd-expressie waar te nemen [^12 ]|| U | MA | >1 |


[^1]: Vastlegging / *Recording method*, volgens <br>**U**: "unstructured"<br>**S**: "structured"<br>**Id**: "identifier" <br>**IRI**: IRI.
[^2]: Verplicht veld?, volgens <br>**M**: "*Must* / Verplicht"<br>**MA**: "*Must if applicable* / Verplicht indien van toepassing"<br>**O**: "*Optional* / Optioneel" 
[^3]: Zie [RDA Media Type](http://www.rdaregistry.info/termList/RDAMediaType/).
[^4]: Zie [RDA Mode of Issuance](http://www.rdaregistry.info/termList/ModeIssue/).
[^5]: Zie [RDA Carrier Type](http://www.rdaregistry.info/termList/RDACarrierType/).
[^6]: Zie [RDA Illustrative Content](http://www.rdaregistry.info/termList/IllusContent/).
[^7]: Zie [RDA Type of Binding](http://www.rdaregistry.info/termList/RDATypeOfBinding/).
[^8]: Zie [Nederlandse Thesaurus van Auteursnamen (NTA)](http://data.bibliotheken.nl/id/dataset/persons).
[^9]: Zie [NACO - Name Authority Cooperative Program](https://www.loc.gov/aba/pcc/naco/). 
[^10]: Zie [Corporatiethesaurus](http://data.bibliotheken.nl/id/dataset/corps).
[^11]: Zie [RDA File Type](http://rdaregistry.info/termList/fileType).
[^12: In 2025 wordt de wet m.b.t. digitale toegankelijkheid van kracht. Uitgevers worden geacht gegevens daarover aan te leveren. Het is van belang deze op te nemen in de metadata.
