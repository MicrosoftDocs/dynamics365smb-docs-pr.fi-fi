---
title: KO-budjettien hallinta| Microsoft Docs
description: Voit määrittää tietoja tulevista käyttöomaisuuden sijoituksista, luovutuksista ja poistoista budjettien ja ennusteiden valmistelussa auttamiseksi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3b435d1e9edae7a13514786f2de51e32237aaf94
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783557"
---
# <a name="manage-budgets-for-fixed-assets"></a>Käyttöomaisuuden budjettien hallinta
Voit määrittää budjetoidun käyttöomaisuuden. Tässä esimerkissä raportteihin voidaan sisällyttää tämän vuoksi mitä tahansa ennakoituja hankintoja ja myyntejä.  

Budjetoidun tuloslaskelman, budjetoidun taseen ja rahoitusbudjetin valmistelua varten tarvitaan tietoja käyttöomaisuuden tulevista investoinneista, luovutuksista ja poistoista. Nämä tiedot saa **Käyttöomaisuus – Suunnit. arvo** -raportista. Ennen kyseisen raportin tulostamista budjetti tulee valmistella.  

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a>Käyttöomaisuuden hankintamenon budjetointi
Budjetin valmistelemista varten tulee määrittää käyttöomaisuuden kortteja käyttöomaisuuserille, joita aiot ostaa tulevaisuudessa. Budjettikäyttöomaisuuserät määritetään tavallisina käyttöomaisuuserinä, mutta ne on määritettävä niin, että pääkirjanpitoon ei tehdä kirjauksia.

Kun kirjaat hankintamenon, annan budjetoidun käyttöomaisuuserän numero **Budjetoidun KO:n nro** -kentässä. Tämä aiheuttaa sen, että ohjelma kirjaa hankintamenon, jolla on vastakkainen etumerkki, budjetoidulle käyttöomaisuudelle. Tämä tarkoittaa sitä, että budjetoidun käyttöomaisuuden kokonaishankintameno on budjetoidun ja todellisen hankintamenon välinen ero.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuus** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto, kun haluat luoda uuden käyttöomaisuuskortin budjetoitua käyttöomaisuutta varten.
3. Valitse **Budjetoitu käyttöomaisuus** -valintaruutu, kun haluat estää kirjauksen pääkirjanpitoon.
4. Täytä jäljellä olevat kentät, liitä poistokirja ja kirjaa ensimmäinen hankintameno ja budjetoitu käyttöomaisuus, joka on annettu päiväkirjarivin **Budjetoidun KO:n nro** -kentässä. Lisätietoja on kohdassa [Käyttöomaisuuden hankinta](fa-how-acquire.md).

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a>Käyttöomaisuuden luovutuksen budjetointi
Jos suunnittelet myyväsi omaisuutta budjettijaksolla, voit syöttää tietoja myyntihinnasta ja myyntipäivämäärästä.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuus** ja valitse sitten liittyvä linkki.
2. Valitse luovutettava käyttöomaisuus ja valitse sitten **Poistokirjat**-toiminto.
3. Lisää sisältö **KO:n poistokirja**-sivulla **Suunnit. luovut. saadut tulot**-kenttään ja **Suunniteltu luovutuspvm** -kentän sisältö. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a>Suunniteltujen luovutusarvojen katsominen
**KO:n suunniteltu arvo** -raportissa voi tarkastella suunniteltuja luovutusarvoja ja laskea voittoja ja tappioita.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n suunniteltu arvo** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät.
3. Valitse **Tulosta**- tai **Esikatsele**-painike.

## <a name="to-budget-depreciation"></a>Poistojen budjetointi
Laske tuleva poisto **Käyttöomaisuus - Suunnit. arvo** -raportin avulla. Raportissa näkyvät kirjanpitoarvo ja kumulatiiviset poistot valitun ajanjakson alusta, jakson aikaiset muutokset sekä kirjanpitoarvo ja kumulatiiviset poistot valitun ajanjakson lopusta.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuuden suunniteltu arvo** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät.
3. Kun haluat nähdä kaikkien käyttöomaisuuserien kokonaisarvot, tyhjennä **Tulosta KO-erittäin** -valintaruutu.
4. Jätä **Käyttöomaisuus**-pikavälilehti tyhjäksi sisällyttääksesi kaikki omaisuuserät. **Budjetoitu käyttöomaisuus** -kenttään syötetään **Ei**, kun budjetoidut käyttöomaisuuserät jätetään huomioimatta, ja **Kyllä**, kun tarkastellaan vain budjetoituja käyttöomaisuuseriä.
5. Valitse **Tulosta**- tai **Esikatsele**-painike.

## <a name="see-also"></a>Katso myös
[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Rahoitus](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]