---
title: Käyttäjien ja roolien hallinta | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten Business Central -sovelluksen käyttäjiä ja roolikeskuksia hallitaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 00a07acfb455b9b1ddf714f7ca7e49a56a8aebbc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304229"
---
# <a name="manage-profiles"></a>Profiilien hallinta
Kaikille [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjille määritetään profiili, joka vastaa heidän liiketoimintorooliaan, osastoaan tai muuta luokittelua. Profiilien avulla järjestelmänvalvojat voivat määrittää ja hallita keskitetysti sitä, mitä erilaiset käyttäjätyypit voida nähdä ja tehdä käyttöliittymässä, jotta he voivat suorittaa työtehtäviään tehokkaasti.

> [!NOTE]
> Tyypillinen profiilin käyttötapa liiketoiminnassa on rooli. Profiilin nimi onkin käyttöliittymässä tämän vuoksi *Profiili (rooli)*.

Järjestelmänvalvojana voi luoda ja hallita profiileja **Profiilit (roolit)** -sivulla. Jokaisella profiililla on kortti, jossa hallitaan liittyvän roolin eri asetuksia, kuten roolin nimeä, käyttäjän asetuksia ja profiilin käyttämään roolikeskusta. Lisätietoja käyttäjän asetuksista ja roolikeskuksista on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).

Käyttäjät on luotava ja lisättävä Office 365 -hallintakeskuksessa, ennen kuin käyttäjien profiileja voi hallita. Voit siittää määrittää kullekin käyttäjälle tai käyttäjäryhmälle oikeuksia, jotka puolestaan määrittävät, mitä ominaisuuksia kyseinen käyttäjä tai käyttäjäryhmä saa tarkastella ja/tai muokata. Lisätietoja on kohdassa [Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).

## <a name="page-customization"></a>Sivun mukauttaminen
Voit mukauttaa profiilin sivuasettelua siten, että kaikki profiiliin määritetyt käyttäjät näkevät mukautetut sivut. Voit mukauttaa järjestelmänvalvojana sivuja samalla toiminnolla, jota käyttäjät käyttävät mukauttamiseen. Lisätietoja on kohdassa [Profiilien sivujen mukauttaminen](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Profiilin luominen
Jos et voi kopioida aiemmin luotua profiilia, voit luoda uuden profiilin manuaalisesti.

> [!NOTE]
> Kaikki profiilit voidaan kopioida, mutta vain käyttäjän luomat profiilien sivujen mukautukset voidaan kopioida.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Profiilit (roolit)** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Profiilit (roolit)** -sivulla **Uusi**-toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-a-profile"></a>Profiilin kopioiminen
Voit säästää työaikaa luomalla uuden profiilin kopioimalla aiemmin luodun profiilin. Kopioi luontia varten profiili, jonka asetukset vastaavat haluamasi profiilin asetuksia.

1. Valitse **Profiilit (roolit)** -sivulla kopioitavan profiilin rivi. Valitse sitten **Kopioi profiili** -toiminto.
2. Täytä **Profiilin tunnus**- ja **Näyttönimi**-kentät ja valitse sitten **OK**-painike.
3. Avaa **Profiilit (roolit)** -sivulla juuri luodun profiilin kortti ja muokkaa sitten tarvittaessa muita kenttiä.

## <a name="to-edit-a-profile"></a>Profiilin muokkaaminen
Voit muokata profiilia muuttamalla **Profiili (rooli)** -sivun kenttiä.

> [!NOTE]
> Et voi muokata profiilia, jos kirjautuneena on käyttäjiä, joille profiili on määritetty.

## <a name="to-assign-a-profile-to-a-user"></a>Profiilin määrittäminen käyttäjälle
Käyttäjät voivat määrittää itselleen rooli (joka vastaa profiilia) valitsemalla **Rooli**-kentän **Omat asetukset** -sivulla. Voit tehdä järjestelmänvalvojana saman **Profiilit (roolit)** -sivulla.

1. Valitse **Profiilit (roolit)** -sivulla määritettävän profiilin rivi. Valitse sitten **Käyttäjän mukautusluettelo** -toiminto.
2. Valitse **Käyttäjän mukautukset** -sivulla se käyttäjä, jolle profiili määritetään. Valitse sitten **Muokkaa**-toiminto.
3. Valitse **Profiilin tunnus** -kentässä sopiva profiili.

> [!NOTE]
> Jos määrität käyttäjälle toisen profiilin, käyttäjän edelliseen profiiliin tekemät mukautukset säilytetään.

## <a name="to-define-user-settings-for-a-profile"></a>Profiilin käyttäjän asetusten määrittäminen
Käyttäjät voivat määrittää **Omat asetukset** -sivulla tilinsä perustoiminnan, kuten roolikeskuksen, kielen ja vastaanotettavat ilmoitukset. Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).

Voit määrittää järjestelmänvalvojana nämä profiilin asetukset ja siten ottaa asetukset käyttöön kaikille liittyvän roolin käyttäjille.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Profiilit (roolit)** ja valitse sitten liittyvä linkki.
2. Valitse sen profiilin rivi, jonka käyttäjän asetuksia haluat muuttaa, valitsemalla **Navigoi**-toiminto ja valitse sitten **Käyttäjän mukautukset** -toiminto.
3. Avaa **Käyttäjän mukautukset** -sivulla sen käyttäjän kortti, jonka asetuksia haluat muuttaa.
4. Muokkaa kenttiä tarvittaessa **Käyttäjän mukautuskortti** -sivulla.

