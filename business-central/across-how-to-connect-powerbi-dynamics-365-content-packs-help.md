---
title: "Power BI- ja Business Central -sovelluksen yhdistäminen | Microsoft Docs"
description: "Analyysitietojen, liiketoimintatietoja ja tunnuslukujen hakeminen Business Central -tiedoista on helppoa Power BI- ja Business Central -sisältöpakettien avulla."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/03/2018
ms.author: solsen
redirect_url: admin-powerbi
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 0196bff5dedb878884fd3d6e0208022faa968dfd
ms.contentlocale: fi-fi
ms.lasthandoff: 05/17/2018

---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a>Power BI- ja Dynamics 365 Business Central -sisältöpakettien yhdistäminen
Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in tietojen analysointi on helppoa Power BI- ja Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -sisältöpakettien avulla. Power BI hakee tiedot ja muodostaa niiden perusteella valmiin koontinäytön ja raportit.

Sinulla on oltava kelvollinen Dynamics 365- ja Power BI -tili. Sinun on ladattava myös [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/), jos haluat luoda omia Power BI -raportteja. Power BI -sisältöpakettien käyttöä varten tarvitaan niiden taulukoiden käyttöoikeus, joista tiedot noudetaan. Lisätietoja on vaatimuksista on jäljempänä.  

## <a name="how-to-connect"></a>Yhdistäminen
1. Valitse **Nouda tiedot** vasemman siirtymisruudun alareunassa.  
![Siirtyminen tietoja noudettaessa](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

Aloittaminen voi olla mahdollista myös Dynamics 365 Business Editionista. Valitse roolikeskuksen Power BI -roolikeskuksessa **Raporttivalinta**. Valitse valintanauhassa joko **Palvelu** tai **Oma organisaatio**. Kun jompikumpi vaihtoehto valitaan, siirry joko Power BI:n organisaatiovalikoimaan tai Power BI:n palvelukirjastoon, joka voidaan myös suodattaa näyttämään vain [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]iin liittyvät sisältöpaketit.

2. Valitse **Palvelut**-ruudussa **Hae**. Avautuvassa ikkunassa näkyy **AppSource** **Power BI -sovellusten sovellukset**.  
![Sisältöpakettien valitseminen verkkopalveluista](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Valitse ensin **Sovellukset** **Power BI -sovellusten sovellukset** -välilehdessä ja sitten käytettävä **Microsoft Dynamics 365 Business Central** -sisältöpaketti. Valitse lopuksi **Hae se nyt**.  
![Dynamics 365 Business Central -sovelluksen ja Hae se nyt -vaihtoehdon valitseminen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Anna kysyttäessä *yrityksen nimi* [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]issa. Se ei ole näyttönimi. Yrityksen nimi sijaitsee [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] -instanssin Yritykset-sivulla. 
![Dynamics 365 Business Central -sovelluksen ja Hae se nyt -vaihtoehdon valitseminen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Kun yhteys on muodostettu, koontinäyttö, raportti ja tietojoukko ladataan automaattisesti Power BI -työtilaan. Kun tämä on tehty, ruudut päivittävät tiedot [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] -yrityksestä.
![Dynamics 365 Business Central -sovelluksen ja Hae se nyt -vaihtoehdon valitseminen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Mitä seuraavaksi?

- Kokeile [kysymyksen kirjoittamista kysymys- ja vastausruutuun](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) koontinäytön yläreunassa.
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

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- Excel-malli Näytä yritys
- Power BI -raporttien selitteet

**Microsoft Dynamics 365 Business Central – Jobs**
- Projektiluettelo
- Projektin suunnittelurivit
- Projektitehtävärivit
- Power BI -raporttien selitteet
- Excel-malli Näytä yritys

**Microsoft Dynamics 365 Business Central - Sales**
- Myynnin koontinäyttö
- Excel-malli Näytä yritys
- Power BI -raporttien selitteet

## <a name="list-page-reports"></a>Luettelosivun raportit 

**Microsoft Dynamics 365 Business Central – Customers List**
- Asiakaskohtainen nimikemyynti
- Power BI -nimikeostoluettelo
- Power BI -nimikemyyntiluettelo
- Myynnin koontinäyttö
- Power BI -asiakasluettelo
- ExcelTemplateViewCompany
- Power BI -raporttien selitteet 

**Microsoft Dynamics 365 Business Central - General Ledger Entries List**
- Power BI -PK-summaluettelo
- Power BI -PK-budjettisumma
- ExcelTemplateViewCompany
- Power BI -raporttien selitteet

**Microsoft Dynamics 365 Business Central – Items List**
- Asiakaskohtainen nimikemyynti
- Power BI -nimikeostoluettelo
- Power BI -nimikemyyntiluettelo
- Myynnin koontinäyttö
- ExcelTemplateViewCompany
- Power BI -raporttien selitteet

**Microsoft Dynamics 365 Business Central – Jobs List**
- Power BI -projektiluettelo
- ExcelTemplateViewCompany
- Power BI -raporttien selitteet

**Microsoft Dynamics 365 Business Central – Purchase Invoices List**
- Power BI -ostoluettelo
- ExcelTemplateViewCompany
- Power BI -raporttien selitteet

**Microsoft Dynamics 365 Business Central – Sales Orders List**
- Power BI -myyntiluettelo
- ExcelTemplateViewCompany
- Power BI -raporttien selitteet


**Microsoft Dynamics 365 Business Central – Vendors List**
- Power BI -nimikeostoluettelo
- Power BI -nimikemyyntiluettelo
- Power BI -toimittajaluettelo
- ExcelTemplateViewCompany
- Power BI -raporttien selitteet

## <a name="web-services"></a>WWW-palvelut
Verkkopalveluja voi etsiä kätevästi hakemalla [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in verkkopalveluja. Varmista, että edellä mainittujen verkkopalvelujen Julkaise-ruutu on valittu luettelossa.

## <a name="troubleshooting"></a>Vianetsintä
Power BI:n koontinäyttö käyttää julkaistuja yllä mainittuja WWW-palveluita. Koontinäytössä ovat esittely-yrityksen tiedot tai oman yrityksesi tiedot, jos toit tiedot nykyisestä rahoitusratkaisustasi. Tämä osa sisältää ratkaisun tyypillisempiin ongelmiin.

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
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in raportoinnin määrittäminen Power BI:ssä](across-how-use-financials-data-source-powerbi.md)  

