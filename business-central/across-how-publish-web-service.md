---
title: Objektien näyttäminen verkkopalveluina
description: Julkaise objektit verkkopalveluina, jolloin niitä voi käyttää heti Business Central -ratkaisussa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/08/2020
ms.author: edupont
ms.openlocfilehash: 658816cfb65580404bc8ef10472a5b62c6815c9e
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989486"
---
# <a name="publish-a-web-service"></a>Verkkopalvelun julkaiseminen

Verkkopalvelut ovat kevyt tapa tuoda sovelluksen toiminnallisuus erilaisten ulkoisten järjestelmien ja käyttäjien saataville. Oletusarvoisesti [!INCLUDE[d365fin](includes/d365fin_md.md)] näyttää useita objekteja verkkopalveluina, että ne voidaan paremmin integroida muihin Microsoft-palveluihin. Voit lisätä muita verkkopalveluita yrityksesi tarpeiden mukaan.  

Määritä verkkopalvelu [!INCLUDE[d365fin](includes/d365fin_md.md)] -sivustossa ja julkaise verkkopalvelu siten, että se on todennettujen käyttäjien käytettävissä. Kaikki valtuutetut käyttäjät voivat käyttää verkkopalveluiden metatietoja, mutta vain käyttäjät, joilla on riittävät oikeudet, voivat käyttää varsinaisia tietoja.  

## <a name="creating-and-publishing-a-web-service"></a>Verkkopalvelun luominen ja julkaiseminen

Seuraavassa kerrotaan, kuinka voit luoda ja julkaista verkkopalvelun.  

### <a name="to-create-and-publish-a-web-service"></a>Verkkopalvelun luominen ja julkaiseminen  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Verkkopalvelut** ja valitse sitten liittyvä linkki.  
2. Valitse **Verkkopalvelut**-sivulla **Uusi**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Koodiyksikkö** ja **Sivu** ovat kelvollisia SOAP-verkkopalveluja. **Sivu** ja **Kysely** ovat kelvollisia OData-verkkopalvelutyyppejä. Versiosta 16.3 lähtien **Codeunit** on myös kelvollinen tyyppi OData v4 -verkkopalveluille, mutta käyttöliittymässä ei näy URL-osoitetta. Jos tietokanta lisäksi sisältää useita yrityksiä, voit valita yhdelle yritykselle kuuluvan objektitunnuksen.  
    > Palvelunimi näkyy verkkopalvelun käyttäjille, ja sen perusteella tunnistetaan ja erotellaan verkkopalvelut, joten nimen on oltava merkityksellinen.

3. Valitse valintaruutu **Julkaistu**-sarakkeessa.  

Kun julkaiset verkkopalvelun, uudet URL-osoitteet näkyvät **OData URL**- ja **SOAP URL** -kentissä. Koodayksiköille, jotka ovat alttiina sitoutumattomina OData v4 -toimintoina, URL-kenttiä ei kuitenkaan näytetä.  

Voit testata verkkopalvelua heti valitsemalla linkit **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä. Vaihtoehtoisesti kopioi kentän arvo ja tallenna se myöhempää käyttöä varten. Voit testata sitoutumattomia OData v4 -toimintoja sisältäviä koodiyksiköitä noudattamalla kehittäjän sisällön [verkkopalvelun käytettävyyden varmistaminen](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) -osan ohjeita.

> [!NOTE]
> Jos verkkopalveluina näyttämäsi objektit eivät ole käytettävissä [!INCLUDE[prodshort](includes/prodshort.md)]-palvelusta online-muodossa, sinun täytyy merkitä koodissa näkyvät menetelmät muodossa `[Scope('OnPrem')]`. Lisätietoja on kohdassa [Alueen määrite](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).

Verkkopalveluna julkaistu palvelu on ulkoisten osapuolien käytettävissä. Voit tarkistaa kyseisen verkkopalvelun saatavuuden selaimen avulla tai valitsemalla linkin **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä **Verkkopalvelut**-sivulla. Seuraavassa on kuvattu, miten voit tarkistaa verkkopalvelun käytettävyyden myöhempää käyttöä varten.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Verkkopalvelun saatavuuden tarkistaminen  

1. Kirjoita selaimeen asianmukainen URL-osoite. Seuraavassa taulukossa on kuvattu URL-osoitteiden tyypit, jotka voi antaa erilaisille verkkopalvelutyypeille.  

    > [!div class="mx-tdBreakAll"]
    > |Tyyppi|Syntaksi|Esimerkki|
    > |----------------|------|-------|
    > |SOAP|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData V4|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    Yrityksen nimi -kentässä huomioidaan kirjainkoko.|

2. Tarkista tiedot, jotka näkyvät selaimessa. Varmista, että näet luomasi verkkopalvelun nimen.  

Kun siirryt verkkopalveluun ja haluat kirjoittaa tiedot takaisin kohteeseen [!INCLUDE[d365fin](includes/d365fin_md.md)], yrityksen nimi on määritettävä. Voit määrittää yrityksen esimerkkien tavoin osana URI:a tai vaihtoehtoisesti osana kyselyparametrejä. Esimerkiksi seuraavat URI:t osoittavat samaan OData-verkkopalveluun ja molemmat ovat kelvollisia URI-osoitteita.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Katso myös

[Hallinta](admin-setup-and-administration.md)  
[Kehittäjien Business Central -verkkopalvelut](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[OData -pyyntörajat](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  
