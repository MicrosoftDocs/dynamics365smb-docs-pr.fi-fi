---
title: Raportin suorituksen ajoittaminen tietylle päivämäärälle ja kellonajalle | Microsoft Docs
description: Tutustu, miten raportti lisätään työjonoon ja ajoitetaan käsiteltäväksi tiettynä päivänä ja tiettyyn kellonaikaan.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 65fcba3f0222b324f132115ea7f1ec53b75d983f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "921407"
---
# <a name="working-with-reports-and-batch-jobs"></a>Raporttien ja eräajojen käsitteleminen
Raportti kerää tietoja määritettyjen ehtojen perusteella. Tiedot järjestetään raporttiin helposti luettavassa ja tulostettavassa muodossa. Sovelluksesta voi käyttää monenlaisia raportteja. Raporteissa on yleensä avattuna olevan sivun sisältöön liittyviä tietoja. Esimerkiksi **Asiakas**-sivun raportit koskevat 10 suurinta asiakasta, myyntitilastoja jne.

Eräajot toimivat käytännössä samalla tavoin kuin raportit, mutta niiden tarkoitus on suorittaa prosessi. Esimerkiksi **Luo muistutukset** -erätyö luo muistutusasiakirjoja asiakkaille, joilla on erääntyneitä maksuja.  

> [!NOTE]
> Tässä ohjeaiheessa viitataan pääsiassa raportteihin, mutta vastaavat tiedot koskevat myös erätöitä.

Voit etsiä raportteja valittujen sivujen **Raportit**-välilehdessä tai käyttää ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") hakua, kun haluat etsiä raportteja nimen mukaan.


## <a name="specifying-the-data-to-include-in-the-report"></a>Raporttiin sisällytettävien tietojen määrittäminen
Raportissa avautuu ensimmäisenä sivu, johon voi tyypillisesti määrittää erilaisia vaihtoehtoja ja suodattimia. Raportin sisältö määrittyy näiden tietojen mukaan. Sivua kutsutaan raporttipyyntösivuksi. Raporttipyyntösivun avulla voit esimerkiksi luoda raportin tietylle asiakkaalle, tietylle aikavälille tai vaihtaa raportin tietojen järjestystä. Tässä on esimerkki raporttipyyntösivusta:

![Raporttiasetukset](media/report_options.png "Raporttiasetukset")

> [!Caution]
> Pyyntösivun **Näytä tulokset** -osassa on raporttien yleinen suodatustoiminto. Nämä suodattimet ovat valinnaisia.<br /><br /> Osa raporteista ohittaa nämä suodattimet, joten raportin tulos sama riippumatta siitä, mikä suodatin on määritetty **Näytä tulokset** -osassa. Eri raporteissa ohitettavista kentistä ei ole mahdollista luoda luetteloa, joten sinun on kokeiltava erilaisten suodattimien käyttöä.<br /><br />
**Esimerkki**: kun käytät **Luo muistutukset** -erätyötä, **Viimeksi lähetetyn muist. taso** -kohdan **Asiakastapahtumat**-kenttä ohitetaan, koska kyseissä työssä käytetään kiinteitä suodattimia.

### <a name="SavedSettings"></a>Tallennettujen asetusten käyttäminen
Joissakin raporteissa, riippuen siitä, kuinka ne on suunniteltu, raporttisivuun voi kuulua **Tallennetut asetukset** -osio, joka sisältää yhden tai useamman merkinnän **Käytä saatua oletusarvoa** -ruudussa. Tämän ruudun merkinnät ovat nimeltään *Tallennetut asetukset*. Tallennettu asetus on periaatteessa valmis vaihtoehto- ja suodatinryhmä, jota voit käyttää raportteihin ennen raportin esikatselu tai sen lähettämistä tiedostoon. **Viimeksi käytetyt asetukset ja suodattimet** -kirjaus on aina saatavilla. Tämä merkintä määrittää raportin käyttämään niitä asetuksia ja suodattimia, joita käytettiin, kun katsoit raporttia edellisen kerran.

Tallennettujen asetusten käyttäminen on nopea ja helppo tapa oikeiden tietojen sisältämien raporttien luomista varten. Kun olet määrittänyt **Käytä oletusarvoa** -ruutua tallennettujen asetusten merkintään, voit muuttaa asetuksia tai suodattimia ennen raportin esikatselua tai tallennusta. Tekemäsi muutokset eivät tallennu tallennettujen asetusten tapahtumaan, mutta ne tallennetaan kohtaan **Viimeksi käytetyt asetukset ja suodattimet**.

>[!NOTE]
>Mikäli olet järjestelmänvalvoja, voit luoda ja hallita kaikkien käyttäjien raporttien tallennettuja asetuksia. Lisätietoja on kohdassa [Raporttien tallennettujen asetusten hallinta](reports-saving-reusing-settings.md).

### <a name="setting-options-and-filters"></a>Asetusvaihtoehdot ja suodattimet
Jos haluat edelleen rajoittaa tai määritellä tarkasti tietoja, jotka sisältyvät raportin tietoihin, voit määrittää muita asetuksia tai suodattimia.

