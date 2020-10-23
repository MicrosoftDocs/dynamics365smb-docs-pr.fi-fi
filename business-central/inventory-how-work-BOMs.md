---
title: Komponenttien hallinta tuoterakenteiden avulla| Microsoft Docs
description: Kokoonpanon tai tuotannon tuoterakenteella voi määrittää komponentit tai resurssit, joita tarvitaan kyseisen tuoterakenteen nimikkeen kokoamiseen.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4aa769c8a2b044f434a9643209eecb97f7f51f13
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919386"
---
# <a name="work-with-bills-of-material"></a>Tuoterakenteen käyttäminen
Tuoterakenteilla voi jäsentää päänimikkeet, jotka resurssien tai kuormituskeskusten on koottava tai tuotettava komponenteista. Kokoonpanon tuoterakennetta voidaan käyttää myös päänimikkeen myyntiin komponenteista koostuvana tuotepakettina.

## <a name="assembly-boms-or-production-boms"></a>Kokoonpanon tuoterakenteet tai tuotannon tuoterakenteet
Voit käyttää kokoonpanotilauksia tehdäksesi lopullisia nimikkeitä osista yksinkertaisesssa prosessissa, joka voidaan suorittaa yhden tai useamman perusresurssin voimin, jotka eivät ole tai kuormitusryhmiä tai tuotantosoluja, tai ilman resursseja. Kokoonpanoprosessi voi olla esimerkiksi kahden viinipullon ja yhden kahvipaketin valinta ja niiden pakkaaminen lahjaksi.  

Kokoonpanon tuoterakenne muodostaa perustiedot, jotka määrittävät, mitkä osanimikkeet käytetään kokoonpanon lopputuotteeseen ja mitkä resurssit käytetään kokoonpanon nimikkeen kokoamiseen. Kun syötät kokoonpanon nimikkeen ja määrän uuden kokoonpanotilauksen otsikkoon, kokoonpanotilausrivit täytetään automaattisesti kokoonpanon tuoterakenteen mukaan yhdellä kokoonpanotilausrivillä osaa tai resurssia kohden. Lisätietoja on kohdassa [Kokoonpanon hallinta](assembly-assemble-items.md).

Tässä ohjeaiheessa käsitellään kokoonpanon tuoterakenteita.

Käytä tuotantotilauksia tehdäksesi loopullisia nimikkeitä osista monimutkaisessa prosessissa, joka edellyttää tuotannon reititystä ja tuotantosoluja tai kuormitusryhmiä, jotka edustavat tuotantokapasiteettia. Tuotantoprosessi voi koostua esimerkiksi toiminnoista, jotka ovat teräslevyjen leikkaaminen, niiden hitsaaminen ja loppunimikkeen maalaaminen viimeisenä toimintona. Lisätietoja on kohdassa [Tuotanto](production-manage-manufacturing.md).  

Tuotannon tuoterakenne määrittää tuotannon kohteen ja sen komponentit. Tuotannon tuoterakenteen on oltava sertifioitu ja määritetty tuotantokohteelle ennen kuin sitä voidaan käyttää tuotantotilauksessa. Kun syötät tuotantonimikkeen tuotantotilausriville joko manuaalisesti tai päivittämällä järjestystä, tuotannon rruoterakenteen sisällöstä tulee tuotantotilauksen komponentit. Lisätietoja on kohdassa [Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md).  

Tuotannossa olevien resurssien konsepti on paljon kehittyneempi kuin kokoonpanon hallinnassa. Tuotantosolut ja kuormitusryhmät toimivat resursseina ja tuotannon vaiheet on esitetty toimina, jotka on määritetty resursseille tuotannon reitityksissä. Lisätietoja on kohdassa [Reititysten luominen](production-how-to-create-routings.md).

Sekä kokoonpanotilaukset että tuotantotilaukset voidaan linkittää suoraan myyntitilauksiin. Voit käyttää kokoonpanotilauksia kuitenkin vain loppunimikkeen mukauttamiseen suoraan asiakkaan pyynnöstä myyntitilauksessa

