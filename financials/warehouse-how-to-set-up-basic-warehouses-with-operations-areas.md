---
title: "Fyysisten perusvarastojen ja toimintoalueiden määrittäminen | Microsoft Docs"
description: "Jos sellaisen fyysisen varaston perusmäärityksissä, jonka sijainnit käyttävät **Var.paikka pakollinen** -asetuskenttää ja mahdollisesti myös **Vaadi poiminta**- ja **Vaadi hyllytys** -asetuskenttää, on sisäisiä toimintoalueita, kuten tuotanto tai kokoonpano, sisäisten toimintoalueiden fyysisen varastoinnin toimintojen tallentamisessa on käytettävä kolmea fyysisen perusvarastoinnin asiakirjoja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 31f057f862b72cd21ecb2c1fb59674c6485a960d
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-basic-warehouses-with-operations-areas"></a>Fyysisten perusvarastojen ja toimintoalueiden määrittäminen
Jos sellaisen fyysisen varaston perusmäärityksissä, jonka sijainnit käyttävät **Var.paikka pakollinen** -asetuskenttää ja mahdollisesti myös **Vaadi poiminta**- ja **Vaadi hyllytys** -asetuskenttää, on sisäisiä toimintoalueita, kuten tuotanto tai kokoonpano, sisäisten toimintoalueiden fyysisen varastoinnin toimintojen tallentamisessa on käytettävä seuraavia fyysisen varastoinnin perusasiakirjoja:  

- **Varastonsiirto**-ikkuna.  
- **Varaston poiminta** -ikkuna.  
- **Varaston hyllytys** -ikkuna.

> [!NOTE]
> Vaikka asetusten nimenä on **Vaadi poiminta** ja **Vaadi hyllytys**, voit silti kirjata vastaanottoja ja toimituksia suoraan lähdeasiakirjoista sijainneissa, joissa olet valinnut nämä valintaruudut.  

Käyttääksesi näitä ikkunoita sisäisillä toiminnoilla, kuten osien poiminta ja siirto tuotantoon, sinun täytyy tehdä joitakin tai kaikki asetusvaiheet sen mukaan, kuinka paljon ohjausta tarvitset:  

- Ota käyttöön varaston poiminta-, siirto- ja hyllytysasiakirjat.  
- Määritä oletusarvoiset varastopaikan rakenteet osille ja valmiille nimikkeille, jotka tulevat ja lähtevät toiminnan resursseista.  
- Tee lähde- ja kohdevarastopaikat, jotka on varattu tietyille työvaiheresursseille, jotta estät nimikkeiden poiminnan lähteviä asiakirjoja varten.

Varastopaikkakoodit, jotka on määritetty sijaintikortteihin, määrittävät oletusarvoisen varaston työnkulun tietyille toiminnoille, kuten osille kokoonpano-osastolla. Lisätoiminnot varmistavat, että tiettyyn varastopaikkaan sijoitettavat nimikkeet eivät ole siirrettävissä tai poimittavissa muihin toimiin. Lisätietoja on kohdassa Eritysvarastopaikkojen luominen.

Seuraavat toimet perustuvat perusvarastoinnin aktiviteettien määrittämiseen tuotantoalueella. Vaiheet ovat samankaltaisia muille toiminta-alueille, kuten kokoonpanolle, huoltohallinnolle ja töille.  

> [!NOTE]  
>  Seuraavassa toimenpiteessä sijaintikorttien **Var.paikka pakollinen** -asetuskenttä valitaan ennakkoehtona, koska sitä pidetään fyysisen varastoinnin hallinnan perustana kaikilla tasoilla.  

## <a name="to-enable-inventory-documents-for-internal-operation-activities"></a>Ota käyttöön sisäisten toimintojen varaston asiakirjat  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sijainnit** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa määritettävä sijaintikortti.  
3.  Valitse **Fyysinen varasto** -pikavälilehdessä **Vaadi hyllytys** -valintaruutu. Se osoittaa, että kun varastopaikkakoodin sisältävä lähtevä tai sisäinen lähdeasiakirja vapautetaan, varaston hyllytys- tai varastosiirtoasiakirja voidaan luoda.  
4.  Valitse **Vaadi poiminta** -valintaruutu. Se osoittaa, että kun varastopaikkakoodin sisältävä lähtevä tai sisäinen lähdeasiakirja luodaan, myös varaston poiminta- tai varastosiirtoasiakirja on luotava.  

