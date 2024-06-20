---
title: Varastopaikkatyyppien määrittäminen
description: 'Määritä varastopaikkojen tyypit ja työnkulkujen perusaktiviteetit ja määritä samalla tapa, jolla varastopaikkoja käytetään tietyissä fyysisen varaston toiminnoissa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 7367
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Varastopaikkatyyppien määrittäminen

Ohjelma on rakennettu ohjaamaan nimikevirta varastopaikkojen läpi, jotka olet määritellyt tietyille fyysisen varastoinnin aktiviteeteille. Kullekin varastopaikalle annetaan nimikevirran perusaktiviteetit – ja samalla määritellään tapa, jolla ohjelma käyttää varastopaikkaa – määrittelemälle sille varastopaikan tyyppi.  

Tyyppejä on kuusi. Voit käyttää fyysistä varastointia kaikilla kuudella mahdollisella varastopaikan tyypillä tai voit valita käyttäväsi vain VASTOTTO-, HYLLPOIM-, LÄHETYS- JA QC-varastopaikan tyyppejä. Nämä neljä varastopaikan tyyppiä mahdollistavat sen, että ohjelma voi tehdä ehdotuksia nimikevirran tukemiseksi, ja ne mahdollistavat varaston eroavaisuuksien tallentamisen.  

## Haluamiesi varastopaikan tyyppien määrittäminen

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastopaikkatyypit** ja valitse sitten vastaava linkki.  
2.  Luo **Varastopaikkatyypit**-sivulla 10-merkkinen koodi varastopaikan tyypille.  
3.  Valitse aktiviteetti, jotka voidaan suorittaa kullekin varastopaikan tyypille.  

> [!NOTE]  
>  Varastopaikkatyypit ovat käytössä vain, jos sijainnissa on käytössä ohjattu hyllytys ja poiminta.  

Varastopaikan tyyppi määrittää, miten ohjelma käyttää tiettyä varastopaikkaa käsitellessään nimikkeiden virtaa varaston läpi. Voit aina ohittaa ohjelman ehdotukset missä tahansa fyysisen varastoinnin asiakirjassa ja voit siirtää nimikkeitä varastopaikkaan tai varastopaikasta tekemällä fyysisen varastoinnin siirron.  

Varastopaikat, joita voi luoda, on luetteloitu seuraavassa.  

|Varastopaikan tyyppi|Description|  
|------------------|---------------------------------------|  
|VAST.OTTO|Nimikkeet, jotka on rekisteröity kirjatuiksi vastaanotoiksi, mutta niitä ei ole vielä hyllytetty.|  
|LÄHETYS|Nimikkeet, jotka on poimittu fyysisen varastoinnin toimitusriveille, mutta joita ei ole vielä kirjattu toimitetuiksi.|  
|HYLLYTYS|Yleensä kohteet voidaan tallentaa suurina mittayksiköinä, mutta et halua käyttää sitä poimintatarkoituksiin. Koska näitä varastopaikkoja ei käytetä keräilyyn, niin tuotantotilauksia kuin toimituksiakaan varten, Hyllytys-tyyppisten varastopaikkojen käyttö voi olla rajallista, mutta tämä varastopaikan tyyppi voi olla hyödyllinen, jos olet ostanut suuren määrän nimikkeitä. Tämän tyyppisillä varastopaikoilla pitäisi aina olla matala varastopaikan luokitus, jotta kun vastaanotetut nimikkeet hyllytetään, muut nimikkeeseen liitetyt korkeamman luokituksen PUTPICK-varastopaikat hyllytetään ensin. Jos käytät tämän tyyppistä varastopaikkaa, sinun täytyy tehdä varastopaikan täydennys säännöllisesti, jotta näihin varastopaikkoihin varastoidut nimikkeet olisivat saatavilla myös HYLLPOIM- ja POIMINTA-tyyppisissä varastopaikoissa.|  
|POIMINTA|Nimikkeille, joita käytetään vain poimintaan, esimerkiksi nimikkeille, joiden vanhentumispäivämäärä lähestyy, ja jotka olet siirtänyt tämän tyyppiseen varastopaikkaan. Näille varastopaikoille olisi hyvä asettaa korkea varastopaikan luokittelu, jotta niiden poimimista ehdotetaan ensin.|  
|HYLLPOIM|Nimikkeet varastopaikoissa, joille on ehdotettu sekä hyllytys- että poimintatoimintoa. Tämän tyyppisillä varastopaikoilla on todennäköisesti eri varastopaikan luokitteluja. Voit määrittää irtotavaran varastopaikat tämän tyyppiseksi varastopaikaksi, jolla on matalia varastopaikan luokitteluja verrattuna tavallisiin poimintavarastopaikkoihin tai edelleen poimimisen alueiden varastopaikkoihin.|  
|QC|Tätä varastopaikkaa käytetään varastomuutoksille, jos varastopaikka määritetään sijaintikortissa **Muutosvarastopaikan koodi** -kentässä. Tämän tyyppisiä varastopaikkoja voi määrittää myös viallisille nimikkeille ja tarkastettaville nimikkeille. Nimikkeitä voi siirtää tämän tyyppiseen varastopaikkaan, jos haluat, että ne eivät ole saatavilla tavallisessa nimikevirrassa.<br /><br /> **HUOMAUTUS:** Toisin kuin kaikki muut varastopaikkatyypit, **QC** -varastopaikkatyypillä ei ole valittuna nimikkeen käsittelyn valintaruutuja oletusarvoisesti. Tämä osoittaa, että QC-varastopaikkaan asetettu sisältö jää pois nimikevirroista.|  

## Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
