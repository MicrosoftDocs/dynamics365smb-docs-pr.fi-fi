---
title: "Raportin suorituksen ajoittaminen tietylle päivämäärälle ja kellonajalle | Microsoft Docs"
description: "Tutustu, miten raportti lisätään työjonoon ja ajoitetaan käsiteltäväksi tiettynä päivänä ja tiettyyn kellonaikaan."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 07/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d0ef9148b082b05a46283f89c3cb98bb1cd0c6d0
ms.openlocfilehash: 560760b1f895ed69c2e7fd80ccf451763e87d19b
ms.contentlocale: fi-fi
ms.lasthandoff: 08/06/2018

---
# <a name="working-with-reports"></a>Raporttien käsittely
Raportti kerää tietoja määritettyjen ehtojen perusteella. Tiedot järjestetään raporttiin helposti luettavassa ja tulostettavassa muodossa. Sovelluksesta voi käyttää monenlaisia raportteja. Raporteissa on yleensä avattuna olevan sivun sisältöön liittyviä tietoja. Esimerkiksi **Asiakas**-sivun raportit koskevat 10 suurinta asiakasta, myyntitilastoja jne.

Voit etsiä raportteja **Raportteja** -välilehdeltä valituilta sivuilta tai voit käyttää hakua ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") etsiäksesi raportteja nimen perusteella.


## <a name="specifying-the-data-to-include-in-the-report"></a>Määrittää raporttiin sisällytettävät tiedot
Raportissa avautuu ensimmäisenä sivu, johon voi tyypillisesti määrittää erilaisia vaihtoehtoja ja suodattimia. Raportin sisältö määrittyy näiden tietojen mukaan. Sivua kutsutaan raporttipyyntösivuksi. Raporttipyyntösivun avulla voit esimerkiksi luoda raportin tietylle asiakkaalle, tietylle aikavälille tai vaihtaa raportin tietojen järjestystä. Tässä on esimerkki raporttipyyntösivusta:

![Raporttiasetukset](media/report_options.png "Raporttiasetukset")

### <a name="SavedSettings"></a>Tallennettujen asetusten käyttäminen
Joissakin raporteissa, riippuen siitä, kuinka ne on suunniteltu, raporttisivuun voi kuulua **Tallennetut asetukset** -osio, joka sisältää yhden tai useamman merkinnän **Käytä saatua oletusarvoa** -ruudussa. Tämän ruudun merkinnät ovat nimeltään *Tallennetut asetukset*. Tallennettu asetus on periaatteessa valmis vaihtoehto- ja suodatinryhmä, jota voit käyttää raportteihin ennen raportin esikatselu tai sen lähettämistä tiedostoon. **Viimeksi käytetyt asetukset ja suodattimet** -kirjaus on aina saatavilla. Tämä merkintä määrittää raportin käyttämään niitä asetuksia ja suodattimia, joita käytettiin, kun katsoit raporttia edellisen kerran.

Tallennettujen asetusten käyttäminen on nopea ja helppo tapa oikeiden tietojen sisältämien raporttien luomista varten. Kun olet määrittänyt **Käytä oletusarvoa** -ruutua tallennettujen asetusten merkintään, voit muuttaa asetuksia tai suodattimia ennen raportin esikatselua tai tallennusta. Tekemäsi muutokset eivät tallennu tallennettujen asetusten tapahtumaan, mutta ne tallennetaan kohtaan **Viimeksi käytetyt asetukset ja suodattimet**.

>[!NOTE]
>Mikäli olet järjestelmänvalvoja, voit luoda ja hallita kaikkien käyttäjien raporttien tallennettuja asetuksia. Lisätietoja on kohdassa [Raporttien tallennettujen asetusten hallinta](reports-saving-reusing-settings.md).

### <a name="setting-options-and-filters"></a>Asetusvaihtoehdot ja suodattimet
Jos haluat edelleen rajoittaa tai määritellä tarkasti tietoja, jotka sisältyvät raportin tietoihin, voit määrittää muita asetuksia tai suodattimia.

Suodattimet mahdollistavat tiettyihin kriteereihin perustuvan tiedon näyttämisen. Suodattimet on ryhmitelty sen entiteetin mukaan, johon ne kuuluvat, kuten **Asiakas** yllä olevassa kuvassa. Voit määrittää suodattimen määrittämällä **Missä**-ruudun kenttään, jonka haluat suodattaa ja lisäämällä ehtoja **on:** -ruutuun. Esimerkiksi yllä olevassa kuvassa on yksi suodatin, joka luo raportin asiakkaalle, jonka **nro** on yhtä kuin **01121212**.

Voit lisätä muita suodattimia asettamalla niitä **Lisää**-ruuduista. Jos käytät useampaa kuin yhtä suodatinta, raporttiin sisällytetään vain tulokset, jotka täyttävät kaikkien suodattimien kriteerit.

Voit määrittää suodatusehdot etsimään täsmällistä vastaavuutta, osittaista vastaavuutta, arvoalueita ja muuta sen mukaan, mitä tyyppistä kenttää suodatat. Neuvoja suodattimien määrittämiseen löytyy ohjeaiheessa:
-   [Suodattaminen](ui-enter-criteria-filters.md#FilterCriteria)
-   [Päivämääräalueiden syöttäminen](ui-enter-date-ranges.md)

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

