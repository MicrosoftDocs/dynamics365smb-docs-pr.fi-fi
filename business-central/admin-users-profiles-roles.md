---
title: Käyttäjien ja roolien hallinta
description: 'Tässä ohjeaiheessa kerrotaan, miten Business Centralissa hallitaan käyttäjäprofiileja.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 07/26/2024
ms.custom: bap-template
ms.search.form: '9171,'
---
# Käyttäjäprofiilien hallinta

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

## Sivun mukauttaminen

Voit mukauttaa profiilin sivuasettelua siten, että kaikki profiiliin määritetyt käyttäjät näkevät mukautetut sivut. Voit mukauttaa järjestelmänvalvojana sivuja samalla toiminnolla, jota käyttäjät käyttävät mukauttamiseen. Lisätietoja sivun asettelujen mukauttamista on kohdassa [Sivujen mukauttaminen profiileja varten](ui-personalization-manage.md).

## Profiilin luominen

Jos et voi kopioida aiemmin luotua profiilia, voit luoda uuden profiilin manuaalisesti.

1. Valitse ![Sivun tai raportin etsiminen.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvaketta, syötä **Profiilit (roolit)** ja valitse sitten liittyvä linkki.  
2. Valitse **Profiilit (roolit)** -sivulla Uusi-toiminto **·** .  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Jos haluat tietyn profiilin olevan käytettävissä vain tietyillä käyttäjillä, voit määrittää **Kuvaus**-kentän arvoksi `Navigation menu only.`. Näin profiili jätetään pois käytettävissä olevien roolien luettelosta kohdassa **Omat asetukset**.

## Profiilin kopioiminen

Voit säästää työaikaa luomalla uuden profiilin kopioimalla aiemmin luodun profiilin. Kopioi luontia varten profiili, jonka asetukset vastaavat haluamasi profiilin asetuksia.

Kun kopioit profiilia, myös kaikki mukana olevat sivun mukautukset, sekä käyttäjän luomat että laajennuksista johdetut, muutetaan.

1.  **Valitse Profiilit (roolit)**  -sivulta sen profiilin rivi, jonka haluat kopioida, ja valitse **sitten Kopioi profiili -** toiminto.
2. Täytä Profiilin tunnus- ja Näyttönimi-kentät **ja valitse sitten OK-painike**  **.**  **·** 
3. Avaa **Profiilit (roolit)** -sivulla juuri luodun profiilin kortti ja muokkaa sitten tarvittaessa muita kenttiä.

## Profiilin muokkaaminen

Voit muokata profiilia muuttamalla **Profiilit (roolit)** -sivun kenttiä. Muutokset eivät kuitenkaan näy käyttäjälle, joka on määrittänyt profiilin, ennen kuin hän kirjautuu ulos ja takaisin sisään.

> [!Caution]
> Älä nimeä profiilia uudelleen, kun profiilin käyttäjät ovat kirjautuneina. Käyttäjät voivat kokea, että tuote jumittuu ja että se on käynnistettävä uudelleen.

## Profiilin liittäminen käyttäjään

Käyttäjät voivat määrittää itselleen rooli (joka vastaa profiilia) valitsemalla **Rooli**-kentän **Omat asetukset** -sivulla. Voit tehdä järjestelmänvalvojana saman **Profiilit (roolit)** -sivulla.

1.  **Valitse Profiilit (roolit)**  -sivulla profiili, jonka haluat liittää, ja valitse **sitten Käyttäjän mukautusluettelo -** toiminto.
2. Valitse **Käyttäjäasetukset-sivulta** käyttäjä, jolle haluat määrittää profiilin, ja valitse **sitten Muokkaa-toiminto** .
3. Valitse **Profiilin tunnus** -kentässä sopiva profiili.

Jos määrität käyttäjälle toisen profiilin, käyttäjän edelliseen profiiliin tekemät mukautukset säilytetään.

## Profiilin käyttäjäasetusten määrittäminen

Käyttäjät voivat määrittää **Omat asetukset** -sivulla tilinsä perustoiminnan, kuten roolikeskuksen, kielen ja vastaanotettavat ilmoitukset. Lisätietoja käyttäjän asetuksista on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).

Järjestelmänvalvojana voit määrittää profiilin asetukset. Asetukset koskevat kaikkia rooliin liitettyjä käyttäjiä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, syötä **Profiilit (roolit)** ja valitse sitten liittyvä linkki.
2. Valitse sen profiilin rivi, jonka käyttäjäasetuksia haluat muuttaa, ja valitse **käyttäjän mukautukset luettelo** -toiminto.
3. Avaa **Käyttäjän mukautukset** -sivulla sen käyttäjän kortti, jonka asetuksia haluat muuttaa.
4. Muokkaa kenttiä tarvittaessa **Käyttäjän mukautuskortti** -sivulla.

## Profiilin aktivoiminen

Profiilia luodessasi voit valita onko profiili tietoineen käyttäjien käytettävissä, missä ne ovat käytettävissä ja miten ne ovat käytettävissä.

Valitse **Profiilit (roolit)**-sivulla seuraavat valintaruudut:

* **Käytössä** määrittää, näkyykö liittyvä rooli **Käytettävissä olevat roolit** -sivulla, jossa ne ovat käyttäjien valittavissa.  
* **Käytä oletusprofiilina** määrittää profiilin, joka koskee käyttäjiä, joille ei ole määritettyä tiettyä roolia.
* **Mukauttamisen käytöstä poistaminen** määrittää, voivatko liittyvän rooli käyttäjät mukauttaa työtilaansa.
* **Näytä roolin hallinta** -kohdassa, jos haluat määrittää, näytetäänkö profiiliin sisältyvissä liiketoimintatoiminnoissa toimintoja roolin hallinnan laajennetussa näkymässä. Lisätietoja roolin hallinnasta on kohdassa [Sivujen etsiminen roolinhallinnalla](ui-role-explorer.md).

