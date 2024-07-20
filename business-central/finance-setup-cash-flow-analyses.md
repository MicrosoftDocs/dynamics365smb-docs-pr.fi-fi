---
title: Kassavirta-analyysin määrittäminen
description: 'Kaavioiden käyttäminen kirjanpitäjän roolikeskuksessa auttaa analysoimaan yrityksen rahavirtaa, kuten menoja ja tuloja, maksuvalmiutta ja kassaanmaksuista vähennettyjä kassamaksuja.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds'
ms.search.form: '846, 847, 849, 851, 855, 862, 869, 1818'
ms.date: 07/01/2024
ms.service: dynamics-365-business-central
---
# Kassavirta-analyysin määrittäminen

Jos tarvitset apua käteisvarojen käytöstä päättämiseen, tutustu Kirjanpitäjä-roolikeskuksen kaavioihin:

* **Käyttöpääomasykli**  
* **Tulot ja kulut**  
* **Kassavirta**  
* **Kassavirtaennusteet**  

Tässä artikkelissa kerrotaan, mistä kaavioiden tiedot saadaan ja (tarvittaessa) miten kaavioiden käyttö aloitetaan.
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc?rel=0]

## Käyttöpääomasykli- ja Tulot ja kulut -kaaviot

Tilikarttaan ja talousraportteihin perustuvat **Käyttöpääomasykli**- ja **Tulot ja kulut** -kaaviot ovat käyttövalmiita. Tilit, joista tiedot haetaan, ja talousraportit laskevat myynnin ja saamisten välisen suhteen. Valmiina on joitakin tilejä ja talousraportteja. Voit käyttää niitä sellaisenaan, muuttaa niitä ja lisää uusia. Jos lisäät KP-tilejä tilikarttaan esimerkiksi tuomalla ne QuickBooksista, yhdistä ne tileihin seuraavien raporttien **Talousraportit**-sivulla:

| Talousraportin nimi | Käyttökohde |
| --- | --- |
| **I_CACYCLE** |Käyttöpääomasykli |
| **I_CASHFLOW** |Kassavirta |
| **I_INCEXP** |Tulot ja kulut |
| **I_MINTRIAL** |Tuloslaskelmana, jos tilikartta ei ole käytössä |

> [!NOTE]
> Talousraportille annetut laskelmat kannattaa säilyttää.

Anna **Yhteensä**-kentässä tilit seuraaville: **Kokonaistuotto**, **Myyntisaamiset yhteensä**, **Ostovelat yhteensä** ja **Varasto yhteensä**. Linkitä tilialue syöttämällä tilinumerot kahdella pisteellä (..) erotettuina seuraavasti: **1111..4444**. Vaihtoehtoisesti voit linkittää tiettyihin tileihin syöttämällä tilinumerot pystyviivalla eroteltuina seuraavasti: **2222|3333|5555**.  

> [!TIP] 
> Tarkista yhdistämismääritys valitsemalla **Yleiskuvaus**-toiminto.  

## Kassavirta-kaavion määrittäminen

Kassavirta-kaavio perustuu seuraaviin tietoihin:  

* Kassavirtatilien kaavio.
* Vähintään yksiin kassavirta-asetuksiin. Nämä asetukset määrittävät kirjanpitoon, ostoihin, myynteihin, palveluihin ja käyttöomaisuuteen käytettävät tilit.  

Käytön aloittamisen helpottamiseksi osa tilistä ja kassavirran asetuksista on määritetty valmiiksi sovelluksessa [!INCLUDE [prod_short](includes/prod_short.md)]. Voit lisätä, muuttaa tai poistaa niitä.  

Voit määrittää tilit käyttämällä hakutermiä **Kassavirtatilien kaavio**, valitsemalla linkin ja täyttämällä kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Toista nämä vaiheet hakutermille **Kassavirran asetukset**.

## Kassavirtaennusteiden määrittäminen

**Kassavirtaennuste**-kaavio käyttää kassavirtatilejä, kassavirran asetuksia ja kassavirtaennusteita. Osa niistä on määritetty valmiiksi, mutta voit tehdä omat määrityksesi avustetun asennusoppaan avulla. Oppaan avulla voit määrittää seuraavanlaisia asioita:

* Milloin ennuste päivitetään
* Mille tileille se perustuu
* Milloin maksat veroa
* Otetaanko [Azure AI](https://azure.microsoft.com/overview/ai-platform/) käyttöön.  

Kassavirtaennusteet voivat käyttää Azure AI:ta aiempaa kattavamman ennusteen luomisessa. Azure AI -yhteys on muodostettu puolestasi. Sinun tarvitsee vain ottaa se käyttöön. Kun kirjaudut [!INCLUDE[prod_short](includes/prod_short.md)]iin, ilmoitus näkyy sinisessä palkissa, ja siinä on linkki kassavirran oletusasetuksiin. Ilmoitus näytetään vain kerran. Jos suljet sen, mutta päätät ottaa Azure AI:n käyttöön, voit tehdä sen asetusten ohjatun määrityksen avulla tai manuaalisesti.  

> [!NOTE]
>
> Voit käyttää myös omaa ennakoivaa verkkopalvelua. Lisätietoja on kohdassa [Kassavirtaennusteiden ennakoivan verkkopalvelun luonti ja käyttö](#AnchorText).  

Voit käyttää avustettua asennusopasta seuraavissa toiminnoissa:  

1. Valitse Kirjanpitäjä-roolikeskuksen **Kassavirtaennuste**-kaaviossa **Avaa avustettu määritys** -toiminto.
2. Täytä kentät oppaan kussakin vaiheessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse kirjanpitäjän roolikeskuksessa **Laske ennuste uudelleen** -toiminto **Kassavirtaennuste** -kaaviossa.

Voit käyttää manuaalista prosessia seuraavasti:  

1. Valitse kirjanpitäjän roolikeskuksessa ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kassavirran asetukset** ja valitse sitten vastaava linkki.
2. Laajenna **Azure AI** -pikavälilehti ja valitse sitten **Azure AI käytössä** -kenttä.
3. Valitse kirjanpitäjän roolikeskuksessa **Laske ennuste uudelleen** -toiminto **Kassavirtaennuste** -kaaviossa.

> [!TIP]  
> Mieti, miten pitkiä jaksoja palvelun laskelmissa käytetään. Mitä enemmän tietoja on käytettävissä, sitä tarkempia ennusteet ovat. Varo myös suuria jaksovaihteluita. Ne vaikuttavat myös ennusteisiin. Jos Azure AI ei löydä riittävästi tietoja tai tiedot ovat kovin erilaisia, palvelu ei voi tehdä ennustetta.  

## Rakennetiedot

[!INCLUDE[prod_short](includes/prod_short.md)]:n tilaukset sisältävät käyttöoikeuden useisiin ennakoitaviin verkkopalveluihin kaikilla alueilla, joilla [!INCLUDE[prod_short](includes/prod_short.md)] on saatavissa. Lisätietoja on Microsoft Dynamics 365 Business Centralin käyttöoikeusoppaassa. Opas on ladattavissa [Business Centralin](https://dynamics.microsoft.com/business-central/overview/) verkkosivulla.

Näillä verkkopalveluilla ei ole tilaa. Ne siis käyttävät tietoja vain ennusteiden laskemiseen tarvittaessa. Ne eivät tallenna tietoja.

> [!NOTE]
>
> Voit käyttää omaa ennakoivaa verkkopalvelua meidän palvelumme sijaan. Lisätietoja on kohdassa [Kassavirtaennusteiden ennakoivan verkkopalvelun luonti ja käyttö](#AnchorText).

### Ennusteeseen vaadittavat tiedot

Jos haluat ennustaa tulevia tuottoja ja kuluja, verkkopalvelut edellyttävät aiempia tietoja myyntisaamisista, ostoveloista ja verotiedoista.

#### Myyntisaamiset

**Eräpäivä**- ja **Summa (LCY)** -kentät **Asiakastapahtumat**-sivulla, jossa:

* Asiakirjan tyyppi on *Lasku* tai *Hyvityslasku*.
* Eräpäivä on **Kassavirran asetukset** -sivun **Aiemmat kaudet**- ja **Kauden tyyppi** -kenttien arvojen perusteella lasketun päivämäärän ja käsittelypäivämäärän välillä.

Ennen ennakoivan verkkopalvelun käyttämistä [!INCLUDE[prod_short](includes/prod_short.md)] tiivistää tapahtumat **eräpäivän** mukaan **Kauden tyyppi** -kentän arvon perusteella **Kassavirran asetukset** -sivulla.

#### Ostovelat

**Eräpäivä**- ja **Summa (LCY)** -kentät **Toimittajatapahtumat**-sivulla, jossa:

* Asiakirjan tyyppi on *Lasku* tai *Hyvityslasku*.
* Eräpäivä on **Kassavirran asetukset** -sivun **Aiemmat kaudet**- ja **Kauden tyyppi** -kenttien arvojen perusteella lasketun päivämäärän ja käsittelypäivämäärän välillä.

Ennen ennakoivan verkkopalvelun käyttämistä [!INCLUDE[prod_short](includes/prod_short.md)] tiivistää tapahtumat **eräpäivän** mukaan **Kauden tyyppi** -kentän arvon perusteella **Kassavirran asetukset** -sivulla.

#### Vero

**Asiakirjan päivämäärä**- ja **Summa (VAT)** -kentät **ALV (vero) -tapahtumat** -sivulla, jossa:

* Asiakirjan tyyppi on *Myynti*.
* Asiakirjan päivämäärä on **Kassavirran asetukset** -sivun **Aiemmat kaudet**- ja **Kauden tyyppi** -kenttien arvojen perusteella lasketun päivämäärän ja käsittelypäivämäärän välillä.

Ennen ennakoivan verkkopalvelun käyttämistä [!INCLUDE[prod_short](includes/prod_short.md)] tiivistää tapahtumat **asiakirjan päivämäärän** mukaan **Kauden tyyppi** -kentän arvon perusteella **Kassavirran asetukset** -sivulla.

## <a name="AnchorText"></a>Kassavirtaennusteiden ennakoivan verkkopalvelun luominen ja käyttäminen

Jotta [!INCLUDE[prod_short](includes/prod_short.md)] toimii verkossa Microsoft julkaisee mallin ja yhdistää sen Microsoft-tilaukseen. Toisia käyttöönottovaihtoehtoja varten on luotava koneoppimisen resursseja omassa Azure-tilauksessaan. Esimerkkivaiheita: [esimerkkiraportti](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). Tämän tehtävän tarkoituksena on noutaa ohjelmointirajapinnan URI ja ohjelmointirajapinnan avain.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kassavirran asetukset** ja valitse sitten vastaava linkki.  
2. Laajenna **Azure AI** -pikavälilehti ja täytä kentät, myös ohjelmointirajapinnan URL-osoite ja avain Azure Machine Learning Studiosta. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse kirjanpitäjän roolikeskuksessa **Laske ennuste uudelleen** -toiminto **Kassavirtaennuste** -kaaviossa.

## Katso myös

[Yrityksen kassavirran analysoiminen](finance-analyze-cash-flow.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ennusteiden ohjelmointirajapinnan yleiskatsaus](/dynamics365/business-central/dev-itpro/developer/ml-forecasting-api-overview)

[!INCLUDE[footer-include](includes/footer-banner.md)]
