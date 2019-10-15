---
title: Huoltotilausten kirjaaminen | Microsoft Docs
description: Kun huoltotilaus on luotu, tarpeelliset tiedot on täytetty ja muutokset tehty, huoltotilauksen voi kirjata. Tilauksessa tulee olla vähintään yksi huoltonimikerivi ja yksi huoltorivi, ennen kuin sen voi kirjata. Jos tilaus sisältää useita huoltorivejä, kaikki rivit kirjataan kerralla.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3b9820c9c79efcf340ff6a417a5a8994dcb9db07
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315994"
---
# <a name="post-service-orders-and-credit-memos"></a>Huoltotilausten ja hyvityslaskujen kirjaaminen
Kun huoltotilaus on luotu, tarpeelliset tiedot on täytetty ja muutokset tehty, huoltotilauksen voi kirjata. Tilauksessa tulee olla vähintään yksi huoltonimikerivi ja yksi huoltorivi, ennen kuin sen voi kirjata. Jos tilaus sisältää useita huoltorivejä, kaikki rivit kirjataan kerralla.  

Jos huoltotilauksia on runsaasti, voit säästää aikaa kirjaamalla ne samalla kertaa käyttämällä eräajoa. Voit suorittaa eräajon mistä tahansa huoltotilauksesta.

> [!Tip]
> Ennen huoltoasiakirjan kirjaamista mahdolliset virheet ja puuttuvat tiedot kannattaa tarkistaa **Testiraportti**-toiminnolla. Jos virheitä löytyy, ongelmat on korjattava. Voit tarkistaa korjauksen tulostamalla uuden testiraportin ja kirjata sitten asiakirjan.
  
## <a name="to-post-a-service-order"></a>Huoltotilauksien kirjaaminen    
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Huoltotilaukset** ja valitse sitten liittyvä linkki.  
2. Avaa haluamasi huoltotilaus.  
3. Valitse **Huoltotilaus**-sivulla jompikumpi seuraavista toimista.  
  
    |**Toiminto**|**Tulos**|  
    |------------------|----------------|  
    |**Testiraportti** | Ohjelma tarkastaa kaikki asiakirjan osat ja esittää tuloksen raportissa. Jos raportti ilmaisee virheitä tai puuttuvia tietoja, ongelmat on korjattava. Sen jälkeen voit tulostaa uuden testiraportin.|  
    |**Kirjaa** | Kirjaa tilauksen ilman toimituksen tai laskun tulostamista.|  
    |**Kirjaa ja tulosta** | Kirjaa tilauksen ja tulostaa toimituksen (jos toimitat tilauksen laskuttamatta) tai laskun (jos laskutat tilauksen).|  
    |**Kirjaa erä** | Kirjaa useita huoltotilauksia samalla kertaa.|  
  
4. Tilausta kirjatessa tilauksen kirjaamista varten on määritettävä jokin seuraavista vaihtoehdoista.  
  
    |**Kirjausvaihtoehto**|**Tulos**|  
    |------------------------|----------------|  
    |**Toimitus** | Kirjaa nimikkeiden toimituksen.|  
    |**Lasku** | Laskuttaa nimikkeet, jotka on jo toimitettu.|  
    |**Toimitus ja lasku** | Laskuttaa ja toimittaa nimikkeet.|  
    |**Toimitus ja kulutus** | Ohjelma kirjaa tilauksen toimituksen ja kulutuksen. Se päivittää tilauksen palveluriveille ja aiemmin kirjatulle huoltotoimitusasiakirjaan asianmukaiset määrät.|  
  
Voit kirjata kulutuksen vain, jos rivillä on toimitettu määrä, jota ei ole laskutettu eikä kulutettu.  
  
Ohjelma luo tilauksen kirjauksen yhteydessä vastaavat tapahtumat ja kirjatut asiakirjat. Se myös päivittää huoltotilausasiakirjan asianmukaiset kentät.  

## <a name="to-batch-post-service-orders"></a>Huoltotilauksien eräkirjaaminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** ja valitse sitten liittyvä linkki.  
2. Valitse **Kirjaa erä** -toiminto.  
3.  Voit asettaa suodatuksen valitsemaan tiettyjä huoltotilausnumeroita tai tietyn tilausnumeroiden välin eräajon käsiteltäväksi.  
4.  Käynnistä eräajo valitsemalla **OK**.  

