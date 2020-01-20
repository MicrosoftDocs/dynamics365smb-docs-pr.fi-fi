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
ms.date: 12/10/2019
ms.author: solsen
ms.openlocfilehash: 7d189ab6fa5aff518b643c797b7600570fcad43e
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910634"
---
# <a name="creating-a-sandbox-environment-in-include-prodshortincludesprodshortmd"></a><span data-ttu-id="2aaea-103">Sandbox-ympäristön luominen [!INCLUDE [prodshort](includes/prodshort.md)]issa</span><span class="sxs-lookup"><span data-stu-id="2aaea-103">Creating a Sandbox Environment in [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

<span data-ttu-id="2aaea-104">[!INCLUDE [prodshort](includes/prodshort.md)]n avulla voit helposti luoda turvallisen ympäristön, jossa voit testata, kouluttaa tai tehdä vianmäärityksiä häiritsemättä yrityksen työprosesseja tai liiketoimintatietoja.</span><span class="sxs-lookup"><span data-stu-id="2aaea-104">With [!INCLUDE [prodshort](includes/prodshort.md)], you can easily create a safe environment where you can test, train, or troubleshoot without disturbing your company's work processes or business data.</span></span> <span data-ttu-id="2aaea-105">Tällaista ei-tuotantoympäristöä kutsutaan *eristysympäristöksi (sandbox)*.</span><span class="sxs-lookup"><span data-stu-id="2aaea-105">Such a non-production environment is called a *sandbox*.</span></span> <span data-ttu-id="2aaea-106">Tuotannosta eristetty Sandbox-ympäristö on paikka, jossa voi turvallisesti tutustua palveluun, opetella sen käyttöä sekä kehittää ja testata sitä ilman, että tuotantoympäristön tiedot ja asetukset vaarantuvat.</span><span class="sxs-lookup"><span data-stu-id="2aaea-106">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>  

