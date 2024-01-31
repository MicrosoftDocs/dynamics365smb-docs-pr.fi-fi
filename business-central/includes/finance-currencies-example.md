---
author: brentholtorf
ms.topic: include
ms.date: 03/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Kun saat laskun yritykseltä ulkomaan valuutassa, laskun paikallisen valuutan (PVA) arvo on melko helppo laskea tämän päivän valuuttakurssin perusteella. Laskussa on kuitenkin usein maksuehdot, joiden nojalla voit viivyttää maksua myöhemmälle päivämäärälle, mikä taas tarkoittaa mahdollisesti erilaista valuuttakurssia. Kun vielä pankkien valuuttakurssit eroavat aina virallisista valuuttakursseista, on mahdotonta ennakoida tarkkaa paikallisen valuutan (PVA) summaa, joka tarvitaan laskun kattamiseen. Jos laskun eräpäivä ulottuu seuraavaan kuukauteen, saatat joutua myös uudelleenarvostamaan paikallisen valuutan (PVA) summan kuun lopussa. Valuutan oikaisu on tarpeen, koska laskun summan kattamiseen tarvittava uusi PVA-arvo saattaa olla erilainen, ja yrityksen velka toimittajalle on mahdollisesti muuttunut. Uusi PVA-summa voi olla edellistä summaa suurempi tai pienempi, joten se edustaa voittoa tai tappiota. Koska laskua ei ole kuitenkaan vielä maksettu, voiton tai tappion katsotaan olevan *toteutumaton*. Myöhemmin lasku maksetaan, ja pankki palauttaa maksun todellisen valuuttakurssin mukaisesti. Vasta nyt lasketaan *toteutunut* voitto tai tappio. Tämä toteutumaton voitto tai tappio peruutetaan ja toteutunut voitto tai tappio kirjataan sen sijaan.

Seuraavassa esimerkissä lasku vastaanotetaan 1.1., ja valuuttasumma on 1 000. Valuuttakurssi on 1,123.

|Pvm|Toiminto|Valuuttasumma|Asiakirjan pvm|PVA-summa asiakirjassa|Oikaisukurssi|Toteutumattomien voittojen summa|Maksukurssi|Realisoituneiden tappioiden summa|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Lasku**|1000|1,123|1 123|||||
|1/31|**Muutos**|1000||1 125|1,125|2|||
|2/15|**Maksun peruutuksen muutos**|1000||||-2|||
|2/15|**Maksu**|1000||1 120|||1,120|-3|

Kuukauden lopussa suoritetaan valuutan muuttaminen, jossa muutoksen valuuttakurssiksi on asetettu 1,125, mikä laukaisee toteutumattoman voiton 2.

Maksuhetkellä pankkitapahtumaan rekisteröity todellinen valuuttakurssi näyttää valuuttakurssia 1,120.

Tähän sisältyy toteutumaton tapahtuma, ja siksi se peruutetaan yhdessä maksun kanssa.

Lopuksi maksu rekisteröidään ja todellinen tappio kirjataan realisoituneen tappion tilille.
