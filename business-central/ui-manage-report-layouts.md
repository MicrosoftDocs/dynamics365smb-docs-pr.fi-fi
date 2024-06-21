---
title: Raporttien ja asiakirjojen asettelujen hallinta
description: 'Voit mukauttaa asiakirjoja raporttiasettelujen avulla. Voit muokata tällä tavoin asiakkaille lähetettävien PDF-tiedostojen fonttia, logoa tai sivuasetuksia.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650, 9660'
ms.date: 01/18/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Raporttien ja asiakirjojen asettelujen yleiskatsaus

Raporttiasettelu ohjaa raportin sisältöä ja muotoa, mukaan lukien, mitkä tietojen kentät näkyvät raportissa ja miten ne järjestetään, tekstityylin, kuvia ja muita ominaisuuksia. Voit luoda [!INCLUDE[prod_short](includes/prod_short.md)]ista uuden asettelun, muuttaa raportissa käytettävää asettelua tai muokata nykyisiä asetteluja.

> [!NOTE]  
> Raportti tarkoittaa [!INCLUDE[prod_short](includes/prod_short.md)]issa myös ulkoisille käyttäjille tarkoitettuja asiakirjoja, kuten myyntilaskuja tai tilausvahvistuksia, jotka lähetetään asiakkaille PDF-tiedostoina.

Voit myös käyttää raporttiasetteluja lisätäksesi sisältöä sähköpostiviesteihin. Raporttiasettelut voivat esimerkiksi säästää aikaa ja auttaa yhdenmukaisuuden varmistamisessa siten, että samaa sisältöä käytetään uudelleen, kun viestit asiakkaidesi kanssa. Jotta voit käyttää mukautettuja raporttiasetteluja sähköpostissa, niiden tiedostotyyppinä on oltava Word. Et voi käyttää RDLC-tiedostotyyppiä. Lisätietoja: [Uudelleenkäytettävien sähköpostitekstien ja -asettelujen määrittäminen](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## Esittely

Erityisesti raporttiasettelu määrittää seuraavat asetukset:

* [!INCLUDE[prod_short](includes/prod_short.md)]-raportin tietojoukosta sisällytettävät tunnus- ja tietokentät.
* Tekstin muoto, kuten kirjasimen tyyppi, koko ja väri.
* Yrityksen logo ja sen sijainti.
* Yleiset sivun asetukset, esimerkiksi reunukset ja taustakuvia.

Raportti voidaan määrittää useille raportin asetteluille, joita voit vaihtaa tarpeen mukaan. 

<!--You can use one of the built-in report layouts or you can create custom report layouts and assign them to your reports as needed. For more information, see [Create a Custom Report or Document Layout](ui-how-create-custom-report-layout.md).-->

Raportin asetteluissa on kaksi tärkeää näkökohtaa, jotka vaikuttavat niiden käsittelytapaan: *asettelun tyyppi* ja *asettelun lähde*. Asettelun tyyppi ilmaisee tiedoston tyypin, johon asettelu perustuu. Asettelun tyyppi ilmaisee asettelun alkuperän.

## Asettelun tyypit

Raporteissa käytettävän asettelun tyyppi voi olla neljänlainen: Word, RDLC, Excel tai ulkoinen.

### Word

Word-asettelut perustuvat Word-asiakirjoihin (.docx-tiedostotyyppi). Word-asetteluiden avulla voit suunnitella raporttiasetteluita käyttämällä Microsoft Wordiä. Word-asettelu määrittää raportin sisällön ja ohjaa sitä, miten sisältöelementit järjestetään ja miltä ne näyttävät. Asettelu Word-asiakirjassa käyttää yleensä taulukoita, joiden avulla voit järjestää sisältöä, jossa solut sisältävät tietokentät, tekstiä tai kuvia.

[![Esimerkki Word-raporttiasetteluasiakirjasta Business Centralille.](media/word-layout-overview.png)](media/word-layout-overview.png#lightbox) 

<!--![Example of a word report layout document for Business Central.](media/nav_wordreportlayout_edit_in_word_example.png) -->

Lisätietoja on kohdassa [Wordin asettelujen käyttö](ui-how-add-fields-word-report-layout.md).

### Excel

Excel-asettelujen perustana ovat Microsoft Excel-työkirjat (.xlsx-tiedostotyyppi). Niiden avulla voit luoda raportteja käyttämällä tuttuja Excelin ominaisuuksia yhteenvetoon, analysointiin ja tietojen esittämiseen työkaluilla, kuten kaavoilla, pivot-taulukoilla ja pivot-kaavioilla.

[![Näyttää esimerkin Excelin asettelusta.](media/excel-layout-2.png)](media/excel-layout-2.png#lightbox)

Lisätietoja on kohdassa [Excel-asettelujen käyttö](ui-excel-report-layouts.md).

### RDLC

RDLC-asettelut perustuvat asiakkaan määrittelemiin raportinasettelutiedostoihin (.rdl- tai .rdlc-tiedostotyypit). Näitä asetteluja luodaan ja muokataan käyttämällä SQL Server Report Builderia tai Microsoft RDLC Report Designeria. RDLC-asettelujen suunnittelukonsepti on samankaltainen kuin Wordin asetteluissa, joissa asettelu määrittää, mitkä kentät näytetään ja miten ne järjestetään. RDLC-asetteluiden suunnitteleminen on kuitenkin monimutkaisempaa kuin Word-asetteluiden.

[![Näyttää esimerkin RDLC-asettelusta.](media/rdlc-layout-overview.png)](media/rdlc-layout-overview.png#lightbox)

Lisätietoja on kohdassa [RDLC-asettelujen käyttö](ui-rdlc-report-layouts.md).

### Ulkoinen

Ulkoinen asettelutyyppi viittaa erikoistyyppiin, joka on suunniteltu erityisesti tiettyjä raportteja varten. Raportit ja kaavat ovat tavallisesti kumppaneiden toimittamia, eivät Microsoftilta. Asettelun todellinen tiedostotyyppi vaihtelee palveluntarjoajan mukaan.

Lisätietoja on ohjeaiheessa [Mukautetun raportin hahmonnuksen kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-report-custom-render).

## Asettelun lähteet

Tyypin lisäksi asettelut jaetaan edelleen kolmeen luokkaan niiden lähteen tai alkuperän perusteella.

* Laajennuksen asettelut

   Laajennuksen asettelut ovat asetteluita, jotka ovat osa ympäristöön asennettua laajennusta. Nämä asettelut ovat tyypillisesti Microsoftin toimittamia vakioasetteluja, esimerkiksi perussovelluksessa. Tai ne voivat olla kaavoja, jotka sisältyvät muiden ohjelmistopalveluiden laajennuksiin. Voit tunnistaa laajennuksen asettelut **Raporttiasettelut**-sivulla, koska laajennuksen nimi ja julkaisija näkyvät **Laajennus**-sarakkeessa.

* Käyttäjän määrittämät asettelut

   Muut asettelujen lähteet ovat loppukäyttäjiä. Business Centralin sisältä käyttäjä, jolla on asianmukaiset käyttöoikeudet, voi lisätä uusia asetteluja eri tavoilla. Voit esimerkiksi aloittaa aiemmin luodusta laajennuksen asettelusta tai muusta käyttäjän määrittämästä asettelusta. **Raporttiasettelut**-kohdassa käyttäjän määrittämässä asettelussa on tyhjä **Laajennus**-sarake.

   Lisätietoja on kohdassa [Aloita raporttiasettelujen luominen](ui-get-started-layouts.md).

* Mukautetut asettelut

  Mukautetut asettelut ovat myös käyttäjien luomia asetteluita. Erona on se, että nämä asettelut luodaan vanhalta **Mukautetut raporttiasettelut** -sivulta, ja ne voivat olla vain Word- tai RDLC-tyyppejä. Vaikka voit yhä luoda mukautettuja asetteluita, ne poistetaan käytöstä käyttäjän määrittämien asettelujen vuoksi (katso yltä).

  Lisätietoja on kohdassa [(Vanha) Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

Lisätietoja siitä, mikä tyyppi sopii parhaiten sinulle, on ohjeaiheessa [Haluamasi asettelun tyypin valitseminen](ui-get-started-layouts.md#decide).

> [!IMPORTANT]
> On tärkeää muistaa, että et voi muokata laajennuksen asetteluita Business Central -asiakkaasta. Et voi esimerkiksi muuttaa asettelun nimeä tai tyyppiä tai ladata ja korvata sitä toisella versiolla. Jos yrität tehdä niin, näyttöön avautuu virhesanoma. Sinun on sen sijaan luotava käyttäjän määrittämä tai mukautettu asettelu laajennuksen asettelun perusteella.

<!--
### Built-in and custom report layouts



[!INCLUDE[prod_short](includes/prod_short.md)] includes several built-in layouts. Built-in layouts are predefined layouts that are designed for specific reports. [!INCLUDE[prod_short](includes/prod_short.md)] reports will have a built-in layout as either an RDLC report layout, Word report layout, or in some cases both. You can’t modify a built-in report layout from [!INCLUDE[prod_short](includes/prod_short.md)] but you use them as a starting point for building your own custom report layouts.

Custom layouts are report layouts that you design to change the appearance of a report. You typically create a custom layout based on a built-in layout, but you can create them from scratch or from a copy of an existing custom layout. Custom layouts enable you to have multiple layouts for the same report, which you switch among as needed. For example, you can have different layouts for each [!INCLUDE[prod_short](includes/prod_short.md)] company, or you can have different layouts for the same company for specific occasions or events, like a special campaign or holiday season.


Deciding on whether to use a Word, Excel, or RDLC layout type will depend on how you want the generated report to look and your knowledge of tools for creating the layouts, like Word, Excel, and SQL Server Report Builder.

* The general design concepts for Word and RDLC layouts are similar. However each type has certain design features that affect how the generated report appears in [!INCLUDE[prod_short](includes/prod_short.md)]. This means that the same report might look different when using the Word report layout compared to the RDLC report layout.

* The process for setting up Word, Excel, and RDLC report layouts on reports is the same. The main difference is in the way you modify the layouts. Word and especially Excel layouts are typically easier to create and modify than RDLC report layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.

* Not all reports and document have a dataset that is optimized for use with an Excel layout. For example, aggregations and complex calculations work best with RDLC or Word layouts. The same is true for documents.

For information about how to switch the layout currently used on a report, see [Set the Layout Used by a Report](ui-set-report-layout.md).

-->
## Katso myös

[Raporttien mukautettujen asetteluiden päivittäminen](ui-update-report-layouts.md)  
[Raporttien mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)  
[Raporttien tai asiakirjojen mukautetun asettelun tuonti ja vienti](ui-how-import-and-export-report-layout.md)  
[Erikoisasiakirja-asettelujen määrittäminen asiakkaille ja toimittajille](ui-define-customer-vendor-document-layouts.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Raporttien, eräajojen ja XMLportien käsitteleminen](ui-work-report.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
