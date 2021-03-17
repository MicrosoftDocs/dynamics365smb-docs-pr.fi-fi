---
title: QuickBooksin siirtolaajennus | Microsoft Docs
description: Tässä ohjeaiheessa käsitellään, miten laajennuksella tuodaan asiakkaita, toimittajia, nimikkeitä ja tilejä QuickBooks Desktopista Business Centraliin.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 990aabaaccbf32a5cbd95c09527657757e5182cb
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391422"
---
# <a name="the-quickbooks-data-migration-extension"></a>QuickBooks-tietojen siirtolaajennus

Tämän laajennuksen avulla asiakkaat, toimittajat, nimikkeet ja tilit on helppo siirtää QuickBooksista [!INCLUDE[prod_short](includes/prod_short.md)]iin. Jos yrityksessä on käytössä QuickBooks, voit viedä tarpeelliset tiedot ja ladata ne sitten [!INCLUDE[prod_short](includes/prod_short.md)]iin avaamalla avustetun asennusoppaan.  
Lisätietoja on kohdassa [Tietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md).

## <a name="data-from-quickbooks-desktop"></a>Tietoja QuickBooks Desktopista

Voit tuoda seuraavat tiedot QuickBooks Onlinesta Business Centraliin:

- Asiakkaat  
- Toimittajat  
- Nimikkeet  
- Tilikartta  
- Pääkirjanpidon alkusaldotapahtuma  
- Varastonimikkeiden varastomäärä  
- Asiakkaiden ja toimittajien avoimet asiakirjat, kuten laskut, hyvityslaskut ja maksut  

Myynti- ja ostoasiakirjoissa vain täydet summat siirretään. Osittain maksettuja summia ei päivitetä. Jos asiakas on esimerkiksi maksanut myyntilaskun 500 dollarista 300, siirrettävä summa on kuitenkin 500. Jos olet vastaanottanut osittaisia maksuja, ne on päivitettävä manuaalisesti ennen tietojen siirtoa tai sen jälkeen. Avoimet tapahtumat on syytä kohdistaa ennen siirtoa, sillä se helpottaa toimintaa siirron jälkeen.

> [!NOTE]
> Osto- tai myyntitilauksia ei siirretä.

## <a name="before-you-start"></a>Ennen aloittamista

Siirtoprosessiin olennaisesti kuuluva osa on määrittää tilit, joihin tapahtumat siirretään. Nämä yhdistämismääritykset on hyvä suunnitella ennen tietojen siirtoa. Kyse on esimerkiksi tileistä, joille seuraavat tapahtumat kirjataan:

- Nimikkeiden tai palvelujen myynti asiakkaille  
- Nimikkeiden tai palvelujen osto toimittajilta  
- Pääkirjanpidon oikaisut  

Business Central edellyttää, että KP-tileille on määritetty tilinumerot. Varmista, että QuickBooks-tileille on määritetty tilinumerot.
QuickBooksin tapahtumissa on verosummia, Business Centralissa on määritettävä veroalueen verotili ennen tapahtumien kirjaamista.

Tietojen saaminen QuickBooks Desktop -sovelluksesta edellyttää Microsoftin tietojen vientityökalun lataamista.  Työkalun ohjeet ovat [!INCLUDE[prod_short](includes/prod_short.md)]in ohjatussa tietojen siirtotoiminnossa. Työkalu muodostaa yhteyden QuickBooks-sovellukseen ja vie soveltuvat tiedot .zip-tiedostoon.  

> [!NOTE]
> Tällä hetkellä tietojen vientityökalua voi käyttää vain QuickBooks 2017:n ja 2018:n kanssa.

## <a name="finding-the-quickbooks-data-migration-extension"></a>QuickBooks-tietojen siirtolaajennuksen etsiminen

QuickBooks-tietojen siirtolaajennus on asennettu ja valmis käytettäväksi tietojen siirtoasetusten ohjatun määrityksen osana. Jos olet valmis aloittamaan käytön nyt ja olet vienyt tiedot QuickBooksista, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asetusten ohjattu määritys** ja valitse sitten liittyvä linkki. Valitse **Siirrä liiketoimintatiedot** ja noudata oppaan ohjeita.  

## <a name="what-do-i-do-after-i-migrate-data"></a>Toimenpiteet tietojen siirtämisen jälkeen

Tietojen siirron jälkeen tapahtumien tila on Kirjaamaton, joten voit tarkastella niitä ja tehdä muutoksia. Voit tarkastella tapahtumia siirtymällä sivulle, jossa ne yleensä ovat. Voit tarkastella kirjaamattomia myyntilaskuja esimerkiksi siirtymällä Myyntilaskut-sivulle. Voit tarkastella maksupäiväkirjoja siirtymällä Maksupäiväkirjat-sivulle.
Tietyt toimenpiteet kannattaa tehdä: Jos QuickBooks Onlinen tapahtumissa oli korotettuja ja alennettuja summia, nämä summat on lisättävä manuaalisesti liittyviin tapahtumiin Business Centralissa ennen niiden kirjaamista.
Jos käytät arvolisäveroa (ALV:tä), liiketoiminnan kirjausryhmä ja tuotteen kirjausryhmä on ehkä lisättävä kirjausasetuksiin ALV-summien kirjaamista varten.
Tarkista pääkirjanpidon tilien alkusaldot. QuickBooks ei tallenna kaikkien tilien ajankohtaisia saldoja, joten alkusaldoja on ehkä korjattava.

## <a name="see-also"></a>Katso myös

[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]