---
title: "ALV-ilmoitusten lähettäminen veroviranomaisille| Microsoft Docs"
description: "Lisätietoja sellaisten ilmoitusten valmistelusta, joissa mainitaan myynnin tai myynnin ja ostojen arvonlisävero tiettynä kautena, ilmoituksen lähettämisestä veroviranomaisille."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c75b9eef5716379f6545494c20cbe6c7b34c1edd
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---

# <a name="how-to-report-vat-to-a-tax-authority"></a>Toimintaohje: ALV:n raportointi veroviranomaisille
Tässä ohjeaiheessa käsitellään [!INCLUDE[d365fin](includes/d365fin_md.md)]in raportteja, joilla voit lähettää myynnin ja ostojen arvolisäverosummia koskevat tiedot alueesi veronviranomaisille.

Käytössä on seuraavat raportit:

* **EU-myyntiluettelo** Euroopan unionin (EU:n) myyntiluettelo sisältää arvolisävero- eli ALV-summat, jotka olet kerännyt EU-maissa sijaitseville ALV-rekisteröidyille asiakkaille suuntautuneesta myynnistä.  
* **ALV-palautus**-raportti sisältää kaikissa sellaisissa maissa toimiville asiakkaille suuntautuneen myynnin ja ostojen ALV:n, joissa käytetään arvonlisäveroa.

Jos haluat tarkastella täydellistä ALV-tapahtumahistoriaa, jokainen ALV:n sisältävä kirjaus luo tapahtuman **ALV-tapahtumat**-ikkunassa. Näitä tapahtumia käytetään laskettaessa ALV-laskelmasi summaa (maksu tai palautus) tietyltä kaudelta. Jos haluat tarkastella ALV-tapahtumia, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-tapahtumat** ja valitse sitten liittyvä linkki.

