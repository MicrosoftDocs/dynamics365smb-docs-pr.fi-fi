---
title: Myynnin ennakkomaksujen määrittäminen ja laskuttaminen
description: Ennakkomaksut ovat maksuja, jotka on laskutettu sekä kirjattu myynti- tai ostoennakkomaksun tilaukseen ennen lopullista laskutusta.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 12/03/2021
ms.author: edupont
ms.openlocfilehash: aaa277f97d1abe36fdffbb97212f1498723e116c
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9535529"
---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Vaihekuvaus: Myynnin ennakkomaksujen määrittäminen ja laskuttaminen

Tässä opastuksessa käsitellään ennakkomaksujen määrittäminen ja käyttö kohteessa [!INCLUDE [prod_short](includes/prod_short.md)]. [!INCLUDE [prepayment_def](includes/prepayment_def.md)]

[!INCLUDE [prepayment_req](includes/prepayment_req.md)]

Voit myös esimerkiksi lähettää lisäennakkomaksulaskuja, jos tilaukseen esimerkiksi lisätään nimikkeitä.  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta  

Tässä vaihekuvauksessa käsitellään seuraavia tilanteita:  

- Ennakkomaksujen määrittäminen  
- Ennakkomaksua edellyttävän tilauksen luominen  
- Ennakkomaksulaskun luominen  
- Tilauksen ennakkomaksuvaatimusten korjaaminen  
- Ennakkomaksujen kohdistaminen tilaukseen  
- Ennakkomaksun sisältävän tilauksen lopullisen summan laskuttaminen  

### <a name="roles"></a>Roolit

Tässä vaihekuvauksessa on seuraaviin rooleihin liittyviä tehtäviä:  

- talouspäällikkö (Paula)  
- tilausten käsittelijä (Susanna)  
- myyntireskontran hoitaja (Erik).  

