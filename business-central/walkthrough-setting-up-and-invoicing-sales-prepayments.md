---
title: 'Vaihekuvaus: Myynnin ennakkomaksujen määrittäminen ja laskuttaminen'
description: Ennakkomaksut ovat maksuja, jotka on laskutettu sekä kirjattu myynti- tai ostoennakkomaksun tilaukseen ennen lopullista laskutusta. Voit edellyttää, että ennakkomaksu maksetaan ennen tilattujen tuotteiden valmistamista tai että maksu suoritetaan ennen nimikkeiden toimittamista asiakkaalle. Ennakkomaksutoimintojen avulla voit laskuttaa ja kerätä asiakkailta edellytettyjä talletuksia tai suorittaa talletuksia toimittajille Business Central -sovelluksessa. Näin voit varmistaa, että kaikki maksut kirjataan laskua vastaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/25/2021
ms.author: edupont
ms.openlocfilehash: dacf9e5492f583513e69f2316a0440fce2597269
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216178"
---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Vaihekuvaus: Myynnin ennakkomaksujen määrittäminen ja laskuttaminen

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Ennakkomaksut ovat maksuja, jotka on laskutettu sekä kirjattu myynti- tai ostoennakkomaksun tilaukseen ennen lopullista laskutusta. Voit edellyttää, että ennakkomaksu maksetaan ennen tilattujen tuotteiden valmistamista tai että maksu suoritetaan ennen nimikkeiden toimittamista asiakkaalle. Ennakkomaksutoimintojen avulla voit laskuttaa ja kerätä asiakkailta edellytettyjä talletuksia tai suorittaa talletuksia toimittajille [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa. Näin voit varmistaa, että kaikki maksut kirjataan laskua vastaan.  

Asiakkaalle tai toimittajalle voi määrittää joko kaikkia nimikkeitä tai valittuja nimikkeitä koskevia ennakkomaksuvaatimuksia. Kun olet määrittänyt tarvittavat asetukset, voit luoda osto- ja myyntitilauksista lasketun ennakkomaksun summan mukaisia ennakkomaksulaskuja. Voit muuttaa laskun oletussummia tarvittaessa. Voit myös esimerkiksi lähettää lisäennakkomaksulaskuja, jos tilaukseen esimerkiksi lisätään nimikkeitä.  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta  

Tässä vaihekuvauksessa käsitellään seuraavia tilanteita:  

-  Ennakkomaksujen määrittäminen  
-  Ennakkomaksua edellyttävän tilauksen luominen  
-  Ennakkomaksulaskun luominen  
-  Tilauksen ennakkomaksuvaatimusten korjaaminen  
-  Ennakkomaksujen kohdistaminen tilaukseen  
-  Ennakkomaksun sisältävän tilauksen lopullisen summan laskuttaminen  

### <a name="roles"></a>Roolit

Tässä vaihekuvauksessa on seuraaviin rooleihin liittyviä tehtäviä:  

-  talouspäällikkö (Paula)  
-  tilausten käsittelijä (Susanna)  
-  myyntireskontran hoitaja (Erik).  

## <a name="story"></a>Taustatietoja

 Paula on talouspäällikkö. Hän tekee päätökset asiakkaista, joiden tarvitsee maksaa vakuus, ennen kuin osat valmistetaan tai toimitetaan. Paula määrittää [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman laskemaan ennakkomaksut automaattisesti.  

 Susanna on myyntitilausten käsittelijä. Kun asiakas soittaa tilauksen, hän syöttää tilauksen järjestelmään sillä aikaa kun asiakas on puhelimessa. Tällä tavoin hän voi tarkistaa hinnat ja maksuehdot asiakkaan kanssa välittömästi, ja hän voi tehdä muutoksia järjestykseen, kun hän neuvottelee asiakkaan kanssa.  

 Erik työskentelee kirjanpito-osastolla, jossa hän kirjaa laskuja ja maksuja.  

 Tässä skenaariossa Paula määrittää ennakkomaksuvaatimukset Tinayhtymä Oy:lle kyseisen asiakkaan luottotietojen perusteella ja kertoo Susannalle, miten Tinayhtymä Oy:n tilaukset käsitellään.  

 Kun asiakas soittaa, Sanna neuvottelee asiakkaan kanssa, kunnes he pääsevät sopimukseen. Hän voi sitten halutessaan laskea ennakkomaksun monin eri tavoin.  

 Kun Sanna on lähettänyt ennakkomaksulaskun, asiakas tilaa ylimääräisen nimikkeen. Sanna päivittää tilauksen ja luo toisen ennakkomaksulaskun.  

 Erik rekisteröi asiakkaan maksun, kohdistaa sen laskuihin ja lähettää lopullisen laskun.  

## <a name="setting-up-prepayments"></a>Ennakkomaksujen määrittäminen

Paula määrittää järjestelmän käsittelemään asiakkaiden ennakkomaksut.  

-  Paula päättää, että ennakkomaksuissa käytetään samaa numerosarjaa kuin myyntilaskuissa.  
-  Paula määrittää sovelluksen tarkistamaan ennakkomaksujen tarpeen ennen tilauksen lopullista laskuttamista.  
-  Paula määrittää ennakkomaksujen vaadittavat oletusprosenttiosuudet tiettyjä nimikkeitä ja asiakkaita varten.  

Seuraavissa kohdissa on kuvattu, miten Paulan työtehtävät suoritetaan.  

#### <a name="to-set-up-number-series-for-prepayments"></a>Ennakkomaksujen numerosarjojen määrittäminen

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntien ja myyntisaamisten asetukset** ja valitse sitten liittyvä linkki.  
2.  Laajenna **Myyntien ja myyntisaamisten asetukset** -sivun **Numerosarja**-pikavälilehti.  
3.  Varmista, että kirjattujen ennakkomaksulaskujen numerosarja (**Kirjattujen ennakkomaksulaskujen nrot** -kenttä) on sama kuin kirjattujen myyntilaskujen numerosarja (**Kirjattujen laskujen nrot**) ja että kirjattujen ennakkomaksun hyvityslaskujen numerosarja (**Kirjattujen ennakkomaksun hyvityslaskujen nrot**) on sama kuin kirjattujen hyvityslaskujen numerosarja (**Kirjattujen hyvityslas. nrot**).  

#### <a name="to-block-shipments-for-unpaid-prepayment"></a>Toimitusten estäminen tilanteissa, joissa ennakkomaksuja on jätetty maksamatta

1.  Valitse **Myyntien ja myyntisaamisten asetukset** -sivun **Yleinen**-pikavälilehdessä **Tarkista ennakkomaksu kirjattaessa** -valintaruudussa.

Et voi nyt toimittaa tai laskuttaa tilausta, jossa on maksamaton ennakkomaksu.  

Paula edellyttää, että asiakkaalta 20000 laskutetaan kaikkien tilausten yhteydessä oletusarvoisesti 30 prosentin ennakkomaksu. Hän lisää ennakkomaksun oletusprosenttiosuuden asiakkaan korttiin.  

Paula edellyttää, että kaikilta asiakkailta laskutetaan 20 prosentin ennakkomaksu nimikkeestä 1896-S. Asiakkaan 20000 maksuhistoria on huono, Näin ollen asiakkaalta 20000 edellytetään 40 prosentin ennakkomaksua nimikkeestä 1896-S. Seuraavassa menettelyssä kuvataan, miten ennakkomaksujen oletusprosentit määritetään.  

#### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Ennakkomaksujen oletusprosenttien määrittäminen asiakkaille ja nimikkeille

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.  
2.  Avaa asiakkaan 20000 (Trey Research) kortti.
3.  Lisää **Ennakkomaksuprosentti**-kenttään **30**.  
4.  Valitse **Liittyvät**, valitse **Myynti** ja valitse sitten **Ennakkomaksuprosentit**
5.  Täytä kaksi riviä **Myynnin ennakkomaksuprosentit** -sivulla seuraavasti.  

    |**Myynnin tyyppi**|**Myyntikoodi**|**Nimikkeen nro**|**Ennakkomaksuprosentti**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Asiakas**|**20000**|**1896-S**|**40**|  
    |**Kaikki asiakkaat**| |**1896-S**|**20**|  

    > [!IMPORTANT]  
    >  Maan tai alueen mukaan sinun täytyy myös määrittää veroryhmän koodi **Laskutus**-pikavälilehdellä nimikkeille 1896-S.  

6.  Sulje kaikki sivut.  

#### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Määritä tili myynnin ennakkomaksuille yleisissä kirjausasetuksissa

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleiset kirjausasetukset** ja valitse sitten liittyvä linkki.  
2.  Valitse rivi, jossa **Ylein. liiketoim. kirjausryhmä** -kentän arvoksi on määritetty **KOTIMAAN** ja **Yleinen tuotteen kirjausryhmä** -kentän arvoksi **VÄH.MYYNTI**.  
3.  Määritä **Myynnin ennakkomaksutili** -kentässä asianmukainen tili. Valintasi tallentuu automaattisesti.  

## <a name="creating-an-order-that-requires-a-prepayment"></a>Ennakkomaksua edellyttävän tilauksen luominen

 Seuraavassa tilanteessa Sanna, tilausten käsittelijä, luo tilauksen puhuessaan asiakkaan kanssa. Asiakkaan tilaamat nimikkeen on maksettava ennakkoon, ja asiakkaalla on ollut maksuvaikeuksia aikaisemmin. Sannaa on kehotettu vaatimaan kiinteää summaa **800** tilauksen ennakkomaksuksi.  

Asiakas voi maksaa 35 % esimaksun, johon Sanna voi suostua. Tämän vuoksi hän muuttaa tilausta.  

Susanna luo ennakkomaksulaskun ja lähettää sen asiakkaalle.  

#### <a name="to-create-a-sales-order-with-a-prepayment"></a>Ennakkomaksun sisältävän myyntitilauksen luominen

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Valitse **Asiakasnro**-kenttään **20000**.  
4.  Sulje näyttöön tuleva erääntyvän saldon varoitus.  
5.  Täytä kahdelle myyntiriville seuraavat tiedot:  

    |**Tyyppi**|**Ei.**|**määrä**|  
    |--------------|-------------|------------------|  
    |**Nimike**|**1896-S**|**1**|  
    |**Nimike**|**1900-S**|**1**|

    Myyntirivien ennakkomaksukentät on oletusarvoisesti piilotettu, joten ne on tuotava näkyviin. Sen tehdäksesi sinun on muokattava sivua. Lisätietoja on kohdassa, jossa [Sivun mukauttaminen mukautusvalintanauhan avulla](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

6.  Varmista, että **Ennakkomaksuprosentti**-kentässä rivillä, jossa on nimike **1900-S**, lukee **30**. Tämä oletusarvo on peräisin myynnin tunnistetiedoista, joka on täytetty asiakkaan kortista.  

    **Ennakkomaksuprosentti**-kentässä rivillä, jolla on nimike **1896-S**, lukee **40**. Tämä on prosenttiosuus, jonka olet lisännyt **Myynnin ennakkomaksuprosentit** -sivulla nimikkeelle **1896-S** ja asiakkaalle **20000**.  

    Lisätietoja on ohjeaiheessa [Ennakkomaksujen määrittäminen](finance-set-up-prepayments.md).  
7.  Valitse **Tilaus**-toiminnossa **Tilastotiedot**.  
8.  **Ennakkomaksu**-pikavälilehden **Ennakkomaksun rivisumma ilman ALV:tä** -kenttä sisältää arvon **458.16**. Jos luot nyt tilaukselle ennakkomaksulaskun, tämä summa näkyy laskussa.  

    Tässä skenaariossa Susannaa on ohjeistettu ehdottamaan tilaukselle ennakkomaksua, jonka kokonaissumma on **800**.  

    > [!IMPORTANT]  
    >  Maan/alueen mukaan seuraavat vaiheet eivät ehkä ole käytössä.  
9.  Muuta **Ennakkomaksun rivisumma ilman veroja** -kentän summaksi **800** ja sulje sivu.  
10.  Kun vahvistat myyntirivien **Ennakkomaksuprosentti**-kentän, se lasketaan uudelleen. Uudet summat ovat **67.02438** ja **67.02282**.  

     Uudelleenlaskentaan sisällytetään kaikki rivit, joiden ennakkomaksuprosentti on suurempi kuin 0.  

     Seuraavaksi asiakas kysyy, voidaanko ennakkomaksuprosentiksi sopia 35 %. Sannan valvoja hyväksyy muutoksen.
11.  Syötä **Myyntitilaus**-sivun **Ennakkomaksu**-pikavälilehden **Ennakkomaksuprosentti**-kenttään **35**.  
12.  Valitse näyttöön tulevassa varoituksessa **Kyllä**. 35 % sovelletaan koko tilaukseen maksuprosenttina.  
13.  Vahvista, että rivit on päivitetty asianmukaisesti.  

## <a name="creating-a-prepayment-invoice"></a>Ennakkomaksulaskun luominen  
Kun Susanna on lisännyt oikean ennakkomaksuarvon tilaukseen, hän luo ennakkomaksulaskun ja lähettää sen asiakkaalle.  

#### <a name="to-create-a-prepayment-invoice"></a>Ennakkomaksulaskun luominen

1.  Valitse **Myyntitilaus**-sivulla **Toiminnot**, sitten **Kirjaus**, sitten **Ennakkomaksu** ja valitse sitten **Kirjaa ja tulosta ennakkomaksulasku**
2.  Kirjaa lasku valitsemalla **Kyllä**-painike.  

> [!NOTE]  
>  Susanna valitsee **Kirjaa ja tulosta ennakkomaksulasku** ja lähettää laskun asiakkaalle.  

## <a name="creating-an-additional-prepayment-invoice"></a>Ylimääräisen ennakkomaksulaskun luominen

Seuraavana päivänä asiakas soittaa Susannalle ja tekee muutoksia tilaukseen. Asiakas haluaisi kaksi kappaletta nimikettä 1100. Susanna avaa tilauksen uudelleen, päivittää tilauksen, luo tilaukselle toisen ennakkomaksulaskun ja lähettää sen asiakkaalle.  

#### <a name="to-create-an-additional-prepayment-invoice"></a>Ylimääräisen ennakkolaskumaksun luominen

1.  Valitse **Myyntitilaus**-sivulla **Vapauta**-toiminto ja sitten **Avaa uudelleen**.  
2.  Syötä nimikkeen **1896-S** kentässä **Määrä** arvoksi **2**.  

    Valitse **Tilaus**-toiminnossa **Tilastotiedot**. **Ennakkomaksun rivin summa ilman ALV:tä** -kenttä sisältää nyt **768.04**, ja **Laskutettu ennakkomaksun summa ilman ALV:tä** -kenttä sisältää **417.76**. Tämä osoittaa, että on ylimääräinen ennakkomaksun määrä, jota ei ole vielä laskutettu.  
3.  Kirjaa ylimääräinen ennakkomaksun summa valitsemalla **Toiminnot**, sitten **Kirjaus**, sitten **Ennakkomaksu** ja sitten valitse **Kirjaa ja tulosta ennakkomaksulasku**.
4.  Kirjaa lasku valitsemalla **Kyllä**-painike.  

## <a name="applying-the-prepayments"></a>Ennakkomaksujen kohdistaminen  
Asiakas maksaa ennakkomaksusumman, ja kirjanpito-osastolla työskentelevä Erik rekisteröi maksun ja kohdistaa sen ennakkomaksulaskuihin.  

#### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Maksun kohdistaminen ennakkomaksulaskuihin

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kassapäiväkirjat** ja valitse sitten liittyvä linkki.  
2.  Täytä päiväkirjan rivi seuraavilla tiedoilla:  

    |Kentän nimi|Syötä|  
    |----------------|-----------|  
    |**Asiakirjatyyppi**|**Maksu**|  
    |**Tilityyppi**|**Asiakas**|  
    |**Tilinro**|**20000**|  
3.  Valitse **Prosessi**-toiminto ja sitten **Kohdista tapahtumat**.  
4.  Valitse **Kohdista asiakastapahtumat** -sivulla ensimmäinen ennakkomaksulasku, valitse **Prosessi**-toiminto ja sitten **Aseta kohdistustunniste**.  
5.  Toista edellinen vaihe toista ennakkomaksua varten.  
6.  Valitse **OK**-painike.  

    Summakentässä on nyt kahden ennakkomaksulaskun summa.  

7.  Kirjaa päiväkirja valitsemalla **Kirjaa/tulosta**-toiminto ja sitten **Kirjaa**.
8.  Valitse **Kyllä**-painike.

## <a name="invoicing-the-remaining-amount"></a>Jäljellä olevan summan laskuttaminen

Erikille on nyt ilmoitettu, että tilauksen nimikkeet on toimitettu ja että tilaus on valmis laskutettavaksi. Erik luo tilauksen laskun.  

#### <a name="to-invoice-the-remaining-amount"></a>Jäljellä olevan summan laskuttaminen

1.  Avaa myyntitilaus.
2.  Valitse **Kirjaus**-toiminto ja sitten **Kirjaa**.
3.  Valitse **Toimitus ja lasku** ja sitten **OK**-painike.
4.  Jos haluat esikatsella laskun, valitse **Kyllä**-painike.

> [!NOTE]  
>  Tavallisesti toimituksesta vastaava osasto olisi jo kirjannut toimituksen.  

Arto näkee historiasta, että myyntilasku on luotu tarkoituksellisesti.

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kirjatut myyntilaskut** ja valitse sitten liittyvä linkki.  

## <a name="next-steps"></a>Seuraavat vaiheet

Tässä vaihekuvauksessa käsiteltiin vaiheita, joita noudattamalla [!INCLUDE[prod_short](includes/prod_short.md)] määritetään käsittelemään ennakkomaksuja. Asiakkaiden ja nimikkeiden ennakkomaksujen oletusprosenttien määrittäminen havainnollistettiin ja useita tilauksen ennakkomaksujen laskentatapoja käytiin läpi. Mukana oli myös tilanne, jossa tilaukseen pyrittiin määrittämään yksi ennakkomaksun kokonaissumma, jonka jälkeen ohjelma määritettiin laskemaan ennakkomaksusumma koko tilauksen prosenttiosuutena.  

Vaihekuvauksessa käsiteltiin myös ennakkomaksulaskun kirjaamista, toisen ennakkomaksulaskun luomista tilauksen muuttumiseen jälkeen sekä jäljellä olevan summan lopullisen laskun kirjaamista.  

[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman ennakkomaksutoiminnolla voit vaivattomasti määrittää sekä valvoa asiakkaiden ja nimikkeiden ennakkomaksusääntöjä. Ennakkomaksutoiminnon ansiosta voit myös kohdistaa jokaisen maksun laskuun.  

## <a name="see-also"></a>Katso myös  
[Ennakkomaksujen laskuttaminen](finance-invoice-prepayments.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
