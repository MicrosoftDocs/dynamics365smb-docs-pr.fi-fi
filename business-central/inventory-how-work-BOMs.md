---
title: Komponenttien hallinta tuoterakenteiden avulla| Microsoft Docs
description: "Kokoonpanon tai tuotannon tuoterakenteella voi määrittää komponentit tai resurssit, joita tarvitaan kyseisen tuoterakenteen nimikkeen kokoamiseen."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f27160f551a002d1d19fa64b86aa637d8fadcf8a
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

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

Erikoisvaatimukset koskevat kokoonpanon tuoterakenteiden nimikkeiden saatavuutta. Lisätietoja on ohjeaiheen [Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md) kohdassa Nimikkeen saatavuuden tarkastelu sen mukaan, miten sitä käytetään kokoonpanon tuoterakenteessa.

Kokoonpanon tuoterakenteen luomisessa on kaksi osaa:
- uuden nimikkeen määrittäminen
- kokoonpanonimikkeen tuoterakenteen määrittäminen.

1. Määritä uusi nimike. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

    Jatka antamalla kokoonpanon tuoterakenteen osat tai resurssit.  
2. Valitse kokoonpanonimikkeen **Nimikekortti**-ikkunassa ensin **Kokoonpano**-toiminto ja sitten **Kokoonpanon tuoterakenne** -toiminto.
3. Täytä **Kokoonpanon tuoterakenne** -ikkunassa tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Kokoonpanonimikkeen osien näyttäminen tuoterakenteen perusteella sisennettyinä
Voit avata **Kokoonpanon tuoterakenne** -ikkunassa erillisen ikkunan, joka näyttää osat ja resursseja sisennettynä kokoonpanonimikkeen alle niiden tuoterakenteen mukaisen sijainnin perusteella.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Nimikkeet** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa kokoonpanonimikkeen kortti. (**Nimikkeet**-ikkunan **Kokoonpanon tuoterakenne** -kentässä on **Kyllä**.)
3. Valitse **Nimikekortti**-ikkunassa ensin **Kokoonpano**-toiminto ja sitten **Kokoonpanon tuoterakenne** -toiminto.
4. Valitse **Kokoonpanon tuoterakenne** -ikkunassa **Näytä tuoterakenne** -toiminto.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Kokoonpanon korvaaminen sen osilla asiakirjariveillä
Voit käyttää missä tahansa kokoonpanonimikkeen sisältävässä myynti- ja ostoasiakirjassa erikoistoimintoa, jolla voit korvata kokoonpanonimikkeen rivin uusilla kokoonpanon komponenttien riveillä. Tämä toiminto on kätevä esimerkiksi silloin, kun haluat myydä komponentit kokoonpanonimikettä vastaavana tuotepakettina.

**Varoitus**: Kun **Pura tuoterakenne** -toimintoa on käytetty, sen kumoaminen ei ole helppoa. Komponentteja vastaavat myyntitilausrivit on poistettava ja kokoonpanonimikkeen myyntitilausrivi on sitten annettava uudelleen.

Seuraava toimenpide perustuu myyntilaskuun. Samoja vaiheet koskeva myös muita myyntiasiakirjoja ja kaikki ostoasiakirjoja.

1. Valitse oikeassa yläkulmassa oleva **Etsi sivu tai raportti** -kuvake, syötä **Myyntilaskut** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa kokoonpanonimikkeen rivin sisältävä myyntilasku.
3. Valitse ensin kokoonpanonimikkeen rivi ja sitten **Pura tuoterakenne** -rivitoimintoa.

Kaikki kokoonpanonimikkeen myyntilaskurivin kentät poistetaan **Nimike**- ja **Kuvaus**-kenttiä lukuun ottamatta. Valmiit myyntilaskurivit lisätään komponenteille ja mahdollisille resursseille, joista kokoonpanonimike koostuu.

**Huomautus**: Pura tuoterakenne -toimintoa voi käyttää myös **Kokoonpanon tuoterakenne** -ikkunassa.

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>Kokoonpanonimikkeen vakiokustannusten laskeminen
Lasket kokoonpano-nimikkeen yksikkökustannuksen vyöryttämällä jokaisen osan yksikkökustannuksen ja resurssin nimikkeen kokoonpanon tuoterakenteessa.

Voit myös laskea ja päivittää yhden tai usean nimikkeen vakiokustannukset **Vakiokust. työkirja** -ikkunassa. Lisätietoja on kohdassa [Vakiokustannusten päivittäminen](finance-how-to-update-standard-costs.md).  

Kokoonpanon tuoterakenteen yksikkökustannus on aina yhtä suuri kuin sen komponenttien (mukaan lukien muut kokoonpanon tuoterakenteet) ja mahdollisten resurssien yhteenlasketut yksikkökustannukset.

1. Valitse oikeassa yläkulmassa oleva **Etsi sivu tai raportti** -kuvake, syötä **Nimikkeet** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa kokoonpanonimikkeen kortti. (**Nimikkeet**-ikkunan **Kokoonpanon tuoterakenne** -kentässä on **Kyllä**.)
3. Valitse **Nimikekortti**-ikkunassa ensin **Kokoonpano**-toiminto ja sitten **Kokoonpanon tuoterakenne** -toiminto.
4. Valitse **Kokoonpanon tuoterakenne** -ikkunassa **Laske vakiokustannus** -toiminto.
5. Valitse ensin jokin seuraavista vaihtoehdoista ja sitten **OK**.

|Asetus |Description |
|-------|------------|
|**Ylätaso**|Laskee kokoonpanon nimikkeen vakiokustannuksen kaikkien ostettujen tai koottujen nimikkeiden kokonaiskustannuksena kokoonpanon tuoterakenteessa riippumatta muista pohjalla olevista kokoonpanon tuoterakenteista.|
|**Kaikki tasot.**|Laskee kokoonpanonimikkeen standardikustannukset seuraavien summana: 1) Kaikkien kokoonpanon tuoterakenteeseen sisältyvien tuoterakenteiden yhteenlaskettu kustannus. 2) Kaikki kokoonpanon tuoterakenteen ostettujen nimikkeiden kustannukset.|



Kokoonpanon tuoterakenteen muodostavien nimikkeiden kustannukset kopioidaan osanimikekorteilta. Kunkin nimikkeen kustannus kerrotaan määrällä ja kokonaiskustannus lisätään kokoonpanon nimikekortin **Yksikkökustannus**-kenttään.

## <a name="see-also"></a>Katso myös
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)     
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

