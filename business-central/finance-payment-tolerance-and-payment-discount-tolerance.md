---
title: Maksutoleranssi ja maksualennustoleranssi | Microsoft Docs
description: Voit määrittää maksutoleranssin sulkeaksesi laskun, kun maksu ei täysin kata laskun summaa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b13426a431eb45183c5c12454ff70ef0cc066229
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788125"
---
# <a name="work-with-payment-tolerances-and-payment-discount-tolerances"></a>Maksutoleranssien ja maksualennustoleranssien käsitteleminen
Voit määrittää maksutoleranssin ja sulkea sen avulla laskun, kun maksu ei täysin kata laskun summaa. Esimerkiksi maksutoleranssit ovat tyypillisesti pieniä maksuja, joiden korjaaminen maksaa enemmän kuin niiden hyväksyntä. Voit määrittää maksualennustoleranssin, jolla voi myöntää maksualennuksen sen jälkeen kun maksualennuspäivämäärä on ohitettu.  

Voit käyttää maksutoleransseja siten, että jokaiselle avoimelle summalle on määritetty suurin sallittu maksutoleranssi. Jos maksutoleranssi täyttyy, maksusumma analysoidaan. Jos maksettu summa on alisuoritus, koko avoin summa kuitataan alisuoritusta vastaan. Ohjelma kirjaa yksityiskohtaisen maksutapahtuman niin, että kohdistetusta laskusta ei jää avointa saldoa. Mikäli maksutoleranssin kriteerit täyttyvät ja maksu on ylisuoritus, uusi yksityiskohtainen reskontratapahtuma kirjataan niin, että maksutapahtumasta ei jää avointa saldoa.

Voit käyttää maksualennustoleransseja siten, että jos hyväksyt maksualennuksen maksualennuspäivämäärän jälkeen, se kirjataan aina joko maksualennustilille tai maksutoleranssin tilille.

## <a name="applying-payment-tolerance-to-multiple-documents"></a>Maksutoleranssien käyttöönotto useissa asiakirjoissa  
Yksittäisellä asiakirjalla on sama maksutoleranssi riippumatta siitä kohdistetaanko se yksinään vai muiden asiakirjojen kanssa samanaikaisesti. Myöhästyneen maksualennuksen hyväksyntä, kun kohdistat maksutoleranssin useisiin asiakirjoihin, tapahtuu automaattisesti kullekin asiakirjalle, kun seuraava sääntö täyttyy:  

*maksualennuspvm < maksupvm (kohdetapahtumalla) <= maksutoleranssipvm*  

