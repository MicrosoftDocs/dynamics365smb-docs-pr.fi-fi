---
title: Ostojen päivämäärälaskenta | Microsoft Docs
description: Sovellus laskee automaattisesti päivämäärän, jolloin nimike on tilattava sen saamiseksi tietyn päivän varastoon. Tämä on päivämäärä, jona voi odottaa tiettynä päivänä tilattujen nimikkeiden olevan valmiita poimittaviksi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 046c829955b38f6f5ea416e0a80c1fe058476942
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918887"
---
# <a name="date-calculation-for-purchases"></a>Ostojen päivämäärälaskenta

[!INCLUDE[d365fin](includes/d365fin_md.md)] laskee automaattisesti päivämäärän, jona nimike on tilattava sen saamiseksi tietyn päivän varastoon. Tämä on päivämäärä, jona voi odottaa tiettynä päivänä tilattujen nimikkeiden olevan valmiita poimittaviksi.  

Jos määrität ostotilauksen otsikolle pyydetyn vastaanottopäivämäärän, laskettu tilauspäivämäärä on päivämäärä, jona tilaus on asetettava vastaanottamaan nimikkeet pyytämänäsi päivämääränä. Sitten lasketaan päivämäärä, jolloin nimikkeet ovat poimittavissa, ja syötetään se **Oletettu vastaanottopvm** -kenttään.  

Jos et määritä pyydettyä vastaanottopäivämäärää, ohjelma käyttää rivillä olevaa tilauspäivämäärää lähtökohtana laskiessaan päivämäärän, jona voit olettaa vastaanottavasi nimikkeet, ja päivämäärän, jona nimikkeet ovat poimittavissa.  

## <a name="calculating-with-a-requested-receipt-date"></a>Laskeminen pyydetyn vastaanottopäivämäärän avulla

Jos ostotilausrivillä on pyydetty vastaanottopäivämäärä, ohjelma käyttää tätä päivämäärää lähtökohtana seuraaville laskennoille:  

- Pyydetty vast.ottopvm - Toimitusajan laskenta = Tilauspvm  
- Pyydetty vast.otto pvm + Saapuva f.var. Käsittelyaika + Toimitusajan varmistus = Oletettu vast.otto pvm  

Jos syötit ostotilauksen otsikkoon pyydetyn vastaanottopäivämäärän, ohjelma kopioi tämän päivämäärän kaikkien tilausrivien vastaavaan kenttään. Päivämäärää voi muuttaa tarpeen mukaan millä tahansa rivillä, tai rivillä olevan päivämäärän voi poistaa.  

> [!NOTE]
> Jos prosessi perustuu taaksepäin laskentaan ja esimerkiksi tilauspäivä saadaan käyttämällä pyydettyä vastaanottopäivää, on suositeltavaa käyttää päivämääräkaavoja, joiden kesto on kiinteä. Sellainen on esimerkiksi 5P viidelle päivälle tai 1V yhdelle viikolle. Päivämääräkaava, jonka kesto ei ole kiinteä, kuten KV kuluvalle viikolle tai KK kuluvalle kuukaudelle, voi aiheuttaa virheellisiä päivämäärälaskelmia. Lisätietoja päivämääräkaavoista on kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-delivery-date"></a>Laskeminen ilman pyydettyä toimituspäivämäärää

Jos lisäät ostotilausrivin ilman pyydettyä toimituspäivämäärää, ohjelma lisää rivin **Tilauspvm**-kenttään ostotilauksen tunnistetietojen **Tilauspvm**-kentän päivämäärän. Tällöin tilauspäivämäärä on joko lisäämäsi päivämäärä tai käsittelypäivämäärä. Ohjelma laskee sen jälkeen seuraavat päivämäärät ostotilausriville käyttäen tilauspäivämäärää lähtökohtana:  

- tilauspvm + toimitusajan laskenta = suunniteltu vast.ottopvm.  
- Suunniteltu vast.otto pvm + Saapuva f.var. Käsittelyaika + Toimitusajan varmistus = Oletettu vast.otto pvm  

Jos muutat rivillä olevaa tilauspäivämäärää (esimerkiksi siitä syystä, että nimikkeet eivät ole saatavilla toimittajallasi ennen kuin myöhempänä ajankohtana), ohjelma laskee automaattisesti uudelleen riville asianmukaiset päivämäärät.  

Jos muutat tilauspäivämäärää tunnistetiedoissa, ohjelma kopioi tämän päivämäärän kaikkien rivien **Tilauspvm**-kenttiin, ja tämän jälkeen se laskee kaikki asiaan liittyvät päivämääräkentät uudelleen.  

## <a name="default-values-for-lead-time-calculation"></a>Toimitusajan laskennan oletusarvot

[!INCLUDE[d365fin](includes/d365fin_md.md)] laskee tilauksen ja oletetut vastaanottopäivämäärät käyttäen ostotilausrivin **Toimitusajan laskenta** -kentän arvoa.  

Voit määrittää manuaalisesti rivin arvon tai antaa ohjelman käyttää arvoja, jotka on määritetty toimittajan kortissa, nimikkeen kortissa, varastointiyksiköiden kortissa tai nimikkeen toimittajakatalogissa.
Toimittajan kortin toimitusajan arvoa käytetään kuitenkin vain, jos toimitusajan nimikettä ei ole määritetty nimikkeen kortissa, varastointiyksiköiden kortissa tai nimikkeen toimittajakatalogissa. Tämä on myös näiden arvojen priorisointijärjestys. Jos ne ovat kaikki käytettävissä, toimittajan kortin toimitusajalla on alhaisin prioriteetti, ja nimikkeen toimittajakatalogin toimitusajalla on korkein prioriteetti.  

## <a name="see-also"></a>Katso myös

[Myynnin päivämäärälaskenta](sales-date-calculation-for-sales.md)   
[Toimituksen lupaamisen päivämäärien laskeminen](sales-how-to-calculate-order-promising-dates.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
