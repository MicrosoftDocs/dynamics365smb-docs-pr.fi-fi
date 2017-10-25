---
title: "Rakennetiedot – sisäisen fyysisen varastoinnin virrat | Microsoft Docs"
description: "Nimikkeiden kulku binien välillä yrityksen sijaintikeskuksissa osien poimintaan ja loppunimikkeiden poistoon kokoonpano- tai tuotantotilauksissa ja tilapäisissä liikkeissä, kuten binin täydentämisissä ilman suhdetta lähdedokumentteihin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9ba5203013af329f1d59432a5e5800fe486658cc
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-internal-warehouse-flows"></a>Rakennetiedot: sisäisen fyysisen varastoinnin virta
Nimikkeiden kulku varastopaikkojen välillä yrityksen sijaintikeskuksissa kokoonpano- tai tuotantotilauksien komponentteja poimittaessa ja loppunimikkeitä hyllytettäessä sekä suunnittelemattomissa siirroissa, kuten varastopaikkojen täydennyksissä, ilman suhdetta lähdeasiakirjoihin. Liittyvien toimenpiteiden laajuus ja luonne vaihtelee perus- ja kehittyneen varastoinnin välillä.  

 Jotkut sisäiset virtaukset peittävät saapuvat tai lähtevät virtaukset. Osa tästä päällekkäisyydestä on esitetty vaiheissa 4 ja 5 graafisissa kaavioissa saapuvissa ja lähtevissä virtauksissa tässä järjestyksessä. Lisätietoja on kohdassa [Rakennetiedot: Saapuva fyysisen varastoinnin virta](design-details-outbound-warehouse-flow.md).  

## <a name="internal-flows-in-basic-warehousing"></a>Sisäiset virtaukset perusvarastoinnissa  
 Varaston perusmäärityksessä nimikkeiden virtaus yrityksen sisällä varastopaikkojen välillä keskittyy komponentin poimintaan ja loppunimikkeiden hyllytykseen tuotanto- tai kokoonpanotilaus- ja ad-hoc-siirroille, kuten varastopaikan täydennykset lähdeasiakirjoihin liittymättä.  

### <a name="flows-to-and-from-production"></a>Virtaa tuotantoon ja tuotannosta  
 Pääintegraatio tuotantotilausten ja perusvarastoinnin toimenpiteiden välillä tulee esille kykynä poimia tuotanto-osia **Varastopoiminta**-ikkunassa tai **Varaston siirtymä** -ikkunassa.  

> [!NOTE]  
>  Komponentin kulutus kirjataan yhdessä poiminnan kirjauksen kanssa **Varaston poiminta**-ikkunassa. Vain varastopaikan muutokset rekisteröidään ja nimiketapahtumia ei tapahdu, kun käytetään **Varaston siirtotapahtuma** -ikkunaa.  

 Komponenttien käsittelyn lisäksi integrointia tukee mahdollisuus hyllyttää tuotetut nimikkeet **Varastohyllytys** -ikkunan avulla.  

 Sijaintikortin **Tuotannon valm.var.paik.koodi**-, **Valm. tuot.nim. var.paik.koodi**- ja **Avoin tuotannon var.paik.koodi** -kenttä tai koneen/tuotantosolun kortit määrittävät tuotantoalueen tulevat ja lähtevät oletustyönkulut.  

 Katso lisätietoja siitä, kuinka komponentin kulutus tyhjennetään tuotannon valmistelu- tai avoin tuotanto -varastopaikoista tämän aiheen kohdasta Materiaalioton tuotantokomponentit f. varastossa.  

### <a name="flows-to-and-from-assembly"></a>Virtaa kokoonpanoon ja kokoonpanosta  
 Pääintegraatio kokoonpanotilausten ja perusvarastoinnin toimenpiteiden välillä tulee esille kykynä siirtää kokoonpano-osia kokoonpanoalueelle.  

 Vaikka kokoonpanonimikkeiden hyllytykselle ei ole tiettyä fyysistä varastointitoimintoa, kokoonpanotilauksen otsikon varastopaikkakoodi voidaan määrittää hyllytyksen oletusvarastopaikaksi. Kokoonpanotilauksen kirjaaminen toimii tämän jälkeen kuin hyllytyksen kirjaaminen. Kokoonpanonimikkeitä fyysiseen varastoon siirtävää varastotoimintaa voi hallita **Sisäinen siirto** -ikkunassa ilman, että se liittyy kokoonpanotilaukseen.  

 Seuraavat sopeuttamiset ovat olemassa.  

|Työnkulku|Description|  
|----------|---------------------------------------|  
|Kokoa-varastoon|Osia tarvitaan kokoonpanotilauksessa, jossa tuotos on tallennettu varastoon.<br /><br /> Tätä fyysisen varaston työnkulkua hallitaan **Varaston siirto** -ikkunassa. Yksi ota-rivi määrittää, minne osat viedään. Yksi asetusrivi määrittää, mihin osat sijoitetaan.|  
|Kokoonpano tilausta varten|Osia tarvitaan kokoonpanotilauksessa, joka on linkitetty myyntitilaukseen, joka lähetetään, kun myyty nimike on koottu yhteen.|  

