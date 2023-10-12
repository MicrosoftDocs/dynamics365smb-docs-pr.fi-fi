---
title: RDLC-asettelujen käyttö
description: Johdatus RDLC-raportin asetteluihin.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/14/2022
ms.author: jswymer
---
# <a name="working-with-rdlc-layouts"></a>RDLC-asettelujen käyttö

RDLC-asettelut perustuvat asiakkaan määrittelemiin raportinasettelutiedostoihin (.rdl- tai .rdlc-tiedostotyypit). RDLC-asettelujen suunnittelukäsitteet muistuttavat muita asettelutyyppejä. Asettelu määrittää, mitkä kentät näytetään ja miten ne järjestetään. RDLC-asetteluiden suunnitteleminen on kuitenkin monimutkaisempaa kuin Word- ja Excel-asetteluiden.

[![Näyttää RDLC-asettelun erilaiset elementit.](media/rdlc-layout.png)](media/rdlc-layout.png#lightbox)

## <a name="required-tools"></a>Tarvittavat työkalut

Voit muokata RDL-asetteluja käyttämällä joko Microsoft SQL Server Report Builderia tai Microsoft RDLC Report Designeria.

- Report Builder on sinun tai järjestelmänvalvojan tietokoneeseesi asentama itsenäinen sovellus. Business Centralin on-premises -versiossa Report Builder asennetaan automaattisesti Business Central Serverin asennuksen yhteydessä. Lisätietoja Report Builderin asentamisesta on kohdassa [Report Builderin asentaminen](/sql/reporting-services/install-windows/install-report-builder) SQL Serverin ohjeissa.

- RDLC Report Designer on Visual Studio 2017:n ja uudempien versioiden laajennus. Voit ladata ja asentaa RDLC Report Designer -ohjelman [Visual Studio Marketplacesta](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftRdlcReportDesignerforVisualStudio-18001).

## <a name="create-and-modify-rdlc-layouts"></a>RDLC-asettelujen luominen ja muokkaaminen

RDLC-asettelujen luominen ja muokkaaminen on edistyksellinen tehtävä, jonka tekevät tyypillisesti tehokäyttäjät tai kehittäjät. Peruskäsitteet eivät liity Business Central -raportin asetteluihin. Tästä syystä pyydämme sinua tutustumaan seuraaviin asiakirjoihin:

- [Luo RDL-asetteluraportti](/dynamics365/business-central/dev-itpro/developer/devenv-howto-rdl-report-layout)

    Tässä artikkelissa kerrotaan, miten RDLC-raportin asettelu luodaan AL-koodista.

- [Raportit, raportin osat ja raporttimääritykset ](/sql/reporting-services/report-design/reports-report-parts-and-report-definitions-report-builder-and-ssrs?)

 Linkittää sinut RDL/RDLC-palvelimen SQL Server Reporting Services -dokumentaatioon. Tässä dokumentaatiossa selitetään käsitteet  
RDL/RDLC:n liittyen sekä miten Report Builderia käytetään.

> [!NOTE]
> Report Builder tunnistaa vain .rdl-tiedostotyypin, ei .rdlc-tyyppiä. Business Centralista viedyt asettelutiedostot ovat .rdlc-tiedostotyyppiä. Jotta voit muokata näitä asetteluja Report Builderissa, nimeä tiedosto uudelleen muotoon .rdl.

## <a name="see-also"></a>Katso myös

[Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
[Raportin käyttämän asettelun määrittäminen](ui-set-report-layout.md)  
[Aloita raporttiasettelujen luominen](ui-get-started-layouts.md)  
[Raporttien, eräajojen ja XMLportien käsitteleminen](ui-work-report.md)  
[Business Intelligence](bi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Raporttitietojen analysointi Excelillä](report-analyze-excel.md).

[!INCLUDE[footer-include](includes/footer-banner.md)]
