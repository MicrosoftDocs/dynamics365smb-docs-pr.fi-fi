---
title: Nimikkeiden poiminta varaston poiminnalla
description: Tietoja varaston poimintojen käyttämisestä lähdeasiakirjojen poiminta- ja toimitustietojen tallentamiseen ja kirjaamiseen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 7377'
---
# Nimikkeiden poiminta varastopoiminnalla

[!INCLUDE[prod_short](includes/prod_short.md)]issa nimikkeet poimintaan ja toimitukseen on käytettävissä neljä tapaa, jotka käsitellään seuraavassa taulukossa.

|Tapa|Lähtevien käsittely|Vaadi poiminta|Vaadi toimitus|Monimutkaisuustaso (lisätietoja on kohdassa [Varastoinninhallinnan yleiskatsaus](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Poiminnan ja toimituksen kirjaaminen tilausriviltä|||Ei määritettyä fyysisen varaston toimintaa.|  
|B|Poiminnan ja toimituksen kirjaaminen varaston poiminta-asiakirjasta|Otettu käyttöön||Perus: tilauksittain.|  
|S|Poiminnan ja toimituksen kirjaaminen fyysisen varastoinnin toimitusasiakirjasta||Otettu käyttöön|Perus: useiden tilausten konsolidoitu vastaanoton ja toimituksen kirjaus.|  
|P|Poiminnan kirjaaminen fyysisen varastoinnin poiminta-asiakirjasta ja toimituksen kirjaaminen fyysisen varastoinnin toimitusasiakirjasta|Otettu käyttöön|Otettu käyttöön|Lisäasetukset|  

Lisätietoja on kohdassa [Fyysisen varaston lähtevä työnkulku](design-details-outbound-warehouse-flow.md).

Tässä artikkelissa viitataan taulukon menetelmään B.

Jos sijainti on määritetty edellyttämään poiminnan mutta ei toimituksen käsittelyä, lähdeasiakirjojen poiminta- ja toimitustietojen tallentamiseen ja kirjaamiseen käytetään **Varaston poiminta** -sivua. Lähtevien lähdeasiakirjat voivat olla myyntitilauksia, ostopalautustilauksia ja lähteviä siirtotilauksia.

> [!NOTE]
> Myös komponenttitarpeita sisältävät tuotanto- ja kokoonpanotilaukset ilmaisevat lähtevien lähdeasiakirjoja. Lisätietoja sisäisten prosessien tuotanto- ja kokoonpanotilausten käsittelemisestä on kohdassa [Rakennetiedot: fyysisen varaston sisäiset virrat](design-details-internal-warehouse-flows.md).
>
> Vaikka myös huoltotilaukset ovat lähteviä lähdeasiakirjoja, ne eivät tue tilauskohtaista perustason monimutkaisuutta.
>
> Kun poiminnan ja toimituksen myyntirivin määriä kokoonpannaan tilausta varten, varaston poimintarivejä luotaessa on noudatettava tiettyjä sääntöjä. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa](#handling-assemble-to-order-items-with-inventory-picks).  

Varaston poiminnan voi luoda kolmella tavalla:

* Varastopoiminta luodaan suoraan lähdeasiakirjasta.  
* Useiden lähdeasiakirjojen varaston poiminnat luodaan samanaikaisesti käyttämällä eräajoa.
* Poimintaa pyydetään kahdessa vaiheessa vapauttamalla ensin lähdeasiakirjan, mikä ilmaisee fyysiseen varastointiin, että lähdeasiakirja on valmis poimittavaksi.

Varaston poiminta voidaan sitten luoda **Varaston poiminta** -sivulta lähdeasiakirjan perusteella.  

## Varastopoiminnan lähdeasiakirjasta luominen

1. Valitse **Luo varaston hyllytys tai poiminta** -toiminto lähdeasiakirjassa, joka voi olla myyntitilaus, ostopalautustilaus tai lähtevä siirtotilaus.
2. Valitse **Luo varaston poiminta** -valintaruutu.  
3. Valitse **OK**-painike. Uusi varaston poiminta luodaan.

## Useiden varaston poimintojen luominen eräajon avulla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo varaston hyllytys/poiminta/siirto** ja valitse sitten vastaava linkki.  
2. Suodata **F.varastoinnin pyyntö** -pikavälilehden **Lähdeasiakirja**- ja **Lähteen nro** -kenttien avulla tietyntyyppiset asiakirjat tai asiakirjanumerovälit. Voit esimerkiksi luoda poimintoja vain myyntitilauksille.  
3. Valitse **Asetukset**-pikavälilehdessä **Luo varaston poiminta** -valintaruutu.
4. Valitse **OK**-painike.

## Poiminnan luominen kahdessa vaiheessa

### Pyydä varastopoiminta vapauttamalla lähdeasiakirja

Jos kyseessä on myyntitilaus, ostopalautustilaus tai lähtevä siirto, voit luoda fyysisen varastoinnin pyynnön vapauttamalla tilauksen. Tilauksen vapauttamien mahdollistaa nimikkeiden poiminnan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.
2. Valitse ensin vapautettava myyntitilaus ja sitten **Vapauta**-toiminto.

### Lähdeasiakirjaan perustuvan varaston poiminnan luominen

Kun tilaus on vapautettu, varastotyöntekijä voi luoda varaston poiminnan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston poiminnat** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Valitse **Lähdeasiakirja**-kentässä poimittavan lähdeasiakirjan tyyppi.  
4. Valitse **Lähteen nro** -kentässä lähdeasiakirja.  
5. Vaihtoehtoisesti valitsemalla **Hae lähdeasiakirja** -toiminto voidaan luoda niiden lähtevien lähdeasiakirjojen luettelo, jotka ovat sijainnissa valmiita poimintaan.  
6. Täytä poimintarivit valittujen lähdeasiakirjojen mukaan valitsemalla **OK**.  

## Varaston poimintojen kirjaaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston poiminta** ja valitse sitten vastaava linkki.  
2. Poimintarivien **Varastopaikkakoodi**-kentässä varastopaikka, josta nimikkeet on poimittava, ehdotetaan nimikkeen oletusvarastopaikan mukaan. Voi muuttaa tarvittaessa varastopaikkaa tällä sivulla.  
3. Suorita poiminta ja syötä poimittu määrä **Käsiteltävä määrä** -kenttään.

    Jos rivin nimikkeitä on poimittava useammasta kuin yhdestä varastopaikasta esimerkiksi siksi, että varastopaikassa ei ole koko määrää, käytä **Rivit**-pikavälilehden **Jaa rivi** -toimintoa. Toiminto luo rivin jäljellä olevalle käsiteltävälle määrälle.

4. Valitse **Kirjaa**-toiminto.  

    * Lähdeasiakirjan poimittujen rivien toimituksen kirjaaminen.
    * Jos sijainnissa käytetään varastopaikkoja, kirjaus luo myös fyysisen varastotapahtumat varastopaikan määrässä tapahtuneiden muutosten kirjaamiseen.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## Tilausta varten kokoonpantavien nimikkeiden käsitteleminen varaston poimintojen avulla

**Varaston poiminta** -sivua voi käyttää myös sellisten nimikkeiden myyntiin poimimiseen ja toimittamiseen, jotka on kokoonpantava ennen toimitusta. Lisätietoja on kohdassa [Tilausta varten kokoonpantavien nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).

Tilausta varten kokoonpantavat nimikkeet eivät ole fyysisesti varastopaikassa, ennen kuin ne koottu ja kirjattu tuotoksena varastopaikkaan. Tilausta varten kokoonpantavien nimikkeiden poimintaan varastopaikasta toimituksiin käytetään erityistyönkulkua.

1. Varastopaikasta varastotyöntekijät vievät kokoonpanon nimikkeet toimituslaituriin ja kirjaavat sitten varastopoiminnan.
2. Kirjattu varaston poiminta kirjaa kokoonpanon tuotoksen, komponentin kulutuksen ja myyntitoimituksen.

Voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in luomaan varaston siirron automaattisesti, kun varastopoiminta luodaan kokoonpanon nimikkeelle. **Luo siirrot automaattisesti** -kenttä valitaan **Kokoonpanon asetukset** -sivulla. Lisätietoja on kohdassa [Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

Myyntinimikkeiden varaston poimintarivit luodaan eri tavalla sen mukaan, onko tilaukseen kokoonpantu mitään, joitakin vai kaikki myyntirivin määrille määritetyt määrät. Skenaarioissa, joissa osa määrästä kokoonpannaan ja osa poimitaan varastosta, luodaan vähintään kaksi varaston poimintariviä.

Myynnissä, jossa myyntitilauksen koko määrä kokoonpannaan tilausta varten, kyseiselle määrälle luodaan yksi varaston poimintarivi. **Kokoonpantava määrä** -kentän arvo on sama kuin **Toimitettava määrä** -kentän arvo. **Kokoonpantava määrä** -kenttä on valittu rivillä.

Jos sijaintiin ei ole määritetty kokoonpanon tuotoksen työnkulkua, varaston poimintarivin **Varastopaikan koodi** -kentässä on seuraavien kenttien arvo seuraavassa järjestyksessä.

* ***Kok. til.ltoimit. -var.p.koodi** <!-- not applicable for inv pick-->
* **Kokoonpanosta-varastop.koodi**

Jos myyntitilausriville ei ole määritetty varastopaikkakoodia eikä sijainnille kokoonpanon tuotoksen työnkulkua, varaston poimintarivin **Varastopaikan koodi** -kenttä on silloin tyhjä. Varastotyöntekijän on avattava **Varastopaikan sisältö** -sivu ja valittava varastopaikka, johon kokoonpanon nimikkeet kootaan.

Skenaarioissa, joissa osa määrästä on kokoonpantava ja osa poimittava, luodaan vähintään kaksi poimintariviä.

* Yksi poimintarivi on tilausta varten kokoonpantavalle määrälle. [!INCLUDE [prod_short](includes/prod_short.md)] käyttää seuraavia kenttiä annetussa järjestyksessä varastopaikan koodin määrittämiseen: **Varastopaikan koodi**, **Kok. til.ltoimit. -var.p.koodi** ja sitten **Kokoonpanosta-varastop.koodi**. Jos nämä kentät ovat tyhjiä, varastotyöntekijän on avattava **Varastopaikan sisältö** -sivu ja valittava varastopaikka, johon nimikkeet kootaan.  
* Toinen poimintarivi määräytyy sen mukaan, mistä varastopaikoista voidaan täyttää jäljellä oleva määrä. Jos nimikettä säilytetään useissa varastopaikoissa, useita rivejä luodaan. Ottorivi perustuu **Toimitettava määrä** -kentän määrään.

> [!NOTE]  
> Jos nimikkeet ovat tilausta varten kokoonpantavia, varaston poiminta koskee linkitettyä myyntitilausta, kunnes varastosiirto luodaan kaikille kokoonpanon komponenteille.  

## Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Vaihekuvaus: Poiminta ja toimitus fyysisen varastoinnin perusmäärityksissä](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
