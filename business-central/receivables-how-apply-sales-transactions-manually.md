---
title: Täsmäytä asiakasmaksut kassapäiväkirjan tai asiakastapahtumien kanssa
description: Asiakkaan kassasuorituksen tai hyvityksen kohdistaminen yhteen tai useaan avoimeen asiakastapahtumaan.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '25, 255'
ms.date: 05/17/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="reconcile-customer-payments-with-a-cash-receipt-journal-or-from-customer-ledger-entries"></a>Asiakasmaksujen täsmäyttäminen kassapäiväkirjan tai asiakastapahtumien kanssa

Kun saat asiakkaalta käteismaksun tai saat hyvityksen, voit kohdistaa maksun tai hyvityksen avointen debet- tai kredit-maksujen päättämiseen. Voit määrittää kohdistettavan summan. Voit esimerkiksi kohdistaa osamaksut asiakastapahtumiin. Asiakastapahtumien sulkeminen varmistaa, että tiedot, kuten asiakkaan tilastotiedot, tiliotteet ja viivästyskulut, ovat päivitettyjä.

> [!TIP]  
> Punainen fontti **Asiakastapahtumat**-sivulla ilmaisee, että liittyvä maksu on myöhässä. Jos erääntyneistä maksuista tulee ongelma, niitä voidaan vähentää. Voit ottaa käyttöön **Myöhäisten maksujen ennusteet** -laajennuksen, joka käyttää Azure Machine Learning -ratkaisussa luodun ennakoivan mallin. Sen avulla voi ennustaa maksujen ajoituksen. Näiden ennusteiden avulla voit vähentää avoimia myyntisaatavia ja tarkentaa perintästrategiaa. Jos maksun ennustetaan olevan myöhässä, voit esimerkiksi muuttaa asiakkaan maksuehtoja tai maksutapaa. Lisätietoja on kohdassa [Myöhästyneiden maksujen ennusteet](ui-extensions-late-payment-prediction.md).  

Voit kohdistaa asiakastapahtumia eri tavoilla:

