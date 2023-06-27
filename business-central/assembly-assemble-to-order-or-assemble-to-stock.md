---
title: Tietoja Kokoonpano tilausta varten- ja Kokoonpano varastoon -toiminnoista
description: Tietoja nimikkeiden kokoamisesta myyntitilauksiin tai varastoitavaksi tulevaa myyntiä varten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock" />Tietoja Kokoonpano tilausta varten- ja Kokoonpano varastoon -toiminnoista

[!INCLUDE [prod_short](includes/prod_short.md)] sallii kokoonpanon nimikkeiden toimittamisen seuraavilla tavoilla:

* Kokoonpano tilausta varten  
* Kokoonpano varastoon  

## <a name="assemble-to-order" />Kokoonpano tilausta varten

Tilausta kokoonpanoa varten käytetään nimikkeissä, joita ei haluta varastoida. Syy tähän voi olla esimerkiksi jokin seuraavista:

* Nimikkeet mukautetaan asiakkaiden vaatimusten mukaisesti.
* Varastointikulut halutaan pitää mahdollisimman pieninä.

Seuraavassa luettelossa on joitakin tilausten varten kokoamisprosessin etuja:  

* Kokoonpanon nimikkeet mukautetaan myyntitilauksen yhteydessä.  
* Kokoonpanon nimikkeen ja sen komponenttien yleinen saatavuus.  
* Kokoonpanon komponenttien varaaminen heti varmistaa tilauksen täyttämisen.  
* Mukautetun tilauksen kannattavuus määritetään koostamalla hinta ja kustannukset.  
* Integrointi fyysiseen varastoon helpottaa kokoonpanoa ja toimitusta.  
* Kokoonpano tilausta varten myyntitarjousta tai puitemyyntitilausta luotaessa.  
* Varastomäärien ja tilausta varten koottavien määrien yhdistäminen.  

Kun prosessina on kokoonpano tilausta varten, myyntitilauksen nimikkeet kootaan. Kokoonpanotilauksen ja myyntitilauksen välillä on yksi yhteen -linkki.  

