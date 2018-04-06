---
title: "Rakenteen tiedot – taulukon rakenne | Microsoft Docs"
description: "Dimensiotapahtumien tallennuksen ja kirjauksen uudelleensuunnittelun ymmärtäminen edellyttää taulukkorakenteen ymmärtämistä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 900605cd276698e3e6146d18e36ed18363b6c99c
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-table-structure"></a>Rakennetiedot: taulukkorakenne
Dimensiotapahtumien tallennuksen ja kirjauksen uudelleensuunnittelun ymmärtäminen edellyttää taulukkorakenteen ymmärtämistä.  

## <a name="new-tables"></a>Uudet taulukot  
 Dimensioyhdistelmätapahtumien hallintaa varten on suunniteltu kolme uutta taulukkoa.  

### <a name="table-480-dimension-set-entry"></a>Taulukko 480 Dimensioyhdistelmän tapahtuma  
 Taulukko 480 **Dimensionasetuskirjaus** on uusi taulukko. Tätä taulukkoa ei voi muuttaa. Kun tiedot on kirjoitettu taulukkoon, et voi poistaa tai muokata niitä. Tietojen poistaminen edellyttää, että tarkistat kaikki dimensioyhdistelmän tunnuksen esiintymät tietokannassa, partner solutions -ratkaisut mukaan lukien.  

|Kentän nro|Kentän nimi|Tietotyyppi|Kommentti|  
|---------------|----------------|---------------|-------------|  
|1|**Tunnus**|Kokonaisluku|> 0.0 on varattu tyhjälle dimensioyhdistelmälle. Viittaukset kenttään 3 taulukossa 481.|  
|2|**Dimensiokoodi**|Koodi 20|Taulukon suhde taulukkoon 348.|  
|3|**Dimension arvokoodi**|Koodi 20|Taulukon suhde taulukkoon 349|  
|4|**Dimensioarvon tunnus**|Kokonaisluku|Viittaukset kenttään 12 taulukossa 349. Se on toissijainen avain, jota käytetään taulukon 481 selaamiseen.|  
|5|**Dimension nimi**|Teksti 30|CalcField. Taulukon 348 haku.|  
|6|**Dimensioarvon nimi**|Teksti 30|CalcField. Taulukon 349 haku.|  

#### <a name="table-481-dimension-set-tree-node"></a>Taulukko 481 Dimensioyhdistelmän puusolmu  
 Taulukko 481 **Dimensionasetuksen puusolmu** on uusi taulukko. Tätä taulukkoa ei voi muuttaa. Sitä käytetään hakuun dimensioyhdistelmässä. Jos dimensioyhdistelmää ei löydy, tällöin luodaan uusi yhdistelmä.  

|Kentän nro|Kentän nimi|Tietotyyppi|Kommentti|  
|---------------|----------------|---------------|-------------|  
|1|**Päädimensioyhdistelmän tunnus**|Kokonaisluku|0 ylimmän tason solmulle.|  
|2|**Dimensioarvon tunnus**|Kokonaisluku|Taulukon suhde kenttään 12 taulukossa 349.|  
|3|**Dimensioyhdistelmän tunnus**|Kokonaisluku|AutoIncrement. Käytetään taulukon 480 kentässä 1.|  
|4|**Käytössä**|Totuusarvo|Epätosi, jos se ei ole käytössä.|  

##### <a name="table-482-reclas-dimension-set-buffer"></a>Taulukko 482 Uudelleenluokita dimensioyhdistelmän puskuri  
 Taulukko 482 **Uudelleenluok. dimensionasetuksen puskuri** on uusi taulukko. Tämän taulukon avulla voit muokata dimensioyhdistelmän tunnusta. Se on pakollinen, kun muokkaat dimensioarvokoodia ja uutta dimensioarvokoodia, esimerkiksi **Nimik. uud.luok.pvk**-taulukossa.  

