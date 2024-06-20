---
author: brentholtorf
ms.topic: include
ms.date: 09/21/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

Varaston työntekijät voivat toimittaa ja vastaanottaa muita kuin varastonimikkeitä sekä fyysisiä tavaroita myynti- ja ostotilauksissa. Muut kuin varaston nimikkeet ovat aineettomia hyödykkeitä, kuten vakuutus tai lisäkustannukset.

Myynti- ja ostotilauksilla on riveillään usein monenlaisia asioita. Tilauksiin voi sisältyä esimerkiksi pääkirjanpidon nimikkeitä, tilejä ja käyttöomaisuutta. Jos käytät fyysisen varastoinnin asiakirjoja fyysisten nimikkeiden käsittelyyn, voit myös kirjata joitain tyyppejä, jotka eivät ole varastonimikkeitä. Esimerkkejä fyysisen varaston asiakirjoista:

* Varaston hyllytykset
* F.var. vast.otot
* Varaston poiminnat
* Fyysisen varaston toimitukset

Jos haluat, että varastotyöntekijät voivat toimittaa ja vastaanottaa muita kuin varastonimikkeitä, täytä **Kirjaa autom. ei-var. f. var. kautta** -kenttä **Myyntien ja myyntisaamisten asetukset**- ja **Ostojen ja ostovelkojen asetukset** -sivuilla. Kentässä ovat seuraavat vaihtoehdot:

|Asetus  |Kuvaus  |
|---------|---------|
|Ei mitään     |Älä toimita tai vastaanota muita kuin varastonimikkeitä.         |
|Liitetty/määritetty     | Kirjaa nimikekulut ja muut kuin varaston nimikerivit, jotka on määritelty tai liitetty fyysisiin nimikkeisiin. Voit liittää muut kuin varastorivit fyysisiin nimikkeisiin käyttämällä **Liitä varastoriviin** -toimintoa.        |
|Kaikki     | Kirjaa kaikki lähdeasiakirjan ei-varastorivit heti, kun fyysisen varastoinnin asiakirja kirjaa vähintään yhden nimikkeen.        |

> [!NOTE]
> Myyntitilauksen **Toimitusohje**-kentän **Valmis**-vaihtoehto on etusijalla fyysisen varaston automaattisen kirjaamisen **Kirjaa autom. ei-var. f. var. kautta** -kentässä **Myyntien ja myyntisaamisten asetukset** -sivulla.