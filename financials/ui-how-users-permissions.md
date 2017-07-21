---
title: "Käyttöoikeuksien määrittäminen ja käyttöoikeusjoukkojen luominen tai muokkaaminen | Microsoft Docs"
description: "Ohjeaiheessa kerrotaan, miten Office 365 -käyttäjät lisätään Financialsiin ja miten käyttöoikeudet ja suojausasetukset määritetään."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 06/27/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 564ef68a1571611efee32db1cf3759cda6a04c80
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-manage-users-and-permissions"></a>Toimintaohje: Käyttäjien ja käyttöoikeuksien hallinta
Käyttäjiä voi lisätä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin sen jälkeen, kun yrityksesi Office 365:n järjestelmänvalvoja on ensin luonut käyttäjät Office 365:n hallintaportaalissa. Lisätietoja on kohdassa [Käyttäjien lisääminen Office 365 for Businessiin](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Kun käyttäjät on luotu Office 365:ssa, heidät voidaan tuoda **Käyttäjät**-ikkunaan **Hae käyttäjät Office 365:stä** -toiminnolla. Käyttäjille määritetään käyttöoikeusjoukot sen mukaan, mitä käyttäjälle on määritetty Office 365:ssä.

Voit sitten määrittää käyttäjille käyttöoikeusjoukkoja, jotka määrittävät, mitä tietokantaobjekteja siten myös mitä käyttöliittymäelementtejä käyttäjät saavat käyttää ja missä yrityksissä niitä saa käyttää.

Oikeussarja on joukko tietyn tietokannan objektien käyttöoikeuksia. Kaikille käyttäjille on määritettävä vähintään yksi käyttöoikeusjoukko, ennen kuin he voivat käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]ia. Tietyt ennalta määritetyt käyttöoikeusryhmät ovat valmiina oletusarvoisesti. Voit käyttää näitä käyttöoikeusjoukkoja oletuksena, muokata käyttöoikeuksien oletusjoukkoja tai luoda lisäkäyttöoikeusjoukkoja.

Voit lisätä käyttäjiä käyttäjäryhmiin. Tämä helpottaa samojen käyttöoikeusjoukkojen määrittämistä useille käyttäjille.

Järjestelmänvalvojat voivat määrittää **Käyttäjäasetukset**-ikkunassa ajanjaksoja, joiden aikana määritetyt käyttäjät voivat tehdä kirjauksia. He voivat myös määrittää, kirjaako järjestelmä ajan, jonka käyttäjät olivat kirjautuneena.

> [!NOTE]  
>   Tämä toiminto edellyttää, että kokemukseksi on valittu Ohjelmistopaketti. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).

## <a name="to-assign-permissions-to-a-user"></a>Käyttöoikeuksien määrittäminen käyttäjälle
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Valitse käyttäjä, jolle haluat määrittää käyttöoikeuden.
Kaikki käyttäjälle jo määritetyt käyttöoikeusjoukot **Käyttöoikeuksien joukot** -tietoruudussa.
3. Avaa **Käyttäjän kortti** -ikkuna valitsemalla **Muokkaa** -toiminto.
4. Täytä **Käyttöoikeuksien joukot** -tietoruudun uudella rivillä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Käyttäjien ryhmittäminen käyttäjäryhmiin
Voit määrittää käyttäjäryhmiä auttamaan hallitsemaan oikeusryhmät käyttäjäryhmille yrityksessä. Voit kopioida toiminnon avulla kaikki käyttöoikeusjoukot aiemmin luodusta käyttäjäryhmästä uuteen käyttäjäryhmään. Käyttäjäryhmän jäseniä ei kopioida.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Vaihtoehtoisesti voit valita **Käyttäjät**-ikkunassa **Käyttäjäryhmät**-toiminnon.
3. Valitse **Käyttäjäryhmät**-ikkunassa ensin kopioitava aiemmin luotu käyttäjäryhmä ja sitten **Kopio käyttäjäryhmä** -toiminto.
4. Määritä **Uuden käyttäjäryhmän koodi** -kentässä uuden käyttäjäryhmän nimi ja valitse sitten **OK**-painike.

    Kopioinnin sijaan voit luoda uuden rivin tyhjälle käyttäjäryhmälle valitsemalla Uusi-toiminnon ja täyttää sen sitten manuaalisesti.
