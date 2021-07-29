---
title: Kassavirta-analyysin määrittäminen
description: Kaavioiden käyttäminen kirjanpitäjän roolikeskuksessa auttaa analysoimaan yrityksen rahavirtaa, kuten menoja ja tuloja, maksuvalmiutta ja kassaanmaksuista vähennettyjä kassamaksuja.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds
ms.date: 06/16/2021
ms.author: bholtorf
ms.openlocfilehash: 919c5cc5781f0f93fbfb79b9e306e42180eb6968
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6446288"
---
# <a name="setting-up-cash-flow-analysis"></a>Kassavirta-analyysin määrittäminen
Jos tarvitset apua käteisvarojen käytöstä päättämiseen, tutustu Kirjanpitäjä-roolikeskuksen kaavioihin:  

* **Käyttöpääomasykli**  
* **Tulot ja kulut**  
* **Kassavirta**  
* **Kassavirtaennusteet**  

Tässä ohjeaiheessa kerrotaan, mistä kaavioiden tiedot saadaan ja (tarvittaessa) miten kaavioiden käyttö aloitetaan.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc?rel=0]

## <a name="the-cash-cycle-and-income--expense-charts"></a>Käyttöpääomasykli- ja Tulot ja kulut -kaaviot
Tilikarttaan ja KP-raporttimalleihin perustuvat **Käyttöpääomasykli**- ja **Tulot ja kulut** -kaaviot ovat käyttövalmiita. Tilit, joista tiedot haetaan, ja KP-raporttimalli laskevat myynnin ja saamisten välisen suhteen. Valmiina on joitakin tilejä ja KP-raporttimalleja. Voit käyttää niitä sellaisenaan, muuttaa niitä ja lisää uusia. Jos lisäät KP-tilejä tilikarttaan esimerkiksi tuomalla ne QuickBooksista, sinun yhdistettävä ne tileihin seuraavan nimisten KP-raporttimallien **KP-raporttimallit**-sivulla:  

| KP-raporttimallin nimi | Käyttökohde |
| --- | --- |
| **I_CACYCLE** |Käyttöpääomasykli |
| **I_CASHFLOW** |Kassavirta |
| **I_INCEXP** |Tulot ja kulut |
| **I_MINTRIAL** |Tuloslaskelmana, jos tilikartta ei ole käytössä |

**Huomautus** KP-raporttimallille annetut laskelmat kannattaa säilyttää.  

Anna **Yhteensä**-kentässä tilit seuraaville: **Kokonaistuotto**, **Myyntisaamiset yhteensä**, **Ostovelat yhteensä** ja **Varasto yhteensä**. Jos yhdistäminen tapahtuu tilialueelle tai useammalle kuin yhdelle tietylle tilille, erota ensimmäisessä tapauksessa tilinumerot toistaan kahdella pisteellä (..) ja jälkimmäisessä pystyviivalla. Esimerkki: **1111..4444** tai **2222|3333|5555**.  

**Vihje** Tarkista yhdistämismääritys valitsemalla **Yleiskuvaus**-toiminto.  

## <a name="set-up-the-cash-flow-chart"></a>Kassavirta-kaavion määrittäminen
Kassavirta-kaavio perustuu seuraaviin:  

* Kassavirtatilien kaavio.
* Vähintään yksiin kassavirta-asetuksiin. Ne määrittävät kirjanpitoon, ostoihin, myynteihin, palveluihin ja käyttöomaisuuteen käytettävät tilit.  

Käytön aloittamisen helpottamiseksi osa tilistä ja kassavirran asetuksista on määritetty valmiiksi. Voit lisätä, muuttaa tai poistaa niitä.  

Voit määrittää ne käyttämällä hakutermiä **kassavirtatilit**, valitsemalla linkin ja täyttämällä kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Toista nämä vaiheet hakutermille **kassavirran asetukset**.  

