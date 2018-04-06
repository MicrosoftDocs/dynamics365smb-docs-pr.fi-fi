---
title: "Käyttäjien ja roolien hallinta | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten Finance and Operations, Business editionin käyttäjiä ja roolikeskuksia hallitaan."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/02/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f8f00e7db1f7594d66e1cae5ed98271e25295472
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="0a7ba-103">Tietoja käyttäjistä, profiileista ja roolikeskuksista</span><span class="sxs-lookup"><span data-stu-id="0a7ba-103">Understanding Users, Profiles, and Role Centers</span></span>
<span data-ttu-id="0a7ba-104">Kaikilla yrityksen henkilöille, joilla on [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeus, on määritetty *profiili*, jonka mahdollistaa *roolikeskuksen* käytön.</span><span class="sxs-lookup"><span data-stu-id="0a7ba-104">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span> <span data-ttu-id="0a7ba-105">Järjestelmänvalvojana voit määrittää ja muuttaa profiileja [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilaus sallii myös käyttäjien lisäämisen ja poistamisen.</span><span class="sxs-lookup"><span data-stu-id="0a7ba-105">As an administrator, you can assign and change profiles in [!INCLUDE[d365fin](includes/d365fin_md.md)], and you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="0a7ba-106">Käyttäjien lisääminen</span><span class="sxs-lookup"><span data-stu-id="0a7ba-106">Adding Users</span></span>
<span data-ttu-id="0a7ba-107">Käyttäjiä voi lisätä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin sen jälkeen, kun yrityksen Office 365:n järjestelmänvalvoja on ensin luonut käyttäjät Office 365:n hallintaportaalissa.</span><span class="sxs-lookup"><span data-stu-id="0a7ba-107">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)], your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="0a7ba-108">Lisätietoja on kohdassa [Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="0a7ba-108">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

## <a name="profiles"></a><span data-ttu-id="0a7ba-109">Profiilit</span><span class="sxs-lookup"><span data-stu-id="0a7ba-109">Profiles</span></span>
<span data-ttu-id="0a7ba-110">Profiilit ovat niiden [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjien kokoelmia, jotka jakavat saman roolikeskuksen.</span><span class="sxs-lookup"><span data-stu-id="0a7ba-110">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="0a7ba-111">Roolikeskus on sivu, jossa voit sijoittaa eri osia.</span><span class="sxs-lookup"><span data-stu-id="0a7ba-111">A Role Center is a type of page on which you can place different parts.</span></span> <span data-ttu-id="0a7ba-112">Jokainen osa on säilö, joka voi sisältää muita sivuja tai ennalta määritettyjä järjestelmän osia, kuten Outlook-osan tai osia tehtävien, ilmoitusten tai huomautusten lisäämiseksi.</span><span class="sxs-lookup"><span data-stu-id="0a7ba-112">Each part is a container in which you can host other pages or pre-defined system parts, such as an Outlook part or parts for adding tasks, notifications, or notes.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0a7ba-113">Et voi lisätä, muokata tai poistaa profiileja [!INCLUDE[d365fin](includes/d365fin_md.md)]in nykyisessä versiossa.</span><span class="sxs-lookup"><span data-stu-id="0a7ba-113">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="0a7ba-114">Kokoonpano ja mukautus</span><span class="sxs-lookup"><span data-stu-id="0a7ba-114">Configuration and Personalization</span></span>
<span data-ttu-id="0a7ba-115">Käyttöliittymän muokkauksen konsepti [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa on jaettu kahtia:</span><span class="sxs-lookup"><span data-stu-id="0a7ba-115">The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:</span></span>  

-   <span data-ttu-id="0a7ba-116">Järjestelmänvalvojan suorittama määritys</span><span class="sxs-lookup"><span data-stu-id="0a7ba-116">Configuration, performed by the administrator</span></span>  

-   <span data-ttu-id="0a7ba-117">Mukauttaminen, käyttäjien suorittama</span><span class="sxs-lookup"><span data-stu-id="0a7ba-117">Personalization, performed by users</span></span>  

<span data-ttu-id="0a7ba-118">Järjestelmänvalvoja konfiguroi käyttöliittymän useille käyttäjille muokkaamalla käyttöliittymän profiilille, johon käyttäjät ovat kirjautuneet.</span><span class="sxs-lookup"><span data-stu-id="0a7ba-118">The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.</span></span>  

<span data-ttu-id="0a7ba-119">Käyttäjät voivat mukauttaa henkilökohtaisen versionsa käyttöliittymää mukauttamalla käyttöliittymää oman kirjautumistunnuksensa osalta.</span><span class="sxs-lookup"><span data-stu-id="0a7ba-119">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="0a7ba-120">Järjestelmänvalvoja voi poistaa tämän mukautuksen.</span><span class="sxs-lookup"><span data-stu-id="0a7ba-120">This personalization can be deleted by the administrator.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0a7ba-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0a7ba-121">See Also</span></span>  
[<span data-ttu-id="0a7ba-122">Käyttäjien ja käyttöoikeuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="0a7ba-122">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
<!-- [Customize the User Interface](../customize-the-user-interface.md)   
 [Security Overview](../Security%20Overview.md)-->

