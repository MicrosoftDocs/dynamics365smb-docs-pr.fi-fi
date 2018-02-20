---
title: Financialsin perusasetusten tarkasteleminen ja muokkaaminen | Microsoft Docs
description: "Tutustu, miten joitakin Financialsin perusasetuksia voi muuttaa. Tällaisia perusasetuksia ovat esimerkiksi roolikeskus, yritys ja käsittelypäivämäärä."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3b2fb6a1d63e689d54d9b89b1edae0f18607f276
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="changing-basic-settings"></a>Perusasetusten muuttaminen
Voit tarkastella **Omat asetukset** -ikkunassa [!INCLUDE[d365fin](includes/d365fin_md.md)]in perusasetuksia ja muuttaa niitä.  

## <a name="role-center"></a>Roolikeskus
Roolikeskus edustaa kotisivua eli aloitussivua, joka on suunniteltu roolia varten. Kotisivu sisältää liiketoiminnan yleiskuvauksen. Vasemmalla olevan siirtymispalkin avulla voit helposti käsitellä asiakkaita, toimittajia, nimikkeitä jne.

Keskellä ovat toimenpideruudut. Toimenpiteet esittävät nykyiset tiedot. Valitun asiakirjan saa helposti käyttöön toimenpiteitä napsauttamalla tai napauttamalla. Suorituskykyilmaisimet voidaan määrittää niin, että ne näyttävät visuaalisesti esimerkiksi kassavirran tai tuottojen ja kulujen valitun kaavion.

Voit luoda kotisivulla myös suosikkiasiakkaiden luettelon niitä asiakkaita varten, joiden kanssa käyt kauppaa usein tai jotka vaativat erityishuomiota. Nuolten avulla voit supistaa osan sivusta, jolloin haluamillesi tiedoille jää enemmän tilaa. Kotisivun yläosassa ovat toiminnot, joita voit käyttää nykyisen sisällön käsittelemisessä. Sekin voidaan supistaa. Voit jatkaa supistetun alueen tarkastelemista napsauttamalla tai napauttamalla aluetta.

Oletusroolikeskus on **Liiketoimintajohtaja**, mutta voit valita tarvittaessa toisen roolikeskuksen. Lisätietoja on kohdassa [Roolikeskuksen vaihtaminen](change-role.md).

## <a name="company"></a>Oma yritys
Yritystoiminnot [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietojen säilönä. Tietokannassa voi olla useita yrityksiä. Kerralla on kuitenkin mahdollista valita vain yksi yritys.

Oletusyrityksen nimi on CRONUS, ja se sisältää vain esittelytietoja.

> [!TIP]  
>   Jos haluat, että yritys näkyy sovelluksessa toisella nimellä (esimerkiksi aloitussivulla), määritä **Nimi**-kenttä **Yritystiedot**-sivulla tai **Näyttönimi**-kenttä **Yritykset**-sivulla.  

## <a name="work-date"></a>Käsittelypvm
Oletuskäsittelypäivä on yleensä kuluvan päivän päivämäärä. Saatat joutua muuttamaan käsittelypäivämäärän väliaikaisesti, jotta voit suorittaa tehtäviä, kuten sellaisten tapahtumien täydentäminen, joiden päivämäärä ei ole kuluvan päivän päivämäärä.

> [!TIP]  
>   Kirjoita **w**, kun haluat antaa käsittelypäivämäärän nopeasti päivämääräkenttään. Kirjoita **t**, kun haluat syöttää nopeasti nykyisen päivämäärän päivämääräkenttään.

> [!IMPORTANT]  
>   Käsittelypäivämäärää muutetaan vain siihen asti, kunnes yritys suljetaan, tai siihen asti, kunnes päivämäärä muuttuu. Jos avaat toisen yrityksen tai jos avaat saman yrityksen uudestaan seuraavana päivänä, käsittelypäivämäärä täytyy määrittää uudestaan, jos tarvitset vielä järjestelmäpäivämäärästä poikkeavan päivämäärän.

## <a name="region"></a>Alue
**Alue**-asetus määrittää, miten päivämäärät, ajat, luvut ja valuutat näkyvät tai miten ne on muotoiltu.   

## <a name="changing-when-i-receive-notifications"></a>Ilmoitusten vastaanoton ajankohta-asetusten muuttaminen
Valitsemalla tämän linkin voit tarkastella tai muuttaa ilmoituksia, joita saat tietyistä tapahtumista tai tilamuutoksista esimerkiksi silloin, kun olet laskuttamassa asiakasta, jolla on erääntynyttä saldoa, tai kun käytettävissä oleva varasto on pienempi kuin myytävä määrä. Lisätietoja on kohdassa [Älykkäät ilmoitukset](ui-smart-notifications.md).

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Roolikeskuksen vaihtaminen](change-role.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttökokemuksen mukauttaminen](ui-experiences.md)  

