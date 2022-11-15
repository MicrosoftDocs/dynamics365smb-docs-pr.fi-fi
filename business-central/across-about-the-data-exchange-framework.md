---
title: Tietoja tiedonvaihto-kehyksestä
description: Tässä aiheessa kerrotaan, miten tiedonsiirtokehyksen avulla hallitaan yritysasiakirjojen, kuten laskujen, tiedonsiirtoa liikekumppaneiden kanssa.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Data exchange framework, data files, data exchange, electronic document, invoice, Business Central, business document, standard-compliant file, OCR
ms.search.form: 189,
ms.date: 06/10/2021
ms.author: edupont
ms.openlocfilehash: d5c8a96066311eb7e2050507b6c4f27066a70f62
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2022
ms.locfileid: "9744648"
---
# <a name="about-the-data-exchange-framework"></a>Tietoja tiedonvaihto-kehyksestä

Voit hallita liiketoiminta-asiakirjojen, pankkitiedostojen, vaihtokurssien ja muiden datatiedostojen siirtoa liikekumppaneille tai viranomaisille tiedonsiirtokehyksen avulla.

Järjestelmänvalvojana tai Microsoft-kumppanina voit käyttää kehystä uusissa integrointiominaisuuksissa määrittämällä, mitä tietoja vaihdetaan ja miten. Esimerkiksi pankkitiedostojen, sähköisten asiakirjojen, valuutanvaihtokurssien ja muiden ERP-järjestelmien tiedostonvaihtomuoto vaihtelee datatiedoston, virran ja maan tai alueen mukaan. [!INCLUDE[prod_short](includes/prod_short.md)] tukee erilaisia pankkitiedostomuotoja ja tietopalvelustandardeja. Käyttämällä tiedonsiirtokehystä voidaan tukea myös muita sähköisiä asiakirjamuotoja.

 Seuraavat kaaviot näyttävät tiedonsiirtokehyksen rakenteen.  

 ![Tiedonsiirtokehys &#45; Tuo.](media/across-data-exchange/dataexchangeframework_import.png)  

 ![Tiedonsiirtokehys &#45; Vie.](media/across-data-exchange/dataexchangeframework_export.png)  

## <a name="electronic-documents"></a>Sähköiset asiakirjat

Sähköpostin liitetiedostojen lähettämisen sijaan liiketoiminta-asiakirjoja voi lähettää ja vastaanottaa sähköisesti. Sähköisellä asiakirjalla tarkoitetaan sitä, että liiketoiminta-asiakirjaa (kuten toimittajan laskua) edustava standardinmukainen tiedosto voidaan vastaanottaa ja muuntaa ostolaskuksi [!INCLUDE[prod_short](includes/prod_short.md)]issa. Kauppakumppanit vaihtavat sähköisiä asiakirjoja ulkoisten asiakirjavaihtopalvelujen välityksellä. Oletusarvoisesti [!INCLUDE[prod_short](includes/prod_short.md)] tukee sähköisten laskujen ja hyvityslaskujen lähettämistä ja vastaanottamista PEPPOL-muodossa. Suurimmat asiakirjojen vaihtopalveluiden tarjoajat tukevat tätä muotoa. Document exchange -palveluiden merkittävä tarjoaja Tradeshift on esimääritetty, ja se on valmis määritettäväksi yrityksellesi. Tuen tarjoamiseen muissa sähköisen asiakirjan muodoissa, sinun on luotava uudet asiakirjojen vaihdon määritykset.  

Ulkoinen OCR (Optical Character Recognition) -palvelu voi luoda saapuvia asiakirjoja vastaavista PDF- tai kuvatiedostoista sähköisiä asiakirjoja, jotka voit sitten muuntaa tiedostotietueiksi [!INCLUDE[prod_short](includes/prod_short.md)]issa samalla tavalla kuin teet sähköisille PEPPOL-asiakirjoille. Kun esimerkiksi saat PDF-muotoisen laskun toimittajalta, voit lähettää sen OCR-palveluun **Saapuvat asiakirjat** -sivulta. Saat tiedoston muutamassa sekunnissa takaisin sähköisenä laskuna, jonka voit muuntaa toimittajan ostolaskuksi. Jos lähetät tiedoston OCR-palveluun sähköpostitse, uusi saapuvan asiakirjan tietue luodaan automaattisesti, kun saat sähköisen asiakirjan takaisin.  

Lähettääksesi esimerkiksi myyntilaskun sähköisenä PEPPOL-tiedostona voit valita **sähköisen asiakirjan** -vaihtoehdon **Kirjaa ja lähettää** valintaikkunassa. Tässä voit määrittää myös asiakkaan oletuslähettämisprofiilin. Aluksi on määritettävä joitakin perustietoja, kuten yrityksen tiedot, asiakkaat, nimikkeet ja mittayksiköt. Näitä käytetään liikekumppanien ja nimikkeiden tunnistamisessa, kun [!INCLUDE[prod_short](includes/prod_short.md)]in kentissä olevat tiedot muunnetaan lähtevän asiakirjatiedoston elementeiksi. PEPPOL-myyntilaskun tietojen muunnon ja lähetyksen hoitavat codeunitit ja XMLport-objektit (sähköisessä **PEPPOL**-asiakirjamuodossa).  

Jotta voisit vastaanottaa esimerkiksi laskun toimittajalta sähköisenä PEPPOL-asiakirjana, asiakirja on muunnettava **Saapuvat asiakirjat** -sivulla [!INCLUDE[prod_short](includes/prod_short.md)]in ostolaskuksi. Voit määrittää Työjono-ominaisuuden, joka käsittelee tiedostot määrätyin aikavälein, tai voit käynnistää prosessin manuaalisesti. Aluksi on määritettävä joitakin perustietoja, kuten yrityksen tiedot, toimittajat, nimikkeet ja mittayksiköt. Näitä käytetään liikekumppanien ja nimikkeiden tunnistamisessa, kun saapuvassa asiakirjatiedostossa olevien elementtien tiedot muunnetaan [!INCLUDE[prod_short](includes/prod_short.md)]in kentiksi. PEPPOL-laskujen vastaanottamisen ja tietojen muunnon suorittaa tietojen vaihtamiskehys (jota edustaa **PEPPOL – Lasku** -tietojenvaihtomääritys).  

  Saat esimerkiksi laskun sähköisenä OCR-tiedostona, kun käsittelet sitä kuin vastaanottaessasi sähköisen PEPPOL-asiakirjan. Sähköisten asiakirjojen vastaanottamisen ja tietojen muunnon OCR:stä suorittaa tietojen vaihtamiskehys (jota edustaa **OCR – Lasku** -tietojenvaihtomääritys).  

## <a name="bank-files"></a>Pankkitiedostot

Pankkitietojen vaihtamiseen tarkoitetut liiketoiminnan hallinnan sovellusten tiedostomuodot vaihtelevat tiedoston toimittajan sekä maan tai alueen mukaan. [!INCLUDE[prod_short](includes/prod_short.md)] tukee yhtenäisen euromaksualueen (SEPA) pankkitiedostojen tuontia ja vientiä. Lisäksi AMC Banking 365 Fundamentals -laajennuksen avulla voit liittää AMC Banking 365 Fundamentals -laajennuksen, jonka tarjoaa ulkopuolinen palveluntarjoaja AMC Consult. Lisätietoja on kohdassa [Maksujen suorittaminen AMC Banking 365 Fundamentals -laajennuksella tai SEPA-hyvityksen siirrolla](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md). Muiden sähköisten asiakirjojamuotojen tuki saadaan käyttämällä tietojen vaihtamiskehystä.  

Jos haluat viedä SEPA-tilisiirtoja, valitse **Maksupäiväkirja**-sivulla **Vie maksut tiedostoon** -painike ja lataa sitten tiedosto pankin käsiteltäväksi. Aluksi on määritettävä joitakin perustietoja, kuten pankkitili, toimittajat ja maksutavat. SEPA-pankkitietojen muunnon ja viennin suorittavat määritetty codeunit ja XMLport, joita edustaa **SEPA-tilisiirto** (pankin vienti-/tuontimääritys). Vaihtoehtoisesti voit määrittää, että AMC Banking 365 Fundamentalsin laajennus suorittaa viennin. Tätä vaihtoehtoa edustaa **AMC Banking 365 Fundamentalsin laajennus – tilisiirto** -tietojenvaihtomääritys.  

 Jos haluat viedä SEPA-suoraveloitusohjeita, valitse **Suoraveloitusperinnät**-sivulla **Vie suoraveloitustiedosto** -painike ja lähetä ohjeet pankillesi, joka kerää tarvittavat asiakasmaksut automaattisesti. Aluksi on määritettävä pankkitilit, asiakkaat, suoraveloitustoimeksiannot sekä maksutavat. SEPA-pankkitietojen muunnon ja viennin suorittavat määritetty codeunit ja XMLport, joita edustaa **SEPA-suoraveloitus** (pankin vienti-/tuontimääritys).  

 Jos haluat tuoda SEPA-tiliotteita, valitse Tuo tiliote -painike **Maksujen täsmäytyskirjauskansio**- ja **Pankkitilin täsmäytys** -sivuilla ja jatka viemällä tiliotemerkintä manuaalisesti tai automaattisesti maksuihin tai pankkitapahtumamerkintöihin. Aluksi on määritettävä pankkitilit. SEPA-pankkitietojen tuonnin ja muunnon suorittaa tietojen vaihtamiskehys (jota edustaa **SEPA CAMT** -tietojenvaihtomääritys). Vaihtoehtoisesti voit määrittää, että AMC Banking 365 Fundamentalsin laajennus suorittaa tuonnin. Tätä vaihtoehtoa edustaa **AMC Banking 365 Fundamentalsin laajennus – tiliote** -tietojenvaihtomääritys.  

 Lisäksi [!INCLUDE[prod_short](includes/prod_short.md)]in paikallinen versio tukee monia muita tiedostomuotoja, joiden avulla voidaan tuoda tai viedä pankkitietoja, palkanlaskentatapahtumia ja muita tietoja. Lisätietoja on ohjeaiheessa oman maasi/alueesi [Paikallisten toimintojen](about-localization.md) -aloitussivulla.  

## <a name="currency-exchange-rates"></a>Valuutan vaihtokurssit

Voit määrittää ulkoisen palvelun pitämään valuutan vaihtokurssit ajan tasalla. Päivitetyt valuuttakurssit määrittävä palvelu otetaan käyttöön tietojenvaihtomäärityksen avulla. Näin ollen **Valuutanvaihtokurssin päivitysasetusten kortti** -sivu on tiivistetty näkymä kyseessä olevan tiedonsiirtomäärityksen **Tiedonsiirtomääritys**-sivulta.  

Voit valmistella kaikille XML-tiedostojen tiedonsiirroille tiedonsiirtoasetukset lataamalla liittyvän XML-rakennetiedoston **XML-mallin tarkastelutoiminto** -sivulla. Voit valita ikkunassa tietoelementit, joita haluat vaihtaa [!INCLUDE[prod_short](includes/prod_short.md)]in kanssa. Tämän jälkeen voit joko käynnistää tiedonsiirtomäärityksen tai luoda XMLportin.

## <a name="intrastat"></a>Intrastat

[!INCLUDE[prod_short](includes/prod_short.md)] käyttää Intrastat-raportoinnin tiedonsiirtokehystä, jossa voit helposti luoda aikaleimattuja tiedostoja eri muodoissa vientiä varten. [!INCLUDE[prod_short](includes/prod_short.md)] sisältää valmiita muotoja lokalisoituja maita ja oletusversioita varten. Voit kuitenkin muuttaa valmista raporttia tai tehdä oman.

## <a name="see-also"></a>Katso myös

[Sähköinen tiedonsiirto](across-data-exchange.md)  
[XML-mallien käyttäminen tietojenvaihtomääritysten valmisteluun](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Tiedonsiirron määrittäminen](across-set-up-data-exchange.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