|Kentän nro|Kentän nimi|Tietotyyppi|Kommentti|  
|---------------|----------------|---------------|-------------|  
|1|**Dimensiokoodi**|Koodi 20|Taulukon suhde taulukkoon 348.|  
|2|**Dimension arvokoodi**|Koodi 20|Taulukon suhde taulukkoon 349|  
|3|**Dimensioarvon tunnus**|Kokonaisluku|Viittaukset kenttään 12 taulukossa 349.|  
|4|**Uusi dimension arvokoodi**|Koodi 20|Taulukon suhde taulukkoon 349|  
|5|**Uusi dimensioarvon tunnus**|Kokonaisluku|Viittaukset kenttään 12 taulukossa 349.|  
|6|**Dimension nimi**|Teksti 30|CalcField. Taulukon 348 haku.|  
|7|**Dimensioarvon nimi**|Teksti 30|CalcField. Taulukon 349 haku.|  
|8|**Uusi dimensioarvon nimi**|Teksti 30|CalcField. Taulukon 349 haku.|  

## <a name="modified-tables"></a>Tietoja muutetuista taulukoista  
 Kaikki tapahtuma- ja budjettitaulukot on muutettu hallitsemaan dimensioyhdistelmän tapahtumia.  

### <a name="changes-to-transaction-and-budget-tables"></a>Muutokset tapahtuma- ja budjettitaulukoihin  
 Kaikkiin tapahtumiin ja budjettitaulukoihin on lisätty uusi kenttä.  

|Kentän nro|Kentän nimi|Tietotyyppi|Kommentti|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensioyhdistelmän tunnus**|Kokonaisluku|Viittaukset kenttään 1 taulukossa 480.|  

#### <a name="changes-to-table-83-item-journal-line"></a>Muutokset taulukkoon 83, nimikepäiväkirjan rivi  
 Kaksi uutta kenttää on lisätty taulukkoon 83, **nimikepäiväkirjarivi**.  

|Kentän nro|Kentän nimi|Tietotyyppi|Kommentti|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensioyhdistelmän tunnus**|Kokonaisluku|Viittaukset kenttään 1 taulukossa 480.|  
|481|**Uusi dimensioyhdistelmän tunnus**|Kokonaisluku|Viittaukset kenttään 1 taulukossa 480.|  

##### <a name="changes-to-table-349-dimension-value"></a>Muutokset taulukkoon 349, dimensioarvo  
 Taulukkoon 349 **Dimensioarvo** on lisätty uusi kenttä.  

|Kentän nro|Kentän nimi|Tietotyyppi|Kommentti|  
|---------------|----------------|---------------|-------------|  
|12|**Dimensioarvon tunnus**|Kokonaisluku|AutoIncrement. Käytetään viitteinä taulukossa 480 ja 481.|  

###### <a name="tables-that-get-new-field-480-dimension-set-id"></a>Taulukot, jotka saavat uuden kentän 480 Dimensionasetustunnus.  
 Uusi kenttä, 480 **Dimensioyhdistelmän tunnus**, on lisätty seuraaviin taulukoihin. Kirjattua tietoa sisältävien taulukoiden osalta kenttä tarjoaa vain ei muokattavissa olevan näkymän niistä dimensioista, joilla on Poraudu-merkintä. Niiden taulukoiden kohdalla, jota tallentavat työasiakirjoja, kenttä on muokattavissa. Puskuritaulukoissa, joita käytetään sisäisesti, ei tarvita muokattava- tai ei-muokattava-kykyä.  

 480-kenttä ei ole muokattavissa seuraavissa taulukoissa.  

