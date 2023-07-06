---
title: Suorita ja tulosta raportteja
description: 'Tutustu, miten raportti lisätään työjonoon ja ajoitetaan käsiteltäväksi tiettynä päivänä ja tiettyyn kellonaikaan.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.search.form: null
ms.date: 09/09/2022
ms.author: jswymer
---
# <a name="run-and-print-reports"></a><a name="run-and-print-reports"></a><a name="run-and-print-reports"></a>Suorita ja tulosta raportteja

Raportti kerää tietoja määritettyjen ehtosarjojen perusteella. Se järjestää ja esittää tiedot helposti luettavassa muodossa, jonka voit tulostaa tai tallentaa tiedostona. Sovelluksen avulla voi käyttää monenlaisia raportteja. Raporteissa on yleensä avattuna olevan sivun sisältöön liittyviä tietoja. Esimerkiksi **Asiakas**-sivun raportit koskevat 10 suurinta asiakasta, myyntitilastoja ja niin edelleen.

> [!NOTE]
> Eräajot ja XMLportit toimivat käytännössä samalla tavoin kuin raportit, mutta niitä käytetään enemmän tietojen käsittelyyn tai vientiin. Esimerkiksi **Luo muistutukset** -erätyö luo muistutusasiakirjoja lähetettäviksi asiakkaille, joilla on erääntyneitä maksuja. Tässä artikkelissa viitataan pääsiassa raportteihin, mutta vastaavat tiedot koskevat myös erätöitä ja XMLporteja.

## <a name="get-started"></a><a name="get-started"></a><a name="get-started"></a>Aloittaminen

