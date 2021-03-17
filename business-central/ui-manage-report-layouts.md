---
title: Raporttien ja asiakirjojen mukautetut ja valmiit asettelut | Microsoft Docs
description: Voit mukauttaa asiakirjoja raporttiasettelujen avulla. Voit muokata tällä tavoin asiakkaille lähetettävien PDF-tiedostojen fonttia, logoa tai sivuasetuksia.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9f5bedb69782d77ea64a3779abd26143969925b3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390272"
---
# <a name="managing-report-and-document-layouts"></a>Raporttien ja asiakirjojen asettelujen hallinta
Raporttiasettelu ohjaa raportin sisältöä ja muotoa, mukaan lukien, mitkä tietojen kentät näkyvät raportissa ja miten ne järjestetään, tekstityylin, kuvia ja muita ominaisuuksia. Voit luoda [!INCLUDE[prod_short](includes/prod_short.md)]ista uuden asettelun, muuttaa raportissa käytettävää asettelua tai muokata nykyisiä asetteluja.

> [!NOTE]  
>   Raportti tarkoittaa [!INCLUDE[prod_short](includes/prod_short.md)]issa myös ulkoisille käyttäjille tarkoitettuja asiakirjoja, kuten myyntilaskuja tai tilausvahvistuksia, jotka lähetetään asiakkaille PDF-tiedostoina.

Erityisesti raporttiasettelu määrittää seuraavat asetukset:

* [!INCLUDE[prod_short](includes/prod_short.md)]-raportin tietojoukosta sisällytettävät tunnus- ja tietokentät.
* Tekstin muoto, kuten kirjasimen tyyppi, koko ja väri.
* Yrityksen logo ja sen sijainti.
* Yleiset sivun asetukset, esimerkiksi reunukset ja taustakuvia.

Raportti voidaan määrittää useille raportin asetteluille, joita voit vaihtaa tarpeen mukaan. Voit valita jonkin valmiin raporttiasettelun tai voit luoda mukautettuja raporttiasetteluja ja määrittää ne raportteihisi tarpeen mukaan. Lisätietoja on kohdassa [Raportin tai asiakirjan mukautetun asettelun luominen](ui-how-create-custom-report-layout.md).

Raporteissa käytettävän raporttiasettelun tyyppi voi olla Word tai RDLC.

## <a name="word-report-layout-overview"></a>Word-raporttiasettelun esittely
Word-raportin asettelu perustuu Word-asiakirjaan (.docx-tiedostotyyppi). Word-raporttiasetteluiden avulla voit suunnitella raporttiasetteluita käyttämällä Microsoft Word 2013 -versiota tai uudempaa. Word-raporttiasettelu määrittää raportin sisällön ja ohjaa sitä, miten sisältöelementit järjestetään ja miltä ne näyttävät. Raportin asettelu Word-asiakirjassa käyttää yleensä taulukoita, joiden avulla voit järjestää sisältöä, jossa solut sisältävät tietokentät, tekstiä tai kuvia.

 ![Esimerkki Word-raporttiasetteluasiakirjasta NAV:lle](media/nav_wordreportlayout_edit_in_word_example.png "NAV_WordReportLayout_Edit_In_Word_Example")  

## <a name="rdlc-layout-overview"></a>RDLC-asettelun yleiskuvaus
RDLC-asettelut perustuvat asiakkaan määrittelemiin raportinasetteluihin (.rdlc- tai .rdl-tiedostotyypit). Näitä asetteluja luodaan ja muokataan käyttämällä SQL Server Report Builderia. RDLC-asetteluiden rakenne muistuttaa Word-asetteluja, joissa asettelu määrittää raportin yleisen muodon ja määrää sisällytettävät tietojoukon kentät. RDLC-asetteluiden suunnitteleminen on monimutkaisempaa kuin Word-asetteluiden. Lisätietoja on kohdassa [RDLC-raporttiasetteluiden suunnitteleminen](/dynamics-nav/Designing-RDLC-Report-Layouts).

## <a name="built-in-and-custom-report-layouts"></a>Valmiit ja mukautetut raporttiasettelut
[!INCLUDE[prod_short](includes/prod_short.md)] sisältää useita valmiita asetteluita. Valmiit asettelut ovat etukäteen määritettyjä asetteluita, jotka on suunniteltu määrätyille raporteille. [!INCLUDE[prod_short](includes/prod_short.md)]in raporteissa on valmis asettelu joko RDLC-raporttiasetteluna, Wordin raporttiasetteluna tai joissakin tapauksissa molempina. Et voi muokata valmista raporttiasettelua [!INCLUDE[prod_short](includes/prod_short.md)]ista, mutta voit käyttää niitä lähtökohtana oman mukautetun raporttiasettelun luomisessa.

Mukautetut asettelut ovat raporttiasetteluita, jotka olet suunnitellut raportin ulkoasun muuttamiseksi. Luot tavallisesti mukautetun asettelun valmiin asettelun perusteella, mutta voit luoda niitä alusta alkaen tai kopioimalla aiemmin luodun mukautetun asettelun. Mukautetut asettelut mahdollistavat useat asettelut samalle raportille, joita voit vaihtaa tarpeen mukaan. Kullakin [!INCLUDE[prod_short](includes/prod_short.md)]-yritykselle voi olla esimerkiksi erilaisia asetteluja tai samalle yritykselle voi olla eri asetteluja tietyissä tapauksissa tai tapahtumissa, kuten erityiskampanjoissa tai lomakaudella.

## <a name="deciding-whether-to-use-a-word-or-rdlc-report-layout"></a>Wordin raporttiasettelun ja RDLC-raporttiasettelun välillä valitseminen
Raporttiasettelu voi perustua Word-asiakirjaan tai RDLC-tiedostoon. Word- tai RDLC-raporttiasettelun käytöstä päätettäessä asettelutyyppi riippuu siitä, miltä luodun raportin halutaan näyttävän ja tietämyksestäsi Wordista ja SQL Server Report Builderista.

Word- ja RDLC-asetteluiden yleiset rakenteet ovat hyvin samanlaisia. Silti, jokaisella tyypillä on tiettyjä suunnittelu ominaisuuksia, jotka vaikuttavat siihen miltä luodut raportit näyttävät [!INCLUDE[prod_short](includes/prod_short.md)]ssa. Tämä tarkoittaa sitä, että sama raportti saattaa näyttää erilaiselta RDLC-raporttiasetteluun verrattuna Word-raporttiasettelua käytettäessä.

Word- ja RDLC-raporttiasetteluiden asettaminen toimii samalla tavalla. Tärkein ero on asetteluiden muokkaustavassa. Word-raporttiasettelut ovat yleensä helpompia luoda ja muokata kuin RDLC-raporttiasettelut, koska voit käyttää Wordia. RDLC-raporttiasetteluja muokataan SQL Server Report Builderilla, joka on tarkoitettu kokeneille käyttäjille.

Lisätietoja näytettävän asettelun vaihtamisesta on kohdassa [Nykyisen raportin asettelun muuttaminen](ui-how-change-layout-currently-used-report.md)

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös
[Päivitä mukautetut raporttiasettelut](ui-update-report-layouts.md)  
[Raporttien mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)  
[Raporttien tai asiakirjojen mukautetun asettelun tuonti ja vienti](ui-how-import-and-export-report-layout.md)  
[Erikoisasiakirja-asettelujen määrittäminen asiakkaille ja toimittajille](ui-define-customer-vendor-document-layouts.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Raporttien, eräajojen ja XMLportien käsitteleminen](ui-work-report.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]