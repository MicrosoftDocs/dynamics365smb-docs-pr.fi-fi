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
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b06c5ee737db74e5011c7854601a21bc04d8872a
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="users-profiles-and-role-centers-in-finance-and-operations-business-edition"></a><span data-ttu-id="1ce0c-103">Finance and Operations, Business editionin käyttäjät, profiilit ja roolikeskukset</span><span class="sxs-lookup"><span data-stu-id="1ce0c-103">Users, Profiles, and Role Centers in Finance and Operations, Business edition</span></span>
<span data-ttu-id="1ce0c-104">Kaikilla yrityksen henkilöille, joilla on [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeus, on määritetty *profiili*, jonka mahdollistaa *roolikeskuksen* käytön.</span><span class="sxs-lookup"><span data-stu-id="1ce0c-104">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span> <span data-ttu-id="1ce0c-105">Järjestelmänvalvojana voit määrittää ja muuttaa profiileja [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilaus sallii myös käyttäjien lisäämisen ja poistamisen.</span><span class="sxs-lookup"><span data-stu-id="1ce0c-105">As an administrator, you can assign and change profiles in [!INCLUDE[d365fin](includes/d365fin_md.md)], and you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="1ce0c-106">Käyttäjien lisääminen</span><span class="sxs-lookup"><span data-stu-id="1ce0c-106">Adding Users</span></span>
<span data-ttu-id="1ce0c-107">Käyttäjiä voi lisätä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin sen jälkeen, kun yrityksen Office 365:n järjestelmänvalvoja on ensin luonut käyttäjät Office 365:n hallintaportaalissa.</span><span class="sxs-lookup"><span data-stu-id="1ce0c-107">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)], your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="1ce0c-108">Lisätietoja on kohdassa [Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="1ce0c-108">For more information, see [Manage Users and Permissions](ui-how-users-permissions.md).</span></span>  

## <a name="profiles"></a><span data-ttu-id="1ce0c-109">Profiilit</span><span class="sxs-lookup"><span data-stu-id="1ce0c-109">Profiles</span></span>
<span data-ttu-id="1ce0c-110">Profiilit ovat niiden [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjien kokoelmia, jotka jakavat saman roolikeskuksen.</span><span class="sxs-lookup"><span data-stu-id="1ce0c-110">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="1ce0c-111">Roolikeskus on sivu, jossa voit sijoittaa eri osia.</span><span class="sxs-lookup"><span data-stu-id="1ce0c-111">A Role Center is a type of page on which you can place different parts.</span></span> <span data-ttu-id="1ce0c-112">Jokainen osa on säilö, joka voi sisältää muita sivuja tai ennalta määritettyjä järjestelmän osia, kuten Outlook-osan tai osia tehtävien, ilmoitusten tai huomautusten lisäämiseksi.</span><span class="sxs-lookup"><span data-stu-id="1ce0c-112">Each part is a container in which you can host other pages or pre-defined system parts, such as an Outlook part or parts for adding tasks, notifications, or notes.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1ce0c-113">Et voi lisätä, muokata tai poistaa profiileja [!INCLUDE[d365fin](includes/d365fin_md.md)]in nykyisessä versiossa.</span><span class="sxs-lookup"><span data-stu-id="1ce0c-113">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="1ce0c-114">Kokoonpano ja mukautus</span><span class="sxs-lookup"><span data-stu-id="1ce0c-114">Configuration and Personalization</span></span>
<span data-ttu-id="1ce0c-115">Käyttöliittymän muokkauksen konsepti [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa on jaettu kahtia:</span><span class="sxs-lookup"><span data-stu-id="1ce0c-115">The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:</span></span>  

-   <span data-ttu-id="1ce0c-116">Järjestelmänvalvojan suorittama määritys</span><span class="sxs-lookup"><span data-stu-id="1ce0c-116">Configuration, performed by the administrator</span></span>  

-   <span data-ttu-id="1ce0c-117">Mukauttaminen, käyttäjien suorittama</span><span class="sxs-lookup"><span data-stu-id="1ce0c-117">Personalization, performed by users</span></span>  

<span data-ttu-id="1ce0c-118">Järjestelmänvalvoja konfiguroi käyttöliittymän useille käyttäjille muokkaamalla käyttöliittymän profiilille, johon käyttäjät ovat kirjautuneet.</span><span class="sxs-lookup"><span data-stu-id="1ce0c-118">The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.</span></span>  

<span data-ttu-id="1ce0c-119">Käyttäjät voivat mukauttaa henkilökohtaisen versionsa käyttöliittymää mukauttamalla käyttöliittymää oman kirjautumistunnuksensa osalta.</span><span class="sxs-lookup"><span data-stu-id="1ce0c-119">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="1ce0c-120">Järjestelmänvalvoja voi poistaa tämän mukautuksen.</span><span class="sxs-lookup"><span data-stu-id="1ce0c-120">This personalization can be deleted by the administrator.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1ce0c-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1ce0c-121">See Also</span></span>  
[<span data-ttu-id="1ce0c-122">Käyttäjien ja käyttöoikeuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="1ce0c-122">Manage Users and Permissions</span></span>](ui-how-users-permissions.md)  
<!-- [Customize the User Interface](../customize-the-user-interface.md)   
 [Security Overview](../Security%20Overview.md)-->