5. Voit lisätä uusia käyttäjiä tai lisäkäyttäjiä valitsemalla **Käyttäjäryhmä**-ikkunassa **Käyttäjäryhmän jäsenet** -toiminnon.
6. Täytä **Käyttäjäryhmän jäsenet** -ikkunan uudella rivillä tarvittavat kentät tekemällä valintoja aiemmin luoduista jäsenistä.
7. Voit lisätä uusia käyttöoikeusjoukkoja tai lisäkäyttöoikeusjoukkoja valitsemalla **Käyttäjäryhmä**-ikkunassa **Käyttäjäryhmän käyttöoikeuksien joukot** -toiminnon.
8. Täytä **Käyttäjäryhmän käyttöoikeuksien joukot** -ikkunan uudella rivillä tarvittavat kentät tekemällä valintoja aiemmin luoduista käyttöoikeuksien joukoista.

## <a name="to-create-or-modify-permission-sets"></a>Käyttöoikeuksien joukkojen luominen tai muokkaaminen
Jos [!INCLUDE[d365fin](includes/d365fin_md.md)]iin sisältyvät oletuskäyttöoikeusjoukot eivät riitä tai eivät sovi organisaatiollesi, voit luoda uusia käyttöoikeusjoukkoja. Ja jos käyttöoikeusjoukon määrittävät yksittäisen objektin käyttöoikeudet eivät ole riittävät, voit muokata käyttöoikeusjoukkoa. Voit luoda käyttöoikeusjoukon manuaalisesti. Vaihtoehtoisesti voit käyttää tallennustoimintoa, joka tallentaa toimesi skenaariossa siirtyessäsi ja muodostaa sitten tarvittavan käyttöoikeusjoukon.

### <a name="to-create-or-modify-permission-sets-manually"></a>Käyttöoikeuksien joukkojen luominen tai muokkaaminen manuaalisesti
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Valitse **Käyttäjät**-ikkunassa **Käyttöoikeuksien joukot** -toiminto.
3. Valitse **Käyttöoikeuksien joukot** -ikkunassa **Uusi**-toiminto.
4. Täytä tarvittaessa uuden rivin kentät.
5. Valitse **Käyttöoikeudet**-toiminto.
6. Täytä **Käyttöoikeudet**-ikkunassa tarvittavat otsikon kentät.
7. Täytä uudella rivillä viisi erilaista seuraavassa taulukossa kuvattua käyttöoikeustyyppiä.

    |Asetus|Kuvaus|
    |------|-----------|
    |Tyhjä|Määrittää, ettei käyttöoikeustyyppiä myönnetä objektille.|
    |**Kyllä**|Määrittää, että myönnetään käyttöoikeustyyppi, jolla objektia voi käyttää suoraan.|
    |**Epäsuora**|Määrittää, että myönnetään käyttöoikeustyyppi, jolla objektia voi käyttää epäsuorasti.|

    Taulukon epäsuorat käyttöoikeudet tarkoittavat, ettet voi avata ja lukea taulukkoa mutta voit tarkastella taulukon tietoja toisen sellaisen objektin kautta, jonka suora käyttöoikeus sinulla on. Tällainen objekti voi olla esimerkiksi sivu. Lisätietoja on tämän ohjeen kohdassa Esimerkki - epäsuorat käyttöoikeudet.

8. Anna **Suojaussuodatin**-kentässä suodatin, jota haluat käyttää käyttöoikeudessa, valitsemalla kenttä, jonka käyttöä haluat rajoittaa käyttäjältä.

    Jos haluat esimerkiksi luoda suojaussuodattimen siten, että käyttäjä voi tarkastella vain tietyn myyjäkoodin myyntiä, valitse kentän numero **Myyjäkoodi**-kentässä. Anna sitten **Kenttäsuodatin**-kentässä arvo, jolla haluat rajoittaa käyttöä. Jos haluat esimerkiksi rajoittaa käyttäjän pääsyn vain Anne Hellung-Larsenin myyntiin, anna AHL.
9. Lisää käyttöoikeuksia käyttöoikeusjoukon lisäobjekteihin toistamalla vaiheet 7 ja 8.

