---
title: Roolien sivujen mukauttaminen | Microsoft Docs
description: Lisätietoja profiilin (roolin) käyttöliittymän mukauttamisesta siten, että kaikki käyttäjät, joille kyseinen rooli on määritetty, näkevät mukautetun työtilan.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: cee71cea69468a45b2e731632fce3827c54794c1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781333"
---
# <a name="customize-pages-for-profiles"></a><span data-ttu-id="d4484-103">Profiilien sivujen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="d4484-103">Customize Pages for Profiles</span></span>
<span data-ttu-id="d4484-104">Käyttäjät voivat mukauttaa työtilan muodostavia sivuja omien mieltymystensä mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="d4484-104">Users can personalize pages that make up their workspace to suit their own preferences.</span></span> <span data-ttu-id="d4484-105">Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="d4484-105">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

<span data-ttu-id="d4484-106">Järjestelmänvalvojat voivat mukauttaa profiilin sivuja liittyvän liiketoimintaroolin tai osaston mukaisesti esimerkiksi siten, että kaikki käyttäjät, joille profiili on määritetty, näkevät mukautetun sivuasettelun.</span><span class="sxs-lookup"><span data-stu-id="d4484-106">Administrators can customize pages for a profile, according to the related business role or department, for example, so that all users that are assigned the profile will see the customized page layout.</span></span> <span data-ttu-id="d4484-107">Järjestelmänvalvoja mukauttaa sivuja samalla toiminnolla, jota käyttäjät mukauttavat sivuja.</span><span class="sxs-lookup"><span data-stu-id="d4484-107">The administrator customizes pages by using the same functionality as users do when they personalize pages.</span></span>

> [!NOTE]
> <span data-ttu-id="d4484-108">Tyypillinen profiilin käyttötapa liiketoiminnassa on rooli.</span><span class="sxs-lookup"><span data-stu-id="d4484-108">The typical business use of a profile is a role.</span></span> <span data-ttu-id="d4484-109">Profiilin nimi onkin käyttöliittymässä tämän vuoksi *Profiili (rooli)*.</span><span class="sxs-lookup"><span data-stu-id="d4484-109">A profile is therefore named *Profile (Role)* in the UI.</span></span>

<span data-ttu-id="d4484-110">Sivun mukauttaminen aloitetaan **Profiilit (roolit)** -sivulla, josta järjestelmänvalvojat aloittavat yksittäisten profiilikorttien käyttäjien profiilien hallinnan.</span><span class="sxs-lookup"><span data-stu-id="d4484-110">Page customization starts from the **Profiles (Roles)** page, the administrator's starting point for managing users' profiles on individual profile cards.</span></span> <span data-ttu-id="d4484-111">Sivun asettelun mukauttamisen lisäksi voi kunkin profiilin **Profiili (rooli)** -sivulla voi hallita useita muita profiilien asetuksia.</span><span class="sxs-lookup"><span data-stu-id="d4484-111">In addition to customizing the page layout, you control various other settings for profiles on the **Profile (Role)** page for each profile.</span></span> <span data-ttu-id="d4484-112">Lisätietoja on kohdassa [Profiilien hallinta](admin-users-profiles-roles.md).</span><span class="sxs-lookup"><span data-stu-id="d4484-112">For more information, see [Manage Profiles](admin-users-profiles-roles.md).</span></span>

