---
title: Toimituksen lupaamisen päivämäärien laskeminen
description: 'Toimituksen lupaamisen toiminto on työkalu, jolla lasketaan aikaisin mahdollinen päivämäärä, jolloin nimike on saatavilla toimitettavaksi tai lähetettäväksi.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 03/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="calculate-order-promising-dates"></a>Toimituksen lupaamisen päivämäärien laskeminen

Yrityksen on voitava ilmoittaa asiakkailleen tilauksen toimituksen päivämäärät. Voit tehdä tämän **Toimituksen lupaamisen rivit** -sivulla myyntitilauksesta.  

[!INCLUDE[prod_short](includes/prod_short.md)] laskee lähetys- ja toimituspäivämäärät tuotteen tunnettujen ja odotettavissa olevien saatavuuspäivien perusteella, jotka voit luvata asiakkaille.  

Jos määrität pyydetyn toimituspäivämäärän myyntitilausrivillä, kyseistä päivämäärää käytetään lähtökohtana seuraaville laskelmille:  

- Pyydetty toimituspvm - Toimitusaika = Suunniteltu lähetyspvm  
- Suunniteltu toimituspvm - Lähtevä f.var. käsittelyaika = Toimituspäivä  

Jos nimikkeet ovat poimittavissa lähetyspäivämääränä, myyntiprosessi voi jatkua. Jos nimikkeet eivät ole poimittavissa lähetyspäivämääränä, näyttöön tulee varastoloppu-varoitus.  

Jos et ole määrittänyt pyydettyä toimituspäivämäärää myyntitilausrivillä tai jos toimitus ei onnistu pyydettynä toimituspäivämääränä, ohjelma laskee varhaisimman päivämäärän, jolloin nimikkeet ovat saatavilla. Tämä päivämäärä annetaan sitten rivin **Toimituspvm**-kenttään. Nimikkeille lasketaan suunniteltu lähetyspäivämäärä ja päivämäärä, jolloin ne toimitetaan asiakkaalle, seuraavilla laskutoimituksilla:  

- Suunniteltu toimituspvm = lähtevä f.var. käsittelyaika + toimituspäivä  
- Suunniteltu toimituspvm + toimitusaika = suunniteltu toimituspvm  

## <a name="about-order-promising"></a>Tietoja toimituksen lupaamisesta

Toimituksen lupaamistoiminnon ansiosta voidaan luvata, että tilaus lähetetään tai toimitetaan tiettynä päivänä. Ohjelma laskee päivämäärän, jolloin nimike on luvattavissa tai mahdollinen luvattavaksi, ja se luo tilausrivejä niille päivämäärille, jotka hyväksyt. Toiminto laskee aikaisimman mahdollisen päivämäärän, jolloin nimike on saatavilla toimitusta tai lähetystä varten. Se luo myös hankintarivit hyväksytyille päivämäärille siinä tapauksessa, että nimikkeitä on ensin tuotettava tai ostettava.

[!INCLUDE[prod_short](includes/prod_short.md)] käyttää kahta peruskäsitettä:  

- Luvattavissa (ATP)  
- Mahdollinen luvattavaksi (CTP)  

### <a name="available-to-promise"></a>Luvattavissa

Luvattavissa (ATP) laskee päivämäärät varausjärjestelmän mukaan. Se suorittaa varaston varaamattomien määrien saatavuustarkistuksen suunnitellun tuotannon, ostojen, siirtojen ja myyntipalautusten varalta. [!INCLUDE[prod_short](includes/prod_short.md)] laskee näiden tietojen perusteella asiakkaan tilauksen toimituspäivämäärän, koska nimikkeet ovat käytettävissä joko varastossa tai suunnitelluissa vastaanotoissa.  

### <a name="capable-to-promise"></a>Mahdollinen luvattavaksi

Mahdollinen luvattavaksi (CTP) olettaa entä jos -esimerkkitilanteen, joka koskee vain nimikemääriä, jotka eivät ole varastossa tai aikataulutetuissa tilauksissa. [!INCLUDE[prod_short](includes/prod_short.md)] laskee tämän skenaarion perusteella varhaisimman päivämäärän, jolloin nimike voi olla käytettävissä, jos se tuotetaan, ostetaan tai siirretään.

#### <a name="example"></a>Esimerkki

Jos tilauksen määrä on 10 kpl ja varastossa tai aikatauluteissa tilauksissa on saatavana 6 kpl, Mahdollinen luvattavaksi -laskennan perustana on 4 kpl.

### <a name="calculations"></a>Laskelmat

Kun [!INCLUDE[prod_short](includes/prod_short.md)] laskee asiakkaan toimituspäivän, se suorittaa kaksi tehtävää:  

