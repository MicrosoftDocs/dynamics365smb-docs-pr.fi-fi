---
title: Aikaraporttien ja niiden hyväksymisen määrittäminen| Microsoft Docs
description: Aikaraportit määritetään seuraamaan projekteihin käytettyä aikaa ja resurssien käyttöä, mikä auttaa projektinhallinnan, henkilöstön ja kapasiteetin suhteen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource, time sheet
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 778d9c4308d28be804d7f1572335bd160faad6d8
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184297"
---
# <a name="set-up-time-sheets"></a>Aikaraporttien määrittäminen
[!INCLUDE[prod_short](includes/prod_short.md)]in aikaraportit käsittelevät aikarekisteröintiä viikoittain seitsemän päivän välein. Voit käyttää niitä projekteissa käytettävän ajan seuraamiseen ja yksinkertaisen resurssin aikarekisteröinnin kirjaamiseen. Ennen kuin voit käyttää aikaraportteja, on määritettävä tavat niiden määrittämiseen ja asetuksiin.

Kun olet määrittänyt, miten organisaatiossa käytetään aikaraportteja, voit määrittää aikaraporttien hyväksymistä koskevat ehdot. Organisaation tarpeista riippuen voit määrittää seuraavat vaihtoehdot:

* Vähintään yhden käyttäjän aikaraportin järjestelmänvalvojaksi ja hyväksyjäksi kaikkia aikaraportteja varten.
* Kunkin resurssin aikaraportin hyväksyjän.

Kun olet määrittänyt aikaraportit, voit luoda resursseille aikaraportit, määrittää ne projektin suunnitteluriveille ja kirjata aikaraporttirivit. Lisätietoja on kohdassa [Aikaraporttien käyttäminen](projects-how-use-time-sheets.md).

## <a name="to-set-up-general-information-for-time-sheets"></a>Aikaraporttien yleistietojen määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssiasetukset** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Aikaraportin projektihyväksyntä** -kenttään jokin seuraavista valinnoista.

| Asetus | Kuvaus |
| --- | --- |
| **Ei koskaan** |Resurssikortin **Aikaraportin hyväksyjän käyttäjätunnus** -kenttä hyväksyy aikaraportin. |
| **Aina** |Projektikortin **Vastuuhenkilö**-kenttä hyväksyy aikaraportin. |
| **Vain kone** |Jos koneen aikaraportti on linkitetty projektiin, projektikortin **Vastuuhenkilö**-kentässä mainittu käyttäjä hyväksyy aikaraportin. Jos koneen aikaraportti on linkitetty resurssiin, resurssikortin **Aikaraportin hyväksyjän käyttäjätunnus** -kentässä mainittu käyttäjä hyväksyy aikaraportin. |

## <a name="to-assign-a-time-sheet-administrator"></a>Aikaraportin järjestelmänvalvojan määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjäasetukset** ja valitse sitten liittyvä linkki.  
2. Lisää uusi käyttäjä, jos käyttäjäluettelo ei sisällä henkilöä, jonka haluat olevan aikaraportin järjestelmänvalvoja. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).
3. Valitse ensin käyttäjä, josta tulee aikaraportin järjestelmänvalvoja, ja valitse sitten **Tuntiraportin valvoja** -valintaruutu.  

> [!TIP]  
>   Yrityksen aikaraportin järjestelmänvalvojaksi kannattaa nimetä vain yksi käyttäjä. Seuraavassa toimenpiteessä määritetään aikaraportin omistaja ja hyväksyjä. Aikaraportin hyväksyjä määritetään jokaiselle resurssille.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>Aikaraportin omistajan ja hyväksyjän määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssit** ja valitse sitten liittyvä linkki.
2. Valitse resurssi, jolle haluat määrittää aikaraporttien käyttömahdollisuuden. Valitse sitten **Käytä aikaraporttia** -valintaruutu.  
3. Syötä aikaraportin omistajan tunnus **Aikaraportin omistajan käyttäjätunnus** -kenttään. Omistaja voi syöttää ajankäytön aikaraporttiin ja lähettää sen hyväksyttäväksi. Jos resurssi on henkilö, tämä henkilö on yleensä myös omistaja.  
4. Syötä aikaraportin hyväksyjän tunnus **Aikaraportin hyväksyjän käyttäjätunnus** -kenttään. Hyväksyjä voi hyväksyä, hylätä tai uudelleenavata aikaraportin.  

> [!NOTE]  
>   Aikaraportin hyväksyjän tunnusta ei voi muuttaa, jos on aikaraportteja, joita ei ole vielä käsitelty ja joiden tila on **Lähetetty** tai **Auki**.

## <a name="see-also"></a>Katso myös
[Projektinhallinnan määrittäminen](projects-setup-projects.md)  
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]