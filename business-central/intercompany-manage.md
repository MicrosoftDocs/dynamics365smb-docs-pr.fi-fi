---
title: Konsernitapahtumien hallinta
description: Voit yksinkertaistaa konsernitoiminnoilla samaan organisaatioon kuuluvien yritysten välisiä liiketoimintaprosesseja ja tapahtumia.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605,'
---
# <a name="managing-intercompany-transactions" />Konsernitapahtumien hallinta

Yritykset, joissa on useampi kuin yksi oikeushenkilöä erillisillä kirjanpitofunktioilla voivat hyötyä konsernin tapahtumista. Se on hyödyllistä esimerkiksi yrityksille, joilla on tytäryhtiöitä useilla kansainvälisillä markkinoilla tai alueilla. Organisaatio saattaa koostua useasta yrityksestä, mutta siinä ei välttämättä ole samaa määrää laskenta- ja hallintotyöryhmiä. Konsernin tapahtumat yksinkertaistavat ja virtaviivaistavat yritysten välisiä liiketoimintaprosesseja ja -tapahtumia konserniyritysten välisessä kumppanuudessa.

Kun olet määrittänyt konsernin tapahtumien asiakas- ja toimittajasuhteet, kumppanit syöttävät tietoja kerran myynti- ja ostoasiakirjoihin. Vastaava asiakirja luodaan tapahtumaan osallistuvalta kumppanilta. Tilikartan ja dimensioiden yhdistämismääritys auttaa varmistamaan, että tiedot näkyvät oikeissa paikoissa.  

Konsernitoimintoihin liittyy neljä merkittävää etua:  

* Ajansäästö ja yksinkertaistetut tapahtumat lisäävät tuottavuutta.  
* Tietojen kertakirjaus ja järjestelmänlaajuiset automaattiset päivitykset vähentävät virheitä  
* Kirjausketju on täydellinen, ja liiketoiminnoilla sekä tapahtumahistorioilla on täysi näkyvyys.  
* Tapahtumat sisar- ja tytäryhtiöiden kanssa ovat tehokkaita ja kannattavia.  

## <a name="streamline-the-flow-of-business-activities" />Liiketoimintojen sujuvuuden parantaminen

Konsernin tapahtumat -toiminto mahdollistaa myynti- ja ostoasiakirjojen sekä yleisen päiväkirjan merkintöjen jakamisen kaikkiin sivutoimistoihin, myyntitoimistoihin tai tytäryrityksiin. Tapahtumien jakelu säästää aikaa ja lisää tehokkuutta koko organisaatiossa vähentämällä tietojen syöttöä. Se vähentää tarvetta lähettää, vastaanottaa, tulostaa ja arkistoida myynti- ja ostoasiakirjoja.  

Kaikki tapahtuma-asiakirjat ovat täysin hallinnassasi. Voit esimerkiksi hylätä sinulle lähetetyn asiakirjan ja käyttää **Päiväkirjakirjauksen peruuttaminen**- ja **Vastaanottojen tai toimitusten kumoaminen** -toimintoja korjausten tekemiseen. Tehdessäsi ostoja kumppani- tai tytäryritykseltä voit päivittää ostotilausta niin kauan kuin myyjäyritys ei ole lähettänyt tavaroita.  

Kun syötät tapahtuman, sinun ei tarvitse määrittää käytössä olevia tilejä. Valitse vain konsernikumppani. Konsernitoiminto luo yleisen päiväkirjan rivejä, jotka täsmäävät molempien tapahtumaan osallistuneiden yritysten tilit. Myyntisaamisissa ja ostoveloissa asiakkaille ja toimittajille voi määrittää konsernikumppanin koodin. Tästä hetkestä lähtien kaikki näiden yritysten välisten tapahtumien tilaukset ja laskut tuottavat vastaavia asiakirjoja yhteistyöyrityksessä. Tuloksena on oikein täsmätyt tilit.  

Konserni keskittyy myynti- ja ostoasiakirjoihin sekä yleisen päiväkirjan riveihin ja mahdollistaa liiketoimet eri [!INCLUDE [prod_short](includes/prod_short.md)]-tietokantojen välillä. Esimerkiksi:

* Eri maissa/alueilla
* Useat valuutat
* Eri tilikartat
* Eri dimensiot
* Eri nimikenumerot  

Konsernin tapahtumissa käytetään erityyppisiä tapahtumia ja asiakirjoja:  

* Yleisen päiväkirjan merkinnät
* osto- ja myyntitilaukset
* osto- ja myyntilaskut
* hyvityslaskut
* palautustilaukset.

Kun konsernin tapahtumat valmistellaan, luodaan luettelo konsernikumppaneista, konsernin tilikartta ja konsernin dimensiot. Tämän jälkeen voit luoda tapahtumia konsernin yleisissä päiväkirjoissa.

> [!NOTE]
> Yleinen päiväkirja ei sinänsä sisällä valuuttoja. Se muuntaa kaikki määrät paikalliseksi valuutaksi nykyisellä vaihtokurssilla.

Kun olet määrittänyt liiketoimintakumppanit asiakkaiksi ja toimittajiksi sekä luonut heille konsernikumppanin koodit, on mahdollista vaihtaa konsernin osto- ja myyntiasiakirjoja, kuten nimikkeitä ja nimikekuluja. 

> [!NOTE]
> Yritykset eivät voi käyttää konsernin sisäisiä tietoja kaikkien tietotyyppien vaihtamiseen. Ostolaskuja ei lähetetä liiketoimintakumppaneille konsernitapahtumaprosessien avulla. Konsernitapahtumaprosessien avulla lähetetyt myyntilaskut luodaan kuitenkin ostolaskuina vastaanottavassa yrityksessä.

Kirjanpitotietojen konsolidoiminen voi olla erityisen tärkeää konsernin sisäisissä prosesseissa. Lisätietoja on kohdassa [Usean yrityksen kirjanpitotietojen konsolidoiminen](finance-consolidated-company-reporting.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.

|Tehtävä |Katso|
|---|---|
|Luo konsernitoimittajat ja -asiakkaat konsernikumppaneina ja määritä konsernin tilikartta.|[Konsernin tietojen määrittäminen](intercompany-how-setup.md)|
|Voit kirjata konsernin asiakirjojen tai päiväkirjojen avulla tapahtumia yhdessä konsernikumppanien kanssa.|[Konserniasiakirjojen ja -päiväkirjojen käyttäminen](intercompany-how-work-documents-journals.md)|
|Järjestää ja käsitellä konsernikumppanien kanssa vaihdettavat saapuvat ja lähtevät tapahtumat.|[Konsernin Saapuneet- ja Lähtevät-kansion hallinta](intercompany-how-manage-intercompany-inbox.md)|
|Konserniyritysten välisten tapahtumien avulla voit jakaa kustannuksia kumppaniyritysten kesken.|[Kustannusten kohdistaminen konsernikumppaneille](intercompany-allocate-costs.md)|

## <a name="see-also" />Katso myös

[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
