---
title: Sandbox-ympäristön luominen | Microsoft Docs
description: Luo tutustumista, oppimista, esittelyä, kehittämistä ja testausta varten sopiva ympäristö.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/26/2019
ms.author: solsen
ms.openlocfilehash: 10ccbc7546aa5d03c3837997a721c63c3ce465da
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796663"
---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a><span data-ttu-id="14908-103">Sandbox-ympäristön luominen</span><span class="sxs-lookup"><span data-stu-id="14908-103">Creating a Sandbox Environment</span></span>
<span data-ttu-id="14908-104">Sandbox-ympäristö (esiversio) on [!INCLUDE[d365fin](includes/d365fin_md.md)]in tuotantoympäristöön kuulumaton ilmentymä.</span><span class="sxs-lookup"><span data-stu-id="14908-104">A sandbox environment (Preview) is a non-production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="14908-105">Tuotannosta eristetty Sandbox-ympäristö on paikka, jossa voi turvallisesti tutustua palveluun, opetella sen käyttöä sekä kehittää ja testata sitä ilman, että tuotantoympäristön tiedot ja asetukset vaarantuvat.</span><span class="sxs-lookup"><span data-stu-id="14908-105">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>

## <a name="to-create-a-sandbox-environment"></a><span data-ttu-id="14908-106">Sandbox-ympäristön luominen</span><span class="sxs-lookup"><span data-stu-id="14908-106">To create a sandbox environment</span></span>
<span data-ttu-id="14908-107">Tarvitse sandbox-ympäristön luontia varten [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilauksen.</span><span class="sxs-lookup"><span data-stu-id="14908-107">You must have a subscription to [!INCLUDE[d365fin](includes/d365fin_md.md)] to be able to create a sandbox environment.</span></span> <span data-ttu-id="14908-108">Kutakin tilausta kohden voi olla vain yksi sandbox-ympäristö.</span><span class="sxs-lookup"><span data-stu-id="14908-108">There can only be one sandbox environment per subscription.</span></span>

1. <span data-ttu-id="14908-109">Kirjaudu [!INCLUDE[d365fin](includes/d365fin_md.md)]-palvelun tuotantoilmentymään.</span><span class="sxs-lookup"><span data-stu-id="14908-109">Sign in to your production instance of the [!INCLUDE[d365fin](includes/d365fin_md.md)] service.</span></span>

2. <span data-ttu-id="14908-110">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sandbox-ympäristö** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="14908-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
<!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="14908-111">Valitse **Luo**-painike.</span><span class="sxs-lookup"><span data-stu-id="14908-111">Choose the **Create** button.</span></span>  

    <span data-ttu-id="14908-112">Näyttöön avautuu toinen [!INCLUDE[d365fin](includes/d365fin_md.md)] -välilehti. Siinä voit tehdä sandbox-ympäristön asennuksen valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="14908-112">Another tab with [!INCLUDE[d365fin](includes/d365fin_md.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="14908-113">Jos ponnahdusikkunoiden esto on selaimessa käytössä, vaihda sen asetukset sallimaan \*.businesscentral.dynamics.com-osoitteen URL-osoitteet.</span><span class="sxs-lookup"><span data-stu-id="14908-113">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

4. <span data-ttu-id="14908-114">Kun sandbox-ympäristö on valmis, sinut uudelleenohjataan sandbox-ympäristön ohjattuun aloitustoimintoon.</span><span class="sxs-lookup"><span data-stu-id="14908-114">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

5. <span data-ttu-id="14908-115">Valitse **Lue lisää** -painike, kun haluat lisätietoja skenaarioista, joita voit kokeilla sandbox-ympäristössä. Valitse **Sulje**-painike, jos haluat jatkaa [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen sandbox-ympäristön Roolikeskukseen.</span><span class="sxs-lookup"><span data-stu-id="14908-115">Choose the **Learn more** button to read about scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>

    <span data-ttu-id="14908-116">Roolikeskuksen yläreunaan avautuvassa ilmoituksessa ilmoitetaan, että kyse on sandbox-ympäristöstä.</span><span class="sxs-lookup"><span data-stu-id="14908-116">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="14908-117">Ympäristön tyyppi näkyy myös asiakasohjelman otsikkopalkissa.</span><span class="sxs-lookup"><span data-stu-id="14908-117">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

    > [!NOTE]
    > <span data-ttu-id="14908-118">Näin luotu sandbox-ympäristö sisältää vain CRONUS-yrityksen oletusesittelytiedot.</span><span class="sxs-lookup"><span data-stu-id="14908-118">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="14908-119">Mitään tietoja ei kopioida tai muutoin siirretä tuotantoympäristöstä.</span><span class="sxs-lookup"><span data-stu-id="14908-119">No data is copied or otherwise transferred from the production environment.</span></span><br /><br />
    > <span data-ttu-id="14908-120">Voit luoda myös sandbox-ympäristön, joka sisältää tuotantotiedot.</span><span class="sxs-lookup"><span data-stu-id="14908-120">You can also create a sandbox environment containing the production data.</span></span> <span data-ttu-id="14908-121">Tämä on tehtävä hallintakeskuksen kautta.</span><span class="sxs-lookup"><span data-stu-id="14908-121">You must do this through the administration center.</span></span> <span data-ttu-id="14908-122">Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeaiheessa [Ympäristöjen hallinta](/business-central/dev-itpro/administration/tenant-admin-center-environments).</span><span class="sxs-lookup"><span data-stu-id="14908-122">For more information, see [Managing Environments](/business-central/dev-itpro/administration/tenant-admin-center-environments) in the Developer and IT-Pro help.</span></span>

6. <span data-ttu-id="14908-123">Voit palata koska tahansa **Sandbox-ympäristö**-sivulle ja palauttaa sandbox-ympäristön alkuasetuksiin.</span><span class="sxs-lookup"><span data-stu-id="14908-123">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>
    > [!NOTE]  
    >  <span data-ttu-id="14908-124">Sandbox-ympäristön palauttaminen alkuasetuksiin poistaa sen kokonaan, ja voit luoda sen uudelleen oletusesittelytiedoilla.</span><span class="sxs-lookup"><span data-stu-id="14908-124">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

7. <span data-ttu-id="14908-125">Voit siirtyä tuotanto- ja sandbox-ympäristöjen välillä Business Central -sovellusten käynnistysohjelman avulla.</span><span class="sxs-lookup"><span data-stu-id="14908-125">To switch between your production and sandbox environments, you can use the Business Central app launcher.</span></span>
<!-- ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

8. <span data-ttu-id="14908-126">Järjestelmänvalvoja tai toinen käyttäjä voi rajoittaa tai jopa estää joidenkin käyttäjien mahdollisuutta käyttää sandbox-ympäristöä.</span><span class="sxs-lookup"><span data-stu-id="14908-126">It is possible for an administrator or another user to limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="14908-127">Se voidaan tehdä tuotteen vakiotietoturvaominaisuuksien, kuten käyttäjäkortin, käyttäjäryhmien tai käyttöoikeusjoukkojen avulla.</span><span class="sxs-lookup"><span data-stu-id="14908-127">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span>

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="14908-128">Sandbox-ympäristön lisätoiminnot</span><span class="sxs-lookup"><span data-stu-id="14908-128">Advanced Functionality in the Sandbox Environment</span></span>
### <a name="designer"></a><span data-ttu-id="14908-129">Rakennenäkymä</span><span class="sxs-lookup"><span data-stu-id="14908-129">Designer</span></span>
<span data-ttu-id="14908-130">Sandbox-ympäristössä on otettu käyttöön **suunnittelutoiminto**, ja voit aktivoida sen valitsemalla sivulla suunnittelukuvakkeen ![Suunnitteluohjelma](./media/across-sandbox/sandbox-inclient-design-icon.png).</span><span class="sxs-lookup"><span data-stu-id="14908-130">In a sandbox environment, you will find the **Designer** enabled, which you can activate by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page.</span></span>

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a><span data-ttu-id="14908-131">Käyttäjäkokemuksen lisätoimintojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="14908-131">To enable the advanced user experience</span></span>
<span data-ttu-id="14908-132">[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisätoiminnot (kaikki toiminnot) voi ottaa käyttöön kokeiltavaksi sandbox-ympäristön vuokraajassa määrittämällä **Kokemus**-kentän **Yrityksen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="14908-132">It is possible to enable and try the advanced (full) functionality of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

<span data-ttu-id="14908-133">Kun olet ottanut lisäasetukset käyttöön sandbox-ympäristön vuokraajassa, voit käyttää kaikkia vakioprofiileja (rooleja) ja roolikeskuksia.</span><span class="sxs-lookup"><span data-stu-id="14908-133">After you have enabled the advanced functionality in a sandbox tenant, you get access to all the standard profiles (roles) and Role Centers.</span></span> <span data-ttu-id="14908-134">Voit myös luoda täysin määritetyn arviointiyrityksen. Tämä yritys sisältää esittelytiedot ja tuotteen lisäalueiden käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="14908-134">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span>

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->


## <a name="see-also"></a><span data-ttu-id="14908-135">Katso myös</span><span class="sxs-lookup"><span data-stu-id="14908-135">See Also</span></span>
<span data-ttu-id="14908-136">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="14908-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
