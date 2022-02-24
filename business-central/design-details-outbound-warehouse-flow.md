---
title: Rakennetiedot – Lähtevän fyysisen varastoinnin virta | Microsoft Docs
description: Varaston lähtevä virta alkaa kysynnällä liittyvistä lähdeasiakirjoista tuoda nimikkeet varastosijainnista, joko lähetettäviksi ulkoiselle osapuolelle tai yrityksen toiseen sijaintiin. Varastotoiminnot suoritetaan varastoalueelta erilaisilla monimutkaisuustasoilla nimikkeiden siirtämiseksi ulos toimituslaitureille.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/07/2020
ms.author: sgroespe
ms.openlocfilehash: 68fa5ebf2b35f0df821e0ef21ddeb286aa744408
ms.sourcegitcommit: 8b2f02dd5189c46ecff33c07223ed62b36842d34
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2020
ms.locfileid: "3542540"
---
# <a name="design-details-outbound-warehouse-flow"></a>Rakennetiedot: lähtevän fyysisen varastoinnin virta

Fyysisen varaston lähtevä virta alkaa liittyvien lähdeasiakirjojen pyynnöllä tuoda nimikkeet varastosijainnista lähetettäviksi joko ulkoiselle osapuolelle tai yrityksen toiseen sijaintiin. Varastotoiminnot suoritetaan varastoalueelta erilaisilla monimutkaisuustasoilla nimikkeiden siirtämiseksi ulos toimituslaitureille.  

 Jokainen nimike tunnistetaan ja kohdistetaan vastaavaan saapuvaan lähdeasiakirjaan. Seuraavat lähtevät lähdeasiakirjat on olemassa:  

- Myyntitilaus  
- Lähtevä siirtotilaus  
- Ostopalautustilaus  
- Huoltotilaus  

Lisäksi olemassa on seuraavat sisäiset lähdeasiakirjat, jotka toimivat kuten lähtevät lähteet:  

- Tuotantotilaus komponenttitarpeella  
- Kokoonpanotilaus komponenttitarpeella  

 Viimeiset kaksi asiakirjaa edustavat varastosta lähteviä virtoja sisäisille toiminta-alueille. Katso lisätietoja sisäisten saapuvien ja lähtevien prosessien fyysisen varaston käsittelystä kohdasta [Rakennetiedot: sisäisen fyysisen varastoinnin virta](design-details-internal-warehouse-flows.md).  

 Lähtevien fyysisen varastoinnin virtojen prosessit ja käyttöliittymän asiakirjat ovat erilaisia fyysisen varastoinnin perusmäärityksissä ja laajennetuissa varastomäärityksissä. Pääero on, että toiminnot suoritetaan fyysisen varastoinnin perusmäärityksissä tilauskohtaisesti, kun taas laajennetuissa varastomäärityksissä tilaukset konsolidoidaan useiksi tilauksiksi. Lisätietoja varastojen monimutkaisuustasoista on kohdassa [Rakennetiedot: Fyysisen varaston yleiskuvaus](design-details-warehouse-setup.md).  

 [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa noudon ja toimituksen lähtevät prosessit voidaan suorittaa neljällä tavalla käyttämällä eri toimintoja varastotason monimutkaisuudesta riippuen.  

|Tapa|Lähtevien käsittely|Varastopaikat|Poiminnat|Toimitukset|Monimutkaisuustaso (katso [Rakennetiedot: Fyysisen varaston asetukset](design-details-warehouse-setup.md))|  
|------|----------------|----|-----|---------|-------------------------------------------------------------------------------------|  
|L|Kirjaa poiminta ja lähetys tilausrivistä|X|||2|  
|B|Poiminnan ja toimituksen kirjaaminen varaston poiminta-asiakirjasta||X||3|  
|N|Kirjaa poiminta ja lähetyksen fyysisen varastoinnin toimituksen asiakirjasta|||X|4/5/6|  
|P|Poiminnan kirjaaminen fyysisen varastoinnin poiminta-asiakirjasta ja toimituksen kirjaaminen fyysisen varastoinnin toimituksen asiakirjasta||X|X|4/5/6|  

 Lähestymistavan valinta riippuu yrityksen hyväksytyistä käytänteistä ja niiden organisatorisen monimutkaisuuden tasosta. Menetelmän A käyttäminen, eli poiminta ja toimitus tilausriviltä on sopivaa yksinkertaisilla prosesseilla toimivassa tilauskohtaisessa ympäristössä, jossa käytetään yksinkertaista varastopaikkarakennetta. Muissa tilauskohtaisissa yrityksissä, joissa yhden tilausrivin nimikkeet saattavat saapua useammasta kuin yhdestä varastopaikasta tai jos varastotyöntekijät eivät voi työskennellä tilausasiakirjojen kanssa, erillisten poiminta-asiakirjojen käyttö on tarkoituksenmukaista, menetelmä B. Kun yrityksen poiminta- ja toimitusprosessit sisältävät useita tilauksen käsittelyjä ja vaativat täten suurempaa hallintaa ja yleiskuvaa, yritys saattaa valita varaston toimitusasiakirjan ja varaston poiminta-asiakirjan käytön poiminta ja toimitustöiden erottamiseksi, menetelmät C ja D.  

 Menetelmissä A, B ja C poiminnan ja toimituksen toiminnot yhdistetään yhteen vaiheeseen, kun vastaava asiakirja kirjataan toimitetuksi. Menetelmässä D poiminta rekisteröidään ensin ja sitten toimitus kirjataan myöhemmin eri asiakirjasta.  

## <a name="basic-warehouse-configurations"></a>Fyysisen varastoinnin perusmääritykset

 Seuraavassa kaaviossa kuvataan lähtevät fyysisen varaston virrat asiakirjatyypeittäin fyysisen varastoinnin perusmäärityksissä. Kaavion luvut vastaavat vaiheita kaavion osa-alueiden mukaan.  

 ![Lähtevä työnkulku fyysisen varastoinnin perusmäärityksissä](media/design_details_warehouse_management_outbound_basic_flow.png "Lähtevä työnkulku fyysisen varastoinnin perusmäärityksissä")  

### <a name="1-release-source-document--create-inventory-pick-or-movement"></a>1: Vapauta lähdeasiakirja / Luo varastopoiminta tai siirto

 Kun lähdeasiakirjoista vastaava käyttäjä, kuten myyntitilausten käsittelijä tai tuotannon suunnittelija, on valmis lähtevää fyysisen varastoinnin toimintoa varten, hän vapauttaa lähdeasiakirjan osoittaakseen varastotyöntekijöille, että myydyt nimikkeet tai osat voidaan poimia ja sijoittaa määritettyihin varastopaikkoihin. Vaihtoehtoisesti käyttäjä voi luoda varaston poiminta- tai siirtoasiakirjat yksittäisille tilausriveille push-muodossa ja tiettyihin lokeroihin ja käsittelymääriin perustuen.  

> [!NOTE]  
> Varastosiirtoja käytetään fyysisen varastoinnin perusmäärityksissä nimikkeiden siirtämiseen sisäisille toiminta-alueille lähdeasiakirjojen perusteella tai suunnittelematta.  

### <a name="2-create-outbound-request"></a>2: Luo lähtevä pyyntö

 Kun lähtevä lähdeasiakirja vapautetaan, fyysisen varastoinnin lähtevä pyyntö luodaan automaattisesti. Se sisältää viittauksia lähdeasiakirjan tyyppiin ja numeroon, eikä se ei näy käyttäjälle.  

### <a name="3-create-inventory-pick-or-movement"></a>3: Luo varastopoiminta tai siirto

 Varastotyöntekijä noutaa pull-muodossa **Varaston poiminta**- tai **Varaston siirto** -sivuilla odottavat lähdeasiakirjarivit, jotka perustuvat lähteviin fyysisen varastoinnin pyyntöihin. Vaihtoehtoisesti, varaston poiminnan rivit on jo luotu push-muodossa sen käyttäjän toimesta, joka on vastuussa lähdeasiakirjasta.  

### <a name="4-post-inventory-pick-or-register-inventory-movement"></a>4: Kirjaa varaston poiminta tai rekisteröi varastosiirto

 Kaikkien osittain tai kokonaan poimittujen tai siirrettyjen nimikkeiden rivin osalta varastotyöntekijä täyttää **Määrä**-kentän ja kirjaa sitten varaston poiminnan tai rekisteröi varastosiirron. Lähdeasiakirjat, jotka liittyvät varaston poimintaan, on tiliöity lähetettyinä tai käytettyinä. Lähdeasiakirjoja, jotka liittyvät varaston kehitykseen, ei ole lähetetty.  

 Varastopoiminnoille luodaan negatiiviset nimiketapahtumat, varastomerkinnät luodaan ja poimintapyyntö poistetaan, jos käsittely on suorittu loppuun. Esimerkiksi **Toimitettu määrä** -kenttä lähtevän lähdeasiakirjan rivillä päivitetään. Luodaan kirjatun toimituksen asiakirja, joka vastaa esimerkiksi myyntitilausta ja toimitettuja nimikkeitä.  

## <a name="advanced-warehouse-configurations"></a>Laajennetut varastomääritykset

 Seuraavassa kaaviossa kuvataan lähtevät fyysisen varaston virrat asiakirjatyypeittäin laajennetuissa varastomäärityksissä. Kaavion luvut vastaavat vaiheita kaavion osa-alueiden mukaan.  

 ![Lähtevä työnkulku fyysisen varastoinnin laajennetuissa määrityksissä](media/design_details_warehouse_management_outbound_advanced_flow.png "Lähtevä työnkulku fyysisen varastoinnin laajennetuissa määrityksissä")  

### <a name="1-release-source-document"></a>1: Vapauta lähdeasiakirja

 Kun lähdeasiakirjoista vastaava käyttäjä, kuten myyntitilausten käsittelijä tai tuotannon suunnittelija, on valmis lähtevää fyysisen varastoinnin toimintoa varten, hän vapauttaa lähdeasiakirjan osoittaakseen varastotyöntekijöille, että myydyt nimikkeet tai osat voidaan poimia ja sijoittaa määritettyihin varastopaikkoihin.  

### <a name="2-create-outbound-request-2"></a>2: Luo lähtevä pyyntö (2)

 Kun lähtevä lähdeasiakirja vapautetaan, fyysisen varastoinnin lähtevä pyyntö luodaan automaattisesti. Se sisältää viittauksia lähdeasiakirjan tyyppiin ja numeroon, eikä se ei näy käyttäjälle.  

### <a name="3-create-warehouse-shipment"></a>3: Luo fyysisen varaston toimitus

 Vastuussa oleva toimitustyöntekijä noutaa **F.var. toimitus** -sivulla odottavat lähdeasiakirjarivit, jotka perustuvat lähtevän fyysisen varastoinnin pyyntöön. Useita lähdeasiakirjan rivejä voidaan yhdistää yhdessä varaston lähetysasiakirjassa.  

### <a name="4-release-shipment--create-warehouse-pick"></a>4: Vapauta toimitus / luo varaston poiminta

 Toimituksesta vastaava työntekijä, vapauttaa varastotoimitukset niin, että varastotyöntekijät voivat luoda tai koordinoida varastopoiminnat kyseiseen toimitukseen.  

 Vaihtoehtoisesti käyttäjä voi luoda varaston poiminta-asiakirjan yksittäisille toimitusriveille push-muodossa ja tiettyihin lokeroihin ja käsittelymääriin perustuen.  

### <a name="5-release-internal-operation--create-warehouse-pick"></a>5: Vapauta sisäinen toiminto / luo varaston poiminta

 Sisäisistä toiminnoista vastaava käyttäjä vapauttaa sisäisen lähdeasiakirjan, kuten tuotanto- tai kokoonpanotilauksen. Tällöin varastotyöntekijät voivat luoda kyseiselle sisäiselle toiminnolle fyysisen varastoinnin poimintoja tai koordinoida niitä.  

 Vaihtoehtoisesti käyttäjä voi luoda varaston poiminta-asiakirjat yksittäiselle tuotannolle tai kokoonpanotilaukselle push-muodossa ja tiettyihin lokeroihin ja käsittelymääriin perustuen.  

### <a name="6-create-pick-request"></a>6: Luo poimintapyyntö

 Kun lähtevä lähdeasiakirja vapautetaan, fyysisen varastoinnin poimintapyyntö luodaan automaattisesti. Se sisältää viittauksia lähdeasiakirjan tyyppiin ja numeroon, eikä se ei näy käyttäjälle. Asetuksesta riippuen tuotanto- ja kokoonpanotilauksen kulutus luo myös poimintapyynnön tarvittavien komponenttien poimimiseksi varastosta.  

### <a name="7-generate-pick-worksheet-lines"></a>7: Luo poimintatyökirjan rivit

 Poimintojen koordinoinnista vastaava käyttäjä vastaanottaa fyysisen varastoinnin poimintarivit **Poimintatyökirja**-työkirjan avulla. Tämä perustuu poimintapyyntöihin, jotka saadaan fyysisen varastoinnin toimituksista tai sisäisten toimintojen poimintapyynnöistä, joilla on komponentin kulutusta. Käyttäjä valitsee poimittavat rivit ja valmistelee poiminnat määrittämällä varastopaikat, joista rivit otetaan ja jonne ne laitetaan, sekä käsiteltävien yksiköiden määrän. Binit voidaan määrittää etukäteen varaston sijainnin tai toiminnan resurssien määritysten avulla.  

 Käyttäjä määrittää keräysmenetelmät fyysisen varaston käsittelyä varten ja luo vastaavan fyysisen varastoinnin poiminta-asiakirjat. Ne liitetään fyysisen varastoinnin poiminnat suorittaville varastotyöntekijöille. Kun fyysisen varastoinnin poiminnat on kokonaan määritetty, **Poimintatyökirja**-kohteen rivit poistetaan.  

### <a name="8-create-warehouse-pick-documents"></a>8: Luo fyysisen varastoinnin poiminta-asiakirjat

 Poiminnan suorittava varastotyöntekijä luo fyysisen varastoinnin poiminta-asiakirjan vapautetun lähdeasiakirjan perusteella. Vaihtoehtoisesti fyysisen varastoinnin poiminta-asiakirja luodaan ja kohdistetaan varastotyöntekijään push-menetelmällä.  

### <a name="9-register-warehouse-pick"></a>9: Rekisteröi f. varastoinnin poiminta

 Kaikkien osittain tai kokonaan poimittujen nimikkeiden rivin osalta varastotyöntekijä täyttää **Määrä**-kentän **F.varastoinnin poiminta** -sivulla ja rekisteröi sitten fyysisen varaston poiminnan.  

 Fyysisen varastoinnin tapahtumat luodaan ja fyysisen varastoinnin poimintarivit poistetaan, jos ne käsitellään kokonaan. Fyysisen varastoinnin poiminta-asiakirja pysyy avoimena niin kauan, kunnes liittyvän fyysisen varastoinnin toimituksen koko määrä on rekisteröity. **Määrä poimittu**-kenttä varaston lähetysriveillä on päivitetty sen mukaisesti.  

### <a name="10-post-warehouse-shipment"></a>10: Kirjaa F.var. toimitusrivit

 Kun fyysisen varastoinnin toimitusasiakirjan kaikki nimikkeet on rekisteröity poimituiksi määritettyihin toimituksen varastopaikkoihin, vastuussa oleva toimitustyöntekijä kirjaa fyysisen varastoinnin toimituksen. Negatiiviset nimiketapahtumat luodaan. Esimerkiksi **Toimitettu määrä** -kenttä lähtevän lähdeasiakirjan rivillä päivitetään.  

## <a name="see-also"></a>Katso myös

[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
