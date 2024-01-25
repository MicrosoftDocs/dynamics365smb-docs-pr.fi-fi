---
title: Kerro-toiminnon usein kysytyt kysymykset
description: 'Tässä artikkelissa on vastauksia Kerro, mitä haluat tehdä -toimintoon liittyviin usein kysyttyihin kysymyksiin, joita kumppanit ja asiakkaat esittävät.'
author: brentholtorf
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'find, search, Tell Me'
ms.search.form: TellMe
ms.date: 09/21/2023
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---
# <a name="tell-me-faq"></a>Kerro, mitä haluat tehdä -toiminnon usein kysytyt kysymykset

Tässä artikkelissa vastataan kokeneiden käyttäjien Kerro, mitä haluat tehdä -ominaisuutta koskeviin usein kysyttyihin kysymyksiin.

## <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Löytyvätkö kaikki nykyisen sivun toiminnot Kerro, mitä haluat tehdä -toiminnon avulla?

Ei. Osissa, kuten myyntirivien osassa tai tietoruuduissa, olevat toiminnot eivät näy Kerro, mitä haluat tehdä -toiminnon avulla.

## <a name="can-i-search-for-a-specific-record"></a>Voinko hakea tiettyä tietuetta?

Kyllä. Jos haluat esimerkiksi löytää nopeasti myyntitilauksen, syötä sen tunnus ja valitse **Hae yrityksen tiedoista** -toiminto. Jos tiedät vain asiakkaan nimen, syötä se. Kerro, mitä haluat tehdä -toiminto järjestää tulokset tyypeittäin, jotta löydät tilauksen Myyntitilaukset-kategoriasta.

## <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>Suodatetaanko Kerro, mitä haluat tehdä -toiminnon tulokset käyttöoikeuksien mukaan?

Jos käyttäjällä ei ole AccessByPermissions-ominaisuutta, toimintoja ei näytetä. Sivut ja raportit näkyvät tuloksissa, mutta niiden käyttäminen edellyttää, että käyttäjällä on tarvittavat käyttöoikeudet. Jos käyttäjällä ei ole objektin katseluoikeuksia, näyttöön tulee asiasta kertova sanoma.

## <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>Sisältääkö Kerro, mitä haluat tehdä -ikkuna omat mukautukset vai asennetut kolmannen osapuolen laajennukset?

Kerro, mitä haluat tehdä -toiminto kerää laajennusten toiminnot, sivut ja raportit. Teknisiä lisätietoja siitä, miten mukautetut sivut ja raportit voidaan tehdä helpommin löydettäviksi, on kohdassa [Sivujen ja raporttien lisääminen hakuun](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

## <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Miksi tämä on erilainen kuin aiempi sivuhaku?

Sivuhaku on kehittynyt Kerro, mitä haluat tehdä -toiminnoksi, jonka avulla työskentely on nopeampaa. Sivuhaku auttoi vain sivuihin ja raportteihin siirtymisessä. Teknisesti ottaen Kerro, mitä haluat tehdä ei enää perustu MenuSuite-käsitteeseen.

## <a name="i-use-on-premises--does-that-include-tell-me"></a>Käytän paikallista [!INCLUDE[prod_short](includes/prod_short.md)] -sovellusta. Sisältääkö se Kerro, mitä haluat tehdä -toiminnon?

Voit käyttää Kerro, mitä haluat tehdä -toimintoa paikallisesti verkkoasiakasohjelmassa, kun haluat etsiä toimintoja, sivuja ja raportteja. Sovelluksia ja konsultointipalveluja ei kuitenkaan voi etsiä sen avulla AppSourcessa.

## <a name="is-tell-me-available-for-all-form-factors"></a>Onko Kerro, mitä haluat tehdä -toiminto käytettävissä kaikissa laitemuodoissa?

Kyllä. Se otettiin käyttöön puhelimissa ja tableteissa Business Central 2023 -julkaisuaallossa 2, mutta se on otettava käyttöön [ominaisuuksien hallinnassa](/dynamics365/business-central/dev-itpro/administration/feature-management) käyttämällä **Ominaisuus: Etsi sivuja ja tietoja mobiilisovelluksella** -kytkintä. 

<!-- removed in v20 because of Help pane
### <a name="are-the-documentation-results-available-in-any-language"></a>Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

## <a name="does-tell-me-give-me-help-on-how-to-use-pages-reports-and-other-things"></a>Antaako Kerro, mitä haluat tehdä -toiminto ohjeita sivujen, raporttien ja muiden asioiden käyttöön?

Ei, mutta saat nämä tiedot helposti ohjeruudusta. Valitse vain **Hae ohjeesta** -toiminto **Kerro, mitä haluat tehdä** -sivulla tai valitse näppäimistöllä <kbd>Ctrl</kbd>+<kbd>F1</kbd>. Lisätietoja ohjeruudusta on [ohjeruudussa](product-help-and-support.md#help-pane).

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a>Miksi hakutulosten kirjanmerkkikuvaketta ei näy?

Kirjanmerkkikuvake ei näy Kerro, mitä haluat tehdä -ikkunassa, kun mukautus on poistettu käytöstä käyttäjäroolissa.

## <a name="see-also"></a>Katso myös

[Luettelonäkymien tallentaminen ja mukauttaminen](ui-views.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Sivujen etsiminen roolienhallinnan avulla](ui-role-explorer.md)  
[Sivun tai raportin kirjanmerkin luominen roolikeskuksessa](ui-bookmarks.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
