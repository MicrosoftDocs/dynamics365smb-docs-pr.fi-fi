---
title: Ongelmien vianmääritys itsepalvelun rekisteröitymisen avulla | Microsoft Docs
description: 'Lisätietoja yleistä syistä, minkä vuoksi Business Central -sovellukseen rekisteröityminen ei onnistu ja miten nämä ongelmat voidaan kiertää.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="troubleshooting-self-service-sign-up"></a>Itsepalvelun rekisteröitymisen vianmääritys
[!INCLUDE[prod_short](includes/prod_short.md)]iin rekisteröityminen on helppoa ja nopeaa. Voit luoda ilmaisen tilin myös silloin, jos organisaatio on olemassa. Tässä artikkelissa kerrotaan ongelmista, joita rekisteröitymisen aikana voi ilmetä.

## <a name="what-email-address-can-i-use-with-business-central"></a>Mitä sähköpostiosoitetta voin käyttää Business Central -sovelluksen kanssa?
[!INCLUDE[prod_short](includes/prod_short.md)] edellyttää työ- tai opiskelupaikan antaman sähköpostiosoitteen käyttämistä rekisteröitymisen yhteydessä. [!INCLUDE[prod_short](includes/prod_short.md)] ei tue kuluttajille tarkoitettujen sähköpostipalveluiden ja tietoliikennepalveluiden tarjoajien sähköpostiosoitteita. Näitä ovat esimerkiksi outlook.com, hotmail.com ja gmail.com.

Jos yrität rekisteröityä käyttämällä henkilökohtaista sähköpostiosoitetta, saat viestin, jossa pyydetään käyttämään työ- tai opiskelupaikan antamaa sähköpostiosoitetta.

## <a name="troubleshooting"></a>Vianetsintä
[!INCLUDE[prod_short](includes/prod_short.md)]iin voidaan usein rekisteröityä rekisteröitymisprosessin avulla. Itsepalvelun rekisteröityminen voi kuitenkin keskeytyä useasta eri syystä. Seuraavassa taulukossa esitellään yleisimpiä syitä, joiden vuoksi rekisteröityminen ei onnistu, sekä ratkaisuja näihin ongelmiin.

