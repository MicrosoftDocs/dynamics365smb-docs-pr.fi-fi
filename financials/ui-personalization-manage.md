---
title: "Mukautusten hallinta Financialsin järjestelmänvalvojana | Microsoft Docs"
description: "Lisätietoja käyttöliittymän mukauttamisesta omaan työskentelytapaan sopivaksi."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4384aeb9a9e1e06ea7abc7b4eecdd1365ac2a0a0
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="b12b1-103">Mukautuksen hallinta järjestelmänvalvojana</span><span class="sxs-lookup"><span data-stu-id="b12b1-103">Managing Personalization as an Administrator</span></span>
<!--NAV in the Web client-->
<span data-ttu-id="b12b1-104">Käyttäjät voivat mukauttaa työtilansa omien mieltymystensä mukaiseksi.</span><span class="sxs-lookup"><span data-stu-id="b12b1-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="b12b1-105">Järjestelmänvalvojana voit ohjata ja hallita mukauttamista poistamalla sivujen mukautusmahdollisuus käyttäjiltä ja poistamalla käyttäjien mahdollisesti tekemät mukautukset.</span><span class="sxs-lookup"><span data-stu-id="b12b1-105">As an administrator, you can control and manage personalization by disabling the ability for users to personalize pages and clearing any page personalizations that users have made.</span></span> 

## <a name="disable-personalization-for-a-profile"></a><span data-ttu-id="b12b1-106">Profiilin mukauttamisen poistaminen</span><span class="sxs-lookup"><span data-stu-id="b12b1-106">Disable personalization for a profile</span></span>
<span data-ttu-id="b12b1-107">Voit estää sivujen mukauttamisen kaikilta tiettyyn profiiliin kuuluvilta käyttäjiltä.</span><span class="sxs-lookup"><span data-stu-id="b12b1-107">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>
1.  <span data-ttu-id="b12b1-108">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Profiilit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b12b1-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profiles**, and then choose the related link.</span></span>
2.  <span data-ttu-id="b12b1-109">Valitse luettelossa muokattava profiili.</span><span class="sxs-lookup"><span data-stu-id="b12b1-109">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="b12b1-110">Valitse **Poista mukauttaminen käytöstä** -valintaruutuja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="b12b1-110">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="clear-user-personalizations"></a><span data-ttu-id="b12b1-111">Käyttäjän mukautusten tyhjentäminen</span><span class="sxs-lookup"><span data-stu-id="b12b1-111">Clear user personalizations</span></span>

<span data-ttu-id="b12b1-112">Mukautetun sivun muutosten tyhjentäminen palauttaa sivun mukautuksia edeltävän alkuperäisen asettelun.</span><span class="sxs-lookup"><span data-stu-id="b12b1-112">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="b12b1-113">Käyttäjien sivulle tekemät mukautukset voi tyhjentää kahdella tavalla: käyttämällä **Poista käyttäjän mukautus** -sivua tai käyttämällä **Käyttäjän mukautuskortti** -sivua.</span><span class="sxs-lookup"><span data-stu-id="b12b1-113">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span> 

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="b12b1-114">Käyttäjän mukautusten tyhjentäminen Poista käyttäjän mukautus -sivun avulla</span><span class="sxs-lookup"><span data-stu-id="b12b1-114">Clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="b12b1-115">Voit tyhjentää **Poista käyttäjän mukautus** -sivulla mukautukset kultakin käyttäjältä sivukohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="b12b1-115">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span> 

1.  <span data-ttu-id="b12b1-116">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Poista käyttäjän mukautus** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b12b1-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="b12b1-117">Sivulla on luettelo kaikista mukautetuista sivuista ja käyttäjästä, jolle se kuuluu.</span><span class="sxs-lookup"><span data-stu-id="b12b1-117">The page lists all the pages that have been personalized and the user it belongs to.</span></span> 

    >[!NOTE]
    > <span data-ttu-id="b12b1-118">**Vanha mukautus** -sarakkeiden valintamerkki ilmaisee, että mukautus tehtiin [!INCLUDE[d365fin](includes/d365fin_md.md)]in vanhassa versiossa, jossa mukautusta käsiteltiin eri tavalla kuin nyt.</span><span class="sxs-lookup"><span data-stu-id="b12b1-118">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="b12b1-119">Mukautus estetään näiden sivujen mukautusta yrittäviltä käyttäjiltä, elleivät he ensin valitse sivun lukituksen poistamista.</span><span class="sxs-lookup"><span data-stu-id="b12b1-119">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="b12b1-120">Lisätietoja on kohdassa [Sivun mukauttamisen estäminen lukitsemalla](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="b12b1-120">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="b12b1-121">Valitse ensin poistettava tapahtuma ja sitten **Poista**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="b12b1-121">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="b12b1-122">Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.</span><span class="sxs-lookup"><span data-stu-id="b12b1-122">The user will see the changes the next time they sign-in.</span></span>

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="b12b1-123">Käyttäjän mukautusten tyhjentäminen Käyttäjän mukautuskortti -sivun avulla</span><span class="sxs-lookup"><span data-stu-id="b12b1-123">Clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="b12b1-124">Voit tyhjentää **Käyttäjän mukautuskortti** -sivulla tietyn käyttäjän kaikki mukautukset.</span><span class="sxs-lookup"><span data-stu-id="b12b1-124">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="b12b1-125">Tämä edellyttää taulukon 2000000072 **Profiili** kirjoitusoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="b12b1-125">This requires write permission to Table 2000000072 **Profile**.</span></span>

1.  <span data-ttu-id="b12b1-126">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Käyttäjän mukautus** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="b12b1-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="b12b1-127">**Käyttäjän mukautus** -sivulla on luettelo kaikista käyttäjistä, joilla mahdollisesti on mukautettuja sivuja.</span><span class="sxs-lookup"><span data-stu-id="b12b1-127">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="b12b1-128">Jos käyttäjä ei löydy luettelosta, kyseisellä käyttäjällä ei ole mukautettuja sivuja.</span><span class="sxs-lookup"><span data-stu-id="b12b1-128">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span> 

2. <span data-ttu-id="b12b1-129">Valitse ensin käyttäjä luettelossa ja sitten **Muokkaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="b12b1-129">Select the user from the list, and then choose the **Edit** action.</span></span>

3.  <span data-ttu-id="b12b1-130">Valitse **Toiminnot**-välilehdessä **Tyhjennä mukautetut sivut**.</span><span class="sxs-lookup"><span data-stu-id="b12b1-130">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="b12b1-131">Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.</span><span class="sxs-lookup"><span data-stu-id="b12b1-131">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="b12b1-132">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b12b1-132">See Also</span></span>
[<span data-ttu-id="b12b1-133">Työtilan mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="b12b1-133">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="b12b1-134">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b12b1-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="b12b1-135">Roolikeskuksen vaihtaminen</span><span class="sxs-lookup"><span data-stu-id="b12b1-135">Change the Role Center</span></span>](change-role.md)  
<span data-ttu-id="b12b1-136">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttökokemuksen mukauttaminen](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="b12b1-136">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  

