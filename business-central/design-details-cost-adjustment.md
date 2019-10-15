---
title: Rakennetiedot – Kustannusten muuttaminen | Microsoft Docs
description: Kustannusten sopeuttamisen päätarkoitus on siirtää eteenpäin kustannusmuutokset kustannuslähteistä kustannusten vastaanottajille nimikkeen kustannuslaskentamenetelmän mukaisesti, jotta se tuottaisi oikean varaston arvostuksen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 79633ad4488a5fbe9df372331c54dd3a0e15f929
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303674"
---
# <a name="design-details-cost-adjustment"></a>Rakennetiedot: kustannuksen muutos
Kustannusten muuttamisen päätarkoitus on siirtää eteenpäin kustannusmuutokset kustannuslähteistä kustannusten vastaanottajille nimikkeen kustannuslaskentamenetelmän mukaisesti, jotta se tuottaisi oikean varaston arvostuksen.  

Nimike voidaan myyntilaskuttaa ennen kuin se ostolaskutetaan niin, että myynnin tallennettu varastoarvo ei vastaa todellista ostokustannusta. Kustannusten muutos päivittää vanhojen myyntitapahtumien myytyjen tuotteiden kustannusta (MTK) sen varmistamiseksi, että ne vastaavat saapuvien tapahtumien kustannuksia joihin niitä käytetään. Katso lisätiedot kohdasta [Rakennetiedot: nimikkeen kohdistus](design-details-item-application.md).  

Seuraavat ovat kustannusten sopeuttamisen toissijaisia tarkoituksia tai toimintoja:  

* Valmiiden tuotantotilausten laskuttaminen:  

    * Arvotapahtumien tilan muutos **Oletettu**-tilasta **Todelliseksi**.  
    * Tyhjennä KET-tilit. Katso lisätietoja kohdasta [Rakennetiedot: tuotantotilauksen kirjaus](design-details-production-order-posting.md).  
    * Kirjaa varianssi. Katso lisätietoja kohdasta [Rakennetiedot: varianssi](design-details-variance.md).  

* Nimikkeen kortin yksikkökustannuksen päivittäminen.  

