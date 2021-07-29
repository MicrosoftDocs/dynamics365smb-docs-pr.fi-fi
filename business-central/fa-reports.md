---
title: Käyttöomaisuuden raportit ja analytiikka
description: Katso, mitkä raportit ja mikä analytiikka on saatavilla Business Centralin vakioversiossa, jotta voit seurata käyttöomaisuuttasi.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: c28e62a2de51323e0a7dcd2f4b5ea26d5896d718
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543334"
---
# <a name="fixed-assets-reports-and-analytics-in-business-central"></a>Käyttöomaisuuden raportit ja analytiikka Business Centralissa

Jotta voit hallita käyttöomaisuuttasi helpommin [!INCLUDE [prod_short](includes/prod_short.md)]issa, vakioraportit ja analytiikka ovat sisään rakennettuina. Se ylittää perinteisen raportoinnin rajoitukset, jotta voit suunnitella tehokkaasti erityyppisiä raportteja.  

## <a name="reports"></a>Raportit

Seuraavassa taulukossa kuvataan joitakin käyttöomaisuusraportoinnin keskeisiä raportteja.

| Raportti | Objektin tunnus | Kuvaus |
|--|--|--|
| **Käyttöomaisuusluettelo** | 5601 | Näyttää käyttöomaisuuserien luettelon ja niiden asetustiedot määritettyä poistokirjaa varten. |
| **KO - hankintaluettelo** | 5608 | Luettelee kaikki omaisuuserät, jotka on hankittu annetulla päivämäärävälillä. Voit sisällyttää myös käyttöomaisuuserän, joka on luotu, mutta jota ei ole vielä hankittu. |
| **Käyttöomaisuuden erittely** | 5604 | Näyttää käyttöomaisuuden kirjanpitotapahtumat. |
| **Käyttöomaisuuden analyysi** | 5600 | Analyysiraportti, jossa voit määrittää kaksi päivämääräsarakkeita ja kolme tietosaraketta näytettäviksi raportissa. Jos esimerkiksi haluat luoda raportin, jota käytetään täsmäytykseen pääkirjanpidon kanssa, lisää sarakkeet seuraavia varten: hankintameno lopetuspäivämäärällä, poisto lopetuspäivämäärällä ja kirjanpitoarvo lopetuspäivämäärällä. Sekkiraportissa voi olla hankinnat/nettomuutos, kirjanpitoarvon alaskirjaus/nettomuutos ja arvonkorotus/nettomuutos, jotta jokainen käyttöomaisuuden muutos voidaan tarvittaessa tarkistaa. Jos valitset **Budjettiraportti**-kentän ja määrität loppupäivämäärän tulevaisuuteen, raportti laskee tulevan poiston ja voi antaa arvioita tulevista poistoista ja kirjanpitoarvoista, jos valitsit kyseiset kentät raporttisarakkeiksi. |
| **Käyttöomaisuuden suunniteltu arvo** | 5607 | Näyttää omaisuuserien suunnitellut poistojen arvot ja kirjanpitoarvot tulevaisuudessa olevalle ajanjaksolle. Raportista on hyötyä, kun käytät omaisuuserillesi erilaisia poistomenetelmiä ja haluat arvioida esimerkiksi ensi vuoden poistoja. Raportin avulla voit luoda poiston budjettisummat valitsemalla budjetin ja **Kopioi KP-budjettiin** -kentän. |
| **KO - Kirjanpitoarvo 01** | 5605 | Tässä raportissa näkyy yksityiskohtaisia tietoja hankintamenosta, poiston arvosta ja kirjanpitoarvosta sekä yksittäisten omaisuuserien että omaisuuserien ryhmien osalta. Kunkin kolmen summatyypin osalta summat lasketaan määritellyn jakson alussa, lopussa sekä itse ajanjaksolta. Jos valitset **Budjettiraportti**-kentän, raportti laskee kauden odotetun poiston. Syötä *ryhmätyyppi*, jos haluat raportin ryhmittelevän käyttöomaisuuserät ja tulostavan ryhmän yhteissummat. Jos KO-luokkia on määritetty esimerkiksi kuusi, valitse *KO-luokka*-vaihtoehto, jotta kunkin kuuden luokkakoodin osalta tulostetaan ryhmän yhteissummat.|
| **KO - Kirjanpitoarvo 02** | 5606 |Näyttää käyttöomaisuuden kirjanpitoarvon erittelyn hankinta-, poisto- ja arvonkorotusmuutoksien mukaan kyseiseltä kaudelta sekä lisäerittelyn lisäysten ja luovutusten mukaan kyseiseltä kaudelta. Tämän raportin avulla voit kuvata käyttöomaisuuden muutoksia tietyltä kaudelta, jonka aikana käyttöomaisuuden ryhmittelyssä tapahtuu paljon muutoksia. Jos valitset **Budjettiraportti**-kentän, raportti laskee kauden odotetun poiston. Syötä *ryhmätyyppi*, jos haluat raportin ryhmittelevän käyttöomaisuuserät ja tulostavan ryhmän yhteissummat. Jos KO-luokkia on määritetty esimerkiksi kuusi, valitse *KO-luokka*-vaihtoehto, jotta kunkin kuuden luokkakoodin osalta tulostetaan ryhmän yhteissummat. |
| **Käyttöomaisuuden KP-analyysi**| 5610 |Tässä raportissa näkyy analyysi käyttöomaisuudesta ja yksittäisten omaisuuserien ja/tai omaisuuserien ryhmien tietoja. Käyttöomaisuus-pikavälilehteen voidaan asettaa suodattimia, jos raportin halutaan sisältävän vain tiettyjä käyttöomaisuuseriä. Asetukset-pikavälilehdellä voit räätälöidä raportin tarpeitasi vastaavaksi. Raportti on samantyyppinen kuin **Käyttöomaisuuden analyysi** -raportti, mutta se on tarkoitettu erityisesti täsmäyttämiseen pääkirjanpidon kanssa ja luovutustapahtumien vahvistamiseen. Raportissa oletetaan, että tunnet kirjauksien asetuksissa määritetyt KP-tilit. |
| **Käyttöomaisuusrekisteri** |5603  |Tässä raportissa näkyvät kirjatut käyttöomaisuustapahtumat lajiteltuina ja jaoteltuina rekisterinumeron mukaan. Näkyvät rekisteritapahtumat voi määrittää asettamalla suodatuksen. Suodatuksen asettaminen on tärkeää, koska muutoin raporttiin voi tulla hyvin suuri määrä tietoa. |

## <a name="see-also"></a>Katso myös

[Rahoituslaskelmien analysointi Microsoft Excelissä](finance-analyze-excel.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Käyttöomaisuuden hallinta](fa-manage.md)  
[Paikallisten toiminnallisuuksien yleiskatsaus](about-localization.md)  
[Kirjanpitäjän käyttökokemukset [!INCLUDE[prod_long](includes/prod_long.md)]issa](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
