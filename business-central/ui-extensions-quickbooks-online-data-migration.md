---
title: QuickBooks Onlinen tietojen siirtolaajennus
description: Tässä ohjeaiheessa käsitellään, miten laajennuksella siirretään asiakkaita, toimittajia, nimikkeitä ja tilejä QuickBooks Onlinesta Business Centraliin.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: extension, migrate, data, QuickBooks, import
ms.search.form: 1830,
ms.date: 06/24/2021
ms.author: bholtorf
ms.openlocfilehash: f2e7c3243a2633534dc36dd37aef5d096a7d1f28
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361365"
---
# <a name="the-quickbooks-online-data-migration-extension"></a>QuickBooks Onlinen tietojen siirtolaajennus

Tämä laajennus sisältyy **tietojen siirron** asetusten ohjattuun määritykseen, joka auttaa siirtämään tärkeitä liiketoimintatietoja QuickBooks Onlinesta [!INCLUDE[prod_short](includes/prod_short.md)]iin. Tämä on kätevää esimerkiksi tilanteessa, jossa liiketoiminta kasvaa ja olet päättänyt päivittää liiketoiminnan hallintasovelluksen aloittamalla [!INCLUDE[prod_short](includes/prod_short.md)]in käytön.

## <a name="what-data-can-i-import-from-quickbooks-online"></a>QuickBooks Onlinesta siirrettävät tiedot

Voit tuoda seuraavat tiedot QuickBooks Onlinesta [!INCLUDE[prod_short](includes/prod_short.md)]iin:  

* Asiakkaat
* Toimittajat
* Nimikkeet
* Tilikartta
* Pääkirjanpidon alkusaldotapahtuma
* Varastonimikkeiden varastomäärä
* Asiakkaiden ja toimittajien avoimet asiakirjat, kuten laskut, hyvityslaskut ja maksut

Myynti- ja ostoasiakirjoissa vain täydet summat siirretään. Osittain maksettuja summia ei päivitetä. Jos asiakas on esimerkiksi maksanut myyntilaskun 500 dollarista 300, siirrettävä summa on kuitenkin 500. Jos olet vastaanottanut osittaisia maksuja, ne on päivitettävä manuaalisesti ennen tietojen siirtoa tai sen jälkeen. Avoimet tapahtumat on syytä kohdistaa ennen siirtoa, sillä se helpottaa toimintaa siirron jälkeen.

> [!NOTE]  
> Osto- tai myyntitilauksia ei siirretä.

## <a name="before-you-start"></a>Ennen kuin aloitat

Siirtoprosessiin olennaisesti kuuluva osa on määrittää tilit, joihin tapahtumat siirretään. Nämä yhdistämismääritykset on hyvä suunnitella ennen tietojen siirtoa. Kyse on esimerkiksi tileistä, joille seuraavat tapahtumat kirjataan:  

* Nimikkeiden tai palvelujen myynti asiakkaille.
* Nimikkeiden tai palvelujen osto toimittajilta.  
* Pääkirjanpidon oikaisut.  

[!INCLUDE[prod_short](includes/prod_short.md)] edellyttää, että KP-tileille on määritetty tilinumerot. Varmista, että QuickBooks Onlinen tileille on määritetty tilinumerot.

Jos QuickBooks Onlinen tapahtumissa on verosummia, [!INCLUDE[prod_short](includes/prod_short.md)]issa on määritettävä veroalueen verotili ennen tapahtumien kirjaamista.

## <a name="how-do-i-start-using-the-extension"></a>Laajennuksen käytön aloittaminen

Aloittaminen on helppoa. Sinun tarvitsee vain suorittaa **tietojen siirron** asetusten ohjattu määritys. Ohjeet:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asetusten ohjattu määritys** ja valitse sitten **Siirrä liiketoimintatiedot**.
2. Noudata asetusten ohjatun määrityksen ohjeita.

## <a name="what-do-i-do-after-i-migrate-data"></a>Toimenpiteet tietojen siirtämisen jälkeen

Tietojen siirron jälkeen tapahtumien tila on **Kirjaamaton**, joten voit tarkastella niitä ja tehdä muutoksia. Voit tarkastella tapahtumia siirtymällä sivulle, jossa ne yleensä ovat. Voit tarkastella kirjaamattomia myyntilaskuja esimerkiksi siirtymällä **Myyntilaskut**-sivulle. Voit tarkastella maksupäiväkirjoja siirtymällä **Maksupäiväkirjat**-sivulle.  

Tietyt toimenpiteet kannattaa tehdä:

* Jos QuickBooks Onlinen tapahtumissa oli korotettuja ja alennettuja summia, nämä summat on lisättävä manuaalisesti liittyviin tapahtumiin [!INCLUDE[prod_short](includes/prod_short.md)]issa ennen niiden kirjaamista.
* Jos käytät arvolisäveroa (ALV:tä), liiketoiminnan kirjausryhmä ja tuotteen kirjausryhmä on ehkä lisättävä kirjausasetuksiin ALV-summien kirjaamista varten.
* Tarkista pääkirjanpidon tilien alkusaldot. QuickBooks Online ei tallenna kaikkien tilien ajankohtaisia saldoja, joten alkusaldoja on ehkä korjattava.

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/migrate-data-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
