---
title: Vastaanotto ja hyllytys laajennetussa varastoinnissa
description: Vastaanoton ja hyllytyksen saapuvat prosessit voidaan suorittaa neljällä tavalla eri toimintojen avulla varastotason monimutkaisuuden mukaan.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
---
# Vaihekuvaus: Vastaanotto ja hyllytys laajennetuissa varastomäärityksissä

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

[!INCLUDE[prod_short](includes/prod_short.md)]issa vastaanoton ja hyllytyksen voi tehdä neljällä tavalla, joista kukin käsitellään seuraavassa taulukossa.

|Tapa|Saapuva prosessi|Vaadi vastaanotot|Vaadi hyllytykset|Monimutkaisuustaso (lisätietoja on kohdassa [Varastoinninhallinnan yleiskatsaus](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Vastaanoton ja hyllytyksen kirjaaminen tilausriviltä|||Ei määritettyä fyysisen varaston toimintaa.|  
|B|Vastaanoton ja hyllytyksen kirjaaminen varaston hyllytysasiakirjasta||Otettu käyttöön|Perus: tilauksittain.|  
|S|Kirjaa vastaanotto ja hyllytys fyysisen varastoinnin vastaanottoasiakirjasta|Otettu käyttöön||Perus: useiden tilausten konsolidoitu vastaanoton ja toimituksen kirjaus.|  
|P|Kirjaa vastaanotto fyysisen varastoinnin vastaanottoasiakirjasta ja kirjaa hyllytys varaston hyllytysasiakirjasta|Otettu käyttöön|Otettu käyttöön|Lisäasetukset|  

Lisätietoja on kohdassa [Saapuvien varastotyönkulku](design-details-inbound-warehouse-flow.md).

Seuraavassa vaihekuvauksessa kuvataan edellisen taulukon menetelmää D.  

## Tietoja tästä vaihekuvauksesta

Jos sijainti on määritetty laajennetuissa varastomäärityksissä edellyttämään vastaanoton käsittelyä hyllytyksen käsittelyn lisäksi, sinun on tallennettava ja kirjattava useiden saapuvien tilausten nimikkeiden vastaanotto **F. varastoinnin vastaanotto** -sivulla. Kun fyysisen varastoinnin vastaanotto kirjataan, yksi tai useampia fyysisen varaston hyllytysasiakirjoja luodaan opastamaan varastotyöntekijöitä ottamaan vastaanotetut nimikkeet ja asettamaan ne osoitetuille paikoille varastopaikan asetusten mukaisesti tai muihin varastopaikkoihin. Nimikkeiden tarkka sijoitus tallennetaan, kun varastoinnin hyllytys rekisteröidään. Saapuva lähdeasiakirja voi olla ostotilaus, myyntipalautustilaus, saapuva siirtotilaus, kokoonpano tai tuotantotilaus jonka tuotos odottaa hyllytystä. Jos vastaanotto on luotu saapuvasta tilauksesta, kuitille voidaan noutaa useampia kuin yksi saapuva lähdeasiakirja. Tällä menetelmällä voit rekisteröidä useita kohteita eri tulevista tilauksista yhdellä vastaanotolla.  

Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

-   Määritetään VALKOINEN-sijainti vastaanotolle ja hyllyttämiselle.  
-   Kahden ostotilauksen luominen ja julkaiseminen koko varaston käsittelyyn.  
-   Fyysisen varastoinnin vastaanottoasiakirjan luominen ja kirjaaminen useille ostotilausriveille tietyiltä toimittajilta.  
-   Rekisteröidään fyysisen varastoinnin hyllytys vastaanotetuille nimikkeille.  

## Roolit

Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:  

-   Varastopäällikkö  
-   Ostaja  
-   Vastaanottava henkilöstö  
-   Varastotyöntekijä  

## Vaatimukset

Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:  

-   CRONUS on asennettu.  
-   Voit tehdä itsestäsi fyysisen varaston työntekijän VALKOISESSA sijainnissa tekemällä seuraavat toimet:  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston työntekijät** ja valitse sitten vastaava linkki.  
2.  Valitse ensin **Käyttäjätunnus**-kenttä ja valitse oma käyttäjätilisi **Käyttäjät**-sivulla.  
3.  Kirjoita **Sijaintikoodi**-kenttään VALKOINEN.  
4.  Valitse **Oletus**-kenttä.  

## Taustatietoja

Ellen on CRONUSin varastopäällikkö, ja hän luo kaksi ostotilausta lisänimikkeille toimittajilta 10 000 ja 20 000 toimitettavaksi VALKOISEEN varastoon. Kun toimitukset saapuvat fyysiseen varastoon, toimittajien 10000 ja 20000 nimikkeiden vastaanottamisesta vastaava Sammy käyttää suodatinta luomaan vastaanoton rivejä ostotilauksille, jotka saapuvat kahdelta toimittajalta. Sammy kirjaa nimikkeet vastaanotetuiksi varastossa yhteen fyysisen varastoinnin vastaanottoon ja asettaa kohteet käytettäviksi myyntiin tai muuhun kysyntään. Varastotyöntekijä Juha ottaa nimikkeet vastaanottavasta varastopaikasta ja hyllyttää ne. John sijoittaa kaikki yksiköt oletusvarastopaikkoihin, lukuun ottamatta neljääkymmentä sadasta vastaanotetusta saranasta, jotka hyllytetään kokoonpano-osastolle jakamalla hyllytyksen rivin. Kun Juha rekisteröi hyllytyksen, varastopaikan sisältö päivitetään ja nimikkeet tuodaan varastosta keräiltäviksi.  

## Tarkistaa VALKOINEN-sijainnin asetuksia

**Sijaintikortti**-sivun asetuksissa määritellään yrityksen varaston työnkulut.  

### Sijainnin asetusten tarkistaminen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
2.  Avaa asianmukaisen VALKOINEN sijainnin kortti.  
3.  Huomaa **F. varastointi** -pikavälilehdellä, että **Ohjattu hyllytys ja poiminta** -valintaruutu valitaan.  

    Sijainti on siis määritetty mahdollisimman monimutkaiseksi, mistä kertoo se, että kaikki pikavälilehden varastokäsittelyn valintaruudut ovat valittuina.  

4.  Huomaa **Varastopaikat**-pikavälilehdellä, että varastopaikat määritetään **Vast.otto var.paikan koodi** - ja **Toimituksen varastopaikkakoodi** -kentissä.  

Tämä tarkoittaa sitä, että kun luot fyysisen varastoinnin vastaanoton, tämä varastopaikkakoodi kopioidaan oletusarvoisesti fyysisen varastoinnin vastaanottoasiakirjan otsikkoon ja fyysisen varaston hyllytysten riveille.  

## Ostotilausten luominen

Ostotilaukset ovat yleisin saapuvien lähdeasiakirjojen tyyppi.  

### Ostotilausten luominen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Luo ostotilaus toimittajalle 10000 (23.1.) käsittelypäivämääränä seuraavien ostontilausrivien kanssa.  

    |Nimike|Sijaintikoodi|määrä.|  
    |----------|-------------------|--------------|  
    |70200|VALKOINEN|100 KPL|  
    |70201|VALKOINEN|50 KPL|  

    Siirry ja ilmoita varastolle, että ostotilaus on valmis varaston käsittelyyn, kun toimitus saapuu.  

4.  Valitse **Vapauta**-toiminto. Tila muuttuu tilasta Avoin tilaan Vapautettu.

    Luo toinen ostotilaus.  

5.  Valitse **Uusi**-toiminto.  
6.  Luo ostotilaus toimittajalle 20000 (23.1.) käsittelypäivämääränä seuraavien ostontilausrivien kanssa.  

    |Nimike|Sijaintikoodi|Määrä|  
    |----------|-------------------|--------------|  
    |70100|VALKOINEN|10 TÖLKKIÄ|  
    |70101|VALKOINEN|12 TÖLKKIÄ|  

    Valitse **Vapauta**-toiminto. Tila muuttuu tilasta Avoin tilaan Vapautettu.

    VALKOINEN-varastoon on saapunut nimikkeiden toimitukset toimittajilta 10000 ja 20000, ja Sammy alkaa käsitellä ostovastaanottoja.  

## Nimikkeiden vastaanotto

Voit hallita **F. varastoinnin vastaanotto** -sivulla useita lähdeasiakirjojen, kuten ostotilausten, saapuvia tilauksia.  

### Nimikkeiden vastaanotto  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston vastaanotot** ja valitse sitten vastaava linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Kirjoita **Sijaintikoodi**-kenttään VALKOINEN.  
4.  Valitse **Toiminnot**, sitten **Funktiot** ja valitse sitten **Käytä suodat. kun haet lähd.d.** -toiminto.  
5.  Kirjoita **Koodi**-kenttään **LISÄLAITTEET**.  
6.  Kirjoita **Kuvaus**-kenttään **Toimittajat 10000 ja 20000**.  
7.  Valitse **Muokkaa**-toiminto.  
8.  Anna **Osto**-pikavälilehden **Tavarantoimittajan nrosuodatus** -kentässä **10000&#124;20000**.  
9. Valitse **Aja**-toiminto. Fyysisen varastoinnin vastaanottoon tulee neljä riviä, jotka edustavat määritettyjen toimittajien ostotilausrivejä. **Vastaanotettava määrä** -kenttä on täytetty, koska et valinnut **Älä täytä käsiteltävää määrää** -valintaruutua **Suod. lähdeasiakirj. saamisek.** -sivulla.  
10. Jos puolestaan haluat käyttää suodatinta aiemmin tässä osassa kuvatulla tavalla, valitse ensin **Hae lähdeasiakirja** -toiminto ja sitten kyseisten toimittajien ostotilaukset.  
11. Valitse **Kirjaus**, sitten **Kirjaa vast.otto** -toiminto ja valitse sitten **Kyllä**-painike.  

    Luodaan positiivisia nimiketapahtumia, jotka heijastavat kirjattuja apuohjelmien tavaran vastaanottoja toimittajilta 10000 ja 20000, ja nimikkeet ovat valmiita hyllyttäviksi vastaanoton varastopaikan varastossa.  

## Nimikkeiden hyllyttäminen

Voit hallita **Kirjaa vast.otto** -sivulla tietyn, useita lähdeasiakirjoja kattavan fyysisen varastoinnin vastaanoton asiakirjan hyllytyksiä. Kuten kaikkia fyysisen varaston toimintojen asiakirjoja, kutakin varaston hyllytyksen nimikettä edustaa Ota-rivi ja Aseta-rivi. Seuraavassa menettelyssä Ota-rivien varastopaikkakoodi on oletusarvoinen vastaanoton varastopaikka VALKOINEN-sijainnissa, W-08-0001.  


### Nimikkeiden hyllyttäminen  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyllytykset** ja valitse sitten vastaava linkki.  
2.  Valitse ainoa fyysisen varastoinnin hyllytysasiakirja luettelosta ja valitse sitten **Muokkaa**-toiminto.  

    Varaston hyllytysasiakirja avaa yhteensä kahdeksan Ota- tai Aseta-riviä neljälle ostotilausriville.

    Varastotyöntekijälle ilmoitetaan, että kokoonpano-osastolle tarvitaan 40 saranaa. Hän jakaa yhden Aseta-rivin määrittääkseen toisen Aseta-rivin lokerolle W-02-0001 kokoonpano-osastolla, johon varastotyöntekijä asettaa vastaanotettujen saranoiden osan.  

3.  Valitse **F.varastoinnin hyllytys** -sivulla toinen rivi, joka on nimikkeen 70200 Aseta-rivi.  
4.  Muuta **Käsiteltävä määrä** -kentän 100 arvoksi 60.  
5.  Valitse **Rivit**-pikavälilehdessä **Toiminnot** ja valitse sitten **Jaa rivi**. **Käsiteltävä määrä** -kentässä nimikkeelle 70200 lisätään uusi rivi, jossa on arvo 40.  
6.  Kirjoita **Varastopaikkakoodi**-kenttään W-02-0001. **Aluekoodi**-kenttä täytetään automaattisesti.  

    Oletusarvoisesti myyntirivien **Alueen koodi** -kentät on piilotettu, joten ne on tuotava näkyviin. Sen tehdäksesi sinun on muokattava sivua. Lisätietoja on kohdassa, jossa [Sivun mukauttaminen mukautusvalintanauhan avulla](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

    Rekisteröi hyllytys.  

7.  Valitse ensin **Rekisteröi hyllytys** -toiminto ja sitten **Kyllä**.  

    Vastaanotetut apuohjelmat on nyt hyllytetty nimikkeiden oletusvarastopaikkoihin, ja 40 saranaa on sijoitettu kokoonpano-osastolle. Vastaanotetut nimikkeet ovat nyt saatavilla sisäisen kysynnän keräystä varten, kuten kokoonpanotilauksiin, tai ulkoiseen kysyntään, kuten myyntitoimituksiin.  

## Katso myös  
 [Nimikkeiden hyllyttäminen ja fyysisen varaston hyllytykset](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Nimikkeiden siirtäminen laajennetuissa varastomäärityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Rakennetiedot: saapuvan fyysisen varastoinnin virta](design-details-inbound-warehouse-flow.md)   
 <!-- [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)    -->
 [Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
