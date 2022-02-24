---
title: Asiakastietojen siirtäminen | Microsoft Docs
description: Voit siirtää aiemmin luodun asiakkaan tiedot aiemmin luodusta ERP-järjestelmästä Business Centraliin RapidStart Servicesin avulla. Voit käyttää Excelin .xlsx-tiedostoja tiedonkuljettajana. Voit siirtää tiedot manuaalisesti kirjoittamalla ne suoraan yrityksen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 48ce8c293b5af411763a8730c9f7d16113062d9a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186847"
---
# <a name="migrate-customer-data"></a>Asiakastietojen siirtäminen
Voit siirtää aiemmin luodun asiakkaan tiedot aiemmin luodusta ERP-järjestelmästä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin RapidStart Servicesin tietojen siirto-työkalujen avulla . Voit käyttää Excel-tiedostoja tiedonkuljettajana. Voit siirtää tiedot manuaalisesti kirjoittamalla ne suoraan yrityksen.

> [!NOTE]
> BLOB-tyypin kenttiä ei voi viedä tai tuoda Excelin avulla.

**Siirron yleiskuvaus**- ja **Määritä työkirja** -sivut mahdollistavat toimintojen käyttämisen ja kaikkien tietojen siirtoon liittyvien tehtävien suorittamiseen näkymissä. On suositeltavaa siirtää yksi taulukkoo kerrallaan tietojen riippuvuuksien käsittelemiseksi. Siirrossa käytetään myös päätietotaulukoita, jotka sisältävät tietoja asiakkaista, toimittajista, nimikkeistä, kontakteista ja pääkirjanpidosta.  

## <a name="to-import-configuration-packages"></a>Määrityspakettien tuominen
Kun luot uuden yhtiön, voit tuoda yrityksen asetukset uudelle yritykselle. Voit tuoda asetukset .rapidstart-tiedostosta, joka toimittaa paketin sisällön pakatussa muodossa. Vastaava joukko oletustietojen siirtotaulukoita tuodaan. Tietojoukko sisältää pää- ja asetustietotaulukot. Ensimmäinen tehtäväsi tietojen siirrossa on arvioida, vastaavatko siirron oletusasetukset uuden yrityksen tarpeita.

> [!NOTE]  
>  Et voi nimetä uudelleen tiedostoa, joka ei ole jo RapidStart Services kokoonpanopaketti, kuten .rapidstart-kokoonpanopakettitiedosto, ja sitten yrittää tuoda sitä. Jos yrität tehdä tämän, saat virheilmoituksen.  

