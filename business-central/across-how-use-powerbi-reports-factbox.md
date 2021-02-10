---
title: Business Central -tietojen mukautettujen Power BI -raporttien näyttäminen | Microsoft Docs
description: Saat Power BI -raporttien avulla lisätietoja luetteloissa olevista tiedoista.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 069efcef517cd442539f13fad5e5a2c89e1533ff
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754465"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a>[!INCLUDE[prod_short](includes/prod_short.md)]in luettelotiedot näyttävien Power BI -raporttien luominen

[!INCLUDE[prod_long](includes/prod_long.md)]in useilla tärkeillä luettelosivuilla on ohjausobjektina tietoruutu, jossa on lisätietoja luettelon tiedoista. Raportti päivitetään ja suodatetaan valitun tapahtuman mukaan, kun siirryt luettelon riveillä. Voit luoda mukautettuja raportteja näyttämään tämän ohjausobjektin. Raporttien toimiminen odotetusti edellyttää muutamien sääntöjen noudattamista.  

## <a name="prerequisites"></a>Vaatimukset

- Power BI -tili.
- Power BI Desktop.

Lisätietoja aloittamisesta on kohdassa [[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power BI -tietolähteenä](across-how-use-financials-data-source-powerbi.md).

## <a name="defining-the-report-data-set"></a>Raportin tietojoukon määrittäminen

Määritä tietolähde, joka sisältää luetteloon liittyvät tiedot. Esimerkiksi myyntiluetteloa koskevaa raporttia luotaessa on varmistettava, että tietojoukko sisältää myyntiin liittyviä tietoja.  

## <a name="defining-the-report-filter"></a>Raporttisuodattimen määrittäminen

Lisäämällä suodatin raporttiin voidaan varmistaa, että tiedot päivittävät valitun tietueen luettelossa. Suodattimessa on oltava kenttä sen tietolähteen kenttä, jota käytetään *perusavaimena*. Useimmissa tapauksissa luettelon perusavain on **Nro** -kentässä.

Voit määrittää raporttisuodattimen valitsemalla käytettävissä olevien kenttien luettelosta perusavaimen sekä vetämällä ja pudottamalla kyseisen kentän **Raporttisuodatin**-kenttään. Suodattimen on oltava kaikille sivuille määritetty perusraporttisuodatin. Se ei voi olla sivu, visualisointi tai lisäsuodatus.

![Myyntilaskuaktiviteetti-raportin raporttisuodattimen määrittäminen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)

## <a name="setting-the-report-size-and-color"></a>Raportin koon ja värin määrittäminen

Raportin kooksi on määritettävä 325 x 310 kuvapistettä. Koon avulla raportti voidaan skaalata oikein Power BI:n tietoruutuohjausobjektin sallimassa tilassa [!INCLUDE[prod_short](includes/prod_short.md)]issa. Voit määrittää raportin koon viemällä kohdistuksen raportin asettelualueen ulkopuolelle ja valitsemalla maalitelakuvakkeen.

![Myyntilaskuaktiviteetti-raportin leveyden ja korkeuden määrittäminen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Voit muuttaa raportin leveyttä ja korkeutta valitsemalla **Tyyppi**-kentässä **Mukautettu**.

Jos haluat, että raportin tausta sulautuu Power BI:n tietoruutuohjausobjektin taustaväriin, määritä raportin taustaväriksi *#FFFFFF*. 

## <a name="using-reports-with-multiple-pages"></a>Useita sivuja sisältävien raporttien käyttäminen

Voit luoda Power BI:ssa yhden raportin, jossa on useita sivuja. Jos raportissa kuitenkin näytetään luettelosivuja, useamman kuin yhden sivun käyttö ei ole suositeltavaa. Power BI -tietoruudussa näkyy vain raportin ensimmäinen sivu.

## <a name="naming-the-report"></a>Raportin nimeäminen

Anna raportille nimi, joka sisältää raporttiin liitetyn luettelosivun nimen. Jos raportti koskee esimerkiksi **Toimittaja**-luettelosivua, nimessä on oltava sana *toimittaja*.  

Tätä nimeämiskäytäntöä ei ole pakko noudattaa. Se kuitenkin nopeuttaa raporttien valitsemista [!INCLUDE[prod_short](includes/prod_short.md)]issa. Jos raportin valintasivu avautuu luettelosivulta, se suodatetaan automaattisesti sivun nimen mukaan. Tämän suodatuksen avulla voidaan rajoittaa näytettävien raporttien määrää. Tyhjentämällä suodattimen käyttäjät saavat näkyviin luettelon kaikista Power BI:ssa käytettävistä raporteista.  

## <a name="fixing-problems"></a>Ongelmien korjaaminen

Tämän osan ohjeiden avulla voi kiertää tavallisimmat Power BI -raportin luomiseen liittyvät ongelmat.  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a>Raportti ei ole näkyvissä Valitse raportti -sivulla

Syynä luultavasti se, että raportin nimi ei sisällä luettelosivun nimeä. Saat näkyviin luettelon kaikista Power BI:ssa käytettävistä raporteista tyhjentämällä suodattimen.  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>Raportti ladataan, mutta se jää tyhjäksi, sitä ei suodateta tai se suodatetaan virheellisesti

Tarkista, että raportin suodattimessa on oikea perusavain. Useimmissa tapauksissa se on **Nro**-kenttä, mutta esimerkiksi **KP-tapahtuma**-kentässä on käytettävä **Tapahtumanro**-kenttää.

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>Raportti ladataan, mutta siinä ei näy odotettua sivua.

Tarkista, että sivu, jonka haluat näkyvän, on raportin ensimmäinen sivu.  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>Raportissa on tarpeettomat harmaat rajat tai se on liian pieni tai liian suuri

Tarkista, että raportin kooksi on määritetty 325 x 310 kuvapistettä. Tallenna raportti ja päivitä sitten luettelosivu.  

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Yritystietojen ottaminen käyttöön Power BI:tä varten](admin-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerbi.md)  
[Käytön aloittaminen](product-get-started.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  
