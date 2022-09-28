---
title: Varastopaikkojen luominen
description: Luo samankaltaisten varastopaikkojen ryhmiä varastopaikan luontityökirjaan, luo varastopaikkoja yksitellen sijaintikortille tai automaattisesti varastopaikan luontityökirjaan.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7368, 7369, 7370, 7371, 7372, 7373
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 217b5c66e61e88917fcfb7bf960633faa38b381e
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533722"
---
# <a name="create-bins"></a>Varastopaikkojen luominen

Tehokkain tapa luoda fyysisen varaston varastopaikkoja on luoda samankaltaisten varastopaikkojen ryhmiä varastopaikan luontityökirjassa, mutta varastopaikkoja voi luoda myös yksittäin sijainnin kortista. Voit luoda varastopaikkoja myös automaattisesti **Var.paikan luontityökirja** -sivulla.  

## <a name="to-create-a-bin-from-the-location-card"></a>Varastopaikan luonti sijaintikortista

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
2.  Valitse ensin sijainti, josta haluat luoda varastopaikan, ja sitten **Varastopaikat**-toiminto.  
3. Valitse **Uusi**-toiminto.
4. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="the-dedicated-field"></a>Erityinen-kenttä

**Varastopaikat**-sivun **Erityinen**-kenttä määrittää, että varastopaikan määrät suojataan poiminnalta muuhun kysyntään. Erityisvarastopaikoissa olevat määrät voidaan kuitenkin edelleen varata. Näin ollen erityisvarastopaikkojen määrät sisällytetään **Varaus**-sivun **Saatavilla oleva kokonaismäärä** -kenttään.

Erillisen varastopaikan tekemisen tuloksena on samantapainen toiminta perusvarastoinnissa kuin varastopaikkatyyppien käyttö, joka on mahdollista vain laajennetussa varastoinnissa. Lisätietoja on kohdassa [Varastopaikkojen määrittäminen](warehouse-how-to-set-up-bin-types.md).

### <a name="example"></a>Esimerkki

Tuotantosolu on määritetty **Tuotannon valmisteluvarastopaikkakoodi** -kentän varastopaikkakoodilla. Oletusvarastopaikkakoodilla varustetut tuotantotilauksen komponenttirivit vaativat, että eteenpäin siirretyt komponentit sijoitetaan niihin. Kunnes kyseisen varastopaikan komponentit on kulutettu loppuun, tästä varastopaikasta voidaan poimia tai kuluttaa muiden komponenttien kysynnän mukaisesti, koska varastopaikat ovat yhä saatavana olevaa varastopaikan sisältöä. Jotta varmistat, että varastopaikan sisältö on käytettävissä vain komponenttitarpeeseen, joka käyttää kyseistä tuotannon valmisteluvarastopaikkaa, sinun on valittava **Erityinen**-kenttä kyseisen varastopaikkakoodin rivillä.

> [!Caution]
> Erikoisvarastopaikoissa olevat nimikkeet eivät ole suojattuja, kun ne on kerätty ja kulutettu tuotanto- tai kokoonpanokomponentteina **Varaston poiminta** -sivun kautta. Lisätietoja on kohdassa [Tuotanto- tai kokoonpanopoiminta perusvarastointimäärityksissä](warehouse-how-to-pick-for-production.md).

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Varastopaikkojen luominen yksittäin varastopaikan luontityökirjassa

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Var.paikan luontityökirja** ja valitse sitten vastaava linkki.  
2.  Täytä jokaisella rivillä kentät, jotka tarvitaan luotavien varastopaikkojen nimeämiseen ja kuvailemiseen.  
3.  Valitse **Luo varastopaikat** -toiminto.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Varastopaikkojen muodostaminen automaattisesti varastopaikkojen luontityökirjassa

Ennen kuin aloitat varastopaikkojen automaattisen luonnin, sinun on päätettävä toimintojesi kannalta olennainen varastopaikkojen tyyppi ja nimikkeiden kätevin kulku fyysisen varaston rakenteiden läpi.  

> [!NOTE]  
> Kun varastopaikkaa on käytetty, sitä ei voi poistaa kuin tyhjänä. Mutta jos haluat joskus käyttää muuta varastopaikan nimeämisjärjestelmää, voit käyttää uudelleenluokittelupäiväkirjaa "siirtääksesi" nimikkeet uuteen varastopaikkajärjestelmään. Tämä prosessi on kuitenkin manuaalinen ja se vie aikaa, joten parasta on määrittää varastopaikat oikein alusta lähtien.  

Voit käyttää **Var.paikan luontityökirja** -sivua, jos sinut on määritetty varastotyöntekijäksi varastopaikkojen sijaintipaikkaan. Lisätietoja on kohdassa [Varastotyöntekijöiden määrittäminen](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Var.paikan luontityökirja** ja valitse sitten vastaava linkki.  
2.  Valitse **Laske varastopaikat** -toiminto.
3. Valitse **Laske varastopaikat** -sivun **Varastopaikkamallin koodi** -kentässä varastopaikkamalli, jota haluat käyttää luotavien varastopaikkojen mallina.
4.  Täytä kuvaus varastopaikoille, joita olet luomassa.  
5.  Luo varastopaikkakoodit täyttämällä **Numerosta**- ja **Numeroon**-kentät sivulla näkyvissä kolmessa luokassa: **Hylly**, **Osio** ja **Taso**. Varastopaikkakoodi voi sisältää enintään 20 merkkiä.  

    > [!NOTE]  
    >  Merkkien lukumäärä, jonka olet syöttänyt kolmeen luokkaan kummankin kentän osalta (esimerkiksi kolmeen **Numerosta**-kenttiin syöttämäsi merkit), sekä kenttien mahdolliset erottimet voivat olla yhteensä korkeintaan 20 merkkiä.  

     Voit käyttää koodissa kirjaimia yksilöivänä yhdistelmänä, mutta kirjaimen täytyy olla sama **Numerosta**- ja **Numeroon**-kentät -kentät. Voit esimerkiksi määritellä hyllyä koskevan koodin osaksi **Numerosta A01** ja **Numeroon A10**. Sovellusta ei ole määritetty luomaan koodeja, joissa on kirjainsarjoja, kuten A01–F05.  

6.  Jos haluat jonkin merkin, esimerkiksi yhdysmerkin, erottavan luokkakenttiä, jotka on määritelty osaksi varastopaikkakoodia, täytä **Kenttäerotin**-kenttään tämä merkki.  
7.  Jos et halua sovelluksen luovan riviä varastopaikalle, jos se on jo luotu, valitse **Tarkasta olemassa olevat var.paikat** -kenttä.  
8. Sen jälkeen kun olet täyttänyt kaikki kentät, paina **OK**-painiketta.

    Sovellus luo työkirjaan rivin kullekin varastopaikalle. Voit nyt poistaa joitain varastopaikoista, jos sinulla on esimerkiksi hylly, jossa on käytävä parin osion kahden ensimmäisen tason välillä.  

9. Kun olet poistanut kaikki tarpeettomat varastopaikat, valitse **Luo varastopaikat** -toiminto, jolloin sovellus luo työkirjan kullekin riville varastopaikan.  

Prosessi toistetaan toisen varastopaikkasarjan osalta, siihen asti kun fyysiseen varastoon on luotu kaikki varastopaikat.  

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/create-new-bins/)

## <a name="see-also"></a>Katso myös

[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