## Vie profiilit

Voit viedä profiileja [!INCLUDE[prod_short](includes/prod_short.md)]:stä ja käyttää niitä uudelleen toisessa vuokraajassa. Kaikki profiili viedään zip-tiedostoon, joka sisältää sovelluksen kielitiedostot (AL). Voit käyttää AL-tiedostoja uudelleen laajennusten kehittämiseksi. Lisätietoja profiilien viennistä on kohdassa [Profiilien ja sivun mukautusten luominen asiakasohjelman avulla](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* Valitse **Profiilit (roolit)**  -sivulla **Vie profiilit** -toiminto.

    Toiminto vie zip-tiedoston, joka sisältää kaikkien profiilien AL-tiedostot.

## Tuo profiilit

Voit tuoda profiileja, jotka viedään Business Centralista. Vaiheet ovat suunnilleen päinvastaiset kuin profiilien viemisessä.

1. Valitse **Profiilit (roolit)**  -sivulla **Tuo profiilit -** toiminto.
1. Seuraa ohjatun **Tuo profiilit** -toiminnon vaiheita.

    Jos haluat tuoda vain valitut profiilit, osoita tuotavat profiilit **Valittu**-valintaruudun avulla.
1. Valitse **Tuo valittu -** painike.

    Toiminto tuo zip-tiedoston, joka sisältää valittujen profiilien AL-tiedostot.

## Profiilin poistaminen

Voit poistaa profiilin valitsemalla **Poista**-toiminto **Profiilit (roolit)** -sivulla. Käytössä on kuitenkin seuraavat rajoitukset:

* Käyttäjälle tai käyttäjäryhmälle määritettyä profiilia ei voi poistaa.
* Et voi poistaa laajennuksista peräisin olevia profiileja. Laajennuksen asennus on poistettava ensin.
* Kerralla voi poistaa vain yhden profiilin.

## Poista mukautukset

### Poista kaikki tietyn käyttäjän tekemät mukautukset.

Voit poistaa kaikki käyttäjän sivuille tekemät muutokset, jolloin sivut palautetaan alkuperäiseen asetteluun. Mukautuksia ei liity profiiliin (rooliin). Jos käyttäjä mukauttaa sivua, hän kokee sivun mukautukset riippumatta siitä, mitä roolia käyttäjä käyttää.<!--Deleting changes can be useful, for example, if an employee changes role and no longer needs them. The profile defines the page layout and deletions restore it back to that definition.--> 

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, syötä **Käyttäjäasetukset** ja valitse sitten liittyvä linkki.

     **Käyttäjäasetukset-sivulla** näkyvät kaikki käyttäjät.<!--who make personalizations-->.

2. Valitse käyttäjä, jonka mukautukset haluat poistaa.
3. Valitse **Käyttäjäasetukset**  kortti-sivulta **Tyhjennä mukautetut sivut** -toiminto ja hyväksy näyttöön tulee sanoma.

Muutokset näkyvät käyttäjälle, kun hän seuraavan kerran kirjautuu sisään.

Voit poistaa myös kaikki profiilin sivun mukautukset. Lisätietoja on kohdassa [Kaikkien profiilin mukautusten poistaminen](ui-personalization-manage.md#delete-all-customizations-for-a-profile).

### Poista tiettyjen sivujen mukautukset

Voit poistaa mukautuksia, joita yksi tai usea käyttäjä tekee tietyille sivuille. Mukautusten poistaminen voi olla kätevää esimerkiksi silloin, jos liiketoimintaprosessin muutos tarkoittaa, että mukautusta ei voi käyttää. Poistaminen palauttaa sivun asettelun takaisin profiilin määrittämäksi asetteluksi.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, syötä **Mukautetut sivut** ja valitse sitten liittyvä linkki.

     **Mukautetut sivut -** sivulla näkyvät kaikki räätälöidut sivut ja käyttäjä, johon ne kuuluvat.

    <!--A checkmark in the **Legacy Personalization** field indicates that the personalization was done in an older version of [!INCLUDE[prod_short](includes/prod_short.md)], which handled personalization differently. Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.-->

2. Valitse poistettavan sivun mukautusrivi ja valitse **sitten Poista-toiminto** .

Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.  

Voit poistaa myös profiilin yksittäisiä sivun mukautukset. Lisätietoja on kohdassa [Profiilin tiettyjen sivujen mukautuksen poistaminen](ui-personalization-manage.md#delete-customization-for-specific-pages-for-a-profile).

## Käyttäjäistuntojen hallinta

[!INCLUDE[prod_short](includes/prod_short.md)] Onlinen järjestelmänvalvojana voit hallita käyttäjäistuntoja hallintakeskuksessa. Lisätietoja on hallintasisällön kohdassa [Istuntojen hallinta][def].  

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises -versiossa istuntoja voidaan hallita esimerkiksi SQL Server Management Studion avulla. Lisätietoja on kohdassa [SQL Serverin tekninen dokumentaatio](/sql/sql-server).  

## Katso myös

[Käyttöoikeuksien delegoiminen käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[Profiilien sivujen mukauttaminen](ui-personalization-manage.md)  
[Työtilan mukauttaminen](ui-personalization-user.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

[def]: /dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions
