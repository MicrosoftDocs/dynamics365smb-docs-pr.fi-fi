---
title: Resurssien kohdistaminen | Microsoft Docs
description: Huoltosopimuksen tai sopimustarjouksen vuosittaista summaa voidaan muuttaa, jos vuosittain laskutettavaa summaa tarvitsee korjata.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5360e9d25b463673e2a1b033b9f8564d0f483301
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---

# <a name="allocate-resources"></a>Resurssien kohdistaminen
Huollon toimittavat henkilöt ovat huoltohallinnon tärkein elementti. Voit määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittämään henkilöt heille soveltuviin projekteihin. Toimeksiannot voivat perustua henkilön tai huollon sijainnin mukaisiin huoltoalueisiin. Lisäksi resurssit voi ryhmitellä yhteen huoltopyyntöihin vastattaessa. Lisätietoja on kohdassa [Resurssien kohdistamisen määrittäminen](service-how-setup-resource-allocation.md).

Huoltonimikkeille kohdistetaan resursseja, esimerkiksi teknikoita, käyttämällä **Lähetystaulukko**, tai huoltotilauksesta. Voit kohdistaa resurssit niiden saatavuuden mukaan suorittamaan tilausten tai tarjousten huoltotehtäviä.

Saman resurssin (esimerkiksi teknikon) tai resurssiryhmän voi kohdistaa kaikille huoltotilauksessa oleville huoltonimikkeille. Ohjelma luo kohdistustapahtumat kaikille tilauksessa oleville huoltonimikkeille, joilla on sama resurssinumero ja kohdistuspäivämäärä kuin kohdistamallasi rivillä. Kohdistetut tunnit ovat tunteja, jotka kohdistit ja jotka on jaettu tilauksessa olevien huoltonimikkeiden lukumäärällä. Kaikkien luotujen tapahtumien **Tila**-kentän arvoksi asetetaan automaattisesti **Aktiivinen**.

## <a name="to-see-an-overview-of-service-orders-and-service-quotes"></a>Huoltotilausten tai -tarjousten yleistilanteen katsominen  
Käyttäjä voi tarvita tiettyjen ehtojen mukaista huoltotilausten ja/tai huoltotarjousten luetteloa, kun tilauksille tai tarjouksille halutaan tehdä toimia yksi kerrallaan. Voit esimerkiksi haluta kohdistaa tietylle asiakkaalle kuuluville huoltotilauksille resursseja.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Lähetystaulukko** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Asiakirjan suodatus** -kentässä, minkä tyyppisiä asiakirjoja haluat tarkastella.
3. Jos haluat nähdä luettelon sellaisia huoltotehtäviä sisältävistä asiakirjoista, joihin on kohdistettu tietty resurssi tai resurssiryhmä, täytä **Resurssisuodatus**- ja **Resurssiryhmän suodatus** -kentät ja paina Enter-näppäintä.  
4. Jos haluat nähdä luettelon asiakirjoista, joiden vastauspäivämäärä tai -päivämäärät ovat tietyn päivämääräjakson sisällä, täytä **Vastauspvm suodatus**-kenttä ja paina **Enter**-näppäintä.  
5. Jos haluat nähdä luettelon asiakirjoista, joilla on tietty kohdistus- tai asiakirjatila, täytä **Kohdistuksen suodatus ja tilan suodatus** -kenttä ja paina **Enter**-näppäintä.  
6. Jos haluat nähdä luettelon asiakirjoista, jotka kuuluvat tiettyyn sopimukseen tai tietylle asiakkaalle tai alueelle, täytä **Sopimussuodatus, asiakassuodatus tai alueen suodatus** -kenttä ja paina **Enter**-näppäintä.  
7. Valitse huoltotilausta tai huoltotarjousta vastaava rivi ja valitse sitten **Näytä asiakirja** -toiminto.  

    **Huoltotilaus**- tai **Huoltotarjous** -ikkuna avautuu, ja voit käsitellä asiakirjaa. Palaa **Lähetystaulukko**-sivulle valitsemalla **OK**.