## <a name="set-up-cash-flow-forecasts"></a>Kassavirtaennusteiden määrittäminen
**Kassavirtaennuste**-kaavio käyttää kassavirtatilejä, kassavirran asetuksia ja kassavirtaennusteita. Osa niistä on määritetty valmiiksi, mutta voit tehdä omat määrityksesi avustetun asennusoppaan avulla. Oppaan avulla voit määrittää esimerkiksi ennusteen päivitystiheyden, ennusteen perustana olevat tilit, verojen maksua koskevat tiedot ja sen, otetaanko [Azure AI](https://azure.microsoft.com/overview/ai-platform/) käyttöön.  

Kassavirtaennusteet voivat käyttää Azure AI:ta tulevien asiakirjojen ennustamisessa. Tällä tavoin saadaan entistä kattavampi ennuste. Azure AI -yhteys on muodostettu puolestasi. Sinun tarvitsee vain ottaa se käyttöön. Kun kirjaudut [!INCLUDE[prod_short](includes/prod_short.md)]iin, ilmoitus näkyy sinisessä palkissa, ja siinä on linkki kassavirran oletusasetuksiin. Ilmoitus näytetään vain kerran. Jos suljet sen mutta päätät ottaa Azure AI:n käyttöön, voit tehdä sen asetusten ohjatun määrityksen avulla tai manuaalisesti.  

> [!NOTE]  
>   Voit käyttää myös omaa ennakoivaa verkkopalvelua. Lisätietoja on kohdassa [Kassavirtaennusteiden ennakoivan verkkopalvelun luonti ja käyttö](#AnchorText).  

Voit käyttää avustettua asennusopasta seuraavissa toiminnoissa:  

1. Valitse Kirjanpitäjä-roolikeskuksen **Kassavirtaennuste**-kaaviossa **Avaa avustettu määritys** -toiminto.  
2. Täytä kentät oppaan kussakin vaiheessa.  
3. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kassavirtaennuste** ja valitse sitten vastaava linkki.
4. Valitse **Kassavirtaennuste**-sivulla **Laske ennuste uudelleen** -toiminto.  

Voit käyttää manuaalista prosessia seuraavasti:  

1. Etsi Kirjanpitäjä-roolikeskuksessa **Kassavirran asetukset** ja valitse sitten vastaava linkki.  
2. Laajenna **Azure AI** -pikavälilehti ja valitse sitten **Azure AI käytössä** -valintaruutu.  
3. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kassavirtaennuste** ja valitse sitten vastaava linkki.
4. Valitse **Kassavirtaennuste**-sivulla **Laske ennuste uudelleen** -toiminto.  

> [!TIP]  
>   Mieti, miten pitkiä jaksoja palvelun laskelmissa käytetään. Mitä enemmän tietoja on käytettävissä, sitä tarkempia ennusteet ovat. Varo myös suuria jaksovaihteluita. Ne vaikuttavat myös ennusteisiin. Jos Azure AI ei löydä riittävästi tietoja tai tiedot ovat kovin erilaisia, palvelu ei voi tehdä ennustetta.  

## <a name="design-details"></a>Rakennetiedot
[!INCLUDE[prod_short](includes/prod_short.md)]:n tilaukset sisältävät käyttöoikeuden useisiin ennakoitaviin verkkopalveluihin kaikilla alueilla, joilla [!INCLUDE[prod_short](includes/prod_short.md)] on saatavissa. Lisätietoja on Microsoft Dynamics 365 Business Centralin käyttöoikeusoppaassa. Opas on ladattavissa [Business Centralin](https://dynamics.microsoft.com/en-us/business-central/overview/) verkkosivulla. 

Näillä verkkopalveluilla ei ole tilaa. Ne siis käyttävät tietoja vain ennusteiden laskemiseen tarvittaessa. Ne eivät tallenna tietoja.

> [!NOTE]  
>   Voit käyttää omaa ennakoivaa verkkopalvelua meidän palvelumme sijaan. Lisätietoja on kohdassa [Kassavirtaennusteiden ennakoivan verkkopalvelun luonti ja käyttö](#AnchorText). 

### <a name="data-required-for-forecast"></a>Ennusteeseen vaadittavat tiedot
Jos haluat ennustaa tulevia tuottoja ja kuluja, verkkopalvelut edellyttävät aiempia tietoja myyntisaamisista, ostoveloista ja verotiedoista.

#### <a name="receivables"></a>Myyntisaamiset:
**Eräpäivä**- ja **Summa (LCY)** -kentät **Asiakastapahtumat**-sivulla, jossa:
- Asiakirjan tyyppi on Lasku tai Hyvityslasku.
- Eräpäivä on **Kassavirran asetukset** -sivun **Aiemmat kaudet**- ja **Kauden tyyppi** -kenttien arvojen perusteella lasketun päivämäärän ja käsittelypäivämäärän välillä.

Ennen ennakoivan verkkopalvelun käyttämistä [!INCLUDE[prod_short](includes/prod_short.md)] tiivistää tapahtumat **eräpäivän** mukaan **Kauden tyyppi** -kentän arvon perusteella **Kassavirran asetukset** -sivulla.

#### <a name="payables"></a>Ostovelat:
**Eräpäivä**- ja **Summa (LCY)** -kentät **Toimittajatapahtumat**-sivulla, jossa:
- Asiakirjan tyyppi on Lasku tai Hyvityslasku.
- Eräpäivä on **Kassavirran asetukset** -sivun **Aiemmat kaudet**- ja **Kauden tyyppi** -kenttien arvojen perusteella lasketun päivämäärän ja käsittelypäivämäärän välillä.

Ennen ennakoivan verkkopalvelun käyttämistä [!INCLUDE[prod_short](includes/prod_short.md)] tiivistää tapahtumat **eräpäivän** mukaan **Kauden tyyppi** -kentän arvon perusteella **Kassavirran asetukset** -sivulla.

#### <a name="tax"></a>Vero:
**Asiakirjan päivämäärä**- ja **Summa (VAT)** -kentät **ALV (vero) -tapahtumat** -sivulla, jossa:
- Asiakirjan tyyppi on Myynti.
- Asiakirjan päivämäärä on **Kassavirran asetukset** -sivun **Aiemmat kaudet**- ja **Kauden tyyppi** -kenttien arvojen perusteella lasketun päivämäärän ja käsittelypäivämäärän välillä.

Ennen ennakoivan verkkopalvelun käyttämistä [!INCLUDE[prod_short](includes/prod_short.md)] tiivistää tapahtumat **asiakirjan päivämäärän** mukaan **Kauden tyyppi** -kentän arvon perusteella **Kassavirran asetukset** -sivulla.

## <a name="create-and-use-your-own-predictive-web-service-for-cash-flow-forecasts"></a><a name="AnchorText"> </a>Kassavirtaennusteiden ennakoivan verkkopalvelun luonti ja käyttö
Voit myös luoda oman ennakoivan verkkopalvelun **Microsoft Business Central -sovelluksen ennustemalli** -nimisen julkisen mallin perusteella. Tämä ennakoiva malli on saatavana verkossa Azure AI Galleryssa. Voit käyttää mallia seuraavien vaiheiden avulla:  

1. Avaa selain ja siirry [Azure AI Galleryyn](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Etsi **Ennustusmalli Microsoft Business Centralille** ja avaa malli Azuren koneoppimisstudiossa.  
3. Kirjaudu työtilaan Microsoft-tilin avulla ja kopioi malli.  
4. Aja malli ja julkaise se verkkopalveluna.  
5. Kirjoita API:n URL-osoite ja API-avain muistiin. Näitä tunnistetietoja käytetään kassavirran asetuksissa.  
6. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kassavirran asetukset** ja valitse sitten vastaava linkki.  
7. Laajenna **Azure AI** -pikavälilehti ja täytä sitten kentät.  

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös
[Yrityksen kassavirran analysoiminen](finance-analyze-cash-flow.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]