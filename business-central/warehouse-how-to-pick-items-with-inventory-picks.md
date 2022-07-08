---
title: Nimikkeiden poiminta varaston poiminnalla
description: Kun sijainti vaatii poiminnan prosessointia, mutta ei toimituksen prosessointia, sinun on käytettävä varaston poiminnan asiakirjoja lähdeasiakirjan poiminnan ja toimituksen tietojen tallennuksessa ja kirjaamisessa.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8764fa82ef8bf408e85655b5a97719d9f649e7be
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9078360"
---
# <a name="pick-items-with-inventory-picks"></a>Nimikkeiden poiminta varastopoiminnalla

Kun sijainti on määritetty vaatimaan poiminnan prosessointia, mutta ei toimituksen prosessointia, käytä **Varaston poiminta** -sivua lähdeasiakirjan poiminnan ja toimituksen tietojen tallennuksessa ja kirjaamisessa. Lähtevä lähdeasiakirja voi olla myyntitilaus, ostopalautustilaus, lähtevä siirtotilaus tai tuotantotilaus, jonka osat ovat valmiina poimittaviksi.

> [!NOTE]  
> Kokoonpanotilausten osia ei voi poimia tai kirjata varastopoiminnan kanssa. Käytä sen sijaan **Varaston siirto** -sivua. Lisätietoja on kohdassa [Komponenttien siirtäminen fyysisen perusvarastoinnin toiminta-alueelle](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).
>
> Kun poiminnan ja toimituksen myyntirivin määriä kootaan tilaukseen, varaston poimintarivejä luotaessa on noudatettava tiettyjä sääntöjä. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa](#handling-assemble-to-order-items-with-inventory-picks) -osassa.  

Varaston poiminnan voi luoda kolmella tavalla:  

- Luo poiminta kahdessa vaiheessa pyytämällä ensin varastopoiminta vapauttamalla lähdeasiakirja. Tämä ilmoittaa fyysiseen varastoon, että lähdeasiakirja on valmiina poimintaa varten. Varaston poiminta voidaan sitten luoda **Varaston poiminta** -sivulla lähdeasiakirjan perusteella.  
- Luomalla varastopoiminta suoraan lähdeasiakirjasta.  
- Voit luoda varastopoiminnat useammalle asiakirjalle yhdellä kertaa käyttämällä eräajoa.  

## <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a>Pyydä varastopoiminta vapauttamalla lähdeasiakirja

Jos kyseessä on myyntitilaus, ostopalautustilaus tai lähtevä siirto, voit luoda fyysisen varastoinnin pyynnön vapauttamalla tilauksen. Seuraavaksi käsitellään, miten se tehdään myyntitilauksesta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.
2. Valitse ensin vapautettava myyntitilaus ja sitten **Vapauta**-toiminto.

Tuotantotilauksissa osien poiminnan fyysisen varastoinnin pyyntö eli *materiaaliotto* luodaan automaattisesti, kun tuotantotilauksen tilaksi tulee **Vapautettu** tai kun vapautettu tuotantotilaus luodaan. Lisätietoja on kohdassa [Tuotannon tai kokoonpanon poiminta](warehouse-how-to-pick-for-production.md).

Kun fyysisen varaston pyyntö on luotu, varastotyöntekijä, jolle nimikkeiden poiminta on määritetty, näkee, että lähdeasiakirja odottaa poimintaa ja voi luoda uuden poiminta-asiakirjan fyysisen varaston pyynnöstä.  

## <a name="to-create-an-inventory-pick-based-on-the-source-document"></a>Lähdeasiakirjaan perustuvan varaston poiminnan luominen

Nyt kun pyyntö on luotu, varastotyöntekijä voi luoda uuden varaston poiminnan vapautetun lähdeasiakirjan perusteella.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston poiminnat** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
    Varmista, että **Nro**-kenttä täytetään **Yleinen**-pikavälilehdessä.
3. Valitse **Lähdeasiakirja**-kentässä sen lähdeasiakirjan tyyppi, jolle teet poiminnan.  
4. Valitse **Lähteen nro** -kentässä lähdeasiakirja.  
5. Vaihtoehtoisesti voit valita **Hae lähdeasiakirja** -toiminnolla asiakirjan niiden lähtevien lähdeasiakirjojen luettelosta, jotka ovat valmiita poimintaan sijainnissa.  
6. Täytä poimintarivit valitun lähdeasiakirjan mukaan valitsemalla **OK**.  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a>Varastopoiminnan lähdeasiakirjasta luominen

1. Valitse **Luo varaston hyllytys tai poiminta** -toiminto lähdeasiakirjassa, joka voi olla myyntitilaus, ostopalautustilaus, lähtevä siirtotilaus tai tuotantotilaus.
2. Valitse **Luo varaston poiminta** -valintaruutu.  
3. Valitse **OK**-painike. Uusi varaston poiminta luodaan.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a>Useiden varaston poimintojen luominen eräajon avulla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo var. hyllytys / poiminta** ja valitse sitten vastaava linkki.  
2. Suodata **F.varastoinnin pyyntö** -pikavälilehden **Lähdeasiakirja**- ja **Lähteen nro** -kenttien avulla tietyntyyppiset asiakirjat tai asiakirjanumerovälit. Voit esimerkiksi luoda poimintoja vain myyntitilauksille.  
3. Valitse **Asetukset**-pikavälilehdessä **Luo varaston poiminta** -valintaruutu.
4. Valitse **OK**-painike. Määritetyt varaston poiminnat luodaan.

> [!NOTE]  
> Jos kyseessä ovat poiminnan ja toimituksen myyntirivin määrät, jotka on koottu tilausta varten, luo varaston poimintarivit tiettyjen sääntöjen mukaan. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa](#handling-assemble-to-order-items-with-inventory-picks) -osassa.  
>
> Fyysisen varastoinnin perusmäärityksissä myyntitilauksiin kootut nimikkeet poimitaan liittyvästä myyntitilauksesta tässä ohjeaiheessa kuvatulla tavalla. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa](#handling-assemble-to-order-items-with-inventory-picks) -osassa.  

## <a name="to-record-the-inventory-picks"></a>Varaston poimintojen kirjaaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston poiminta** ja valitse sitten vastaava linkki.  
2. Poimintarivien **Varastopaikkakoodi**-kentässä varastopaikka, josta nimikkeet on poimittava, ehdotetaan nimikkeen oletusvarastopaikan mukaan. Voi muuttaa tarvittaessa varastopaikkaa tällä sivulla.  
3. Suorita poiminta ja annan todellisia hyllytysmääriä koskevat tiedot **Käsiteltävä määrä** -kentässä.

    Jos yhden rivin nimikkeet on poimittava useasta varastopaikasta esimerkiksi siksi, että niitä ei ole saatavilla määritetyssä varastopaikassa, käytä **Rivit**-pikavälilehden **Jaa rivi** -toimintoa. Lisätietoja rivien jakamisesta on kohdassa [Varastotoimintorivien jakaminen](warehouse-how-to-split-warehouse-activity-lines.md).  
4. Kun olet suorittanut poiminnan, valitse **Kirjaa**-toiminto.  

Kirjausprosessi kirjaa toimituksen poimituille lähdeasiakirjariveille tai tuotantilauksen olessa kyseessä se kirjaa kulutusta. Jos sijainti käyttää var.paikkoja, kirjaus luo myös f.var.tapahtumia kirjatakseen var.paikan määrä muutoksia.  

## <a name="to-delete-inventory-pick-lines"></a>Poista varaston poimintarivit

Jos varaston poiminnan nimikkeet eivät ole saatavissa, voit poistaa nämä varaston poimintarivit kirjaamisen jälkeen ja poistaa sitten varaston poiminta-asiakirjan. Lähdeasiakirjassa, esimerkiksi myyntitilauksessa tai tuotantotilauksessa, on jäljellä vain poimittavat nimikkeet, jotka voidaan ottaa mukaan myöhemmin uuden varaston poiminnan aikana, kun nimikkeet ovat taas saatavissa.  

> [!WARNING]  
> Tämä toimenpide ei ole mahdollinen, jos sarja- tai eränumerot on määritetty lähdeasiakirjassa. Jos esimerkiksi myyntitilausrivi sisältää sarja-/eränumeron, tämän nimikeseurannan määritys poistetaan, jos sarja-/eränumeron varaston poimintarivi poistetaan.  
>
> Jos varaston poimintariveillä on sarja-/eränumeroita, jotka eivät ole saatavissa, näitä rivejä ei saa poistaa. Sinun on sen sijaan muutettava **Käsiteltävä määrä** -kentän arvoksi nolla, kirjattava toteutuneet poiminnat ja poistettava sitten varaston poiminta-asiakirja. Tämä varmistaa, että näiden sarja-/eränumeroiden varaston poimintarivit voidaan myöhemmin luoda uudelleen myyntitilauksesta.  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa

**Varaston poiminta** -sivulla voi myös poimia ja toimittaa myyntiin nimikkeitä, jotka on koottava ennen toimitusta. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).

