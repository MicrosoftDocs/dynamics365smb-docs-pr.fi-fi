---
title: "Kassavirta-analyysin määrittäminen| Microsoft Docs"
description: "Kaavioiden määrittäminen kirjanpitäjän roolikeskuksessa auttaa analysoimaan yrityksen rahavirtaa, kuten menoja ja tuloja, maksuvalmiutta ja kassaanmaksuista vähennettyjä kassamaksuja."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9424a8ba632cf43628ad37dce963e3f1641e593d
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-cash-flow-analysis"></a>Kassavirta-analyysin määrittäminen
Jos tarvitset apua käteisvarojen käytöstä päättämiseen, tutustu Kirjanpitäjä-roolikeskuksen kaavioihin:  

* **Käyttöpääomasykli**  
* **Tulot ja kulut**  
* **Kassavirta**  
* **Kassavirtaennusteet**  

Tässä ohjeaiheessa kerrotaan, mistä kaavioiden tiedot saadaan ja (tarvittaessa) miten kaavioiden käyttö aloitetaan.  

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
**Kassavirtaennuste**-kaavio käyttää kassavirtatilejä, kassavirran asetuksia ja kassavirtaennusteita. Osa niistä on määritetty valmiiksi, mutta voit tehdä omat määrityksesi avustetun asennusoppaan avulla. Oppaan avulla voit määrittää esimerkiksi ennusteen päivitystiheyden, ennusteen perustana olevat tilit, verojen maksua koskevat tiedot ja sen, otetaanko [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) käyttöön.  

Kassavirtaennusteet voivat sisällyttää Cortana Intelligencen avulla asiakirjoja, joiden eräpäivä on tulevaisuudessa. Tällä tavoin saadaan entistä kattavampi ennuste. Cortana Intelligence -yhteys on muodostettu valmiiksi. Sinun tarvitsee vain ottaa se käyttöön. Kun kirjaudut [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, ilmoitus näkyy sinisessä palkissa, ja siinä on linkki kassavirran oletusasetuksiin. Ilmoitus näytetään vain kerran. Jos suljet sen mutta päätät ottaa Cortana Intelligencen käyttöön, voit tehdä sen avustetun asennusoppaan avulla tai manuaalisesti.  

> [!NOTE]  
>   Voit käyttää myös omaa ennakoivaa verkkopalvelua. Lisätietoja on kohdassa [Kassavirtaennusteiden ennakoivan verkkopalvelun luonti ja käyttö](#AnchorText).  

Voit käyttää avustettua asennusopasta seuraavissa toiminnoissa:  

1. Valitse Kirjanpitäjä-roolikeskuksen **Kassavirtaennuste**-kaaviossa **Avaa avustettu määritys** -toiminto.  
2. Täytä kentät oppaan kussakin vaiheessa.  
3. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Kassavirtaennuste** ja valitse sitten aiheeseen liittyvä linkki.
4. Valitse **Kassavirtaennuste**-ikkunassa **Laske ennuste uudelleen** -toiminto.  

Voit käyttää manuaalista prosessia seuraavasti:  

1. Etsi Kirjanpitäjä-roolikeskuksessa **Kassavirran asetukset** ja valitse sitten vastaava linkki.  
2. Laajenna **Cortana Intelligence**-pikavälilehti ja valitse sitten **Cortana Intelligence käytössä** -valintaruutu.  
3. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Kassavirtaennuste** ja valitse sitten aiheeseen liittyvä linkki.
4. Valitse **Kassavirtaennuste**-ikkunassa **Laske ennuste uudelleen** -toiminto.  

> [!TIP]  
>   Mieti, miten pitkiä jaksoja palvelun laskelmissa käytetään. Mitä enemmän tietoja on käytettävissä, sitä tarkempia ennusteet ovat. Varo myös suuria jaksovaihteluita. Ne vaikuttavat myös ennusteisiin. Jos Cortana Intelligence ei löydä riittävästi tietoja tai tiedot ovat kovin erilaisia, palvelu ei voi tehdä ennustetta.  

## <a name="AnchorText"> </a>Kassavirtaennusteiden ennakoivan verkkopalvelun luonti ja käyttö
Voit myös luoda oman ennakoivan verkkopalvelun **Microsoft Business Central -sovelluksen ennustemalli** -nimisen julkisen mallin perusteella. Tämä ennakoiva malli on saatavana verkossa Cortana Intelligence Galleryssa. Voit käyttää mallia seuraavien vaiheiden avulla:  

1. Avaa selain ja siirry [Cortana Intelligence Galleryyn](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Hae **Microsoft Business Central -sovelluksen ennustemalli** ja avaa sitten malli Azure Machine Learning Studiossa.  
3. Kirjaudu työtilaan Microsoft-tilin avulla ja kopioi malli.  
4. Aja malli ja julkaise se verkkopalveluna.  
5. Kirjoita API:n URL-osoite ja API-avain muistiin. Näitä tunnistetietoja käytetään kassavirran asetuksissa.  
6. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Kassavirran asetukset** ja valitse sitten aiheeseen liittyvä linkki.  
7. Laajenna **Cortana Intelligence** -pikavälilehti ja täytä sitten kentät.  

## <a name="see-also"></a>Katso myös
[Yrityksen kassavirran analysoiminen](finance-analyze-cash-flow.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

