---
title: Varastonarvostuksen ja kustannuslaskennan määrittäminen
description: 'Voit varmistaa, että varastokustannukset kirjataan oikein, määrittämällä tietyt kentät ja sivut ennen nimiketapahtumien tekemistä.'
author: SorenGP
ms.topic: conceptual
ms.search.keywords: null
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="setting-up-inventory-valuation-and-costing"></a><a name="setting-up-inventory-valuation-and-costing"></a><a name="setting-up-inventory-valuation-and-costing"></a>Varastonarvostuksen ja kustannuslaskennan määrittäminen

Voit varmistaa, että varastokustannukset kirjataan oikein, määrittämällä tietyt kentät ja sivut ennen nimiketapahtumien tekemistä. Yleensä yritykset valitsevat tietyn kustannuslaskentamenetelmän ja soveltavat niitä esimerkiksi varastonimikkeisiin voidakseen seurata varastossa olevien nimikkeiden arvoa.  

> [!TIP]
> Lisätietoja kustannuslaskennan käyttöönotosta [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa on kohdassa [Tietoja kustannuslaskennasta](finance-learn-about-costing.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.

|**Tehtävä**|**Katso**|  
|------------|-------------|
|Määritä yritykselle oletusarvoinen kustannuslaskentamenetelmä sen hallitsemiseksi, kuinka saapuvia kustannuksia käytetään varastojen arvon ja myytyjen tavaroiden kustannusten laskemiseen.|[Yleisten varastotietojen määrittäminen](inventory-how-setup-general.md)|  
|Määrittele yksittäisten nimikkeiden kustannuslaskentamenetelmä, jos ne edellyttävät eri kustannuslaskentamenetelmää.|[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)|  
|Varmistaminen, että kustannus kirjataan automaattisesti pääkirjanpitoon aina, kun varastotapahtuma kirjataan.|**Varastonhallinnan asetukset** -sivun **Automaattinen kustann. kirjaus** -kenttä|  
|Varmistaminen, että oletetut kustannukset kirjataan pääkirjanpitoon, jotta väliaikaisilla KP-tileillä näkyy arvio erääntyvistä summista ja kaupattujen nimikkeiden kustannuksista ennen nimikkeiden varsinaista laskuttamista.|**Varastonhallinnan asetukset** -sivun **Oletettu kust. kirjaus KP:toon** -kenttä|  
|Järjestelmän määrittäminen siten, että kustannusmuutokset päivittyvät automaattisesti aina varastotapahtumien kirjaamisen yhteydessä.|[Nimikekustannusten muuttaminen](inventory-how-adjust-item-costs.md)|  
|Määrittä, lasketaanko keskimääräinen hinta vain nimikettä kohden vai kutakin nimikettä kohden kussakin varastointiyksikössä ja kutakin nimikevarianttia kohden.|**Varastonhallinnan asetukset** -sivun **Keskim. kust. laskentatyyppi** -kenttä|  
|Keskimääräisen kustannuksen laskentamenetelmää käyttävien nimikkeiden painotetun keskimääräisen kustannuksen laskemiseen käytettävän ajanjakson valitseminen.|**Varastonhallinnan asetukset** -sivun **Keskimääräisen kustannuksen jakso** -kenttä|  
|Varastokausien määrittäminen varaston arvon pitkäaikaista hallintaa varten kieltämällä kirjaukset suljettuihin varastokausiin.|[Varastokausien käsitteleminen](finance-how-to-work-with-inventory-periods.md)|  
|Varmista, että myyntipalautukset kohdistetaan alkuperäiseen lähtevään tapahtumaan varaston arvon säilyttämiseksi.|**Myynnit ja myyntisaamiset** -sivun **Todellisen kust. peruutt. pakollinen** -kenttä|  
|Varmista, että ostopalautukset kohdistetaan alkuperäiseen saapuvaan tapahtumaan varaston arvon säilyttämiseksi.|**Ostot ja ostovelat** -sivun **Todellisen kust. peruutt. pakollinen** -kenttä|
|Nimikehintojen ja vakiokustannusten muuttamisessa tai ehdottamisessa käytettävien pyöristyssääntöjen määrittäminen.|**Pyöristystapa**-sivu|  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Yleisten varastotietojen määrittäminen](inventory-how-setup-general.md)  
[Varaston kustannusten täsmäyttäminen pääkirjanpitoon](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Parhaiden käytäntöjen määrittäminen: Arvostusmenetelmä](setup-best-practices-costing-method.md)  
[Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)  
[Rakennetiedot: nimikkeiden arvostusmenetelmän muuttaminen](design-details-changing-costing-methods.md)  
[Business Centralin käyttäminen](ui-work-product.md)  
[Rahoitus](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
