---
title: Asiakastapahtumien kohdistaminen maksujen täsmäyttämistä varten | Microsoft Docs
description: Ohjeaiheessa kerrotaan, miten asiakkaan kassaanmaksut tai hyvitykset kohdistetaan vähintään yhteen avoimeen asiakastapahtumaan ja asiakasmaksut täsmäytetään.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipt
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a0e2c67b3fd6cdd24074a0a59a012ce325692f16
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781711"
---
# <a name="reconcile-customer-payments-with-the-cash-receipt-journal-or-from-customer-ledger-entries"></a>Asiakkaan maksujen täsmäyttäminen kassapäiväkirjan avulla tai asiakastapahtumista
Kun asiakkaalta saadaan kassaanmaksu tai asiakkaalle tehdään käteishyvitys, on päätettävä, kohdistetaanko maksu tai hyvitys yhteen vai useaan avoimeen debet- tai kredit-tapahtumaan sen sulkemiseksi. Voit määrittää kohdistettavan summan. Voit esimerkiksi kohdistaa osamaksut asiakastapahtumiin. Asiakastapahtumat sulkeminen varmistaa, että tiedot, kuten asiakkaan tilastotiedot, tiliotteet ja viivästyskulut, ovat oikein.

> [!TIP]  
>   Punainen fontti **Asiakastapahtumat**-sivulla ilmaisee, että liittyvä maksu on myöhässä. Jos erääntyneistä maksuista tulee ongelma, niitä voidaan vähentää. Voit ottaa käyttöön **Myöhäisten maksujen ennusteet** -laajennuksen, joka käyttää Azure Machine Learning -ratkaisussa luodun ennakoivan mallin. Sen avulla voi ennustaa maksujen ajoituksen. Näiden ennusteiden avulla voit vähentää avoimia myyntisaatavia ja tarkentaa perintästrategiaa. Jos maksun ennustetaan olevan myöhässä, voit esimerkiksi muuttaa asiakkaan maksuehtoja tai maksutapaa. Lisätietoja on kohdassa [Myöhästyneiden maksujen ennusteet](ui-extensions-late-payment-prediction.md).  

Voit kohdistaa asiakastapahtumia eri tavoilla:

* Antamalla tiedot tietyillä sivuilla:
    * **Maksujen täsmäytyskirjauskansio** -sivu. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).
    * **Maksurekisteröinti**-sivu. Lisätietoja on kohdassa [Asiakasmaksujen täsmäyttäminen maksamattomien myyntiasiakirjojen luettelosta](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).
    * **Kassapäiväkirja**. Tämä käsitellään jäljempänä.
* Täyttämällä **Kohdistetaan asiakirjaan nro** -kenttä myyntihyvityslaskuasiakirjoissa. Tämä käsitellään jäljempänä.
* Käyttämällä **Määritä kohdistustunniste** -toimintoa asiakastapahtumassa. Tämä käsitellään jäljempänä.

> [!NOTE]  
>   Jos asiakkaan kortin **Kohdistustapa**-kentän arvo on **Kohdista vanhimpaan**, maksut kohdistetaan automaattisesti vanhimpaan avoimeen kredit-tapahtumaan, ellei tapahtumaa määritetä manuaalisesti. Jos kohdistustapa on **Manuaalinen**, tapahtumat kohdistetaan aina manuaalisesti.

## <a name="to-fill-and-post-a-cash-receipt-journal"></a>Kassapäiväkirjan täyttäminen ja kirjaaminen
Kassapäiväkirja on yleisen päiväkirjan tyyppi, joten sitä voidaan käyttää kirjaamaan myyntitapahtumia yleinen päiväkirja -, pankki-, asiakas-, toimittaja- ja käyttöomaisuustileille. Voit kohdistaa maksun yhteen tai useampaan debet-tapahtumaan, kun kirjaat maksun, tai tehdä kohdistuksen myöhemmin kirjatuista tapahtumista.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kassapäiväkirja** ja valitse sitten liittyvä linkki.
2. Valitse **Muokkaa päiväkirjaa** -toiminto.
3. Valitse haluamasi erä **Erän nimi** -kentässä.
4. Täytä **Kirjauspvm.**-kentän tiedot.  
5. Valitse **Asiakirjatyyppi**-kentässä **Maksu**.

    **Asiakirjan nro** -kenttään täytetään erään liitetty numerosarja.  
6. Tallenna tunnus, kuten asiakkaan sekin numero, **Ulkoisen asiakirjan nro** -kenttään.
7. Valitse **Tilityyppi**-kentässä **Asiakas**.
8. Valitse **Tilinumero**-kentässä käsiteltävä KP-tili.
9. Jos haluat kirjata kohdistuksen samaan aikaan päiväkirjan kirjaamisen yhteydessä, valitse jokin seuraavista menetelmistä:
10. Valitse **Vastatilin tyyppi** -kentässä kassamaksuille **KP-tili** ja muille maksuille **Pankkitili**.
11. Valitse **Vastatilin nro** -kentässä kassamaksujen kassatili tai muiden maksujen asianmukainen pankkitili.
12. Kirjaa päiväkirja.

