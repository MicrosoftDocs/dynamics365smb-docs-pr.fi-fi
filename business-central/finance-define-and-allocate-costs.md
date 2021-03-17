---
title: Kustannusten määrittäminen ja kohdistaminen | Microsoft Docs
description: Kustannusten kohdistukset siirtävät kustannukset ja tuotot eri kustannustyyppien, kustannuspaikkojen ja kustannuskohteiden välillä. Voit määrittää niin monta kodhistusta kuin on tarpeen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9d4167751289b26926bdde3148d6f2241df787cf
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388597"
---
# <a name="defining-and-allocating-costs"></a>Kustannusten määrittäminen ja kohdistaminen
Kustannusten kohdistukset siirtävät kustannuksia ja tuottoja eri kustannustyyppien, kustannuspaikkojen ja kustannuskohteiden välillä. Voit määrittää niin monta kodhistusta kuin on tarpeen. Jokainen kohdistus koostuu:  

-   Kohdistamisen lähde.  
-   Vähintään yksi kohdistuskohde.  

Kohdistuksen lähde määrittää, mitkä kustannukset täytyy kohdistaa sekä kohdistustavoitteet määrittävät, missä kustannukset on kohdistettava. Esimerkiksi kohdistuksen lähde voi olla Sähkö ja lämmitys -kustannuslajin kustannukset. Kohdista kaikki sähkö ja lämmityskustannukset kolmeen kustannuspaikkaan: korjaamo, tuotanto ja myynti. Näihin kustannuspaikkoihin kohdistetaan kohteita.  

Määritä jokaiselle kohdistuksen lähteelle kohdistustaso, voimassaoloaika ja variantti ryhmittelyn tunnukseksi. Erätyön avulla voit määrittää suodattimia valitaksesi kohdistusmääritelmiä ja suorittaaksesi sitten kustannusten kohdistukset automaattisesti.  

Määritä jokaiselle kohdistuksen kohteelle kohdistusperuste. Kohdistusperuste voi olla joko staattinen tai dynaaminen.  

-   Staattinen kohdistaminen perustuu määriteltyihin arvoihin, kuten pinta-alaan tai vahvistettu-varaus -suhteeseen, esimerkiksi 5:2:4.  
-   Dynaaminen kohdistus perustuu muutettaviin arvoihin, kuten työntekijöiden määrään kustannuspaikassa, kustannuskohteen myyntituottoihin tiettynä aikajaksona.  

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.

## <a name="setting-up-allocation-source-and-targets"></a>Kohdistuksen lähteen ja sen tavoitteiden määrittäminen
Jokainen kohdistus koostuu kohdistuslähteestä ja sekä vähintään yhdestä kohdistuskohteesta. Kohdistuksen lähde määrittää, mitkä kustannukset kohdistetaan. Kohdistuskohteet määrittävät, mihin kustannukset kohdistetaan.  

### <a name="to-set-up-cost-allocations"></a>Määritä kustannusten kohdistamiset  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kustannusten kohdistaminen** ja valitse sitten liittyvä linkki.  
2.  Valitse **Kustannusten kohdistaminen** -sivulla **Muokkaa**-toiminto.  
3.  Kirjoita tunnus kohdistuslähteelle **Tunnus**-kentässä.  
4.  Määritä taso numerona väliltä 1-99 **Taso**-kentässä Kohdistuksen kirjauksen tulee noudattaa tasojen järjestystä.  
5.  Syötä kustannustyyppi, joka määrittää mitkä kustannukset kohdistetaan **Kustannustyypin väli** -kentässä. Jos kustannustyypin kaikki kustannukset on kohdistettu, alueväliä ei ole määritetty.  
6.  Määritä kustannuspaikka ja kustannukset, jotka kohdistetaan **Kustannuspaikan koodi** -kentässä.  
7.  Määritä kustannusobjekti ja kustannukset, jotka kohdistetaan **Kustannusobjektin koodi** -kentässä. Tämä kenttä pysyy useimmiten tyhjänä, koska kustannuskohteet kohdistetaan harvoin toisiin kustannuskohteisiin.  
8.  Syötä kustannustyyppi **Luotto kustannustyyppiin** -kenttään. Kohdistetut kustannukset hyvitetään lähdekustannustyypille. Hyvityskirjaus kirjataan tässä annettuun kustannustyyppiin.  
9. Määritä **Rivit**-pikavälilehdessä kohdistuksen kohteet. Valitse **Kohdekustannustyyppi** -kentässä ensimmäisellä rivillä kustannustyyppi. Se määrittää, mille kustannustyypille kohdistaminen veloitetaan.  
10. Anna ensimmäisellä rivillä ensimmäinen kohdistuskohde **Kohdekustannuspaikka** -kenttää tai **Kohdekustannuskohde** -kenttään. Nämä kaksi kenttää määrittävät, mistä kustannuspaikasta tai kustannuskohteesta kohdistaminen veloitetaan. Voit täyttää vaon yhden näistä kentistä, mutta et molempia.  
11. Toista samat vaiheet toisella rivillä määrittääksesi lisäkohdistustavoitteet.  
12. Kun olet määrittänyt kohdistuksen kohteet ja lähteet, laske kokonaisjakauma-arvot valitsemalla **Laske kohdistusavain** -toiminto.  

