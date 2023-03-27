---
title: Tuotantotilausten luominen myyntitilauksista
description: 'Tietoja eri tavoista, joiden avulla voidaan luoda tuotettujen nimikkeiden tuotantotilaukset suodaan myyntitilauksista.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '99000883, 99000884,'
---
# Tuotantotilausten luominen myyntitilauksista

Voit luoda tuotettujen nimikkeiden tuotantotilaukset suodaan myyntitilauksista.  

## Tuotantotilausten luominen myyntitilauksista  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Valitse myyntitilaus, jolle haluat luoda tuotantotilauksen.  
3. Valitse **Suunnittelu**-toiminto. Nimikkeen saatavuus näkyy **Myyntitilaus suunnittelu** -sivulla.  
4. Valitse **Luo tuotantotilaus** -toiminto.  
5. Valitse tila ja tilaustyyppi.  
6. Valitse **Kyllä** -painike luodaksesi yhden tai useamman tuotantotilauksen niiden rivien osalta, joilla on **Tuotantotilaus** **Täydennysjärjestelmä**-kentässään.

    > [!NOTE]  
    > Kysyntärivit, joiden **Täydennysjärjestelmä**-kentässä on **Tuotantotilaus**, ilmaisevat perustana olevat tuotantotilaukset. Kun nämä tuotantotilaukset on luotu, on muistettava määrittää niiden mahdollinen täyttämätön komponenttikysyntä. Täyttämätön kysyntä voidaan tunnistaa käyttämällä **Tilauksen suunnittelu** -sivua tai **Uudelleensuunnittelu**-toimintoa.
    >
    > Kun myyntitilauksille luodaan tuotantotilauksia Myyntitilauksen suunnittelu -sivulla, tilausten välisiä linkkejä käytetään kysynnän ja tarjonnan välillä. Kun tilausten välisiä linkkejä on määritetty, suunnittelujärjestelmä ei sisällytä linkitettyä tarjontaa tai varastoa täsmäytykseen. Lisätietoja täsmäytyksestä on kohdassa [Tilausten väliset linkit](design-details-central-concepts-of-the-planning-system.md#order-to-order-links).

## Tilaustyyppi  

Seuraavassa taulukossa käsitellään kaksi tuotantotilausten luontitapaa.

|Asetus|Kuvaus|
|------|-----------|
|Nimiketilaus|Kullekin nimikkeelle, jolla on rivi **Myyntitilauksen suunnittelu** -sivulla, luodaan yksi tuotantotilaus.|
|Projektitilaus|Kaikille nimikkeille, joilla on rivi **Myyntitilauksen suunnittelu** -sivulla, luodaan yksi monirivinen tuotantotilaus. Projektitilauksia käytettäessä tuotantotilauksen **Lähdetyyppi**-kentässä on **Myynnin tunnistetiedot**. Tilauksessa on yksi rivi kullekin tuotettavalle myyntitilausriville.|

## Katso myös  

[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md)  
[Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