## <a name="to-allocate-a-resource-using-resource-or-resource-group-availability"></a>Resurssin kohdistaminen resurssin tai resurssiryhmän saatavuuden avulla    
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Lähetystaulukko** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse ensin huoltotilaus ja sitten **Resurssin kohdistukset** -toiminto.  
3. Valitse tapahtuma, jossa on huoltotehtävä, johon haluat kohdistaa resurssin.  
4. Valitse joko **Resurssin saatavuus**- tai **Resurssiryhmän saatavuus** -toiminto.  
5. Valitse **Res. saatavuus (huolto)** -ikkunassa **Näytä matriisi**.  
6. Valitse kohdistettava resurssi. Voit perustaa valintasi riippumatta siitä, onko resurssi sopiva tehtävää varten, sijaitseeko se asiakkaan alueella ja/tai onko se asiakkaan ensisijainen valinta.  
7. Määritä päivämäärä, jolloin resurssilla on tarpeeksi tunteja tehtävälle ja joka on lähellä huoltotilauksen vastauspäivämäärää.  
8. Anna **Kohdistettava määrä** -kenttään tuntimäärä, jonka ajaksi haluat kohdistaa resurssin huoltotehtävälle.  
9. Valitse **Toiminnot**-välilehti **Toiminnot**-ryhmässä, valitse **Kohdista** ja kohdista valittu resurssiryhmä valittuun päivämäärään.  

     **Tila**-kentän arvoksi asetetaan automaattisesti **Aktiivinen**.  

 Toista nämä vaiheet kunkin päivämäärän osalta, jolloin haluat kohdistaa resurssin huoltotehtävälle.  

> [!NOTE]  
>  Huoltotilauksessa olevalla huoltonimikkeellä voi olla vain **aktiivisia** kohdistustapahtumia, joissa on yksi resurssi tai resurssiryhmä kerralla.  

## <a name="to-allocate-a-resource-using-a-service-order"></a>Resurssien kohdistaminen huoltotilausta käyttämällä:  
Kun huoltotilaus tai tilaustarjous on luotu ja täytetty, voidaan asiakirjan huoltonimikeriveiksi rekisteröidyille huoltotehtäville kohdistaa resurssit (esimerkiksi teknikoita).  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltotilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse ensin huoltotilaus ja sitten **Muokkaa**.  
3. Valitse sen huoltotehtävän huoltonimikerivi, jolle haluat kohdistaa resursseja.  
4. Valitse **Resurssin kohdistukset**.
5. Valitse **Resurssin kohdistukset** -ikkunassa muu kuin aktiivinen kohdistustapahtuma, joka sisältää kohdistettavan huoltotehtävän. Jos kohdistustapahtumaa ei ole, voit luoda uuden valitsemalla **Uusi**.  
7. Määritä huoltotehtävä täyttämällä **Huoltonimikkeen nro.** kenttä samalla rivillä.  
8. Valitse resurssi **Resurssin nro** -kentässä. Jos resurssi kuuluu resurssiryhmään, ohjelma täyttää automaattisesti resurssiryhmän numeron **Resurssiryhmän nro** -kentässä.  
9. Täytä **Kohdistuspvm**- ja **Kohdistetut tunnit** -kentät. **Tila**-kentän arvoksi asetetaan **Aktiivinen**. Tämä tarkoittaa, että resurssi on kohdistettu huoltotehtävään.  
10. Jos sen sijaan haluat määrittää resurssin kaikille nimikkeille, valitse **Kohd. kaikkiin huoltonimik**.

> [!NOTE]  
>  Huoltotilauksessa olevalla huoltonimikkeellä voi olla vain aktiivisia kohdistustapahtumia, joissa on yksi resurssi tai resurssiryhmä kerralla.

## <a name="to-reallocate-resources-on-a-service-order"></a>Huoltotilauksen resurssien uudelleenkohdistaminen  
Resursseja voidaan kohdistaa uudelleen suoraan huoltotilauksesta tai huoltotarjouksesta tätä käsiteltäessä. Alkuperäinen tapahtuma on edelleen olemassa, mutta sen tila päivitetään seuraavalla tavalla:  

