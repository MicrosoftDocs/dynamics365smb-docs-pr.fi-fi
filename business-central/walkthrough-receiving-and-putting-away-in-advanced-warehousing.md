---
title: "Vastaanotto ja hyllytys laajennetussa fyysisessä varastoinnissa | Microsoft Docs"
description: "Business Central -sovelluksessa vastaanoton ja hyllytyksen saapuvat prosessit voidaan suorittaa neljällä tavalla eri toimintojen avulla varastotason monimutkaisuuden mukaan."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3c1f7a6d08ac03da0d89bad464784b71249c36a2
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-receiving-and-putting-away-in-advanced-warehouse-configurations"></a>Vaihekuvaus: Vastaanotto ja hyllytys laajennetuissa varastomäärityksissä
[!INCLUDE[d365fin](includes/d365fin_md.md)]issa vastaanoton ja hyllytyksen saapuvat prosessit voidaan suorittaa neljällä tavalla eri toimintojen avulla varastotason monimutkaisuuden mukaan.  

|Tapa|Saapuva prosessi|Varastopaikat|Vastaanotot|Hyllytykset|Monimutkaisuustaso (katso [Rakennetiedot: Fyysisen varaston asetukset](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|L|Vastaanoton ja hyllytyksen kirjaaminen tilausriviltä|X|||2|  
|B|Vastaanoton ja hyllytyksen kirjaaminen varaston hyllytysasiakirjasta|||X|3|  
|N|Kirjaa vastaanotto ja hyllytys fyysisen varastoinnin vastaanottoasiakirjasta||X||4/5/6|  
|P|Kirjaa vastaanotto fyysisen varastoinnin vastaanottoasiakirjasta ja kirjaa hyllytys varaston hyllytysasiakirjasta||X|X|4/5/6|  

Lisätietoja on kohdassa [Rakennetiedot: Saapuvan fyysisen varastoinnin virta](design-details-inbound-warehouse-flow.md).  

Seuraavassa vaihekuvauksessa kuvataan edellisen taulukon menetelmää D.  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta  
Jos sijainti on määritetty laajennetuissa varastomäärityksissä edellyttämään vastaanoton käsittelyä hyllytyksen käsittelyn lisäksi, sinun on tallennettava ja kirjattava useiden saapuvien tilausten nimikkeiden vastaanotto **F. varastoinnin vastaanotto** -ikkunassa. Kun fyysisen varastoinnin vastaanotto kirjataan, yksi tai useampia fyysisen varaston hyllytysasiakirjoja luodaan opastamaan varastotyöntekijöitä ottamaan vastaanotetut nimikkeet ja asettamaan ne osoitetuille paikoille varastopaikan asetusten mukaisesti tai muihin varastopaikkoihin. Nimikkeiden tarkka sijoitus tallennetaan, kun varastoinnin hyllytys rekisteröidään. Saapuva lähdeasiakirja voi olla ostotilaus, myyntipalautustilaus, saapuva siirtotilaus, kokoonpano tai tuotantotilaus jonka tuotos odottaa hyllytystä. Jos vastaanotto on luotu saapuvasta tilauksesta, kuitille voidaan noutaa useampia kuin yksi saapuva lähdeasiakirja. Tällä menetelmällä voit rekisteröidä useita kohteita eri tulevista tilauksista yhdellä vastaanotolla.  

Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä.  

-   Määritetään VALKOINEN-sijainti vastaanotolle ja hyllyttämiselle.  
-   Kahden ostotilauksen luominen ja julkaiseminen koko varaston käsittelyyn.  
-   Fyysisen varastoinnin vastaanottoasiakirjan luominen ja kirjaaminen useille ostotilausriveille tietyiltä toimittajilta.  
-   Rekisteröidään fyysisen varastoinnin hyllytys vastaanotetuille nimikkeille.  

## <a name="roles"></a>Roolit  
Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:  

-   Varastopäällikkö  
-   Ostaja  
-   Vastaanottava henkilöstö  
-   Varastotyöntekijä  

## <a name="prerequisites"></a>Vaatimukset  
Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:  

-   CRONUS Finland Oy on asennettu.  
-   Voit tehdä itsestäsi fyysisen varaston työntekijän VALKOISESSA sijainnissa tekemällä seuraavat toimet:  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Varaston työntekijät** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse ensin **Käyttäjätunnus**-kenttä ja valitse oma käyttäjätilisi **Käyttäjät**-ikkunassa.  
3.  Kirjoita **Sijaintikoodi**-kenttään VALKOINEN.  
4.  Valitse **Oletus**-kenttä.  

## <a name="story"></a>Taustatietoja  
Ellen on CRONUS Finland Oy:n varastopäällikkö, ja hän luo kaksi ostotilausta lisänimikkeille toimittajilta 10 000 ja 20 000 toimitettavaksi VALKOISEEN varastoon. Kun toimitukset saapuvat fyysiseen varastoon, toimittajien 10000 ja 20000 nimikkeiden vastaanottamisesta vastaava Sammy käyttää suodatinta luomaan vastaanoton rivejä ostotilauksille, jotka saapuvat kahdelta toimittajalta. Sammy kirjaa nimikkeet vastaanotetuiksi varastossa yhteen fyysisen varastoinnin vastaanottoon ja asettaa kohteet käytettäviksi myyntiin tai muuhun kysyntään. Varastotyöntekijä Juha ottaa nimikkeet vastaanottavasta varastopaikasta ja hyllyttää ne. Hän sijoittaa kaikki yksiköt oletusvarastopaikkoihin, lukuun ottamatta neljääkymmentä sadasta vastaanotetusta saranasta, jotka hän hyllyttää kokoonpano-osastolle jakamalla hyllytyksen rivin. Kun Juha rekisteröi hyllytyksen, varastopaikan sisältö päivitetään ja nimikkeet tuodaan varastosta keräiltäviksi.  

## <a name="reviewing-the-white-location-setup"></a>Tarkistaa VALKOINEN-sijainnin asetuksia  
**Sijaintikortti**-ikkunan asetuksissa määritellään yrityksen varaston työnkulut.  

### <a name="to-review-the-location-setup"></a>Sijainnin asetusten tarkistaminen  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sijainnit** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Avaa asianmukaisen VALKOINEN sijainnin kortti.  
3.  Huomaa **F. varastointi** -pikavälilehdellä, että **Ohjattu hyllytys ja poiminta** -valintaruutu valitaan.  

    Sijainti on siis määritetty mahdollisimman monimutkaiseksi, mistä kertoo se, että kaikki pikavälilehden varastokäsittelyn valintaruudut ovat valittuina.  

4.  Huomaa **Varastopaikat**-pikavälilehdellä, että varastopaikat määritetään **Vast.otto var.paikan koodi** - ja **Toimituksen varastopaikkakoodi** -kentissä.  

Tämä tarkoittaa sitä, että kun luot fyysisen varastoinnin vastaanoton, tämä varastopaikkakoodi kopioidaan oletusarvoisesti fyysisen varastoinnin vastaanottoasiakirjan otsikkoon ja fyysisen varaston hyllytysten riveille.  

## <a name="creating-the-purchase-orders"></a>Ostotilausten luominen  
Ostotilaukset ovat yleisin saapuvien lähdeasiakirjojen tyyppi.  

### <a name="to-create-the-purchase-orders"></a>Ostotilausten luominen  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostotilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Luo ostotilaus toimittajalle 10000 (23.1.) käsittelypäivämääränä seuraavien ostontilausrivien kanssa.  

    |Nimike|Sijaintikoodi|määrä.|  
    |----------|-------------------|--------------|  
    |70200|VALKOINEN|100 KPL|  
    |70201|VALKOINEN|50 KPL|  

    Siirry ja ilmoita varastolle, että ostotilaus on valmis varaston käsittelyyn, kun toimitus saapuu.  

4.  Valitse **Vapauta**-toiminto.  

    Luo toinen ostotilaus.  

5.  Valitse **Uusi**-toiminto.  
6.  Luo ostotilaus toimittajalle 20000 käsittelypäivämääränä seuraavien ostontilausrivien kanssa.  

    |Nimike|Sijaintikoodi|Määrä|  
    |----------|-------------------|--------------|  
    |70100|VALKOINEN|10 TÖLKKIÄ|  
    |70101|VALKOINEN|12 TÖLKKIÄ|  

    Valitse **Vapauta**-toiminto.  

    VALKOINEN-varastoon on saapunut nimikkeiden toimitukset toimittajilta 10000 ja 20000, ja Sammy alkaa käsitellä ostovastaanottoja.  

## <a name="receiving-the-items"></a>Nimikkeiden vastaanotto  
Voit hallita **F. varastoinnin vastaanotto** -ikkunassa useita lähdeasiakirjojen, kuten ostotilausten, saapuvia tilauksia.  

### <a name="to-receive-the-items"></a>Nimikkeiden vastaanotto  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **F.var. vast.otot** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Kirjoita **Sijaintikoodi**-kenttään VALKOINEN.  
4.  Valitse **Käytä suodat. kun haet lähd.d** -toiminto.  
5.  Kirjoita **Koodi**-kenttään **LISÄLAITTEET**.  
6.  Kirjoita **Kuvaus**-kenttään **Toimittajat 10000 ja 20000**.  
7.  Valitse **Muokkaa**-toiminto.  
8.  Anna **Osto**-pikavälilehden **Tavarantoimittajan nrosuodatus** -kentässä **10000&#124;20000**.  
9. Valitse **Aja**-toiminto. Fyysisen varastoinnin vastaanottoon tulee neljä riviä, jotka edustavat määritettyjen toimittajien ostotilausrivejä. **Vastaanotettava määrä** -kenttä on täytetty, koska et valinnut **Älä täytä käsiteltävää määrää** -valintaruutua **Suod. lähdeasiakirj. saamisek.** -ikkunassa.  
10. Jos puolestaan haluat käyttää suodatinta aiemmin tässä osassa kuvatulla tavalla, valitse ensin **Hae lähdeasiakirja** -toiminto ja sitten kyseisten toimittajien ostotilaukset.  
11. Valitse ensin **Kirjaa vast.otto** -toiminto ja sitten **Kyllä**.  

    Luodaan positiivisia nimiketapahtumia, jotka heijastavat kirjattuja apuohjelmien tavaran vastaanottoja toimittajilta 10000 ja 20000, ja nimikkeet ovat valmiita hyllyttäviksi vastaanoton varastopaikan varastossa.  

## <a name="putting-the-items-away"></a>Nimikkeiden hyllyttäminen  
Voit hallita **Kirjaa vast.otto** -ikkunassa tietyn, useita lähdeasiakirjoja kattavan fyysisen varastoinnin vastaanoton asiakirjan hyllytyksiä. Kuten kaikkia fyysisen varaston toimintojen asiakirjoja, kutakin varaston hyllytyksen nimikettä edustaa Ota-rivi ja Aseta-rivi. Seuraavassa menettelyssä Ota-rivien varastopaikkakoodi on oletusarvoinen vastaanoton varastopaikka VALKOINEN-sijainnissa, W-08-0001.  

### <a name="to-put-the-items-away"></a>Nimikkeiden hyllyttäminen  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Hyllytykset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse ainoa fyysisen varastoinnin hyllytysasiakirja luettelosta ja valitse sitten **Koti**-välilehdellä **Hallinta**-ryhmässä **Muokkaa**.  

    Varaston hyllytysasiakirja avaa yhteensä kahdeksan Ota- tai Aseta-riviä neljälle ostotilausriville.

    Varastotyöntekijälle ilmoitetaan, että kokoonpano-osastolle tarvitaan 40 saranaa. Hän jakaa yhden Aseta-rivin määrittääkseen toisen Aseta-rivin lokerolle W-02-0001 kokoonpano-osastolla, johon hän asettaa vastaanotettujen saranoiden osan.  

3.  Valitse **F.varastoinnin hyllytys** -ikkunassa toinen rivi, joka on nimikkeen 70200 Aseta-rivi.  
4.  Muuta **Käsiteltävä määrä** -kentän 100 arvoksi 60.  
5.  Valitse **Rivit**-pikavälilehdessä **Toiminnot** ja valitse sitten **Jaa rivi**. **Käsiteltävä määrä** -kentässä nimikkeelle 70200 lisätään uusi rivi, jossa on arvo 40.  
6.  Kirjoita **Varastopaikkakoodi**-kenttään W-02-0001. **Aluekoodi**-kenttä täytetään automaattisesti.  

    Rekisteröi hyllytys.  

7.  Valitse ensin **Rekisteröi hyllytys** -toiminto ja sitten **Kyllä**.  

    Vastaanotetut apuohjelmat on nyt hyllytetty nimikkeiden oletusvarastopaikkoihin, ja 40 saranaa on sijoitettu kokoonpano-osastolle. Vastaanotetut nimikkeet ovat nyt saatavilla sisäisen kysynnän keräystä varten, kuten kokoonpanotilauksiin, tai ulkoiseen kysyntään, kuten myyntitoimituksiin.  

## <a name="see-also"></a>Katso myös  
 [Nimikkeiden hyllyttäminen ja fyysisen varaston hyllytykset](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Nimikkeiden siirtäminen laajennetuissa varastomäärityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Rakennetiedot: saapuvan fyysisen varastoinnin virta](design-details-inbound-warehouse-flow.md)   
 [Vaihekuvaus: Vastaanotto ja hyllytys fyysisen varastoinnin perusmäärityksissä](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)   
 [Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)

