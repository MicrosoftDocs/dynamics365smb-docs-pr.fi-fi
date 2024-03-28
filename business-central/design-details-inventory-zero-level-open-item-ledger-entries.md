---
title: Nollavaraston avoimien nimiketapahtumien merkinnät
description: 'Tässä artikkelissa kerrotaan ongelmasta, jossa varastomäärä on nolla, vaikka avoimia nimiketapahtumia on.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Rakennetiedot: Nimikkeen kohdistuksen tunnettu ongelma
Tässä artikkelissa kerrotaan ongelmasta, jossa varastomäärä on nolla, vaikka [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa on avoimia nimiketapahtumia.  

Artikkelin alussa kerrotaan ongelman tyypilliset oireet. Tämän jälkeen käsitellään nimikkeen kohdistuksen perusteita, jotka tukevat tämän ongelman kuvattuja syitä. Artikkelin lopussa kerrotaan ratkaisu avointen nimiketapahtumien ongelmaan.  

## Ongelman oireet  
 Jos varastomäärä on nolla, vaikka avoimia nimiketapahtumia on olemassa, oireet ovat yleensä seuraavat:  

-   Kun varastokautta yritetään sulkea, näyttöön tulee seuraava sanoma: Varastoa ei voi sulkea, koska vähintään yhdellä nimikkeellä on negatiivista varastoa.  

-   Nimiketapahtuma, jossa sekä lähtevä nimiketapahtuma että siihen liittyvä saapuva nimiketapahtuma ovat avoimia.  

     Katso seuraava esimerkki nimiketapahtumasta.  

     |Tapahtumanro|Kirjauspäivämäärä|Tapahtuman tyyppi|Asiakirjatyyppi|Asiakirjanumero|Nimikenro|Sijaintikoodi|Määrä|Kustannussumma (todellinen)|Laskutettu määrä|Jäljellä oleva määrä|Avaa|  
     |---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
     |333|28.1.2018|Myynti|Myyntitoimitus|102043|TESTI|SININEN|-1|-10|-1|-1|Kyllä|  
     |334|28.1.2018|Myynti|Myyntitoimitus|102043|TESTI|SININEN|1|10|1|1|Kyllä|  

## Nimikkeen kohdistuksen perusteet  
 Nimikkeen kohdistustapahtuma luodaan jokaiselle varastotapahtumalle, jotta kustannusten vastaanottaja voidaan linkittää kustannusten vastaanottajan kustannuslähteeseen. Näin kustannus voidaan välittää edelleen arvostusmenetelmän mukaisesti. Katso lisätiedot kohdasta [Rakennetiedot: nimikkeen kohdistus](design-details-item-application.md).  

-   Saapuvalle nimiketapahtumalle luodaan nimikkeen kohdistustapahtuma nimiketapahtuman luomisen yhteydessä.  

-   Lähtevälle nimiketapahtumalle luodaan nimikkeen kohdistustapahtuma nimiketapahtuman kirjaamisen yhteydessä, jos olemassa on avoin saapuva nimiketapahtuma, jonka käytettävissä olevaan määrään kohdistustapahtuma voidaan kohdistaa. Jos avointa saapuvaa nimiketapahtumaa, johon kohdistus voidaan tehdä, ei ole, lähtevä nimiketapahtuma pysyy avoimena niin kauan, kunnes saapuva nimiketapahtuma, johon kohdistus voidaan tehdä, kirjataan.  

 Nimikkeen kohdistuksen kaksi tyyppiä ovat seuraavat:  

-   Määrän kohdistus  

-   Kustannusten kohdistus  

### Määrän kohdistus  
 Määrän kohdistukset tehdään kaikille varastotapahtumille. Ne luodaan automaattisesti, mutta erityisissä prosesseissa manuaalisesti. Kun määrän kohdistukset tehdään manuaalisesti, niitä kutsutaan kiinteiksi kohdistuksiksi.  

 Seuraavassa kaaviossa näytetään, miten määrän kohdistukset tehdään.  

![Kustannusten oikaisuprosessi ostoista myyntiin.](media/helene/TechArticleInventoryZero2.png "Kustannusten oikaisuprosessi ostoista myyntiin")

 Huomaa, että nimiketapahtuma 1 (osto) on sekä nimikkeen toimittaja että kohdistetun nimiketapahtuman kustannuslähde, nimiketapahtuma 2 (myynti).  

> [!NOTE]  
>  Jos lähtevä nimiketapahtuma arvostetaan keskimääräisen kustannuksen mukaan, kohdistettu saapuva nimiketapahtuma ei ole yksilöivä kustannuslähde. Sen sijaan se on kauden keskimääräisen kustannuksen laskennan osa.  

### Kustannusten kohdistus  
Kustannusten kohdistukset luodaan vain niille saapuville tapahtumille, joissa **Kohdistus nimiketapahtumasta** -kenttä täytetään kiinteän kohdistuksen antamiseksi. Tämä tapahtuu yleensä myyntihyvityslaskun tai toimitusskenaarion peruuttamisen yhteydessä. Kustannuksen kohdistus varmistaa, että nimike lisää varaston uudelleen käyttämällä toimituksen kustannusta.  

Seuraavassa kaaviossa näytetään, miten kustannusten kohdistukset tehdään.  

|Tapahtumanro|Kirjauspäivämäärä|Tapahtuman tyyppi|Asiakirjatyyppi|Asiakirjanumero|Nimikenro|Sijaintikoodi|Määrä|Kustannussumma (todellinen)|Laskutettu määrä|Jäljellä oleva määrä|Avaa|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
|333|28.1.2018|Myynti|Myyntitoimitus|102043|TESTI|SININEN|-1|-10|-1|-1|Kyllä|  
|334|28.1.2018|Myynti|Myyntitoimitus|102043|TESTI|SININEN|1|10|1|1|Kyllä|  

 Huomaa, että saapuva nimiketapahtuma 3 (myyntipalautus) on alkuperäisen lähtevän nimiketapahtuman (myynti) kustannusten vastaanottaja.  

## Peruskustannusvirran kuva  
 Oletetaan, että täydellinen kustannusvirta, jossa nimike vastaanotetaan, toimitetaan ja laskutetaan. Se palautetaan\-täydellisen kustannuksen palautuksen kanssa ja toimitetaan uudelleen.  

 Seuraavassa kaaviossa esitetään kustannusvirta.  

![Kustannusten oikaisuprosessi myynnistä myyntipalautuksiin.](media/helene/TechArticleInventoryZero4.png "Kustannusten oikaisuprosessi myynnistä myyntipalautuksiin")

 Huomaa, että kustannus ohjataan edelleen nimiketapahtumalle 2 (myynti), tämän jälkeen nimiketapahtumalle 3 (myyntipalautus) ja lopulta nimiketapahtumalle 4 (myynti 2).  

## Ongelman syyt  
 Syy siihen, että varastomäärä on nolla, vaikka avoimia nimiketapahtumia on olemassa, voi olla jompikumpi seuraavista skenaarioista:  

-   Skenaario 1: Toimitus ja lasku on kirjattu, vaikka nimike ei ole käytettävissä. Tällöin kirjaus peruutetaan todellisten kustannusten perusteella myyntihyvityslaskun kanssa.  

-   Skenaario 2: Toimitus on kirjattu, vaikka nimike ei ole käytettävissä. Kirjaus peruutetaan Peruuta toimitus -toiminnon avulla.  

 Seuraavassa kaaviossa näytetään, miten nimikkeen kohdistukset tehdään kummassakin skenaariossa.  

![Kustannusten oikaisuprosessi tapahtuu molempiin suuntiin.](media/helene/TechArticleInventoryZero6.png "Kustannusten oikaisuprosessi tapahtuu molempiin suuntiin")  

 Huomaa, että kustannuksen kohdistus (siniset nuolet) tehdään, jotta voidaan varmistaa nimiketapahtuman 2 (myyntipalautus) liittäminen samoihin kustannuksiin, joihin sen peruuttama nimiketapahtuma 1 (myynti 1) on liitetty. Määrän kohdistusta (punaiset nuolet) ei tehdä.  

 Nimiketapahtuma 2 (myyntipalautus) ei voi olla samalla sekä alkuperäisen nimiketapahtuman kustannusten vastaanottaja että nimikkeiden ja niiden kustannuslähteiden toimittaja. Tämän vuoksi alkuperäinen nimiketapahtuma 1 (myynti 1) on auki, kunnes sallittu lähde löytyy.  

## Ongelman tunnistaminen  
 Voit määrittää, onko avoimia nimiketapahtumia luotu, tekemällä seuraavat toiminnot vastaavassa skenaariossa:  

 Tunnista ongelma skenaariossa 1 seuraavasti:  

-   Hae **Kirjattu myyntihyvityslasku**- tai **Kirjattu palautusvastaanotto** -sivulla **Kohdistus \-nimiketapahtumasta** -kenttä ja tarkista, onko kenttä täytetty. Jos on, tarkista, mihin nimiketapahtumaan palautusvastaanoton kustannus on kohdistettu.  

 Tunnista ongelma skenaariossa 2 jommallakummalla tavalla:  

-   Etsi avoin lähtevä ja saapuva nimiketapahtuma, joilla on samat numerot **Asiakirjanumero**-kentässä ja Kyllä-arvo **Korjaus**-kentässä. Katso seuraava esimerkki tällaisesta nimiketapahtumasta.  

|Tapahtumanro|Kirjauspäivämäärä|Tapahtuman tyyppi|Asiakirjatyyppi|Asiakirjanumero|Nimikenro|Sijaintikoodi|Määrä|Kustannussumma (todellinen)|Laskutettu määrä|Jäljellä oleva määrä|Avaa|Korjaus|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|---------|
|333|28.1.2018|Myynti|Myyntitoimitus|102043|TESTI|SININEN|-1|-10|-1|-1|Kyllä|Ei|  
|334|28.1.2018|Myynti|Myyntitoimitus|102043|TESTI|SININEN|1|10|1|1|Kyllä|**Kyllä**|  

-   Hae **Kirjattu myyntitoimitus** -sivulla **Kohdistus nimiketapahtumasta** -kenttä ja tarkista, onko kenttä täytetty. Jos on, tarkista, mihin nimiketapahtumaan palautusvastaanoton kustannus on kohdistettu.  

> [!NOTE]  
>  Kustannusten kohdistuksia ei voi tunnistaa **Kohdistetut nimiketapahtumat** -sivulla, koska siinä näkyvät vain määrän kohdistukset.  

 Tunnista mukana olevat kustannusten kohdistukset seuraavasti molemmissa skenaarioissa:  

1.  Avaa **Nimikkeen kohdistustapahtuma** -taulukko.  

2.  Suodata **Nimiketapahtuman nro** -kentän avulla käyttämällä myyntipalautuksen nimiketapahtuman numeroa.  

3.  Analysoi nimiketapahtuma ja ota huomioon seuraavat asiat:  

     Jos saapuvan nimiketapahtuman (positiivinen määrä) **Lähtevän nimiketapahtuman nro** -kenttä on täytetty, saapuva nimiketapahtuma on lähtevän nimiketapahtuman kustannusten vastaanottaja.  

     Katso seuraava esimerkki nimikkeen kohdistustapahtumasta.  

     |Tapahtumanro|Nimiketapahtuman nro|Saapuvan nimiketapahtuman nro|Lähtevän nimiketapahtuman nro|Määrä|Kirjauspäivämäärä|Kustannusten kohdistus|  
     |---------|---------------------|----------------------|-----------------------|--------|------------|----------------|  
     |299|334|334|333|1|28.1.2018|Kyllä|  
<!--![Why is inventory zero 8.](media/helene/TechArticleInventoryZero8.png "Whyisinventoryzero\_8")  -->

 Huomaa, että saapuvan nimiketapahtuman 334 kustannukset on kohdistettu lähtevään nimiketapahtumaan 333.  

## Ongelman ratkaisu  
 Kirjaa **Nimikepäiväkirja**-sivulla kyseisen nimikkeen seuraavat rivit:  

-   Positiivinen muutos, kun avoin lähtevä nimiketapahtuma suljetaan.  

-   Negatiivinen muutos, kun määrä on sama.  

     Tämä muutos täsmäyttää positiivisen muutoksen aiheuttaman varaston arvonlisäyksen ja sulkee avoimen saapuvan nimiketapahtuman.  

 Tuloksena varaston määrä on nolla ja kaikki nimiketapahtumat suljetaan.  

## Katso myös  
[Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md)   
[Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]