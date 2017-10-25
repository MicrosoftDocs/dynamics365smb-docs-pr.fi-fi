---
title: "Dynamics 365 for Financialsin sähköiset asiakirjat | Microsoft Docs"
description: "Johdanto sähköisten asiakirjojen lähettämiseen ja vastaanottamiseen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: dac82da00a2f4afe16bc784641abea8f6a29c537
ms.contentlocale: fi-fi
ms.lasthandoff: 09/27/2017

---
# <a name="exchanging-data-electronically"></a>Sähköinen tiedonsiirto
Voit siirtää liiketoiminta-asiakirjoja, pankkitiedostoja, vaihtokursseja ja muita datatiedostoja liikekumppaneille tiedonsiirtokehyksen avulla.

## <a name="electronic-documents"></a>Sähköiset asiakirjat
Sähköpostin liitetiedostojen lähettämisen sijaan liiketoiminta-asiakirjoja voi lähettää ja vastaanottaa sähköisesti. Sähköisellä asiakirjalla tarkoitetaan sitä, että liiketoiminta-asiakirjaa (kuten toimittajan laskua) edustava standardinmukainen tiedosto voidaan vastaanottaa ja muuntaa ostolaskuksi [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Document exchange -palveluiden ulkoinen palveluntarjoaja suorittaa kahden liikekumppanin välisen sähköisten asiakirjojen vaihdon. [!INCLUDE[d365fin](includes/d365fin_md.md)]in yleinen versio tukee sähköisten laskujen ja hyvityslaskujen lähettämistä ja vastaanottamista PEPPOL-muodossa. Suurimmat asiakirjojen vaihtopalveluiden tarjoajat tukevat tätä muotoa. Tavallisin document exchange -palveluiden tarjoaja on esimääritetty, ja se on valmis määritettäväksi yrityksellesi. Tuen tarjoamiseen muissa sähköisen asiakirjan muodoissa, sinun on luotava uusi päivämäärän muutosmääritys Data Exchange -kehyksen avulla.  

Ulkoinen OCR (Optical Character Recognition) -palvelu voi luoda saapuvia asiakirjoja vastaavista PDF- tai kuvatiedostoista sähköisiä asiakirjoja, jotka voit sitten muuntaa tiedostotietueiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]issa samalla tavalla kuin teet sähköisille PEPPOL-asiakirjoille. Esimerkiksi kun saat PDF-muodossa laskun toimittajalta, voit lähettää sen OCR-palveluun **Saapuvat asiakirjat** -ikkunasta. Muutaman sekunnin kuluttua saat tiedoston takaisin sähköisenä laskuna, jonka voit muuntaa toimittajan ostolaskuksi. Jos lähetät tiedoston OCR-palveluun sähköpostitse, uusi saapuvan asiakirjan tietue luodaan automaattisesti, kun saat sähköisen asiakirjan takaisin.  

Lähettääksesi esimerkiksi myyntilaskun sähköisenä PEPPOL-tiedostona voit valita **sähköisen asiakirjan** -vaihtoehdon **Kirjaa ja lähettää** valintaikkunassa. Tässä voit määrittää myös asiakkaan oletuslähettämisprofiilin. Aluksi on määritettävä joitakin perustietoja, kuten yrityksen tiedot, asiakkaat, nimikkeet ja mittayksiköt. Näitä käytetään liikekumppanien ja nimikkeiden tunnistamisessa, kun [!INCLUDE[d365fin](includes/d365fin_md.md)]in kentissä olevat tiedot muunnetaan lähtevän asiakirjatiedoston elementeiksi. PEPPOL-myyntilaskun tietojen muunnon ja lähetyksen hoitavat koodiyksiköt ja XMLport-objektit (sähköisessä **PEPPOL**-asiakirjamuodossa).  

Jotta voisit vastaanottaa esimerkiksi laskun toimittajalta sähköisenä PEPPOL-asiakirjana, asiakirja on muunnettava **Saapuvat asiakirjat** -ikkunassa [!INCLUDE[d365fin](includes/d365fin_md.md)]in ostolaskuksi. Voit määrittää Työjono-ominaisuuden, joka käsittelee tiedostot määrätyin aikavälein, tai voit käynnistää prosessin manuaalisesti. Aluksi on määritettävä joitakin perustietoja, kuten yrityksen tiedot, toimittajat, nimikkeet ja mittayksiköt. Näitä käytetään liikekumppanien ja nimikkeiden tunnistamisessa, kun saapuvassa asiakirjatiedostossa olevien elementtien tiedot muunnetaan [!INCLUDE[d365fin](includes/d365fin_md.md)]in kentiksi. PEPPOL-laskujen vastaanottamisen ja tietojen muunnon suorittaa tietojen vaihtamiskehys (jota edustaa **PEPPOL – Lasku** -tietojenvaihtomääritys).  

 Saat esimerkiksi laskun sähköisenä OCR-tiedostona, kun käsittelet sitä kuin vastaanottaessasi sähköisen PEPPOL-asiakirjan. Sähköisten asiakirjojen vastaanottamisen ja tietojen muunnon OCR:stä suorittaa tietojen vaihtamiskehys (jota edustaa **OCR – Lasku** -tietojenvaihtomääritys).  

