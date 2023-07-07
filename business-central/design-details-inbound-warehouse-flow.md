---
title: Rakennetiedot – fyysisen varastoinnin saapuva virta
description: 'Fyysisen varastoinnin saapuva virta käynnistyy, kun nimikkeet saapuvat yrityksen fyysiseen varastoon sekä kun ne rekisteröidään ja täsmäytetään saapuvien lähdeasiakirjoihin.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/14/2022
ms.author: bholtorf
---
# <a name="design-details-inbound-warehouse-flow"></a>Rakennetiedot: saapuvan fyysisen varastoinnin virta

Varaston tuleva virta alkaa, kun nimikkeet saapuvat yrityksen sijainnin varastoon joko vastaanotettuina ulkoisista lähteistä tai toisesta yrityksen sijainnista. Saapuvien tilausten vastaanotossa on periaatteessa kaksi toimintaa:

* Nimikkeiden vastaanottaminen fyysisen varaston vastaanottolaiturilla, jossa nimikkeet tunnistetaan, jossa ne täsmäytetään lähdeasiakirjaan ja jossa vastaanotettu määrä kirjataan. 
* Nimikkeet hyllytetään varastoon ja hyllytyspaikka kirjataan.

Saapuvan fyysisen varastoinnin lähdeasiakirjat:

* Ostotilaukset  
* Saapuvat siirtotilaukset  
* Myyntipalautustilaukset  

> [!NOTE]
> Myös tuotannon ja kokoonpanon tulokset ovat saapuvien lähdeasiakirjoja. Lisätietoja sisäisten prosessien tuotannon ja kokoonpanon tuotosten käsittelemisestä on kohdassa [Rakennetiedot: fyysisen varaston sisäiset virrat](design-details-internal-warehouse-flows.md).  

[!INCLUDE[prod_short](includes/prod_short.md)]issa nimikkeiden vastaanottoon ja hyllytykseen on neljä tapaa, jotka käsitellään seuraavassa taulukossa.

