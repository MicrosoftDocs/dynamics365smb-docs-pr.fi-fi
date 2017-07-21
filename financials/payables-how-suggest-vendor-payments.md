---
title: "Ehdota toimittajamaksuja -eräajon käyttäminen| Microsoft Docs"
description: "Määrittämällä toimittajan maksuasetukset saat ehdotuksia maksuista, joiden eräpäivä on pian tai joissa on käytettävissä alennus."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 50daaf0a9f0d3beb31a75aa8c554c8833b4d2c8e
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-suggest-vendor-payments"></a>Toimittajamaksujen ehdottaminen
Voit ehdottaa maksurivejä käyttämällä **Maksupäiväkirja**-ikkunassa **Ehdota toimittajamaksuja** -eräajoa. Asetusten mukaan ehdotetaan rivejä, kuten pian erääntyviä maksuja tai maksuja, joissa on käytettävissä maksualennus.

Ehdotettuja rivejä voi hyödyntää täysimääräisesti, kun toimittajat on ensin priorisoitu. Lisätietoja on ohjeaiheessa [Toimintaohje: Toimittajien priorisoiminen](purchasing-how-prioritize-vendors.md).  

**Estossa**-tilassa olevat toimittajatapahtumat eivät sisälly tähän.  

> [!IMPORTANT]  
>   Jos haluat käyttää maksualennuksia ja olet antanut käytettävissä olevan summan, summaa käytetään  

* priorisoiduissa erääntyvissä toimittajatapahtumissa tärkeysjärjestyksessä  
* erääntyneissä toimittajatapahtumissa, joita ei ole priorisoitu  
* avoimissa toimittajatapahtumissa, joissa voi käyttää maksualennuksia, toimittajanumeron mukaan järjestettynä.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>Ehdota toimittajamaksuja -toiminnon käyttäminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksupäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.  
2. Avaa asianmukainen päiväkirja ja valitse **Ehdota toimittajamaksuja** -toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Valitse **OK**-painike.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Eräpäivän lisääminen maksupäiväkirjan rivien kirjauspäivämääräksi
Kun **Ehdota toimittajamaksuja** -eräajoa käytetään toimittajien maksurivien luomisessa, täyttämällä kaksi erikoiskenttää voi varmistaa, että luodut rivit käyttävät eräpäivää kirjauspäivämäärän laskemisessa. Nämä kentät ovat **Laske kirjauspäivämäärä kohdistuksen asiakirjan eräpäivästä** ja **Kohdistuksen asiakirjan eräpäivän siirtymä**.  

> [!IMPORTANT]  
>   Et voi käyttää **Laske kirjauspäivämäärä kohdistuksen asiakirjan eräpäivästä** -kenttää yhdessä **Hae maksualennukset**- tai **Tee yhteenveto toimittajittain** -kentän kanssa. Jos kirjauspäivä perustuu eräpäivään, joitain maksualennuksia ei ehkä ole laskettu oikein, koska kirjauspäivä on maksualennuspäivän jälkeen.  

Jos laskettu kirjauspäivämäärä on myös menneisyydessä, kirjauspäivämäärää siirretään käsittelypäivämäärään ja näyttöön tulee varoitus.  

Vaihtoehtoisesti voit luoda maksurivejä manuaalisesti niin, että eräpäivää käytetään kirjauspäivämäärän laskemisessa. Kun kohdistat toimittajatapahtumia, voit päivittää päiväkirjan rivin kirjauspäivän liittyvän ostolaskun eräpäivällä käyttämällä **Laske kirjauspäivämäärä** -toimintoa. Lisätietoja on kohdassa [Toimintaohje: Ostotapahtumien kohdistaminen manuaalisesti](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
>   Jos ostolasku on myöhässä, kirjauspäivämäärä määritetään käsittelypäivämääräksi ja rivin fontti muuttuu punaiseksi.  

## <a name="see-also"></a>Katso myös
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Maksujen suorittaminen](payables-make-payments.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

