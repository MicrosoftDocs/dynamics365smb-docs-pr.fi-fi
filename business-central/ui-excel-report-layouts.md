---
title: Excel-asettelujen käyttö
description: Tietoja Excelin avulla rakennettujen raportin asettelujen luomisesta ja muokkaamisesta.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/14/2022
ms.author: jswymer
ms.openlocfilehash: 609678742ccf9593407e96ea412a377f37c8abf9
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525059"
---
# <a name="working-with-excel-layouts"></a>Excel-asettelujen käyttö

Excel-raportin asettelujen perustana ovat Microsoft Excel-työkirjat (.xlsx-tiedostot). Niiden avulla voit luoda raportteja käyttämällä tuttuja Excelin ominaisuuksia yhteenvetoon, analysointiin ja tietojen esittämiseen, kuten kaavoja, pivot-taulukoita ja pivot-kaavioita.

![Näyttää esimerkin Excelin asettelusta.](media/excel-layout-2.png)

Tässä artikkelissa selitetään joitakin tärkeimpiä asioita, jotka sinun on tiedettävä, jotta voit aloittaa Excelin asettelujen käytön.

## <a name="why-use-excel-layouts"></a>Miksi kannattaa käyttää Excel-asetteluja?

Seuraavassa on joitakin Excelin asettelujen käyttämisen etuja:

