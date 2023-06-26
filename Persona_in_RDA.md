# Introductie van de 'Persona' binnen RDA

Zoals ook besproken in [RDA als linked data](./rdf/RDA_als_linkeddata.md), kan informatie verloren gaan als van het meest gangbare RDA-implementatiescenario, dat wat gebaseerd is op (geautoriseerde) ingangen, overgestapt wordt op het linked data-implementatiescenario, gebaseerd op IRI's. Dit komt omdat geautoriseerde ingangen, anders dan IRI's, niet zomaar *identifers* zijn maar **betekenisdragende** *identifiers*.

Specifiek speelt dit informatieverlies bij de koppeling tussen `Work`-entiteiten met alternatieve identiteiten van auteurs. Zo is in de volgende RDF, gebaseerd op geautoriseerde ingangen, duidelijk dat `<person_1>` de auteur is van `<work_1>` én van `<work_2>`, maar dat alleen `<work_1>` bekend werd als publicatie onder de auteursnaam "*Lewis Carroll*". 

	<work_1>
		rdaw:authorPerson “Carroll, Lewis” .

	<work_2>
		rdaw:authorPerson “Dodgson, Charles Lutwidge” .

	<person_1>
		rdaa:authorizedAccessPointOfPerson “Dodgson, Charles Lutwidge” ;
		rdaa:authorizedAccessPointOfPerson “Carroll, Lewis” .
		
Als we nu het object van de `rdaw:authorPerson`-relatie vervangen door de IRI `<person_1>`, dan kunnen we deze conclusie niet meer zomaar trekken. We weten dan niet meer welk werk behoort bij "*Lewis Carroll*":

	<work_1>
		rdaw:authorPerson <person_1> .	# range is een Person

	<work_2>
		rdaw:authorPerson <person_1> . # range is een Person

	<person_1>
		rdaa:authorizedAccessPointOfPerson “Dodgson, Charles Lutwidge” ;
		rdaa:authorizedAccessPointOfPerson “Carroll, Lewis” .

Het verlies aan informatie kan ongedaan gemaakt worden door twee `Nomen`-entiteiten te introduceren:

	<work_1>
		rdaw:authorPerson <person_1> ;
		rdaw:relatedNomenOfWork <nomen_1> .

	<work_2>
		rdaw:authorPerson <person_1> ;
		rdaw:relatedNomenOfWork <nomen_2> .

	<person_1>
		rdaa:realIdentityOfPerson <nomen_2> ;
		rdaa:alternateIdentityOfPerson <nomen_1> .

	<nomen_1>
		rdan:accesspointForPersonOf <person_1> ;
		rdan:nomenString “Carroll, Lewis” .

	<nomen_2>
		rdan:accesspointForPersonOf <person_1> ;
		rdan:nomenString “Dodgson, Charles Lutwidge” .

De bibliografische praktijk is vaak niet zo eenvoudig als gepresenteerd in voorgaande voorbeeld, waarbij één identiteit (of alternatieve identiteit) van een auteur in één naam, in één `Nomen-string`, gevat kan worden. In die praktijk zien we dat er behoefte is aan het werken met **clusters van namen per identiteit van een auteur**. Denk daarbij bijvoorbeeld aan alternatieve schrijfwijzen, bijvoorbeeld transliteraties van een naam naar andere schriften. Zo biedt bijvoorbeeld de *Nederlandse Thesaurus van Auteursnamen*, de NTA, in *records* geclusterde sets van auteursnamen, die per *record* behoren bij één **publieke identiteit** van één auteur. Ook *identifiers* zoals die van ISNI of VIAF zijn vaak verbonden aan zo'n publieke identiteit.

Bij de publieke identiteit van een persoon, van een auteur, hoort dus vaak een cluster met meerdere namen. Zo'n publieke identiteit noemen we ook wel een **Persona**. RDA kent geen Persona als een zelfstandige entiteit, maar het is wel mogelijk in RDA om de namen die bij zo'n identiteit horen, te clusteren, om zo op een indirecte wijze een Persona binnen RDA te kunnen weerspiegelen. 

RDA biedt de mogelijkheid om vergelijkbare namen als `Nomen` aan elkaar te verbinden met het `equivalentTo`-kenmerk (`rdan:P80113`) en zo clusters te vormen. Dit is nog geen volledige oplossing voor het werken met de Persona. 

Een praktisch eis is niet alleen het kunnen vastlegen van 'Persona'-Nomenclusters, maar ook dat die clusters in een geautomatiseerde systeem eenvoudig herkend kunnen worden. 

Hiertoe wordt, zoals voorgesteld binnen dit toepassingsprofiel, gebouwd op de RDA-kenmerken `rdaa:P50429` ("*has real identity of Person*") en `rdaa:P500428` ("h*as alternate identity of person*"). Deze kenmerken verwijzen bij de voorgesteld aanpak **alleen naar de centrale naam** (Nomen) in de 'Persona'-cluster. Een 'Persona' van een auteur wordt zo gereflecteerd door deze twee kenmerken gecombineerd met de daaraan gekoppelde Nomen-clusters. De volgende afbeelding illustreert deze aanpak.

![persona](https://github.com/renevoorburg/rdanl/assets/465625/fc7d0820-5911-4790-8017-f48072f4c954)

