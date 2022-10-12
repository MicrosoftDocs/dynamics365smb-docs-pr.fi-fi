---
title: Kokoa nimikkeet
description: Jos nimikkeen kortin Täydennysjärjestelmä-kenttä sisältää kokoonpanon, nimikkeen toimituksen oletustapa on koota nimike määritetyistä komponenteista.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: e9d53a6369e2955e0e097471e70cb83438540539
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607043"
---
# <a name="assemble-items"></a>Kokoa nimikkeet

Jos nimikkeen kortin **Täydennysjärjestelmä**-kenttä sisältää **kokoonpanon**, nimikkeen toimituksen oletustapa on koota nimike määritetyistä komponenteista ja mahdollisesti määritetyn resurssin toimesta.  

Tämänkaltaiseen kokoonpanon nimikkeeseen kuuluvat osat ja resurssit tulee määritellä kokoonpanon tuoterakenteessa. Lisätietoja on kohdassa [Kokoonpanon tuoterakenteiden käyttäminen](assembly-how-work-assembly-boms.md).

Kokoonpanon nimikkeitä voidaan määrittää kahdelle eri kokoonpanoprosessille:  

- Kokoonpano varastoon.  
- Kokoonpano tilausta varten.  

Käytät yleensä **Kokoonpano varastoon** nimikkeille, jotka haluat koota ennen myyntiä, kuten valmistauta kampanjapakettiin ja pitää varastossa, kunnes ne on tilattu. Nämä kohteet ovat yleensä vakiokohteita, kuten pakattuja sarjoja, joita ei tarjota asiakkaalle heidän pyyntöjensä mukauttamiseksi.  

Käytät yleensä **Kokoonpano tilausta varten** nimikkeille, joita et halua varastoida, koska oletat mukauttavasti ne asiakkaan pyyntöjä astaaviksi tai koska haluat pienentää varastokustannuksia toimittamalla juuri ajoissa. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).  

Lisätietoja kokoonpanon nimikkeen määrittämisestä on kohdassa [Tietoja Kokoonpano tilausta varten- ja Kokoonpano varastoon -toiminnoista](assembly-assemble-to-order-or-assemble-to-stock.md).  

Nämä asetukset ovat oletusasetuksia, jotka hallitsevat sitä, miten myynnin ja kokoonpanontilauksen rivejä aluksi käsitellään. Voit poiketa näistä oletuksista ja toimittaa kokoonpanon nimikkeen kaikkein parhaalla tavalla myyntejä käsiteltäessä. Lisätietoja on kohdissa [Varastonimikkeiden myyminen kokoonpano tilausta varten -virroissa](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) ja [Kokoonpano tilausta varten -nimikkeiden ja varastonimikkeiden myyminen yhdessä](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Kokoonpanon komponentit käsitellään tietyllä tavalla fyysisen varastoinnin perusmäärityksissä. Lisätietoja on ohjeaiheen [Nimikkeiden poiminta varaston poiminnoissa](warehouse-how-to-pick-items-with-inventory-picks.md) kohdassa Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa.   

Tässä toimenpiteessä luot kokoonpanotilauksen varastoon (eli ilman myyntitilausta) koottavia nimikkeitä varten ja käsittelet tilausta. Vaiheita ovat kokoonpanotilauksen käynnistäminen, mahdollisten osien saatavuusongelmien käsitteleminen ja osittainen kokoonpanon nimikkeen tuotoksen kirjaaminen.

## <a name="to-assemble-an-item"></a>Kokoa nimike

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kokoonpanotilaukset** ja valitse sitten vastaava linkki.  
2.  Valitse **Uusi**-toiminto. **Uusi kokoonpanotilaus**-sivu avautuu.  
3.  Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Valitse **Nimikenro**-kentässä kokoonpanon nimike, jota haluat käsitellä. Kenttä on suodatettu näyttämään vain ne kohteet, jotka on määritetty kokoonpanolle, joka tarkoittaa sitä, että niille on määritetty kokoonpanon tuoterakenne.  
5.  Määritä **Määrä**-kentässä, miten monta nimikkeen yksikköä haluat koottavan.  

    > [!NOTE]  
    >  Jos vähintään yksi komponentti ei ole saatavana syötetyn kokoonpanon nimikkeen määrän täyttämiseksi määritettynä eräpäivänä, **Kokoonpanon saatavuus** -sivu avautuu automaattisesti ja näyttää niiden kokoonpanon nimikkeiden yksityiskohtaiset tiedot, jotka ovat käytettävissä kokoonpanoa varten komponentin saatavuuden perusteella. Lisätietoja on kohdassa [Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md). Kun suljet sivun, kokoonpanotilaus luodaan liittyvien komponenttirivien saatavuushälytyksillä.  

    Kokoonpanotilauksen riveille täytetään automaattisesti kokoonpanon tuoterakenteen sisältö, sekä rivien määrät kokoonpanotilauksen otsikon mukaisesti.  

    > [!NOTE]  
    >  Jos **Kokoonpanon saatavuus** -sivu avautui kokoonpanotilauksen otsikon täyttämisen yhteydessä, kaikkien kokoonpanotilausrivien **Käytettävissä oleva varoitus** -kentässä on arvo **Kyllä** ja linkki yksityiskohtaisiin saatavuustietoihin. Lisätietoja on kohdassa Tarkasta saatavuus. Voit ratkaista osan saatavuusongelman lykkäämällä aloituspäivämäärää, korvaamalla osan toisella nimikkeellä tai valitsemalla käytettävissä olevan korvaavan nimikkeen, jos sellainen on määritetty.  

6.  Määritä **Kokoonpantava määrä** -kentässä, miten monta kokoonpanon nimikkeen yksikköä haluat kirjata tuotoksena, kun seuraavan kerran kirjaat kokoonpanotilauksen. Tämä määrä voi olla alhaisempi kuin **Määrä**-kentän arvo, niin että se vastaa osittaista tuotoksen kirjausta.  

    > [!NOTE]  
    >  Varmista, että komponentin kulutuksen kirjaus vastaa nimikkeen kokoonpanon tuotoksen kirjausta, kokoonpanotilauksen määräkentät säätävät automaattisesti arvon, jonka syötät **Kokoonpantava määrä** -kenttään.  
7.  Määritä **Nimike**- tai **Resurssi** tyyppisten kokoonpanotilausrivien **Kulutettava määrä** -kentässä, miten monta yksikköä haluat kirjata kulutettuna, kun seuraavan kerran kirjaat kokoonpanotilauksen.
8.  Kun olet valmis tekemään osittaisen tai täysimääräisen kirjauksen, valitse **Kirjaat**-toiminto.  

    > [!NOTE]  
    >  Jos jollakin kokoonpanorivillä on vielä varoituksia, kirjaus on estetty. Näkyviin tulee sanoma siitä, mitkä komponentit eivät ole varastossa.  

Kun kirjaus on onnistunut, kokoonpanon nimike kirjatataan sijaintikoodiin ja mahdolliseen varastopaikkakoodiin, jotka on määritetty kokoonpano tilauksessa. Jos kokoonpanotilaus on luotu manuaalisesti, sijainti voidaan kopioida **Tilausten oletussijainti** -asetuskentästä Jos kyseessä on kokoonpano tilausta varten -virrat, sijaintikoodi voidaan kopioida myyntitilausriviltä.  

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Kokoonpanon tuoterakenteiden käyttäminen](assembly-how-work-assembly-boms.md)  
[Varasto](inventory-manage-inventory.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
