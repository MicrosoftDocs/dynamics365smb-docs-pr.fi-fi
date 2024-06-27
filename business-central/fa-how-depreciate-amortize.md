---
title: Käyttöomaisuuden poistaminen tai kuolettaminen
description: 'Määritä, miten kukin käyttöomaisuuserä, kuten koneet ja laitteet, arvostetaan, poistetaan tai kuoletetaan niiden elinkaaren aikana.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: write down
ms.search.form: '5610, 5611, 5629, 5633, 5659, 5660, 5663, 5619, 5666'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="depreciate-or-amortize-fixed-assets"></a>Käyttöomaisuuden poistaminen tai kuolettaminen

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

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Laske poisto** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Valitse **OK**-painike.  

    Eräajo laskee poiston ja luo rivejä käyttöomaisuuden KP-päiväkirjaan.

4. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO - KP-päiväkirjat** ja valitse sitten vastaava linkki.  

    **Käyttöomaisuuden KP-päiväkirja** -sivun **Poistopäivien lukumäärä** -kentän avulla nähdään, kuinka monta poistopäivää on laskettu.  
5. Valitse **Kirjaa**-toiminto.  

> [!NOTE]
> Tunnettu rajoitus: Jos valitset **Käytä päivien lukumäärän pakottamista** -kentän arvoksi Kyllä ja **Pakota päivien lukumäärä** -kenttään on määritetty arvo, jonka tuloksena **Kirjauspäivämäärä** miinus **Päivien lukumäärä** -kenttien arvo on edellisen kalenterivuoden päivämäärä, poistoa ei voi kirjata.
> Kiertotapa on vähentää **Pakota päivien lukumäärä** -kenttä korkeintaan laskettuihin päiviin kirjauspäivämäärään asti käyttämällä 30 päivää/kuukausi -mallia TAI valita **Tilikausi 365 päivää** -kenttä poistokirjassa.
> Suosittelemme ensimmäistä vaihtoehtoa, koska et ehkä halua muuttaa 30 päivää/kuukausi -mallin käyttöä poistoissa. Lisätietoja on kohdassa [Tilikausi 365 päivää -kentän poisto](fa-how-setup-depreciation.md#fiscal-year-365-days-field-depreciation).


## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Poistojen kirjaaminen manuaalisesti käyttöomaisuuden KP-päiväkirjasta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöom. KP-päiväkirja** ja valitse sitten liittyvä linkki.  
2. Luo alkuperäisen päiväkirjan rivi ja täytä kentät tarpeen mukaan.  
3. Valitse **KO:n kirjaustyyppi** -kentässä **Poisto**.  
4. Valitse **Syötä KO-vastatili** -toiminto. Toinen päiväkirjan rivi luodaan vastatilille, joka on määritetty poiston kirjaamista varten. Lisätietoja on kohdassa [Käyttöomaisuuden kirjausryhmien määrittäminen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Valitse **Kirjaa**-toiminto kirjataksesi päiväkirjan.  

**Käyttöomaisuuden kortti** -sivun **Kirjanpitoarvo**-kenttä päivitetään sen mukaisesti.

Jos summien kohdistamiseksi eri osastoille tai projekteille on määritetty käyttöomaisuuden kohdistusavaimia, summat kohdistetaan kirjaamisen aikana. Lisätietoja on kohdassa [Käyttöomaisuuden yleisten tietojen määrittäminen](fa-how-setup-general.md).  

## <a name="to-manage-the-ending-book-value"></a>Loppukirjanpitoarvon hallinta

**KO-poistokirjat**-sivun **Loppukirjanpitoarvo**-kentässä voit määrittää kirjanpitoarvon, jonka haluat käyttöomaisuuserälle olevan tämänhetkisessä poistokirjassa sen jälkeen, kun se on kokonaan poistettu. Voit syöttää arvon manuaalisesti tai voit täyttää**Poistokirja**-sivun **Loppukirjanpitoarvo, oletus** -kentän. Arvo täytetään kenttään automaattisesti.

> [!NOTE]
> Jos viimeinen poisto aiheuttaa sen, että **Käyttöomaisuuden kortti** -sivun **Kirjanpitoarvo**-kentän arvoksi tulee nolla, ohjelma vähentää automaattisesti viimeisestä poistosta kyseisen summan.<br /><br />
> Jos **Kirjanpitoarvo** on suurempi kuin nolla viimeisen poiston jälkeen, esimerkiksi pyöristysongelman tai jäännösarvon takia, **Loppukirjanpitoarvo**-kenttää **KO-poistokirjat**-sivulla ei huomioida. Lisätietoja on kohdassa [Jäännösarvon kirjaaminen yhdessä hankintamenon kanssa](fa-how-acquire.md#to-post-the-salvage-value-together-with-the-acquisition-cost).

## <a name="to-calculate-allocations-for-a-fixed-asset"></a>Käyttöomaisuuden kohdistusten laskeminen


1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n kirjausryhmät** ja valitse sitten vastaava linkki.
2. Valitse **Aiheeseen liittyvät**, **Kirjausryhmä**, **Kohdistukset** ja valitse sitten **Poisto**.
3. Täytä KP-tilit ja vastaavat kohdistusprosentit kunkin kirjausryhmän osalta ja sulje sivu.
4. Valitse seuraavaksi ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöom. KP-päiväkirjat** ja valitse sitten liittyvä linkki.
5. Syötä Käyttöomaisuus, ja vastaava KO:n kirjausryhmä ja poistokirja määrittävät kohdistusrivit.
6. Valitse **Kirjaa**-toiminto kirjataksesi päiväkirjan.

> [!NOTE]  
> Jos useat osastot käyttävät käyttöomaisuutta, dimensio voidaan valita Käyttöomaisuuden KP-päiväkirja -rivillä.

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Valmistele useiden poistokirjojen kirjaaminen monistusluetteloiden avulla

Kun täytät poistokirjaan kirjattavat päiväkirjarivit, voit monistaa rivit erilliseen päiväkirjaan, josta ne voidaan kirjata eri poistokirjaan. Lisätietoja on kohdassa [Tapahtumien kirjaaminen eri poistokirjoihin](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poistokirjat** ja valitse sitten vastaava linkki.  
2. Avaa poistokirja ja valitse **Osa monistusluettelosta** -valintaruutu.  

> [!IMPORTANT]  
>   Jos olet lisännyt valintamerkin **Käytä monistusluetteloa** -kenttään, älä käytä päiväkirjassa numerosarjaa. Tämä sen vuoksi, että käyttöomaisuuden KP-päiväkirjan numerosarjat ja käyttöomaisuuspäiväkirjan numerosarjat eivät ole samoja.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Tapahtumien kirjaaminen eri poistokirjoihin

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöom. KP-päiväkirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Käytä monistusluetteloa** -valintaruutu siinä päiväkirjassa, johon poisto kirjataan.  
3. Täytä tarvittavat jäljellä olevat kentät.  
4. Valitse **Kirjaa**-toiminto.  
5. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO-päiväkirjat** ja valitse sitten vastaava linkki.  

    > [!NOTE]  
    > **Käyttöomaisuuspäiväkirja**-sivu sisältää uusia rivejä eri poistokirjoille monistusluettelon mukaan.  
6. Tarkista rivit tai muokkaa niitä ja valitse sitten **Kirjaa**-toiminto.  

    > [!NOTE]  
    > Toinen tapa monistaa tapahtuma erilliseen kirjaan on syöttää poistokirjan koodi **Monista poistokirjaan** -kenttään silloin, kun päiväkirjariviä täytetään.  

Tapahtumia voidaan kopioida poistokirjasta toiseen käyttämällä **Kopioi poistokirja** -eräajoa. Eräajo luo päiväkirjarivejä päiväkirjan erään, jonka olet määrittänyt **KO-päiväkirjan asetukset** -sivulla poistokirjalle, johon haluat kopioida. Lue lisää kohdasta [Käyttöomaisuustapahtumien kopioiminen poistokirjojen välillä](#to-copy-fixed-asset-ledger-entries-between-depreciation-books).  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Käyttöomaisuustapahtumien kopioiminen poistokirjojen välillä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poistokirjat** ja valitse sitten vastaava linkki.  
2. Avaa poistokirjan kortti ja valitse **Kopioi poistokirja** -toiminto.  
3. Täytä **Kopioi poistokirja** -sivun kentät tarvittaessa.  
4. Valitse **OK**-painike.  

Kopioidut rivit luodaan joko käyttöomaisuuden KP-päiväkirjassa tai käyttöomaisuuspäiväkirjassa sen mukaisesti, onko kopioitava poistokirja integroitu pääkirjanpitoon.  

## <a name="see-also"></a>Katso myös

[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Taloushallinto](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
