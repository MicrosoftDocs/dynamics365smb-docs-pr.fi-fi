---
title: ALV-ilmoitusten lähettäminen veroviranomaisille| Microsoft Docs
description: Lisätietoja sellaisten ilmoitusten valmistelusta, joissa mainitaan myynnin tai myynnin ja ostojen arvonlisävero tiettynä kautena, ilmoituksen lähettämisestä veroviranomaisille.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: caacf8eb62dd9539f050dbf55543dee862a6d7f8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779120"
---
# <a name="report-vat-to-tax-authorities"></a>ALV:n raportointi veroviranomaisille
Tässä ohjeaiheessa käsitellään [!INCLUDE[prod_short](includes/prod_short.md)]in raportteja, joilla voit lähettää myynnin ja ostojen arvolisäverosummia koskevat tiedot alueesi veronviranomaisille. 

Käytössä on seuraavat raportit:

* **EU-myyntiluettelo** Euroopan unionin (EU:n) myyntiluettelo sisältää arvolisävero- eli ALV-summat, jotka olet kerännyt EU-maissa sijaitseville ALV-rekisteröidyille asiakkaille suuntautuneesta myynnistä.  
* **ALV-palautus**-raportti sisältää kaikissa sellaisissa maissa toimiville asiakkaille suuntautuneen myynnin ja toimittajilta tehtyjen ostojen ALV:n, joissa käytetään arvonlisäveroa.

Jos haluat tarkastella täydellistä ALV-tapahtumahistoriaa, jokainen ALV:n sisältävä kirjaus luo tapahtuman **ALV-tapahtumat**-sivulla. Näitä tapahtumia käytetään laskettaessa ALV-laskelmasi summaa (maksu tai palautus) tietyltä kaudelta. Valitse ALV-tapahtumien katselemiseksi ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **ALV-tapahtumat** ja valitse sitten liittyvä linkki.

> [!NOTE]
> Jokaisen [!INCLUDE[prod_short](includes/prod_short.md)] -ympäristön on tarkoitus käsitellä yhden maan lakisääteinen raportointi. Esimerkiksi [!INCLUDE[prod_short](includes/prod_short.md)]in hollantilainen versio käsittelee vain Alankomaiden ALV-raportointia. Vastaavasti Yhdysvaltain [!INCLUDE[prod_short](includes/prod_short.md)]in versio käsittelee 1099-raportointia Yhdysvalloissa, eikä se tue ALV-raportointia muissa maissa ellei sitä ole tuotu kumppaniekosysteemin laajennuksella tai asiakaskohtaisella koodimuokkauksella.

