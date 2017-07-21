---
title: ALV-viranomaisilmoitusten hallinta| Microsoft Docs
description: "Opi valmistelemaan raportti, jossa luetellaan myynneistä tiettynä kautena saatu arvonlisävero sekä lähettämään raportti veroviranomaiselle."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9b0db56fc08881a94b1f80bafed32d7bcbc24fd8
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---

# <a name="how-to-report-vat-to-tax-authorities"></a>ALV:n raportointi veroviranomaisille
Euroopan yhteisö (EY) -myyntiluetteloraportti sisältää luettelon arvonlisäveron (ALV) summista, jotka olet kerännyt myynneistä EU:n sisällä, jotta voit lähettää ALV-summat veroviranomaisen verkkopalveluun.

> [!NOTE]  
>   Isossa-Britanniassa kaikki yritykset, joiden vuosittainen myynti EU-jäsenvaltioissa sijaitseville asiakkaille ylittää tietyn summan, ovat velvoitettuja lähettämään sähköisen version Euroopan yhteisön (EY) -myyntiluetteloraportista XML-muodossa Britannian veroviranomaisen verkkosivun kautta.

EY-myyntiluetteloraportti toimii vain EU-maiden kohdalla. Se ei esimerkiksi sisällä arvonlisäveroa myynneistä Kiinan tai Yhdysvaltain kaltaisiin maihin.

Jotta voisit ilmoittaa arvonlisäveron viranomaiselle sähköisesti, [!INCLUDE[d365fin](includes/d365fin_md.md)] on yhdistettävä veroviranomaisen verkkopalveluun. Tämä edellyttää, että luot tilin ALV-viranomaisen kanssa. Kun sinulla on tili, voit ottaa käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tarjotun palveluyhteyden. Esimerkiksi Iso-Britanniassa voit käyttää **GovTalk**-palveluyhteyttä.

Raportti sisältää yhden rivin kullekin asiakastapahtumalle ja näyttää kokonaissumman tietyntyyppisille tapahtumille. Raportti voi sisältää kolmentyyppisiä tapahtumia:  
  
* B2B-tuotteet  
* B2B-palvelut  
* B2B-kolmikantakaupan tuotteet  
  
B2B-tuotteet ja palvelut määrittävät, onko myyty tavaraa vai palvelua, joita hallitsee **EU-palvelu** -asetus ALV-kirjausasetuksissa. B2B-kolmikantakaupan tuotteet ilmaisevat kaupankäyntiä kolmannen osapuolen kanssa, ja näitä hallitaan myyntiasiakirjojen, kuten myyntitilausten, laskujen ja hyvityslaskujen **EU-kolmikantakauppa**-asetuksella.  
  
Kun lähetät raportin, [!INCLUDE[d365fin](includes/d365fin_md.md)] valvoo palvelua ja pitää kirjaa yhteydenpidosta. **Tila**-kenttä ilmaisee raportin kulun prosessissa. Kun viranomainen on esimerkiksi käsitellyt raporttisi, sen tilaksi tulee **Onnistui**. Jos veroviranomaiselle lähetetyssä raportissa on virheitä, sen tilaksi muutetaan **Epäonnistui**. Voit tarkastella virheitä kohdassa **Virheet ja varoitukset**, korjata ne ja lähettää raportin uudelleen. Voit tarkastella luetteloa kaikista EY-myyntiluetteloraporteistasi **EU-myyntiluetteloraportit**-sivulla.  
  
> [!NOTE]  
>   Jos raportti lähetetään jollakin muulla tavalla, esimerkiksi viemällä se XML-tiedostoksi ja lataamalla sen veroviranomaisen verkkosivulle, raportointikauden voi sulkea sen jälkeen valitsemalla **Merkitse lähetetyksi**. Kun olet merkinnyt ALV-raportin vapautetuksi, siitä tulee ei muokattava. Jos raporttia on muutettava sen jälkeen, kun se on merkitty vapautetuksi, raportti on ensin avattava uudelleen. 
  