- Vuorovaikutteisten raporttien luominen osittajien kaltaisten visualisointien avulla
- Raakatietojen tarkasteleminen raportin tietojoukosta, jotta ymmärrät paremmin raportin toiminnan ja visuaalisten tietojen lähteen
- Käytä sisäisiä Office-ominaisuuksia, kun haluat tehdä hahmonnettujen raporttien jälkikäsittelyn, esimerkiksi:
  - [Työkirjojen suojaaminen](https://support.microsoft.com/en-us/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Arkaluonteisuusselitteiden käyttäminen](https://support.microsoft.com/en-us/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Kommenttien ja muistiinpanojen lisääminen](https://support.microsoft.com/en-us/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Ennuste ja analyysi](https://support.microsoft.com/en-us/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4) 
- Käytä asennettuja apuohjelmia ja sovellusten integraatioita, kuten Power Automate-työnkulut tai OneDrive.

## <a name="get-started"></a>Aloitus

Raportin Excel-asettelun määrittämiseen liittyy periaatteessa kaksi tehtävää:

1. Luo uusi Excel-asettelutiedosto.
2. Lisää uusi asettelu raporttiin.

## <a name="task-1-create-the-excel-layout-file"></a>Tehtävä 1: Luo Excel-asettelutiedosto

Excel-asettelutiedoston voi luoda raporttiin kolmella tavalla tässä osassa selitetyllä tavalla.

### <a name="from-any-report"></a>[Mistä tahansa raportista](#tab/any-report)

Seuraavien vaiheiden avulla voit luoda Excelin asettelun mistä tahansa raportista valitusta asettelutyypistä riippumatta. Excel-asettelussa on tarvittava **Tiedot**-laskentataulukko ja -taulukko, **Raportin metatiedot** -laskentataulukko ja ei mitään muuta.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Valitse **Raporttiasettelut**-luettelosta raportin asettelu ja valitse sitten **Suorita raportti** -toiminto.
3. Valitse raportin pyyntösivulla **Lähetä** > **Microsoft Excel Asiakirja (vain tiedot)** > **OK**.

   Tämä vaihe lataa Excel-työkirjan, joka sisältää raportin tietojoukon.
4. Avaa ladattu tiedosto Excelissä, tee muutokset ja tallenna sitten tiedosto.

### <a name="from-another-excel-layout-on-a-report"></a>[Toisesta raportin Excel-asettelusta](#tab/other-layout)

Jos raportille on jo Excel-asettelu, voit käyttää aiemmin luotua asettelua lähtökohtana. Käytettävissä on kaksi tapaa saada kopio asettelusta. Voit viedä aiemmin luodun asettelun **Raporttiasettelut**-sivulta tai ladata asettelun raportin pyyntösivulta. Kumpikin tapa lataa Excel-asettelutiedoston, joka sisältää kaikki olemassa olevan tiedoston raportit. Erona on se, että pyyntösivulta asettelu sisältää todellisia tietoja. Tiedot eivät ole pakollisia, mutta ne auttavat asettelun suunnittelussa.

#### <a name="approach-1-export-the-layout-from-the-report-layouts-page"></a>Lähestymistapa 1: asettelun vieminen **Raporttiasettelut**-sivulta

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Valitse Excel-asettelu luettelosta ja valitse sitten **Vie asettelu** -toiminto sivun yläosasta.
3. Avaa tiedosto Excelissä, tee muutokset ja tallenna sitten tiedosto.

#### <a name="approach-2-download-the-layout-from-the-reports-request-page"></a>Lähestymistapa 2: Lataa asettelu raportin pyyntösivulta

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Valitse **Raporttiasettelut**-luettelosta raportin asettelu ja valitse sitten **Suorita raportti** -toiminto.
3. Valitse raporttipyyntösivulta **Lataa**.
4. Avaa tiedosto Excelissä, tee muutokset ja tallenna sitten tiedosto.

### <a name="from-al-code"></a>[AL-koodista](#tab/from-code)

Tämä on kehittynein tapa. Se vaatii tietoa AL-koodista, joten se on kohdistettu ohjelmoijille. Tässä tapauksessa Excel-asettelut ovat osa asennettavia laajennuspaketteja. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeen kohdassa [Excel-asetteluraportin luominen](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout).

---

## <a name="task-2-add-the-excel-layout-to-the-report"></a>Tehtävä 2: Lisää Excel-asettelu raporttiin

Kun sinulla on Excelin asettelutiedosto, seuraava tehtävä on lisätä se raportin uudeksi asetteluksi.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Valitse **Uusi asettelu**.
3. Määritä raportoitava **Raportin tunnus**.
4. Syötä nimi kohtaan **Asettelun nimi**.
5. Määritä **Muotoasetukset**-kohdan arvoksi **Excel**.
6. Valitse **OK** > **Valitse**, jos haluat avata Resurssienhallinnan laitteessasi. 
7. Etsi ja valitse Excel-tiedosto ja valitse sitten **Avaa**.

   Valitsemasi tiedosto ladataan asetteluun, ja palaat **Raporttiasettelut**-sivulle.
8. Jos haluat nähdä, miltä raportti näyttää uudessa asettelussa, valitse asettelu luettelosta ja valitse sitten **Suorita raportti**.


<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet can only include one table named **Data**.

**Data** table
  - The **Data** sheet must include a table that has the name **Data**.
  - The table must have at least one column and can only include columns that are also in report dataset.
  - The table must start in the first cell A1 of the **Data** sheet.

3. Report Metadata 
-->

## <a name="understanding-excel-layouts"></a>Tietoja Excelin asetteluista

On muutamia asioita, jotka kannattaa tietää tai ottaa huomioon, kun alat luoda tai tehdä muutoksia Excelin asetteluihin. Jokaisessa Excel-asettelussa on oltava kaksi elementtiä: **Tiedot**-laskentataulukko ja **Tiedot**-taulukko. Nämä elementit muodostavat asettelun perusteet määrittämällä Business Centralin liiketoimintatiedot, joita voit käsitellä. Voit ajatella **Tiedot**-laskentataulukkoa eräänlaisena sopimuksena yritystietojen asettelun välillä. Näitä tietoja käytetään niiden laskentojen ja visualisointien lähteenä, jotka haluat esittää muissa laskentataulukoissa.

Excel-työkirjan rakenteeseen liittyy tiettyjä erityisvaatimuksia. Jos vaatimukset eivät täyty, asettelun käytössä on ongelmia. Seuraavassa kaaviossa ja taulukossa on Excelin asettelun elementit ja vaatimukset.

[![Näyttää Excelin asettelun erilaiset elementit.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|Ei.|Elementti|Kuvaus|Pakollinen|
|---|-------|----|---|
|1|**Tiedot**-laskentataulukko|<ul><li>On oltava nimeltään **Tiedot**</li><li>Voi sisältää vain yhden taulukon, ja taulukon on oltava nimeltään **Tiedot**</li></ul>|![On pakollinen](media/check.png) | 
|2|**Tiedot**-taulukko|<ul><li>On oltava nimeltään **Tiedot**</li><li>Pitää sisältää vähintään yksi sarake.</li><li>Voi sisältää vain raportin tietojoukon sarakkeita.</li><li>Pitää alkaa ensimmäisestä solusta **A1** **Tiedot**-laskentataulukossa</li></ul>|![On pakollinen](media/check.png)|
|3|Esitystaulukot|<ul><li>Käytetään tietojen esittämisessä.</li><li>Tiedot ovat peräisin **Tiedot**-laskentataulukosta. </li></ul>||
|4|**Raportin metatiedot** -laskentataulukko|<ul><li>Sisällytetään automaattisesti, jos asettelu luotiin viemällä toinen raportti Excel-muodossa</li><li>Sisältää yleistietoa raportista</li><li>Voidaan poistaa</li></ul>|

Yhteenveto siitä, mitä voit ja mitä et voi tehdä **Tiedot**-laskentataulukossa:

- Älä muuta **Tiedot**-laskentataulukon, **Tiedot**-taulukon tai sarakkeiden nimeä.
- Voit poistaa tai piilottaa sarakkeita.
- Älä lisää sarakkeita, elleivät ne sisälly raportin tietojoukkoon.
- Voit sijoittaa laskentataulukot mihin tahansa järjestykseen. Esimerkiksi **Tiedot**-laskentataulukko voi olla ensimmäinen tai viimeinen.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
[Nykyisen raportin asettelun muuttaminen](ui-how-change-layout-currently-used-report.md)  
[Raporttien tai asiakirjojen mukautetun asettelun tuonti ja vienti](ui-how-import-and-export-report-layout.md)  
[Raporttien, eräajojen ja XMLportien käsitteleminen](ui-work-report.md)  
[Talousraportoinnin valmisteleminen KP-raporttimallien ja tililuokkien avulla](bi-how-work-account-schedule.md)  
[Liiketoimintatiedot](bi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Raporttitietojen analysointi Excelillä](report-analyze-excel.md).


[!INCLUDE[footer-include](includes/footer-banner.md)]