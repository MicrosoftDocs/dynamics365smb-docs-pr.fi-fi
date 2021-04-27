---
title: Komponenttien materiaalinotto toiminnan tuotoksen mukaan
description: Jos nimikkeiden määrityksessä on käytetty Taaksepäin-materiaalinottotapaa, oletustoiminto laskee ja kirjaa kulutuksen automaattisesti, kun vapautetun tuotantotilauksen tilaksi muutetaan Valmis.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d1448b9105426103d70abfb820bd38b6adb41db8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779251"
---
# <a name="flush-components-according-to-operation-output"></a>Komponenttien materiaalinotto toiminnan tuotoksen mukaan
Voit määrittää erilaisia materiaaliottostrategioita automatisoimaan komponenttien kulutuksen rekisteröintiä. 

Tuotantotilauksessa voidaan esimerkiksi määrittää, että 800 metrin tuottaminen vaatii 8 kg komponentteja. Jos tuotokseksi kirjataan 200 metriä, kulutukseksi kirjataan automaattisesti 2 kg. 

Tämä toiminto on hyödyllinen seuraavista syistä:  

- **Varaston arvostus**

    Tuotoksen ja kulutuksen arvotapahtumat luodaan rinnakkain tuotantotilauksen edetessä. Ilman reitityslinkkien koodeja varastoarvo kasvaa, kun tuotos kirjataan ja vähenee sitten myöhemmin, kun komponentin kulutusarvo kirjataan yhdessä valmiin tuotantotilauksen kanssa.  
- **Varastosaatavuus**

    Asteittaista kulutuskirjausta käytettäessä komponenttinimikkeiden saatavuus on paremmin ajan tasalla, mikä on tärkeää kysynnän ja tarjonnan välisen sisäisen tasapainon ylläpitämiseksi. Ilman reitityslinkkien koodeja muut osan vaatimukset voivat olettaa, että se on käytettävissä, niin kauan kuin se odottaa viivästynyttä kulukirjausta.  
- **Just-in-Time**

    Voit mukauttaa tuotteita asiakkaan pyyntöjen mukaan ja siten minimoida jätteet varmistamalla, että työ- ja järjestelmämuutoksia tehdään vain tarvittaessa.  

Se tehdään yhdistämällä taaksepäin suuntautuvan materiaalinottomenetelmä ja reitityslinkkien koodit siten, että materiaalinottomäärä toimintoa kohden on verrannollinen toiminnon todelliseen tuotokseen. Jos nimikkeiden määrityksessä on käytetty Taaksepäin-materiaalinottotapaa, oletustoiminto laskee ja kirjaa kulutuksen automaattisesti, kun vapautetun tuotantotilauksen tilaksi muutetaan **Valmis**. Jos määrität myös reitityslinkin koodeja, laskenta ja kirjaus tehdään toiminnon valmistuttua. Toiminnon kuluttama todellinen määrä kirjataan. Lisätietoja on kohdassa [Reititysten luominen](production-how-to-create-routings.md).  

## <a name="to-flush-components-according-to-operation-output"></a>Voit tyhjentää osat toiminnon tuotoksen mukaan

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.  
2.  Valitse **Muokkaa** -toiminto.  
3.  Valitse **Täydennys**-pikavälilehden **Materiaalinottotapa**-kentässä **Taaksepäin**.  

    > [!NOTE]  
    >  Valitse **Poiminta + taaksepäin**, jos komponenttia käytetään ohjatuille hyllytyksille ja poiminnoille määritetyssä sijainnissa.  

