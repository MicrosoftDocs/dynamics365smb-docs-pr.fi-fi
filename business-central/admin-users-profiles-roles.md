---
title: "Käyttäjien ja roolien hallinta | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten Business Central -sovelluksen käyttäjiä ja roolikeskuksia hallitaan."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a>Tietoja käyttäjistä, profiileista ja roolikeskuksista

[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa järjestelmänvalvoja lisää käyttäjät ja antaa käyttäjille [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen niiden alueiden käyttöoikeuden, joita käyttäjät tarvitsevat työssään.  

Toimintojen käyttöä hallitaan *käyttäjäryhmien* ja *profiilien* avulla. Järjestelmänvalvojana voit lisätä ja poistaa käyttäjiä [!INCLUDE[d365fin](includes/d365fin_md.md)] -tilauksesta. Voit myös määrittää käyttäjien oikeuksia käyttäjäryhmien avulla.  

## <a name="adding-users"></a>Käyttäjien lisääminen

Käyttäjiä voi lisätä [!INCLUDE[d365fin](includes/d365fin_md.md)] online -versioon sen jälkeen, kun yrityksen Office 365:n järjestelmänvalvoja on ensin luonut käyttäjät Office 365:n hallintaportaalissa. Lisätietoja on kohdassa [Käyttäjien lisääminen Office 365 for Businessiin](https://aka.ms/CreateOffice365Users).

Tämän jälkeen järjestelmänvalvoja voi määrittää käyttöoikeudet kullekin käyttäjälle ja käyttäjäryhmälle. Lisätietoja on kohdassa [Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).  

### <a name="users-of-on-premises-deployments"></a>Paikallisten käyttöönottojen käyttäjät

Järjestelmänvalvoja voi valita käyttäjille [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen paikallisten käyttöönottojen eri tunnistetietojen mekanismeista. Kun olet luonut käyttäjän, annat eri tietoja riippuen tunnistetiedoista, joita käytät tietyssä [!INCLUDE[server](includes/server.md)] -ilmentymässä. Lisätietoja on [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen kehittäjän ja ITPro-sisällön järjestelmänvalvojan osan [Todennus ja tunnistetietotyypit](/dynamics365/business-central/dev-itpro/administration/users-credential-types) -kohdassa.  

## <a name="profiles"></a>Profiilit

Kaikilla yrityksen henkilöille, joilla on [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeus, on määritetty *profiili*, jonka mahdollistaa *roolikeskuksen* käytön.

Profiilit ovat niiden [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjien kokoelmia, jotka jakavat saman roolikeskuksen. Roolikeskus on [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen aloituskohta ja kotisivu. Sen avulla tärkeimpien tehtävien aloitus on nopeaa ja se sisältää paljon tietoja työstä, mukaan lukien työn suorituskykyilmaisimet.  

> [!NOTE]  
>  Et voi lisätä, muokata tai poistaa profiileja nykyisessä [!INCLUDE[d365fin](includes/d365fin_md.md)] online -versiossa.  

## <a name="configuration-and-personalization"></a>Kokoonpano ja mukautus
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
Käyttäjät voivat mukauttaa henkilökohtaisen versionsa käyttöliittymää mukauttamalla käyttöliittymää oman kirjautumistunnuksensa osalta. Järjestelmänvalvoja voi poistaa tämän mukautuksen. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).  

## <a name="see-also"></a>Katso myös  
[Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)  
[Mukautuksen hallinta järjestelmänvalvojana](ui-personalization-manage.md)  
[Työtilan mukauttaminen](ui-personalization-user.md)  