## <a name="to-define-a-default-bin-structure-in-the-production-area"></a>Varastopaikan oletusrakenteen määrittäminen tuotantoalueella  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sijainnit** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa määritettävä sijainti.  
3.  Anna **Varastopaikat**-pikavälilehden **Avoin tuotannon var.paik.koodi** -kentässä tuotantoalueen sen varastopaikan koodi, jossa on paljon komponentteja, joita koneenkäyttäjä voi kuluttaa pyytämättä varastoinin toimintoa niiden tuomiseksi varastopaikkaan. Tähän varastopaikkaan sijoitetuille nimikkeille määritetään yleensä automaattinen kirjaus tai materiaalinotto. Tämä tarkoittaa, että **Materiaalinottotapa**-kenttä sisältää arvon **Eteenpäin** tai **Taaksepäin**.  
4. Anna **Tuotannon valm.var.paik.koodi** -kentässä tuotantoalueen sen varastopaikan koodi, johon tässä sijainnissa tuotantoon poimitut osat oletuksena sijoitetaan ennen niiden kuluttamista. Tähän varastopaikkaan sijoitetuille nimikkeille määritetään yleensä manuaalinen kulutuskirjaus. Tämä tarkoittaa, että **Materiaalinottotapa**-kenttä sisältää arvon **Manuaalinen** tai **Poiminta + Eteenpäin** tai **Poiminta + Taaksepäin** fyysisen varastoinnin poiminnoille ja varastosiirroille.  

    > [!NOTE]  
    >  Kun käytät varaston poimintoja **Varastopaikkakoodi** -kenttä tuotantotilauksen komponentin rivinumero määrittää*ota* -varastopaikan, josta osat vähenevät, kun kulutus kirjataan. Kun käytät varaston siirtotapahtumia, tuotantotilauksen komponenttirivien **Varastopaikkakoodi**-kenttä määrittää toiminta-alueen *paikka*-varastopaikan, johon varastotyöntekijän on sijoitettava komponentit.  

5. Anna **Varastopaikat**-pikavälilehdeb **Valm. tuot.nim. var.paik.koodi** -kentässä tuotantoalueen sen varastopaikan koodi, josta lopulliset nimikkeet oletusasetuksena otetaan, kun prosessiin liittyy varastoinnin toiminto. Fyysisen varastoinnin perusmäärityksissä toiminto kirjataan varaston hyllytyksenä tai varastosiirtona.  

Nyt oletusvarastopaikkakoodilla varustetut tuotantotilauksen komponenttirivit vaativat, että eteenpäin siirretyt komponentit sijoitetaan niihin. Kunnes kyseisen varastopaikan komponentit on kulutettu loppuun, tästä varastopaikasta voidaan poimia tai kuluttaa muiden komponenttien kysynnän mukaisesti, koska varastopaikat ovat yhä saatavana olevaa varastopaikan sisältöä. Jotta varmistat, että varastopaikan sisältö on käytettävissä vain komponenttitarpeeseen, joka käyttää kyseistä tuotannon valmisteluvarastopaikkaa, sinun on valittava **Erityinen**-kenttä kyseisen varastopaikkakoodin rivillä **Varastopaikat**-ikkunassa, jonka avaat sijaintikortista.

Tämä työnkulkukaavio näyttää, miten tuotantotilauksen osarivien**Varastopaikkakoodi**-kenttä täytetään asetusten mukaisesti.  

![Varastopaikkojen vuokaavio](media/binflow.png "BinFlow")    

