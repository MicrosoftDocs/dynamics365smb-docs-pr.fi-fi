---
title: Käyttäjien ja roolien hallinta
description: 'Tässä ohjeaiheessa kerrotaan, miten Business Centralissa hallitaan käyttäjäprofiileja.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 01/11/2023
ms.custom: bap-template
ms.search.form: 9171
---
# <a name="manage-user-profiles"></a>Käyttäjäprofiilien hallinta

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Määritä kaikki käyttäjät profiileihin, jotka kuvaavat:

* Heidän liiketoimintarooliaan
* Osastoa, jossa he työskentelevät
* Muun tyyppistä luokittelua

Profiilien avulla järjestelmänvalvojat voivat keskitetysti määrittää ja hallita sitä, mitä erityyppiset käyttäjät voivat käyttää Business Centralissa.

Tyypillinen profiilin käyttötapa liiketoiminnassa on rooli. Profiilin nimi onkin käyttöliittymässä tämän vuoksi *Profiili (rooli)*.

Järjestelmänvalvojana voi luoda ja hallita profiileja **Profiilit (roolit)** -sivulla. Jokaisella profiililla on kortti, jossa hallitaan liittyvän roolin asetuksia. Kortti sisältää seuraavat tiedot:

* Roolin nimi
* Käyttäjän mukautukset
* Profiilin käyttämä roolikeskus

Lisätietoja käyttäjän asetuksista ja roolikeskuksista on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).

Käyttäjät on luotava ja lisättävä Microsoft 365 -hallintakeskuksessa, ennen kuin käyttäjäprofiileja voi hallita. Sen jälkeen voit määrittää käyttöoikeudet kullekin käyttäjälle tai käyttäjäryhmälle. Käyttöoikeudet määrittävät ominaisuudet, joita käyttäjät voivat käyttää. Lisätietoja käyttöoikeuksien joukoista on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).

## <a name="page-customization"></a>Sivun mukauttaminen

Voit mukauttaa profiilin sivuasettelua siten, että kaikki profiiliin määritetyt käyttäjät näkevät mukautetut sivut. Voit mukauttaa järjestelmänvalvojana sivuja samalla toiminnolla, jota käyttäjät käyttävät mukauttamiseen. Lisätietoja sivun asettelujen mukauttamista on kohdassa [Sivujen mukauttaminen profiileja varten](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Profiilin luominen

Jos et voi kopioida aiemmin luotua profiilia, voit luoda uuden profiilin manuaalisesti.

1. Valitse ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Profiilit (Roolit)** ja valitse sitten vastaava linkki.  
2. Valitse **Profiilit (roolit)** -sivulla **Uusi**-toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Jos haluat tietyn profiilin olevan käytettävissä vain tietyillä käyttäjillä, voit määrittää **Kuvaus**-kentän arvoksi `Navigation menu only.`. Näin profiili jätetään pois käytettävissä olevien roolien luettelosta kohdassa **Omat asetukset**.

## <a name="to-copy-a-profile"></a>Profiilin kopioiminen

Voit säästää työaikaa luomalla uuden profiilin kopioimalla aiemmin luodun profiilin. Kopioi luontia varten profiili, jonka asetukset vastaavat haluamasi profiilin asetuksia.

Kun kopioit profiilia, myös kaikki mukana olevat sivun mukautukset, sekä käyttäjän luomat että laajennuksista johdetut, muutetaan.

1. Valitse **Profiilit (roolit)** -sivulla kopioitavan profiilin rivi. Valitse sitten **Kopioi profiili** -toiminto.
2. Täytä **Profiilin tunnus**- ja **Näyttönimi**-kentät ja valitse sitten **OK**-painike.
3. Avaa **Profiilit (roolit)** -sivulla juuri luodun profiilin kortti ja muokkaa sitten tarvittaessa muita kenttiä.

## <a name="to-edit-a-profile"></a>Profiilin muokkaaminen

Voit muokata profiilia muuttamalla **Profiilit (roolit)** -sivun kenttiä. Muutokset eivät kuitenkaan näy käyttäjälle, joka on määrittänyt profiilin, ennen kuin hän kirjautuu ulos ja takaisin sisään.

> [!Caution]
> Älä nimeä profiilia uudelleen, kun profiilin käyttäjät ovat kirjautuneina. Käyttäjät voivat kokea, että tuote jumittuu ja että se on käynnistettävä uudelleen.

## <a name="to-assign-a-profile-to-a-user"></a>Profiilin määrittäminen käyttäjälle

Käyttäjät voivat määrittää itselleen rooli (joka vastaa profiilia) valitsemalla **Rooli**-kentän **Omat asetukset** -sivulla. Voit tehdä järjestelmänvalvojana saman **Profiilit (roolit)** -sivulla.

1. Valitse **Profiilit (roolit)** -sivulla määritettävän profiilin rivi. Valitse sitten **Käyttäjän mukautusluettelo** -toiminto.
2. Valitse **Käyttäjän mukautukset** -sivulla se käyttäjä, jolle profiili määritetään. Valitse sitten **Muokkaa**-toiminto.
3. Valitse **Profiilin tunnus** -kentässä sopiva profiili.

Jos määrität käyttäjälle toisen profiilin, käyttäjän edelliseen profiiliin tekemät mukautukset säilytetään.

## <a name="to-define-user-settings-for-a-profile"></a>Profiilin käyttäjän asetusten määrittäminen

Käyttäjät voivat määrittää **Omat asetukset** -sivulla tilinsä perustoiminnan, kuten roolikeskuksen, kielen ja vastaanotettavat ilmoitukset. Lisätietoja käyttäjän asetuksista on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).