## <a name="to-create-an-assembly-bom"></a>Luo kokoonpanon tuoterakenne
Kokoonpanon tuoterakenne on luotava, jos haluat määrittää päänimikkeen, joka koostuu muista nimikkeistä ja mahdollisesti resursseista, joita tarvitaan päänimikkeen kokoamiseen.  

Kokoonpanon tuoterakenteet sisältävät yleensä nimikkeitä, mutta ne voivat sisältää myös resursseja, joita tarvitaan niiden kokoamiseen.

Kokoonpanon tuoterakenteessa voi olla useita tasoja. Toisin sanoen kokoonpanon tuoterakenteen komponentti voi olla itsessään kokoonpanonimike. Siinä tapauksessa kokoonpanon tuoterakennerivillä olevassa **Kokoonpanon tuoterakenne** -kentässä on **Kyllä**.

Erikoisvaatimukset koskevat kokoonpanon tuoterakenteiden nimikkeiden saatavuutta. Lisätietoja on kohdassa [Nimikkeen saatavuuden tarkastelu sen mukaan, miten sitä käytetään kokoonpanon tuoterakenteessa](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Kokoonpanon tuoterakenteen luomisessa on kaksi osaa:
- uuden nimikkeen määrittäminen
- kokoonpanonimikkeen tuoterakenteen määrittäminen.

1. Määritä uusi nimike. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

    Jatka antamalla kokoonpanon tuoterakenteen osat tai resurssit.  
2. Valitse kokoonpanonimikkeen **Nimikekortti**-sivulla ensin **Kokoonpano**-toiminto ja sitten **Kokoonpanon tuoterakenne** -toiminto.
3. Täytä **Kokoonpanon tuoterakenne** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-edit-assembly-boms"></a>Kokoonpanon tuoterakenteiden muokkaaminen
Voit muokata kokoonpanon tuoterakenteen rivejä milloin tahansa. Huomaa kuitenkin, että tuoterakenne voi olla käytössä päätason myynnissä tai kokoonpanoissa, joihin muutos voi vaikuttaa. Valitse **Käyttökohde-**-toiminto, jossa näet, mitä nimikkeitä se käyttää ja voiko se vaikuttaa myynti- tai kokoonpanotilauksiin.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Valitse **Kyllä**-arvo **Kokoonpanon tuoterakenne** -sarakkeesta.
3. Valitse **Kokoonpanon tuoterakenne** -sivulla **Muokkaa luetteloa** -toiminto ja muuta sitten mitä tahansa kenttää tarpeen mukaan.

## <a name="to-view-components-and-resources-indented-according-to-the-bom-structure"></a>Kokoonpanonimikkeen osien ja resurssien näyttäminen tuoterakenteen perusteella sisennettyinä
Voit avata **Kokoonpanon tuoterakenne** -sivulla erillisen sivun, joka näyttää osat ja resursseja sisennettynä kokoonpanonimikkeen alle niiden tuoterakenteen mukaisen sijainnin perusteella.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa kokoonpanonimikkeen kortti. (**Nimikkeet**-sivun **Kokoonpanon tuoterakenne** -kentässä on **Kyllä**.)
3. Valitse **Nimikekortti**-sivulla ensin **Kokoonpano**-toiminto ja sitten **Kokoonpanon tuoterakenne** -toiminto.
4. Valitse **Kokoonpanon tuoterakenne** -sivulla **Näytä tuoterakenne** -toiminto.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Kokoonpanon korvaaminen sen osilla asiakirjariveillä
Voit käyttää missä tahansa kokoonpanonimikkeen sisältävässä myynti- ja ostoasiakirjassa erikoistoimintoa, jolla voit korvata kokoonpanonimikkeen rivin uusilla kokoonpanon komponenttien riveillä. Tämä toiminto on kätevä esimerkiksi silloin, kun haluat myydä komponentit kokoonpanonimikettä vastaavana tuotepakettina.

Pura tuoterakennetoiminto on käytettävissä myös **Kokoonpanon tuoterakenne** -sivulla keinona tarkastella kokoonpanon tuoterakenteen alikokoonpanojen alatason kohteita.

> [!CAUTION]  
>  Kun **Pura tuoterakenne** -toimintoa on käytetty, sen kumoaminen ei ole helppoa. Komponentteja vastaavat myyntitilausrivit on poistettava ja kokoonpanonimikkeen myyntitilausrivi on sitten annettava uudelleen.

Seuraava toimenpide perustuu myyntilaskuun. Samoja vaiheet koskeva myös muita myyntiasiakirjoja ja kaikki ostoasiakirjoja.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntilaskut** ja valitse sitten liittyvä linkki.
2. Avaa kokoonpanonimikkeen rivin sisältävä myyntilasku.
3. Valitse ensin kokoonpanonimikkeen rivi ja sitten **Pura tuoterakenne** -rivitoimintoa.

Kaikki kokoonpanonimikkeen myyntilaskurivin kentät poistetaan **Nimike**- ja **Kuvaus**-kenttiä lukuun ottamatta. Valmiit myyntilaskurivit lisätään komponenteille ja mahdollisille resursseille, joista kokoonpanonimike koostuu.

> [!NOTE]
> Myös **Poimintaluettelo tilauksen mukaan** -raportti muuttuu niin, että siinä näkyvät vain komponentit. Tämä tarkoittaa sitä, että varastotyöntekijä, joka poimii päänimikkeen, kokoonpanonimikkeen, ei näe sitä keräysluettelossa. Lisätietoja on kohdassa [Tulosta poimintaluettelo](sales-how-print-picking-list.md).

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>Kokoonpanonimikkeen vakiokustannusten laskeminen
Lasket kokoonpano-nimikkeen yksikkökustannuksen vyöryttämällä jokaisen osan yksikkökustannuksen ja resurssin nimikkeen kokoonpanon tuoterakenteessa.

Voit myös laskea ja päivittää yhden tai usean nimikkeen vakiokustannukset **Vakiokust. työkirja** -sivulla. Lisätietoja on kohdassa [Vakiokustannusten päivittäminen](finance-how-to-update-standard-costs.md).  

Kokoonpanon tuoterakenteen yksikkökustannus on aina yhtä suuri kuin sen komponenttien (mukaan lukien muut kokoonpanon tuoterakenteet) ja mahdollisten resurssien yhteenlasketut yksikkökustannukset.

1. Valitse oikeassa yläkulmassa oleva **Etsi sivu tai raportti** -kuvake, syötä **Nimikkeet** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa kokoonpanonimikkeen kortti. (**Nimikkeet**-sivun **Kokoonpanon tuoterakenne** -kentässä on **Kyllä**.)
3. Valitse **Nimikekortti**-sivulla ensin **Kokoonpano**-toiminto ja sitten **Kokoonpanon tuoterakenne** -toiminto.
4. Valitse **Kokoonpanon tuoterakenne** -sivulla **Laske vakiokustannus** -toiminto.
5. Valitse ensin jokin seuraavista vaihtoehdoista ja sitten **OK**.

|Asetus |Description |
|-------|------------|
|**Ylätaso**|Laskee kokoonpanon nimikkeen vakiokustannuksen kaikkien ostettujen tai koottujen nimikkeiden kokonaiskustannuksena kokoonpanon tuoterakenteessa riippumatta muista pohjalla olevista kokoonpanon tuoterakenteista.|
|**Kaikki tasot.**|Laskee kokoonpanonimikkeen standardikustannukset seuraavien summana: 1) Kaikkien kokoonpanon tuoterakenteeseen sisältyvien tuoterakenteiden yhteenlaskettu kustannus. 2) Kaikki kokoonpanon tuoterakenteen ostettujen nimikkeiden kustannukset.|



Kokoonpanon tuoterakenteen muodostavien nimikkeiden kustannukset kopioidaan osanimikekorteilta. Kunkin nimikkeen kustannus kerrotaan määrällä ja kokonaiskustannus lisätään kokoonpanon nimikekortin **Yksikkökustannus**-kenttään.

## <a name="see-also"></a>Katso myös
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)     
[Varasto](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
