---
title: Inkomende documentrecords maken
description: 'Gebruik verschillende functies op de pagina Inkomende documenten om onkostenbewijzen te bekijken, OCR-taken te beheren, inkomende documentbestanden te converteren en externe bestanden bij te voegen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="create-incoming-document-records" />Inkomende documentrecords maken

Op de pagina **Inkomende documenten** kunt u verschillende functies gebruiken om onkostenbewijzen te controleren, OCR-taken te beheren en inkomende documentbestanden handmatig of automatisch te converteren naar de relevante documenten of dagboekregels. De externe bestanden kunnen worden gekoppeld in elke procesfase, inclusief naar geboekte documenten en naar de resulterende leverancier, klant en grootboekposten.

Als u een extern document wilt registreren in [!INCLUDE[prod_short](includes/prod_short.md)], moet u eerst een inkomende documentrecord maken of voltooien. U kunt deze taken handmatig uitvoeren of u kunt een foto van het externe document maken om de inkomende documentrecord te maken met het afbeeldingsbestand bijgevoegd.

Voordat u de functie **Inkomende documenten** gebruikt, moet u de benodigde instellingen uitvoeren. Zie voor meer informatie [Inkomende documenten instellen](across-how-setup-income-documents.md).

## <a name="approve-or-reject-an-incoming-document" />Een inkomend document goedkeuren of weigeren

Als u de functie **Inkomende documenten** hebt ingesteld om goedkeuring te vereisen om documenten te maken, moeten gebruikers met de juiste rechten de records goedkeuren voordat ze worden verwerkt. Zie voor meer informatie [Fiatteurs van inkomende documentrecords instellen](across-how-setup-income-documents.md#to-set-up-approvers-of-incoming-document-records).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkomende documenten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel met het document dat u wilt goedkeuren of weigeren en kies vervolgens de actie **Goedkeuren** of **Weigeren**.

Als u de inkomende documentrecord goedkeurt, wordt het selectievakje **Vrijgegeven** op de regel van het inkomende document geselecteerd. De gebruiker die verantwoordelijk is voor het aanmaken van, bijvoorbeeld, inkoopfacturen kan doorgaan om de record te verwerken.

## <a name="create-an-incoming-document-record-by-taking-a-photo" />Een inkomende documentrecord maken door een foto te maken

> [!NOTE]  
> De volgende procedure geldt alleen voor de tablet en telefoonclient van [!INCLUDE[prod_short](includes/prod_short.md)].

1. Kies in het rolcentrum de tegel **Inkomend document maken van camera** en ga vervolgens naar stap 4.
2. Of kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkomende documenten** in en kies vervolgens de gerelateerde koppeling.
3. Kies op de pagina **Inkomende documenten** **Nieuw** en kies vervolgens **Maken van camera**. De camera op de tablet of de telefoon wordt ingeschakeld.
4. Maak een foto van een document, zoals een inkoopontvangst, dat u wilt verwerken als een inkomend document en kies vervolgens de knop **Gebruiken**.

    Er wordt een nieuwe documentrecord gemaakt met de afbeelding gekoppeld.

## <a name="attach-an-image-to-an-incoming-document-record-by-taking-a-photo" />Een afbeelding aan een inkomende documentrecord koppelen door een foto te maken

> [!NOTE]  
> De volgende procedure geldt alleen voor de tablet en telefoonclient van [!INCLUDE[prod_short](includes/prod_short.md)].

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkomende documenten** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor een bestaande inkomende documentrecord.
3. Kies op de documentrecordpagina **Verwerken** en kies vervolgens **Afbeelding van camera bijvoegen**. De camera op de tablet of de telefoon wordt ingeschakeld.
4. Maak een foto van een document, zoals een inkoopontvangst, dat u wilt verwerken als een inkomend document en kies vervolgens de knop **Gebruiken**.

    De afbeelding wordt gekoppeld aan de inkomende documentrecord.

## <a name="create-an-incoming-document-record-manually" />Een inkomend documentrecord handmatig maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkomende documenten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** en kies vervolgens de actie **Maken van bestand**.  
3. Selecteer op de pagina **Bestand invoegen** een bestand en kies vervolgens **Openen**. Het bestand wordt automatisch gekoppeld.
4. U kunt ook de actie **Nieuw** kiezen.
5. Als u een bestand wilt koppelen, kiest u **Verwerken** en vervolgens de actie **Bestand koppelen**.
6. Op de pagina **Bestand invoegen**, selecteert u het bestand dat het betreffende inkomende document vertegenwoordigt. Kies vervolgens de knop **Openen**.
7. Vul op de pagina **Inkomende documenten** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-microsoft-trainingtrainingmodulesincoming-documents-dynamics-365-business-central" />Zie gerelateerde [Microsoft-training](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md)
[Inkomende documentrecords maken direct van documenten en posten](across-how-connect-disconnect-income-document-records.md)
[Geboekte documenten zonder inkomende documentrecords zoeken](across-how-find-posted-documents-without-income-document-records.md)
[Inkomende documenten](across-income-documents.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
