---
title: "Raportin suorituksen ajoittaminen tietylle päivämäärälle ja kellonajalle | Microsoft Docs"
description: "Tutustu, miten raportti lisätään työjonoon ja ajoitetaan käsiteltäväksi tiettynä päivänä ja tiettyyn kellonaikaan."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 07/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c1accaa517efa3fb9958316d2586b06fa8cadb80
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="working-with-reports"></a>Raporttien käsittely
Raportti kerää tietoja määritettyjen ehtojen perusteella. Tiedot järjestetään raporttiin helposti luettavassa ja tulostettavassa muodossa. Sovelluksesta voi käyttää monenlaisia raportteja. Raporteissa on yleensä avattuna olevan sivun sisältöön liittyviä tietoja. Esimerkiksi **Asiakas**-sivun raportit koskevat 10 suurinta asiakasta, myyntitilastoja jne.

Raportit sijaitsevat valittujen sivujen **Raportit**-välilehdellä. Voit myös etsiä raportteja nimen perusteella. Raportissa avautuu ensimmäisenä sivu, johon voi määrittää tietoja (vaihtoehtoja ja suodattimia). Raportin sisältö määrittyy näiden tietojen mukaan. Raportin mukaan voit määrittää esimerkiksi päivämäärävälin, tietyn tietueen, kuten asiakkaan, tai lajittelujärjestyksen. Esimerkki:

![Raporttiasetukset](media/report_options.png "Raporttiasetukset")

## <a name="previewing-a-report"></a>Raportin esikatselu
Voit avata raportin selaimeen katsottavaksi valitsemalla **Esikatselu**. Valikkorivi tulee näkyviin, kun osoitat jotakin kohtaa raportissa.  

![Raportin esikatselun työkalurivi](media/report_viewer.png "Raportin esikatselun työkalurivi")

Valikkorivin avulla voi

-   siirtyä sivuilla
-   lähentää ja loitontaa
-   muuttaa ikkunan koon sopivaksi
-   Valitse teksti

    Voit kopioida raportista tekstiä ja liittää sen toisaalle, kuten [!INCLUDE[d365fin](includes/d365fin_md.md)]in sivulle tai Microsoft Wordiin.  Aseta hiiri aloituskohtaan, pidä hiiren painike painettuna ja valitse sitten sanat, lauseet tai kappaleet hiirtä siirtämällä. Voit sitten painaa hiiren kakkospainiketta ja valita **Kopioi**. Voit liittää valitun tekstin valitsemaasi paikkaan.
-   Panoroi asiakirja

    Voit siirtää näkyvissä olevaa raportin aluetta kaikkiin suuntiin, joten saat näkyviin myös raportin muut alueet. Tämä on kätevää, jos olet lähentänyt tekstiin yksityiskohtia tarkastelemaan.  Paina esimerkiksi hiiren painiketta pitkään raportin esikatselussa ja siirrä sitten hiirtä.

-   Ladata PDF-tiedosto tietokoneessa tai verkossa.
-   Tulosta


## <a name="saving-a-report"></a>Raportin tallentaminen
Voit tallentaa raportin PDF-tiedostona, Microsoft Word -asiakirjana tai Microsoft Excel -tiedostona valitsemalla **Lähetä kohteeseen** ja tekemällä valinnan.

## <a name="ScheduleReport"></a> Suoritettavan raportin aikatauluttaminen
Voit aikatauluttaa raportin suorituksen tietylle päivämäärälle ja kellonajalle. Aikataulutetut raportit syötetään työjonoon ja käsitellään aikataulutettuna aikana vastaavasti kuin muut työt. Voit tallentaa käsitellyn raportin tiedostoon, kuten Excel-, Word- tai PDF-tiedostoon, tulostaa sen valitulle tulostimelle tai vain käsitellä sen. Jos haluat tallentaa raportin tiedostoon, käsitelty raportti lähetetään aloitussivun **Saapuneet raportit** -alueelle, jossa voit tarkastella sitä.

Voit aikatauluttaa raportin sen avaamisen yhteydessä. Valitse **Aikataulu**-toiminto ja anna tiedot, kuten tulostin, kellonaika ja päivämäärä. Raportti lisätään tämän jälkeen työjonoon ja suoritetaan määritettynä ajankohtana. Kun raportti on käsitelty, kohde poistetaan työjonosta. Jos tallensit käsitellyn raportin tiedostoon, se on käytettävissä **Saapuneet raportit** -alueella.

## <a name="PrintReport"></a>Raportin tulostaminen
Voit tulostaa raportin asetussivun **Tulosta**-painikkeella. Tämä sivu avautuu, kun avaat raportin. Se näkyy myös esikatselun valikkorivillä.

## <a name="using-saved-settings"></a>Tallennettujen asetusten käyttäminen
Raportin **Tallennetut asetukset** -ruudussa voi olla yksi merkintä tai useita merkintöjä. *Tallennetut asetukset* on periaatteessa valmis vaihtoehto- ja suodatinryhmä, jota voit käyttää raportteihin ennen raportin esikatselu tai sen lähettämistä tiedostoon. Tallennettujen asetusten käyttäminen on nopea ja helppo tapa oikeiden tietojen sisältämien raporttien luomista varten.

**Viimeksi käytetyt asetukset ja suodattimet** -kirjaus on aina saatavilla. Tämä merkintä määrittää raportin käyttämään niitä asetuksia ja suodattimia, joita käytettiin, kun katsoit raporttia edellisen kerran.

>[!NOTE]
>Järjestelmänvalvojana voit luoda ja hallita kaikkien käyttäjien raporttien tallennettuja asetuksia. Lisätietoja on kohdassa [Raporttien tallennettujen asetusten hallinta](reports-saving-reusing-settings.md).

## <a name="changing-the-layout-and-look-of-a-report"></a>Raportin asettelun ja ulkoasun muuttaminen
Raportin asettelu määrittää, mitä raportissa näytetään, miten se on järjestetty ja mitä tyyliä siinä käytetään. Lisätietoja toiseen asetteluun vaihtamisesta on kohdassa [Raportissa käytössä olevan asettelun muuttaminen](ui-how-change-layout-currently-used-report.md). Jos puolestaan haluat mukauttaa omaa raporttiasettelua, lisätietoja on kohdassa [Mukautetun raporttiasettelun luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Katso myös
[Tulostimen valinnan määrittäminen raporteille](ui-specify-printer-selection-reports.md)  
[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

