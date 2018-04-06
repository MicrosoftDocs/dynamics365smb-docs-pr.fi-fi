---
title: KP-budjettien luominen| Microsoft Docs
description: "Tässä artikkelissa käsitellään, miten luodaan KP-budjetteja ennustamaan erilaisia taloudellisia toimintoja ja miten dimensiot määritetään liiketoimintatietoja varten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f6969d05cfde9ba7ce5767a961d4af1c7b3bd983
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="create-gl-budgets"></a>KP-budjettien luominen
Sinulla voi olla useita budjetteja samalle ajanjaksolle, kun luot budjetit eri nimillä. Määrittele ensin budjetin nimi ja syötä budjettiluvut. Budjetin nimi tulee sitten kaikkiin luomiisi budjettitapahtumiin.  

 Kun luot budjetin, voit määritellä jokaiselle budjetille neljä dimensiota. Näitä budjettikohtaisia dimensioita kutsutaan budjettidimensioiksi. Valitse budjettidimensiot jo luomistasi dimensioista. Budjettidimensioita voidaan käyttää, kun halutaan asettaa suodatin budjetille tai kun halutaan lisätä dimensiotietoa budjettitapahtumiin. Lisätietoja on kohdassa [Dimensioiden käyttäminen](finance-dimensions.md).

 Budjeteilla on tärkeä osa liiketoimintatiedoissa, kuten KP-raporttimalleihin perustuvissa tilinpäätöksissä, jotka sisältävät budjettitapahtumia, tai analysoitaessa budjetoituja summia todellisia summia vastaan tilikartassa. Lisätietoja on ohjeaiheessa [Business Intelligence](bi.md).

 Budjeteilla on tärkeä osa budjettitapahtumia sisältävissä liiketoimintatiedoissa, kuten KP-raporttimalleihin perustuvissa tilinpäätöksissä, tai analysoitaessa tilikartan budjetoituja ja todellisia summia. Lisätietoja on kohdassa [Business Intelligence](bi.md).

Voit käsitellä kustannusbudjetteja samalla tavoin kustannuslaskennassa. Lisätietoja on kohdassa [Kustannusbudjettien luominen](finance-create-cost-budgets.md).    

## <a name="to-create-a-new-gl-budget"></a>Uuden KP-budjetin luominen  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KP-budjetit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Muokkaa luetteloa** -toiminto ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Valitse **Muokkaa budjettia** -toiminto.
4. Täyttämällä **Budjetti**-ikkunan yläosan kentät määrität, mitä näytetään.  

    Näytössä näkyvät vain ne tapahtumat, joilla on **Budjetin nimi** -kentässä annettu nimi. Koska budjetin nimi on juuri luotu, suodatinta vastaavia tapahtumia ei ole. Tämän vuoksi ikkuna on tyhjä.  
5. Jos haluat lisätä summan, napsauta solua matriisissa. **KP-budjetin tapahtumat** -ikkuna avautuu.  
6. Luo uusi rivi ja määritä **Summa**-kentän arvo. Sulje **KP-budjetin tapahtumat** -ikkuna.  
7. Toista vaiheet 5 ja 6, kunnes olet määrittänyt kaikki budjettisummat.  

> [!NOTE]  
>  **Suodattimet** -pikavälilehdessä voit suodattaa budjettitietoja sen mukaan, mitä budjettidimensioita olet luonut budjetin nimen alle.   

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Business Intelligence](bi.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