## <a name="about-the-ec-sales-list-report"></a>Tietoja EU-myyntiluettelo-raportista
Isossa-Britanniassa kaikkien tavaroita ja palveluja ALV-rekisteröidyille asiakkaille, myös muiden EU-maiden asiakkaille, myyvien yritysten on lähetettävä EU-myyntiluettelo-raportin sähköinen versio XML-muodossa HMRC (Her Majesty's Revenue and Customs) -viraston sivuston kautta. EU-myyntiluettelo-raportti toimii vain EU-maiden kohdalla.

Raportti sisältää yhden rivin kullekin asiakastapahtumalle ja näyttää kokonaissumman tietyntyyppisille tapahtumille. Raportti voi sisältää kolmentyyppisiä tapahtumia:  

* B2B-tuotteet  
* B2B-palvelut  
* B2B-kolmikantakaupan tuotteet  

B2B-tuotteet ja -palvelut määrittävät, onko kyse myydystä tavarasta tai palvelusta, jota voi hallita ALV-kirjausasetusten **EU-palvelu**-asetuksella. B2B-kolmikantakaupan tuotteet ilmaisevat, onko kyse kaupankäynnistä kolmannen osapuolen kanssa, jolloin niitä voi hallita myyntiasiakirjojen, kuten myyntitilausten, laskujen ja hyvityslaskujen, **EU-kolmikantakauppa**-asetuksella.  

Kun veroviranomainen on tarkistanut raporttisi, yrityksesi yhteyshenkilö saa viranomaiselta sähköpostiviestin. [!INCLUDE[prod_short](includes/prod_short.md)]issa yhteyshenkilö määritetään **Yritystiedot**-sivulla. Ennen kuin lähetät raportin, varmista, että olet valinnut yhteyshenkilön.

## <a name="about-the-vat-return-report"></a>Tietoja ALV-palautusraportista
Voit lähettää tällä raportilla osto- ja myyntiasiakirjoissa olevan ALV:n. Näitä asiakirjoja ovat esimerkiksi osto- ja myyntitilaukset, laskut ja hyvityslaskut. Tiedot ovat raportissa samassa muodossa kuin tulli- ja veroviranomaisille tehtävässä yhteenvetoilmoituksessa.  

ALV lasketaan määritettyjen ALV-kirjausasetusten ja ALV-kirjausryhmien perusteella.

Tapahtumat voidaan määrittää sisältämään ALV-palautuksia varten seuraavat tiedot:

* Lähetä vain avoimet tapahtumat tai avoimet ja suljetut tapahtumat. Tämä on kätevää esimerkiksi silloin, kun valmistelet lopullista vuositason ALV-palautusta.
* Lähetä vain määritettyjen kausien tapahtumat tai sisällytä myös edellisten kausien tapahtumat. Tämä on kätevää päivitettäessä jo lähetettyä ALV-palautusta, jos esimerkiksi toimittaa lähettää laskun myöhässä.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Veroviranomaisen verkkopalveluun yhdistäminen
[!INCLUDE[prod_short](includes/prod_short.md)] sisältää palveluyhteyden veroviranomaisten sivustoihin. Jos toimit esimerkiksi Isossa-Britanniassa, voit ottaa käyttöön **GovTalk**-palveluyhteyden, jonka kautta voit lähettää EU-myyntiluettelo- ja ALV-palautus-raportit sähköisessä muodossa. Jos haluat lähettää raportin manuaalisesti antamalla tiedot esimerkiksi veronviranomaisten sivustossa, yhteyttä ei ole pakko ottaa käyttöön.   

Jotta voisit ilmoittaa arvonlisäveron viranomaiselle sähköisesti, [!INCLUDE[prod_short](includes/prod_short.md)] on yhdistettävä veroviranomaisen verkkopalveluun. Tämä edellyttää, että luot tilin ALV-viranomaisen kanssa. Kun sinulla on tili, voit ottaa käyttöön [!INCLUDE[prod_short](includes/prod_short.md)]issa tarjotun palveluyhteyden.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltoyhteydet** ja valitse sitten sopiva linkki.
2. Täytä vaaditut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > Yhteyden toimivuus kannattaa testata. Sen voi tehdä valitsemalla **Testitila**-valintaruudun sekä valmistelemalla ja lähettämällä ALV-raportin kohdassa _ALV-raportin valmisteleminen ja lähettäminen_ kuvatulla tavalla. Palvelu testaa testitilassa, voiko veroviranomainen vastaanottaa raportin. Raportin tila ilmaisee, onnistuiko testilähetys vai ei. Muista kuitenkin, että tietoja ei ole vielä oikeasti lähetetty. Kun haluat lähettää raportin oikeasti, poista **Testitila**-valintaruudun valinta ja toista sitten lähetysprosessi.

## <a name="to-set-up-vat-reports-in-prod_short"></a>ALV-raporttien määrittäminen [!INCLUDE[prod_short](includes/prod_short.md)]issa
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **VAT-raportoinnin asetukset** ja valitse sitten liittyvä linkki.  
2. Jos haluat, että käyttäjät voivat muuttaa ja uudelleenlähettää näitä raportteja, valitse **Muokkaa lähetettyjä raportteja** -valintaruutu.  
3. Valitse kussakin raportissa käytettävä numerosarja.  

## <a name="to-prepare-and-submit-a-vat-report"></a>ALV-raportin valmisteleminen ja lähettäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **EC-myyntiluettelo** tai **ALV-palautus** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi** ja täytä sitten tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit luoda raportin sisällön **Ehdota rivejä** -toiminnolla.  

    > [!NOTE]  
    >   Voit tarkastella EU-myyntiluettelo-raportin riveillä olevia tapahtumia ennen raportin lähettämistä. Valitse ensin rivi ja valitse sitten **Näytä ALV-tapahtumat**-toiminto.  
4. Voit tarkistaa ja valmistella raportin lähetystä varten valitsemalla **Vapauta**-toiminnon.  

    > [!NOTE]  
    > [!INCLUDE[prod_short](includes/prod_short.md)] vahvistaa, että raportti on määritetty oikein. Jos tarkistus epäonnistuu, virheet näkyvät **Virheet ja varoitukset** -kohdassa ja voit tehdä näiden tietojen perusteella tarvittavat korjaukset. Jos kyse on [!INCLUDE[prod_short](includes/prod_short.md)]in puuttuvasta asetuksesta, voit yleensä avata korjaukseen tarvittavat tiedot sisältävän sivun napsauttamalla sanomaa.  
5. Raportin voit lähettää **Lähetä** -toiminnolla.  

Kun lähetät raportin, [!INCLUDE[prod_short](includes/prod_short.md)] valvoo palvelua ja pitää kirjaa yhteydenpidosta. **Tila**-kenttä ilmaisee raportin kulun prosessissa. Kun viranomainen on esimerkiksi käsitellyt raporttisi, sen tilaksi tulee **Onnistui**. Jos veroviranomaiselle lähetetyssä raportissa on virheitä, sen tilaksi muutetaan **Epäonnistui**. Voit tarkastella virheitä **Virheet ja varoitukset** -kohdassa, korjata virheet ja lähettää raportin uudelleen. Voit tarkastella luetteloa kaikista EY-myyntiluetteloraporteistasi **EU-myyntiluetteloraportit**-sivulla.  

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
Voit käyttää EY-myyntiraporttiluetteloa sellaisenaan, mutta voit myös luoda omat raporttisi. Tämä edellyttää muutaman codeunitit luomista. Ohjeita saat tarvittaessa Microsoft-kumppanilta.  

Seuraavassa taulukossa kuvataan codeunitit, jotka sinun on luotava raporttiasi varten.

| Codeunit | Mitä raportin on tehtävä |
|----|-----|
|Ehdota rivejä| Hakea tiedot ALV-tapahtumat-taulukosta ja näytettävä ne riveinä ALV-raportilla.|
|Sisältö | Hallittava raportin muotoa. Onko raportti esimerkiksi XML- vai JSON-muotoinen. Muoto, jota käytetään riippuu veroviranomaisesi verkkopalvelun vaatimuksista. |
|Lähettäminen | Määrittää miten ja milloin ALV-raportti lähetetään veroviranomaisten vaatimusten mukaisesti. |
|Vastauksen käsittelijä | Veroviranomaisen vastauksen käsittely. Viranomainen voi esimerkiksi lähettää sähköpostin yrityksesi yhteyshenkilölle. |
|Peruuta | Aiemmin veroviranomaiselle lähetetyn ALV-raportin peruutussanoman lähettäminen. |  

> [!Note]
> Ota **ALV-raportin versio** -kentän arvo huomioon, kun luot raportin codeunitit. Tässä kentässä on oltava sama versio, joka on tai oli veroviranomaisen vaatimuksena. Voit esimerkiksi kirjoittaa kentän arvoksi **2017** osoittamaan, että raportti noudattaa kyseisenä vuonna voimassa olleita vaatimuksia. Voimassa olevan version saat selville veroviranomaiseltasi.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös
[Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen](finance-setup-vat.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Myynnin laskutus](sales-how-invoice-sales.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]