| Oire/virhesanoma | Syy ja ratkaisu |
| --------------------- | -------------------- |
| Jos Microsoft 365 -sähköpostiosoitteita ei ole rekisteröity tuetussa maassa, sinulle lähetetään rekisteröitymisen yhteydessä seuraava viesti:<br /><br />**Toiminto ei onnistunut. Microsoft ei vielä tue maatasi tai aluettasi.** |[!INCLUDE[prod_short](includes/prod_short.md)] tukee nykyään vain Microsoft 365:n sähköpostitileihin, jotka on rekisteröity rajallisille markkinoille. Lisätietoja on kohdassa [Aluekohtainen saatavuus](#regional-availability). |
| Henkilökohtaisia sähköpostiosoitteita, kuten nancy@gmail.com, ei tueta. Näyttöön tulee rekisteröitymisen yhteydessä seuraavan tyyppinen viesti:<br /><br />**Annoit henkilökohtaisen sähköpostiosoitteen: anna työsähköpostiosoite, jotta yrityksen tiedot voidaan tallentaa turvallisesti.**<br> tai <br> **Tämä näyttää henkilökohtaiselta sähköpostiosoitteelta. Anna työsähköpostiosoite, jotta voimme yhdistää sinut muihin yrityksesi henkilöihin. Eikä hätää; Microsoft ei jaa osoitettasi kenenkään kanssa.** |[!INCLUDE[prod_short](includes/prod_short.md)] ei tue kuluttajille tarkoitettujen sähköpostipalveluiden ja tietoliikennepalveluiden tarjoajien sähköpostiosoitteita. Tee rekisteröityminen valmiiksi yrittämällä uudelleen työpaikan tai koulun myöntämällä sähköpostiosoitteella. Jos rekisteröityminen ei onnistu vieläkään ja haluat kokeilla monimutkaisempaa asetusprosessia, voit rekisteröityä uuteen Microsoft 365 -kokeiluversioon ja rekisteröityä kyseisellä sähköpostiosoitteella. |
| sähköpostiosoitteet .gov tai .mil. Rekisteröitymisen yhteydessä saat seuraavan tyyppisen viestin:<br /><br />**[!INCLUDE[prod_short](includes/prod_short.md)] ei ole käytettävissä: [!INCLUDE[prod_short](includes/prod_short.md)] ei ole tällä hetkellä niiden käyttäjien käytettävissä, joiden sähköpostiosoitteen pääte on .gov tai .mil. Käytä toista työsähköpostiosoitetta tai yritä myöhemmin uudelleen.** <br>tai <br>**Rekisteröityminen ei onnistu. Näyttää siltä, että [!INCLUDE[prod_short](includes/prod_short.md)] ei ole tällä hetkellä työpaikkasi tai koulusi käytettävissä.** |[!INCLUDE[prod_short](includes/prod_short.md)] ei tue tällä hetkellä sähköpostiosoitteita, joiden pääte on .gov tai .mil. |
| Itsepalvelun rekisteröityminen ei ole käytössä. Näyttöön tulee rekisteröitymisen yhteydessä seuraavan tyyppinen viesti:<br /><br />**Rekisteröityminen ei onnistu. IT-osasto on poistanut [!INCLUDE[prod_short](includes/prod_short.md)]iin kirjautumisen käytöstä. Ota IT-osastoon yhteys, kun haluat viimeistellä rekisteröitymisen.** <br>tai <br> **Tämä näyttää henkilökohtaiselta sähköpostiosoitteelta. Anna työsähköpostiosoite, jotta voimme yhdistää sinut muihin yrityksesi henkilöihin. Eikä hätää; Microsoft ei jaa osoitettasi kenenkään kanssa.** |Organisaation IT-järjestelmänvalvoja on poistanut [!INCLUDE[prod_short](includes/prod_short.md)]in itsepalvelun rekisteröitymisen käytöstä. Viimeistele rekisteröityminen ottamalla yhteys IT-osastoon ja pyytämällä heitä noudattamaan [tämän sivun](/dynamics365/business-central/dev-itpro/developer/devenv-business-central-manage-selfservice-signups) ohjeita. Niiden avulla nykyiset käyttäjät voivat rekisteröityä [!INCLUDE[prod_short](includes/prod_short.md)]iin ja uudet käyttäjät voivat liittyä olemassa olevaan vuokraajaan. Tämä ongelma saattaa esiintyä myös silloin, kun rekisteröidyt Microsoft 365:een kumppanin kautta. |
| Sähköpostiosoite ei ole Microsoft 365:n tunnus. Näyttöön tulee rekisteröitymisen yhteydessä seuraavan tyyppinen viesti:<br /><br />**Sähköpostiosoitettasi ei löydy contoso.com-tiedoista. Käytätkö eri tunnusta töissä tai koulussa? Yritä rekisteröityä tällä toisella tunnuksella. Jos rekisteröityminen ei onnistu, ota yhteys yrityksen IT-osastoon.** |Organisaatiosi kirjautuu Microsoft 365:een ja muihin Microsoft-palveluihin tunnuksilla eikä sähköpostiosoitteella. Sähköpostiosoitteesi voi olla esimerkiksi Nancy.Smith@contoso.com, kun taas tunnuksesi voi olla nancys@contoso.com. Voit tehdä rekisteröitymisen valmiiksi käyttämällä tunnusta, jonka organisaatio on määrittänyt Microsoft 365:een tai muihin Microsoft-palveluihin rekisteröitymistä varten. Jos et tiedä tunnusta, ota yhteys IT-järjestelmänvalvojaan. Jos rekisteröityminen ei onnistu vieläkään ja haluat kokeilla monimutkaisempaa asetusprosessia, voit rekisteröityä uuteen Microsoft 365 -kokeiluversioon ja rekisteröityä kyseisellä sähköpostiosoitteella. |
| Jos Microsoft 365 -tili on rekisteröity tuetussa maassa ja olet rekisteröitymässä [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan eri maassa, näyttöön tulee rekisteröitymisen yhteydessä seuraavan tyyppinen viesti:<br /><br />**Toiminto ei onnistunut. Microsoft ei vielä tue maatasi tai aluettasi.**| Organisaation Microsoft 365 -tilaus on rekisteröity tietyssä maassa Microsoft 365:n hallintaportaalissa. [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman rekisteröitymisessä käytetään nykyisen selaimen kieltä ja kielialuetta. Tämän vuoksi saatat saada virhesanoman, vaikka sijaintisi olisi tuettu maa. Pyydä IT-järjestelmänvalvojaa tarkistamaan [Microsoft 365:n hallintaportaalin](https://portal.office.com/adminportal/home#/companyprofile) organisaatioprofiilissa määritetty maa tai alue. Saatat joutua käyttämään eri tiliä [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa.|

## <a name="regional-availability"></a>Aluekohtainen saatavuus

[!INCLUDE[prod_short](includes/prod_short.md)] on saatavilla useissa maissa tai alueilla, joiden lokalisointi on Microsoftin tai hyväksytyn lokalisointipartnerin tarjoama. Täydellinen luettelo tällä hetkellä tuetuista maista ja alueista on kohdassa [Saatavuus maassa/alueella ja tuetut käännökset.](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json)  

Yleiskuvaus Dynamics 365:n tukemista markkinoista on kohdassa [Microsoft Dynamics 365:n kansainvälinen saatavuus](/dynamics365/get-started/availability). Lisätietoja [!INCLUDE[prod_short](includes/prod_short.md)]:n paikallisista toiminnoista on [paikallisten toimintojen](about-localization.md) aloitussivulla.  

## <a name="see-also"></a>Katso myös

[Rekisteröidy maksuttoman Dynamics 365 Business Central kokeiluversion käyttäjäksi](trial-signup.md)  
[Dynamics 365 Business Central kokeiluversion usein kysytyt kysymykset](trial-faq.md)  
[Tervetuloa [!INCLUDE[prod_short](includes/prod_long.md)]iin!](welcome.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Paikalliset toiminnot](about-localization.md)  
[Saatavuus maassa/alueella ja tuetut käännökset](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json)  
[Microsoft Dynamics 365:n kansainvälinen saatavuus](/dynamics365/get-started/availability)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
