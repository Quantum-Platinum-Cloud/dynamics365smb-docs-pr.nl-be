---
title: Aanbevolen procedures voor instellen van algemene planning | Microsoft Docs
description: "Het sneltabblad **Planning** in het venster **Productie-instellingen** bevat verschillende velden die de algemene regels voor de voorraadplanning definiëren."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5f9eda3b9bb2482a446370058c7bd4a503dde6ee
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="setup-best-practices-global-planning-setup"></a>Aanbevolen procedures instellen: Instellen algemene planning
Het sneltabblad **Planning** in het venster **Productie-instellingen** bevat verschillende velden die de algemene regels voor de voorraadplanning definiëren.  

 De volgende tabel bevat de aanbevolen procedures voor het instellen van de geselecteerde globale planningparametervelden. Voor meer informatie over een veld, kiest u de koppeling in de kolom **Veld instellen**.  

|Veld instellen|Aanbevolen procedure|Opmerking|  
|-----------------|-------------------|-------------|  
|Prognose op vestigingen gebruiken|Selecteer als u prognoses hebt voor specifieke locaties.||  
|Onderdelen op vestiging|Als artikelen niet als SKU's zijn gedefinieerd, selecteert u de vestigingscode van het hoofdmagazijn.|Dit geldt ook als u alleen het inkoopvoorstel gebruikt.|  
|Blanco-overflowniveau|Selecteer **Standaardberekening toestaan** als u migreert van Microsoft Dynamics NAV 5.0 of eerder.|Alleen gebruiken als u toestaat dat alle of sommige van uw objecten het bestelpunt overschrijden.|  
|Standaard dempingsperiode|Ingesteld tussen 1D en 5D.<br /><br /> Indien planning in [!INCLUDE[d365fin](includes/d365fin_md.md)] nieuw is voor u stelt u een langere periode in.|Wanneer gebruikers meer vertrouwd zijn met de verschillende redenen voor planningsboodschappen, kort dan de dempingsperiode in om meer wijzigingssuggesties toe te staan.|  
|Demping standaardhoeveelheid|Tussen 5 en 20 procent van de lotgrootte van het item instellen.||  

## <a name="see-also"></a>Zie ook  
 [Aanbevolen procedures instellen: Voorraadplanning](setup-best-practices-supply-planning.md)   
 [Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)   
 [Complexe toepassingsgebieden instellen met aanbevolen procedures](set-up-complex-application-areas-using-best-practices.md)  
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
