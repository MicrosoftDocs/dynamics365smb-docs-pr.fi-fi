---
title: 'Projektin resurssikustannusten, hintojen ja kapasiteetin määrittäminen'
description: Voit käyttää resursseja ja helpottaa projektinhallintaa määrittämällä yksittäisten resurssien tai resurssiryhmien kustannukset ja hinnat sekä resurssikapasiteetin.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '72, 76, 77, 203, 204'
ms.date: 08/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-resources-for-projects"></a>Projektien resurssien määrittäminen

Jotta voit hallita resurssitoimintoja tarkasti, sinun on määritettävä resurssit sekä niihin liittyvät kustannukset ja hinnat. Projekteihin liittyvät hinnat, alennukset ja kustannustekijäsäännöt määritetään projektikortissa. Voit määrittää kustannukset ja hinnat yksittäisille resursseille, resurssiryhmille tai kaikille yrityksen käytettävissä oleville resursseille.

Kun resursseja käytetään tai myydään projektissa, niihin liittyvät hinnat ja kustannukset haetaan määrittämistäsi tiedoista.

Tuntikohtainen oletussumma määritetään resurssin luomisen yhteydessä. Jos käytät projektissa esimerkiksi tiettyä konetta viisi tuntia, projekti lasketaan tuntikohtaisen summan perusteella.

> [!NOTE]
> Tiettyä projektia varten ei voi ostaa ulkoisia resursseja. On suositeltavaa, että tämän tyyppistä Huolto-tyyppistä nimikettä käytetään.

## <a name="to-set-up-a-resource"></a>Resurssin määrittäminen

Luo jokaiselle projekteissa käytettävälle resurssille kortti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssit** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-a-resource-group"></a>Resurssiryhmän määrittäminen

Yhteen resurssiryhmään voi yhdistää useita resursseja. Kaikki resurssiryhmien kapasiteetit ja budjetit kertyvät yksittäisistä resursseista. Resurssiryhmille voi syöttää kapasiteetteja joko kertyneistä arvoista itsenäisesti tai niiden lisäksi.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssiryhmät** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät.

## <a name="to-set-capacity-for-a-resource"></a>Resurssin kapasiteetin määrittäminen