Järjestelmänvalvojana voit määrittää profiilin asetukset. Asetukset koskevat kaikkia rooliin liitettyjä käyttäjiä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Profiilit (Roolit)** ja valitse sitten vastaava linkki.
2. Valitse sen profiilin rivi, jonka käyttäjän asetuksia haluat muuttaa, ja valitse sitten **Käyttäjän mukautuslista** -toiminto.
3. Avaa **Käyttäjän mukautukset** -sivulla sen käyttäjän kortti, jonka asetuksia haluat muuttaa.
4. Muokkaa kenttiä tarvittaessa **Käyttäjän mukautuskortti** -sivulla.

## <a name="to-activate-a-profile"></a>Profiilin aktivointi

Profiilia luodessasi voit valita onko profiili tietoineen käyttäjien käytettävissä, missä ne ovat käytettävissä ja miten ne ovat käytettävissä.

Valitse **Profiilit (roolit)**-sivulla seuraavat valintaruudut:

* **Käytössä** määrittää, näkyykö liittyvä rooli **Käytettävissä olevat roolit** -sivulla, jossa ne ovat käyttäjien valittavissa.  
* **Käytä oletusprofiilina** määrittää profiilin, joka koskee käyttäjiä, joille ei ole määritettyä tiettyä roolia.
* **Mukauttamisen käytöstä poistaminen** määrittää, voivatko liittyvän rooli käyttäjät mukauttaa työtilaansa.
* **Näytä roolin hallinta** -kohdassa, jos haluat määrittää, näytetäänkö profiiliin sisältyvissä liiketoimintatoiminnoissa toimintoja roolin hallinnan laajennetussa näkymässä. Lisätietoja roolin hallinnasta on kohdassa [Sivujen etsiminen roolinhallinnalla](ui-role-explorer.md).

## <a name="to-export-profiles"></a>Profiilien vieminen

