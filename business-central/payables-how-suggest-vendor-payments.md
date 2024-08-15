---
title: Toimittajan maksujen ehdottaminen
description: Käytä Ehdota toimittajamaksuja -erätyötä luodaksesi maksurivejä toimittajillesi eräpäivien ja maksualennusten perusteella.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256,'
ms.date: 07/17/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Toimittajan maksujen ehdottaminen

Voit ehdottaa maksurivejä käyttämällä **Maksupäiväkirja**-sivulla **Ehdota toimittajamaksuja** -eräajoa. [!INCLUDE [prod_short](includes/prod_short.md)] ehdottaa asetuksiin perustuvia rivejä:

- Pian erääntyvät maksut.
- Maksut, joille on saatavilla maksualennus.

Maksuehdotuksia voi hyödyntää täysimääräisesti, kun toimittajat on priorisoitu. Lisätietoja toimittajien priorisoinnista on kohdassa [toimittajien priorisointi](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Eräajo ei sisällä toimittajatapahtumia, jotka ovat **Pidossa** tai jotka on jo kohdistettu ja joilla on arvo **Kohdistus tunnisteeseen** -kentässä.  

> [!IMPORTANT]  
> Jos haluat käyttää maksualennuksia ja olet antanut käytettävissä olevan summan, summaa käytetään  
>
> * Priorisoiduissa erääntyvissä toimittajatapahtumissa tärkeysjärjestyksessä.
> * erääntyneissä toimittajatapahtumissa, joita ei ole priorisoitu  
> * Avoimissa toimittajatapahtumissa, joissa voi käyttää maksualennuksia. Tapahtumat on järjestetty toimittajan numeron mukaan.  

## Ehdota toimittajamaksuja -toiminnon käyttäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten vastaava linkki.  
2. Avaa päiväkirja ja valitse **Ehdota toimittajamaksuja** -toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Valitse **OK**-painike.  

## Eräpäivän lisääminen maksupäiväkirjan rivien kirjauspäivämääräksi

Kun **Ehdota toimittajamaksuja** -eräajoa käytetään toimittajien maksurivien luomisessa, täyttämällä kaksi erikoiskenttää voi varmistaa, että luodut rivit käyttävät eräpäivää kirjauspäivämäärän laskemisessa. Nämä kentät ovat **Laske kirjauspvm kohdistetaan asiakirjaan -kentästä. Eräpäivä** ja **Kohdistetaan asiakirjaan Eräpäivän vastakirjaus**.  

> [!IMPORTANT]  
> Laske kirjauspvm kohdistetaan asiakirjaan -kentästä ei voi käyttää **. Eräpäivä-kenttä** yhdessä Etsi maksualennukset -kentän tai **Tiivistys** toimittajaa **kohti -kentän kanssa** . Jos kirjauspäivä perustuu eräpäivään, joitain maksualennuksia ei ehkä ole laskettu oikein, koska kirjauspäivä on maksualennuspäivän jälkeen.  

Jos laskettu kirjauspäivämäärä on myös menneisyydessä, kirjauspäivämäärää siirretään käsittelypäivämäärään ja näyttöön tulee varoitus.  

Voit myös luoda maksurivejä manuaalisesti niin, että eräpäivää käytetään kirjauspäivämäärän laskemisessa. Kun kohdistat toimittajatapahtumia, voit päivittää päiväkirjan rivin kirjauspäivän liittyvän ostolaskun eräpäivällä käyttämällä **Laske kirjauspäivämäärä** -toimintoa. Lisätietoja manuaalista prosessista on kohdassa [Ostotapahtumien manuaalinen kohdistaminen](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
> Jos ostolasku on myöhässä, kirjauspäivämäärä määritetään käsittelypäivämääräksi ja rivin fontti muuttuu punaiseksi.  

## Katso myös

- [Ostovelkojen hallinta](payables-manage-payables.md)  
- [Maksujen suorittaminen](payables-make-payments.md)  
- [Yleisten päiväkirjojen käsitteleminen](ui-work-general-journals.md)  
- [Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
