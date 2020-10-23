---
title: Vaihekuvaus – Myynnin ennakkomaksujen määrittäminen ja laskuttaminen | Microsoft Docs
description: Ennakkomaksut ovat maksuja, jotka on laskutettu ja kirjattu myynti- tai ostoennakkomaksun tilaukseen ennen lopullista laskutusta. Voit edellyttää, että ennakkomaksu maksetaan ennen tilattujen tuotteiden valmistamista tai että maksu suoritetaan ennen nimikkeiden toimittamista asiakkaalle. Ennakkomaksutoimintojen avulla voit laskuttaa ja kerätä asiakkailta edellytettyjä talletuksia tai suorittaa talletuksia toimittajille Business Central -sovelluksessa. Näin voit varmistaa, että kaikki maksut kirjataan laskua vastaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e94bef3f127d52ca7ee5c7e31f0f126e57b44210
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914808"
---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Vaihekuvaus: Myynnin ennakkomaksujen määrittäminen ja laskuttaminen

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

Ennakkomaksut ovat maksuja, jotka on laskutettu sekä kirjattu myynti- tai ostoennakkomaksun tilaukseen ennen lopullista laskutusta. Voit edellyttää, että ennakkomaksu maksetaan ennen tilattujen tuotteiden valmistamista tai että maksu suoritetaan ennen nimikkeiden toimittamista asiakkaalle. Ennakkomaksutoimintojen avulla voit laskuttaa ja kerätä asiakkailta edellytettyjä talletuksia tai suorittaa talletuksia toimittajille [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa. Näin voit varmistaa, että kaikki maksut kirjataan laskua vastaan.  

 Asiakkaalle tai toimittajalle voi määrittää joko kaikkia nimikkeitä tai valittuja nimikkeitä koskevia ennakkomaksuvaatimuksia. Kun olet määrittänyt tarvittavat asetukset, voit luoda osto- ja myyntitilauksista lasketun ennakkomaksun summan mukaisia ennakkomaksulaskuja. Voit muuttaa laskun oletussummia tarvittaessa. Voit myös esimerkiksi lähettää lisäennakkomaksulaskuja, jos tilaukseen esimerkiksi lisätään nimikkeitä.  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta  
 Tässä vaihekuvauksessa käsitellään seuraavia tilanteita:  

-   Ennakkomaksujen määrittäminen  
-   Ennakkomaksua edellyttävän tilauksen luominen  
-   Ennakkomaksulaskun luominen  
-   Tilauksen ennakkomaksuvaatimusten korjaaminen  
-   Ennakkomaksujen kohdistaminen tilaukseen  
-   Ennakkomaksun sisältävän tilauksen lopullisen summan laskuttaminen  

### <a name="roles"></a>Roolit  
 Tässä vaihekuvauksessa on seuraaviin rooleihin liittyviä tehtäviä:  

-   talouspäällikkö (Paula)  
-   tilausten käsittelijä (Susanna)  
-   myyntireskontran hoitaja (Erik).  

## <a name="story"></a>Taustatietoja  
 Paula on talouspäällikkö. Hän tekee päätökset asiakkaista, joiden tarvitsee maksaa vakuus, ennen kuin osat valmistetaan tai toimitetaan. Paula määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman laskemaan ennakkomaksut automaattisesti.  

 Susanna on myyntitilausten käsittelijä. Kun asiakas soittaa tilauksen, hän syöttää tilauksen järjestelmään sillä aikaa kun asiakas on puhelimessa. Tällä tavoin hän voi tarkistaa hinnat ja maksuehdot asiakkaan kanssa välittömästi, ja hän voi tehdä muutoksia järjestykseen, kun hän neuvottelee asiakkaan kanssa.  

 Erik työskentelee kirjanpito-osastolla, jossa hän kirjaa laskuja ja maksuja.  

 Tässä skenaariossa Paula määrittää ennakkomaksuvaatimukset Tinayhtymä Oy:lle kyseisen asiakkaan luottotietojen perusteella ja kertoo Susannalle, miten Tinayhtymä Oy:n tilaukset käsitellään.  

 Kun asiakas soittaa, Sanna neuvottelee asiakkaan kanssa, kunnes he pääsevät sopimukseen. Hän voi sitten halutessaan laskea ennakkomaksun monin eri tavoin.  

 Kun Sanna on lähettänyt ennakkomaksulaskun, asiakas tilaa ylimääräisen nimikkeen. Sanna päivittää tilauksen ja luo toisen ennakkomaksulaskun.  

 Erik rekisteröi asiakkaan maksun, kohdistaa sen laskuihin ja lähettää lopullisen laskun.  

## <a name="setting-up-prepayments"></a>Ennakkomaksujen määrittäminen  
 Paula määrittää järjestelmän käsittelemään asiakkaiden ennakkomaksut.  

-   Paula päättää, että ennakkomaksuissa käytetään samaa numerosarjaa kuin myyntilaskuissa.  
-   Paula määrittää sovelluksen tarkistamaan ennakkomaksujen tarpeen ennen tilauksen lopullista laskuttamista.  
-   Paula määrittää ennakkomaksujen vaadittavat oletusprosenttiosuudet tiettyjä nimikkeitä ja asiakkaita varten.  

Seuraavissa kohdissa on kuvattu, miten Paulan työtehtävät suoritetaan.  

#### <a name="to-set-up-number-series-for-prepayments"></a>Ennakkomaksujen numerosarjojen määrittäminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntien ja myyntisaamisten asetukset** ja valitse sitten liittyvä linkki.  
2.  Laajenna **Myyntien ja myyntisaamisten asetukset** -sivun **Numerointi**-pikavälilehti.  
3.  Varmista, että kirjattujen ennakkomaksulaskujen numerosarja (**Kirjattujen ennakkomaksulaskujen nrot** -kenttä) on sama kuin kirjattujen myyntilaskujen numerosarja (**Kirjattujen laskujen nrot**) ja että kirjattujen ennakkomaksun hyvityslaskujen numerosarja (**Kirjattujen ennakkomaksun hyvityslaskujen nrot**) on sama kuin kirjattujen hyvityslaskujen numerosarja (**Kirjattujen hyvityslas. nrot**).  

#### <a name="to-block-shipments-for-unpaid-prepayment"></a>Toimitusten estäminen tilanteissa, joissa ennakkomaksuja on jätetty maksamatta  
1.  Valitse **Myyntien ja myyntisaamisten asetukset** -sivun **Yleinen**-pikavälilehdessä **Tarkista ennakkomaksu kirjattaessa** -valintaruudussa.

    Et voi nyt toimittaa tai laskuttaa tilausta, jossa on maksamaton ennakkomaksu.  

Paula edellyttää, että asiakkaalta 20000 laskutetaan kaikkien tilausten yhteydessä oletusarvoisesti 30 prosentin ennakkomaksu. Hän lisää ennakkomaksun oletusprosenttiosuuden asiakkaan korttiin.  

Paula edellyttää, että kaikilta asiakkailta laskutetaan 20 prosentin ennakkomaksu nimikkeestä 1100. Asiakkaan 20000 maksuhistoria on huono, joten asiakkaalta 20000 edellytetään 40 prosentin ennakkomaksua nimikkeestä 1100. Seuraavassa menettelyssä kuvataan, miten ennakkomaksujen oletusprosentit määritetään.  

#### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Ennakkomaksujen oletusprosenttien määrittäminen asiakkaille ja nimikkeille  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.  
2.  Avaa asiakkaan 20000 (Tinayhtymä) kortti.
3.  Kirjoita **Ennakkomaksuprosentti**-kenttään **30**.  
4.  Sulje asiakaskortti valitsemalla **OK**-painike.  
5.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.  
6.  Avaa asiakkaan 1100 kortti.
7.  Valitse **Ennakkomaksuprosentit**-toiminto.  
8.  Täytä kaksi riviä **Myynnin ennakkomaksuprosentit** -sivulla seuraavasti.  

    |**Myynnin tyyppi**|**Myyntikoodi**|**Nimikkeen nro**|**Ennakkomaksuprosentti**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Asiakas**|**20000**|**1100**|**40**|  
    |**Kaikki asiakkaat**||**1100**|**20**|  

    > [!IMPORTANT]  
    >  Maan/alueen mukaan sinun täytyy myös määrittää veroryhmän koodi  **Laskutus**-pikavälilehdellä nimikkeille 1000 ja 1100.  

9. Sulje kaikki sivut.  

#### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Määritä tili myynnin ennakkomaksuille yleisissä kirjausasetuksissa  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleiset kirjausasetukset** ja valitse sitten liittyvä linkki.  
2.  Valitse rivi, jossa **Ylein. liiketoim. kirjausryhmä** -kentän arvoksi on määritetty **VIE** ja **Yleinen tuotteen kirjausryhmä** -kentän arvoksi **VÄH.MYYNTI**. Valitse sitten **Muokkaa**-toiminto.  
3.  Määritä **Yleisten kirj.asetusten kortti** -sivun **Myynnin ennakkomaksutili** -kentässä käsiteltävä tili.  
4.  Valitse **OK**-painike.  

## <a name="creating-an-order-that-requires-a-prepayment"></a>Ennakkomaksua edellyttävän tilauksen luominen  
 Seuraavassa tilanteessa Sanna, tilausten käsittelijä, luo tilauksen puhuessaan asiakkaan kanssa. Asiakkaan tilaamat nimikkeen on maksettava ennakkoon, ja asiakkaalla on ollut maksuvaikeuksia aikaisemmin. Sannaa on kehotettu vaatimaan 2 000:n kiinteää summaa tilauksen ennakkomaksuksi.  

Asiakas voi maksaa 35 % esimaksun, johon Sanna voi suostua. Tämän vuoksi hän muuttaa tilausta.  

Susanna luo ennakkomaksulaskun ja lähettää sen asiakkaalle.  

#### <a name="to-create-a-sales-order-with-a-prepayment"></a>Ennakkomaksun sisältävän myyntitilauksen luominen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Valitse **Tilausasiakkaan nro** **20000**.  
5.  Hyväksy näyttöön tuleva erääntyvän saldon varoitus.  
6.  Täytä kahdelle myyntiriville seuraavat tiedot:  

    |**Tyyppi**|**Nro**|**Määrä**|  
    |--------------|-------------|------------------|  
    |**Nimike**|**1000**|**1**|  
    |**Nimike**|**1100**|**1**|

    Myyntirivien ennakkomaksukentät on oletusarvoisesti piilotettu, joten ne on tuotava näkyviin.  

7. Varmista, että **Ennakkomaksuprosentti**-kentässä rivillä, jossa on nimike **1000**, lukee **30**. Tämä oletusarvo on peräisin myynnin tunnistetiedoista, joka on täytetty asiakkaan kortista.  

    **Ennakkomaksuprosentti**-kentässä rivillä, jolla on nimike **1100**, lukee **40**. Tämä on prosenttiosuus, jonka olet lisännyt **Myynnin ennakkomaksuprosentit** -sivulla nimikkeelle **1100** ja asiakkaalle **20000**.  

    Lisätietoja on ohjeaiheessa [Ennakkomaksujen määrittäminen](finance-set-up-prepayments.md).  
8. Valitse **Tilastot**-toiminto.  
9. **Ennakkomaksu**-pikavälilehden **Ennakkomaksun rivisumma ilman ALV:tä** -kentän arvona on **1 560**. Jos luot nyt tilaukselle ennakkomaksulaskun, tämä summa näkyy laskussa.  

    Tässä skenaariossa Susannaa on ohjeistettu ehdottamaan tilaukselle ennakkomaksua, jonka kokonaissumma on 2 000.  

    > [!IMPORTANT]  
    >  Maan/alueen mukaan seuraavat vaiheet eivät ehkä ole käytössä.  
10. Muuta **Ennakkomaksun rivisumma ilman ALV:tä** -kentän summaksi **2 000** ja sulje sivu.  
11. Kun vahvistat myyntirivien **Ennakkomaksuprosentti**-kentän, se lasketaan uudelleen. Uusi summa on **40,81625**.  

    Uudelleenlaskentaan sisällytetään kaikki rivit, joiden ennakkomaksuprosentti on suurempi kuin 0.  

    Seuraavaksi asiakas kysyy, voidaanko ennakkomaksuprosentiksi sopia 35 %. Sannan valvoja hyväksyy muutoksen.  

12. Anna **Myyntitilaus**-sivun **Ennakkomaksu**-kentässä **35**.  
13. Valitse näyttöön tulevassa varoituksessa **Kyllä**. 35 % sovelletaan koko tilaukseen maksuprosenttina.  
14. Vahvista, että rivit on päivitetty asianmukaisesti.  

## <a name="creating-a-prepayment-invoice"></a>Ennakkomaksulaskun luominen  
Kun Susanna on lisännyt oikean ennakkomaksuarvon tilaukseen, hän luo ennakkomaksulaskun ja lähettää sen asiakkaalle.  

#### <a name="to-create-a-prepayment-invoice"></a>Ennakkomaksulaskun luominen  

1.  Valitse **Myyntitilaus**-sivulla **Kirjaa ennakkomaksulasku** -toiminto.  

> [!NOTE]  
>  Susanna valitsee **Kirjaa ja tulosta ennakkomaksulasku** ja lähettää laskun asiakkaalle.  

## <a name="creating-an-additional-prepayment-invoice"></a>Ylimääräisen ennakkomaksulaskun luominen  
Seuraavana päivänä asiakas soittaa Susannalle ja tekee muutoksia tilaukseen. Asiakas haluaisi kaksi kappaletta nimikettä 1100. Susanna avaa tilauksen uudelleen, päivittää tilauksen, luo tilaukselle toisen ennakkomaksulaskun ja lähettää sen asiakkaalle.  

#### <a name="to-create-an-additional-prepayment-invoice"></a>Ylimääräisen ennakkolaskumaksun luominen  

1.  Valitse **Myyntitilaus**-sivulla **Avaa uudelleen** -toiminto.  
2.  Lisää **1100**-nimikkeen **Määrä**-kenttään **2**.  

    Vieritä nähdäksesi ennakkomaksukentät. **Ennakkomaksun rivin summa ilman ALV:tä** -kenttä sisältää nyt **630**, ja **Laskutettu ennakkomaksun summa ilman ALV:tä** -kenttä sisältää **315**. Tämä osoittaa, että on ylimääräinen ennakkomaksun määrä, jota ei ole vielä laskutettu.  
3.  Voit kirjata laskun ylimääräisestä ennakkomaksusta valitsemalla **Kirjaa ennakkomaksulasku** -toiminnon.  

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
3. Valitse **Kohdista tapahtumat** -toiminto.  
4.  Valitse **Kohdista asiakastapahtumat** -sivulla ensimmäinen ennakkomaksulasku ja valitse sitten **Aseta kohdistustunniste**-toiminto.  
5.  Toista edellinen vaihe toista ennakkomaksua varten.  
6.  Valitse **OK**-painike.  

    Summakentässä on nyt kahden ennakkomaksulaskun summa.  

7.  Kirjaa päiväkirja.  

## <a name="invoicing-the-remaining-amount"></a>Jäljellä olevan summan laskuttaminen  
Erikille on nyt ilmoitettu, että tilauksen nimikkeet on toimitettu ja että tilaus on valmis laskutettavaksi. Erik luo tilauksen laskun.  

#### <a name="to-invoice-the-remaining-amount"></a>Jäljellä olevan summan laskuttaminen  
1. Avaa myyntitilaus.  
2. Valita ensin **Toimitus ja lasku** ja sitten **OK**.  

> [!NOTE]  
>  Tavallisesti toimituksesta vastaava osasto olisi jo kirjannut toimituksen.  

Arto näkee historiasta, että myyntilasku on luotu tarkoituksellisesti.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kirjatut myyntilaskut** ja valitse sitten liittyvä linkki.  

## <a name="next-steps"></a>Seuraavat vaiheet  
Tässä vaihekuvauksessa käsiteltiin vaiheita, joita noudattamalla [!INCLUDE[d365fin](includes/d365fin_md.md)] määritetään käsittelemään ennakkomaksuja. Asiakkaiden ja nimikkeiden ennakkomaksujen oletusprosenttien määrittäminen havainnollistettiin ja useita tilauksen ennakkomaksujen laskentatapoja käytiin läpi. Mukana oli myös tilanne, jossa tilaukseen pyrittiin määrittämään yksi ennakkomaksun kokonaissumma, jonka jälkeen ohjelma määritettiin laskemaan ennakkomaksusumma koko tilauksen prosenttiosuutena.  

Vaihekuvauksessa käsiteltiin myös ennakkomaksulaskun kirjaamista, toisen ennakkomaksulaskun luomista tilauksen muuttumiseen jälkeen sekä jäljellä olevan summan lopullisen laskun kirjaamista.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman ennakkomaksutoiminnolla voit vaivattomasti määrittää sekä valvoa asiakkaiden ja nimikkeiden ennakkomaksusääntöjä. Ennakkomaksutoiminnon ansiosta voit myös kohdistaa jokaisen maksun laskuun.  

## <a name="see-also"></a>Katso myös  
[Ennakkomaksujen laskuttaminen](finance-invoice-prepayments.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)
