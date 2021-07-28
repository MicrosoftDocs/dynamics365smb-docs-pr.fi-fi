---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 636cbbd2e20dd357fba734187195f64d8ccaa754
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6440049"
---
Voit käyttää automaattisia tilikoodeja automaattisen tilin kirjausryhmän luonnin jälkeen.  

## <a name="to-set-up-automatic-account-posting-groups"></a>Automaattisten tilin kirjausryhmien määrittäminen  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Automaattiset tiliryhmät** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Täytä **Yleinen**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |-----------|-----------------|  
    |**Nro**|Anna automaattiselle tilin kirjausryhmälle yksilöivä aakkosnumeerinen numero.|  
    |**Kuvaus**|Anna automaattisen tilin kirjausryhmän kuvaus.|  

4. Täytä **Automaattinen tilirivi** -pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |-----------|-----------------|  
    |**Kohdistusprosentti**|Anna lähderivin summan kohdistettava prosentti.|  
    |**KP-tilinro**|Anna kirjanpitotilin numero, jolle kohdistus kirjataan.|  

    > [!NOTE]  
    >  **Kokonaissaldo**-kentässä lasketaan yhteen kirjausryhmän automaattisten tilirivien **Kohdistusprosentti**-kentän arvot. Jos kirjausryhmän kokonaiskohdistusprosentti ei ole nolla, nimikkeen kirjauksen yhteydessä näytetään virhesanoma.  

5. Valitse **OK**-painike.  