* Jos huolto aloitettiin silloin, kun kohdistus oli **Aktiivinen** (eli tapahtumassa olevan huoltonimikkeen korjauksen tilaksi muutettiin **Työn alla**), ohjelma muuttaa kohdistuksen tilan **Uudelleenkohdistus tarvitaan** **Valmiiksi**.  
* Jos huoltoa ei aloitettu silloin, kun kohdistus oli **Aktiivinen**, ohjelma muuttaa kohdistuksen tilan **Uudelleenkohdistus tarvitaan** **Peruutetuksi**.  
* Jos olet kohdistamassa uudelleen huoltotilausta, jonka olet muuntanut tarjouksesta, ohjelma muuttaa aina tarjoukselle rekisteröityjen kohdistustapahtumien tilaksi **Valmis** silloin, kun huoltotilauksessa olevia huoltonimikkeitä uudelleenkohdistetaan.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltotilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Avaa haluamasi huoltotilaus.  
3. Napsauta sen huoltotehtävän huoltonimikeriviä, jolle haluat kohdistaa resursseja.  Valitse ensin **Toiminnot**, sitten **Rivi** ja lopuksi **Resurssin kohdistukset**.  
4. Valitse **Resurssin kohdistukset** -ikkunasta kohdistustapahtuma, joka sisältää uudelleen kohdistuksen kohteena olevan huoltotehtävän. Valitse **Resurssin nro** -kentässä asianmukainen resurssi. Se korvaa kentässä jo olevan resurssinumeron.  
5. Paina Enter-näppäintä. Näyttöön tulee valintaikkuna, jossa kysytään, haluatko kohdistaa tapahtuman uudelleen. Täytä **Syykoodi**-kenttä tarvittaessa ja vahvista uudelleenkohdistus valitsemalla **Kyllä**.  
6. Täytä **Kohdistuspvm**- ja **Kohdistetut tunnit** -kentät. Tapahtuma sisältää nyt uuden resurssin, ja sen tila on **Aktiivinen**.

## <a name="to-reallocate-a-resource-using-the-dispatch-board"></a>Resurssien kohdistaminen lähetystaulukkoa käyttämällä  
Jos huoltotehtävään kohdistettu resurssi ei kykene suorittamaan tehtävää, on kyseiselle huoltotehtävälle kohdistettava uusi resurssi. Huoltotehtäviin kohdistetaan uusia resursseja tavallisesti **lähetystaulukkoa** käyttämällä.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Lähetystaulukko** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Kohdistuksen suodatus** -kentässä **Uudelleenkohdistamista tarvitaan**. **Lähetystaulukko**-ikkunaan tulee nyt luettelo huoltotilauksista, joissa on uudelleenkohdistamista tarvitsevia huoltotehtäviä.  
3. Avaa haluamasi huoltotilaus. Valitse **Navigoi**-välilehden **Suunnittelu**-ryhmässä **Resurssin kohdistukset**. **Resurssin kohdistukset** -ikkuna aukeaa.  
4. Valitse kohdistustapahtuma, jossa on huoltotehtävä, johon haluat kohdistaa uuden resurssin.  
5. Valitse **Resurssin nro** -kentässä asianmukainen resurssi. Se korvaa kentässä jo olevan resurssinumeron.  
6. Paina Enter-näppäintä. **Tapahtuman uudelleenkohdistuksen syyt** -valintaikkuna aukeaa, jossa kysytään, haluatko uudelleenkohdistaa tapahtuman. Täytä **Syykoodi**-kenttä tarvittaessa ja vahvista uudelleenkohdistus valitsemalla **Kyllä**.  
7.  Täytä **Kohdistuspvm**- ja **Kohdistetut tunnit** -kentät. Tapahtuma sisältää nyt uuden resurssin, ja sen tila on **Aktiivinen**.  

    > [!NOTE]  
    >  Vanha tapahtuma on edelleen olemassa, mutta ohjelma päivittää sen tilan seuraavalla tavalla:  
    >   
    >  * Jos huolto aloitettiin silloin, kun kohdistus oli **Aktiivinen** (eli tapahtumassa olevan huoltonimikkeen korjauksen tilaksi muutettiin **Työn alla**), ohjelma muuttaa kohdistuksen tilan **Uudelleenkohdistus tarvitaan** **Valmiiksi**.  
    > * Jos huoltoa ei aloitettu silloin, kun kohdistus oli **Aktiivinen**, ohjelma muuttaa kohdistuksen tilan **Uudelleenkohdistus tarvitaan** **Peruutetuksi**.  
    > * Jos olet kohdistamassa uudelleen huoltotilausta, jonka olet muuntanut tarjouksesta, tarjoukselle rekisteröityjen kohdistustapahtumien tilaksi muutetaan **Valmis** aina silloin, kun huoltotilauksessa olevia huoltonimikkeitä uudelleenkohdistetaan.  

