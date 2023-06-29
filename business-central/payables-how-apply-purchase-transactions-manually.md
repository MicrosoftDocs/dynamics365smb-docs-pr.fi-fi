---
title: Toimittajan maksukuittien tai hyvitysten täsmäyttäminen maksupäiväkirjassa
description: Voit käsitellä tai täsmäyttää toimittajamaksut tai palautukset manuaalisesti kohdistamalla summan ainakin yhteen avoimeen toimittajatapahtumaan.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment application, payment processing, match payments'
ms.search.form: '62, 233, 522, 623'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="reconcile-vendor-payments-with-the-payment-journal-or-from-vendor-ledger-entries"></a><a name="reconcile-vendor-payments-with-the-payment-journal-or-from-vendor-ledger-entries"></a>Toimittajamaksujen täsmäyttäminen maksukirjauskansiolla tai toimittajatapahtumista
Kun lähetät maksukuitin toimittajalle tai saat hyvityksen toimittajalta, päätä, kohdistetaanko maksu tai hyvitys yhteen avoimeen debet- tai kredit-tapahtumaan vai useaan tällaiseen tapahtumaan. Voit määrittää tarkasti summan, jota käytetään maksukuitin tai hyvityksen kohdistuksessa, eli toimittajapahtumat kohdistetaan tällöin vain osittain. Kaikki toimittajatapahtumat täytyy sulkea (kohdistaa), jotta toimittajatilastot sekä tiliotteiden ja viivästyskulujen raportit ovat virheettömiä.

> [!NOTE]  
>   Toimittajat voivat toisinaan antaa maksuhyvityksen tulevia laskuja vastaan kirjattavan hyvityslaskun sijasta – etenkin silloin, kun palautat nimikkeitä, jotka olet jo maksanut, tai olet maksanut enemmän kuin laskun summan.

Voit kohdistaa toimittajatapahtumia seuraavilla kolmella tavalla:

* antamalla tiedot soveltuvilla sivuilla, kuten **Maksupäiväkirja**- ja **Maksujen täsmäytyskirjauskansio** -sivuilla.
* ostohyvityslaskuasiakirjoista
* toimittajatapahtumista sen jälkeen, kun ostoasiakirjat on kirjattu, mutta ei kohdistettu.

> [!NOTE]  
>   Jos toimittajan kortin **Kohdistustapa**-kentässä on **Kohdista vanhimpaan**, maksut kohdistetaan automaattisesti vanhimpaan avoimeen kredit-tapahtumaan, jos tapahtumaa, johon kohdistetaan, ei määritetä manuaalisesti. Jos asiakkaan kohdistustapa on **Manuaalinen**, tapahtumat on kohdistettava manuaalisesti.

Voit kohdistaa toimittajan maksut manuaalisesti liittyviin ostoasiakirjoihin, kun kirjaat maksut **Maksupäiväkirja**-sivulla. Lisätietoja maksupäiväkirjan täyttämisestä on kohdassa [Maksujen suorittaminen](payables-make-payments.md).