## <a name="to-define-a-default-bin-structure-in-the-assembly-area"></a>Varastopaikan oletusrakenten määrittäminen kokoonpanoalueella
Kokoonpanotilausten osia ei voi poimia tai kirjata varastopoiminnan kanssa. Käytä sen sijaan **Varaston siirto** -ikkunaa. Lisätietoja on kohdassa [Komponenttien siirtäminen fyysisen perusvarastoinnin toiminta-alueelle](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Kun poiminnan ja toimituksen myyntirivin määriä kootaan tilaukseen, varaston poimintarivejä luotaessa on noudatettava tiettyjä sääntöjä. Lisätietoja on ohjeaiheen [Nimikkeiden poiminta varaston poiminnoissa](warehouse-how-to-pick-items-with-inventory-picks.md) kohdassa Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa.

Lisätietoja on kohdassa [Kokoonpanon hallinta](assembly-assemble-items.md).

### <a name="to-set-up-that-an-inventory-movement-is-automatically-created-when-the-inventory-pick-for-the-assembly-item-is-created"></a>Automaattisesti luotavan varastosiirron luominen, kun varasto poiminta luodaan kokoonpanon nimikkeelle
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kokoonpanon asetukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Luo varaston siirrot automaattisesti** -valintaruutu.

### <a name="to-set-up-the-bin-in-the-assembly-area-where-components-are-placed-by-default-before-they-can-be-consumed-in-assembly"></a>Komponenttien oletusvarastopaikan kokoonpanoalueen määrittäminen, ennen kuin ne voidaan kuluttaa kokoonpanossa
Tämän kentän arvo lisätään automaattisesti kokoonpanorivien **Varastopaikkakoodi**-kenttään, kun tämä sijainti lisätään kokoonpanorivin **Sijaintikoodi**-kenttään.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sijainnit** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa määritettävä sijainti.
3. Täytä **Kokoonpanoon-varastop.koodi**-kenttä.

### <a name="to-set-up-the-bin-in-the-assembly-area-where-finished-assembly-items-are-posted-to-when-they-are-assembled-to-stock"></a>Varastopaikan määrittäminen kokoonpanoalueella, jossa varastoon koottavat valmiit kokoonpanon nimikkeet kirjataan
Tämän kentän arvo lisätään automaattisesti kokoonpano-otsikoiden **Varastopaikkakoodi**-kenttään, kun tämä sijaintikoodi täytetään kokoonpano-otsikon **Sijaintikoodi**-kentässä.

Varastopaikkakoodit, jotka on määritetty sijaintikortteihin, määrittävät oletusarvoisen varaston työnkulun tietyille varaston toiminnoille, kuten osien kulutukselle kokoonpanoalueella. Lisätoiminnot varmistavat, että oletusvarastopaikkaan sijoitettavat nimikkeet eivät ole siirrettävissä tai poimittavissa muihin toimiin.

> [!NOTE]
> Asennus on mahdollista vain paikoissa, joissa Var.paikka pakollinen -kenttä on valittuna.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sijainnit** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa määritettävä sijainti.
3. Täytä **Kokoonpanosta-varastop.koodi**-kenttä.

### <a name="to-set-up-the-bin-where-finished-assembly-items-are-posted-to-when-they-are-assembled-to-a-linked-sales-order"></a>Sellaisen varastopaikan määrittäminen, jossa valmiit kokoonpanon nimikkeet kirjataan, kun ne kootaan linkitettyyn myyntitilaukseen
Kokoonpanon nimikkeet toimitetaan tästä varastopaikasta välittömästi varaston poiminnan kautta myyntitilauksen tarpeiden täyttämiseksi.

> [!NOTE]
> Tätä kenttää voi käyttää vain, jos sijainnissa on määritetty käytettäväksi ohjattua poimintaa ja hyllytystä.

Varastopaikkakoodi kopioidaan myyntitilausrivin kokoonpanon otsikkoon, jonka perusteella kokoajille välittyy tieto, mihin tuotos sijoitetaan toimituksen valmistelua varten. Se myös kopioidaan varaston poimintariville varastointityöntekijöitä varten ohjeeksi, mistä se otetaan toimitettavaksi.

> [!NOTE]
> Tilausta varten tehtävien kokoonpanojen toimituksen varastopaikka on aina tyhjä. Silloin, kun kirjaat kokoonpano tilausta varten myyntirivin, varastopaikan sisältö on ensin positiivisesti säädetty kokoonpanon tuotoksen kanssa. Heti jälkikäteen. Muutetaan negatiivisesti toimitetun määrän kanssa.

Tämän kentän arvo lisätään automaattisesti myyntitilausrivin Varastopaikkakoodi-kenttään, joka sisältää **Kokoonpantava määrä tilausta varten** -kentän määrän tai jos myytävällä nimikkeellä on **Kokoonpano tilausta varten** **Täydennysjärjestelmä**-kentässä.

Jos **Kok. til.ltoimit. -var.p.koodi** on tyhjä, **Kokoonpanosta-varastop.koodi**-kenttää käytetään sen sijaan. Jos molemmat asetuskentät ovat tyhjiä, myyntitilausrivien **Varastopaikkakoodi**-kentässä käytetään viimeksi käytettyä varastopaikkaa, jolla on sisältöä.

Sama varastopaikkakoodi kopioidaan puolestaan varaston poimintarivin **Varastopaikkakoodi**-kenttään, joka hallitsee tilaukselle kootun määrän toimitusta. Lisätietoja on ohjeaiheen [Nimikkeiden poiminta varaston poiminnoissa](warehouse-how-to-pick-items-with-inventory-picks.md) kohdassa Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sijainnit** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa määritettävä sijainti.
3. Täytä **Kok. til.ltoimit. -var.p.koodi** -kenttä.

## <a name="to-create-dedicated-component-bins"></a>Osien erityisvarastopaikkojen luominen
Voit määrittää, että varastopaikan määrät suojataan nykyistä tarkoitusta lukuun ottamatta kaikilta muiden tarpeiden poiminnoilta.

Erityisvarastopaikoissa olevat määrät voidaan edelleen varata. Näin ollen erityisvarastopaikkojen määrät sisällytetään **Varaus**-ikkunan **Saatavilla oleva kokonaismäärä** -kenttään.

Esimerkiksi tuotantosolu on määritetty **Tuotannon valmisteluvarastopaikkakoodi** -kentän varastopaikkakoodilla. Oletusvarastopaikkakoodilla varustetut tuotantotilauksen komponenttirivit vaativat, että eteenpäin siirretyt komponentit sijoitetaan niihin. Kunnes kyseisen varastopaikan komponentit on kulutettu loppuun, tästä varastopaikasta voidaan poimia tai kuluttaa muiden komponenttien kysynnän mukaisesti, koska varastopaikat ovat yhä saatavana olevaa varastopaikan sisältöä. Voit varmistaa, että vain kyseistä tuotannon valmisteluvarastopaikkaa käyttävä komponenttitarve voi käyttää sen sisältöä valitsemalla **Erityinen**-kentän kyseisen varastopaikkakoodin rivillä sijaintikortista avattavassa **Varastopaikat**-ikkunassa.

Erillisen varastopaikan tekeminen tuottaa samantapaisen toiminnan kuin varastopaikkatyyppien käyttö, joka on mahdollista vain laajennetussa varastoinnissa. Lisätietoja on kohdassa [Varastopaikkojen määrittäminen](warehouse-how-to-set-up-bin-types.md).

> [!Caution]
> Erikoisvarastopaikoissa olevat nimikkeet eivät ole suojattuja, kun ne on kerätty ja kulutettu tuotantokomponentteina Varaston poiminta -ikkunan kautta.

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sijainnit** ja valitse sitten aiheeseen liittyvä linkki. Avaa sijainti, jonka haluat päivittää.  
2.  Valitse **Varastopaikat**-toiminto.  
3.  Valitse **Erityinen** -kenttä jokaiselle varastopaikalle, jolle haluat käyttää yksinomaan tiettyjä sisäisiä operaatioita ja joille haluat varata määriä sisäiselle operaatiolle, kun se on sijoitettu sinne.  

> [!NOTE]  
>  Varastopaikan on oltava tyhjä ennen kuin voit valita tai poistaa **Erityinen**-kentän.

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
