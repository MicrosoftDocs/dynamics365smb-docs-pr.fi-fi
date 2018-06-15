---
title: "Ongelmien vianmääritys itsepalvelun rekisteröitymisen avulla | Microsoft Docs"
description: "Lisätietoja yleistä syistä, minkä vuoksi Business Central -sovellukseen rekisteröityminen ei onnistu ja miten nämä ongelmat voidaan kiertää."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 4fceff1a6cf728608a49182a9704f187d31767fe
ms.openlocfilehash: f1d432ae73696e9e81bdc96c939051b676008e54
ms.contentlocale: fi-fi
ms.lasthandoff: 05/28/2018

---
# <a name="troubleshooting-self-service-sign-up"></a>Itsepalvelun rekisteröitymisen vianmääritys
[!INCLUDE[d365fin](includes/d365fin_md.md)]iin rekisteröityminen on helppoa ja nopeaa. Voit luoda ilmaisen tilin myös silloin, jos organisaatio on olemassa. Tässä artikkelissa kerrotaan ongelmista, joita rekisteröitymisen aikana voi ilmetä.

## <a name="what-email-address-can-i-use-with-business-central"></a>Mitä sähköpostiosoitetta voin käyttää Business Central -sovelluksen kanssa?
[!INCLUDE[d365fin](includes/d365fin_md.md)] edellyttää työ- tai opiskelupaikan antaman sähköpostiosoitteen käyttämistä rekisteröitymisen yhteydessä. [!INCLUDE[d365fin](includes/d365fin_md.md)] ei tue kuluttajille tarkoitettujen sähköpostipalveluiden ja tietoliikennepalveluiden tarjoajien sähköpostiosoitteita. Näitä ovat esimerkiksi outlook.com, hotmail.com ja gmail.com.

Jos yrität rekisteröityä käyttämällä henkilökohtaista sähköpostiosoitetta, saat viestin, jossa pyydetään käyttämään työ- tai opiskelupaikan antamaa sähköpostiosoitetta.

## <a name="troubleshooting"></a>Vianetsintä
[!INCLUDE[d365fin](includes/d365fin_md.md)]iin voidaan usein rekisteröityä rekisteröitymisprosessin avulla. Itsepalvelun rekisteröityminen voi kuitenkin keskeytyä useasta eri syystä. Seuraavassa taulukossa esitellään yleisimpiä syitä, joiden vuoksi rekisteröityminen ei onnistu, sekä ratkaisuja näihin ongelmiin.

