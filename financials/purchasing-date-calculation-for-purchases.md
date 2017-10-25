---
title: "Ostojen päivämäärälaskenta | Microsoft Docs"
description: "Ohjelma laskee automaattisesti päivämäärän, jolloin nimike on tilattava sen saamiseksi tietyn päivän varastoon. Tämä on päivämäärä, jona voi odottaa tiettynä päivänä tilattujen nimikkeiden olevan valmiita poimittaviksi."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7e569474e3d222a56500665fa73408f47480f338
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

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

## <a name="calculating-without-a-requested-delivery-date"></a>Laskeminen ilman pyydettyä toimituspäivämäärää  
Jos lisäät ostotilausrivin ilman pyydettyä toimituspäivämäärää, ohjelma lisää rivin **Tilauspvm**-kenttään ostotilauksen tunnistetietojen **Tilauspvm**-kentän päivämäärän. Tällöin tilauspäivämäärä on joko lisäämäsi päivämäärä tai käsittelypäivämäärä. Ohjelma laskee sen jälkeen seuraavat päivämäärät ostotilausriville käyttäen tilauspäivämäärää lähtökohtana:  

- tilauspvm + toimitusajan laskenta = suunniteltu vast.ottopvm.  
- Suunniteltu vast.otto pvm + Saapuva f.var. Käsittelyaika + Toimitusajan varmistus = Oletettu vast.otto pvm  

Jos muutat rivillä olevaa tilauspäivämäärää (esimerkiksi siitä syystä, että nimikkeet eivät ole saatavilla toimittajallasi ennen kuin myöhempänä ajankohtana), ohjelma laskee automaattisesti uudelleen riville asianmukaiset päivämäärät.  

Jos muutat tilauspäivämäärää tunnistetiedoissa, ohjelma kopioi tämän päivämäärän kaikkien rivien **Tilauspvm**-kenttiin, ja tämän jälkeen se laskee kaikki asiaan liittyvät päivämääräkentät uudelleen.  

## <a name="see-also"></a>Katso myös  
 [Myynnin päivämäärälaskenta](sales-date-calculation-for-sales.md)   
 [Toimituksen lupaamisen päivämäärän laskeminen](sales-how-to-calculate-order-promising-dates.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

