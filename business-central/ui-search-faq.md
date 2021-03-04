---
title: Kerro, mitä haluat tehdä -toimintoon liittyviä usein kysyttyjä kysymyksiä | Microsoft Docs
description: Tässä artikkelissa on vastauksia Kerro, mitä haluat tehdä -toimintoon liittyviin usein kysyttyihin kysymyksiin, joita kumppanit ja asiakkaat esittävät.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 7b880ef5cb49a02dcbb3973f87bc64eae48b2b3a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760240"
---
# <a name="tell-me-faq"></a>Kerro, mitä haluat tehdä -toiminnon usein kysytyt kysymykset
Tässä ohjeaiheessa vastataan kokeneiden käyttäjien Kerro, mitä haluat tehdä -ominaisuutta koskeviin usein kysyttyihin kysymyksiin.

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Löytyvätkö kaikki nykyisen sivun toiminnot Kerro, mitä haluat tehdä -toiminnon avulla?
Ei. Osissa, kuten myyntirivien osassa tai tietoruuduissa, olevat toiminnot eivät näy Kerro, mitä haluat tehdä -toiminnon avulla.

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>Suodatetaanko Kerro, mitä haluat tehdä -toiminnon tulokset käyttöoikeuksien mukaan?
Jos käyttäjällä ei ole AccessByPermissions-ominaisuutta, toimintoja ei näytetä. Sivut ja raportit näkyvät tuloksissa, mutta niiden käyttäminen edellyttää, että käyttäjällä on tarvittavat käyttöoikeudet. Jos käyttäjällä ei ole objektin katseluoikeuksia, näyttöön tulee asiasta kertova sanoma.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>Sisältääkö Kerro, mitä haluat tehdä -ikkuna omat mukautukset vai asennetut kolmannen osapuolen laajennukset?
Kerro, mitä haluat tehdä -toiminto kerää laajennusten toiminnot, sivut ja raportit, mutta mukautettua ohjeen dokumentaatiota ei kerätä. Teknisiä lisätietoja siitä, miten mukautetut sivut ja raportit voidaan tehdä helpommin löydettäviksi, on kohdassa [Sivujen ja raporttien lisääminen hakuun](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Miksi tämä on erilainen kuin aiempi sivuhaku?
Sivuhaku on kehittynyt Kerro, mitä haluat tehdä -toiminnoksi, jonka avulla työskentely on nopeampaa. Sivuhaku auttoi vain sivuihin ja raportteihin siirtymisessä. Teknisesti ottaen Kerro, mitä haluat tehdä ei enää perustu MenuSuite-käsitteeseen.

### <a name="i-use-on-premises-prod_short-does-that-include-tell-me"></a>Käytän paikallista [!INCLUDE[prod_short](includes/prod_short.md)] -sovellusta. Sisältääkö se Kerro, mitä haluat tehdä -toiminnon?
Voit käyttää Kerro, mitä haluat tehdä -toimintoa paikallisesti verkkoasiakasohjelmassa, kun haluat etsiä toimintoja, sivuja ja raportteja. Ohjeistusta tai sovelluksia ja konsultointipalveluja ei kuitenkaan voi etsiä sen avulla AppSourcessa.

### <a name="is-tell-me-available-for-all-form-factors"></a>Onko Kerro, mitä haluat tehdä -toiminto käytettävissä kaikissa laitemuodoissa?
Kerro, mitä haluat tehdä -toiminto on käytettävissä vain WWW-asiakasohjelmassa ja Windows-työpöytäsovelluksessa.

### <a name="are-the-documentation-results-available-in-any-language"></a>Ovatko dokumentaation tulokset käytettävssä kaikilla kielillä?
Tämän ohjeen artikkelit näkyvät **Omat asetukset** -kohdassa määritetyllä kielellä, jos ohje on käännetty kyseiselle kielelle.

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a>Miksi hakutulosten kirjanmerkkikuvaketta ei näy?
Kirjanmerkkikuvake ei näy Kerro, mitä haluat tehdä -ikkunassa, kun mukautus on poistettu käytöstä käyttäjäroolissa.


## <a name="see-also"></a>Katso myös  
[Luettelonäkymien tallentaminen ja mukauttaminen](ui-views.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Sivujen etsiminen roolienhallinnan avulla](ui-role-explorer.md)  
[Sivun tai raportin kirjanmerkin luominen roolikeskuksessa](ui-bookmarks.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]