<span data-ttu-id="2aaea-107">Järjestelmänvalvoja voi luoda eristysympäristöjä [hallintakeskuksessa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), mutta jos haluat testata jotain nopeasti, voit luoda [!INCLUDE [prodshort](includes/prodshort.md)]ssa eristetyn ympäristön.</span><span class="sxs-lookup"><span data-stu-id="2aaea-107">Your administrator can create sandbox environments in the [administration center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), but if you want to quickly test something, you can create a sandbox environment from inside [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

> [!NOTE]
> <span data-ttu-id="2aaea-108">Teknisesti eristysympäristöt ovat hyvin erilaisia tuotantoympäristöihin verrattuna, vaikka järjestelmänvalvoja luo eristysympäristön, joka sisältää tuotantotiedot.</span><span class="sxs-lookup"><span data-stu-id="2aaea-108">Technically, sandbox environments are very different from production environments, even if your administrator creates a sandbox that includes production data.</span></span> <span data-ttu-id="2aaea-109">Sandbox-ominaisuutta ei voi käyttää vertailuun, eikä esimerkiksi tietokannan vientiä voi pyytää.</span><span class="sxs-lookup"><span data-stu-id="2aaea-109">You cannot use a sandbox for benchmarking, and you cannot request a database export, for example.</span></span> <span data-ttu-id="2aaea-110">Jos haluat luoda eristysympäristön vertailuun, järjestelmänvalvoja voi luoda erillisen tuotantoympäristön hallintakeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="2aaea-110">If you want to create a sandbox for benchmarking, your administrator can create a dedicated production environment in the administration center.</span></span> <span data-ttu-id="2aaea-111">Lisätietoja on kohdassa [Ympäristötyypit](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span><span class="sxs-lookup"><span data-stu-id="2aaea-111">For more information, see [Types of environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span></span>

## <a name="to-create-a-sandbox-environment-in-your-include-prodshortincludesprodshortmd"></a><span data-ttu-id="2aaea-112">Sandbox-ympäristön luominen [!INCLUDE [prodshort](includes/prodshort.md)]ssa</span><span class="sxs-lookup"><span data-stu-id="2aaea-112">To create a sandbox environment in your [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

1. <span data-ttu-id="2aaea-113">Kirjaudu [!INCLUDE[d365fin](includes/d365fin_md.md)]-palvelun tuotantoilmentymään.</span><span class="sxs-lookup"><span data-stu-id="2aaea-113">Sign in to your production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

2. <span data-ttu-id="2aaea-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Eristysympäristö** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2aaea-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="2aaea-115">Valitse **Luo**-painike.</span><span class="sxs-lookup"><span data-stu-id="2aaea-115">Choose the **Create** button.</span></span>  

    <span data-ttu-id="2aaea-116">Näyttöön avautuu toinen [!INCLUDE[d365fin](includes/d365fin_md.md)] -välilehti. Siinä voit tehdä sandbox-ympäristön asennuksen valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="2aaea-116">Another tab with [!INCLUDE[d365fin](includes/d365fin_md.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="2aaea-117">Jos ponnahdusikkunoiden esto on selaimessa käytössä, vaihda sen asetukset sallimaan \*.businesscentral.dynamics.com-osoitteen URL-osoitteet.</span><span class="sxs-lookup"><span data-stu-id="2aaea-117">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

<span data-ttu-id="2aaea-118">Kun sandbox-ympäristö on valmis, sinut uudelleenohjataan sandbox-ympäristön ohjattuun aloitustoimintoon.</span><span class="sxs-lookup"><span data-stu-id="2aaea-118">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

<span data-ttu-id="2aaea-119">Voit valita **Lue lisää** -painikkeen, kun haluat lisätietoja kehittäjäskenaarioista, joita voit kokeilla sandbox-ympäristössä. Valitse **Sulje**-painike, jos haluat jatkaa [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen sandbox-ympäristön Roolikeskukseen.</span><span class="sxs-lookup"><span data-stu-id="2aaea-119">You can choose the **Learn more** button to read about developer scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>

<span data-ttu-id="2aaea-120">Roolikeskuksen yläreunaan avautuvassa ilmoituksessa ilmoitetaan, että kyse on sandbox-ympäristöstä.</span><span class="sxs-lookup"><span data-stu-id="2aaea-120">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="2aaea-121">Ympäristön tyyppi näkyy myös asiakasohjelman otsikkopalkissa.</span><span class="sxs-lookup"><span data-stu-id="2aaea-121">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> <span data-ttu-id="2aaea-122">Näin luotu sandbox-ympäristö sisältää vain CRONUS-yrityksen oletusesittelytiedot.</span><span class="sxs-lookup"><span data-stu-id="2aaea-122">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="2aaea-123">Mitään tietoja ei kopioida tai muutoin siirretä tuotantoympäristöstä.</span><span class="sxs-lookup"><span data-stu-id="2aaea-123">No data is copied or otherwise transferred from the production environment.</span></span><br /><br />
> <span data-ttu-id="2aaea-124">Voit luoda myös sandbox-ympäristön, joka sisältää tuotantotiedot.</span><span class="sxs-lookup"><span data-stu-id="2aaea-124">You can also create a sandbox environment containing the production data.</span></span> <span data-ttu-id="2aaea-125">Tämä on tehtävä hallintakeskuksen kautta.</span><span class="sxs-lookup"><span data-stu-id="2aaea-125">You must do this through the administration center.</span></span> <span data-ttu-id="2aaea-126">Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeaiheessa [Ympäristöjen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments).</span><span class="sxs-lookup"><span data-stu-id="2aaea-126">For more information, see [Managing Environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in the Developer and IT-Pro help.</span></span>

<span data-ttu-id="2aaea-127">Voit palata koska tahansa **Sandbox-ympäristö**-sivulle ja palauttaa sandbox-ympäristön alkuasetuksiin.</span><span class="sxs-lookup"><span data-stu-id="2aaea-127">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>

> [!NOTE]  
> <span data-ttu-id="2aaea-128">Sandbox-ympäristön palauttaminen alkuasetuksiin poistaa sen kokonaan, ja voit luoda sen uudelleen oletusesittelytiedoilla.</span><span class="sxs-lookup"><span data-stu-id="2aaea-128">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

<span data-ttu-id="2aaea-129">Järjestelmänvalvoja voi rajoittaa tai jopa estää joidenkin käyttäjien mahdollisuutta käyttää sandbox-ympäristöä.</span><span class="sxs-lookup"><span data-stu-id="2aaea-129">An administrator can limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="2aaea-130">Se voidaan tehdä tuotteen vakiotietoturvaominaisuuksien, kuten käyttäjäkortin, käyttäjäryhmien tai käyttöoikeusjoukkojen avulla.</span><span class="sxs-lookup"><span data-stu-id="2aaea-130">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span> <span data-ttu-id="2aaea-131">Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="2aaea-131">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="2aaea-132">Sandbox-ympäristön lisätoiminnot</span><span class="sxs-lookup"><span data-stu-id="2aaea-132">Advanced Functionality in the Sandbox Environment</span></span>

<span data-ttu-id="2aaea-133">Eristysympäristö ei ole vähiten hyödyllinen, koska se sisältää muutamia käteviä ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="2aaea-133">The sandbox environment is not least useful because it includes a couple of handy features.</span></span>

### <a name="designer"></a><span data-ttu-id="2aaea-134">Rakennenäkymä</span><span class="sxs-lookup"><span data-stu-id="2aaea-134">Designer</span></span>

<span data-ttu-id="2aaea-135">Sandbox-ympäristössä on **Rakennenäkymä** käytössä.</span><span class="sxs-lookup"><span data-stu-id="2aaea-135">In a sandbox environment, you will find the **Designer** enabled.</span></span> <span data-ttu-id="2aaea-136">Voit aktivoida Rakennenäkymän valitsemalla Rakennenäkymä-kuvakkeen ![Rakennenäkymä](./media/across-sandbox/sandbox-inclient-design-icon.png) sivulta tai valitsemalla **Rakennenäkymä**-valikkovaihtoehdon ![Asetukset](media/ui-experience/settings_icon_small.png) Asetukset-valikosta.</span><span class="sxs-lookup"><span data-stu-id="2aaea-136">You can activate Designer by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page, or by choosing the **Design** menu item in the ![Settings](media/ui-experience/settings_icon_small.png) Settings menu.</span></span>

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a><span data-ttu-id="2aaea-137">Käyttäjäkokemuksen lisätoimintojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="2aaea-137">To enable the advanced user experience</span></span>
<span data-ttu-id="2aaea-138">On mahdollista ottaa käyttöön ja kokeilla [!INCLUDE[d365fin](includes/d365fin_md.md)]in perusversion täyttä toiminnallisuutta Sandbox-vuokraajassa asettamalla **Kokemus**-kenttä **Yrityksen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2aaea-138">It is possible to enable and try the full functionality of the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

<span data-ttu-id="2aaea-139">Kun olet ottanut käyttöön *Premium*-käyttökokemuksen, saat käyttöösi kaikki vakioprofiilit (roolit) ja roolikeskukset vakioversiossa.</span><span class="sxs-lookup"><span data-stu-id="2aaea-139">After you have enabled the *Premium* user experience, you get access to all the standard profiles (roles) and Role Centers in the standard version.</span></span> <span data-ttu-id="2aaea-140">Voit myös luoda täysin määritetyn arviointiyrityksen. Tämä yritys sisältää esittelytiedot ja tuotteen lisäalueiden käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="2aaea-140">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span> <span data-ttu-id="2aaea-141">Vaihtoehtoisesti voit ottaa yhteyttä jälleenmyyntiyhteistyökumppaniin, jotta saat esittelyn ominaisuuksista.</span><span class="sxs-lookup"><span data-stu-id="2aaea-141">Alternatively, contact a reselling partner for a demonstration of the capabilities.</span></span> <span data-ttu-id="2aaea-142">Lisätietoja on kohdassa [Miten löydän jälleenmyyjäpartnerin?](across-faq.md#findpartner).</span><span class="sxs-lookup"><span data-stu-id="2aaea-142">For more information, see [How do I find a reselling partner?](across-faq.md#findpartner).</span></span>  

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## <a name="see-also"></a><span data-ttu-id="2aaea-143">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2aaea-143">See Also</span></span>

<span data-ttu-id="2aaea-144">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2aaea-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="2aaea-145">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]Kokeilut ja tilaukset](across-preview.md)</span><span class="sxs-lookup"><span data-stu-id="2aaea-145">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Trials and Subscriptions](across-preview.md)</span></span>  
[<span data-ttu-id="2aaea-146">Ympäristöjen hallinta Business Centralin hallintakeskuksessa</span><span class="sxs-lookup"><span data-stu-id="2aaea-146">Managing Environments in the Business Central administration center</span></span>](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