| Oire/virhesanoma | Syy ja ratkaisu |
| --- | --- |
| Jos Office 365 -sähköpostiosoitteita ei ole rekisteröity tuetussa maassa, sinulle lähetetään rekisteröitymisen yhteydessä seuraava viesti:<br /><br />**Toiminto ei onnistunut. Microsoft ei vielä tue maatasi tai aluettasi.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] tukee nykyään vain Office 365:n sähköpostitileihin, jotka on rekisteröity rajallisille markkinoille. Lisätietoja on kohdassa [Aluekohtainen saatavuus](#regional-availability). |
| Henkilökohtaisia sähköpostiosoitteita, kuten nancy@gmail.com, ei tueta. Näyttöön tulee rekisteröitymisen yhteydessä seuraavan tyyppinen viesti:<br /><br />**Annoit henkilökohtaisen sähköpostiosoitteen: anna työsähköpostiosoite, jotta yrityksen tiedot voidaan tallentaa turvallisesti.**<br> tai <br> **Tämä näyttää henkilökohtaiselta sähköpostiosoitteelta. Anna työsähköpostiosoite, jotta voimme yhdistää sinut muihin yrityksesi henkilöihin. Eikä hätää; Microsoft ei jaa osoitettasi kenenkään kanssa.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] ei tue kuluttajille tarkoitettujen sähköpostipalveluiden ja tietoliikennepalveluiden tarjoajien sähköpostiosoitteita. Tee rekisteröityminen valmiiksi yrittämällä uudelleen työpaikan tai koulun myöntämällä sähköpostiosoitteella. Jos rekisteröityminen ei onnistu vieläkään ja haluat kokeilla monimutkaisempaa asetusprosessia, voit rekisteröityä uuteen Office 365 -kokeiluversioon ja rekisteröityä kyseisellä sähköpostiosoitteella. |
| sähköpostiosoitteet .gov tai .mil. Rekisteröitymisen yhteydessä saat seuraavan tyyppisen viestin:<br /><br />**[!INCLUDE[d365fin](includes/d365fin_md.md)] ei ole käytettävissä: [!INCLUDE[d365fin](includes/d365fin_md.md)] ei ole tällä hetkellä niiden käyttäjien käytettävissä, joiden sähköpostiosoitteen pääte on .gov tai .mil. Käytä toista työsähköpostiosoitetta tai yritä myöhemmin uudelleen.** <br>tai <br>**Rekisteröityminen ei onnistu. Näyttää siltä, että [!INCLUDE[d365fin](includes/d365fin_md.md)] ei ole tällä hetkellä työpaikkasi tai koulusi käytettävissä.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] ei tue tällä hetkellä sähköpostiosoitteita, joiden pääte on .gov tai .mil. |
| Itsepalvelun rekisteröityminen ei ole käytössä. Näyttöön tulee rekisteröitymisen yhteydessä seuraavan tyyppinen viesti:<br /><br />**Rekisteröityminen ei onnistu. IT-osasto on poistanut [!INCLUDE[d365fin](includes/d365fin_md.md)]iin kirjautumisen käytöstä. Ota IT-osastoon yhteys, kun haluat viimeistellä rekisteröitymisen.** <br>tai <br> **Tämä näyttää henkilökohtaiselta sähköpostiosoitteelta. Anna työsähköpostiosoite, jotta voimme yhdistää sinut muihin yrityksesi henkilöihin. Eikä hätää; Microsoft ei jaa osoitettasi kenenkään kanssa.** |Organisaation IT-järjestelmänvalvoja on poistanut [!INCLUDE[d365fin](includes/d365fin_md.md)]in itsepalvelun rekisteröitymisen käytöstä. Viimeistele rekisteröityminen ottamalla yhteys IT-osastoon ja pyytämällä heitä noudattamaan alla olevan sivun ohjeita. Niiden avulla nykyiset käyttäjät voivat rekisteröityä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin ja uudet käyttäjät voivat liittyä olemassa olevaan vuokraajaan. Tämä ongelma saattaa esiintyä myös silloin, kun rekisteröidyt Office 365:een kumppanin kautta. |
| Sähköpostiosoite ei ole Office 365:n tunnus. Näyttöön tulee rekisteröitymisen yhteydessä seuraavan tyyppinen viesti:<br /><br />**Sähköpostiosoitettasi ei löydy contoso.com-tiedoista. Käytätkö eri tunnusta töissä tai koulussa? Yritä rekisteröityä tällä toisella tunnuksella. Jos rekisteröityminen ei onnistu, ota yhteys yrityksen IT-osastoon.** |Organisaatiosi kirjautuu Office 365:een ja muihin Microsoft-palveluihin tunnuksilla eikä sähköpostiosoitteella. Sähköpostiosoitteesi voi olla esimerkiksi Nancy.Smith@contoso.com, kun taas tunnuksesi voi olla nancys@contoso.com. Voit tehdä rekisteröitymisen valmiiksi käyttämällä tunnusta, jonka organisaatio on määrittänyt Office 365:een tai muihin Microsoft-palveluihin rekisteröitymistä varten. Jos et tiedä tunnusta, ota yhteys IT-järjestelmänvalvojaan. Jos rekisteröityminen ei onnistu vieläkään ja haluat kokeilla monimutkaisempaa asetusprosessia, voit rekisteröityä uuteen Office 365 -kokeiluversioon ja rekisteröityä kyseisellä sähköpostiosoitteella. |
| Jos Office 365 -tili on rekisteröity tuetussa maassa ja olet rekisteröitymässä [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan eri maassa, näyttöön tulee rekisteröitymisen yhteydessä seuraavan tyyppinen viesti:<br /><br />**Toiminto ei onnistunut. Microsoft ei vielä tue maatasi tai aluettasi.**| Organisaation Office 365 -tilaus on rekisteröity tietyssä maassa Office 365:n hallintaportaalissa. [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman rekisteröitymisessä käytetään nykyisen selaimen kieltä ja kielialuetta. Tämän vuoksi saatat saada virhesanoman, vaikka sijaintisi olisi tuettu maa. Pyydä IT-järjestelmänvalvojaa tarkistamaan [Office 365:n hallintaportaalin](https://portal.office.com/adminportal/home#/companyprofile) organisaatioprofiilissa määritetty maa. Saatat joutua käyttämään eri tiliä [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa.|

## <a name="regional-availability"></a>Aluekohtainen saatavuus
[!INCLUDE[d365fin](includes/d365fin_md.md)] on tällä hetkellä saatavana seuraavilla markkinoilla:

| Eurooppa | Pohjois-Amerikka |
| --- | --- |
| Itävalta | Kanada |
| Belgia | Yhdysvallat |
| Tanska | |
| Saksa | |
| Suomi | |
| Ranska | |
| Italia | |
| Alankomaat | |
| Espanja | |
| Ruotsi | |
| Sveitsi | |
| Iso-Britannia | |

## <a name="see-also"></a>Katso myös
[Tervetuloa [!INCLUDE[d365fin](includes/d365fin_long_md.md)]iin!](index.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