> [!NOTE]  
>  Jos nimikkeet on koottu tilaukseen, linkitettyjen myyntitilausten varastopoiminta käynnistää varastosiirron kaikille mukana oleville kokoonpanokomponenteille, eikä pelkästään myydylle nimikkeelle, kuten varastonimikkeitä toimitettaessa.  

 Sijaintikortin **Kokoonpanoon-varastop.koodi**, **Kokoonpanosta-varastop.koodi**- ja **Kok. til.ltoimit. -var.p.koodi** -kentät määrittävät kokoonpanoalueiden saapuvat ja lähtevät oletustyönkulut.  

> [!NOTE]  
>  **Kok. til.ltoimit. -var.p.koodi** -kentän toiminnot, kuten kokoonpanosta varastopaikkaan, Kokoonpano tilausta varten -malleissa.  

### <a name="ad-hoc-movements"></a>Ad-Hoc-liikkeet  
 Fyysisen varastoinnin perusmäärityksissä nimikkeiden siirrot varastopaikasta toiseen ilman, että ne on liitetty lähdeasiakirjoihin, suoritetaan **Sisäinen siirto** -ikkunassa, joka toimii yhdessä **Varaston siirto** -ikkunan kanssa.  

 Nimikkeitä voi siirtää suunnittelematta varastopaikkojen välillä myös kirjaamalla positiivisia tapahtumia **Nimikkeen uudel.luokit. pvk** -ikkunan **Uusi varastopaikkakoodi** -kentässä.  

## <a name="internal-flows-in-advanced-warehousing"></a>Sisäiset virtaukset laajennetussa varastoinnissa  
 Laajennetuissa varaston määrityksissä nimikkeiden virtaus yrityksen sisällä varastopaikkojen välillä keskittyy komponentin poimintaan ja loppunimikkeiden hyllyttämiseen tuotantotilauksille ja komponenttien poimintaan kokoonpanontilauksille. Lisäksi sisäiset virrat tapahtuvat ad-hoc-siirtoina, kuten varastopaikan täydennyksinä ilman suhdetta lähdeasiakirjoihin.  

### <a name="flows-to-and-from-production"></a>Virtaa tuotantoon ja tuotannosta  
 Pääintegraatio tuotantotilausten ja kehittyneen varastoinnin toimenpiteiden välillä tulee esille kykynä poimia tuotanto-osia **Varastopoiminta** -ikkunassa ja **Poimi taulukko** -ikkunassa, ja kyky poistaa tuotetut nimikkeet **Whse. sisäinen poisto** -ikkunassa.  

 Toinen tuotannon integrointikohta on **F. var. siirto** -ikkunassa, jossa voi yhdessä Siirtotyökirja-ikkunan kanssa sijoittaa komponentteja ja ottaa vapautettujen tuotantotilausten tuotettuja nimikkeitä.  

 Sijaintikortin **Tuotannon valm.var.paik.koodi**-, **Valm. tuot.nim. var.paik.koodi**- ja **Avoin tuotannon var.paik.koodi** -kenttä tai koneen/tuotantosolun kortit määrittävät tuotantoalueen tulevat ja lähtevät oletustyönkulut.  

 Katso lisätietoja siitä, kuinka komponentin kulutus tyhjennetään tuotannon valmistelu- tai avoin tuotanto -varastopaikoista tämän aiheen kohdasta Materiaalioton tuotantokomponentit f. varastossa.  

### <a name="flows-to-and-from-assembly"></a>Virtaa kokoonpanoon ja kokoonpanosta  
 Pääintegraatio kokoonpanotilausten ja kehittyneen varastoinnin toimenpiteiden välillä tulee esille kykynä poimia kokoonpano-osia, sekä **Varastopoiminta**-ikkunassa että **Poimi taulukko** -ikkunassa. Tämä toiminto on samanlainen kuin komponenttien poiminta tuotantotilaukseen.  

 Vaikka kokoonpanonimikkeiden hyllytykselle ei ole tiettyä fyysistä varastointitoimintoa, kokoonpanotilauksen otsikon varastopaikkakoodi voidaan määrittää hyllytyksen oletusvarastopaikaksi. Kokoonpanotilauksen kirjaaminen toimii tämän jälkeen kuin hyllytyksen kirjaaminen. Fyysisessä varastossa nimikkeiden siirtämiseen käytettyä varastotoimintoa voi hallita **Siirtotyökirja**- tai **F.var. sis. hyllytys** -ikkunassa ilman, että se liittyy kokoonpanotilaukseen.  

> [!NOTE]  
>  Jos nimikkeet on koottu tilaukseen, linkitettyjen myyntitilausten fyysisen varaston toimitus käynnistää fyysisen varastoinnin poiminnan kaikille mukana oleville kokoonpanokomponenteille, eikä pelkästään myydylle nimikkeelle, kuten varastonimikkeitä toimitettaessa.  

 Sijaintikortin **Kokoonpanoon-varastop.koodi**- ja **Kokoonpanosta-varastop.koodi** -kenttä määrittävät kokoonpanoalueiden saapuvat ja lähtevät oletustyönkulut.  

