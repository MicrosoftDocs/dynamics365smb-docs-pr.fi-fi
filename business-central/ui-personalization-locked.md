---
title: Syitä, miksi sivun mukauttaminen ei onnistu | Microsoft Docs
description: Lisätietoja syistä, miksi sivua ei voi mukauttaa ja miten sivun lukituksen voi avata mukauttamista varten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d24e78d7f0286e1ef633008e22ceb3f922b48768
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781358"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="a9db0-103">Sivun mukauttamisen estäminen lukitsemalla</span><span class="sxs-lookup"><span data-stu-id="a9db0-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="a9db0-104">Kaksi ehtoa estää sivun mukauttamisen.</span><span class="sxs-lookup"><span data-stu-id="a9db0-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="a9db0-105">Sivu on joko lukittu (kuten ![Mukautuksen lukitus](media/personalization-lock-icon.png "Mukautuksen lukitus") -kuvake osoittaa) tai se on lukittu (kuten ![Mukautuksen esto](media/personalization-blocked-icon.png "Mukauttaminen estetty") -kuvake osoittaa).</span><span class="sxs-lookup"><span data-stu-id="a9db0-105">Either the page is locked (as indicated by the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) icon or it is blocked (as indicated by the ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="a9db0-106">Mukauttaminen estetty lukitsemalla</span><span class="sxs-lookup"><span data-stu-id="a9db0-106">Locked from Personalizing</span></span>

<span data-ttu-id="a9db0-107">Jos ![Mukautuksen lukitus](media/personalization-lock-icon.png "Mukautuksen lukitus") -kuvake on **Mukautetaan** -palkissa sivun avaamisen yhteydessä, sivulle ei tällä hetkellä voi tehdä mukautuksia.</span><span class="sxs-lookup"><span data-stu-id="a9db0-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page, this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="a9db0-108">Syitä voi olla kaksi:</span><span class="sxs-lookup"><span data-stu-id="a9db0-108">There can be two reasons for this:</span></span>

1. <span data-ttu-id="a9db0-109">Olet mukauttanut sivua aiemmin, mutta silloin käytössä oli tuotteen aikaisempi versio.</span><span class="sxs-lookup"><span data-stu-id="a9db0-109">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="a9db0-110">Mukautuksen taustatoimintoja on muutettu sen jälkeen, kun sivua on edellisen kerran mukautettu.</span><span class="sxs-lookup"><span data-stu-id="a9db0-110">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="a9db0-111">Valitettavasti vanhaa ja uutta toimintatapaa ei voi käyttää yhtä aikaa.</span><span class="sxs-lookup"><span data-stu-id="a9db0-111">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="a9db0-112">Tähän saakka olet mukauttanut sivua vain [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)]illa.</span><span class="sxs-lookup"><span data-stu-id="a9db0-112">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="a9db0-113">Sivun lukituksen poistaminen</span><span class="sxs-lookup"><span data-stu-id="a9db0-113">Unlocking the Page</span></span>

<span data-ttu-id="a9db0-114">Jos haluat poistaa sivun lukituksen ja jatkaa sen mukauttamista, valitse ensin ![Mukautuksen lukitus](media/personalization-lock-icon.png "Mukautuksen lukitus") -kuvake ja valitse sitten **Poista lukitus** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="a9db0-114">If you want to unlock a page and continue personalizing it, choose the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon, and then choose the **Unlock** action.</span></span>  

<span data-ttu-id="a9db0-115">Ota kuitenkin seuraavat huomioon ennen sivun lukituksen poistamista:</span><span class="sxs-lookup"><span data-stu-id="a9db0-115">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="a9db0-116">Sivun nykyiset mukautukset poistetaan.</span><span class="sxs-lookup"><span data-stu-id="a9db0-116">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="a9db0-117">Sivu voi palautua alkuperäiseen asetteluun ja sinun on aloitettava alusta.</span><span class="sxs-lookup"><span data-stu-id="a9db0-117">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="a9db0-118">Sivu säilyy [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)]issa nykyisellään eivätkä Business Central -asiakasohjelmassa tehdyt uudet mukautusmuutokset vaikuta siihen.</span><span class="sxs-lookup"><span data-stu-id="a9db0-118">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="a9db0-119">Jatkossa [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)]in ja Business Central -asiakasohjelman mukauttaminen on erotettu täysin toisistaan.</span><span class="sxs-lookup"><span data-stu-id="a9db0-119">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="a9db0-120">Mukauttaminen estetty</span><span class="sxs-lookup"><span data-stu-id="a9db0-120">Blocked from Personalizing</span></span>

<span data-ttu-id="a9db0-121">Jos ![Mukautuksen esto](media/personalization-blocked-icon.png "Mukauttaminen estetty") -kuvake on **Mukautetaan**-palkissa, sivulle ei voi tehdä mukautuksia.</span><span class="sxs-lookup"><span data-stu-id="a9db0-121">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the **Personalizing** banner, this means that you are blocked from doing any personalization to the page.</span></span>

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

<span data-ttu-id="a9db0-122">Syynä on se, että käyttäjätiliin tällä hetkellä liitetty roolikeskus tai rooli muokkaa tätä sivua roolin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a9db0-122">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="a9db0-123">Pyydä apua järjestelmänvalvojalta.</span><span class="sxs-lookup"><span data-stu-id="a9db0-123">Contact your administrator for assistance.</span></span> <span data-ttu-id="a9db0-124">Vaihtoehtoisesti voit yrittää siirtyä roolikeskukseen, jossa on tämän sivun roolimukautus.</span><span class="sxs-lookup"><span data-stu-id="a9db0-124">Alternatively, try switching to a Role Center that does include role-tailoring for this page.</span></span> <span data-ttu-id="a9db0-125">Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="a9db0-125">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a9db0-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a9db0-126">See Also</span></span>
[<span data-ttu-id="a9db0-127">Työtilan mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="a9db0-127">Personalize Your Workspace</span></span>](ui-personalization-user.md)  
[<span data-ttu-id="a9db0-128">Profiilien sivujen mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="a9db0-128">Customize Pages for Profiles</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="a9db0-129">Perusasetusten muuttaminen</span><span class="sxs-lookup"><span data-stu-id="a9db0-129">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="a9db0-130">Näytettävien ominaisuuksien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="a9db0-130">Change Which Features are Displayed</span></span>](ui-experiences.md)  
