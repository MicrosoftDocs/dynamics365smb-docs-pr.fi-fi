---
title: Pankkitilien hallinta |Microsoft Docs
description: Pankkitapahtumat on täsmäytettävä säännöllisesti niihin liittyviin pankkitilitapahtumiin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: db4afccdd67e400f2effd34b2db3c449db10432a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779705"
---
# <a name="reconciling-bank-accounts"></a>Pankkitilien täsmäytys

Pankkitilin täsmäytys tulee suorittaa säännöllisin väliajoin kaikille pankkitileille, jotta yrityksen käteistietueet ovat oikein. Voit tehdä tämän vertaamalla sisäisten pankkitilien tapahtumia pankkitapahtumiin pankistasi ja kirjaamalla sitten saldot sisäisiin pankkitileihin, jolloin summat ovat talouspäälliköiden käytettävissä. Pankkitilin täsmäytys on myös käytännöllinen tapa löytää ja ratkaista puuttuvat maksut ja kirjanpitovirheet.

Voit suorittaa tehtävän erikseen maksukäsittelystä **Pankkitilin täsmäytys** -sivulla, jossa etsit vastaavat (täsmäytät) vasemmassa ruudussa olevat pankin tiliotteen rivit oikealla puolella olevien sisäisen pankkitilin kirjanpidon tapahtumien kanssa. Vaihtoehtoisesti voit suorittaa tämän tehtävän **Maksujen täsmäytyskirjauskansio** -sivulla pankin tiliotteessa olevien maksujen käsittelyn osana. Molemmilla sivuilla voi täyttää pankin tiliotteen tiedot tuomalla tiedoston tai syötteen ja voit käyttää automaattisia vastaavuusehdotuksia.

> [!NOTE]  
> Pohjois-Amerikan versioissa voi suorittaa pankkitilin täsmäytyksen myös **Pankin täsmäytyksen työkirja** -sivulla, joka sopii paremmin sekeille ja talletuksille mutta ei sisällä pankin tiliotetiedostojen tuontia. Voit käyttää tätä sivua **Pankkitilin täsmäytys** -sivun sijasta poistamalla **Pankin täsmäytys ja autom. vastaavuus** -kentän valinta **Pääkirjanpidon asetukset** -sivulla. Lisätietoja on kohdan [Pankkitilien täsmäyttäminen](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) Yhdysvaltain paikallisissa toimintoja käsittelevässä osassa.

Jokainen pankkitili on määritettävä pankkitilin kortiksi, ennen kuin pankkitilejä voidaan hallita kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]. Lisäksi on määritettävä sähköiset palvelut, joita käytetään pankin tiliotteen tuonnissa ja maksutiedoston viennissä. Lisätietoja on kohdassa [Pankkitoiminnan määrittäminen](bank-setup-banking.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.

| Tehtävä | Katso |
| --- | --- |
| Täsmäytä pankkitilit erillisenä tehtävänä **Pankkitilin täsmäytys** -sivulla. |[Pankkitilien täsmäytys](bank-how-reconcile-bank-accounts-separately.md) |
| Täsmäytä maksukäsittelyyn liittyvät pankkitilit **Maksujen täsmäytyskirjauskansio** -sivulla. |[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

> [!TIP]
> Pankkitilin täsmäytyksen avulla voi varmistaa, että kirjat ovat ajan tasalla ja että täsmäytystä ei kirjata, ennen kuin olet tyytyväinen täsmäytykseen.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Pankkitilien täsmäytys](bank-how-reconcile-bank-accounts-separately.md)  
[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Siirrä pankkivarat](bank-how-transfer-bank-funds.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]