---
title: Kirjauksen kumoaminen kirjaamalla palautustapahtuma
description: 'Jos huomaat virheen yleisen päiväkirjan kirjauksessa, voit käyttää Peruuta tapahtuma -toimintoa kumotaksesi kirjauksen ja luodaksesi oikean kirjausketjun.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a>Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen

Käänteiset päiväkirjan kirjaukset ovat hyödyllisiä esimerkiksi virheiden korjaamiseen ja vanhan jaksotustapahtuman tyhjentämiseen ennen uuden syöttämistä. Käänteinen kirjaus on sama kuin alkuperäinen kirjaus, mutta sillä on vastakkainen merkki **Summa**-kentässä. Käänteisellä kirjauksella tulee olla sama asiakirjanumero ja kirjauspäivämäärä kuin alkuperäisessä kirjauksessa. Kun peruutat tapahtuman, lisää tapahtuma korjattuna.

Vain yleisen päiväkirjan riviltä kirjatut tapahtumat voi peruuttaa. Tapahtuman voi peruuttaa vain kerran.

Voit kumota vastaanoton tai toimituksen kirjauksen ennen niiden kirjaamista laskutettuina käyttämällä kirjatun asiakirjan **Kumoa**-toimintoa. Voit kumota määriä, jotka ovat tyyppiä **Nimike** tai **Resurssi**.

Jos olet tehnyt virheellisen negatiivisen määräkirjauksen, kuten kirjannut ostotilaukselle väärän määrän vastaanotetuksi mutta ei laskutetuksi, voit kumota kirjauksen.

Jos olet tehnyt virheellisen positiivisen määräkirjauksen, kuten kirjannut myyntitoimitukselle tai ostopalautustoimitukselle väärän määrän toimitetuksi mutta ei laskutetuksi, voit kumota kirjauksen.

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Pääkirjanpidon tapahtuman päiväkirjakirjauksen peruuttaminen

Tapahtumia voi peruuttaa kaikista **Tapahtumakirjaukset**-sivuilta. Seuraava menettely perustuu **Pääkirjanpidon tapahtumat** -sivuun.

> [!NOTE]
> Kirjauksen on oltava peräisin päiväkirjan kirjauksesta.
>
> Et voi peruuttaa tapahtumia, jotka on kirjattu työn tiedoilla tai joilla on realisoituneet voitot ja tappiot samassa tapahtumassa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon tapahtumat** ja valitse sitten vastaava linkki.
2. Valitse ensin peruutettava tapahtuma ja sitten **Peruuta tapahtuma** -toiminto.
3. Valitse **Peruuta tapahtumakirjaukset**-sivulla **Peruuta**-toiminto.
4. Vahvista peruutus valitsemalla **Kyllä**.

## <a name="to-post-a-negative-entry"></a>Negatiivisen tapahtuman kirjaaminen

Kirjaa **Korjaus**-kentän avulla tilille negatiivinen debet kreditin sijaan tai negatiivinen kredit debetin sijaan. Oletusarvon mukaan kenttä on käytettävissä kaikissa päiväkirjoissa. **Debet-summa**- ja **Kredit-summa**-kentät sisältävät sekä alkuperäisen että korjatun tapahtuman. Kentät eivät vaikuta tilin saldoon.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten vastaava linkki.  
2. Valitse haluttu erän nimi **Erän nimi** -kentässä.  
3. Lisää tiedot asianmukaisiin kenttiin.  
4. Valitse **Korjaus**-valintaruutu sen kirjauskansion rivillä, jonka haluat ottaa käyttöön negatiivisia tapahtumia varten.  
5. Kirjaa kirjauskansio valitsemalla **Kirjaa**-toiminto ja valitsemalla sitten **Kyllä**-painike.

## <a name="to-undo-a-quantity-on-a-posted-purchase-receipt"></a>Kirjatun ostovastaanoton määrän kumoaminen

Seuraavissa vaiheissa kerrotaan, miten kirjattu nimikkeiden tai resurssien vastaanotto kumotaan. Vaiheet ovat samankaltaisia kirjatuissa toimituksissa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut ostovastaanotot** ja valitse sitten vastaava linkki.  
2. Avaa kirjattu vastaanotto, jonka haluat kumota.  
3. Valitse kumottavat rivit.  
4. Valitse **Peruuta vast.otto** -toiminto.

Korjaava rivi lisätään valitun kuittirivin alle. Jos määrä vastaanotettiin fyysisen varastoinnin vastaanottona, korjaava rivi lisätään kirjattuun fyysisen varastoinnin vastaanottoon.  

**Vastaanotettu määrä** ja **Vast.otettu laskuttamaton määrä** -kenttien arvoiksi liittyvällä ostotilauksella asetetaan nolla.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Kirjatun palautustoimituksen määrän kirjauksen kumoaminen ja tekeminen uudelleen

Seuraavissa vaiheissa kerrotaan, miten

* Nimikkeiden tai resurssien kirjattu palautustoimitus peruutetaan.
* Ostopalautus kirjataan uudelleen uudella määrällä.

Vaiheet ovat samankaltaisia kirjatuissa palautuskuiteissa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut palautustoimitukset** ja valitse sitten vastaava linkki.  
2. Kirjatun palautustoimituksen palautus avataan.
3. Peruutettavat rivit valitaan.  

4. Valitse **Peruuta palautustoimitus** -toiminto.  

    Ohjelma syöttää korjaavan rivin kirjatulle asiakirjalle ja **Toimitettu palautusmäärä** ja **Pal.määrä toimitettu ei laskutettu** -kentät palautustilauksella asetetaan nollaksi.  

    Palaa nyt ostopalautustilaukseen ja tee kirjaus uudelleen.  

5. Kirjoita muistiin numero, joka on **Kirjattu palautustoimitus** -sivun **Palautustilauksen nro** -kentässä.  
6. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostopalautustilaukset** ja valitse sitten vastaava linkki.  
7. Avaa kyseinen palautustilaus ja valitse **Avaa uudelleen** -toiminto.  
8. Korjaa tapahtuma **Määrä**-kentässä ja kirjaa ostopalautustilaus uudelleen.  

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

## <a name="see-also"></a>Katso myös

[Kokoonpanon kirjauksen kumoaminen](assembly-how-to-undo-assembly-posting.md)  
[Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Rahoitus](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
