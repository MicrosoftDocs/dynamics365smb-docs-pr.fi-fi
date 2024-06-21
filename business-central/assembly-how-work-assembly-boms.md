---
title: Kokoonpanon tuoterakenteiden käyttäminen
description: 'Kokoonpanon tuoterakenteella voi määrittää komponentit, joita tarvitaan kyseisen tuoterakenteen nimikkeen kokoamiseen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'assembly bom, bills of material,'
ms.search.form: '36, 5870, 5872, 5874'
ms.date: 09/26/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Kokoonpanon tuoterakenteiden käyttäminen

Kokoonpanon tuoterakenteilla (BOM) voi jäsentää päänimikkeet, jotka on koottava tai tuotettava komponenteista hyvin vähillä resursseilla. Kokoonpanon tuoterakennetta voidaan käyttää esimerkiksi päänimikkeen myyntiin komponenttinimikkeistä koostuvana tuotepakettina.

Voit käyttää kokoonpanotilauksia, kun teet komponenteista loppunimikkeitä yksinkertaisella prosessilla. Tämä prosessi voidaan toteutetaan vähintään yhdellä perusresurssilla, joka ei ole kuormituskeskus eikä tuotantosolu, tai ilman resursseja. Kokoonpanoprosessi voi olla esimerkiksi kahden viinipullon ja yhden kahvipaketin valinta ja niiden pakkaaminen lahjaksi.  

Kokoonpanon tuoterakenne muodostaa perustiedot, jotka määrittävät, mitkä osanimikkeet käytetään kokoonpanon lopputuotteeseen ja mitkä resurssit käytetään kokoonpanon nimikkeen kokoamiseen. Kun syötät kokoonpanon nimikkeen ja määrän uuden kokoonpanotilauksen otsikkoon, kokoonpanotilausrivit täytetään automaattisesti kokoonpanon tuoterakenteen mukaan yhdellä kokoonpanotilausrivillä osaa tai resurssia kohden. Lisätietoja on kohdassa [Kokoonpanon hallinta](assembly-assemble-items.md).

[!INCLUDE[prod_short](includes/prod_short.md)] tukee myös tuotannon tuoterakenteita. Tuotannon tuoterakenteet eroavat kokoonpanon tuoterakenteista sillä, että ne ottavat käyttöön monimutkaisempia menettelyjä, kuten resurssien käyttöä, tuotannon reititystä ja tuotanto- tai kuormitusryhmiä. Lue lisää eroista kohdista [Tuoterakenteiden käyttäminen](inventory-how-work-BOMs.md) ja [Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md).

## Luo kokoonpanon tuoterakenne

Kokoonpanon tuoterakenne on luotava, jos haluat määrittää päänimikkeen, joka koostuu muista nimikkeistä ja mahdollisesti resursseista, joita tarvitaan päänimikkeen kokoamiseen.  

Kokoonpanon tuoterakenteet sisältävät yleensä nimikkeitä, mutta ne voivat sisältää myös resursseja, joita tarvitaan niiden kokoamiseen.

Kokoonpanon tuoterakenteessa voi olla useita tasoja. Toisin sanoen kokoonpanon tuoterakenteen komponentti voi olla itsessään kokoonpanonimike. Siinä tapauksessa kokoonpanon tuoterakennerivillä olevassa **Kokoonpanon tuoterakenne** -kentässä on **Kyllä**.

