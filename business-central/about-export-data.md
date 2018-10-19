---
title: Business Central -tietojen vieminen Exceliin | Microsoft Docs
description: "Voit viedä tilinpäätökset ja liiketoimintatiedot Business Central -sovelluksesta Exceliin tai avata tiedot Excelissä."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 33ccc1dbe9654245129bdbd760896054c10cd2f1
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="exporting-your-business-data-to-excel"></a>Liiketoimintatietojen vienti Exceliin
Jos haluat käsitellä [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja Excelissä, voit avata kaikki luettelot Excelissä ja käsitellä niitä siellä. Jos haluat vastaavasti peruuttaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in tilauksen, voit viedä tiedot Exceliin, jotta ne ovat edelleen käytettävissä.

## <a name="opening-lists-in-excel"></a>Luetteloiden avaaminen Excelissä
Voit avata minkä tahansa päiväkirjan, luettelon tai työkirjan tiedot Excelissä. Avaa haluamasi sivu ja valitse sitten **Avaa Excelissä**. Voit esimerkiksi avata asiakasluettelon (hae **Asiakkaat**) ja valitse sitten **Avaa Excelissä**. Selain pyytää sinua avaamaan tai tallentamaan luodun Excel-työkirjan.  

Jokaisessa luettelossa tietty määrä sarakkeita, ja Exceliin viedään kaikki nykyisessä näkymässä olevat sarakkeet. Jos haluat lisätä tai poistaa sarakkeita ennen luettelon avaamista Excelissä, sinun tarvitsee vain avata jonkin sarakkeen pikavalikko ja määrittää, mitkä sarakkeet haluat nähdä. Sarakeluettelo vaihtelee luettelon mukaan, ja se vastaa sen tietokannan rakennetta, johon tiedot on tallennettu. Jos et ole varma, minkä tyyppistä tietoa tietyssä sarakkeessa on, voit lisätä sen näkymään ja päättää sitten, haluatko poistaa sen uudelleen.  

### <a name="edit-data-in-excel"></a>Muokkaa tietoja Excelissä
Oma [!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää laajennuksen Exceliin niin, että Excel-tietoja voidaan muokata. Lisätietoja on kohdassa [Rahoituslaskelmien analysointi Microsoft Excelissä](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Tietojen vienti muihin rahoitusjärjestelmiin
Jos päätät peruuttaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in tilauksen, voit viedä tiedot Exceliin ja viedä ne sitten seuraavaa rahoitusjärjestelmään.  

Voit tietenkin viedä kaikki sivut, mutta et kuitenkaan välttämättä tarvitse niitä kaikkia. Kannattaakin harkita vain seuraavien keskeisten sivujen vientiä. Muista myös lisätä kaikki sarakkeet edellä kuvatulla tavalla.  

* Tilikartta  
* Asiakkaat  
* Toimittajat  
* Pankit  
* Nimikkeet  

Jos haluat myös kaikki rahoitustapahtumat, kyse on suuresta tietomäärästä, joten vienti ei useinkaan tapahdu muutamassa minuutissa. Rahoitustapahtumat näkyvät **Pääkirjanpidon tapahtumat** -ikkunassa.  

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
>   Jos olet määrittänyt [!INCLUDE[d365fin](includes/d365fin_md.md)]iin useita yrityksiä, kunkin yrityksen kyseiset tiedot on vietävä.

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)]-tilauksen peruuttaminen](admin-cancel.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Rahoituslaskelmien analysointi Microsoft Excel](finance-analyze-excel.md):issä  
[Rahoitus](finance.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

