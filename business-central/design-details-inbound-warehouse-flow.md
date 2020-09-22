---
title: Rakennetiedot – Saapuva fyysisen varastoinnin virta | Microsoft Docs
description: Varaston tuleva virta alkaa, kun nimikkeet saapuvat yrityksen sijainnin varastoon joko vastaanotettuina ulkoisista lähteistä tai toisesta yrityksen sijainnista. Työntekijä rekisteröi nimikkeet tavallisesti skannaamalla viivakoodin. Varastotoiminnot suoritetaan vastaanottavasta laiturista erilaisilla monimutkaisuustasoilla nimikkeiden siirtämiseksi varastointialueelle.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 7d893b810c85faaa297f7775cbf02c208fc67a2e
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787844"
---
# <a name="design-details-inbound-warehouse-flow"></a>Rakennetiedot: saapuvan fyysisen varastoinnin virta
Fyysiseen varastoon saapuva virta alkaa, kun nimikkeet saapuvat yrityksen sijainnin fyysiseen varastoon joko vastaanotettuina ulkoisista lähteistä tai toisesta yrityksen sijainnista. Työntekijä rekisteröi nimikkeet tavallisesti skannaamalla viivakoodin. Varastotoiminnot suoritetaan vastaanottavasta laiturista erilaisilla monimutkaisuustasoilla nimikkeiden siirtämiseksi varastointialueelle.  

 Jokainen nimike tunnistetaan ja kohdistetaan vastaavaan saapuvaan lähdeasiakirjaan. Seuraavat saapuvat lähdeasiakirjat on olemassa:  

- Ostotilaus  
- Tuleva siirtotilaus  
- Myyntipalautustilaus  

Lisäksi olemassa on seuraavat sisäiset lähdeasiakirjat, jotka toimivat kuten saapuvat lähteet:  

- Tuotantotilaus tuotoksen kirjauksella  
- Kokoonpanotilaus tuotoksen kirjauksella  

Viimeiset kaksi edustavat varastoon saapuvia virtoja sisäisiltä toiminta-alueilta. Katso lisätietoja sisäisten saapuvien ja lähtevien prosessien fyysisen varaston käsittelystä kohdasta [Rakennetiedot: sisäisen fyysisen varastoinnin virta](design-details-internal-warehouse-flows.md).  

Saapuvan fyysisen varastoinnin virtojen prosessit ja käyttöliittymän asiakirjat ovat erilaisia fyysisen varastoinnin perusmäärityksissä ja laajennetuissa varastomäärityksissä. Pääero on, että toiminnot suoritetaan fyysisen varastoinnin perusmäärityksissä tilauskohtaisesti, kun taas laajennetuissa varastomäärityksissä tilaukset konsolidoidaan useiksi tilauksiksi. Lisätietoja varastojen monimutkaisuustasoista on kohdassa [Rakennetiedot: Fyysisen varaston yleiskuvaus](design-details-warehouse-setup.md).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa vastaanoton ja hyllytyksen saapuvat prosessit voidaan suorittaa neljällä tavalla käyttämällä eri toimintoja varastotason monimutkaisuudesta riippuen.  

