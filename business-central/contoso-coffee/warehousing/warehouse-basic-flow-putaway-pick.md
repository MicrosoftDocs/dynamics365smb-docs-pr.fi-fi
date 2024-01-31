---
title: 'Vastaanotto, hyllytys, poiminta ja toimitus fyysisen varastoinnin perusmäärityksissä'
description: Business Central -sovelluksessa saapuvat ja lähtevät prosessit voidaan suorittaa neljällä eri tavalla varastotason monimutkaisuuden mukaan.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Vaihekuvaus: Saapuva ja lähtevä työnkulku fyysisen varaston perusmäärityksissä

Tässä vaihekuvauksessa kuvataan, miten saapuvat ja lähtevät virrat suoritetaan kohdassa perustiedot: tilauskohtainen konfiguraatio. Lisätietoja on kohdassa [Erilaisten määritysvaihtoehtojen yleiskatsaus](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## Vaatimukset  
Tämän vaihekuvauksen suorittaminen edellyttää, että teet itsestäsi fyysisen varastoinnin työntekijän *HOPEA*-sijainnissa noudattamalla seuraavia ohjeita:  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston työntekijät** ja valitse sitten vastaava linkki.  
2. Valitse ensin **Käyttäjätunnus**-kenttä ja valitse oma käyttäjätilisi **Käyttäjät**-sivulla.  
3. Kirjoita **Sijaintikoodi**-kenttään *HOPEA*.  

## Saapuva työnkulku: Vastaanotto ja hyllytys fyysisen varastoinnin perusmäärityksissä

[!INCLUDE[prod_short](../../includes/prod_short.md)]issa vastaanoton ja hyllytyksen saapuvat prosessit voidaan suorittaa neljällä tavalla eri toimintojen avulla varastotason monimutkaisuuden mukaan.  

|Tapa|Saapuva prosessi|Varastopaikat|Vastaanotot|Hyllytykset|Monimutkaisuustaso (katso [Rakennetiedot: Fyysisen varaston asetukset](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|L|Vastaanoton ja hyllytyksen kirjaaminen tilausriviltä|X|||2|  
|B|Vastaanoton ja hyllytyksen kirjaaminen varaston hyllytysasiakirjasta|||X|3|  
|N|Kirjaa vastaanotto ja hyllytys fyysisen varastoinnin vastaanottoasiakirjasta||X||4/5/6|  
|P|Kirjaa vastaanotto fyysisen varastoinnin vastaanottoasiakirjasta ja kirjaa hyllytys varaston hyllytysasiakirjasta||X|X|4/5/6|  

Lisätietoja on kohdassa [Rakennetiedot: Saapuvan fyysisen varastoinnin virta](../../design-details-inbound-warehouse-flow.md).  

Seuraavassa vaihekuvauksessa kuvataan edellisen taulukon menetelmää B.  

### Skenaario  
Alicia, ostaja, luo ostotilauksen erilaisille paahdetuille pavuille. Kun toimitus saapuu varastoon, Joakim, varastotyöntekijä, asettaa nimikkeet pois sopiviin varastopaikkoihin. Kun Joakim kirjaa hyllytyksen, nimikkeet kirjataan vastaanotetuksi varastoon, ja ne ovat käytettävissä myyntiä tai muita kysyntää varten.  

### Vaiheet
1. **Sijaintikortti**-sivun asetuksissa määritetään yrityksen saapuvat varastointityönkulut.  

    1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
    2.  Avaa asianmukaisen *HOPEA*-sijainnin kortti.  
    3.  Valitse **Vaadi hyllytys** -valintaruutu.  

2. Määritä oletusvarastopaikka nimikkeelle määrittääksesi sen hyllytyspaikan

    1.  Valitse **Varastopaikat**-toiminto **sijaintikortissa**
    2.  Valitse varastopaikan *S-1-01* ensimmäinen rivi ja valitse sitten **Sisältö**-toiminto.  
    3.  Valitse **Uusi**-toiminto.  
    4.  Valitse **Kiinteä**- ja **Oletus**-kentät.  
    5.  Anna **Nimikenro**-kentässä *WRB-1000*.  

3. Luo ostotilaus, joka on yleisin saapuvien lähdeasiakirjojen tyyppi.  

    1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.  
    2.  Valitse **Uusi**-toiminto.  
    3.  Luo ostotilaus toimittajalle 10000 seuraavien ostontilausrivien kanssa. Käytä mukautustyökaluja, jos **Varastopaikan koodi** -kenttä ei ole näkyvissä. Lisätietoja on kohdassa [Työtilan mukauttaminen](../../ui-personalization-user.md). 

    |Nimike|Sijaintikoodi|Varastopaikan koodi|määrä|  
    |----------|----------|---------|--------------|  
    |WRB-1000|HOPEINEN|S-1-01|20|  
    |WRB-1001|HOPEINEN||30|

    Ensimmäisen varastopaikan koodi täytetään määrityksen mukaan. Toisen nimikkeen varastopaikan koodi on tyhjä, koska sillä ei ole oletusarvoja. Pidä se tällä tavalla.  

    4.  Valitse **Vapauta**-toiminto ja ilmoita varastolle, että ostotilaus on valmis varaston käsittelyyn, kun toimitus saapuu.  

4. Luo **Varaston hyllytys** vastaanottamaan ja asettamaan toimitetut nimikkeet pois  

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston hyllytykset** ja valitse sitten vastaava linkki.  
    2. Valitse **Uusi**-toiminto. 
    3. Valitse **Sijaintikoodi**-kentässä *HOPEA*.
    4. Valitse ensin **Lähdeasiakirja**-kenttä ja sitten **Ostotilaus**.  
    5. Valitse **Lähteen nro** -kentästä toimittajan 10000 oston rivi ja täytä sitten hyllytysrivit valitun lähdeasiakirjan mukaan valitsemalla **OK**.

        Vaihtoehtoisesti voit valita ensin **Hae lähdeasiakirja** -toiminnon ja sitten ostotilauksen.  

5. Muokkaa varaston hyllytystä nimikkeiden todellisen asettamisen ja kirjauksen perusteella

    Hyllyttäessään nimikkeitä varastopaikkoihin Joakim huomasi, että oletusvarastopaikassa on jo joitain nimikkeitä, joten hän päätti käyttää toista varastopaikkaa. Joakim sijoittaa myös muita nimikkeitä varastopaikkoihin, koska vastaanotettu määrä ei mahdu kapasiteettiin.

    1. Ensimmäisen rivin muutos **Varastopaikan koodi** kohteesta *S-1-01*, joka kopioitiin ostotilauksesta kohteeseen *S-1-02*. 
    2.  Syötä 20 varaston hyllytyksen rivin **Käsiteltävä määrä** -kenttään nimikkeellä WBR-1000.  
    3. Syötä toiselle riville 20 **Käsiteltävä määrä** -kenttään ja valitse **Jaa rivi** -toiminto. Näyttöön tulee uusi rivi, joka on muuten identtinen kopio alkuperäisestä rivistä, mutta sen **Käsiteltävä määrä** -kentässä on alkuperäiseltä riviltä poistamasi määrä. 
    4. Täytä nimikkeen WBR-1001 varastopaikkojen koodit:

    |Nimike|Varastopaikan koodi|määrä|  
    |----------|-------------------|--------------|  
    |WRB-1001|S-1-03|20|  
    |WRB-1001|S-1-04|10|

    5.  Valitse ensin **Kirjaa**-toiminto, sitten **Vastaanotto**-toiminto ja lopuksi **OK**.  

### Tulokset 
 - paahdetut pavut on nyt rekisteröity hyllytettynä määritellyissä varastopaikoissa
 - **Kirjattu varastohyllytys** luodaan
 - **Kirjattu ostovastaanotto** luodaan
 - ostotilauksen **vastaanotettu määrä** on päivittynyt vastaanotetuille riveille
 - **Varasto**-nimike kasvaa valitulla määrällä
    

## Lähtevä virta: Poiminta ja toimitus fyysisen varastoinnin perusmäärityksissä

[!INCLUDE[prod_short](../../includes/prod_short.md)] -ohjelmassa noudon ja toimituksen lähtevät prosessit voidaan suorittaa neljällä tavalla käyttämällä eri toimintoja varastotason monimutkaisuudesta riippuen.  

|Tapa|Saapuva prosessi|Varastopaikat|Poiminnat|Toimitukset|Monimutkaisuustaso (katso [Rakennetiedot: Fyysisen varaston asetukset](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|L|Poiminnan ja toimituksen kirjaaminen tilausriviltä|X|||2|  
|B|Poiminnan ja toimituksen kirjaaminen varaston poiminta-asiakirjasta||X||3|  
|N|Kirjaa poiminta ja lähetyksen fyysisen varastoinnin toimituksen asiakirjasta|||X|4/5/6|  
|P|Poiminnan kirjaaminen fyysisen varastoinnin poiminta-asiakirjasta ja toimituksen kirjaaminen fyysisen varastoinnin toimituksen asiakirjasta||X|X|4/5/6|  

Katso lisätietoja kohdasta [Rakennetiedot: lähtevän fyysisen varastoinnin virta](../../design-details-outbound-warehouse-flow.md).  

Seuraavassa vaihekuvauksessa kuvataan edellisen taulukon menetelmää B.

### Skenaario  
Tilauksen käsittelijä Susanna luo myyntitilauksen erilaisia paahdettuja papuja varten ja siirtää sen varastoon. Johnin, varastotyöntekijän, täytyy varmistaa, että lähetys on valmisteltu ja toimitettu asiakkaalle. John hallitsee kaikkia **Varaston poiminta** -sivulla olevia tehtäviä, jotka viittaavat automaattisesti varastopaikkoihin, joissa nimikettä paahdettuja papuja varastoidaan.

### Vaiheet
Tämä on jatkoa kohteelle [Saapuva työnkulku: Vastaanotto ja hyllytys fyysisen varastoinnin perusmäärityksissä](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. **Sijaintikortti**-sivun asetuksissa määritetään yrityksen saapuvat varastointityönkulut.  

    1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 5.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
    2.  Avaa asianmukaisen *HOPEA*-sijainnin kortti.  
    3.  Valitse **Vaadi poiminta** -valintaruutu.  

2. Luo myyntitilaus, joka on yleisin lähtevien lähdeasiakirjojen tyyppi.  

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 6.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
    2. Valitse **Uusi**-toiminto.  
    3. Luo asiakkaalle 10000 myyntitilaus käyttäen seuraavaa myyntitilausriviä.  

    |Nimike|Sijaintikoodi |määrä|  
    |----|-------------|--------|  
    |WRB-1000|HOPEINEN|20|  
    |WRB-1001|HOPEINEN|30|  

    Varastopaikkojen koodit täytetään automaattisesti oletusvarastopaikoilla.

    4. Valitse **Luo varaston hyllytys/poiminta/siirto** -toiminto.
    5. Valitse **Luo varaston poiminta** -valintaruutu.  
    6. Valitse **OK**-painike. Uusi varaston poiminta luodaan.

3. Nimikkeiden poiminta ja lähettäminen

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 7.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston poiminnat** ja valitse sitten vastaava linkki.  
    2. Valitse varaston poiminta asiakkaalle 10000
    
    Luotu varaston poiminta ohitti varastopaikan, joka on määritelty nimikkeelle *WRB-1000*, koska se ei sisällä varastoa, ja käytti toista varastopaikkaa. Toinen rivi, jolla on nimike *WRB-1001*, jakaantui automaattisesti poimimaan useista varastopaikoista.
    
4. Valitse **Täytä autom. käsitelt. määrä** -toiminto.  

5. Valita ensin **Kirjaa**-toiminto, sitten **Toimitus** ja lopuksi **OK**.  

### Tulokset
 - paahdetut pavut on nyt rekisteröity poimittuina määritellyissä varastopaikoissa
 - **Kirjattu varastopoiminta** luodaan
 - **Kirjattu myyntitoimitus** luodaan
 - myyntitilauksen **Toimitettu määrä** on päivittynyt toimitetuille riveille
 - **Varasto**-nimike pienenee valitulla määrällä


## Katso myös
[Hyllytysnimikkeet ja varaston hyllytykset](../../warehouse-how-to-put-items-away-with-inventory-put-aways.md) 
[Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) 
[Rakennetiedot: saapuvan fyysisen varastoinnin virta](../../design-details-inbound-warehouse-flow.md) 
[Nimikkeiden poiminta varastopoiminnalla](../../warehouse-how-to-pick-items-with-inventory-picks.md) 
[Rakennetiedot: lähtevän fyysisen varastoinnin virta](../../design-details-outbound-warehouse-flow.md) 
[Nimikkeiden saatavuuden tarkasteleminen](../../inventory-how-availability-overview.md) 
