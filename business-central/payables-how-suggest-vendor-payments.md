---
title: Ehdota toimittajamaksuja -eräajo
description: 'Määrittämällä toimittajan maksuasetukset saat ehdotuksia maksuista, joiden eräpäivä on pian tai joissa on käytettävissä alennus.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: 256
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="suggest-vendor-payments"></a><a name="suggest-vendor-payments"></a><a name="suggest-vendor-payments"></a>Ehdota toimittajamaksuja

Voit ehdottaa maksurivejä käyttämällä **Maksupäiväkirja**-sivulla **Ehdota toimittajamaksuja** -eräajoa. Asetusten mukaan ehdotetaan rivejä, kuten pian erääntyviä maksuja tai maksuja, joissa on käytettävissä maksualennus.

Maksuehdotuksia voi hyödyntää täysimääräisesti, kun toimittajat on ensin priorisoitu. Lisätietoja on kohdassa [Toimittajien priorisoiminen](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Toimittajatapahtumia, jotka on merkitty **Estossa**-merkinnällä, ei sisällytetä eräajoon.  

> [!IMPORTANT]  
>   Jos haluat käyttää maksualennuksia ja olet antanut käytettävissä olevan summan, summaa käytetään  
    * priorisoiduissa erääntyvissä toimittajatapahtumissa tärkeysjärjestyksessä   
    * erääntyneissä toimittajatapahtumissa, joita ei ole priorisoitu  
    * avoimissa toimittajatapahtumissa, joissa voi käyttää maksualennuksia, toimittajanumeron mukaan järjestettynä.  

## <a name="to-use-the-suggest-vendor-payments-function"></a><a name="to-use-the-suggest-vendor-payments-function"></a><a name="to-use-the-suggest-vendor-payments-function"></a>Ehdota toimittajamaksuja -toiminnon käyttäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten vastaava linkki.  
2. Avaa asianmukainen päiväkirja ja valitse **Ehdota toimittajamaksuja** -toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Valitse **OK**-painike.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a><a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a><a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Eräpäivän lisääminen maksupäiväkirjan rivien kirjauspäivämääräksi

Kun **Ehdota toimittajamaksuja** -eräajoa käytetään toimittajien maksurivien luomisessa, täyttämällä kaksi erikoiskenttää voi varmistaa, että luodut rivit käyttävät eräpäivää kirjauspäivämäärän laskemisessa. Nämä kentät ovat **Laske kirjauspäivämäärä kohdistuksen asiakirjan eräpäivästä** ja **Kohdistuksen asiakirjan eräpäivän siirtymä**.  

> [!IMPORTANT]  
>   Et voi käyttää **Laske kirjauspäivämäärä kohdistuksen asiakirjan eräpäivästä** -kenttää yhdessä **Hae maksualennukset**- tai **Tee yhteenveto toimittajittain** -kentän kanssa. Jos kirjauspäivä perustuu eräpäivään, joitain maksualennuksia ei ehkä ole laskettu oikein, koska kirjauspäivä on maksualennuspäivän jälkeen.  

Jos laskettu kirjauspäivämäärä on myös menneisyydessä, kirjauspäivämäärää siirretään käsittelypäivämäärään ja näyttöön tulee varoitus.  

Vaihtoehtoisesti voit luoda maksurivejä manuaalisesti niin, että eräpäivää käytetään kirjauspäivämäärän laskemisessa. Kun kohdistat toimittajatapahtumia, voit päivittää päiväkirjan rivin kirjauspäivän liittyvän ostolaskun eräpäivällä käyttämällä **Laske kirjauspäivämäärä** -toimintoa. Lisätietoja on kohdassa [Ostotapahtumien kohdistaminen manuaalisesti](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
>   Jos ostolasku on myöhässä, kirjauspäivämäärä määritetään käsittelypäivämääräksi ja rivin fontti muuttuu punaiseksi.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/suggest-vendor-payments-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Ostovelkojen hallinta](payables-manage-payables.md)  
[Maksujen suorittaminen](payables-make-payments.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