## <a name="to-apply-a-payment-to-a-single-customer-ledger-entry"></a>Maksun kohdistaminen yhteen asiakastapahtumaan:
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kassapäiväkirja** ja valitse sitten liittyvä linkki.
2. Valitse **Muokkaa päiväkirjaa** -toiminto.
3. Syötä ensimmäiselle päiväkirjariville asianmukaiset tiedot kohdistettavasta tapahtumasta.
4. Syötä **Asiakirjatyyppi**-kenttään **Maksu**.
5. Syötä **Tilityyppi**-kenttään **Asiakas**.
6. Syötä **Vastatilin tyyppi** -kenttään **Pankkitili**.
7. Avaa **Kohdista asiakastapahtumat** -sivu valitsemalla **Kohdistetaan asiakirjaan nro** -kentässä kenttä.
8. Valitse **Kohdista asiakastapahtumat** -sivulla tapahtuma, johon maksu kohdistetaan.
9. Syötä tapahtumaan kohdistettava summa **Kohdistettava summa** -kenttään. Jos summaa ei määritetä, käytetään enimmäissummaa.

    **Kohdista asiakastapahtumat** -sivun alaosan **Kohdistettu summa** -kentässä on tietty summa sekä tieto siitä, täsmääkö kohdistus.  
10. Valitse **OK**-painike. **Kassapäiväkirja**-sivulla näkyy nyt tapahtuma, jonka olet antanut **Kohdistetaan asiakirjatyyppiin**- ja **Kohdistetaan asiakirjaan nro** -kenttiin.
11. Kirjaa kassapäiväkirja.

## <a name="to-apply-a-payment-to-multiple-customer-ledger-entries"></a>Maksun kohdistaminen useaan asiakastapahtumaan:
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kassapäiväkirja** ja valitse sitten liittyvä linkki.
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
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntihyvityslaskut** ja valitse sitten liittyvä linkki.
2. Avaa haluamasi myyntihyvityslasku.
3. Jos haluat kohdistaa hyvityslaskun yksittäiseen asiakastapahtumaan kirjauksen yhteydessä, valitse **Kohdistetaan asiakirjaan nro** -kentässä tapahtuma, johon haluat kohdistaa maksun.
4. Määritä tapahtumaan kohdistettava summa rivin **Kohdistettava summa** -kenttään.  

    Jos summaa ei määritetä, sovellus kohdistaa automaattisesti enimmäissumman. **Kohdista asiakastapahtumat** -sivun alaosan **Kohdistettu summa** -kentässä on tietty summa sekä tieto siitä, täsmääkö kohdistus.    
5. Valitse **OK**-painike. **Myyntihyvityslasku**-sivulla näkyy nyt tapahtuma, jonka olet antanut **Kohdistetaan asiakirjatyyppiin**- ja **Kohdistetaan asiakirjaan nro** -kentissä. -ikkunassa näkyy nyt kirjattava hyvityslaskun summa sekä mahdolliset maksualennukset.
6. Kirjaa hyvityslasku.

## <a name="to-apply-a-credit-memo-to-multiple-customer-ledger-entries"></a>Hyvityslaskun kohdistaminen useaan asiakastapahtumaan:
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntihyvityslaskut** ja valitse sitten liittyvä linkki.
2. Avaa haluamasi myyntihyvityslasku.
3. Voit kohdistaa hyvityslaskun useaan asiakastapahtumaan kirjaamisen yhteydessä valitsemalla **Kohdista tapahtumat** -toiminto.
4. Valitse rivit, joiden tapahtumiin tapahtuma kohdistetaan, ja valitse sitten **Aseta kohdistustunniste** -toiminto.
5. Määritä yksittäiseen tapahtumaan kohdistettava summa kunkin rivin **Kohdistettava summa** -kenttään. Jos summaa ei määritetä, käytetään enimmäissummaa.  

    **Kohdista asiakastapahtumat** -sivun alaosan **Kohdistettu summa** -kentässä on tietty summa sekä tieto siitä, täsmääkö kohdistus.  
6. Valitse **OK**-painike. **Myyntihyvityslasku**-sivulla näkyy nyt kirjattava hyvityslaskun summa sekä mahdolliset maksualennukset.
7. Kirjaa hyvityslasku.

## <a name="to-apply-posted-customer-ledger-entries"></a>Kirjattujen asiakastapahtumien kohdistaminen:
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
2. Avaa sen asiakkaan kortti, jonka tapahtumia haluat kohdistaa.
3. Valitse **Tapahtumakirjaukset**-toiminto ja valitse sitten sen tapahtuman rivi, johon tapahtuma kohdistetaan.
4. Valitse **Kohdista tapahtumat** -toiminto. Näyttöön avautuu **Kohdista asiakastapahtumat** -sivu, jossa näkyvät asiakkaan avoimet tapahtumat.
5. Valitse rivit, joiden tapahtumiin tapahtuma kohdistetaan, ja valitse sitten **Aseta kohdistustunniste** -toiminto.
6. Määritä yksittäiseen tapahtumaan kohdistettava summa kunkin rivin **Kohdistettava summa** -kenttään. Jos summaa ei määritetä, käytetään enimmäissummaa.  

    Tietty summa näkyy **Kohdista asiakastapahtumat** -sivun alaosan **Kohdistettu summa** -kentässä.  
