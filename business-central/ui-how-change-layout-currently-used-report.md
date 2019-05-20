---
title: Raportin ulkoasun muuttaminen erilaisilla asetteluvalinnoilla | Microsoft Docs
description: Voit käyttää raportissa erilaisia asetteluja ja muuttaa raportin ulkoa asua asetteluja vaihtelemalla.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: f24f1cd24a31ddbd0b455b876821ae0173a677c3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249431"
---
# <a name="change-which-layout-is-currently-used-on-a-report"></a>Raportissa tällä hetkellä käytettävän asettelun muuttaminen
Raportti voidaan määrittää useille raportin asetteluille, joita voidaan vaihtaa tarpeen mukaan.

Raporttiin käytettävissä olevien asettelujen mukaan voit valita valmiin RDLC-raporttiasettelun, sisäänrakennetun Word-raportin asettelun tai mukautetun asettelun käytön välillä. Lisätietoja RDLC- ja Word-raporttiasettelusta sekä valmiista ja mukautetuista asetteluista ja muista ominaisuuksista on ohjeaiheessa [Raporttiasetteluiden hallinta](ui-manage-report-layouts.md).

> [!TIP]  
> Word-raportin asettelua käyttävät asiakirjaraportit (eivät luettelot) ovat yleensä nopeampia kuin RDLC-raporttiasettelua käyttävät raportit. Jos sinulla on mahdollisuus valita asiakirjaraportin asetteluksi joko Word- tai RDLC-raportin asettelua, Word-raporttiasettelu on paras vaihtoehto.  

## <a name="to-change-the-layout-that-is-used-on-a-report"></a>Raportissa käytetyn asettelun muuttaminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttiasetteluvalinta** ja valitse sitten liittyvä linkki.  
   **Raporttiasetteluvalinta**-sivulla on luettelo kaikista raporteista, joita voi käyttää sivun yläosan Yritys-kentässä määritetyssä yrityksessä. Valittu asettelu -kenttä määrittää tällä hetkellä raportissa käytetyn asettelun.
2. Määritä **Yritys**-kenttä sivun yläosassa yritykseksi, joka sisältää raportin.
3. Voit muuttaa raportin käyttämää asettelua valitsemalla raportin rivin luettelosta ja asettamalla **Valittu asettelu** -kentän arvoksi yhden seuraavista vaihtoehdoista:
   * RDLC (valmis), käyttää raportissa valmista RDLC-raporttiasettelua.
   * Word (valmis), käyttää raportissa valmista Word-raporttiasettelua.
   * Mukautettu, käyttää raportissa mukautettua asettelua.  
     Raportissa käytettävissä olevat mukautetut asettelut näkyvät Raporttiasettelujen osat -tietoruudussa. Jos raportille ei ole mukautettuja asetteluja, sinun on ensin luotava yksi. Jos valitset tämän vaihtoehdon, siirry seuraavaan toimenpiteeseen ja määritä mukautettu asettelu, jota haluat käyttää.

    > [!NOTE]  
    >   Jos valitset **RDLC (sisäinen)** tai **Word (sisäinen)** ja näyttöön tulee virhesanoma siitä, että raportin asettelu ei määritetyn tyyppinen, sinun on valittava toinen asetteluvaihtoehto tai luotava mukautettu raportin asettelu, joka on haluamasi tyyppinen.

Lisätoimia ei vaadita, jos valitsit valmiin RDLC- tai Word-raporttiasettelun ja asettelua käytetään, kun raportti suoritetaan seuraavan kerran.

## <a name="to-specify-a-custom-layout-on-a-report"></a>Mukautetun asettelun määrittäminen raportille
1. Voit määrittää **Mukautetut raporttiasettelut** -sivulla raportille käytettävän mukautetun asettelun. Jos **Mukautetut raporttiasettelut** -sivu ei ole avoinna, valitse hakupainike **Raporttiasettelun kuvaus** -kentässä.
2. Valitse **Mukautetut raporttiasettelut** -sivulla rivi mukautetulle asettelulle, jota haluat käyttää, ja sulje sivu.

Palaa **Raporttiasetteluvalinta**-sivulle. Valitun mukautetun asettelun nimi näkyy **Mukautetun asettelun kuvaus** -kentässä. Mukautettua asettelua käytetään seuraavan kerran, kun suoritat raportin.

## <a name="see-also"></a>Katso myös
[Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
