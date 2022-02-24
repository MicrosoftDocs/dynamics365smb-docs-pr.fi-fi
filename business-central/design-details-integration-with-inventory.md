---
title: Rakennetiedot – Integrointi varaston kanssa | Microsoft Docs
description: Varastoinninhallinta- ja Varasto-sovellusalue ovat yhteydessä toistensa kanssa inventoinnissa ja inventoinnin tai fyysisen varaston muutoksessa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: bbc9c0e55041f4584ae7609f727179737adaa041
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185346"
---
# <a name="design-details-integration-with-inventory"></a>Rakennetiedot: integrointi varaston kanssa
Varastoinninhallinta- ja Varasto-sovellusalue ovat yhteydessä toistensa kanssa inventoinnissa ja inventoinnin tai fyysisen varaston muutoksessa.  
  
## <a name="physical-inventory"></a>Fyysinen varasto  
 **F. var. inventointipvk** -sivu käytetään **Inventointipäiväkirja**-sivulla kaikkien fyysisen varaston lisäsijaintien osalta. Varaston tai bin-tiedoston taso lasketaan ja tulostettu luettelo annetaan varastotyöntekijälle. Luettelossa näytetään, mitkä nimikkeet missä bineissä täytyy laskea.  
  
 Varastotyöntekijä antaa inventoidun määrän **F. var. inventointipvk** -sivulla ja kirjaa päiväkirjan.  
  
 Jos laskettu määrä on suurempi kuin päiväkirjarivillä oleva määrä, siirto kirjataan tälle erolle oletusarvoisesta muutosvarastopaikasta laskettuun varastopaikkaan. Tämä nostaa määrää inventoidussa varastopaikassa ja laskee määrää muutoksen oletusvarastopaikassa.  
  
 Jos laskettu määrä on pienempi kuin päiväkirjarivillä oleva määrä, siirto kirjataan tälle erolle lasketusta varastopaikasta oletusarvoiseen muutosvarastopaikkaan. Tämä laskee määrää inventoidussa varastopaikassa ja nostaa määrää muutoksen oletusvarastopaikassa.  
  
 Laajennetuissa varastomäärityksissä **Määrä (laskettu)**-kentän arvo noudetaan nimiketapahtumista ja **Määrä (inventointi)**-kentän arvo noudetaan fyysisen varaston tapahtumista, varastopaikan sisällön muutosta lukuun ottamatta. **Määrä**-kenttä määrittää eron ensimmäisten kahden kentän välillä, jonka tulisi olla yhtä suuri kuin mukautetun binin sisältö.  
  
 Kun kirjaat inventointipäiväkirjan, varaston ja oletusmuutoksen varastopaikka päivitetään.  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a>Nimikekirjausten fyysisen varastoinnin muutokset  
 **Nimikepäiväkirja**-sivun ja **Laske f.var. muutos** -toiminnon avulla voit muuttaa nimiketapahtuman varaston sen mukaan, miten fyysisen varastoinnin varastopaikan nimikemäärää on muutettu. Kun haluat luoda linkin varaston ja fyysisen varaston välille, määritä oletusmuutosvarastopaikka sijaintia kohti.  
  
 Oletusarvoinen mukautettava bin rekisteröi varastonimikkeet, kun tiliöit varaston kasvun. Jos kuitenkin kirjaat vähennystä, myös oletusvarastopaikan määrä vähenee. Molemmissa tapauksissa luodaan nimiketapahtumat ja fyysisen varastoinnin tapahtumat.  
  
> [!NOTE]  
>  Mukautettua biniä ei ole sisällytetty saatavuuslaskelmaan.  
  
 Jos haluat muuttaa varastopaikan sisältöä, voit käyttää fyysisen varastoinnin nimikepäiväkirjaa, josta voit kirjoittaa muutettavan nimikenumeron, vyöhykekoodin, varastopaikkakoodin ja määrän.  
  
 Jos kirjoitat positiivisen määrän ja kirjaat rivin, varastopaikkaan tallennettu varaston määrä lisääntyy ja oletusarvoisen muutosvarastopaikan määrä pienenee vastaavasti.  
  
## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: f. varaston hallinta](design-details-warehouse-management.md)   
 [Rakennetiedot: saatavuus varastossa](design-details-availability-in-the-warehouse.md)