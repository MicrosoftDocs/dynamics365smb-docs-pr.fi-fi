---
title: Poimintojen suunnitteleminen työkirjassa | Microsoft Docs
description: Kun fyysisessä varastossa on määritetty pakolliseksi sekä poiminnan että toimituksen käsittely, fyysisessä varastossa voidaan valita, että toimitusasiakirjojen rivejä ei muuteta automaattisesti poimintaohjeiksi, vaan ne määritetään saatavilla oleviksi poimintatyökirjaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 55ac86ff992709bb454eaadfa65d8d5eed98732e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782582"
---
# <a name="plan-picks-in-worksheets"></a>Poimintojen suunnitteleminen työkirjoissa

Kun fyysisessä varastossa on määritetty pakolliseksi sekä poiminnan että toimituksen käsittely, fyysisessä varastossa voidaan valita, että toimitusasiakirjojen rivejä ei muuteta automaattisesti poimintaohjeiksi, vaan ne määritetään saatavilla oleviksi poimintatyökirjaan.  

> [!NOTE]  
> Jos fyysisen varastoinnin poimintaohjeet on jo luotu ja haluaisit yhdistää ohjeet yhdeksi tehokkaaksi poimintaohjeeksi, poista fyysisen varastoinnin yksittäiset poiminnat. Poimittavat rivit voidaan nyt näyttää työkirjassa.  

Poimintatyökirjassa työntekijöille voidaan määrittää poimintaluetteloita, joiden avulla minimoidaan työntekijöillä fyysisen varastoinnin poimintanimikkeiden siirtelyyn kuluva aika. Sovelluksessa on kenttiä, joissa on tietoja laiturointivarastopaikoissa saatavilla olevien nimikkeiden määristä. Laiturointitilanteissa on hyödyllistä suunnitella työtehtäviä, koska sovellus ehdottaa aina poimintaa laiturointivarastopaikasta ennen muita varastopaikkoja mittayksiköstä riippumatta. Työkirjassa olevat rivit voivat olla peräisin useista lähdeasiakirjoista, ja ne voidaan lajitella nimikkeen, hyllynumeron, lähdeasiakirjan, eräpäivän tai toimitusasiakkaan osoitteen mukaan.  

Jos järjestelet eräpäivän mukaan, voit valita poistavasi työkirjasta kaikki rivit paitsi ne, jotka vaativat välitöntä huomiota. Vähemmän kiireellisiä rivejä ei suoraan poisteta, vaan ne lähetetään takaisin **Poiminta valinta** -työkirjaan. Kun luot poiminnan, rivit on jo järjestelty eräpäivän mukaan, ja voit valita määritteleväsi poiminnan tietylle työntekijälle.  

> [!NOTE]  
> Toimitettavaa myyntitilausta varten kokoonpantavien nimikkeiden fyysisen varastoinnin toimituksessa noudatetaan samoja vaiheita kuin tavallisen fyysisen varastoinnin poiminnoissa toimitusta varten, kuten tässä ohjeaiheessa on kuvattu. Poimittavien rivien määrä toimitettavan määrän mukaan voi kuitenkin olla monta yhteen, koska poimittavana ovat komponentit eikä kokoonpanon nimike.  
>
> Fyysisen varastoinnin poimintarivit luodaan kokoonpanotilauksen **Jäljellä oleva määrä** -kentässä olevalle arvolle; kyseinen kokoonpanotilaus on linkitetty toimitettavaan myyntitilausriviin. Tämä varmistaa, että kaikki osat kerätään yhdellä kerralla.  
>
> Lisätietoja on ohjeaiheen Fyysisen varaston toimitus kohdassa Kokoonpano tilausta varten -nimikkeiden käsitteleminen fyysisen varastoinnin toimituksissa.  
>
> Lisätietoja kokoonpanotilausten komponenttien poiminnasta yleensä (mukaan lukien tilanteet, joissa kokoonpanon nimike ei eräänny myyntitoimituksen yhteydessä) on kohdassa [Kokoonpano- tai tuotantopoiminta laajennetuissa varastointimäärityksissä](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="to-plan-picks-in-the-worksheet"></a>Poimintojen suunnitteleminen työkirjassa

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poimintatyökirja** ja valitse sitten liittyvä linkki.  
2. Valitse **Hae f. varastoinnin asiakirjat** -toiminto.  
3. Valitse toimitukset, joille haluat valmistella poiminnan. Rivejä voi nyt järjestellä tiettyyn pisteeseen asti, mutta tässä tekemääsi järjestystä ei siirretä poimintaohjeeseen. Voit myös poistaa joitain rivejä tehokkaamman poiminnan tekemiseksi. Esimerkiksi jos on useita rivejä, joilla on nimikkeitä laiturointivarastopaikoissa, voit haluta luoda poiminnan kaikille riveille, jotka liittyvät kyseisiin riveihin. Laituroidut nimikkeet toimitetaan (muiden toimituksissa olevien nimikkeiden kanssa), ja näin laiturointivarastopaikkoihin tulee tilaa uusille saapuville nimikkeille.  
4. Valitse **Luo poiminta** -toimina ja täytä **Luo poiminta** -pyyntösivun tiedot. Tässä pyytämäsi järjestely lajittelee luomasi poimintarivit. Voit esimerkiksi luoda yhden poiminnan kullekin alueelle ja järjestellä rivit varastopaikan luokittelulla jokaisessa poiminnassa.  
5. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Fyysisen varaston poiminnat** ja valitse sitten liittyvä linkki. Avaa **Fyysisen varaston poiminnat** -ikkuna avautuu.  
6. Löydät juuri luomasi poimintatehtävän valitsemalla poiminnan, jonka numero on suurin.  
7. Poiminnassa voit silti tarpeen mukaan muuttaa määriteltyä käyttäjätunnusta ja tapaa, jolla rivit järjestellään.  
8. Tulosta poimintaohjeet valitsemalla **Tulosta**.  
9. Valitse poiminnan suorittamisen jälkeen **Rekisteröi**-toiminto.  

Jos varastopaikat on numeroitu tavalla, joka kuvastaa fyysisen varaston järjestystä, varastopaikan koodin mukaan järjestetyt rivit mahdollistavat sen, että poimija voi poimia useita toimituksia yhdellä fyysisen varaston kierroksella. Työntekijä ottaa vaaditun määrän nimikkeitä kullekin toimitusriville kustakin varastopaikasta ja sijoittaa ne muiden nimikkeiden kanssa tiettyä toimitusta varten. Poimija voi säästää paljon aikaa poimimalla useaa toimitusta varten yhdellä käynnillä varastopaikkaan.  

Toinen tehokas järjestelyvaihtoehto on varastopaikan luokittelu, jos fyysisen varaston järjestely vastaa enemmän varastopaikan luokittelua kuin varastopaikan koodia.  

Poimintatyökirjassa voi järjestellä myös toimitusosoitteen mukaan, niin että tilauksia voi kerätä ja toimittaa ensin kaukaisille asiakkaille.  

## <a name="see-also"></a>Katso myös

[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]