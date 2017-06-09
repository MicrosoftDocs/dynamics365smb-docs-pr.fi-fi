---
title: "Itsepalvelun rekisteröitymisen vianmääritys | Microsoft Docs"
description: "Azure AD- ongelmien vianmääritys rekisteröitymisen yhteydessä."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2016
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 9bd980c6c6172d736915119806c0ba154b22bc8a
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="troubleshooting-self-service-sign-up"></a>Itsepalvelun rekisteröitymisen vianmääritys
[!INCLUDE[d365fin](includes/d365fin_md.md)]iin rekisteröityminen on helppoa ja nopeaa. Voit luoda ilmaisen tilin myös silloin, jos organisaatio on olemassa. Tässä artikkelissa kerrotaan ongelmista, joita rekisteröitymisen aikana voi ilmetä.

## <a name="what-email-address-can-i-use-with-financials"></a>Mitä sähköpostiosoitetta voin käyttää Financialsin kanssa?
[!INCLUDE[d365fin](includes/d365fin_md.md)] edellyttää työ- tai opiskelupaikan antaman sähköpostiosoitteen käyttämistä rekisteröitymisen yhteydessä. [!INCLUDE[d365fin](includes/d365fin_md.md)] ei tue kuluttajille tarkoitettujen sähköpostipalveluiden ja tietoliikennepalveluiden tarjoajien sähköpostiosoitteita. Näitä ovat esimerkiksi outlook.com, hotmail.com ja gmail.com.

Jos yrität rekisteröityä käyttämällä henkilökohtaista sähköpostiosoitetta, saat viestin, jossa pyydetään käyttämään työ- tai opiskelupaikan antamaa sähköpostiosoitetta.

## <a name="troubleshooting"></a>Vianetsintä
[!INCLUDE[d365fin](includes/d365fin_md.md)]iin voidaan usein rekisteröityä rekisteröitymisprosessin avulla. Itsepalvelun rekisteröityminen voi kuitenkin keskeytyä useasta eri syystä. Seuraavassa taulukossa esitellään yleisimpiä syitä, joiden vuoksi rekisteröityminen ei onnistu, sekä ratkaisuja näihin ongelmiin.

| Oire/virhesanoma | Syy ja ratkaisu |
| --- | --- |
| Jos Office 365 -sähköpostiosoitteita ei ole rekisteröity Yhdysvalloissa, sinulle lähetetään rekisteröitymisen yhteydessä seuraava viesti:<br /><br />**Toiminto ei onnistunut. Microsoft ei vielä tue maatasi tai aluettasi.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] tukee tällä hetkellä vain Office 365:n Yhdysvalloissa rekisteröityjä sähköpostitilejä. |
| Henkilökohtaisia sähköpostiosoitteita, kuten nancy@gmail.com, ei tueta. Näyttöön tulee rekisteröitymisen yhteydessä seuraavan tyyppinen viesti:<br /><br />**Annoit henkilökohtaisen sähköpostiosoitteen: anna työsähköpostiosoite, jotta yrityksen tiedot voidaan tallentaa turvallisesti.**<br> tai <br> **Tämä näyttää henkilökohtaiselta sähköpostiosoitteelta. Anna työsähköpostiosoite, jotta voimme yhdistää sinut muihin yrityksesi henkilöihin. Eikä hätää; Microsoft ei jaa osoitettasi kenenkään kanssa.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] ei tue kuluttajille tarkoitettujen sähköpostipalveluiden ja tietoliikennepalveluiden tarjoajien sähköpostiosoitteita. Tee rekisteröityminen valmiiksi yrittämällä uudelleen työpaikan tai koulun myöntämällä sähköpostiosoitteella. Jos rekisteröityminen ei onnistu vieläkään, ja haluat kokeilla monimutkaisempaa asetusprosessia, voit rekisteröityä uuteen Office 365 -kokeiluversioon ja rekisteröityä kyseisellä sähköpostiosoitteella. |
| sähköpostiosoitteet .gov tai .mil. Rekisteröitymisen yhteydessä saat seuraavan tyyppisen viestin:<br /><br />**[!INCLUDE[d365fin](includes/d365fin_md.md)] ei ole käytettävissä: [!INCLUDE[d365fin](includes/d365fin_md.md)] ei ole tällä hetkellä niiden käyttäjien käytettävissä, joiden sähköpostiosoitteen pääte on .gov tai .mil. Käytä toista työsähköpostiosoitetta tai yritä myöhemmin uudelleen.** <br>tai <br>**Rekisteröityminen ei onnistu. Näyttää siltä, että [!INCLUDE[d365fin](includes/d365fin_md.md)] ei ole tällä hetkellä työpaikkasi tai koulusi käytettävissä.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] ei tue tällä hetkellä sähköpostiosoitteita, joiden pääte on .gov tai .mil. |
| Itsepalvelun rekisteröityminen ei ole käytössä. Näyttöön tulee rekisteröitymisen yhteydessä seuraavan tyyppinen viesti:<br /><br />**Rekisteröityminen ei onnistu. IT-osasto on poistanut [!INCLUDE[d365fin](includes/d365fin_md.md)]iin kirjautumisen käytöstä. Ota IT-osastoon yhteys, kun haluat viimeistellä rekisteröitymisen.** <br>tai <br> **Tämä näyttää henkilökohtaiselta sähköpostiosoitteelta. Anna työsähköpostiosoite, jotta voimme yhdistää sinut muihin yrityksesi henkilöihin. Eikä hätää; Microsoft ei jaa osoitettasi kenenkään kanssa.** |Organisaation IT-järjestelmänvalvoja on poistanut [!INCLUDE[d365fin](includes/d365fin_md.md)]in itsepalvelun rekisteröitymisen käytöstä. Viimeistele rekisteröityminen ottamalla yhteys IT-osastoon ja pyytämällä heitä noudattamaan alla olevan sivun ohjeita. Niiden avulla nykyiset käyttäjät voivat rekisteröityä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin ja uudet käyttäjät voivat liittyä olemassa olevaan vuokraajaan. Tämä ongelma saattaa esiintyä myös silloin, kun rekisteröidyt Office 365:een kumppanin kautta. |
| Sähköpostiosoite ei ole Office 365:n tunnus. Näyttöön tulee rekisteröitymisen yhteydessä seuraavan tyyppinen viesti:<br /><br />**Sähköpostiosoitettasi ei löydy contoso.com-tiedoista. Käytätkö eri tunnusta töissä tai koulussa? Yritä rekisteröityä tällä toisella tunnuksella. Jos rekisteröityminen ei onnistu, ota yhteys yrityksen IT-osastoon.** |Organisaatiosi käyttää sähköpostiosoitteiden sijaan tunnuksia Office 365:een ja muihin Microsoft-palveluihin rekisteröitymisessä. Sähköpostiosoitteesi voi olla esimerkiksi Nancy.Smith@contoso.com, kun taas tunnuksesi voi olla nancys@contoso.com. Voit tehdä rekisteröitymisen valmiiksi käyttämällä tunnusta, jonka organisaatio on määrittänyt Office 365:een tai muihin Microsoft-palveluihin rekisteröitymistä varten. Jos et tiedä tunnusta, ota yhteys IT-järjestelmänvalvojaan. Jos rekisteröityminen ei onnistu vieläkään, ja voit kokeilla monimutkaisempaa asetusprosessia, voit rekisteröityä uuteen Office 365 -kokeiluversioon ja rekisteröityä kyseisellä sähköpostiosoitteella. |

## <a name="see-also"></a>Katso myös
[Tervetuloa [!INCLUDE[d365fin](includes/d365fin_long_md.md)]iin](index.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)


