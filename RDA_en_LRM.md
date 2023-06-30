# RDA en IFLA LRM

RDA maakt het mogelijk om rijker en specifieker te catalogiseren, vereenvoudigt de stap naar het publiceren van bruikbare linked data en laat de metadata dankzij modellering in entiteiten beter aansluiten op een scala aan gebruikswensen.

## IFLA Library Reference Model

RDA is gebaseerd op het IFLA Library Reference Model (LRM). LRM is een model dat concepten en relaties definieert ter modellering van bibliografische beschrijvingen, gericht op het tegemoet kunnen komen aan hedendaagse gebruikerswensen [^1]. Centraal in LRM staan de zogenaamde WEMI-entiteiten, ofwel instanties uit de klasses `Work`, `Expression`, `Manifestation` en `Item`.

* `Work`: Een intellectuele of artistieke creatie op het **conceptuele niveau**. 

* `Expression`: De **vastlegde intellectuele of artistieke realisatie** **van een `Work`, bijvoorbeeld als een tekst, in muzikale of choreografische notatie, etc., of een combinatie van dergelijke vormen. 

* `Manifestation`: Het **productieplan voor de fysieke belichaming** van een `Expression` . 

* `Item`: Een enkele **fysieke belichaming** van een `Manifestation`. 

LRM is niet alleen geschikt voor bijvoorbeeld het beschrijven van bibliografische objecten. De *creaties* waar LRM betrekking op heeft, worden in algemene zin ook wel *resources* of bronnen genoemd. Binnen het bibliotheekdomein gaat het dan om bijvoorbeeld gedrukte en digitale tekstuele bronnen, niet-tekstuele bronnen, handschriften of niet-gepubliceerde bronnen zoals die in bibliotheken aangeschaft worden.


Naast de klasses van de genoemde WEMI-entiteiten kent ondescheidt LRM ook de klasse `Agent` voor de verantwoordelijke voor een *resource*. De klasse `Agent` kent als twee subklasses zde `Person` en de `Collective Agent`. Deze laatste kan ook weer verdeeld worden in de `Corporate Body` en de `Family`.

## RDA

RDA (Resource Description and Access) is een standaard voor data-inhoud gebaseerd op het conceptuele model IFLA LRM. RDA biedt een pakket van data-elementen, richtlijnen en instructies voor het creëren van metadata met betrekking tot *resources* in bibliotheken en erfgoedinstellingen. 

### RDA-elementen
De data-elementen van RDA zijn op te delen in:

* **Klasse-definities** voor de entiteiten van IFLA LRM, zoals gedefinieerd binnen RDA.
* Per klasse toe te passen **kenmerken** (*properties*), voor het beschrijven van relaties tussen entiteiten of het vastleggen van attributen van entiteiten. 
* Verschillende **gecontroleerde begrippenlijsten** (*controlled vocabularies*), in RDA ook *Vocabulary Encoding Schemes* (**VES**) genoemd.

De data-elementen van RDA zijn formeel gedefinieerd in RDF (Resource Description Framework), wat RDA ook zeer geschikt maakt voor linked data-toepassingen. Alle beschrijvingen in RDA zijn dus als zogenaamde linked data-*triples* vast te leggen. De definities van de RDA-elementen, ook in RDF-vorm, zijn te vinden in de [RDA Registry](https://www.rdaregistry.info). De richtlijnen en instructies voor de toepassing van RDA zijn te vinden op de [RDA Toolkit](https://rdatoolkit.org/).

### RDA Implementatie-scenario's

RDA kan ingezet worden in traditionele catalogiseersystemen maar ook binnen linked data-omgevingen. De mogelijkheden van het systeem zijn mede bepalend voor hoe RDA toegepast kan worden. RDA spreekt daarom over verschillende implementatie scenario's. 

In een linked data-omgeving zullen bijvoorkeur IRI's [^2] gebruikt worden om relaties tussen RDA-entiteiten vast te leggen. Dit noemt RDA het 'linked open data'-implementatie scenario. In een catalogiseersysteem zijn IRI's vaak niet voorhanden. Relaties tussen RDA-entiteiten zullen dan gelegd worden via bijvoorbeeld geautoriseerde ingangen (zoals `Douwes Dekker, Eduard (1820-1887)`. Dit is het bibliografische- of '*authority data*'-scenario. Relaties kunnen ook via abstracte *identifiers* uit het informatiesysteem vastgelegd worden. Dit is het relationele- of object georienteerde-scenario.

De al dan niet door het informatiesysteem beperkte keuze voor een implementatiescenario *kan* gevolgen hebben voor de wijze waarop informatie het beste vastgelegd kan worden. Zie hiervoor ook [RDA als linked data](rdf/RDA_als_linkeddata.md).

 
[^1]: De zogenaamde *user tasks*, het helpen van gebruikers bij het vinden, identificeren, selecteren, verkrijgen en ontdekken van de gewenste informatie, zie [IFLA LRM](https://www.ifla.org/wp-content/uploads/2019/05/assets/cataloguing/frbr-lrm/ifla-lrm-august-2017_rev201712.pdf) 
[^2]: IRI's (of URI's) zijn *identifiers* in de vorm van een http(s) -URL, een webadres. Dit is de standaard manier waarop in linked data entiteiten van een *identifier* worden voorzien.