Toimitettavat nimikkeet eivät ole paikalla, kunnes ne kootaan ja kirjataan kokoonpanoalueen varastopaikan tuotokseksi. Tämä tarkoittaa, että kokoonpano tilausta varten -nimikkeiden poiminta toimitusta varten noudattaa eritystä virtaa. Varastopaikasta varastotyöntekijät vievät kokoonpanon nimikkeet toimituslaituriin ja kirjaavat sitten varastopoiminnan. Kirjattu varaston poiminta kirjaa sitten kokoonpanon tuotoksen, komponentin kulutuksen ja myyntitoimituksen.

Voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in luomaan varaston siirron automaattisesti, kun varastopoiminta luodaan kokoonpanon nimikkeelle. Tämä toiminta otetaan käyttöön valitsemalla **Luo siirrot automaattisesti** -kenttä **Kokoonpanon asetukset** -sivulla. Lisätietoja on kohdassa [Komponenttien siirtäminen fyysisen perusvarastoinnin toiminta-alueelle](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Myyntinimikkeiden varaston poimintarivit luodaan eri tavalla sen mukaan, onko tilaukseen koottu mitään, joitakin vai kaikki myyntirivin määrille määritetyt määrät.

Normaalissa myynnissä, jossa varaston määrien toimitus kirjataan varaston poimintoina, kullekin myyntitilausriville luodaan yksi varaston poimintarivi tai useita varaston poimintarivejä, jos nimike sijoitetaan eri varastopaikkoihin. Tämä poimintarivi perustuu **Toimitettava määrä** -kentän määrään.

Kokoonpano tilausta varten -myynnissä, jossa myyntitilauksen koko määrä kootaan tilaukseen, kyseiselle määrälle luodaan yksi varaston poimintarivi. Näin ollen Kokoonpantava määrä -kentän arvo on sama kuin **Toimitettava määrä** -kentän arvo. **Kokoonpantava määrä** -kenttä on valittu rivillä.

Jos sijainnin kokoonpanon tuotoksen virta on määritetty, **Kok. til.ltoimit. -var.p.koodi** -kentän arvo tai **Kokoonpanosta-varastop.koodi** -kentän arvo lisätään tässä järjestyksessä varaston poimintarivin **Varastopaikan koodi** -kenttään.

Jos myyntitilausriville ei ole määritetty varastopaikkakoodia eikä sijainnille kokoonpanon tuotoksen virtaa, varaston poimintarivin **Varastopaikan koodi** -kenttä on tyhjä. Varastotyöntekijän on avattava **Varastopaikan sisältö** -sivu ja valittava varastopaikka, johon kokoonpanon nimikkeet kootaan.

Yhdistelmätilanteissa, joissa osa määrästä on koottava ensin ja toinen poimittava varastosta, luodaan vähintään kaksi varaston toimitusriviä. Yksi poimintarivi on kokoonpano tilausta varten -määrälle. Toinen poimintarivi riippuu siitä, mistä varastopaikoista voidaan saada jäljellä oleva määrä. Kahden rivin varastopaikkakoodit on täytetty eri tavoin kahden vastaavan myyntityypin mukaan. Lisätietoja on ohjeaiheen [Tietoja Kokoonpano tilausta varten- tai Kokoonpano varastoon -toiminnoista](assembly-assemble-to-order-or-assemble-to-stock.md) kohdassa Skenaarioiden yhdistelmä.

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Katso myös

[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Vaihekuvaus: Poiminta ja toimitus fyysisen varastoinnin perusmäärityksissä](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]