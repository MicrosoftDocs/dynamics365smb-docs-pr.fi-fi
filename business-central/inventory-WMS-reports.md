---
title: Varasto, varastoraportit ja analytiikka
description: Katso, mitkä varastoraportit ja mikä analytiikka on saatavilla Business Centralin vakioversiossa, jotta voit seurata liiketoimintaasi.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 8a4418699f28acd3ede80616ba69c56f50781e43
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216348"
---
# <a name="inventory-and-warehouse-reports-and-analytics-in-business-central"></a>Varasto, varastoraportit ja analytiikka Business Centralissa

[!INCLUDE [prod_short](includes/prod_short.md)] -varastoraporttien avulla varaston ja liiketoiminnan ammattilaiset voivat saada merkityksellistä tietoa ja analytiikkaa nykyisistä ja aiemmista varastotoiminnoista.  

## <a name="reports"></a>Raportit

Seuraavassa taulukossa kuvataan joitakin varastoraportoinnin keskeisiä raportteja.

|Raportti |Objektin tunnus|Kuvaus  |
|---------|---------|---------|
|**Varasto – Saatavuussuunnitelma**|707|Jos haluat yleiskatsauksen tietyistä nimikkeistä tai varastointiyksiköistä ja niiden saatavuudesta. Tässä raportissa näkyvät kumulatiiviset arvot, esimerkiksi bruttotarpeet, aikataulutetut ja suunnitellut vastaanotot ja varasto. |
|**Varaston arvostus**|1001|Tässä raportissa näkyy varaston arvostus valittujen varastossa olevien nimikkeiden osalta. Raportissa näkyy tietoja myös varaston arvon laskuista ja nousuista valitulta ajanjaksolta.|
|**Nimikkeen vanhentuminen – Määrä**|5809|Näyttää yleiskuvauksen varaston valituista nimikkeistä, joiden vanhentumispäivämäärät ovat tietyn määräajan kuluessa. Luettelossa on määritetyllä aikavälillä vanhentuvien valittujen nimikkeiden yksikkömäärät. Tulostetussa asiakirjassa näkyy kunkin raporttia määrittäessäsi määrittämäsi nimikkeen yksikkömäärä, joka vanhentuu kunkin kolmen yhtä pitkän aikavälin aikana, sekä valitun nimikkeen kokonaisvarastomäärä.<br>Asettamalla suodattimia voit määrittää, mitä raporttiin sisällytetään. Jos suodattimia ei aseteta, raporttiin sisällytetään kaikki tietueet. Raportin ilmoittamat määrät vastaavat määriä vain nimikkeessä, jonka vanhentumispäivämäärät on määritetty.|
|**Nimikeiän koostumus – Määrä** tai **Nimikeiän koostumus – Arvo**|5807 tai 5808|Raportin avulla saat yleiskuvauksen valittujen, varastossa olevien nimikkeiden tämänhetkisestä iän koostumuksesta. Luettelossa on valitun nimikkeen yksiköiden lukumäärä tai arvo, joka lisättiin varastoon tai poistettiin sieltä sekä aika, jolloin yksiköt lisättiin tai poistettiin. Nimikkeitä voidaan lisätä varastoon tai poistaa sieltä ostojen, myyntien ja positiivisten ja negatiivisten muutosten seurauksena.|
|**Varaston kust.- ja &hintaluett.**|716|Tässä raportissa on luettelo hintatiedoista valittujen nimikkeiden tai varastointiyksiköiden osalta: välitön yksikkökustannus, viimeinen välitön kustannus, yksikköhinta, tuottoprosentti ja tuotto. |
|**F. var. var.paikkaluettelo**|7319|Näyttää varastopaikkojen yleiskuvauksen, niiden asetukset ja varastopaikkojen nimikkeiden määrän. Tätä raporttia voidaan käyttää kaikissa sijainneissa, joissa on "varastopaikka" pakollisena kenttänä. |
|**Fyysisen varaston toimituksen tila**|7313|Näyttää avoimien lähdeasiakirjojen ja toimitettujen tai toimitettavien nimikkeiden sijaintikohtaisen yhteenvedon. Tätä raporttia voidaan käyttää kaikissa sijainneissa, joissa **Pakolliset toimitukset** on otettu käyttöön. **Fyysisen varaston toimituksen tila** näyttää sijainnit, varastopaikkakoodit, asiakirjan tilan ja määrät.|
|**Varaston poimintaluettelo**|813|Raportissa näkyy luettelo myyntitilauksista, joihin nimike sisältyy. Jokaisesta nimikkeestä näkyvät seuraavat tiedot: myyntitilausrivi sekä sen asiakasnumero, varianttikoodi, sijantikoodi, var.paikkakoodi, toimituspäivämäärä, toimitettava määrä ja mittayksikkö. Toimitettava määrä lasketaan yhteen jokaisen nimikkeen osalta. Raporttia voidaan käyttää silloin, kun nimikkeet poimitaan varastosta.<br>Huomautus: Tämä toiminto ei ole käytettävissä varaston lisätoiminnoissa.|
|**F. var. muutosvar.paikka**|7320|Tämä erityisraportti on tarkoitettu vain edistyneelle fyysiselle varastoinnille, ja siinä näkyvät jäljellä olevat määrät, jotka ovat edelleen varastoituina muutosvarastopaikassa. Tavallisesti tämän tietyn varastopaikan pitäisi olla tyhjä. Ainoa syy tämän varastopaikan täyttämiselle on fyysinen inventaario tai se, että nimikkeiden määriä on lisätty fyysiseen varastoon tai poistettu fyysisestä varastosta.|


## <a name="tasks"></a>Tehtävät

Seuraavissa artikkeleissa kuvataan joitakin yrityksen tilan analysointiin liittyviä keskeisiä tehtäviä:

* [Analyysiraporttien luominen](bi-how-create-analysis-views-reports.md)  
* [Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)


## <a name="see-also"></a>Katso myös

[Varaston määrittäminen](inventory-setup-inventory.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
