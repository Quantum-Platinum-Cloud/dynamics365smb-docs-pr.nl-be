---
title: 'Ontwerpdetails: Inkomende magazijnstroom'
description: De inkomende magazijnstroom begint wanneer artikelen aankomen in het bedrijfsmagazijn en worden geregistreerd en gekoppeld aan inkomende brondocumenten.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/14/2022
ms.author: bholtorf
---
# <a name="design-details-inbound-warehouse-flow" />Ontwerpdetails: Inkomende magazijnstroom

De inkomende stroom in een magazijn begint wanneer artikelen in het magazijn van de bedrijfsvestiging arriveren, ofwel ontvangen via externe bronnen of van een andere bedrijfsvestiging. Het proces van het ontvangen van inkomende orders bestaat in principe uit twee activiteiten:

* Artikelen ontvangen in het ontvangstdok van het magazijn, waar u de artikelen identificeert, ze koppelen aan een brondocument en de ontvangen hoeveelheid registreren. 
* Artikelen in voorraad opslaan en vastleggen waar u ze opslaat.

De brondocumenten voor de inkomende magazijnstroom zijn:

* Inkooporders  
* Inkomende transferorders  
* Verkoopretourorders  

> [!NOTE]
> Productie- en assemblageoutput vertegenwoordigen ook inkomende brondocumenten. Lees meer over het afhandelen van productie- en assemblage-output voor interne processen op [Ontwerpdetails: Interne magazijnstromen](design-details-internal-warehouse-flows.md).  

In [!INCLUDE[prod_short](includes/prod_short.md)] gebeurt het ontvangen en opslaan op een van de volgende vier manieren, zoals beschreven in de volgende tabel.

