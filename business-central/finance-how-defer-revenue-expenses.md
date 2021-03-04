---
title: Tuottojen ja kulujen siirtäminen| Microsoft Docs
description: Jos haluat tulouttaa tuoton tai kulun jaksoon, joka on eri kuin se, jonka aikana tapahtuma on kirjattu, voit siirtää tai lykätä ne automaattisesti tietyn aikataulun mukaan.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b9d936cffabaea38571fe755ca43ed0cd9a961b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750878"
---
# <a name="defer-revenues-and-expenses"></a>Tuottojen ja kulujen siirtäminen
Jos haluat tulouttaa tuoton tai kulun jaksoon, joka on eri kuin se, jonka aikana tapahtuma on kirjattu, käytä toimintoja, jotka siirtävät tuotot ja kulut automaattisesti tietyn aikataulun mukaan.

Voit jakaa tuotot tai kulut liittyville kirjanpitojaksoille määrittämällä sille resurssille, nimikkeelle tai KP-tilille siirtomallin, jolle tuotto tai kulu kirjataan. Kun kirjaat liittyvän myynti- tai ostoasiakirjan, tuotto tai kulu siirretään liittyville kirjanpitojaksoille sen siirron aikataulun mukaan, jota siirtomallin ja kirjauspäivämäärän asetukset koskevat.

## <a name="to-set-up-a-gl-account-for-deferral"></a>KP-tilin määrittäminen siirtoa varten
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Tilikartta** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Luo siirretyille tuotoille KP-tili täyttämällä tarvittavat kentät. Lisätietoja on kohdassa [Pääkirjanpito ja tilikartta](finance-general-ledger.md).
4. Luo siirretyille kuluille uusi KP-tili toistamalla vaiheet 2 ja 3.

Valitse kummallekin siirtotyypille **Tase** **Tyyppi**-kenttään. Anna tileille soveltuvat nimet, kuten esimerkiksi siirretyille tuotoille Ansaitsematon tulo ja siirretyille kuluille Maksamattomat kulut.

## <a name="to-set-up-a-deferral-template"></a>Siirtomallin määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirtomallit** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät.
4. Määritä **Laskentamenetelmä**-kenttään, miten **Siirron aikataulu** -sivun kunkin jakson **Summa**-kentän arvo lasketaan. Voit valita seuraavista vaihtoehdoista:

   * **Tasapoisto**: Jaksoittaiset siirtosummat lasketaan jaksojen lukumäärän mukaan. Ne jaetaan jakson pituuden mukaan.
   * **Tasan jaksoittain**: Jaksoittaiset siirtosummat lasketaan jaksojen lukumäärän mukaan. Ne jaetaan tasan kaikille jaksoille.
   * **Päivät jaksoittain**: Jaksoittaiset siirtosummat lasketaan jakson päivien lukumäärän mukaan.
   * **Käyttäjän määrittämä**: Jaksottaisia siirtosummia ei lasketa. Siirron aikataulu -sivun kunkin jakson **Summa**-kenttä on täytettävä manuaalisesti. Lisätietoja on Siirron aikataulun muuttaminen myyntilaskusta -osassa.
5. Määritä **Jakson kuvaus** -kenttään kuvaus, joka näytetään siirron kirjauksen tapahtumissa. Voit syöttää tyypillisille arvoille seuraavat paikanvaraajien koodit. Ne lisätään automaattisesti, kun jakson kuvaus näytetään.

   * %1 = jakson kirjauspäivämäärän päivän numero
   * %2 = jakson kirjauspäivämäärän viikon numero
   * %3 = jakson kirjauspäivämäärän kuukauden numero
   * %4 = jakson kirjauspäivämäärän kuukauden nimi
   * %5 = jakson kirjauspäivämäärän kirjanpitojakson nimi
   * %6 = jakson kirjauspäivämäärän tilikausi

Esimerkki: Kirjauspäivämäärä on 6.2.2016. Jos annat Kulut siirretty: %4 %6, näytettävä kuvaus on Kulut siirretty: helmikuu 2016.

## <a name="to-assign-a-deferral-template-to-an-item"></a>Siirtomallin määrittäminen nimikkeelle
> [!NOTE]  
>   Tämän proseduurin vaiheet ovat samat kuin silloin, kun siirtomalli liitetään KP-tiliin tai -resurssiin.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimike** ja valitse sitten liittyvä linkki.
2. Avaa sen nimikkeen kortti, jonka tuotot tai kulut on siirrettävä kirjanpitojaksoille nimikkeen myynnin tai oston yhteydessä.
3. Valitse **Oletussiirtomalli**-kenttään sopiva siirtomalli.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice"></a>Siirtomallin muuttaminen myyntilaskusta
> [!NOTE]  
>   Tämän menettelytavan vaiheet ovat samat kuin vaiheet silloin, kun kulun siirtomalli muutetaan ostolaskusta.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntilaskut** ja valitse sitten liittyvä linkki.
2. Luo myyntilasku nimikkeestä, jolle on määritetty siirtomalli. Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).

    Huomaa, että heti, kun laskuriville on syötetty nimike (tai resurssi tai KP-tili), ohjelma syöttää **Siirron koodi** -kenttään määritetyn siirtomallin koodin.
3. Valitse **Siirron aikataulu** -toiminto.
4. Muuta **Siirron aikataulu** -sivun otsikon tai rivin arvojen asetuksia. Voit esimerkiksi siirtää summan lisäkirjanpitojaksoon.
5. Valitse **Laske aikataulu** -toiminto.
6. Valitse **OK**-painike. Myyntilaskun siirron aikataulu päivitetään. Liittyvää siirtomallia ei muuteta.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger"></a>Siirrettyjen tuottojen tai kulujen kirjanpitoon kirjaamisen tarkasteleminen
> [!NOTE]  
>   Tämän menettelytavan vaiheet ovat samat kuin kulujen siirtojen kirjausten esikatselun vaiheet.

1. Valitse **Myyntilasku**-sivulla **Esikatsele kirjaus** -toiminto.
2. Valitse **Esikatsele kirjaus** -sivulla **KP-tapahtuma**-toiminto ja valitse sitten **Näytä aiheeseen liittyvät tapahtumat** -toiminto.

Tietylle siirtotilille, kuten Ansaitsematon tulo -tilille, kirjattavat KP-tapahtumat merkitään kuvauksella, joka syötettiin siirtomallin **Jakson kuvaus** -kenttään. Esimerkki: Siirretyt kulut: helmikuu 2016.

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report"></a>Kirjattujen siirtojen tarkasteleminen Myynnin siirron yhteenveto -raportissa
> [!NOTE]  
>   Tämän menettelytavan vaiheet ovat samat kuin Ostojen siirron yhteenveto -raportin tarkastelun vaiheet.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myynnin siirron yhteenveto** ja valitse sitten liittyvä linkki.
2. Syötä **Myynnin siirron yhteenveto** -sivun **Saldon tilanne** -kenttään päivämäärä, johon asti siirretyt tuotot näytetään.
3. Valitse **Esikatsele**-painike.

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]