## <a name="story"></a>Taustatietoja

 Paula on talouspäällikkö. Hän tekee päätökset asiakkaista, joiden tarvitsee maksaa vakuus, ennen kuin osat valmistetaan tai toimitetaan. Paula määrittää [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman laskemaan ennakkomaksut automaattisesti.  

 Susanna on myyntitilausten käsittelijä. Kun asiakas soittaa tilauksen, hän syöttää tilauksen järjestelmään sillä aikaa kun asiakas on puhelimessa. Tällä tavoin hän voi tarkistaa hinnat ja maksuehdot asiakkaan kanssa välittömästi, ja hän voi tehdä muutoksia järjestykseen, kun hän neuvottelee asiakkaan kanssa.  

 Erik työskentelee kirjanpito-osastolla, jossa hän kirjaa laskuja ja maksuja.  

 Tässä skenaariossa Paula määrittää ennakkomaksuvaatimukset Tinayhtymä Oy:lle kyseisen asiakkaan luottotietojen perusteella. Paula antaa Susanille ohjeita tilausten käsittelyyn.  

 Kun asiakas soittaa, Sanna neuvottelee asiakkaan kanssa, kunnes he pääsevät sopimukseen. Hän voi sitten halutessaan laskea ennakkomaksun monin eri tavoin.  

 Kun Sanna on lähettänyt ennakkomaksulaskun, asiakas tilaa ylimääräisen nimikkeen. Sanna päivittää tilauksen ja luo toisen ennakkomaksulaskun.  

 Erik rekisteröi asiakkaan maksun, kohdistaa sen laskuihin ja lähettää lopullisen laskun.  

## <a name="set-up-prepayments"></a>Ennakkomaksujen määrittäminen

Paula määrittää järjestelmän käsittelemään asiakkaiden ennakkomaksut.  

- Paula päättää, että ennakkomaksuissa käytetään samaa numerosarjaa kuin myyntilaskuissa.  
- Paula määrittää sovelluksen tarkistamaan ennakkomaksujen tarpeen ennen tilauksen lopullista laskuttamista.  
- Paula määrittää ennakkomaksujen vaadittavat oletusprosenttiosuudet tiettyjä nimikkeitä ja asiakkaita varten.  

Seuraavissa kohdissa on kuvattu, miten Paulan työtehtävät suoritetaan.  

### <a name="to-set-up-number-series-for-prepayments"></a>Ennakkomaksujen numerosarjojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntien ja myyntisaamisten asetukset** ja valitse sitten vastaava linkki.  
2. Laajenna **Myyntien ja myyntisaamisten asetukset** -sivun **Numerosarja**-pikavälilehti.  
3. Varmista, että kirjattujen ennakkomaksulaskujen numerosarja (**Kirjattujen ennakkomaksulaskujen nrot** -kenttä) on sama kuin kirjattujen myyntilaskujen numerosarja (**Kirjattujen laskujen nrot**) ja että kirjattujen ennakkomaksun hyvityslaskujen numerosarja (**Kirjattujen ennakkomaksun hyvityslaskujen nrot**) on sama kuin kirjattujen hyvityslaskujen numerosarja (**Kirjattujen hyvityslas. nrot**).  

### <a name="to-block-shipments-for-unpaid-prepayment"></a>Toimitusten estäminen tilanteissa, joissa ennakkomaksuja on jätetty maksamatta

1. Valitse **Myyntien ja myyntisaamisten asetukset** -sivun **Yleinen**-pikavälilehdessä **Tarkista ennakkomaksu kirjattaessa** -valintaruudussa.

Et voi nyt toimittaa tai laskuttaa tilausta, jossa on maksamaton ennakkomaksu.  

Paula edellyttää, että asiakkaalta 20000 laskutetaan kaikkien tilausten yhteydessä oletusarvoisesti 30 prosentin ennakkomaksu. Hän lisää ennakkomaksun oletusprosenttiosuuden asiakkaan korttiin.  

Paula edellyttää, että kaikilta asiakkailta laskutetaan 20 prosentin ennakkomaksu nimikkeestä 1896-S. Asiakkaan 20000 maksuhistoria on huono, joten asiakkaalta 20000 edellytetään 40 prosentin ennakkomaksua nimikkeestä 1896-S. Seuraavassa menettelyssä kuvataan, miten ennakkomaksujen oletusprosentit määritetään.  

### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Ennakkomaksujen oletusprosenttien määrittäminen asiakkaille ja nimikkeille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.  
2. Avaa asiakkaan 20000 (Trey Research) kortti.
3. Anna **Maksut**-pikavälilehden **Ennakkomaksuprosentti**-kentässä **30**.  
4. Valitse **Liittyvät**-toiminto, **Myynti**-valikkokohde ja sitten **Ennakkomaksuprosentit**-valikkokohde.  
5. Täytä kaksi riviä **Myynnin ennakkomaksuprosentit** -sivulla seuraavasti.  

    |**Myynnin tyyppi**|**Myyntikoodi**|**Nimikkeen nro**|**Ennakkomaksuprosentti**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Asiakas**|**20000**|**1896-S**|**40**|
    |**Asiakas**|**20000**|**1900-S**|**30**|  
    
    > [!TIP]
    > Maan tai alueen mukaan sinun täytyy myös määrittää veroryhmän koodi **Kustannukset ja kirjaus** -pikavälilehdellä nimikkeille 1896-S. Kun käytät esittely-yritystä, tämä kenttä on jo määritetty.

6. Sulje kaikki sivut.  

### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Määritä tili myynnin ennakkomaksuille yleisissä kirjausasetuksissa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset kirjausasetukset** ja valitse sitten vastaava linkki.  
2. Valitse rivi, jossa **Ylein. liiketoim. kirjausryhmä** -kentän arvoksi on määritetty **KOTIMAAN** ja **Yleinen tuotteen kirjausryhmä** -kentän arvoksi **VÄH.MYYNTI**.  
3. Määritä **Myynnin ennakkomaksutili** -kentässä asianmukainen tili. Valintasi tallentuu automaattisesti.  

> [!TIP]
> Jos **Yleiset kirjausasetukset** -sivun kenttä ei ole näkyvissä, siirry sivulla oikealle sivun alaosassa olevan vaakavierityspalkin avulla.  

## <a name="create-an-order-that-requires-a-prepayment"></a>Ennakkomaksua edellyttävän tilauksen luominen

 Seuraavassa tilanteessa Sanna, tilausten käsittelijä, luo tilauksen puhuessaan asiakkaan kanssa. Asiakkaan tilaamissa nimikkeissä tarvitaan ennakkomaksu. Lisäksi asiakas on maksanut aiemmin maksuja myöhässä. Susania on kehotettu vaatimaan kiinteää summaa **800** tilauksen ennakkomaksuksi.  

Asiakas pyytää, että hän saisi maksaa 35 prosenttia, johon Susan voi myöntyä. Hän tekee tarvittavat muutokset tilaukseen.  

Susanna luo ennakkomaksulaskun ja lähettää sen asiakkaalle.  

### <a name="to-create-a-sales-order-with-a-prepayment"></a>Ennakkomaksun sisältävän myyntitilauksen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Valitse **Asiakkaan nimi** -kentässä **Trey Research**.  
4. Sulje näyttöön tuleva erääntyvän saldon varoitus.  
5. Täytä kahdelle myyntiriville seuraavat tiedot:  

    |**Tyyppi**|**Ei.**|**määrä**|  
    |--------------|-------------|------------------|  
    |**Nimike**|**1896-S**|**1**|  
    |**Nimike**|**1900-S**|**1**|

    Myyntirivien ennakkomaksukentät on oletusarvoisesti piilotettu. Jos haluat näyttää kentät, sinun täytyy mukauttaa sivua. Lisätietoja on kohdassa, jossa [Sivun mukauttaminen mukautusvalintanauhan avulla](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

6. Varmista, että **Ennakkomaksuprosentti**-kentässä rivillä, jossa on nimike **1900-S**, lukee **30**. Tämä oletusarvo on peräisin myynnin tunnistetiedoista, joka on täytetty asiakkaan kortista.  

    **Ennakkomaksuprosentti**-kentässä rivillä, jolla on nimike **1896-S**, lukee **40**. 40 on prosenttiosuus, jonka olet lisännyt **Myynnin ennakkomaksuprosentit** -sivulla nimikkeelle **1896-S** ja asiakkaalle **20000**.  

    Lisätietoja on ohjeaiheessa [Ennakkomaksujen määrittäminen](finance-set-up-prepayments.md).  
7. Valitse **Tilaus**-toiminnossa **Tilastotiedot**.  
8. **Ennakkomaksu**-pikavälilehden **Ennakkomaksun summa ilman ALV:tä** -kenttä sisältää arvon **458,16**. Jos luot nyt tilaukselle ennakkomaksulaskun, 458.16 on summa, joka näkyy laskussa.  

    Tässä skenaariossa Susannaa on ohjeistettu ehdottamaan tilaukselle ennakkomaksua, jonka kokonaissumma on **800**.  

    > [!IMPORTANT]  
    >  Maan/alueen mukaan seuraavat vaiheet eivät ehkä ole käytössä.  
9. Muuta **Ennakkomaksun summa ilman veroja** -kentän summaksi **800** ja sulje sivu.  
10. Kun vahvistat myyntirivien **Ennakkomaksuprosentti**-kentän, se lasketaan uudelleen. Uudet summat ovat **67.02438** ja **67.02282**.  

     Uudelleenlaskentaan sisällytetään kaikki rivit, joiden ennakkomaksuprosentti on suurempi kuin 0.  

     Seuraavaksi asiakas kysyy, voidaanko ennakkomaksuprosentiksi sopia 35 %. Sannan valvoja hyväksyy muutoksen.
11. Syötä **Myyntitilaus**-sivun **Ennakkomaksu**-pikavälilehden **Ennakkomaksuprosentti**-kenttään **35**.  
12. Valitse näyttöön tulevassa varoituksessa **Kyllä**. 35 % sovelletaan koko tilaukseen maksuprosenttina.  
13. Vahvista, että rivit on päivitetty oikein.  

## <a name="create-a-prepayment-invoice"></a>Ennakkomaksulaskun luominen

Kun Susanna on lisännyt oikean ennakkomaksuarvon tilaukseen, hän luo ennakkomaksulaskun ja lähettää sen asiakkaalle.  

### <a name="to-create-a-prepayment-invoice"></a>Ennakkomaksulaskun luominen

1. Valitse **Myyntitilaus**-sivulla **Toiminnot**, sitten **Kirjaus**, sitten **Ennakkomaksu** ja valitse sitten **Kirjaa ja tulosta ennakkomaksulasku**
2. Kirjaa lasku valitsemalla **Kyllä**-painike.  

> [!NOTE]  
> Susanna lähettää laskun asiakkaalle.  

## <a name="create-an-additional-prepayment-invoice"></a>Ylimääräisen ennakkolaskumaksun luominen

Seuraavana päivänä asiakas soittaa Susannalle ja tekee muutoksia tilaukseen. Asiakas haluaisi kaksi kappaletta nimikettä 1896-S. Susan avaa tilauksen uudelleen ja päivittää sen. Hän luo tilauksesta toisen ennakkomaksulaskun ja lähettää sen asiakkaalle.  

### <a name="to-create-an-additional-prepayment-invoice"></a>Ylimääräisen ennakkolaskumaksun luominen

1. Valitse **Myyntitilaus**-sivulla **Vapauta**-toiminto ja sitten **Avaa uudelleen**.  
2. Syötä nimikkeen **1896-S** kentässä **Määrä** arvoksi **2**.  

    Valitse **Tilaus**-toiminnossa **Tilastotiedot**. **Ennakkomaksun summa ilman ALV:tä** -kenttä sisältää nyt arvon **768,04**, ja **Laskutettu ennakkomaksun summa ilman ALV:tä** -kenttä sisältää arvon **417,76**. Nämä arvot osoittavat, että on ylimääräinen ennakkomaksun määrä, jota ei ole vielä laskutettu.  
3. Kirjaa ylimääräinen ennakkomaksun summa valitsemalla **Toiminnot**, sitten **Kirjaus**, sitten **Ennakkomaksu** ja sitten valitse **Kirjaa ja tulosta ennakkomaksulasku**
4. Kirjaa lasku valitsemalla **Kyllä**-painike.  

## <a name="apply-the-prepayments"></a>Ennakkomaksujen kohdistaminen

Asiakas maksaa ennakkomaksusumman. Kirjanpito-osaston Arnie rekisteröi maksun ja kohdistaa sen ennakkomaksulaskuihin.  

### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Maksun kohdistaminen ennakkomaksulaskuihin

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kassapäiväkirjat** ja valitse sitten vastaava linkki.  
2. Täytä päiväkirjan rivi seuraavilla tiedoilla:  

    |Kentän nimi|Syötä|  
    |----------------|-----------|  
    |**Asiakirjatyyppi**|**Maksu**|  
    |**Tilityyppi**|**Asiakas**|  
    |**Tilinro**|**20000**|  
3. Valitse **Prosessi**-toiminto ja sitten **Kohdista tapahtumat**.  
4. Valitse **Kohdista asiakastapahtumat** -sivulla ensimmäinen ennakkomaksulasku, valitse **Prosessi**-toiminto ja valitse sitten **Aseta kohdistustunniste** -toiminto.  
5. Toista edellinen vaihe toista ennakkomaksua varten.  
6. Valitse **OK**-painike.  

    **Summa**-kentissä on nyt kahden ennakkomaksulaskun summa.  

7. Kirjaa päiväkirja valitsemalla **Kirjaa/tulosta**-toiminto ja sitten **Kirjaa**.
8. Valitse **Kyllä**-painike.

## <a name="invoice-the-remaining-amount"></a>Jäljellä olevan summan laskuttaminen

Erikille on nyt ilmoitettu, että tilauksen nimikkeet on toimitettu ja että tilaus on valmis laskutettavaksi. Erik luo tilauksen laskun.  

### <a name="to-invoice-the-remaining-amount"></a>Jäljellä olevan summan laskuttaminen

1. Avaa myyntitilaus.
2. Valitse **Kirjaus**-toiminto ja sitten **Kirjaa**.
3. Valitse **Toimitus ja lasku** ja sitten **OK**-painike.
4. Jos haluat esikatsella laskun, valitse **Kyllä**-painike.

    > [!NOTE]  
    > Tavallisesti toimituksesta vastaava osasto olisi jo kirjannut toimituksen.  

    Arto näkee historiasta, että myyntilasku on luotu tarkoituksellisesti.

5. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntilaskut** ja valitse sitten vastaava linkki.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Ennakkoon maksettujen tilausten ja laskujen tilan päivittäminen automaattisesti

Voit nopeuttaa tilausten ja laskujen käsittelemistä määrittämällä työjonotapahtumat, jotka päivittävät kyseisten asiakirjojen tilan automaattisesti. Kun ennakkomaksulasku on maksettu, työjonotapahtumat voivat automaattisesti muuttaa asiakirjan tilan **odottavasta ennakkomaksusta** **lähetetyksi**. Kun määrität työjonon tapahtumia, koodiyksiköt, joita tarvitset, ovat **383 Upd. Pending Prepmt. Sales** ja **383 Upd. Pending Prepmt. Purchase**. On suositeltavaa ajoittaa tapahtumat suoritettavaksi usein, esimerkiksi joka minuutti. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).

## <a name="next-steps"></a>Seuraavat vaiheet

Tässä vaihekuvauksessa käsiteltiin seuraavia vaiheita, joita noudattamalla [!INCLUDE[prod_short](includes/prod_short.md)] määritetään käsittelemään ennakkomaksuja. 

- Ennakkomaksujen oletusprosenttien määrittäminen asiakkaille ja nimikkeille.
- Käytä eri menetelmiä tilauksen ennakkomaksujen laskemiseen.  
- Laske ennakkomaksusumma prosentteina tilauksen kokonaissummasta.
- Määritä tilaukseen yhden ennakkomaksun kokonaissumma.  

Vaihekuvauksessa käsiteltiin myös ennakkomaksulaskun kirjaamista, toisen ennakkomaksulaskun luomista tilauksen muuttumiseen jälkeen sekä jäljellä olevan summan lopullisen laskun kirjaamista.  

Ennakkomaksuominaisuuksien avulla on helppo määrittää ja pakottaa asiakkaiden ja nimikkeiden ennakkomaksusääntöjä. Niiden avulla voit myös kirjata jokaisen maksun laskua vastaan.  

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/prepayment-invoices-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Ennakkomaksujen laskuttaminen](finance-invoice-prepayments.md)  
[Rahoitus](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