## <a name="to-post-a-service-credit-memo"></a>Huollon hyvityslaskujen kirjaaminen  
Kun olet luonut huoltohyvityslaskun ja täyttänyt sen, voit kirjata hyvityslaskun. Jos ohjelma löytää hyvityslaskusta virheitä tai puuttuvia tietoja kirjauksen aikana, prosessi pysähtyy virhesanomaan.  
   
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huollon hyvityslaskut** ja valitse sitten liittyvä linkki.  
2. Luo uusi huollon hyvityslasku. Valitse **Kotisivu**-välilehden **Uusi**-ryhmässä **Uusi**.  
3. Täytä kentät tarpeen mukaan.  
4. Valitse **Toiminnot**-välilehden **Kirjaus**-ryhmässä **Kirjaa**. Jos haluat tulostaa hyvityslaskun kirjaamisen yhteydessä, valitse edellisen sijaan **Kirjaa ja tulosta**.  
5. Testaa hyvityslaskut ennen kirjausta valitsemalla **Testiraportti**. Kun suoritat raportin, asiakirjaan määritetyt kirjauspäivämäärät tarkistetaan.  
6. Kirjaa useita huollon hyvityslaskuja samalla kertaa. Suorita **Eräkirjaa huollon hyvityslaskut** -eräajon. Tästä voi olla apua, jos kirjattavana on suuri määrä hyvityslaskuja.  
  
> [!NOTE]  
>  On tärkeä syöttää kaikki tarvittavat hyvityslaskujen tiedot ennen erän kirjausta. Muutoin on mahdollista, että niitä ei kirjata. Kun eräajo on lopettanut kirjauksen, näyttöön tuleva viesti ilmoittaa, kuinka monta huoltopalautustilausta on kirjattu.  

## <a name="to-post-consumption-from-a-service-order"></a>Kulutuksen kirjaaminen huoltotilauksesta  
Seuraavassa ohjeessa neuvotaan, miten kirjataan nimikkeet, resurssitunnit ja/tai kulut, joita käytetään huoltotoimenpiteessä, jota ei laskuteta asiakkaalta. Huomaa, että voit kirjata kulutetut nimikkeet, tunnit tai kustannukset vain sellaista kirjattua toimitusta, jolla ei ole kirjattuaj laskuja tai kulutusta.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** ja valitse sitten liittyvä linkki.  
2. Avaa huoltotilaus, jonka kulutuksen haluat kirjata.  
3. Valitse huoltonimike. Valitse ensin **Toiminnot**, sitten **Tilaus** ja lopuksi **Huoltorivit**.  
4. Etsi tarvittavat tapahtumat ja määritä **Laskutettava määrä** -kentässä määrät, joiden kulutuksen kirjaat. Määrä ei voi olla suurempi kuin jo toimitettu määrä ja jäljellä oleva määrä, mutta jota ei ole laskutettu tämän toimituksen osalaskutuksen jälkeen.  
  
    > [!NOTE]  
    >  Jos haluat ohjelman rekisteröivän kulutuksen Projektit-alueelle, täytä huoltorivin **Projektinro**-, **Projektitehtävänro**- ja **Projektin rivityyppi** -kentän arvot.  
  
5. Valitse ensin kirjattavat rivit ja sitten **Kirjaa**-toiminto. Valitse avautuvalla sivulla **Lähetä ja kuluta**.  
  
Huolto kirjataan joko kokonaan tai osittain käytettynä, riippuen **Kulutettava määrä** -kentän arvosta, ja liittyvät päiväkirjamerkinnät luodaan. Lisäksi aiemmin kirjatut huoltotoimitusasiakirjat päivitetään aikajärjestyksessä kulutettujen määrien kanssa. Määrät päivitetään tilauksen huoltoriveillä.  

## <a name="to-post-shipments-from-service-orders"></a>Toimitusten kirjaaminen huoltotilauksista  
Huollon tietojen määrityksen jälkeen voit muuttaa ja kirjata käytettyjen nimikkeiden määrät, käytetyn ajan ja aiheutuneet kustannukset. Tämän jälkeen [!INCLUDE[d365fin](includes/d365fin_md.md)] tekee tarvittavat muutokset varaston nykyisen tilan ja tietyn tilauksen käsittelyn nykyisen tilan mukaan.  
  