Kun tilausta varten koottava nimike syötetään myyntitilausriville, kokoonpanotilaus luodaan automaattisesti. Kokoonpanotilaus perustuu myyntiriviin, ja sen rivit perustuvat nimikkeen kokoonpanon tuoterakenteeseen. Kokoonpanon tuoterakenteen komponenttien määrä kerrotaan tilauksen määrällä. **Kokoonpano tilausta varten -rivit** -sivulla on tietoja linkitetyissä kokoonpanotilauksen riveistä. Tiedot voivat auttaa mukauttamaan kokoonpanon nimikettä. Toimituspäivä perustuu komponenttien saatavuuteen. Lisätietoja nimikkeiden kokoamisesta myyntitilaukseen on kohdassa [Tilauksen mukaan koottujen nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
> Vaikka kyse ei ole oletusprosessin osasta, varastomääriä ja tilausta varten koottuja määriä voidaan myydä samassa myyntitilauksessa. Lisätietoja varastoitujen ja tilausta varten koottujen nimikkeiden yhdistämisestä on kohdassa [Varastonimikkeiden myyminen kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

Nimike määritetään tilausta varten koottavaksi valitsemalla nimikkeen **Nimikekortti**-sivun **Kokoonpanokäytäntö**-kentässä **Kokoonpano tilausta varten**.  

## <a name="assemble-to-stock" />Kokoonpano varastoon

Kokoonpano varastoon -prosessia käytetään nimikkeissä, jotka kokoonpannaan ja varastoidaan tulevaa myyntiä varten. Varastoon kokoonpantavat nimikkeet ovat vakionimikkeitä, kuten tuotepaketteja, joita ei mukauteta. Näitä nimikkeitä voidaan kuluttaa myös alikokoonpanon komponentteina. Nämä nimikkeet poimitaan ja niitä käsitellään yksittäisenä nimikkeinä, jotka katsotaan valmistuneiksi tuotantonimikkeiksi. Lisätietoja kokoonpanon nimikkeistä on kohdassa [Nimikkeiden kokoaminen](assembly-how-to-assemble-items.md).  

Kun myyntiriville määritetään varastoon koottava nimike, nimikettä käsitellään samoin kuin muitakin varastosta myytäviä nimikkeitä. [!INCLUDE [prod_short](includes/prod_short.md)] esimerkiksi tarkistaa vain kootun nimikkeen, ei sen komponenttien saatavuuden.  

> [!NOTE]  
> Vaikka kyse ei ole oletusprosessin osasta, nimike voidaan koota tilaukseen, vaikka se olisi määritetty varastoon koottavaksi. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden ja varastonimikkeiden myyminen yhdessä](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)  

Nimike määritetään varastoon koottavaksi valitsemalla nimikkeen **Nimikekortti**-sivun **Kokoonpanokäytäntö**-kentässä **Kokoonpano varastoon**.  

## <a name="combination-scenarios" />Yhdistelmäskenaariot

Kun tilausta varten kootut määrät ja varastomäärät yhdistetään myyntirivillä, tilausta varten kootut on toimitettava ensimmäisenä.  

Jos kokoonpanotilaus on linkitetty myyntitilauksen riville, myyntitilausrivin **Kokoonpantava määrä tilausta varten** -kentän arvo kopioidaan **Kokoonpantava määrä** -kenttään kokoonpanotilauksen **Määrä**-kentän välityksellä. Lisätietoja on kohdassa [Tilausta varten kokoonpantavien nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).  

**Kokoonpantava määrä** -kentän arvo liittyy myyntitilausrivin **Toimitettava määrä** -kentän arvoon. Tämä suhde määrittää, miten tilausta varten kokoonpantava määrät toimitetaan osittain tai kokonaan:

* Myyntitilausrivin koko määrä kootaan tilausta varten
* Yhdistelmäskenaarioissa osa määrästä kokoonpannaan tilausta varten ja osa toimitetaan varastosta.

Yhdistelmäskenaario mahdollistaa joustavat osittaiset toimitukset. **Kokoonpantava määrä** -kentän avulla voidaan määrittää määrä, joka toimitetaan osittain varastosta ja osittain tilausta varten kokoonpantuna.  

Jos myyntirivin koko määrä on kokoonpantava tilausta varten ja toimitettava, **Toimitettava määrä** -kentän arvo kopioidaan linkitetyn kokoonpanotilauksen **Kokoonpantava määrä** -kenttään toimitettavan määrän muuttuessa. Tämä päivitys varmistaa, että toimitettu määrä on täysin tilausta varten kokoonpannun määrän mukainen.   

Yhdistelmäskenaarioissa **Toimitettava määrä** -kentän koko arvoa ei kuitenkaan kopioida kokoonpanotilauksen **Kokoonpantava määrä** -kenttään. Oletusarvo lisätään sen sijaan **Kokoonpantava määrä** -kenttään. Arvo lasketaan **Toimitettava määrä** -kentästä, mikä varmistaa, että tilausta varten kokoonpantavat määrät toimitetaan ensin.

Oletusarvosta poikkeaminen esimerkiksi siksi, että kokoonpantavan määrän halutaan olevan suurempi tai pienempi kuin **Toimitettava määrä** -kentässä oleva määrä, **Kokoonpantava määrä** -kenttää voi muokata ennalta määritettyjen sääntöjen mukaisesti seuraavan kuvan tavoin.  

Kokoonpantavaa määrää voitaisiin muokata esimerkiksi siksi, että varastomäärien toimituksen osakirjaus halutaan tehdä on kokoonpanon tuotoksen toimittamista.  

Seuraavissa taulukoissa käsitellään sääntöjä, joilla määritetään pienin ja suurin **Kokoonpantava määrä** -kenttään annettava arvo, kun halutaan poiketa yhdistelmätilanteen oletusarvosta. Taulukossa näkyy yhdistelmätilanne, jossa linkitetyn myyntitilausrivin arvo **Toimitettava määrä** -kentässä muutetaan 7:stä 4:ksi, ja **Kokoonpantava määrä** -oletusarvoksi tulee sen vuoksi 4.  

**Myyntitilausrivi**

|                | **määrä** | **Toimitettava määrä** | **Kokoonpantava määrä tilausta varten** | **Toimitettu määrä** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Alkuarvo**| 10          | 7                | 7                             | 0                    |
|**Muutos**      |              | 4                |                               |                      |

**Kokoonpanotilauksen otsikko**

|                | **määrä** | **Toimitettava määrä** | **Kokoonpantava määrä tilausta varten** | **Toimitettu määrä** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Alkuarvo**| 7           | 7                | 0                             | 7                    |
|**Muutos**      |              | 4 (lisätään oletusarvon mukaan)|                         |                      |

Tämän esimerkin perusteella **Kokoonpantava määrä** -kenttää voidaan muuttaa seuraavasti:  

* Pienin syötettävä määrä on 1. Vähintään yksi yksikkö on koottava, jotta neljän yksikön myynti on mahdollista, olettaen, että loput kolme ovat saatavana varastossa.  
* Suurin määrä, joka voidaan syöttää on 4. Tämä raja varmistaa, että kokoonpantavien nimikkeiden määrä ei ylitä myyntiin tarvittavaa määrää.  

## <a name="see-related-microsoft-training" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Kokoonpanon tuoterakenteiden käyttäminen](assembly-how-work-assembly-boms.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastonhallinnan yleiskatsaus](design-details-warehouse-management.md)
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
