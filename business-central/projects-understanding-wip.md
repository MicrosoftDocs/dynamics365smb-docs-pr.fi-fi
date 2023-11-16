---
title: KET-menetelmien laskeminen ja projektin edistymisen kirjaaminen
description: 'Tässä artikkelissa kerrotaan KET-menetelmistä, joilla kirjataan, seurataan ja lasketaan keskeneräisen projektien rahoitustietoja.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'work in process, work in progress, calculate project WIP'
ms.search.form: 1010
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="understanding-wip-methods-in-project-management"></a>Tietoja projektinhallinnan KET-menetelmistä

Projektin edetessä kulutetaan materiaaleja, resursseja ja muita kuluja, ja nämä on kirjattava projektiin. Keskeneräinen työ (KET) on ominaisuus, jonka avulla voit arvioida kirjanpidossa olevien projektien taloudellisen arvon projektin ollessa meneillään. Monissa tapauksissa saatat kirjata projektille kuluja ennen projektin laskuttamista. Kun projektista on kirjattu vain kuluja, rahoituslaskelma on epätarkka.

Voit seurata arvoa kirjanpidossa laskemalla KET:n ja kirjaamalla arvon kirjanpitoon. Lisätietoja on kohdassa [Projektin edistymisen ja suorituskyvyn](projects-how-monitor-progress-performance.md)valvominen.

[!INCLUDE[prod_short](includes/prod_short.md)] tukee seuraavia keskeneräisen työn arvon laskennan ja kirjaamisen menetelmiä.

| KET-menetelmä | Laskentakaava | Laskennan kuvaus |
| --- | --- | --- |
| Kustannusarvo |Tuloutettu tuotto = laskutettava laskutettu hinta <br /><br />Budjetin kustannusten suhde = Budjetin kokonaiskustannukset / budjetin kokonaishinta <br /><br />Arvioidut kokonaiskustannukset = laskutettava kokonaishinta x budjetin kustannusten suhde <br /><br />Valmistumisen %-osuus = käytön kokonaiskustannukset / budjetoidut kokonaiskustannukset <br /><br />Laskutettu % = laskutettava laskutettu hinta / laskutettava kokonaishinta <br /><br />KET-kustannus = (valmistumisen %-osuus - laskutettu -%) * arvioidut kokonaiskustannukset <br /><br />Tuloutetut kustannukset = käytön kokonaiskustannukset - KET-kustannukset|Kustannusarvon laskelmat aloitetaan laskemalla tuotettujen arvo. Se tehdään ottamalla osa valmistumisen prosenttiosuuteen perustuvista arvioiduista kustannuksista. Laskutetut kustannukset vähennetään ottamalla osa laskutettuun prosenttiin perustuvista arvioiduista kokonaiskustannuksista.<br /><br />Tämä laskenta vaatii, että koko projektin laskutettava kokonaishinta, budjetoitu kokonaishinta ja budjetoidut kokonaiskustannukset on syötettävä oikein. |
| Myynnin kulut |Tuloutettu tuotto = laskutettava laskutettu hinta<br /><br /> Tuloutetut kustannukset = budjetoidut kokonaiskustannukset x laskutettu prosenttiosuus<br /><br /> Laskutettu % = laskutettava laskutettu hinta / laskutettava kokonaishinta<br /> (Laskutettu % on projektitehtävärivin sarake)<br /><br /> KET-kustannukset = käytön kokonaiskustannukset - tuloutetut kustannukset |Myynnin kulujen laskeminen alkaa tuloutettujen kustannusten laskemisella. Kustannukset tuloutetaan suhteessa budjetin kokonaiskustannuksiin.<br /><br /> Tämä laskenta vaatii, että koko projektin laskutettava kokonaishinta ja budjetin kokonaiskustannukset on syötettävä oikein. |
| Myyntiarvo |Tuloutetut kustannukset = käytön kokonaiskustannukset<br /><br /> Tuloutettu tuotto = käytön kokonaishinta x odotettu laskutuksen suhde<br /><br /> Kustannusten korvaus-% = laskutettava kokonaishinta / budjetin kokonaishinta<br /><br /> KET-myynti = tuloutettu myynti - laskutettava laskutettu hinta |Myyntiarvon laskelmat tulouttavat tuoton suhteessa käytön kokonaiskustannuksiin ja odotettuihin kustannuksiin korvaussuhteen perusteella.<br /><br /> Tämä laskenta vaatii, että koko projektin laskutettava kokonaishinta ja budjetin kokonaishinta on syötettävä oikein. |
| Valmistumisen prosenttiosuus |Tuloutetut kustannukset = käytön kokonaiskustannukset<br /><br /> Tuloutettu tuotto = laskutettava kokonaishinta x valmistumisen %-osuus<br /><br /> Valmistumisen %-osuus = käytön kokonaiskustannukset / budjetoidut kokonaiskustannukset<br /> (Tallennetaan projektitehtäväriveillä **Kustannuksen valmistumisprosentti** -kenttään)<br /><br /> KET-myynti = tuloutettu myynti - laskutettava laskutettu hinta |Valmistumisen %-osuuden laskennat tulouttavat tuoton suhteessa valmistumisen prosenttiosuuteen (eli käytön kokonaiskustannuksiin ja budjetin kustannuksiin).<br /><br /> Tämä laskenta vaatii, että koko projektin laskutettava kokonaishinta ja budjetin kokonaiskustannukset on syötettävä oikein. |
| Valmis sopimus |KET-summa = KET-kustannusten summa = käyttö (kokonaiskustannukset)<br /><br /> KET-myynnin summa = laskutettava (laskutettu hinta) |Valmis sopimus ei tulouta tuottoa ja kustannuksia ennen projektin valmistumista. Tästä voi olla hyötyä, kun projektin kustannusten ja tuoton arviointi on hyvin epävarmaa.<br /><br /> Kaikki käyttö kirjataan KET-kustannusten tilille (saatavat) ja kaikki laskutettu myynti kirjataan laskutetun KET-myynnin tilille (velat), kunnes projekti on valmis. |

## <a name="see-also"></a>Katso myös

[Projektien hallinta](projects-manage-projects.md)  
[Taloushallinto](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