**Raportit**-valikon raportit löytyvät valituilta sivuilta sekä valituista luetteloista ja korteista. Halutessasi voit käyttää haussa ![Lamppu, joka avaa Kerro-ominaisuutta.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") , jos haluat etsiä raportteja nimen mukaan. Sovelluksen [!INCLUDE[prod_short](includes/prod_short.md)] luokan mukaan lajiteltujen käytettävissä olevien sisäisten raporttien yleiskuvaus on kohdassa [Käytettävissä olevat raportit kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md).

Kun valitset raportin, yleensä näkyviin tulee pyydetty sivu, jonka otsikkona on raportin nimi. Sivulla voit määrittää useita asetuksia ja suodattimia, jotka määrittävät sisällytettävät tiedot. Seuraavissa osissa kerrotaan, kuinka pyyntösivua käytetään raportin luomiseen, esikatseluun ja tulostamiseen.

## <a name="using-default-valuesmdashpredefined-settings"></a><a name="using-default-valuesmdashpredefined-settings"></a><a name="using-default-valuesmdashpredefined-settings"></a><a name="SavedSettings"></a>Oletusarvojen käyttäminen – ennalta määritetyt asetukset

Useimmat raportin pyyntösivut sisältävät **Käytä oletusarvoja** -kentän. Tämän kentän avulla voit valita raportille ennalta määritettyjä asetuksia, jotka automaattisesti määrittävät asetukset ja suodattimet. Valitse tapahtuma avattavasta luettelosta. Näet vaihtoehtojen ja suodattimien raportin pyyntösivulla muuttuvan vastaavasti.

**Viimeksi käytetyt asetukset ja suodattimet** -kirjaus on aina saatavilla. Tämä merkintä määrittää raportin käyttämään niitä asetuksia ja suodattimia, joita käytettiin, kun ajoit raportin edellisen kerran.

**Käytä oletusarvoja** -kentästä saadaan nopea ja luotettava tapa luoda raportteja, jotka sisältävät oikeat tiedot. Kun olet valinnut tapahtuman, voit muuttaa mitä tahansa vaihtoehtoa ja suodatinta ennen raportin esikatselua tai tulostamista. Tekemäsi muutokset eivät tallennu ennalta määritettyjen asetusten tapahtumaan, mutta ne tallennetaan **Viimeksi käytetyt asetukset ja suodattimet** -tapahtumaan.

> [!NOTE]
> Järjestelmänvalvoja määrittää ja hallinnoi tavallisesti esimääritettyjä asetuksia. Lisätietoja on kohdassa [Raporttien ja erätöiden tallennettujen asetusten hallinta](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-a-report"></a><a name="specifying-the-data-to-include-in-a-report"></a><a name="specifying-the-data-to-include-in-a-report"></a>Raportteihin sisällytettävien tietojen määrittäminen

Muuta tai rajoita raportin tietoja **Asetukset**- ja **Suodattimet**-kohdissa olevien kenttien avulla. Voit määrittää raportin suodattimet käytännössä samalla tavoin kuin luetteloiden suodattimet. Katso lisätietoja [Suodattaminen](ui-enter-criteria-filters.md#filtering)-osasta.

> [!CAUTION]
> Raportin pyyntösivun **Suodatus**-pikavälilehdessä on raporttien yleinen suodatustoiminto. Nämä suodattimet ovat valinnaisia.
>
> Osa raporteista ohittaa nämä suodattimet, joten raportin tulos sama riippumatta siitä, mikä suodatin on määritetty **Suodatin**-pikavälilehdessä. Eri raporteissa ohitettavista kentistä ei ole mahdollista luoda luetteloa, joten sinun on kokeiltava erilaisten suodattimien käyttöä.
>
> **Esimerkki**: kun käytät **Luo muistutukset** -erätyötä, **Viimeksi lähetetyn muist. taso** -kohdan **Asiakastapahtumat**-kenttä ohitetaan, koska kyseissä työssä käytetään kiinteitä suodattimia.

## <a name="previewing-a-report"></a><a name="previewing-a-report"></a><a name="previewing-a-report"></a>Raportin esikatselu

Raportin esikatselussa voit nähdä, miltä raportti näyttää ennen tulostamista. Esikatselu ei perustu pyyntösivun **Tulostin**-kentässä valittuun tulostimeen. Se on selaimen hallinnassa. Esikatselun jälkeen voit palata pyyntösivulle ja tehdä muutoksia asetuksiin ja suodattimiin tarpeen mukaan.

**Raportin pyyntösivun** esikatseluvalinnat riippuvat raportista. Joissakin raporteissa voit valita **Esikatsele**-vaihtoehdon. Joissakin raporteissa vaihtoehdon nimi on **Esikatsele ja sulje**. Molemmat vaihtoehdot avaavat raportin esikatselun. Erona on, että **Esikatselu** pitää pyyntösivun avoinna, joten voit palata siihen, tehdä muutoksia, esikatsella uudelleen tai tulostaa. Sen sijaan **Esikatsele ja sulje** -vaihtoehdossa pyyntösivu sulkeutuu. Raportti on avattava uudelleen, jotta voit tehdä muutoksia tai tulostaa.

> [!NOTE]
> Jos käytät Business Centralin vuoden 2020 1. julkaisuaaltoa tai sitä vanhempaa versiota, saatavilla on vain **Esikatsele**-painike, joka sulkee pyyntösivun esikatselussa, kuten **Esikatsele ja sulje** -toiminnossa yllä kuvatulla tavalla.

### <a name="work-with-the-preview"></a><a name="work-with-the-preview"></a><a name="work-with-the-preview"></a>Esikatselun käyttäminen

Raportin esiversion valikkorivin avulla voi:

- siirtyä sivuilla
- lähentää ja loitontaa
- muuttaa sivulle sopivaksi
- Valitse teksti

    Voit kopioida raportista tekstiä ja liittää sen toisaalle, kuten sovelluksen [!INCLUDE[prod_short](includes/prod_short.md)] sivulle tai Microsoft Wordiin. Esimerkiksi hiirtä käytettäessä painetaan hiiren ykköspainiketta ja pidetään sitä painettuna kohdassa, josta halutaan aloittaa. Liu'uta hiirtä valitaksesi vähintään yhden sanan, lauseen tai kappaleen. Paina sitten hiiren kakkospainiketta ja valitse **Kopioi**. Voit nyt liittää valitun tekstin haluamaasi kohtaan.
- Panoroi asiakirja

    Voit siirtää näkyvissä olevaa raportin aluetta kaikkiin suuntiin, joten saat näkyviin myös raportin muut alueet. Panorointi on kätevää, jos olet lähentänyt tekstiin yksityiskohtia tarkastelemaan. Paina esimerkiksi hiiren ykköspainiketta pitkään raportin esikatselussa ja valitse sitten raportin osa siirtämällä hiirtä.

- Ladata PDF-tiedosto tietokoneessa tai verkossa.
- Tulostus

## <a name="saving-a-report-to-a-file"></a><a name="saving-a-report-to-a-file"></a><a name="saving-a-report-to-a-file"></a>Raportin tallentaminen tiedostoon

Voit tallentaa raportin PDF-tiedostona, Microsoft Word -asiakirjana, Microsoft Excel -työkirjana tao XML-asiakirjana valitsemalla **Lähetä kohteeseen** -kohdan ja tekemällä valinnan. Tiedosto ladataan laitteellesi.

Jos organisaatio on määrittänyt OneDriven järjestelmän virheitä varten, lataamisen sijaan Excel-työkirjat ja Word-asiakirjat avataan selaimessa käyttämällä Exceliä tai Wordia verkossa.

> [!TIP]
> **Microsoft Excel -asiakirja (vain tiedot)**- ja **XML-asiakirja**-vaihtoehdot ovat enimmäkseen edistyneitä tarkoituksia varten. Näitä asetuksia käytetään tavallisesti yksityiskohtaisten tietojen analysoinnin tekemiseen. Lisätietoja on kohdassa [Raporttitietojen analysointi Excelillä ja XML:llä](report-analyze-excel.md).
>
> Voit myös käyttää **Microsoft Excel -asiakirja (vain tiedot)** -kohtaa, kun haluat luoda uusia Excelin asetteluita tietylle raportille. LIsätietoja on kohdassa [Excel-asetteluiden käyttäminen](ui-excel-report-layouts.md).  

## <a name="scheduling-a-report-to-run-later-or-periodically"></a><a name="scheduling-a-report-to-run-later-or-periodically"></a><a name="scheduling-a-report-to-run-later-or-periodically"></a><a name="ScheduleReport"></a> Raportin aikatauluttaminen suoritettavaksi myöhemmin tai säännöllisesti

Voit aikatauluttaa yksittäisen tai toistuvan raportin ajon tietylle päivämäärälle ja kellonajalle. Aikataulutetut raportit syötetään työjonoon ja käsitellään aikataulutettuna aikana vastaavasti kuin muut työt. Valitse **Aikataulu**-asetus sen jälkeen, kun **Lähetä kohteeseen** on valittu. Tämän jälkeen annetaan tiedot, kuten tulostin sekä päivämäärä ja kellonaika. Raportti lisätään tämän jälkeen työjonoon ja suoritetaan määritettynä ajankohtana. Kun raportti on käsitelty, kohde poistetaan työjonosta. Lue lisätietoja kohdasta [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).  

Kun raportti aikataulutetaan suoritettavaksi, se voidaan määrittää suoritettavaksi esimerkiksi joka torstai määrittämällä **Seuraavan suorituspäivän kaava** -kentän arvoksi *D4*. Lisätietoja on [Päivämäärän kaavojen käyttäminen](ui-enter-date-ranges.md#use-date-formulas) -osassa.  

Voit tallentaa raportin tiedostoon (kuten Excel-, Word- tai PDF-tiedostoon), tulostaa sen tai vain luoda raportin. Jos haluat tallentaa raportin tiedostoon, käsitelty raportti lähetetään roolikeskuksen **Saapuneet raportit** -sivulle, jossa voit tarkastella sitä. Lisätietoja on kohdassa [Raporttien jakaminen ja vieminen Saapuneet raportit -toiminnon avulla](ui-work-report-inbox.md)

### <a name="manage-scheduled-recurring-reports"></a><a name="manage-scheduled-recurring-reports"></a><a name="manage-scheduled-recurring-reports"></a>Aikataulutettujen toistuvien raporttien hallinta

Aikataulutetut raportit luodaan **Työjonon tapahtumat** -sivulla hallittujen erätöiden mukaan. Näet kunkin raportin tilan ja muut tiedot sivulla. Voit myös pysäyttää ja jatkaa raportin erätyötä sekä luoda raportin tarvittaessa.

**Työjonon tapahtumat** -sivulla voit myös muuttaa joitakin raportin parametreja, kuten tulostuksen tiedostotyyppiä, toistumista, suorituspäivämäärää sekä aloitus- ja lopetusaikoja. Ennen aiemmin luodun ajoitetun raportin muokkaamista täytyy kuitenkin asettaa raportin työjono estoon seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työjonon tapahtumat** ja valitse vastaava linkki.  
2. Valitse **Työjonon tapahtumat** -sivulla haluamasi raportti.
3. Valitse **Määritä pitoon** -toiminto.
4. Avaa aikataulutettu raportti ja muokkaa sitä valitsemalla sen tila (*Pidossa*).

Kun raportin asetusten muokkaaminen on tehty, toista kaksi ensimmäistä vaihetta ja valitse **Määritä tilaksi valmis** -toiminto jatkaaksesi raportin luomista.

Lisätietoja työjonojen hallinnasta on kohdassa [Työjonojen käyttäminen ajoitustehtäviin](admin-job-queues-schedule-tasks.md).  

## <a name="printing-a-report"></a><a name="printing-a-report"></a><a name="printing-a-report"></a><a name="PrintReport"></a>Raportin tulostaminen

Tulosta raportti, valitse **Tulosta** raportin pyyntösivulla tai **Esikatselu**-sivun valikkorivillä.

Kun raportti käyttää Excel-asettelua, et näe **Tulostin**-kenttää etkä **Tulosta**- ja **Esikatselu**-painiketta. Sen sijaan näkyvissä on **Lataus**-vaihtoehto. Jos haluat tulostaa, valitse **Lataa** ja avaa sitten ladattu tiedosto Excelissä ja tulosta sieltä.

### <a name="printer"></a><a name="printer"></a><a name="printer"></a><a name="Printer"></a>Tulostin

**Tulostin**-kentässä raportin pyyntösivulla näkyy, mille tulostimelle raportti tulostetaan. Tulostimen voi vaihtaa valitsemalla tulostimen luettelossa.

> [!NOTE]
> **(Selaimen käsittelemä)** -vaihtoehto ilmaisee, että raportille ei ole määritetty tulostinta. Tässä tapauksessa selain käsittelee tulosteen ja näyttää vakiotulostusvaiheet. Voit valita laitteeseesi yhdistetyn paikallisen tulostimen. **(Käsitellään selaimessa)** -vaihtoehto ei ole käytössä mobiilisovelluksessa [!INCLUDE[prod_short](includes/prod_short.md)] tai Microsoft Teamsin selaimessa.

> [!TIP]
> Oletustulostimeksi valittu tulostin määritetään **Tulostimen valinnat** -sivulla. Lisätietoja oletustulostimen muuttamisesta on [Oletustulostimien määrittäminen](ui-specify-printer-selection-reports.md#default) -osassa.

### <a name="printing-reports-in-thai"></a><a name="printing-reports-in-thai"></a><a name="printing-reports-in-thai"></a>Raporttien tulostaminen Thain kielelle

Koskien erityisesti [!INCLUDE[prod_short](includes/prod_short.md)]in Thaimaalaista versioita, **Tulosta** painike ei voi tulostaa raportteja oikein, johtuen tulostettavien PDF tiedostojen palvelun rajoituksista. Sen sijaan, raportin voi avata Wordilla, ja tallentaa sen tulostettavaan PDF muotoon.  

Voit myös pyytää järjestelmänvalvojaa luomaan Wordin raporttiasettelun käytetyimmille raporteillesi. Lisätietoja on kohdassa [Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md).  

## <a name="switching-the-report-layout"></a><a name="switching-the-report-layout"></a><a name="switching-the-report-layout"></a>Raportin asettelun vaihtaminen

Raportin asettelu määrittää, mitä raportissa näytetään, miten se on järjestetty ja mitä tyyliä siinä käytetään. Voit muuttaa asettelua seuraavilla tavoilla:

- Kun olet määrittämässä raportin suoritusta, pyyntösivulla on näkyvissä nykyinen asettelu **Raportin asettelu** -kentässä. Jos haluat vaihtaa väliaikaisesti eri asetteluun, valitse **Raportin asettelu** -kenttä ja valitse sitten asettelu tälle raportille käytettävissä olevien asettelujen luettelosta.
- Jos haluat muuttaa raportin käyttämää oletusasettelua, siirry **Raportin asettelut**- tai **Raportin asettelun valinta** -sivulle.

Lisätietoja on kohdassa [Raportin käyttämän asettelun määrittäminen](ui-set-report-layout.md). Jos puolestaan haluat mukauttaa omaa raporttiasettelua, siirry kohtaan [Aloita asettelujen luominen](ui-get-started-layouts.md).

## <a name="change-language-and-format-of-numbers-dates-and-times"></a><a name="change-language-and-format-of-numbers-dates-and-times"></a><a name="change-language-and-format-of-numbers-dates-and-times"></a>Numeroiden, päivämäärien ja kellonaikojen kielen ja muodon muuttaminen

Oletusarvon mukaan raportin numeroiden, päivämäärien ja kellonaikojen kieli ja muoto määräytyvät **Omat asetukset** -sivulla määritettyjen työkieli- ja alueasetusten mukaan. Voit kuitenkin muuttaa kieltä ja alueasetusta tapauskohtaisesti, kun esikatselet, tulostat tai lähetät raportin. Valitse pyyntösivulla **Lisäasetukset** ja määritä sitten haluamasi **Kieli** ja **Alueasetus**.

Lisätietoja **Omat asetukset** -sivusta on kohdassa [Muuta perusasetuksia](ui-change-basic-settings.md#region).

## <a name="advanced-options"></a><a name="advanced-options"></a><a name="advanced-options"></a>Lisäasetukset

Tulostimen resursseja hallitaan luodun raportin **Lisäasetukset**-pikavälilehden kentissä. Näitä asetuksia ei yleensä tarvitse muuttaa, ellei sinulla ole suurta raporttia. Jos raportti ylittää nämä rajoitukset ja yrität esikatsella tai tulostaa, näyttöön tulee sanoma, jossa kerrotaan, mikä rajoitus on ylitetty. Tämän jälkeen voit muuttaa asetuksia raportin mukaisiksi. Jokaisella kentällä on kuitenkin seuraavat maksimiarvot, josta sinun tulee olla tietoinen:

|Kenttä|Maksimiarvo|
|-----|-------------|
|Hahmonnuksen enimmäisaika|12:00:00|
|Rivien enimmäismäärä|1000000|
|Asiakirjojen enimmäismäärä|500|

> [!NOTE]
> Enimmäisarvot voivat olla erilaiset [!INCLUDE[prod_short](includes/prod_short.md)] paikallisesti, ja järjestelmänvalvoja voi muuttaa niitä. Lisätietoja on [Business Central Serverin määrittäminen - raportit](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports) -osassa. Yhteenveto raportin rajoituksista [!INCLUDE[prod_short](includes/prod_short.md)] onlinessa on kohdassa [Toimintarajat](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Katso [Microsoftin koulutukset](/training/paths/setup-reporting-dynamics-365-business-central/).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Käytettävissä olevat raportit kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Raporttien käyttö päivittäisessä työssä](reports-use-reports.md)  
[Business Intelligencen ja raportoinnin yleiskuva](reports-bi-reporting.md)  
[Tulostimien määrittäminen](ui-specify-printer-selection-reports.md)  
[Eräajojen ja XMLportien suorittaminen](ui-how-run-batch-jobs.md)  
[Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md)  
[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
[Taloudelliset liiketoimintatiedot](bi.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
