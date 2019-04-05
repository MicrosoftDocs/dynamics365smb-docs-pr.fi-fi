---
title: Raporttien ja asiakirjojen mukautettujen asettelujen luominen ja muokkaaminen | Microsoft Docs
description: Voit tutustua omien mukautettujen asettelujen luomiseen ja raportin ulkoasun muokkaamiseen, kun sitä tarkastellaan, tulostetaan tai tallennetaan.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: 2f86eb50422b5d780ea7a0be2f6798c0b2cc3bfd
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/19/2019
ms.locfileid: "852330"
---
# <a name="create-and-modify-a-custom-report-or-document-layout"></a>Raporttien tai asiakirjojen mukautetun asettelun luominen ja muokkaaminen
Oletusarvon mukaan raportilla on valmis raporttiasettelu, joka voi olla RDLC-raporttiasettelu, Word-raporttiasettelu tai molemmat. Et voi muuttaa valmiita asetteluita. Voit kuitenkin luoda omia mukautettuja asetteluita, joiden avulla voit muuttaa raportin ulkoasua, kun sitä tarkastellaan, tulostetaan tai tallennetaan. Voit luoda useita mukautettuja raporttiasetteluja samalle raportille ja vaihtaa sitten raportin käyttämää asettelua tarpeen mukaan.

> [!NOTE]  
>   Raportti tarkoittaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa myös ulkoisille käyttäjille tarkoitettuja asiakirjoja, kuten myyntilaskuja tai tilausvahvistuksia, jotka lähetetään asiakkaille PDF-tiedostoina.

Jos haluat luoda mukautetun asettelun, voit joko kopioida aiemmin mukautetun asettelun tai lisätä uuden mukautetun asettelun, joka useimmissa tapauksissa perustuu valmiiseen asetteluun. Kun lisäät uuden mukautetun asettelun, voit lisätä RDLC-raporttiasettelutyypin, Word-raporttiasettelutyypin tai molemmat. Uusi mukautettu asettelu perustuu automaattisesti raportin valmiiseen asetteluun, jos sellainen on käytettävissä. Jos tyypille ei ole sisäänrakennettua asettelua, järjestelmä luo uuden tyhjän asettelun ja sinun on muokattava ja luotava alusta alkaen. Lisätietoja RDLC- ja Word-raporttiasettelusta sekä valmiista ja mukautetuista asetteluista ja muista ominaisuuksista on ohjeaiheessa [Raporttiasetteluiden hallinta](ui-manage-report-layouts.md).  

## <a name="to-create-a-custom-layout"></a>Mukautetun asettelun luonti
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Raporttiasetteluvalinta** ja valitse sitten liittyvä linkki.

    **Raporttiasetteluvalinta**-sivulla on luettelo kaikista raporteista, joita voi käyttää sivun yläosan **Yritys**-kentässä määritetyssä yrityksessä.
2. Aseta **Yritys**-kenttä yritykselle jolle haluat luoda raporttiasettelun.
3. Valitse sen raportin rivi, johon haluat luoda asettelun, ja valitse sitten **Mukautetut asettelut** -toiminto.  
   **Mukautetut raporttiasettelut** -sivulla näkyvät kaikki mukautetut asettelut, jotka ovat käytettävissä valitussa raportissa.
4. Jos haluat luoda kopion aiemmin luodusta mukautetusta asettelusta, valitse luettelossa ensin aiemmin luotu mukautettu asettelu ja valitse **Kopioi** -toiminto.  
   Mukautetun asettelun kopio näkyy **Mukautetut raporttiasettelut** -sivulla, jonka **Kuvaus**-kentässä on sana *Kopio*.
5. Jos haluat lisätä uuden mukautetun asettelun, joka perustuu valmiiseen asetteluun, toimi seuraavasti:  
   1. Valitse **Uusi**-toiminto. **Lisää raportin valmis asettelu** -sivu avautuu. **Tunnus**- ja **Nimi**-kentät täytetään automaattisesti.
   2. Voit lisätä mukautetun Word-raporttiasettelun tyypin valitsemalla **Lisää Word-asettelu** -valintaruutu.
   3. Voit lisätä mukautetun RDLC-raporttiasettelun tyypin valitsemalla **Lisää RDLC-asettelu** -valintaruutu.
   4. Valitse **OK**-painike.  
      Uudet mukautetut asettelut näkyvät **Mukautetut raporttiasettelut** -sivulla. Jos uusi asettelu perustuu valmiiseen asetteluun, sitten siinä on sanat **valmiin asettelun kopio** **Kuvaus**-kentässä. Jos valmista asettelua ei ole saatavilla, uudessa asettelussa on sanat **uusi asettelu** **Kuvaus**-kentässä. Tämä osoittaa, että mukautettu asettelu on tyhjä.
6. Oletusarvon mukaan **Yrityksen nimi** -kenttä on tyhjä, joten mukautettu asettelu ovat käytettävissä kaikissa yrityksen raporteissa. Voit asettaa mukautetun asettelun vain tietyn yrityksen käytettäväksi valitsemalla **Muokkaa** ja määrittämällä sitten **Yrityksen nimi** -kenttään haluamasi yritys.

Mukautettu asettelu on luotu. Voit nyt muokata mukautettua asettelua tarpeen mukaan.

## <a name="ModifyCustomLayout"></a>Mukautetun asettelun muokkaaminen
Voit muokata raporttiasettelua viemällä raporttiasettelun ensin tiedostona tietokone- tai verkkosijaintiin ja avaamalla sitten viedyn asiakirjan Wordissa ja tekemällä muutokset. Kun olet tehnyt haluamasi muutokset, voit tuoda raporttiasettelun.

### <a name="to-modify-a-custom-layout"></a>Mukautetun asettelun muokkaaminen
1.  Voit viedä mukautetun asettelun **Mukautetut raporttiasettelut** -sivulla. Jos sivu ei ole vielä avoinna, etsi ja avaa **Raporttiasetteluvalinta**-sivu, valitse raportti, jossa muokattava asettelu on, ja valitse sitten **Mukautetut asettelut** -toiminto.  
2.  Valitse **Mukautetut raporttiasettelut** -sivulla ensin muokattava raportti ja sitten **Vie asettelu** -toiminto. Tallenna raporttiasetteluasiakirja sitten tietokone- tai verkkosijaintiin valitsemalla **Tallenna** tai **Tallenna nimellä**.  

3.  Avaa juuri tallentamasi raporttiasettelu ja tee muutokset.

      Jos muutat Word-asettelua, avaa asetteluasiakirja Wordissa. Lisätietoja on seuraavassa kohdassa [Muutosten tekeminen raporttiasetteluun](ui-how-create-custom-report-layout.md#MakeChangesToLayout).

      RDLC-raporttiasettelut ovat kehittyneempiä kuin Word-raporttiasettelut. Lisätietoja RDLC-raporttiasettelujen muokkaamisesta on kohdassa [RDLC-raporttiasettelujen suunnitteleminen](/dynamics-nav/Designing-RDLC-Report-Layouts).

      Muista tallentaa muutokset, kun olet valmis.

4.  Palaa **Mukautetut raporttiasettelut** -sivulle, valitse viety ja muokattu raporttiasettelu ja valitse lopuksi **Tuo asettelu** -toiminto.  

5. Etsi ja valitse raporttiasetteluasiakirja valitsemalla **Tuo**-valintaruudussa ensin **Valitse** ja sitten **Avaa**.

##  <a name="MakeChangesToLayout"></a> Muutosten tekeminen Word-raporttiasetteluun  
Voit tehdä yleisiä muotoilu- ja asettelumuutoksia, kuten vaihtaa tekstin fontin sekä lisätä taulukon ja muokata sitä tai poista tietokentän, käyttämällä samoja Wordin perustoimintoja kuin muissakin Word-asiakirjoissa.

Jos olet suunnittelemassa Wordin raporttiasettelua alusta tai lisäämässä uusia tietokenttiä, aloita lisäämällä taulukko, jossa on rivejä ja sarakkeita, jotka ovat lopulta tietokenttiä.

> [!TIP]  
>  Näytä taulukon ruudukko siten, että näet taulukon solujen rajat. Muista piilottaa ruudukko, kun lopetat muokkauksen. Voit näyttää tai piilottaa ruudukot valitsemalla taulukon ja valitsemalla **Asettelu**-kohdan alta **Taulukko**-välilehdellä **Näytä ruudukko**.

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Fonttien upottaminen Word-asetteluihin yhdenmukaisuuden vuoksi

Upottamalla fontit Word-asiakirjaan voit varmistaa, että raportit näkyvät ja tulostuvat aiotuilla fonteilla riippumatta siitä, missä käyttäjä avaa tai tulostaa raportit. Huomaa kuitenkin, että fonttien upottaminen voi suurentaa merkittävästi Word-tiedostojen kokoa. Lisätietoja fonttien upottamisesta Wordiin on kohdassa [Fonttien upottaminen Wordissa, PowerPointissa tai Excelissä](https://support.office.com/en-us/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Otsikko- ja tietokenttien poistaminen Word-asetteluissa  
 Raportin otsikko- ja tietokentät sisältyvät Wordin sisällön ohjausobjekteihin. Seuraavassa kuvassa on esitetty sisällön ohjausobjekti, kun se on valittuna Word-asiakirjassa.  

 ![Kentän sisällönhallinta Word-raporttiasettelussa](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 Selitteen tai tietokentän nimi näkyy sisällön ohjausobjektissa. Esimerkissä kentän nimi on CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>Selitteen tai tietokentän poistaminen  

1.  Napsauta poistettavaa kenttää hiiren kakkospainikkeella ja valitse **Poista sisällön hallinta**.  

     Sisällön ohjausobjekti poistetaan, mutta kentän nimi säilyy tekstinä.  

2.  Poistaa jäljellä olevan tekstin tarpeen mukaan.  

### <a name="adding-data-fields"></a>Tietokenttien lisääminen
Tietokenttien lisääminen raportin tietojoukosta on kuitenkin lisäasetus ja edellyttää tietoja raportin tietojoukosta. Lisätietoja tieto-, otsikko- ja kuvakenttien lisäämisestä on kohdassa [Kenttien lisääminen Word-raporttiasetteluun](ui-how-add-fields-word-report-layout.md).  

###


## <a name="see-also"></a>Katso myös
[Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
[Raportissa tällä hetkellä käytettävän asettelun muuttaminen](ui-how-change-layout-currently-used-report.md)  
[Raporttien tai asiakirjojen mukautetun asettelun tuonti ja vienti](ui-how-import-and-export-report-layout.md)  
[Raporttien ja eräajojen käsitteleminen](ui-work-report.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
