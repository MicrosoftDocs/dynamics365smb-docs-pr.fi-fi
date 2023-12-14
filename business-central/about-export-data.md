---
title: Business Central -tietojen vieminen Exceliin
description: Voit viedä tilinpäätökset ja liiketoimintatiedot Business Central -sovelluksesta Exceliin tai avata tiedot Excelissä.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'analysis, reporting, financial report, business intelligence, BI, Excel'
ms.search.form: 9901
ms.date: 04/01/2021
ms.author: bholtorf
---
# Liiketoimintatietojen vieminen Exceliin

Excel on tehokas työkalu tietojen käsittelyyn. [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman sisältä voit avata minkä tahansa luettelon Excelissä. Voit myös muokata tietoja Excelissä ja lähettää tiedot takaisin [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan. Saman ominaisuuden ansiosta sinun on helppo ottaa tiedot mukaan, jos päätät peruuttaa tilauksesi.

## Luetteloiden avaaminen Excelissä

Voit avata minkä tahansa päiväkirjan, luettelon tai työkirjan tiedot Excelissä. Avaa haluamasi sivu ja valitse sitten **Avaa Excelissä**. Voit esimerkiksi avata asiakasluettelon (hae **Asiakkaat**) ja valitse sitten **Avaa Excelissä**. Selain pyytää sinua avaamaan tai tallentamaan luodun Excel-työkirjan.  

> [!NOTE]
> Käytä tätä vaihtoehtoa, jos et halua tehdä muutoksia ja julkaista niitä takaisin [!INCLUDE[prod_short](includes/prod_short.md)]iin.  

Jokaisessa luettelossa on joitakin sarakkeita. Exceliin vieminen sisältää kaikki avoinna olevan näkymän sarakkeet. Muuta sarakkeita avaamalla minkä tahansa sarakkeen pikavalikko ja määrittämällä näytettävät sarakkeet. Sarakeluettelo on erilainen useimmissa luetteloissa. Sarakkeet vastaavat tietokannan rakennetta, johon tiedot tallennetaan. Jos et ole varma, minkä tyyppistä tietoa tietty sarake sisältää, lisää se näkymään. Voit poistaa sen aina uudelleen.  

### Muokkaa tietoja Excelissä

Oma [!INCLUDE[prod_short](includes/prod_short.md)] sisältää laajennuksen Exceliin niin, että Excel-tietoja voidaan muokata. Lisätietoja on kohdassa [Rahoituslaskelmien analysointi Microsoft Excelissä](finance-analyze-excel.md).  

## Tietojen vienti muihin rahoitusjärjestelmiin

Jos päätät peruuttaa [!INCLUDE[prod_short](includes/prod_short.md)]in tilauksen, voit viedä tiedot Exceliin ja viedä ne sitten seuraavaa rahoitusjärjestelmään.  

Voit viedä kaikki sivut, mutta et kuitenkaan välttämättä tarvitse niitä kaikkia. Kannattaakin harkita vain seuraavien keskeisten sivujen vientiä. Muista myös lisätä kaikki sarakkeet edellä kuvatulla tavalla.  

* Tilikartta  
* Asiakkaat  
* Toimittajat  
* Pankit  
* Nimikkeet  

Jos haluat myös kaikki rahoitustapahtumat, kyse on suuresta tietomäärästä, joten vienti ei useinkaan tapahdu muutamassa minuutissa. Rahoitustapahtumat näkyvät **Pääkirjanpidon tapahtumat** -sivulla.  

Myös seuraavien sivujen tietojen vienti on suositeltavaa:  

* Asiakastapahtumat  
* Toimittajatapahtumat  
* Pankkitilitapahtumat  
* Nimiketapahtumat  
* Yleiset kirjausasetukset  
* Asiakkaan kirjausryhmät  
* Toimittajan kirjausryhmät  
* Nimikkeen kirjausryhmät  
* Pankkitilin kirjausryhmä  
* KP-budjetit  
* KP-budjetin tapahtumat  
* Myyntitarjoukset  
* Myyntilaskut  
* Ostolaskut  
* Kontaktit  
* Myyjät  

> [!NOTE]  
> Jos olet määrittänyt [!INCLUDE[prod_short](includes/prod_short.md)]iin useita yrityksiä, kunkin yrityksen kyseiset tiedot on vietävä.

> [!NOTE]
> Tietojen avaaminen tai muokkaaminen Excelissä edellyttää vähintään yhtä seuraavista käyttöoikeuksista:
>
> * käyttöoikeuksien joukko *D365 Excelin vientitoiminto*  
> * Järjestelmän käyttöoikeus 6110 *Salli toiminnon vieminen Exceliin*.  

Lisätietoja on kohdassa [Käyttäjän käyttöoikeuksien yleiskatsauksen hankkiminen](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).

## Katso myös
[[!INCLUDE[prod_short](includes/prod_short.md)]-tilauksen peruuttaminen](admin-cancel.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Rahoituslaskelmien analysointi Microsoft Excelissä](finance-analyze-excel.md)  
[Rahoitus](finance.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
