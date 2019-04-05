---
title: Business Central- ja Power BI -sisältöpaketit | Microsoft Docs
description: Analyysitietojen, liiketoimintatietoja ja tunnuslukujen hakeminen Business Central -tiedoista on helppoa Power BI- ja Business Central -sisältöpakettien avulla.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: 26fe722a863ada2bcd017e2bc614b976a7119a25
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795063"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Yritystietojen ottaminen käyttöön Power BI:tä varten
Lisätietojen hakeminen [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoihin on helppoa Power BI- ja [!INCLUDE[d365fin](includes/d365fin_md.md)] -sisältöpakettien avulla. Power BI hakee tiedot ja muodostaa näiden tietojen perusteella valmiin koontinäytön ja raportit.  

Sinulla on oltava kelvollinen Dynamics 365- ja Power BI -tili. Lisäksi [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) on ladattava, jos haluat luoda oman Power BI -raportteja. Power BI -sisältöpakettien käyttöä varten tarvitaan niiden taulukoiden käyttöoikeus, joista tiedot noudetaan. Lisätietoja on vaatimuksista on jäljempänä.  

Microsoft on julkaissut seuraavat sisältöpaketit:

| Sovellus | Description |
| --- | --- |
| Microsoft Business Central | Sisältää koontinäytön, jossa on tärkeitä aikaperusteisia taloustietoja, kuten tulojen ja menojen vertailu, käyttökate ja käyttöpääomasykli.|
| Microsoft Business Central - CRM | Sisältää koontinäytön, jossa on tärkeitä tietoja myyntimahdollisuuksista ja kontakteista.  |
| Microsoft Business Central - Myynti | Sisältää koontinäytön, jossa on tärkeitä tietoja myynnistä ja varastosta. |

## <a name="using-the-dashboards"></a>Koontinäyttöjen käyttäminen
Kussakin sisältöpaketissa on raportteja, joilla voi porautua tietoihin:

* Valitse koontinäytöstä jokin visuaalinen kohde, kun haluat käsitellä jotakin perustana olevasta raportista.  
* Suodata raportti tai lisää seurattavia kenttiä.  
* Kiinnitä tämä mukautettu näkymä koontinäyttöön, kun haluat jatkaa seuraamista.  
  Voit päivittää tiedot manuaalisesti ja määrittää päivitysaikataulun. Lisätietoja on kohdassa [Aikataulutetun päivityksen määrittäminen](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/).  

Sisältöpaketit on määritetty etukäteen niin, että niitä voidaan käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]iin rekisteröityessä saatavan esittely-yrityksen tietojen kanssa. Kun asennat sovelluksia Power BI:hin ja yhdistät ne omiin tietoihisi, jotkin raportit eivät ehkä toimi, koska ne perustuvat tietoihin, joita yrityksellä ei ole. Voit siinä tapauksessa poistaa raportin koontinäytöstä.  

