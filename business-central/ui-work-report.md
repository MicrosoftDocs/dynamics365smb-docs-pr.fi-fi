---
title: Raporttien, eräajojen ja XMLportien käsitteleminen
description: Tutustu, miten raportti lisätään työjonoon ja ajoitetaan käsiteltäväksi tiettynä päivänä ja tiettyyn kellonaikaan.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.date: 02/09/2022
ms.author: jswymer
ms.openlocfilehash: 142a9f826e200f06172b741e72e54d49ff9caf47
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102601"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Raporttien, eräajojen ja XMLportien käsitteleminen

Raportti kerää tietoja määritettyjen ehtosarjojen perusteella. Se järjestää ja esittää tiedot helposti luettavassa muodossa, jonka voit tulostaa tai tallentaa tiedostona. Sovelluksesta voi käyttää monenlaisia raportteja. Raporteissa on yleensä avattuna olevan sivun sisältöön liittyviä tietoja. Esimerkiksi **Asiakas**-sivun raportit koskevat 10 suurinta asiakasta, myyntitilastoja ja niin edelleen.

Eräajot ja XMLportit toimivat käytännössä samalla tavoin kuin raportit, mutta niitä käytetään enemmän tietojen käsittelyyn tai vientiin. Esimerkiksi **Luo muistutukset** -erätyö luo muistutusasiakirjoja asiakkaille, joilla on erääntyneitä maksuja.  

> [!NOTE]
> Tässä ohjeaiheessa viitataan pääsiassa raportteihin, mutta vastaavat tiedot koskevat myös erätöitä ja XMLporteja.

## <a name="getting-started"></a>Aloitusopas

Löydät raportteja valittujen sivujen **Raportit**-välilehdessä tai käytä ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") , jos haluat etsiä raportteja nimen mukaan.

Raportissa, erätyössä tai XMLportissa avautuu ensimmäisenä pyyntösivu, johon voi tyypillisesti määrittää erilaisia vaihtoehtoja ja suodattimia. Raportin sisältö määrittyy näiden tietojen mukaan. Seuraavissa osissa kerrotaan, kuinka pyyntösivua käytetään raportin luomiseen, esikatseluun ja tulostamiseen.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Oletusarvojen käyttäminen - ennalta määritetyt asetukset

Useimmat pyyntösivut sisältävät **Käytä oletusarvoja** -kentän. Tämän kentän avulla voit valita raportille ennalta määritettyjä asetuksia, jotka automaattisesti antavat raportin asetukset ja suodattimet. Valitse tapahtuma avattavasta luettelosta ja näet vaihtoehdot ja suodattimet muutospyyntösivulla vastaavasti.

**Viimeksi käytetyt asetukset ja suodattimet** -kirjaus on aina saatavilla. Tämä merkintä määrittää raportin käyttämään niitä asetuksia ja suodattimia, joita käytettiin, kun ajoit raportin edellisen kerran.

**Käytä oletusarvoja** -kentästä saadaan nopea ja luotettava tapa luoda raportteja, jotka sisältävät oikeat tiedot. Kun olet valinnut tapahtuman, voit muuttaa mitä tahansa vaihtoehtoa ja suodatinta ennen raportin esikatselua tai tulostamista. Tekemäsi muutokset eivät tallennu ennalta määritettyjen asetusten tapahtumaan, mutta ne tallennetaan **Viimeksi käytetyt asetukset ja suodattimet** -tapahtumaan.

