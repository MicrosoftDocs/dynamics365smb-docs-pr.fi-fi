---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: acde432acabc2d3e73658b0e916d6e4830ccaf52
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104102"
---
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

