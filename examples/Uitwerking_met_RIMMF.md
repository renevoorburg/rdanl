# Uitwerking met RIMMF


*Ter illustratie* de volgende beschrijving van een `Work` met bijbehorende `Expressions` en `Manifestations` zoals gegeneerd door RIMMF [^1]. Hierbij wordt een traditioneel implementatiescenario gevolgd, gebaseerd op (geautoriseerde) ingangen. De identifiers zijn door RIMMF gegeneerd. 

In dit voorbeeld van RIMMF wordt niet de voorgestelde [Persona-aanpak](Persona_in_RDA.md) gevolgd.  Zie de [uitwerking in RDF](../rdf/examples) voor een beschrijving in lijn met de voorgestelde aanpak.




## Work

| kenmerk | waarde |
| --- | --- |
| a	| rdanl:Work |
| rdanl:identifierForWork | "kob105" |
| rdanl:preferredTitleOfWork | "Aan den weg der vreugde" |
| rdanl:variantTitleOfWork | "Een vrouw van het noorden" |
| rdanl:authorizedAccessPointForWork | "Couperus, Louis (1863-1923 \| Aan den weg der vreugde" |
| rdanl:variantAccessPointForWork | "Couperus, Louis (1863-1923 \| Een vrouw van het noorden" |
| rdanl:categoryOfWork | "romans en novellen" |
| rdanl:extensionPlan | "static plan" |
| rdanl:expressionOfWork | "Couperus, Louis (1863-1923) \| Aan den weg der vreugde \| text \| Dutch" |
| rdanl:authorPerson | "Couperus, Louis (1863-1923)" |
| rdanl:dateOfWork | "1908" |


## Expression



| kenmerk | waarde |
| --- | --- |
| a	| rdanl:Expression |
| rdanl:identifierForExpression | "kob103" |
| rdanl:authorizedAccessPointForExpression | "Couperus, Louis (1863-1923) \| Aan den weg der vreugde \| text \| Dutch" |
| rdanl:workExpressed | "Couperus, Louis (1863-1923 \| Aan den weg der vreugde" |
| rdanl:manifestationOfExpression | "Aan den weg der vreugde \| L.J. Veen \| [1908] \| volume " |
| rdanl:languageOfExpression | "Dutch" |
| rdanl:contentType | "text" |

| kenmerk | waarde |
| --- | --- |
| a	| rdanl:Expression |
| rdanl:identifierForExpression | "kob109" |
| rdanl:authorizedAccessPointForExpression | "Couperus, Louis (1863-1923) \| Een vrouw van het noorden \| text \| Dutch" |
| rdanl:workExpressed | "Couperus, Louis (1863-1923 \| Aan den weg der vreugde" |
| rdanl:preferredTitleOfExpression | "Een vrouw van het noorden" |
| rdanl:manifestationOfExpression | "Een vrouw van het noorden \| Pandorra \| [1999] \| volume \| 2e dr" |
| rdanl:languageOfExpression | "Dutch" |
| rdanl:contentType | "text" |

| kenmerk | waarde |
| --- | --- |
| a	| rdanl:Expression |
| rdanl:identifierForExpression | "kob111" |
| rdanl:authorizedAccessPointForExpression | "Am Wege der Freude \| text \| German \| Otten, Else (1873-1931)"  |
| rdanl:workExpressed | "Couperus, Louis (1863-1923 \| Aan den weg der vreugde" |
| rdanl:preferredTitleOfExpression | "Am Wege der Freude" |
| rdanl:manifestationOfExpression | "Am Wege der Freude \| Ulstein \| [1920] \| volume" |
| rda:nl:translatorPerson | "Otten, Else (1873-1931)" |
| rdanl:languageOfExpression | "German" |
| rdanl:contentType | "text" |

## Manifestation

