---
title: Toimituksen lupaamisen päivämäärän laskeminen | Microsoft Docs
description: Toimituksen lupaamisen toiminto on työkalu, jolla lasketaan aikaisin mahdollinen päivämäärä, jolloin nimike on saatavilla toimitettavaksi tai lähetettäväksi. Toiminnolla luodaan myös hankintarivejä hyväksymillesi päivämäärille.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2cc3fd679909e51422afe75ee4a1436f5ad8cb9c
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788998"
---
# <a name="calculate-order-promising-dates"></a>Toimituksen lupaamisen päivämäärien laskeminen
Yrityksen on voitava ilmoittaa asiakkailleen tilauksen toimituksen päivämäärät. Voit tehdä tämän **Toimituksen lupaamisen rivit** -sivulla myyntitilauksen riviltä.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] laskee heti nimikkeen tunnettujen ja oletettujen päivämäärien perusteella toimitus- ja lähetyspäivämäärät, jotka voidaan sitten luvata asiakkaalle.  

Jos määrität pyydetyn toimituspäivämäärän myyntitilausrivillä, kyseistä päivämäärää käytetään lähtökohtana seuraaville laskelmille:  

- Pyydetty toimituspvm - Toimitusaika = Suunniteltu lähetyspvm  
- Suunniteltu toimituspvm - Lähtevä f.var. käsittelyaika = Toimituspäivä  

Jos nimikkeet ovat poimittavissa lähetyspäivämääränä, myyntiprosessi voi jatkua. Jos nimikkeet eivät ole poimittavissa lähetyspäivämääränä, näyttöön tulee varastoloppu-varoitus.  

Jos et ole määrittänyt pyydettyä toimituspäivämäärää myyntitilausrivillä tai jos toimitus ei onnistu pyydettynä toimituspäivämääränä, ohjelma laskee varhaisimman päivämäärän, jolloin nimikkeet ovat saatavilla. Tämä päivämäärä annetaan sitten rivin **Toimituspvm**-kenttään. Nimikkeille lasketaan suunniteltu lähetyspäivämäärä ja päivämäärä, jolloin ne toimitetaan asiakkaalle, seuraavilla laskutoimituksilla:  

- Suunniteltu toimituspvm = lähtevä f.var. käsittelyaika + toimituspäivä  
- Suunniteltu toimituspvm + toimitusaika = suunniteltu toimituspvm  

## <a name="about-order-promising"></a>Tietoja toimituksen lupaamisesta
Toimituksen lupaamistoiminnon ansiosta voidaan luvata, että tilaus lähetetään tai toimitetaan tiettynä päivänä. Ohjelma laskee päivämäärän, jolloin nimike on luvattavissa tai mahdollinen luvattavaksi, ja se luo tilausrivejä niille päivämäärille, jotka hyväksyt. Toiminto laskee aikaisimman mahdollisen päivämäärän, jolloin nimike on saatavilla toimitusta tai lähetystä varten. Se luo myös hankintarivit hyväksytyille päivämäärille siinä tapauksessa, että nimikkeiden on oltava ensin ostoja.

[!INCLUDE[d365fin](includes/d365fin_md.md)] käyttää kahta peruskäsitettä:  

- Luvattavissa (ATP)  
- Mahdollinen luvattavaksi (CTP)  

### <a name="available-to-promise"></a>Luvattavissa  
Luvattavissa (ATP) laskee päivämäärät varausjärjestelmän mukaan. Se suorittaa varaston varaamattomien määrien saatavuustarkistuksen suunnitellun tuotannon, ostojen, siirtojen ja myyntipalautusten varalta. [!INCLUDE[d365fin](includes/d365fin_md.md)] laskee näiden tietojen perusteella automaattisesti asiakkaan tilauksen toimituspäivämäärän, koska nimikkeet ovat käytettävissä joko varastossa tai suunnitelluissa vastaanotoissa.  

### <a name="capable-to-promise"></a>Mahdollinen luvattavaksi  
Mahdollinen luvattavaksi (CTP) olettaa entä jos -esimerkkitilanteen, joka koskee vain nimikemääriä, jotka eivät ole varastossa tai aikataulutetuissa tilauksissa. [!INCLUDE[d365fin](includes/d365fin_md.md)] laskee tämän skenaarion perusteella varhaisimman päivämäärän, jolloin nimike voi olla käytettävissä, jos se tuotetaan, ostetaan tai siirretään.

#### <a name="example"></a>Esimerkki
Jos tilauksen määrä on 10 kpl ja varastossa tai aikatauluteissa tilauksissa on saatavana 6 kpl, Mahdollinen luvattavaksi -laskennan perustana on 4 kpl.

