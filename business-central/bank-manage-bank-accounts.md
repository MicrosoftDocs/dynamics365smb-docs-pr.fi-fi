---
title: Pankkitilien hallinta |Microsoft Docs
description: "Pankkitapahtumat on täsmäytettävä säännöllisesti niihin liittyviin pankkitilitapahtumiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 05/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 319faa64adc93c9e54cf792325daeb6a5a8e0b80
ms.contentlocale: fi-fi
ms.lasthandoff: 06/28/2018

---
# <a name="managing-bank-accounts"></a>Pankkitilien hallinta
Täsmäytä [!INCLUDE[d365fin](includes/d365fin_md.md)]in pankkitilitapahtumat säännöllisin väliajoin pankin pankkitilin liittyvien pankkitapahtumien kanssa. Kirjaa sitten saldo pankkitilille. Voit suorittaa tämän tehtävän **Maksujen täsmäytyskirjauskansio** -kohdassa pankin tiliotteessa olevien maksujen käsittelyn osana. Vaihtoehtoisesti voit suorittaa tehtävän erikseen maksukäsittelystä **Pankkitilin täsmäytys** -ikkunasta, jossa etsit vastaavat (täsmäytät) pankin tiliotteen rivit vasemmassa ruudussa sisäisen pankkitilin kirjanpidon tapahtumien kanssa oikealla puolella. Molemmissa ikkunoissa voi täyttää pankin tiliotteen tiedot tuomalla tiedoston tai syötteen ja voit käyttää automaattisia vastaavuusehdotuksia.

> [!NOTE]  
> Pohjois-Amerikan versioissa, voit suorittaa pankkitilin täsmäytyksen myös **Pankin täsmäytyksen työkirja** -ikkunassa, joka sopii paremmin sekeille ja talletuksille, mutta ei tarjoa pankin tiliotetiedostojen tuomista. Voit käyttää tätä ikkunaa **Pankkitilin täsmäytys** -ikkunan sijasta poistamalla **Pankin täsmäytys ja autom. vastaavuus** -kentän valinnan **Pääkirjanpidon asetukset** -ikkunassa. Lisätietoja löydät Yhdysvaltain paikalliset toiminnot -ohjeen Pankkitilien täsmäyttäminen -kohdassa.

[!INCLUDE[d365fin](includes/d365fin_md.md)]issa on joskus siirrettävä summia pankkitilien välillä pankin siirtojen mukaisesti. Tämä tehtävä suoritetaan **Yleinen päiväkirja** -ikkunassa varojen valuutan osoittamalla tavalla.

Jokainen pankkitili on määritettävä pankkitilin kortiksi, ennen kuin pankkitilejä voidaan hallita. Lisäksi on määritettävä sähköiset palvelut, joita käytetään pankin tiliotteen tuonnissa ja maksutiedoston viennissä. Lisätietoja on kohdassa [Pankkitilien määrittäminen](bank-setup-banking.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.

| Toiminta | Katso |
| --- | --- |
| Täsmäytä maksukäsittelyyn liittyvät pankkitilit **Maksujen täsmäytyskirjauskansio** -ikkunassa. |[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Täsmäytä pankkitilit, kuten sekkitapahtumat, erillisinä tehtävinä **Pankkitilin täsmäytys** -ikkunassa. |[Pankkitilien täsmäyttäminen erikseen](bank-how-reconcile-bank-accounts-separately.md) |
| Kirjaa pankkitilien väliset siirrot samassa valuutassa tai eri valuutoissa. |[Siirrä pankkivarat](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Katso myös
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

