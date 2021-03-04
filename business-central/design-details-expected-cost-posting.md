---
title: Rakenteen tiedot – Oletetun kustannuksen kirjaus | Microsoft Docs
description: Oletetut kustannukset kuvaavat esimerkiksi arviota ostetun nimikkeen kustannuksesta, jonka kirjaat ennen nimikkeen laskun vastaanottamista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 22e01f8b22c7f222674ff43090a27f5466dd8387
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751628"
---
# <a name="design-details-expected-cost-posting"></a>Rakennetiedot: oletetun kustannuksen kirjaus
Oletetut kustannukset kuvaavat esimerkiksi arviota ostetun nimikkeen kustannuksesta, jonka kirjaat ennen nimikkeen laskun vastaanottamista.  

 Voit kirjata oletetut kustannukset varastoon ja pääkirjanpitoon. Kun kirjaat määrän, joka on vastaanotettu tai toimitettu, mutta ei laskutettu, siitä luodaan arvotapahtuma ja oletetut kustannukset. Tämä oletettu kustannus vaikuttaa varaston arvoon, mutta se kirjataan pääkirjaan vain, jos järjestelmä määritetään tekemään niin.  

> [!NOTE]  
>  Oletettuja kustannuksia hallitaan vain nimiketapahtumille. Oletetut kustannukset eivät ole aineettomia tapahtumatyyppejä, kuten kapasiteetti ja nimikekulut.  

 Jos vain osa varaston arvon lisäyksestä on kirjattu, pääkirjanpidon varastoarvo ei muutu, ellet ole valinnut **Oletettu kust. kirjaus KP:toon** -valintaruutua **Varastonhallinnan asetukset** -sivulla. Tässä tapauksessa oletettu kustannus kirjataan väliaikaisille tileille vastaanottohetkellä. Kun vastaanotto on laskutettu kokonaan, väliaikaiset tilit täsmätään ja todellinen kustannus kirjataan varastotilille.  

 Laskutetussa arvotapahtumassa näkyy väliaikaisten tilien täsmäyttämiseksi kirjattu oletettu kustannussumma. Tämä tukee täsmäytystä ja jäljitystä.  

## <a name="example"></a>Esimerkki  
 Seuraavassa esimerkissä näytetään oletetut kustannukset, jos **Automaattinen kustann. kirjaus** -valintaruutu ja **Oletettu kust. kirjaus KP:toon** -valintaruutu on valittu **Varastonhallinnan asetukset** -sivulla.  

 Kirjaa ostotilaus vastaanotetuksi. Oletetut kustannukset ovat LCY 95.00.  

 **arvotapahtumat**  

|Kirjauspvm|Tapahtuman tyyppi|Kustannussumma (oletettu)|Olet. kust. kirjattu KP:oon|Oletettu kustannus|Nimiketapahtuman nro|Tapahtumanro|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|01-01-20|Välitön kustannus|95.00|95.00|Kyllä|1|1|  

 **Liittyvät kirjaukset G/L – nimikkeen pääkirjan suhdetaulukko**  

|KP-tapahtuman nro|Arvotapahtumanro|KP-rekisterin nro|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  

 **Pääkirjanpidon tapahtumat**  

|Kirjauspvm|KP-tili|Tilinro (En-US-esittely)|Summa|Tapahtumanro|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|Varastokertymätili (väliaik)|5530|-95.00|2|  
|01-01-20|Varastotili (väliaik)|2131|95.00|1|  

 Myöhemmin kirjaat ostotilauksen laskutettuna. Laskutetut kustannukset ovat LCY 100.00.  

 **arvotapahtumat**  

|Kirjauspvm|Kustannussumma (Tod.)|Kustannussumma (oletettu)|KP:oon kirjattu kustannus|Oletettu kustannus|Nimiketapahtuman nro|Tapahtumanro|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|01-15-20|100,00|-95.00|100,00|Ei|1|2|  

 **Liittyvät kirjaukset G/L – nimikkeen pääkirjan suhdetaulukko**  

|KP-tapahtuman nro|Arvotapahtumanro|KP-rekisterin nro|  
|--------------------|---------------------|-----------------------|  
|3|2|2|  
|4|2|2|  
|5|2|2|  
|6|2|2|  

 **Pääkirjanpidon tapahtumat**  

|Kirjauspvm|KP-tili|Tilinro (En-US-esittely)|Summa|Tapahtumanro|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-15-20|Varastokertymätili (väliaik)|5530|95.00|4|  
|01-15-20|Varastotili (väliaik)|2131|-95.00|3|  
|01-15-20|Välitön kust. kohdistettutili|7291|-100|6|  
|01-15-20|Varastotili|2130|100|5|  

## <a name="see-also"></a>Katso myös
 [Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)   
 [Rakennetiedot: kustannuksen muutos](design-details-cost-adjustment.md)   
 [Rakennetiedot: täsmäytys pääkirjanpidon kanssa](design-details-reconciliation-with-the-general-ledger.md)   
 [Rakennetiedot: Varastokirjaus](design-details-inventory-posting.md)   
 [Rakennetiedot: varianssi](design-details-variance.md)  
 [Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
 [Rahoitus](finance.md)  
 [[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]