## <a name="to-register-resource-hours"></a>Resurssituntien rekisteröiminen  
Kun työskentelet huoltotilauksissa olevien huoltonimikkeiden parissa, huollolle käytetyt resurssitunnit tulee rekisteröidä. Seuraavassa kuvataan, miten resurssitunnit rekisteröidään **Huoltonimikkeen työkirja** -ikkunassa.  

Samaa menettelyä voidaan käyttää rekisteröimään tunteja **Huoltorivit** -ikkunassa, jonka voit avata Huoltotilaus -ikkunasta. Avaa käsiteltävä huoltokortti ja valitse ensin **Toiminnot**, sitten **Tilaus** ja lopuksi **Huoltorivit**.  

Jos sama resurssi työskentelee kaikkien huoltotilauksessa olevien huoltonimikkeiden parissa, kokonaisresurssitunnit voi rekisteröidä vain yhdelle huoltonimikkeelle ja resurssirivi jakaa sitten resurssituntien määrittelemiseksi muille huoltonimikkeille.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltotehtävät** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse ensin huoltonimikkeen sisältävä rivi ja sitten **Nimikkeen työkirja** -toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-resource-to-all-service-items-in-an-order"></a>Resurssien kohdistaminen kaikkiin tilauksen huoltonimikkeisiin
Jos sama resurssi (esimerkiksi teknikko) työskentelee kaikkien huoltotilauksessa olevien huoltonimikkeiden parissa, kokonaisresurssitunnit voi rekisteröidä vain yhdelle huoltonimikkeelle ja resurssirivin voi sitten jakaa, jotta resurssitunnit voidaan jakaa resurssiriveille muiden huoltonimikkeiden osalta.  

Seuraavassa kuvataan, miten resurssirivejä jaetaan **Huoltolaskun rivit** -ikkunassa.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltotilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Avaa haluamasi huoltotilaus.  
3. Valitse **Rivit**-pikavälilehdessä ensin **Toiminnot**, sitten **Tilaus** ja lopuksi **Huoltorivit**. **Huoltorivit**-ikkuna aukeaa.  
4. Napsauta resurssiriviä, jonka haluat jakaa. Ohjelma jakaa **Määrä**-kentän sisällön kaikkien tilauksessa olevien huoltonimikkeiden kesken.  
5. Valitse **Toiminnot**-välilehdessä **Jaa resurssirivi** -toiminto. Vahvista valinta valitsemalla **Kyllä**.  

    Ohjelma luo resurssirivejä muille tilauksessa oleville huoltonimikkeille, joilla on sama resurssinumero kuin jakamallasi rivillä. Määrä on määrä jakamasi rivin osalta jaettuna tilauksessa olevien huoltonimikkeiden lukumäärällä.  

## <a name="to-cancel-an-allocation"></a>Kohdistusten peruuttaminen  
Voit peruuttaa huoltotehtävien resurssien kohdistukset ilman, että tehtävät on kohdistettava uudelleen.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Lähetystaulukko** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse ensin huoltotilaus ja sitten **Resurssin kohdistukset** -toiminto.  
3. Valitse se kohdistustapahtuma, jossa on huoltotehtävä, jonka osalta haluat peruuttaa kohdistuksen.  
4. Valitse **Peruuta kohdistus** -toiminto.  
5. Valitse **Syykoodi**-kentässä asianmukainen syykoodi.  
6. Vahvista peruutus valitsemalla **Kyllä**.  

    > [!NOTE]  
    > Ohjelma valitsee automaattisesti **Uudelleenkohdistamista tarvitaan** -vaihtoehdon **Tila**-kentässä. Jos tapahtumassa olevan huoltonimikkeen korjauksen tila on **Alku**, ohjelma muuttaa korjauksen tilaksi **Lykätty** (huoltoa ei ole aloitettu). Jos korjauksen tila on **Työn alla**, ohjelma muuttaa korjauksen tilaksi **Osittain huollettu** (osa huollosta on suoritettu loppuun).

## <a name="see-also"></a>Katso myös
[Resurssien kohdistamisen määrittäminen](service-how-setup-resource-allocation.md)  
[Kohdistuksen tila ja korjauksen tila](service-allocation-status-and-repair-status.md)  