* Lisää tietoja seuraaville sivuille:
   * **Maksujen täsmäytyskirjauskansio** -sivu. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).
   * **Maksurekisteröinti**-sivu. Lisätietoja on kohdassa [Asiakasmaksujen täsmäyttäminen maksamattomien myyntiasiakirjojen luettelosta](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).
   * Kassapäiväkirja-sivu **·** . Lisätietoja [on kohdassa Kassapäiväkirjan täyttäminen ja kirjaaminen](#to-fill-and-post-a-cash-receipt-journal).
* Täyttämällä **Kohdistetaan asiakirjaan nro** -kenttä myyntihyvityslaskuasiakirjoissa. Lisätietoja on kohdassa [Hyvityslaskun kohdistaminen yhteen asiakastapahtumaan](#to-apply-a-credit-memo-to-a-single-customer-ledger-entry).
* Käyttämällä **Määritä kohdistustunniste** -toimintoa asiakastapahtumassa. Lisätietoja [on kohdassa Maksun kohdistaminen yhteen asiakastapahtumaan](#to-apply-a-payment-to-a-single-customer-ledger-entry).
* Käyttämällä **Kohdista tapahtumat** -toimintoa **Pankkitalletus**-sivulla ja syöttämällä laskun numeron **Kohdistetaan tunnisteeseen** -kenttään. Lisätietoja on kohdassa [Pankkitalletusten luominen](bank-create-bank-deposits.md).

> [!NOTE]  
> Jos asiakkaan kortin **Kohdistustapa**-kentän arvo on **Kohdista vanhimpaan**, maksut kohdistetaan automaattisesti vanhimpaan avoimeen kredit-tapahtumaan, ellei tapahtumaa määritetä manuaalisesti. Jos kohdistustapa on **Manuaalinen**, tapahtumat kohdistetaan aina manuaalisesti.

## <a name="to-fill-and-post-a-cash-receipt-journal"></a>Kassapäiväkirjan täyttäminen ja kirjaaminen

Kassapäiväkirja on yleisen päiväkirjan tyyppi. Sen avulla voit merkitä transaktioita pääkirjanpidon, pankin, asiakkaan, toimittajan ja kiinteän omaisuuden tileihin. Voit kohdistaa maksun yhteen tai useampaan debet-tapahtumaan, kun kirjaat maksun. Voit myös tehdä kohdistuksen myöhemmin kirjatuista tapahtumista.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kassapäiväkirja** ja valitse sitten vastaava linkki.
2. Valitse **Muokkaa päiväkirjaa** -toiminto.
3. Valitse haluamasi erä **Erän nimi** -kentässä.
4. Täytä **Kirjauspvm.**-kentän tiedot.  
5. Valitse **Asiakirjatyyppi**-kentässä **Maksu**.

    **Asiakirjan nro** -kenttään täytetään erään liitetty numerosarja.  
6. Tallenna tunnus, kuten asiakkaan sekin numero, **Ulkoisen asiakirjan nro** -kenttään.

   > [!NOTE]
   > Oletusarvo on Ulkoisen asiakirjan nro kenttä on piilotettu. Jos näin on ja haluat käyttää sitä, voit lisätä sen mukautuskäytön avulla. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

7. Valitse **Tilityyppi**-kentässä **Asiakas**.
8. Tilinro-kentässä **·** -kentästä, valitse asiakas.
9. Voit kirjata kohdistuksen päiväkirjan kirjaamisen yhteydessä täyttämällä seuraavat kentät:
   1. Valitse **Vastatilin tyyppi** -kentässä kassamaksuille **KP-tili** ja muille maksuille **Pankkitili**.
   2. Valitse **Vastatilin nro** -kentässä kassamaksujen kassatili tai muiden maksujen asianmukainen pankkitili.
10. Kirjaa päiväkirja.

## <a name="to-apply-a-payment-to-a-single-customer-ledger-entry"></a>Maksun kohdistaminen yhteen asiakastapahtumaan:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, syötä **Kassapäiväkirja** ja valitse liittyvä linkki.
2. Valitse **Muokkaa päiväkirjaa** -toiminto.
3. Syötä ensimmäiselle päiväkirjariville asianmukaiset tiedot kohdistettavasta tapahtumasta.
4. Syötä **Asiakirjatyyppi**-kenttään **Maksu**.
5. Syötä **Tilityyppi**-kenttään **Asiakas**.
6. Syötä **Vastatilin tyyppi** -kenttään **Pankkitili**.
7. Avaa **Kohdista asiakastapahtumat** -sivu valitsemalla **Kohdistetaan asiakirjaan nro** -kentässä kenttä.
8. Valitse **Kohdista asiakastapahtumat** -sivulla tapahtuma, johon maksu kohdistetaan.
9. Syötä tapahtumaan kohdistettava summa **Kohdistettava summa** -kenttään. Jos summaa ei määritetä, käytetään enimmäissummaa.

    **Kohdista asiakastapahtumat** -sivun alaosan **Kohdistettu summa** -kentässä on tietty summa sekä tieto siitä, täsmääkö kohdistus.  
10. Valitse **OK**-painike. **Kassapäiväkirja**-sivulla näkyy nyt tapahtuma **Kohdistetaan asiakirjatyyppiin**- ja **Kohdistetaan asiakirjaan nro** -kentissä.
11. Kirjaa kassapäiväkirja.

## <a name="to-apply-a-payment-to-multiple-customer-ledger-entries"></a>Maksun kohdistaminen useaan asiakastapahtumaan:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kassapäiväkirja** ja valitse sitten vastaava linkki.
2. Valitse **Muokkaa päiväkirjaa** -toiminto.
3. Syötä ensimmäiselle päiväkirjariville asianmukaiset tiedot kohdistettavasta tapahtumasta.
4. Syötä **Asiakirjatyyppi**-kenttään **Maksu**.
5. Syötä **Tilityyppi**-kenttään **Asiakas**.
6. Syötä **Vastatilin tyyppi** -kenttään **Pankkitili**.
7. Syötä **Summa**-kenttään täysi maksu negatiivisena summana.
8. Voit kohdistaa maksun useaan asiakastapahtumaan kirjaamisen yhteydessä valitsemalla **Kohdista tapahtumat** -toiminto.  
9. Valitse rivit, joiden tapahtumiin tapahtuma kohdistetaan, ja valitse sitten **Aseta kohdistustunniste** -toiminto.  
10. Määritä yksittäiseen tapahtumaan kohdistettava summa kunkin rivin **Kohdistettava summa** -kenttään. Jos summaa ei määritetä, käytetään enimmäissummaa.

    **Kohdista asiakastapahtumat** -sivun alaosan **Kohdistettu summa** -kentässä on tietty summa sekä tieto siitä, täsmääkö kohdistus.  
11. Valitse **OK**-painike.
12. Kirjaa kassapäiväkirja.

## <a name="to-apply-a-credit-memo-to-a-single-customer-ledger-entry"></a>Hyvityslaskun kohdistaminen yhteen asiakastapahtumaan:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntihyvityslaskut** ja valitse sitten vastaava linkki.
2. Avaa haluamasi myyntihyvityslasku.
3. Jos haluat kohdistaa hyvityslaskun yksittäiseen asiakastapahtumaan kirjauksen yhteydessä, valitse **Kohdistetaan asiakirjaan nro** -kentässä tapahtuma, johon haluat kohdistaa maksun.
4. Määritä tapahtumaan kohdistettava summa rivin **Kohdistettava summa** -kenttään.  

    Jos summaa ei määritetä, sovellus kohdistaa automaattisesti enimmäissumman. **Kohdista asiakastapahtumat** -sivun alaosan **Kohdistettu summa** -kentässä on tietty summa sekä tieto siitä, täsmääkö kohdistus.  
5. Valitse **OK**-painike.  **Myynnin hyvityslasku** -sivulla näkyy nyt kohdistetaan asiakirjatyyppiin **- ja** Kohdistetaan asiakirjaan nro -kentässä valitsemasi **tapahtuma.** Kentät. -ikkunassa näkyy nyt kirjattava hyvityslaskun summa sekä mahdolliset maksualennukset.
6. Kirjaa hyvityslasku.

## <a name="to-apply-a-credit-memo-to-multiple-customer-ledger-entries"></a>Hyvityslaskun kohdistaminen useaan asiakastapahtumaan:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntihyvityslaskut** ja valitse sitten vastaava linkki.
2. Avaa haluamasi myyntihyvityslasku.
3. Voit kohdistaa hyvityslaskun useaan asiakastapahtumaan kirjaamisen yhteydessä valitsemalla **Kohdista tapahtumat** -toiminto.
4. Valitse rivit, joiden tapahtumiin tapahtuma kohdistetaan, ja valitse sitten **Aseta kohdistustunniste** -toiminto.
5. Määritä yksittäiseen tapahtumaan kohdistettava summa kunkin rivin **Kohdistettava summa** -kenttään. Jos summaa ei määritetä, käytetään enimmäissummaa.  

    **Kohdista asiakastapahtumat** -sivun alaosan **Kohdistettu summa** -kentässä on tietty summa sekä tieto siitä, täsmääkö kohdistus.  
6. Valitse **OK**-painike. **Myyntihyvityslasku**-sivulla näkyy nyt kirjattava hyvityslaskun summa sekä mahdolliset maksualennukset.
7. Kirjaa hyvityslasku.

## <a name="to-apply-posted-customer-ledger-entries"></a>Kirjattujen asiakastapahtumien kohdistaminen:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Avaa sen asiakkaan kortti, jonka tapahtumia haluat kohdistaa.
3.  **Valitse Tapahtumakirjaukset-toiminto** ja valitse rivi, jolla on kohdistustapahtuma.
4. Valitse **Kohdista tapahtumat** -toiminto. Näyttöön avautuu **Kohdista asiakastapahtumat** -sivu, jossa näkyvät asiakkaan avoimet tapahtumat.
5. Valitse rivit, joiden tapahtumiin tapahtuma kohdistetaan, ja valitse sitten **Aseta kohdistustunniste** -toiminto.
6. Määritä yksittäiseen tapahtumaan kohdistettava summa kunkin rivin **Kohdistettava summa** -kenttään. Jos summaa ei määritetä, käytetään enimmäissummaa.  

    Tietty summa näkyy **Kohdista asiakastapahtumat** -sivun alaosan **Kohdistettu summa** -kentässä.  
7. Valitse **Kirjaa kohdistus** -toiminto. Näyttöön avautuu **Kirjaa kohdistus** -sivu, joka sisältää kohdistettavan tapahtuman asiakirjanumeron sekä viimeksi kirjatun tapahtuman kirjauspäivämäärän.  
8. Kirjaa sovellus valitsemalla **OK**.

    Jos kirjatun kohdistuksen tuloksena oli suljettuja asiakastapahtumia, **Avoin-kenttä** tyhjeni näiden tapahtumien osalta.  
9. Kirjanpitotapahtumat nähdäksesi valitse ![Lamppu, joka avaa toisena Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki. Etsi asianmukaisen asiakkaan kortti nähdäksesi tapahtumat.  

**Avaa**-valintaruutua, joka sijaitsee sen tapahtumakirjausluettelon rivillä, joka sisältää kokonaan kohdistetun tapahtumakirjauksen, ei ole valittu.  

> [!NOTE]  
> Kun valitset tapahtuman **Kohdista asiakastapahtumat** -sivulla tai useita tapahtumia määrittämällä **Kohdistetaan tunnisteeseen** -kohdan arvon, päiväkirjarivin **Kohdistettu summa** -kentässä näytetään valittujen kirjattujen tapahtumien jäljellä oleva yhteissumma, ellei kentässä ole jo arvoa. Jos asiakkaan kortin **Kohdistustapa**-kentässä valitaan **Kohdista vanhimpaan**, sovellus tekee kohdistuksen automaattisesti.

## <a name="to-apply-customer-ledger-entries-in-different-currencies-to-one-another"></a>Erivaluuttaisten asiakastapahtumien kohdistaminen toisiinsa:

Jos asiakkaalle myydään yhdessä valuutassa ja maksu vastaanotetaan toisessa valuutassa, maksu voidaan kohdistaa laskuun.  

Esimerkki: Tapahtuma A kohdistetaan toisessa valuutassa tapahtumaan B. Tapahtuman A kirjauspäivämäärää käytetään, kun halutaan löytää vaihtokurssi, jota käytetään muunnettaessa summia tapahtumassa B. Vaihtokurssi löytyy **Valuutan vaihtokurssit** -sivulta.  

Asiakastapahtumien kohdistaminen eri valuutoissa on otettava käyttöön. Lisätietoja on kohdassa [Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kassapäiväkirja** ja valitse sitten vastaava linkki.
2. Avaa haluamasi päiväkirja ja täytä ensimmäinen tyhjä päiväkirjan rivi valuuttakoodilla.
3. Valitse **Kohdista tapahtumat** -toiminto.
4. Valitse rivi, jonka tapahtumaan kassapäiväkirjan tapahtuma kohdistetaan. Valitse sitten **Aseta kohdistustunniste** -toiminto ja valitse tapahtuma, johon kohdistetaan.
5. Valitse **OK**-painike palataksesi kassapäiväkirjaan.
6. Kirjaa myyntipäiväkirja.  

> [!IMPORTANT]  
>   Kun erivaluuttaisia tapahtumia kohdistetaan, tapahtumat muunnetaan paikallista valuuttaa (USD) käyttäen. Vaikka valuuttojen vaihtokurssit ovat kiinteät (esimerkiksi Yhdysvaltain dollarin ja euron välillä), pieniä jäännössummia saattaa esiintyä, kun ulkomaan valuutat muunnetaan Yhdysvaltain dollariksi. Nämä pienet jäännössummat kirjataan voitoiksi ja tappioiksi **Valuutat**-sivun **Realisoitun. val.voitt. tili**- ja **Realisoitun. val.tapp. tili** -kentissä määritetyille tileille. **Summa (USD)** -kenttää muokataan myös toimittajatapahtumien mukaan.  

## <a name="to-correct-an-application-of-customer-entries"></a>Asiakkaan tapahtumien kohdistuksen korjaaminen
Kun kohdistus korjataan, ohjelma luo ja kirjaa korjaavat tapahtumat kaikille tapahtumille. Korjaustapahtumat ovat samat kuin alkuperäiset, mutta niillä on vastakkainen merkki **Summa**-kentässä. Korjaustapahtumat sisältävät kaikki kohdistuksesta johdetut pääkirjanpidon tapahtumat. Esimerkiksi maksualennus ja valuuttavoitot/-tappiot. Kohdistuksen sulkema tapahtumat avataan uudelleen.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Avaa haluamasi asiakkaan kortti.
3. Valitse **Tapahtumakirjaukset**-toiminto.
4. Valitse haluamasi tapahtuma ja valitse sitten **Peruuta kohdistus** -toiminto.
5. Vaihtoehtoisesti voit valita **Yksityiskoht. tapahtumat.** -toiminnon.
6. Valitse haluamasi kohdistustapahtuma ja valitse sitten **Peruuta kohdistus** -toiminto.
7. Täytä pyyntöikkunan kentät ja valitse sitten **Peruuta kohdistus** -toiminto.  

> [!IMPORTANT]  
>   Jos tapahtumaan on tehty useita kohdistuksia, on viimeisin kohdistustapahtuma poistettava ensin.  

## <a name="see-also"></a>Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