Resurssien kapasiteetti on määritettävä työkalenteriin jaksoittaisena saatavuusaikana, jotta voit laskea, kuinka kauan resurssia voi käyttää projektissa. Tätä määritystä käytetään silloin, kun täytät projektin suunnittelurivit, jotka sisältävät resurssin. Lisätietoja on kohdassa [Projektien luominen](projects-how-create-jobs.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssit** ja valitse sitten vastaava linkki.
2. Avaa asianmukainen resurssikortti ja valitse **Resurssikapasiteetti**-toiminto.
3. **Resurssikapasiteettimatriisi**-pikavälilehden sarakkeissa näytettävä jakson pituus, kuten **Päivä**, määritetään **Resurssikapasiteetti**-sivun **Näyttöperuste**-kentässä.
4. Kullekin rivin resurssille määritetään kunkin kauden käytettävät tunnit jakson sarakkeisiin.
5. Vaihtoehtoisesti resurssin viikoittaisen kapasiteetin tiedot, kuten alkamis- ja päättymispäivämäärän, voi määrittää valitsemalla **Aseta kapasiteetti** -toiminnon.
6. Täytä **Resurssin kapasiteetti asetuk.**-sivun rivillä tarvittavat kentät.
7. Valitse **Päivitä kapasiteetti** -toiminto. **Resurssikapasiteetti**-sivulle päivitetään annettu kapasiteetti.
8. Sulje sivu.

## <a name="to-set-up-alternate-resource-costs"></a>Vaihtoehtoisten resurssikustannusten määrittäminen

Resurssikortissa määritettyjen kustannusten lisäksi voit määrittää kullekin resurssille vaihtoehtoiset kustannukset. Jos esimerkiksi maksat työntekijälle suurempaa tuntipalkkaa ylityöstä, ylityöpalkalle voi määrittää resurssikustannuksen. Resurssille määritetty vaihtoehtoinen kustannus ohittaa resurssikortissa olevan kustannuksen silloin, kun resurssia käytetään resurssipäiväkirjassa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssit** ja valitse sitten vastaava linkki.  
2. Valitse resurssi, jolle haluat määrittää vähintään yhden vaihtoehtoisen kustannuksen. Valitse sitten **Kustannukset**-toiminto.  
3. Täytä **Resurssikustannukset**-sivun rivillä tarvittavat kentät.  
4. Toista vaihe 3 kaikkien määritettävien vaihtoehtoisten resurssikustannusten kohdalla.

> [!NOTE]
> Voit määrittää kaikki resursseja ja resurssiryhmiä koskevat resurssikustannukset avaamalla **Resurssikustannukset-sivun** ja täyttämällä kentät.

## <a name="to-set-up-alternate-resource-prices"></a>Vaihtoehtoisten resurssihintojen määrittäminen

Resurssikortissa määritetyn hinnan lisäksi voit määrittää kullekin resurssille vaihtoehtoiset hinnat. Vaihtoehtoiset hinnat voivat olla ehdollisia. Ne voivat riippua siitä, minkä projekti- tai työtyypin yhteydessä resurssia käytetään.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssit** ja valitse sitten vastaava linkki.
2. Valitse resurssi, jolle haluat määrittää vähintään yhden vaihtoehtoisen hinnan. Valitse sitten **Hinnat**-toiminto.
3. Täytä **Resurssihinnat**-sivun rivillä tarvittavat kentät.
4. Toista vaihe 3 kaikkien määritettävien vaihtoehtoisten resurssihintojen kohdalla.

## <a name="to-adjust-resource-prices"></a>Resurssihintojen muuttaminen

Jos haluat muuttaa useiden resurssien kustannuksia tai hintoja, voit käyttää eräajoa.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muuta resurssin kustannuksia tai hintoja** ja valitse sitten vastaava linkki.
2. Täytä rivin tarvittavat kentät ja valitse **OK**-painike.

> [!NOTE]  
> Tämä eräajo ei luo tai muuta vaihtoehtoisia kustannuksia tai hintoja resursseille. Se muuttaa vain sen **Muuta kenttää** -kentässä olevan resurssin kortin kentän sisältöä, joka on valittu eräajoon. Muutos tulee resurssien osalta voimaan heti, joten tarkista muutoskertoimet ennen eräajon suorittamista.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Resurssihintojen muutosehdotusten saaminen olemassa olevien vaihtoehtoisten hintojen perusteella

Jos olet jo määrittänyt vaihtoehtoisia resurssihintoja joillekin resursseille, voit käyttää eräajoa useiden vaihtoehtoisten resurssihintojen määrittämiseen.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssin hinnan muutokset** ja valitse sitten vastaava linkki.
2. Valitse **Ehdota res.hintamuut. (hinta)** -toiminto ja täytä tarvittavat kentät.
3. Valitse **OK**-painike.  
4. Kun eräajo on päättynyt, eräajon tulokset näkyvät **Resurssin hinnan muutokset** -sivulla.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Resurssihintojen muutosehdotusten saaminen vakiohintojen perusteella

Jos haluat määrittää useita vaihtoehtoisia resurssihintoja resurssikorttien vakiohintojen perusteella, voit käyttää eräajoa.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssin hinnan muutokset** ja valitse sitten vastaava linkki.
2. Valitse **Ehdota res.hintamuut. (res.)** -toiminto ja täytä tarvittavat kentät.  
3. Valitse **OK**-painike.  
4. Kun eräajo on päättynyt, voit katsoa eräajon tulokset avaamalla **Resurssin hinnan muutokset** -sivun.

## <a name="see-also"></a>Katso myös

[Projektinhallinnan määrittäminen](projects-setup-projects.md)  
[Projektien hallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