## <a name="to-activate-a-profile"></a>Profiilin aktivointi
Profiilia luotaessa valitaan erilaisia valintaruutuja, jotka määrittävät, onko profiili tietoineen käyttäjien käytettävissä, missä ne ovat käytettävissä ja miten ne ovat käytettävissä.

1. Valitse **Profiili (rooli)**-sivulla seuraavat valintaruudut:
    - **Käytössä** määrittää, näkyykö liittyvä rooli **Käytettävissä olevat roolit** -sivulla, jossa ne ovat käyttäjien valittavissa.  
    - **Käytä oletusprofiilina** määrittää profiilin, joka koskee käyttäjiä, joille ei ole määritettyä tiettyä roolia.
    - **Mukauttamisen käytöstä poistaminen** määrittää, voivatko liittyvän rooli käyttäjät mukauttaa työtilaansa.
    - **Näyttäminen roolienhallinnassa** määrittää, näytetäänkö profiiliin sisältyvät liiketoimintatoiminnot avaavat valikkovaihtoehdot toiminnon yleiskatsauksessa. Lisätietoja on kohdassa [Sivujen etsiminen toiminnon yleiskatsauksessa](ui-role-explorer.md).

    ## <a name="to-export-user-created-profiles"></a>Käyttäjän luomien profiilien vieminen
    Voit viedä joko itse muuttamasi tai käyttäjien muuttamat profiilit, mistä on ilmaisuna **Lähde**-kentän **(Käyttäjän luoma)** -kohta. Profiili viedään zip-tiedostoon, ja siinä on .al-tiedostot, joiden avulla voidaan kehittää laajennuksia. Lisätietoja on kohdassa [Profiilien ja sivun mukautusten luominen asiakasohjelman avulla](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

    * Valitse **Profiilit (roolit)** -sivulla **Vie käyttäjän luomat profiilit** -toiminto.

    Juuri lisättyjen tai muokattujen profiilien .al-tiedostot sisältävä zip-tiedosto viedään.

## <a name="to-delete-a-profile"></a>Profiilin poistaminen
Voit poistaa profiilin valitsemalla **Poista**-toiminto **Profiilit (roolit)** -sivulla. Käytössä on kuitenkin seuraavat rajoitukset:

- Et voi poistaa laajennuksista peräisin olevia profiileja. Laajennuksen asennus on poistettava ensin.
- Profiili on poistettava käytöstä. Tämä myös varmistaa, ettei kukaan profiiliin määritetty käyttäjä ole kirjautuneena, kun profiili poistetaan.
- Kerralla voi poistaa vain yhden profiilin.  

## <a name="to-delete-all-personalizations-made-by-a-user"></a>Kaikkien käyttäjän tekemien mukautusten poistaminen
Voit poistaa kaikki muutokset, jotka käyttäjä on tehnyt työtilan muodostaville sivuille. Tästä voi olla hyötyä esimerkiksi silloin, jos työntekijä on muuttanut roolia eikä enää tarvitse mukautuksia. Käyttäjien mukautusten poistaminen muuttaa sivun asettelun takaisin profiilin määrittämäksi asetteluksi.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän mukautukset** ja valitse sitten liittyvä linkki.

    **Käyttäjän mukautukset** -sivulla on luettelo kaikista käyttäjistä, jotka ovat tehneet mukautuksia.

2. Avaa sen käyttäjän kortti, jonka mukautukset haluat poistaa.
3. Valitse **Käyttäjän mukautuskortti** -sivulla **Tyhjennä mukautetut sivut** -toiminto ja hyväksy sitten avautuva sanoma.

Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.

Voit poistaa myös kaikki profiilin sivun mukautukset. Lisätietoja on kohdassa [Kaikkien profiilin mukautusten poistaminen](ui-personalization-manage.md#to-delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages"></a>Tiettyjen sivujen mukautusten poistaminen
Voit poistaa mukautuksia, joita yksi tai usea käyttäjä on tehnyt tietyille työtilan muodostaville sivuille. Tämä voi olla kätevää esimerkiksi silloin, jos liiketoimintaprosessin muutos tarkoittaa, että käyttäjät eivät enää saa käyttää mukautusta. Käyttäjien mukautusten poistaminen muuttaa sivun asettelun takaisin profiilin määrittämäksi asetteluksi.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän sivun mukautukset** ja valitse sitten liittyvä linkki.

    **Käyttäjän sivun mukautukset** -sivulla on luettelo kaikista mukautetuista sivuista ja käyttäjistä, joille nämä sivut kuuluvat.

    > [!Note]
    > **Vanha mukautus** -kentän valintamerkki ilmaisee, että mukautus tehtiin [!INCLUDE[d365fin](includes/d365fin_md.md)]in vanhassa versiossa, jossa mukautusta käsiteltiin eri tavalla. Mukautus estetään näiden sivujen mukautusta yrittäviltä käyttäjiltä, elleivät he ensin valitse sivun lukituksen poistamista. Lisätietoja on kohdassa [Sivun mukauttamisen estäminen lukitsemalla](ui-personalization-locked.md).

2. Valitse ensin poistettavan sivun mukautuksen rivi ja sitten **Poista**-toiminto.

Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.    

Voit poistaa myös profiilin yksittäisiä sivun mukautukset. Lisätietoja on kohdassa [Profiilin tiettyjen sivujen mukautuksen poistaminen](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## <a name="see-also"></a>Katso myös  
[Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)  
[Profiilien sivujen mukauttaminen](ui-personalization-manage.md)  
[Työtilan mukauttaminen](ui-personalization-user.md)  
