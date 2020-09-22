---
title: Raportin suorituksen ajoittaminen tietylle päivämäärälle ja kellonajalle | Microsoft Docs
description: Tutustu, miten raportti lisätään työjonoon ja ajoitetaan käsiteltäväksi tiettynä päivänä ja tiettyyn kellonaikaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 06/10/2020
ms.author: edupont
ms.openlocfilehash: f209088459f29ba5618b065c3a340b0e3bd250e5
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788394"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Raporttien, eräajojen ja XMLportien käsitteleminen

Raportti kerää tietoja määritettyjen ehtojen perusteella. Tiedot järjestetään raporttiin helposti luettavassa muodossa, jonka voi tulostaa tai tallentaa tiedostona. Sovelluksesta voi käyttää monenlaisia raportteja. Raporteissa on yleensä avattuna olevan sivun sisältöön liittyviä tietoja. Esimerkiksi **Asiakas**-sivun raportit koskevat 10 suurinta asiakasta, myyntitilastoja ja niin edelleen.

Eräajot ja XMLportit toimivat käytännössä samalla tavoin kuin raportit, mutta niiden tarkoitus on suorittaa prosessi tai viedä tietoja. Esimerkiksi **Luo muistutukset** -erätyö luo muistutusasiakirjoja asiakkaille, joilla on erääntyneitä maksuja.  

> [!NOTE]
> Tässä ohjeaiheessa viitataan pääsiassa raportteihin, mutta vastaavat tiedot koskevat myös erätöitä ja XMLporteja.

Voit etsiä raportteja valittujen sivujen **Raportit**-välilehdessä tai käyttää ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toimintoa](media/ui-search/search_small.png "Kerro, mitä haluat tehdä"), jos haluat etsiä raportteja nimen mukaan.

## <a name="specifying-the-data-to-include-in-reports"></a>Raportteihin sisällytettävien tietojen määrittäminen
Raportissa, erätyössä tai XMLportissa avautuu ensimmäisenä pyyntösivu, johon voi tyypillisesti määrittää erilaisia vaihtoehtoja ja suodattimia. Raportin sisältö määrittyy näiden tietojen mukaan.

Raportin suodattimet määritetään käytännössä samalla tavoin kuin luetteloiden suodattimet. Lisätietoja on kohdassa [Suodattaminen](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Pyyntösivun **Luettelon suodatusperuste** -osassa on raporttien yleinen suodatustoiminto. Nämä suodattimet ovat valinnaisia.
>
> Osa raporteista ohittaa nämä suodattimet, joten raportin tulos sama riippumatta siitä, mikä suodatin on määritetty **Luettelon suodatusperuste** -osassa. Eri raporteissa ohitettavista kentistä ei ole mahdollista luoda luetteloa, joten sinun on kokeiltava erilaisten suodattimien käyttöä.
>
> **Esimerkki**: kun käytät **Luo muistutukset** -erätyötä, **Viimeksi lähetetyn muist. taso** -kohdan **Asiakastapahtumat**-kenttä ohitetaan, koska kyseissä työssä käytetään kiinteitä suodattimia.

## <a name="using-saved-settings"></a><a name="SavedSettings"></a>Tallennettujen asetusten käyttäminen
Pyyntösivulla voi olla **Tallennetut asetukset** -osa, jossa on vähintään yksi merkintä **Käytä oletusarvoa** -ruudussa. Tallennettu asetus on periaatteessa valmis vaihtoehto- ja suodatinryhmä, jota voit käyttää raportteihin ennen raportin esikatselu tai sen lähettämistä tiedostoon. **Viimeksi käytetyt asetukset ja suodattimet** -kirjaus on aina saatavilla. Tämä merkintä määrittää raportin käyttämään niitä asetuksia ja suodattimia, joita käytettiin, kun käytit raporttia edellisen kerran.

Tallennettujen asetusten käyttäminen on nopea ja helppo tapa oikeiden tietojen sisältämien raporttien luomista varten. Kun olet määrittänyt **Käytä oletusarvoa** -ruutua tallennettujen asetusten merkintään, voit muuttaa asetuksia tai suodattimia ennen raportin esikatselua tai tallennusta. Tekemäsi muutokset eivät tallennu tallennettujen asetusten tapahtumaan, mutta ne tallennetaan **Viimeksi käytetyt asetukset ja suodattimet** -tapahtumaan.

>[!NOTE]
>Mikäli olet järjestelmänvalvoja, voit luoda ja hallita kaikkien käyttäjien raporttien tallennettuja asetuksia. Lisätietoja on kohdassa [Raporttien ja erätöiden tallennettujen asetusten hallinta](reports-saving-reusing-settings.md).

## <a name="previewing-a-report"></a>Raportin esikatselu

Tarkastele raporttia raporttipyyntösivulla valitsemalla **Esikatselu**-painike. Raportin esikatselun valikkorivin avulla voi

- siirtyä sivuilla
- lähentää ja loitontaa
- muuttaa sivulle sopivaksi
- Valitse teksti

    Voit kopioida raportista tekstiä ja liittää sen toisaalle, kuten [!INCLUDE[d365fin](includes/d365fin_md.md)]in sivulle tai Microsoft Wordiin.  Aseta hiiri aloituskohtaan, pidä hiiren painike painettuna ja valitse sitten sanat, lauseet tai kappaleet hiirtä siirtämällä. Voit sitten painaa hiiren kakkospainiketta ja valita **Kopioi**. Voit sitten liittää valitun tekstin valitsemaasi paikkaan.
- Panoroi asiakirja

    Voit siirtää näkyvissä olevaa raportin aluetta kaikkiin suuntiin, joten saat näkyviin myös raportin muut alueet. Tämä on kätevää, jos olet lähentänyt tekstiin yksityiskohtia tarkastelemaan.  Paina esimerkiksi hiiren painiketta pitkään raportin esikatselussa ja siirrä sitten hiirtä.

- Ladata PDF-tiedosto tietokoneessa tai verkossa.
- Tulosta

## <a name="saving-a-report"></a>Raportin tallentaminen
Voit tallentaa raportin PDF-tiedostona, Microsoft Word -asiakirjana tai Microsoft Excel -tiedostona valitsemalla **Lähetä kohteeseen** -painikkeen ja tekemällä valinnan.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Suoritettavan raportin aikatauluttaminen

Voit aikatauluttaa raportin tai erätyön ajon tietylle päivämäärälle ja kellonajalle. Aikataulutetut raportit ja erätyöt syötetään työjonoon ja käsitellään aikataulutettuna aikana vastaavasti kuin muut työt. **Aikataulu**-asetus valitaan sen jälkeen, kun **Lähetä kohteeseen** -painike on valittu, minkä jälkeen annetaan tiedot, kuten tulostin sekä päivämäärä ja kellonaika. Raportti lisätään tämän jälkeen työjonoon ja suoritetaan määritettynä ajankohtana. Kun raportti on käsitelty, kohde poistetaan työjonosta. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).  

