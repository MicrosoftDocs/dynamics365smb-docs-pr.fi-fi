---
title: Käyttäjien ja roolien hallinta | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten Business Central -sovelluksen käyttäjiä ja roolikeskuksia hallitaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ca0ca5f756d0d7423c92ca25034038fa1fb05727
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4745981"
---
# <a name="manage-profiles"></a>Profiilien hallinta

Kaikille [!INCLUDE[prod_short](includes/prod_short.md)]in käyttäjille määritetään profiili, joka vastaa heidän liiketoimintorooliaan, osastoaan tai muuta luokittelua. Profiilien avulla järjestelmänvalvojat voivat määrittää ja hallita keskitetysti sitä, mitä erilaiset käyttäjätyypit voida nähdä ja tehdä käyttöliittymässä, jotta he voivat suorittaa työtehtäviään tehokkaasti.

> [!NOTE]
> Tyypillinen profiilin käyttötapa liiketoiminnassa on rooli. Profiilin nimi onkin käyttöliittymässä tämän vuoksi *Profiili (rooli)*.

Järjestelmänvalvojana voi luoda ja hallita profiileja **Profiilit (roolit)** -sivulla. Jokaisella profiililla on kortti, jossa hallitaan liittyvän roolin eri asetuksia, kuten roolin nimeä, käyttäjän asetuksia ja profiilin käyttämään roolikeskusta. Lisätietoja käyttäjän asetuksista ja roolikeskuksista on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).

Käyttäjät on luotava ja lisättävä Microsoft 365 -hallintakeskuksessa, ennen kuin käyttäjien profiileja voi hallita. Voit siittää määrittää kullekin käyttäjälle tai käyttäjäryhmälle oikeuksia, jotka puolestaan määrittävät, mitä ominaisuuksia kyseinen käyttäjä tai käyttäjäryhmä saa tarkastella ja/tai muokata. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).