- Laskee aikaisimman toimituspäivän, kun asiakas ei ole pyytänyt tiettyä toimituspäivämäärää.  
- Tarkistaa, onko asiakkaan pyytämä tai asiakkaalle luvattu toimituspäivämäärä realistinen.  

Jos asiakas ei pyydä tiettyä toimituspäivämäärää, toimituspäivämääräksi määritetään käsittelypäivämäärä. Saatavuus perustuu tähän päivämäärään. Jos nimike on varastossa, [!INCLUDE[prod_short](includes/prod_short.md)] ajoittaa tilauksen toimitusajankohdan tulevaisuuteen. Tämä toteutetaan seuraavilla kaavoilla:  

- Toimituspvm + Lähtevä f.var. käsittelyaika= Suunniteltu toimituspvm  
- Suunniteltu lähetyspvm + Toimitusaika = Suunniteltu toimituspvm  

[!INCLUDE[prod_short](includes/prod_short.md)] tarkistaa sitten, onko laskettu toimituspäivä mahdollinen laskemalla ajassa taaksepäin, milloin nimikkeen on oltava saatavissa, jotta luvattu päivämäärä toteutuisi. Tämä toteutetaan seuraavilla kaavoilla:  

- Suunniteltu lähetyspvm + Toimitusaika = Suunniteltu toimituspvm  
- Suunniteltu toimituspvm - Lähtevä f.var. käsittelyaika= Toimituspvm  

Toimituspäivää käytetään saatavuuden tarkistuksessa. Jos nimike on saatavana kyseisenä päivänä, [!INCLUDE[prod_short](includes/prod_short.md)] vahvistaa, että pyydetty tai luvattu toimitus voidaan tehdä suunniteltuna toimituspäivämääränä. Se onnistuu määrittämällä pyydetty luvattu toimituspäivämäärä suunnitelluksi toimituspäivämääräksi. Jos nimike ei ole saatavana, se palauttaa tyhjän päivämäärän ja tilausten käsittelijä voi käyttää CTP-toiminnallisuutta.  

Perustuen uusiin päivämääriin ja kellonaikoihin, kaikki liittyvät päivämäärät lasketaan kaavoilla, jotka on lueteltu aiemmin tässä osassa. CTP-laskenta kestää kauemmin, mutta se antaa tarkan päivämäärän, jona asiakas voi odottaa nimikkeen toimitusta. CTP-arvosta lasketut päivämäärät näkyvät **Toimituksen lupaamisen rivit** -sivun **Suunniteltu toimituspvm**- ja **Aikaisin lähetyspvm** -kentissä.  

Tilausten käsittelijä päättää CTP-prosessin hyväksymällä päivämäärät. Tämä tarkoittaa sitä, että nimikkeelle luodaan suunnittelutyökirjan rivi ja varaustapahtuma ennen laskettuja päivämääriä sen varmistamiseksi, että tilaus voidaan toteuttaa.  

**Toimituksen lupaamisen rivit** -sivulla suoritettavan ulkoisen toimituksen lupaamisen lisäksi voit luvata tuoterakenteen nimikkeille myös sisäisiä tai ulkoisia päivämääriä. Lisätietoja on kohdassa [Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md).

## <a name="to-set-up-order-promising"></a>Toimituksen lupaamisen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimituksen lupaamisen asetuk.** ja valitse sitten vastaava linkki.  
2. Syötä **Offset (Aika)** -kenttään numero ja aikayksikön koodi. Valitse yksi seuraavista koodeista:  

    |Koodi|Kuvaus|  
    |----------|-----------------|  
    |**d**|Kalenteripäivä|  
    |**w**|Viikko|  
    |**m**|Kuukausi|  
    |**q**|Vuosineljännes|  
    |**v**|Vuosi|  

    Esimerkiksi "3vi" osoittaa offset-ajan olevan kolme viikkoa. Voit osoittaa nykyistä aikayksikköä kirjoittamalla etuliitteeksi "n" mille tahansa edellä mainituista koodeista. Jos haluat offset-ajan olevan esimerkiksi nykyinen kuukausi, kirjoita **nk**.  
3. Anna **Toimituksen lupaamisen nrot** -kenttään numerosarja valitsemalla rivi **Nrosarjat**-sivun luettelosta.  
4. Anna **Toimituksen lupaamisen malli** -kenttään toimituksen lupaamisen malli valitsemalla rivi **Hankintalistan mallien luett.** -sivun luettelosta.  
5. Anna **Toimituk. lupaamisen työkirja** -kenttään hankintalista valitsemalla rivi **Hankintalistojen nimet** -sivun luettelosta.

