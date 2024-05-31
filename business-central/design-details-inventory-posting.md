---
title: Rakennetiedot – Varastokirjaus | Microsoft Docs
description: 'Jokainen varastotapahtuma, kuten tavaran vastaanotto tai myyntitoimitus, kirjaa kaksi erityyppistä tapahtumaa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Rakennetiedot: varaston kirjaus

Jokainen varastotapahtuma, kuten tavaran vastaanotto tai myyntitoimitus, kirjaa kaksi erityyppistä tapahtumaa.  

|Tapahtuman tyyppi|Description|  
|----------|-----------|  
|Määrä|Kuvaa varastomäärän muutosta. Nämä tiedot tallennetaan nimiketapahtumiin.<br /><br /> Nimikkeen kohdistustapahtumien mukana.|  
|Arvo|Kuvaa varaston arvon muutosta. Nämä tiedot tallennetaan arvotapahtumiin.<br /><br /> Jokaista nimiketapahtumaa tai kapasiteettitapahtumaa kohti voi olla yksi tai useampi arvotapahtuma.<br /><br /> Lisätietoja kapasiteetin arvotapahtumista, jotka liittyvät tuotanto- tai kokoonpanoresurssien käyttöön, on kohdassa [Rakennetiedot: tuotantotilauksen kirjaus](design-details-production-order-posting.md).|  

 Määrän kirjausten osalta nimikkeen kohdistustapahtumat ovat olemassa varaston arvon lisäyksen linkittämiseksi varaston arvon laskun kanssa. Tämän avulla kustannuslaskentaohjelma lähettää kustannukset arvon nousuista liittyviin arvon laskuihin ja päinvastoin. Katso lisätiedot kohdasta [Rakennetiedot: nimikkeen kohdistus](design-details-item-application.md).  

 Nimiketapahtumat, arvotapahtumat ja nimikkeen kohdistustapahtumat luodaan nimikepäiväkirjarivin kirjauksen seurauksena joko epäsuorasti tilausrivin kirjauksella tai epäsuorasti nimikkeen päiväkirjasivulla.  

 Varastokirjanpitoon luodut arvotapahtumat kirjataan säännöllisin väliajoin pääkirjanpitoon dynaamisesti kahden kirjanpidon täsmäyttämiseksi varainhoidon valvonnan vuoksi. Lisätietoja on kohdassa [Rakennetiedot: täsmäytys pääkirjanpidon kanssa](design-details-reconciliation-with-the-general-ledger.md).  

 ![Merkintätyönkulku varaston täsmäyttämisessä KP-kirjanpidon kanssa.](media/design_details_inventory_costing_1_entry_flow.png "Merkintätyönkulku varaston täsmäyttämisessä KP-kirjanpidon kanssa")  

## Esimerkki

Seuraavassa esimerkissä kuvataan, kuinka nimikkeen pääkirjan kirjaukset, arvokirjaukset ja nimikkeen sovelluskirjaukset vaikuttavat pääkirjan kirjauksiin.  

 Kirjaa ostotilaus vastaanotetuksi ja laskutetuksi 10 nimikkeelle, joiden välitön yksikkökustannus on 7 (PVA) ja yleiskustannuksen arvo 1 (PVA). Kirjauspäivämäärä on 1.1.2020. Seuraavat tapahtumat luodaan.  

### Nimiketapahtumat (1)

|Kirjauspäivämäärä|Tapahtuman tyyppi|Kustannussumma (Tod.)|määrä|Tapahtumanro|  
|------------|----------|--------------------|--------|---------|  
|01-01-20|Osto|80.00|10|1|  

### Arvotapahtumat (1)

|Kirjauspäivämäärä|Tapahtuman tyyppi|Kustannussumma (Tod.)|Nimiketapahtuman nro|Tapahtumanro|  
|------------|----------|--------------------|---------------------|---------|  
|01-01-20|Välitön kustannus|70,00|1|1|  
|01-01-20|Välillinen kustannus|10,00|1|2|  

### Nimikkeen kohdistustapahtumat (1)

|Tapahtumanro|Nimiketapahtuman nro|Saapuvan nimiketapahtuman nro|Lähtevän nimiketapahtuman nro|määrä.|  
|---------|---------------------|----------------------|-----------------------|--------|  
|1|1|1|0|10|  

 Seuraavaksi kirjaat 10 yksikön nimikkeen myynnin kirjauspäivämäärällä 15.1.2000.  

