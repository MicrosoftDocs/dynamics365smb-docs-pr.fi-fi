---
title: "Syitä, miksi sivun mukauttaminen ei onnistu | Microsoft Docs"
description: "Lisätietoja syistä, miksi sivua ei voi mukauttaa ja miten sivun lukituksen voi avata mukauttamista varten."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 09/07/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 6b225548e95abacc688a97f1c3f8b5e8472a8f8f
ms.contentlocale: fi-fi
ms.lasthandoff: 04/18/2018

---
# <a name="why-a-page-is-locked-from-personalizing"></a><span data-ttu-id="4d6f7-103">Sivun mukauttamisen estäminen lukitsemalla</span><span class="sxs-lookup"><span data-stu-id="4d6f7-103">Why a Page is Locked From Personalizing</span></span>
<span data-ttu-id="4d6f7-104">Jos avatun sivun **Mukautetaan**-palkissa on lukkokuvake (kuten kuvassa), sivun muuttaminen mukauttamalla on tällä hetkellä estetty.</span><span class="sxs-lookup"><span data-stu-id="4d6f7-104">If there is a lock icon in the **Personalizing** bar when you open a page (as shown), this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<span data-ttu-id="4d6f7-105">![Mukautuksen lukitus](media/personalization-locked.png "Mukautuksen lukitus")</span><span class="sxs-lookup"><span data-stu-id="4d6f7-105">![Personalize Lock](media/personalization-locked.png "Personalize lock")</span></span>

<span data-ttu-id="4d6f7-106">Syynä tähän on mukautuksen taustatoimintoja on muutettu sen jälkeen, kun sivua on edellisen kerran mukautettu.</span><span class="sxs-lookup"><span data-stu-id="4d6f7-106">This is because we changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="4d6f7-107">Valitettavasti vanhaa ja uutta toimintatapaa ei voi käyttää yhtä aikaa.</span><span class="sxs-lookup"><span data-stu-id="4d6f7-107">Unfortunately, the old way and new of doing things do not work together.</span></span>

<span data-ttu-id="4d6f7-108">Sivu sisältää tällä hetkellä viimeksi tekemäsi muutokset.</span><span class="sxs-lookup"><span data-stu-id="4d6f7-108">The page currently includes the last personalization changes that you made.</span></span> <span data-ttu-id="4d6f7-109">Jos haluat jatkaa sivun mukauttamista, sinun on valittava ensin lukkokuvake ja sitten **Poista lukitus**.</span><span class="sxs-lookup"><span data-stu-id="4d6f7-109">If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**.</span></span> <span data-ttu-id="4d6f7-110">Muista kuitenkin, että jos päätät poistaa sivun lukituksen, sivun nykyinen mukautus poistetaan ja sinun on aloitettava alusta.</span><span class="sxs-lookup"><span data-stu-id="4d6f7-110">Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.</span></span>


## <a name="see-also"></a><span data-ttu-id="4d6f7-111">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4d6f7-111">See Also</span></span>
[<span data-ttu-id="4d6f7-112">Työtilan mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="4d6f7-112">Personalizing Your Workspace</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="4d6f7-113">Mukautuksen hallinta</span><span class="sxs-lookup"><span data-stu-id="4d6f7-113">Managing Personalization</span></span>](ui-personalization-manage.md)  
<span data-ttu-id="4d6f7-114">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4d6f7-114">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4d6f7-115">Perusasetusten muuttaminen</span><span class="sxs-lookup"><span data-stu-id="4d6f7-115">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="4d6f7-116">Näytettävien ominaisuuksien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="4d6f7-116">Changing Which Features are Displayed</span></span>](ui-experiences.md)  

