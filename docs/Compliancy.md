---
layout: page-with-side-nav
title: Compliancy Prefill eFormulierenservices
---
# Compliancy Prefill eFormulierenservices

|   |   |
| --- | --- |
| Testsetversie: | 1.1 |
| Status | In gebruik |
| Datum laatst gewijzigd | 19 mei 2015 |

## Inleiding
De standaard [Prefill eFormulierenservices 1.0](documenten/Koppelvlakspecificatie_-_prefill_eFormulieren_v1.00.pdf) is op 2 april 2014 formeel vastgesteld door de StUF Regiegroep. Daarmee heeft de standaard de status ‘In gebruik’ en wordt gemeenten aanbevolen om deze standaard te gebruiken.

Voor een juiste toepassing van de standaard Prefill eFormulierenservices worden door VNG Realisatie compliancy instrumenten ontwikkeld met als doel interoperabiliteitsproblemen tussen applicaties bij gemeenten preventief te verminderen. In de paragraaf 2.1 ”Wanneer is een softwareproduct compliant” is aangegeven wanneer een softwareproduct compliant is aan de Prefill eFormulierenservices 1.0.

VNG Realisatie adviseert gemeenten bij aanschaf van software die moet voldoen aan deze standaard gebruik te maken van de [Handreiking Levering en Acceptatievoorwaarden ICT](documenten/130131_Leverings_en_acceptatievoorwaarden_versie_2_Definitief.pdf). Daarin zijn voorwaarden opgenomen over het gebruik van compliancy instrumenten.

Op 25 juni 2014 heeft VNG Realisatie de technische professionals van leveranciers tekst en uitleg gegeven over het deze testset en het gebruik van het StUF Testplatform. Onderliggend document maakt deel uit van de compliancy instrumenten van VNG Realisatie.

## Doel van document
Doel van dit document is het definiëren van een standaard testset voor het testen van koppelingen die gebaseerd zijn op de Prefill eFormulierenservices 1.0. Deze testset beschrijft de tests die minimaal voorafgaand aan het in productie nemen van (aangepaste of nieuwe) software door de betreffende softwareleverancier uitgevoerd moeten worden.

De testen dienen uitgevoerd te worden conform deze beschrijving en met behulp en conform de voorwaarden van het StUF Testplatform. Voor gebruik van deze testset is een abonnement nodig op het StUF Testplatform nodig. Organisaties dienen zich, voor zover ze nog geen abonnement hebben, aan te melden. Zie: [www.stuftestplatform.nl StUF Testplatform]

Indien voldaan wordt aan alle compliancy eisen uit kan de betreffende leverancier aangeven dat het geteste softwareproduct compliant is aan de Prefill eFormulierenservices 1.0.

## Wanneer is een softwareproduct compliant
Een softwareproduct is compliant aan de Prefill eFormulierenservices 1.0 (*), indien aan alle onderstaande vijf eisen wordt voldaan:

| Nr  | Eis |
|---- |---- |
| 1	  | Het betreffende softwareproduct getest is conform de eisen en voorwaarden uit onderliggende document inclusief de bijlagen en |
| 2	  | De uitvoering heeft plaatsgevonden op en conform de voorwaarden van het StUF testplatform en |
| 3	  | Een foutloos testresultaat is behaald en |
| 4	  | Finale en authentieke testrapporten openbaar zijn gemaakt op het internet en |
| 5	  | In de [GEMMA softwarecatalogus](https://www.softwarecatalogus.nl/) heeft u het authentieke testrapport uit stap 4 gepubliceerd bij het betreffende softwareproduct en aangegeven (aangevinkt) dat u compliant bent. |

(*) Hoewel een foutloos testresultaat van deze testset geen absolute zekerheid geeft van 100% interoperabiliteit tussen applicaties, geeft dit wel een goede indicatie van de kwaliteit van de ondersteuning van de standaard.

## Specificatie van testset
Leveranciers van gemeentelijke software dienen koppelingen te leveren die volledig voldoen aan de standaard. Afhankelijk van de GEMMA referentiecomponent(en) die een softwareproduct invult binnen het toepassingsgebied van de standaard, stelt de standaard andere eisen. Daardoor is de testscope niet voor alle applicaties gelijk.

## Procesinteracties en systeemcomponenten
De specificatie beschrijft drie referentiecomponenten. Dit zijn:

* E-formulierenapplicatie
* Gegevensmagazijn
* Gemeentelijke servicebus

Onderstaand overzicht beschrijft het applicatielandschap met de te standaardiseren proces- en systeeminteracties. De interacties met een grijs bolletje en een B erin zijn buiten scope geplaatst.

<img src="./images/Prefill_eFormulieren_ICT_1.png" width="600"/>

## Definities:
* Referentiecomponent: Lijst van definities zoals opgenomen in de GEMMA Applicatieatlas.
* eFormulierenapplicatie: Systeem voor ondersteuning van het publiceren, ontwerpen, bouwen en beheren van e-Formulieren.
* Gegevensmagazijn: Systeem voor opslag van gemeentelijke basisgegevens (GBA, NHR en BAG). Conform het RSGB. Deze basisgegevens kunnen ook uit de landelijke registratie worden opgevraagd.
* Gemeentelijke servicebus: het gemeentelijke concept om informatiesystemen te koppelen en gegevens te laten uitwisselen.

## Consumer en provider testen
Bij elke test is middels een P of C aangegeven of het een Provider of Consumer test betreft. Bij een provider test moet de te testen applicatie een service beschikbaar stellen aan het StUF Testplatform; het StUF Testplatform zal één of meerdere berichten versturen naar de te testen applicatie. In geval van een consumer test levert het StUF Testplatform een service aan de te testen applicatie. De te testen applicatie moet in deze gevallen één of meerdere berichten versturen naar het StUF Testplatform. Afhankelijk of een test een provider of consumer test is verwacht het StUF Testplatform dus een bericht van de te testen applicatie of verstuurt het StUF Testplatform een bericht naar de te testen applicatie.

<img src="./images/Interactiepatroon.png" width="600"/>

In de volgende paragrafen wordt per referentiecomponent/rol(*) beschreven welke testen uitgevoerd moeten worden, de testscope. Indien een softwareproduct invulling geeft aan meerdere referentiecomponenten dan is de testscope voor het softwareproduct gelijk aan de gezamenlijke testscope van alle ingevulde referentiecomponenten. Bijvoorbeeld, als een softwareproduct zowel de functionaliteit levert van de referentiecomponent Zaaksysteem als van een Document Management systeem, dan dienen zowel de testen van het referentiecomponent Zaaksysteem als Document Management systeem uitgevoerd te worden.

*Een rol kan gezien worden als een groep van referentiecomponenten die dezelfde generieke functionaliteit bieden. Een voorbeeld hiervan is de Zaakservice consumer. Indien een softwareproduct de rol van Zaakservice consumer invult dan betekent dit dat in dit softwareproduct zaakgerelateerde informatie ontstaat of wordt aangepast en dat deze informatie volgens de services uit de Zaak- en Documentservices wordt ontsloten naar een Zaaksysteem. Vrijwel elk softwareproduct kan de rol van Zaakservice consumer invullen. Denk aan vergunningsystemen, handhavingssystemen, uitkeringensysteem etc.

## Testscope e-Formulieren
Indien een softwareproduct invulling geeft aan de referentiecomponent e-Formulieren, dan moet op het StUF Testplatform de testset prefill eFormulieren services uitgevoerd worden voor de referentiecomponent e-Formulieren.

Tijdens de testset uitvoering mogen geen fouten geconstateerd worden door het StUF Testplatform.

Tijdens de testuitvoering simuleert het StUF Testplatform een gegevensmagazijn. Er worden berichten naar het softwareproduct gestuurd waarin zowel verplichte als optionele elementen voorkomen. Tijdens de testuitvoering worden de volgende services getest:

1. natuurlijkPersoon (C)
2. gezinssituatieOpAdresAanvrager (C)
3. kinderenVanAanvrager (C)
4. vestiging (C)

## Testscope Gegevensmagazijn
Indien een softwareproduct invulling geeft aan de referentiecomponent gegevensmagazijn, dan moet op het StUF Testplatform de testset prefill eFormulieren services uitgevoerd worden voor de referentiecomponent gegevensmagazijn.

Tijdens de testset uitvoering mogen geen fouten geconstateerd worden door het StUF Testplatform.

Tijdens de testuitvoering simuleert het StUF Testplatform een eFormulieren applicatie. Er worden berichten naar het te testen softwareproduct gestuurd waarin zowel verplichte als optionele elementen voorkomen. Tijdens de testuitvoering worden de volgende services getest:

* natuurlijkPersoon (P)
* gezinssituatieOpAdresAanvrager (P)
* kinderenVanAanvrager (P)
* vestiging (P)

## Testscope Gemeentelijke servicebus Implementatievariant B
De testscope van de gemeentelijke servicebus Implementatievariant B is gelijk aan die van Gegevensmagazijn (zie Testscope Gegevensmagazijn). Op het StUF Testplatform moet de testset prefill eFormulieren services (Implementatievariant B) in de rol van gemeentelijke servicebus uitgevoerd worden.

## Testscope Gemeentelijke servicebus Implementatievariant C
Indien een softwareproduct invulling geeft aan de referentiecomponent gemeentelijke servicebus in de implementatievariant C, dan moet op het StUF Testplatform de testset prefill eFormulieren services (Implementatievariant C) uitgevoerd worden voor de referentiecomponent Gemeentelijke servicebus.

Tijdens de testset uitvoering mogen geen fouten geconstateerd worden door het StUF Testplatform.

Tijdens de testuitvoering simuleert het StUF Testplatform een eFormulieren applicatie. Er worden berichten naar het te testen softwareproduct gestuurd waarin zowel verplichte als optionele elementen voorkomen. Tijdens de testuitvoering worden de volgende services getest:

1. natuurlijkPersoon (P)
2. vestiging (P) 

## Bericht varianten
Voor elk testscenario geldt dat de services worden getest met een minimale en maximale variant van een bericht.

De maximale variant van een bericht bevat alle door de standaard verplichte en optionele elementen, voorzien van een volgens het RSGB/RGBZ geldige waarde waarbij gerelateerde elementen maximaal twee keer voorkomen en maximaal twee niveaus diep (gerelateerde van een gerelateerde)

De minimale variant van een bericht bevat alleen de verplichte elementen, voorzien van een volgens het RSGB/RSGZ geldige waarde waarbij gerelateerde (verplichte) elementen maximaal 1 keer voorkomen.

## Beschrijving testset scenario’s
De testscenario’s behorende bij deze testset zijn beschreven in een spreadsheet.

Per referentiecomponent/rol is een tabblad opgenomen waar u de testscenario’s vindt die relevant zijn voor softwareproducten die deze referentiecomponent/rol invullen. Een testscenario beschrijving bestaat uit een sequence diagram (in UML) en een tabel waarin wordt toegelicht welke acties uitgevoerd moeten worden en wat daarbij het resultaat moet zijn.

<img src="./images/Testscenario_afbeelding_1.png" width="600"/>

Afbeelding 2: voorbeeld scenariobeschrijving

Het sequence diagram geeft aan in welke volgorde de berichten verstuurd moeten worden door het StUF Testplatform of de te testen applicatie. De rode bolletjes geven de scenariostappen weer.

<img src="./images/Testscenario_afbeelding_2.png" width="600"/>

Afbeelding 3: voorbeeld sequence diagram

## Gebruik van het StUF Testplatform
Het StUF Testplatform is een onafhankelijk en formeel toetsinginstrument voor het testen van koppelingen gebaseerd op standaarden uit de StUF familie. Het platform is vanaf eind 2011 in productie en wordt beheerd en doorontwikkeld door VNG Realisatie.

Primair is het StUF Testplatform voor ICT softwareleveranciers die werkzaam zijn op de gemeentelijke markt. Zij kunnen vroegtijdig tijdens de ontwikkeling van software testen of applicatie-applicatiekoppelingen voldoen aan StUF. Leveranciers worden geacht een (preventieve) test uit te voeren op het StUF Testplatform voordat een softwareproduct in productie wordt genomen.

In de [handleiding StUF Testplatform](./documenten/Gebruikershandleiding_StUF_Testplatform.pdf) wordt verder toegelicht hoe het testplatform gebruikt kan worden.
