---
title: Raportin suorituksen ajoittaminen tietylle päivämäärälle ja kellonajalle | Microsoft Docs
description: Tutustu, miten raportti lisätään työjonoon ja ajoitetaan käsiteltäväksi tiettynä päivänä ja tiettyyn kellonaikaan.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: e4b1615ebf177db94e3dfb372809fa71ed2f1459
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760165"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Raporttien, eräajojen ja XMLportien käsitteleminen

Raportti kerää tietoja määritettyjen ehtojen perusteella. Tiedot järjestetään raporttiin helposti luettavassa muodossa, jonka voi tulostaa tai tallentaa tiedostona. Sovelluksesta voi käyttää monenlaisia raportteja. Raporteissa on yleensä avattuna olevan sivun sisältöön liittyviä tietoja. Esimerkiksi **Asiakas**-sivun raportit koskevat 10 suurinta asiakasta, myyntitilastoja ja niin edelleen.

Eräajot ja XMLportit toimivat käytännössä samalla tavoin kuin raportit, mutta niiden tarkoitus on suorittaa prosessi tai viedä tietoja. Esimerkiksi **Luo muistutukset** -erätyö luo muistutusasiakirjoja asiakkaille, joilla on erääntyneitä maksuja.  

> [!NOTE]
> Tässä ohjeaiheessa viitataan pääsiassa raportteihin, mutta vastaavat tiedot koskevat myös erätöitä ja XMLporteja.

## <a name="getting-started"></a>Aloitusopas

Löydät raportteja valittujen sivujen **Raportit**-välilehdessä tai käytä ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toimintoa](media/ui-search/search_small.png "Kerro, mitä haluat tehdä"), jos haluat etsiä raportteja nimen mukaan.

Raportissa, erätyössä tai XMLportissa avautuu ensimmäisenä pyyntösivu, johon voi tyypillisesti määrittää erilaisia vaihtoehtoja ja suodattimia. Raportin sisältö määrittyy näiden tietojen mukaan. Seuraavissa osissa kerrotaan, kuinka pyyntösivua käytetään raportin luomiseen, esikatseluun ja tulostamiseen.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Oletusarvojen käyttäminen - ennalta määritetyt asetukset 

Useimmat pyyntösivut sisältävät **Käytä oletusarvoja** -kentän. Tämän kentän avulla voit valita raportille ennalta määritettyjä asetuksia, jotka automaattisesti antavat raportin asetukset ja suodattimet. Valitse tapahtuma avattavasta luettelosta ja näet vaihtoehdot ja suodattimet muutospyyntösivulla vastaavasti.

**Viimeksi käytetyt asetukset ja suodattimet** -kirjaus on aina saatavilla. Tämä merkintä määrittää raportin käyttämään niitä asetuksia ja suodattimia, joita käytettiin, kun ajoit raportin edellisen kerran.

**Käytä oletusarvoja** -kentästä saadaan nopea ja luotettava tapa luoda raportteja, jotka sisältävät oikeat tiedot. Kun olet valinnut tapahtuman, voit muuttaa mitä tahansa vaihtoehtoa ja suodatinta ennen raportin esikatselua tai tulostamista. Tekemäsi muutokset eivät tallennu ennalta määritettyjen asetusten tapahtumaan, mutta ne tallennetaan **Viimeksi käytetyt asetukset ja suodattimet** -tapahtumaan.

>[!NOTE]
> Järjestelmänvalvoja määrittää ja hallinnoi tavallisesti esimääritettyjä asetuksia. Lisätietoja on kohdassa [Raporttien ja erätöiden tallennettujen asetusten hallinta](reports-saving-reusing-settings.md).
<!--
Depending on the report, the request page might include the **Use default values from** field. This field lets you select a predefined set of can include the **Saved Settings** section that contains one or more entries in the **Use default value from** box. A saved setting is basically a predefined group of options and filters that you can apply to the report before previewing or sending the report to a file. The saved settings entry called **Last used options and filters** is always available. This entry sets the report to use options and filters that were used the last time you used the report.

Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data. After you set the **Use default value from** box to a saved settings entry, you can change any of the options and filters before previewing or saving the report. The changes that you make will not be saved to the saved settings entry you selected, but they will be saved to the **Last used options and filters** entry.

>[!NOTE]
>If you are an administrator, you can create and manage the saved settings for reports for all users. For more information, see [Manage Saved Settings for Reports and Batch Jobs](reports-saving-reusing-settings.md).
-->
## <a name="specifying-the-data-to-include-in-reports"></a>Raportteihin sisällytettävien tietojen määrittäminen

Käytä **vaihtoehtojen** ja **suodattimien** alla olevia kenttiä muuttaaksesi raporttiin haluamasi tietojen rajoja. Raportin suodattimet määritetään käytännössä samalla tavoin kuin luetteloiden suodattimet. Lisätietoja on kohdassa [Suodattaminen](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Pyyntösivun **Luettelon suodatusperuste** -osassa on raporttien yleinen suodatustoiminto. Nämä suodattimet ovat valinnaisia.
>
> Osa raporteista ohittaa nämä suodattimet, joten raportin tulos sama riippumatta siitä, mikä suodatin on määritetty **Luettelon suodatusperuste** -osassa. Eri raporteissa ohitettavista kentistä ei ole mahdollista luoda luetteloa, joten sinun on kokeiltava erilaisten suodattimien käyttöä.
>
> **Esimerkki**: kun käytät **Luo muistutukset** -erätyötä, **Viimeksi lähetetyn muist. taso** -kohdan **Asiakastapahtumat**-kenttä ohitetaan, koska kyseissä työssä käytetään kiinteitä suodattimia.

## <a name="previewing-a-report"></a>Raportin esikatselu

Raportin esikatselussa voit nähdä, miltä raportti näyttää ennen tulostamista. Esikatselu määrittää raportin asetukset pyyntösivun **Tulostin**-kentässä näkyvän [tulostimen](#Printer) perusteella. Esikatselun jälkeen voit palata pyyntösivulle ja tehdä muutoksia asetuksiin ja suodattimiin tarpeen mukaan.

Voit esikatsella raporttia valitsemalla raportin pyyntösivun **Esikatselu**- tai **Esikatsele & Sulje** -painikkeen. Näyttöön tulee raportti, jossa näkyy **Esikatselu**-painike, ja toisissa on **Esikatsele & Sulje** -painike. Molemmat painikkeet avaavat raportin esikatselun. Erona on, että **Esikatselu** pitää pyyntösivun avoinna, joten voit palata siihen, tehdä muutoksia, esikatsella uudelleen tai tulostaa. Kun **Esikatsele & sulje** -vaihtoehdossa pyyntösivu sulkeutuu, joten sinun on avattava raportti uudelleen, jotta voit tehdä muutoksia tai tulostaa.

> [!NOTE]
> Jos käytät Business Central 2020 julkaisuaalto 1-versiota tai sitä vanhempaa versiota, saatavilla on vain **Esikatselu**-painike, joka sulkee pyyntösivun esikatselussa, kuten **Esikatsele & sulje** -toiminto.

### <a name="working-with-the-preview"></a>Esikatselun käyttäminen

Raportin esiversion valikkorivin avulla voi:

- siirtyä sivuilla
- lähentää ja loitontaa
- muuttaa sivulle sopivaksi
- Valitse teksti

    Voit kopioida raportista tekstiä ja liittää sen toisaalle, kuten [!INCLUDE[prod_short](includes/prod_short.md)]in sivulle tai Microsoft Wordiin.  Aseta hiiri aloituskohtaan, pidä hiiren painike painettuna, valitse sitten sanat, lauseet tai kappaleet hiirtä siirtämällä. Paina sitten hiiren kakkospainiketta ja valitse **Kopioi**. Voit sitten liittää valitun tekstin valitsemaasi paikkaan.
- Panoroi asiakirja

    Voit siirtää näkyvissä olevaa raportin aluetta kaikkiin suuntiin, joten saat näkyviin myös raportin muut alueet. Panorointi on kätevää, jos olet lähentänyt tekstiin yksityiskohtia tarkastelemaan.  Paina esimerkiksi hiiren painiketta pitkään raportin esikatselussa ja siirrä sitten hiirtä.

- Ladata PDF-tiedosto tietokoneessa tai verkossa.
- Tulosta

## <a name="saving-a-report"></a>Raportin tallentaminen

Voit tallentaa raportin PDF-tiedostona, Microsoft Word -asiakirjana tai Microsoft Excel -tiedostona valitsemalla **Lähetä kohteeseen** -painikkeen ja tekemällä valinnan.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Suoritettavan raportin aikatauluttaminen

Voit aikatauluttaa raportin tai erätyön ajon tietylle päivämäärälle ja kellonajalle. Aikataulutetut raportit ja erätyöt syötetään työjonoon ja käsitellään aikataulutettuna aikana vastaavasti kuin muut työt. **Aikataulu**-asetus valitaan sen jälkeen, kun **Lähetä kohteeseen** -painike on valittu, minkä jälkeen annetaan tiedot, kuten tulostin sekä päivämäärä ja kellonaika. Raportti lisätään tämän jälkeen työjonoon ja suoritetaan määritettynä ajankohtana. Kun raportti on käsitelty, kohde poistetaan työjonosta. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).  

Kun raportti aikataulutetaan suoritettavaksi, se voidaan määrittää suoritettavaksi joka torstai määrittämällä esimerkiksi **Seuraavan suorituspäivän kaava** -kentän arvoksi *D4*. Lisätietoja on kohdassa [Päivämäärän kaavojen käyttäminen](ui-enter-date-ranges.md#using-date-formulas).  

Voit tallentaa raportin tiedostoon, kuten Excel-, Word- tai PDF-tiedostoon, tulostaa sen valitulle tulostimelle tai vain luoda sen. Jos haluat tallentaa raportin tiedostoon, käsitelty raportti lähetetään roolikeskuksen **Saapuneet raportit** -alueelle, jossa voit tarkastella sitä.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Raportin tulostaminen

Tulosta raportti, valitse **Tulosta**-painike pyyntösivulla tai **Esikatselu**-sivun valikkorivillä.

<!--
### Printer selection

The report prints to the printer shown in the **Selected printer** field on the report request page. You can't change the printer from this page.

The selected printer is either set on the **Printer Selections** page or it's the default printer set up on the **Printer Management** page. If you want to use another printer, see  [Set Up Printers](ui-specify-printer-selection-reports.md).

If no printer is specified on the **Printer Selections** page or set as default on the **Printer Management** page, the browser printing feature is used. In this case, **Browser** appears in the **Selected printer** field on the report request page.
-->
### <a name="printer"></a><a name="Printer"></a>Tulostin

**Tulostin**-kentässä raportin pyyntösivulla näkyy mille tulostimelle raportti tulostetaan. **(Selaimen käsittelemä)** ilmaisee, että raportille ei ole määritetty tulostinta. Tässä tapauksessa selain käsittelee tulosteen ja näyttää vakiokokemuksen, jossa voit valita laitteeseesi yhdistetyn paikallisen tulostimen.

Tulostinta ei voi muuttaa **tulostin**-kentän avulla. Jos haluat muuttaa tulostinta, siirry **tulostimen valinnat**- tai **tulostimen hallinta** -sivulle. Tulostimen määrittäminen on yleensä järjestelmänvalvojan tehtävä. Jos haluat lukea lisää, katso [Tulostimien määrittäminen](ui-specify-printer-selection-reports.md).

<!--
### Browser printing

Because [!INCLUDE[prod_short](includes/prod_short.md)] is a cloud service, it can't reach local printers connected to your computer. However, it can connect to cloud-enabled printers. In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a cloud printer named **Email Printer** is installed as an extension and is ready to use after initial setup.

If a cloud printer is not installed and set up, or if an installed printer fails, then printing will default to the printing options for the browser.

> [!NOTE]
> The browser printing options work independently of [!INCLUDE[prod_short](includes/prod_short.md)]. So any printer settings that might have been set up from printers in [!INCLUDE[prod_short](includes/prod_short.md)] aren't carried over to the browser print options.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
### <a name="printing-reports-in-thai"></a>Thainkielisten raporttien tulostaminen

Koskien erityisesti [!INCLUDE[prod_short](includes/prod_short.md)]in Thaimaalaista versioita, **Tulosta** painike ei voi tulostaa raportteja oikein, johtuen tulostettavien PDF tiedostojen palvelun rajoituksista. Sen sijaan, raportin voi avata Wordilla, ja tallentaa sen tulostettavaan PDF muotoon.  

Vaihtoehtoisesti, voit pyytää järjestelmänvalvojaa luomaan Word-raporttipohjan käytetyimmille raporteillesi. Lisätietoja on kohdassa [Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Raporttiasetteluiden muuttaminen

Raportin asettelu määrittää, mitä raportissa näytetään, miten se on järjestetty ja mitä tyyliä siinä käytetään. Lisätietoja toiseen asetteluun vaihtamisesta on kohdassa [Nykyisen raporttiasettelun muuttaminen](ui-how-change-layout-currently-used-report.md). Jos puolestaan haluat mukauttaa omaa raporttiasettelua, lisätietoja on kohdassa [Mukautetun raporttiasettelun luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

## <a name="advanced-options"></a>Lisäasetukset

Tulostimen resursseja hallitaan luodun raportin **lisäasetukset**-kohdan kentissä. Näitä asetuksia ei yleensä tarvitse muuttaa, ellei sinulla ole suurta raporttia. Jos raportti ylittää nämä rajoitukset, kun yrität esikatsella tai tulostaa, näyttöön tulee sanoma, jossa kerrotaan, mikä rajoitus on ylitetty. Tämän jälkeen voit muuttaa asetuksia raportin mukaisiksi. Jokaisella kentällä on kuitenkin maksimiarvo, josta sinun tulee olla tietoinen:

|Kenttä|Maksimiarvo|
|-----|-------------|
|Hahmonnuksen enimmäisaika|12:00:00|
|Rivien enimmäismäärä|1000000|
|Asiakirjojen enimmäismäärä|500|

> [!NOTE]
> Enimmäisarvot voivat olla erilaiset [!INCLUDE[prod_short](includes/prod_short.md)] paikallisesti, ja järjestelmänvalvoja voi muuttaa niitä. Lisätietoja on kohdassa [Business Central Serverin määrittäminen - raportit](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Yhteenveto raporttien rajoituksista [!INCLUDE[prod_short](includes/prod_short.md)] onlinessa, on kohdassa [Toimintarajat](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-also"></a>Katso myös

[Tulostimien määrittäminen](ui-specify-printer-selection-reports.md)  
[Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md)  
[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)
