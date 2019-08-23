---
title: Syitä, miksi sivun mukauttaminen ei onnistu | Microsoft Docs
description: Lisätietoja syistä, miksi sivua ei voi mukauttaa ja miten sivun lukituksen voi avata mukauttamista varten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 1a3edaca2e76388d82ea8991c3196410dd9c7288
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796757"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="58785-103">Sivun mukauttamisen estäminen lukitsemalla</span><span class="sxs-lookup"><span data-stu-id="58785-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="58785-104">Kaksi ehtoa estää sivun mukauttamisen.</span><span class="sxs-lookup"><span data-stu-id="58785-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="58785-105">Sivu on joko lukittu (jonka ![Mukautuksen lukitus](media/personalization-lock-icon.png "Mukautuksen lukitus") ilmaisee) tai se on estetty (jonka ![Mukautuksen esto](media/personalization-blocked-icon.png "Mukautuksen esto") ilmaisee).</span><span class="sxs-lookup"><span data-stu-id="58785-105">Either the page is locked (as indicated by ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) or it is blocked (as indicated by ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked")).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="58785-106">Mukauttaminen estetty lukitsemalla</span><span class="sxs-lookup"><span data-stu-id="58785-106">Locked from Personalizing</span></span>

<span data-ttu-id="58785-107">Jos avatun sivun **Mukautetaan**-palkissa on ![Mukautuksen lukitus](media/personalization-lock-icon.png "Mukautuksen lukitus") -kuvake (kuten kuvassa), sivua ei voi tällä hetkellä muuttaa mukauttamalla.</span><span class="sxs-lookup"><span data-stu-id="58785-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page (as shown), this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<span data-ttu-id="58785-108">![Mukautuksen lukitus](media/personalization-locked.png "Mukautuksen lukitus")</span><span class="sxs-lookup"><span data-stu-id="58785-108">![Personalize Lock](media/personalization-locked.png "Personalize lock")</span></span>


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="58785-109">Syitä voi olla kaksi:</span><span class="sxs-lookup"><span data-stu-id="58785-109">There can be two reasons for this:</span></span>

1. <span data-ttu-id="58785-110">Olet mukauttanut sivua aiemmin, mutta silloin käytössä oli tuotteen aikaisempi versio.</span><span class="sxs-lookup"><span data-stu-id="58785-110">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="58785-111">Mukautuksen taustatoimintoja on muutettu sen jälkeen, kun sivua on edellisen kerran mukautettu.</span><span class="sxs-lookup"><span data-stu-id="58785-111">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="58785-112">Valitettavasti vanhaa ja uutta toimintatapaa ei voi käyttää yhtä aikaa.</span><span class="sxs-lookup"><span data-stu-id="58785-112">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="58785-113">Tähän saakka olet mukauttanut sivua vain [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)]illa.</span><span class="sxs-lookup"><span data-stu-id="58785-113">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="58785-114">Sivun lukituksen poistaminen</span><span class="sxs-lookup"><span data-stu-id="58785-114">Unlocking the Page</span></span>

<span data-ttu-id="58785-115">Jos haluat poistaa sivun lukituksen ja jatkaa sen mukauttamista, valitse ensin ![Mukautuksen lukitus](media/personalization-lock-icon.png "Mukautuksen lukitus") ja sitten **Poista lukitus**.</span><span class="sxs-lookup"><span data-stu-id="58785-115">If you want to unlock a page and continue personalizing it, choose ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock"), and then **Unlock**.</span></span>  

<span data-ttu-id="58785-116">Ota kuitenkin seuraavat huomioon ennen sivun lukituksen poistamista:</span><span class="sxs-lookup"><span data-stu-id="58785-116">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="58785-117">Sivun nykyiset mukautukset poistetaan.</span><span class="sxs-lookup"><span data-stu-id="58785-117">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="58785-118">Sivu voi palautua alkuperäiseen asetteluun ja sinun on aloitettava alusta.</span><span class="sxs-lookup"><span data-stu-id="58785-118">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="58785-119">Sivu säilyy [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)]issa nykyisellään eivätkä Business Central -asiakasohjelmassa tehdyt uudet mukautusmuutokset vaikuta siihen.</span><span class="sxs-lookup"><span data-stu-id="58785-119">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="58785-120">Jatkossa [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)]in ja Business Central -asiakasohjelman mukauttaminen on erotettu täysin toisistaan.</span><span class="sxs-lookup"><span data-stu-id="58785-120">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="58785-121">Mukauttaminen estetty</span><span class="sxs-lookup"><span data-stu-id="58785-121">Blocked from Personalizing</span></span>

<span data-ttu-id="58785-122">Jos Mukautetaan-palkissa on ![Mukautuksen esto](media/personalization-blocked-icon.png "Mukautuksen esto") -kuvake, mukauttaminen sivulla on estetty.</span><span class="sxs-lookup"><span data-stu-id="58785-122">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the Personalizing banner, this means that you are blocked from doing any personalization to the page.</span></span>

<span data-ttu-id="58785-123">![Mukautuksen esto](media/personalization-blocked.png "Mukautuksen esto")</span><span class="sxs-lookup"><span data-stu-id="58785-123">![Personalize blocked](media/personalization-blocked.png "Personalize lock")</span></span>

<span data-ttu-id="58785-124">Syynä on se, että käyttäjätiliin tällä hetkellä liitetty roolikeskus tai rooli muokkaa tätä sivua roolin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="58785-124">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="58785-125">Pyydä apua järjestelmänvalvojalta tai jos se tuntuu järkevältä, yritä vaihtaa roolikeskukseen, joka sisältää tämän sivun roolin mukauttamisen. (Valitse [**Omat asetukset**](https://businesscentral.dynamics.com?page=9176 "Siirry suoraan Business Centralin käyttäjäasetusten sivulle").)</span><span class="sxs-lookup"><span data-stu-id="58785-125">Please contact your administrator for assistance or, if it makes sense, try switching to a Role Center (from  [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central")) that does include role-tailoring for this page.</span></span>

## <a name="see-also"></a><span data-ttu-id="58785-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="58785-126">See Also</span></span>
[<span data-ttu-id="58785-127">Työtilan mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="58785-127">Personalizing Your Workspace</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="58785-128">Mukautuksen hallinta</span><span class="sxs-lookup"><span data-stu-id="58785-128">Managing Personalization</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="58785-129">Perusasetusten muuttaminen</span><span class="sxs-lookup"><span data-stu-id="58785-129">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="58785-130">Näytettävien ominaisuuksien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="58785-130">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