Voit viedä profiileja [!INCLUDE[prod_short](includes/prod_short.md)]:stä ja käyttää niitä uudelleen toisessa vuokraajassa. Kaikki profiili viedään zip-tiedostoon, joka sisältää sovelluksen kielitiedostot (AL). Voit käyttää AL-tiedostoja uudelleen laajennusten kehittämiseksi. Lisätietoja profiilien viennistä on kohdassa [Profiilien ja sivun mukautusten luominen asiakasohjelman avulla](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* Valitse **Profiilit (roolit)** -sivulla **Vie profiilit** -toiminto.

    Toiminto vie zip-tiedoston, joka sisältää kaikkien profiilien AL-tiedostot.

## <a name="to-import-profiles"></a>Profiilien tuominen

Voit tuoda profiileja, jotka viedään Business Centralista. Vaiheet ovat suunnilleen päinvastaiset kuin profiilien viemisessä.

1. Valitse **Profiilit (roolit)** -sivulla **Tuo profiilit** -toiminto.
1. Seuraa ohjatun **Tuo profiilit** -toiminnon vaiheita.

    Jos haluat tuoda vain valitut profiilit, osoita tuotavat profiilit **Valittu**-valintaruudun avulla.
1. Valitse **Tuo valitut** -painike.

    Toiminto tuo zip-tiedoston, joka sisältää valittujen profiilien AL-tiedostot.

## <a name="to-delete-a-profile"></a>Profiilin poistaminen

Voit poistaa profiilin valitsemalla **Poista**-toiminto **Profiilit (roolit)** -sivulla. Käytössä on kuitenkin seuraavat rajoitukset:

* Käyttäjälle tai käyttäjäryhmälle määritettyä profiilia ei voi poistaa.
* Et voi poistaa laajennuksista peräisin olevia profiileja. Laajennuksen asennus on poistettava ensin.
* Kerralla voi poistaa vain yhden profiilin.

## <a name="to-delete-all-personalizations-made-by-a-user"></a>Kaikkien käyttäjän tekemien mukautusten poistaminen

Voit poistaa kaikki muutokset, jotka käyttäjä tekee sivuille. Muutosten poistamisesta voi olla hyötyä esimerkiksi silloin, jos työntekijä muuttaa roolia eikä enää tarvitse niitä. Profiili määrittää sivun asettelun ja poistot palauttavat sen takaisin kyseiseen määritykseen.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän mukautukset** ja valitse sitten vastaava linkki.

    **Käyttäjän mukautukset** -sivulla on luettelo kaikista käyttäjistä, jotka tekevät mukautuksia.

2. Avaa sen käyttäjän kortti, jonka mukautukset haluat poistaa.
3. Valitse **Käyttäjän mukautuskortti** -sivulla **Tyhjennä mukautetut sivut** -toiminto ja hyväksy sitten avautuva sanoma.

Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.

Voit poistaa myös kaikki profiilin sivun mukautukset. Lisätietoja on kohdassa [Kaikkien profiilin mukautusten poistaminen](ui-personalization-manage.md#delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages"></a>Tiettyjen sivujen mukautusten poistaminen

Voit poistaa mukautuksia, joita yksi tai usea käyttäjä tekee tietyille sivuille. Mukautusten poistaminen voi olla kätevää esimerkiksi silloin, jos liiketoimintaprosessin muutos tarkoittaa, että mukautusta ei voi käyttää. Poistaminen palauttaa sivun asettelun takaisin profiilin määrittämäksi asetteluksi.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän sivun mukautukset** ja valitse sitten vastaava linkki.

    **Käyttäjän sivun mukautukset** -sivulla on luettelo kaikista mukautetuista sivuista ja käyttäjistä, joille nämä sivut kuuluvat.

    **Vanha mukautus** -kentän valintamerkki ilmaisee, että mukautus tehtiin [!INCLUDE[prod_short](includes/prod_short.md)]in vanhassa versiossa, jossa mukautusta käsiteltiin eri tavalla. Mukautus estetään näiden sivujen mukautusta yrittäviltä käyttäjiltä, elleivät he ensin valitse sivun lukituksen poistamista.

2. Valitse ensin poistettavan sivun mukautuksen rivi ja sitten **Poista**-toiminto.

Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.  

Voit poistaa myös profiilin yksittäisiä sivun mukautukset. Lisätietoja on kohdassa [Profiilin tiettyjen sivujen mukautuksen poistaminen](ui-personalization-manage.md#delete-customization-for-specific-pages-for-a-profile).

## <a name="managing-user-sessions"></a>Käyttäjäistuntojen hallinta

[!INCLUDE[prod_short](includes/prod_short.md)] Onlinen järjestelmänvalvojana voit hallita käyttäjäistuntoja hallintakeskuksessa. Lisätietoja on hallintasisällön kohdassa [Istuntojen hallinta][def].  

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises -versiossa istuntoja voidaan hallita esimerkiksi SQL Server Management Studion avulla. Lisätietoja on kohdassa [SQL Serverin tekninen dokumentaatio](/sql/sql-server).  

## <a name="see-also"></a>Katso myös

[Käyttöoikeuksien delegoiminen käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[Profiilien sivujen mukauttaminen](ui-personalization-manage.md)  
[Työtilan mukauttaminen](ui-personalization-user.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

[def]: /dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions
