---
title: Raportin ulkoasun muuttaminen erilaisilla asetteluvalinnoilla | Microsoft Docs
description: "Voit käyttää raportissa erilaisia asetteluja ja muuttaa raportin ulkoa asua asetteluja vaihtelemalla."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 677b7319baff476671c4c8ade4afed843f936c36
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-change-which-layout-is-currently-used-on-a-report"></a>Miten voit: muuta tällä hetkellä raportissa käytettävää asettelua
Raportti voidaan määrittää useille raportin asetteluille, joita voidaan vaihtaa tarpeen mukaan.

Raporttiin käytettävissä olevien asettelujen mukaan voit valita valmiin RDLC-raporttiasettelun, sisäänrakennetun Word-raportin asettelun tai mukautetun asettelun käytön välillä. Lisätietoja RDLC- ja Word-raporttiasettelusta sekä valmiista ja mukautetuista asetteluista ja muista ominaisuuksista on kohdassa [Raporttiasetteluiden hallinta](ui-manage-report-layouts.md).

## <a name="to-change-the-layout-that-is-used-on-a-report"></a>Raportissa käytetyn asettelun muuttaminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Raporttiasetteluvalinta** ja valitse sitten aiheeseen liittyvä linkki.  
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

