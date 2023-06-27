---
title: Tuotannon suorittaminen
description: 'Kun kysyntä on suunniteltu ja materiaalit on otettu tuotannon tuoterakenteen mukaisesti, tuotantotoiminnot voivat alkaa, ja ne suoritetaan tuotantotilauksen reitityksen määrittämässä järjestyksessä.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5406, 5407, 5728, 8903, 9011, 9012, 9013, 9041, 9044, 9047, 9323, 9324, 9325, 9326, 9327, 99000784, 99000785'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="manufacturing" />Tuotanto

> [!NOTE]
> Tässä ohjeaiheessa ja aliohjeaiheissa esitellyt toiminnot näkyvät käyttöliittymässä vain, jos käytössä on **Premium**-käyttökokemus. Lisätietoja on kohdassa [Näytettävien ominaisuuksien muuttaminen](ui-experiences.md).

Kun kysyntä on suunniteltu ja materiaalit on otettu tuotannon tuoterakenteen mukaisesti, tuotantotoiminnot voivat alkaa, ja ne suoritetaan tuotantotilauksen reitityksen määrittämässä järjestyksessä.  

Järjestelmän näkökulmasta tärkeä tuotannon toteutuksen osa on kirjata tuotantomäärä tietokantaan edistymisen raportoimiseksi ja varastomäärän päivittämiseksi valmiilla tuotteilla. Tuotoskirjaus voidaan tehdä manuaalisesti täyttämällä päiväkirjarivit ja kirjaamalla ne tuotantotoimintojen jälkeen. Se voidaan tehdä myös automaattisesti taaksepäinsiirron avulla. Tällöin materiaalin kulutus kirjataan automaattisesti tuotoksen kanssa, kun tuotantotilauksen tilaksi tulee Valmis.  

Vaihtoehto useiden tuotantotilausten tuotoksen kirjaamiselle eräpäiväkirjaan on yhden tuotantotilausrivin kulutuksen ja/tai tuotoksen kirjaaminen **Tuotantopäiväkirja**-sivulla.

Ennen nimikkeiden tuotannon aloittamista on tehtävä useita asetuksia, esimerkiksi tuotantosoluissa, reitityksissä ja tuotannon tuoterakenteissa. Lisätietoja on kohdassa [Tuotannon määrittäminen](production-configure-production-processes.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Tietoja tuotantotilausten käytöstä.|[Tietoja tuotantotilauksista](production-about-production-orders.md)|
|Luo tuotantotilaukset manuaalisesti.|[Tuotantotilausten luominen](production-how-to-create-production-orders.md)|
|Ulkoista tuotantotilauksen kaikki toiminnot tai valitut toiminnot alihankkijalle.|[Tuotanto alihankintana](production-how-to-subcontract-manufacturing.md)|
|Tallenna ja kirjaa yksittäisen vapautetun tuotantotilausrivin tuotos sekä materiaalien ja ajan kulutus.|[Yhden vapautetun tuotantotilausrivin kulutuksen ja tuotoksen kirjaaminen.](production-how-to-register-consumption-and-output.md)|  
|Tee eräkirjauksena toiminnon käyttämien komponenttien määrä päiväkirjaan, joka voi käsitellä useita suunniteltuja tuotantotilauksia.|[Kulutuksen eräkirjaus](production-how-to-post-consumption.md)|
|Kirjaa toimintakohtainen valmistuneiden nimikkeiden määrä ja käytetty aika päiväkirjaan, joka voi käsitellä useita vapautettuja tuotantotilauksia.|[Tuotos- ja suoritusaikojen eräkirjaus](production-how-to-post-output-quantity.md)|
|Kumoa tuotos esimerkiksi tapahtuneen tietojen syöttövirheen tai virheellisen summan vuoksi.  |[Tuotoksen kirjaamisen peruuttaminen](production-how-to-reverse-output-posting.md)|  
|Kirjaa valmiiksi saatujen toimintojen osalta sellaisten tuotettujen nimikkeiden määrä, joita ei ole luokiteltu valmiiksi tuotokseksi vaan hukkatavaraksi.|[Hukkatavaran kirjaaminen](production-how-to-post-scrap.md)|
|Tarkastele tuotannon kuormitusta suunniteltujen ja vapautettujen tuotantotilausten tuloksena.|[Tuotantosolujen ja kuormitusryhmien kuormituksen tarkasteleminen](production-how-to-view-the-load-on-work-centers.md)|  
|Käytä **Kapasiteettipäiväkirja**-sivua, jonka avulla voit kirjata sellaisia kulutettuja kapasiteetteja, joita ei ole kohdistettu tuotantotilaukseen (esimerkiksi kunnossapitotyö).|[Kapasiteettien kirjaaminen](production-how-to-post-capacities.md)|  
|Laske ja muuta valmiiden tuotantonimikkeiden kustannuksia ja kulutettuja komponentteja kirjanpidon täsmäytystä varten.|[Tietoja valmiin tuotantotilauksen kustannuksista](finance-about-finished-production-order-costs.md)|  

## <a name="see-also" />Katso myös

[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
