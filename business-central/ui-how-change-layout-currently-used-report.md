---
title: Raportin ulkoasun muuttaminen erilaisilla asetteluvalinnoilla | Microsoft Docs
description: "Voit käyttää raportissa erilaisia asetteluja ja muuttaa raportin ulkoa asua asetteluja vaihtelemalla."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 98a2e773dbde6ba4ba0493e2b0dc7b632bbea4d0
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="change-which-layout-is-currently-used-on-a-report"></a>Raportissa tällä hetkellä käytettävän asettelun muuttaminen
Raportti voidaan määrittää useille raportin asetteluille, joita voidaan vaihtaa tarpeen mukaan.

Raporttiin käytettävissä olevien asettelujen mukaan voit valita valmiin RDLC-raporttiasettelun, sisäänrakennetun Word-raportin asettelun tai mukautetun asettelun käytön välillä. Lisätietoja RDLC- ja Word-raporttiasettelusta sekä valmiista ja mukautetuista asetteluista ja muista ominaisuuksista on ohjeaiheessa [Raporttiasetteluiden hallinta](ui-manage-report-layouts.md).

## <a name="to-change-the-layout-that-is-used-on-a-report"></a>Raportissa käytetyn asettelun muuttaminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttiasetteluvalinta** ja valitse sitten liittyvä linkki.  
   **Raporttiasetteluvalinta**-ikkunassa näkyvät kaikki raportit, jotka ovat käytettävissä yritykselle, joka on määritetty Yritys-kentässä ikkunan yläosassa. Valittu asettelu -kenttä määrittää tällä hetkellä raportissa käytetyn asettelun.
2. Aseta **Yritys**-kenttä ikkunan yläosassa yritykseksi, joka sisältää raportin.
3. Voit muuttaa raportin käyttämää asettelua valitsemalla raportin rivin luettelosta ja asettamalla **Valittu asettelu** -kentän arvoksi yhden seuraavista vaihtoehdoista:
   * RDLC (valmis), käyttää raportissa valmista RDLC-raporttiasettelua.
   * Word (valmis), käyttää raportissa valmista Word-raporttiasettelua.
   * Mukautettu, käyttää raportissa mukautettua asettelua.  
     Raportissa käytettävissä olevat mukautetut asettelut näkyvät Raporttiasettelujen osat -tietoruudussa. Jos raportille ei ole mukautettuja asetteluja, sinun on ensin luotava yksi. Jos valitset tämän vaihtoehdon, siirry seuraavaan toimenpiteeseen ja määritä mukautettu asettelu, jota haluat käyttää.

    > [!NOTE]  
    >   Jos valitset **RDLC (sisäinen)** tai **Word (sisäinen)** ja näyttöön tulee virhesanoma siitä, että raportin asettelu ei määritetyn tyyppinen, sinun on valittava toinen asetteluvaihtoehto tai luotava mukautettu raportin asettelu, joka on haluamasi tyyppinen.

Lisätoimia ei vaadita, jos valitsit valmiin RDLC- tai Word-raporttiasettelun ja asettelua käytetään, kun raportti suoritetaan seuraavan kerran.

## <a name="to-specify-a-custom-layout-on-a-report"></a>Mukautetun asettelun määrittäminen raportille
1. Voit määrittää **Mukautetut raporttiasettelut** -ikkunassa raportille käytettävän mukautetun asettelun. Jos **Mukautetut raporttiasettelut** -ikkuna ei ole avoinna, valitse hakupainike **Raporttiasettelun kuvaus** -kentässä.
2. Valitse **Mukautetut raporttiasettelut** -ikkunassa rivi mukautetulle asettelulle, jota haluat käyttää, ja sulje ikkuna.

Palaa **Raporttiasetteluvalinta**-ikkunaan. Valitun mukautetun asettelun nimi näkyy **Mukautetun asettelun kuvaus** -kentässä. Mukautettua asettelua käytetään seuraavan kerran, kun suoritat raportin.

## <a name="see-also"></a>Katso myös
[Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

