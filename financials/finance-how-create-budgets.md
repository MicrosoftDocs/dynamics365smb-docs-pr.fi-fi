---
title: Budjettien luonti| Microsoft Docs
description: "Tässä artikkelissa kuvataan, miten luot budjetteja ennustamaan erilaisia taloudellisia toimintoja ja miten määrität dimensioita liiketoimintatietoja varten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7dfd3cc7efe00b48a39982bb220ccc21b7409da4
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create--budgets"></a>Uusien budjettien luominen
Sinulla voi olla useita budjetteja samalle ajanjaksolle, kun luot budjetit eri nimillä. Määrittele ensin budjetin nimi ja syötä budjettiluvut. Budjetin nimi tulee sitten kaikkiin luomiisi budjettitapahtumiin.  

 Kun luot budjetin, voit määritellä jokaiselle budjetille neljä dimensiota. Näitä budjettikohtaisia dimensioita kutsutaan budjettidimensioiksi. Valitse budjettidimensiot jo luomistasi dimensioista. Budjettidimensioita voidaan käyttää, kun halutaan asettaa suodatin budjetille tai kun halutaan lisätä dimensiotietoa budjettitapahtumiin. Lisätietoja on kohdassa [Dimensioiden käyttäminen](finance-dimensions.md).

 Budjeteilla on tärkeä osa liiketoimintatiedoissa, kuten KP-raporttimalleihin perustuvissa tilinpäätöksissä, jotka sisältävät budjettitapahtumia, tai analysoitaessa budjetoituja summia todellisia summia vastaan tilikartassa. Lisätietoja on ohjeaiheessa [Business Intelligence](bi.md).   

 > [!NOTE]  
>   Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).  

### <a name="to-create-a-new-budget"></a>Uuden budjetin luominen  

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **KP-budjetit** ja valitse sitten aiheeseen liittyvä linkki.  
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
