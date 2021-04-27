---
title: Tietojen tuominen Business Central -ohjelmaan Excelin avulla
description: Voit lisätä asiakastietoja Excelissä oletusmäärityspaketin avulla ja tuoda tiedot takaisin Business Central -sovellukseen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 984186e8bb08cc9e99ab91dbc08f0e85c58e0804
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777946"
---
# <a name="importing-business-data-from-other-finance-systems"></a>Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä

Kun rekisteröidyt [!INCLUDE[prod_short](includes/prod_short.md)]iin, voit luoda tyhjän yrityksen, ladata siihen omat tietosi ja testata uuden [!INCLUDE[prod_short](includes/prod_short.md)]-yrityksesi. Yrityksen tällä hetkellä käytössä olevan rahoitusratkaisun mukaan voit siirtää tietoja asiakkaista, toimittajista, varastosta ja pankkitileistä.  

Roolikeskuksen avustetun asennusoppaan avulla voit siirtää liiketoimintatiedot Excel-tiedostosta tai muista muodoista. Ladattavissa olevien tiedostojen tyyppi riippuu käytettävissä olevista laajennuksista. Voit esimerkiksi siirtää tietoja QuickBooks-ohjelmasta, koska [!INCLUDE[prod_short](includes/prod_short.md)] sisältää laajennuksen, joka käsittelee QuickBooks-tietojen muunnoksen. Jos haluat siirtää tietoja muista rahoitusratkaisuista, tarkista, onko kyseiselle ratkaisulle saatavana laajennus, tai tuo tiedot Excelistä.  

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää malleja tileille, asiakkaille, toimittajille ja varastonimikkeille, joita voit kohdistaa tietojen tuomisen yhteydessä.

Voit tuoda päätiedot ja joitakin tapahtumatietoja muista rahoitusjärjestelmistä [!INCLUDE[prod_short](includes/prod_short.md)]in oletusmäärityspaketin perusteella. Voit käsitellä tuotavaa pakettia **Määrityspaketit**-sivulla, jossa voit myös tarkistaa tiedot ennen paketin käyttämistä.  

> [!TIP]  
> Suosittelemme, että käytät tietojen siirtotoimintoja, jos haluat tuoda tietoja Dynamics GP:stä, Dynamics NAVista tai QuickBooksista. Lisätietoja on kohdassa [Paikallisten tietojen siirtäminen Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) -ohjelmaan hallintasisällössä tai [QuickBooks-tiedonsiirto-ohjelmassa](ui-extensions-quickbooks-data-migration.md).

> [!NOTE]  
> Jos kyseessä on suuri toteutustyö, voit käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in RapidStart Servicesia. Se koostuu työkalupaketista, jonka avulla määritetään uusia ratkaisuja asiakkaiden liiketoimintavaatimusten ja asetustietojen perusteella. RapidStart Services sisältää myös liiketoimintatietojen tuontitoimintoja. Lisätietoja on kohdassa [Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md).

Voit tuoda nimikekuvat **Varastonhallinnan asetukset** -sivulla olevalla toiminnolla. Lisätietoja on kohdassa [Useiden nimikekuvien tuominen](inventory-how-import-item-pictures.md).

## <a name="importing-data-from-configuration-packages"></a>Tietojen tuominen määrityspaketeista
[!INCLUDE[prod_short](includes/prod_short.md)] sisältää määrityspaketin, jonka voit viedä Exceliin tietojen määrittämiseksi siellä. Tämän jälkeen voit tuoda tiedot uudelleen Excelistä. Paketissa on 27 taulukkoa, mukaan lukien päätiedot, kuten asiakkaat, toimittajat, nimikkeet ja tilit, muita perusasetustaulukkoja, kuten toimitustavat, ja tapahtumataulukot, kuten myyntiotsikko ja rivit.  

> [!NOTE]  
>   Määrityspakettien käyttäminen on lisätoiminto ja onkin suositeltavaa keskustella sen käytöstä järjestelmänvalvojan kanssa. Lisätietoja on kohdassa [Tietojen tuominen vanhasta kirjanpito-ohjelmistosta määrityspaketin avulla](across-import-data-configuration-packages.md).

## <a name="working-with-data-in-excel"></a>Tietojen käsittely Excelissä
Kun tuot oletusmäärityspaketin Exceliin, luodussa työkirjassa on kutakin paketin taulukkoa vastaava laskentataulukko. Yksinkertaistaaksesi tehtäviä voit hyödyntää XML manipulointityökaluja, jotka on sisällytetty Exceliin. Voit käyttää myös Excelin valmiita funktioita tietojen muotoilun auttamiseksi ja tiedon asettamiseksi oikeisiin soluihin. Lisää esimerkiksi tyhjä laskentataulukko ja kopioi vanhat tiedot siihen. Tee sitten Excel-kaava määrittämään muunnostyökirjan tiedot viedyn laskentataulukon kenttien ja vanhojen asiakastietojen välille. Kun olet yhdistänyt kaikki tiedot, kopioi tietoalue taulukon työkirjaan.  

> [!IMPORTANT]  
>  Älä muuta sarakkeita työkirjoissa. Jos niitä on siirretty, muutettu tai poistettu, laskentataulukkoa ei voi tuoda [!INCLUDE[prod_short](includes/prod_short.md)]iin.

> [!NOTE]
> BLOB-tyypin kenttiä ei voi viedä tai tuoda Excelin avulla.

## <a name="tables-in-the-default-configuration-package"></a>Oletusmäärityspaketin taulukot
Oletusmäärityspaketti tukee seuraavia taulukoita:

-   Maksuehdot
-   Asiakkaan hintaryhmä
-   Toimitusehto
-   Myyjä/Ostaja
-   Sijainti
-   KP-tili
-   Asiakas
-   Toimittaja
-   Vaihtoehto
-   Myynnin tunnistetiedot
-   Myyntirivi
-   Ostojen tunnistetiedot
-   Ostorivi
-   Yl. päiväkirjan rivi
-   Nimikepäiväkirjan rivi
-   Asiakkaan kirjausryhmä
-   Toimittajan kirjausryhmä
-   Varaston kirjausryhmä
-   Mittayksikkö
-   Yl. liiketoim. kirjausryhmä
-   Yl. Tuotteen kirjausryhmä
-   Yleiset kirjausasetukset
-   Territorio
-   Nimikeluokka
-   Myyntihinta
-   Ostohinta

## <a name="see-also"></a>Katso myös
[Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md)  
[Paikallisten tietojen siirtäminen Business Central Onlineen](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[QuickBooks-tietojen siirto](ui-extensions-quickbooks-data-migration.md)  
[Useiden nimikekuvien tuominen](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]