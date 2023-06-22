---
title: Sijaintikortin ja siirtoreittien määrittäminen (sisältää videon)
description: 'Jos ostat, tallennat tai myyt nimikkeitä useassa paikassa, voit määrittää kunkin paikan sijainniksi.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, distribution center'
ms.search.forms: '5703, 15'
ms.date: 03/25/2023
ms.author: bholtorf
---
# <a name="set-up-locations" />Sijaintien määrittäminen

Sijainnit ovat paikkoja, kuten varasto, jossa nimikkeitä ostetaan, säilytetään tai myydään. [!INCLUDE [prod_short](includes/prod_short.md)] käyttää sijainteja varaston seurannassa sekä yksinkertaisissa että monimutkaisissa varastoprosesseissa.

Voit sitten luoda asiakirjarivejä tietylle sijainnille, tarkastella saatavuutta sijainnin perusteella ja siirtää varastonimikkeitä sijainnista toiseen. Saat lisätietoja siirtymällä [Varaston hallinta](inventory-manage-inventory.md) -kohtaan.
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards" />Sijaintikortit

Tietoja sijainnista, esimerkiksi fyysisestä varastosta tai jakelukeskuksesta määritetään **Sijaintikortti**-sivulla. Kullekin sijainnille annetaan sijaintia kuvaava nimi ja koodi. Tämän jälkeen sijaintikoodin voi syöttää muualle ohjelmaan silloin, kun haluat tallentaa transaktioita tietylle sijainnille.  

Voit syöttää tietoja varastopaikasta ja fyysisen varaston periaatteista jokaiselle sijainnille. Fyysisen varaston käytännöistä riippuen voit käyttää **Varastopaikat**-pikavälilehden vaihtoehtoja määrittääksesi varastopaikat, joita käytetään tapahtumissa oletusarvoisesti. Jos käytät ohjattua hyllytystä ja poimintaa, voit määrittää **Var.paikkojen periaatteet** -pikavälilehden vaihtoehtojen avulla, miten haluat käyttää fyysisen varaston lisäominaisuuksia.  

Jotkut vaihtoehtokentät määräytyvät **Sijaintikortti**-sivun asetusten mukaan. Tällä rajoitetaan asetusyhdistelmiä, joita ei tueta.  

Valitse toiminnot **Alueet** tai **Varastopaikat** nähdäksesi tiedot alueista ja varastopaikoista, jotka on määritetty sijainnille.

### <a name="to-set-up-a-location" />Sijaintien määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Sijaintikortti**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Toista vaiheet 2 ja 3 jokaiselle sijainnille, jossa haluat pitää varastoa.

> [!NOTE]  
> Monet sijaintikorttisivun kentät viittaavat saapuvien ja lähtevien varastoprosessien nimikkeiden käsittelyyn. Nämä kentät eivät ole olennaisia yrityksille, jotka eivät tarvitse monimutkaista varastotoimintoa. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

Voit muuttaa sijainnin määritystä, jos sijainnissa ei ole nimiketapahtumia.  

