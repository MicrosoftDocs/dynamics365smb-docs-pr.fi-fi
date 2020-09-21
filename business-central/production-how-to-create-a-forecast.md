---
title: Kysyntäennusteen luominen | Microsoft Docs
description: Voit luoda myynti- ja tuotantoennusteita **Kysyntäennuste**-sivulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 6935f96c39ae378ddd8fa960c574f150bba16328
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3777764"
---
# <a name="create-a-demand-forecast"></a>Kysyntäennusteen luominen
Voit luoda myynti- ja tuotantoennusteita **Kysyntäennuste**-sivulla.  

Ennustetoimintojen avulla käyttäjä voi luoda ennakoitua kysyntää; toteutunut kysyntä on peräisin myynti- ja tuotantotilauksista. Tuotanto-ohjelmaa luotaessa ennuste nettoutetaan myynti- ja tuotantotilauksiin verraten. Ennusteen *Komponentti*-vaihtoehto määrittää, minkä tyyppiset vaatimukset nettouttamisessa otetaan huomioon. Jos ennuste koskee myyntinimikettä, ennuste nettoutetaan vain myyntitilauksiin verraten. Jos kyseessä ovat komponentit, ennuste nettoutetaan vain tuotantotilausten komponenttien ei-itsenäiseen kysyntään verraten.  

Ennustetoiminnon avulla yritys voi luoda "mitä jos" -tyyppisiä mallinnuksia ja tehdä kysyntään perustuvia suunnitelmia tehokkaasti sekä taloudellisesti. Tarkoilla ennusteilla voi olla ratkaiseva vaikutus asiakkaiden tyytyväisyyteen, koska toimitusajat voidaan määrittää tarkasti ja toimitukset tehdä ajallaan.  

## <a name="sales-forecasts-and-production-forecasts"></a>Myyntiennusteet ja tuotantoennusteet  
Sovelluksen ennustetoimintoja voidaan käyttää joko yhdistettyjen tai erillisten myynti- tai tuotantoennusteiden luomiseen. Esimerkiksi useimmat tilauspohjaista tuotantoa harjoittavat yritykset eivät pidä tuotteita valmiina varastossa, koska nimikkeitä tuotetaan tilausten mukaan. Tilausten ennakoiminen (myyntiennuste) on kriittisen tärkeää valmiiden tuotteiden kohtuullisen odotusajan varmistamiseksi (tuotannon ennuste). Esimerkiksi osien pitkät toimitusajat, jos niitä ei ole tilattu tai ei ole varastossa, voivat viivyttää tuotantoa.  

-   Myyntiennuste on myyntiosaston paras arvio tulevista myyntimääristä; se on nimike- ja jaksokohtainen. Myyntiennuste ei kuitenkaan aina riitä tuotannon määrittämiselle.  
-   Tuotantoennuste on tuotantosuunnittelijan ennuste siitä, miten monta loppunimikettä ja johdettua osakokoonpanoa tiettyjen jaksojen aikana on tuotettava, jotta ennustettu myynti saavutetaan.  

Tuotannon suunnittelija muokkaakin myyntiennustetta useimmiten tuotannon edellytysten mukaisesti, mutta siten, että myyntiennuste kuitenkin täyttyy.  

Voit luoda ennusteita manuaalisesti **Kysyntäennuste**-sivulla. Järjestelmässä voi olla useita erinimisiä ja erityyppisiä ennusteita. Ennusteita voi tarvittaessa kopioida ja muokata. Muistathan, että vain yksi ennuste kerrallaan kelpaa suunnittelun pohjaksi.  

Ennusteessa on joukko tietueita, joista jokaisessa on nimikkeen numero, ennustepäivämäärä ja ennustettava määrä. Nimikkeen ennuste kattaa tietyn jakson, jonka määrittävät ennustepäivämäärä sekä seuraavan (myöhäisemmän) ennustetietueen ennustepäivämäärä. Suunnittelun kannalta ennustettavan määrän pitäisi olla käytettävissä kysyntäjakson alussa.  

Määritä ennusteen mukaan *Nimikkeen myynti*, *Osa* tai *Molemmat*. Ennustetyyppiä *Myyntinimike* käytetään myynnin ennusteissa. Tuotantoennuste on luotu käyttämällä *Osa*-tyyppiä. Ennustetyyppiä *Molemmat* käytetään ainoastaan antamaan suunnittelijalle yleiskuva sekä myynti- että tuotantoennusteesta. Tässä vaihtoehdossa tuotantoennusteen tapahtumat eivät ole muokattavia. Määrittämällä nämä ennustetyypit tässä, voit käyttää samaa työkirja määrittääksesi myyntiennusteen ja tuotantoennusteen, sekä tarkastella molempia ennusteita samanaikaisesti samalta lomakkeelta. Huomaa, että järjestelmä kohtelee eri tuotantopanoksia (myynti ja tuotanto) eri tavalla laskettaessa suunnittelumäärityksiä, nimikeperusteisia määrityksiä sekä valmistus- ja tuotantomäärityksiä.  

