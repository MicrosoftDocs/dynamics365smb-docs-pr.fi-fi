---
title: Tuotanto-, kokoonpano- ja projektipoiminta perusvarastoinnissa
description: Kun fyysisen varaston sijainnissa on pakollinen poiminnan käsittely mutta ei pakollista toimituksen käsittelyä, voit kirjata komponenttien poiminnan Varaston poiminta -sivun avulla.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/02/2022
ms.author: bholtorf
ms.openlocfilehash: 859c70ebc51f2649000d41817d173292ed5b0870
ms.sourcegitcommit: b4da421c19c3aa3031b0344ec2829d2038be6642
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2022
ms.locfileid: "9617874"
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Tuotanto-, kokoonpano- ja projektipoiminta perusvarastointimäärityksissä

Tuotantoon tai koonpanotilauksiin poimittujen komponenttien hyllytystapa määräytyy sen mukaan, miten fyysinen varasto on määritetty sijaintina. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Poiminta tuotantoon fyysisen varastoinnin perusmäärityksissä

Jos sijainti vaatii poiminnan käsittelyn, mutta ei toimituksen käsittelyä, voit käyttää **Varaston poiminta** -sivua. **Varaston poiminta** -sivun avulla voit järjestää ja tallentaa nimikkeiden poiminnan, joiden materiaalinoton tavaksi on määritetty **Manuaalinen**. Kun rekisteröit varaston poiminnan, poimittujen komponenttien kulutus kirjataan. Voit käyttää myös **varaston siirtoa** ja viitettä lähdeasiakirjaan, jos haluat liittää komponentit, joiden tuotantotilausten materiaalinottotavaksi on määritetty **Manuaalinen**, **Poiminta + eteenpäin**, **Poiminta + taaksepäin**.

Jos tuotanto on integroitu varastoprosesseihin, joko varastopaikkojen tai ohjattujen hyllytysten ja poimintojen perusteella, varastopaikka, josta osia käytetään, on se varastopaikka, joka on määritetty kunkin tuotantotilauksen komponenttirivillä. Kaikkien tarvittavien komponenttien on oltava käytettävissä kyseisessä varastopaikassa. Muutoin kyseisen komponentin manuaalinen tai poistettava materiaalinotto pysäytetään.

> [!NOTE]  
> Varastopoimintojen, varaston siirtojen ja fyysisen varastoinnin poimintojen välillä on seuraavia, merkittäviä eroja:  
>
> - Kun rekisteröit varaston poiminnan sisäiseen toimintoon, kuten tuotanto, vpoimittujen osien kulutus kirjataan samaan aikaan. Kun rekisteröit varaston siirron tai fyysisen varastoinnin poiminnan sisäiselle toiminnolle, vain tarvittavien komponenttien fyysiset siirrot tallennetaan varastopaikkaan toiminta-alueella ilman kulutuksen kirjaamista.  
> - Kun käytät varaston poimintoja **Varastopaikkakoodi** -kenttä tuotantotilauksen komponentin rivinumero määrittää *ota* -varastopaikan, josta osat vähenevät, kun kulutus kirjataan. Kun käytät varaston siirtoja tai fyysisen varastoinnin poimintaa, tuotantotilauksen komponenttirivien **Varastopaikkakoodi**-kenttä määrittää toiminta-alueen *paikka*-varastopaikan, johon varastotyöntekijän on sijoitettava komponentit.  

Jos lähdeasiakirjojen komponentteja poimitaan tai siirretään, lähtevän varaston pyynnön on ilmoitettava varastoalueelle tarvittavasta komponentista. Fyysisen varastoinnin lähtevä pyyntö luodaan, kun toimit seuraavasti:

- Vaihda tuotantotilauksen tilaksi Vapautettu.
- Luo vapautettu tuotantotilaus.  

Materiaaliottotavat vaikuttavat myös komponenttien siirtymiseen tuotantoon. Lisätietoja on kohdassa [Komponenttien materiaalinotto toiminnan tuotoksen mukaan](production-how-to-flush-components-according-to-operation-output.md). Lähdeasiakirjaan viittaavaa **varaston siirtoa** ja **fyysisen varastoinnin poimintaa** ei voi käyttää sellaisten komponenttien poimimiseen, joiden materiaaliottotapana on *Eteenpäin* ja *Taaksepäin*. **Varaston poimintaa** ei voi käyttää poimimaan komponentteja, joilla on jokin muu materiaaliottotapa kuin *Manuaalinen*. Jäljellä olevien komponenttien käsittelemiseen käytetään **varaston siirtoa**, jossa ei viitata lähdeasiakirjaan. Lisätietoja on kohdassa [Komponenttien siirtäminen toiminta-alueelle fyysisen varaston perusmäärityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Niissä laajennetuissa varastomäärityksissä, joissa sijainnit edellyttävät sekä poimintoja että toimituksia, ne komponentit, joiden materiaaliottotavaksi on määritetty *Manuaalinen*, *Poiminta + eteenpäin*, *Poiminta + taaksepäin*, on tuotava tuotantotilauksiin **F. varastoinnin poiminta** -sivulla. Lisätietoja on kohdassa [Tuotanto- tai kokoonpanopoiminta laajennetuissa varastointimäärityksissä](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="to-pick-components-for-production-and-jobs-in-basic-warehouse-configurations"></a>Poimi komponentteja tuotantoa ja projekteja varten perusvarastointimäärityksissä

Fyysisen varaston perusmäärityksissä, joissa sijainti on määritetty käyttämään vain poimintaa, komponentteja voi poimia tuotantotoimintoihin ja projektin suunnitteluriveille **Varaston poiminta** -sivulla. Lisätietoja on kohdassa [Nimikkeiden poiminta varastopoiminnalla](warehouse-how-to-pick-items-with-inventory-picks.md).

> [!NOTE]
> Projektin suunnittelurivien komponenttien poimintamahdollisuus lisättiin sovellukseen [!INCLUDE[d365fin](includes/d365fin_md.md)] vuoden 2022 2. julkaisuaallossa. Jotta ominaisuutta voi käyttää, järjestelmänvalvojan on otettava käyttöön **Ominaisuuspäivitys: Ota käyttöön varaston ja fyysisen varaston poiminnat projekteista** **Ominaisuuksien hallinta** -sivulla.
>
>[!INCLUDE[prod_short](includes/prod_short.md)] käyttää arvoa **Jäljellä oleva määrä** -kentässä työn suunnittelurivillä, kun se luo varastopoiminnat. Jos haluat käyttää töiden varastopoimintoja, **Käytä käyttölinkkiä** -vaihtopainike on otettava käyttöön työn **Työkortti**-sivulla. Tämän ansiosta voit seurata, vastaako käyttö suunnitelmaa. Jos et ota vaihtopainiketta käyttöön, jäljelle jäävän määrän arvona pysyy **0** eikä varastopoimintaa luoda. Lisätietoja on kohdassa [Projektin käytön seurannan määrittäminen](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston poiminnat** ja valitse sitten vastaava linkki.  
2. Voit tarkastella tuotantotilauksen komponentteja valitsemalla ensin **Hae lähdedokumentit** -toiminnon ja sitten vapautetun tuotantotilauksen.  
3. Poimi komponentti ja kirjaa sitten poimintatiedot **Käsiteltävä määrä** -kenttään.  
4. Kun rivit ovat valmiit kirjaamista varten, valitse **Kirjaa**-toiminto. Kirjaus luo tarvittavat fyysisen varaston tapahtumat ja kirjaa nimikkeiden kulutuksen.  

Voit myös luoda **Varastopoiminnan** suoraan vapautetusta tuotantotilauksesta. Valitse ensin **Luo varaston hyllytys, poiminta tai siirto** -toiminto, sitten **Luo varaston poiminta** -valintaruutu ja lopuksi **OK**.

Vaihtoehtoisesti voi siirtää nimikkeitä varastopaikasta toiseen käyttämällä lähdeasiakirjaan viittaavaa **varaston siirtoa**. Kulutus on sitten rekisteröitävä erikseen. Lisätietoja on kohdassa [Tuotannon kulutuksen eräkirjaaminen](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Poiminta kokoonpanoon fyysisen varastoinnin perusmäärityksissä

Käytä seuraavia sivuja kokoonpanotilausten poimimisessa:

- **Varaston siirto** -sivu.
- Jos sijainti vaatii poiminnat, mutta ei toimituksia, käytä **Varaston poiminta** -sivua niiden myyntitilausten poiminnassa, kokoonpanossa ja toimituksessa, joiden nimikkeet edellyttävät kokoonpanoa ennen toimitusta. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Fyysisen varaston laajennetuissa määrityksissä, joissa sijanneille on määritettävä sekä poiminnat että toimitukset, komponentit on tuotava kokoonpanotilauksiin **F.varastoinnin poiminta** -sivulla. Lisätietoja on kohdassa [Tuotanto- tai kokoonpanopoiminta laajennetuissa varastointimäärityksissä](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa

**Varaston poiminta** -sivulla voi myös poimia ja toimittaa myyntiin nimikkeitä, jotka on koottava ennen toimitusta. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).

Kokoonpano tilausta varten -nimikkeet toimitusta varten ei lasketa mukaan ennen kuin niiden kokoonpano on tehty ja ne on kirjattu kokoonpanoalueen varastopaikan tuotokseksi. Tämän vuoksi nimikkeiden poiminta toimitusta varten noudattaa erityistyönkulkua. Varastopaikasta varastotyöntekijät vievät kokoonpanon nimikkeet toimituslaituriin ja kirjaavat sitten varastopoiminnan. Kirjattu varaston poiminta kirjaa sitten kokoonpanon tuotoksen, komponentin kulutuksen ja myyntitoimituksen.

Voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in luomaan varaston siirron automaattisesti, kun varastopoiminta luodaan kokoonpanon nimikkeelle. Voit luoda siirtoja automaattisesti valitsemalla **Luo siirrot automaattisesti** -kenttä **Kokoonpanon asetukset** -sivulla. Lisätietoja on kohdassa [Komponenttien siirtäminen fyysisen perusvarastoinnin toiminta-alueelle](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

[!INCLUDE[prod_short](includes/prod_short.md)] luo myyntinimikkeiden varaston poimintarivit luodaan eri tavalla sen mukaan, onko tilaukseen koottu mitään, joitakin vai kaikki myyntirivin määrille määritetyt määrät.

- Myynnissä käytetään varaston poimintaa varaston toimituksen kirjaamisessa. [!INCLUDE[prod_short](includes/prod_short.md)] luo yhden varaston poimintarivin jokaiselle myyntitilausriville. Jos nimike sijoitetaan eri varastopaikkoihin, luodaan useita rivejä. Poimintarivit perustuvat **Toimitettava määrä** -kentän määrään.
- Myynnissä, jossa myyntitilauksen koko määrä kootaan tilaukseen, kyseiselle määrälle luodaan yksi varaston poimintarivi. Kokoonpantava määrä -kentän arvo on sama kuin **Toimitettava määrä** -kentän arvo. **Kokoonpantava määrä** -kenttä on valittu rivillä.

Jos sijainnin kokoonpanon tuotoksen virta on määritetty, **Kok. til.ltoimit. -var.p.koodi** -kentän arvo tai **Kokoonpanosta-varastop.koodi** -kentän arvo lisätään tässä järjestyksessä varaston poimintarivin **Varastopaikan koodi** -kenttään.

Jos myyntitilausriville ei ole määritetty varastopaikkakoodia eikä sijainnille kokoonpanon tuotoksen virtaa, varaston poimintarivin **Varastopaikan koodi** -kenttä on tyhjä. Varastotyöntekijän on avattava **Varastopaikan sisältö** -sivu ja valittava varastopaikka, johon kokoonpanon nimikkeet kootaan.

Kun osa määrästä on koottava ensin ja toinen poimittava varastosta, [!INCLUDE[prod_short](includes/prod_short.md)] luo vähintään kaksi varaston toimitusriviä. Yksi poimintarivi on kokoonpano tilausta varten -määrälle. Toinen poimintarivi riippuu siitä, mistä varastopaikoista voidaan saada jäljellä oleva määrä. Kahden rivin varastopaikkakoodit on täytetty eri tavoin kahden vastaavan myyntityypin mukaan. Lisätietoja on ohjeaiheen [Tietoja Kokoonpano tilausta varten- tai Kokoonpano varastoon -toiminnoista](assembly-assemble-to-order-or-assemble-to-stock.md) kohdassa Skenaarioiden yhdistelmä.

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
