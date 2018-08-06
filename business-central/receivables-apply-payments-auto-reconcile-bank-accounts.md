---
title: "Bankrekeningen reconciliëren en betalingen vereffenen | Microsoft Docs"
description: "Schetst taken om uw bank-, tegoeden- en schuldenrekeningen te reconciliëren, kasontvangsten of onkosten te boeken en betalingen automatisch te vereffenen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 02/28/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 992e51f11d11b86685cf6de813e0b7610350a6a7
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Betalingen automatisch vereffenen en bankrekeningen reconciliëren
U moet regelmatig uw bankrekening en de rekeningen met tegoeden en betalingsverplichtingen reconciliëren, door betalingen die op de bank zijn vastgelegd te vereffenen met de gerelateerde onbetaalde facturen en creditnota's of andere openstaande posten in [!INCLUDE[d365fin](includes/d365fin_long_md.md)].  

U kunt deze taak in het venster **Dagboek betalingsreconciliatie** uitvoeren door een bankafschriftbestand of -feed te importeren om de betalingen snel in project te registreren. Betalingen worden vereffend met openstaande leveranciers- of klantenposten, op basis van overeenkomsten tussen de betalingtekst en de informatie in de posten. U kunt automatische vereffeningen controleren en wijzigen voordat u het dagboek boekt. U kunt ervoor kiezen om openstaande bankrekeningposten met betrekking tot de vereffende posten te sluiten wanneer u het dagboek boekt. De bankrekening wordt automatisch gereconcilieerd wanneer alle betalingen worden vereffend.

U kunt ook bankrekeningen reconciliëren zonder tegelijkertijd betalingen te vereffenen. U doet dit werk in het venster **Bankreconciliatie**. Zie [Bankrekening apart reconciliëren](bank-how-reconcile-bank-accounts-separately.md) voor meer informatie.   

Als u bankafschriften als een bankfeed wilt importeren, moet u eerst de feedservice van de Envestnet Yodlee Bank instellen en inschakelen en vervolgens uw bankrekeningen aan de gerelateerde online bankrekeningen koppelen. Zie voor meer informatie [De feedservice van de Envestnet Yodlee Bank instellen](bank-how-setup-bank-statement-service.md).  

U kunt ook de conversieservice voor bankgegevens gebruiken om een bankafschriftbestand in een willekeurige indeling om te zetten in een gegevensstroom die u kunt importeren in [!INCLUDE[d365fin](includes/d365fin_long_md.md)]. Zie voor meer informatie [De conversieservice bankgegevens instellen](bank-how-setup-bank-data-conversion-service.md).  

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.  

| Als u dit wilt doen | Zie |
| --- | --- |
| Vereffen betalingen om klant- of leveranciersposten te openen door een bankafschrift te importeren en de bankrekening te reconciliëren wanneer alle betalingen zijn vereffend. |[Betalingen reconciliëren met automatische vereffening](receivables-how-reconcile-payments-auto-application.md) |
| Vereffen handmatig betalingen door gedetailleerde informatie over afgestemde gegevens weer te geven en suggesties voor openstaande kandidaatposten om betalingen mee te vereffenen. |[Betalingen na automatische vereffening controleren of vereffenen](receivables-how-review-apply-payments-auto-application.md) |
| Betalingen oplossen die niet automatisch met de gerelateerde openstaande posten kunnen worden vereffend. Bijvoorbeeld omdat bedragen afwijken, of omdat geen gerelateerde post bestaat. |[Betalingen reconciliëren die niet automatisch kunnen worden vereffend](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Koppel tekst op betalingen aan specifieke klant-, leverancier- of grootboekrekeningen om periodieke ontvangsten of kosten altijd naar deze rekeningen te boeken als er geen documenten zijn voor vereffening. |[Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliatie](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |

## <a name="see-also"></a>Zie ook
[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