## <a name="to-customize-pages-for-a-profile"></a><span data-ttu-id="d4484-113">Profiilin sivujen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="d4484-113">To customize pages for a profile</span></span>
1. <span data-ttu-id="d4484-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Profiilit (Roolit)** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="d4484-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles (Roles)**, and then choose the related link.</span></span>
2. <span data-ttu-id="d4484-115">Valitse ensin sen profiilin rivi, jonka sivuja haluat mukauttaa, ja valitse sitten **Muokkaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d4484-115">Select the line for the profile that you want to customize pages for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="d4484-116">Valitse **Mukauta sivuja** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d4484-116">Choose the **Customize pages** action.</span></span>

    [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d4484-117">avaa valitun profiilin uudessa selaimen välilehdessä siten, että **Mukauttaminen**-palkki on aktivoitu.</span><span class="sxs-lookup"><span data-stu-id="d4484-117">opens on a new browser tab for the selected profile with the **Customizing** banner activated.</span></span> <span data-ttu-id="d4484-118">**Mukauttaminen**-palkissa on samat toiminnot kuin käyttäjien käyttämässä **Mukautus**-palkissa.</span><span class="sxs-lookup"><span data-stu-id="d4484-118">The **Customizing** banner offers the same functionality as the **Personalizing** banner that is available to users.</span></span>

4. <span data-ttu-id="d4484-119">Mukauta sivuja kyseisen roolin tai osaston tarpeiden mukaan samalla tavoin kuin käyttäjä tekee omat mukautuksensa.</span><span class="sxs-lookup"><span data-stu-id="d4484-119">Customize pages according to the needs of the role or department in question in the same way as a user would do when personalizing.</span></span> <span data-ttu-id="d4484-120">Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="d4484-120">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

    > [!NOTE]
    > <span data-ttu-id="d4484-121">Voit siirtyä mukauttamisen aikana käyttämällä toiminnossa CTRL+napsautus-yhdistelmää, jos nuolenpää osoittaa toiminnon olevan valittuna.</span><span class="sxs-lookup"><span data-stu-id="d4484-121">To navigate during personalization, use Ctrl + Click on an action if it is highlighted by the arrowhead.</span></span>

5. <span data-ttu-id="d4484-122">Kun olet muuttanut yhden tai usean sivun asettelua, valitse**Mukauttaminen**-palkissa **Valmis**-painike.</span><span class="sxs-lookup"><span data-stu-id="d4484-122">When you have finished changing the layout on one or more pages, choose the **Done** button on the **Customizing** banner.</span></span>
6. <span data-ttu-id="d4484-123">Sulje selaimen välilehti.</span><span class="sxs-lookup"><span data-stu-id="d4484-123">Close the browser tab.</span></span>

<span data-ttu-id="d4484-124">Sivujen mukauttaminen on nyt tallennettu profiiliin.</span><span class="sxs-lookup"><span data-stu-id="d4484-124">The customization of pages is now recorded for the profile.</span></span>

## <a name="to-view-all-customized-pages-for-a-profile"></a><span data-ttu-id="d4484-125">Kaikkien profiilin mukautettujen sivujen näyttäminen</span><span class="sxs-lookup"><span data-stu-id="d4484-125">To view all customized pages for a profile</span></span>
<span data-ttu-id="d4484-126">Saat tarvittaessa yleiskuvan profiiliin mukautetuista sivuista, mikä auttaa suunnittelemaan esimerkiksi sivujen lisämukautuksia tai poistamisia.</span><span class="sxs-lookup"><span data-stu-id="d4484-126">You can get an overview of which pages are customized for a profile, for example to plan which to customize further or delete.</span></span>

- <span data-ttu-id="d4484-127">Valitse **Profiili (rooli)** -sivulla **Mukautetut sivut** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d4484-127">On the **Profile (Role)** page, choose the **Customized Pages** action.</span></span>

## <a name="to-delete-all-customizations-for-a-profile"></a><span data-ttu-id="d4484-128">Profiilin kaikkien mukautusten poistaminen</span><span class="sxs-lookup"><span data-stu-id="d4484-128">To delete all customizations for a profile</span></span>
<span data-ttu-id="d4484-129">Voit peruuttaa kaikki profiiliin tehdyt mukautukset.</span><span class="sxs-lookup"><span data-stu-id="d4484-129">You can cancel all customizations that you have made for a profile.</span></span> <span data-ttu-id="d4484-130">Laajennukseen perustuvia mukautuksia ja käyttäjän tekemiä mukautuksia ei poisteta.</span><span class="sxs-lookup"><span data-stu-id="d4484-130">Customizations introduced with an extension and personalizations made by a user will not be deleted.</span></span> <span data-ttu-id="d4484-131">Voit poistaa kaikki mukautukset toisella toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="d4484-131">You can delete all personalizations with another action.</span></span> <span data-ttu-id="d4484-132">Lisätietoja on kohdassa [Kaikkien käyttäjän tekemien mukautusten poistaminen](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).</span><span class="sxs-lookup"><span data-stu-id="d4484-132">For more information, see [To delete all personalizations made by a user](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).</span></span>

- <span data-ttu-id="d4484-133">Valitse mukautetun profiilin **Profiili (rooli)** -sivulla **Poista mukautetut sivut** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d4484-133">On the **Profile (Role)** page for a customized profile, choose the **Clear customized pages** action.</span></span>

<span data-ttu-id="d4484-134">Profiilin sivujen asetteluksi palautetaan oletusasettelu.</span><span class="sxs-lookup"><span data-stu-id="d4484-134">The layout on pages for the profile is reset to the default layout.</span></span>  

## <a name="to-delete-customization-for-specific-pages-for-a-profile"></a><span data-ttu-id="d4484-135">Profiilin tiettyjen sivujen mukautusten poistaminen</span><span class="sxs-lookup"><span data-stu-id="d4484-135">To delete customization for specific pages for a profile</span></span>
<span data-ttu-id="d4484-136">Voit poistaa profiilin yksittäisen sivun mukautukset.</span><span class="sxs-lookup"><span data-stu-id="d4484-136">You can delete individual page customizations that you have made for a profile.</span></span> <span data-ttu-id="d4484-137">Laajennukseen perustuvia mukautuksia ja käyttäjän tekemiä mukautuksia ei poisteta.</span><span class="sxs-lookup"><span data-stu-id="d4484-137">Customizations introduced with an extension and personalizations made by a user will not be deleted.</span></span> <span data-ttu-id="d4484-138">Voit poistaa tietyn sivun mukautukset toisella toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="d4484-138">You can delete specific page personalizations with another action.</span></span> <span data-ttu-id="d4484-139">Lisätietoja on kohdassa [Tiettyjen sivujen mukautusten poistaminen](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).</span><span class="sxs-lookup"><span data-stu-id="d4484-139">For more information, see [To delete personalizations for specific pages](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).</span></span>

1. <span data-ttu-id="d4484-140">Valitse **Profiili (rooli)** -sivulla **Mukautetut sivut** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="d4484-140">On the **Profile (Role)** page, choose the **Customized Pages** action.</span></span>
2. <span data-ttu-id="d4484-141">Valitse **Profiilin mukautukset** -sivulla vähintään yhden poistettavan sivun mukautuksen rivi ja valitse sitten **Poista**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="d4484-141">On the **Profile Customizations** page, select on or more lines for page customizations that you want to delete, and then choose the **Delete** action.</span></span>

<span data-ttu-id="d4484-142">Valitun sivun asettelu muutetaan vastaamaan tekemiäsi muutoksia.</span><span class="sxs-lookup"><span data-stu-id="d4484-142">The layout on the selected pages is adjusted to the changes you made.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4484-143">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d4484-143">See Also</span></span>
[<span data-ttu-id="d4484-144">Työtilan mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="d4484-144">Personalize Your Workspace</span></span>](ui-personalization-user.md)  
[<span data-ttu-id="d4484-145">Profiilien hallinta</span><span class="sxs-lookup"><span data-stu-id="d4484-145">Manage Profiles</span></span>](admin-users-profiles-roles.md)  
[<span data-ttu-id="d4484-146">Perusasetusten muuttaminen</span><span class="sxs-lookup"><span data-stu-id="d4484-146">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="d4484-147">Näytettävien ominaisuuksien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="d4484-147">Change Which Features are Displayed</span></span>](ui-experiences.md)  
<span data-ttu-id="d4484-148">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d4484-148">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