Kun veroviranomainen on tarkistanut raporttisi, yrityksesi yhteyshenkilö saa viranomaiselta sähköpostiviestin. [!INCLUDE[d365fin](includes/d365fin_md.md)]issa yhteyshenkilö määritetään **Yritystiedot**-sivulla. Ennen kuin lähetät raportin, varmista, että olet valinnut yhteyshenkilön.

<!--> [!NOTE]  
>   EY-myyntiluetteloraportti voi sisältää enintään 1000 riviä. Jos rivejä on enemmän, lähetä useampi raportti. -->

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Veroviranomaisen verkkopalveluun yhdistäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] tarjoaa palveluyhteydet, jotka yhdistävät veroviranomaisen sivustoihin. Esimerkiksi Iso-Britanniassa sinun on otettava käyttöön **GovTalk**-palveluyhteys.  

1. Kirjoita **Etsi sivuja tai raportteja** -kenttään **Palveluyhteydet** ja valitse sitten asiaankuuluva linkki. <!-- remember to get the updated text for this-->  
2. Täytä vaaditut kentät.  

## <a name="to-set-up-the-ec-sales-list-report"></a>EY-myyntiluetteloraportin määrittäminen
1. Kirjoita **Etsi sivuja tai raportteja** -kenttään **ALV-raportin asetukset** ja valitse sitten asiaankuuluva linkki.  
2. Jos haluat antaa käyttäjille mahdollisuuden muuttaa ja uudelleenlähettää näitä raportteja, valitse **Muokkaa lähetettyjä raportteja** -valintaruutu.  
3. Määritä EY-myyntiluetteloraporteissa käytettävä numerosarja.  

## <a name="to-prepare-and-submit-the-ec-sales-list-report"></a>EY-myyntiluetteloraportin valmistelu ja lähettäminen
1. Kirjoita **Etsi sivuja tai raportteja** -kenttään **EY-myyntiluetteloraportti** ja valitse sitten asiaankuuluva linkki.  
2. Valitse **Uusi** ja täytä sitten tarvittavat kentät.  
3. Voit luoda raportin sisällön **Ehdota rivejä** -toiminnolla.  

    > [!NOTE]  
>   Voit tarkastella rivin tapahtumia ennen kuin lähetät raportin. Valitse ensin rivi ja valitse sitten **Näytä ALV-tapahtumat**-toiminto.  
4. Kun haluat valmistella raportin lähettämistä varten, valitse **Vapauta**-toiminto.  
5. Raportin voit lähettää **Lähetä** -toiminnolla.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] vahvistaa, että raportti on määritetty oikein. Jos vahvistus epäonnistuu, virheet näkyvät **Virheet ja varoitukset** -ikkunassa niin, että voit tehdä tarvittavat muutokset.

## <a name="viewing-communications-with-your-tax-authority"></a>Veroviranomaisen ja yrityksen välisen viestintähistorian tarkastelu
Joissakin maissa tapahtuu viestinvaihtoa veroviranomaiselle raporttien lähettämisen yhteydessä. Näet ensimmäisen ja viimeisen lähettämäsi tai vastaanottamasi sanoman valitsemalla **Lataa lähetysviesti** ja **Lataa vastausviesti** -toiminnon.  

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

> [!NOTE]  
>   Kiinnitä huomiota raportin koodiyksiköitä luodessasi **ALV-raportin versio** -kentän arvoon. Tässä kentässä on oltava sama versio, joka on tai oli veroviranomaisen vaatimuksena. Voit esimerkiksi kirjoittaa kentän arvoksi **2017** osoittamaan, että raportti noudattaa kyseisenä vuonna voimassa olleita vaatimuksia. Voimassa olevan version saat selville veroviranomaiseltasi.  

## <a name="see-also"></a>Katso myös .
[Määritä ALV](finance-setup-vat.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Toimintaohje: Myynnin laskutus](sales-setup-sales.md)  

