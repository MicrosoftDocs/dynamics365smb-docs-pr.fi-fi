---
title: Nimikkeiden kokoaminen | Microsoft Docs
description: Jos nimikkeen kortin **Täydennysjärjestelmä**-kenttä sisältää **kokoonpanon**, nimikkeen toimituksen oletustapa on koota nimike määritetyistä komponenteista ja mahdollisesti määritetyn resurssin toimesta.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 12/17/2018
ms.author: sgroespe
ms.openlocfilehash: 10b8021bd688e3f699a73d6a95f511b9a26b8341
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795835"
---
# <a name="assemble-items"></a>Kokoa nimikkeet
Jos nimikkeen kortin **Täydennysjärjestelmä**-kenttä sisältää **kokoonpanon**, nimikkeen toimituksen oletustapa on koota nimike määritetyistä komponenteista ja mahdollisesti määritetyn resurssin toimesta.  

Tämänkaltaiseen kokoonpanon nimikkeeseen kuuluvat osat ja resurssit tulee määritellä kokoonpanon tuoterakenteessa. Lisätietoja on kohdassa [Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md).  

Kokoonpanon nimikkeitä voidaan määrittää kahdelle eri kokoonpanoprosessille:  

-   Kokoonpano varastoon.  
-   Kokoonpano tilausta varten.  

Käytät yleensä **Kokoonpano varastoon** nimikkeille, jotka haluat koota ennen myyntiä, kuten valmistauta kampanjapakettiin ja pitää varastossa, kunnes ne on tilattu. Nämä kohteet ovat yleensä vakiokohteita, kuten pakattuja sarjoja, joita ei tarjota asiakkaalle heidän pyyntöjensä mukauttamiseksi.  

Käytät yleensä **Kokoonpano tilausta varten** nimikkeille, joita et halua varastoida, koska oletat mukauttavasti ne asiakkaan pyyntöjä astaaviksi tai koska haluat pienentää varastokustannuksia toimittamalla juuri ajoissa. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).  

Lisätietoja kokoonpanon nimikkeen määrittämisestä on kohdassa [Tietoja Kokoonpano tilausta varten- ja Kokoonpano varastoon -toiminnoista](assembly-assemble-to-order-or-assemble-to-stock.md).  

Nämä asetukset ovat oletusasetuksia, jotka hallitsevat sitä, miten myynnin ja kokoonpanontilauksen rivejä aluksi käsitellään. Voit poiketa näistä oletuksista ja toimittaa kokoonpanon nimikkeen kaikkein parhaalla tavalla myyntejä käsiteltäessä. Lisätietoja on kohdissa [Varastonimikkeiden myyminen kokoonpano tilausta varten -virroissa](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) ja [Kokoonpano tilausta varten -nimikkeiden ja varastonimikkeiden myyminen yhdessä](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Kokoonpanon komponentit käsitellään tietyllä tavalla fyysisen varastoinnin perusmäärityksissä. Lisätietoja on ohjeaiheen [Nimikkeiden poiminta varaston poiminnoissa](warehouse-how-to-pick-items-with-inventory-picks.md) kohdassa Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa.   

Tässä toimenpiteessä luot kokoonpanotilauksen varastoon (eli ilman myyntitilausta) koottavia nimikkeitä varten ja käsittelet tilausta. Vaiheita ovat kokoonpanotilauksen käynnistäminen, mahdollisten osien saatavuusongelmien käsitteleminen ja osittainen kokoonpanon nimikkeen tuotoksen kirjaaminen.

## <a name="to-assemble-an-item"></a>Kokoa nimike  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kokoonpanotilaukset** ja valitse sitten liittyvä linkki.  
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
7.  Määritä **Nimike**- tai **Resurssi**tyyppisten kokoonpanotilausrivien **Kulutettava määrä** -kentässä, miten monta yksikköä haluat kirjata kulutettuna, kun seuraavan kerran kirjaat kokoonpanotilauksen.
8.  Kun olet valmis tekemään osittaisen tai täysimääräisen kirjauksen, valitse **Kirjaat**-toiminto.  

    > [!NOTE]  
    >  Jos jollakin kokoonpanorivillä on vielä varoituksia, kirjaus on estetty. Näkyviin tulee sanoma siitä, mitkä komponentit eivät ole varastossa.  

Kun kirjaus on onnistunut, kokoonpanon nimike kirjatataan sijaintikoodiin ja mahdolliseen varastopaikkakoodiin, jotka on määritetty kokoonpano tilauksessa. Jos kokoonpanotilaus on luotu manuaalisesti, sijainti voidaan kopioida **Tilausten oletussijainti** -asetuskentästä Jos kyseessä on kokoonpano tilausta varten -virrat, sijaintikoodi voidaan kopioida myyntitilausriviltä.  

## <a name="see-also"></a>Katso myös
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
