---
title: Objektien näyttäminen verkkopalveluina | Microsoft Docs
description: Julkaise objektit verkkopalveluina, jolloin niitä voi käyttää heti Business Central -ratkaisussa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 05/19/2020
ms.author: edupont
ms.openlocfilehash: 230f3a7fc11e19813d77da2ff15388433642c744
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697645"
---
# <a name="publish-a-web-service"></a>Verkkopalvelun julkaiseminen

Verkkopalvelut ovat kevyt tapa tuoda sovelluksen toiminnallisuus useiden ulkoisten järjestelmien ja käyttäjien saataville. [!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää useita objekteja, jotka näytetään oletusarvoisesti verkkopalveluina, koska ne on integroitu muiden Microsoftin palvelujen kanssa, mutta voit lisätä myös muita verkkopalveluja.  

Verkkopalvelu määritetään [!INCLUDE[d365fin](includes/d365fin_md.md)] -asiakasohjelmassa. Sinun tulee sitten julkaista verkkopalvelu, jotta se on saatavilla huoltopyyntöjen käytettäväksi verkon välityksellä. Käyttäjät löytävät verkkopalvelut osoittamalla selainta palvelinsijainnissa ja pyytämällä luettelon käytettävissä olevista palveluista. Kun julkaiset verkkopalvelun, se tulee välittömästi käyttöön todennetuille käyttäjille verkon kautta. Kaikki valtuutetut käyttäjät voivat käyttää verkkopalveluiden metatietoja, mutta vain käyttäjät, joilla on riittävät oikeudet, voivat käyttää varsinaisia tietoja.

## <a name="creating-and-publishing-a-web-service"></a>Verkkopalvelun luominen ja julkaiseminen

Seuraavassa kerrotaan, kuinka voit luoda ja julkaista verkkopalvelun.  

<!--
    You can also create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] instead. Choose one of the following methods:

      - Use the **Create Data Set** action on the **Web Services** page
      - Use the **Set Up Reporting** Assisted Setup guide
      - Choose the **Edit in Excel** action in any lists
    -->

### <a name="to-create-and-publish-a-web-service"></a>Verkkopalvelun luominen ja julkaiseminen  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Verkkopalvelut** ja valitse sitten liittyvä linkki.  
2. Valitse **Verkkopalvelut**-sivulla **Uusi**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Koodiyksikkö** ja **Sivu** ovat kelvollisia SOAP-verkkopalveluja. **Sivu** ja **Kysely** ovat kelvollisia OData-verkkopalvelutyyppejä.  
    > Jos tietokanta lisäksi sisältää useita yrityksiä, voit valita yhdelle yritykselle kuuluvan objektitunnuksen.  
    > Palvelunimi näkyy verkkopalvelun käyttäjille, ja sen perusteella tunnistetaan ja erotellaan verkkopalvelut, joten nimen on oltava merkityksellinen.

3. Valitse valintaruutu **Julkaistu**-sarakkeessa.  

Kun julkaiset verkkopalvelun, **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä näkyvät verkkopalvelua varten luodut URL-osoitteet. Voit testata verkkopalvelua heti valitsemalla linkit **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä. Vaihtoehtoisesti voit kopioida kentän arvon ja tallentaa sen myöhempää käyttöä varten.  

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

Kun siirryt verkkopalveluun ja haluat kirjoittaa tiedot takaisin kohteeseen [!INCLUDE[d365fin](includes/d365fin_md.md)], yrityksen nimi on määritettävä. Voit määrittää yrityksen esimerkkien tavoin osana URI:a tai osana kyselyparametrejä. Esimerkiksi seuraavat URI:t osoittavat samaan OData-verkkopalveluun ja molemmat ovat kelvollisia URI-osoitteita.  

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
