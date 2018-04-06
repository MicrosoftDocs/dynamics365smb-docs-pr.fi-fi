---
title: "Finance and Operations, Business editionin raportoinnin määrittäminen Power BI:ssa| Microsoft Docs"
description: "Financials-tietoja voidaan käyttää Power BI:n tietolähteenä, ja niiden avulla voidaan luoda tehokkaita liiketoiminnan tilasta kertovia raportteja."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/21/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 73dc6048f7184054c853f9b9187cbb1a8d5131ff
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-as-power-bi-data-source-for-building-reports"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttö Power BI:n tietolähteenä raportteja luotaessa
[!INCLUDE[d365fin](includes/d365fin_md.md)]-tietoja voidaan käyttää Power BI:n tietolähteenä, ja niiden avulla voidaan luoda tehokkaita liiketoiminnan tilasta kertovia raportteja.  

> [!NOTE]  
> Sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja Power BI -tili. Sinun on ladattava myös [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisääminen Power BI Desktopin tietolähteeksi
1. Valitse Power BI Desktopin vasemmassa siirtymisruudussa **Nouda tiedot**.
2. Valitse **Nouda tiedot** -ikkunassa ensin **Online Services**, sitten **Dynamics 365 for Finance and Operations, Business edition** ja lopuksi **Muodosta yhteys**.
3. Power BI avaa ohjatun toiminnon, joka auttaa [yhteyden muodostusprosessissa](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Ensimmäiseksi kirjaudutaan palveluun. Valitse ensin **Kirjaudu sisään** ja sitten tili, johon haluat kirjautua. Valitse sama tili, jolla kirjaudut [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.
4. Jatka valitsemalla **Muodosta yhteys**. Ohjatussa Power BI -toiminnossa on luettelo [!INCLUDE[d365fin](includes/d365fin_md.md)]in yrityksistä ja tietolähteistä. Nämä tietolähteet viittaavat kaikkiin verkkopalveluihin, jotka on julkaistu kullekin yritykselle [!INCLUDE[d365fin](includes/d365fin_md.md)]ista.
5. Voit vaihtoehtoisesti luoda uuden verkkopalvelun URL-osoitteen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa käyttämällä **Luo tietojoukko** -toimintoa **WWW-palvelut**-sivulla tai asetusten ohjattua **Määritä raportointi** -määritystä tai valitsemalla **Muokkaa Excelissä** -toiminnon jossakin luettelossa.
6. Määritä tietomalliin lisättävät tiedot ja valitse sitten **Lataa**-painike.
7. Lisää muita [!INCLUDE[d365fin](includes/d365fin_md.md)]-tietoja Power BI -tietomalliin toistamalla edellä olevat vaiheet.

> [!NOTE]  
> Kun yhteys [!INCLUDE[d365fin](includes/d365fin_md.md)]iin on muodostettu, sinua ei pyydetä kirjautumaan uudelleen.

Kun tiedot on ladattu, ne näkyvät sivun oikeassa siirtymisruudussa. Olet nyt muodostanut yhteyden Finance and Operations, Business editionin tietoihin ja olet valmis aloittamaan oman Power BI -raportin luomisen. Lisätietoja on kohdassa [Power BI -dokumentaatio](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Katso myös
[Business Intelligence](bi.md)  
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](upload-data.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)   
[Rahoitus](finance.md)  
[Power BI:n yhdistäminen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  