> [!NOTE]  
>  Deaktivoi kohdistamisen määritys valitsemalla **Estetty** -valintaruutu.

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Suodattimien määrittäminen dynaamisen kohdistuksen perusteille.
Dynaaminen kohdistusmenetelmä on perustuu muutettaviin arvoihin. Esimerkiksi kustannuspaikan työntekijöiden tai kustannuskohteen myytyjen nimikkeiden määrä tietyn ajanjakson aikana. Ohjelmassa on yhdeksän ennalta määritettyä kohdistamisen perustetta ja kaksitoista dynaamista päivämääräväliä. Voit määrittää eri suodattimia kohdistuksen perusteella.  

### <a name="setting-filters-for-dynamic-allocation-bases"></a>Suodattimien määrittäminen dynaamisen kohdistuksen perusteille.  
 Seuraavassa taulukossa on esitetty mitä suodattimia on mahdollista käyttää eri kohdistusperusteille ja mitkä arvot ovat mahdollisia **Nrosuodatus**- ja **Ryhmäsuodatus**-kentissä. Paina F1-näppäintä **Päivämäärän suodatuskoodi** -kentässä, jos haluat lukea yksityiskohtaiset kuvaukset.  

|**Peruste**|**Nro suodatus**|**Päivämäärän suodatuskoodi**|**Kustannuspaikkasuodatus**|**Kustannuskohdesuodatus**|**Ryhmäsuodatus**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|KP-tapahtumat|KP-tili|Kyllä|Kyllä|Kyllä|Ei saatavilla|  
|KP-budjetin tapahtumat|KP-tili|Kyllä|Kyllä|Kyllä|KP-budjetin nimi|  
|Kustannustyyppitapahtumat|Kustannustyyppi|Kyllä|Kyllä|Kyllä|Ei saatavilla|  
|Kustannusbudjettitapahtumat|Kustannustyyppi|Kyllä|Kyllä|Kyllä|Budjetin nimi|  
|Työntekijöiden määrä|Ei saatavilla|Kyllä|Kyllä|Kyllä|Ei saatavilla|  
|Nimikkeitä myyty (Määrä)|Nimikkeen nro|Kyllä|Kyllä|Kyllä|Varaston kirjausryhmä|  
|Nimikkeitä ostettu (Määrä)|Nimikkeen nro|Kyllä|Kyllä|Kyllä|Varaston kirjausryhmä|  
|Nimikkeitä myyty (Summa)|Nimikkeen nro|Kyllä|Kyllä|Kyllä|Varaston kirjausryhmä|  
|Nimikkeitä ostettu (Summa)|Nimikenro|Kyllä|Kyllä|Kyllä|Varaston kirjausryhmä|

## <a name="scenario-1-defining-static-allocations-based-on-allocation-ratio"></a>Skenaario 1: Kohdistamissuhteeseen perustuvan staattisen kohdistamisen määrittäminen
Staattinen kohdistaminen perustuu määriteltyihin arvoihin, kuten pinta-alaan tai vahvistettu-varaus -suhteeseen, esimerkiksi 5:2:4.  

Tässä aiheessa kuvataan, miten määrittää kolmen uuden kohdistuskohteen kustannuskohteet TUOT kustannuspaikoille käyttäen vahvistettu-varaus -suhdetta 5:2:4. Kolme kohdekustannuskohdetta ovat LISÄLAITT, MAALIT ja KALUSTO.  

> [!NOTE]  
>  Esimerkissä käytetään demodataa [!INCLUDE[prod_short](includes/prod_short.md)]:sta.  

### <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Määritä varauksen lähde TUOT kustannuspaikka yleisessä pikavälilehdessä  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kustannusten kohdistaminen** ja valitse sitten liittyvä linkki.  
2.  Valitse **Kustannusten kohdistaminen** -sivulla **Uusi**-toiminto.  
3.  Paina **Tunnus**-kentässä Enter tai kirjoita tunnus.  
4.  Syötä **Taso**-kenttään **1**.  
5.  Syötä arvot **Voimassaolo alkaa**- ja **Voimassaolo päättyy** -kenttiin.  
6.  Syötä **Kustanuspaikkakoodi**-kenttään **TUOT**.  
7.  Syötä **Luotto kustannustyyppiin** -kenttään kustannustyyppi **9903**.  

### <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Määritä kodhistuskohteen kustannus-objektit Rivit-pikavälilehdellä  