|Tapa|Saapuva prosessi|Vaadi vastaanotot|Vaadi hyllytykset|Monimutkaisuustaso (lisätietoja on kohdassa [Varastoinninhallinnan yleiskatsaus](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Vastaanoton ja hyllytyksen kirjaaminen tilausriviltä|||Ei määritettyä fyysisen varaston toimintaa.|  
|B|Vastaanoton ja hyllytyksen kirjaaminen varaston hyllytysasiakirjasta||Otettu käyttöön|Perus: tilauksittain.|  
|S|Kirjaa vastaanotto ja hyllytys fyysisen varastoinnin vastaanottoasiakirjasta|Otettu käyttöön||Perus: useiden tilausten konsolidoitu vastaanoton ja toimituksen kirjaus.|  
|P|Kirjaa vastaanotto fyysisen varastoinnin vastaanottoasiakirjasta ja kirjaa hyllytys varaston hyllytysasiakirjasta|Otettu käyttöön|Otettu käyttöön|Lisäasetukset|  

Lähestymistavan valinta määräytyy yrityksen käytäntöjen ja organisaation monimutkaisuustason mukaan. Seuraavat esimerkiksi voivat auttaa päätöksenteossa.

* Tilauksittain toimivassa fyysisessä varastoympäristössä, jossa suurin osa varastohenkilökunnasta käsittelee tilausasiakirjoja suoraan, päätetään ehkä käyttää menetelmää A. 
* Jos tilauksittain toimivassa fyysisessä varastossa on käytössä monimutkainen hyllytysprosessi tai jos varastohenkilökunta erottelee hyllytystoiminnot tilausasiakirjasta, käyttöön kannattaa ehkä ottaa menetelmä B.
* Yrityksille, joiden on suunniteltava useiden tilausten käsittely, saattaa on hyödyllistä käyttää fyysisen varaston vastaanottoasiakirjoja eli menetelmiä C ja D.  

Menetelmissä A, B ja C vastaanotto ja hyllytys yhdistetään yhteen vaiheeseen, kun asiakirjat kirjataan vastaanotetuiksi. Menetelmässä D vastaanotto kirjataan ensin, ja tällä tavoin kirjataan varaston lisääntyminen ja nimikkeiden saatavuus myyntiin. Tämän jälkeen varastotyöntekijä rekisteröi hyllytyksen ja tuo näin nimikkeet poimittaviksi lähteviin tilaukseen. 

> [!NOTE]
> Vaikka fyysisen varaston hyllytykset ja varaston hyllytykset vaikuttavat samanlaisilta, ne ovat eri asiakirjoja ja niitä käytetään eri prosesseissa.
> * Menetelmässä B käytetty varaston hyllytys yhdessä hyllytystietojen rekisteröinnin kanssa kirjaa myös lähdeasiakirjan vastaanoton.
> * Menetelmässä D käytettyä fyysisen varaston hyllytystä ei vo kirjata, ja se vain rekisteröi hyllytyksen. Rekisteröinti tuo nimikkeet saataville lisäkäsittelyä varten, muttei kirjaa vastaanottoa. Saapuvassa virrassa fyysisen varaston edellyttää fyysisen varaston vastaanottoa.

## <a name="no-dedicated-warehouse-activity"></a>Ei määritettyä varastotoimintoa

Seuraavissa artikkeleissa on tietoja lähdeasiakirjojen vastaanottojen käsittelystä, jos varastotoimintoja ei ole määritetty.

* [Ostojen kirjaus](purchasing-how-record-purchases.md)
* [Siirtotilaukset](inventory-how-transfer-between-locations.md)
* [Myyntipalautustilausten käsittely](sales-how-process-sales-returns-orders.md)

## <a name="basic-warehouse-configurations"></a>Fyysisen varastoinnin perusmääritykset

Fyysisen varastoinnin perusmäärityksissä **Vaadi hyllytys** on otettu vaihtopainikkeella käyttöön sijainnin Sijaintikortti-sivulla mutta **Vaadi vastaanotto** ei ole.

Seuraavassa kaaviossa kuvataan saapuvat fyysisen varastoinnin virrat asiakirjatyypeittäin fyysisen varastoinnin perusmäärityksissä. Kaavion luvut vastaavat vaiheita kaavion osa-alueiden mukaan.  

:::image type="content" source="media/design_details_warehouse_management_inbound_basic_flow.png" alt-text="Fyysisen varaston saapuvien perusvirta":::

### <a name="1-release-a-source-document-to-create-a-request-for-an-inventory-put-away"></a>1: Varaston hyllytyspyynnön luominen vapauttamalla lähdeasiakirja

Nimikkeitä vastaanotettaessa lähdeasiakirja, kuten ostotilaus tai saapuva siirtotilaus, vapautetaan. Asiakirjan vapauttaminen mahdollistaa nimikkeiden hyllyttämisen. Varaston hyllytysasiakirjat voidaan luoda myös yksittäisille tilausriveille push-menetelmänä määritettyjen varastopaikkojen ja käsiteltävien määrien perusteella.  

### <a name="2-create-an-inventory-put-away"></a>2: Varaston hyllytyksen luominen

Saapuviin fyysisen varastoinnin pyyntöihin perustavat odottavat lähdeasiakirjan rivit voi hakea **Varastohyllytys**-sivulta pull-menetelmällä. Lisäksi lähdeasiakirjaa luotaessa varaston hyllytysrivejä voidaan luoda push-menetelmällä.  

### <a name="3-post-an-inventory-put-away"></a>3: Varaston hyllytyksen kirjaaminen

Kaikkien osittain tai kokonaan hyllytettyjen nimikkeiden rivin osalta täytetään **Määrä**-kenttä ja kirjataan sitten varastohyllytys. Lähdeasiakirjat, jotka liittyvät varastopoistoon, on lähetetty vastaanotettuina.  

* Positiiviset nimiketapahtumat luodaan.
* Fyysiset varastointitapahtumat luodaan sijainteihin, joissa on käytettävä varastopaikkakoodia kaikissa nimiketapahtumissa.
* Hyllytyspyyntö poistetaan, jos se on kokonaisuudessaan käsitelty. Esimerkiksi **Vastaanotettu määrä** -kenttä saapuvan lähdeasiakirjan rivillä päivitetään.
* Luodaan kirjatun vastaanoton asiakirja, joka vastaa esimerkiksi ostotilausta ja vastaanotettuja nimikkeitä.  

## <a name="advanced-warehouse-configurations"></a>Laajennetut varastomääritykset

Fyysisen varastoinnin laajennetuissa määrityksissä **Vaadi vastaanotto** on otettu vaihtopainikkeella käyttöön sijainnin Sijaintikortti-sivulla. **Vaadi hyllytys** -vaihtopainikkeen käyttö on valinnaista.

Seuraavassa kaaviossa havainnollistetaan fyysisen varastoinnin saapuva virta asiakirjatyypeittäin. Kaavion luvut vastaavat vaiheita kaavion osa-alueiden mukaan.  

:::image type="content" source="media/design_details_warehouse_management_inbound_advanced_flow.png" alt-text="Saapuva virta fyysisen varastoinnin laajennetuissa määrityksissä":::

### <a name="1-release-the-source-document"></a>1: Lähdeasiakirjan vapauttaminen

Nimikkeitä vastaanotettaessa lähdeasiakirja, kuten ostotilaus tai saapuva siirtotilaus, vapautetaan. Asiakirjan vapauttaminen mahdollistaa nimikkeiden hyllyttämisen. Hyllytys sisältää viittauksia lähdeasiakirjan tyyppiin ja numeroon.

### <a name="2-create-a-warehouse-receipt"></a>2: Fyysisen varastoinnin vastaanoton luominen

Saapuvan lähdeasiakirjan rivit haetaan **F. varastoinnin vastaanotto** -sivulla. Useita lähdeasiakirjan rivejä voidaan yhdistää yhdessä fyysisen varaston vastaanottoasiakirjassa. **Käsiteltävä määrä** -kenttä täytetään ja tarvittaessa valitaan vastaanottava alue ja varastopaikka.  

### <a name="3-post-the-warehouse-receipt"></a>3: Fyysisen varastoinnin vastaanoton kirjaaminen

Positiiviset nimiketapahtumat luodaan kirjaamalla fyysisen varastoinnin vastaanotto. **Vastaanotettu määrä** -kenttä päivitetään saapuvan lähdeasiakirjan rivillä.  

Jos **Vaadi hyllytys** ei ole otettu käyttöön vaihtopainikkeella sijaintikortissa, prosessi päättyy tähän. Muussa tapauksessa saapuvan lähdeasiakirjan kirjaaminen mahdollistaa nimikkeiden hyllyttämisen. Hyllytys sisältää viittauksia lähdeasiakirjan tyyppiin ja numeroon.  

### <a name="4-optional-generate-put-away-worksheet-lines"></a>4: (Valinnainen) Hyllytystyökirjan rivien luominen

Fyysisen varastoinnin hyllytysrivit haetaan **hyllytystyökirjassa** kirjattujen fyysisen varastoinnin vastaanottojen tai tuotoksen tuottavien työvaiheiden perusteella. Hyllytettävät nimikkeet valitaan ja seuraavat tiedot määritetään:

* Varastopaikat, joista nimikkeet otetaan.
* Varastopaikat, joihin nimikkeet asetetaan.
* Käsiteltävien yksiköiden määrä.

Varastopaikat voidaan määrittää etukäteen fyysisen varaston sijainnin tai työvaiheen suorittaneen resurssien määritysten avulla.  

Kun kaikki hyllytykset on suunniteltu ja määritetty varastotyöntekijöille, fyysisen varastoinnin hyllytysasiakirjat luodaan. Täysin määritetyt hyllytysrivit poistetaan **hyllytystyökirjasta**.  

> [!NOTE]  
> Jos **Käytä hyllytystyökirjaa** ei ole otettu vaihtopainikkeella käyttöön sijaintikortissa, fyysisen varastoinnin hyllytysasiakirjat luodaan suoraan kirjattujen fyysisen varastoinnin vastaanottojen perusteella. Siinä tapauksessa tätä vaihetta ei tarvita.  

### <a name="5-create-a-warehouse-put-away-document"></a>5: Fyysisen varastoinnin hyllytysasiakirjan luominen

Fyysisen varastoinnin hyllytysasiakirja voidaan luoda pull-menetelmällä kirjatun fyysisen varastoinnin vastaanoton perusteella. Fyysisen varastoinnin hyllytysasiakirja voidaan vaihtoehtoisesti luoda ja määrittää varastotyöntekijälle push-menetelmällä.  

### <a name="6-register-a-warehouse-put-away"></a>6: Fyysisten varaston hyllytyksen rekisteröinti

Kaikkien osittain tai kokonaan hyllytettyjen nimikkeiden rivin osalta täytetään **Määrä**-kenttä **F.varastoinnin hyllytys** -sivulla, jonka jälkeen rekisteröidään fyysisen varaston hyllytyksen.  

* Fyysiset varastointitapahtumat luodaan sijainteihin, joissa on käytettävä varastopaikkakoodia kaikissa nimiketapahtumissa.
* Fyysisen varaston hyllytysrivit poistetaan, jos ne on kokonaisuudessaan käsitelty.
* Fyysisen varastoinnin hyllytysasiakirja pysyy avoimena niin kauan, kunnes liittyvän kirjatun fyysisen varastoinnin vastaanoton koko määrä on rekisteröity.
* **Määrä hyllytetty** -kenttä päivitetään kirjatun fyysisen varaston vastaanoton tilausriveillä.

## <a name="related-tasks"></a>Liittyvät tehtävät

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Nimikkeiden vastaanotto kirjataan fyysisissä varastosijainneissa käyttämällä fyysisen varastoinnin vastaanottona, jos sijainnissa käytetään osittain tai kokonaan automatisoitua varastokäsittelyä.|[Nimikkeiden vastaanottaminen](warehouse-how-receive-items.md)|
|Nimikkeet hyllytetään tilauskohtaisesti ja vastaanotto kirjataan yhtenä toimintona fyysisen varastoinnin perusmäärityksissä.|[Nimikkeiden hyllyttäminen varastohyllytyksen avulla](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Useista ostoista, myyntipalautuksista tai siirtotilauksista vastaanotettujen nimikkeiden hyllyttäminen fyysisen varastoinnin laajennetuissa määrityksissä.|[Nimikkeiden hyllyttäminen ja fyysisen varaston hyllytykset](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  


## <a name="see-also"></a>Katso myös

[!INCLUDE[footer-include](includes/footer-banner.md)]
