---
title: "Varastonarvostuksen ja kustannuslaskennan määrittäminen | Microsoft Docs"
description: "Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: aa5ee6d9942390a2b4ad0aa8787172b0f7b141d0
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-inventory-valuation-and-costing"></a>Varastonarvostuksen ja kustannuslaskennan määrittäminen
Voit varmistaa, että varastokustannukset kirjataan oikein, määrittämällä tietyt kentät ja ikkunat ennen nimiketapahtumien tekemistä.

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Kustannuslaskentamenetelmän määrittäminen kullekin nimikkeelle. Valitun menetelmän mukaan määräytyy, miten nimikkeen saapuvia kustannuksia käytetään varaston arvon ja myytyjen tuotteiden kustannusten laskemiseen.|[Toimintaohje: Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)|  
|Varmistaminen, että kustannus kirjataan automaattisesti pääkirjanpitoon aina, kun varastotapahtuma kirjataan.|**Varastonhallinnan asetukset** -ikkunan **Automaattinen kustann. kirjaus** -kenttä|  
|Varmistaminen, että oletetut kustannukset kirjataan pääkirjanpitoon, jotta väliaikaisilla KP-tileillä näkyy arvio erääntyvistä summista ja kaupattujen nimikkeiden kustannuksista ennen nimikkeiden varsinaista laskuttamista.|**Varastonhallinnan asetukset** -ikkunan **Oletettu kust. kirjaus KP:toon** -kenttä|  
|Järjestelmän määrittäminen siten, että kustannusmuutokset päivittyvät automaattisesti aina varastotapahtumien kirjaamisen yhteydessä.|[Toimintaohje: Nimikekustannusten muokkaaminen](inventory-how-adjust-item-costs.md)|  
|Määrittä, lasketaanko keskimääräinen hinta vain nimikettä kohden vai kutakin nimikettä kohden kussakin varastointiyksikössä ja kutakin nimikevarianttia kohden.|**Varastonhallinnan asetukset** -sivun **Keskim. kust. laskentatyyppi** -kenttä|  
|Keskimääräisen kustannuksen laskentamenetelmää käyttävien nimikkeiden painotetun keskimääräisen kustannuksen laskemiseen käytettävän ajanjakson valitseminen.|**Varastonhallinnan asetukset** -sivun **Keskimääräisen kustannuksen jakso** -kenttä|  
|Varastokausien määrittäminen varaston arvon pitkäaikaista hallintaa varten kieltämällä kirjaukset suljettuihin varastokausiin.|[Toimintaohje: Varastokausien käsitteleminen](finance-how-to-work-with-inventory-periods.md)|  
|Varmista, että myyntipalautukset kohdistetaan alkuperäiseen lähtevään tapahtumaan varaston arvon säilyttämiseksi.|**Myynnit ja myyntisaamiset** -ikkunan **Todellisen kust. peruutt. pakollinen** -kenttä|  
|Varmista, että ostopalautukset kohdistetaan alkuperäiseen saapuvaan tapahtumaan varaston arvon säilyttämiseksi.|**Ostot ja ostovelat** -ikkunan **Todellisen kust. peruutt. pakollinen** -kenttä|
|Nimikehintojen ja vakiokustannusten muuttamisessa tai ehdottamisessa käytettävien pyöristyssääntöjen määrittäminen.|**Pyöristystapa**-sivu|  

## <a name="see-also"></a>Katso myös  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Financialsin käyttäminen](ui-work-product.md)  
[Rahoitus](finance.md)  