Varmista ennen aloittamista, että sinulla on oikeudet suorittaa RapidStart Services -objektit. Voit esimerkiksi käyttää SUPER- tai D365 RAPIDSTART-käyttöoikeusjoukkoja. Suosittelemme myös, että olet roolikeskuksessa, jossa on linkkejä RapidStart Servicesiin, kuten hallintaroolikeskuksessa. Lisätietoja on kohdassa [Roolin vaihtaminen](ui-change-basic-settings.md#to-change-the-role).  

> [!IMPORTANT]  
> Kun yrityksen tietokantojen välillä tuodaan tai viedään määrityspaketteja, tietokantojen tulisi noudattaa samaa rakennetta, jotta kaikki tiedot siirtyvät onnistuneesti. Tämä tarkoittaa, että tietokannoilla tulisi olla sama taulukko- ja kenttärakenne, jossa taulukoilla on samat ensisijaiset avaimet ja kentillä on samat tunnukset ja tietotyypit.  
>
>  Tietokannasta, jolla on eri rakenne kuin kohdetietokanta, voi tuoda määrityspaketin. Mitään määrityspaketissa olevia taulukoita tai kenttiä, joita ei löydy kohdetietokannasta, ei kuitenkaan tuoda.
>
> Taulukoita, joilla on poikkeavat ensisijaiset avaimet tai kenttiä, joilla on poikkeavat tietotyypit ei myöskään voi tuoda. Tietoja ei voi tuoda, jos esimerkiksi määrityspaketissa on taulukko **50000 Asiakas**, jonka ensisijainen avain on **Code20**, ja kohdetietokannassa on taulukko **50000 Asiakkaan pankkitili**,jonka ensisijainen avain on **Code20 + Code 20**.  

1. Avaa uusi yritys  
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määrityspaketit** ja valitse sitten liittyvä linkki.  
3. Valitse **Tuo paketti** -toiminto. Siirry tuotavaan rapidstart-paketin tiedostoon ja valitse **Avaa**-toiminto. Tuonnin aikana paketin sisältö puretaan ja paketin tietue luodaan.  

    Kun tuonti on valmis, näet niiden määritystaulukoiden määrän, jotka on tuotu **Taulukoiden määrä** -kentästä.  
4. Voit tarkistaa määritystaulukoiden luettelon valitsemalla **Näytä**-toiminnon.  
5. Voit käyttää pakettia valitsemalla **Käytä pakettia** -toiminnon.  

    > [!NOTE]  
    >  Tietojen siirtotiedot perustuvat kokoonpanomalleihin, jos sellainen on määritetty. Malli pitää ensin päivittää, jotta kenttäluetteloa voidaan muuttaa.  

6.  Voit tarkistaa kenttien valinnat valitsemalla taulukon ja valitsemalla sitten **Rivit**-välilehden **Kentät**-toiminnon. Vertaa ja tarkastele kenttiä, jotka ovat käytettävissä kentille, joiden tietoja on käytetty.  

Jos valitut taulukot eivät vastaa tarpeitasi, voit luoda uusia tietojen siirtotaulukoita. Jos tiedostot ovat riittävät, voit jatkaa tietojen siirtämistä Excel- tai XML-tiedostojen avulla.

## <a name="to-create-a-data-migration-file"></a>Luo siirtotiedosto

Voit luoda uuden tietojen siirron tiedostoja ja mukauttaa niitä liiketoiminnan tukemiseksi.  

> [!TIP]
> Tiedostoa voi kuitenkin käyttää vain sellaisen kentän siirtämisessä, jonka **FieldClass**-ominaisuuden arvoksi on määritetty **Normaali**.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määrityspaketti** ja valitse sitten liittyvä linkki.  
2. Valitse ja avaa paketti, jota haluat käyttää tietojen siirtämisessä. Valitse sitten **Hae taulukot** -toiminto. **Hae pakettitaulukko** -sivu avautuu.  
3. Anna **TableID**-kentässä taulukkonumero tai valitse taulukko luettelosta, esimerkiksi taulukko 18, **Asiakas**. **Taulukon nimi** -kenttä täytetään automaattisesti.  
4. Valitse uusi siirtotaulukko ja valitse sitten **Taulukot**-välilehdessä **Kentät**-toiminto. **Siirtokentät**-sivu avautuu.  
5. Tyhjennä **Sisällytä kenttä** -valintaruutu kaikilta kentiltä, joita ei tuoda. Valitse sitten **Aseta sisällytetty**- tai **Tyhjennä sisällytetty** -toiminto.  

> [!IMPORTANT]  
>  Jos **Sisällytä kenttä** -valintaruutu on valittuna oletusarvon mukaan, tämä kenttä on perusavaimen osa. Valintaa ei tulisi tyhjentää, sillä se aiheuttaa virheitä eikä tietuetta voi tuoda.  
>
>  Jos sisällytät kentän, jolla on suhde toisen taulukon kanssa, **Tarkista kenttä** -valintaruutu valitaan automaattisesti. Vahvistus voi johtaa tämän ja muiden taulukoiden muiden kenttien päivityksiin ja suoritetaan kenttänumerojärjestyksessä.  

Uusi siirtotaulukko luodaan.  

## <a name="to-export-data-migration-files"></a>Vie siirtotiedostot.
Kun olet määrittänyt taulukot, joihin haluat siirtää asiakastietoja, voit viedä tiedostot.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määrityspaketit** ja valitse sitten liittyvä linkki.  
2. Valitse ja avaa paketti, jota haluat käyttää vientiä varten.
3. Valitse vietävä taulukko tai vietävät taulukot ja valitse sitten **Vie Exceliin** -toiminto.
4. Tallenna viety Excel-tiedosto.  
5. Toista nämä vaiheet kaikille asiaankuuluville tiedonsiirtotaulukoille. Jos valitset useita taulukkoja yhdellä kertaa, niiden tiedot viedään yleiseen työkirjaan.  

Jos taulukko on tyhjä, tuloksena saatava tietojen siirtotaulukko sisältää tyhjiä soluja uuden yrityksen siirtotaulukoiden valinnan tai luonnin yhteydessä valittujen kenttien osalta. Jos valittu tietojen siirtotaulukko sisältää tietoja, se viedään.  

## <a name="to-map-values-to-be-used-during-import"></a>Tuonnin aikana käytettävien arvojen yhdistäminen
Kun Excelistä tai RapidStart-paketista tuodut tiedot kohdistetaan, [!INCLUDE[d365fin](includes/d365fin_md.md)] käsittelee yhdistämismääritystä taulun suhteiden perusteella seuraavasti:  

- Jos määrität linkityksen suoraan taulukon kenttään, [!INCLUDE[d365fin](includes/d365fin_md.md)] käyttää sitä.  

- Jos kentässä on suhde toiseen taulukkoon, [!INCLUDE[d365fin](includes/d365fin_md.md)] -haut määritellään yhdistetyn taulukon perusavainkentän yhdistämistä varten. Liittyvän taulukon on oltava määrityspaketin osa.  

- Jos määritystiedot on annettu molemmissa paikoissa, suoraan kenttään ja liittyvän taulun perusavaimeen, [!INCLUDE[d365fin](includes/d365fin_md.md)] etsii molemmista paikoista määrittämistä varten.  

- Jos samat määritykset tehdään suoraan kentälle ja liittyvään taulukkoon, mutta uudet arvot eivät ole samat, suoraan kenttään tehty määritys on etusijalla viittaavan kentän sisältävään taulukkoon tehtyyn määritykseen verrattuna.  

Seuraavissa toimenpiteissä sinun tulisi tarkastaa ennalta mitkä arvot haluat säilyttää siirtoprosessin aikana. Seuraavien vaiheiden suorittaminen edellyttää tietojen siirtotiedostoja (.xlsx), jotka on viety [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmasta. Lisätietoja on kohdassa [Tietojen siirtotiedostojen vieminen](admin-migrate-customer-data.md#to-export-data-migration-files).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määrityspaketit** ja valitse sitten liittyvä linkki.
2. Avaa kyseisen yrityksen määrityspaketti.  
3. Valitse taulukko, johon haluat yhdistää arvoja ja valitse sitten **Taulukot**-välilehden **Kentät**-toiminto.  
4. Valitse jokaiselle yhdistettävälle kentälle **Yhdistämismääritys**-toiminto.  
5. Kirjoita **Vanha arvo** -kenttään arvo, jota haluat muuttaa. Kirjoita **Uusi arvo** -kenttään arvo, joksi haluat muuttaa vanhan arvon. Valitse **OK**-painike.  
6. Tuo asiakkaan tiedot. Lisätietoja on kohdassa [Asiakastietojen tuominen](admin-migrate-customer-data.md#to-import-customer-data).
7. Katso onko **Pakettivirheiden määrä** -kentässä ilmoitettu virheitä. Jos niitä on, poraudu alaspäin, jotta saat virheet näkyviin. **Määritä pakettitietueet** -sivu avautuu.
8. Valitse **Näytä virhe** -toiminto. Näyttöön avautuu seuraava virhe: **XX ei ole kelvollinen vaihtoehto. Kelvolliset vaihtoehdot ovat XX**. Valitse **OK**-painike.  
9. Voit ottaa määrittämäsi yhdistämismäärityksen käyttöön valitsemalla **Käytä tietoja** -toiminnon.  

### <a name="mapping-example"></a>Yhistämismäärityksen esimerkki  
Seuraavassa esimerkissä kuvataan, kuinka [!INCLUDE[d365fin](includes/d365fin_md.md)] toteuttaa yhdistämismääritykset.  

1. Luo määritystaulukko, jolla on **Myyjä/ostaja**-taulukko. Määritä yhdistämismääritys **Koodi**-kenttään.  
2. Lisää pakettiin taulukoita, esimerkiksi **Asiakas** ja **Toimittaja**. Molemmat taulukot viittaavat **Myyjä/ostaja** -taulukkoon **myyjäkoodin** ja **ostajakoodin** kautta.  
3. Kun käytät tietoja, vastaavuusmääritys, joka on annettu **Myyjä/ostaja**-taulukon **Koodi**-kenttään, otetaan huomioon **Myyjäkoodi**- ja **Ostajakoodi**-kentissä.

## <a name="to-add-additional-values-to-d365fin"></a>Uusien arvojen lisääminen [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määrityspaketit** ja valitse sitten liittyvä linkki.  
2. Valitse taulukko, johon haluat lisätä arvoja, ja valitse sitten **Taulukot**-pikavälilehden **Kentät**-toiminto.  
3. Kentille, joille haluat [!INCLUDE[d365fin](includes/d365fin_md.md)]:n sallivan lisäarvoja siirron aikana, valitse **Luo puuttuvat koodit** -valintaruutu.  
4. Tuo asiakkaan tiedot. Lisätietoja on kohdassa [Asiakastietojen tuominen](admin-migrate-customer-data.md#to-import-customer-data).

## <a name="to-clean-up-and-process-data-before-applying-data"></a>Voit tyhjentää ja käsitellä tietoja ennen tietojen käyttämistä
Joissakin tapauksissa haluat ehkä tyhjentää asiakkaan tiedot ja käsitellä ne ennen kuin kohdistat ne tietokantaan. Voit tehdä tämän korjaamalla ongelmat **Määrityspaketti – käsittely** -eräajon avulla seuraavasti:  

- Muuntaa päivämäärät ja desimaalit käyttäjän tietokoneen aluekohtaisten asetusten edellyttämään muotoon.  
- Poista alussa tai lopussa olevat välilyönnit tai erikoismerkit.  

Kun olet suorittanut erätyön, käsittele tiedot seuraavan menettelytavan avulla.  

1. Avaa yrityksen määrityspaketti.  
2. Valitse **Käsittele tiedot** -toiminto.  
3. Voit ottaa määrittämäsi yhdistämismäärityksen käyttöön valitsemalla **Käytä tietoja** -toiminnon.

## <a name="to-migrate-customer-data"></a>Asiakastietojen siirtäminen
Kun olet vienyt siirtotaulukon, seuraava vaihe on asiakkaan vanhoja tietojen antaminen. Yksinkertaistaaksesi tehtäviä voit hyödyntää XML manipulointityökaluja, jotka on sisällytetty Exceliin. Voit käyttää myös Excelin valmiita funktioita tietojen muotoilun auttamiseksi ja tiedon asettamiseksi oikeisiin soluihin.

Jos haluat apua XML:n käytössä, ota käyttöön Excel-valintanauhan **Kehittäjä**-välilehti. Valitse sitten **Lähde**-toiminto, jos haluat nähdä siirtotaulukon XML-mallin Excelin esittämällä tavalla.

Seuraavassa toimenpide perustuu Excel-taulukkoon, jonka olet luonut siirtoa varten. Lisätietoja on kohdassa [Tietojen siirtotiedostojen vieminen](admin-migrate-customer-data.md#to-export-data-migration-files).

> [!IMPORTANT]  
> Älä muuta sarakkeita Excel-työkirjoissa. Jos niitä on siirretty, muutettu tai poistettu, laskentataulukkoa ei voi tuoda [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.

1. Avaa viemäsi datatiedosto Excelissä. Ohjelmassa on työkirja, jossa on taulukon nimi.
2. Nimeä sivu1 uudelleen ilmaisee, että työkirjaa käytetään tietojen siirtämiseen. Kopioi otsikkorivi ilman muotoilua viedystä taulukosta uuteen työkirjaan.
3. Kopioi kolmannessa työkirjassa kaikki asiakastiedot. Anna sivulle nimeksi esimerkiksi Vanhat tiedot.
4. Tee Excel-kaava muunnostyökirjan tietojen määrittämiseksi viedyn työkirjan kenttien ja vanhojen asiakastietojen välillei.
5. Kun olet yhdistänyt kaikki tiedot, kopioi tietoalue taulukon työkirjaan.
6. Tallenna tiedosto ja varmista, että et muuta tiedostotyyppiä.

Olet nyt valmis siirtämään tietojen siirto-tiedostoja, jotka sisältävät asiakkaan vanhat tiedot [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan.

## <a name="to-import-customer-data"></a>Tuo asiakkaan tietoja
Kun asiakkaan tiedot on syötetty siirron tiedostoihin Excelissä, voit tuoda tiedostot [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan.

1. Avaa **Määritä pakettikortti** -sivu.
2. Valitse taulukko, johon haluat tuoda tiedot, ja valitse sitten **Taulukot**-välilehden **Tuo Excelistä** -toiminto.
3. Etsi ja avaa tiedosto, josta haluat tuoda tietoja.
4. Tarkista tuotavat tiedot **Määrityspaketin tuonnin esikatselu** -sivulla.

    **Määrityspaketin tuonnin esikatselu** -sivulla on yleiskatsaus tuotavan Excel-tiedoston sisällöstä. Se ilmaisee myös, onko määrityspaketti juuri luotu vai onko se päivitetty ja onko määrityspaketin rivit (taulukot) luotu vai aiemmin luodut rivit päivitetty.    
5. Valitse **Tuo**-toiminto.

Tiedoston tiedot on tuotu määrityspakettitaulukoihin. **Tietokantatietueiden määrä** -kentässä näet tuotujen tietueiden määrän. Lisäksi voit katsella siirtovirheitä.

## <a name="to-validate-customer-data"></a>Tarkista asiakastiedot
Asiakkaan tiedot on tarkistettava, ennen kuin voit käyttää tietueita [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietokannassa.  

> [!NOTE]  
>  Useimmissa tapauksissa tietokantaan ei luoda virheellisiä tietoja. Sovelluksen toiminta voidaan kuitenkin joskus estää, jos tuotu siirtotaulukko sisältää virheitä.  

1. Tarkista **Siirron yleiskuvaus** -sivun **Siirtovirheiden määrä**-kentästä tuonnin aikana tapahtuneet virheet.  
2. Jos virheitä löytyy, valitse siirtotaulukko ja valitse sitten **Taulukot**-välilehden **Virheet**-toiminto. **Virheellinen**-valintaruutu on merkittynä jokaiselle tietueelle, jossa on virhe.  
3. Tarkastele virheitä valitsemalla rivi ja valitsemalla sitten **Näytä virhe**-toiminto.  

    **Virheteksti**-kenttä sisältää virheen syyn. **Kentän seloste** -kenttä sisältää virheen sisältävän kentän selosteen.  
4.  Voit korjata virheen tai tehdä päivityksen valitsemalla **Siirron yleiskuvaus** -sivu. Valitse **Siirtotietueet**-toiminto ja korjaa virheellinen tietue **Siirtotietueet**-sivulla.  

Kun olet tehnyt korjauksen, tietue poistetaan tietueiden luettelosta **Tiedonsiirtovirheet**-sivulla.  

Olet nyt valmis soveltamaan asiakkaan tietoja tietokantaan.  

## <a name="to-apply-customer-data"></a>Käytä asiakkaan tietoja
Kun olet tuonut kaikki tietojen siirtotietueet, jotka ovat voimassa ja joissa ei ole virheitä, voit käyttää tietueita [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietokannassa.  

1. Avaa **Määrityspaketit**-sivu.  
2. Valitse tietojen siirtotiedostolle taulukko, jota haluat käyttää, ja valitse sitten **Käytä tietoja** -toiminto.

Näet tietokantatietueita, jotka on luotu **Tietokantatietueiden määrä** -kentässä. Varmista, että luodut tiedot olivat oikeat, valitsemalla **Tietokantatietueiden määrä** -kentän linkki.  

Asiakkaan yritystietokanta on nyt valmiiksi asetettu ja perustiedot tuodaan. Seuraavaksi täytäntöönpanoprosessissa on käyttäjien kouluttaminen, prosessien määrittäminen, uusien tietojen luominen, raporttien mukauttaminen jne.

## <a name="see-also"></a>Katso myös  
[Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)
