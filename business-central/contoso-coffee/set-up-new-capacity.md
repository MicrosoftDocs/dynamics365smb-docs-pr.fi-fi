---
title: Määritä uusi kapasiteetti
description: 'Vaihekuvauksessa opit määrittämään uuden tuotantosolun, jossa on kapasiteettikalenteri yksittäistä vuoroa varten Business Centralissa.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Vaihekuvaus: Määritä uusi kapasiteetti

Tässä artikkelissa on tietoja Contoso Coffee -esittelyn tietojen käytöstä kapasiteetin hallinnassa.  

## Esimerkkitilanne

Olet Contoso Coffeen tuotantosuunnittelija. Vastauksena tuotantokerroksen muutoksiin sinun täytyy määrittää uusi tuotantosolu, testiosasto. Uudessa tuotantosolussa on yksi kuormitusryhmä, testaus. Uusissa keskuksissa täytyy olla kapasiteettikalenteri yksittäiselle vuorolle klo 8-16 maanantaista perjantaihin.  

## Vaiheet

1. Määritä tuotantosolu.

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **tuotantosolut** ja valitse sitten vastaava linkki.  

    2. Valitse **Uusi**-toiminto ja täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä  |Arvo  |
        |---------|---------|
        |**Ei.** |700|
        |**Nimi** |Testiosasto|
        |**Tuotantosoluryhmän koodi** |1, Tuotanto-osasto|
        |**Välitön yksikkökustannus**|3.25|
        |**Yksikkökustannuslaskenta**|Aika|
        |**Materiaalinottotapa**|Manuaalinen|
        |**Yleinen tuotteen kirjausryhmä**|EI ALV:TÄ</br></br>Huomaa, että tämä valinta riippuu laskenta-asetuksista ja maasta.|
        |**Mittayksikön koodi** |MINUUTTIA|
        |**Kapasiteetti** |1|
        |**Tehokkuus** |90|
        |**Tuotantokalenterin koodi** |1|

        **Tuotantokalenterin koodi** -kentässä asetus 1 tarkoittaa yhtä vuoroa maanantaista perjantaihin.

    3. Sulje tuotantosolun kortti.

2. Määritä kuormitusryhmä.

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **kuormitusryhmät** ja valitse sitten vastaava linkki.  

    2. Valitse **Uusi**-toiminto ja täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä  |Arvo  |
        |---------|---------|
        |**Ei.** |760|
        |**Nimi** |Testaus|
        |**Tuotantosolunro** |700, Testiosasto|
        |**Välitön yksikkökustannus**|3.25|
        |**Materiaalinottotapa**|Manuaalinen|
        |**Yleinen tuotteen kirjausryhmä**|EI ALV:TÄ</br></br>Huomaa, että tämä valinta riippuu laskenta-asetuksista ja maasta.|
        |**Kapasiteetti** |1|
        |**Tehokkuus** |90|
    3. Laajenna **Reitityksen asetukset** -pikavälilehti ja syötä **Määritysaika**-kenttään *10*.  

3. Laske kuormitusryhmän kapasiteettikalenteri.  

    1. Valitse **Kalenteri**-toiminto.  

    2. Määritä **Kuormitusryhmän kalenteri** -sivun **Matriisivaihtoehdot**-pikavälilehdessä **Näyttöperuste**-kentän arvoksi *Kuukausi*.  

    3. Valitse **Näytä matriisi** -toiminto.  

    4. Valitse **Kuormitusryhmän kalenterimatriisi** -sivulla **Laske**-toiminto.  

    5. Määritä **Laske kuormitusryhmän kalent.** -sivun **Vaihtoehdot**-pikavälilehdessä **Aloituspvm**-kentän arvoksi *1. tammikuuta*.  

    6. Aseta **Lopetuspvm** -kentän arvoksi 31. joulukuuta.  

    7. Täytä **Kuormitusryhmä**-pikavälilehden **Nro** -suodatinkenttä, valitse *760, testaus*.  

    8. Valitse **OK**-painike. Kun eräajo on valmis, se palauttaa sinut **Kuormitusryhmän kalenterimatriisi** -sivulle.  

    9. Valitse **Päivitä**-toiminto.  

    10. Kuormitusryhmä 760, testaus -rivillä valitse arvo Tammikuu-sarakkeessa.  

**Kalenteritapahtumat**-sivulla **Kapasiteetti (yhteensä)** -kentän päivittäiset kapasiteettitapahtumat ovat 480 minuuttia. Tämä vastaa yhtä 8 tunnin vuoroa jokaiselle työpäivälle. **Kapasiteetti (varsinainen)** -kentässä näkyy myös 432 minuuttia. Tämä ilmaisee kuormitusryhmälle määritetyn 90 prosentin tehokkuusprosentin.  

## Katso myös

[Johdatus Contoson kahvidemotietoihin](contoso-coffee-intro.md)  
