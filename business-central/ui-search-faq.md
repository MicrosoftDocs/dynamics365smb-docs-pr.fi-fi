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
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: d04f78b31b9fb0403201cb9e5cb1f98f1ef935e1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248007"
---
# <a name="tell-me-faq"></a><span data-ttu-id="62714-103">Kerro, mitä haluat tehdä -toiminnon usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="62714-103">Tell Me FAQ</span></span>
<span data-ttu-id="62714-104">Tässä ohjeaiheessa vastataan kysymyksiin, joita edistyneet käyttäjät usein esittävät uudesta Kerro, mitä haluat tehdä -toiminnosta. Se korvasi aiemman sivun hakutoiminnon, jonka nimi on **Etsi sivut ja raportit**.</span><span class="sxs-lookup"><span data-stu-id="62714-104">This topic answers questions that our advanced users often ask about the new Tell Me feature, which has replaced the previous Page Search feature known as **Find Pages and Reports**.</span></span>

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a><span data-ttu-id="62714-105">Löytyvätkö kaikki nykyisen sivun toiminnot Kerro, mitä haluat tehdä -toiminnon avulla?</span><span class="sxs-lookup"><span data-stu-id="62714-105">Are all actions from my current page discoverable in Tell Me?</span></span>
<span data-ttu-id="62714-106">Ei.</span><span class="sxs-lookup"><span data-stu-id="62714-106">No.</span></span> <span data-ttu-id="62714-107">Osissa, kuten myyntirivien osassa tai tietoruuduissa, olevat toiminnot eivät näy Kerro, mitä haluat tehdä -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="62714-107">Actions in parts, such as the Sales Lines part or FactBoxes, are not displayed in Tell Me.</span></span>

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a><span data-ttu-id="62714-108">Suodatetaanko Kerro, mitä haluat tehdä -toiminnon tulokset käyttöoikeuksien mukaan?</span><span class="sxs-lookup"><span data-stu-id="62714-108">Are the results in Tell Me filtered by permissions?</span></span>
<span data-ttu-id="62714-109">Jos käyttäjällä ei ole AccessByPermissions-ominaisuutta, toimintoja ei näytetä.</span><span class="sxs-lookup"><span data-stu-id="62714-109">If the user does not have AccessByPermissions then actions are not displayed.</span></span> <span data-ttu-id="62714-110">Sivut ja raportit näkyvät tuloksissa, mutta niiden käyttäminen edellyttää, että käyttäjällä on tarvittavat käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="62714-110">However, pages and reports appear in the results but require that the user has permission to access them.</span></span> <span data-ttu-id="62714-111">Jos käyttäjällä ei ole objektin katseluoikeuksia, näyttöön tulee asiasta kertova sanoma.</span><span class="sxs-lookup"><span data-stu-id="62714-111">A message will display if the user does not have permission to view the object.</span></span>

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a><span data-ttu-id="62714-112">Sisältääkö Kerro, mitä haluat tehdä -ikkuna omat mukautukset vai asennetut kolmannen osapuolen laajennukset?</span><span class="sxs-lookup"><span data-stu-id="62714-112">Does Tell Me display content from my customizations or installed third-party extensions?</span></span>
<span data-ttu-id="62714-113">Kerro, mitä haluat tehdä -toiminto kerää laajennusten toiminnot, sivut ja raportit, mutta mukautettua ohjeen dokumentaatiota ei kerätä.</span><span class="sxs-lookup"><span data-stu-id="62714-113">Actions, pages, and reports that originate from extensions are picked up by Tell Me, but custom help documentation is not.</span></span> <span data-ttu-id="62714-114">Teknisiä lisätietoja siitä, miten mukautetut sivut ja raportit voidaan tehdä helpommin löydettäviksi, on kohdassa [Sivujen ja raporttien lisääminen hakuun](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span><span class="sxs-lookup"><span data-stu-id="62714-114">For technical information about how to make custom pages and reports discoverable, see [Adding Pages and Reports to Search](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span></span>

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a><span data-ttu-id="62714-115">Miksi tämä on erilainen kuin aiempi sivuhaku?</span><span class="sxs-lookup"><span data-stu-id="62714-115">What makes this different from what was previously known as Page Search?</span></span>
<span data-ttu-id="62714-116">Sivuhaku on kehittynyt Kerro, mitä haluat tehdä -toiminnoksi, jonka avulla työskentely on nopeampaa.</span><span class="sxs-lookup"><span data-stu-id="62714-116">Page Search has evolved into Tell Me to help you get work done quickly.</span></span> <span data-ttu-id="62714-117">Sivuhaku auttoi vain sivuihin ja raportteihin siirtymisessä.</span><span class="sxs-lookup"><span data-stu-id="62714-117">Page Search could only help you navigate to pages or reports.</span></span> <span data-ttu-id="62714-118">Teknisesti ottaen Kerro, mitä haluat tehdä ei enää perustu MenuSuite-käsitteeseen.</span><span class="sxs-lookup"><span data-stu-id="62714-118">At a technical level, Tell Me is no longer based on the legacy MenuSuite concept.</span></span>

### <a name="i-use-on-premises-included365finincludesd365finmdmd-does-that-include-tell-me"></a><span data-ttu-id="62714-119">Käytän paikallista [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellusta.</span><span class="sxs-lookup"><span data-stu-id="62714-119">I use on-premises [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="62714-120">Sisältääkö se Kerro, mitä haluat tehdä -toiminnon?</span><span class="sxs-lookup"><span data-stu-id="62714-120">Does that include Tell Me?</span></span>
<span data-ttu-id="62714-121">Voit käyttää Kerro, mitä haluat tehdä -toimintoa paikallisesti verkkoasiakasohjelmassa, kun haluat etsiä toimintoja, sivuja ja raportteja. Ohjeistusta tai sovelluksia ja konsultointipalveluja ei kuitenkaan voi etsiä sen avulla AppSourcessa.</span><span class="sxs-lookup"><span data-stu-id="62714-121">You can use Tell Me in the on-premises Web Client to find actions, pages, and reports, but not documentation, or apps and consulting services on AppSource.</span></span> <span data-ttu-id="62714-122">Kun käyttäjät muodostavat yhteyden [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksesta Dynamics NAV -asiakasohjelmaan, käytössä on yhä sivuhaku.</span><span class="sxs-lookup"><span data-stu-id="62714-122">Users connecting to [!INCLUDE[d365fin](includes/d365fin_md.md)] from the Dynamics NAV client continue to use Page Search.</span></span>

### <a name="is-tell-me-available-for-all-form-factors"></a><span data-ttu-id="62714-123">Onko Kerro, mitä haluat tehdä -toiminto käytettävissä kaikissa laitemuodoissa?</span><span class="sxs-lookup"><span data-stu-id="62714-123">Is Tell Me available for all form factors?</span></span>
<span data-ttu-id="62714-124">Kerro, mitä haluat tehdä -toiminto on käytettävissä vain WWW-asiakasohjelmassa ja Windows-työpöytäsovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="62714-124">Tell Me is only available in the Web Client or Windows desktop app.</span></span>

### <a name="are-the-documentation-results-available-in-any-language"></a><span data-ttu-id="62714-125">Ovatko dokumentaation tulokset käytettävssä kaikilla kielillä?</span><span class="sxs-lookup"><span data-stu-id="62714-125">Are the documentation results available in any language?</span></span>
<span data-ttu-id="62714-126">Tämän ohjeen artikkelit näkyvät **Omat asetukset** -kohdassa määritetyllä kielellä, jos ohje on käännetty kyseiselle kielelle.</span><span class="sxs-lookup"><span data-stu-id="62714-126">The help articles display in the language you have specified in **My Settings**, if help is available in that language.</span></span>

## <a name="see-also"></a><span data-ttu-id="62714-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="62714-127">See Also</span></span>  
[<span data-ttu-id="62714-128">Toimintojen ja tietojen etsiminen</span><span class="sxs-lookup"><span data-stu-id="62714-128">Finding Features and Information</span></span>](ui-search.md)