4.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Reititykset** ja valitse sitten liittyvä linkki.  
5.  Määritä reitityslinkkikoodit jokaiselle työvaiheelle, joka kuluttaa komponentin. Lisätietoja on kohdassa [Reititysten luominen ](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > Älä käytä samaa reitityslinkkiä reitityksen eri toiminnoille, sillä silloin kunkin linkitetyn toiminnon komponentin kulutus rekisteröidään.  
6.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Tuotannon tuoterakenne** ja valitse sitten liittyvä linkki.  
7.  Määritä reitityslinkkikoodit kustakin komponentin esiintymästä toimintoon, jossa se kulutetaan.

Kulutus kirjataan automaattisesti, kun tuotos rekisteröidään. Lisätietoja on kohdassa [Tuotoksen ja ajoaikojen eräkirjaaminen](production-how-to-post-output-quantity.md).

## <a name="flushing-methods"></a>Materiaalinottotavat

Seuraavassa taulukossa käsitellään käytettävissä olevia materiaaliottomenetelmien vaihtoehtoja, jotka voidaan määrittää **Nimike**- ja **Varastointiyksikkö**-korteissa.

|Asetus|Kuvaus|
|------------|-------------|  
|Manuaalinen|Edellyttää, että annat ja kirjaat kulutuksen manuaalisesti kulutuspäiväkirjaan.|
|Eteenpäin|Kirjaa kulutuksen automaattisesti tuotantotilauksen osarivien mukaan. <br><br>Oletusarvon mukaan komponentin kulutuksen kirjaus tapahtuu, kun tuotantotilauksen tila muutetaan **vapautetuksi**. Jos kuitenkin käytät tuotantotilauksen komponenttirivien **Reitityslinkin** koodi -kenttää, kirjaukset tehdään toiminnoittain toiminnon käynnistyessä. Lisätietoja on kohdassa [Reitityslinkkien luominen](production-how-to-create-routings.md#to-create-routing-links). <br><br> **Huomautus**<br>Eteenpäin tapahtuvassa materiaalinotossa reitityslinkin koodien yhteydessä saatava toimintokohtainen kirjaus perustuu komponenttirivillä määritettyyn oletettuun määrään. Lisätietoja toimintokohtaisista materiaalinotoista toteutuneen tuloksen mukaan on tämän aiheen **Taaksepäin**-kuvauksessa.<br><br>Jos sijainnille tai resursseille, joissa tämä komponentti kulutetaan, on määritetty varastopaikan oletusrakenne, nimike kulutetaan **avoimen tuotannon varastopaikasta**. Lisätietoja on kohdassa [Toimintaohje: Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md). <br><br> **Tärkeää** <br>Eteenpäin suuntautuva materiaalinotto tapahtuu myös, kun valitset tyhjästä luodussa vapautetussa tuotantotilauksessa **Päivitä**. Näissä suoraan luoduissa vapautetuissa tuotantotilauksissa ei voi muuttaa varastopaikkatietoja, koska tuotantotilauksen komponenttirivit luodaan tilauksen päivityksen yhteydessä, jolloin komponentteja samalla siirretään eteenpäin. Jos siis halutaan muuttaa tuotantotilauksen osarivien varastopaikkatietoa ennen tyhjennyksen tapahtumista, luotavan tilauksen tilan on oltava *Suunniteltu* tai *Sitovasti suunniteltu*.|
|Taaksepäin|Laskee ja kirjaa kulutuksen automaattisesti tuotantotilauksen osarivien mukaan.<br><br> Oletusarvon mukaan komponentin kulutuksen laskenta ja kirjaus tapahtuu, kun vapautetun tuotantotilauksen tilaksi muutetaan **Valmis**. Jos kuitenkin käytät tuotantotilauksen komponenttirivien **Reitityslinkin koodi** -kenttää, laskennat ja kirjaukset tehdään kunkin toiminnon päättyessä.<br><br> **Huomautus** <br>Taaksepäin suuntautuvat materiaalinoton ja reitityslinkkien koodit voidaan yhdistää niin, että materiaalinottomäärä toimintoa kohden on verrannollinen toiminnon todelliseen tuotokseen. Lisätietoja on kohdassa [Komponenttien materiaalinotto toiminnan tuotoksen mukaan](#to-flush-components-according-to-operation-output).<br><br> Jos sijainnille tai kuormitusryhmälle, jossa tämä komponentti kulutetaan, on määritetty varastopaikan oletusrakenne, nimike kulutetaan **avoimen tuotannon varastopaikasta**.|
|Poiminta + eteenpäin|Sama kuin materiaalinottotapa eteenpäin lukuun ottamatta sitä, että toimintoa käytetään vain sijainneissa, joissa käytetään ohjattua hyllytystä ja poimintaa.<br><br> Kulutus lasketaan ja kirjataan varastopaikasta, joka on määritetty **Tuotannon valm.var.paik.koodi** -kentässä sijainnissa tai kuormitusryhmässä sen jälkeen, kun komponentti on poimittu varastosta.<br><br> **Huomautus** <br>Jos komponentin materiaalinottotavaksi on määritetty Poiminta + Eteenpäin, sillä ei voi olla toiminnon reitityslinkkikoodia, jonka materiaalinottotavaksi on määritetty Eteenpäin. Osa poistetaan automaattisesti toiminnon alkaessa, minkä vuoksi poimintatoimintoa ei voi pyytää.|
|Poiminta + taaksepäin|Sama kuin materiaalinottotapa taaksepäin lukuun ottamatta sitä, että toimintoa käytetään vain sijainneissa, joka käyttää ohjattua hyllytystä ja poimintaa.<br><br> Kulutus lasketaan ja kirjataan varastopaikasta, joka on määritetty **Tuotannon valm.var.paik.koodi** -kentässä sijainnissa tai kuormitusryhmässä sen jälkeen, kun komponentti on poimittu varastosta.|

## <a name="see-also"></a>Katso myös

[Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)  
[Suunnittelu](production-planning.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
