---
title: Perusasetusten tarkasteleminen ja muokkaaminen | Microsoft Docs
description: "Tietoja siitä, miten joitakin perusasetuksia voi muuttaa. Tällaisia perusasetuksia ovat esimerkiksi roolikeskus, yritys ja käsittelypäivämäärä."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 03/02/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 30dcd44d84ecca873de7b3a0401325377987324f
ms.contentlocale: fi-fi
ms.lasthandoff: 06/01/2018

---
# <a name="changing-basic-settings"></a>Perusasetusten muuttaminen
Voit tarkastella **Omat asetukset** -ikkunassa [!INCLUDE[d365fin](includes/d365fin_md.md)]in perusasetuksia ja muuttaa niitä. Tekemäsi muutokset vaikuttavat vain omaan työtilaasi; ei muiden käyttäjien työtiloihin.  

## <a name="role-center"></a>Roolikeskus
Roolikeskus edustaa kotisivua eli aloitussivua, joka on suunniteltu organisaation tiettyä roolia varten. Roolisi mukaan roolikeskus antaa yleiskuvan yrityksestäsi, osastostasi tai henkilökohtaisista tehtävistäsi. Se auttaa myös siirtymään päivittäisten tehtävien välillä ja löytämään työt, jotka on määritetty sinulle.

-   Yläreunan siirtymisvalikon avulla voit siirtyä asiakkaiden, toimittajien, nimikkeiden ja muiden tärkeiden tietoluetteloiden välillä. Vastaavasti toimintojen avulla voit aloittaa tehtävät, kuten luoda uuden myyntilaskun suoraan roolikeskuksesta.

-   Keskellä ovat **Toimenpiteet**. Toimenpiteissä näkyvät nykyiset tiedot, joista saa yksityiskohtaisia tietoja napsauttamalla tai napauttamalla. Suorituskykyilmaisimet voidaan määrittää niin, että ne näyttävät visuaalisesti esimerkiksi kassavirran tai tuottojen ja kulujen valitun kaavion. Voit luoda kotisivulla myös suosikkiasiakkaiden luettelon niitä asiakkaita varten, joiden kanssa käyt kauppaa usein tai jotka vaativat erityishuomiota.

### <a name="to-change-role-center"></a>Roolikeskuksen vaihtaminen
Oletusroolikeskus on **Liiketoimintajohtaja**, mutta voit valita tarvittaessa toisen roolikeskuksen.
1. Valitse oikeassa yläkulmassa **Asetukset**-kuvake ![Asetukset](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") ja valitse sitten **Omat asetukset**.
2. Valitse **Omat asetukset** -ikkunan **Roolikeskus**-kenttään roolikeskus, jonka haluat valita vakioroolikeskukseksi. Valitse esimerkiksi **Kirjanpitäjä**.
3. Valitse **OK**-painike.

## <a name="company"></a>Oma yritys
Yritystoiminnot [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietojen säilönä. Tietokannassa voi olla useita yrityksiä. Kerralla on kuitenkin mahdollista valita vain yksi yritys.

Oletusyrityksen nimi on CRONUS, ja se sisältää vain esittelytietoja.

> [!TIP]  
>   Jos haluat, että yritys näkyy sovelluksessa toisella nimellä (esimerkiksi roolikeskuksessa), määritä **Nimi**-kenttä **Yritystiedot**-sivulla tai **Näyttönimi**-kenttä **Yritykset**-sivulla.  

## <a name="work-date"></a>Käsittelypvm
Oletuskäsittelypäivä on yleensä kuluvan päivän päivämäärä. Saatat joutua muuttamaan käsittelypäivämäärän väliaikaisesti, jotta voit suorittaa tehtäviä, kuten sellaisten tapahtumien täydentäminen, joiden päivämäärä ei ole kuluvan päivän päivämäärä.

> [!TIP]  
>   Kirjoita **w**, kun haluat antaa käsittelypäivämäärän nopeasti päivämääräkenttään. Kirjoita **t**, kun haluat syöttää nopeasti nykyisen päivämäärän päivämääräkenttään.

> [!IMPORTANT]  
>   Käsittelypäivämäärää muutetaan vain siihen asti, kunnes yritys suljetaan, tai siihen asti, kunnes päivämäärä muuttuu. Jos avaat toisen yrityksen tai jos avaat saman yrityksen uudestaan seuraavana päivänä, käsittelypäivämäärä täytyy määrittää uudestaan, jos tarvitset vielä järjestelmäpäivämäärästä poikkeavan päivämäärän.

## <a name="region"></a>Alue
**Alue**-asetus määrittää, miten päivämäärät, ajat, luvut ja valuutat näkyvät tai miten ne on muotoiltu.   


## <a name="language"></a>Kieli
Muuttaa näyttökielen. Tämä kenttä näkyy vain, kun useita kieliä voi valita. 

Alkuperäinen kieli määräytyy joko järjestelmänvalvojan asettamien tai selaimen asetusten mukaan, kun rekisteröidyt [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellukseen. Määrittämääsi kieltä käytetään kaikissa laitteissa, joista kirjaudut, esimerkiksi puhelimessa ja tabletissa. 

## <a name="changing-when-i-receive-notifications"></a>Ilmoitusten vastaanoton ajankohta-asetusten muuttaminen
Valitsemalla tämän linkin voit tarkastella tai muuttaa ilmoituksia, joita saat tietyistä tapahtumista tai tilamuutoksista esimerkiksi silloin, kun olet laskuttamassa asiakasta, jolla on erääntynyttä saldoa, tai kun käytettävissä oleva varasto on pienempi kuin myytävä määrä. Lisätietoja on kohdassa [Älykkäät ilmoitukset](ui-smart-notifications.md).

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  

