---
title: "Business Central -raportoinnin määrittäminen Power BI:ssa | Microsoft Docs"
description: "Määritä tiedot käytettäviksi Power BI:n tietolähteenä ja tehokkaiden liiketoiminnan tilasta kertovien raporttien luomista varten."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: ca4c27eaa1fe66e9bee678d6ec197fee7b928bdd
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="using-included365finlongmdincludesd365finlongmdmd-as-power-bi-data-source-for-building-reports"></a>[!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in käyttö Power BI:n tietolähteenä raportteja luotaessa
[!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-tietoja voidaan käyttää Power BI:n tietolähteenä, ja niiden avulla voidaan luoda tehokkaita liiketoiminnan tilasta kertovia raportteja.  

Sinulla on oltava kelvollinen [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]- ja Power BI -tili. Sinun on ladattava myös [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finlongmdincludesd365finlongmdmd-as-a-data-source-in-power-bi-desktop"></a>[!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in lisääminen Power BI Desktopin tietolähteeksi
1. Valitse Power BI Desktopin vasemmassa siirtymisruudussa **Nouda tiedot**.
2. Valitse **Nouda tiedot** -sivulla ensin **Online Services**, sitten **Microsoft Dynamics 365 Business Central** ja lopuksi **Muodosta yhteys** -painike.
3. Power BI avaa ohjatun toiminnon, joka auttaa [yhteyden muodostusprosessissa](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Sinua pyydetään kirjatumaan palveluun. Valitse ensin **Kirjaudu sisään** ja sitten tili, johon haluat kirjautua. Valitse sama tili, jolla kirjaudut [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]iin.
4. Jatka valitsemalla **Muodosta yhteys**. Ohjatussa Power BI -toiminnossa on luettelo Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]in yrityksistä ja tietolähteistä. Nämä tietolähteet viittaavat kaikkiin verkkopalveluihin, jotka on julkaistu kullekin yritykselle Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]issa.
5. Voit vaihtoehtoisesti luoda uuden verkkopalvelun URL-osoitteen [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]issa käyttämällä **Luo tietojoukko** -toimintoa **WWW-palvelut**-sivulla tai asetusten ohjattua **Määritä raportointi** -määritystä tai valitsemalla **Muokkaa Excelissä** -toiminnon jossakin luettelossa.
6. Määritä tietomalliin lisättävät tiedot ja valitse sitten **Lataa**-painike.
7. Lisää uusia Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]- tai muita tietoja Power BI -tietomalliin toistamalla edellä olevat vaiheet.

> [!NOTE]  
> Kun yhteys Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]iin on muodostettu, sinua ei pyydetä kirjautumaan uudelleen.

Kun tiedot on ladattu, ne näkyvät sivun oikeassa siirtymisruudussa. Olet nyt muodostanut yhteyden Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -tietoihin ja olet valmis aloittamaan oman Power BI -raportin luomisen. 

Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -teematiedosto kannattaa tuoda ennen raportin luontia.  Teematiedosto luo värivalikoiman, jonka avulla voit luoda raportteja samalla värityylillä kuin Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -sisältöpaketeissa ilman, että kunkin visuaalisen ominaisuuden mukautetut värit on määritettävä erikseen.

Lisätietoja on kohdassa [Power BI -dokumentaatio](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Katso myös
[Business Intelligence](bi.md)  
[Käytön aloittaminen](product-get-started.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)   
[Rahoitus](finance.md)  
[Power BI:n yhdistäminen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  