Erikoisvaatimukset koskevat kokoonpanon tuoterakenteiden nimikkeiden saatavuutta. Lisätietoja on kohdassa [Nimikkeen saatavuuden tarkastelu sen mukaan, miten sitä käytetään kokoonpanon tuoterakenteessa](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Kokoonpanon tuoterakenteen luomisessa on kaksi osaa:

- uuden nimikkeen määrittäminen
- kokoonpanonimikkeen tuoterakenteen määrittäminen.

1. Määritä uusi nimike. Lisätietoja on kohdassa [Uusien nimikkeiden rekisteröinti](inventory-how-register-new-items.md).

   Jatka antamalla kokoonpanon tuoterakenteen osat tai resurssit.  
2. Valitse kokoonpanonimikkeen **Nimikekortti**-sivulla ensin **Kokoonpano**-toiminto, sitten **Kokoonpanon tuoterakenne** -toiminto.
3. Täytä **Kokoonpanon tuoterakenne** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Kokoonpanon nimikkeillä voi olla erilaisia variantteja [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa, kuten millä tahansa muuta nimikkeillä, mikä auttaa pitämään saatavilla olevien tuotteiden luettelon lyhyempänä. Lisätietoja ominaisuudesta on [Tuotevarianttien hallinnassa](inventory-item-variants.md).

## Kokoonpanon tuoterakenteiden muokkaaminen

Voit muokata kokoonpanon tuoterakenteen rivejä milloin tahansa. Huomaa kuitenkin, että tuoterakenne voi olla käytössä päätason myynnissä tai kokoonpanoissa, joihin muutos voi vaikuttaa. Valitse **Käyttökohde-**-toiminto, jossa näet, mitä nimikkeitä se käyttää ja voiko se vaikuttaa myynti- tai kokoonpanotilauksiin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet**, valitse sitten vastaava linkki.
2. Valitse **Kyllä**-arvo **Kokoonpanon tuoterakenne** -sarakkeesta.
3. Valitse **Kokoonpanon tuoterakenne** -sivulla **Muokkaa luetteloa** -toiminto, muuta sitten mitä tahansa kenttää tarpeen mukaan.

## Kokoonpanonimikkeen osien ja resurssien näyttäminen tuoterakenteen perusteella sisennettyinä

Voit avata **Kokoonpanon tuoterakenne** -sivulla erillisen sivun, joka näyttää osat ja resursseja sisennettynä kokoonpanonimikkeen alle niiden tuoterakenteen mukaisen sijainnin perusteella.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet**, valitse sitten vastaava linkki.
2. Avaa kokoonpanonimikkeen kortti. (**Nimikkeet**-sivun **Kokoonpanon tuoterakenne** -kentässä on **Kyllä**.)
3. Valitse **Nimikekortti**-sivulla ensin **Kokoonpano**-toiminto, sitten **Kokoonpanon tuoterakenne** -toiminto.
4. Valitse **Kokoonpanon tuoterakenne** -sivulla **Näytä tuoterakenne** -toiminto.

## Kokoonpanon korvaaminen sen osilla asiakirjariveillä

Voit käyttää missä tahansa kokoonpanonimikkeen sisältävässä myynti- ja ostoasiakirjassa erikoistoimintoa, jolla voit korvata kokoonpanonimikkeen rivin uusilla kokoonpanon komponenttien riveillä. Tämä toiminto on kätevä esimerkiksi silloin, kun haluat myydä komponentit kokoonpanonimikettä vastaavana tuotepakettina.

**Pura tuoterakenne** -toiminto on käytettävissä myös **Kokoonpanon tuoterakenne** -sivulla keinona tarkastella kokoonpanon tuoterakenteen alikokoonpanojen alatason kohteita.

> [!CAUTION]  
> Kun **Pura tuoterakenne** -toimintoa on käytetty, sen kumoaminen ei ole helppoa. Komponentteja vastaavat myyntitilausrivit on poistettava ja kokoonpanonimikkeen myyntitilausrivi on sitten annettava uudelleen.

Seuraava toimenpide perustuu myyntilaskuun. Samat vaiheet koskevat myös muita myyntiasiakirjoja ja kaikkia ostoasiakirjoja.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut**, valitse sitten vastaava linkki.
2. Avaa kokoonpanonimikkeen rivin sisältävä myyntilasku.
3. Valitse ensin kokoonpanonimikkeen rivi, sitten **Pura tuoterakenne** -rivitoimintoa.

Kaikki kokoonpanonimikkeen myyntilaskurivin kentät poistetaan **Nimike**- ja **Kuvaus**-kenttiä lukuun ottamatta. Valmiit myyntilaskurivit lisätään komponenteille ja mahdollisille resursseille, joista kokoonpanonimike koostuu.

> [!NOTE]
> Myös **Poimintaluettelo tilauksen mukaan** -raportti muuttuu niin, että siinä näkyvät vain komponentit. Tämä tarkoittaa sitä, että varastotyöntekijä, joka poimii päänimikkeen, kokoonpanonimikkeen, ei näe sitä keräysluettelossa. Lisätietoja on kohdassa [Poiminta luettelon tulostaminen](sales-how-print-picking-list.md).

## Kokoonpanonimikkeen vakiokustannusten laskeminen

Lasket kokoonpano-nimikkeen yksikkökustannuksen vyöryttämällä jokaisen osan yksikkökustannuksen ja resurssin nimikkeen kokoonpanon tuoterakenteessa.

Voit myös laskea ja päivittää yhden tai usean nimikkeen vakiokustannukset **Vakiokust. työkirja** -sivulla. Lisätietoja on kohdassa [Vakiokustannusten päivittäminen](finance-how-to-update-standard-costs.md).  

Kokoonpanon tuoterakenteen yksikkökustannus on aina yhtä suuri kuin sen komponenttien (mukaan lukien muut kokoonpanon tuoterakenteet) ja mahdollisten resurssien yhteenlasketut yksikkökustannukset.  

> [!NOTE]
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)]

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet**, valitse sitten vastaava linkki.
2. Avaa kokoonpanonimikkeen kortti. (**Nimikkeet**-sivun **Kokoonpanon tuoterakenne** -kentässä on **Kyllä**.)
3. Valitse **Nimikekortti**-sivulla ensin **Kokoonpano**-toiminto, sitten **Kokoonpanon tuoterakenne** -toiminto.
4. Valitse **Kokoonpanon tuoterakenne** -sivulla **Laske vakiokustannus** -toiminto.
5. Valitse ensin jokin seuraavista vaihtoehdoista, sitten **OK**-painike.

|Asetus |Kuvaus |
|-------|------------|
|**Ylätaso**|Laskee kokoonpanon nimikkeen vakiokustannuksen kaikkien ostettujen tai koottujen nimikkeiden kokonaiskustannuksena kokoonpanon tuoterakenteessa riippumatta muista pohjalla olevista kokoonpanon tuoterakenteista.|
|**Kaikki tasot.**|Laskee kokoonpanonimikkeen standardikustannukset seuraavien summana: 1) Kaikkien kokoonpanon tuoterakenteeseen sisältyvien tuoterakenteiden yhteenlaskettu kustannus. 2) Kaikki kokoonpanon tuoterakenteen ostettujen nimikkeiden kustannukset.|

Kokoonpanon tuoterakenteen muodostavien nimikkeiden kustannukset kopioidaan osanimikekorteilta. Kunkin nimikkeen kustannus kerrotaan määrällä ja kokonaiskustannus lisätään kokoonpanon nimikekortin **Yksikkökustannus**-kenttään.

## Katso myös

[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Tuotevarianttien hallinta](inventory-item-variants.md)  
[Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)  
[Varasto](inventory-manage-inventory.md)  
[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)  
[Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
