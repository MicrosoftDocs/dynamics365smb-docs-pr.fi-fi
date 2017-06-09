---
title: 'Toimintaohje: Raportin tai asiakirjan mukautetun asettelun luominen | Microsoft Docs'
description: "Lisätietoja raportin ulkoasun suunnittelusta."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 79c1e5c1ea01077e2e5012ba07618760ccf2a4af
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-create-a-custom-report-or-document-layout"></a>Toimintaohje: Raportin tai asiakirjan mukautetun asettelun luominen
Oletusarvon mukaan raportilla on valmis raporttiasettelu, joka voi olla RDLC-raporttiasettelu, Word-raporttiasettelu tai molemmat. Et voi muuttaa valmiita asetteluita. Voit kuitenkin luoda omia mukautettuja asetteluita, joiden avulla voit muuttaa raportin ulkoasua, kun sitä tarkastellaan, tulostetaan tai tallennetaan. Voit luoda useita mukautettuja raporttiasetteluja samalle raportille ja vaihtaa sitten raportin käyttämää asettelua tarpeen mukaan.

**Huomautus**: Raportti tarkoittaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa myös ulkoisille käyttäjille tarkoitettuja asiakirjoja, kuten myyntilaskuja tai tilausvahvistuksia, jotka lähetetään asiakkaille PDF-tiedostoina.

Jos haluat luoda mukautetun asettelun, voit joko kopioida aiemmin mukautetun asettelun tai lisätä uuden mukautetun asettelun, joka useimmissa tapauksissa perustuu valmiiseen asetteluun. Kun lisäät uuden mukautetun asettelun, voit lisätä RDLC-raporttiasettelutyypin, Word-raporttiasettelutyypin tai molemmat. Uusi mukautettu asettelu perustuu automaattisesti raportin valmiiseen asetteluun, jos sellainen on käytettävissä. Jos tyypille ei ole sisäänrakennettua asettelua, järjestelmä luo uuden tyhjän asettelun ja sinun on muokattava ja luotava alusta alkaen. Lisätietoja RDLC- ja Word-raporttiasettelusta sekä valmiista ja mukautetuista asetteluista ja muista ominaisuuksista on kohdassa [Raporttiasetteluiden hallinta](ui-manage-report-layouts.md).  

## <a name="to-create-a-custom-layout"></a>Mukautetun asettelun luonti
1. Valitse oikeassa yläkulmassa oleva **Etsi sivua tai raporttia** -kuvake![Etsi sivua tai raporttia](media/ui-search/search_small.png "Search for Page or Report icon"), kirjoita **Raporttiasetteluvalinta** ja valitse sitten aiheeseen liittyvä linkki.  
   **Raporttiasetteluvalinta**-ikkunassa näkyvät kaikki yrityksen käytettävissä olevat raportit. Kyseinen yritys määritetty Yritys-kentässä ikkunan yläosassa.
2. Aseta **Yritys**-kenttä yritykselle jolle haluat luoda raporttiasettelun.
3. Valitse rivi raportille, jolle haluat luoda asettelun, ja valitse sitten **Mukautetut asettelut**.  
   **Mukautetut raporttiasettelut** -ikkunassa näkyvät kaikki mukautetut asettelut, jotka ovat käytettävissä valitussa raportissa.
4. Jos haluat luoda kopion aiemmin luodusta mukautetusta asettelusta, valitse luettelosta aiemmin luotu mukautettu asettelu ja valitse sitten **Kopioi**.  
   Mukautetun asettelun kopio näkyy **Mukautetut raporttiasettelut** -ikkunassa, jonka Kuvaus-kentässä on sana Kopio.
5. Jos haluat lisätä uuden mukautetun asettelun, joka perustuu valmiiseen asetteluun, toimi seuraavasti:  
   1. Valitse **Uusi**. **Lisää raportin valmis asettelu** -ikkuna avautuu. **Tunnus**- ja **Nimi**-kentät täytetään automaattisesti.
   2. Voit lisätä mukautetun Word-raporttiasettelun tyypin valitsemalla **Lisää Word-asettelu** -valintaruutu.
   3. Voit lisätä mukautetun RDLC-raporttiasettelun tyypin valitsemalla **Lisää RDLC-asettelu** -valintaruutu.
   4. Valitse **OK**-painike.  
      Uudet mukautetut asettelut näkyvät **Mukautetut raporttiasettelut** -ikkunassa. Jos uusi asettelu perustuu valmiiseen asetteluun, sitten siinä on sanat **valmiin asettelun kopio** **Kuvaus**-kentässä. Jos valmista asettelua ei ole saatavilla, uudessa asettelussa on sanat **uusi asettelu** **Kuvaus**-kentässä. Tämä osoittaa, että mukautettu asettelu on tyhjä.
6. Oletusarvon mukaan **Yrityksen nimi** -kenttä on tyhjä, joten mukautettu asettelu ovat käytettävissä kaikissa yrityksen raporteissa. Voit asettaa mukautetun asettelun vain tietyn yrityksen käytettäväksi valitsemalla **Muokkaa** ja määrittämällä sitten **Yrityksen nimi** -kenttään haluamasi yritys.

## <a name="see-also"></a>Katso myös
[Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
[Toimintaohje: Raportissa tällä hetkellä käytettävän asettelun muuttaminen](ui-how-change-layout-currently-used-report.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

