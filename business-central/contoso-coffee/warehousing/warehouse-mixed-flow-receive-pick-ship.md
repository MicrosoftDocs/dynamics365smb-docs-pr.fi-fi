---
title: 'Vastaanotto, hyllytys, poiminta ja toimitus fyysisen sekavaraston perusmäärityksissä'
description: Business Central -sovelluksessa saapuvat ja lähtevät prosessit voidaan suorittaa neljällä eri tavalla varastotason monimutkaisuuden mukaan.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Vaihekuvaus: Saapuva ja lähtevä työnkulku fyysisen sekavaraston perusmäärityksissä

Tässä vaihekuvauksessa kuvataan, miten saapuvat ja lähtevät työnkulut suoritetaan sekakokoonpanossa, jossa saapuvalle työnkululle varasto määritetään Perus: tilauksittain ja lähtevälle työnkululle käytetään lisäkonfiguraatiota. Lisätietoja on kohdassa [Erilaisten määritysvaihtoehtojen yleiskatsaus](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## Vaatimukset  
Tämän vaihekuvauksen suorittaminen edellyttää, että teet itsestäsi fyysisen varastoinnin työntekijän *KELTAINEN*-sijainnissa noudattamalla seuraavia ohjeita:  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston työntekijät** ja valitse sitten vastaava linkki.  
2. Valitse ensin **Käyttäjätunnus**-kenttä ja valitse oma käyttäjätilisi **Käyttäjät**-sivulla.  
3. Kirjoita **Sijaintikoodi**-kenttään *KELTAINEN*.  

## Saapuva työnkulku: Vastaanotto ja hyllytys fyysisen varastoinnin perusmäärityksissä

[!INCLUDE[prod_short](../../includes/prod_short.md)]issa vastaanoton ja hyllytyksen saapuvat prosessit voidaan suorittaa neljällä tavalla eri toimintojen avulla varastotason monimutkaisuuden mukaan.  

|Tapa|Saapuva prosessi|Varastopaikat|Vastaanotot|Hyllytykset|Monimutkaisuustaso (katso [Rakennetiedot: Fyysisen varaston asetukset](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|L|Vastaanoton ja hyllytyksen kirjaaminen tilausriviltä|X|||2|  
|B|Vastaanoton ja hyllytyksen kirjaaminen varaston hyllytysasiakirjasta|||X|3|  
|N|Kirjaa vastaanotto ja hyllytys fyysisen varastoinnin vastaanottoasiakirjasta||X||4/5/6|  
|P|Kirjaa vastaanotto fyysisen varastoinnin vastaanottoasiakirjasta ja kirjaa hyllytys varaston hyllytysasiakirjasta||X|X|4/5/6|  

Lisätietoja on kohdassa [Rakennetiedot: Saapuvan fyysisen varastoinnin virta](../../design-details-inbound-warehouse-flow.md).  

Seuraavassa vaihekuvauksessa kuvataan edellisen taulukon menetelmää C.  

### Skenaario  
Alicia, ostaja, luo ostotilaukset erilaisille paahdetuille pavuille kysynnän mukaan. Kun yhdistetty toimitus saapuu varastoon, Joakim, varastotyöntekijä, vastaanottaa ja laittaa nimikkeet pois. Kun Joakim kirjaa vastaanoton, nimikkeet kirjataan vastaanotetuksi varastoon, ja ne ovat käytettävissä myyntiä tai muita kysyntää varten.  

### Vaiheet
1. **Sijaintikortti**-sivun asetuksissa määritetään yrityksen saapuvat varastointityönkulut.  

    1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
    2.  Avaa *KELTAINEN*-sijaintikortti.  
    3.  Poista käytöstä **Vaadi hyllytys** -vaihtopainike.  

2. Vapauta ostotilaukset fyysiseen varastoon.  

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.  
    2. Valitse toimittajan 10000 tilaukset KELTAINEN-sijainnissa. Toimittajatilausten numerot ovat *Y-1* ja *Y-2*. Käytä mukautustyökaluja, jos **Toimittajan tilausnumero** -kenttä ei ole näkyvissä. Lisätietoja on kohdassa [Työtilan mukauttaminen](../../ui-personalization-user.md).
    3. Valitse **Vapauta**-toiminto ja ilmoita varastolle, että valitut ostotilaukset ovat valmiit varaston käsittelyyn, kun toimitus saapuu.  

3. Luo fyysisen varastoinnin vastaanotto vastaanottamaan ja laittamaan toimitetut nimikkeet pois
    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston vastaanotot** ja valitse vastaava linkki.
    2. Valitse **Uusi**-toiminto
    3. Paina fyysisen varastoinnin vastaanotto -sivulla ENTER-näppäintä, jos haluat, että fyysisen varastoinnin vastaanottonumero valitaan automaattisesti
    4. Syötä **sijaintikoodi** *keltaisena*.
    5. Valitse **Hae lähdeasiakirjat...** -toiminto
    6. Valitse toimittajalta 10000 aiemmin vapautetut ostotilaukset ja valitse **OK**-painike.
        Riveillä on uusi tapahtuma kullekin ostotilausriville.

4. Muuta vastaanotettava määrä vastaanotetun määrän ja kirjatun asiakirjan perusteella
    1. Valitse rivi, jonka nimike on *WRB-1000*.
    2. Valitse *OVERRCPT10* **Vastaanoton ylittävän määrän koodi** -kentässä ja muuta **Vastaanotettava määrä** -kentän arvo arvosta *100* arvoon *110*.
    3. Valitse rivi, jonka nimike on *WRB-1001* ja 
    4. Toisella rivillä muuta **Vastaanotettava määrä** -kentän arvo arvosta *200* arvoon *190*.
    5. Valitse **Kirjaa vast.otto** -toiminto.

### Tulokset 
 - paahdetut pavut ovat nyt rekisteröity hyllytetyiksi
 - **Kirjatut fyysisen varaston vastaanotot** luodaan
 - **Kirjattu ostovastaanotto** luodaan
 - ostotilauksen **vastaanotettu määrä** on päivittynyt vastaanotetuille riveille
 - **Varasto**-nimike kasvaa valitulla määrällä
    

## Lähtevä virta: Poiminta ja toimitus fyysisen varastoinnin laajennetuissa määrityksissä

[!INCLUDE[prod_short](../../includes/prod_short.md)] -ohjelmassa noudon ja toimituksen lähtevät prosessit voidaan suorittaa neljällä tavalla käyttämällä eri toimintoja varastotason monimutkaisuudesta riippuen.  

|Tapa|Saapuva prosessi|Varastopaikat|Poiminnat|Toimitukset|Monimutkaisuustaso (katso [Rakennetiedot: Fyysisen varaston asetukset](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|L|Poiminnan ja toimituksen kirjaaminen tilausriviltä|X|||2|  
|B|Poiminnan ja toimituksen kirjaaminen varaston poiminta-asiakirjasta||X||3|  
|N|Kirjaa poiminta ja lähetyksen fyysisen varastoinnin toimituksen asiakirjasta|||X|4/5/6|  
|P|Poiminnan kirjaaminen fyysisen varastoinnin poiminta-asiakirjasta ja toimituksen kirjaaminen fyysisen varastoinnin toimituksen asiakirjasta||X|X|4/5/6|  

Katso lisätietoja kohdasta [Rakennetiedot: lähtevän fyysisen varastoinnin virta](../../design-details-outbound-warehouse-flow.md).  

Seuraavassa vaihekuvauksessa kuvataan edellisen taulukon menetelmää D.

### Skenaario  
Tilauksen käsittelijä Susanna luo myyntitilaukset erilaisia paahdettuja papuja varten ja siirtää sen varastoon. Koska kaikki tilaukset ovat peräisin samalta asiakkaalta, Ellen, varastopäällikkö päättää toimittaa ne yhdessä. Johnin, varastotyöntekijän, täytyy varmistaa, että lähetys on valmisteltu ja toimitettu asiakkaalle.

### Vaiheet
Tämä on jatkoa kohteelle [Saapuva työnkulku: Vastaanotto ja hyllytys fyysisen varastoinnin perusmäärityksissä](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Vapauta myyntitilaukset fyysiseen varastoon.  

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 5.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
    2. Valitse asiakkaan 10000 tilaukset KELTAINEN-sijainnissa. Ulkoisen tilauksen numerot ovat *Y-3*, *Y-4* ja *Y-5*.
    3. Valitse **Vapauta**-toiminto, joka ilmoittaa varastolle, että valitut myyntitilaukset ovat valmiit fyysisen varastoinnin käsittelyä varten.  

2. Nimikkeiden toimittaminen  
    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 6.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston toimitukset** ja valitse sitten vastaava linkki.  
    2. Valitse **Uusi**-toiminto.  
    3. Kirjoita **Sijaintikoodi**-kenttään *KELTAINEN*.  
    4. Valitse **Käytä suodat. kun haet lähd.d** -toiminto.  
    5. Kirjoita **Koodi**-kenttään **CUST10000**.  
    6. Kirjoita **Kuvaus**-kenttään **Asiakas 10000**.  
    7. Valitse **Muokkaa**-toiminto.  
    8. Määritä **Myynti** -pikavälilehden **Tilausasiakkaan nro suodatus** -kentässä *10000*.  
    9. Valitse **Aja**-toiminto. 
    
    Fyysisen varastoinnin toimitukseen tulee neljä riviä, jotka edustavat määritetyn asiakkaan myyntitilausrivejä. **Toimitettava määrä** -kenttä on tyhjä, koska nimikkeet tulee poimia ensin.

3. Luo fyysisen varastoinnin poiminta fyysisen varastoinnin toimituksesta
    1. Valitse f. varastoinnin toimitus -sivulla **Luo poiminta** -toiminto.
    2. Vahvista kaikki tarvittavat poiminta-asetukset, esimerkiksi valitse *Nimike* **Järjestämistapa aktiviteettiriveille** -kentässä, jos haluat ryhmitellä samat nimikkeet yhteen. Valitse **OK**-painike.
    3. Saat vahvistusviestin, jossa on poimintanumero. 

4. Ava fyysisen varaston poiminta
    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 7.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston poiminnat** ja valitse vastaava linkki.
    2. Etsi luomasi poiminta ja avaa se.
    3. Päivitä **Käsiteltävä määrä** tarvittaessa.
    4. Valitse **Rekisteröi poiminta** -toiminto.
    5. F. varastoinnin poiminta suljetaan ja poistetaan, jos kaikki määrät on käsitelty.

5. Fyysisen varastoinnin toimituksen kirjaaminen
   1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 8.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston toimitukset** ja valitse sitten vastaava linkki.  
   2. Etsi aiemmin luomasi toimitus ja avaa se.
    Huomaa, että **Toimitettava määrä** on täytetty.
    3. Voit tarvittaessa päivittää kohdat **Kirjauspvm**, **Ulkoisen asiakirjan nro**, **Kuljetusliikkeen koodi**, **Toimitustapa**. Muut kuin tyhjät arvot välitetään lähdeasiakirjoihin.
    4. Valitse **Kirjaa toimitus** -toiminto.
    5. Vahvista **Toimitus**-valinta.

### Tulokset
 - paahdetut pavut ovat nyt rekisteröity poimituiksi 
 - **Rekisteröity fyysisen varaston poiminta** luodaan
 - **Kirjattu fyysisen varaston toimitus** luodaan
 - kolme **Kirjattua myyntitoimitusta** luodaan
 - myyntitilauksen **Toimitettu määrä** on päivittynyt toimitetuille riveille
 - **Varasto**-nimike pienenee valitulla määrällä


## Katso myös
[Nimikkeiden vastaanottaminen](../../warehouse-how-receive-items.md)
[Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)
[Rakennetiedot: saapuvan fyysisen varastoinnin virta](../../design-details-inbound-warehouse-flow.md)
[Nimikkeiden lähettäminen](../../warehouse-how-ship-items.md)
[Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten](../../warehouse-how-to-pick-items-for-warehouse-shipment.md)
[Rakennetiedot: lähtevän fyysisen varastoinnin virta](../../design-details-outbound-warehouse-flow.md)
[Nimikkeiden saatavuuden tarkasteleminen](../../inventory-how-availability-overview.md)
