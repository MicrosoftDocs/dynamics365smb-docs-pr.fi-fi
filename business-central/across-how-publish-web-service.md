---
title: "Objektien näyttäminen verkkopalveluina | Microsoft Docs"
description: Kun julkaiset objekteja verkkopalveluina, ne ovat heti saatavilla verkossa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: be986c07849db4cdc19ad2e492887373753f5dbe
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="publish-a-web-service"></a>Verkkopalvelun julkaiseminen

Verkkopalvelut ovat kevyt tapa tuoda sovelluksen toiminnallisuus useiden ulkoisten järjestelmien ja käyttäjien saataville. [!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää useita objekteja, jotka näytetään oletusarvoisesti verkkopalveluina, koska ne on integroitu muiden Microsoftin palvelujen kanssa, mutta voit lisätä myös muita verkkopalveluja.  

Voit määrittää verkkopalvelun Windows- tai verkkoasiakasohjelmassa. Sinun tulee sitten julkaista verkkopalvelu, jotta se on saatavilla huoltopyyntöjen käytettäväksi verkon välityksellä. Käyttäjät löytävät verkkopalvelut osoittamalla selainta palvelinsijainnissa ja pyytämällä luettelon käytettävissä olevista palveluista. Kun julkaiset verkkopalvelun, se tulee välittömästi käyttöön todennetuille käyttäjille verkon kautta. Kaikki valtuutetut käyttäjät voivat käyttää verkkopalveluiden metatietoja, mutta vain käyttäjät, joilla on riittävät oikeudet, voivat käyttää varsinaisia tietoja.

## <a name="creating-and-publishing-a-web-service"></a>Verkkopalvelun luominen ja julkaiseminen  
Seuraavassa kerrotaan, kuinka voit luoda ja julkaista verkkopalvelun.  

### <a name="to-create-and-publish-a-web-service"></a>Verkkopalvelun luominen ja julkaiseminen  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **WWW-palvelut** ja valitse sitten liittyvä linkki.  
2.  Valitse **Verkkopalvelut**-ikkunassa **Uusi**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  **Koodiyksikkö** ja **Sivu** ovat kelvollisia SOAP-verkkopalveluja. **Sivu** ja **Kysely** ovat kelvollisia OData-verkkopalvelutyyppejä.  
    Jos tietokanta lisäksi sisältää useita yrityksiä, voit valita yhdelle yritykselle kuuluvan objektitunnuksen.  
    Palvelunimi näkyy verkkopalvelun käyttäjille, ja sen perusteella tunnistetaan ja erotellaan verkkopalvelut, joten nimen on oltava merkityksellinen.

3.  Valitse valintaruutu **Julkaistu**-sarakkeessa.  

Kun julkaiset verkkopalvelun, **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä näkyvät verkkopalvelua varten luodut URL-osoitteet. Voit testata verkkopalvelua heti valitsemalla linkit **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä. Vaihtoehtoisesti voit kopioida kentän arvon ja tallentaa sen myöhempää käyttöä varten.  

Verkkopalveluna julkaistu palvelu on ulkoisten osapuolien käytettävissä. Voit tarkistaa kyseisen verkkopalvelun saatavuuden selaimen avulla tai valitsemalla linkin **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä **Verkkopalvelut**-ikkunassa. Seuraavassa on kuvattu, miten voit tarkistaa verkkopalvelun käytettävyyden myöhempää käyttöä varten.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Verkkopalvelun saatavuuden tarkistaminen  

1.  Kirjoita selaimeen asianmukainen URL-osoite. Seuraavassa taulukossa on kuvattu URL-osoitteiden tyypit, jotka voi antaa erilaisille verkkopalvelutyypeille.  
> [!div class="mx-tdBreakAll"]
> |Tyyppi|Syntaksi|Esimerkki|
> |----------------|------|-------|
> |SOAP |https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/ |https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com |
> |OData |https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')|[https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com](https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com) <br />    Yrityksen nimi -kentässä huomioidaan kirjainkoko.|

2.  Tarkista tiedot, jotka näkyvät selaimessa. Varmista, että näet luomasi verkkopalvelun nimen.  

Kun siirryt verkkopalveluun ja haluat kirjoittaa tiedot takaisin kohteeseen [!INCLUDE[d365fin](includes/d365fin_md.md)], yrityksen nimi on määritettävä. Voit määrittää yrityksen esimerkkien tavoin osana URI:a tai osana kyselyparametrejä. Esimerkiksi seuraavat URI:t osoittavat samaan OData-verkkopalveluun ja molemmat ovat kelvollisia URI-osoitteita.  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a>Katso myös  
[Hallinta](admin-setup-and-administration.md)  

