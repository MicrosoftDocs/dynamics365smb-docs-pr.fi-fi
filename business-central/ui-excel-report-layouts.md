---
title: Excel-asettelujen käyttö
description: Tietoja Excelin avulla rakennettujen raportin asettelujen luomisesta ja muokkaamisesta.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 11/10/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Microsoft Excel -asetteluiden käyttäminen

Excel-työkirjojen perustana ovat Microsoft Excel -raporttiasettelut (.xlsx-tiedostot). Niiden avulla voit luoda raportteja, jotka sisältävät tuttuja Excelin ominaisuuksia yhteenvetoon, analysointiin ja tietojen, kuten kaavojen, pivot-taulukoiden ja pivot-kaavioiden, esittämiseen.

![Näyttää esimerkin Excelin asettelusta.](media/excel-layout-2.png)

Tässä artikkelissa selitetään joitakin tärkeitä, asioita, jotka sinun on tiedettävä, jotta voit aloittaa Excelin asettelujen käytön.

## Miksi kannattaa käyttää Excel-asetteluja?

Seuraavassa kerrotaan Excelin asettelujen käyttämisen hyötyjä:

- Vuorovaikutteisten raporttien luominen osittajien kaltaisten visualisointien avulla.
- Tarkastele raportin tietojoukon raakatietoja, jotta ymmärrät paremmin raportin toiminnan ja visuaalisten tietojen lähteen.
- Käytä sisäisiä Microsoft Office -ominaisuuksia, kun haluat tehdä hahmonnettujen raporttien jälkikäsittelyn, joka voi olla esimerkiksi jokin seuraavista toiminnoista:
  - [Työkirjojen suojaaminen](https://support.microsoft.com/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Arkaluonteisuusselitteiden käyttäminen](https://support.microsoft.com/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Kommenttien ja muistiinpanojen lisääminen](https://support.microsoft.com/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Ennuste ja analyysi](https://support.microsoft.com/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4)
- Käytä asennettuja apuohjelmia ja sovellusten integraatioita, kuten Power Automate-työnkulkuja tai OneDrivea.

## Aloittaminen

Raportin Excel-asettelun määrittämiseen liittyy periaatteessa kaksi seuraavaa tehtävää:

1. Luo uusi Excel-asettelutiedosto.
2. Lisää uusi asettelu raporttiin.

## Tehtävä 1: Luo Excel-asettelutiedosto

Excel-asettelutiedoston voi luoda raporttiin kolmella alla mainitulla tavalla.

### [Mistä tahansa raportista](#tab/any-report)

Näiden vaiheiden avulla voit luoda Excelin asettelun mistä tahansa raportista valitusta asettelutyypistä riippumatta. Excel-asettelussa on tarvittava **Tiedot**-laskentataulukko ja -taulukko, **Raportin metatiedot** -laskentataulukko ja ei mitään muuta.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Valitse **Raporttiasettelut**-sivulla mikä tahansa raportin asettelu ja valitse sitten **Suorita raportti** -toiminto.
3. Valitse raportin pyyntösivulla **Lähetä** > **Microsoft Excel Asiakirja (vain tiedot)** > **OK**.

   Tämä vaihe lataa Excel-työkirjan, joka sisältää raportin tietojoukon.
4. Avaa ladattu tiedosto Excelissä, tee muutokset ja tallenna sitten tiedosto.

### [Toisesta Excel-raportin asettelusta](#tab/other-layout)

Jos raportille on jo Excel-asettelu, voit käyttää aiemmin luotua asettelua lähtökohtana. Käytettävissä on kaksi tapaa saada kopio asettelusta. Voit joko viedä aiemmin luodun asettelun **Raporttiasettelut**-sivulta tai ladata asettelun raportin pyyntösivulta. Kumpikin tapa lataa Excel-asettelutiedoston, joka sisältää kaikki olemassa olevan tiedoston raportit. Jos se ladataan pyyntösivulta, asettelu sisältää todelliset tiedot. (Tiedot eivät ole pakollisia, mutta ne auttavat asettelun suunnittelussa.)

#### Lähestymistapa 1: asettelun vieminen **Raporttiasettelut**-sivulta

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Valitse Excel-asettelu luettelosta ja valitse sitten **Vie asettelu** -toiminto sivun yläosasta.
3. Avaa tiedosto Excelissä, tee muutokset ja tallenna sitten tiedosto.

#### Lähestymistapa 2: Lataa asettelu raportin pyyntösivulta

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Valitse **Raporttiasettelut**-sivulla mikä tahansa raportin asettelu ja valitse sitten **Suorita raportti** -toiminto.
3. Valitse raportin pyyntösivulta **Lataa**.
4. Avaa tiedosto Excelissä, tee muutokset ja tallenna sitten tiedosto.

### [AL-koodista](#tab/from-code)

Tämä on kehittynein tapa Excel-raportin asettelun luomiseksi. Se on kohdistettu ohjelmoijille, koska se vaatii tietämystä AL-koodista. Tässä tapauksessa Excel-asettelut ovat osa asennettavia laajennuspaketteja. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeen kohdassa [Excel-asetteluraportin luominen](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout).

---

## Tehtävä 2: Lisää Excel-asettelu raporttiin

Kun sinulla on Excelin asettelutiedosto, seuraava tehtävä on lisätä se raportin uudeksi asetteluksi.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Valitse **Uusi asettelu**.
3. Määritä **raportin tunnukseksi** *Raportti*.
4. Syötä nimi kohtaan **Asettelun nimi**.
5. Määritä **Muotoasetukset**-kohdan arvoksi **Excel**.
6. Valitse **OK** ja lataa sitten raportin asettelutiedosto tekemällä jokin seuraavista toimista:

   [!INCLUDE[file-upload](includes/file-upload.md)]

   Valitsemasi tiedosto ladataan asetteluun, ja **Raporttiasettelut**-sivu avautuu.
8. Näet, miltä raportti näyttää uudessa asettelussa, valitsemalla asettelu luettelosta ja valitsemalla sitten **Suorita raportti**.

<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet must include a table named **Data**.

**Data** table
  - The **Data** sheet must include a table named **Data**.
  - The table must have at least one column and can only include columns that are also in the report dataset.
  - The table must start in the first cell **A1** of the **Data** sheet.

3. Report metadata 
-->

## Tietoja Excelin asetteluista

On muutamia asioita, jotka tulee tietää tai ottaa huomioon, kun alat luoda tai tehdä muutoksia Excelin asetteluihin. Jokaisessa Excel-asettelussa on oltava kaksi elementtiä: **Tiedot**-laskentataulukko ja **Tiedot**-taulukko. Nämä elementit muodostavat asettelun perusteet määrittämällä Business Centralin liiketoimintatiedot, joita voit käsitellä. Voit ajatella **Tiedot**-laskentataulukkoa eräänlaisena sopimuksena asettelun ja yritystietojen välillä. Näitä tietoja käytetään niiden laskentojen ja visualisointien lähteenä, jotka haluat esittää muissa laskentataulukoissa.

Excel-työkirjan rakenteeseen liittyy tiettyjä erityisvaatimuksia. Jos vaatimukset eivät täyty, asettelun käytössä on ongelmia. Seuraavassa kaaviossa ja taulukossa on Excelin asettelun elementit ja vaatimukset.

[![Näyttää Excelin asettelun erilaiset elementit.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|Nro|Elementti|Kuvaus|Pakollinen|
|---|-------|----|---|
|1|**Tiedot**-laskentataulukko|<ul><li>On oltava nimeltään **Tiedot**.</li><li>Voi sisältää vain yhden taulukon, ja jonka on oltava nimeltään **Tiedot**.</li></ul>|![On pakollinen](media/check.png) | 
|2|**Tiedot**-taulukko|<ul><li>On oltava nimeltään **Tiedot**.</li><li>Pitää sisältää vähintään yksi sarake.</li><li>Voi sisältää vain raportin tietojoukon sarakkeita.</li><li>Pitää alkaa ensimmäisestä solusta **A1** **Tiedot**-laskentataulukossa.</li></ul>|![On pakollinen](media/check.png)|
|3|Esitystaulukot|<ul><li>Käytetään tietojen esittämisessä.</li><li>Tiedot ovat peräisin **Tiedot**-laskentataulukosta. </li></ul>||
|4|**Raportin metatiedot** -laskentataulukko|<ul><li>Sisällytetään automaattisesti, jos asettelu luotiin viemällä toinen Excel-raportti.</li><li>Sisältää yleistietoa raportista.</li><li>Voidaan poistaa.</li></ul>|

Seuraavassa on yhteenveto tiedoista, jotka **Tiedot**-laskentataulukossa tulee olla ja joita siellä ei tule olla:

- Älä muuta **Tiedot**-laskentataulukon, **Tiedot**-taulukon tai sarakkeiden nimeä.
- Voit poistaa tai piilottaa sarakkeita.
- Älä lisää sarakkeita, elleivät ne sisälly raportin tietojoukkoon.
- Voit sijoittaa laskentataulukot haluamaasi järjestykseen niin, että **Tiedot**-laskentataulukko on ensimmäisenä tai viimeisenä.

## Katso myös

[Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
[Nykyisen raportin asettelun muuttaminen](ui-how-change-layout-currently-used-report.md)  
[Raporttien tai asiakirjojen mukautetun asettelun tuonti ja vienti](ui-how-import-and-export-report-layout.md)  
[Raporttien, eräajojen ja XMLportien käsitteleminen](ui-work-report.md)  
[Talousraportoinnin valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md)  
[Business Intelligence](bi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Raporttitietojen analysointi Excelillä](report-analyze-excel.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
