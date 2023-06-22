---
title: Rakenteen tiedot – taulukon rakenne | Microsoft Docs
description: Dimensiotapahtumien tallennuksen ja kirjauksen uudelleensuunnittelun ymmärtäminen edellyttää taulukkorakenteen ymmärtämistä.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-table-structure" />Rakennetiedot: taulukkorakenne
Dimensiotapahtumien tallennuksen ja kirjauksen ymmärtäminen edellyttää taulukkorakenteen ymmärtämistä.  

## <a name="table--dimension-set-entry" />Taulukko 480, Dimensioyhdistelmän tapahtuma
Tätä taulukkoa ei voi muuttaa. Kun tiedot on kirjoitettu taulukkoon, et voi poistaa tai muokata niitä.

|Kentän nro|Kentän nimi|Tietotyyppi|Kommentti|  
|---------------|----------------|---------------|-------------|  
|1|**Tunnus**|Kokonaisluku|> 0.0 on varattu tyhjälle dimensioyhdistelmälle. Viittaukset kenttään 3 taulukossa 481.|  
|2|**Dimensiokoodi**|Koodi 20|Taulukon suhde taulukkoon 348.|  
|3|**Dimension arvokoodi**|Koodi 20|Taulukon suhde taulukkoon 349|  
|4|**Dimensioarvon tunnus**|Kokonaisluku|Viittaukset kenttään 12 taulukossa 349. Se on toissijainen avain, jota käytetään taulukon 481 selaamiseen.|  
|5|**Dimension nimi**|Teksti 30|CalcField. Taulukon 348 haku.|  
|6|**Dimensioarvon nimi**|Teksti 30|CalcField. Taulukon 349 haku.|  

## <a name="table--dimension-set-tree-node" />Taulukko 481, Dimensioyhdistelmän puusolmu
Tätä taulukkoa ei voi muuttaa. Sitä käytetään hakuun dimensioyhdistelmässä. Jos dimensioyhdistelmää ei löydy, tällöin luodaan uusi yhdistelmä.  

|Kentän nro|Kentän nimi|Tietotyyppi|Kommentti|  
|---------------|----------------|---------------|-------------|  
|1|**Päädimensioyhdistelmän tunnus**|Kokonaisluku|0 ylimmän tason solmulle.|  
|2|**Dimensioarvon tunnus**|Kokonaisluku|Taulukon suhde kenttään 12 taulukossa 349.|  
|3|**Dimensioyhdistelmän tunnus**|Kokonaisluku|AutoIncrement. Käytetään taulukon 480 kentässä 1.|  
|4|**Käytössä**|Totuusarvo|Epätosi, jos se ei ole käytössä.|  

## <a name="table--reclas-dimension-set-buffer" />Taulukko 482 Uudelleenluokita dimensioyhdistelmän puskuri
Taulukkoa käytetään, kun muutat dimensioarvon koodia esimerkiksi nimiketapahtumassa käyttämällä **Nimikkeen uudelleenluokituspäiväkirja** -sivua.  

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

## <a name="transaction-and-budget-tables" />Tapahtuma- ja budjettitaulukot
Muiden taulukon dimensiokenttien lisäksi tämä kenttä on tärkeä:  

|Kentän nro|Kentän nimi|Tietotyyppi|Kommentti|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensioyhdistelmän tunnus**|Kokonaisluku|Viittaukset kenttään 1 taulukossa 480.|  

### <a name="table--item-journal-line" />Taulukko 83, Nimikepäiväkirjan rivi
Muiden taulukon dimensiokenttien lisäksi nämä kentät ovat tärkeitä.  

|Kentän nro|Kentän nimi|Tietotyyppi|Kommentti|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensioyhdistelmän tunnus**|Kokonaisluku|Viittaukset kenttään 1 taulukossa 480.|  
|481|**Uusi dimensioyhdistelmän tunnus**|Kokonaisluku|Viittaukset kenttään 1 taulukossa 480.|  

### <a name="table--dimension-value" />Taulukko 349, Dimensioarvo
Muiden taulukon dimensiokenttien lisäksi nämä kentät ovat tärkeitä.  

|Kentän nro|Kentän nimi|Tietotyyppi|Kommentti|  
|---------------|----------------|---------------|-------------|  
|12|**Dimensioarvon tunnus**|Kokonaisluku|AutoIncrement. Käytetään viitteinä taulukossa 480 ja 481.|  

### <a name="tables-that-contain-the-dimension-set-id-field" />Taulukot, jotka sisältävät Dimensionasetustunnus-kentän
 **Dimensioasetustunnus**-kenttä (480) on seuraavissa taulukoissa. Kirjattua tietoa sisältävien taulukoiden osalta kenttä tarjoaa vain ei muokattavissa olevan näkymän niistä dimensioista, joilla on Poraudu-merkintä. Niiden taulukoiden kohdalla, jota tallentavat työasiakirjoja, kenttä on muokattavissa. Puskuritaulukoissa, joita käytetään sisäisesti, ei tarvita muokattava- tai ei-muokattava-kykyä.  

 Kenttä 480 ei ole muokattavissa seuraavissa taulukoissa.  

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

Kenttä 480 on muokattavissa seuraavissa taulukoissa.  

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

Kenttä 480 on seuraavissa puskuritaulukoissa.  

|Taulukon nro|Taulukon nimi|  
|---------------|----------------|  
|49|**Laskun kirjauspuskuri**|  
|212|**Projektin kirjauspuskuri**|  
|372|**Maksupuskuri**|  
|382|**AT tapahtumapuskuri**|  
|461|**Ennakkomaksulaskun rivipuskuri**|  
|5637|**KO - KP-kirjauspuskuri**|  
|7136|**Nimikkeen budjettipuskuri**|  

## <a name="see-also" />Katso myös

[Dimensioyhdistelmätapahtumien yleiskuva](design-details-dimension-set-entries-overview.md)  
[Rakennetiedot: Dimensioyhdistelmien etsiminen](design-details-searching-for-dimension-combinations.md)   
