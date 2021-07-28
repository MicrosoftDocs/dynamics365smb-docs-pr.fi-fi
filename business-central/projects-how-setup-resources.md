---
title: Resurssin kustannusten, hintojen ja kapasiteetin määrittäminen| Microsoft Docs
description: Voit käyttää resursseja ja helpottaa projektinhallintaa määrittämällä yksittäisten resurssien tai resurssiryhmien kustannukset ja hinnat sekä resurssikapasiteetin.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: eb0d6f0ebe08abfb4b6f769f1bdbff1f02bc677f
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6439793"
---
# <a name="set-up-resources"></a>Resurssien määrittäminen
Jotta voit hallita resurssitoimintoja tarkasti, sinun on määritettävä resurssit sekä niihin liittyvät kustannukset ja hinnat. Projekteihin liittyvät hinnat, alennukset ja kustannustekijäsäännöt määritetään projektikortissa. Voit määrittää kustannukset ja hinnat yksittäisille resursseille, resurssiryhmille tai kaikille yrityksen käytettävissä oleville resursseille.

Kun resursseja käytetään tai myydään projektissa, niihin liittyvät hinnat ja kustannukset haetaan määrittämistäsi tiedoista.

Tuntikohtainen oletussumma määritetään resurssin luomisen yhteydessä. Jos käytät projektissa esimerkiksi tiettyä konetta viisi tuntia, projekti lasketaan tuntikohtaisen summan perusteella.

> [!NOTE]
> Voit ostaa ulkoisia resursseja, kuten esimerkiksi laskuttaa toimittajaa tehdystä työstä. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).<br /><br />
> Tällaisessa tapauksessa on suositeltavaa nimetä tai ryhmitellä ulkoiset resurssit niiden tarkoituksen mukaisesti, jotta niitä ei sekoiteta sisäisiin resursseihin.

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
Resurssien kapasiteetti on määritettävä työkalenteriin jaksoittaisena saatavuusaikana, jotta voit laskea, kuinka kauan resurssia voi käyttää työssä. Tätä määritystä käytetään silloin, kun täytät työn suunnittelurivit, jotka sisältävät resurssin. Lisätietoja on kohdassa [Projektien luominen](projects-how-create-jobs.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssit** ja valitse sitten vastaava linkki.
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

**Huomautus**. Voit määrittää kaikki resursseja ja resurssiryhmiä koskevia resurssikustannuksia avaamalla **Resurssikustannukset**-sivun ja täyttämällä sen kentät.

## <a name="to-set-up-alternate-resource-prices"></a>Vaihtoehtoisten resurssihintojen määrittäminen
Resurssikortissa määritetyn hinnan lisäksi voit määrittää kullekin resurssille vaihtoehtoiset hinnat. Vaihtoehtoiset hinnat voivat olla ehdollisia. Ne voivat riippua siitä, minkä projekti- tai työtyypin yhteydessä resurssia käytetään.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssit** ja valitse sitten vastaava linkki.
2. Valitse resurssi, jolle haluat määrittää vähintään yhden vaihtoehtoisen hinnan. Valitse sitten **Hinnat**-toiminto.
3. Täytä **Resurssihinnat**-sivun rivillä tarvittavat kentät.
4. Toista vaihe 3 kaikkien määritettävien vaihtoehtoisten resurssihintojen kohdalla.

## <a name="see-also"></a>Katso myös
[Projektinhallinnan määrittäminen](projects-setup-projects.md)  
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]