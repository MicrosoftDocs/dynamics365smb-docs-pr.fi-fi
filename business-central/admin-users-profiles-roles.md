---
title: "Käyttäjien ja roolien hallinta | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten Business Central -sovelluksen käyttäjiä ja roolikeskuksia hallitaan."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 06/20/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 3331849cf94c70d0597ae5f37d3109451947c9fc
ms.openlocfilehash: 6d1b6a31bb4476471ccd1f351291f6fcec34d556
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="482b6-103">Tietoja käyttäjistä, profiileista ja roolikeskuksista</span><span class="sxs-lookup"><span data-stu-id="482b6-103">Understanding Users, Profiles, and Role Centers</span></span>
<span data-ttu-id="482b6-104">Kaikilla yrityksen henkilöille, joilla on [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeus, on määritetty *profiili*, jonka mahdollistaa *roolikeskuksen* käytön.</span><span class="sxs-lookup"><span data-stu-id="482b6-104">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span> <span data-ttu-id="482b6-105">Järjestelmänvalvojana voit lisätä ja poistaa käyttäjiä [!INCLUDE[d365fin](includes/d365fin_md.md)] -tilauksesta. Voit myös määrittää käyttäjien oikeuksia käyttäjäryhmien avulla.</span><span class="sxs-lookup"><span data-stu-id="482b6-105">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="482b6-106">Käyttäjien lisääminen</span><span class="sxs-lookup"><span data-stu-id="482b6-106">Adding Users</span></span>
<span data-ttu-id="482b6-107">Käyttäjiä voi lisätä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin sen jälkeen, kun yrityksen Office 365:n järjestelmänvalvoja on ensin luonut käyttäjät Office 365:n hallintaportaalissa.</span><span class="sxs-lookup"><span data-stu-id="482b6-107">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)], your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="482b6-108">Tämän jälkeen järjestelmänvalvoja voi määrittää käyttöoikeudet kullekin käyttäjälle ja käyttäjäryhmälle.</span><span class="sxs-lookup"><span data-stu-id="482b6-108">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="482b6-109">Lisätietoja on kohdassa [Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="482b6-109">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

## <a name="profiles"></a><span data-ttu-id="482b6-110">Profiilit</span><span class="sxs-lookup"><span data-stu-id="482b6-110">Profiles</span></span>
<span data-ttu-id="482b6-111">Profiilit ovat niiden [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjien kokoelmia, jotka jakavat saman roolikeskuksen.</span><span class="sxs-lookup"><span data-stu-id="482b6-111">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span>  <span data-ttu-id="482b6-112">Roolikeskus on [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen aloituskohta ja kotisivu. Sen avulla tärkeimpien tehtävien aloitus on nopeaa ja se sisältää paljon tietoja työstä, mukaan lukien työn suorituskykyilmaisimet.</span><span class="sxs-lookup"><span data-stu-id="482b6-112">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="482b6-113">Et voi lisätä, muokata tai poistaa profiileja [!INCLUDE[d365fin](includes/d365fin_md.md)]in nykyisessä versiossa.</span><span class="sxs-lookup"><span data-stu-id="482b6-113">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you cannot add, edit, or delete profiles.</span></span>

## <a name="configuration-and-personalization"></a><span data-ttu-id="482b6-114">Kokoonpano ja mukautus</span><span class="sxs-lookup"><span data-stu-id="482b6-114">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
<span data-ttu-id="482b6-115">Käyttäjät voivat mukauttaa henkilökohtaisen versionsa käyttöliittymää mukauttamalla käyttöliittymää oman kirjautumistunnuksensa osalta.</span><span class="sxs-lookup"><span data-stu-id="482b6-115">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="482b6-116">Järjestelmänvalvoja voi poistaa tämän mukautuksen.</span><span class="sxs-lookup"><span data-stu-id="482b6-116">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="482b6-117">Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="482b6-117">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="482b6-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="482b6-118">See Also</span></span>  
[<span data-ttu-id="482b6-119">Käyttäjien ja käyttöoikeuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="482b6-119">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="482b6-120">Mukautuksen hallinta järjestelmänvalvojana</span><span class="sxs-lookup"><span data-stu-id="482b6-120">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="482b6-121">Työtilan mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="482b6-121">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  

