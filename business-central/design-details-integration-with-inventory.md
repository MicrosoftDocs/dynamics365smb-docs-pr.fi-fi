---
title: Rakennetiedot – integrointi varaston kanssa
description: Varastonhallinta- ja Varasto-sovellusalue ovat yhteydessä toistensa kanssa inventoinnissa ja inventoinnin tai fyysisen varaston muutoksessa.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-integration-with-inventory"></a>Rakennetiedot: integrointi varaston kanssa

Varastonhallinta- ja varasto-ominaisuudet ovat yhteydessä toistensa kanssa inventoinnissa ja inventoinnin tai fyysisen varaston muutoksessa.  

## <a name="physical-inventory"></a>Fyysinen varasto

**F. var. inventointipvk** -sivu käytetään **Inventointipäiväkirja**-sivulla kaikkien fyysisen varaston lisäsijaintien osalta. Varaston tai bin-tiedoston taso lasketaan ja tulostettu luettelo annetaan varastotyöntekijälle. Luettelossa näytetään, mitkä nimikkeet missä bineissä täytyy laskea.  
  
Varastotyöntekijä antaa inventoidun määrän **F. var. inventointipvk** -sivulla ja kirjaa päiväkirjan.  
  
Jos laskettu määrä on suurempi kuin päiväkirjarivillä oleva määrä, siirto kirjataan tälle erolle oletusarvoisesta muutosvarastopaikasta laskettuun varastopaikkaan. Tämä nostaa määrää inventoidussa varastopaikassa ja laskee määrää muutoksen oletusvarastopaikassa.  
  
Jos laskettu määrä on pienempi kuin päiväkirjarivillä oleva määrä, siirto kirjataan tälle erolle lasketusta varastopaikasta oletusarvoiseen muutosvarastopaikkaan. Tämä laskee määrää inventoidussa varastopaikassa ja nostaa määrää muutoksen oletusvarastopaikassa.  
  
Laajennetuissa varastomäärityksissä **Määrä (laskettu)**-kentän arvo noudetaan nimiketapahtumista ja **Määrä (inventointi)**-kentän arvo noudetaan fyysisen varaston tapahtumista, varastopaikan sisällön muutosta lukuun ottamatta. **Määrä**-kenttä määrittää eron ensimmäisten kahden kentän välillä, jonka tulisi olla yhtä suuri kuin mukautetun binin sisältö.  
  
Kun kirjaat inventointipäiväkirjan, varaston ja oletusmuutoksen varastopaikka päivitetään.  

[!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]
  
## <a name="warehouse-adjustments-to-the-item-ledger"></a>Nimikekirjausten fyysisen varastoinnin muutokset

**Nimikepäiväkirja**-sivun ja **Laske f.var. muutos** -toiminnon avulla voit muuttaa nimiketapahtuman varaston sen mukaan, miten fyysisen varastoinnin varastopaikan nimikemäärää on muutettu. Kun haluat luoda linkin varaston ja fyysisen varaston välille, määritä oletusmuutosvarastopaikka sijaintia kohti.  
  
Oletusarvoinen mukautettava bin rekisteröi varastonimikkeet, kun tiliöit varaston kasvun. Jos kuitenkin kirjaat vähennystä, myös oletusvarastopaikan määrä vähenee. Molemmissa tapauksissa luodaan nimiketapahtumat ja fyysisen varastoinnin tapahtumat.  
  
> [!NOTE]  
> Varastolaskentaan ei sisälly muutoksen varastopaikkaa.  
  
Voidaksesi muuttaa varastopaikan sisältöä, käytä fyysisen varastoinnin nimikepäiväkirjaa, johon voit kirjoittaa muutettavan nimikenumeron, vyöhykekoodin, varastopaikkakoodin ja määrän.  
  
Jos kirjoitat positiivisen määrän ja kirjaat rivin, varastopaikkaan tallennettu varaston määrä lisääntyy ja oletusarvoisen muutosvarastopaikan määrä pienenee vastaavasti.  
  
## <a name="see-also"></a>Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)  
[Rakennetiedot: saatavuus varastossa](design-details-availability-in-the-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
