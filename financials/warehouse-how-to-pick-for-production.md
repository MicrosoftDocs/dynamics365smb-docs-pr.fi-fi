---
title: "Komponenttien poiminta tuotantoon fyysisen varaston perusmäärityksissä | Microsoft Docs"
description: "Kun fyysisen varastoinnin sijainnissa on pakollinen poiminnan käsittely mutta ei pakollista toimituksen käsittelyä, voit järjestää ja kirjata komponenttien poiminnan **Varaston poiminta** -ikkunan avulla."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 68702e384ea750535a8d7e5b83ee619856b6a34b
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="pick-for-production-or-assembly"></a>Poiminta tuotantoon tai kokoonpanoon
Tuotantoon tai koonpanotilauksiin poimittujen komponenttien hyllytystapa määräytyy sen mukaan, miten fyysinen varasto on määritetty sijaintina. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

Jos fyysisen varaston perusmäärityksissä sijainti edellyttää poiminnan käsittelyä mutta ei toimituksen käsittelyä, voit järjestää ja kirjata komponenttien poiminnan **Varaston poiminta** -ikkunassa.  

Fyysisen varaston perusmäärityksissä poiminta kokoonpanotilauksiin on tehtävä **Varastosiirto**-ikkunassa. Lisätietoja on ohjeaiheen [Nimikkeiden poiminta varaston poiminnoissa](warehouse-how-to-pick-items-with-inventory-picks.md) kohdassa Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa.  

Fyysisen varaston laajennetuissa määrityksissä, joissa sijanneille on määritettävä sekä poiminnat että toimitukset, komponentit tuodaan tuotanto- tai kokoonpanotilauksiin **F.varastoinnin poiminta** -ikkunassa.

> [!NOTE]  
>  Varastopoiminnan ja varastosiirron välillä on seuraavia, merkittäviä eroja:  
>   
>  -   Kun rekisteröit varaston poiminnan sisäiseen toimintoon, kuten tuotanto, vpoimittujen osien kulutus kirjataan samaan aikaan. Kun rekisteröit varaston siirtotapahtuman sisäiselle toiminnolle, tallennat vain tarvittavien osien fyysiset siirrot varastopaikkaan toiminta-alueella ilman kulutuksen kirjaamista.  
> -   Kun käytät varaston poimintoja **Varastopaikkakoodi** -kenttä tuotantotilauksen komponentin rivinumero määrittää*ota* -varastopaikan, josta osat vähenevät, kun kulutus kirjataan. Kun käytät varaston siirtotapahtumia, tuotantotilauksen komponenttirivien **Varastopaikkakoodi**-kenttä määrittää toiminta-alueen *paikka*-varastopaikan, johon varastotyöntekijän on sijoitettava komponentit.  

