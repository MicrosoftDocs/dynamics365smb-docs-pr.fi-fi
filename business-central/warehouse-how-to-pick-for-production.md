---
title: Poiminta tuotantoon tai kokoonpanoon fyysisen varaston perusmäärityksissä
description: Kun fyysisen varaston sijainnissa on pakollinen poiminnan käsittely mutta ei pakollista toimituksen käsittelyä, voit järjestää ja kirjata komponenttien poiminnan Varaston poiminta -sivun avulla.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 2814fe1f9ca71c3a14bb288427c9b12603d0463a
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529135"
---
# <a name="pick-for-production-or-assembly-in-basic-warehouse-configurations"></a>Tuotanto- tai kokoonpanopoiminta perusvarastointimäärityksissä

Tuotantoon tai koonpanotilauksiin poimittujen komponenttien hyllytystapa määräytyy sen mukaan, miten fyysinen varasto on määritetty sijaintina. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Poiminta tuotantoon fyysisen varastoinnin perusmäärityksissä

Materiaaliottotavat vaikuttavat myös komponenttien siirtymiseen tuotantoon. Lisätietoja on kohdassa [Komponenttien materiaalinotto toiminnan tuotoksen mukaan](production-how-to-flush-components-according-to-operation-output.md).

Niissä laajennetuissa varastomäärityksissä, joissa sijainnit edellyttävät sekä poimintoja että toimituksia, ne komponentit, joiden materiaaliottotavaksi on määritetty *Manuaalinen*, *Poiminta + eteenpäin*, *Poiminta + taaksepäin*, on tuotava tuotantotilauksiin **F. varastoinnin poiminta** -sivulla. Lisätietoja on kohdassa [Tuotanto- tai kokoonpanopoiminta laajennetuissa varastointimäärityksissä](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

Jos fyysisen varaston perusmäärityksissä sijainti edellyttää poiminnan käsittelyä mutta ei toimituksen käsittelyä, voit järjestää ja kirjata sellaisten komponenttien poiminnan myös **Varaston poiminta** -sivulla, joiden materiaaliottotavaksi on määritetty *Manuaalinen*. Kun rekisteröit varaston poiminnan sisäiseen toimintoon, kuten tuotanto, vpoimittujen osien kulutus kirjataan samaan aikaan. Vaihtoehtoisesti voit käyttää lähdeasiakirjaan viittaavaa **varaston siirtoa** tuomaan tuotantotilauksiin sellaiset komponentit, joiden materiaaliottotavaksi on määritetty *Manuaalinen*, *Poiminta + eteenpäin*, *Poiminta + taaksepäin*.

Kun tuotantoprosessit on integroitu varastoprosesseihin, joko varastopaikkojen tai ohjattujen hyllytysten ja poimintojen perusteella, varastopaikka, josta osia käytetään, on se varastopaikka, joka on määritetty kunkin tuotantotilauksen komponenttirivillä. Kaikkien tarvittavien komponenttien on oltava käytettävissä kyseisessä varastopaikassa. Muutoin kyseisen komponentin manuaalinen tai poistettava kulutuskirjaus pysäytetään.

Lähdeasiakirjaan viittaavaa **varaston siirtoa** ja **fyysisen varastoinnin poimintaa** ei voi käyttää sellaisten komponenttien poimimiseen, joiden materiaaliottotapana on *Eteenpäin* ja *Taaksepäin*. **Varaston poimintaa** ei voi käyttää poimimaan komponentteja, joilla on jokin muu materiaaliottotapa kuin *Manuaalinen*. Jäljellä olevien komponenttien käsittelemiseen käytetään **varaston siirtoa**, jossa ei viitata lähdeasiakirjaan. Lisätietoja on kohdassa [Komponenttien siirtäminen toiminta-alueelle fyysisen varaston perusmäärityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

> [!NOTE]  
>  Varastopoimintojen, varaston siirtojen ja fyysisen varastoinnin poimintojen välillä on seuraavia, merkittäviä eroja:  
>   
>  -   Kun rekisteröit varaston poiminnan sisäiseen toimintoon, kuten tuotanto, vpoimittujen osien kulutus kirjataan samaan aikaan. Kun rekisteröit varaston siirron tai fyysisen varastoinnin poiminnan sisäiselle toiminnolle, vain tarvittavien komponenttien fyysiset siirrot tallennetaan varastopaikkaan toiminta-alueella ilman kulutuksen kirjaamista.  
> -   Kun käytät varaston poimintoja **Varastopaikkakoodi** -kenttä tuotantotilauksen komponentin rivinumero määrittää *ota* -varastopaikan, josta osat vähenevät, kun kulutus kirjataan. Kun käytät varaston siirtoja tai fyysisen varastoinnin poimintaa, tuotantotilauksen komponenttirivien **Varastopaikkakoodi**-kenttä määrittää toiminta-alueen *paikka*-varastopaikan, johon varastotyöntekijän on sijoitettava komponentit.  

Järjestelmän ennakkoehto komponenttien poiminnalle tai siirtämiselle lähdeasiakirjoissa on, että lähtevän varaston pyyntö olemassa, jotta varasto saa tiedon tarvittavasta komponentista. Ohjelma luo lähtevän fyysisen varastoinnin pyynnön, kun tuotantotilauksen tilaksi muutetaan Vapautettu tai kun vapautettu tuotantotilaus luodaan.  

## <a name="to-pick-production-components-in-basic-warehouse-configurations-using-inventory-pick"></a>Tuotantokomponenttien poiminta fyysisen varaston perusmäärityksissä Varaston poiminta -toiminnolla

Fyysisen varaston perusmäärityksissä, joissa sijainti on määritetty käyttämään vain poimintaa, komponentteja voi poimia tuotantotoimintoihin **Varaston poiminta** -sivulla. Lisätietoja on kohdassa [Nimikkeiden poiminta varastopoiminnalla](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston poiminnat** ja valitse sitten vastaava linkki.  
2.  Voit tarkastella tuotantotilauksen komponentteja valitsemalla ensin **Hae lähdedokumentit** -toiminnon ja sitten vapautetun tuotantotilauksen.  
3.  Tee poiminta ja kirjaa sitten varsinaiset poimintatiedot **Käsiteltävä määrä** -kenttään.  
4.  Kun rivit ovat valmiit kirjaamista varten, valitse **Kirjaa**-toiminto. Kirjaus luo tarvittavat fyysisen varaston tapahtumat ja kirjaa nimikkeiden kulutuksen.  

Voit myös luoda **Varastopoiminnan** suoraan vapautetusta tuotantotilauksesta. Valitse ensin **Luo varaston hyllytys, poiminta tai siirto** -toiminto, sitten **Luo varaston poiminta** -valintaruutu ja lopuksi **OK**.

Vaihtoehtoisesti voi siirtää nimikkeitä varastopaikasta toiseen käyttämällä lähdeasiakirjaan viittaavaa **varaston siirtoa**. Kulutus on sitten rekisteröitävä erikseen. Lisätietoja on kohdassa [Tuotannon kulutuksen eräkirjaaminen](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Poiminta kokoonpanoon fyysisen varastoinnin perusmäärityksissä

Fyysisen varaston laajennetuissa määrityksissä, joissa sijanneille on määritettävä sekä poiminnat että toimitukset, komponentit on tuotava kokoonpanotilauksiin **F.varastoinnin poiminta** -sivulla. Lisätietoja on kohdassa [Tuotanto- tai kokoonpanopoiminta laajennetuissa varastointimäärityksissä](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

Fyysisen varaston perusmäärityksissä poiminta kokoonpanotilauksiin voidaan tehdä myös **Varaston siirto** -sivulla. 

Niissä fyysisen varastoinnin perusmäärityksissä, joissa sijainti edellyttää poiminnan mutta ei toimituksen käsittelyä, **Varaston poiminta** -sivua käytetään myös sellaisten myyntitilausten poimimiseen, kokoamiseen ja toimittamiseen, jossa nimikkeet on koottava ennen toimitusta. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

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

## <a name="filling-the-consumption-bin"></a>Kulutuksen varastopaikan täyttäminen

Tämä työnkulkukaavio näyttää, miten tuotantotilauksen osarivien **Varastopaikkakoodi**-kenttä täytetään sijaintiasetusten mukaisesti.

![Varastopaikkojen työnkulkukaavio.](media/binflow.png "BinFlow")

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Katso myös

[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
