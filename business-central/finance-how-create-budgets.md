---
title: Luodaan KP-budjetteja
description: Tässä artikkelissa käsitellään, miten luodaan KP-budjetteja ennustamaan erilaisia taloudellisia toimintoja ja miten dimensiot määritetään liiketoimintatietoja varten.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: 113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 87fb665d57aaa6c66b4b3c2659d9e93a6e51239d
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514041"
---
# <a name="create-gl-budgets"></a>KP-budjettien luominen

Sinulla voi olla useita budjetteja samalle ajanjaksolle, kun luot budjetit eri nimillä. Määrittele ensin budjetin nimi ja syötä budjettiluvut. Budjetin nimi tulee sitten kaikkiin luomiisi budjettitapahtumiin.  

Kun luot budjetin, voit määritellä jokaiselle budjetille neljä dimensiota. Näitä budjettikohtaisia dimensioita kutsutaan budjettidimensioiksi. Valitse budjettidimensiot jo luomistasi dimensioista. Budjettidimensioita voidaan käyttää, kun halutaan asettaa suodatin budjetille tai kun halutaan lisätä dimensiotietoa budjettitapahtumiin. Lisätietoja on kohdassa [Dimensioiden käyttäminen](finance-dimensions.md).

Budjeteilla on tärkeä osa liiketoimintatiedoissa, kuten KP-raporttimalleihin perustuvissa tilinpäätöksissä, jotka sisältävät budjettitapahtumia, tai analysoitaessa budjetoituja summia todellisia summia vastaan tilikartassa. Lisätietoja on kohdassa [Business Intelligence](bi.md).

Voit käsitellä kustannusbudjetteja samalla tavoin kustannuslaskennassa. Lisätietoja on kohdassa [Kustannusbudjettien luominen](finance-create-cost-budgets.md).  

## <a name="to-create-a-new-gl-budget"></a>Uuden KP-budjetin luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KP-budjetit** ja valitse sitten vastaava linkki.  
2. Valitse **Muokkaa luetteloa** -toiminto ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Valitse **Muokkaa budjettia** -toiminto.
4. Täyttämällä **Budjetti**-sivun yläosan kentät määrität, mitä näytetään.  

    Näytössä näkyvät vain ne tapahtumat, joilla on **Budjetin nimi** -kentässä annettu nimi. Koska budjetin nimi on juuri luotu, suodatinta vastaavia tapahtumia ei ole. Tämän vuoksi sivu on tyhjä.  
5. Jos haluat lisätä summan, napsauta solua matriisissa. **KP-budjetin tapahtumat** -sivu avautuu.  
6. Luo uusi rivi ja määritä **Summa**-kentän arvo. Sulje **KP-budjetin tapahtumat** -sivu.  
7. Toista vaiheet 5 ja 6, kunnes olet määrittänyt kaikki budjettisummat.  

> [!NOTE]  
> **Suodattimet** -pikavälilehdessä voit suodattaa budjettitietoja sen mukaan, mitä budjettidimensioita olet luonut budjetin nimen alle.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>KP-budjettien vieminen ja tuominen Excelissä

Niin kuin käytännössä kaikkia muitakin sivuja voit viedä budjettisivujen tiedot Exceliin lisäkäsittelyä tai -analyysia varten. Lisätietoja on kohdassa [Liiketoimintatietojen vieminen Exceliin](about-export-data.md).

> [!NOTE]
> Tilikartassa, johon KP-budjetit perustuvat, on Otsikko-tilityypin rivejä, joissa ilmoitetaan otsikon alla olevien rivien määrä. Kun viet KP-budjetin, kaikkien rivien tiedot viedään tilityypistä riippumatta. Kuitenkin vain Kirjaus-tilityypin rivien tiedot voida tuoda takaisin. Näin ollen: <br /><br /> **Kun tuot KP-budjetin, kaikki Otsikko-riveillä olevat arvot poistetaan.** <br /><br /> Tällä tavoin estetään virheelliset yhteissummat sen jälkeen, kun Excelissä luotuja tai muokattuja tietoja on tuotu.<br /><br /> **Esimerkkitilanne**: Tiedät, että uudet budjetoidut palkkakustannukset tulevat olemaan PVA:na 1 200 000. Haluat, että palkkaosaston budjetissa on tietyt kolme (Kirjaus-tilityypin) riviä: kokoaikaiset työntekijät, osa-aikaiset työntekijät ja satunnaiset työntekijät. Nämä kolme riviä ryhmitellään Palkat-otsikkorivin kohdalle.<br /><br />Lisää 1 200 000 Otsikko-riville, vie budjetti Exceliin ja lähetä se sitten palkkaosastolle ja pyydä heitä jakamaan PVA 1 200 000.<br /><br /> Palkkaosasto jakaa summan kolmelle kirjaustilille. Kun tuot KP-budjetin takaisin, uudet Excel-tiedot on täytetty kolmelle tilille. Niiden summa on PVA 1 200 000 ja otsikkorivi on tyhjä.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Liiketoimintatietojen vienti Exceliin](about-export-data.md)  
[Rahoitus](finance.md)  
[Business Intelligence](bi.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]