Voit kohdistaa toimittajan maksuja ja asiakkaan maksuja myös sen jälkeen, kun maksut näkyvät negatiivisina pankkitapahtumina pankissa. **Maksujen täsmäytyskirjauskansio** -sivulla voit käyttää pankin tiliotteen tuonnin, automaattisen kohdistuksen ja pankkitilin täsmäytyksen toimintoja. Lisätietoja on kohdassa [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

## <a name="to-apply-a-payment-to-a-single-or-multiple-vendor-ledger-entries"></a><a name="to-apply-a-payment-to-a-single-or-multiple-vendor-ledger-entries"></a>Maksun kohdistaminen yhteen tai useaan toimittajatapahtumaan
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirja** ja valitse sitten vastaava linkki.
2. Syötä **Maksupäiväkirja**-sivulla ensimmäiselle päiväkirjariville asianmukaiset tiedot maksutapahtumasta.
3. Voit kohdistaa yhden toimittajatapahtuman seuraavasti:
   1. Avaa **Kohdista toimittajatapahtumat** -sivu valitsemalla **Kohdistetaan asiakirjaan nro** -kentässä kenttä.
   2. Valitse **Kohdista toimittajatapahtumat** -sivulla tapahtuma, johon maksu kohdistetaan.
   3. Määritä tapahtumaan kohdistettava summa rivin **Kohdistettava summa** -kenttään.
4. Vaihtoehtoisesti voit kohdistaa useita toimittajatapahtumia seuraavasti:

   1. Valitse **Kohdista tapahtumat** -toiminto.
   2. Valitse **Kohdista toimittajatapaht.** -sivulla rivit, joilla oleville tapahtumille maksu kohdistetaan.
   3. Valitse **Aseta kohdistustunniste** -toiminto.  
   4. Määritä yksittäiseen tapahtumaan kohdistettava summa kunkin rivin **Kohdistettava summa** -kenttään.

      Jos summaa ei määritetä, ohjelma kohdistaa automaattisesti enimmäissumman. **Kohdista toimittajatapaht.** -sivun alaosan Kohdistettu summa -kentästä voi tarkistaa summan sekä sen, täsmääkö kohdistus.
5. Valitse **OK**-painike.
6. Valitse **Kirjaa**-toiminto, kun haluat kirjata maksupäiväkirjan.

## <a name="to-apply-a-credit-memo-to-a-single-or-multiple-vendor-ledger-entries"></a><a name="to-apply-a-credit-memo-to-a-single-or-multiple-vendor-ledger-entries"></a>Hyvityslaskun kohdistaminen yhteen tai useaan toimittajatapahtumaan
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostohyvityslasku** ja valitse sitten vastaava linkki.
2. Avaa hyvityslasku, jonka haluat kohdistaa.
3. Syötä tarvittavat tiedot otsikkoon.
4. Voit kohdistaa yhden toimittajan tapahtuman valitsemalla **Kohdistus**-pikavälilehden **Kohdistetaan asiakirjaan nro** -kentässä tapahtuman, johon hyvitys kohdistetaan, ja antamalla sitten **Kohdistettava summa** -kentässä tapahtumaan kohdistettavan summan.
5. Vaihtoehtoisesti voit kohdistaa useita toimittajatapahtumia seuraavasti:

   1. Valitse **Kohdista tapahtumat** -toiminto.
   2. Valitse rivit, joiden tapahtumiin hyvityslaskun tapahtumat kohdistetaan.
   3. Valitse **Aseta kohdistustunniste** -toiminto.  
   4. Määritä yksittäiseen tapahtumaan kohdistettava summa kunkin rivin **Kohdistettava summa** -kenttään.

       Jos summaa ei määritetä, ohjelma kohdistaa automaattisesti enimmäissumman. **Kohdista toimittajatapaht.** -sivun alaosan **Kohdistettu summa** -kentästä voi tarkistaa summan sekä sen, täsmääkö kohdistus.
6. Valitse **OK**-painike.  
   **Ostohyvityslasku**-sivulla näkyy tapahtuma, jonka olet valinnut **Kohdistetaan asiakirjatyyppiin**- ja **Kohdistetaan asiakirjaan nro** -kentissä. Sivulla näkyy myös kirjattava hyvityslaskun summa sekä mahdolliset maksualennukset.
7. Kirjaa ostohyvityslasku valitsemalla **Kirjaa**-painike.

## <a name="to-apply-posted-vendor-ledger-entries"></a><a name="to-apply-posted-vendor-ledger-entries"></a>Kirjattujen toimittajatapahtumien kohdistus:
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten vastaava linkki.
2. Avaa asianmukainen toimittaja, jolla on aiemmin kirjattuja tapahtumia.
3. Valitse **Tapahtumakirjaukset**-toiminto ja valitse sitten **Kohdista tapahtumat** -toiminto.
4. **Kohdista toimittajatapaht.** -sivulla näkyvät toimittajan avoimet tapahtumat.
5. Valitse rivi, jolla kohdistettava tapahtuma on.
6. Valitse **Aseta kohdistustunniste** -toiminto.

    **Kohdistetaan tunnisteeseen** -kentässä on näkyvissä kolme tähteä, jos työskentelet yhden käyttäjän järjestelmässä, tai käyttäjätunnuksesi, jos työskentelet useamman käyttäjän järjestelmässä.  
7. Määritä yksittäiseen tapahtumaan kohdistettava summa kunkin rivin **Kohdistettava summa** -kenttään.

    Jos summaa ei määritetä, ohjelma kohdistaa automaattisesti enimmäissumman. Summan voi tarkistaa **Kohdista toimittajatapaht.** -sivun **Kohdistettu summa** -kentästä.
8. Valitse **Kirjaa kohdistus** -toiminto.  

    Näyttöön avautuu **Kirjaa kohdistus** -sivu, joka sisältää kohdistettavan tapahtuman asiakirjanumeron sekä viimeksi kirjatun tapahtuman kirjauspäivämäärän.
9. Kirjaa sovellus valitsemalla **OK**.

## <a name="to-apply-vendor-ledger-entries-in-different-currencies-to-one-another"></a><a name="to-apply-vendor-ledger-entries-in-different-currencies-to-one-another"></a>Eri valuutoissa olevien toimittajatapahtumien kohdistaminen toisiinsa:
Jos ostat toimittajalta yhdessä valuutassa ja maksat maksun toisessa valuutassa, maksu voidaan silti kohdistaa maksun laskuun.

Jos tapahtuma (tapahtuma 1) kohdistetaan eri valuuttaa käyttävään tapahtumaan (tapahtuma 2), tapahtuman 2 summien muuntamisessa käytettävä vaihtokurssi etsitään tapahtuman 1 kirjauspäivämäärän mukaan. Vaihtokurssi löytyy **Valuutan vaihtokurssit** -sivulta. Siinä tapauksessa toimittajatapahtumien kohdistus on otettava käyttöön eri valuutoissa. Lisätietoja on kohdassa [Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa](finance-how-enable-application-ledger-entries-different-currencies.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirja** ja valitse sitten vastaava linkki.
2. Avaa haluamasi päiväkirja ja täytä ensimmäinen tyhjä päiväkirjan rivi valuuttakoodilla.
3. Valitse **Kohdista tapahtumat** -toiminto.
4. Valitse rivi, jonka tapahtumaan maksupäiväkirjan tapahtuma kohdistetaan. Valitse sitten **Aseta kohdistustunniste** -toiminto ja valitse tapahtuma, johon kohdistetaan.
5. Valitse **OK**-painike palataksesi maksupäiväkirjaan.
6. Kirjaa maksupäiväkirja.

> [!IMPORTANT]  
>   Kun erivaluuttaisia tapahtumia kohdistetaan toisiinsa, tapahtumat muunnetaan paikalliseen valuuttaan (USD). Vaikka asianmukaisten valuuttojen vaihtokurssit ovat kiinteät (esimerkiksi Yhdysvaltain dollarin ja euron välillä), pieniä jäännössummia saattaa esiintyä, kun ohjelma muuntaa nämä ulkomaan valuutat USD:ksi. Nämä pienet jäännössummat kirjataan voitoiksi ja tappioiksi **Valuutat**-sivun **Realisoitun. val.voitt. tili**- ja **Realisoitun. val.tapp. tili** -kentissä määritetyille tileille. **Summa (USD)** -kenttää muokataan myös asianmukaisten toimittajatapahtumien mukaan.

## <a name="to-unapply-an-application-of-vendor-entries"></a><a name="to-unapply-an-application-of-vendor-entries"></a>Toimittajan tapahtumien kohdistuksen peruuttaminen
Kun tehdään virheellinen kohdistus, ohjelma luo ja kirjaa korjaavat tapahtumat (eli tapahtumat, jotka ovat alkuperäisten tapahtumien kanssa identtisiä mutta joiden summakentässä on vastakkainen etumerkki) kaikille tapahtumille, myös kaikille kohdistuksesta johdetuille KP-kirjauksille, kuten maksualennuksille ja valuuttavoitoille- tai tappioille. Ohjelma avaa uudelleen kohdistuksen sulkemat tapahtumat.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten vastaava linkki.
2. Avaa asianmukainen toimittajan kortti.
3. Valitse **Tapahtumakirjaukset**-toiminto.
4. Valitse haluamasi tapahtuma ja valitse sitten **Peruuta kohdistus** -toiminto.
5. Vaihtoehtoisesti voit valita **Yksityiskoht. tapahtumat.** -toiminnon.
6. Valitse haluamasi kohdistustapahtuma ja valitse sitten **Peruuta kohdistus** -toiminto.
7. Täytä pyyntöikkunan kentät ja valitse sitten **Peruuta kohdistus** -toiminto.

> [!IMPORTANT]  
>   Jos tapahtumaan on tehty useita kohdistuksia, on viimeisin kohdistustapahtuma poistettava ensin.

## <a name="see-also"></a><a name="see-also"></a>Katso myös
[Ostovelat](payables-manage-payables.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
