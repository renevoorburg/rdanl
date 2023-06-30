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

De data-elementen van RDA zijn op te delen in:

* **Klasse-definities** voor de entiteiten van IFLA LRM.
* Per klasse toe te passen **kenmerken** (*properties*), voor het beschrijven van relaties tussen entiteiten of het vastleggen van attributen. 
* Verschillende **gecontroleerde begrippenlijsten** (*controlled vocabulairies*), in RDA ook *Vocabulary Encoding Schemes* (**VES**) genoemd.

De data-elementen van RDA zijn formeel gedefinieerd in RDF (Resource Description Framework), wat RDA ook zeer geschikt maakt voor linked data-toepassingen. De definities van de RDA-elementen zijn te vinden in de [RDA Registry](https://www.rdaregistry.info). 

 
[^1]: De zogenaamde *user tasks*, het helpen van gebruikers bij het vinden, identificeren, selecteren, verkrijgen en ontdekken van de gewenste informatie, zie [IFLA LRM](https://www.ifla.org/wp-content/uploads/2019/05/assets/cataloguing/frbr-lrm/ifla-lrm-august-2017_rev201712.pdf) 