Järjestelmän ennakkoehto komponenttien poiminnalle tai siirtämiselle lähdeasiakirjoissa on, että lähtevän varaston pyyntö olemassa, jotta varasto saa tiedon tarvittavasta komponentista. Ohjelma luo lähtevän fyysisen varastoinnin pyynnön, kun tuotantotilauksen tilaksi muutetaan Vapautettu tai kun vapautettu tuotantotilaus luodaan.  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a>Komponenttien poiminta fyysisen varaston perusmäärityksissä
Fyysisen varaston perusmäärityksissä, joissa sijainti on määritetty käyttämään vain poimintaa, komponentteja voi poimia tuotantotoimintoihin **Varaston poiminta** -ikkunassa. Lisätietoja on kohdassa [Nimikkeiden poiminta varastopoiminnalla](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Varaston poiminnat** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Voit tarkastella tuotantotilauksen komponentteja valitsemalla ensin **Hae lähdedokumentit** -toiminnon ja sitten vapautetun tuotantotilauksen.  
3.  Tee poiminta ja kirjaa sitten varsinaiset poimintatiedot **Määrä poimittu** -kenttään.  
4.  Kun rivit ovat valmiit kirjaamista varten, valitse **Kirjaa**-toiminto. Kirjaus luo tarvittavat fyysisen varaston tapahtumat ja kirjaa nimikkeiden kulutuksen.  

Voit myös luoda **Varastopoiminnan** suoraan vapautetusta tuotantotilauksesta. Valitse ensin **Luo varastohyllytys/-poiminta** -toiminto, sitten **Luo varaston poiminta** -valintaruutu ja lopuksi **OK**.

Vaihtoehtoisesti voit siirtää nimikkeitä varastopaikasta toiseen **Varaston siirto**-ikkunassa ilman viittausta lähdeasiakirjaan.
Lisätietoja on kohdassa [Komponenttien siirtäminen toiminta-alueelle fyysisen varaston perusmäärityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa
**Varaston poiminta** -ikkunassa voi myös poimia ja toimittaa myyntiin nimikkeitä, jotka on koottava ennen toimitusta. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).

Toimitettavat nimikkeet eivät ole paikalla, kunnes ne kootaan ja kirjataan kokoonpanoalueen varastopaikan tuotokseksi. Tämä tarkoittaa, että kokoonpano tilausta varten -nimikkeiden poiminta toimitusta varten noudattaa eritystä virtaa. Varastopaikasta varastotyöntekijät vievät kokoonpanon nimikkeet toimituslaituriin ja kirjaavat sitten varastopoiminnan. Kirjattu varaston poiminta kirjaa sitten kokoonpanon tuotoksen, komponentin kulutuksen ja myyntitoimituksen.

Voit määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in luomaan varaston siirron automaattisesti, kun varastopoiminta luodaan kokoonpanon nimikkeelle. Tämä toiminta otetaan käyttöön valitsemalla **Luo siirrot automaattisesti** -kenttä **Kokoonpanon asetukset** -ikkunassa. Lisätietoja on kohdassa [Komponenttien siirtäminen fyysisen perusvarastoinnin toiminta-alueelle](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Myyntinimikkeiden varaston poimintarivit luodaan eri tavalla sen mukaan, onko tilaukseen koottu mitään, joitakin vai kaikki myyntirivin määrille määritetyt määrät.

Normaalissa myynnissä, jossa varaston määrien toimitus kirjataan varaston poimintoina, kullekin myyntitilausriville luodaan yksi varaston poimintarivi tai useita varaston poimintarivejä, jos nimike sijoitetaan eri varastopaikkoihin. Tämä poimintarivi perustuu **Toimitettava määrä** -kentän määrään.

Kokoonpano tilausta varten -myynnissä, jossa myyntitilauksen koko määrä kootaan tilaukseen, kyseiselle määrälle luodaan yksi varaston poimintarivi. Näin ollen Kokoonpantava määrä -kentän arvo on sama kuin **Toimitettava määrä** -kentän arvo. **Kokoonpantava määrä** -kenttä on valittu rivillä.

Jos sijainnin kokoonpanon tuotoksen virta on määritetty, **Kok. til.ltoimit. -var.p.koodi** -kentän arvo tai **Kokoonpanosta-varastop.koodi** -kentän arvo lisätään tässä järjestyksessä varaston poimintarivin **Varastopaikan koodi** -kenttään.

Jos myyntitilausriville ei ole määritetty varastopaikkakoodia eikä sijainnille kokoonpanon tuotoksen virtaa, varaston poimintarivin **Varastopaikan koodi** -kenttä on tyhjä. Varastotyöntekijän on avattava **Varastopaikan sisältö** -ikkuna ja valittava varastopaikka, johon kokoonpanon nimikkeet kootaan.

Yhdistelmätilanteissa, joissa osa määrästä on koottava ensin ja toinen poimittava varastosta, luodaan vähintään kaksi varaston toimitusriviä. Yksi poimintarivi on kokoonpano tilausta varten -määrälle. Toinen poimintarivi riippuu siitä, mistä varastopaikoista voidaan saada jäljellä oleva määrä. Kahden rivin varastopaikkakoodit on täytetty eri tavoin kahden vastaavan myyntityypin mukaan. Lisätietoja on ohjeaiheen [Tietoja Kokoonpano tilausta varten- tai Kokoonpano varastoon -toiminnoista](assembly-assemble-to-order-or-assemble-to-stock.md) kohdassa Skenaarioiden yhdistelmä.

## <a name="to-pick-components-in-advanced-warehouse-configurations"></a>Komponenttien poiminta laajennetussa varastointimäärityksissä
Jos sijainti on määritetty laajennetuissa varastomäärityksissä käyttämään sekä poimintaa että toimitusta, tuotannon ja kokoonpanon toimintojen komponentteja voi poimia **F.varastoinnin poiminta** -ikkunassa. Lisätietoja on kohdassa [Nimikkeiden poiminta fyysisen varaston poiminnassa](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Vaihtoehtoisesti voit siirtää kohteita varastopaikasta toiseen **Siirtotyökirja**-ikkunassa ilman viittausta lähdeasiakirjaan. Lisätietoja on kohdassa [Nimikkeiden siirtäminen laajennetussa varastointimäärityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Fyysisen varastoinnin poiminta-asiakirjaa ei voi luoda alusta alkaen, koska poimintatoiminto on aina osa työnkulkua sekä pull- että push-menetelmässä.  

Voit luoda fyysisen varastoinnin poiminta-asiakirjan valitsemalla push-menetelmässä lähdeasiakirjassa **Luo F.var. poiminta** -toiminnon. Tällainen lähdeasiakirja voi olla esimerkiksi julkaistu kokoonpanotilaus tai fyysisen varaston toimitus. Lisätietoja on kohdassa [Nimikkeiden poiminta fyysisen varaston poiminnassa](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Vaihtoehtoisesti voit luoda varastopoiminta-asiakirjan tunnistamalla sekä toimitusten että sisäisten toimintojen poimintapyynnöt **Poimi työkirja** -ikkunassa ja luomalla sitten tarvittavat varastopoiminta-asiakirjat.  

Seuraavassa ohjeissa selitetään vetotilanne, jossa **Valitse työkirja** -ikkunassa poimitaan komponentteja vapautetulle tuotantotilaukselle. Menettely koskee myös kokoonpanotilauksia.  

Luodaksesi poimintapyynnöt sekä veto- että työntötilanteille, kyseiset lähdeasiakirjat on vapautettava. Vapauta sisäisten toimintojen lähdeasiakirjat seuraavilla tavoilla.  

 |Lähdeasiakirja|Vapautustapa|  
 |---------------------|--------------------|  
 |Tuotantotilaus|Muuta tilauksen tyypiksi vapautettu tuotantotilaus.|  
 |Kokoonpanotilaus|Muuta tilaksi Vapautettu.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Komponenttien poiminta poimintatyökirjoista  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Poimintatyökirja** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse ensin **Hae f. varastoinnin asiakirjat** -toiminto ja sitten komponenttirivit vapautetusta tuotantotilauksesta.  
3.  Käy rivit läpi, järjestele ne tehokkaaksi poimintakierrokseksi ja yhdistele niitä tarpeen mukaan muiden työkirjarivien kanssa siten, että työntekijän aika käytetään mahdollisimman tehokkaasti.  
4.  Valitse **Luo poiminta** -toiminto.  
5.  Määritä, miten voit luoda fyysisen varastoinnin poiminta-asiakirjat ja lajitella poimintarivit täyttämällä kentät **Luo poiminta** -ikkunassa.  
6.  Valitse **OK**-painike.

Varastopoiminta-asiakirjat on nyt luotu poimintarivien kanssa jokaiselle osalle, jota tarvitaan sisäisessä toiminnassa.

Jos sisäiselle toimintoalueelle, kuten tuotantokerrokselle, määritetään oletusvarastopaikka toiminnossa käytettävien komponenttien sijoitusta varten, tämä varastopaikkakoodi lisätään fyysisen varaston poiminta-asiakirjan Aseta-riveille. Se ohjaa varastotyöntekijöitä nimikkeiden sijoittamisessa paikoilleen. Lisätietoja on kohdassa [Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

## <a name="filling-the-consumption-bin"></a>Kulutuksen varastopaikan täyttäminen
Tämä työnkulkukaavio näyttää, miten tuotantotilauksen osarivien**Varastopaikkakoodi**-kenttä täytetään sijaintiasetusten mukaisesti.

![Varastopaikkojen vuokaavio](media/binflow.png "BinFlow")

## <a name="see-also"></a>Katso myös
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