7. Valitse **Kirjaa kohdistus** -toiminto. Näyttöön avautuu **Kirjaa kohdistus** -sivu, joka sisältää kohdistettavan tapahtuman asiakirjanumeron sekä viimeksi kirjatun tapahtuman kirjauspäivämäärän.  
8. Kirjaa sovellus valitsemalla **OK**.

    Jos kirjatun kohdistuksen tuloksena on suljettuja asiakastapahtumia, näiden tapahtumien **Avoin**-kentässä ei enää ole valintamerkkiä.    
9. Jos haluat nähdä päiväkirjatapahtumat, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten liittyvä linkki. Etsi asianmukaisen asiakkaan kortti nähdäksesi tapahtumat.  

**Avaa**-valintaruutua, joka sijaitsee sen tapahtumakirjausluettelon rivillä, joka sisältää kokonaan kohdistetun tapahtumakirjauksen, ei ole valittu.  

> [!NOTE]  
>   Kun valitset tapahtuman **Kohdista asiakastapahtumat** -sivulla tai useita tapahtumia määrittämällä **Kohdistetaan tunnisteeseen** -kohdan arvon, päiväkirjarivin **Kohdistettu summa** -kentässä näytetään valittujen kirjattujen tapahtumien jäljellä oleva yhteissumma, ellei kentässä ole jo arvoa. Jos asiakkaan kortin **Kohdistustapa**-kentässä valitaan **Kohdista vanhimpaan**, sovellus tekee kohdistuksen automaattisesti.

## <a name="to-apply-customer-ledger-entries-in-different-currencies-to-one-another"></a>Erivaluuttaisten asiakastapahtumien kohdistaminen toisiinsa:
Jos asiakkaalle myydään yhdessä valuutassa ja maksu vastaanotetaan toisessa valuutassa, maksu voidaan kohdistaa laskuun.  

Jos tapahtuma (tapahtuma 1) kohdistetaan eri valuuttaa käyttävään tapahtumaan (tapahtuma 2), tapahtuman 2 summien muuntamisessa käytettävä vaihtokurssi etsitään tapahtuman 1 kirjauspäivämäärän mukaan. Vaihtokurssi löytyy **Valuutan vaihtokurssit** -sivulta.  

Asiakastapahtumien kohdistaminen eri valuutoissa on otettava käyttöön. Lisätietoja on kohdassa [Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kassapäiväkirja** ja valitse sitten liittyvä linkki.
2. Avaa haluamasi päiväkirja ja täytä ensimmäinen tyhjä päiväkirjan rivi valuuttakoodilla.
3. Valitse **Kohdista tapahtumat** -toiminto.
4. Valitse rivi, jonka tapahtumaan kassapäiväkirjan tapahtuma kohdistetaan. Valitse sitten **Aseta kohdistustunniste** -toiminto ja valitse tapahtuma, johon kohdistetaan.
5. Valitse **OK**-painike palataksesi kassapäiväkirjaan.
6. Kirjaa myyntipäiväkirja.  

> [!IMPORTANT]  
>   Kun erivaluuttaisia tapahtumia kohdistetaan, tapahtumat muunnetaan paikallista valuuttaa (USD) käyttäen. Vaikka valuuttojen vaihtokurssit ovat kiinteät (esimerkiksi Yhdysvaltain dollarin ja euron välillä), pieniä jäännössummia saattaa esiintyä, kun ulkomaan valuutat muunnetaan Yhdysvaltain dollariksi. Nämä pienet jäännössummat kirjataan voitoiksi ja tappioiksi **Valuutat**-sivun **Realisoitun. val.voitt. tili**- ja **Realisoitun. val.tapp. tili** -kentissä määritetyille tileille. **Summa (USD)** -kenttää muokataan myös toimittajatapahtumien mukaan.  

## <a name="to-correct-an-application-of-customer-entries"></a>Asiakkaan tapahtumien kohdistuksen korjaaminen
Kun kohdistus korjataan, ohjelma luo ja kirjaa korjaavat tapahtumat (eli tapahtumat, jotka ovat alkuperäisten tapahtumien kanssa identtisiä mutta joiden summakentässä on vastakkainen etumerkki) kaikille tapahtumille, myös kaikille kohdistuksesta johdetuille KP-kirjauksille, kuten maksualennuksille ja valuuttavoitoille tai tappioille. Ohjelma avaa uudelleen kohdistuksen sulkemat tapahtumat.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.
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
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]