Kun raportti aikataulutetaan suoritettavaksi, se voidaan määrittää suoritettavaksi joka torstai määrittämällä esimerkiksi **Seuraavan suorituspäivän kaava** -kentän arvoksi *D4*. Lisätietoja on kohdassa [Päivämäärän kaavojen käyttäminen](ui-enter-date-ranges.md#using-date-formulas).  

Voit tallentaa käsitellyn raportin tiedostoon, kuten Excel-, Word- tai PDF-tiedostoon, tulostaa sen valitulle tulostimelle tai vain käsitellä sen. Jos haluat tallentaa raportin tiedostoon, käsitelty raportti lähetetään roolikeskuksen **Saapuneet raportit** -alueelle, jossa voit tarkastella sitä.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Raportin tulostaminen

Tulosta raportti valitsemalla **Tulosta**-painikkeen raportin pyyntösivulla tai **Esikatselu**-sivun valikkorivillä.

### <a name="printer-selection"></a>Tulostimen valinta

Raportti tulostetaan tulostimelle, joka näkyy raportin pyyntösivun **Valittu tulostin** -kentässä. Tulostinta ei voi muuttaa tältä sivulta.

Valittu tulostin on joko määritetty **Tulostimen valinta** -sivulla tai se on **Tulostimen hallinta** -sivulla määritetty oletustulostin. Jos haluat käyttää toista tulostinta, lisätietoja on ohjeaiheessa [Tulostimien määrittäminen](ui-specify-printer-selection-reports.md).

Jos **Tulostinvalinnat** -sivulla ei ole määritetty tulostinta tai jos **Tulostimen hallinta** -sivulla ei ole määritetty oletustulostinta, käytössä on selaimen tulostustoiminto. Tässä tapauksessa **Selain** näkyy raporttipyyntösivun **Valittu tulostin** -kentässä. 

### <a name="browser-printing"></a>Selaimesta tulostaminen

Koska [!INCLUDE[prodshort](includes/prodshort.md)] on pilvipalvelu, se ei voi käyttää paikallisia tulostimia, jotka on yhdistetty tietokoneeseesi. Se voi kuitenkin muodostaa yhteyden pilvipalveluun yhteensopiviin tulostimiin. Sovelluksen [!INCLUDE[prodshort](includes/prodshort.md)] yleisessä versiossa pilvitulostin nimeltä **Sähköpostitulostin** asennetaan laajennuksena. Se on käyttövalmis alkuasetusten jälkeen.

Jos pilvitulostinta ei ole asennettu ja määritetty tai jos asennettu tulostin ei toimi kunnolla, tulostuksessa käytetään selaimen tulostusasetusten oletustulostinta.

> [!NOTE]
> Selaimen tulostusasetukset toimivat kohteesta [!INCLUDE[prodshort](includes/prodshort.md)] riippumatta. [!INCLUDE[prodshort](includes/prodshort.md)] -kohteen Tulostimet-kohdassa määritetyt tulostimen asetukset eivät siirry selaimen tulostusasetuksiin.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
### <a name="printing-reports-in-thai"></a>Thainkielisten raporttien tulostaminen
Koskien erityisesti [!INCLUDE[prodshort](includes/prodshort.md)]in Thaimaalaista versioita, **Tulosta** painike ei voi tulostaa raportteja oikein, johtuen tulostettavien PDF tiedostojen palvelun rajoituksista. Sen sijaan, raportin voi avata Wordilla, ja tallentaa sen tulostettavaan PDF muotoon.  

Vaihtoehtoisesti, voit pyytää järjestelmänvalvojaa luomaan Word-raporttipohjan käytetyimmille raporteillesi. Lisätietoja on kohdassa [Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Raporttiasetteluiden muuttaminen
Raportin asettelu määrittää, mitä raportissa näytetään, miten se on järjestetty ja mitä tyyliä siinä käytetään. Lisätietoja toiseen asetteluun vaihtamisesta on kohdassa [Nykyisen raporttiasettelun muuttaminen](ui-how-change-layout-currently-used-report.md). Jos puolestaan haluat mukauttaa omaa raporttiasettelua, lisätietoja on kohdassa [Mukautetun raporttiasettelun luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Katso myös

[Tulostimien määrittäminen](ui-specify-printer-selection-reports.md)  
[Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md)  
[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
