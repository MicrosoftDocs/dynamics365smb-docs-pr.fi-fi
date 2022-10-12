---
title: Raporttien ja asiakirjojen mukautettujen asettelujen luominen ja muokkaaminen
description: Voit tutustua mukautettujen asettelujen luomiseen ja raportin ulkoasun muokkaamiseen, kun sitä tarkastellaan, tulostetaan tai tallennetaan.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/06/2022
ms.author: edupont
ms.openlocfilehash: 465954e6549ee7ffd0822438a0ad004686d5b424
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2022
ms.locfileid: "9604775"
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a>(Vanha) Raporttien mukautettujen asettelujen luominen ja muokkaaminen

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Oletusarvoisesti raporteilla on valmis asettelu. Raporttiasettelu voi olla RDLC- tai Microsoft Word -raporttiasettelu tai molemmat. Vaikka et voi muokata sisäisiä asetteluita, mutta voit luoda mukautettuja asetteluita. Raportissa voi olla useita mukautettuja raporttiasetteluja.

> [!NOTE]  
> Raportti tarkoittaa [!INCLUDE[prod_short](includes/prod_short.md)]issa myös ulkoisille käyttäjille tarkoitettuja asiakirjoja, kuten myyntilaskuja tai tilausvahvistuksia, jotka lähetetään asiakkaille PDF-tiedostoina.

Voit luoda mukautetun asettelun joko kopioimalla aiemmin luodun mukautetun asettelun tai lisäämällä uuden mukautetun asettelun. Mukautetut asettelut perustuvat usein valmiisiin asetteluihin. Kun lisäät uuden mukautetun asettelun, voit lisätä RDLC- tai Word-raporttiasettelutyypin tai molemmat. Uusi mukautettu asettelu perustuu raportin valmiiseen asetteluun, jos sellainen on käytettävissä. Jos raporttityypille ei ole valmista asettelua, luodaan uusi tyhjä asettelu. Sinun täytyy muokata ja suunnitella tämä tyhjä asettelu alusta alkaen. Lisätietoja esimerkiksi RDLC- ja Word-raporttiasettelusta sekä valmiista ja mukautetuista asetteluista on kohdassa [Raporttiasetteluiden hallinta](ui-manage-report-layouts.md).  

> [!TIP]
> Talousraporttien avulla saat tietoja tilikarttaan sisältyvistä kirjanpitotiedoista. Lisätietoja on kohdassa [Talousraportoinnin valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md).

Kun olet määrittänyt mukautettuja raporttiasetteluja, voit valita ne asiakaskortti- ja toimittajakorttisivuilla. Asetteluita käytetään luotaessa asiakirjoja asiakkaalle tai toimittajalle. Lisätietoja on kohdassa [Asiakirja-asettelujen määrittäminen asiakkaille ja toimittajille](ui-define-customer-vendor-document-layouts.md).

Voit myös käyttää mukautettuja raporttiasetteluja lisätäksesi sisältöä sähköpostiviesteihin. Raporttiasettelut voivat säästää aikaa ja auttaa yhdenmukaisuuden varmistamisessa siten, että samaa sisältöä käytetään uudelleen, kun viestit asiakkaidesi kanssa. Jotta voit käyttää mukautettuja raporttiasetteluja sähköpostissa, niiden tiedostotyyppinä on oltava Word. RDLC-tiedostotyyppiä ei voi käyttää. Lisätietoja on kohdassa [Uudelleenkäytettävien sähköpostitekstien ja -asettelujen määrittäminen](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).

## <a name="create-a-custom-layout"></a>Mukautetun asettelun luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttiasetteluvalinta** ja valitse sitten vastaava linkki.

    **Raporttiasetteluvalinta**-sivulla on luettelo kaikista raporteista, joita voi käyttää sivun yläosan **Yrityksen nimi** -kentässä määritetyssä yrityksessä.
2. Valitse **Yrityksen nimi** -kentässä yritys, jolle haluat luoda raporttiasettelun.
3. Valitse sen raportin rivi, johon haluat luoda asettelun, ja valitse sitten **Mukautetut asettelut** -toiminto.  

   **Mukautetut raporttiasettelut** -sivulla näkyvät kaikki mukautetut asettelut, jotka ovat käytettävissä valitussa raportissa.
4. Jos haluat luoda kopion aiemmin luodusta mukautetusta asettelusta, valitse luettelossa ensin aiemmin luotu mukautettu asettelu ja valitse **Kopioi**-toiminto.  

   Mukautetun asettelun kopio näkyy **Mukautetut raporttiasettelut** -sivulla, jonka **Kuvaus**-kentässä on sana *Kopio*.
5. Jos haluat lisätä uuden mukautetun asettelun valmiin asettelun perusteella, noudata seuraavia vaiheita:  
   1. Valitse **Uusi**-toiminto. **Lisää raportin valmis asettelu** -sivun **Tunnus**- ja **Nimi**-kentät täytetään automaattisesti.
   2. Ota käyttöön **Lisää Word-asettelu** -vaihtopainike, jos haluat lisätä mukautetun Word-raporttiasettelun tyypin tai ottaa käyttöön **Lisää RDLC-asettelu** -vaihtopainikkeen RDLC-raporttiasettelun tyypin lisäämiseksi.
   4. Valitse **OK**-painike.  

    Uusi mukautettu asettelu näkyy nyt **Mukautetut raporttiasettelut** -sivulla. Jos uusi asettelu perustuu valmiiseen asetteluun, siinä on sanat **valmiin asettelun kopio** **Kuvaus**-kentässä. Jos valmista asettelua ei ole saatavilla, uudessa asettelussa on sanat **uusi asettelu** **Kuvaus**-kentässä. Tämä osoittaa, että mukautettu asettelu on tyhjä.
6. Oletusarvon mukaan **Yrityksen nimi** -kenttä on tyhjä ja mukautettu asettelu on käytettävissä kaikkien yritysten raporteissa. Voit asettaa mukautetun asettelun vain tietyn yrityksen käytettäväksi valitsemalla **Muokkaa** ja määrittämällä sitten **Yrityksen nimi** -kenttään haluamasi yritys.

Mukautettu asettelu on luotu, ja voit muokata sitä haluamallasi tavalla.

> [!TIP]
> Voit viedä raportin tulokset Microsoft Excel -tiedostoon koko tietojoukon tarkastelemista varten, kaikki sarakkeet mukaan lukien, mutta ilman asettelua. Excel-tiedoston avulla voit diagnosoida ongelmia tai tarkistaa, että raportti palauttaa odotetut tiedot. Lisätietoja on kohdassa [Raporttitietojen analysointi Excelillä](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Mukautetun asettelun muokkaaminen

Jos haluat muokata mukautetun raportin asettelua, sinun täytyy ensin viedä raportin asettelu tiedostona sijaintiin tietokoneessasi tai verkossa. Avaa sitten viety asia kirja ja tee muutokset. Kun olet tehnyt haluamasi muutokset, voit tuoda raporttiasettelun.

### <a name="modify-a-custom-layout"></a>Mukautetun asettelun muokkaaminen

1. Vie mukautettu asettelu **Mukautetut raporttiasettelut** -sivulla. Jos sivu ei ole vielä avoinna, etsi ja avaa **Raporttiasetteluvalinta**-sivu, valitse raportti, jossa muokattava asettelu on, ja valitse sitten **Mukautetut asettelut** -toiminto.  
2. Valitse **Mukautetut raporttiasettelut** -sivulla ensin muokattava raportti ja sitten **Vie asettelu** -toiminto. Tallenna raporttiasetteluasiakirja sitten tietokone- tai verkkosijaintiin valitsemalla **Tallenna** tai **Tallenna nimellä**.  
3. Avaa tallentamasi raporttiasetteluasiakirja ja tee muutokset.

   Jos muutat Word-asettelua, avaa asetteluasiakirja Wordissa. Lisätietoja Word-raporttien muokkaamisesta on kohdassa [Word-asetteluiden käsitteleminen](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   RDLC-raporttiasettelut ovat kehittyneempiä kuin Word-raporttiasettelut. Lisätietoja RDLC-raporttiasettelun muokkaamisesta on kohdassa [RDLC-raporttiasettelujen suunnitteleminen](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Muista tallentaa muutokset, kun olet valmis.

4. Palaa **Mukautetut raporttiasettelut** -sivulle, valitse viety ja muokattu raporttiasettelu ja valitse lopuksi **Tuo asettelu** -toiminto.  

5. Etsi ja valitse muokattu raporttiasetteluasiakirja valitsemalla **Tuo**-valintaruudussa ensin **Valitse** ja sitten **Avaa**.

> [!IMPORTANT]
> Muista tuoda muokkaamasi raporttiasetteluasiakirja. Muussa tapauksessa uusi raportin asettelu ei ole käytettävissä.

<!--
##  <a name="MakeChangesToLayout"></a> Create and modify custom report layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### Embedding fonts in Word layouts for consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. Learn more about embedding fonts in Word at [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Removing label and data fields in Word layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### To remove a label or data field  

1. Right-click the field you want to delete, then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### Adding data fields

Adding data fields from a report dataset is more advanced and requires some knowledge of the report dataset. Learn more about adding fields for data, labels, and images at [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
[Nykyisen raportin asettelun muuttaminen](ui-how-change-layout-currently-used-report.md)  
[Raporttien tai asiakirjojen mukautetun asettelun tuonti ja vienti](ui-how-import-and-export-report-layout.md)  
[Raporttien, eräajojen ja XMLportien käsitteleminen](ui-work-report.md)  
[Talousraportoinnin valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md)  
[Business Intelligence](bi.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
