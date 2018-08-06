---
title: Power BI verbinden met Business Central | Microsoft Docs
description: Inzicht, bedrijfsinformatie en KPI's krijgen uit uw Business Central-gegevens is gemakkelijk met Power BI en de Business Central-inhoudspakketten.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/03/2018
ms.author: solsen
redirect_url: admin-powerbi
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 0196bff5dedb878884fd3d6e0208022faa968dfd
ms.contentlocale: nl-be
ms.lasthandoff: 05/17/2018

---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a>Power BI verbinden met Dynamics 365 Business Central-inhoudspakketten
Inzicht krijgen in uw Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-gegevens is gemakkelijk met Power BI en de inhoudspakketten van Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Power BI haalt uw gegevens op en maakt vervolgens een kant-en-klaar dashboard en rapporteert op basis van die gegevens.

U moet een geldig account bij Dynamics 365 en Power BI hebben. U moet ook [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) downloaden als u uw eigen Power BI-rapporten wilt maken. Voor Power BI-inhoudspakketten zijn machtigingen vereist voor de tabellen waaruit de gegevens worden opgehaald. Meer details over de vereisten worden verderop beschreven.  

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatiedeelvenster.  
![Navigeren om gegevens op te halen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

U kunt ook aan de slag gaan vanuit Dynamics 365 Business Edition. Navigeer in het rolcentrum naar **Rapportselectie** in het onderdeel Power BI-rolcentrum. Selecteer **Service** of **Mijn organisatie** vanuit het lint. Wanneer een van deze acties wordt geselecteerd, gaat u naar de Organisatiegalerie in Power BI of naar de servicebibliotheek in Power BI, die ook wordt gefilterd op alleen weergave van inhoudspakketten die verband houden met [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

2. Selecteer **Ophalen** in het vak **Diensten**. Hierdoor wordt een venster geopend met de **AppSource** en **Apps voor Power BI-apps**.  
![Inhoudspakketten kiezen uit online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Selecteer **Apps** op het tabblad **Apps voor Power BI-apps** en kies het **Microsoft Dynamics 365 Business Central**-inhoudspakket dat u wilt gebruiken. Selecteer vervolgens **Nu ophalen**.  
![Selecteer Dynamics 365 Business Central en selecteer Nu ophalen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Voer wanneer daarom wordt gevraagd de naam van *uw bedrijf* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Dit is niet de weergavenaam. De bedrijfsnaam kan op de pagina Bedrijven worden gevonden binnen uw [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-exemplaar. 
![Selecteer Dynamics 365 Business Central en selecteer Nu ophalen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Nadat verbinding is gemaakt, worden automatisch een dashboard, rapport en gegevensset geladen in uw Power BI-werkruimte. Wanneer dit is voltooid, worden de tegels bijgewerkt met gegevens uit uw [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-bedrijf.
![Selecteer Dynamics 365 Business Central en selecteer Nu ophalen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Wat nu?

- Probeer [een vraag te stellen in het vraag- en antwoordvak](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) boven aan het dashboard.
- [Wijzig de tegels](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in het dashboard.  
- [Selecteer een tegel](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) om het onderliggende rapport te openen.  
- Terwijl uw gegevensset wordt gepland om dagelijks te worden vernieuwd, kunt u het vernieuwingsschema wijzigen of op verzoek proberen te vernieuwen met **Nu vernieuwen**.

## <a name="system-requirements"></a>Systeemvereisten
Als u de gegevens [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] in Power BI wilt importeren, moet u machtigingen hebben voor de webservices die worden gebruikt om gegevens op te halen. De webservices die voor elk inhoudspakket vereist zijn omvatten:

## <a name="role-center-reports"></a>Rolcentrumrapporten

**Microsoft Dynamics 365 Business Central – CRM**
- Verkoopopportunities
- Excel-sjabloonweergave Bedrijf
- Labels van Power BI-rapport

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- Excel-sjabloonweergave Bedrijf
- Labels van Power BI-rapport

**Microsoft Dynamics 365 Business Central – Jobs**
- Projectoverzicht
- Projectplanningsregels
- Projecttaakregels
- Labels van Power BI-rapport
- Excel-sjabloonweergave Bedrijf

**Microsoft Dynamics 365 Business Central - Sales**
- Verkoopdashboard
- Excel-sjabloonweergave Bedrijf
- Labels van Power BI-rapport

## <a name="list-page-reports"></a>Lijstpaginarapporten 

**Microsoft Dynamics 365 Business Central – Customers List**
- Artikelverkopen per klant
- Power BI-artikelinkoopoverzicht
- Power BI-artikelverkoopoverzicht
- Verkoopdashboard
- Power BI-klantenoverzicht
- ExcelTemplateViewCompany
- Labels van Power BI-rapport 

**Microsoft Dynamics 365 Business Central - General Ledger Entries List**
- Power BI-overzicht met grootboekbedragen
- Power BI gebudgetteerd grootboekbedrag
- ExcelTemplateViewCompany
- Labels van Power BI-rapport

**Microsoft Dynamics 365 Business Central – Items List**
- Artikelverkopen per klant
- Power BI-artikelinkooplijst
- Power BI-artikelverkooplijst
- Verkoopdashboard
- ExcelTemplateViewCompany
- Labels van Power BI-rapport

**Microsoft Dynamics 365 Business Central – Jobs List**
- Power BI-projectenoverzicht
- ExcelTemplateViewCompany
- Labels van Power BI-rapport

**Microsoft Dynamics 365 Business Central – Purchase Invoices List**
- Power BI-inkoopoverzicht
- ExcelTemplateViewCompany
- Labels van Power BI-rapport

**Microsoft Dynamics 365 Business Central – Sales Orders List**
- Power BI-verkoopoverzicht
- ExcelTemplateViewCompany
- Labels van Power BI-rapport


**Microsoft Dynamics 365 Business Central – Vendors List**
- Power BI-artikelinkooplijst
- Power BI-artikelverkooplijst
- Power BI-leveranciersoverzicht
- ExcelTemplateViewCompany
- Labels van Power BI-rapport

## <a name="web-services"></a>Webservices
Een eenvoudige manier om de webservices te vinden is te zoeken naar webservices in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. In de lijst moet u ervoor zorgen het vakje Publiceren is gemarkeerd voor de hierboven genoemde webservices.

## <a name="troubleshooting"></a>Problemen oplossen
Het dashboard van Power BI gebruikt de gepubliceerde webservices die hierboven worden genoemd en bevat gegevens van het demobedrijf of uw eigen bedrijf als u gegevens importeert uit uw huidige financiële oplossing. Als er echter iets verkeerd gaat, biedt deze sectie een oplossing voor de meest voorkomende problemen.

### <a name="incorrect-company-name"></a>Onjuiste bedrijfsnaam  
Een veel voorkomende fout is de weergavenaam van het bedrijf in te voeren in plaats van de bedrijfsnaam. Als u de bedrijfsnaam wilt vinden, zoekt u naar **Bedrijven**. Gebruik vervolgens het veld **Naam** wanneer u uw bedrijfsnaam invoert.

### <a name="incorrect-user-name-and-password"></a>Onjuiste gebruikersnaam en wachtwoord  
De gebruikersnaam en het wachtwoord die worden gebruikt om verbinding te maken, zijn hetzelfde als wat wordt gebruikt om verbinding te maken met uw Microsoft Office 365-account.  

De inhoudspakketten vereisen ook dat u een Microsoft-[!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] hebt. Zodra u uw aanmeldingsgegevens invoert, worden eventuele Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-tenants waartoe u toegang hebt, automatisch gevonden. Als u geen gelicentieerd of proef Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-account hebt, wordt een foutbericht weergegeven.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>De sleutel kwam met geen rijen uit de tabel overeen
Als u een ongeldige bedrijfsnaam invoert tijdens het verbindingsproces, kunt u de foutmelding "De sleutel kwam met geen rijen uit de tabel overeen" krijgen. Geef de juiste bedrijfsnaam op en probeer opnieuw verbinding te maken.

## <a name="see-also"></a>Zie ook
[Aan de slag met Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI-basisconcepten](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[Bedrijfsinformatie](bi.md)  
[Aan de slag](product-get-started.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Financiën](finance.md)  
[Rapportage instellen voor [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)  
