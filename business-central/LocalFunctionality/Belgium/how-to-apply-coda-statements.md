---
title: CODA-afschriften vereffenen
description: "Nadat een CODA-afschrift is geïmporteerd, kunnen de afschriftregels worden geopend vanuit het venster **Bankrekeningkaart**. De vereffeningsstatus is op elke regel leeg omdat de afschriftbedragen niet zijn vereffend met openstaande posten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 22f67c0aeaf821a5d9db03d3ca5cb57226149ae9
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="apply-coda-statements"></a>CODA-afschriften vereffenen
Nadat een CODA-afschrift is geïmporteerd, kunnen de afschriftregels worden geopend vanuit het venster **Bankrekeningkaart**. De vereffeningsstatus is op elke regel leeg omdat de afschriftbedragen niet zijn vereffend met openstaande posten.  

Afschriftbedragen kunnen als volgt worden vereffend met openstaande posten:  

-   Door CODA-afschriftregels handmatig te vereffenen.  
-   Door CODA-afschriftbedragen automatisch te vereffenen met de betreffende posten en rekeningen. De automatische verwerking van CODA-afschriftregels wordt aanbevolen.  

## <a name="to-manually-apply-the-coda-statement-lines"></a>De CODA-afschriftregels handmatig vereffenen  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer de bankrekening en kies de actie **CODA-afschriften**.  
3.  Selecteer het CODA-afschrift en kies vervolgens de actie **Bewerken**.  
4.  Vul op het sneltabblad **CODA-afschriftregels** voor elke afschriftregel de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Rekeningnr.**|Voer het nummer van de grootboekrekening, de bank, de klant, de leverancier of een vast activum in waaraan de afschriftregel van de bankrekening is gekoppeld.|  
    |**Beschrijving**|In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] wordt automatisch de omschrijving van het geïmporteerde CODA-bestand opgehaald, maar u kunt de inhoud van dit veld wijzigen.|  

5.  Kies de knop **OK**.  

## <a name="to-automatically-apply-the-coda-statement-lines"></a>De CODA-afschriftregels automatisch vereffenen  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer de bankrekening en kies de actie **CODA-afschriften**.  
3.  Selecteer het CODA-afschrift en kies vervolgens de actie **Bewerken**.  
4.  Kies de actie **CODA-afschriftregels**.  
5.  Vul de velden in zoals beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Standaardboeking**|Selecteer deze optie als u wilt dat met de batchverwerking afschriftbedragen worden geboekt die niet aan bestaande posten kunnen worden gekoppeld. Zie Transactiecodering voor meer informatie.|  
    |**Lijst afdrukken**|Selecteer deze optie om een overzicht van afschriftbedragen af te drukken die niet automatisch kunnen worden gekoppeld.|  

6.  Kies de knop **OK**.  

    Wanneer u de batchverwerking start, worden de afschriftbedragen vereffend met bestaande posten op basis van de transactiecodes. Zie voor meer informatie [Bankrekeningen instellen voor CODA](how-to-set-up-bank-accounts-for-coda.md).  

## <a name="see-also"></a>Zie ook  
 [CODA-bankafschriften](coda-bank-statements.md)   
 [Bankrekeningen instellen voor CODA](how-to-set-up-bank-accounts-for-coda.md)   
 [IBLC-BLWI-transactiecodes instellen](how-to-set-up-iblc-blwi-transaction-codes.md)   
 [CODA-afschriften importeren](how-to-import-coda-statements.md)   
 [Financiële dagboeken maken](how-to-create-financial-journals.md)   
 [CODA-afschriften automatisch overbrengen en boeken](how-to-automatically-transfer-and-post-coda-statements.md)   
 [CODA-afschriften handmatig overbrengen en boeken](how-to-manually-transfer-and-post-coda-statements.md)