### <a name="calculations"></a>Laskelmat  
Kun [!INCLUDE[d365fin](includes/d365fin_md.md)] laskee asiakkaan toimituspäivän, se suorittaa kaksi tehtävää:  

- Laskee aikaisimman toimituspäivän, kun asiakas ei ole pyytänyt tiettyä toimituspäivämäärää.  
- Tarkistaa, onko asiakkaan pyytämä tai asiakkaalle luvattu toimituspäivämäärä realistinen.  

Jos asiakas ei pyydä tiettyä toimituspäivämäärää, toimituspäivämääräksi määritetään käsittelypäivämäärä. Saatavuus perustuu tähän päivämäärään. Jos nimike on varastossa, [!INCLUDE[d365fin](includes/d365fin_md.md)] ajoittaa tilauksen toimitusajankohdan tulevaisuuteen. Tämä toteutetaan seuraavilla kaavoilla:  

- Toimituspvm + Lähtevä f.var. käsittelyaika= Suunniteltu toimituspvm  
- Suunniteltu lähetyspvm + Toimitusaika = Suunniteltu toimituspvm  

[!INCLUDE[d365fin](includes/d365fin_md.md)] tarkistaa sitten, onko laskettu toimituspäivä mahdollinen laskemalla ajassa taaksepäin, milloin nimikkeen on oltava saatavissa, jotta luvattu päivämäärä toteutuisi. Tämä toteutetaan seuraavilla kaavoilla:  

- Suunniteltu lähetyspvm + Toimitusaika = Suunniteltu toimituspvm  
- Suunniteltu toimituspvm - Lähtevä f.var. käsittelyaika= Toimituspvm  

Toimituspäivää käytetään saatavuuden tarkistuksessa. Jos nimike on saatavana kyseisenä päivänä, [!INCLUDE[d365fin](includes/d365fin_md.md)] vahvistaa, että pyydetty tai luvattu toimitus voidaan tehdä suunniteltuna toimituspäivämääränä. Se onnistuu määrittämällä pyydetty luvattu toimituspäivämäärä suunnitelluksi toimituspäivämääräksi. Jos nimike ei ole saatavana, se palauttaa tyhjän päivämäärän ja tilausten käsittelijä voi käyttää CTP-toiminnallisuutta.  

Perustuen uusiin päivämääriin ja kellonaikoihin, kaikki liittyvät päivämäärät lasketaan kaavoilla, jotka on lueteltu aiemmin tässä osassa. CTP-laskenta kestää kauemmin, mutta se antaa tarkan päivämäärän, jona asiakas voi odottaa nimikkeen toimitusta. CTP-arvosta lasketut päivämäärät näkyvät **Toimituksen lupaamisen rivit** -sivun **Suunniteltu toimituspvm**- ja **Aikaisin lähetyspvm** -kentissä.  

Tilausten käsittelijä päättää CTP-prosessin hyväksymällä päivämäärät. Tämä tarkoittaa sitä, että nimikkeelle luodaan suunnittelutyökirjan rivi ja varaustapahtuma ennen laskettuja päivämääriä sen varmistamiseksi, että tilaus voidaan toteuttaa.  

**Toimituksen lupaamisen rivit** -sivulla suoritettavan ulkoisen toimituksen lupaamisen lisäksi voit luvata tuoterakenteen nimikkeille myös sisäisiä tai ulkoisia päivämääriä. Lisätietoja on kohdassa [Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md).

## <a name="to-set-up-order-promising"></a>Toimituksen lupaamisen määrittäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Toimituksen lupaamisen asetuk.** ja valitse sitten liittyvä linkki.  
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

### <a name="to-enter-inbound-warehouse-handling-time-in-the-inventory-setup-page"></a>Saapuvan fyysisen varastoinnin käsittelyajan antaminen varastonhallinnan asetussivulla  
Jos haluat ohjelman sisällyttävän saapuvan fyysisen varastoinnin käsittelyajan ostorivin toimituksen lupaamisen laskentaan, voit määrittää sen oletusarvoksi varastolle ja sijainnille.    
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastonhallinnan asetukset** ja valitse sitten liittyvä linkki.  
2. Syötä **Yleinen**-pikavälilehden **Saapuva f. var. käsittelyaika** -kenttään päivien lukumäärä, jonka haluat ohjelman sisällyttävän tilauksen lupaamisen laskentaan.  

> [!NOTE]  
>  Jos olet täyttänyt **Saapuva f. var. käsittelyaika** -kentän **sijaintikortissa** sijaintisi osalta, ohjelma käyttää kyseisen kentän sisältöä oletusarvoisena saapuvan fyysisen varastoinnin käsittelyaikana.  