1.  Syötä laskun ensimmäiselle riville **Kohdekustannustyyppi**-kenttään **9903**.  
2.  Syötä ensimmäiselle riville **Kohdekustannuskohde**-kenttään **LISÄLAITT**.  
3.  Valitse ensimmäisen rivin **Kohdistuksen kohdetyyppi** -kentässä **Kaikki kustannukset** ja määritä, miten kaikki jaksotetut kustannukset kohdistetaan.  
4.  Valitse ensimmäisen rivin **Peruste**-kentässä **Staattinen**, jos haluat käyttää staattista kohdistusmenetelmää.  
5.  Anna ensimmäisen rivin **Jaa**-kentässä varaussuhde **5**.  
6.  Syötä toiselle riville **Kohdekustannustyyppi**-kenttään **9903**.  
7.  Syötä toiselle riville **Kohdekustannuskohde**-kenttään **MAALI**.  
8.  Valitse toiselle riville **Kohdistuksen kohdetyyppi** -kentässä **Kaikki kustannukset** ja määritä, miten kaikki jaksotetut kustannukset kohdistetaan.  
9. Valitse toisen rivin **Peruste**-kentässä **Staattinen**, jos haluat käyttää staattista kohdistusmenetelmää.  
10. Anna toisen rivin **Jaa**-kentässä varaussuhde **2**.  
11. Syötä kolmannelle riville **Kohdekustannustyyppi**-kenttään **9903**.  
12. Syötä kolmannelle riville **Kohdekustannuskohde**-kenttään **KALUSTO**.  
13. Valitse kolmannen rivin **Kohdistuksen kohdetyyppi** -kentässä **Kaikki kustannukset** ja määritä, miten kaikki jaksotetut kustannukset kohdistetaan.  
14. Valitse kolmannen rivin **Peruste**-kentässä **Staattinen**, jos haluat käyttää staattista kohdistusmenetelmää.  
15. Anna kolmannen rivin **Jaa**-kentässä varaussuhde **4**.  

> [!IMPORTANT]  
>  [!INCLUDE[prod_short](includes/prod_short.md)] laskee automaattisesti **Prosentti**-kenttään prosenttiarvon, joka määräytyy kaikkien niiden kolmen kohdistussuhteen mukaan, jotka syötetty **Osuus**-kenttään kaikilla kolmella rivillä.

## <a name="scenario-2-defining-dynamic-allocations-based-on-items-sold"></a>Skenaario 2: Dynaamisten kohdistamisten määrittäminen myytyjen nimikkeiden perusteella
Tässä aiheessa kuvataan esimerkki siitä, kuinka kohdistuksia määritetään käyttämällä dynaamista kohdistustapaa. Esimerkissä muutetaan MYYNTI-kustannuspaikan kustannusten dynaaminen kohdistaminen tukemaan uutta IT-LAITTEISTO -kustannuskohdetta. IT-LAITTEISTO-paketeissa ovat nimikenumerot välilä 8904-W – 8924-W. Osuus lasketaan edellisen vuoden myyntilukujen avulla. Kohdistus kirjataan apukustannuslajiin 9903.  

> [!NOTE]  
>  Esimerkissä käytetään demodataa [!INCLUDE[prod_short](includes/prod_short.md)]:sta.  

### <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Märitä edellisvuonna myyytihin nimikkeisiin perustuvat dynaamiset kohdistukset  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kustannusten kohdistukset** ja valitse sitten liittyvä linkki.  
2.  Valitse **Kustannusten kohdistaminen** -sivulla **Uusi**-toiminto.  
3.  Paina **Tunnus**-kentässä Enter tai kirjoita tunnus.  
4.  Syötä **Taso**-kenttään **1**.  
5.  Syötä arvot **Voimassaolo alkaa**- ja **Voimassaolo päättyy** -kenttiin.  
6.  Syötä **Kustannuspaikkakoodi**-kenttään **MYYNTI**.  
7.  Syötä **Luotto kustannustyyppiin** -kenttään kustannustyyppi **9903**.  
8.  Syötä **Kohdekustannustyyppi** -kenttään kustannustyyppi **9903**.  
9. Valitse **Kohdekustannuskohde**-kentässä **Uusi**, luo uusi kustannuskohde IT-LAITTEISTO ja täytä kentät tarpeen mukaan. Valitse **IT-LAITTEET**. Jätä **Kohdekustannuspaikka**-kenttä tyhjäksi.  
10. Valitse **Kohdistuksen kohdetyyppi** -kentässä **Kaikki kustannukset** ja määritä, miten kaikki kertyneet kustannukset kohdistetaan.  
11. Valitse **Peruste**-kentässä kohdistusperuste **Nimikkeitä myyty (summa)**.  
12. Syötä **Nro suodatus** -kenttään **8904-W..8924-W**.  
13. Syötä **Päivämäärän suodatuskoodi** -kenttään **Edellinen vuosi**.  
14. Valitse **Laske kohdistusavain** -toiminto ja laske osuus.  

> [!IMPORTANT]  
>  [!INCLUDE[prod_short](includes/prod_short.md)] käyttää edellisen vuoden myyntilukuja laskettaessa 1596.50 PVA:n 100 prosentin osuus IT-LAITTEISTO -paketteja varten. Tämä tarkoittaa sitä, että kaikki viime vuonna myydyt nimikkeet kohdennetaan kustannuskohteelle IT-LAITTEISTO.

## <a name="see-also"></a>Katso myös  
 [Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md)   
 [Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md)   
 [Kustannuslaskenta](finance-manage-cost-accounting.md)   
 [Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md)   
 [Tietoja kustannuslaskennasta](finance-about-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]