---
title: Automaattisten tilin kirjausryhmien määrittäminen
description: Voit käyttää automaattisia tilikoodeja automaattisen tilin kirjausryhmän luonnin jälkeen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: ca456f36adf3aaf67d1317f63fdcf6df2a89b5d2
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300216"
---
# <a name="set-up-automatic-account-posting-groups"></a>Automaattisten tilin kirjausryhmien määrittäminen
Voit käyttää automaattisia tilikoodeja automaattisen tilin kirjausryhmän luonnin jälkeen.  

## <a name="to-set-up-automatic-account-posting-groups"></a>Automaattisten tilin kirjausryhmien määrittäminen  

1.  Valitse ![Etsi sivu tai raportti -kuvake](../../media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Automaattijakauma** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Täytä **Yleinen**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |-----------|-----------------|  
    |**Nro**|Anna automaattiselle tilin kirjausryhmälle yksilöivä aakkosnumeerinen numero.|  
    |**Kuvaus**|Anna automaattisen tilin kirjausryhmän kuvaus.|  

4.  Täytä **Automaattinen tilirivi** -pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |-----------|-----------------|  
    |**Kohdistusprosentti**|Anna lähderivin summan kohdistettava prosentti.|  
    |**KP-tilinro**|Anna kirjanpitotilin numero, jolle kohdistus kirjataan.|  

    > [!NOTE]  
    >  **Kokonaissaldo**-kentässä lasketaan yhteen kirjausryhmän automaattisten tilirivien **Kohdistusprosentti**-kentän arvot. Jos kirjausryhmän kokonaiskohdistusprosentti ei ole nolla, nimikkeen kirjauksen yhteydessä näytetään virhesanoma.  

5.  Valitse **OK**-painike.  

## <a name="see-also"></a>Katso myös  
 [Automaattiset tilikoodit](automatic-account-codes.md)   
 [Kirjausryhmien määrittäminen](../../finance-posting-groups.md)  
 [Rahoitus](../../finance.md)
