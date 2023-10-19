---
title: Variantit
description: 'Vaihekuvaus, jossa kerrotaan, miten tuotteen kunkin variantin kysyntäennuste päivitetään Business Centralin avulla.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-variants"></a>Vaihekuvaus: Variantit

Tässä artikkelissa on tietoja Contoso Coffee -esittelyn tietojen käytöstä varianttien suhteen.

## <a name="scenario"></a>Esimerkkitilanne

Olet Contoso Coffeen tuotantosuunnittelija. Jokaisen nimikkeen SP-SCM1006, AutoDripLite variantin osalta on päivitettävä kysyntäennuste. Koska ne ovat eri värisiä, sinun täytyy varmistaa, että oikeaa tuoterakennetta (BOM) käytetään kunkin variantin osalta. Suorita suunnittelutyökirja toimitusten laskemiseksi.  

## <a name="steps"></a>Vaiheet

1. Määritä varastointiyksiköt nimikkeelle SP-SCM1006, AutoDripLite. Määritä tuoterakenne varastointiyksikölle muunnoksilla PUNAINEN ja VALKOINEN.

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä *Nimikkeet* ja valitse sitten vastaava linkki.  

    2. Avaa nimike **SP-SCM1006, AutoDripLite**.

    3. Valitse **Luo varastointiyksikkö** -toiminto.  

    4. Määritä **Luo per** -kentän arvoksi *Sijainti & variantti*.

    5. Aseta suodatin sijainnille arvoon *MAIN* ja valitse sitten **OK**-painike.

    6. Valitse **Varastointiyksiköt**-toiminto.  

    7. Päivitä seuraavien varastointiyksiköiden tuotannon tuoterakenteet:

        1. PUNAINEN, MAIN, aseta SP-SCM1006-RED  

        2. VALKOINEN, MAIN, aseta SP-SCM1006-WHITE  

        3. Säilytä tuotannon tuoterakenteen nro tyhjänä arvolle MUSTA ja MAIN  

2. Päivitä tuotannon asetukset ja kunnioita kysynnän ennustetta sijainneissa ja varianteissa.  

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä *Tuotannon asetukset* ja valitse sitten vastaava linkki.  

    2. Ota käyttöön **Käytä ennustetta sijainnissa** -kenttä.

    3. Ota käyttöön **Käytä ennustetta variantille** -kenttä.

    4. Sulje **Tuotannon asetukset** -ikkuna.

3. Luo uusi kuukausittainen kysyntäennuste, *AUTODRIP*. Suodata se nimikkeellä SP-SCM1006 ja sijainnilla MAIN. Aseta kunkin variantin kysyntä toukokuussa. 

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä *Kysynnän ennuste* ja valitse sitten vastaava linkki.

    2. Luo uusi kysyntäennuste nimellä *AUTODRIP*.

    3. Valitse **Muokkaa kysyntäennustetta** -toiminto.

    4. Valitse **Näyttöperuste** -kentässä *Kuukausi*.

    5. Valitse **Nimikesuodatus**-kentässä *SP-SCM1006*

    6. Ota käyttöön **Käytä ennustetta sijainnissa** -kenttä.

    7. Valitse **Sijaintisuodatus**-kentässä *MAIN*.

    8. Ota käyttöön **Käytä ennustetta variantille** -kenttä.

    9. Kunkin rivin päivitettyjen arvojen osalta toukokuun sarakkeessa

        1. PUNAINEN, MAIN, aseta 100

        2. VALKOINEN, MAIN, aseta 200

        3. MUSTA, MAIN, aseta 300

    10. Sulje Kysyntäennuste-ikkunat

4. Suorita tuotanto-ohjelman suunnitelma toukokuussa luoduille kysyntäennusteille. Tarkastele komponentteja ja tarkista, että nimikkeen maalit korreloivat variantin kanssa.

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä *Suunnittelutyökirja* ja valitse sitten vastaava linkki.

    2. Valitse **Laske uudelleensuunnittelu** -toiminto.

    3. Ota käyttöön **Tuotanto-ohjelma**-kenttä.

    4. Poista käytöstä **Tuotanto-ohjelma**-kenttä.

    5. Valitse **Aloituspvm**-kentässä *1. toukokuuta*

    6. Valitse **Lopetuspvm**-kentässä *31. toukokuuta*

    7. Valitse **Käytä ennustetta** -kentässä *AUTODRIP*

    8. Valitse **OK**-toiminto.

    9. Valitse jokaiselle luodulle riville **Komponentit**-toiminto ja tarkista, mitä maalia käytetään.  

## <a name="see-also"></a>Katso myös

[Johdatus Contoson kahvidemotietoihin](../contoso-coffee-intro.md)  
