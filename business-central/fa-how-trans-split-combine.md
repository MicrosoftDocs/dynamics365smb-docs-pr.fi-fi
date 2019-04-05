---
title: Käyttöomaisuuden uudelleen luokittelu| Microsoft Docs
description: Voit luokitella käyttöomaisuuden uudelleen eri osastoon, jakaa sen tai yhdistää sen käyttöomaisuuseriin.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 81b23fd28426d5241ce24b2a3bd40a5b3ec3379d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795881"
---
# <a name="transfer-split-or-combine-fixed-assets"></a>Käyttöomaisuuserien siirtäminen, jakaminen tai yhdistäminen
Käyttöomaisuuden uudelleenluokittelupäiväkirjaa voidaan käyttää käyttöomaisuuserien siirtämisessä, jakamisessa ja yhdistämisessä. Käyttöomaisuuden uudelleenluokittelun tuloksia tarkastellaan ja ne voidaan tulostaa **KO - Kirjanpitoarvo 02** -raportin avulla.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a>Käyttöomaisuuden siirtäminen toiselle osastolle
Käyttöomaisuus on ehkä siirrettävä toiselle osastolle esimerkiksi silloin, kun omaisuuserä sijoitetaan tuotanto-osastoon silloin, kun sitä vielä rakennetaan, ja kun se siirretään hallinto-osastoon valmistumisen jälkeen.  

1. Määritä uusi käyttöomaisuuserä. Syötä uusi osasto **Osastokoodi**-kenttään.
2. Liitä käyttöomaisuuden poistokirja uuteen käyttöomaisuuteen. Lisätietoja on kohdassa [Käyttöomaisuuden hankinta](fa-how-acquire.md).
3. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n uudelleenluokituspäiväkirjat** ja valitse sitten liittyvä linkki.
4. Luo uudelleenluokittelupäiväkirjan, jonka **KO-nro**-kentässä on alkuperäinen käyttöomaisuuserä ja **Uusi KO-nro** -kentässä on uusi siirrettävä käyttöomaisuuserä.  
5. Valitse **Uudelleenluokita** -toiminto.

    Rivit luodaan nyt käyttöomaisuuden KP-päiväkirjaan käyttämällä mallia ja erää, jotka olet määrittänyt **KO-päiväkirjan asetukset** -sivulla määritellyn poistokirjan osalta. Lisätietoja on kohdassa [Käyttöomaisuuden poiston määrittäminen](fa-how-setup-depreciation.md).
6. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **KO - KP-päiväkirjat** ja valitse sitten liittyvä linkki.    
7. Valitse **Käyttöomaisuuden KP-päiväkirja** -sivulla **Kirjaa**-toiminto ja kirjaa vaiheissa 4 ja 5 suoritettu uudelleenluokittelu.

Jos yhdelle omaisuuserälle on kirjattu hankintameno, käyttöomaisuuden uudelleenluokituspäiväkirjaa voidaan käyttää jakamaan hankintameno usean omaisuuserän kesken.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>Käyttöomaisuuden jakaminen kolmeen käyttöomaisuuserään
Voit jakaa yhden käyttöomaisuuserän useiksi käyttöomaisuuseriksi esimerkiksi silloin, kun käyttöomaisuuserä on jaettava kolmelle osastolle. Tällöin siirretään esimerkiksi 25 % hankintamenosta ja poistosta alkuperäisen käyttöomaisuuserän osalta toiselle KO-erälle ja 45 % kolmannelle KO-erälle. Jäljelle jäävät 30 % säilyvät alkuperäisellä käyttöomaisuuserällä.

1. Määritä kaksi uutta käyttöomaisuuserää. Syötä uusi osasto **Osastokoodi**-kenttään.
2. Liitä käyttöomaisuuden poistokirjat uusiin käyttöomaisuuseriin. Lisätietoja on kohdassa [Käyttöomaisuuden hankinta](fa-how-acquire.md).
3. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n uudelleenluokituspäiväkirjat** ja valitse sitten liittyvä linkki.
4. Luo kaksi uudelleenluokittelupäiväkirjan riviä, yksi kullekin uudelle käyttöomaisuuserälle.
5. Anna ensimmäisellä rivillä toinen käyttöomaisuuserä **Uusi KO-nro** -kentässä ja 25 **Uudell.luokita hankintameno-%** -kentässä.
6. Anna toisella rivillä kolmas käyttöomaisuuserä **Uusi KO-nro** -kentässä ja 40 **Uudell.luokita hankintameno-%** -kentässä.
7. Valitse molemmilla riveillä **Uudelleenluokita hankintameno**- ja **Uudelleenluokita poisto** -valintaruutu.   
8. Valitse **Uudelleenluokita** -toiminto.

    Rivit luodaan nyt käyttöomaisuuden KP-päiväkirjaan käyttämällä mallia ja erää, jotka olet määrittänyt **KO-päiväkirjan asetukset** -sivulla määritellyn poistokirjan osalta. Lisätietoja on kohdassa [Käyttöomaisuuden poiston määrittäminen](fa-how-setup-depreciation.md).    
9. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **KO - KP-päiväkirjat** ja valitse sitten liittyvä linkki.
10. Valitse **Käyttöomaisuuden KP-päiväkirja** -sivulla **Kirjaa**-toiminto ja kirjaa vaiheissa 4–8 suoritettu uudelleenluokittelu.

## <a name="to-combine-two-fixed-assets-into-one"></a>Kahden käyttöomaisuuserän yhdistäminen yhdeksi eräksi
Voit yhdistää useita käyttöomaisuuseriä yhdeksi käyttöomaisuuseräksi esimerkiksi silloin, kun siirrät jaetut käyttöomaisuuserät yhteen osastoon. Jos olet kirjannut siirrettävän käyttöomaisuuserän hankintamenot ja poiston, nämä arvot voidaan yhdistää yhdeksi käyttöomaisuuseräksi.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n uudelleenluokituspäiväkirjat** ja valitse sitten liittyvä linkki.
2. Luo uudelleenluokittelupäiväkirjan, jonka **KO-nro**-kentässä on siirrettävä tai yhdistettäv käyttöomaisuuserä ja **Uusi KO-nro** -kentässä on käyttöomaisuuserä, jonka kanssa se yhdistetään.
3. Jätä **Uudell.luokita hankintameno-%** -kenttä tyhjäksi ja siirrä/yhdistä kaikki hankintamenot.    
4. Valitse **Uudelleenluokita hankintameno**- ja **Uudelleenluokita poisto** -valintaruutu.
5. Valitse **Toiminnot**-välilehdessä **Uudelleenluokita**.

    Rivit luodaan nyt käyttöomaisuuden KP-päiväkirjaan käyttämällä mallia ja erää, jotka olet määrittänyt **KO-päiväkirjan asetukset** -sivulla määritellyn poistokirjan osalta. Lisätietoja on kohdassa [Käyttöomaisuuden poiston määrittäminen](fa-how-setup-depreciation.md).   
6. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **KO - KP-päiväkirjat** ja valitse sitten liittyvä linkki.
7. Valitse **Käyttöomaisuuden KP-päiväkirja** -sivulla **Kirjaa**-toiminto ja kirjaa vaiheissa 2–5 suoritettu uudelleenluokittelu.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>Muutetun poistokirjan arvojen tarkasteleminen käyttöomaisuuden uudelleenluokittelun vuoksi
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO-kirjanpitoarvo 02** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät.
3. Valitse **Tulosta**- tai **Esikatsele**-painike.  

## <a name="see-also"></a>Katso myös
[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Rahoitus](finance.md)  
[Käytön aloittaminen](product-get-started.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