## <a name="component-forecast"></a>Komponenttiennuste  
Komponenttiennustetta voisi pitää vaihtoehtoisena ennusteena suhteessa päänimikkeeseen. Siitä voi olla hyötyä, jos suunnittelija voi esimerkiksi ennakoida komponentin kysynnän.  

Koska komponenttiennuste on suunniteltu määrittämään päänimikkeen vaihtoehdot, komponenttiennusteen pitäisi olla yhtä suuri tai pienempi kuin myyntinimikkeen ennusteen määrä. Jos komponenttiennuste on suurempi kuin myyntinimikkeen ennuste, järjestelmä käsittelee näiden kahden ennustetyypin erotusta erillisenä kysyntänä.  

## <a name="forecasting-periods"></a>Ennustejaksot  
 Ennustejakso on kelvollinen alkamispäivämäärästä seuraavan ennusteen alkamispäivämäärään saakka. Aikavälisivulla on useita vaihtoehtoja, joiden avulla voit lisätä kysynnän tiettyyn jakson päivämäärään. Sen vuoksi ennustejakson pituutta ei kannatakaan muuttaa, jos aloituspäivämäärän kaikkia ennustetapahtumia ei ole tarkoitus siirtää tämän jakson alkamispäivämäärään.  

## <a name="forecast-by-locations"></a>Ennusteet sijainnin mukaan  
Jos haluat suodattaa ennusteen sijainnin mukaan suunnitelman laskemisen yhteydessä, voit osoittaa sen tuotannon asetuksissa. Huomaathan kuitenkin, että jos sijaintiperustaisia ennusteita tarkastellaan erillään muista, kokonaisennuste ei välttämättä ole totuudenmukainen.

## <a name="to-create-a-demand-forecast"></a>Kysyntäennusteen luominen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kysyntäennuste** ja valitse sitten liittyvä linkki.  
2. Valitse **Yleinen**-pikavälilehden **Kysyntäennusteen nimi** -kentässä ennuste. Ennusteita voi olla useita erinimisiä ja -tyyppisiä.  
3. Valitse **Sijaintisuodatus**-kentässä sijainti, jota tämä ennuste koskee.
4. **Näyttösivu** -kentässä voit muuttaa sarakkeissa näkyvän jakson. Mahdollisia valittavia aikavälejä ovat **Päivä**, **Viikko**, **Kuukausi**, **Vuosineljännes**, **Vuosi** tai taloushallinnossa määritetty **Kirjanpitojakso**.    

> [!NOTE]  
>  Kannattaa miettiä, mitä aikavälejä tulevissa ennusteissa käytetään, jotta aikaväli pysyy koko ajan yhdenmukaisena. Kun lisäät ennusteen määrän, se on voimassa valitsemasi aikavälin ensimmäisenä päivänä. Jos esimerkiksi valitset kuukauden, ennusteen määrä lisätään kuukauden ensimmäiselle päivälle. Jos valitset vuosineljänneksen, ennusteen määrä lisätään vuosineljänneksen ensimmäisen kuukauden ensimmäiselle päivälle.

5. Valitse **Näyttömuoto**-kentässä, miten aikavälin ennustemäärät näytetään. Jos valitset **Nettomuutos**, aikaväliltä näytetään saldon nettomuutos. Jos valitset **Saldo pvm:ttäin**, sivulla näkyy aikavälin viimeisen päivän saldo.  
6. Valitse **Ennusteen tyyppi** -kentässä **Myyntinimike**,  **Komponentti** tai **Molemmat**. Jos valitset **Myyntinimike** tai **Komponentti**, voit muokata määrää jakson mukaan. Jos valitset **Molemmat**, määrää ei voi muuttaa, mutta voit valita alanuolipainikkeen ja tarkastella kysyntäennustetapahtumia.  
7. Määritä **Pvm-suodatus**, jos haluat rajoittaa näkyvien tietojen määrää.  
8. Syötä ennustetut määrät pikavälilehdellä **Kysynnän ennustematriisi** kirjoittamalla määrä soluun, joka edustaa nimikettä tiettynä päivämääränä tai jakson aikana. Huomaa, että tyhjissä soluissa hakupainike avaa tyhjän sivun, joka ilmaisee, että arvo täytyy syöttää manuaalisesti.   

> [!NOTE]  
>  Voit myös muokata olemassa olevaa ennustetta. Valitse **Kysyntäennustematriisi**-sivulla **Kopioi kysyntäennuste** -toiminto ja lisää aiemmin luodun ennusteen tiedot **Kysyntäennuste**-sivulle. Sen jälkeen voit tehdä tarvittavat muutokset määriin.  

## <a name="see-also"></a>Katso myös  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md)   
[Asetukset - parhaat käytännöt: toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