Varaston kustannuksia on muutettava ennen kuin liittyvät arvotapahtumat voi täsmäyttää pääkirjanpidon kanssa. Lisätietoja on kohdassa [Rakennetiedot: täsmäytys pääkirjanpidon kanssa](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="detecting-the-adjustment"></a>Muutoksen havaitseminen  
Nimikepäiväkirja - kirjaa rivi -rutiini määrittää ensisijaisesti sen, tuleeko kustannuksia muuttaa, kun taas kustannusten muuttamisen tapahtumien laskemisen ja luomisen suorittaa **Muuta kustannuksia - Nimiketapahtumat** -eräajo.  

Kun haluat siirtää kustannukset eteenpäin, tunnistusmekanismi määrittää kustannusten muuttuneet lähteet ja kohteet, joihin nämä kustannukset tulisi siirtää. Seuraavat kolme havaintotoimintoa ovat olemassa kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

* Nimikkeen kohdistustapahtuma  
* Keskimääräinen kustannusten oikaisun tulopaikka  
* Tilauksen taso  

### <a name="item-application-entry"></a>Nimikkeen kohdistustapahtuma  
Tätä tunnistustoimintoa käytetään nimikkeissä, jotka käyttävät FIFO-, LIFO- tai Vakio-arvostusmenetelmään tai spesifistä arvostusmenetelmää ja myös kiinteän kohdistuksen skenaarioita. Toiminto toimii seuraavasti:  

* Hinnan muutos havaitaan merkitsemällä lähdenimiketapahtumat arvolla *Kohdist. tapaht. muutettavaksi*, aina kun nimiketapahtuma tai arvotapahtuma kirjataan.  
* Kustannus siirretään eteenpäin kustannusketjujen mukaan, jotka on kirjattu **Nimikkeen kohdistustapahtuma** -taulukossa.  

### <a name="average-cost-adjustment-entry-point"></a>Keskimääräinen kustannusten oikaisun tulopaikka  
Tätä tunnistustoimintoa käytetään nimikkeissä, jotka käyttävät keskimääräistä arvostusmenetelmää. Toiminto toimii seuraavasti:  

* Kustannusten muuttaminen havaitaan merkitsemällä tietue **Keskim. kust. muutoksen tulopaikka** -taulukossa aina, kun arvotapahtuma kirjataan.  
* Kustannus siirretään eteenpäin soveltamalla kustannukset arvotapahtumiin, joilla on myöhäisempi arvostuspäivämäärä.  

### <a name="order-level"></a>Tilauksen taso  
Tätä tunnistustoimintoa käytetään muunnoksen skenaarioissa, tuotannossa ja kokoonpanossa. Toiminto toimii seuraavasti:  

* Kustannusten muuttaminen havaitaan merkitsemällä tilaus aina, kun materiaali/resurssi kirjataan kulutetuksi/käytetyksi.  
* Kustannus siirretään eteenpäin soveltamalla kustannukset materiaalista/resurssista tuotostapahtumiin, jotka on liitetty samaan tilaukseen.  

Tilaustason toimintoa käytetään havaitsemaan kokoonpanotiliöinnin määrittämisessä. Seuraavassa kaaviossa esitetään sopeuttamiskirjauksen rakenne:  

![Kustannusmuutoksen tapahtumavirta](media/design_details_assembly_posting_3.png "Kustannusmuutoksen tapahtumavirta")  

Lisätietoja on kohdassa [Rakennetiedot: Kokoonpanotilauksen kirjaus](design-details-assembly-order-posting.md).  

## <a name="manual-versus-automatic-cost-adjustment"></a>Manuaalinen kustannusten muuttaminen verrattuna automaattiseen kustannusten muuttamiseen  
Kustannusten muuttaminen voidaan tehdä kahdella tavalla:  

* Manuaalisesti suorittamalla **Muuta kustannuksia - Nimiketapahtumat** -eräajon. Voit suorittaa tämän eräajon kaikille nimikkeille tai vain tietyille nimikkeille tai nimikeluokille. Tämä eräajo muuttaa varaston niiden nimikkeiden kustannuksia, joille on tehty lähtevä tapahtuma, kuten osto. Keskiarvo-arvostusmenetelmää käyttävien nimikkeiden eräajo suorittaa myös oikaisun, jos luodaan lähteviä tapahtumia.  
* Automaattisesti säätämällä kustannukset joka kerta, kun kirjaat varastotapahtuman ja kun suoritat tuotantotilauksen loppuun. Kustannusten sopeuttaminen on käytössä vain tietylle nimikkeelle tai nimikkeille, joita tiliöinti koskee. Tämä määritetään **Varastonhallinnan asetukset** -sivun **Automaattinen kustannusten muuttaminen** -valintaruudun valinnan yhteydessä.  

On hyvän käytännön mukaista suorittaa kustannuksen muuttaminen automaattisesti kirjauksen yhteydessä, koska yksikkökustannukset päivitetään useammin ja tämän vuoksi tarkemmin. Haittana on se, että tietokannan toimintaan voidaan vaikuttaa suorittamalla kustannusten sopeuttaminen niin usein.  

Koska nimikkeen yksikkökustannuksen pitäminen ajan tasalla on tärkeää, on suositeltavaa, että suoritat **Muuta kustannuksia - Nimiketapahtumat** -eräajon niin usein kuin mahdollista työajan ulkopuolella. Voit käyttää vaihtoehtoisesti myös automaattista kustannusten muuttamista. Tämä varmistaa, että nimikkeiden yksikkökustannus päivitetään päivittäin.  

Muutosprosessi ja sen seuraukset ovat samat, suoritettiin kustannusten muutos manuaalisesti tai automaattisesti. [!INCLUDE[d365fin](includes/d365fin_md.md)] laskee saapuvien tapahtumien arvon ja siirtää tämän kustannuksen mihin tahansa lähteviin tapahtumiin, kuten myynnit tai menekki, joita on sovellettu saapuviin tapahtumiin. Kustannusten sopeuttaminen luo arvokirjauksia, jotka sisältävät sopeuttamissummia ja summia, jotka kompensoivat pyöristystä.  

Uusissa sopeuttamis- ja pyöristysarvokirjauksissa on liittyvän laskun tiliöintipäivä. Poikkeuksen muodostavat arvotapahtumat, jotka osuvat suljetulle kirjanpitojaksolle tai varastokaudelle tai jos kirjauspäivämäärä on aiemmin kuin **Ensimm. sallittu kirjauspvm** -kentän päivämäärä **Pääkirjanpidon asetukset** -sivulla. Jos näin tapahtuu, eräajo määrittää kirjauspäivämääräksi seuraavan avoimen jakson ensimmäisen päivämäärän.  

## <a name="adjust-cost---item-entries-batch-job"></a>Muuta kustann. - Nimiketapaht. -eräajo  
Kun **Muuta kustannuksia - Nimiketapahtumat** -eräajo suoritetaan, se voidaan suorittaa kaikille nimikkeille tai vain tietyille nimikkeille tai luokille.  

> [!NOTE]  
>  Eräajo kannattaa aina suorittaa kaikille nimikkeille. Suodatustoimintoa kannattaa käyttää vain ajonaikaisten eräajojen vähentämiseksi tai tietyn nimikkeen kustannusten korjaamiseksi.  

### <a name="example"></a>Esimerkki  
Seuraavassa esimerkissä kuvataan se, jos tiliöit ostonimikkeen vastaanotetuksi ja laskutetuksi 01-01-20. Myöhemmin kirjaat myydyn nimikkeen toimitetuksi ja laskutetuksi 15.1.2020. Suorita sitten **Muuta kustannuksia - Nimiketapahtumat** ja **Kirjaa varaston kustannus KP:oon** -eräajot. Seuraavat tapahtumat luodaan.  

**Arvotapahtumat**  

|Kirjauspvm|Nimiketapahtuman tyyppi|Kustannussumma (Tod.)|KP:oon kirjattu kustannus|Laskutettu määrä|Tapahtumanro|  
|------------------|----------------------------|----------------------------|-------------------------|-----------------------|---------------|  
|01-01-20|Osto|10,00|10,00|1|1|  
|01-15-20|Myynti|-10.00|-10.00|-1|2|  

**Liittyvät kirjaukset G/L – nimikkeen pääkirjan suhdetaulukko**  

|KP-tapahtuman nro|Arvotapahtumanro|KP-rekisterin nro|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  

**Pääkirjanpidon tapahtumat**  

|Kirjauspvm|KP-tili|Tilinro (En-US-esittely)|Summa|Tapahtumanro|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|[Varastotili]|2130|10,00|1|  
|01-01-20|[Välitön kust. kohdistettutili]|7291|-10.00|2|  
|01-15-20|[Varastotili]|2130|-10.00|3|  
|01-15-20|[COGS-tili]|7290|10,00|4|  

Myöhemmin kirjaat liittyvän oston nimikekulun 2,00 PVA, laskutettu 10.2.2000. Suorita sitten **Muuta kustannuksia - Nimiketapahtumat** -eräajo ja sen jälkeen **Kirjaa varaston kustannus KP:oon** -eräajo. Kustannusten muuttamisen eräajo säätää myyntikustannukset -2,00 PVA:n mukaan ja **Kirjaa varaston kustannus KP:oon** -eräajo kirjaa uudet arvotapahtumat pääkirjaan. Tulos on seuraavanlainen.  

**arvotapahtumat**  

|Kirjauspvm|Nimiketapahtuman tyyppi|Kustannussumma (Tod.)|KP:oon kirjattu kustannus|Laskutettu määrä|Muutos|Tapahtumanro|  
|------------------|----------------------------|----------------------------|-------------------------|-----------------------|----------------|---------------|  
|02-10-20|Osto|2,00|2,00|0|Ei|3|  
|01-15-20|Myynti|-2.00|-2.00|0|Kyllä|4|  

**Liittyvät kirjaukset G/L – nimikkeen pääkirjan suhdetaulukko**  

|KP-tapahtuman nro|Arvotapahtumanro|KP-rekisterin nro|  
|--------------------|---------------------|-----------------------|  
|5|3|2|  
|6|3|2|  
|7|4|2|  
|8|4|2|  

**Pääkirjanpidon tapahtumat**  

|Kirjauspvm|KP-tili|Tilinro (En-US-esittely)||Summa|Tapahtumanro|  
|------------------|------------------|---------------------------------|-|------------|---------------|  
|02-10-20|[Varastotili]|2130||2,00|5|  
|02-10-20|[Välitön kust. kohdistettutili]|7291||-2.00|6|  
|01-15-20|[Varastotili]|2130||-2.00|7|  
|01-15-20|[COGS-tili]|7290||2,00|8|  

## <a name="automatic-cost-adjustment"></a>Automaattinen kustannusten muuttaminen  
Voit määrittää kustannusten muutoksen automaattiseksi varastotapahtuman kirjaamisen yhteydessä käyttämällä **Varastonhallinnan asetukset** -sivun **Automaattinen kustannusten muuttaminen** -kenttää. Tämän kentän avulla voit valita, millainen ajanjakso nykyistä käsittelypäivämäärää edeltävältä ajalta sisällytetään automaattiseen kustannusten muuttamiseen. Käytettävissä ovat seuraavat vaihtoehdot.  

|Asetus|Description|  
|----------------------------------|---------------------------------------|  
|Ei koskaan|Kustannuksia ei muuteta, kun suoritat kirjauksen.|  
|Päivä|Kustannuksia muutetaan, jos kirjauspäivämäärän ja käsittelypäivämäärän ero on enintään yksi päivä.|  
|Viikko|Kustannuksia muutetaan, jos kirjauspäivämäärän ja käsittelypäivämäärän ero on enintään yksi viikko.|  
|Kuukausi|Kustannuksia muutetaan, jos kirjauspäivämäärän ja käsittelypäivämäärän ero on enintään yksi kuukausi.|  
|Neljännes|Kustannuksia muutetaan, jos kirjauspäivämäärän ja käsittelypäivämäärän ero on enintään yksi vuosineljännes.|  
|Vuosi|Kustannuksia muutetaan, jos kirjauspäivämäärän ja käsittelypäivämäärän ero on enintään yksi vuosi.|  
|Aina|Kustannuksia muutetaan kirjauspäivämäärästä riippumatta aina, kun kirjaat.|  

Tämä valinta, jonka teet **Automaattinen kustannusten muuttaminen** -kentässä, on tärkeä kustannusten suorituskyvylle ja tarkkuudelle. Lyhyemmät ajanjaksot, kuten **Päivä** tai **Viikko**, vaikuttavat järjestelmän toimintaan vähemmän, koska niillä on tiukemmat vaatimukset, joka maksaa vain, kun se on annettu edellisenä päivänä, tai viikkoa voidaan säätää automaattisesti. Tämä tarkoittaa, että automaattista kustannusten muuttamista ei suoriteta yhtä usein. Tämän vuoksi se vaikuttaa järjestelmän suorituskykyyn vähemmän. Tämä tarkoittaa kuitenkin myös sitä, että yksikkökustannukset voivat olla vähemmän tarkkoja.  

### <a name="example"></a>Esimerkki  
Seuraavassa esimerkissä kuvataan automaattinen kustannusten sopeuttamisskenaario:  

* 10. tammikuuta kirjaat ostetun nimikkeen vastaanotetuksi ja laskutetuksi.  
* 15. tammikuuta kirjaat myyntitilauksen nimikkeelle toimitetuksi ja laskutetuiksi.
* 5. helmikuuta vastaanotat laskun alkuperäisen oston rahtikuluista. Kirjaa tämä rahtikulu ja kohdista se alkuperäiseen ostolaskuun. Tämä nostaa alkuperäisen oston kustannuksia.  

Jos olet asettanut automaattisen kustannusten muutoksen käytettäväksi kirjauksissa, jotka tapahtuvat kuukauden tai neljännesvuoden sisällä nykyisestä työpäivästä, automaattinen kustannusten muutos suoritetaan ja se siirtää oston kustannuksen myyntiin.  

Jos olet määrittänyt automaattisia kustannuksen muutoksia kirjauksiin, jotka tapahtuvat päivän tai viikon kuluessa nykyisestä työpäivästä, automaattinen kustannuksen muutos ei toimi ja oston kustannusta ei siirretä eteenpäin myyntiin, ennen kuin suoritat **Muuta kustannuksia - Nimiketapahtumat** -eräajon.  

## <a name="see-also"></a>Katso myös
[Nimikekustannusten muuttaminen](inventory-how-adjust-item-costs.md)   
[Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)   
[Rakennetiedot: Täsmäytys pääkirjanpidon kanssa](design-details-reconciliation-with-the-general-ledger.md)   
[Rakennetiedot: varaston kirjaus](design-details-inventory-posting.md)   
[Rakennetiedot: varianssi](design-details-variance.md)   
[Rakennetiedot: kokoonpanotilauksen kirjaus](design-details-assembly-order-posting.md)   
[Rakennetiedot: tuotantotilauksen kirjaus](design-details-production-order-posting.md)  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
