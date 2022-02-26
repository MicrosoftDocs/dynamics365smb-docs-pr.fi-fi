---
title: Rakennetiedot - oletetun kustannuksen kirjaus
description: Oletetut kustannukset kuvaavat esimerkiksi arviota ostetun nimikkeen kustannuksesta, jonka kirjaat ennen nimikkeen laskun vastaanottamista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/20/2021
ms.author: edupont
ms.openlocfilehash: 1327eaf9a26ff2bbf8aa3dab8f2e7f64b8f00ab4
ms.sourcegitcommit: ecbabd2d0fdf2566cea4a05a25b09ff6ca6256c6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/22/2021
ms.locfileid: "6649835"
---
# <a name="design-details-expected-cost-posting"></a>Rakennetiedot: oletetun kustannuksen kirjaus
Oletetut kustannukset kuvaavat esimerkiksi arviota ostetun nimikkeen kustannuksesta, jonka kirjaat ennen nimikkeen laskun vastaanottamista.  

 Voit kirjata oletetut kustannukset varastoon ja pääkirjanpitoon. Kun kirjaat määrän, joka on vastaanotettu tai toimitettu, mutta ei laskutettu, siitä luodaan arvotapahtuma ja oletetut kustannukset. Tämä oletettu kustannus vaikuttaa varaston arvoon, mutta se kirjataan pääkirjaan vain, jos järjestelmä määritetään tekemään niin.  

> [!NOTE]  
>  Oletettuja kustannuksia hallitaan vain nimiketapahtumille. Oletetut kustannukset eivät ole aineettomia tapahtumatyyppejä, kuten kapasiteetti ja nimikekulut.  

 Jos vain osa varaston arvon lisäyksestä on kirjattu, pääkirjanpidon varastoarvo ei muutu, ellet ole valinnut **Oletettu kust. kirjaus KP:toon** -valintaruutua **Varastonhallinnan asetukset** -sivulla. Tässä tapauksessa oletettu kustannus kirjataan väliaikaisille tileille vastaanottohetkellä. Kun vastaanotto on laskutettu kokonaan, väliaikaiset tilit täsmätään ja todellinen kustannus kirjataan varastotilille.  

 Laskutetussa arvotapahtumassa näkyy väliaikaisten tilien täsmäyttämiseksi kirjattu oletettu kustannussumma. Tämä tukee täsmäytystä ja jäljitystä.  

## <a name="prerequisites-for-posting-expected-costs"></a>Oletetun kustannuksen kirjaamisen edellytykset

Jotta odotetut kustannukset voidaan kirjata, sinun on tehtävä seuraavat toimet:
1. **Varastonhallinnan asetukset** -sivulla valitse **Automaattinen kustann. kirjaus** -valintaruutu ja **Oletettu kust. kirjaus KP:oon** -valintaruutu.
2. Määritä, mitä väliaikaisia tilejä käytetään oletetun kustannuksen kirjausprosessin aikana.  

  Tarkista **Varaston kirjausasetukset** -sivulla **Varastotili**- ja **Varastotili (väliaikainen)** -kentät ostettavan nimikkeen kentälle **Sijaintikoodi ja Varaston kirj.ryhmän koodi**. Lisätietoja näistä tileistä on kohdassa [Rakennetiedot - Tilit pääkirjanpidossa](design-details-accounts-in-the-general-ledger.md).
3. Tarkista **Yleiset kirjausasetukset** -sivulla **Varaston kertymätili (väliaik)** -kenttä käyttämillesi **Yleinen liiketoim. kirjausryhmä**- ja **Yleinen tuotteen kirjausryhmä** -ryhmille.
4. Kun luot ostotilauksen, oletusarvona on, että **Toimittajan laskun nro** -kenttä on pakollinen. Sinun on poistettava se käytöstä **Ostojen ja ostovelkojen asetukset** -sivulla poistamalla **Ulkois. asiakirjan nro pakoll.** -kentän valinta.

## <a name="example"></a>Esimerkki  

> [!NOTE]  
> Tässä esimerkissä käytetyt tilinumerot ovat vain viitteenä, ja ne ovat erilaisia järjestelmässäsi. Määritä ne yllä olevissa edellytyksissä olevien ohjeiden mukaan.

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

|Kirjauspäivämäärä|KP-tili|Tilinro (Vain esimerkit!)|Summa|Tapahtumanro|  
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