## <a name="page-customization"></a>Sivun mukauttaminen
Voit mukauttaa profiilin sivuasettelua siten, että kaikki profiiliin määritetyt käyttäjät näkevät mukautetut sivut. Voit mukauttaa järjestelmänvalvojana sivuja samalla toiminnolla, jota käyttäjät käyttävät mukauttamiseen. Lisätietoja on kohdassa [Profiilien sivujen mukauttaminen](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Profiilin luominen
Jos et voi kopioida aiemmin luotua profiilia, voit luoda uuden profiilin manuaalisesti.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Profiilit (roolit)** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Profiilit (roolit)** -sivulla **Uusi**-toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-a-profile"></a>Profiilin kopioiminen
Voit säästää työaikaa luomalla uuden profiilin kopioimalla aiemmin luodun profiilin. Kopioi luontia varten profiili, jonka asetukset vastaavat haluamasi profiilin asetuksia.

> [!NOTE]
> Kun kopioit profiilia, myös kaikki mukana olevat sivun mukautukset, sekä käyttäjän luomat että laajennuksista johdetut, muutetaan.

1. Valitse **Profiilit (roolit)** -sivulla kopioitavan profiilin rivi. Valitse sitten **Kopioi profiili** -toiminto.
2. Täytä **Profiilin tunnus**- ja **Näyttönimi**-kentät ja valitse sitten **OK**-painike.
3. Avaa **Profiilit (roolit)** -sivulla juuri luodun profiilin kortti ja muokkaa sitten tarvittaessa muita kenttiä.

## <a name="to-edit-a-profile"></a>Profiilin muokkaaminen
Voit muokata profiilia muuttamalla **Profiili (rooli)** -sivun kenttiä. Muutokset eivät kuitenkaan näy käyttäjälle, joka on määrittänyt profiilin, ennen kuin hän kirjautuu ulos ja takaisin sisään.

> [!Caution]
> Älä nimeä profiilia uudelleen, kun profiilin käyttäjät ovat kirjautuneina. Käyttäjät voivat kokea, että tuote jumittuu ja että se on käynnistettävä uudelleen.

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

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Profiilit (Roolit)** ja valitse sitten liittyvä linkki.
2. Valitse sen profiilin rivi, jonka käyttäjän asetuksia haluat muuttaa, ja valitse sitten **Käyttäjän mukautuslista** -toiminto.
3. Avaa **Käyttäjän mukautukset** -sivulla sen käyttäjän kortti, jonka asetuksia haluat muuttaa.
4. Muokkaa kenttiä tarvittaessa **Käyttäjän mukautuskortti** -sivulla.

## <a name="to-activate-a-profile"></a>Profiilin aktivointi
Profiilia luotaessa valitaan erilaisia valintaruutuja, jotka määrittävät, onko profiili tietoineen käyttäjien käytettävissä, missä ne ovat käytettävissä ja miten ne ovat käytettävissä.

* Valitse **Profiili (rooli)**-sivulla seuraavat valintaruudut:
    - **Käytössä** määrittää, näkyykö liittyvä rooli **Käytettävissä olevat roolit** -sivulla, jossa ne ovat käyttäjien valittavissa.  
    - **Käytä oletusprofiilina** määrittää profiilin, joka koskee käyttäjiä, joille ei ole määritettyä tiettyä roolia.
    - **Mukauttamisen käytöstä poistaminen** määrittää, voivatko liittyvän rooli käyttäjät mukauttaa työtilaansa.
    - **Näytä roolin hallinta** -kohdassa, jos haluat määrittää, näytetäänkö profiiliin sisältyvissä liiketoimintatoiminnoissa toimintoja roolin hallinnan laajennetussa näkymässä. Lisätietoja on kohdassa [Sivujen etsiminen roolinhallinnalla](ui-role-explorer.md).

## <a name="to-export-profiles"></a>Profiilien vieminen
Voit viedä profiileja [!INCLUDE[prod_short](includes/prod_short.md)]:stä ja esimerkiksi käyttää niitä uudelleen toisessa vuokraajassa. Profiilit viedään zip-tiedostoon, ja siinä on .al-tiedostot, joiden avulla voidaan kehittää laajennuksia. Lisätietoja on kohdassa [Profiilien ja sivun mukautusten luominen asiakasohjelman avulla](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* Valitse **Profiilit (roolit)** -sivulla **Vie profiilit** -toiminto.

Kaikkien profiilien .al-tiedostot sisältämä zip-tiedosto viedään.

## <a name="to-import-profiles"></a>Profiilien tuominen
Voit tuoda profiileja, jotka on viety [!INCLUDE[prod_short](includes/prod_short.md)]:stä. Vaiheet ovat suunnilleen päinvastaiset kuin profiilien viemisessä. Lisätietoja on kohdassa [Profiilien vieminen](admin-users-profiles-roles.md#to-export-profiles).

1. Valitse **Profiilit (roolit)** -sivulla **Tuo profiilit** -toiminto.
2. Seuraa ohjatun **Tuo profiilit** -toiminnon vaiheita.

    Jos haluat tuoda vain valitut profiilit, osoita tuotavat profiilit **Valittu**-valintaruudun avulla.
3. Valitse **Tuo valitut** -painike.

Valittujen profiilien .al-tiedostot sisältävä zip-tiedosto tuodaan.

## <a name="to-delete-a-profile"></a>Profiilin poistaminen
Voit poistaa profiilin valitsemalla **Poista**-toiminto **Profiilit (roolit)** -sivulla. Käytössä on kuitenkin seuraavat rajoitukset:

- Käyttäjälle tai käyttäjäryhmälle määritettyä profiilia ei voi poistaa.
- Et voi poistaa laajennuksista peräisin olevia profiileja. Laajennuksen asennus on poistettava ensin.
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

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjäsivun mukautukset** ja valitse sitten liittyvä linkki.

    **Käyttäjän sivun mukautukset** -sivulla on luettelo kaikista mukautetuista sivuista ja käyttäjistä, joille nämä sivut kuuluvat.

    > [!Note]
    > **Vanha mukautus** -kentän valintamerkki ilmaisee, että mukautus tehtiin [!INCLUDE[prod_short](includes/prod_short.md)]in vanhassa versiossa, jossa mukautusta käsiteltiin eri tavalla. Mukautus estetään näiden sivujen mukautusta yrittäviltä käyttäjiltä, elleivät he ensin valitse sivun lukituksen poistamista. Lisätietoja on kohdassa [Sivun mukauttamisen estäminen lukitsemalla](ui-personalization-locked.md).

2. Valitse ensin poistettavan sivun mukautuksen rivi ja sitten **Poista**-toiminto.

Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.  

Voit poistaa myös profiilin yksittäisiä sivun mukautukset. Lisätietoja on kohdassa [Profiilin tiettyjen sivujen mukautuksen poistaminen](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## <a name="managing-user-sessions"></a>Käyttäjäistuntojen hallinta

[!INCLUDE[prod_short](includes/prod_short.md)] Onlinen järjestelmänvalvojana voit hallita käyttäjäistuntoja hallintakeskuksessa. Lisätietoja on hallintasisällön kohdassa [Istuntojen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions).  

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises -versiossa istuntoja voidaan hallita esimerkiksi SQL Server Management Studion avulla. Lisätietoja on kohdassa [SQL Serverin tekninen dokumentaatio](/sql/sql-server).  

## <a name="see-also"></a>Katso myös  
[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[Profiilien sivujen mukauttaminen](ui-personalization-manage.md)  
[Työtilan mukauttaminen](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]