>[!NOTE]
> Järjestelmänvalvoja määrittää ja hallinnoi tavallisesti esimääritettyjä asetuksia. Lisätietoja on kohdassa [Raporttien ja erätöiden tallennettujen asetusten hallinta](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-reports"></a>Raportteihin sisällytettävien tietojen määrittäminen

Käytä **vaihtoehtojen** ja **suodattimien** alla olevia kenttiä muuttaaksesi raporttiin haluamasi tietojen rajoja. Raportin suodattimet määritetään käytännössä samalla tavoin kuin luetteloiden suodattimet. Lisätietoja on kohdassa [Suodattaminen](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Pyyntösivun **Luettelon suodatusperuste** -osassa on raporttien yleinen suodatustoiminto. Nämä suodattimet ovat valinnaisia.
>
> Osa raporteista ohittaa nämä suodattimet, joten raportin tulos sama riippumatta siitä, mikä suodatin on määritetty **Luettelon suodatusperuste** -osassa. Eri raporteissa ohitettavista kentistä ei ole mahdollista luoda luetteloa, joten sinun on kokeiltava erilaisten suodattimien käyttöä.
>
> **Esimerkki**: kun käytät **Luo muistutukset** -erätyötä, **Viimeksi lähetetyn muist. taso** -kohdan **Asiakastapahtumat**-kenttä ohitetaan, koska kyseissä työssä käytetään kiinteitä suodattimia.

## <a name="previewing-a-report"></a>Raportin esikatselu

Raportin esikatselussa voit nähdä, miltä raportti näyttää ennen tulostamista. Esikatselu ei perustu pyyntösivun **Tulostin**-kentässä valittuun tulostimeen. Se on selaimen hallinnassa. Esikatselun jälkeen voit palata pyyntösivulle ja tehdä muutoksia asetuksiin ja suodattimiin tarpeen mukaan.

Voit esikatsella raporttia valitsemalla raportin pyyntösivun **Esikatselu**- tai **Esikatsele & Sulje** -painikkeen. Näyttöön tulee raportti, jossa näkyy **Esikatselu**-painike, ja toisissa on **Esikatsele & Sulje** -painike. Molemmat painikkeet avaavat raportin esikatselun. Erona on, että **Esikatselu** pitää pyyntösivun avoinna, joten voit palata siihen, tehdä muutoksia, esikatsella uudelleen tai tulostaa. Kun **Esikatsele & sulje** -vaihtoehdossa pyyntösivu sulkeutuu, joten sinun on avattava raportti uudelleen, jotta voit tehdä muutoksia tai tulostaa.

> [!NOTE]
> Jos käytät Business Centralin vuoden 2020 1. julkaisuaaltoa tai sitä vanhempaa versiota, saatavilla on vain **Esikatselu**-painike, joka sulkee pyyntösivun esikatselussa, kuten **Esikatsele ja sulje** -toiminnossa on kuvattu.

### <a name="working-with-the-preview"></a>Esiversion käyttäminen

Raportin esiversion valikkorivin avulla voi:

- siirtyä sivuilla
- lähentää ja loitontaa
- muuttaa sivulle sopivaksi
- Valitse teksti

    Voit kopioida raportista tekstiä ja liittää sen toisaalle, kuten [!INCLUDE[prod_short](includes/prod_short.md)]in sivulle tai Microsoft Wordiin.  Esimerkiksi hiirtä käyttäessäsi voit pitää hiiren osoitinta painettuna kohdassa, josta haluat aloittaa. Valitse sitten yksi tai useampi sana, lause tai kappale liikuttaen hiirtä. Paina sitten hiiren kakkospainiketta ja valitse **Kopioi**. Voit sitten liittää valitun tekstin valitsemaasi paikkaan.
- Panoroi asiakirja

    Voit siirtää näkyvissä olevaa raportin aluetta kaikkiin suuntiin, joten saat näkyviin myös raportin muut alueet. Panorointi on kätevää, jos olet lähentänyt tekstiin yksityiskohtia tarkastelemaan.  Paina esimerkiksi hiiren painiketta pitkään raportin esikatselussa ja siirrä sitten hiirtä.

- Ladata PDF-tiedosto tietokoneessa tai verkossa.
- Tulosta

## <a name="saving-a-report-to-a-file"></a>Raportin tallentaminen tiedostoon

Voit tallentaa raportin PDF-tiedostona, Microsoft Word -asiakirjana tai Microsoft Excel -työkirjana valitsemalla **Lähetä kohteeseen** -painikkeen ja tekemällä valinnan.

### <a name="about-sending-to-excel"></a>Tietoja Exceliin lähettämisestä

Voit käsitellä [!INCLUDE [prod_short](includes/prod_short.md)] -tietoja Excelissä tarkempia analyyseja varten. Lisätietoja [Raporttitietojen analysointi Excelissä](report-analyze-excel.md).  
<!--
### About sending to Word

Use the **Microsoft Word Document** option to generate a report as a Word document.  

> [!NOTE]
> You can specify the layout to use for each report on the **Report Selection** page in the **Selected Layout** field. The default setting for reports is **RDLC (built-in)**, which produces reports in the same, or similar, layout as the **Microsoft Word Document** layout. However, the key difference is whether you want to generate a single or multiple report documents. For single documents, you can use the RDLC (built-in) option. For multiple documents, set the **Microsoft Word Document** as the default layout for the report. For more information, see [Managing Report and Document Layouts](ui-manage-report-layouts.md).

-->

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Suoritettavan raportin aikatauluttaminen

Voit aikatauluttaa raportin tai erätyön ajon tietylle päivämäärälle ja kellonajalle. Aikataulutetut raportit ja erätyöt syötetään työjonoon ja käsitellään aikataulutettuna aikana vastaavasti kuin muut työt. **Aikataulu**-asetus valitaan sen jälkeen, kun **Lähetä kohteeseen** -painike on valittu, minkä jälkeen annetaan tiedot, kuten tulostin sekä päivämäärä ja kellonaika. Raportti lisätään tämän jälkeen työjonoon ja suoritetaan määritettynä ajankohtana. Kun raportti on käsitelty, kohde poistetaan työjonosta. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).  

Kun raportti aikataulutetaan suoritettavaksi, se voidaan määrittää suoritettavaksi joka torstai määrittämällä esimerkiksi **Seuraavan suorituspäivän kaava** -kentän arvoksi *D4*. Lisätietoja on kohdassa [Päivämäärän kaavojen käyttäminen](ui-enter-date-ranges.md#using-date-formulas).  

Voit tallentaa raportin tiedostoon (kuten Excel-, Word- tai PDF-tiedostoon), tulostaa sen tai vain luoda raportin. Jos haluat tallentaa raportin tiedostoon, käsitelty raportti lähetetään roolikeskuksen **Saapuneet raportit** -alueelle, jossa voit tarkastella sitä.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Raportin tulostaminen

Tulosta raportti, valitse **Tulosta**-painike pyyntösivulla tai **Esikatselu**-sivun valikkorivillä.

### <a name="printer"></a><a name="Printer"></a>Tulostin

**Tulostin**-kentässä raportin pyyntösivulla näkyy mille tulostimelle raportti tulostetaan. Tulostimen voi vaihtaa valitsemalla tulostimen luettelossa.

> [!NOTE]
> **(Käsitellään selaimessa)** ilmaisee, että raportille ei ole määritetty tulostinta. Tässä tapauksessa selain käsittelee tulosteen ja näyttää vakiokokemuksen, jossa voit valita laitteeseesi yhdistetyn paikallisen tulostimen. **(Käsitellään selaimessa)** ei ole käytössä [!INCLUDE[prod_short](includes/prod_short.md)] -mobiilisovelluksessa tai Microsoft Teamsin selaimessa.

> [!TIP]
> Oletustulostimeksi valittu tulostin määritetään **Tulostimen valinnat** -sivulla. Lisätietoja oletustulostimen vaihtamisesta on kohdassa [Tulostimien ja niiden tulostamien raporttien valitseminen](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Thainkielisten raporttien tulostaminen

Koskien erityisesti [!INCLUDE[prod_short](includes/prod_short.md)]in Thaimaalaista versioita, **Tulosta** painike ei voi tulostaa raportteja oikein, johtuen tulostettavien PDF tiedostojen palvelun rajoituksista. Sen sijaan, raportin voi avata Wordilla, ja tallentaa sen tulostettavaan PDF muotoon.  

Voit myös pyytää järjestelmänvalvojaa luomaan Wordin raporttiasettelun käytetyimmille raporteillesi. Lisätietoja on kohdassa [Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md).  

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


[!INCLUDE[footer-include](includes/footer-banner.md)]