|Methode|Inkomend proces|Ontvangst vereist|Opslag vereist|Complexiteitsniveau (meer informatie op [Overzicht van magazijnbeheer](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Ontvangst en opslag van de orderregel boeken|||Geen specifieke magazijnactiviteit.|  
|B|Ontvangst en opslag van een voorraadopslagdocument boeken||Ingeschakeld|Basis: Order voor order|  
|H|Ontvangst en opslag van een magazijnontvangstdocument boeken|Ingeschakeld||Basis: Geconsolideerde boeking voor ontvangen/verzenden voor meerdere orders.|  
|D|Ontvangst van een magazijnontvangstdocument en opslag van een magazijnopslagdocument boeken|Ingeschakeld|Ingeschakeld|Geavanceerd|  

Het selecteren van een aanpak hangt af van de toegestane praktijken van uw bedrijf en het niveau van de organisatorische complexiteit. De volgende zijn enkele voorbeelden die u kunnen helpen beslissen.

* In een order-voor-order magazijnomgeving, waar de meeste magazijnmedewerkers direct met orderdocumenten werken, zou u kunnen besluiten om methode A te gebruiken. 
* Een order-voor-order magazijn met een complexer opslagproces, of waar magazijnpersoneel hun opslagactiviteiten scheidt van het orderdocument, kan methode B worden gebruikt.
* Bedrijven die de afhandeling van meerdere bestellingen moeten plannen, kunnen het handig vinden om magazijnontvangstdocumenten, methoden C en D, te gebruiken.  

Bij methode A, B en C worden ontvangen en opslaan in één stap gecombineerd wanneer documenten als ontvangen worden geboekt. Bij methode D wordt eerst de ontvangst geboekt om de positieve voorraadmutatie vast te leggen en dat artikelen beschikbaar zijn voor verkoop. De magazijnmedewerker registreert vervolgens de opslag om de artikelen beschikbaar te maken voor uitgaande orders. 

> [!NOTE]
> Hoewel magazijnopslag en voorraadopslag vergelijkbaar klinken, zijn het verschillende documenten en worden ze in verschillende processen gebruikt.
> * De voorraadopslag die wordt gebruikt in methode B, samen met het registreren van opslaginformatie, boekt ook de ontvangst van het brondocument.
> * De magazijnopslag die wordt gebruikt in methode D, kan niet worden geboekt en registreert alleen de opslag. De registratie maakt de artikelen beschikbaar voor de verdere verwerking, maar boekt de ontvangst niet. In de inkomende stroom vereist de magazijnopslag een magazijnontvangst.

## <a name="no-dedicated-warehouse-activity" />Geen specifieke magazijnactiviteit

De volgende artikelen bevatten informatie over het verwerken van ontvangsten voor brondocumenten als u geen specifieke magazijnactiviteiten hebt.

* [Inkopen vastleggen](purchasing-how-record-purchases.md)
* [Transferorders](inventory-how-transfer-between-locations.md)
* [Verkoopretourorders verwerken](sales-how-process-sales-returns-orders.md)

## <a name="basic-warehouse-configurations" />Standaardmagazijnconfiguraties

In een basismagazijnconfiguratie is de schakelaar **Opslag vereist** aangezet, maar de schakelaar **Ontvangst vereisen** is uitgeschakeld op de pagina Vestiging van de vestiging.

In het volgende diagram worden de inkomende magazijnstromen aangegeven op documentsoort in standaardmagazijnconfiguraties. De nummers in het diagram komen overeen met de stappen in de gedeelten na het diagram.  

:::image type="content" source="media/design_details_warehouse_management_inbound_basic_flow.png" alt-text="De inkomende basisstroom in magazijn.":::

### <a name="1-release-a-source-document-to-create-a-request-for-an-inventory-put-away" />1. Een brondocument vrijgeven om een aanvraag te maken van een voorraadopslag

Wanneer u artikelen ontvangt, geeft u het brondocument vrij, zoals een inkooporder of een inkomende transferorder. Door het document vrij te geven worden de artikelen beschikbaar om te worden opgeslagen. U kunt ook via pushen voorraadopslagdocumenten voor afzonderlijke orderregels maken op basis van opgegeven opslaglocaties en te verwerken aantallen.  

### <a name="2-create-an-inventory-put-away" />2: Een voorraadopslag maken

Op de pagina **Voorraadopslag** haalt de magazijnmedewerker door middel van pulling de wachtende brondocumentregels op, op basis van inkomende magazijnverzoeken. Op een push-manier kunt u ook voorraadopslagregels maken wanneer u het brondocument maakt.  

### <a name="3-post-an-inventory-put-away" />3: Een voorraadopslag boeken

Op elke regel voor artikelen die gedeeltelijk of volledig zijn opgeslagen, vult u het veld **Aantal** in en boekt u vervolgens de voorraadopslag. Brondocumenten met betrekking tot de voorraadopslag worden geboekt als ontvangen.  

* Er worden positieve artikelposten gemaakt
* Magazijnboekingen worden gemaakt voor vestigingen die een opslaglocatiecode vereisen voor alle artikeltransacties.
* Het opslagverzoek wordt verwijderd als het volledig is afgehandeld. Het veld **Ontvangen aantal** in het inkomende brondocument wordt bijvoorbeeld bijgewerkt.
* Er wordt een geboekt ontvangstdocument gemaakt voor bijvoorbeeld de inkooporder en de ontvangen artikelen.  

## <a name="advanced-warehouse-configurations" />Geavanceerde magazijnconfiguraties

In een geavanceerde magazijnconfiguratie is de schakelaar **Ontvangst vereisen** aangezet op de pagina Vestiging voor de vestiging. De schakelaar **Opslag vereist** is optioneel.

In het volgende diagram wordt de inkomende magazijnstroom aangegeven op documentsoort. De nummers in het diagram komen overeen met de stappen in de gedeelten na het diagram.  

:::image type="content" source="media/design_details_warehouse_management_inbound_advanced_flow.png" alt-text="De geavanceerde inkomende stroom in een magazijn":::

### <a name="1-release-the-source-document" />1: Het brondocument vrijgeven

Wanneer u artikelen ontvangt, geeft u het brondocument vrij, zoals de inkooporder of een inkomende transferorder. Door het document vrij te geven worden de artikelen beschikbaar om te worden opgeslagen. De opslag bevat verwijzingen naar het brondocument en het nummer.

### <a name="2-create-a-warehouse-receipt" />2: Een magazijnontvangst maken

De brondocumentregels verschijnen op de pagina **Magazijnontvangst**. U kunt verschillende brondocumentregels combineren in één magazijnontvangstdocument. Vul het veld **Te verwerken aantal** in en selecteert de ontvangstzone en opslaglocatie, indien nodig.  

### <a name="3-post-the-warehouse-receipt" />3. Boek de magazijnontvangst

Boek de magazijnontvangst om positieve artikelposten te maken. Het veld **Ontvangen aantal** in het inkomende brondocument wordt bijgewerkt.  

Als de schakelaar **Opslag vereist** niet is ingeschakeld op de vestigingskaart, stopt het proces hier. Anders maakt het boeken van het inkomende brondocument de artikelen beschikbaar om te worden opgeslagen. De opslag bevat verwijzingen naar het brondocument en het nummer.  

### <a name="4-optional-generate-put-away-worksheet-lines" />4: (optioneel) Opslagvoorstelregels genereren

Haal magazijnopslagregels op in het **Opslagvoorstel** op basis van geboekte magazijnontvangsten of bewerkingen die output produceren. Kies de regels die u wilt opbergen en geef de volgende informatie op:

* De opslaglocaties om artikelen uit te halen.
* De opslaglocaties om artikelen in op te slaan.
* Hoeveel eenheden moeten worden verwerkt.

De opslaglocaties kunnen vooraf worden gedefinieerd door de instelling van de magazijnvestiging of de resource die de bewerking heeft uitgevoerd.  

Wanneer alle opslagactiviteiten zijn gepland en toegewezen aan magazijnmedewerkers, genereert u de magazijnopslagdocumenten. Volledig toegewezen opslagregels worden verwijderd uit het **Opslagvoorstel**.  

> [!NOTE]  
> Als het veld **Opslagvoorstel gebruiken** niet op de vestigingskaart is ingeschakeld, worden magazijnopslagdocumenten gemaakt die direct zijn gebaseerd op geboekte magazijnontvangsten. In dat geval is deze stap niet nodig.  

### <a name="5-create-a-warehouse-put-away-document" />5. Een magazijnopslagdocument maken

Maak een magazijnopslagdocument op een pull-manier, op basis van de geboekte magazijnontvangst. Of maak het magazijnopslagdocument en wijs het door pushing toe aan een magazijnmedewerker.  

### <a name="6-register-a-warehouse-put-away" />6: Een magazijnopslag registreren

Op elke regel voor artikelen die gedeeltelijk of volledig zijn opgeslagen, vult u het veld **Aantal** op de pagina **Magazijnopslag** in en registreert u vervolgens de magazijnopslag.  

* Magazijnboekingen worden gemaakt voor vestigingen die een opslaglocatiecode vereisen voor alle artikeltransacties.
* De magazijnopslagregels worden verwijderd als ze volledig zijn afgehandeld.
* Het magazijnopslagdocument blijft geopend totdat het totale aantal van het gerelateerde geboekte magazijnontvangst is geregistreerd.
* Het veld **Opgeslagen aantal** op de magazijnontvangstorderregels wordt bijgewerkt.

## <a name="related-tasks" />Verwante taken

De volgende tabel beschrijft een reeks taken, met koppelingen naar de onderwerpen waarin deze worden beschreven.

|**Functie**|**Zie**|  
|------------|-------------|  
|Leg de ontvangst van artikelen op magazijnvestigingen vast met een magazijnontvangst, in het geval van deels of volledig geautomatiseerde magazijnverwerking op de vestiging.|[Artikelen ontvangen](warehouse-how-receive-items.md)|
|Sla artikelen op een order-voor-order basis op en boek de ontvangst in één activiteit in standaardmagazijnconfiguraties.|[Artikelen opslaan met voorraadopslag](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Sla artikelen die uit meerdere aankopen, verkoopretouren of transferorders zijn ontvangen, op in een geavanceerde magazijnconfiguratie.|[Artikelen opslaan met magazijnopslag](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  


## <a name="see-also" />Zie ook

[!INCLUDE[footer-include](includes/footer-banner.md)]
