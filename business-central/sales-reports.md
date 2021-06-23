---
title: Myyntiraportit ja analytiikka
description: Katso, mitkä myyntiraportit ja mikä analytiikka on saatavilla Business Centralin vakioversiossa, jotta voit seurata liiketoimintaasi.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: a8ada1c8488e8c5dec581db98dccf02d89da21c3
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216346"
---
# <a name="sales-reports-and-analytics-in-business-central"></a>Business Centralin myyntiraportit ja analytiikka

[!INCLUDE [prod_short](includes/prod_short.md)] -myyntiraporttien avulla myynnin ja liiketoiminnan ammattilaiset voivat saada merkityksellistä tietoa ja analytiikkaa nykyisistä ja aiemmista myyntitoiminnoista.  

## <a name="reports"></a>Raportit

Seuraavassa taulukossa kuvataan joitakin myyntiraportoinnin keskeisiä raportteja.

|Raportti |Objektin tunnus|Kuvaus  |
|---------|---------|---------|
|**Asiakas – Tilausyhteenveto**|107| Tässä raportissa on jokaisen asiakkaan tilauserittely (ei vielä toimitettu määrä) kolmessa 30 päivän jaksossa alkaen määritetystä päivämäärästä. Raportissa on myös sarakkeita, joissa on tilauksia, jotka toimitetaan ennen näitä kolmea ajanjaksoa ja niiden jälkeen, ja sarake, jossa on jokaisen asiakkaan kokonaistilauserittely. Raporttia voidaan käyttää analysoimaan yrityksen odotettua liikevaihtoa. |
|**Asiakkaat – 10 pääasiakasta**|111| Tässä raportissa näkyy tietoja asiakkaiden ostoista ja saldoista valitulta ajanjaksolta. Voit valita raporttiin sisällytettävien asiakkaiden määrän. Vain ne asiakkaat, joilla on joko ostoja jakson aikana tai saldo jakson lopussa, sisällytetään.<br>Asiakkaat lajitellaan summan mukaan, ja voit valita, lajitellaanko ne myyntisummittain vai saldoittain. Raportin avulla saa nopean yleissilmäyksen asiakkaista, jotka ostavat eniten, ja asiakkaista, jotka ovat eniten velkaa.|
|**Asiakas-/nimikemyynti**|113|Tässä raportissa näkyy luettelo nimikemyynneistä kunkin asiakkaan osalta tietyltä ajanjaksolta. Raportissa on tietoja määrästä, myyntisummasta, tuotosta ja mahdollisista alennuksista. Sitä voidaan käyttää esimerkiksi analysoimaan yrityksen asiakasryhmiä.|
|**Varasto – Asiakasmyynti**|713|Fyysisen varastoinnin näkökulman yleiskuvaus. Tämä näkymä on erilainen verrattuna **Asiakas-/nimikemyynti**-raporttiin. Siinä näkyy ensimmäisenä nimike ja sitten asiakas, joka osti tätä tuotetta.|
|**Asiakas – Myyntiluettelo**|119|Näyttää asiakkaan myynnin aikajaksolta. Sitä käytetään tulli- ja veroviranomaisraportoinnissa. Voit valita sisällytettäväksi vain asiakkaaat, joiden kokonaismyynti ylittää minimisumman. Voit myös määrittää, haluatko raportin näyttävän jokaisen asiakkaan osoitetiedot.<br>Raportti perustuu asiakastapahtumien kirjattuihin myynteihin (PVA). Raportoitujen myyntien yhteissumma näkyy PVA:na raportin alareunassa. Yhteissumma perustuu asiakkaisiin, jotka olet sisällyttänyt raporttiin, eli asiakkaisiin, jotka ovat Asiakas-pikavälilehdessä määritettyjen suodattimien ehtojen mukaisia ja joiden myyntien yhteissumma on suurempi kuin summa, joka on määritetty **Summat (PVA) suurempia kuin** -kentässä **Asetukset**-pikavälilehdessä.|
|**Asiakas – Saldo tähän mennessä**|121|Näyttää valittujen asiakkaiden eritellyn saldon. Raporttia voi käyttää esimerkiksi kirjanpitojakson tai tilikauden päättyessä.|
|**Asiakas – Alustava saldo**|129|Tässä raportissa näkyy valittujen asiakkaiden eritelty saldo. Voit käyttää raporttia sen varmistamiseen, että asiakaskirjausryhmän saldon vastaa liittyvän KP-tilin saldoa tiettynä päivämääränä. Raporttia voi käyttää esimerkiksi kirjanpitojakson tai tilikauden päättyessä. Jos tarvitset yksityiskohtaisemman version tämäntyyppisestä raportista, käytä **Asiakastiedot Alustava saldo** (104) -raporttia.|
|**Myynnin tilastot**|112|Tässä raportissa näkyvät jokaisen asiakkaan osalta myynti-, tuotto-, laskualennus- ja maksualennussummat (PVA) sekä tuottoprosentti. Kustannukset ja tuotot näkyvät sekä alkuperäisinä että muutettuina. Alkuperäiset kustannukset ja tuotot ovat kirjaamisen yhteydessä laskettuja, kun taas muutetuissa kustannuksissa ja tuotoissa näkyvät myyntien nimikkeiden alkuperäisiin hintoihin tulleet muutokset. Raportissa näkyvä kustannuksen muutossumma on alkuperäisen kustannuksen ja muutetun kustannuksen erotus.<br>Luvut on jaoteltu kolmelle ajanjaksolle. Näiden jaksojen pituuden voi määritellä alkamaan valitusta päivämäärästä. Raportissa on myös sarakkeet summille ennen kolmea ajanjaksoa ja niiden jälkeen. Raporttia voidaan käyttää esimerkiksi yksittäiseltä asiakkaalta saatujen tulojen sekä tulokehityksien analysoimiseen. |
|**Myyntivarausten saatavuus**|209|Tässä raportissa näkyy myyntiasiakirjojen osalta nimikesaatavuus toimitusta varten. Määritä, näkyykö raportissa jokaisen asiakirjan vai jokaisen myyntirivin tila. Raporttia tulostaessasi voit myös päivittää toimitukseen saatavilla olevan määrän myyntirivien **Toimitettava määrä** -kenttään. Sitten voit käyttää raporttia määrittämään, mitkä asiakirjat kirjataan.<br>On myös toiminto, jonka avulla voit määrittää toimitettavien tavaroiden määrän. **Huomautus**: Tämä raportti ei ole käytettävissä varaston lisätoiminnoissa.|
|**Fyysisen varaston toimituksen tila**|7313|Tätä raporttia voidaan käyttää kaikissa sijainneissa, joissa **Vaadi toimitus** -kenttä on valittu. **Fyysisen varaston toimituksen tila** -raportissa näkyvät kaikki kirjaamattomat fyysisen varastoinnin toimitusasiakirjat, kuten sijainnit, varastopaikkakoodit, asiakirjan tila ja määrät. Tämä raportti on täydellinen yleiskuvan saamiseen.|
|**Varaston poimintaluettelo**|813|Raportissa näkyy luettelo myyntitilauksista, joihin nimike sisältyy. Jokaisesta nimikkeestä näkyvät seuraavat tiedot: asiakkaan nimen sisältävä myyntitilausrivi, varianttikoodi, sijantikoodi, var.paikkakoodi, toimituspäivämäärä, toimitettava määrä ja mittayksikkö. Toimitettava määrä lasketaan yhteen jokaisen nimikkeen osalta. Raporttia voidaan käyttää silloin, kun nimikkeet poimitaan varastosta.<br>**Huomautus**: Tämä raportti ei ole käytettävissä varaston lisätoiminnoissa.|
|**Varasto – Myynnin jälkitoim.**|718|Tässä raportissa on luettelo, jossa on tilausrivit, joiden lähetyksen päivämäärä on mennyt ohi. Kunkin nimikkeen yksittäisistä tilauksista näytetään seuraavia tietoja: numero, asiakkaan nimi, asiakkaan puhelinnumero, lähetyksen päivämäärä, tilausmäärä ja jälkitoimituksen määrä. Raportissa näkyy myös se, onko asiakkaalle muita nimikkeitä jälkitoimituksessa.|



## <a name="tasks"></a>Tehtävät

Seuraavissa artikkeleissa kuvataan joitakin yrityksen tilan analysointiin liittyviä keskeisiä tehtäviä:

* [Analyysiraporttien luominen](bi-how-create-analysis-views-reports.md)  
* [Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)


## <a name="see-also"></a>Katso myös

[Myynnin määrittäminen](sales-setup-sales.md)  
[Myynti](sales-manage-sales.md)  
[Nimikkeiden varaaminen](inventory-how-to-reserve-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
