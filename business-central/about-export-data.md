---
title: Business Central -tietojen vieminen Exceliin | Microsoft Docs
description: Voit viedä tilinpäätökset ja liiketoimintatiedot Business Central -sovelluksesta Exceliin tai avata tiedot Excelissä.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0058fd8aa684fd12392e641dda3bbb0ee6862134
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753690"
---
# <a name="exporting-your-business-data-to-excel"></a>Liiketoimintatietojen vienti Exceliin
Jos haluat käsitellä [!INCLUDE[prod_short](includes/prod_short.md)]in tietoja Excelissä, voit avata kaikki luettelot Excelissä ja käsitellä niitä siellä. Jos haluat vastaavasti peruuttaa [!INCLUDE[prod_short](includes/prod_short.md)]in tilauksen, voit viedä tiedot Exceliin, jotta ne ovat edelleen käytettävissä.

## <a name="opening-lists-in-excel"></a>Luetteloiden avaaminen Excelissä
Voit avata minkä tahansa päiväkirjan, luettelon tai työkirjan tiedot Excelissä. Avaa haluamasi sivu ja valitse sitten **Avaa Excelissä**. Voit esimerkiksi avata asiakasluettelon (hae **Asiakkaat**) ja valitse sitten **Avaa Excelissä**. Selain pyytää sinua avaamaan tai tallentamaan luodun Excel-työkirjan.  

> [!NOTE]
> Käytä tätä vaihtoehtoa, jos et halua tehdä muutoksia ja julkaista niitä takaisin [!INCLUDE[prod_short](includes/prod_short.md)]iin.  

Jokaisessa luettelossa tietty määrä sarakkeita, ja Exceliin viedään kaikki nykyisessä näkymässä olevat sarakkeet. Jos haluat lisätä tai poistaa sarakkeita ennen luettelon avaamista Excelissä, sinun tarvitsee vain avata jonkin sarakkeen pikavalikko ja määrittää, mitkä sarakkeet haluat nähdä. Sarakeluettelo vaihtelee luettelon mukaan, ja se vastaa sen tietokannan rakennetta, johon tiedot on tallennettu. Jos et ole varma, minkä tyyppistä tietoa tietyssä sarakkeessa on, voit lisätä sen näkymään ja päättää sitten, haluatko poistaa sen uudelleen.  

### <a name="edit-data-in-excel"></a>Muokkaa tietoja Excelissä
Oma [!INCLUDE[prod_short](includes/prod_short.md)] sisältää laajennuksen Exceliin niin, että Excel-tietoja voidaan muokata. Lisätietoja on kohdassa [Rahoituslaskelmien analysointi Microsoft Excelissä](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Tietojen vienti muihin rahoitusjärjestelmiin
Jos päätät peruuttaa [!INCLUDE[prod_short](includes/prod_short.md)]in tilauksen, voit viedä tiedot Exceliin ja viedä ne sitten seuraavaa rahoitusjärjestelmään.  

Voit tietenkin viedä kaikki sivut, mutta et kuitenkaan välttämättä tarvitse niitä kaikkia. Kannattaakin harkita vain seuraavien keskeisten sivujen vientiä. Muista myös lisätä kaikki sarakkeet edellä kuvatulla tavalla.  

* Tilikartta  
* Asiakkaat  
* Toimittajat  
* Pankit  
* Nimikkeet  

Jos haluat myös kaikki rahoitustapahtumat, kyse on suuresta tietomäärästä, joten vienti ei useinkaan tapahdu muutamassa minuutissa. Rahoitustapahtumat näkyvät **Pääkirjanpidon tapahtumat** -sivulla.  

Myös seuraavien sivujen tietojen vienti on suositeltavaa:  

* Asiakastapahtumat  
* Toimittajatapahtumat  
* Pankkitilitapahtumat  
* Nimiketapahtumat  
* Yleiset kirjausasetukset  
* Asiakkaan kirjausryhmät  
* Toimittajan kirjausryhmät  
* Nimikkeen kirjausryhmät  
* Pankkitilin kirjausryhmä  
* KP-budjetit  
* KP-budjetin tapahtumat  
* Myyntitarjoukset  
* Myyntilaskut  
* Ostolaskut  
* Kontaktit  
* Myyjät  

> [!NOTE]  
> Jos olet määrittänyt [!INCLUDE[prod_short](includes/prod_short.md)]iin useita yrityksiä, kunkin yrityksen kyseiset tiedot on vietävä.

> [!NOTE]
> Tietojen avaaminen tai muokkaaminen Excelissä edellyttää vähintään yhtä seuraavista käyttöoikeuksista:
>    - käyttöoikeuksien joukko *D365 Excelin vientitoiminto*  
>    - Järjestelmän käyttöoikeus 6110 *Salli toiminnon vieminen Exceliin*.  

Lisätietoja on kohdassa [Käyttäjän käyttöoikeuksien yleiskatsauksen hankkiminen](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös
[[!INCLUDE[prod_short](includes/prod_short.md)]-tilauksen peruuttaminen](admin-cancel.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Rahoituslaskelmien analysointi Microsoft Excel:issä](finance-analyze-excel.md)  
[Rahoitus](finance.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
