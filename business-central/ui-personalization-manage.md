---
title: Mukautusten hallinta Business Centralin järjestelmänvalvojana | Microsoft Docs
description: Lisätietoja käyttöliittymän mukauttamisesta omaan työskentelytapaan sopivaksi.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: ad3b4cf3be7031ab1c7c4699bed6020fe09bd2d1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795710"
---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="fdd17-103">Mukautuksen hallinta järjestelmänvalvojana</span><span class="sxs-lookup"><span data-stu-id="fdd17-103">Managing Personalization as an Administrator</span></span>
<span data-ttu-id="fdd17-104"><!--NAV in the Web client--> Käyttäjät voivat mukauttaa työtilansa omien mieltymystensä mukaiseksi.</span><span class="sxs-lookup"><span data-stu-id="fdd17-104"><!--NAV in the Web client--> Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="fdd17-105">Järjestelmänvalvojana voit ohjata ja hallita mukauttamista poistamalla sivujen mukautusmahdollisuus käyttäjiltä ja poistamalla käyttäjien mahdollisesti tekemät mukautukset.</span><span class="sxs-lookup"><span data-stu-id="fdd17-105">As an administrator, you can control and manage personalization by disabling the ability for users to personalize pages and clearing any page personalizations that users have made.</span></span>

## <a name="disable-personalization-for-a-profile"></a><span data-ttu-id="fdd17-106">Profiilin mukauttamisen poistaminen</span><span class="sxs-lookup"><span data-stu-id="fdd17-106">Disable personalization for a profile</span></span>
<span data-ttu-id="fdd17-107">Voit estää sivujen mukauttamisen kaikilta tiettyyn profiiliin kuuluvilta käyttäjiltä.</span><span class="sxs-lookup"><span data-stu-id="fdd17-107">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>
1.  <span data-ttu-id="fdd17-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Profiililuettelo** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="fdd17-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profile List**, and then choose the related link.</span></span>
2.  <span data-ttu-id="fdd17-109">Valitse luettelossa muokattava profiili.</span><span class="sxs-lookup"><span data-stu-id="fdd17-109">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="fdd17-110">Valitse **Poista mukauttaminen käytöstä** -valintaruutuja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="fdd17-110">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="clear-user-personalizations"></a><span data-ttu-id="fdd17-111">Käyttäjän mukautusten tyhjentäminen</span><span class="sxs-lookup"><span data-stu-id="fdd17-111">Clear user personalizations</span></span>

<span data-ttu-id="fdd17-112">Mukautetun sivun muutosten tyhjentäminen palauttaa sivun mukautuksia edeltävän alkuperäisen asettelun.</span><span class="sxs-lookup"><span data-stu-id="fdd17-112">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="fdd17-113">Käyttäjien sivulle tekemät mukautukset voi tyhjentää kahdella tavalla: käyttämällä **Poista käyttäjän mukautus** -sivua tai käyttämällä **Käyttäjän mukautuskortti** -sivua.</span><span class="sxs-lookup"><span data-stu-id="fdd17-113">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="fdd17-114">Käyttäjän mukautusten tyhjentäminen Poista käyttäjän mukautus -sivun avulla</span><span class="sxs-lookup"><span data-stu-id="fdd17-114">Clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="fdd17-115">Voit tyhjentää **Poista käyttäjän mukautus** -sivulla mukautukset kultakin käyttäjältä sivukohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="fdd17-115">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1.  <span data-ttu-id="fdd17-116">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poista käyttäjän mukautus** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="fdd17-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="fdd17-117">Sivulla on luettelo kaikista mukautetuista sivuista ja käyttäjästä, jolle se kuuluu.</span><span class="sxs-lookup"><span data-stu-id="fdd17-117">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="fdd17-118">**Vanha mukautus** -sarakkeiden valintamerkki ilmaisee, että mukautus tehtiin [!INCLUDE[d365fin](includes/d365fin_md.md)]in vanhassa versiossa, jossa mukautusta käsiteltiin eri tavalla kuin nyt.</span><span class="sxs-lookup"><span data-stu-id="fdd17-118">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="fdd17-119">Mukautus estetään näiden sivujen mukautusta yrittäviltä käyttäjiltä, elleivät he ensin valitse sivun lukituksen poistamista.</span><span class="sxs-lookup"><span data-stu-id="fdd17-119">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="fdd17-120">Lisätietoja on kohdassa [Sivun mukauttamisen estäminen lukitsemalla](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="fdd17-120">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="fdd17-121">Valitse ensin poistettava tapahtuma ja sitten **Poista**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="fdd17-121">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="fdd17-122">Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.</span><span class="sxs-lookup"><span data-stu-id="fdd17-122">The user will see the changes the next time they sign-in.</span></span>

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="fdd17-123">Käyttäjän mukautusten tyhjentäminen Käyttäjän mukautuskortti -sivun avulla</span><span class="sxs-lookup"><span data-stu-id="fdd17-123">Clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="fdd17-124">Voit tyhjentää **Käyttäjän mukautuskortti** -sivulla tietyn käyttäjän kaikki mukautukset.</span><span class="sxs-lookup"><span data-stu-id="fdd17-124">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="fdd17-125">Tämä edellyttää taulukon 2000000072 **Profiili** kirjoitusoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="fdd17-125">This requires write permission to Table 2000000072 **Profile**.</span></span>

1.  <span data-ttu-id="fdd17-126">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän mukautus** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="fdd17-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="fdd17-127">**Käyttäjän mukautus** -sivulla on luettelo kaikista käyttäjistä, joilla mahdollisesti on mukautettuja sivuja.</span><span class="sxs-lookup"><span data-stu-id="fdd17-127">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="fdd17-128">Jos käyttäjä ei löydy luettelosta, kyseisellä käyttäjällä ei ole mukautettuja sivuja.</span><span class="sxs-lookup"><span data-stu-id="fdd17-128">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="fdd17-129">Valitse ensin käyttäjä luettelossa ja sitten **Muokkaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="fdd17-129">Select the user from the list, and then choose the **Edit** action.</span></span>

3.  <span data-ttu-id="fdd17-130">Valitse **Toiminnot**-välilehdessä **Tyhjennä mukautetut sivut**.</span><span class="sxs-lookup"><span data-stu-id="fdd17-130">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="fdd17-131">Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.</span><span class="sxs-lookup"><span data-stu-id="fdd17-131">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="fdd17-132">Katso myös</span><span class="sxs-lookup"><span data-stu-id="fdd17-132">See Also</span></span>
[<span data-ttu-id="fdd17-133">Työtilan mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="fdd17-133">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="fdd17-134">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fdd17-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="fdd17-135">Perusasetusten muuttaminen</span><span class="sxs-lookup"><span data-stu-id="fdd17-135">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="fdd17-136">Näytettävien ominaisuuksien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="fdd17-136">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
