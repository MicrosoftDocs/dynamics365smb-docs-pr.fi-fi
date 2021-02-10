---
title: Kerro, mitä haluat tehdä -toimintoon liittyviä usein kysyttyjä kysymyksiä | Microsoft Docs
description: Tässä artikkelissa on vastauksia Kerro, mitä haluat tehdä -toimintoon liittyviin usein kysyttyihin kysymyksiin, joita kumppanit ja asiakkaat esittävät.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 7b880ef5cb49a02dcbb3973f87bc64eae48b2b3a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760240"
---
# <a name="tell-me-faq"></a><span data-ttu-id="7c1fa-103">Kerro, mitä haluat tehdä -toiminnon usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="7c1fa-103">Tell Me FAQ</span></span>
<span data-ttu-id="7c1fa-104">Tässä ohjeaiheessa vastataan kokeneiden käyttäjien Kerro, mitä haluat tehdä -ominaisuutta koskeviin usein kysyttyihin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-104">This topic answers questions that our advanced users often ask about the Tell Me feature.</span></span>

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a><span data-ttu-id="7c1fa-105">Löytyvätkö kaikki nykyisen sivun toiminnot Kerro, mitä haluat tehdä -toiminnon avulla?</span><span class="sxs-lookup"><span data-stu-id="7c1fa-105">Are all actions from my current page discoverable in Tell Me?</span></span>
<span data-ttu-id="7c1fa-106">Ei.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-106">No.</span></span> <span data-ttu-id="7c1fa-107">Osissa, kuten myyntirivien osassa tai tietoruuduissa, olevat toiminnot eivät näy Kerro, mitä haluat tehdä -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-107">Actions in parts, such as the Sales Lines part or FactBoxes, are not displayed in Tell Me.</span></span>

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a><span data-ttu-id="7c1fa-108">Suodatetaanko Kerro, mitä haluat tehdä -toiminnon tulokset käyttöoikeuksien mukaan?</span><span class="sxs-lookup"><span data-stu-id="7c1fa-108">Are the results in Tell Me filtered by permissions?</span></span>
<span data-ttu-id="7c1fa-109">Jos käyttäjällä ei ole AccessByPermissions-ominaisuutta, toimintoja ei näytetä.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-109">If the user does not have AccessByPermissions then actions are not displayed.</span></span> <span data-ttu-id="7c1fa-110">Sivut ja raportit näkyvät tuloksissa, mutta niiden käyttäminen edellyttää, että käyttäjällä on tarvittavat käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-110">However, pages and reports appear in the results but require that the user has permission to access them.</span></span> <span data-ttu-id="7c1fa-111">Jos käyttäjällä ei ole objektin katseluoikeuksia, näyttöön tulee asiasta kertova sanoma.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-111">A message will display if the user does not have permission to view the object.</span></span>

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a><span data-ttu-id="7c1fa-112">Sisältääkö Kerro, mitä haluat tehdä -ikkuna omat mukautukset vai asennetut kolmannen osapuolen laajennukset?</span><span class="sxs-lookup"><span data-stu-id="7c1fa-112">Does Tell Me display content from my customizations or installed third-party extensions?</span></span>
<span data-ttu-id="7c1fa-113">Kerro, mitä haluat tehdä -toiminto kerää laajennusten toiminnot, sivut ja raportit, mutta mukautettua ohjeen dokumentaatiota ei kerätä.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-113">Actions, pages, and reports that originate from extensions are picked up by Tell Me, but custom help documentation is not.</span></span> <span data-ttu-id="7c1fa-114">Teknisiä lisätietoja siitä, miten mukautetut sivut ja raportit voidaan tehdä helpommin löydettäviksi, on kohdassa [Sivujen ja raporttien lisääminen hakuun](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span><span class="sxs-lookup"><span data-stu-id="7c1fa-114">For technical information about how to make custom pages and reports discoverable, see [Adding Pages and Reports to Search](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span></span>

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a><span data-ttu-id="7c1fa-115">Miksi tämä on erilainen kuin aiempi sivuhaku?</span><span class="sxs-lookup"><span data-stu-id="7c1fa-115">What makes this different from what was previously known as Page Search?</span></span>
<span data-ttu-id="7c1fa-116">Sivuhaku on kehittynyt Kerro, mitä haluat tehdä -toiminnoksi, jonka avulla työskentely on nopeampaa.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-116">Page Search has evolved into Tell Me to help you get work done quickly.</span></span> <span data-ttu-id="7c1fa-117">Sivuhaku auttoi vain sivuihin ja raportteihin siirtymisessä.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-117">Page Search could only help you navigate to pages or reports.</span></span> <span data-ttu-id="7c1fa-118">Teknisesti ottaen Kerro, mitä haluat tehdä ei enää perustu MenuSuite-käsitteeseen.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-118">At a technical level, Tell Me is no longer based on the legacy MenuSuite concept.</span></span>

