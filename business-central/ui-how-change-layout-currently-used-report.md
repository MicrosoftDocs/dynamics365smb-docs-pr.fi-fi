---
title: Raportin ulkoasun muuttaminen erilaisilla asetteluvalinnoilla | Microsoft Docs
description: Voit käyttää raportissa erilaisia asetteluja ja muuttaa raportin ulkoa asua asetteluja vaihtelemalla.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 74d161636d9110fcc366733245951e3044662e80
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193810"
---
# <a name="change-the-current-report-layout"></a>Nykyisen raportin asettelun muuttaminen
Raportti voidaan määrittää useille raportin asetteluille, joita voidaan vaihtaa tarpeen mukaan.

Raporttiin käytettävissä olevien asettelujen mukaan voit valita valmiin RDLC-raporttiasettelun, sisäänrakennetun Word-raportin asettelun tai mukautetun asettelun käytön välillä. Lisätietoja RDLC- ja Word-raporttiasettelusta sekä valmiista ja mukautetuista asetteluista ja muista ominaisuuksista on ohjeaiheessa [Raporttiasetteluiden hallinta](ui-manage-report-layouts.md).

Kun mukautettuja raportin asetteluita määritetään, voit valita ne asiakas- ja toimittajakorteista ja määrittää, että valittuja asetteluita käytetään asiakirjoissa, jotka ovat kyseessä olevalle asiakkaalle tai toimittajalle. Lisätietoja on kohdassa [Asiakkaiden ja toimittajien asiakirja-asettelujen määrittäminen ](ui-define-customer-vendor-document-layouts.md).

> [!TIP]  
> Word-raportin asettelua käyttävät asiakirjaraportit (eivät luettelot) ovat yleensä nopeampia kuin RDLC-raporttiasettelua käyttävät raportit. Jos sinulla on mahdollisuus valita asiakirjaraportin asetteluksi joko Word- tai RDLC-raportin asettelua, Word-raporttiasettelu on paras vaihtoehto.

## <a name="to-change-which-report-layout-to-use-for-a-report-or-document"></a>Raporttia tai asiakirjaa varten käytettävän raporttiasettelun muuttaminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Raporttiasetteluvalinta** ja valitse sitten liittyvä linkki.  
   **Raporttiasetteluvalinta**-sivulla on luettelo kaikista raporteista, joita voi käyttää sivun yläosan **Yritys**-kentässä määritetyssä yrityksessä. **Valittu asettelu** -kenttä määrittää tällä hetkellä raportissa käytetyn asettelun.
2. Määritä **Yritys**-kenttä sivun yläosassa yritykseksi, joka sisältää raportin.
3. Voit muuttaa raportin käyttämää asettelua valitsemalla raportin rivin ja asettamalla **Valittu asettelu** -kentän arvoksi yhden seuraavista vaihtoehdoista:
   * **RDLC (valmis)**, käyttää raportissa valmista RDLC-raporttiasettelua.
   * **Word (valmis)**, käyttää raportissa valmista Word-raporttiasettelua.
   * **Mukautettu**, käyttää raportissa mukautettua asettelua.  

> [!NOTE]
> Jos valitset raporttiasettelutyypin **RDLC (sisäinen)** tai **Word (sisäinen)** ja näyttöön tulee virhesanoma siitä, että raportin asettelu ei määritetyn tyyppinen, sinun on valittava toinen asetteluvaihtoehto tai luotava mukautettu raportin asettelu, joka on haluamasi tyyppinen. Tutustu seuraaviin toimiin.

Lisätoimia ei vaadita, jos valitsit valmiin RDLC- tai Word-raporttiasettelun ja asettelua käytetään, kun raportti suoritetaan seuraavan kerran.

## <a name="to-change-the-custom-layout-to-use-for-a-report-layout"></a>Raporttiasettelussa käytettävän mukautetun asettelun muuttaminen
Haluat ehkä myös muuttaa käytössä olevaa mukautettua asettelua. Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

Kaikki yrityksen raportin asetteluissa olevat mukautetut raporttiasettelut näkyvät **Mukautetut raporttiasettelut** -sivulla. **Raporttiasettelun valinta** -sivulla voit nähdä, mitkä mukautetut asettelut ovat käytettävissä **Mukautetut asettelut** -tietoruudussa.

1. Valitse **Raporttiasettelun valinta** -sivun muokattavan raporttiasettelun riviltä valintapainike **Mukautetun asettelun kuvaus** -kentässä.
2. Valitse **Mukautetut raporttiasettelut** -sivulla rivi mukautetulle asettelulle, jota haluat käyttää. Valitse sitten **OK**-painike.

Valitsemasi mukautetun asettelun nimi näkyy nyt **Mukautetun asettelun kuvaus** -kentässä, ja sitä käytetään, kun raporttia tai asiakirjaa esikatsellaan, tulostetaan tai lähetetään seuraavan kerran.

Voit nyt siirtyä asiakas- ja toimittajakortteihin ja määrittää, mitä asetteluita käytetään eri asiakirjoissa, joita lähetät kyseessä olevalle asiakkaalle tai toimittajalle – esimerkiksi tilausvahvistuksissa tai maksumuistutuksissa. Lisätietoja on kohdassa [Asiakkaiden ja toimittajien asiakirja-asettelujen määrittäminen ](ui-define-customer-vendor-document-layouts.md).

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös
[Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