|Taulukon nro|Taulukon nimi|  
|---------------|----------------|  
|17|**KP-tapahtuma**|  
|21|**Asiakastapahtuma**|  
|25|**Toimittajatapahtuma**|  
|32|**Nimiketapahtuma**|  
|110|**Lähtevän toimituksen otsikko**|  
|111|**Lähtevän toimituksen rivi**|  
|112|**Myyntilaskun otsikko**|  
|113|**Myyntilaskurivi**|  
|114|**Myynnin hyvityslaskun otsikko**|  
|115|**Myynnin hyvityslaskun rivi**|  
|120|**Tavaran vastaanoton otsikko**|  
|121|**Tavaran vastaanoton rivi**|  
|122|**Ostolaskun otsikko**|  
|123|**Nimikkeen ostolaskurivi**|  
|124|**Oston hyvityslaskun otsikko**|  
|125|**Ostohyvityslaskun rivi**|  
|169|**Projektitapahtuma**|  
|203|**Resurssitapahtuma**|  
|271|**Pankkitilitapahtuma**|  
|281|**Inventointitapahtuma**|  
|297|**Lähetetyn muistutuksen otsikko**|  
|304|**Lähetetyn viiv.kululaskun ots.**|  
|5107|**Myyntiotsikon arkisto**|  
|5108|**Myyntirivin arkisto**|  
|5109|**Ostojen otsikkoarkisto**|  
|5110|**Ostorivin arkisto**|  
|5601|**KO-tapahtuma**|  
|5625|**Kunnossapitotapahtuma**|  
|5629|**Vakuutuksen kattavuustapahtuma**|  
|5744|**Siirtotoimituksen otsikko**|  
|5745|**Siirtotoimituksen rivi**|  
|5746|**Siirtovastaanoton otsikko**|  
|5747|**Siirtovastaanottorivi**|  
|5802|**Arvotapahtuma**|  
|5832|**Kapasiteettitapahtuma**|  
|5907|**Huoltotapahtuma**|  
|5908|**Huolto-otsikko**|  
|5933|**Huoltotilauksen kirjauspuskuri**|  
|5970|**Arkistoidun huoltosop. otsikko**|  
|5990|**Huoltotoimituksen otsikko**|  
|5991|**Huoltotoimitusrivi**|  
|5992|**Huoltolaskun otsikko**|  
|5993|**Huoltolaskun rivi**|  
|5994|**Huollon hyvityslaskun otsikko**|  
|5995|**Huollon hyvityslaskurivi**|  
|6650|**Pal.toimituksen otsikko**|  
|6651|**Palautustoimituksen rivi**|  
|6660|**Palautusvast.oton otsikko**|  
|6661|**Pal.vastaanottorivi**|  

 480-kenttä on muokattavissa seuraavissa taulukoissa.  

|Taulukon nro|Taulukon nimi|  
|---------------|----------------|  
|36|**Myynnin tunnistetiedot**|  
|37|**Myyntirivi**|  
|38|**Ostojen tunnistetiedot**|  
|39|**Ostorivi**|  
|81|**Yleisen päiväkirjan rivi**|  
|83|**Nimikepäiväkirjan rivi**|  
|89|**Tuoterakenteen päiväkirjan rivi**|  
|96|**KP-budjetin tapahtuma**|  
|207|**Resurssipäiväkirjan rivi**|  
|210|**Projektipäiväkirjan rivi**|  
|221|**Yleisen päiväkirjan kohdistus**|  
|246|**Hankintarivi**|  
|295|**Muistutuksen otsikko**|  
|302|**Viivästyskululaskun otsikko**|  
|5405|**Tuotantotilaus**|  
|5406|**Tuotantotilauksen rivi**|  
|5407|**Tuotantotilauksen komponentti**|  
|5615|**KO-kohdistus**|  
|5621|**KO-päiväkirjan rivi**|  
|5635|**Vakuutuspäiväkirjan rivi**|  
|5740|**Siirto-otsikko**|  
|5741|**Siirtorivi**|  
|5900|**Huolto-otsikko**|  
|5901|**Huoltonimikerivi**|  
|5902|**Huoltorivi**|  
|5965|**Huoltosopimuksen otsikko**|  
|5997|**Vakiohuoltorivi**|  
|7134|**Nimikkeen budjettitapahtuma**|  
|99000829|**Suunnittelun komponentti**|  

 480-kenttä on lisätty seuraaviin puskuritaulukoihin.  

|Taulukon nro|Taulukon nimi|  
|---------------|----------------|  
|49|**Laskun kirjauspuskuri**|  
|212|**Projektin kirjauspuskuri**|  
|372|**Maksupuskuri**|  
|382|**AT tapahtumapuskuri**|  
|461|**Ennakkomaksulaskun rivipuskuri**|  
|5637|**KO - KP-kirjauspuskuri**|  
|7136|**Nimikkeen budjettipuskuri**|  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Dimensioyhdistelmätapahtumat](design-details-dimension-set-entries.md)   
 [Dimensioyhdistelmätapahtumien yleiskuva](design-details-dimension-set-entries-overview.md)   
 [Rakennetiedot: dimensioyhdistelmien etsiminen](design-details-searching-for-dimension-combinations.md)   
 [Rakennetiedot: Koodiyksikön 408 dimension hallinta](design-details-codeunit-408-dimension-management.md)   
 [Rakennetiedot: koodiesimerkkejä muuttuneista kuvioista muutoksissa](design-details-code-examples-of-changed-patterns-in-modifications.md)

