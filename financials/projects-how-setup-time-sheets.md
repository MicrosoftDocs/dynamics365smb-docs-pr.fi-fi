---
title: "Toimintaohje: Aikaraporttien määrittäminen| Microsoft Docs"
description: "Artikkelissa kerrotaan, miten järjestelmä valmistellaan käyttämään aikaraportteja projektien hallitsemiseen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: aa93e7fe867893c52e3b3973a58ea8a43291c1b1
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-time-sheets"></a>Aikaraporttien määrittäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)]in aikaraportit käsittelevät aikarekisteröintiä viikoittain seitsemän päivän välein. Voit käyttää niitä projekteissa käytettävän ajan seuraamiseen ja yksinkertaisen resurssin aikarekisteröinnin kirjaamiseen. Ennen kuin voit käyttää aikaraportteja, on määritettävä tavat niiden määrittämiseen ja asetuksiin.

Kun olet määrittänyt, miten organisaatiossa käytetään aikaraportteja, voit määrittää aikaraporttien hyväksymistä koskevat ehdot. Organisaation tarpeista riippuen voit määrittää seuraavat vaihtoehdot:

* Vähintään yhden käyttäjän aikaraportin järjestelmänvalvojaksi ja hyväksyjäksi kaikkia aikaraportteja varten.
* Kunkin resurssin aikaraportin hyväksyjän.

Kun olet määrittänyt aikaraportit, voit luoda resursseille aikaraportit, määrittää ne projektin suunnitteluriveille ja kirjata aikaraporttirivit. Lisätietoja on kohdassa [Toimintaohje: Aikaraporttien käyttäminen](projects-how-use-time-sheets.md).

## <a name="to-set-up-general-information-for-time-sheets"></a>Aikaraporttien yleistietojen määrittäminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Resurssienhallinnan asetukset** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Aikaraportin projektihyväksyntä** -kenttään jokin seuraavista valinnoista.

| Asetus | Kuvaus |
| --- | --- |
| **Ei koskaan** |Resurssikortin **Aikaraportin hyväksyjän käyttäjätunnus** -kenttä hyväksyy aikaraportin. |
| **Aina** |Projektikortin **Vastuuhenkilö**-kenttä hyväksyy aikaraportin. |
| **Vain kone** |Jos koneen aikaraportti on linkitetty projektiin, projektikortin **Vastuuhenkilö**-kentässä mainittu käyttäjä hyväksyy aikaraportin. Jos koneen aikaraportti on linkitetty resurssiin, resurssikortin **Aikaraportin hyväksyjän käyttäjätunnus** -kentässä mainittu käyttäjä hyväksyy aikaraportin. |

## <a name="to-assign-a-time-sheet-administrator"></a>Aikaraportin järjestelmänvalvojan määrittäminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Käyttäjäasetukset** ja valitse sitten liittyvä linkki.  
2. Lisää uusi käyttäjä, jos käyttäjäluettelo ei sisällä henkilöä, jonka haluat olevan aikaraportin järjestelmänvalvoja. Lisätietoja on kohdan [Valmistautuminen liiketoimintaan](ui-get-ready-business.md) Käyttäjien luominen -osassa.  
3. Valitse käyttäjä, josta tulee aikaraportin järjestelmänvalvoja, ja valitse sitten **Aikaraportin valvoja** -valintaruutu.  

**Vihje**: Yrityksen aikaraportin järjestelmänvalvojaksi kannattaa nimetä vain yksi käyttäjä. Seuraavassa toimenpiteessä määritetään aikaraportin omistaja ja hyväksyjä. Aikaraportin hyväksyjä määritetään jokaiselle resurssille.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>Aikaraportin omistajan ja hyväksyjän määrittäminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Resurssit** ja valitse sitten liittyvä linkki.
2. Valitse resurssi, jolle haluat määrittää aikaraporttien käyttömahdollisuuden. Valitse sitten **Käytä aikaraporttia** -valintaruutu.  
3. Syötä aikaraportin omistajan tunnus **Aikaraportin omistajan käyttäjätunnus** -kenttään. Omistaja voi syöttää ajankäytön aikaraporttiin ja lähettää sen hyväksyttäväksi. Jos resurssi on henkilö, tämä henkilö on yleensä myös omistaja.  
4. Syötä aikaraportin hyväksyjän tunnus **Aikaraportin hyväksyjän käyttäjätunnus** -kenttään. Hyväksyjä voi hyväksyä, hylätä tai uudelleenavata aikaraportin.  

**Huomautus**: Aikaraportin hyväksyjän tunnusta ei voi muuttaa, jos on aikaraportteja, joita ei ole vielä käsitelty ja joiden tila on **Lähetetty** tai **Avoin**.

## <a name="see-also"></a>Katso myös
[Projektinhallinnan määrittäminen](projects-setup-projects.md)  
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  

