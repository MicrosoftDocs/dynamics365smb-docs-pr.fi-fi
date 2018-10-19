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
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="b048a-103">Tietoja käyttäjistä, profiileista ja roolikeskuksista</span><span class="sxs-lookup"><span data-stu-id="b048a-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="b048a-104">[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa järjestelmänvalvoja lisää käyttäjät ja antaa käyttäjille [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen niiden alueiden käyttöoikeuden, joita käyttäjät tarvitsevat työssään.</span><span class="sxs-lookup"><span data-stu-id="b048a-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="b048a-105">Toimintojen käyttöä hallitaan *käyttäjäryhmien* ja *profiilien* avulla.</span><span class="sxs-lookup"><span data-stu-id="b048a-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="b048a-106">Järjestelmänvalvojana voit lisätä ja poistaa käyttäjiä [!INCLUDE[d365fin](includes/d365fin_md.md)] -tilauksesta. Voit myös määrittää käyttäjien oikeuksia käyttäjäryhmien avulla.</span><span class="sxs-lookup"><span data-stu-id="b048a-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="b048a-107">Käyttäjien lisääminen</span><span class="sxs-lookup"><span data-stu-id="b048a-107">Adding Users</span></span>

<span data-ttu-id="b048a-108">Käyttäjiä voi lisätä [!INCLUDE[d365fin](includes/d365fin_md.md)] online -versioon sen jälkeen, kun yrityksen Office 365:n järjestelmänvalvoja on ensin luonut käyttäjät Office 365:n hallintaportaalissa.</span><span class="sxs-lookup"><span data-stu-id="b048a-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="b048a-109">Lisätietoja on kohdassa [Käyttäjien lisääminen Office 365 for Businessiin](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="b048a-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="b048a-110">Tämän jälkeen järjestelmänvalvoja voi määrittää käyttöoikeudet kullekin käyttäjälle ja käyttäjäryhmälle.</span><span class="sxs-lookup"><span data-stu-id="b048a-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="b048a-111">Lisätietoja on kohdassa [Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="b048a-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="b048a-112">Paikallisten käyttöönottojen käyttäjät</span><span class="sxs-lookup"><span data-stu-id="b048a-112">Users of on-premises deployments</span></span>

<span data-ttu-id="b048a-113">Järjestelmänvalvoja voi valita käyttäjille [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen paikallisten käyttöönottojen eri tunnistetietojen mekanismeista.</span><span class="sxs-lookup"><span data-stu-id="b048a-113">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="b048a-114">Kun olet luonut käyttäjän, annat eri tietoja riippuen tunnistetiedoista, joita käytät tietyssä [!INCLUDE[server](includes/server.md)] -ilmentymässä.</span><span class="sxs-lookup"><span data-stu-id="b048a-114">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="b048a-115">Lisätietoja on [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen kehittäjän ja ITPro-sisällön järjestelmänvalvojan osan [Todennus ja tunnistetietotyypit](/dynamics365/business-central/dev-itpro/administration/users-credential-types) -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="b048a-115">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="b048a-116">Profiilit</span><span class="sxs-lookup"><span data-stu-id="b048a-116">Profiles</span></span>

<span data-ttu-id="b048a-117">Kaikilla yrityksen henkilöille, joilla on [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeus, on määritetty *profiili*, jonka mahdollistaa *roolikeskuksen* käytön.</span><span class="sxs-lookup"><span data-stu-id="b048a-117">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="b048a-118">Profiilit ovat niiden [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjien kokoelmia, jotka jakavat saman roolikeskuksen.</span><span class="sxs-lookup"><span data-stu-id="b048a-118">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="b048a-119">Roolikeskus on [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen aloituskohta ja kotisivu. Sen avulla tärkeimpien tehtävien aloitus on nopeaa ja se sisältää paljon tietoja työstä, mukaan lukien työn suorituskykyilmaisimet.</span><span class="sxs-lookup"><span data-stu-id="b048a-119">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b048a-120">Et voi lisätä, muokata tai poistaa profiileja nykyisessä [!INCLUDE[d365fin](includes/d365fin_md.md)] online -versiossa.</span><span class="sxs-lookup"><span data-stu-id="b048a-120">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="b048a-121">Kokoonpano ja mukautus</span><span class="sxs-lookup"><span data-stu-id="b048a-121">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
<span data-ttu-id="b048a-122">Käyttäjät voivat mukauttaa henkilökohtaisen versionsa käyttöliittymää mukauttamalla käyttöliittymää oman kirjautumistunnuksensa osalta.</span><span class="sxs-lookup"><span data-stu-id="b048a-122">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="b048a-123">Järjestelmänvalvoja voi poistaa tämän mukautuksen.</span><span class="sxs-lookup"><span data-stu-id="b048a-123">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="b048a-124">Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="b048a-124">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="b048a-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b048a-125">See Also</span></span>  
[<span data-ttu-id="b048a-126">Käyttäjien ja käyttöoikeuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="b048a-126">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="b048a-127">Mukautuksen hallinta järjestelmänvalvojana</span><span class="sxs-lookup"><span data-stu-id="b048a-127">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="b048a-128">Työtilan mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="b048a-128">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  