## <a name="bank-files"></a>Pankkitiedostot  
 Pankkitietojen vaihtoon tarkoitetut ERP-järjestelmien tiedostomuodot vaihtelevat tiedoston toimittajan sekä maan/alueen mukaan. [!INCLUDE[d365fin](includes/d365fin_md.md)]in yleinen versio tukee SEPA (Single Euro Payments Area) -pankkitiedostojen tuontia ja vientiä sekä ulkoisen palveluntarjoajan (AMC Consult) pankkitietojen muuntopalvelua. Muiden sähköisten asiakirjojamuotojen tuki saadaan käyttämällä tietojen vaihtamiskehystä.  

Jos haluat viedä SEPA-tilisiirtoja, valitse **Maksupäiväkirja**-ikkunassa **Vie maksut tiedostoon** -painike ja lataa sitten tiedosto pankin käsiteltäväksi. Aluksi on määritettävä joitakin perustietoja, kuten pankkitili, toimittajat ja maksutavat. SEPA-pankkitietojen muunnon ja viennin suorittavat määritetty koodiyksikkö ja XMLport-objekti, joita edustaa**SEPA-tilisiirto** (pankin vienti-/tuontimääritys). Vaihtoehtoisesti voit määrittää, että pankkitietojen muuntopalvelu suorittaa viennin. Tätä vaihtoehtoa edustaa **Pankkitietojen muuntopalvelu – tilisiirto** -tietojenvaihtomääritys.  

Jos haluat viedä SEPA-suoraveloitusohjeita, valitse **Suoraveloitusperinnät**-ikkunassa **Vie suoraveloitustiedosto** -painike ja lähetä ohjeet pankillesi, joka kerää tarvittavat asiakasmaksut automaattisesti. Aluksi on määritettävä pankkitilit, asiakkaat, suoraveloitustoimeksiannot sekä maksutavat. SEPA-pankkitietojen muunnon ja viennin suorittavat määritetty koodiyksikkö ja XMLport-objekti, joita edustaa**SEPA-suoraveloitus** (pankin vienti-/tuontimääritys).  

Jos haluat tuoda SEPA-tiliotteita, valitse Tuo tiliote -painike **Maksujen täsmäytyskirjauskansio**- ja **Pankkitilin täsmäytys** -ikkunoissa ja jatka viemällä tiliotemerkintä manuaalisesti tai automaattisesti maksuihin tai pankkitapahtumamerkintöihin. Aluksi on määritettävä pankkitilit. SEPA-pankkitietojen tuonnin ja muunnon suorittaa tietojen vaihtamiskehys (jota edustaa **SEPA CAMT** -tietojenvaihtomääritys). Vaihtoehtoisesti voit määrittää, että pankkitietojen muuntopalvelu suorittaa tuonnin. Tätä vaihtoehtoa edustaa **Pankkitietojen muuntopalvelu – tiliote** -tietojenvaihtomääritys.  

 Lisäksi [!INCLUDE[d365fin](includes/d365fin_md.md)]in paikallinen versio tukee monia muita tiedostomuotoja, joiden avulla voidaan tuoda tai viedä pankkitietoja, palkanlaskentatapahtumia ja muita tietoja. Lisätietoja on [!INCLUDE[d365fin](includes/d365fin_md.md)]in maaversion ohjeen Paikalliset toiminnot -osiossa.  

## <a name="currency-exchange-rates"></a>Valuutan vaihtokurssit  
Voit määrittää ulkoisen palvelun pitämään valuutan vaihtokurssit ajan tasalla. Päivitetyt valuuttakurssit määrittävä palvelu otetaan käyttöön tietojenvaihtomäärityksen avulla. Näin ollen **Valuutanvaihtokurssin päivitysasetusten kortti** -ikkuna on tiivistetty näkymä kyseessä olevan tiedonsiirtomäärityksen **Tiedonsiirtomääritys**-ikkunasta.  

Voit valmistella kaikille XML-tiedostojen tiedonsiirroille tiedonsiirtoasetukset lataamalla liittyvän XML-rakennetiedoston **XML-mallin tarkastelutoiminto** -ikkunassa. Voit valita ikkunassa tietoelementit, joita haluat vaihtaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in kanssa. Tämän jälkeen voit joko käynnistää tiedonsiirtomäärityksen tai luoda XMLport-objektin.  

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.  

|Vastaanottaja|Katso|  
|--------|---------|  
|Lue tietoja tiedonsiirtokehyksen toiminnasta.|[Tietoja tiedonvaihto-kehyksestä](across-about-the-data-exchange-framework.md)|  
|Valmistele tiedoston tietojen vaihto käyttämällä tiedoston XML-rakennetta. Määritä tietojenvaihtomääritykset. Määritä perustiedot sähköisten asiakirjojen lähettämistä varten. Määritä pankin tuonti- ja vientikentät.|[Tiedonsiirron määrittäminen](across-set-up-data-exchange.md)|  
|Lähetä PEPPOL-laskuja, vastaanota PEPPOL-laskuja, tuo tiliotteita ja vie pankin maksutiedostoja tietojenvaihtomääritysten mukaisesti.|[Tiedonsiirto](across-exchange-data.md)|  

## <a name="see-also"></a>Katso myös  
[Tietoja tiedonsiirtokehyksestä](across-about-the-data-exchange-framework.md)  
[Toimintaohje: XML-rakenteiden käyttäminen tiedonsiirtomääritysten valmistelussa](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Tiedonsiirron määrittäminen](across-set-up-data-exchange.md)  
[Tiedonsiirto](across-exchange-data.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

