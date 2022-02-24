---
title: Erityisten asiakirja-asettelujen määrittäminen asiakkaille tai toimittajille | Microsoft Docs
description: Kun mukautettuja raportin asetteluita määritetään, voit valita ne asiakas- ja toimittajakorteista ja määrittää, että valittuja asetteluita käytetään asiakirjoissa, jotka ovat kyseessä olevalle asiakkaalle tai toimittajalle.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 11/15/2019
ms.author: sgroespe
ms.openlocfilehash: 23c4573c3121a660b8263c3bc9bb2c6ac8b1d331
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/15/2019
ms.locfileid: "2809397"
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Asiakirja-asettelujen määrittäminen asiakkaille ja toimittajille
Kun mukautettuja raportin asetteluita määritetään, voit valita ne asiakas- ja toimittajakorteista ja määrittää, mitä asetteluita käytetään eri asiakirjoissa, jotka on tarkoitettu kyseessä olevalle asiakkaalle tai toimittajalle. **Käyttö**-kentän arvo määrittää, mihin prosessiin asiakirjan asettelua käytetään (esimerkiksi **Muistutus**, **Toimitus** tai **Vahvistus**).

Sen lisäksi, että määrität, mitä asetteluita asiakirjalle käytetään, voit säästää aikaa, kun lähetät asiakirjoja eri asiakas- tai toimittajakontakteille määrittämällä tiettyjen kontaktien sähköpostiosoitteet tiettyjen asiakirjojen kanssa käytettäviksi. Asiakastiliotteet lähetetään esimerkiksi kirjanpitäjäkontakteille, myyntitilaukset asiakkaiden ostajille ja ostotilaukset toimittajien myyjille tai asiakkuuspäälliköille.

Kun määrität asiakirjan asettelun asiakkaalle tai toimittajalle, voit myös määrittää sen kontaktihenkilön sähköpostiosoitteen, jolle asiakirja on osoitettu. Voit tehdä tämän nopeasti käyttämällä **Valitse sähköpostiosoite kontakteista** -toimintoa, joka suodattaa automaattisesti kontaktien sähköpostiosoitteet, jotka on rekisteröity kyseiselle asiakkaalle tai toimittajalle.

Ennen kuin voit määrittää, mitä asiakirja-asettelua käytetään mihinkin prosessiin ja mille kontaktille asiakirjan voi lähettää, sinun täytyy ladata kaikki käytettävissä olevat raportit (asiakirjat) **Raporttivalinnat**-sivulta. Voit tehdä tämän nopeasti **Kopioi raporttivalinnasta** -toiminnolla.

Seuraavassa kuvataan, miten myyntiasiakirja-asetteluita määritetään asiakaskortista. Työvaiheet ovat samat ostoasiakirjan asetteluille toimittajan kortista.

## <a name="to-enable-all-available-sales-documents-for-a-customer"></a>Kaikkien saatavilla olevien myyntiasiakirjojen ottaminen käyttöön asiakkaalle
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
2. Avaa sen asiakkaan kortti, jonka asiakirja-asettelut haluat määrittää liiketoimintaprosessin mukaan.
3. Valitse **Asiakkaan kortti** -sivulla **Asiakirjojen asettelut** -sivu.
4. Valitse **Asiakirjojen asettelu** -sivulla **Kopioi raporttivalinnasta** -toiminto.

Kyseisen asiakkaan **Asiakirjojen asettelut** -sivu täytetään kaikilla järjestelmässä olevilla myynnin raporttiasetteluilla. Lisätietoja niiden luonnista on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

Nyt voit siirtyä muokkaamaan luetteloa mukautettujen raporttien asetteluilla tai niiden kontaktien sähköpostiosoitteilla, joille asiakirjat on lähetettävä.

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Valitse myyntiasiakirjan asettelussa käytettävä mukautettu raporttiasettelu
Jos vähintään yhdelle **Asiakirjojen asettelut** -sivulla määritetyistä asiakkaan raportin asetteluista ei ole määritetty mukautettua raporttiasettelua, voit tehdä sen nopeasti.

1. Valitse **Asiakirjojen asettelut** -sivulla **Mukautetun asettelun kuvaus** -kenttä siltä raporttiasettelun riviltä, jolle haluat käyttää mukautettua asettelua. Kenttä täytetään, jos asiakkaan asettelu on jo valittuna – muutoin se on tyhjä.
2. Valitse **Mukautetut raporttiasettelut** -sivulta erityinen asiakirjan asettelu, jota haluat käyttää kyseessä olevassa myyntiasiakirjatyypissä. Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

## <a name="to-set-up-which-contact-receives-which-document-layout-for-a-customer"></a>Sen määrittäminen, mikä kontakti saa asiakkaan asiakirja-asettelun
Voit säästää aikaa lähetettäessä asiakirjoja eri asiakkaiden tai toimittajien kontakteille määrittämällä kontaktien sähköpostiosoitteet **Asiakirjojen asettelut** -sivun eri riveille. Asiakastiliotteet voidaan lähettää esimerkiksi kirjanpitäjäkontakteille, myyntitilaukset asiakkaiden ostajille ja ostotilaukset toimittajien myyjille tai asiakkuuspäälliköille.

1. Valitse **Asiakirjan asettelut** -sivulla **Valitse sähköpostiosoite kontakteista** -toiminto siltä raporttiasettelun riviltä, jonka haluat lähettää asiakkaan tietylle kontaktille.
2. Valitse **Yhteyshenkilöt**-sivulla asianmukaisen kontaktin rivi ja valitse sitten **OK**-painike.

Kontaktin sähköpostiosoite lisätään nyt asiakirjan asettelun riville, joten kyseinen myyntiasiakirja, esimerkiksi muistutus, lähetetään aina kyseiselle kontaktille asiakkaan yrityksessä.

## <a name="see-also"></a>Katso myös  
[Päivitä mukautetut raporttiasettelut](ui-update-report-layouts.md)  
[Raporttien mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)  
[Raporttien tai asiakirjojen mukautetun asettelun tuonti ja vienti](ui-how-import-and-export-report-layout.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
[Raporttien, eräajojen ja XMLportien käsitteleminen](ui-work-report.md)  
[Raporttien, eräajojen ja XMLportien käsitteleminen](ui-work-report.md)  