### <a name="ad-hoc-movements"></a>Ad-Hoc-liikkeet  
 Laajennetussa varastoinnissa nimikkeiden siirtoja varastopaikasta toiseen ilman, että ne liittyvät lähdeasiakirjoihin, hallitaan **Siirtotyökirja**-ikkunassa ja rekisteröidään F. var. siirto -ikkunassa.  

## <a name="flushing-production-components-in-the-warehouse"></a>Materiaalioton tuotantokomponentit f. varastossa  
 Jos nimikkeen kortilla on näin asetettu, varastoinnin poiminnalla poimitut komponentit kirjataan tuotantotilauksen kuluttamiksi, kun varastoinnin poiminta rekisteröidään. Käyttämällä **Poiminta + eteenpäin** -menetelmää ja **Poiminta + taaksepäin**-materiaalinottotapaa, poiminnan rekisteröinti laukaisee liittyvän kulutuksen kirjaamisen ensimmäisen toimenpiteen alettua tai viimeisen toimenpiteen päätyttyä.  

 Mietitään seuraavaa tilannetta, joka perustuu [!INCLUDE[d365fin](includes/d365fin_md.md)]in esittelytietokannan VALKOINEN-sijaintiin.  

 Nimikkeen LS-100 15 kappaleen tuotantotilaus on olemassa. Jotkut osaluettelon nimikkeistä täytyy pakottaa manuaalisesti kulutuserään ja toiset luettelon nimikkeet voidaan poimia ja pakottaa automaattisesti käyttämällä **Poimi + takaisin** -virtausmenetelmää.  

> [!NOTE]  
>  **Poiminta + eteenpäin** toimii vain jos toinen tuotannon reitityslinjan toiminto käyttää reitityslinkin koodia. Suunnitellun tuotantotilauksen julkaiseminen aloittaa niiden osien eteenpäin virtauksen, joille on määritetty **Poimi + eteenpäin**. Materiaalinotto ei voi kuitenkaan tapahtua ennen komponenttien poiminnan rekisteröintiä joka taas voi tapahtua, kun tilaus vapautetaan.  

 Seuraavissa vaiheissa kuvataan eri käyttäjien ja liittyvän vastauksen mukana olevia toimintoja:  

1.  Kaupan työnjohtaja vapauttaa tuotantotilauksen. Ne nimikkeet, jotka käyttävät **Eteenpäin**-materiaalinottotapaa ja joilla ei ole reitityslinkki-koodia, vähennetään avoimen tuotannon varastopaikasta.  
2.  Työnjohtaja kaupassa valitsee **Luo varastopoiminta** -painikkeen tuotantotilauksesta. Fyysisen varaston poiminta-asiakirja luodaan poimimaan nimikkeitä **Manuaalinen**-, **Poiminta + taaksepäin**- ja **Poiminta + eteenpäin**-materiaalinottotavoilla. Nämä nimikkeet on asetettu tuotannon valmisteluvarastopaikkaan.  
3.  Varastopäällikkö määrittää poiminnat varastotyöntekijöille.  
4.  Varastotyöntekijä poimii nimikkeet soveltuvista varastopaikoista ja asettaa ne tuotannon valmisteluvarastopaikkaan tai fyysisen varastoinnin poiminnan määritettyyn varastopaikkaan. Se voi olla tuotantosolun tai kuormitusryhmän varastopaikka.  
5.  Varastotyöntekijä rekisteröi poiminnan. Määrää vähennetään poimintabineistä ja lisätään kulutusbiniin. kaikkien poimittujen nimikkeiden **Poimittu määrä** -kenttä osaluettelossa on päivitetty.  

    > [!NOTE]  
    >  Vain poimittu määrä voidaan kuluttaa.  

6.  Koneenkäyttäjä tiedottaa tuotantojohtajaa, että loppukohdat ovat lopussa.  
7.  Kaupan työnjohtaja käyttää kulutuslokia tai tuotantolokia ja tiliöi osan nimikkeiden kulutuksen, joka käyttää joko **Manuaalinen** -virtausmenetelmää tai **Vie eteenpäin** tai **Poimi + vie eteenpäin** -virtausmenetelmää yhdessä reitityslinkkikoodien kanssa.  
8.  Tuotantopäällikkö tiliöi tuotantotilauksen tuotannon ja vaihtaa tilaksi **Valmis**. Osan nimikkeiden määrää, joka käyttää **Takaisin** -virtausmenetelmää, vähennetään avoimesta kaupan myyntikärrystä, ja osan nimikkeiden määrää, jota käytetään **Poimi + takaisin** -virtausmenetelmässä, vähennetään Tuotantoon-binistä.  

 Seuraavassa kuvassa esitetään, milloin **Bin-koodi** -kenttä osaluettelossa täytetään sijainnin tai koneen/työkeskuksen asetusten mukaisesti.  

 ![Varastopaikkojen vuokaavio](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)

