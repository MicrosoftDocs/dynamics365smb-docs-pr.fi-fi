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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ed0a6848f07999246566ad740e02abfc561ae130
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="changing-basic-settings"></a>Perusasetusten muuttaminen
Voit tarkastella **Omat asetukset** -ikkunassa [!INCLUDE[d365fin](includes/d365fin_md.md)]in perusasetuksia ja muuttaa niitä.  

## <a name="role-center"></a>Roolikeskus
Roolikeskus edustaa kotisivua eli aloitussivua, joka on suunniteltu roolia varten. Kotisivu sisältää liiketoiminnan yleiskuvauksen. Vasemmalla olevan siirtymispalkin avulla voit helposti käsitellä asiakkaita, toimittajia, nimikkeitä jne.

Keskellä ovat toimenpideruudut. Toimenpiteet esittävät nykyiset tiedot. Valitun asiakirjan saa helposti käyttöön toimenpiteitä napsauttamalla tai napauttamalla. Suorituskykyilmaisimet voidaan määrittää niin, että ne näyttävät visuaalisesti esimerkiksi kassavirran tai tuottojen ja kulujen valitun kaavion.

Voit luoda kotisivulla myös suosikkiasiakkaiden luettelon niitä asiakkaita varten, joiden kanssa käyt kauppaa usein tai jotka vaativat erityishuomiota. Nuolten avulla voit supistaa osan sivusta, jolloin haluamillesi tiedoille jää enemmän tilaa. Kotisivun yläosassa ovat toiminnot, joita voit käyttää nykyisen sisällön käsittelemisessä. Sekin voidaan supistaa. Voit jatkaa supistetun alueen tarkastelemista napsauttamalla tai napauttamalla aluetta.

Oletusroolikeskus on **Liiketoimintajohtaja**, mutta voit valita tarvittaessa toisen roolikeskuksen. Lisätietoja on kohdassa [Toimintaohje: Roolikeskuksen vaihtaminen](change-role.md).

## <a name="company"></a>Oma yritys
Yritystoiminnot [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietojen säilönä. Tietokannassa voi olla useita yrityksiä. Kerralla on kuitenkin mahdollista valita vain yksi yritys.

Oletusyrityksen nimi on CRONUS, ja se sisältää vain esittelytietoja.

> [!TIP]  
>   Jos haluat, että yritys näkyy sovelluksessa toisella nimellä (esimerkiksi aloitussivulla), määritä **Nimi**-kenttä **Yritystiedot**-sivulla tai **Näyttönimi**-kenttä **Yritykset**-sivulla.  

## <a name="work-date"></a>Työn päivämäärä
Oletuskäsittelypäivä on yleensä kuluvan päivän päivämäärä. Saatat joutua muuttamaan käsittelypäivämäärän väliaikaisesti, jotta voit suorittaa tehtäviä, kuten sellaisten tapahtumien täydentäminen, joiden päivämäärä ei ole kuluvan päivän päivämäärä.

> [!TIP]  
>   Kirjoita **w**, kun haluat antaa käsittelypäivämäärän nopeasti päivämääräkenttään. Kirjoita **t**, kun haluat syöttää nopeasti nykyisen päivämäärän päivämääräkenttään.

> [!IMPORTANT]  
>   Käsittelypäivämäärää muutetaan vain siihen asti, kunnes yritys suljetaan, tai siihen asti, kunnes päivämäärä muuttuu. Jos avaat toisen yrityksen tai jos avaat saman yrityksen uudestaan seuraavana päivänä, käsittelypäivämäärä täytyy määrittää uudestaan, jos tarvitset vielä järjestelmäpäivämäärästä poikkeavan päivämäärän.

## <a name="confirmation-dialogs"></a>Vahvistusvalintaikkunat
Tämän osan vaihtoehtojen avulla voit määrittää asiakirjojen kirjaamiselle lisätarkistuksia. Vaihtoehdot on valittu oletusarvoisesti, mutta voit tyhjentää valintaruudut, jos haluat välttää tiettyjä varoituksia ja sanomia.

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Toimintaohje: Roolikeskuksen vaihtaminen](change-role.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttökokemuksen mukauttaminen](ui-experiences.md)  