> [!NOTE]  
>   Voit myös luoda omia raportteja ja koontinäyttöjä Power BI:ssä [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietojen perusteella. Lisätietoja on kohdassa [Liiketoimintatietojen yhdistäminen Power BI:hin](across-how-use-financials-data-source-powerbi.md).  

## <a name="how-to-connect"></a>Yhdistäminen
1. Valitse **Nouda tiedot** vasemman siirtymisruudun alareunassa.  
![Siirtyminen tietoja noudettaessa](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

Voit ehkä aloittaa käyttämisen Dynamics 365 Business Editionista. Valitse roolikeskuksen Power BI -roolikeskuksessa **Raporttivalinta**. Valitse valintanauhassa joko **Palvelu** tai **Oma organisaatio**. Kun jompikumpi vaihtoehto valitaan, siirry joko Power BI:n organisaatiovalikoimaan tai Power BI:n palvelukirjastoon, joka voidaan myös suodattaa näyttämään vain [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]iin liittyvät sisältöpaketit.

2. Valitse **Palvelut**-ruudussa **Hae**. Avautuvalla sivulla näkyy **AppSource** ja **Power BI -sovellusten sovellukset**.  
![Sisältöpakettien valitseminen verkkopalveluista](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Valitse ensin **Sovellukset** **Power BI -sovellusten sovellukset** -välilehdessä ja sitten käytettävä **Microsoft Dynamics 365 Business Central** -sisältöpaketti. Valitse lopuksi **Hae se nyt**.  
![Valitse ensin Dynamics 365 Business Central ja sitten Hae se nyt](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Anna kysyttäessä *yrityksen nimi* [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]issa. Se ei ole näyttönimi. Yrityksen nimi sijaitsee [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] -instanssin Yritykset-sivulla.  
![Valitse ensin Dynamics 365 Business Central ja sitten Hae se nyt](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Kun yhteys on muodostettu, koontinäyttö, raportti ja tietojoukko ladataan automaattisesti Power BI -työtilaan. Kun tämä on tehty, ruudut päivittävät tiedot [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] -yrityksestä.
![Valitse ensin Dynamics 365 Business Central ja sitten Hae se nyt](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Mitä seuraavaksi?

- Kokeile [kysymyksen kirjoittamista kysymys- ja vastausruutuun](https://docs.microsoft.com/en-us/power-bi/service-q-and-a-tips) koontinäytön yläreunassa.
- [Vaihda ruutuja](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) koontinäytössä.  
- [Avaa taustalla oleva raportti valitsemalla ruutu](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles).  
- Vaikka tietojoukko on ajoitettu päivittymään kerran päivässä, voit muuttaa päivitysaikataulua. Voit myös kokeilla sen päivittämistä tarvittaessa **Päivitä nyt** -vaihtoehdolla.

## <a name="system-requirements"></a>Järjestelmävaatimukset
Jos haluat tuoda [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in tietoja Power BI:hen, sinulla on oltava tietojen noutamiseen käytettävien verkkopalvelujen käyttöoikeudet. Kunkin sisältöpaketin kanssa on käytettävä esimerkiksi seuraavia verkkopalveluja:

## <a name="role-center-reports"></a>Roolikeskuksen raportit

**Microsoft Dynamics 365 Business Central – CRM**
- Myyntimahdollisuudet
- Excel-malli Näytä yritys
- Power BI -raporttien selitteet

**Microsoft Dynamics 365 Business Central – rahoitus**
- PowerBIFinance
- Excel-malli Näytä yritys
- Power BI -raporttien selitteet

**Microsoft Dynamics 365 Business Central – työt**
- Projektiluettelo
- Projektin suunnittelurivit
- Projektitehtävärivit
- Power BI -raporttien selitteet
- Excel-malli Näytä yritys

**Microsoft Dynamics 365 Business Central – myynti**
- Myynnin koontinäyttö
- Excel-malli Näytä yritys
- Power BI -raporttien selitteet

## <a name="list-page-reports"></a>Luettelosivun raportit

**Microsoft Dynamics 365 Business Central – asiakasluettelo**
- Asiakaskohtainen nimikemyynti
- Power BI -nimikkeiden ostoluettelo
- Power BI -nimikkeiden myyntiluettelo
- Myynnin koontinäyttö
- Power BI -asiakasluettelo
- ExcelTemplateViewCompany
- Power BI -raporttien selitteet

**Microsoft Dynamics 365 Business Central – kirjanpitotapahtumien luettelo**
- Power BI -PK-summaluettelo
- Power BI -PK-budjettisumma
- ExcelTemplateViewCompany
- Power BI -raporttien selitteet

**Microsoft Dynamics 365 Business Central – nimikeluettelo**
- Asiakaskohtainen nimikemyynti
- Power BI -nimikkeiden ostoluettelo
- Power BI -nimikkeiden myyntiluettelo
- Myynnin koontinäyttö
- ExcelTemplateViewCompany
- Power BI -raporttien selitteet

**Microsoft Dynamics 365 Business Central – projektiluettelo**
- Power BI -projektiluettelo
- ExcelTemplateViewCompany
- Power BI -raporttien selitteet

**Microsoft Dynamics 365 Business Central – ostolaskuluettelo**
- Power BI -ostoluettelo
- ExcelTemplateViewCompany
- Power BI -raporttien selitteet

**Microsoft Dynamics 365 Business Central – myyntitilausluettelo**
- Power BI -myyntiluettelo
- ExcelTemplateViewCompany
- Power BI -raporttien selitteet


**Microsoft Dynamics 365 Business Central – toimittajaluettelo**
- Power BI -nimikkeiden ostoluettelo
- Power BI -nimikkeiden myyntiluettelo
- Power BI -toimittajaluettelo
- ExcelTemplateViewCompany
- Power BI -raporttien selitteet

## <a name="web-services"></a>WWW-palvelut
Verkkopalveluja voi etsiä kätevästi hakemalla [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in verkkopalveluja. Varmista, että edellä mainittujen verkkopalvelujen Julkaise-ruutu on valittu luettelossa.

## <a name="troubleshooting"></a>Vianetsintä
Power BI:n koontinäyttö käyttää julkaistuja edellä mainittuja verkkopalveluita. Koontinäytössä ovat esittely-yrityksen tiedot tai oman yrityksesi tiedot, jos toit tiedot nykyisestä rahoitusratkaisustasi. Tämä osa sisältää ratkaisun tyypillisempiin ongelmiin.

### <a name="incorrect-company-name"></a>Virheellinen yrityksen nimi  
Yleinen virhe on antaa yrityksen näyttönimi yrityksen nimen sijaan. Voit etsiä yrityksen nimen hakusanalla **Yritykset**. Anna sitten yrityksen nimi **Nimi**-kentässä.

### <a name="incorrect-user-name-and-password"></a>Virheellinen käyttäjänimi ja salasana  
Yhdistämiseen on käytettävä käyttäjänimeä ja salasanaa, joilla muodostetaan yhteys Microsoft Office 365 -tiliin.  

Sisältöpaketit edellyttävät myös, että sinulla Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -tili. Kun olet antanut tunnistetietosi, järjestelmä havaitsee automaattisesti ne Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -vuokraajat, joiden käyttöoikeus sinulla on. Jos sinulla ei ole Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -tilin käyttöoikeutta tai kokeiluversiota, saat virhesanoman.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Avain ei vastannut mitään taulukon riviä
Jos annat yhteydenmuodostusprosessin aikana yrityksen nimen, joka ei ole sallittu, näyttöön voi avautua virhesanoma, jonka mukaan avain ei vastannut mitään taulukon riviä. Anna oikea yrityksen nimi ja yritä muodostaa yhteys uudelleen.

## <a name="see-also"></a>Katso myös
[Power BI:n käytön aloittaminen](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI – peruskäsitteet](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[Business Intelligence](bi.md)  
[Käytön aloittaminen](product-get-started.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen PowerApps-tietolähteenä](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Microsoft Flow'ssa](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
