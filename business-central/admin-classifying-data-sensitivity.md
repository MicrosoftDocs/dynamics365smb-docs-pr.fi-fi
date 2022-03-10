---
title: Tietojen luottamuksellisuuden luokitteleminen
description: Tallennettavien henkilöitä koskevien tietojen tyyppi on määritettävä, jotta voit vastata tietojen kohteiden pyyntöihin.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.search.form: 1752
ms.date: 06/14/2021
ms.openlocfilehash: 4ec4e6cd24c620829b35b7e3e25a27d4f127e045
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8136424"
---
# <a name="classifying-data-sensitivity-fields"></a>Tietojen luottamuksellisuuskenttien luokitteleminen
Microsoft-kumppani voi luokitella luottamuksellisia tai henkilökohtaisia tietoja sisältävät kentät määrittämällä kentille ominaisuuden ```DataClassification```. Tämä edellyttää tietokantataulujen käyttämistä joko kehitysympäristössä tai suorittamalla Windows PowerShell -komentosarja. Lisätietoja on kohdassa [Tietojen luokitteleminen](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data).  

Asiakkaana voit lisätä luokittelulle toisen tason, kun määrität vakiokentille ja mukautetuille kentille tietojen luottamuksellisuuden tasot. Tietojen luottamuksellisuuden luokitteleminen auttaa varmistamaan, että tiedät henkilökohtaisten tietojen tallennussijainnin järjestelmässä. Sen avulla on myös helppo vastata tietojen kohteiden pyyntöihin. Yhteyshenkilö tai asiakas voi esimerkiksi pyytää henkilökohtaisten tietojen viemistä. Lisätietoja on kohdassa [Henkilökohtaisia tietoja koskeviin pyyntöihin vastaaminen](admin-responding-to-requests-about-personal-data.md).

> [!Important]
> Microsoft tarjoaa tämän tietojen luottamuksellisuuden luokittelutoiminnon lisäämään mukavuutta. Käyttäjä on vastuussa tietojen asianmukaisesta luokittelemisesta ja yritystä koskevien lakien ja asetusten noudattamisesta. Microsoft ei ota vastuuta mistään tietojesi luokitteluun liittyvistä vaatimuksista.  

Seuraavassa taulukossa kerrotaan, millaisia tietojen luottamuksellisuustasoja voit määrittää.

|Luottamuksellisuus|Description|
|----|----|
|Luottamuksellinen | Tietojen kohteen rotua tai etnistä alkuperää, poliittisia mielipiteitä, uskonnollista vakaumusta, ammattiliitoissa toimimista, fyysistä ja psyykkistä terveyttä, seksuaalisuutta ja rikoksia koskevat tiedot. |
|Henkilökohtainen | Tiedot, joiden avulla tietojen kohde voidaan tunnistaa joko suoraan tai yhdessä muiden tietojen kanssa.|
|Luottamuksellinen | Kirjanpidossa tai muissa liiketoimintatarkoituksissa käytettävät liiketoimintatiedot, joita ei haluta paljastaa muille yksiköille. Näitä tietoja voivat olla esimerkiksi kirjanpidon tapahtumat.|
|Normaali | Yleistiedot, jotka eivät kuulu muihin luokkiin.|

## <a name="how-do-i-classify-my-data"></a>Miten tiedot luokitellaan?
Jos kenttiä on paljon, niiden tietojen luottamuksellisuuden luokitteleminen yksitellen kestäisi kauan. Voit nopeuttaa prosessia käyttämällä työkaluja, jotka mahdollistavat kenttien luottamuksellisuuden joukkoluokittelun sekä tiettyjen kenttien luokitteluiden hienosäädön. Työkalut löytyvät tietojen luokittelun työkirjasta. Se sijaitsee käyttäjien, käyttäjäryhmien ja käyttöoikeuksien hallinnan roolikeskuksessa. Tätä työkirjaa voi käyttää vain järjestelmänvalvoja.

> [!Important]
> Kun avaat tietojen luokittelun työkirjan ensimmäisen kerran, se on tyhjä. Voit luoda kenttäluettelon suorittamalla tietojen luokittelun oppaan. Aloita opas valitsemalla **Määritä tietojen luokitukset** -toiminto.

Tietojen luokittelun työkirjan avulla voit tehdä esimerkiksi seuraavat toiminnot:  

* Vie kentät tietojen luokittelun oppaan avulla Excel-työkirjaan, jossa voit joukkoluokitella ne. Ecxel-työkirjan käyttäminen on erityisen hyödyllistä, jos teet yhteistyötä Microsoft-kumppanin kanssa. Kun työkirja on päivitetty, voit tuoda luokittelut ja käyttää niitä oppaan avulla. Voit käyttää opasta myös kenttien manuaalisessa luokittelussa.  
* Valitse kenttä ja suodata luettelo, jotta voit etsiä samanlaisia kenttiä, jotka todennäköisesti kuuluvat samaan luokitteluun kuin kenttä, johon haku perustuu.  
* Tutki kenttää sen sisällön avulla.  

> [!Tip]
> Olemme määrittäneet esimerkkitietojen luottamuksellisuuden luokittelut Cronus-esittely-yrityksen taulukoille ja kentille. Voit käyttää näitä luokitteluita inspiraation lähteenä, kun luokittelet omia taulukoita ja kenttiä.

## <a name="see-also"></a>Katso myös

[Tietojen luokitteleminen](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]