|Tapa|Saapuva prosessi|Varastopaikat|Vastaanotot|Hyllytykset|Monimutkaisuustaso (katso [Rakennetiedot: Fyysisen varaston asetukset](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|L|Kirjaa vastaanotto ja hyllytys tilausrivistä|X|||2|  
|B|Vastaanoton ja hyllytyksen kirjaaminen varaston hyllytysasiakirjasta|||X|3|  
|N|Kirjaa vastaanotto ja hyllytys fyysisen varastoinnin vastaanottoasiakirjasta||X||4/5/6|  
|P|Kirjaa vastaanotto fyysisen varastoinnin vastaanottoasiakirjasta ja kirjaa hyllytys varaston hyllytysasiakirjasta||X|X|4/5/6|  

Lähestymistavan valinta riippuu yrityksen hyväksytyistä käytänteistä ja niiden organisatorisen monimutkaisuuden tasosta. Tilauskohtaisessa varastoympäristössä, jossa suurin osa varaston työntekijöistä työskentelee suoraan tilausasiakirjojen kanssa yritys saattaa päättää menetelmän A käyttämisestä. Tilauskohtainen varasto, jonka hyllytysprosessi on monimutkaisempi tai varastoinnin toimintoja suorittaa omistautunut varastohenkilökunta, hyllytystoimintojen erittely tilausasiakirjasta, menetelmä B, saattaa olla parempi vaihtoehto. Lisäksi useiden tilausten käsittelyn suunnittelua käyttävien yritysten saattaa olla helpompi käyttää varaston vastaanottoasiakirjoja eli menetelmiä C ja D.  

Menetelmissä A, B ja C vastaanoton ja hyllytyksen toiminnot yhdistetään yhteen vaiheeseen, kun vastaavat asiakirjat kirjataan vastaanotetuiksi. Menetelmässä D vastaanotto kirjataan ensin, jolla hyväksytään varaston arvon nousu ja se, että nimikkeet ovat myytävissä. Tämän jälkeen varastotyöntekijä rekisteröi hyllytyksen, jonka jälkeen nimikkeet voidaan poimia.  

## <a name="basic-warehouse-configurations"></a>Fyysisen varastoinnin perusmääritykset  
Seuraavassa kaaviossa kuvataan saapuvat fyysisen varastoinnin virrat asiakirjatyypeittäin fyysisen varastoinnin perusmäärityksissä. Kaavion luvut vastaavat vaiheita kaavion osa-alueiden mukaan.  

![Saapuva työnkulku fyysisen varastoinnin perusmäärityksissä](media/design_details_warehouse_management_inbound_basic_flow.png "Saapuva työnkulku fyysisen varastoinnin perusmäärityksissä")  

### <a name="1-release-source-document--create-inventory-put-away"></a>1: Vapauta lähdeasiakirjasta / luo varaston hyllytys  
Kun nimikkeet vastaanotetaan fyysiseen varastointiin, lähdeasiakirjan vapautukset, kuten ostotilauksen tai lähtevän siirtotilauksen, vastaanottava käyttäjä tiedottaa varastotyöntekijöille, että vastaanotetut nimikkeet voidaan hyllyttää. Vaihtoehtoisesti käyttäjä voi luoda varaston hyllytysasiakirjat yksittäisille tilausriveille push-muodossa ja tiettyihin lokeroihin ja käsittelymääriin perustuen.  

### <a name="2-create-inbound-request"></a>2: Luo saapuva pyyntö  
Kun saapuva lähdeasiakirja vapautetaan, fyysisen varastoinnin saapuva pyyntö luodaan automaattisesti. Se sisältää viittauksia lähdeasiakirjan tyyppiin ja numeroon, eikä se ei näy käyttäjälle.  

### <a name="3-create-inventory-put-away"></a>3: Luo varaston hyllytys.  
Nimikkeiden vastaanottamisesta vastuussa oleva varastotyöntekijä noutaa pull-muodossa **Varastohyllytys**-sivulla odottavat lähdeasiakirjarivit, jotka perustuvat saapuviin fyysisen varastoinnin pyyntöihin. Vaihtoehtoisesti, varaston hyllytysrivit on jo luotu push-muodossa sen käyttäjän toimesta, joka on vastuussa lähdeasiakirjasta.  

### <a name="4-post-inventory-put-away"></a>4: Kirjaa Var. hyllytys  
Kaikkien osittain tai kokonaan hyllytettyjen nimikkeiden rivin osalta varastotyöntekijä täyttää **Määrä**-kentän ja kirjaa sitten varastohyllytyksen. Lähdeasiakirjat, jotka liittyvät varastopoistoon, on lähetetty vastaanotettuina.  

Positiiviset nimiketapahtumat luodaan, varastotapahtumat luodaan ja hyllytyspyyntö poistetaan, jos käsittely on suorittu loppuun. Esimerkiksi **Vastaanotettu määrä** -kenttä saapuvan lähdeasiakirjan rivillä päivitetään. Luodaan kirjatun vastaanoton asiakirja, joka vastaa esimerkiksi ostotilausta ja vastaanotettuja nimikkeitä.  

## <a name="advanced-warehouse-configurations"></a>Laajennetut varastomääritykset  
Seuraavassa kaaviossa kuvataan saapuva fyysisen varastoinnin virta asiakirjatyypeittäin laajennetuissa varastomäärityksissä. Kaavion luvut vastaavat vaiheita kaavion osa-alueiden mukaan.  

![Saapuva työnkulku fyysisen varastoinnin laajennetuissa määrityksissä](media/design_details_warehouse_management_inbound_advanced_flow.png "Saapuva työnkulku fyysisen varastoinnin laajennetuissa määrityksissä")  

### <a name="1-release-source-document"></a>1: Vapauta lähdeasiakirja  
Kun nimikkeet vastaanotetaan fyysiseen varastointiin, lähdeasiakirjan vapautukset, kuten ostotilauksen tai lähtevän siirtotilauksen, vastaanottava käyttäjä tiedottaa varastotyöntekijöille, että vastaanotetut nimikkeet voidaan hyllyttää.  

### <a name="2-create-inbound-request"></a>2: Luo saapuva pyyntö  
Kun saapuva lähdeasiakirja vapautetaan, fyysisen varastoinnin saapuva pyyntö luodaan automaattisesti. Se sisältää viittauksia lähdeasiakirjan tyyppiin ja numeroon, eikä se ei näy käyttäjälle.  

### <a name="3-create-warehouse-receipt"></a>3: Luo f. varastoinnin vastaanotto  
Nimikkeiden vastaanottamisesta vastuussa oleva käyttäjä noutaa **F. varastoinnin vastaanotto** -sivulla odottavat lähdeasiakirjarivit, jotka perustuvat saapuvaan fyysisen varastoinnin pyyntöön. Useita lähdeasiakirjan rivejä voidaan yhdistää yhdessä varaston kuittiasiakirjassa.  

Käyttäjä täyttää **Käsiteltävä määrä** -kentän ja valitsee tarvittaessa vastaanottavan alueen ja varastopaikan.  

### <a name="4-post-warehouse-receipt"></a>4: Kirjaa fyysisen varastoinnin vastaanotto.  
Käyttäjä kirjaa fyysisen varastoinnin vastaanoton. Positiiviset nimiketapahtumat luodaan. Esimerkiksi **Vastaanotettu määrä** -kenttä saapuvan lähdeasiakirjan rivillä päivitetään.  

### <a name="5-create-warehouse-internal-put-away"></a>5: Luo fyysisen varaston sisäinen hyllytys  
Sisäisten toimintojen hyllytyksistä vastaava käyttäjä luo fyysisen varastoinnin sisäisen hyllytyksen nimikkeille, jotka on hyllytettävä fyysisessä varastossa. Näitä ovat esimerkiksi tuotos tai kokoonpanon tuotos. Käyttäjä määrittää määrän, alueen ja varastopaikan, jonne nimikkeen hyllytetään esimerkiksi **Hae var.paikan sisältö** -toiminnon avulla. Käyttäjä vapauttaa fyysisen varastoinnin sisäisen hyllytyksen. Tämä luo saapuvan fyysisen varastoinnin pyynnön, jolloin tehtävä voidaan hakea fyysisen varaston hyllytysasiakirjoista tai hyllytystyökirjasta.  

### <a name="6-create-put-away-request"></a>6: Luo hyllytyspyyntö  
Kun lähtevä lähdeasiakirja kirjataan, fyysisen varastoinnin hyllytyspyyntö luodaan automaattisesti. Se sisältää viittauksia lähdeasiakirjan tyyppiin ja numeroon, eikä se ei näy käyttäjälle. Asetuksesta riippuen, tuotantotilauksen tuotos luo myös hyllytyspyynnön valmiiden nimikkeiden hyllyttämiseksi varastossa.  

### <a name="7-generate-put-away-worksheet-lines-optional"></a>7: Luo hyllytystyökirjan rivit (valinnainen)  
Hyllytyksistä vastaava käyttäjä vastaanottaa fyysisen varastoinnin hyllytysrivit **Hyllytystyökirja**-työkirjan avulla. Tämä perustuu kirjattuihin fyysisen varastoinnin vastaanottoihin tai sisäisiin toimintoihin, joilla on tuotos. Käyttäjä valitsee rivit, jotka hyllytetään, ja valmistelee hyllytykset määrittämällä varastopaikat, joista rivit otetaan ja jonne ne laitetaan, sekä käsiteltävien yksiköiden määrän. Binit voidaan määrittää etukäteen varaston sijainnin tai toiminnan resurssien määritysten avulla.  

Kun hyllytyksiä suunnitellaan ja ne määritetään varastotyöntekijöille, käyttäjä luo fyysisen varastoinnin hyllytysasiakirjat. Täysin määritetyt hyllytysrivit poistetaan **hyllytystyökirjasta**.  

> [!NOTE]  
>  Jos **Käytä hyllytystyökirjaa** -kenttää ei ole valittu sijaintikortissa, tällöin fyysisen varastoinnin hyllytysasiakirjat luodaan suoraan kirjattujen fyysisen varastoinnin vastaanottojen perusteella. Tässä tapauksessa vaihe 7 jää pois.  

### <a name="8-create-warehouse-put-away-document"></a>8: Luo fyysisen varaston hyllytysasiakirja  
Hyllytyksen suorittava varastotyöntekijä luo fyysisen varastoinnin hyllytysasiakirjan kirjatun fyysisen varastoinnin vastaanoton perusteella. Vaihtoehtoisesti fyysisen varastoinnin hyllytysasiakirja luodaan ja kohdistetaan varastotyöntekijään push-menetelmällä.  

### <a name="9-register-warehouse-put-away"></a>9: Rekisteröi F.var. hyllytysrivit  
Kaikkien osittain tai kokonaan hyllytettyjen nimikkeiden rivin osalta varastotyöntekijä täyttää **Määrä**-kentän **F.varastoinnin hyllytys** -sivulla ja rekisteröi sitten fyysisen varaston hyllytyksen.  

Fyysisen varastoinnin tapahtumat luodaan ja fyysisen varastoinnin hyllytysrivit poistetaan, jos ne käsitellään kokonaan. Fyysisen varastoinnin hyllytysasiakirja pysyy avoimena niin kauan, kunnes liittyvän kirjatun fyysisen varastoinnin vastaanoton koko määrä on rekisteröity. **Määrä hyllytetty** -kenttä varastokuitin tilausriveillä on päivitetty.  

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)
