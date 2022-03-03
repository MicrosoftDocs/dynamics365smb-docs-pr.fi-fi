---
title: Poimintojen suunnitteleminen työkirjassa
description: Tietoja toimitusasiakirjojen rivien tuomisesta käyttöön varastotyöntekijöiden poiminnan työkirjoissa.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/13/2021
ms.author: edupont
ms.openlocfilehash: fbb85d69cdd7844bbc63e6367ea962897ab30478
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144305"
---
# <a name="plan-picks-in-worksheets"></a>Poimintojen suunnitteleminen työkirjoissa

Jos varasto on määritetty edellyttämään sekä poiminnan että toimituksen käsittelyä, toimitusasiakirjojen rivit on mahdollista valita käytettäviksi poiminnan työkirjoissa poimintaohjeiden sijaan.  

> [!NOTE]  
> Jos varastoinnin poimintaohjeet on jo luotu ja haluat yhdistää ohjeet yhdeksi poimintaohjeeksi, varastoinnin yksittäiset poiminnat on poistettava. Poimittavat rivit voidaan nyt näyttää poiminnan työkirjassa.  

**Poiminnan työkirjat** -sivulla voidaan määrittää poimintaluettelot, jotka auttavat työntekijöitä keräämään nimikkeitä varastossa. Sivulla näkyy määrät, jotka ovat saatavana laiturointivarastopaikoissa, mikä on kätevää suunniteltaessa työtehtäviä laiturointitilanteissa. [!INCLUDE[prod_short](includes/prod_short.md)] ehdottaa aina ensin poimimista laiturointivarastopaikasta. Työkirjan rivit voidaan saada useasta lähdeasiakirjasta. Ne voivat tulla esimerkiksi useammasta kuin yhdestä myyntitilauksesta. 

> [!NOTE]  
> Toimitettavaa myyntitilausta varten koottavien nimikkeiden poiminnassa noudatetaan samoja vaiheita kuin toimituksissa tavallisessa varastoinnissa. Poimittavien rivien määrä toimitettavan määrän mukaan voi kuitenkin olla monta yhteen, koska poimittavana ovat komponentit eikä kokoonpanon nimike.  
>
> Fyysisen varastoinnin poimintarivit luodaan kokoonpanotilauksen **Jäljellä oleva määrä** -kentässä olevalle arvolle; kyseinen kokoonpanotilaus on linkitetty toimitettavaan myyntitilausriviin. Tämä varmistaa, että kaikki osat kerätään yhdellä kerralla. Lisätietoja on kohdassa [Varastonimikkeiden myyminen Kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  
>
> Lisätietoja kokoonpanotilausten komponenttien poiminnasta yleensä (mukaan lukien tilanteet, joissa kokoonpanon nimike ei eräänny myyntitoimituksen yhteydessä) on kohdassa [Kokoonpano- tai tuotantopoiminta laajennetuissa varastointimäärityksissä](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="sorting-lines-on-a-pick-worksheet"></a>Lajittelurivit poiminnan työkirjassa
Rivejä voidaan lajitella nimikkeen, hyllynumeron, lähdeasiakirjan, eräpäivän tai kohteen mukaan. Lajittelu voi olla kätevää esimerkiksi seuraavin tavoin.

* Jos lajittelu tehdään eräpäivän mukaan, voit valita kaikkien muiden rivien poiston paitsi ne rivit, jotka vaativat välitöntä huomiota. Vähemmän kiireellisiä rivejä ei suoraan poisteta, vaan ne lähetetään takaisin **Poiminta valinta** -työkirjaan. Kun luot poiminnan, rivit on jo lajiteltu eräpäivän mukaan ja voit valita poiminnan määrittämisen työntekijälle.
* Jos varastopaikat on numeroitu varaston fyysistä asettelua vastaavaksi, rivien lajittelu varastopaikan numeroiden mukaan helpottaa useiden toimitusten poimimista samanaikaisesti. 
* Jos käytössä on varastopaikkojen luokittelu, lajittelu luokittelun mukaan voi säästää aikaa. 
* Kohteen mukainen lajittelu antaa mahdollisuuden koota ja lähettää tilauksia asiakaskohtaisesti.

## <a name="to-plan-picks-in-the-worksheet"></a>Poimintojen suunnitteleminen työkirjassa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poimintatyökirja** ja valitse sitten vastaava linkki.  
2. Valitse **Hae f. varastoinnin asiakirjat** -toiminto.  
3. Valitse toimitukset, joille haluat valmistella poiminnan. Vaikka rivit voidaan lajitella, lajittelua ei käytetä poimintaohjeessa. Voit myös poistaa joitain rivejä tehokkaamman poiminnan tekemiseksi. Jos esimerkiksi useilla riveillä on nimikkeitä, joita ovat laiturointivarastopaikoissa, kaikkien rivien poiminta voidaan luoda. Laituroidut nimikkeet toimitetaan (muiden toimituksissa olevien nimikkeiden kanssa), ja näin laiturointivarastopaikkoihin tulee tilaa uusille saapuville nimikkeille.  
4. Valitse **Luo poiminta** -toiminto ja täytä **Luo poiminta** -sivun tiedot. Tässä pyytämäsi järjestely lajittelee luomasi poimintarivit. Voit esimerkiksi luoda yhden poiminnan kullekin alueelle ja järjestellä rivit varastopaikan luokittelulla jokaisessa poiminnassa.  
5. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston poiminnat** ja valitse sitten vastaava linkki. Avaa **Fyysisen varaston poiminnat** -ikkuna avautuu.  
6. Poimintatehtävä löytyy valitsemalla poiminta, jonka numero on suurin.  
7. Tarvittaessa voidaan määrittää toinen käyttäjä tai rivit voidaan lajitella eri tavalla.  
8. Tulosta poimintaohjeet valitsemalla **Tulosta**.  
9. Valitse poiminnan valmistumisen jälkeen **Rekisteröi**-toiminto.  

## <a name="see-also"></a>Katso myös

[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]