Suodattimet mahdollistavat tiettyihin kriteereihin perustuvan tiedon näyttämisen. Suodattimet on ryhmitelty sen entiteetin mukaan, johon ne kuuluvat, kuten **Asiakas** yllä olevassa kuvassa. Voit määrittää suodattimen määrittämällä **Missä**-ruudun kenttään, jonka haluat suodattaa ja lisäämällä ehtoja **on:** -ruutuun.

Voit lisätä suodattimia täyttämällä **Ja**- ja **on**-ruudut. Jos käytät useampaa kuin yhtä suodatinta, raporttiin sisällytetään vain tulokset, jotka täyttävät kaikkien suodattimien kriteerit.

Voit määrittää suodatusehdot etsimään täsmällistä vastaavuutta, osittaista vastaavuutta, arvoalueita ja muuta sen mukaan, mitä tyyppistä kenttää suodatat. Neuvoja suodattimien määrittämiseen löytyy ohjeaiheessa:
-   [Suodattaminen](ui-enter-criteria-filters.md#FilterCriteria)
-   [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md)

## <a name="previewing-a-report"></a>Raportin esikatselu
Voit avata raportin selaimeen katsottavaksi valitsemalla **Esikatselu**. Valikkorivi tulee näkyviin, kun osoitat jotakin kohtaa raportissa.  

![Raportin esikatselun työkalurivi](media/report_viewer.png "Raportin esikatselun työkalurivi")

Valikkorivin avulla voi

-   siirtyä sivuilla
-   lähentää ja loitontaa
-   muuttaa sivulle sopivaksi
-   Valitse teksti

    Voit kopioida raportista tekstiä ja liittää sen toisaalle, kuten [!INCLUDE[d365fin](includes/d365fin_md.md)]in sivulle tai Microsoft Wordiin.  Aseta hiiri aloituskohtaan, pidä hiiren painike painettuna ja valitse sitten sanat, lauseet tai kappaleet hiirtä siirtämällä. Voit sitten painaa hiiren kakkospainiketta ja valita **Kopioi**. Voit sitten liittää valitun tekstin valitsemaasi paikkaan.
-   Panoroi asiakirja

    Voit siirtää näkyvissä olevaa raportin aluetta kaikkiin suuntiin, joten saat näkyviin myös raportin muut alueet. Tämä on kätevää, jos olet lähentänyt tekstiin yksityiskohtia tarkastelemaan.  Paina esimerkiksi hiiren painiketta pitkään raportin esikatselussa ja siirrä sitten hiirtä.

-   Ladata PDF-tiedosto tietokoneessa tai verkossa.
-   Tulosta


## <a name="saving-a-report"></a>Raportin tallentaminen
Voit tallentaa raportin PDF-tiedostona, Microsoft Word -asiakirjana tai Microsoft Excel -tiedostona valitsemalla **Lähetä kohteeseen** ja tekemällä valinnan.

## <a name="ScheduleReport"></a> Suoritettavan raportin aikatauluttaminen
Voit aikatauluttaa raportin suorituksen tietylle päivämäärälle ja kellonajalle. Aikataulutetut raportit syötetään työjonoon ja käsitellään aikataulutettuna aikana vastaavasti kuin muut työt. Voit tallentaa käsitellyn raportin tiedostoon, kuten Excel-, Word- tai PDF-tiedostoon, tulostaa sen valitulle tulostimelle tai vain käsitellä sen. Jos haluat tallentaa raportin tiedostoon, käsitelty raportti lähetetään roolikeskuksen **Saapuneet raportit** -alueelle, jossa voit tarkastella sitä.

Voit aikatauluttaa raportin sen avaamisen yhteydessä. Valitse **Aikataulu**-toiminto ja anna tiedot, kuten tulostin, kellonaika ja päivämäärä. Raportti lisätään tämän jälkeen työjonoon ja suoritetaan määritettynä ajankohtana. Kun raportti on käsitelty, kohde poistetaan työjonosta. Jos tallensit käsitellyn raportin tiedostoon, se on käytettävissä **Saapuneet raportit** -alueella.

## <a name="PrintReport"></a>Raportin tulostaminen
Voit tulostaa raportin asetussivun **Tulosta**-painikkeella. Tämä sivu avautuu, kun avaat raportin. Se näkyy myös esikatselun valikkorivillä.

## <a name="changing-the-layout-and-look-of-a-report"></a>Raportin asettelun ja ulkoasun muuttaminen
Raportin asettelu määrittää, mitä raportissa näytetään, miten se on järjestetty ja mitä tyyliä siinä käytetään. Lisätietoja toiseen asetteluun vaihtamisesta on kohdassa [Raportissa käytössä olevan asettelun muuttaminen](ui-how-change-layout-currently-used-report.md). Jos puolestaan haluat mukauttaa omaa raporttiasettelua, lisätietoja on kohdassa [Mukautetun raporttiasettelun luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Katso myös
[Tulostimen valinnan määrittäminen raporteille](ui-specify-printer-selection-reports.md)  
[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
