---
title: "Dynamics 365 for Financialsin käyttäminen Power BI:n tietolähteenä | Microsoft Docs"
description: "Financials-tietoja voidaan käyttää Power BI:n tietolähteenä, ja niiden avulla voidaan luoda tehokkaita liiketoiminnan tilasta kertovia raportteja."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/02/2016
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 5213b515dfdf1f0e538a6d003cf921781ca6b3ff
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-as-a-power-bi-data-source"></a>Dynamics 365 for Financialsin käyttäminen Power BI:n tietolähteenä
[!INCLUDE[d365fin](includes/d365fin_md.md)]-tietoja voidaan käyttää Power BI:n tietolähteenä, ja niiden avulla voidaan luoda tehokkaita liiketoiminnan tilasta kertovia raportteja.  

**Huomautus**: sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja Power BI -tili. Sinun on ladattava myös [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisääminen Power BI Desktopin tietolähteeksi
1. Valitse Power BI Desktopin vasemmassa siirtymisruudussa **Nouda tiedot**.
2. Valitse **Nouda tiedot** -ikkunassa ensin **Online Services**, sitten **Dynamics 365 for Financials** ja lopuksi **Muodosta yhteys** -painike.

   Power BI näyttää ohjatun toiminnon, joka auttaa yhteyden muodostusprosessissa. Ensimmäisessä vaiheessa annetaan [!INCLUDE[d365fin](includes/d365fin_md.md)]-tiliin liitetty ODatan URL-osoite ja yrityksen nimi.  

   Voit kopioida *OData URL* -osoitteeksi minkä tahansa [!INCLUDE[d365fin](includes/d365fin_md.md)]in **WWW-palvelut**-sivulla mainitun verkkopalvelun OData V4 URL-osoitteen, kuten `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Käytä *yrityksen nimenä* nimeä, joka näkyy [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Oman yrityksen tiedot** -ikkunan **Nimi**-kentässä. Jos [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on useita yrityksiä, valitse sopiva yrityksen nimi **Yritykset**-ikkunassa olevasta luettelosta. Varmista kummassakin tapauksessa, että ohjatussa Power BI -toiminnossa määrittämäsi nimi on kirjoitettu täsmälleen samoin kuin [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Esimerkki: `My Company`.
3. Kun olet antanut tiedot, paina OK-painiketta. Ohjatun toiminnon seuraavassa vaiheessa annetaan käyttäjänimi ja salasana.

   **Huomautus**: jos vasemmassa siirtymisruudussa on valittavana muita todennusvaihtoehtoja, valitse *Perus*.
4. Anna käyttäjänimi ja salasana. Nämä tiedot ovat [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Käyttäjät**-ikkunassa. Käytä salasanana **verkkopalvelun käyttöoikeusavainta**.

   Käyttäjänimesi on esimerkiksi *JÄRJESTELMÄNVALVOJA* ja salasanana toimiva verkkopalvelun käyttöoikeusavain on *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
5. Jatka valitsemalla **Yhteys**-painike. Ohjatussa Power BI -toiminnossa on luettelo [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietolähteistä. Nämä tietolähteet viittaavat kaikkiin [!INCLUDE[d365fin](includes/d365fin_md.md)]ista julkaistuihin verkkopalveluihin.

   Voit vaihtoehtoisesti luoda uuden verkkopalvelun URL-osoitteen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa käyttämällä **Luo tietojoukko** -toimintoa **WWW-palvelut**-sivulla tai avustettua **Määritä raportointi** -asetusopasta tai valitsemalla **Muokkaa Excelissä** -toiminnon missä tahansa luettelossa.
6. Määritä tietomalliin lisättävät tiedot ja valitse sitten **Lataa**-painike.
7. Lisää muita [!INCLUDE[d365fin](includes/d365fin_md.md)]-tietoja Power BI -tietomalliin toistamalla edellä olevat vaiheet.

   **Huomautus**: kun [!INCLUDE[d365fin](includes/d365fin_md.md)]-yhteys on muodostettu, ODatan URL-osoitetta, käyttäjänimeä tai salasanaa ei enää kysytä.

Kun tiedot on ladattu, ne näkyvät sivun oikeassa siirtymisruudussa. Olet nyt muodostanut yhteyden Dynamics 365 -tietoihin ja olet valmis aloittamaan oman Power BI -raportin luomisen. Lisätietoja on kohdassa [Power BI -dokumentaatio](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Katso myös
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin](index.md)  
[Yritystietojen tuonti muista rahoitusjärjestelmistä] (upload-data.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  