### <a name="i-use-on-premises-prod_short-does-that-include-tell-me"></a><span data-ttu-id="7c1fa-119">Käytän paikallista [!INCLUDE[prod_short](includes/prod_short.md)] -sovellusta.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-119">I use on-premises [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="7c1fa-120">Sisältääkö se Kerro, mitä haluat tehdä -toiminnon?</span><span class="sxs-lookup"><span data-stu-id="7c1fa-120">Does that include Tell Me?</span></span>
<span data-ttu-id="7c1fa-121">Voit käyttää Kerro, mitä haluat tehdä -toimintoa paikallisesti verkkoasiakasohjelmassa, kun haluat etsiä toimintoja, sivuja ja raportteja. Ohjeistusta tai sovelluksia ja konsultointipalveluja ei kuitenkaan voi etsiä sen avulla AppSourcessa.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-121">You can use Tell Me in the on-premises Web Client to find actions, pages, and reports, but not documentation, or apps and consulting services on AppSource.</span></span>

### <a name="is-tell-me-available-for-all-form-factors"></a><span data-ttu-id="7c1fa-122">Onko Kerro, mitä haluat tehdä -toiminto käytettävissä kaikissa laitemuodoissa?</span><span class="sxs-lookup"><span data-stu-id="7c1fa-122">Is Tell Me available for all form factors?</span></span>
<span data-ttu-id="7c1fa-123">Kerro, mitä haluat tehdä -toiminto on käytettävissä vain WWW-asiakasohjelmassa ja Windows-työpöytäsovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-123">Tell Me is only available in the Web Client or Windows desktop app.</span></span>

### <a name="are-the-documentation-results-available-in-any-language"></a><span data-ttu-id="7c1fa-124">Ovatko dokumentaation tulokset käytettävssä kaikilla kielillä?</span><span class="sxs-lookup"><span data-stu-id="7c1fa-124">Are the documentation results available in any language?</span></span>
<span data-ttu-id="7c1fa-125">Tämän ohjeen artikkelit näkyvät **Omat asetukset** -kohdassa määritetyllä kielellä, jos ohje on käännetty kyseiselle kielelle.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-125">The help articles display in the language you have specified in **My Settings**, if help is available in that language.</span></span>

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a><span data-ttu-id="7c1fa-126">Miksi hakutulosten kirjanmerkkikuvaketta ei näy?</span><span class="sxs-lookup"><span data-stu-id="7c1fa-126">Why don't I see a bookmark icon for my search results?</span></span>
<span data-ttu-id="7c1fa-127">Kirjanmerkkikuvake ei näy Kerro, mitä haluat tehdä -ikkunassa, kun mukautus on poistettu käytöstä käyttäjäroolissa.</span><span class="sxs-lookup"><span data-stu-id="7c1fa-127">The bookmark icon is not displayed in the Tell Me window when personalization is disabled for a user role.</span></span>


## <a name="see-also"></a><span data-ttu-id="7c1fa-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7c1fa-128">See Also</span></span>  
[<span data-ttu-id="7c1fa-129">Luettelonäkymien tallentaminen ja mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="7c1fa-129">Save and Personalize List Views</span></span>](ui-views.md)  
[<span data-ttu-id="7c1fa-130">Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla</span><span class="sxs-lookup"><span data-stu-id="7c1fa-130">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
[<span data-ttu-id="7c1fa-131">Sivujen etsiminen roolienhallinnan avulla</span><span class="sxs-lookup"><span data-stu-id="7c1fa-131">Finding Pages with the Role Explorer</span></span>](ui-role-explorer.md)  
[<span data-ttu-id="7c1fa-132">Sivun tai raportin kirjanmerkin luominen roolikeskuksessa</span><span class="sxs-lookup"><span data-stu-id="7c1fa-132">Bookmark a Page or Report on Your Role Center</span></span>](ui-bookmarks.md)
