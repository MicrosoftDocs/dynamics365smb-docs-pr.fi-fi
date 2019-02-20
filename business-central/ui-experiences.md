---
title: "Lisätoiminnot näyttävän tai piilottavan käyttäjäkokemuksen valitseminen | Microsoft Docs"
description: "Tietoja siitä, miten Essential- ja Basic-käyttäjäkokemus tarkoittaa käyttöliittymässä, sovellusalueilla ja yrityksessä."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 02/04/2019
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ce612d546349d05883016646fe14a35553c2f55a
ms.openlocfilehash: 3317df5f54a359e5b143d5b288a378a350d49440
ms.contentlocale: fi-fi
ms.lasthandoff: 02/04/2019

---
# <a name="changing-which-features-are-displayed"></a>Näytettävien ominaisuuksien muuttaminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] on suunniteltu auttamaan liiketoiminnan käytännön asioissa toimialasta riippumatta. [!INCLUDE[d365fin](includes/d365fin_md.md)]in ydintä ovat talousraportointi sekä myynti- ja ostoprosessit. Voit lisätä siihen kokemuksia liiketoiminnan tarpeiden mukaan lisäämällä laajennuksia AppSourcesta tai muuttamalla yrityksen Kokemus-asetusta. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md) tai alla olevassa Toimintojen näyttäminen tai piilottaminen käyttäjäkokemuksen valinnan avulla -osassa.

## <a name="choosing-a-user-experience-to-show-or-hide-features"></a>Ominaisuuksien näyttäminen tai piilottaminen valitsemalla käyttäjäkokemus
Käyttäjäkokemus määrittää, kuinka suurta osaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in perustoiminnoista voit työtovereittesi kanssa käyttää. Voit valita yrityksen käyttökokemuksen **Yrityksen tiedot** -sivun **Kokemus**-kentässä.

> [!NOTE]  
> Tämä asetus koskee kaikki yrityksen käyttäjiä. Käyttäjät voivat lisäksi mukauttaa omaa kokemustaan muuttamalla sivun asettelua ja sisältöä. Lisätietoja on kohdassa [Työtilan ja sivujen mukauttaminen](ui-personalization-user.md).  

Seuraavassa taulukossa on luettelo nyt käytettävissä olevista kokemuksista.

| Kokemus | Vaikutus käyttöliittymään |
| --- | --- |
| **Essential** |Näyttää kaikkien yleisten liiketoimintatoimintojen kaikki toiminnot ja kentät.|
| **Premium** |Näyttää kaikkien liiketoimintojen toiminnot ja kentät myös valmistukselle ja huoltohallinnolle.|

> [!NOTE]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa valitut käyttökokemukset riippuvat ratkaisun käyttöoikeudesta, jota kutsutaan palvelupaketiksi. Lisätietoja **Essential**- ja **Premium**-palvelupaketeista on Microsoft Dynamics 365:n markkinointisivuston kohdassa [Business Central](https://go.microsoft.com/fwlink/?linkid=870242). Katso myös [[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen käyttöoikeusopas](https://go.microsoft.com/fwlink/?linkid=2068931) (edellyttää CustomerSourcen tai PartnerSourcen käyttöoikeutta).

> [!IMPORTANT]  
> Kaikki ratkaisun tavalliset käyttäjät täytyy liittää samaan suunnitelmaan (Essential tai Premium) ennen kyseisen käyttökokemuksen valitsemista yritykselle. Näin ollen yksi käyttäjä ei voi käyttää Premium-ominaisuuksia, jos vähintään yksi käyttäjä voi käyttää vain Essential-ominaisuuksia. Tämä ei koske erikoiskäyttäjiä, joiden tyyppi on ryhmän jäsen, sisäinen järjestelmänvalvoja, ulkoinen kirjanpitäjä tai delegoitu järjestelmänvalvoja, joille voidaan määrittää eri suunnitelma kuin muille ratkaisun käyttäjille.

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Premium-ominaisuuksien käyttöönotto suunnitelman päivittämisen jälkeen
Käyttäjille määritetään suunnitelmat Office 365 -hallintakeskuksessa samassa yhteydessä kuin Business Central -käyttäjiä määritetään. Lisätietoja on kohdassa [Käyttäjien lisääminen Office 365 for Businessiin](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Voit sitten määrittää, mitkä käyttökokemuksen toiminnot ja sivut ovat käyttäjien käytettävissä, määrittämällä käyttöoikeusjoukkoja. Lisätietoja on kohdassa [Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).

### <a name="to-update-plan-changes-in-users-groups"></a>Suunnitelman muutoksien päivittäminen käyttäjäryhmissä
Kun olet tehnyt muutoksia käyttäjien suunnitelmiin Office 365 -hallintakeskuksessa (kuten määrittänyt enemmän käyttäjiä Premium-suunnitelmaan), sinun tulee tehdä muutoksia myös [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa.

1. Kirjaudu sisään järjestelmänvalvojana.
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
3. Vaihtoehtoisesti voit valita **Käyttäjät**-sivulla **Päivitä kaikki käyttäjäryhmät** -toiminnon.

Käyttäjien suunnitelmien ja heidän määriteltyjen käyttäjäryhmiensä uudet tiedot päivitetään nyt suunnitelman muutoksien mukaisesti.

### <a name="to-select-the-premium-experience"></a>Premium-käyttäjäkokemuksen valinta
Voit nyt siirtyä valitsemaan uuden käyttökokemuksen.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yrityksen tiedot** ja valitse sitten liittyvä linkki.
2. Valitse **Yrityksen tiedot** -sivun **Käyttäjäkokemus**-pikavälilehden **Kokemus**-kentässä Premium.

## <a name="help-assumes-premium-experience"></a>Ohje käsittelee Premium-käyttäjäkokemusta
[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen käyttäjän dokumentaation kaikkien toimintojen kuvauksissa käsitellään **Premium**-käyttökokemusta. Tämä tarkoittaa sitä, että kuvaukset sisältävät käyttöliittymän kaikki elementit. Valmistuksen ja huoltohallinnon toimintojen alueiden ylätason ohjeaiheisiin lisätyssä tekstimuistiinpanossa kerrotaan, että vaatimuksena on **Premium**-käyttökokemus.

## <a name="see-also"></a>Katso myös .
[Uusien yritysten luominen](about-new-company.md)  
[Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)    
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen käyttöoikeusopas](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

