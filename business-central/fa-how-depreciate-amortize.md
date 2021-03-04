---
title: Käyttöomaisuuden poisto tai kuoletus| Microsoft Docs
description: Määritä, miten toteutat käyttöomaisuutesi arvonalennukset, poistot tai kuoletukset.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3eb4cffd4e67c4cd375619ec8b36e17e6ee527b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749441"
---
# <a name="depreciate-or-amortize-fixed-assets"></a>Käyttöomaisuuden poisto tai kuolettaminen
Poistoja käytetään jakamaan käyttöomaisuuden, esimerkiksi koneiden ja laitteiden, kustannuksia niiden poistoajalle. Jokaisen käyttöomaisuuserän osalta tulee määrittää, miten sille tehdään poistoja.  

 Poistot voi kirjata kahdella tavalla:  

* automaattisesti **Laske poisto** -eräajon avulla.  
* Manuaalisesti käyttöomaisuuden KP-päiväkirjan avulla.  

[!INCLUDE[prod_short](includes/prod_short.md)] voi laskea päivittäisen poiston, jolloin voit laskea poiston mille tahansa ajanjaksolle. Nykyisiä toiminnan tuloksia voi siis analysoida esimerkiksi kuukausittain, neljännesvuosittain tai vuosittain. Laskennassa käytetään 360 päivän vakiovuotta ja 30 päivän vakiokuukautta. Lisätietoja on kohdassa [Poistotavat](fa-depreciation-methods.md).  

Jos useat osastot käyttävät käyttöomaisuuserää, jaksottaiset poistot voidaan kohdistaa automaattisesti näille osastoille käyttäjäkohtaisen kohdistustaulukon mukaisesti.  

Virheellisiä poistotapahtumia voi peruuttaa **Peruuta KO-tapahtumat** -eräajolla. Oikean poistosumman voi kirjata tämän jälkeen suorittamalla uudelleen **Laske poisto** -eräajon. Virheet kirjataan korjattaessa KO-virhetapahtumiksi.  

Indeksointia käytetään muuttamaan arvoja yleisten hintatason muutosten mukaan. **Tee indeksimuutos KO:teen** -eräajoa voidaan käyttää poistosummien uudelleenlaskemiseen.  

## <a name="to-calculate-depreciation-automatically"></a>Poistojen laskeminen automaattisesti
**Laske poisto** -eräajon voi suorittaa kerran kuukaudessa tai valitsemanasi ajankohtana. Eräajo ei huomioi myytyjä tai suljettuja käyttöomaisuuseriä eikä käyttöomaisuuseriä, jotka eivät ole aktiivisia ja jotka käyttävät manuaalista poistomenetelmää.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Laske poisto** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Valitse **OK**-painike.  

    Eräajo laskee poiston ja luo rivejä käyttöomaisuuden KP-päiväkirjaan.

4. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuuden KP-päiväkirjat** ja valitse sitten liittyvä linkki.  

    **Käyttöomaisuuden KP-päiväkirja** -sivun **Poistopäivien lukumäärä** -kentän avulla nähdään, kuinka monta poistopäivää on laskettu.  
5. Valitse **Kirjaa**-toiminto.  

## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Poistojen kirjaaminen manuaalisesti käyttöomaisuuden KP-päiväkirjasta
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuuden KP-päiväkirja** ja valitse sitten liittyvä linkki.  
2. Luo alkuperäisen päiväkirjan rivi ja täytä kentät tarpeen mukaan.  
3. Valitse **KO:n kirjaustyyppi** -kentässä **Poisto**.  
4. Valitse **Syötä KO-vastatili** -toiminto. Toinen päiväkirjan rivi luodaan vastatilille, joka on määritetty poiston kirjaamista varten. Lisätietoja on kohdassa [Käyttöomaisuuden kirjausryhmien määrittäminen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Valitse **Kirjaa**-toiminto kirjataksesi päiväkirjan.  

**Käyttöomaisuuden kortti** -sivun **Kirjanpitoarvo**-kenttä päivitetään sen mukaisesti.

Jos summien kohdistamiseksi eri osastoille tai projekteille on määritetty käyttöomaisuuden kohdistusavaimia, summat kohdistetaan kirjaamisen aikana. Lisätietoja on kohdassa [Käyttöomaisuuden yleisten tietojen määrittäminen](fa-how-setup-general.md).  

## <a name="to-manage-the-ending-book-value"></a>Loppukirjanpitoarvon hallinta
**KO-poistokirjat**-sivun **Loppukirjanpitoarvo**-kentässä voit määrittää kirjanpitoarvon, jonka haluat käyttöomaisuuserälle olevan tämänhetkisessä poistokirjassa sen jälkeen, kun se on kokonaan poistettu. Voit tehdä sen manuaalisesti tai voit täyttää **Poistokirja**-sivun **Loppukirjanpitoarvo, oletus** -kentän, jota käytetään tämän jälkeen kentän automaattiseen täyttämiseen.

> [!NOTE]
> Jos viimeinen poisto aiheuttaa sen, että **Käyttöomaisuuden kortti** -sivun **Kirjanpitoarvo**-kentän arvoksi tulee nolla, ohjelma vähentää automaattisesti viimeisestä poistosta kyseisen summan.<br /><br />
> Jos **Kirjanpitoarvo** on suurempi kuin nolla viimeisen poiston jälkeen, esimerkiksi pyöristysongelman tai jäännösarvon takia, **Loppukirjanpitoarvo**-kenttää **KO-poistokirjat**-sivulla ei huomioida. Lisätietoja on kohdassa [Jäännösarvon kirjaaminen yhdessä hankintamenon kanssa](fa-how-acquire.md#to-post-the-salvage-value-together-with-the-acquisition-cost).

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>Käyttöomaisuuden KO-päiväkirjan kohdistusten laskeminen
Jos useat osastot käyttävät käyttöomaisuuserää, jaksottaiset poistot voidaan kohdistaa automaattisesti näille osastoille käyttäjäkohtaisen kohdistustaulukon mukaisesti.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuuden KP-päiväkirja** ja valitse sitten liittyvä linkki.  
2. Luo alkuperäinen rivi ja täytä kentät tarpeen mukaan.
3. Valitse **KO:n kirjaustyyppi** -kentässä **Kohdistus**.  
4. Valitse **Syötä KO-vastatili** -toiminto. Toinen päiväkirjan rivi luodaan vastatilille, joka on määritetty kohdistuksen kirjaamista varten.  
5. Valitse **Kirjaa**-toiminto kirjataksesi päiväkirjan.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Valmistele useiden poistokirjojen kirjaaminen monistusluetteloiden avulla
Kun täytät poistokirjaan kirjattavat päiväkirjarivit, voit monistaa rivit erilliseen päiväkirjaan, josta ne voidaan kirjata eri poistokirjaan. Lisätietoja on kohdassa [Tapahtumien kirjaaminen eri poistokirjoihin](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poistokirjat** ja valitse sitten liittyvä linkki.  
2. Avaa poistokirja ja valitse **Osa monistusluettelosta** -valintaruutu.  

> [!IMPORTANT]  
>   Jos olet lisännyt valintamerkin **Käytä monistusluetteloa** -kenttään, älä käytä päiväkirjassa numerosarjaa. Tämä sen vuoksi, että käyttöomaisuuden KP-päiväkirjan numerosarjat ja käyttöomaisuuspäiväkirjan numerosarjat eivät ole samoja.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Tapahtumien kirjaaminen eri poistokirjoihin
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuuden KP-päiväkirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Käytä monistusluetteloa** -valintaruutu siinä päiväkirjassa, johon poisto kirjataan.  
3. Täytä tarvittavat jäljellä olevat kentät.  
4. Valitse **Kirjaa**-toiminto.  
5. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **KO-päiväkirjat** ja valitse sitten liittyvä linkki.  

    > [!NOTE]  
    >   **Käyttöomaisuuspäiväkirja**-sivu sisältää uusia rivejä eri poistokirjoille monistusluettelon mukaan.  
6. Tarkista rivit tai muokkaa niitä ja valitse sitten **Kirjaa**-toiminto.  

    > [!NOTE]  
    >   Toinen tapa monistaa tapahtuma erilliseen kirjaan on syöttää poistokirjan koodi **Monista poistokirjaan** -kenttään silloin, kun päiväkirjariviä täytetään.  

Tapahtumia voidaan kopioida poistokirjasta toiseen käyttämällä **Kopioi poistokirja** -eräajoa. Eräajo luo päiväkirjarivejä päiväkirjan erään, jonka olet määrittänyt **KO-päiväkirjan asetukset** -sivulla poistokirjalle, johon haluat kopioida. Katso lisätietoja seuraavasta menettelystä.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Käyttöomaisuustapahtumien kopioiminen poistokirjojen välillä
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poistokirjat** ja valitse sitten liittyvä linkki.  
2. Avaa poistokirjan kortti ja valitse **Kopioi poistokirja** -toiminto.  
3. Täytä **Kopioi poistokirja** -sivun kentät tarvittaessa.  
4. Valitse **OK**-painike.  

Kopioidut rivit luodaan joko käyttöomaisuuden KP-päiväkirjassa tai käyttöomaisuuspäiväkirjassa sen mukaisesti, onko kopioitava poistokirja integroitu pääkirjanpitoon.  

## <a name="see-also"></a>Katso myös
[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]