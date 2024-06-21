---
title: Näytä mukautetut Power BI -raportit
description: Voit käyttää Power BI -tietoruutua Power BI -raporttien näyttämiseen ja saat myös lisää merkityksellistä tietoa tärkeiden luetteloiden tietuetiedoista.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 12/13/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# [!INCLUDE[prod_short](includes/prod_short.md)]in luettelotiedot näyttävien Power BI -raporttien luominen

[!INCLUDE[prod_long](includes/prod_long.md)] sisältää Power BI -tietoruudun ohjausobjektielementin monilla tärkeillä luettelosivuilla. Tietoruudun tarkoitus on näyttää Power BI -raportteja, jotka liittyvät luetteloissa oleviin tietueisiin. Tällä tavoin tiedoista saadaan parempi käsitys. Raportti päivitetään valitun tapahtuman mukaan, kun siirryt luettelon riveillä.

Osa näistä raporteista toimitetaan [!INCLUDE[prod_long](includes/prod_long.md)]in mukana. Lisäksi tässä tietoruudussa näytettäväksi voi luoda omia mukautettuja raportteja. Näiden raporttien luonti muistuttaa muiden raporttien luontia. On kuitenkin muutamia suunnittelusääntöjä, joita noudattamalla voidaan varmistaa, että raportit näkyvät odotetusti. Näitä sääntöjä käsitellään tässä artikkelissa.

> [!NOTE]
> Yleisiä tietoja Business Centralin Power BI -raporttien luomisesta ja julkaisemisesta on kohdassa [Power BI -raporttien muodostaminen näyttämään [!INCLUDE [prod_long](includes/prod_long.md)] -tietoja](across-how-use-financials-data-source-powerbi.md). 

## Vaatimukset

- Power BI -tili.
- Power BI Desktop.

