---
title: 'Vastaanotto, hyllytys, siirto, poiminta ja toimitus edistyneissä varastokokoonpanoissa'
description: Saapuvat ja lähtevät prosessit voidaan suorittaa neljällä eri tavalla varastotason monimutkaisuuden mukaan.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 12/07/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Vaihekuvaus: Saapuva ja lähtevä työnkulku edistyneissä varastokokoonpanoissa

Tässä vaihekuvauksessa kuvataan, miten saapuvat ja lähtevät työnkulut suoritetaan kohteessa Lisäasetukset: Ohjatun hyllytyksen ja poiminnan määritys. Lisätietoja on kohdassa [Erilaisten määritysvaihtoehtojen yleiskatsaus](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## Vaatimukset  
Tämän vaihekuvauksen suorittaminen edellyttää, että teet itsestäsi fyysisen varastoinnin työntekijän *VALKOINEN*-sijainnissa noudattamalla seuraavia ohjeita:  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston työntekijät** ja valitse sitten vastaava linkki.  
2. Valitse ensin **Käyttäjätunnus**-kenttä ja valitse oma käyttäjätilisi **Käyttäjät**-sivulla.  
3. Kirjoita **Sijaintikoodi**-kenttään VALKOINEN.  
4. Ota käyttöön **Oletus**-vaihto.


## Skenaario  
Ellen, varastopäällikkö, käyttää laiturointia ja varastopaikan täydennystoimintoja nopeuttamaan vastaanottoa ja toimitusaikaa.  

## Vaiheet

1. Luo fyysisen varaston toimitus.  

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
    2. Valitse asiakkaan 10000 tilaus VALKOINEN-sijainnissa. Ulkoisen tilauksen numero on *W-1*.
    3. Valitse **Luo fyysisen varaston toimitus** -toimenpide, kun haluat luoda fyysisen varastoinnin toimituksen valitulle myyntitilaukselle.
    4. Valitse **Vapauta**-toiminto, joka ilmoittaa varastolle, että myyntitoimitus on valmis fyysisen varastoinnin käsittelyä varten.  

2. Määritä varastopaikat nimikkeelle määrittääksesi sen hyllytyspaikan 

    1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
    2.  Valitse *WRB-1000* ja valitse sitten **Varastopaikan sisältö** -toiminto.  
    3.  Valitse **Uusi**-toiminto. Lisää kaksi riviä.
    
    |Vaihtoehto|Sijaintikoodi|Varastopaikan koodi|Korjattu|Mittayksikkö|
    |----------|----------|---------|---|------|  
    |WRB-1000|VALKOINEN|W-05-0001|Kyllä|LAUKKU|  
    |WRB-1000|VALKOINEN|W-05-0002|Kyllä|LAUKKU|

3. Luo fyysisen varastoinnin vastaanotto.  

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.  
    2. Valitse toimittajan 10000 tilaus VALKOINEN-sijainnissa. Toimittajan tilauksen numero on *W-2*. Käytä mukautustyökaluja, jos **Toimittajan tilausnumero** -kenttä ei ole näkyvissä. Lisätietoja on kohdassa [Työtilan mukauttaminen](../../ui-personalization-user.md).
    3. Valitse **Luo fyysisen varastoinnin vastaanotto** -toimenpide, kun haluat luoda fyysisen varastoinnin vastaanoton valitulle ostotilaukselle.


4. Tarkista, onko lähteviä tilauksia, jotka tarvitsevat vastaanotettuja nimikkeitä, ja kirjaa vastaanotto
    1. Valitse **Laske laiturointi** -toiminto. Tämä täyttää **Laiturointimäärä**-sarakkeen.
    2. Syötä 0 **Laiturointimäärä**-kenttään riville, jolla on nimike *WRB-1000*, koska et aio pakata niitä uudelleen vastaanottoalueella.
    3. Valitse **Kirjaa vast.otto** -toiminto.

5. Fyysisen varastoinnin hyllytyksen rekisteröinti
    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 5.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston hyllytykset** ja valitse sitten vastaava linkki.
    2. Etsi fyysisen varastoinnin hyllytysasiakirja, joka on luotu fyysisen varastoinnin vastaanotosta, ja avaa se.
    3. Tarkista **Fyysisen varaston hyllytykset** -sivulla **Rivit**-osa

    Tässä vaiheessa varastopaikan kapasiteettilogiikka paljastuu. fyysisen varastoinnin hyllytysriveillä on kolme riviä nimikkeelle *WRB-1000*:
    - Ottorivi, jolla vastaanotetut määrät siirretään vastaanottavasta varastopaikasta (W-08-0001)
    - Aseta-rivi, joka siirtää yhden säilön yhteen määritetyistä varastopaikoista (W-05-0001)
    - Aseta-rivi, joka siirtää toisen säilön toiseen kiinteään varastopaikkaan (W-05-0002). Tämä johtuu siitä, että yksittäinen vakiovarastopaikka ei voi sisältää koko vastaanoton määrää.

    Koska tämä hyllytys sisältää laiturointirivejä, nimikkeelle *WRB-1001* on kolme riviä:
    -  Ottorivi, jolla vastaanotetut määrät siirretään vastaanottavasta varastopaikasta (W-08-0001)
    -  Aseta-rivi kahdelle laiturointivarastopaikkaan
    -  Jäljellä olevan määrän Aseta-rivi varastopaikassa

    4. Valitse **Rekisteröi hyllytys** -toiminto.


6. Määritä poiminnan varastopaikat nimikkeelle hallitaksesi, mistä se poimitaan 

    1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 6.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
    2.  Avaa *VALKOINEN*-sijaintikortti.  
    3.  Valitse **Varastopaikat**-toiminto **sijaintikortissa**
    4.  Valitse varastopaikka *W-02-0001* ja valitse sitten **Sisältö**-toiminto.  
    5.  Valitse **Uusi**-toiminto.  
    6.  Ota käyttöön **Kiinteä**-vaihto.  
    7.  Anna **Nimikenro**-kentässä *WRB-1000*. 
    8.  Syötä **Vähimmäismäärä**-kenttään *2*. 
    9.  Syötä **Enimmäismäärä**-kenttään *10*. 

    Käytä mukautustyökaluja, jos **Vähimmäismäärä**- ja **Enimmäismäärä**-kentät eivät ole näkyvissä. Lisätietoja on kohdassa [Työtilan mukauttaminen](../../ui-personalization-user.md). 

7. Järjestä fyysinen varasto uudelleen siirtämällä nimikkeitä irtotavaran varastointialueelta poiminta-alueelle ja optimoidaksesi poiminta-ajan.

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 7.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston siirron työkirjat** ja valitse liittyvä linkki
    2. Valitse **Laske var.paikan täydennys**-toiminto. 

    Fyysisen varastoinnin työkirja, jossa on nimikkeen *WRB-1000* siirtämistä koskeva ehdotus irtotavaran varastoinnista poiminta-alueelle luodaan.

    3. Valitse **Luo varaston siirto** -toiminto ja vahvista asiakirjan luonti.
    4.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 8.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston siirrot** ja valitse vastaava linkki
    5.  Avaa luomasi fyysisen varaston siirto, tarkista **Rivit**-osa

     Tässä vaiheessa erottelutoiminnallisuus paljastuu. Rivejä on neljä:
    - Rivi, joka ottaa yhden säiliön pois irtotavaran varastopaikasta
    - Rivi, joka sijoittaa 48 kpl takaisin varastoon samaan paikkaan. 
    - Rivi, joka ottaa 10 säiliötä pois irtotavaran varastopaikasta
    - Rivi, joka sijoittaa 10 kpl poimintapaikkaan

    6.  Valitse **Rekisteröi varastosiirto** -toiminto.

8. Luo fyysisen varaston poiminnat

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 9.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poimintatyökirjat** ja valitse vastaava linkki
    2. Valitse **Hae f. varastoinnin asiakirjat** -toiminto, valitse asiakkaan 10000 myyntitilauksen rivi ja valitse sitten **OK**-painike , niin työkirjan rivit täytetään valitun asiakirjan mukaisesti.

    3. Tarkista **Määrä laitur.var.paikassa** -kenttä. 

    4. Valitse **Luo poiminta** -toiminto.
    5. Vahvista kaikki tarvittavat poiminta-asetukset, esimerkiksi ota käyttöön **Per lähtöalue** -vaihto. Valitse **OK**-painike.
    
    Saat vahvistusviestin, jossa on poimintanumerot. On olemassa kaksi poimintaa, koska jotkut kohteet sijaitsevat laiturointialueella, lähellä toimitusaluetta, ja olisi järkevää käsitellä niitä erikseen.

9.  Fyysisen varastoinnin poiminnan rekisteröinti
    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 10.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston poiminnat** ja valitse vastaava linkki.
    2. Etsi luomasi poiminnat ja avaa se.
    3. Valitse **Rekisteröi poiminta** -toiminto.
    4. Toista toisen poiminnan osalta

10. Fyysisen varastoinnin toimituksen kirjaaminen
    
    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 11.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston toimitus** ja valitse vastaava linkki.
    2. Tarkista fyysisen varaston toimituksen sivulla **Rivit**-osa. Kun fyysisen varastoinnin poiminta on rekisteröity, fyysisen varastoinnin toimitus päivitetään määrä **Toimitettava määrä** -kenttä täytettynä.
    3. Valitse **Kirjaa toimitus** -toiminto.
    4. Vahvista **Toimitus**-valinta.


## Tulokset
- **Kirjatut fyysisen varaston vastaanotot** luodaan
- **Rekisteröity fyysisen varaston hyllytys** luodaan    
- **Kirjattu ostovastaanotto** luodaan    
- **ostotilauksen** **vastaanotettu määrä** on päivittynyt vastaanotetuille riveille
- **Rekisteröity fyysisen varaston siirto** luodaan
- **Rekisteröity fyysisen varaston poiminta** luodaan
- **Kirjattu fyysisen varaston toimitus** luodaan
- **Kirjattu myyntitoimitus** luodaan
- **myyntitilauksen** **Toimitettu määrä** on päivittynyt toimitetuille riveille
- nimikkeen **Varasto** kasvaa jäljellä olevalla määrällä, jota ei lähetetä



## Katso myös
[Nimikkeiden vastaanottaminen](../../warehouse-how-receive-items.md) 
[Rakennetiedot: saapuvan fyysisen varastoinnin virta](../../design-details-inbound-warehouse-flow.md) 
[Nimikkeiden lähettäminen](../../warehouse-how-ship-items.md) 
[Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten](../../warehouse-how-to-pick-items-for-warehouse-shipment.md) 
[Rakennetiedot: lähtevän fyysisen varastoinnin virta](../../design-details-outbound-warehouse-flow.md) 
[Nimikkeiden saatavuuden tarkasteleminen](../../inventory-how-availability-overview.md) 