## <a name="about-the-ec-sales-list-report"></a>Tietoja EU-myyntiluettelo-raportista
Isossa-Britanniassa kaikkien tavaroita ja palveluja ALV-rekisteröidyille asiakkaille, myös muiden EU-maiden asiakkaille, myyvien yritysten on lähetettävä EU-myyntiluettelo-raportin sähköinen versio XML-muodossa HMRC (Her Majesty's Revenue and Customs) -viraston sivuston kautta. EU-myyntiluettelo-raportti toimii vain EU-maiden kohdalla.

Raportti sisältää yhden rivin kullekin asiakastapahtumalle ja näyttää kokonaissumman tietyntyyppisille tapahtumille. Raportti voi sisältää kolmentyyppisiä tapahtumia:  

* B2B-tuotteet  
* B2B-palvelut  
* B2B-kolmikantakaupan tuotteet  

B2B-tuotteet ja -palvelut määrittävät, onko kyse myydystä tavarasta tai palvelusta, jota voi hallita ALV-kirjausasetusten **EU-palvelu**-asetuksella. B2B-kolmikantakaupan tuotteet ilmaisevat, onko kyse kaupankäynnistä kolmannen osapuolen kanssa, jolloin niitä voi hallita myyntiasiakirjojen, kuten myyntitilausten, laskujen ja hyvityslaskujen, **EU-kolmikantakauppa**-asetuksella.  

Kun veroviranomainen on tarkistanut raporttisi, yrityksesi yhteyshenkilö saa viranomaiselta sähköpostiviestin. [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa yhteyshenkilö määritetään **Yritystiedot**-ikkunassa. Ennen kuin lähetät raportin, varmista, että olet valinnut yhteyshenkilön.

## <a name="about-the-vat-return-report"></a>Tietoja ALV-palautusraportista
Voit lähettää tällä raportilla osto- ja myyntiasiakirjoissa olevan ALV:n. Näitä asiakirjoja ovat esimerkiksi osto- ja myyntitilaukset, laskut ja hyvityslaskut. Tiedot ovat raportissa samassa muodossa kuin tulli- ja veroviranomaisille tehtävässä yhteenvetoilmoituksessa.  

ALV lasketaan määritettyjen ALV-kirjausasetusten ja ALV-kirjausryhmien perusteella.

Tapahtumat voidaan määrittää sisältämään ALV-palautuksia varten seuraavat tiedot:

* Lähetä vain avoimet tapahtumat tai avoimet ja suljetut tapahtumat. Tämä on kätevää esimerkiksi silloin, kun valmistelet lopullista vuositason ALV-palautusta.
* Lähetä vain määritettyjen kausien tapahtumat tai sisällytä myös edellisten kausien tapahtumat. Tämä on kätevää päivitettäessä jo lähetettyä ALV-palautusta, jos esimerkiksi toimittaa lähettää laskun myöhässä.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Veroviranomaisen verkkopalveluun yhdistäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää palveluyhteyden veroviranomaisten sivustoihin. Jos toimit esimerkiksi Isossa-Britanniassa, voit ottaa käyttöön **GovTalk**-palveluyhteyden, jonka kautta voit lähettää EU-myyntiluettelo- ja ALV-palautus-raportit sähköisessä muodossa. Jos haluat lähettää raportin manuaalisesti antamalla tiedot esimerkiksi veronviranomaisten sivustossa, yhteyttä ei ole pakko ottaa käyttöön.   

Jotta voisit ilmoittaa arvonlisäveron viranomaiselle sähköisesti, [!INCLUDE[d365fin](includes/d365fin_md.md)] on yhdistettävä veroviranomaisen verkkopalveluun. Tämä edellyttää, että luot tilin ALV-viranomaisen kanssa. Kun sinulla on tili, voit ottaa käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tarjotun palveluyhteyden.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Palvelun yhteydet** ja valitse sitten soveltuva linkki.
2. Täytä vaaditut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >   Yhteyden toimivuus kannattaa testata. Sen voi tehdä valitsemalla **Testitila**-valintaruudun sekä valmistelemalla ja lähettämällä ALV-raportin kohdassa _ALV-raportin valmisteleminen ja lähettäminen_ kuvatulla tavalla. Palvelu testaa testitilassa, voiko veroviranomainen vastaanottaa raportin. Raportin tila ilmaisee, onnistuiko testilähetys vai ei. Muista kuitenkin, että tietoja ei ole vielä oikeasti lähetetty. Kun haluat lähettää raportin oikeasti, poista **Testitila**-valintaruudun valinta ja toista sitten lähetysprosessi.

## <a name="to-set-up-vat-reports-in-included365finincludesd365finmdmd"></a>ALV-raporttien määrittäminen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-raportin asetukset** ja valitse sitten liittyvä linkki.  
2. Jos haluat, että käyttäjät voivat muuttaa ja uudelleenlähettää näitä raportteja, valitse **Muokkaa lähetettyjä raportteja** -valintaruutu.  
3. Valitse kussakin raportissa käytettävä numerosarja.  

## <a name="to-prepare-and-submit-a-vat-report"></a>ALV-raportin valmisteleminen ja lähettäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **EU-myyntiluettelo** tai **ALV-palautus** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi** ja täytä sitten tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit luoda raportin sisällön **Ehdota rivejä** -toiminnolla.  

    > [!NOTE]  
    >   Voit tarkastella EU-myyntiluettelo-raportin riveillä olevia tapahtumia ennen raportin lähettämistä. Valitse ensin rivi ja valitse sitten **Näytä ALV-tapahtumat**-toiminto.  
4. Voit tarkistaa ja valmistella raportin lähetystä varten valitsemalla **Vapauta**-toiminnon.  

    > [!NOTE]  
    >   [!INCLUDE[d365fin](includes/d365fin_md.md)] vahvistaa, että raportti on määritetty oikein. Jos tarkistus epäonnistuu, virheet näkyvät **Virheet ja varoitukset** -kohdassa ja voit tehdä näiden tietojen perusteella tarvittavat korjaukset. Jos kyse on [!INCLUDE[d365fin](includes/d365fin_md.md)]in puuttuvasta asetuksesta, voit yleensä avata korjaukseen tarvittavat tiedot sisältävän sivun napsauttamalla sanomaa.  
5. Raportin voit lähettää **Lähetä** -toiminnolla.  

Kun lähetät raportin, [!INCLUDE[d365fin](includes/d365fin_md.md)] valvoo palvelua ja pitää kirjaa yhteydenpidosta. **Tila**-kenttä ilmaisee raportin kulun prosessissa. Kun viranomainen on esimerkiksi käsitellyt raporttisi, sen tilaksi tulee **Onnistui**. Jos veroviranomaiselle lähetetyssä raportissa on virheitä, sen tilaksi muutetaan **Epäonnistui**. Voit tarkastella virheitä **Virheet ja varoitukset** -kohdassa, korjata virheet ja lähettää raportin uudelleen. Voit tarkastella luetteloa kaikista EY-myyntiluetteloraporteistasi **EU-myyntiluetteloraportit**-ikkunassa.  

## <a name="viewing-communications-with-your-tax-authority"></a>Veroviranomaisen ja yrityksen välisen viestintähistorian tarkastelu
Joissakin maissa tapahtuu viestinvaihtoa veroviranomaiselle raporttien lähettämisen yhteydessä. Näet ensimmäisen ja viimeisen lähettämäsi tai vastaanottamasi sanoman valitsemalla **Lataa lähetysviesti** ja **Lataa vastausviesti** -toiminnon.  

## <a name="submitting-vat-reports-manually"></a>ALV-raporttien lähettäminen manuaalisesti
Jos raportti lähetetään jollakin muulla tavalla, esimerkiksi viemällä se XML-tiedostoksi ja lataamalla sen veroviranomaisen verkkosivulle, raportointikauden voi sulkea sen jälkeen valitsemalla **Merkitse lähetetyksi**. Kun olet merkinnyt ALV-raportin vapautetuksi, siitä tulee ei muokattava. Jos raporttia on muutettava sen jälkeen, kun se on merkitty vapautetuksi, raportti on ensin avattava uudelleen.

## <a name="vat-settlement"></a>ALV-laskelma
Netto-ALV on jaksoittain maksettava veroviranomaisille. Jos ALV on laskettava usein, voit suorittaa **Laske ja kirjaa ALV-laskelma** -eräajon, joka sulkee avoimet ALV-tapahtumat ja siirtää ostojen ja myynnin ALV-summat ALV-maksutilille.

Kun siirrät ALV-summat maksutilille, ostojen ALV-tilille hyvitetään ja myyntien ALV-tililtä veloitetaan ne summat, jotka on laskettu määritetylle ajalle. Nettosumma hyvitetään (tai veloitetaan, jos ostojen ALV-summa on suurempi) ALV-maksutilille. Voit kirjata maksun välittömästi tai tulostaa ensin testiraportin.  

> [!Note]
> Kun suoritat **Laske ja kirjaa ALV-laskelma** -eräajon mutta et määritä **Liiketoiminnan ALV-kirjausryhmä**- ja **Tuotteen ALV-kirjausryhmä** -asetuksia, kaikkien liiketoiminnan kirjausryhmien ja tuotteen kirjausryhmien koodien tapahtumat sisällytetään.

## <a name="configuring-your-own-vat-reports"></a>Omien ALV-raporttien määrittäminen
Voit käyttää EY-myyntiraporttiluetteloa sellaisenaan, mutta voit myös luoda omat raporttisi. Tämä edellyttää muutaman koodiyksiköt luomista. Ohjeita saat tarvittaessa Microsoft-kumppanilta.  

Seuraavassa taulukossa kuvataan koodiyksiköt, jotka sinun on luotava raporttiasi varten.

| Koodiyksikkö | Mitä raportin on tehtävä |
|----|-----|
|Ehdota rivejä| Hakea tiedot ALV-tapahtumat-taulukosta ja näytettävä ne riveinä ALV-raportilla.|
|Sisältö | Hallittava raportin muotoa. Onko raportti esimerkiksi XML- vai JSON-muotoinen. Muoto, jota käytetään riippuu veroviranomaisesi verkkopalvelun vaatimuksista. |
|Lähettäminen | Määrittää miten ja milloin ALV-raportti lähetetään veroviranomaisten vaatimusten mukaisesti. |
|Vastauksen käsittelijä | Veroviranomaisen vastauksen käsittely. Viranomainen voi esimerkiksi lähettää sähköpostin yrityksesi yhteyshenkilölle. |
|Peruuta | Aiemmin veroviranomaiselle lähetetyn ALV-raportin peruutussanoman lähettäminen. |  

> [!Note]
> Ota **ALV-raportin versio** -kentän arvo huomioon, kun luot raportin koodiyksiköt. Tässä kentässä on oltava sama versio, joka on tai oli veroviranomaisen vaatimuksena. Voit esimerkiksi kirjoittaa kentän arvoksi **2017** osoittamaan, että raportti noudattaa kyseisenä vuonna voimassa olleita vaatimuksia. Voimassa olevan version saat selville veroviranomaiseltasi.
 
## <a name="see-also"></a>Katso myös .
[Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen](finance-setup-vat.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Myynnin laskutus](sales-how-invoice-sales.md)  