### Nimiketapahtumat (2)

|Kirjauspäivämäärä|Tapahtuman tyyppi|Kustannussumma (Tod.)|määrä|Tapahtumanro|  
|------------|----------|--------------------|--------|---------|  
|01-15-20|Myynti|-80.00|-10|2|  

### Arvotapahtumat (2)

|Kirjauspäivämäärä|Tapahtuman tyyppi|Kustannussumma (Tod.)|Nimiketapahtuman nro|Tapahtumanro|  
|------------|----------|--------------------|---------------------|---------|  
|01-15-20|Välitön kustannus|-80.00|2|3|  

### Nimikkeen kohdistustapahtumat (2)

|Tapahtumanro|Nimiketapahtuman nro|Saapuvan nimiketapahtuman nro|Lähtevän nimiketapahtuman nro|Määrä|  
|---------|---------------------|----------------------|-----------------------|--------|  
|2|2|1|2|-10|  

Kirjanpitojakson lopussa voit täsmäyttää nämä varastotapahtumat pääkirjanpidon kanssa suorittamalla **Kirjaa varaston kustannus KP:oon** -eräajon.  

 Lisätietoja on kohdassa [Rakennetiedot: Pääkirjanpidon tilit](design-details-accounts-in-the-general-ledger.md).  

 Seuraavissa taulukoissa esitetään varastosiirtojen täsmäytyksen tulokset tässä esimerkissä pääkirjan kanssa.  

### Arvotapahtumat (3)  

|Kirjauspäivämäärä|Tapahtuman tyyppi|Kustannussumma (Tod.)|KP:oon kirjattu kustannus|Nimiketapahtuman nro|Tapahtumanro|  
|------------|----------|--------------------|------------------|---------------------|---------|  
|01-01-20|Välitön kustannus|70,00|70,00|1|1|  
|01-01-20|Välillinen kustannus|10,00|10,00|1|2|  
|01-15-20|Välitön kustannus|-80.00|-80.00|2|3|  

### Pääkirjanpidon tapahtumat (3)

|Kirjauspäivämäärä|KP-tili|Tilinro (En-US-esittely)|Summa|Tapahtumanro|  
|------------|-----------|------------------------|------|---------|  
|01-01-20|[Varastotili]|2130|70,00|1|  
|01-01-20|[Välitön kust. kohdistettutili]|7291|-70.00|2|  
|01-01-20|[Varastotili]|2130|10,00|3|  
|1.1.2007|[Yleiskustannus kohdistettutili]|7292|-10.00|4|  
|01-15-20|[Varastotili]|2130|-80.00|5|  
|01-15-20|[COGS-tili]|7290|80.00|6|  

> [!NOTE]  
> Pääkirjan kirjausten tiliöintipäivä on sama kuin liittyvien arvokirjausten.  
> 
> **Arvotapahtuma**-taulukon **KP:oon kirjattu kustannus** -kenttä on täytetty.  

 Arvotapahtumien ja pääkirjapidon tapahtumien suhde tallennetaan **Kirjanpito - nimikekirjauksen suhde** -taulukkoon.  

### Liittyvät kirjaukset G/L – nimikkeen pääkirjan suhdetaulukko (3)

|KP-tapahtuman nro|Arvotapahtumanro|KP-rekisterin nro|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  
|5|3|1|  
|6|3|1|  

## Kokoonpanon ja tuotannon kirjaus

Kapasiteetti- ja resurssitapahtumat edustavat sitä hetkeä, joka kirjataan kulutetuksi tuotannossa tai kokoonpanossa. Prosessin kustannukset kirjataan arvotapahtumina pääkirjanpitoon mukana olevien materiaalikustannusten kanssa samanlaisena rakenteena kuin nimiketapahtumien kohdalla. Lisätietoja on tässä ohjeaiheessa.  

Katso lisätietoja kohdasta [Rakennetiedot: kokoonpanotilauksen kirjaus](design-details-assembly-order-posting.md).  

## Katso myös

 [Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)  
 [Rakennetiedot: pääkirjanpidon tilit](design-details-accounts-in-the-general-ledger.md)  
 [Rakennetiedot: Kustannuskomponentit](design-details-cost-components.md) [Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
 [Rahoitus](finance.md)  
 [Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]