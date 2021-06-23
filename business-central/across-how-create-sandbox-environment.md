---
title: Eristysympäristön (sandbox) luominen
description: Luo Business Centralissa sopiva ympäristö tutustumista, oppimista, esittelyä, kehittämistä ja testausta varten.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/08/2021
ms.author: solsen
ms.openlocfilehash: a76ae33815b8e9368f45b72fd8703bfc47cbd079
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215626"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a><span data-ttu-id="2e8c1-103">Sandbox-ympäristön luominen [!INCLUDE[prod_short](includes/prod_short.md)]issa</span><span class="sxs-lookup"><span data-stu-id="2e8c1-103">Creating a Sandbox Environment in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

<span data-ttu-id="2e8c1-104">[!INCLUDE[prod_short](includes/prod_short.md)]n avulla voit helposti luoda turvallisen ympäristön, jossa voit testata, kouluttaa tai tehdä vianmäärityksiä häiritsemättä yrityksen työprosesseja tai liiketoimintatietoja.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-104">With [!INCLUDE[prod_short](includes/prod_short.md)], you can easily create a safe environment where you can test, train, or troubleshoot without disturbing your company's work processes or business data.</span></span> <span data-ttu-id="2e8c1-105">Tällaista ei-tuotantoympäristöä kutsutaan *eristysympäristöksi (sandbox)*.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-105">Such a non-production environment is called a *sandbox*.</span></span> <span data-ttu-id="2e8c1-106">Tuotannosta eristetty Sandbox-ympäristö on paikka, jossa voi turvallisesti tutustua palveluun, opetella sen käyttöä sekä kehittää ja testata sitä ilman, että tuotantoympäristön tiedot ja asetukset vaarantuvat.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-106">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>  

<span data-ttu-id="2e8c1-107">Järjestelmänvalvoja hallinnoi eristysympäristöjä [hallintakeskuksessa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), mutta jos haluat testata jotain nopeasti, voit luoda [!INCLUDE[prod_short](includes/prod_short.md)]ssa eristetyn ympäristön.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-107">Your administrator manages sandbox environments in the [administration center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), but if you want to quickly test something, you can create a sandbox environment from inside [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="2e8c1-108">Kun olet valmis, voit poistaa eristysympäristön hallintakeskuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-108">Once you're done, you can remove the sandbox, using the administration center.</span></span>  