### <a name="to-enter-inbound-warehouse-handling-time-on-location-cards"></a>Saapuvan fyysisen varastoinnin käsittelyajan syöttäminen sijaintikortteihin  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sijainti** ja valitse sitten liittyvä linkki.  
2.  Avaa käsiteltävä sijainnin kortti.  
3.  Syötä **Fyysinen varasto**-pikavälilehden **Saapuva f. var. käsittelyaika** -kenttään päivien lukumäärä, jonka haluat ohjelman sisällyttävän tilauksen lupaamisen laskentaan.  

> [!NOTE]  
>  Jos jätät **Saapuva f. var. käsittelyaika** -kentän tyhjäksi, laskennassa käytetään **Varastonhallinnan asetukset** -sivulla olevaa arvoa.

### <a name="to-enter-outbound-warehouse-handling-time-in-the-inventory-setup-page"></a>Lähtevän fyysisen varastoinnin käsittelyajan antaminen varastonhallinnan asetussivulla  
Jos haluat määrittää lähtevän fyysisen varastoinnin käsittelyajan sisällytettäväksi myyntirivin toimituksen lupaamisen laskentaan, voit määrittää tämän oletusarvoksi varastolle.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastonhallinnan asetukset** ja valitse sitten liittyvä linkki.  
2. Syötä **Yleinen**-pikavälilehden **Lähtevä f. var. käsittelyaika** -kenttään päivien lukumäärä, jonka haluat ohjelman sisällyttävän tilauksen lupaamisen laskentaan.  

> [!NOTE]  
>  Jos olet täyttänyt **Lähtevä f. var. käsittelyaika** -kentän sijaintikortissa sijaintisi osalta, ohjelma käyttää kyseisen kentän sisältöä oletusarvoisena lähtevän fyysisen varastoinnin käsittelyaikana.  

### <a name="to-enter-outbound-warehouse-handling-time-on-location-cards"></a>Lähtevän fyysisen varastoinnin käsittelyajan syöttäminen sijaintikortteihin  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sijainnit** ja valitse sitten liittyvä linkki.  
2.  Avaa käsiteltävä sijainnin kortti.  
3.  Syötä **Fyysinen varasto**-pikavälilehden **Lähtevä f. var. käsittelyaika** -kenttään päivien lukumäärä, jonka haluat ohjelman sisällyttävän tilauksen lupaamisen laskentaan.  

> [!NOTE]  
>  Jos jätät **Lähtevä f. var. käsittelyaika** -kentän tyhjäksi, laskennassa käytetään **Varastonhallinnan asetukset** -sivulla olevaa arvoa.

## <a name="to-make-an-item-critical"></a>Nimikkeen määritteleminen kriittiseksi  
Nimike on merkittävä kriittiseksi, ennen kuin sen voi sisällyttää toimituksen lupaamislaskentaan. Tämä asetus varmistaa, etteivät ei-kriittiset nimikkeet aiheuta turhia toimituksen lupaamislaskutoimituksia.   
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.  
2.  Avaa oikea nimikkeen kortti.  
3.  Valitse **Suunnittelu**-pikavälilehdessä **Kriittinen**-kenttä.  

## <a name="to-calculate-an-order-promising-date"></a>Toimituksen lupaamisen päivämäärän laskeminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntitilaus** ja valitse sitten liittyvä linkki.  
2.  Avaa asianmukainen myyntitilaus ja valitse myyntitilausrivit, jotka haluat sovelluksen laskevan.  
3.  Valitse ensin **Toimituksen lupaaminen** -toiminto ja sitten **toimituksen lupaamisen rivit** -toiminto.  
4.  Valitse ensin rivi ja sitten jokin seuraavista vaihtoehdoista:  

    - Valitse **Luvattavissa**, jos haluat ohjelman laskevan aikaisimman päivämäärän, jolloin nimike on saatavilla varaston, aikataulutettujen vastaanottojen ja bruttotarpeiden osalta.  
    - Valitse **Mahdollinen luvattavaksi**, jos tiedät, että nimikettä ei ole nyt varastossa, ja jos haluat ohjelman laskevan aikaisimman päivämäärän, jolloin nimike voi olla saatavilla, lähettämällä uusia täydennyshankintoja.  
5.  Valitse **Hyväksy** -painike hyväksyäksesi aikaisimman mahdollisimman lähetyspäivämäärän.  

## <a name="see-also"></a>Katso myös  
[Myynti](sales-manage-sales.md)  
[Ostojen päivämäärälaskenta](purchasing-date-calculation-for-purchases.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
