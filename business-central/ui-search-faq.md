---
title: Kerro-toiminnon usein kysytyt kysymykset
description: 'Tässä artikkelissa on vastauksia Kerro, mitä haluat tehdä -toimintoon liittyviin usein kysyttyihin kysymyksiin, joita kumppanit ja asiakkaat esittävät.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.search.form: TellMe
ms.date: 05/23/2022
ms.author: bholtorf
---
# <a name="tell-me-faq" />Kerro, mitä haluat tehdä -toiminnon usein kysytyt kysymykset
Tässä artikkelissa vastataan kokeneiden käyttäjien Kerro, mitä haluat tehdä -ominaisuutta koskeviin usein kysyttyihin kysymyksiin.

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me" />Löytyvätkö kaikki nykyisen sivun toiminnot Kerro, mitä haluat tehdä -toiminnon avulla?

Ei. Osissa, kuten myyntirivien osassa tai tietoruuduissa, olevat toiminnot eivät näy Kerro, mitä haluat tehdä -toiminnon avulla.

### <a name="are-the-results-in-tell-me-filtered-by-permissions" />Suodatetaanko Kerro, mitä haluat tehdä -toiminnon tulokset käyttöoikeuksien mukaan?

Jos käyttäjällä ei ole AccessByPermissions-ominaisuutta, toimintoja ei näytetä. Sivut ja raportit näkyvät tuloksissa, mutta niiden käyttäminen edellyttää, että käyttäjällä on tarvittavat käyttöoikeudet. Jos käyttäjällä ei ole objektin katseluoikeuksia, näyttöön tulee asiasta kertova sanoma.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions" />Sisältääkö Kerro, mitä haluat tehdä -ikkuna omat mukautukset vai asennetut kolmannen osapuolen laajennukset?

Kerro, mitä haluat tehdä -toiminto kerää laajennusten toiminnot, sivut ja raportit. Teknisiä lisätietoja siitä, miten mukautetut sivut ja raportit voidaan tehdä helpommin löydettäviksi, on kohdassa [Sivujen ja raporttien lisääminen hakuun](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search" />Miksi tämä on erilainen kuin aiempi sivuhaku?

Sivuhaku on kehittynyt Kerro, mitä haluat tehdä -toiminnoksi, jonka avulla työskentely on nopeampaa. Sivuhaku auttoi vain sivuihin ja raportteihin siirtymisessä. Teknisesti ottaen Kerro, mitä haluat tehdä ei enää perustu MenuSuite-käsitteeseen.

### <a name="i-use-on-premises--does-that-include-tell-me" />Käytän paikallista [!INCLUDE[prod_short](includes/prod_short.md)] -sovellusta. Sisältääkö se Kerro, mitä haluat tehdä -toiminnon?

Voit käyttää Kerro, mitä haluat tehdä -toimintoa paikallisesti verkkoasiakasohjelmassa, kun haluat etsiä toimintoja, sivuja ja raportteja. Sovelluksia ja konsultointipalveluja ei kuitenkaan voi etsiä sen avulla AppSourcessa.

### <a name="is-tell-me-available-for-all-form-factors" />Onko Kerro, mitä haluat tehdä -toiminto käytettävissä kaikissa laitemuodoissa?

Kerro, mitä haluat tehdä -toiminto on käytettävissä vain WWW-asiakasohjelmassa ja Windows-työpöytäsovelluksessa.

<!-- removed in v20 because of Help pane
### <a name="are-the-documentation-results-available-in-any-language" />Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

### <a name="does-tell-me-give-me-help-on-how-to-use-pages-reports-and-other-things" />Antaako Kerro, mitä haluat tehdä -toiminto ohjeita sivujen, raporttien ja muiden asioiden käyttöön?

Ei, mutta saat nämä tiedot helposti ohjeruudusta. Valitse **Ohje**-valikkokohdetta (kysymysmerkki oikeassa yläkulmassa) tai käytä näppäinyhdistelmää <kbd>Ctrl</kbd>+<kbd>F1</kbd>. Lisätietoja: [Ohjeruutu](product-help-and-support.md#help-pane).

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results" />Miksi hakutulosten kirjanmerkkikuvaketta ei näy?

Kirjanmerkkikuvake ei näy Kerro, mitä haluat tehdä -ikkunassa, kun mukautus on poistettu käytöstä käyttäjäroolissa.


## <a name="see-also" />Katso myös
[Luettelonäkymien tallentaminen ja mukauttaminen](ui-views.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Sivujen etsiminen roolienhallinnan avulla](ui-role-explorer.md)  
[Sivun tai raportin kirjanmerkin luominen roolikeskuksessa](ui-bookmarks.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
