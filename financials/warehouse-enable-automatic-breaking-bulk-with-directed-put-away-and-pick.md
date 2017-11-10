---
title: Automatisch splitsen van bulkgoederen met gestuurde opslag en pick | Microsoft Docs
description: Voor locaties die gebruikmaken van gestuurde opslag en pick, kunt u eenheden opsplitsen in kleinere eenheden wanneer er magazijninstructies worden gemaakt die voldoen aan de eisen met betrekking tot brondocumenten, -productieorders of interne picks en opslag.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 910596b9716ff944a1e491076b599ab6c39c8859
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Procedure: Automatisch splitsen van bulkgoederen met gestuurde opslag en pick inschakelen
Voor locaties die gebruikmaken van gestuurde opslag en pick, kan [!INCLUDE[d365fin](includes/d365fin_md.md)] in allerlei situaties, bulkgoederen automatisch splitsen (dit houdt in dat een bepaalde eenheid wordt opgesplitst in kleinere eenheden) wanneer er magazijninstructies worden gemaakt die voldoen aan de eisen met betrekking tot brondocumenten, -productieorders of interne picks en opslag. Bulksplitsing betekent soms ook het verzamelen van kleinere eenheden, indien nodig, om te voldoen aan uitgaande verzoeken door de grotere eenheid op het brondocument of de productieorder te splitsen in kleinere eenheden die in het magazijn beschikbaar zijn.   

## <a name="breakbulking-in-picks"></a>Bulksplitsing in picks  
Als u artikelen wilt opslaan in een aantal verschillende eenheden en deze, zo nodig automatisch wilt laten combineren tijdens het pickproces, selecteert u het veld **Breakbulk toestaan** op de vestigingskaart.  

Als u een taak wilt uitvoeren, zoekt het programma automatisch naar een artikel in dezelfde eenheid. Als deze vorm van het artikel echter niet wordt gevonden en u dit veld hebt geselecteerd, wordt u gevraagd een bepaalde eenheid op te splitsen in de vereiste eenheid.  

Als het systeem alleen kleinere eenheden kan vinden, wordt u gevraagd artikelen te verzamelen om aan de hoeveelheid op de verzending of productieorder te kunnen voldoen. In de praktijk wordt de grotere eenheid op het brondocument opgesplitst in kleinere pickeenheden.  

## <a name="breakbulking-in-put-aways"></a>Bulksplitsing in opslag  
Bij de magazijnopslag stelt het programma automatisch Plaatsen-actieregels voor in de opslageenheid, bijvoorbeeld stuks, hoewel de artikelen in een andere eenheid arriveren.  

## <a name="breakbulking-in-movements"></a>Bulksplitsing in verplaatsingen  
Het programma past ook automatisch bulksplitsing toe op aanvullingsverplaatsingen, als u het standaard ingeschakelde selectievakje **Breakbulk toestaan** op het sneltabblad **Optie** van het venster **Opslagloc.-aanvulling** berekenen niet uitschakelt.  

U kunt de resultaten van de omzetting van de ene eenheid in de andere weergeven als tussenliggende bulksplitsingsregels in de opslag-, pick- of verplaatsingsinstructies.  

> [!NOTE]  
>  Als u het veld **Breakbulkfilter** in de kop van de magazijninstructie selecteert, worden de bulksplitsingsregels verborgen wanneer de grotere eenheid volledig wordt gebruikt. Bijvoorbeeld: als een pallet 12 stuks bevat en u alle 12 stuks gaat gebruiken, wordt u gevraagd 1 pallet te nemen en 12 stuks te plaatsen. Als u echter maar 9 stuks nodig hebt, worden de opsplitsingsregels niet verborgen, zelfs niet als u het veld **Breakbulkfilter** hebt geselecteerd omdat u de resterende drie stuks ergens in het magazijn moet plaatsen.  

> [!NOTE]  
>  Als u wilt dat uw eenheden optimaal presteren in het magazijn, ook in verband met de bulksplitsingsfunctionaliteit, moet u waar mogelijk proberen om:  
>   
> - De basiseenheid voor een artikel in te stellen als de kleinste eenheid die u denkt nodig te hebben in de magazijnprocessen.  
> - Alternatieve eenheden voor het artikel instellen als veelvouden van de basiseenheid.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
