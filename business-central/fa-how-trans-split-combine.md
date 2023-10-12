---
title: Käyttöomaisuuden luokitteleminen uudelleen
description: 'Voit luokitella käyttöomaisuuden uudelleen eri osastoon, jakaa sen tai yhdistää sen käyttöomaisuuseriin.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5638, 5636, 5640, 5637'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="transfer-split-or-combine-fixed-assets"></a>Käyttöomaisuuserien siirtäminen, jakaminen tai yhdistäminen

Käyttöomaisuuden uudelleenluokittelupäiväkirjaa voidaan käyttää käyttöomaisuuserien siirtämisessä, jakamisessa ja yhdistämisessä. Käyttöomaisuuden uudelleenluokittelun tuloksia tarkastellaan ja ne voidaan tulostaa **KO - Kirjanpitoarvo 02** -raportin avulla.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a>Käyttöomaisuuden siirtäminen toiselle osastolle

Käyttöomaisuus on ehkä siirrettävä toiselle osastolle esimerkiksi silloin, kun omaisuuserä sijoitetaan tuotanto-osastoon silloin, kun sitä vielä rakennetaan, ja kun se siirretään hallinto-osastoon valmistumisen jälkeen.  

1. Määritä uusi käyttöomaisuuserä. Syötä uusi osasto dimensioksi.  
2. Liitä käyttöomaisuuden poistokirja uuteen käyttöomaisuuteen. Lisätietoja on kohdassa [Käyttöomaisuuden hankinta](fa-how-acquire.md).
3. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuuden uudelleenluokittelun päiväkirjat** ja valitse sitten liittyvä linkki.
4. Luo päiväkirjan rivi, jonka **KO-nro**-kentässä on alkuperäinen käyttöomaisuuserä ja **Uusi KO-nro** -kentässä on uusi siirrettävä käyttöomaisuuserä. Täytä tarvittaessa myös muut kentät.  
5. Valitse **Uudelleenluokita** -toiminto.

    Rivit luodaan nyt käyttöomaisuuden KP-päiväkirjaan käyttämällä mallia ja erää, jotka olet määrittänyt **KO-päiväkirjan asetukset** -sivulla määritellyn poistokirjan osalta. Lisätietoja on kohdassa [Käyttöomaisuuden poiston määrittäminen](fa-how-setup-depreciation.md).
6. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO - KP-päiväkirjat** ja valitse sitten vastaava linkki.    
7. Valitse **Käyttöomaisuuden KP-päiväkirja** -sivulla **Kirjaa**-toiminto ja kirjaa vaiheissa 4 ja 5 suoritettu uudelleenluokittelu.

Jos yhdelle omaisuuserälle on kirjattu hankintameno, käyttöomaisuuden uudelleenluokituspäiväkirjaa voidaan käyttää jakamaan hankintameno usean omaisuuserän kesken.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>Käyttöomaisuuden jakaminen kolmeen käyttöomaisuuserään
Voit jakaa yhden käyttöomaisuuserän useiksi käyttöomaisuuseriksi esimerkiksi silloin, kun käyttöomaisuuserä on jaettava kolmelle osastolle. Tällöin siirretään esimerkiksi 25 % hankintamenosta ja poistosta alkuperäisen käyttöomaisuuserän osalta toiselle KO-erälle ja 45 % kolmannelle KO-erälle. Jäljelle jäävät 30 % säilyvät alkuperäisellä käyttöomaisuuserällä.

1. Määritä kaksi uutta käyttöomaisuuserää. Syötä asiaankuuluvat osastot dimensioiksi.  
2. Liitä käyttöomaisuuden poistokirjat uusiin käyttöomaisuuseriin. Lisätietoja on kohdassa [Käyttöomaisuuden hankinta](fa-how-acquire.md).
3. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuuden uudelleenluokittelun päiväkirjat** ja valitse sitten liittyvä linkki.
4. Luo kaksi uudelleenluokittelupäiväkirjan riviä, yksi kullekin uudelle käyttöomaisuuserälle.
5. Anna ensimmäisellä rivillä toinen käyttöomaisuuserä **Uusi KO-nro** -kentässä ja 25 **Uudell.luokita hankintameno-%** -kentässä.
6. Anna toisella rivillä kolmas käyttöomaisuuserä **Uusi KO-nro** -kentässä ja 40 **Uudell.luokita hankintameno-%** -kentässä.
7. Valitse molemmilla riveillä **Uudelleenluokita hankintameno**- ja **Uudelleenluokita poisto** -valintaruutu.  
8. Valitse **Uudelleenluokita** -toiminto.  

    Rivit luodaan nyt käyttöomaisuuden KP-päiväkirjaan käyttämällä mallia ja erää, jotka olet määrittänyt **KO-päiväkirjan asetukset** -sivulla määritellyn poistokirjan osalta. Lisätietoja on kohdassa [Käyttöomaisuuden poiston määrittäminen](fa-how-setup-depreciation.md).    
9. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO - KP-päiväkirjat** ja valitse sitten vastaava linkki.
10. Valitse **Käyttöomaisuuden KP-päiväkirja** -sivulla **Kirjaa**-toiminto ja kirjaa vaiheissa 4–8 suoritettu uudelleenluokittelu.

## <a name="to-combine-two-fixed-assets-into-one"></a>Kahden käyttöomaisuuserän yhdistäminen yhdeksi eräksi

Voit yhdistää useita käyttöomaisuuseriä yhdeksi käyttöomaisuuseräksi esimerkiksi silloin, kun siirrät jaetut käyttöomaisuuserät yhteen osastoon. Jos olet kirjannut siirrettävän käyttöomaisuuserän hankintamenot ja poiston, nämä arvot voidaan yhdistää yhdeksi käyttöomaisuuseräksi.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuuden uudelleenluokittelun päiväkirjat** ja valitse sitten liittyvä linkki.
2. Luo uudelleenluokittelupäiväkirjan, jonka **KO-nro**-kentässä on siirrettävä tai yhdistettäv käyttöomaisuuserä ja **Uusi KO-nro** -kentässä on käyttöomaisuuserä, jonka kanssa se yhdistetään.
3. Jätä **Uudell.luokita hankintameno-%** -kenttä tyhjäksi ja siirrä/yhdistä kaikki hankintamenot.  
4. Valitse **Uudelleenluokita hankintameno**- ja **Uudelleenluokita poisto** -valintaruutu.
5. Valitse **Uudelleenluokita** -toiminto.

    Rivit luodaan nyt käyttöomaisuuden KP-päiväkirjaan käyttämällä mallia ja erää, jotka olet määrittänyt **Käyttöomaisuuspäiväkirjan asetukset** -sivulla määritellyn poistokirjan osalta. Lisätietoja on kohdassa [Käyttöomaisuuden poiston määrittäminen](fa-how-setup-depreciation.md).   
6. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöom. KP-päiväkirjat** ja valitse sitten liittyvä linkki.
7. Valitse **Käyttöomaisuuden KP-päiväkirja** -sivulla **Kirjaa**-toiminto ja kirjaa vaiheissa 2–5 suoritettu uudelleenluokittelu.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>Muutetun poistokirjan arvojen tarkasteleminen käyttöomaisuuden uudelleenluokittelun vuoksi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuuden kirjanpitoarvo 02** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät.
3. Valitse **Tulosta**- tai **Esikatsele**-painike.  

## <a name="see-also"></a>Katso myös

[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Taloushallinto](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