| kenmerk | waarde |
| --- | --- |
| a	| rdanl:Manifestation |
| rdanl:identifierForManifestation | "kob102" |
| rdanl:expressionManifested | "Couperus, Louis (1863-1923) \| "Aan den weg der vreugde \| text \| Dutch" |
| rdanl:authorizedAccessPointForManifestation | "Aan den weg der vreugde \| L.J. Veen \| [1908] | volume" |
| rdanl:titleProper | "Aan den weg der vreugde" |
| rdanl:statementOfResponsibilityRelatingToTitleProper | "door Louis Couperus" | rdanl:manufactureStatement | "Nijmegen : G.J. Thieme" |
| rdanl:nameOfManufacturer | "G.J. Thieme" | 
| rdanl:placeOfManufacture | "Nijmegen" |
| rdanl:publicationStatement | "Amsterdam : L.J. Veen, [1908]" |
| rdanl:nameOfPublisher | "L.J. Veen" |
| rdanl:placeOfPublication | "Amsterdam" |
| rdanl:dateOfPublication | "[1908]" |
| rdanl:modeOfIssuance | "single unit" | 
| rdanl:extentOfManifestation | "207 pagina's" |
| rdanl:dimensions | "21 cm" |
| rdanl:carrierType | "volume" |
| rdanl:mediaType | "unmediated" |

| kenmerk | waarde |
| --- | --- |
| a	| rdanl:Manifestation |
| rdanl:identifierForManifestation | "kob108" |
| rdanl:expressionManifested | "Couperus, Louis (1863-1923) \| Een vrouw van het noorden \| text \| Dutch" |
| rdanl:authorizedAccessPointForManifestation | "Een vrouw van het noorden \| Pandora \| [1999] \| volume \| 2e dr" |
| rdanl:titleProper | "Een vrouw van het noorden" |
| rdanl:variantTitleOfManifestation | "Aan den weg der vreugde" |
| rdanl:statementOfResponsibilityRelatingToTitleProper | "Louis Couperus" | rdanl:manufactureStatement | "Nijmegen : G.J. Thieme" |
| rdanl:nameOfManufacturer | "G.J. Thieme" | 
| rdanl:placeOfManufacture | "Nijmegen" |
| rdanl:publicationStatement | "Amsterdam : L.J. Veen, [1908]" |
| rdanl:nameOfPublisher | "L.J. Veen" |
| rdanl:placeOfPublication | "Amsterdam" |
| rdanl:designationOfEdition | "2e dr" |
| rdanl:dateOfPublication | "[1908]" |
| rdanl:modeOfIssuance | "single unit" | 
| rdanl:extentOfManifestation | "158 pagina's" |
| rdanl:dimensions | "18 cm" |
| rdanl:carrierType | "volume" |
| rdanl:mediaType | "unmediated" |


| kenmerk | waarde |
| --- | --- |
| a	| rdanl:Manifestation |
| rdanl:identifierForManifestation | "kob08" |
| rdanl:expressionManifested | "Am Wegen der Freude \| Ullstein \| [1920] \| volume" |
| rdanl:authorizedAccessPointForManifestation | "Aan den weg der vreugde \| L.J. Veen \| [1908] \| volume" |
| rdanl:titleProper | "Am Wege der Freude" |
| rdanl:titleOfSeries | "Ullstein-Bücher" |
| rdanl:statementOfResponsibilityRelatingToTitleProper | "von Louis Couperus" |
| rdanl:statementOfResponsibilityRelatingToTitleProper | "autor. Übertr. aus dem Holländischen von Else Otten" | 
| rdanl:otherTitleInformation | "Roman" |
| rdanl:publicationStatement | "Amsterdam : L.J. Veen, [1908]" |
| rdanl:nameOfPublisher | "Ullstein" |
| rdanl:placeOfPublication | "Berlin" |
| rdanl:dateOfPublication | "[1920]" |
| rdanl:modeOfIssuance | "single unit" | 
| rdanl:extentOfManifestation | "278 pagina's" |
| rdanl:dimensions | "15 cm" |
| rdanl:carrierType | "volume" |
| rdanl:mediaType | "unmediated" |


[^1]: [RIMMF](https://www.rimmf.com/) - RDA in Many Metadata Formats" - is een hulpmiddel voor MS Windows voor het (leren) werken met RDA.