<!-- 
For more information about getting started, see [Use [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## Raportin luominen luettelosivulle

1. Käynnistä Power BI Desktop.
2. Valitse **Hae tiedot** ja aloita raportin tietolähteen valitseminen.

    Määritä Business Centralin luettelosivut, jotka sisältävät raportissa käytettävät tiedot. Esimerkiksi **myyntilaskuluetteloa** koskevaa raporttia luotaessa sisällytetään myyntiin liittyvät sivut.

    Lisätietoja on kohdassa [[!INCLUDE[prod_short](includes/prod_short.md)]in lisääminen tietolähteenä Power BI Desktopissa](across-how-use-financials-data-source-powerbi.md#getdata).

3. Määritä raporttisuodatin.

    Lisäämällä suodatin raporttiin voidaan varmistaa, että tiedot päivittävät valitun tietueen luettelossa. Suodattimessa on oltava sen tietolähteen kenttä, jota käytetään luettelon kunkin tietueen yksilöivään tunnistamiseen. Kehittäjät kutsuvat tätä kenttää *perusavaimeksi*. Useimmissa tapauksissa luettelon perusavain on **Nro** -kentässä.

    Määritä suodatin seuraavasti:

    1. Valitse **Suodattimet**-kohdassa perusavainkenttä käytettävissä olevien kenttien luettelosta.
    2. Vedä kenttä **Suodattimet**-ruutuun ja pudota se **Suodattimet kaikilla sivuilla** -ruutuun.
    3. Määritä **suodattimen tyypiksi** **Perussuodatus**. Se ei voi olla sivu, visualisointi tai lisäsuodatus.

    ![Myyntilaskuaktiviteetti-raportin raporttisuodattimen määrittäminen.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. Suunnittele raportin asettelu.

    Luo suunnittelu vetämällä kenttiä ja lisäämällä visualisointeja. Lisätietoja on Power BI -dokumentaation kohdassa [Raporttinäkymän käyttäminen Power BI Desktopissa](/power-bi/create-reports/desktop-report-view).

5. Seuraavissa osissa on tietoja raportin koon muuttamisesta ja useiden sivujen käyttämisestä.

6. Tallenna raportti ja anne sille nimi.

    Anna raportille nimi, joka sisältää raporttiin liitetyn luettelosivun nimen, koska se on asiakasohjelmassa. Kirjainkoolla ei ole merkitystä. Oletetaan, että raportti on **Myyntilaskut**-luettelosivulla. Tässä tapauksessa sisällytetään sana **myyntilaskut** jonnekin kohtaa nimeä, esimerkiksi **omat myyntilaskut.pbix** tai **omat_myyntilaskut_luettelona.pbix**.

    Tätä nimeämiskäytäntöä ei ole pakko noudattaa. Se kuitenkin nopeuttaa raporttien valitsemista [!INCLUDE[prod_short](includes/prod_short.md)]issa. Jos raportin valintasivu avautuu luettelosivulta, siihen kohdistetaan automaattisesti suodatin sivun nimen mukaan. Suodattimella on syntaksi `@*<caption>*`, esimerkiksi `@*Sales Invoices*`. Tämän suodatuksen avulla voidaan rajoittaa näytettävien raporttien määrää. Tyhjentämällä suodattimen käyttäjät saavat näkyviin luettelon kaikista Power BI:ssa käytettävistä raporteista.

7. Kun olet valmis, julkaise raportti tavalliseen tapaan.

    Lisätietoja on kohdassa [Raportin julkaiseminen](across-how-use-financials-data-source-powerbi.md#publish-reports).

8. Testaa raporttia.

    Kun raportti on julkaistu työtilaan, sitä pitäisi voida käyttää Power BI -tietoruudusta [!INCLUDE[prod_short](includes/prod_short.md)]in luettelosivulla.

    Testaa seuraavasti, että näin on:

    1. Avaa [!INCLUDE[prod_short](includes/prod_short.md)] ja siirry luettelosivulle.
    2. Jos Power BI -tietoruutu ei ole näkyvissä, valitse siinä tapauksessa toimintorivillä **Toiminnot** > **Näytä** > **Näytä tai piilota Power BI -raportit**.
    3. Valitse Power BI -tietoruudussa ensin **Valitse raportit**, sitten raportin **Ota käyttöön** -ruutu ja lopuksi **OK**.

    Oikein suunniteltu raportti tulee näkyviin.  

## Raportin koon ja värin määrittäminen

Raportin kooksi on määritettävä 325 x 310 kuvapistettä. Koon avulla raportti voidaan skaalata oikein Power BI:n tietoruutuohjausobjektin sallimassa tilassa [!INCLUDE[prod_short](includes/prod_short.md)]issa. Voit määrittää raportin koon viemällä kohdistuksen raportin asettelualueen ulkopuolelle ja valitsemalla maalitelakuvakkeen.

![Myyntilaskuaktiviteetti-raportin leveyden ja korkeuden määrittäminen.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Voit muuttaa raportin leveyttä ja korkeutta valitsemalla **Tyyppi**-kentässä **Mukautettu**.

Jos haluat, että raportin tausta sulautuu Power BI:n tietoruutuohjausobjektin taustaväriin, määritä raportin taustaväriksi *#FFFFFF* (valkoinen). 

> [!TIP]
> Muodosta [!INCLUDE [prod_short](includes/prod_short.md)] -teematiedoston avulla raportteja, joissa on käytössä sama värityyli kuin [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksissa. Lisätietoja on ohjeaiheessa [[!INCLUDE [prod_short](includes/prod_short.md)] -raporttiteeman käyttäminen](across-how-use-financials-data-source-powerbi.md#theme).

## Useita sivuja sisältävät raportit

Voit luoda Power BI:ssa yhden raportin, jossa on useita sivuja. Jos raportissa kuitenkin näytetään luettelosivuja, useamman kuin yhden sivun käyttö ei ole suositeltavaa. Power BI -tietoruudussa näkyy vain raportin ensimmäinen sivu.

## Ongelmien korjaaminen

Tässä osassa on ohjeet sellaisten ongelmien korjaamiseen, joita voi esiintyä yrittäessäsi näyttää tuotteen [!INCLUDE[prod_short](includes/prod_short.md)] luettelosivun Power BI -raporttia.  

### Power BI -tietoruutu ei näy luettelosivulla.

Power BI -tietoruutu on oletusarvoisesti piilotettu. Tietoruudun voi näyttää sivulla valitsemalla toimintorivillä **Toiminnot** > **Näytä** > **Näytä tai piilota Power BI -raportit**.

### Raportti ei ole näkyvissä Valitse raportti -ruudussa

Raportin nimi ei sisällä näytettävän luettelosivun nimeä. Saat näkyviin luettelon kaikista Power BI:ssa käytettävistä raporteista tyhjentämällä suodattimen.  

### Raportti ladataan, mutta se jää tyhjäksi, sitä ei suodateta tai se suodatetaan virheellisesti

Tarkista, että raportin suodattimessa on oikea perusavain. Useimmissa tapauksissa se on **Nro**-kenttä, mutta esimerkiksi **KP-tapahtuma**-kentässä on käytettävä **Tapahtumanro**-kenttää.

### Raportti ladataan, mutta siinä ei näy odotettua sivua.

Tarkista, että sivu, jonka haluat näkyvän, on raportin ensimmäinen sivu.  

### Raportissa on tarpeettomat harmaat rajat tai se on liian pieni tai liian suuri

Tarkista, että raportin kooksi on määritetty 325 x 310 kuvapistettä. Tallenna raportti ja päivitä sitten luettelosivu.  

## Katso myös

[Yritystietojen ottaminen käyttöön Power BI:ta varten](admin-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerbi.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
