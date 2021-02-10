---
title: Arvotapahtumien kirjauspäivämäärä
description: Lisätietoja siitä, miten Muuta kustannuksia - Nimiketapahtumat -eräajo tunnistaa ja määrittää niiden arvotapahtumien kirjauspäivämäärän, joita eräajo on luomassa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fe03f25c4f9024cb82b83af915e69073d2fdcf1e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751503"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Rakennetiedot: Muutoksen arvotapahtuman kirjauspäivämäärä
Tässä artikkelissa on ohjeita [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen varaston arvostustoimintojen käyttäjille. Tässä artikkelissa on ohjeita siitä, miten **Muuta kustannuksia - Nimiketapahtumat** -eräajo tunnistaa ja määrittää niiden arvotapahtumien kirjauspäivämäärän, joita eräajo on luomassa.  

Ensin tarkistetaan prosessin käsite eli miten eräajo tunnistaa ja määrittää luotavan arvotapahtuman kirjauspäivämäärän. Tämän jälkeen jaetaan muutamia skenaarioita, joihin tukitiimit tärmäävät silloin tällöin. Lopuksi tutustutaan versiossa 3.0 käytettävien käsitteiden yhteenvetoon.  

## <a name="the-concept"></a>Käsite  
Versiossa 5.0 **Muuta kustannuksia - Nimiketapahtumat** -eräajo määrittää kirjauspäivämäärän arvotapahtumalle, jonka se luo seuraavien vaiheiden avulla:  

1.  Alussa luotavan tapahtuman kirjauspäivämäärä on sama kuin päivämäärän, jota se muuttaa.  

2.  Kirjauspäivämäärä vahvistetaan varastokausien ja/tai pääkirjanpidon asetusten avulla.  

3.  Kirjauspäivämäärän määritys: jos alkuperäinen kirjauspäivämäärä ei kuulu sallittuun kirjauspäivämääräalueeseen, eräajo määrittää sallitu kirjauspäivämäärän pääkirjanpidon asetuksista tai varastokausista. Jos pääkirjanpidon asetuksissa on määritetty sekä varastokaudet että sallitut kirjauspäivämäärät, muutoksen arvotapahtumalle määritetään myöhempi näistä kahdesta päivämäärästä.  

 Tarkastellaan tätä prosessia lähemmin. Oletetaan, että käsittelyssä on myynnin nimiketapahtuma. Nimike on toimitettu 5.9.2013 ja laskutettu päivää myöhemmin.  

![Nimiketapahtumien tila skenaariossa](media/helene/TechArticleAdjustcost1.png "Nimiketapahtumien tila skenaariossa")  

Alla oleva ensimmäinen arvotapahtuma (379) edustaa toimitusta. Sen kirjauspäivämäärä on sama kuin päänimiketapahtuman päivämäärä.  

Toinen arvotapahtuma (381) edustaa laskua.  

 Kolmas arvotapahtuma (391) on laskutuksen arvotapahtuman (381) muutos  

 ![Arvotapahtumien tila skenaariossa](media/helene/TechArticleAdjustcost2.png "Arvotapahtumien tila skenaariossa")  

 Vaihe 1: Luotava muutoksen arvotapahtuma on määritetty samaan kirjauspäivämäärään kuin tapahtuma, jota se muuttaa, kuten yläpuolella oleva arvotapahtuma 391 osoittaa.  

 Vaihe 2: Alussa määritetyn kirjauspäivämäärän tarkistus.  

**Muuta kustannuksia - Nimiketapahtumat** -eräajo määrittää, kuuluuko muutoksen arvotapahtuman alkuperäinen kirjauspäivämäärä sallittuun kirjauspäivämääräalueeseen varastokausien ja/tai pääkirjanpidon asetusten perusteella.  

 Tarkistetaan yllämainittu myynti lisäämällä sallittujen kirjauspäivämääräalueiden asetukset.  

 Varastokaudet:  

![Varastokaudet skenaariossa](media/helene/TechArticleAdjustcost3.png "Varastokaudet skenaariossa")

 Ensimmäinen sallittu kirjauspäivämäärä on ensimmäisen avoimen kauden ensimmäinen päivä. 1.9.2013  

 Pääkirjanpidon asetukset:  

![Pääkirjanpidon asetukset skenaariossa](media/helene/TechArticleAdjustcost4.png "Pääkirjanpidon asetukset skenaariossa")

 Ensimmäinen sallittu kirjauspäivämäärä on Ensimm. sallittu kirjauspvm -kentässä mainittu päivämäärä: 10.9.2013.  

 Jos pääkirjanpidon asetuksissa on määritetty sekä varastokaudet että sallitut kirjauspäivämäärät, jälkimmäinen päivämäärä määrittää sallitun kirjauspäivämäärän.  

 Vaihe 3: Sallitun kirjauspäivämäärän määrittäminen  

 Alkuperäinen määritetty kirjauspäivämäärä oli 6.9., kuten vaiheessa 1 kerrottiin. Toisessa vaiheessa kuitenkin Muuta kustannuksia - Nimiketapahtumat -eräajo määrittää, että aikaisin sallittu kirjauspäivämäärä on 10.9. ja tämän vuoksi määrittää alla muutoksen arvotapahtumalle päivämäärän 10.9.  

 ![Arvotapahtumien tila skenaariossa 2](media/helene/TechArticleAdjustcost5.png "Arvotapahtumien tila skenaariossa 2")

 Olemme nyt käyneet läpi kirjauspäivämäärien määrittämisen arvotapahtumille, jotka Muuta kustannuksia - Nimiketapahtumat -eräajo on luonut.  

 Jatketaan tutkimalla skenaarioita, joita tukitiimi tapaa ajoittain, kun Muuta kustannuksia - Nimiketapahtumat -eräajon ja liittyvien asetusten määritettyjen kirjauspäivämäärien kohdalla.  

## <a name="scenarios"></a>Esimerkkitilanteet  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Skenaario I: Kirjauspäivämäärä ei kuulu sallittujen kirjauspäivämäärien alueeseen...  
 Tässä skenaariossa käyttäjä näkee mainitun virhesanoman, kun Muuta kustannuksia - Nimiketapahtumat -eräajo suoritetaan.  

 Edellisessä kirjauspäivämäärien määrittämistä koskevassa osassa Muuta kustannuksia - Nimiketapahtumat -eräajon tarkoitus on luoda arvotapahtuma, jonka kirjauspäivämäärä on 10.9.  

![Kirjauspäivämäärää koskeva virhesanoma](media/helene/TechArticleAdjustcost6.png "Kirjauspäivämäärää koskeva virhesanoma")

 Seurataan käyttäjäasetuksia;  

![Käyttäjän sallittujen kirjauspäivämäärien asetus](media/helene/TechArticleAdjustcost7.png "Käyttäjän sallittujen kirjauspäivämäärien asetus")

 Tässä tapauksessa käyttäjälle määritetty sallittu kirjauspäivämääräalue on 11.9. - 30.9. Muutoksen arvotapahtuman kirjauspäivämäärä ei siis voi olla 10.9.  

![Asiaankuuluvan kirjauspäivämäärän asetuksen yleiskuvaus](media/helene/TechArticleAdjustcost8.png "Asiaankuuluvan kirjauspäivämäärän asetuksen yleiskuvaus")

 Knowledge Base -artikkeli [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) sisältää lisää mainittuun virhesanomaan liittyviä skenaarioita.  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Skenaario II: Kirjauspäivämäärään verratun muutoksen arvotapahtuman kirjauspäivämäärän vuoksi muutos voi olla uudelleenarvostus tai nimikekulu.  

### <a name="revaluation-scenario"></a>Uudelleenarvostusskenaario:  
 Vaatimukset:  

 Varastonhallinnan asetukset:  

-   Automaattinen kustannusten kirjaus = Kyllä  

-   Automaattinen kustannusten muuttaminen = Aina  

-   Keskim. kust. laskentatyyppi = Nimike  

-   Keskimääräisen kustannuksen jakso = Päivä  

 Pääkirjanpidon asetukset:  

-   Ensimm. sallittu kirjauspvm = 1.1.2014  

-   Viimeinen sallittu kirjauspvm = tyhjä  

 Käyttäjäasetukset:  

-   Ensimm. sallittu kirjauspvm = 1.12.2013  

-   Viimeinen sallittu kirjauspvm = tyhjä  

##### <a name="to-test-the-scenario"></a>Skenaarion testaaminen  

1.  Luo TESTI-nimike:  

     Perusmittayksikkö = Kpl  

     Arvostusmenetelmä = Keskiarvo  

     Valitse vaihtoehtoiset kirjausryhmät.  

2.  Avaa nimikepäiväkirja ja luo ja kirjaa rivit seuraavasti:  

     Kirjauspäivämäärä = 15.12.2013  

     Nimike = TESTI  

     Tapahtuman tyyppi = Osto  

     Määrä = 100  

     Yksikkösumma = 10  

3.  Avaa nimikepäiväkirja ja luo ja kirjaa rivit seuraavasti:  

     Päivämäärä = 20.12.2013  

     Nimike = TESTI  

     Tapahtuman tyyppi = Negatiivinen muutos  

     Määrä = 2  

4.  Avaa nimikepäiväkirja ja luo ja kirjaa rivit seuraavasti:  

     Päivämäärä = 15.1.2014  

     Nimike = TESTI  

     Tapahtuman tyyppi = Negatiivinen muutos  

     Määrä = 3  

5.  Avaa uudelleenarvostuspäiväkirja ja luo ja kirjaa rivit seuraavasti:  

     Nimike = TESTI  

     Kohdistetaan tapahtumaan = valitse vaiheessa 2 kirjattu ostotapahtuma. Uudelleenarvostuksen kirjauspäivämäärä on sama kuin tapahtuman, jota se muuttaa.  

     Uudelleenarvostettu yksikkökustannus = 40  

 Seuraavat nimikekirjaukset ja arvotapahtumat on kirjattu:  

![Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 1](media/helene/TechArticleAdjustcost9.png "Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 1")

 ![Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 2](media/helene/TechArticleAdjustcost10.png "Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 2")

 Muuta kustannuksia - Nimiketapahtumat -eräajo on tunnistavut muutokset kustannuksissa ja muuttanut negatiivisia muutoksia.  

 **Luotujen muutoksen arvotapahtumien kirjauspäivämäärien tarkistaminen:** Muuta kustannuksia - Nimiketapahtumat -eräajon aikaisin sallittu kirjauspäivämäärä on 1.1.2014 pääkirjanpidon asetusten mukaan.  

 **Negatiivinen muutos vaiheessa 3:** määritetty kirjauspäivämäärä on 1.1. pääkirjanpidon asetusten mukaan. Muutoksen arvotapahtuman kirjauspäivämäärä on 20.12.2013. Pääkirjanpidon asetusten mukaan päivämäärä ei kuulu sallittuun kirjauspäivämääräalueeseen. Tämän vuoksi muutoksen arvotapahtumalle on määritetty pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän kirjauspäivämäärä.  

 **Negatiivinen muutos vaiheessa 4:** määritetty kirjauspäivämäärä on 15.1. Muutoksen arvotapahtuman kirjauspäivämäärä on 15.1., joka kuuluu sallittuun kirjauspäivämääräalueeseen pääkirjanpidon asetusten mukaan.  

 Negatiiviseen muutokseen vaiheessa 3 tehty muutos aiheuttaa keskustelua. Muutoksen arvotapahtuman suositeltu kirjauspäivämäärä olisi ollut 20.12. tai jokin muu joulukuun päivämäärä, koska myytyjen tuotteiden kustannusten muutoksen aiheuttanut uudelleenarvostus kirjattiin joulukuussa.  

 Jotta negatiiviseen muutokseen voidaan tehdä muutos joulukuussa vaiheessa 3, pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän päivämäärän on oltava joulukuussa.  

 **Yhteenveto.**  

 Tämän skenaarion kokemusten perusteella yritykselle parhaiten sopivin sallitun kirjauspäivämääräalueen asetus voisi olla noudattaa seuraavia periaatteita: niin kauan kuin varastoarvon muutokset voidaan kirjata kauden aikana, tässä tapauksessa joulukuussa, yrityksen sallitun kirjauspäivämääräalueen asetus tulee määrittää tämän mukaan. Pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kenttä, johon on määritetty 1.12., sallii joulukuussa tehdyn uudelleenarvostuksen ohjauksen edelleen saman kauden muuttuneisiin lähteviin tapahtumiin.  

 Tässä skenaariossa ollut asetus, jonka mukaan käyttäjäryhmät, jotka eivät voi tehdä kirjauksia joulukuussa, voivat tehdä niitä tammikuussa, kannattaa määrittää käyttäjäasetuksissa pääkirjanpidon asetusten sijaan.  

### <a name="item-charge-scenario"></a>Nimikekulujen skenaario:  
 Vaatimukset:  

 Varastonhallinnan asetukset:  

-   Automaattinen kustannusten kirjaus = Kyllä  

-   Automaattinen kustannusten muuttaminen = Aina  

-   Keskim. kust. laskentatyyppi = Nimike  

-   Keskimääräisen kustannuksen jakso = Päivä  

 Pääkirjanpidon asetukset:  

-   Ensimm. sallittu kirjauspvm = 1.12.2013  

-   Viimeinen sallittu kirjauspvm = tyhjä  

 Käyttäjäasetukset:  

-   Ensimm. sallittu kirjauspvm = 1.12.2013  

-   Viimeinen sallittu kirjauspvm = tyhjä  

##### <a name="to-test-the-scenario"></a>Skenaarion testaaminen  

1.  Luo nimikekulu:  

     Perusmittayksikkö = Kpl  

     Arvostusmenetelmä = Keskiarvo  

     Valitse vaihtoehtoiset kirjausryhmät.  

2.  Luo uusi ostotilaus  

     Tavarantoimittajan nro: 10 000  

     Kirjauspäivämäärä = 15.12.2013  

     Toimittajan laskunro: 1 234  

     Ostotilausrivillä:  

     Nimike = KULU  

     Määrä = 1  

     Välitön yksikkökustannus = 100  

     Kirjaa vastaanottaminen ja lasku.  

3.  Luo uusi myyntitilaus:  

     Tilausasiakkaan nro: 10000  

     Kirjauspäivämäärä = 16.12.2013  

     Myytitilausrivillä:  

     Nimike = KULU  

     Määrä = 1  

     Yksikköhinta = 135  

     Kirjaa toimitus ja lasku.  

4.  Pääkirjanpidon asetukset:  

     Ensimm. sallittu kirjauspvm = 1.1.2014  

     Viimeinen sallittu kirjauspvm = tyhjä  

5.  Luo uusi ostotilaus:  

     Tavarantoimittajan nro: 10 000  

     Kirjauspäivämäärä = 2.1.2014  

     Toimittajan laskunro: 2 345  

     Ostotilausrivillä:  

     Nimikekulu = JB-RAHTI  

     Määrä = 1  

     Välitön yksikkökustannus = 3  

     Määritä nimikekuluksi ostovastaanotto vaiheesta 2.  

     Kirjaa vastaanotto ja lasku.  

     ![Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 3](media/helene/TechArticleAdjustcost11.png "Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 3")

6.  Ostolasku saapuu käsittelypäivänä 3.1. Ostolasku sisältää vaiheessa 2 ostoon tehdyn lisäkulun. Tämän laskun asiakirjan päivämäärä on 30.12. Tämän vuoksi sen kirjauspäivämääräksi tulee 30.12.2013.  

     Luo uusi ostotilaus:  

     Tavarantoimittajan nro: 10 000  

     Kirjauspäivämäärä = 30.12.2013  

     Toimittajan laskunro: 3 456  

     Ostotilausrivillä:  

     Nimikekulu = JB-RAHTI  

     Määrä = 1  

     Välitön yksikkökustannus = 2  

     Määritä nimikekuluksi ostovastaanotto vaiheesta 2  

     Kirjaa vastaanotto ja lasku.  

   ![Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 4](media/helene/TechArticleAdjustcost12.png "Tuloksena saatavien nimike- ja arvotapahtumien yleiskuvaus 4")

 Varaston arvostus -raportti tulostetaan 31.12.2013.  

![Varaston arvostusraportin sisältö](media/helene/TechArticleAdjustcost13.png "Varaston arvostusraportin sisältö")

 **Skenaarion yhteenveto:**  

 Kuvattu skenaario loppuu Varaston arvostus -raporttiin, jossa määrä = 0 ja arvo = 2. Vaiheessa 11 kirjattu nimikekulu on osa varaston arvon nousua joulukuussa. Saman kauden varaston arvon lasku ei ole muuttunut.  

 Pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän arvo 1.1. on sopiva ensimmäiselle nimikekululle. Varaston arvon nousun ja laskun kustannukset tallennettiin samaan kauteen. Pääkirjanpidon asetusten vuoksi toinen nimikekulu aiheuttaa kuitenkin muutoksen myytyjen tuotteiden kustannuksessa. Muutos otetaan huomioon seuraavan kauden aikana.  

 **Yhteenveto.**  

 On haastavaa, kun Varaston arvostus -raportissa määritetään, että määrä = 0 samalla, kun arvo <> 0. Tässä tapauksessa on vaikeaa kertoa optimaaliset asetukset, koska ostolaskut saapuvat samana päivänä mutta ne koskevat eri kausia tai jopa eri tilivuosia. Uuteen tilivuoteen siirtäminen vaatii yleensä suunnittelua. Muuta kustannuksia - Nimiketapahtumat -prosessin on myös otettava huomioon myytyjen tuotteiden kustannukset.  

 Tässä skenaariossa eräs vaihtoehto olisi ollut määrittää pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän arvoksi muutamaa päivää aikaisempi joulukuun päivämäärä ja kirjata ensimmäinen nimikekulu viiveellä, jolloin edellisen kauden/tilivuoden kaikki kustannukset tuloutettaisiin kaudelle, jolle ne alussa kuuluivat. Tämän jälkeen suoritettaisiin Muuta kustannuksia - Nimiketapahtumat -eräajo ja siirrettäisiin sallittu kirjauspäivämäärä seuraavaan kauteen\/tilivuoteen. Kirjatuksi olisi tullut ensimmäinen nimikekulu, jonka kirjauspäivämäärä on 2.1.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Muuta kustannuksia - Nimiketapahtumat -eräajon historia  
 Alla on Muuta kustannuksia - Nimiketapahtumat -eräajon muutoksen arvotapahtumien kirjauspäivämäärien määrittämisen yhteenveto versiosta 3.0 lähtien.  

### <a name="from-version-30370a"></a>Versiosta 3.0..3.70.A lähtien  
 Muuta kustannuksia - Nimiketapahtumat -eräajon pyyntölomakkeessa on käyttäjän antama kirjauspäivämäärä. Eräajo käy läpi kaikki pakolliset muutokset ja luo arvotapahtumat, joille annetaan pyyntölomakkeen kirjauspäivämäärät. Ehdotettu kirjauspäivämäärä on tämän päivän päivämäärä.  

### <a name="version-370b40"></a>Versio 3.70.B..4.0  
 Muuta kustannuksia - Nimiketapahtumat -eräajon pyyntölomakkeessa on käyttäjän antama suljetun kauden tapahtuman kirjauspäivämäärä. Eräajo käy läpi kaikki tarvittavat muutokset ja luo arvotapahtumat ja päänimikkeen tapahtuman kirjauspäivämäärän (sen myynnin toimituspäivämäärä, jota muutos koskee). Jos päänimikkeen tapahtuma ei kuulu sallittuun kirjauspäivämääräalueeseen, suljetun kauden tapahtuman kirjauspäivämääränä ilmoitetulle kirjauspäivämäärälle määritetää muutoksen arvotapahtuma. Päivämäärä on suljetulla kaudella, kun se on aikaisempi kuin pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän päivämäärä.  

### <a name="from-version-50"></a>Versiosta 5.0 lähtien:  
 Muuta kustannuksia - Nimiketapahtumat -eräajon pyyntölomakkeessa ei ole enää ilmoitettavaa kirjauspäivämäärää. Eräajo käy läpi kaikki pakolliset muutokset ja luo arvotapahtumat, joilla on sen arvotapahtuman kirjauspäivämäärä, jonka eräajo muuttaa. Jos kirjauspäivämäärä ei kuulu sallittuun kirjauspäivämääräalueeseen, käytetään pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän kirjauspäivämäärä tai mahdollisesti käytössä olevien varastokausien kirjauspäivämäärää sen mukaan, kumpi on myöhempi. Katso edellä kuvattua käsitettä.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Kirjaa varaston kustannukset kirjanpitoon -eräajon historia  
 Kirjaa varaston kustannukset kirjanpitoon -eräajo liittyy läheisesti Muuta kustannuksia - Nimiketapahtumat -eräajoon. Tämän vuoksi kyseisen eräajon historiasta tehdään yhteenveto, joka jaetaan myös täällä.  

### <a name="from-version-30370a"></a>Versiosta 3.0..3.70.A lähtien  
 Kirjaa varaston kustannukset kirjanpitoon -eräajon pyyntölomakkeessa on käyttäjän antama kirjauspäivämäärä. Eräajo käy läpi kaikki suodattimen mahdolliset arvotapahtumat ja luo pääkirjanpidon tapahtumat, joille annetaan pyyntölomakkeen kirjauspäivämäärät.  

### <a name="version-370b40"></a>Versio 3.70.B..4.0  
 Kirjaa varaston kustannukset kirjanpitoon -eräajon pyyntölomakkeessa on käytettävissä Suljetun kauden tapahtuman kirjauspäivämäärä -kenttä. Sovellus käyttää tähän kenttään annettua päivämäärää niiden pääkirjanpidon tapahtumien kirjauspäivämääränä, jotka se luo arvotapahtumille, joiden kirjauspäivämäärät ovat suljetuilla tilikausilla. Muussa tapauksessa pääkirjanpidon tapahtumilla on samat kirjauspäivämäärät kuin alkuperäisillä arvotapahtumilla. Päivämäärä on suljetulla kaudella, kun se on aikaisempi kuin pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän päivämäärä. Jos kirjaus tehdään kirjanpitoon kirjausryhmän mukaan, pääkirjanpidon tapahtumien kirjauspäivämäärä on pyyntölomakkeen Kirjauspäivämäärä-kentässä määritetty päivämäärä.  

 Versioissa 3 ja 4 eräajo skannaa kaikki arvotapahtumat ja määrittää, löytyykö arvotapahtumia, joiden kustannussumma (todellinen) on eri kuin kirjanpitoon kirjattu kustannus. Jos eroja löytyy, eroava summa kirjataan KP-tapahtumaan. Jos käytössä on oletettujen kustannusten kirjaus, vastaavat kentät käsitellään samalla tavalla.  

![Todelliset kustannukset vs. oletetut kustannukset](media/helene/TechArticleAdjustcost14.png "Todelliset kustannukset vs. oletetut kustannukset")

### <a name="from-version-50"></a>Versiosta 5.0 lähtien:  
 Kirjaa varaston kustannukset kirjanpitoon -eräajon pyyntölomakkeessa ei ole enää ilmoitettavaa kirjauspäivämäärää. Luodaan KP-tapahtuma, jolla on sama kirjauspäivämäärä kuin liittyvällä arvotapahtumalla. Jotta eräajo voidaan suorittaa, sallitun kirjauspäivämääräalueen on sallittava luodun KP-tapahtuman kirjauspäivämäärä. Muussa tapauksessa sallittu kirjauspäivämääräalue on avattava uudelleen tilapäisesti joko muuttamalla päivämääriä tai poistamalla niitä pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm- ja Viimeinen sallittu kirjauspvm -kentissä. Vältät täsmäytysongelmat, kun KP-tapahtuman kirjauspäivämäärä vastaa arvotapahtuman kirjauspäivämäärää.  

 Kirjaa arvotapahtuma kirjanpitoon -eräajo skannaa taulukon 5811 ja tunnistaa alueeseen kuuluvat arvotapahtumat pääkirjanpitoon kirjaamista varten. Kun eräajo on suoritettu, taulukko tyhjennetään.

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)  
[Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md)  
