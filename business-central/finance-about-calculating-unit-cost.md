---
title: Tietoja yksikkökustannuslaskennasta
description: 'Tutustu siihen, miten arvostusmenetelmä ja muut tekijät vaikuttavat nimikekortin yksikkökustannukseen.'
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: article
ms.date: 03/06/2022
ms.author: bholtorf
---
# <a name="about-unit-cost-calculation"></a>Tietoja yksikkökustannuslaskennasta

Kullakin nimikkeellä on yksikkökustannus, joka lasketaan yrityksen arvostusmenetelmän ja muiden tekijöiden perusteella. *Vakio*-arvostusmenetelmässä sääntönä on, että **Yksikkökustannus**-kentän arvo perustuu nimikkeen vakiokustannukseen. Kaikissa muissa arvostusmenetelmissä (*FIFO*, *LIFO*, *Spesifi* ja *Keskiarvo*) yksikköhinta lasketaan tietyn ajan keskimääräisen yksikkökustannuksen perusteella.  

Lisätietoja on kohdassa [Varaston kustannusten hallinta](finance-manage-inventory-costs.md).  

## <a name="when-is-the-unit-cost-field-updated"></a>Yksikkökustannuksen kentän päivittämisaika

Valittu arvostusmenetelmä vaikuttaa siihen, milloin **Yksikkökustannus**-kenttä päivitetään.

Kun arvostusmenetelmänä on *Vakio*, **Yksikkökustannus**-kenttä päivitetään aina, kun vakiokustannusta muutetaan, ja käyttäjät eivät voi muokata **Yksikkökustannus**-kenttää. Lisätietoja on kohdassa [Vakiokustannusten päivittäminen](finance-how-to-update-standard-costs.md).

Jos arvostusmenetelmänä on *FIFO*, *LIFO*, *Spesifi* tai *Keskiarvo*, **Yksikkökustannus** päivitetään seuraavissa tapauksissa:

* Kun nimikkeen kustannukset tarkistetaan automaattisesti tai [Tarkista kustannus](inventory-how-adjust-item-costs.md#to-adjust-item-costs-manually) -tehtävällä.
* Ostolaskujen kirjauksen yhteydessä, tuotos tai positiivinen muutos, jos jokin seuraavista ehdoista toteutuu:
  * Nimikkeen laskutettu nettomäärä muuttuu negatiivisesta tai nollasta positiiviseksi.
  * Nykyinen yksikkökustannus on nolla.

Jos jokin näistä ehdoista on tosi, **Yksikkökustannus**-kenttä päivitetään nimikekortin **Viimeisin välitön kustannus** -kentän arvolla.

> [!NOTE]
> **Yksikkökustannus**-kenttää ei päivitetä, jos nykyinen yksikkökustannus on suurempi kuin nolla ja uusi yksikkökustannus on nolla. Jos yksikkökustannus on nolla, se katsotaan poikkeukseksi normaalista liiketoiminnasta. Siksi nykyinen yksikkökustannus säilytetään antamaan viimeisin tunnettu, merkityksellisin arvo. Tämä poikkeus pätee, vaikka olemassa oleva varasto olisi arvostettu uudelleen nollaan.

Nimikekortin **Yksikkökustannus**-kentässä voit porautua tarkastelemaan tapahtumahistoriaa, jonka perusteella varastossa olevien yksikköjen keskimääräinen hinta **Keskimääräisten kustannusten laskennan yleiskuvaus** -ikkunassa lasketaan.

## <a name="unit-cost-calculation-for-purchases"></a>Yksikkökustannusten laskeminen ostoille

Aina kun ostat nimikkeitä, nimikekortin **Viimeinen välitön kustannus** -kentän arvo kopioidaan ostorivin **Välitön yksikkökustannus** -kenttään tai nimikepäiväkirjan rivin **Yksikkösumma**-riville.

Se, mitä valitset **Kustannustapa**-kentässä vaikuttaa siihen, miten [!INCLUDE[prod_short](includes/prod_short.md)] laskee **Yksikkökustannus**-kentän sisällön riveillä.

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Kustannusmenetelmä FIFO, LIFO, Spesifi tai Keskimäärä

[!INCLUDE[prod_short](includes/prod_short.md)] laskee ostorivin **Yksikkökustannus PVA** -kentän sisällön tai nimikepäiväkirjan rivin **Yksikkökustannus**-kentän sisällön seuraavan laskukaavan mukaan:

*Yksikkökustannus (PVA) = (Välitön yksikkökustannus - (Alennussumma / Määrä)) * (1 + Välillinen kustannus-% / 100) + Yleiskustannus*

### <a name="costing-method-standard"></a>Arvostusmenetelmä Vakio

Järjestelmä syöttää **yksikkökustannus (PVA)** -kentän ostoriville sekä **yksikkökustannus** -kentän nimikepäiväkirjalle kopioimalla arvon nimikekortin **yksikkökustannus** -kentästä. Jos arvostustapa on *Vakio*, perustuu kustannus aina vakiokustannukseen.

Kun kirjaat oston, [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelma käyttää ostorivin tai nimikepäiväkirjan yksikkökustannusta oston nimikelaskutapahtumaan. Sen voi nähdä nimikkeen tapahtumaluettelossa

### <a name="all-costing-methods"></a>Kaikki arvostusmenetelmät

Lähdeasiakirjan rivin yksikkökustannusta käytetään kyseiseen nimiketapahtumaan liittyvän **Kustannussumma todellinen** -kentän (tai tarpeen mukaan **Kustannussumma oletettu** -kentän) sisällön laskennassa huolimatta siitä, mikä nimikkeen arvostusmenetelmä on.

## <a name="unit-cost-calculation-for-sales"></a>Myynnin yksikkökustannusten laskenta

Kun myyt nimikkeitä, ohjelma kopioi yksikkökustannuksen nimikekortin **Yksikkökustannus**-kentästä myyntiriville tai nimikepäiväkirjan riville.

Kirjauksen yhteydessä ohjelma kopioi yksikkökustannuksen myyntilaskun nimiketapahtumaan, ja se näkyy nimikkeen tapahtumaluettelossa. [!INCLUDE[prod_short](includes/prod_short.md)] käyttää lähdeasiakirjan rivin yksikkökustannusta kyseiseen nimiketapahtumaan liittyvän arvotapahtuman **Kustannussumma todellinen** -kentän (tai tarpeen mukaan **Kustannussumma oletettu** -kentän) sisällön laskennassa.

## <a name="see-also"></a>Katso myös

[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Tietoja varaston kustannuslaskennasta](finance-learn-about-costing.md)  
[Varasto](inventory-manage-inventory.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Suunnittelun yksityiskohdat: vähennyskelvoton ALV](design-details-nondeductible-vat.md)
[Asetukset - parhaat käytännöt: Arvostusmenetelmä](setup-best-practices-costing-method.md)  
[Rakennetiedot: Kustannuslaskennan menetelmät](design-details-costing-methods.md)  
[Rakennetiedot: Kustannuksen muutos](design-details-cost-adjustment.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
