---
title: "Toimintaohje: Käyttöomaisuuden budjettien hallinta| Microsoft Docs"
description: "Tässä artikkelissa kerrotaan, miten käyttöomaisuus budjetoidaan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 99df89d29271b7c8426959019dc52ece42525709
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-manage-budgets-for-fixed-assets"></a>Toimintaohje: Käyttöomaisuuden budjettien hallinta
Voit määrittää budjetoidun käyttöomaisuuden. Tässä esimerkissä raportteihin voidaan sisällyttää tämän vuoksi mitä tahansa ennakoituja hankintoja ja myyntejä.  

Budjetoidun tuloslaskelman, budjetoidun taseen ja rahoitusbudjetin valmistelua varten tarvitaan tietoja käyttöomaisuuden tulevista investoinneista, luovutuksista ja poistoista. Nämä tiedot saa **Käyttöomaisuus – Suunnit. arvo** -raportista. Ennen kyseisen raportin tulostamista budjetti tulee valmistella.  

**Huomautus**: Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]-kokemuksen mukauttaminen](ui-experiences.md).

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a>Käyttöomaisuuden hankintamenon budjetointi
Budjetin valmistelemista varten tulee määrittää käyttöomaisuuden kortteja käyttöomaisuuserille, joita aiot ostaa tulevaisuudessa. Budjettikäyttöomaisuuserät määritetään tavallisina käyttöomaisuuserinä, mutta ne on määritettävä niin, että pääkirjanpitoon ei tehdä kirjauksia.

Kun kirjaat hankintamenon, syötä budjetoidun käyttöomaisuuserän numero **Budjetoidun KO:n nro** -kentässä. Tämä aiheuttaa sen, että ohjelma kirjaa hankintamenon, jolla on vastakkainen etumerkki, budjetoidulle käyttöomaisuudelle. Tämä tarkoittaa sitä, että budjetoidun käyttöomaisuuden kokonaishankintameno on budjetoidun ja todellisen hankintamenon välinen ero.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Käyttöomaisuus** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto, kun haluat luoda uuden käyttöomaisuuskortin budjetoitua käyttöomaisuutta varten.
3. Valitse **Budjetoitu käyttöomaisuus** -valintaruutu, kun haluat estää kirjauksen pääkirjanpitoon.
4. Täytä jäljellä olevat kentät, liitä poistokirja ja kirjaa ensimmäinen hankintameno ja budjetoitu käyttöomaisuus, joka on syötetty **Budjetoidun KO:n nro** -kenttään päiväkirjarivillä. Lisätietoja on kohdassa [Toimintaohje: Käyttöomaisuuden hankinta](fa-how-acquire.md).

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a>Käyttöomaisuuden luovutuksen budjetointi
Jos suunnittelet myyväsi omaisuutta budjettijaksolla, voit syöttää tietoja myyntihinnasta ja myyntipäivämäärästä.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Käyttöomaisuus** ja valitse sitten liittyvä linkki.
2. Valitse luovutettava käyttöomaisuus ja valitse sitten **Poistokirjat**-toiminto.
3. Lisää sisältö **KO:n poistokirja**-ikkunassa **Suunnit. luovut. saadut tulot**-kenttään ja **Suunniteltu luovutuspvm** -kentän sisältö. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a>Suunniteltujen luovutusarvojen katsominen
**KO:n suunniteltu arvo** -raportissa voi tarkastella suunniteltuja luovutusarvoja ja laskea voittoja ja tappioita.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **KO:n suunniteltu arvo** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät.
3. Valitse **Tulosta**- tai **Esikatsele**-painike.

## <a name="to-budget-depreciation"></a>Poistojen budjetointi
Laske tuleva poisto **Käyttöomaisuus - Suunnit. arvo** -raportin avulla. Raportissa näkyvät kirjanpitoarvo ja kumulatiiviset poistot valitun ajanjakson alusta, jakson aikaiset muutokset sekä kirjanpitoarvo ja kumulatiiviset poistot valitun ajanjakson lopusta.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **KO:n suunniteltu arvo** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät.
3. Kun haluat nähdä kaikkien käyttöomaisuuserien kokonaisarvot, tyhjennä **Tulosta KO-erittäin** -valintaruutu.
4. Jätä **Käyttöomaisuus**-pikavälilehti tyhjäksi sisällyttääksesi kaikki omaisuuserät. **Budjetoitu käyttöomaisuus** -kenttään syötetään **Ei**, kun budjetoidut käyttöomaisuuserät jätetään huomioimatta, ja **Kyllä**, kun tarkastellaan vain budjetoituja käyttöomaisuuseriä.
5. Valitse **Tulosta**- tai **Esikatsele**-painike.

## <a name="see-also"></a>Katso myös
[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Rahoitus](finance.md)  
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin](index.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)
