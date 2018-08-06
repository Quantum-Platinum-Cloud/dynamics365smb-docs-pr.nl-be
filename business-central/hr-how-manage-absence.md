---
title: Werknemersafwezigheid beheren | Microsoft Docs
description: Beschrijft hoe u werknemersafwezigheid registreert en afwezigheidsstatistieken analyseert.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/08/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 09866f6774af5b2d9644015e986772052146d901
ms.contentlocale: nl-be
ms.lasthandoff: 04/18/2018

---
# <a name="manage-employee-absence"></a>Werknemersafwezigheid beheren
Als u de afwezigheid van een werknemer wilt beheren, moet u de afwezigheid registreren in het venster **Afwezigheidsregistratie**. Het kan dan op verschillende manieren voor analyse- en rapportagedoeleinden worden weergegeven.

U kunt werknemersafwezigheid weergeven in twee verschillende vensters:

* In het venster **Afwezigheidsregistratie**, waar u alle werknemersafwezigheid registreert met een regel voor elke afwezigheid.
* Het venster **Werknemersafwezigheid**, waar de afwezigheid van slechts één werknemer wordt weergegeven. Dit zijn de gegevens die u hebt ingevoerd in het venster **Afwezigheidsregistratie**, gefilterd op de specifieke werknemer.

Gebruik daarbij wel altijd dezelfde tijdseenheid (uren of dagen).

## <a name="to-register-employee-absence"></a>Werknemersafwezigheid registreren
U kunt werknemersafwezigheid per dag of met een ander interval dat voldoet aan de behoeften van uw organisatie registreren.

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport**, voer **Afwezigheidsregistratie** in en klik vervolgens op de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul een regel in voor elke werknemersafwezigheid die u wilt registreren.
4. Sluit het venster.

    > [!Tip]
    > Om duidelijke statistische gegevens te verkrijgen, is het belangrijk dat u steeds dezelfde eenheid (uur of dag) gebruikt bij de registratie van werknemersafwezigheid.

## <a name="to-view-an-individual-employees-absence"></a>Afwezigheid van een individuele werknemer weergeven
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport**, voer **Werknemers** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer de betreffende werknemer en kies vervolgens de actie **Afwezigheid**.

    Het venster **Werknemersafwezigheid** wordt geopend met alle afwezigheid, inclusief de begin- en einddatums van de afwezigheid.

## <a name="to-view-an-employees-absence-by-categories"></a>Afwezigheid van een werknemer weergeven per categorie
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport**, voer **Werknemers** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer de betreffende werknemer en kies vervolgens de actie **Afwezigheid per categorie**.
3. Vul in het venster **Werkn.-afwezigh. per categorie** de benodigde filtervelden in en kies vervolgens de actie **Matrix weergeven**.

    Het venster **Matrix voor werknemerafwezigheid per categorie** wordt geopend met alle afwezigheden, opgesplitst op oorzaken van afwezigheid.

## <a name="to-view-all-employee-absences-by-category"></a>Alle werknemersafwezigheid per categorie weergeven
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport**, voer **Afwezigheidsregistratie** in en klik vervolgens op de gerelateerde koppeling.
2. Kies in het venster **Afwezigheidsregistratie** de actie **Overzicht per categorie**.
3. Stel in het venster **Afwezigheid per categorie** in het veld **Werknemerfilter** een filter in om de afwezigheid te bekijken van een individuele werknemer of een gedefinieerde groep werknemers.
4. Kies de actie **Matrix weergeven**.

    Het venster **Matrix voor afwezigheidsoverzicht per categorie** wordt geopend met de afwezigheid van alle werknemers, gesplitst per afwezigheidsreden.

## <a name="to-view-all-employee-absences-by-period"></a>Alle werknemersafwezigheid per periode weergeven
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport**, voer **Afwezigheidsregistratie** in en klik vervolgens op de gerelateerde koppeling.
   Kies in het venster **Afwezigheidsregistratie** de actie **Overzicht per periode**.
2. Stel in het venster **Afwezigheid per periode** in het veld **Afw.-filter** een filter in om werknemersafwezigheid wegens opgegeven afwezigheidsredenen te bekijken.
3. Kies de actie **Matrix weergeven**.

    Het venster **Matrix voor afwezigheidsoverzicht per periode** wordt geopend met de werknemersafwezigheid, gesplitst op periode.

## <a name="see-also"></a>Zie ook
[Human Resources beheren](hr-manage-human-resources.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)
