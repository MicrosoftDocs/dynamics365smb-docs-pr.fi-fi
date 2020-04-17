---
title: Komponenttien poiminta tuotantoon fyysisen varaston perusmäärityksissä | Microsoft Docs
description: Kun fyysisen varastoinnin sijainnissa on pakollinen poiminnan käsittely mutta ei pakollista toimituksen käsittelyä, voit järjestää ja kirjata komponenttien poiminnan **Varaston poiminta** -sivun avulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: a5ae614f37cec06d6702b8cf494e3a00f2ba5585
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193020"
---
# <a name="pick-for-production-or-assembly-in-basic-warehouse-configurations"></a>Tuotanto- tai kokoonpanopoiminta perusvarastointimäärityksissä
Tuotantoon tai koonpanotilauksiin poimittujen komponenttien hyllytystapa määräytyy sen mukaan, miten fyysinen varasto on määritetty sijaintina. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

Jos fyysisen varaston perusmäärityksissä sijainti edellyttää poiminnan käsittelyä mutta ei toimituksen käsittelyä, voit järjestää ja kirjata komponenttien poiminnan **Varaston poiminta** -sivulla.  

Fyysisen varaston perusmäärityksissä poiminta kokoonpanotilauksiin on tehtävä **Varastosiirto**-sivulla. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Fyysisen varaston laajennetuissa määrityksissä, joissa sijanneille on määritettävä sekä poiminnat että toimitukset, komponentit tuodaan tuotanto- tai kokoonpanotilauksiin **F.varastoinnin poiminta** -sivulla. Lisätietoja on kohdassa [Tuotanto- tai kokoonpanopoiminta laajennetuissa varastointimäärityksissä](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

> [!NOTE]  
>  Varastopoiminnan ja varastosiirron välillä on seuraavia, merkittäviä eroja:  
>   
>  -   Kun rekisteröit varaston poiminnan sisäiseen toimintoon, kuten tuotanto, vpoimittujen osien kulutus kirjataan samaan aikaan. Kun rekisteröit varaston siirtotapahtuman sisäiselle toiminnolle, tallennat vain tarvittavien osien fyysiset siirrot varastopaikkaan toiminta-alueella ilman kulutuksen kirjaamista.  
> -   Kun käytät varaston poimintoja **Varastopaikkakoodi** -kenttä tuotantotilauksen komponentin rivinumero määrittää*ota* -varastopaikan, josta osat vähenevät, kun kulutus kirjataan. Kun käytät varaston siirtotapahtumia, tuotantotilauksen komponenttirivien **Varastopaikkakoodi**-kenttä määrittää toiminta-alueen *paikka*-varastopaikan, johon varastotyöntekijän on sijoitettava komponentit.  

Järjestelmän ennakkoehto komponenttien poiminnalle tai siirtämiselle lähdeasiakirjoissa on, että lähtevän varaston pyyntö olemassa, jotta varasto saa tiedon tarvittavasta komponentista. Ohjelma luo lähtevän fyysisen varastoinnin pyynnön, kun tuotantotilauksen tilaksi muutetaan Vapautettu tai kun vapautettu tuotantotilaus luodaan.  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a>Komponenttien poiminta fyysisen varaston perusmäärityksissä
Fyysisen varaston perusmäärityksissä, joissa sijainti on määritetty käyttämään vain poimintaa, komponentteja voi poimia tuotantotoimintoihin **Varaston poiminta** -sivulla. Lisätietoja on kohdassa [Nimikkeiden poiminta varastopoiminnalla](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varaston poiminnat** ja valitse sitten liittyvä linkki.  
2.  Voit tarkastella tuotantotilauksen komponentteja valitsemalla ensin **Hae lähdedokumentit** -toiminnon ja sitten vapautetun tuotantotilauksen.  
3.  Tee poiminta ja kirjaa sitten varsinaiset poimintatiedot **Määrä poimittu** -kenttään.  
4.  Kun rivit ovat valmiit kirjaamista varten, valitse **Kirjaa**-toiminto. Kirjaus luo tarvittavat fyysisen varaston tapahtumat ja kirjaa nimikkeiden kulutuksen.  

Voit myös luoda **Varastopoiminnan** suoraan vapautetusta tuotantotilauksesta. Valitse ensin **Luo varastohyllytys/-poiminta** -toiminto, sitten **Luo varaston poiminta** -valintaruutu ja lopuksi **OK**.

Vaihtoehtoisesti voit siirtää nimikkeitä varastopaikasta toiseen **Varaston siirto**-sivulla ilman viittausta lähdeasiakirjaan.
Lisätietoja on kohdassa [Komponenttien siirtäminen toiminta-alueelle fyysisen varaston perusmäärityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa
**Varaston poiminta** -sivulla voi myös poimia ja toimittaa myyntiin nimikkeitä, jotka on koottava ennen toimitusta. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).

Toimitettavat nimikkeet eivät ole paikalla, kunnes ne kootaan ja kirjataan kokoonpanoalueen varastopaikan tuotokseksi. Tämä tarkoittaa, että kokoonpano tilausta varten -nimikkeiden poiminta toimitusta varten noudattaa eritystä virtaa. Varastopaikasta varastotyöntekijät vievät kokoonpanon nimikkeet toimituslaituriin ja kirjaavat sitten varastopoiminnan. Kirjattu varaston poiminta kirjaa sitten kokoonpanon tuotoksen, komponentin kulutuksen ja myyntitoimituksen.

Voit määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in luomaan varaston siirron automaattisesti, kun varastopoiminta luodaan kokoonpanon nimikkeelle. Tämä toiminta otetaan käyttöön valitsemalla **Luo siirrot automaattisesti** -kenttä **Kokoonpanon asetukset** -sivulla. Lisätietoja on kohdassa [Komponenttien siirtäminen fyysisen perusvarastoinnin toiminta-alueelle](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Myyntinimikkeiden varaston poimintarivit luodaan eri tavalla sen mukaan, onko tilaukseen koottu mitään, joitakin vai kaikki myyntirivin määrille määritetyt määrät.

Normaalissa myynnissä, jossa varaston määrien toimitus kirjataan varaston poimintoina, kullekin myyntitilausriville luodaan yksi varaston poimintarivi tai useita varaston poimintarivejä, jos nimike sijoitetaan eri varastopaikkoihin. Tämä poimintarivi perustuu **Toimitettava määrä** -kentän määrään.

Kokoonpano tilausta varten -myynnissä, jossa myyntitilauksen koko määrä kootaan tilaukseen, kyseiselle määrälle luodaan yksi varaston poimintarivi. Näin ollen Kokoonpantava määrä -kentän arvo on sama kuin **Toimitettava määrä** -kentän arvo. **Kokoonpantava määrä** -kenttä on valittu rivillä.

Jos sijainnin kokoonpanon tuotoksen virta on määritetty, **Kok. til.ltoimit. -var.p.koodi** -kentän arvo tai **Kokoonpanosta-varastop.koodi** -kentän arvo lisätään tässä järjestyksessä varaston poimintarivin **Varastopaikan koodi** -kenttään.

Jos myyntitilausriville ei ole määritetty varastopaikkakoodia eikä sijainnille kokoonpanon tuotoksen virtaa, varaston poimintarivin **Varastopaikan koodi** -kenttä on tyhjä. Varastotyöntekijän on avattava **Varastopaikan sisältö** -sivu ja valittava varastopaikka, johon kokoonpanon nimikkeet kootaan.

Yhdistelmätilanteissa, joissa osa määrästä on koottava ensin ja toinen poimittava varastosta, luodaan vähintään kaksi varaston toimitusriviä. Yksi poimintarivi on kokoonpano tilausta varten -määrälle. Toinen poimintarivi riippuu siitä, mistä varastopaikoista voidaan saada jäljellä oleva määrä. Kahden rivin varastopaikkakoodit on täytetty eri tavoin kahden vastaavan myyntityypin mukaan. Lisätietoja on ohjeaiheen [Tietoja Kokoonpano tilausta varten- tai Kokoonpano varastoon -toiminnoista](assembly-assemble-to-order-or-assemble-to-stock.md) kohdassa Skenaarioiden yhdistelmä.

## <a name="filling-the-consumption-bin"></a>Kulutuksen varastopaikan täyttäminen
Tämä työnkulkukaavio näyttää, miten tuotantotilauksen osarivien **Varastopaikkakoodi**-kenttä täytetään sijaintiasetusten mukaisesti.

![Varastopaikkojen työnkulkukaavio](media/binflow.png "BinFlow")

## <a name="see-also"></a>Katso myös
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