### <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Käyttöoikeusjoukkojen luominen tai muokkaaminen toimia tallentamalla
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Valitse **Käyttäjät**-ikkunassa **Käyttöoikeuksien joukot** -toiminto.
3. Valitse **Käyttöoikeuksien joukot** -ikkunassa **Uusi**-toiminto.
4. Täytä tarvittaessa uuden rivin kentät.
5. Valitse **Käyttöoikeudet**-toiminto.
6. Valitse **Käyttöoikeudet**-ikkunassa **Aloita**-toiminto.

    Tallennusprosessi aloittaa kaikkien käyttöliittymässä tekemiesi toimien tallentamisen.
7. Siirry niihin [!INCLUDE[d365fin](includes/d365fin_md.md)]in ikkunoihin ja toimintoihin, joita haluat tämän käyttöoikeusjoukon käyttäjien käyttävän. Sinun on tehtävä ne tehtävät, joille haluat tallentaa käyttöoikeudet.
8. Kun tallennus on valmis, palaa **Käyttöoikeudet**-ikkunaan ja valitse sitten **Lopeta**-toiminto.
9. Lisää tallennetut käyttöoikeudet uuteen käyttöoikeusjoukkoon valitsemalla **Kyllä**.
10. Määritä jokaiselle tallennetun luettelon objektille, saavatko käyttäjät lisätä, muokata tai poistaa tietueita tallennetuissa taulukoissa. Katso Käyttöoikeuksien joukkojen luominen tai muokkaaminen manuaalisesti -osan vaihe 7.

### <a name="example---indirect-permission"></a>Esimerkki - epäsuora käyttöoikeus
Voit määrittää epäsuoria käyttöoikeuksia, jos haluat käyttää objektia vain toisen objektin kautta.
Käyttäjällä voi olla esimerkiksi oikeus suorittaa codeunit 80, **Myynti kirjattu**. Codeunit **Myynti kirjattu** suorittaa useita tehtäviä, myös muokkaa taulukkoa 37, **Ostorivi**. Kun käyttäjä kirjaa myyntiasiakirjan, codeunitin **Myynti kirjattu**, [!INCLUDE[d365fin](includes/d365fin_md.md)] tarkistaa, onko käyttäjällä oikeus muokata **Ostorivi**-taulukkoa. Jos ei, codeunit ei voi suorittaa tehtäviä ja käyttäjä saa virhesanoman. Tällöin koodiyksikön suorittaminen onnistuu.

Käyttäjällä ei kuitenkaan tarvitse olla **Ostorivi**-taulukon täysiä käyttöoikeuksia codeunitin suorittamiseksi. Jos käyttäjällä on **Ostorivi**-taulukon epäsuorat käyttöoikeudet, codeunitin **Myynti kirjattu** suorittaminen onnistuu. Kun käyttäjällä on epäsuorat oikeudet, kyseinen käyttäjä voi muokata vain **Ostorivi**-taulukkoa suorittamalla codeunitin **Myynti kirjattu** tai toisen objektin, jolla on **Ostorivi**-taulukon muokkausoikeudet. Käyttäjä voi muokata **Ostorivi**-taulukkoa vain silloin, kun se tapahtuu tuetulla sovellusalueella. Käyttäjä ei voi suorittaa toimintoa vahingossa tai tahallaan muita menetelmiä käyttäen.

## <a name="to-set-up-user-time-constraints"></a>Määritä käyttäjän aikarajoitukset
Järjestelmänvalvojat voivat määrittää ajanjaksoja, joiden aikana määritetyt käyttäjät voivat tehdä kirjauksia. He voivat myös määrittää, kirjaako järjestelmä ajan, jonka käyttäjät olivat kirjautuneena. Järjestelmänvalvojat voivat myös määrittää käyttäjille vastuupaikkoja.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "") -kuvake, kirjoitta **Resurssienhallinnan asetukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse avautuvassa **Käyttäjäasetukset**-ikkunassa **Uusi**-toiminto.
3. Anna **Käyttäjätunnus**-kentässä käyttäjän tunnus tai valitse kenttä, jos haluat nähdä kaikki järjestelmässä tällä hetkellä olevat Windows-käyttäjät.
4. Täytä tarvittavat kentät.

## <a name="see-also"></a>Katso myös
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Tervetuloa [!INCLUDE[d365fin](includes/d365fin_md.md)]iin!](index.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

