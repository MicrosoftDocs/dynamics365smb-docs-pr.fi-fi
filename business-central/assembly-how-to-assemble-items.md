---
title: Kokoa nimikkeet
description: Tutustu Business Centralin Kokoonpano tilausta varten- ja Kokoonpano varastoon -prosesseihin
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: kit, kitting
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.custom: bap-template
ms.openlocfilehash: 35d75808f0d2a0212396151dd2a7a2438dfc7fe5
ms.sourcegitcommit: 61f22aeede684f0ae772353ede6530ff03ff2f90
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/24/2022
ms.locfileid: "9804497"
---
# <a name="assemble-items" /><a name="assemble-items"></a>Kokoa nimikkeet

Jos nimikkeen kortin **Täydennysjärjestelmä**-kenttä sisältää **kokoonpanon**, nimikkeen toimituksen oletustapa on koota nimike kokoonpanon tuoterakenteen mukaan ja mahdollisesti tietyn resurssin toimesta. Lisätietoja on kohdassa [Kokoonpanon tuoterakenteiden käyttäminen](assembly-how-work-assembly-boms.md). Lisätietoja kokoonpanon nimikkeen määrittämisestä on kohdassa [Tietoja Kokoonpano tilausta varten- ja Kokoonpano varastoon -toiminnoista](assembly-assemble-to-order-or-assemble-to-stock.md).

Voit määrittää kokoonpanon nimikkeitä kahdelle kokoonpanoprosessille.

|Käsittele  |Kuvaus  |
|---------|---------|
|Kokoonpano varastoon     | Nimikkeet, jotka kokoat ja varastoit tulevaa myyntiä varten. Ne voivat olla esimerkiksi paketteja tulevaa myyntikampanjaa varten. Nimikkeitä ei liitetä myyntitilaukseen ainakaan vielä. Tavallisesti näitä nimikkeitä ei mukauteta asiakkaiden toiveiden mukaan.        |
|Kokoonpano tilausta varten     | Nimikkeet, joita et halua varastoida. Saatat esimerkiksi haluta mukauttaa nimikkeitä asiakkaan toiveiden mukaan tai vähentää varastointikuluja. |
  
Tämä artikkeli kuvaa Kokoonpano varastoon -prosessin vakioasetukset. Saatavilla saattaa kuitenkin olla muita tapoja, jotka soveltuvat paremmin yrityksellesi. Lisätietoja on kohdissa [Varastonimikkeiden myyminen kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) ja [Kokoonpano tilausta varten -nimikkeiden ja varastonimikkeiden myyminen yhdessä](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Kokoonpanon komponentit käsitellään tietyllä tavalla fyysisen varastoinnin perusmäärityksissä. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

## <a name="to-assemble-an-item-to-stock" /><a name="to-assemble-an-item-to-stock"></a>Nimikkeen kokoaminen varastoon

Noudata näitä ohjeita kootaksesi nimikkeen varasoton. Lisätietoja Kokoonpano tilausta varten -prosessista on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kokoonpanotilaukset** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto. **Uusi kokoonpanotilaus**-sivu avautuu.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **Nimikenro**-kentästä nimike, jonka haluat koota. Voit valita nimikkeitä, jotka on määritetty kokoamista varten ja joilla on kokoonpanon tuoterakenne, tai nimikkeitä, joilla ei ole kokoonpanon tuoterakennetta. Jälkimmäinen vaihtoehto on hyödyllinen suunnittelemattomille kokoonpanoille tai skenaarioille, kun haluat käyttää nimikkeiden uudelleenluokittelua ja seurata kustannuksia.  
5. Määritä **Määrä**-kentässä, miten monta nimikkeen yksikköä haluat koottavan.  

    > [!NOTE]  
    >  Jos yksi tai useampi komponenteista ei ole käytettävissä määrän täyttämiseksi eräpäivänä, **Kokoonpanon saatavuus** -sivu avautuu. Sivulla näytetään, kuinka monta kokoonpanon nimikettä voidaan koota komponenttien saatavuuden perusteella. Lisätietoja on kohdassa [Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md). Kun suljet sivun, järjestelmä luo kokoonpanotilauksen, jossa asiaankuuluvien komponenttien riveillä näytetään saatavuutta koskevia hälytyksiä.  

    Rivit sisältävät kokoonpanon tuoterakenteen sisällön ja määritetyt määrät.  

    > [!NOTE]  
    >  Jos **Kokoonpanon saatavuus** -sivu avautui kokoonpanotilauksen otsikon täyttämisen yhteydessä, kaikkien kokoonpanotilausrivien **Käytettävissä oleva varoitus** -kentässä on arvo **Kyllä** ja linkki yksityiskohtaisiin saatavuustietoihin. <!--check whether this field help is useful For more information, see Check Availability.--> Voit ratkaista komponentin saatavuusongelman:

    > * lykkäämällä alkamispäivää
    > * korvaamalla komponentin toisella nimikkeellä
    > * valitsemalla saatavilla olevan korvaavan vaihtoehdon, jos sellainen on määritetty.  

6. Määritä **Kokoonpantava määrä** -kentässä, miten monta kokoonpanon nimikkeen yksikköä haluat kirjata tuotoksena, kun seuraavan kerran kirjaat kokoonpanotilauksen. Tämä määrä voi olla alhaisempi kuin **Määrä**-kentän arvo, niin että se vastaa osittaista tuotoksen kirjausta.  

    > [!NOTE]  
    >  Varmista, että komponentin kulutuksen kirjaus vastaa nimikkeen kokoonpanon tuotoksen kirjausta, kokoonpanotilauksen määräkentät säätävät automaattisesti arvon, jonka syötät **Kokoonpantava määrä** -kenttään.  
7. Määritä **Nimike**- tai **Resurssi** tyyppisten kokoonpanotilausrivien **Kulutettava määrä** -kentässä, miten monta yksikköä haluat kirjata kulutettuna, kun seuraavan kerran kirjaat kokoonpanotilauksen.
8. Kun olet valmis tekemään osittaisen tai täysimääräisen kirjauksen, valitse **Kirjaat**-toiminto.  

    > [!NOTE]  
    >  Jos kokoonpanotilauksen riveillä on vielä varoituksia, et voi kirjata tilausta. Viesti näyttää komponentin tai komponentit, jotka eivät ole varastossa.  

Kun kirjaus on onnistunut, kokoonpanon nimike kirjatataan sijaintikoodiin ja mahdolliseen varastopaikkakoodiin, jotka on määritetty kokoonpano tilauksessa. Jos kokoonpanotilaus on luotu manuaalisesti, sijainti voidaan kopioida **Tilausten oletussijainti** -asetuskentästä Jos kyseessä on kokoonpano tilausta varten -virrat, sijaintikoodi voidaan kopioida myyntitilausriviltä.  

## <a name="see-related-microsoft-training" /><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also" /><a name="see-also"></a>Katso myös

[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Kokoonpanon tuoterakenteiden käyttäminen](assembly-how-work-assembly-boms.md)  
[Varasto](inventory-manage-inventory.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