Seuraavassa ohjeessa neuvotaan, miten kirjataan toimitus huoltorivin nimikkeille, jotka ovat sijainneissa, joissa ei vaadita varastonhallintaa.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaus** ja valitse sitten liittyvä linkki. 2. Valitse valitun huoltotilauksen sivulla **Toiminnot**, **Tilaus**, **Huoltorivit**.  
3. Etsi pakolliset tapahtumat **Huoltorivit**-sivulla ja määritä kirjattava määrä **Toimitettava määrä** -kenttään.  
  
   > [!NOTE]  
   >  Toimitettavan määrän arvo riippuu siitä, kirjataanko toimitus kokonaan vai osittain. Jos toimitus tehdään kokonaan, **Toimitettava määrä** -kentän arvon ja **Määrä**-kentän arvon on oltava sama. Kun kirjaat osittaisen toimituksen, sinun on määritettävä ensimmäiseksi toimitettava määrä. Jos olet jo toimittanut osan tilauksen huollosta, tee huomautus **Toimitettu määrä** -kentän arvoon. **Toimitettava määrä** -kenttään syötettävä enimmäismäärä on toimittamattomien yksiköiden määrä.  
  
4. Valitse **Toiminnot**, **Kirjaus**, **Kirjaa**. Valitse avautuvalla sivulla **Toimitus**.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] luo tapahtumat (takuu-, nimike-, huolto- tai kirjanpitotapahtuma), luo kirjatun huoltotoimitusasiakirjan ja päivittää huoltotilauksen huoltorivien kentät.  
  
Jos sijainti on määritetty niin, että fyysisen varaston käsittely on pakollinen, huoltonimikerivien toimitus ja siirtäminen tapahtuu samalla tavalla kuin muissa lähdeasiakirjoissa. Ainoa ero on, että huoltorivin nimikkeet voidaan käyttää joko ulkoisesti tai sisäisesti, ja vaativat sen vuoksi kaksi eri vapautustoimintoa.  
  
Lisätietoja huoltorivinimikkeiden toimituksesta laajennetussa varastomäärityksissä on kohdassa [Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten](warehouse-pick-items.md).  

## <a name="to-undo-posted-consumption"></a>Kirjatun kulutuksen kumoaminen  
Voit peruuttaa kulutuksen huoltotilauksissa. Syynä voi olla esimerkiksi vahingossa tehty kirjaus.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut huoltotoimitukset** ja valitse sitten liittyvä linkki.  
2. Avaa kirjattu huoltotoimitus, jolle on kirjattu virheellinen kulutus.  
3. Valitse ensin **Toiminnot**, sitten **Toimitus** ja lopuksi **Huoltotoimitusrivit**.  
4. Valitse ensin virheellisen kulutuksen sisältävät rivit ja sitten **Kumoa kulutus** -toiminto.  
  
 Ohjelma lisää täsmäyttävän huoltotoimitusrivin negatiivisilla arvoilla valittujen rivien määräkenttiin.  
  
> [!NOTE]  
>  Huollon kulutus ei voi kumota, jos  

>    * huoltotilaus on suljettu  
>    * se on kirjattu Projektit-alueelle, joten siihen on linkitetty projektitapahtumia.  
  
## <a name="to-post-service-lines"></a>Huoltorivien kirjaaminen  
Jos huoltotilaukset ovat työn alla huomattavan ajan ennen niiden kirjausta, voit kirjata joitain linkitetyistä huoltoriveistä, jotta voit esimerkiksi pitää varastosi päivitettynä. Voit kirjata määrittämällä määrät kirjattavilla riveillä. Voit valita rivit yksitellen tai valita useita rivejä kerralla.  
  
Seuraavassa ohjeessa neuvotaan, miten toimitus kirjataan suoraan huoltotilauksesta paikoissa, joissa ei ole varastonhallintaa. Jos sijainti on määritetty niin, että fyysisen varaston käsittely on pakollinen, toimituksen kirjaus tapahtuu eri fyysisen varastoinnin asiakirjassa sijainnin asetusten mukaan.
  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** ja valitse sitten liittyvä linkki.  
2. Avaa huoltotilaus ja valitse sitten **Huoltorivit**-toiminto.  
4. Täytä kirjattavien rivien **Toimitettava määrä**-, **Laskutettava määrä**- ja **Kulutettava määrä** -kentät sen mukaan, miten rivit kirjataan.  
5. Valitse **Kirjaa**-toiminto.
  
## <a name="see-also"></a>Katso myös  
[Kirjaaminen huoltohallinnassa](service-service-posting.md)  
[Huoltotilauksen luominen](service-how-to-create-service-orders.md)  
