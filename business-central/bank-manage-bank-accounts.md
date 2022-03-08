---
title: Pankkitilien hallinta |Microsoft Docs
description: Pankkitapahtumat on täsmäytettävä säännöllisesti niihin liittyviin pankkitilitapahtumiin.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 01/10/2020
ms.author: sgroespe
ms.openlocfilehash: 0d1a38468f5d07a1170027bc728ba16996f2b782
ms.sourcegitcommit: 2f741f442226b8be74586e355f283f365e43220f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947235"
---
# <a name="reconciling-bank-accounts"></a>Pankkitilien täsmäytys
Pankkitilin täsmäytys tulee suorittaa säännöllisin väliajoin kaikille pankkitileille, jotta yrityksen käteistietueet ovat oikein. Voit tehdä tämän vertaamalla sisäisten pankkitilien tapahtumia pankkitapahtumiin pankistasi ja kirjaamalla sitten saldot sisäisiin pankkitileihin, jolloin summat ovat talouspäälliköiden käytettävissä. Pankkitilin täsmäytys on myös käytännöllinen tapa löytää ja ratkaista puuttuvat maksut ja kirjanpitovirheet.

Voit suorittaa tehtävän erikseen maksukäsittelystä **Pankkitilin täsmäytys** -sivulla, jossa etsit vastaavat (täsmäytät) vasemmassa ruudussa olevat pankin tiliotteen rivit oikealla puolella olevien sisäisen pankkitilin kirjanpidon tapahtumien kanssa. Vaihtoehtoisesti voit suorittaa tämän tehtävän **Maksujen täsmäytyskirjauskansio** -sivulla pankin tiliotteessa olevien maksujen käsittelyn osana. Molemmilla sivuilla voi täyttää pankin tiliotteen tiedot tuomalla tiedoston tai syötteen ja voit käyttää automaattisia vastaavuusehdotuksia.

> [!NOTE]  
> Pohjois-Amerikan versioissa, voit suorittaa pankkitilin täsmäytyksen myös **Pankin täsmäytyksen työkirja** -sivulla, joka sopii paremmin sekeille ja talletuksille, mutta ei tarjoa pankin tiliotetiedostojen tuomista. Voit käyttää tätä sivua **Pankkitilin täsmäytys** -sivun sijasta poistamalla **Pankin täsmäytys ja autom. vastaavuus** -kentän valinta **Pääkirjanpidon asetukset** -sivulla. Lisätietoja löydät Yhdysvaltain paikalliset toiminnot -ohjeen Pankkitilien täsmäyttäminen -kohdassa.

Jokainen pankkitili on määritettävä pankkitilin kortiksi, ennen kuin pankkitilejä voidaan hallita kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)]. Lisäksi on määritettävä sähköiset palvelut, joita käytetään pankin tiliotteen tuonnissa ja maksutiedoston viennissä. Lisätietoja on kohdassa [Pankkitilien määrittäminen](bank-setup-banking.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.

| Tehtävä | Katso |
| --- | --- |
| Täsmäytä pankkitilit erillisenä tehtävänä **Pankkitilin täsmäytys** -sivulla. |[Pankkitilien täsmäytys](bank-how-reconcile-bank-accounts-separately.md) |
| Täsmäytä maksukäsittelyyn liittyvät pankkitilit **Maksujen täsmäytyskirjauskansio** -sivulla. |[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Siirrä pankkivarat](bank-how-transfer-bank-funds.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)