Tämä sääntö määrittää myös sen, näytetäänkö varoituksia, kun maksutoleranssia käytetään useissa tiedostoissa. Maksualennuksen toleranssivaroitus näytetään jokaiselle tapahtumalle, joka täyttää päivämääräkriteerin. Lisätietoja on kohdassa [Esimerkki 2 – Useiden asiakirjojen toleranssilaskelmat](finance-payment-tolerance-and-payment-discount-tolerance.md#example-2---tolerance-calculations-for-multiple-documents).

Voit tuoda näyttöön varoituksen, joka perustuu eri poikkeamatilanteisiin.  

- Ensimmäinen varoitusteksti liittyy maksualennustoleranssiin. Saat tiedon, että voit hyväksyä myöhästyneen maksualennuksen. Sitten voit valita hyväksytkö toleranssin alennuspäivänä.  
- Toinen varoitusteksti liittyy maksutoleranssiin. Käyttäjälle ilmoitetaan, että kaikki tapahtumat voidaan sulkea, koska ero on pienempi kuin maksimi maksutoleranssi kohdistettaville tapahtumille. Sitten voit valita hyväksytkö toleranssin maksumäärässä.

> [!NOTE]
> Kun varoitusviesti otetaan käyttöön, voidaan valita, miten toleranssin rajoissa suoritettavat maksut käsitellään. Jos et ota sanomaa käyttöön ja toleranssitaso on määritetty, laskut, joiden summat ovat toleranssin sisällä, suljetaan automaattisesti, etkä voi valita, että jäljellä oleva summa jätetään pois. 

Lisätietoja on kohdassa [Maksutoleranssin varoitusten käyttöönotto tai käytöstäpoisto](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings). 

## <a name="to-set-up-tolerances"></a>Toleranssien määrittäminen  
Toleranssi päivillä ja summilla sallii laskun sulkemisen vaikka maksu ei täysin kata laskun summaa, johtuu tämä sitten maksualennuspäivän ylittämisestä, virheellisten tavaroiden aiheuttamasta vähennyksestä tai pienestä virheestä. Tämä pätee myös hyvityksiin ja hyvityslaskuihin.  

Määrittääksesi toleranssin sinun tulee määrittää useita toleranssitilejä, sekä maksualennustoleranssin että maksutoleranssin kirjaustavat ja sitten ajaa **Muuta maksutoleranssia** -eräajo  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleiset kirjausasetukset** ja valitse sitten liittyvä linkki.  
2. Määritä **Yleiset kirjausasetukset** -sivulla debet- ja kredit-myynnin maksutoleranssin tili ja debet- ja kredit-ostojen maksutoleranssin tili.  
3. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaan kirjausryhmät** ja valitse sitten liittyvä linkki.    
4. Määritä **Asiakkaan kirjausryhmät** -sivulla debet- ja kredit-maksutoleranssitili. Lisätietoja on kohdassa [Kirjausryhmien määrittäminen](finance-posting-groups.md).  
5. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Toimittajan kirjausasetukset** ja valitse sitten liittyvä linkki.  
6. Määritä **Toimittajan kirjausryhmät** -sivulla debet- ja kredit-maksutoleranssitili.  
7. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon määritykset** ja valitse sitten liittyvä linkki.  
8. Avaa **Pääkirjanpidon asetukset** -sivu.  
9. Täytä **Kohdistus** -pikavälilehdessä **Maksualennustoler. kirjaaminen**-, **Maksualennuksen ylityskausi**- ja **Maksutoleranssin kirjaus** -kentät.   
10. Valitse **Muuta maksutoleranssia** -toiminto.
11. Täytä **Muuta maksutoleranssia** -sivulla **Maksutoleranssi %**- ja **Maksimi maksutoleranssisumma** -kentät ja valitse **OK**.

> [!IMPORTANT]  
>  Nyt olet määrittänyt maksutoleranssin vain paikalliselle valuutalle. Jos haluat, että [!INCLUDE[prod_short](includes/prod_short.md)] käsittelevän maksujen, hyvityslaskujen ja hyvitysten toleransseja ulkomaan valuuttana, sinun on tehtävä **Muuta maksutoleranssia** -eräajo **Valuuttakoodi**-kentän arvolla.  

> [!NOTE]  
>  Mikäli haluat saada maksutoleranssivaroituksen joka kerran kun kirjaat kohdistuksen, joka osuu toleranssialueelle, sinun tulee aktivoida maksualennusvaroitus. Lisätietoja on kohdassa [Maksutoleranssin varoituksen ottaminen käyttöön tai poistaminen käytöstä](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings).  
>   
>  Jos haluat poistaa toleranssin käytöstä asiakkaalta tai toimittajalta, toleranssit on estettävä kyseisen asiakkaan tai toimittajan kortissa. Lisätietoja on kohdassa [Asiakkaiden maksutoleranssin estäminen](finance-payment-tolerance-and-payment-discount-tolerance.md#to-block-payment-tolerance-for-customers).  
>   
>  Kun määrität toleranssin, [!INCLUDE[prod_short](includes/prod_short.md)] tarkastaa onko avoimia tapahtumia ja laskee toleranssin myös näille tapahtumille.

## <a name="to-enable-or-disable-payment-tolerance-warnings"></a>Maksutoleranssivaroitusten ottaminen käyttöön tai poistaminen käytöstä
Maksutoleranssivaroitus ilmestyy, kun kirjaat kohdistuksen, jonka saldo mahtuu sallittuun toleranssiin. Voit sitten päättää kuinka kirjaat ja dokumentoit saldon.    
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon määritykset** ja valitse sitten liittyvä linkki.  
2. Voit ottaa varoituksen käyttöön laittamalla **Pääkirjanpidon asetukset** -sivun **Kohdistus**-pikavälilehden **Maksutoleranssin varoitus** -kytkimen päälle. Voit poistaa varoituksen käytöstä laittamalla kytkimen pois päältä.  

> [!NOTE]  
>  Oletusarvon mukainen vaihtoehto **Maksutoleranssin varoitus** -sivulla on **Jätä saldo jäljelläolevaksi summaksi**. Oletusarvon mukainen vaihtoehto **Maksualennustoler. varoitus** -sivulle on **Älä hyväksy myöhästynyttä maksualennusta**.

## <a name="to-block-payment-tolerance-for-customers"></a>Maksutoleranssin estäminen asiakkailta  
Oletusarvo maksutoleranssiasetukselle on sallittu. Estääksesi tietyn asiakkaan tai toimittajan maksutoleranssin sinun tulee estää toleranssi kyseisen asiakkaan tai toimittajan kortilta Seuraavaksi kerrotaan, miten se tehdään asiakkaalle. Toimittajaa koskevat vaiheet ovat samanlaisia.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** tai **Toimittaja** ja valitse sitten liittyvä linkki.  
2. Valitse **Maksut**-pikavalintalehdessä **Estä maksutoleranssi** -valintaruutu.  

> [!NOTE]  
>  Jos asiakkaalla tai toimittajalla on avoimia tapahtumia, sinun on ensin poistettava maksutoleranssi avoimista tapahtumista.

## <a name="example-1---tolerance-calculations-for-a-single-document"></a>Esimerkki 1 – Yksittäisen asiakirjan toleranssilaskennat
Seuraavassa muutamia esimerkkejä oletetuista toleranssilaskelmista ja kirjauksista, erilaisissa tilanteissa.  

**Pääkirjanpidon asetukset** -sivulla on seuraavat asetukset:
- Maksutoleranssin ylityskausi: 5P  
- Maksimi maksutoleranssi: 5  

Seuraavissa tilanteissa käytössä on vaihtoehto A tai B:  

- **A** Tässä tapauksessa maksualennustoleranssivaroitus on suljettu TAI käyttäjällä on varoitus käytössä ja hän on sallinut myöhästyneen maksualennuksen (Kirjataanko saldo maksutoleranssina?).  
- **B** Tässä tapauksessa käyttäjällä on käytössä varoitus ja hän on valinnut, ettei salli myöhästynyttä maksualennusta (Jätä saldo jäljellä olevaksi summaksi).  

|—|Lask.|Maksuale|Maks. maksutol.|Maksualen. pvm|Maksualen.tol. Pvm|Maksupvm|Maksu|Tol. tyyppi|Kaikki tapaht. suljettu|Maksualen.tol. KP/MR|Maksutol. KP|  
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
|1|1000|20|5|01/15/03|20.1.03|<=15.1.03|985|Maksutol.|Kyllä|0|-5|  
|2|**1,000**|**20**|**5**|**15.1.03**|**20.1.03**|**<=15.01.03**|**980**|**Ei mitään**|**Kyllä**|**0**|**0**|  
|3|1000|20|5|01/15/03|n|<=15.1.03|975|Maksutol.|Kyllä|0|5|  
|4A|1000|20|5|01/15/03|20.1.03|16.1.03 20.1.03|1005|Maksuale. tol.|Ei, 25 maksulla|20/-20|0|  
|5A|1000|20|5|01/15/03|20.1.03|16.1.03 20.1.03|1000|Maksuale. tol.|Ei, 20 maksulla|20/-20|0|  
|6A|1000|20|5|01/15/03|20.1.03|16.1.03 20.1.03|995|Maksuale. tol.|Ei, 15 maksulla|20/-20|0|  
|4B|1000|20|5|01/15/03|20.1.03|16.1.03 20.1.03|1005|Maksutol.|Kyllä|0|-5|  
|**5B**|**1,000**|**20**|**5**|**15.1.03**|**20.1.03**|**16.1.03 20.1.03**|**1000**|**Ei mitään**|**Kyllä**|**0**|**0**|  
|6B|1000|20|5|01/15/03|20.1.03|16.1.03 20.1.03|995|Maksutol.|Kyllä|0|5|  
|7|1000|20|5|01/15/03|20.1.03|16.1.03 20.1.03|985|Maksuale. tol. ja Maksutol.|Kyllä|20/-20|-5|  
|8|1000|20|5|01/15/03|20.1.03|16.1.03 20.1.03|980|Maksuale. tol.|Kyllä|20/-20|0|  
|9|1000|20|5|01/15/03|20.1.03|16.1.03 20.1.03|975|Maksuale. tol. ja Maksutol.|Kyllä|20/-20|5|  
|10|1000|20|5|01/15/03|20.1.03|>20.1.03|1005|Maksutol.|Kyllä|0|-5|  
|**11**|**1,000**|**20**|**5**|**15.1.03**|**20.1.03**|**>20.1.03**|**1000**|**Ei mitään**|**Kyllä**|**0**|**0**|  
|12|1000|20|5|01/15/03|20.1.03|>20.1.03|995|Maksutol.|Kyllä|0|5|  
|13|1000|20|5|01/15/03|20.1.03|>20.1.03|985|Ei mitään|Ei, 15 laskulla|0|0|  
|14|1000|20|5|01/15/03|20.1.03|>20.1.03|980|Ei mitään|Ei, 20 laskulla|0|0|  
|15|1000|20|5|01/15/03|20.1.03|>20.1.03|975|Ei mitään|Ei, 25 laskulla|0|0|  

### <a name="payment-range-diagrams"></a>Maksualuediagrammit  
Yo. tapaukseen liittyen maksudiagrammi on seuraavanlainen:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Maksupvm <=15.01.03 (Tapaukset 1-3)  
Jäljellä oleva summa per  

Normaalit kohdistussäännöt  

![Kertamaksutoleranssin säännöt 1](media/singlePmtTolRules(Pre1503).gif "Kertamaksutoleranssin säännöt 1")  

(1) Mikäli maksu osuu tälle välille, kaikki kohdistettavat tapahtumat voidaan sulkea toleranssilla tai ilman sitä.  

(2) Mikäli maksu osuu tälle välille kaikkia kohdistettavia tapahtumia ei voida sulkea edes toleranssilla.  

#### <a name="2-payment-date-is-between-011603-and-012003-scenarios-4-9"></a>(2) Maksupvm on välillä 16.1.03 ja 20.1.03 (Tapaukset 4-9)  
Jäljellä oleva summa per  

Normaalit kohdistussäännöt  

![Kertamaksutoleranssin säännöt 2](media/singlePmtTolRules(GracePeriod).gif "Kertamaksutoleranssin säännöt 2")  

(1) Mikäli maksu osuu tälle välille, kaikki kohdistettavat tapahtumat voidaan sulkea toleranssilla tai ilman sitä.  

(2) Mikäli maksu osuu tälle välille kaikkia kohdistettavia tapahtumia ei voida sulkea edes toleranssilla.  

#### <a name="3-payment-date-is-after-012003-scenarios-10-15"></a>(3) Maksupvm 20.01.2003 jälkeen (Tapaukset 10-15)  
Jäljellä oleva summa per  

Normaalit kohdistussäännöt  

![Kertamaksutoleranssin säännöt 3](media/singlePmtTolRules(Post0120).gif "Kertamaksutoleranssin säännöt 3")  

(1) Mikäli maksu osuu tälle välille, kaikki kohdistettavat tapahtumat voidaan sulkea toleranssilla tai ilman sitä.  

(2) Mikäli maksu osuu tälle välille kaikkia kohdistettavia tapahtumia ei voida sulkea edes toleranssilla.  

## <a name="example-2---tolerance-calculations-for-multiple-documents"></a>Esimerkki 2 – Useiden asiakirjojen toleranssilaskelmat
Seuraavassa on muutamia esimerkkejä oletetuista toleranssilaskelmista ja kirjauksista, erilaisissa tilanteissa. Nämä esimerkit rajoittuvat vain tilanteisiin, joissa kaikki kohdistettavat tapahtumat suljetaan.  

**Pääkirjanpidon asetukset** -sivulla on seuraavat asetukset:
- Maksutoleranssin ylityskausi 5P  
- Maksimi maksutoleranssi 5  

Seuraavissa tilanteissa käytössä on vaihtoehdot A, B, C tai D:  

- **A** Tässä tapauksessa maksualennuksen toleranssivaroitus on suljettu TAI käyttäjällä on varoitus käytössä ja hän on sallinut myöhästyneen maksualennuksen (Kirjaa toleranssina) jossakin laskussa.  
- **B** Tässä tapauksessa käyttäjällä on varoitus käytössä ja hän on valinnut, ettei salli myöhästynyttä maksualennusta missään laskussa.  
- **C** Tässä tapauksessa käyttäjällä on varoitus käytössä ja hän on päättänyt sallia myöhästyneen maksualennuksen ensimmäisessä laskussa mutta ei toisessa.  
- **D** Tässä tapauksessa käyttäjällä on varoitus käytössä ja hän on päättänyt ettei salli myöhästynyttä maksualennusta ensimmäisessä laskussa mutta sallii sen toisessa.  

|—|Lask.|Maksuale|Maks. maksutol.|Maksualen. pvm|Maksualen.tol. Pvm|Maksupvm|Maksu|Tol. tyyppi|Kaikki tapaht. suljettu|Maksualen.tol. KP/MR|Maksutol. KP|  
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
|1|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|<=15.1.03|1920|Maksutol.|Kyllä|0<br /><br /> 0|-5 <br />-5|  
|**2**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.1.03** <br />**17.1.03**|**20.1.03** <br />**22.1.03**|**<=15.01.03**|**1910**|**Ei mitään**|**Kyllä**|**0**<br /><br /> **0**|0 <br />0|  
|3|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|<=15.1.03|1900|Maksutol.|Kyllä|0<br /><br /> 0|5 <br />5|  
|4B|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|16.1.03 - 16.1.03|1980|Maksutol.|Kyllä|0<br /><br /> 0|-5<br /><br /> -5|  
|**5B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.1.03** <br />**17.1.03**|**20.1.03** <br />**22.1.03**|**16.1.2003 17.1.2013**|**1970**|**Ei mitään**|**Kyllä**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|6B|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|16.1.03 - 16.1.03|1960|Maksutol.|Kyllä|0<br /><br /> 0|5<br /><br /> 5|  
|7A|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|16.1.03 - 16.1.03|1920|Maksuale. tol. ja Maksutol.|Kyllä|60/60<br /><br /> 0/0|-5 <br />-5|  
|8A|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|16.1.03 - 16.1.03|1910|Maksuale. tol.|Kyllä|60/60<br /><br /> 0/0|0 <br />0|  
|9A|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|16.1.03 - 16.1.03|1900|Maksuale. tol. ja Maksutol.|Kyllä|60/60|5 <br />5|  
|10B|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|18.1.2013 20.1.2013|2010|Maksutol.|Kyllä|0<br /><br /> 0|-5<br /><br /> -5|  
|**11B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.1.03** <br />**17.1.03**|**20.1.03** <br />**22.1.03**|**18.1.2013 20.1.2013**|**2000**|**Ei mitään**|**Kyllä**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|12B|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|18.1.2013 20.1.2013|1990|Maksutol.|Kyllä|0<br /><br /> 0|5<br /><br /> 5|  
|13D|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|18.1.2013 20.1.2013|1980|Maksuale. tol. ja Maksutol.|Kyllä|0/0<br /><br /> 30/-30|-5 <br />-5|  
|14D|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|18.1.2013 20.1.2013|1970|Maksuale. tol.|Kyllä|0/0<br /><br /> 30/-30|0 <br />0|  
|15D|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|18.1.2013 20.1.2013|1960|Maksuale. tol. ja Maksutol.|Kyllä|0/0<br /><br /> 30/-30|5 <br />5|  
|16D|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|18.1.2013 20.1.2013|1950|Maksuale. tol. ja Maksutol.|Kyllä|60/-60<br /><br /> 0/0|-5 <br />-5|  
|17D|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|18.1.2013 20.1.2013|1940|Maksuale. tol.|Kyllä|60/-60<br /><br /> 0/0|0 <br />0|  
|18D|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|18.1.2013 20.1.2013|1930|Maksuale. tol. ja Maksutol.|Kyllä|60/-60<br /><br /> 0/0|5 <br />5|  
|19A|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|18.1.2013 20.1.2013|1920|Maksuale. tol. ja Maksutol.|Kyllä|60/-60<br /><br /> 30/-30|-5 <br />-5|  
|20A|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|18.1.2013 20.1.2013|1910|Maksuale. tol.|Kyllä|60/-60<br /><br /> 30/-30|0 <br />0|  
|21A|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|18.1.2013 20.1.2013|1900|Maksuale. tol. ja Maksutol.|Kyllä|60/-60<br /><br /> 30/-30|5 <br />5|  
|22B|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|21.1.2013 22.1.2013|2010|Maksutol.|Kyllä|0<br /><br /> 0|-5<br /><br /> -5|  
|**23B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.1.03** <br />**17.1.03**|**20.1.03** <br />**22.1.03**|**21.1.03 22.1.03**|**2000**|**Ei mitään**|**Kyllä**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|24B|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|21.1.2013 22.1.2013|1990|Maksutol.|Kyllä|0<br /><br /> 0|5<br /><br /> 5|  
|25A|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|21.1.2013 22.1.2013|1980|Maksuale. tol. ja Maksutol.|Kyllä|0/0<br /><br /> 30/30|-5 <br />-5|  
|26A|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|21.1.2013 22.1.2013|1970|Maksuale. tol.|Kyllä|0/0<br /><br /> 30/30|0 <br />0|  
|27A|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|21.1.2013 22.1.2013|1960|Maksuale. tol. ja Maksutol.|Kyllä|0/0<br /><br /> 30/30|5 <br />5|  
|28|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|>22.1.03|2010|Maksutol.|Kyllä|0|-5|  
|**29**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.1.03** <br />**17.1.03**|**20.1.03** <br />**22.1.03**|**>22.1.03**|**2000**|**Ei mitään**|**Kyllä**|**0**|**0**|  
|30|1000 <br />1000|60 <br />30|5 <br />5|01/15/03 <br />17.1.2013|20.1.03 <br />22.1.2013|>22.1.03|1990|Maksutol.|Kyllä|0|5|  

### <a name="payment-range-diagrams"></a>Maksualuediagrammit  
Yo. tapaukseen liittyen maksudiagrammi on seuraavanlainen:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Maksupvm <=15.01.03 (Tapaukset 1–3)  
Jäljellä oleva summa per  

Normaalit kohdistussäännöt  

:::image type="content" source="media/multiplePmtTolRules(Pre1503).gif" alt-text="Useiden maksujen toleranssin säännöt 1a":::

(1) Mikäli maksu osuu tälle välille, kaikki kohdistettavat tapahtumat voidaan sulkea toleranssilla tai ilman sitä.  

(2) Mikäli maksu osuu tälle välille kaikkia kohdistettavia tapahtumia ei voida sulkea edes toleranssilla.  

#### <a name="2-payment-date-is-between-011603-and-011703-scenarios-4-9"></a>(2) Maksupvm on välillä 16.1.03 ja 17.01.2003 (Tapaukset 4-9)  
Jäljellä oleva summa per  

Normaalit kohdistussäännöt  

:::image type="content" source="media/multiplePmtTolRules(GracePeriodInv1-2).gif" alt-text="Useiden maksujen toleranssin säännöt 2":::

(1) Mikäli maksu osuu tälle välille, kaikki kohdistettavat tapahtumat voidaan sulkea toleranssilla tai ilman sitä.  

(2) Mikäli maksu osuu tälle välille kaikkia kohdistettavia tapahtumia ei voida sulkea edes toleranssilla.  

#### <a name="3-payment-date-is-between-011803-and-012003-scenarios-10-21"></a>(3) Maksupvm on välillä 18.01.2003 ja 20.1.03 (Tapaukset 10-21)  
Jäljellä oleva summa per  

Normaalit kohdistussäännöt  

:::image type="content" source="media/multiplePmtTolRules(GracePeriodInv1).gif" alt-text="Useiden maksujen toleranssin säännöt 3":::

(1) Mikäli maksu osuu tälle välille, kaikki kohdistettavat tapahtumat voidaan sulkea toleranssilla tai ilman sitä.  

(2) Mikäli maksu osuu tälle välille kaikkia kohdistettavia tapahtumia ei voida sulkea edes toleranssilla.  

#### <a name="4-payment-date-is-between-012103-and-012203-scenarios-22-27"></a>(4) Maksupvm on välillä 21.01.2003 ja 22.01.2003 (Tapaukset 22-27)  
Jäljellä oleva summa per  

Normaalit kohdistussäännöt  

:::image type="content" source="media/multiplePmtTolRules(GracePeriodInv2).gif" alt-text="Useiden maksujen toleranssin säännöt 4":::

(1) Mikäli maksu osuu tälle välille, kaikki kohdistettavat tapahtumat voidaan sulkea toleranssilla tai ilman sitä.  

(2) Mikäli maksu osuu tälle välille kaikkia kohdistettavia tapahtumia ei voida sulkea edes toleranssilla.  

#### <a name="5-payment-date-is-after-012203-scenarios-28-30"></a>(5) Maksupvm 22.01.2003 jälkeen (Tapaukset 28-30)  
Jäljellä oleva summa per  

Normaalit kohdistussäännöt  

:::image type="content" source="media/multiplePmtTolRules(Post0122).gif" alt-text="Useiden maksujen toleranssin säännöt 5":::

(1) Mikäli maksu osuu tälle välille, kaikki kohdistettavat tapahtumat voidaan sulkea toleranssilla tai ilman sitä.  

(2) Mikäli maksu osuu tälle välille kaikkia kohdistettavia tapahtumia ei voida sulkea edes toleranssilla.

## <a name="see-also"></a>Katso myös  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]