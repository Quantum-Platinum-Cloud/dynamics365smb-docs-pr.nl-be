---
title: SEPA-betalingen via automatische incasso boeken | Microsoft Docs
description: Wanneer een verzameling van automatische incasso wordt verwerkt door uw bank, kunt u doorgaan met het boeken van de ontvangst van de betaling voor de betrokken verkoopfacturen.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5beb5f6795bd7f4943a6ed9d8b691c05fc5ecb63
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-sepa-direct-debit-payment-receipts"></a>Procedure: SEPA-betalingsontvangsten via automatische incasso boeken
Wanneer een incasso-opdracht wordt verwerkt door uw bank, kunt u doorgaan met het boeken van de ontvangst van de betaling voor de betrokken verkoopfacturen. Zie voor meer informatie [Procedure: SEPA-verzamelingsposten van automatische incasso maken en exporteren naar een bankbestand](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  

U kunt de betalingsontvangst van het venster **Incasso-opdrachten** of het venster **Verzamelingsposten van incasso** direct boeken. U kunt ook het werk aan een andere gebruiker doorgeven door de dagboekregels voor te bereiden.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a>Een betalingsontvangst van een automatische incasso boeken vanuit het venster Verzamelingen van automatische incasso  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Incasso-opdrachten** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer een regel voor een verzameling automatische incasso die is geëxporteerd naar een bankbestand en verwerkt door de bank. Zie voor meer informatie [Procedure: SEPA-verzamelingsposten van automatische incasso maken en exporteren naar een bankbestand](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  
3. Kies de actie **Betalingsontvangsten boeken**.  
4. Vul in het venster **Incasso-opdracht boeken** de velden in, zoals is beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Incasso-opdrachtnr.**|Geef de verzameling automatische incasso op waar u een betalingsontvangst voor wilt boeken.|  
    |**Algemeen dagboeksjabloon**|Geef op welk dagboeksjabloon te gebruiken voor het boeken van de betalingsontvangst, zoals de sjabloon voor ontvangsten.|  
    |**Batchnaam financieel dagboek**|Geef op welke dagboekbatch moet worden gebruikt voor het boeken van de betalingsontvangst.|  
    |**Alleen dagboek aanmaken**|Schakel dit selectievakje in als u niet de betalingsontvangst boeken wilt wanneer u de **OK** knop kiest. De betalingsontvangst in het opgegeven dagboek wordt voorbereid en wordt niet geboekt totdat iemand de dagboekregels in kwestie boekt.|  

5. Kies de knop **OK**.  

## <a name="see-also"></a>Zie ook  
 [Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md)   
 [Verkoop](sales-manage-sales.md)
