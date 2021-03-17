---
title: Lisätoiminnot näyttävän tai piilottavan käyttäjäkokemuksen valitseminen | Microsoft Docs
description: Tietoja siitä, miten Essential- ja Basic-käyttäjäkokemus tarkoittaa käyttöliittymässä, sovellusalueilla ja yrityksessä.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e53ef4e33d489de7ff92e537b01b8563e62ba77
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379631"
---
# <a name="change-which-features-are-displayed"></a>Näytettävien ominaisuuksien muuttaminen
[!INCLUDE[prod_short](includes/prod_short.md)] on suunniteltu auttamaan sinua pyörittämään yritystäsi sen koosta ja monimutkaisuudesta riippumatta. Tuotteen ytimessä on olennaisia ominaisuuksia, kuten talousraportointi, myynti, osto ja varastonhallinta. Kun liiketoiminnan monimutkaisuus kasvaa, voit ottaa käyttöön esimerkiksi tuotannon ja huollon hallinnan toiminnot.

Voit määrittää tuotteen monimutkaisuustason ja siten sen, mihin ominaisuuksiin yrityksen käyttäjät pääsevät muuttamalla **Kokemus**-asetuksia **Yrityksen tiedot** -sivulla. Huomaa, että kokemusasetusta voidaan muuttaa myös lisäämällä tiettyjä laajennuksia AppSourcesta. Lisätietoja on kohdassa [[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md).

Seuraavassa taulukossa on luettelo nyt käytettävissä olevista kokemuksista.

| Kokemus | Vaikutus käyttöliittymään |
| --- | --- |
| **Essential** |Näyttää kaikkien yleisten liiketoimintatoimintojen kaikki toiminnot ja kentät.|
| **Premium** |Näyttää kaikkien liiketoimintojen toiminnot ja kentät myös valmistukselle ja huoltohallinnolle.|

[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman valittavissa olevat kokemukset, jotka vastaavat tuotteelle määritettyjä ratkaisulisenssejä, nimeltään suunnitelmat. Lisätietoja Essential- ja Premium-palvelupaketeista on [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) -kohdassa Microsoft Dynamics 365:n markkinointisivustossa. Katso myös [[!INCLUDE[prod_short](includes/prod_short.md)]in käyttöoikeusopas](https://go.microsoft.com/fwlink/?linkid=2068931) (edellyttää CustomerSourcen tai PartnerSourcen käyttöoikeutta).

> [!IMPORTANT]  
> Kaikki ratkaisun tavalliset käyttäjät täytyy liittää samaan suunnitelmaan (Essential tai Premium) ennen kyseisen käyttökokemuksen valitsemista yritykselle. Näin ollen yksi käyttäjä ei voi käyttää Premium-ominaisuuksia, jos vähintään yksi käyttäjä voi käyttää vain Essential-ominaisuuksia. Tämä ei koske erikoiskäyttäjiä, joiden tyyppi on ryhmän jäsen, sisäinen järjestelmänvalvoja, ulkoinen kirjanpitäjä tai delegoitu järjestelmänvalvoja, joille voidaan määrittää eri suunnitelma kuin muille ratkaisun käyttäjille.<br /><br /> Vain Evaluation- tai Premium-tyyppiset käyttäjät voivat muuttaa **Kokemus**-kentän arvoa Essentialista Premiumiin.

Ennen kuin määrität yrityksen kokemusasetukset, voit määrittää käyttäjien käyttöoikeuden tiettyihin toimintoihin ja sivuihin määrittämällä käyttöoikeusjoukkoja. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).

**Kokemus**-asetus koskee yrityksen kaikkia käyttäjiä, mutta jokainen käyttäjä voi mukauttaa omia kokemuksiaan muuttamalla sivun asettelua ja sisältöä. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Premium-ominaisuuksien käyttöönotto suunnitelman päivittämisen jälkeen
Käyttäjille määritetään suunnitelmat Microsoft 365 -hallintakeskuksessa samassa yhteydessä kuin Business Central -käyttäjiä määritetään. Lisätietoja on kohdassa [Käyttäjien lisääminen ja käyttöoikeuksien määrittäminen samaan aikaan](/microsoft-365/admin/add-users/add-users?view=o365-worldwide&preserve-view=true).

### <a name="to-update-plan-changes-in-users-groups"></a>Suunnitelman muutoksien päivittäminen käyttäjäryhmissä
Kun olet tehnyt muutoksia käyttäjien suunnitelmiin Microsoft 365 -hallintakeskuksessa (kuten määrittänyt enemmän käyttäjiä Premium-suunnitelmaan), sinun tulee tehdä muutoksia myös [!INCLUDE[prod_short](includes/prod_short.md)]:ssa.

1. Kirjaudu sisään järjestelmänvalvojana.
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
3. Vaihtoehtoisesti voit valita **Käyttäjät**-sivulla **Päivitä kaikki käyttäjäryhmät** -toiminnon.

Käyttäjien suunnitelmien ja heidän määriteltyjen käyttäjäryhmiensä uudet tiedot päivitetään nyt suunnitelman muutoksien mukaisesti.

### <a name="to-select-the-premium-experience"></a>Premium-käyttäjäkokemuksen valinta
Voit nyt siirtyä valitsemaan uuden käyttökokemuksen.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yrityksen tiedot** ja valitse sitten liittyvä linkki.
2. Valitse **Yrityksen tiedot** -sivun **Käyttäjäkokemus**-pikavälilehden **Kokemus**-kentässä Premium.

## <a name="help-assumes-premium-experience"></a>Ohje käsittelee Premium-käyttäjäkokemusta
[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen käyttäjän dokumentaation kaikkien toimintojen kuvauksissa käsitellään **Premium**-käyttökokemusta. Tämä tarkoittaa sitä, että kuvaukset sisältävät käyttöliittymän kaikki elementit.

## <a name="see-also"></a>Katso myös
[Työtilan mukauttaminen](ui-personalization-user.md)  
[Business Central -sovelluksen mukauttaminen](ui-customizing-overview.md)  
[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[Uusien yritysten luominen](about-new-company.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen käyttöoikeusopas](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]