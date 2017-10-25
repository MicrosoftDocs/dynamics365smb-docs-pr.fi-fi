---
title: "Objektien näyttäminen verkkopalveluina | Microsoft Docs"
description: "Julkaise [!INCLUDE[d365fin](includes/d365fin_md.md)]in objekteja verkkopalveluina, jonka jälkeen niitä voi käyttää heti verkossa."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 278515fc479a72957fb52dad71ce2f98d354ee32
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-publish-a-web-service"></a>Toimintaohje: verkkopalvelun julkaiseminen
Verkkopalvelut ovat kevyt tapa tuoda sovelluksen toiminnallisuus useiden ulkoisten järjestelmien ja käyttäjien saataville. [!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää useita objekteja, jotka näytetään oletusarvoisesti verkkopalveluina, koska ne on integroitu muiden Microsoftin palvelujen kanssa, mutta voit lisätä myös muita verkkopalveluja.  

Voit määrittää verkkopalvelun Windows- tai verkkoasiakasohjelmassa. Sinun tulee sitten julkaista verkkopalvelu, jotta se on saatavilla huoltopyyntöjen käytettäväksi verkon välityksellä. Käyttäjät löytävät verkkopalvelut osoittamalla selainta palvelinsijainnissa ja pyytämällä luettelon käytettävissä olevista palveluista. Kun julkaiset verkkopalvelun, se tulee välittömästi käyttöön todennetuille käyttäjille verkon kautta. Kaikki valtuutetut käyttäjät voivat käyttää verkkopalveluiden metatietoja, mutta vain käyttäjät, joilla on riittävät oikeudet, voivat käyttää varsinaisia tietoja.

## <a name="creating-and-publishing-a-web-service"></a>Verkkopalvelun luominen ja julkaiseminen  
 Seuraavassa kerrotaan, kuinka voit luoda ja julkaista verkkopalvelun.  

#### <a name="to-create-and-publish-a-web-service"></a>Verkkopalvelun luominen ja julkaiseminen  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Verkkopalvelut** ja valitse sitten aiheeseen liittyvä linkki.  

2.  Valitse **Verkkopalvelut**-sivulla **Uusi**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  **Koodiyksikkö** ja **Sivu** ovat kelvollisia SOAP-verkkopalveluja. **Sivu** ja **Kysely** ovat kelvollisia OData-verkkopalvelutyyppejä.  
    Jos tietokanta lisäksi sisältää useita yrityksiä, voit valita yhdelle yritykselle kuuluvan objektitunnuksen.  
    Palvelunimi näkyy verkkopalvelun käyttäjille, ja sen perusteella tunnistetaan ja erotellaan verkkopalvelut, joten nimen on oltava merkityksellinen.

3.  Valitse valintaruutu **Julkaistu**-sarakkeessa.  

     Kun julkaiset verkkopalvelun, **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä näkyvät verkkopalvelua varten luodut URL-osoitteet. Voit testata verkkopalvelua heti valitsemalla linkit **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä. Vaihtoehtoisesti voit kopioida kentän arvon ja tallentaa sen myöhempää käyttöä varten.  

Verkkopalveluna julkaistu palvelu on ulkoisten osapuolien käytettävissä. Voit tarkistaa kyseisen verkkopalvelun saatavuuden selaimen avulla tai valitsemalla linkin **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä **Verkkopalvelut**-ikkunassa. Seuraavassa on kuvattu, miten voit tarkistaa verkkopalvelun käytettävyyden myöhempää käyttöä varten.  

#### <a name="to-verify-the-availability-of-a-web-service"></a>Verkkopalvelun saatavuuden tarkistaminen  

1.  Kirjoita selaimeen asianmukainen URL-osoite. Seuraavassa taulukossa on kuvattu URL-osoitteiden tyypit, jotka voi syöttää. Käytä SOAP-verkkopalveluihin seuraavaa URI:n muotoa.  

    <table>
    <tr>
    <th>Verkkopalvelun tyyppi</th>
    <th>Syntaksi</th>
    <th>Esimerkki</th>
    </tr>
    <tr>
    <td>SOAP</td>
    <td>https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/</td>
    <td>https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com</td>
    </tr>
    <tr>
    <td>OData</td>
    <td>https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')</td>
    <td>https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com

         The company name is case-sensitive.</td>
    </tr>
    </table>

2.  Tarkista tiedot, jotka näkyvät selaimessa. Varmista, että näet luomasi verkkopalvelun nimen.  

 Kun siirryt verkkopalveluun ja haluat kirjoittaa tiedot takaisin kohteeseen [!INCLUDE[d365fin](includes/d365fin_md.md)], yrityksen nimi on määritettävä. Voit määrittää yrityksen esimerkkien tavoin osana URI:a tai osana kyselyparametrejä. Esimerkiksi seuraavat URI:t osoittavat samaan OData-verkkopalveluun ja molemmat ovat kelvollisia URI-osoitteita.  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a>Katso myös  
[Dynamics 365 for Financialsin määrittäminen ja hallinta](admin-setup-and-administration.md)  