Jos sinulla on useampia sijainteja, voit määrittää sijaintien välisiä siirtoreittejä. Lisätietoja siirtoreiteistä on kohdassa [Siirtoreittien luominen](inventory-how-setup-locations.md#to-create-a-transfer-route).

### <a name="to-create-a-transfer-route" />Siirtoreittien luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirtoreitit** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
4. Täytä **Sijaintikortti**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Voit nyt siirtää varastonimikkeitä sijaintien välillä. Lisätietoja siirroista on kohdassa [Varastonimikkeiden siirtäminen sijaintien välillä](inventory-how-transfer-between-locations.md).

## <a name="bins" />Varastopaikat

Varastopaikat edustavat fyysisen varaston perusrakennetta. Ne voivat ehdottaa, minne nimikkeet kannattaa sijoittaa. Varastopaikoissa voi olla sisältöä tai ne voivat olla määrittelemättömiä varastopaikkoja, joissa ei ole tiettyä sisältöä.

Jos haluat käyttää varastopaikkatoimintoa sijainnissa, aktivoi toiminto ensin **Sijaintikortti**-sivulla valitsemalla **Fyysinen varasto** -pikavälilehdessä **Varastopaikat pakollisia** -valintapainike. Voit suunnitella nimikkeen työnkulun sijainnissa määrittämällä varastopaikkakoodit kentissä fyysisen varaston prosesseja varten **Varastopaikat**- ja **Var.paikkojen periaatteet** -pikavälilehdissä.

> [!NOTE]
> Ennen kuin voit määrittää varastopaikkakoodeja sijainnissa, on luotava varastopaikkakoodit. Saat lisätietoja varastopaikoista valitsemalla [Varastopaikkojen luominen](warehouse-how-to-create-individual-bins.md) ja [Varastopaikkojen määrittäminen](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones" />Alueet

Jos haluat jäsentää varastopaikat alueiden alla, voit tehdä sen **Alueet**-sivulla. Kun varastopaikoille määritetään alue, [!INCLUDE [prod_short](includes/prod_short.md)] kopioi tiedot alueelta varastopaikkoihin. Voit myös määrittää yhden alueen ja käyttää varastopaikkoja yksin fyysisen varaston järjestämiseksi. Lisätietoja vyöhykkeistä on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations" />Sijaintien oletusdimensiot

Dimensiot ovat tapahtumia luokittelevia arvoja, joita voi seurata ja analysoida erilaisilla raportointityökaluilla. Dimensioiden avulla voit esimerkiksi ilmaista, mistä osastosta tai projektista tapahtuma on lähtöisin. Kun oletusdimensiot ovat käytössä, käyttäjät eivät voi tehdä virheitä ja syöttää dimensioita manuaalisesti transaktiotasolle, jos kaikki tavarat ovat peräisin yhdestä sijainnista ja osastosta.

Määritä oletusdimensiot sijainnille **Sijaintikortti**-sivulle valitsemalla **Dimensiot**. Tämän jälkeen sijainnin oletusdimensiot määritetään seuraaville asiakirjoille, kun valitset sijainnin rivillä.

* Siirtotilaukset
* Fyysisen varaston tilaukset
* Varastotoimitukset
* Varaston vastaanotot
* Nimikepäiväkirjat

Tarvittaessa voit poistaa rivin dimension tai muuttaa sitä. **Arvon kirjaaminen** -kentässä voit vaatia, että ihmiset määrittävät dimensiot sijainneille, ennen kuin he voivat kirjata tapahtuman. Jos haluat, että ihmiset voivat valita vain tietyt dimensioarvot, voit määrittää arvot **Sallittujen arvojen suodatin** -kentässä. Voit myös sisällyttää sijainnin dimensioarvoja **Oletusdimensioprioriteetit**-sivulle ja prioriteetti- ja dimensiosääntöjen yhdistelmien osalta **Dimensioyhdistelmät**-sivulle.

Koska siirtotilausasiakirjat ja uudelleenluokittelupäiväkirjat käsittelevät useampaa kuin yhtä sijaintia, tietojen syöttämisen järjestys on tärkeää. Oletusdimensiot kopioidaan viimeinen sijainti -kentästä (kuljetuksessa-sijainti ohitetaan).

### <a name="example-of-default-dimensions-on-locations" />Esimerkki sijaintien oletusdimensioista

Seuraavissa esimerkeissä havainnollistetaan, miten oletusdimensiota käytetään.

Sinulla on seuraavat dimension asetukset:

* Sijainti EAST. Osaston dimensio on ADM
* Sijainti WEST. Osaston dimensio on PROD

Sijainti määritellään siirtotilauksessa seuraavasti:

1. Sijainnista = EAST
2. Sijaintiin = WEST

PROD-dimensio kopioidaan sijainnista WEST.

Kentät on täytettävä vastakkaisessa järjestyksessä seuraavasti:

1. Sijaintiin = WEST
2. Sijainnista = EAST

ADM-dimensio kopioidaan sijainnista EAST.

## <a name="see-related-training-at-microsoft-learnlearnmodulestrade-set-up-dynamics--business-central" />Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/trade-set-up-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Varaston hallinta](inventory-manage-inventory.md)  
[Varastonimikkeiden siirtäminen sijaintien välillä](inventory-how-transfer-between-locations.md)  
[Varastopaikkojen luominen](warehouse-how-to-create-individual-bins.md)  
[Varastopaikkojen määrittäminen](warehouse-how-to-set-up-bin-types.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
