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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1d312a9c93b1cb93a7ff2582d49600f09597359a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3180808"
---
# <a name="set-up-automatic-account-posting-groups"></a>Automaattisten tilin kirjausryhmien määrittäminen
Voit käyttää automaattisia tilikoodeja automaattisen tilin kirjausryhmän luonnin jälkeen.  

## <a name="to-set-up-automatic-account-posting-groups"></a>Automaattisten tilin kirjausryhmien määrittäminen  

1.  Valitse ![Etsi sivu tai raportti](../../media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Automaattijakauma** ja valitse sitten aiheeseen liittyvä linkki.  
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
