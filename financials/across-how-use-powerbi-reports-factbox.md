---
title: "Näytä mukautettuja Power BI -raportteja| Microsoft Docs"
description: "Voit käyttää Power BI -raportteja saamaan lisätietoja Financialsin luetteloissa olevista tiedoista."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 9b4190ca0ffbc0a922c6679fcf98367a72980eea
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="viewing-list-data-in-power-bi-reports-in-finance-and-operations-business-edition"></a>Power BI -raporttien luettelotietojen tarkastelu Finance and Operations, Business editionissa 
[!INCLUDE[d365fin](includes/d365fin_md.md)] in useilla tärkeillä luettelosivuilla on ohjauselementtinä tietoruutu, jolla saa lisätietoja luettelon tiedoista. Raportti päivitetään ja suodatetaan valitun tapahtuman mukaan, kun siirryt luettelon riveillä. Voit luoda mukautettuja raportteja, joissa tämä ohjausobjekti on esillä. Raportteja luotaessa on kuitenkin noudatettava tiettyjä sääntöjä, jotta ne toimisivat halutulla tavalla.  

> [!NOTE]  
>   Sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja Power BI -tili. Sinun on ladattava myös [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/). Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power BI -tietolähteenä](across-how-use-financials-data-source-powerbi.md).  

## <a name="report-data-set"></a>Raportin tietojoukko
Kun luot raportin Power BI Desktopissa, sinun on määritettävä tietolähde tai verkkopalvelu, joka sisältää siihen luetteloon liittyvät tiedot, johon haluat liittää raportin. Jos haluat esimerkiksi luoda myyntiluetteloa koskevan raportin, varmista, että tietojoukko sisältää myyntiin liittyviä tietoja.  

Jos haluat suodattaa raporttien tietoja luettelosivulta valitun tietueen perusteella, raportin suodattimena on käytettävä perusavainta. Perusavaimien on oltava osa tietojoukkoa, jotta raportti voidaan suodattaa oikein. Useimmissa tapauksissa luettelon perusavain on **Nro** -kentässä.  

## <a name="defining-the-report-filter"></a>Raporttisuodattimen määrittäminen
Raportissa on oltava perusraporttisuodatin (ei sivu-, visuaalinen eikä lisäsuodatus), jotta suodatus tapahtuu oikein Power BI:n tietoruutuohjausobjektissa. Power BI -raporttiin kultakin luettelosivulta siirrettävä suodatin perustuu perusavaimeen edellisessä osassa kuvatulla tavalla.  

Voit määrittää raporttisuodattimen valitsemalla käytettävissä olevien kenttien luettelosta perusavaimen sekä vetämällä ja pudottamalla kyseisen kentän **Raporttisuodatin**-kenttään.  

![Myyntilaskuaktiviteetti-raportin raporttisuodattimen määrittäminen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="report-size-and-color"></a>Raportin koko ja väri
Raportin kooksi on määritettävä 325 x 310 kuvapistettä. Tämä on välttämätöntä, jotta raportin voi skaalata oikein Power BI:n tietoruutuohjausobjektin sallimassa tilassa. Voit määrittää raportin koon viemällä kohdistuksen raportin asettelualueen ulkopuolelle ja valitsemalla maalitelakuvakkeen.

![Myyntilaskuaktiviteetti-raportin leveyden ja korkeuden määrittäminen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

Voit muuttaa raportin leveyttä ja korkeutta valitsemalla **Tyyppi**-kentässä **Mukautettu**.

Jos vastaavasti haluat, että raportin tausta sekoittuu Power BI:n tietoruutuohjausobjektin taustaväriin, määritä mukautetun raportin taustaväriksi *E5E5E5*. Tämä on vapaaehtoinen.  

## <a name="reports-with-multiple-pages"></a>Useita sivuja sisältävät raportit
Voit luoda Power BI:ssa yhden raportin, jossa on useita sivuja. [!INCLUDE[d365fin](includes/d365fin_md.md)]in luettelosivulla näkyvien visualisointien on oltava Power BI:n raporttien ensimmäisellä sivulla.  

> [!NOTE]  
>  Power BI:n tietoruutu voi näyttää vain raportin ensimmäisen sivun. Jos haluat nähdä muut sivut, laajenna raportti ja siirry muille sivuille raportin alareunassa olevien välilehtien avulla.  

## <a name="saving-your-report"></a>Raportin tallentaminen

Raporttia tallennettaessa on parhaan käytännön mukaista käyttää raportin nimessä sen luettelosivun nimeä, jossa haluat näyttää raportin. Esimerkki: *Toimittaja*-sanan on sisällyttävä niiden raporttien nimiin, jotka ovat käytettävissä toimittajaluettelossa.  

Vaikka tämä ei ole välttämätöntä, se helpottaa raporttien valitsemista. Kun raportin valintasivu avataan luettelosivulta, suodatin siirretään sivun nimen perusteella rajoittamaan näytettäviä raportteja.  Voit poistaa suodattimen, jos haluat luettelon kaikista käytössäsi olevista Power BI:n raporteista.  

## <a name="troubleshooting"></a>Vianetsintä
Tässä osassa esitellään tapa, jolla voidaan kiertää tavallisimmat Power BI -raportin luomiseen liittyvät ongelmat.  

**Käyttäjä ei näe Valitse raportti -sivulla raporttia, jonka he haluavat valita** Jos et voi valita raporttia, raportin nimi kannattaa tarkistaa ja varmistaa, että se sisältää luettelosivun nimen. Voit myös tyhjentää suodattimen, jos haluat luettelon kaikista käytössä olevista Power BI:n raporteista.  

**Raportti on ladattu, mutta se on tyhjä, suodattamaton tai virheellisesti suodatettu** Tarkista, että raporttisuodatin sisältää oikean perusavaimen. Useimmissa tapauksissa se on **Nro**-kenttä, esimerkiksi **KP-tapahtuma**-kentässä on käytettävä **Tapahtumanro**-kenttää.

**Raportti on ladattu, mutta näkyvissä ei ole odotettu sivu** Tarkista, että näytettävä sivu on raportin ensimmäinen sivu.  

**Raportissa on tarpeettomat harmaat rajat tai se on liian pieni tai suuri**

Tarkista, että raportin kooksi on määritetty 325 x 310 kuvapistettä. Tallenna raportti ja päivitä sitten luettelosivu.  

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power BI -tietolähteenä](across-how-use-financials-data-source-powerbi.md)  
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)    
[Rahoitus](finance.md)  