> [!NOTE]
> <span data-ttu-id="2e8c1-109">Teknisesti eristysympäristöt ovat hyvin erilaisia tuotantoympäristöihin verrattuna, vaikka järjestelmänvalvoja luo eristysympäristön, joka sisältää tuotantotiedot.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-109">Technically, sandbox environments are very different from production environments, even if your administrator creates a sandbox that includes production data.</span></span> <span data-ttu-id="2e8c1-110">Sandbox-ominaisuutta ei voi käyttää vertailuun, eikä esimerkiksi tietokannan vientiä voi pyytää.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-110">You cannot use a sandbox for benchmarking, and you cannot request a database export, for example.</span></span> <span data-ttu-id="2e8c1-111">Jos haluat luoda eristysympäristön vertailua varten, järjestelmänvalvoja voi luoda erillisen ympäristön hallintakeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-111">If you want to create a sandbox for benchmarking, your administrator can create a dedicated environment in the administration center.</span></span> <span data-ttu-id="2e8c1-112">Lisätietoja on kohdassa [Tuotanto- ja eristysympäristöt](/dynamics365/business-central/dev-itpro/administration/environment-types).</span><span class="sxs-lookup"><span data-stu-id="2e8c1-112">For more information, see [Production and Sandbox Environments](/dynamics365/business-central/dev-itpro/administration/environment-types).</span></span>

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a><span data-ttu-id="2e8c1-113">Sandbox-ympäristön luominen [!INCLUDE[prod_short](includes/prod_short.md)]ssa</span><span class="sxs-lookup"><span data-stu-id="2e8c1-113">To create a sandbox environment in your [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

1. <span data-ttu-id="2e8c1-114">Kirjaudu [!INCLUDE[prod_short](includes/prod_short.md)]-palvelun tuotantoilmentymään.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-114">Sign in to your production instance of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

2. <span data-ttu-id="2e8c1-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Eristysympäristö** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="2e8c1-116">Valitse **Luo**-painike.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-116">Choose the **Create** button.</span></span>  

    <span data-ttu-id="2e8c1-117">Näyttöön avautuu toinen [!INCLUDE[prod_short](includes/prod_short.md)] -välilehti. Siinä voit tehdä sandbox-ympäristön asennuksen valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-117">Another tab with [!INCLUDE[prod_short](includes/prod_short.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="2e8c1-118">Jos ponnahdusikkunoiden esto on selaimessa käytössä, vaihda sen asetukset sallimaan \*.businesscentral.dynamics.com-osoitteen URL-osoitteet.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-118">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

<span data-ttu-id="2e8c1-119">Kun sandbox-ympäristö on valmis, sinut uudelleenohjataan sandbox-ympäristön ohjattuun aloitustoimintoon.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-119">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

<span data-ttu-id="2e8c1-120">Voit valita **Lue lisää** -painikkeen, kun haluat lisätietoja kehittäjäskenaarioista, joita voit kokeilla sandbox-ympäristössä. Valitse **Sulje**-painike, jos haluat jatkaa [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen sandbox-ympäristön Roolikeskukseen.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-120">You can choose the **Learn more** button to read about developer scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[prod_short](includes/prod_short.md)] sandbox instance.</span></span>

<span data-ttu-id="2e8c1-121">Roolikeskuksen yläreunaan avautuvassa ilmoituksessa ilmoitetaan, että kyse on sandbox-ympäristöstä.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-121">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="2e8c1-122">Ympäristön tyyppi näkyy myös asiakasohjelman otsikkopalkissa.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-122">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> <span data-ttu-id="2e8c1-123">Näin luotu sandbox-ympäristö sisältää vain CRONUS-yrityksen oletusesittelytiedot.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-123">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="2e8c1-124">Mitään tietoja ei kopioida tai muutoin siirretä tuotantoympäristöstä.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-124">No data is copied or otherwise transferred from the production environment.</span></span>
>
> <span data-ttu-id="2e8c1-125">Vaihtoehtoisesti voit luoda tuotantotietoihin perustuvan eristysympäristön.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-125">Alternatively, create a sandbox environment based on production data.</span></span> <span data-ttu-id="2e8c1-126">Tämä on tehtävä hallintakeskuksen kautta.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-126">You must do this through the administration center.</span></span> <span data-ttu-id="2e8c1-127">Lisätietoja on kehittäjä- ja hallintasisällön kohdassa [Ympäristöjen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments).</span><span class="sxs-lookup"><span data-stu-id="2e8c1-127">For more information, see [Managing Environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in the developer and administration content.</span></span>  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

<span data-ttu-id="2e8c1-128">Järjestelmänvalvoja voi rajoittaa tai jopa estää joidenkin käyttäjien mahdollisuutta käyttää sandbox-ympäristöä.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-128">An administrator can limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="2e8c1-129">Se voidaan tehdä tuotteen vakiotietoturvaominaisuuksien, kuten käyttäjäkortin, käyttäjäryhmien tai käyttöoikeusjoukkojen avulla.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-129">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span> <span data-ttu-id="2e8c1-130">Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="2e8c1-130">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="2e8c1-131">Sandbox-ympäristön lisätoiminnot</span><span class="sxs-lookup"><span data-stu-id="2e8c1-131">Advanced Functionality in the Sandbox Environment</span></span>

<span data-ttu-id="2e8c1-132">Eristysympäristö on hyödyllinen muun muassa seuraavien kätevien ominaisuuksien ansiosta:</span><span class="sxs-lookup"><span data-stu-id="2e8c1-132">The sandbox environment is not least useful because it includes a couple of handy features:</span></span>

* [<span data-ttu-id="2e8c1-133">Käyttäjäkokemuksen parannus</span><span class="sxs-lookup"><span data-stu-id="2e8c1-133">Advanced user experience</span></span>](#advanced-user-experience)  
* [<span data-ttu-id="2e8c1-134">Täydelliset esimerkkitiedot</span><span class="sxs-lookup"><span data-stu-id="2e8c1-134">Complete sample data</span></span>](#complete-sample-data)  
* [<span data-ttu-id="2e8c1-135">Suunnitteluohjelma</span><span class="sxs-lookup"><span data-stu-id="2e8c1-135">Designer</span></span>](#designer)  

### <a name="advanced-user-experience"></a><span data-ttu-id="2e8c1-136">Käyttäjäkokemuksen parannus</span><span class="sxs-lookup"><span data-stu-id="2e8c1-136">Advanced user experience</span></span>

<span data-ttu-id="2e8c1-137">[!INCLUDE[prod_short](includes/prod_short.md)]in perusversion voi ottaa käyttöön ja sen kaikkia toimintoja voi käyttää eristysvuokraajassa määrittämällä **Kokemus**-kentän asetukseksi *Premium* **Yrityksen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-137">It is possible to enable and try the full functionality of the standard version of [!INCLUDE[prod_short](includes/prod_short.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page to *Premium*.</span></span> Etsi **Yrityksen tiedot** -sivu :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Asetuskuvake":::-valikossa.  

<span data-ttu-id="2e8c1-139">Kun olet ottanut käyttöön *Premium*-käyttökokemuksen, saat käyttöösi kaikki vakioprofiilit (roolit) ja roolikeskukset vakioversiossa.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-139">After you have enabled the *Premium* user experience, you get access to all the standard profiles (roles) and Role Centers in the standard version.</span></span> <span data-ttu-id="2e8c1-140">Voit myös luoda täysin määritetyn arviointiyrityksen. Tämä yritys sisältää esittelytiedot ja tuotteen lisäalueiden käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-140">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span> <span data-ttu-id="2e8c1-141">Vaihtoehtoisesti voit ottaa yhteyttä jälleenmyyntiyhteistyökumppaniin, jotta saat esittelyn ominaisuuksista.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-141">Alternatively, contact a reselling partner for a demonstration of the capabilities.</span></span> <span data-ttu-id="2e8c1-142">Lisätietoja on kohdassa [Miten löydän jälleenmyyjäkumppanin?](/dynamics365/business-central/across-faq.yml#findpartner).</span><span class="sxs-lookup"><span data-stu-id="2e8c1-142">For more information, see [How do I find a reselling partner?](/dynamics365/business-central/across-faq.yml#findpartner).</span></span>  

### <a name="complete-sample-data"></a><span data-ttu-id="2e8c1-143">Täydelliset esimerkkitiedot</span><span class="sxs-lookup"><span data-stu-id="2e8c1-143">Complete sample data</span></span>

<span data-ttu-id="2e8c1-144">Jos tarvitset lisää esimerkkitietoja, käänny jälleenmyyjäkumppanin puoleen.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-144">For situations where you need additional sample data, please talk to your reselling partner.</span></span>
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a><span data-ttu-id="2e8c1-145">Täydelliset näytetiedot sisältävän yrityksen luonti eristysympäristössä</span><span class="sxs-lookup"><span data-stu-id="2e8c1-145">To create a company with complete sample data in a sandbox</span></span>

1. <span data-ttu-id="2e8c1-146">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yritykset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2e8c1-147">Valitse ensin **Uusi**-toiminto ja valitse sitten **Luo uusi yritys**.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-147">Choose the **New** action, and then choose **Create New Company**.</span></span>  
3. <span data-ttu-id="2e8c1-148">Valitse **Yrityksen luontiasetusten ohjattu määritys** -sivulla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-148">In the **Assisted Setup for Creating a Company** page, choose **Next**.</span></span>  
4. <span data-ttu-id="2e8c1-149">Määritä uuden yrityksen nimi ja valitse sitten **Aloita valitsemalla tiedot ja asetukset** -kentässä **Laajennettu arviointi - Kaikki mallitiedot**.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-149">Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.</span></span>  
5. <span data-ttu-id="2e8c1-150">Suorita asetusten ohjatun määritysoppaan loput vaiheet.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-150">Complete the rest of the assisted setup guide.</span></span>  

<span data-ttu-id="2e8c1-151">Kun asetuksen ohjattu määritysopas on suoritettu, voi aloittaa uuteen yritykseen tutustumisen täydellisten mallitietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-151">When the assisted setup guide completes, you can start exploring the new company with the complete sample data.</span></span> <span data-ttu-id="2e8c1-152">Lisätietoa on kohdassa [Uusien yritysten luominen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="2e8c1-152">For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span></span>  

### <a name="designer"></a><span data-ttu-id="2e8c1-153">Rakennenäkymä</span><span class="sxs-lookup"><span data-stu-id="2e8c1-153">Designer</span></span>

<span data-ttu-id="2e8c1-154">Sandbox-ympäristössä on **Rakennenäkymä** käytössä.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-154">In a sandbox environment, you will find the **Designer** enabled.</span></span> <span data-ttu-id="2e8c1-155">Voit aktivoida Rakennenäkymän valitsemalla Rakennenäkymä-kuvakkeen ![Rakennenäkymä](./media/across-sandbox/sandbox-inclient-design-icon.png) sivulta tai valitsemalla **Rakennenäkymä**-valikkovaihtoehdon ![Asetukset](media/ui-experience/settings_icon_small.png) Asetukset-valikosta.</span><span class="sxs-lookup"><span data-stu-id="2e8c1-155">You can activate Designer by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page, or by choosing the **Design** menu item in the ![Settings](media/ui-experience/settings_icon_small.png) Settings menu.</span></span>  

<span data-ttu-id="2e8c1-156">Lisätietoja on kehittäjä- ja järjestelmänvalvojasisällön kohdassa [Suunnitteluohjelman käyttäminen ](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) (vain englanniksi).</span><span class="sxs-lookup"><span data-stu-id="2e8c1-156">For more information, see [Using Designer](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) in the developer and admin content (in English only).</span></span>  

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a><span data-ttu-id="2e8c1-157">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2e8c1-157">See Also</span></span>

<span data-ttu-id="2e8c1-158">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2e8c1-158">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="2e8c1-159">[[!INCLUDE[prod_long](includes/prod_long.md)]Kokeilut ja tilaukset](across-preview.md)</span><span class="sxs-lookup"><span data-stu-id="2e8c1-159">[[!INCLUDE[prod_long](includes/prod_long.md)] Trials and Subscriptions](across-preview.md)</span></span>  
[<span data-ttu-id="2e8c1-160">Ympäristöjen hallinta Business Centralin hallintakeskuksessa</span><span class="sxs-lookup"><span data-stu-id="2e8c1-160">Managing Environments in the Business Central administration center</span></span>](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
