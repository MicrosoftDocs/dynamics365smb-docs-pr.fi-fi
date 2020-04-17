---
title: Business Centralin käyttäminen Power BI -raporteissa | Microsoft Docs
description: Määritä tiedot käytettäviksi Power BI:n tietolähteenä ja tehokkaiden liiketoiminnan tilasta kertovien raporttien luomista varten.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 4f140303f037ea4a914cba1ded44fd453bcdfabb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187890"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a>[!INCLUDE [prodlong](includes/prodlong.md)]in käyttö Power BI:n tietolähteenä raportteja luotaessa

Voit määrittää [!INCLUDE[prodlong](includes/prodlong.md)]in tiedot käytettäviksi Power BI:n tietolähteenä ja tehokkaiden liiketoiminnan tilasta kertovien raporttien luomista varten.  

Sinulla on oltava kelvollinen [!INCLUDE[prodshort](includes/prodshort.md)]- ja Power BI -tili. Lisäksi on ladattava [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Lisätietoja on kohdassa [Pika-aloitus: Power BI Desktopin tietoihin yhdistäminen](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a>[!INCLUDE[prodshort](includes/prodshort.md)]in lisääminen Power BI Desktopin tietolähteeksi

1. Valitse Power BI Desktopin vasemmassa siirtymisruudussa **Nouda tiedot**.
2. Valitse **Nouda tiedot** -sivulla **Online Services**. Valitse sitten **Microsoft Dynamics 365 Business Central** ja valitse lopuksi **Muodosta yhteys** -painike.
3. Power BI avaa ohjatun toiminnon, joka auttaa yhteyden muodostusprosessissa. Tähän kuuluu myös sovellukseen [!INCLUDE [prodshort](includes/prodshort.md)] kirjautuminen. Valitse **Kirjaudu sisään**ja valitse sitten haluamasi tili. Käytä samaa tiliä, jonka avulla kirjaudut sisään sovellukseen [!INCLUDE [prodshort](includes/prodshort.md)].
4. Jatka valitsemalla **Muodosta yhteys**. Ohjatussa Power BI -toiminnossa on luettelo Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]:n ympäristöistä, yrityksistä ja tietolähteistä. Nämä tietolähteet viittaavat kaikkiin sovelluksesta [!INCLUDE [prodshort](includes/prodshort.md)] julkaistuihin verkkopalveluihin.

    Voit myös luoda uuden verkkopalvelun URL-osoitteen sovelluksessa [!INCLUDE [prodshort](includes/prodshort.md)]. Valitse yksi seuraavista menetelmistä.

      - Käytä **Luo tietojoukkoa** -toiminto **Verkkopalvelut**-sivulla
      - Käytä **raportoinnin määrityksen** asetusten ohjattua määritysopasta
      - Valitse **Muokkaa Excelissä** -toiminto luetteloista

5. Määritä tietomalliin lisättävät tiedot ja valitse sitten **Lataa**-painike.
6. Lisää uusia [!INCLUDE [prodshort](includes/prodshort.md)]in tai muita tietoja Power BI -tietomalliin toistamalla edellä olevat vaiheet.

> [!NOTE]  
> Kun yhteys [!INCLUDE [prodshort](includes/prodshort.md)]iin on muodostettu, sinua ei pyydetä kirjautumaan uudelleen.

Kun tiedot on ladattu, ne näkyvät sivun oikeassa siirtymisruudussa. Olet muodostanut yhteyden sovelluksen [!INCLUDE [prodshort](includes/prodshort.md)] tietoihin ja voit aloittaa oman Power BI -raportin luomisen.  

[!INCLUDE [prodshort](includes/prodshort.md)] -teematiedosto kannattaa tuoda ennen raportin luontia.  Teematiedosto luo värivalikoiman, jonka avulla voit luoda raportteja samalla värityylillä kuin [!INCLUDE [prodshort](includes/prodshort.md)] -sovelluksissa ilman, että kunkin visuaalisen ominaisuuden mukautetut värit on määritettävä erikseen.

Lisätietoja on [Power BI -dokumentaatiossa](/power-bi/consumer/).

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Yritystietojen ottaminen käyttöön Power BI:tä varten](admin-powerbi.md)  
[Business Intelligence](bi.md)  
[Käytön aloittaminen](product-get-started.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  
[Pika-aloitus: Tietojen yhdistäminen Power BI Desktopiin](/power-bi/desktop-quickstart-connect-to-data)  
