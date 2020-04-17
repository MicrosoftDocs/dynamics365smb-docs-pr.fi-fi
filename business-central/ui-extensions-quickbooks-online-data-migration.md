---
title: QuickBooksin siirtolaajennuksen käyttäminen | Microsoft Docs
description: Tässä ohjeaiheessa käsitellään, miten laajennuksella siirretään asiakkaita, toimittajia, nimikkeitä ja tilejä QuickBooks Onlinesta Business Centraliin.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: c3e5415c5da03c4dd9a2228cc21b7c08a9beeec3
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189721"
---
# <a name="the-quickbooks-online-data-migration-extension"></a>QuickBooks Onlinen tietojen siirtolaajennus
Tämä laajennus sisältyy **tietojen siirron** asetusten ohjattuun määritykseen, joka auttaa siirtämään tärkeitä liiketoimintatietoja QuickBooks Onlinesta [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Tämä on kätevää esimerkiksi tilanteessa, jossa liiketoiminta kasvaa ja olet päättänyt päivittää liiketoiminnan hallintasovelluksen aloittamalla [!INCLUDE[d365fin](includes/d365fin_md.md)]in käytön.

## <a name="what-data-can-i-import-from-quickbooks-online"></a>QuickBooks Onlinesta siirrettävät tiedot
Voit tuoda seuraavat tiedot QuickBooks Onlinesta [!INCLUDE[d365fin](includes/d365fin_md.md)]iin:  

* Asiakkaat
* Toimittajat
* Nimikkeet
* Tilikartta
* Pääkirjanpidon alkusaldotapahtuma
* Varastonimikkeiden varastomäärä
* Asiakkaiden ja toimittajien avoimet asiakirjat, kuten laskut, hyvityslaskut ja maksut

Myynti- ja ostoasiakirjoissa vain täydet summat siirretään. Osittain maksettuja summia ei päivitetä. Jos asiakas on esimerkiksi maksanut myyntilaskun 500 dollarista 300, siirrettävä summa on kuitenkin 500. Jos olet vastaanottanut osittaisia maksuja, ne on päivitettävä manuaalisesti ennen tietojen siirtoa tai sen jälkeen. Avoimet tapahtumat on syytä kohdistaa ennen siirtoa, sillä se helpottaa toimintaa siirron jälkeen.

> [!NOTE]  
>   Osto- tai myyntitilauksia ei siirretä.

## <a name="before-you-start"></a>Ennen kuin aloitat
Siirtoprosessiin olennaisesti kuuluva osa on määrittää tilit, joihin tapahtumat siirretään. Nämä yhdistämismääritykset on hyvä suunnitella ennen tietojen siirtoa. Kyse on esimerkiksi tileistä, joille seuraavat tapahtumat kirjataan:  

* Nimikkeiden tai palvelujen myynti asiakkaille.
* Nimikkeiden tai palvelujen osto toimittajilta.  
* Pääkirjanpidon oikaisut.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] edellyttää, että KP-tileille on määritetty tilinumerot. Varmista, että QuickBooks Onlinen tileille on määritetty tilinumerot.

Jos QuickBooks Onlinen tapahtumissa on verosummia, [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on määritettävä veroalueen verotili ennen tapahtumien kirjaamista.

## <a name="how-do-i-start-using-the-extension"></a>Laajennuksen käytön aloittaminen
Aloittaminen on helppoa. Sinun tarvitsee vain suorittaa **tietojen siirron** asetusten ohjattu määritys. Ohjeet:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asetusten ohjattu määritys** ja valitse sitten **Siirrä liiketoimintatiedot**
2. Noudata asetusten ohjatun määrityksen ohjeita.

## <a name="what-do-i-do-after-i-migrate-data"></a>Toimenpiteet tietojen siirtämisen jälkeen
Tietojen siirron jälkeen tapahtumien tila on **Kirjaamaton**, joten voit tarkastella niitä ja tehdä muutoksia. Voit tarkastella tapahtumia siirtymällä sivulle, jossa ne yleensä ovat. Voit tarkastella kirjaamattomia myyntilaskuja esimerkiksi siirtymällä **Myyntilaskut**-sivulle. Voit tarkastella maksupäiväkirjoja siirtymällä **Maksupäiväkirjat**-sivulle.   

Tietyt toimenpiteet kannattaa tehdä:

* Jos QuickBooks Onlinen tapahtumissa oli korotettuja ja alennettuja summia, nämä summat on lisättävä manuaalisesti liittyviin tapahtumiin [!INCLUDE[d365fin](includes/d365fin_md.md)]issa ennen niiden kirjaamista.
* Jos käytät arvolisäveroa (ALV:tä), liiketoiminnan kirjausryhmä ja tuotteen kirjausryhmä on ehkä lisättävä kirjausasetuksiin ALV-summien kirjaamista varten.
* Tarkista pääkirjanpidon tilien alkusaldot. QuickBooks Online ei tallenna kaikkien tilien ajankohtaisia saldoja, joten alkusaldoja on ehkä korjattava.

## <a name="see-also"></a>Katso myös
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