### <a name="inbound-and-outbound-warehouse-handling-times-in-order-promising"></a>Saapuvan ja lähtevän fyysisen varastoinnin käsittelyajat toimituksen lupaamisen aikana

Jos haluat sisällyttää varaston käsittelyajan ostorivin tilauslupaavaan laskelmaan, **Varaston asetukset** -sivulla voit määrittää oletuskäsittelyn ajan myynti- ja ostotositteisiin käytettäväksi. Voit myös määrittää kullekin sijainnille tietyt ajat **Sijaintikortti**-sivulla. 

#### <a name="to-enter-default-inbound-and-outbound-warehouse-handling-times-for-sales-and-purchase-documents"></a>Saapuvien ja lähtevien varastointien oletuskäsittelyaikojen syöttäminen myynti- ja ostoasiakirjoihin

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastonhallinnan asetukset** ja valitse sitten vastaava linkki.  
2. Syötä **Yleinen**-pikavälilehden **Saapuva f. var. käsittelyaika**- ja **Lähtevä f. var. käsittelyaika** -kenttiin päivien lukumäärä, jonka haluat ohjelman sisällyttävän tilauksen lupaamisen laskentaan.  

#### <a name="to-enter-inbound-and-outbound-warehouse-handling-times-on-locations"></a>Saapuvan ja lähtevän fyysisen varastoinnin käsittelyaikojen syöttäminen sijainteihin

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainti** ja valitse sitten vastaava linkki.  
2.  Avaa käsiteltävä sijainnin kortti.  
3.  Syötä **Fyysinen varasto** -pikavälilehden **Saapuva f. var. käsittelyaika**- ja **Lähtevä f. var. käsittelyaika** -kenttiin päivien lukumäärä, jonka haluat ohjelman sisällyttävän tilauksen lupaamisen laskentaan.  

> [!NOTE]  
>  Kun luot ostotilausta, valitse **Toimitus ja maksu** -pikavälilehden **Lähetys**-kentässä **Sijainti** ja valitse sitten sijainti **Sijaintikoodi**-kentässä, **Lähtevä f. var. käsittelyaika** ja **Saapuva f. var. käsittelyaika** -kentät käyttävät sijainnille määritettyä käsittelyaikaa. Myyntitilausten osalta sama pätee, jos valitset sijainnin **Sijaintikoodi**-kentässä. Jos sijainnille ei ole määritetty käsittelyaikaa, **Lähtevä f. var. käsittelyaika** ja **Saapuva f. var. käsittelyaika** -kentät ovat tyhjiä. Jos jätät **Sijaintikoodi**-kentän tyhjäksi osto- ja myyntiasiakirjoissa, laskennassa käytetään **Varastonhallinnan asetukset** -sivulla määritettyä käsittelyaikaa.

## <a name="to-make-an-item-critical"></a>Nimikkeen määritteleminen kriittiseksi

Nimike on merkittävä kriittiseksi, ennen kuin sen voi sisällyttää toimituksen lupaamislaskentaan. Tämä asetus varmistaa, etteivät ei-kriittiset nimikkeet aiheuta turhia toimituksen lupaamislaskutoimituksia.   
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2.  Avaa oikea nimikkeen kortti.  
3.  Valitse **Suunnittelu**-pikavälilehdessä **Kriittinen**-kenttä.  

## <a name="to-calculate-an-order-promising-date"></a>Toimituksen lupaamisen päivämäärän laskeminen

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaus** ja valitse sitten vastaava linkki.  
2.  Avaa asianmukainen myyntitilaus ja valitse myyntitilausrivit, jotka haluat sovelluksen laskevan.  
3.  Valitse ensin **Toimituksen lupaaminen** -toiminto ja sitten **toimituksen lupaamisen rivit** -toiminto.  
4.  Valitse ensin rivi ja sitten jokin seuraavista vaihtoehdoista:  

    - Valitse **Luvattavissa**, jos haluat ohjelman laskevan aikaisimman päivämäärän, jolloin nimike on saatavilla varaston, aikataulutettujen vastaanottojen ja bruttotarpeiden osalta.  
    - Valitse **Mahdollinen luvattavaksi**, jos tiedät, että nimikettä ei ole nyt varastossa, ja jos haluat ohjelman laskevan aikaisimman päivämäärän, jolloin nimike voi olla saatavilla, lähettämällä uusia täydennyshankintoja.  
5.  Valitse **Hyväksy** -painike hyväksyäksesi aikaisimman mahdollisimman lähetyspäivämäärän.  

## <a name="see-also"></a>Katso myös

[Myynti](sales-manage-sales.md)  
[Ostojen päivämäärien laskeminen](purchasing-date-calculation-for-purchases.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
