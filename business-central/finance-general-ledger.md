---
title: "Tietoja pääkirjanpidosta ja aitoustodistuksesta| Microsoft Docs"
description: "Tämä artikkeli sisältää tietoja pääkirjanpidosta, tilikartasta ja tililuokista."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 1c5fda0c8cd063e784ec44448b040a298bfeaf2f
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="understanding-the-general-ledger-and-the-coa"></a>Pääkirjanpito ja aitoustodistus
Pääkirjanpito sisältää taloustiedot ja tilikartta näyttää tilit, joihin kaikki pääkirjanpidon tapahtumat kirjataan. [!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää tilikartan, joka on valmis tukemaan liiketoimintaasi.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Pääkirjanpidon asetukset ja yleiset kirjausasetukset
Pääkirjanpidon asetukset ovat keskeisiä rahoitusprosesseja, sillä niillä määritetään tietojen kirjaaminen.  

**Pääkirjanpidon asetukset** -ikkunassa määritetään, miten esimerkiksi seuraavat yrityksen kirjanpitoasiat:  

* Laskun pyöristystiliedot  
* Osoitteen muodot  
* Talousraportointi  

Samaan tapaan määritetään **Yleiset kirjausasetukset** -ikkunassa, miten liiketoiminnan ja tuotteen yleisten kirjausryhmien yhdistelmät määritetään. Kirjausryhmät yhdistävät objektit, kuten asiakkaat, toimittajat, nimikkeet, resurssit sekä myynti- ja ostoasiakirjoja pääkirjanpidon tileille. Jokaiselle liiketoiminnan kirjausryhmän ja tuotteen kirjausryhmän yhdistelmälle täytetään rivi. Lisätietoja on kohdassa [Kirjausryhmien asetukset](finance-posting-groups.md)  

## <a name="the-chart-of-accounts"></a>Tilikartta
Kaikki pääkirjanpidon tilit näkyvät tilikartassa. Tilikartassa voi tehdä esimerkiksi seuraavia toimintoja:  

* Voit tarkastella pääkirjanpitotapahtumat- ja saldot näyttäviä raportteja.  
* Voit sulkea tuloslaskelman.  
* Voita avata KP-tilikortin asetusten lisäämistä tai muuttamista varten.  
* Voit tarkastella luetteloa kirjausryhmistä, jotka tekevät kirjauksia kyseiselle tilille.
* Yhden tilin erillisten debet- ja kreditsaldojen näyttäminen  

Voit lisätä, muuttaa tai poistaa pääkirjanpidon tilejä. Ristiriitojen estämiseksi et voi kuitenkaan poistaa pääkirjanpidon tiliä, jos sen tietoja käytetään tilikartassa.  

## <a name="account-categories"></a>Tililuokat
Voit räätälöidä rahoituslaskelmien rakennetta yhdistämällä pääkirjanpidon tilit tililuokkiin.  

**KP-tilin luokat** -ikkunassa on aiemmin luodut pää- ja alaluokat sekä niihin liitetyt KP-tilit. Voit luoda uusia alaluokkia ja liittää luokat aiemmin luotuihin tileihin.  

Voit luoda luokkaryhmän sisentämällä **KP-tilin luokat** -ikkunan rivin alla olevia muita alaluokkia. Tällöin yleiskuvauksen saaminen on helppoa, koska kunkin ryhmittelyn yhteydessä näytetään kokonaissaldo. Voit luoda esimerkiksi alaluokkia eri käyttöomaisuustyypeille ja luoda sitten luokkaryhmiä esimerkiksi käyttöomaisuudelle ja nykyisille vastaaville.  

Voit määrittää, onko kunkin alaluokan tilit sisällytettävä tietyn tyyppisiin raportteihin. Tililuokat auttavat rahoituslaskelmien asettelun määrittämisessä.  

Esimerkiksi oletussaldon tiliotteessa on Käteisvarat-alaluokka Vastaavaa-kohdassa. Jos haluat, että tiliote ottaa käteiskassan ja sekit huomioon, voit  

1. lisätä kaksi uutta alaluokkaa. Niistä toinen on tarkoitettu käteiskassalle ja toinen sekkitilille.  
2. Määritä näille alaluokille lisäraporttimääritys **Käteistilit**.  
3. Sisennä ne **Käteisvarat**-alaluokassa.  

Kun luot seuraavan kerran KP-raporttimalleja, tiliotteessa näkyy käteisvarojen kokonaissaldo sekä käteiskassan ja sekkitilin saldojen kaksi riviä.  

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Tilikartan määrittäminen tai muuttaminen](finance-setup-chart-accounts.md)  
[Business Intelligence](bi.md)  

