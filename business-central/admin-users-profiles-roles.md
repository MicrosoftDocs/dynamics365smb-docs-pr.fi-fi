---
title: "Käyttäjien ja roolien hallinta | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten Business Central -sovelluksen käyttäjiä ja roolikeskuksia hallitaan."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 10/24/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 7ecd8a5ad2b321d4d1683047e70ede90c7ce229f
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="2481d-103">Tietoja käyttäjistä, profiileista ja roolikeskuksista</span><span class="sxs-lookup"><span data-stu-id="2481d-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="2481d-104">[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa järjestelmänvalvoja lisää käyttäjät ja antaa käyttäjille [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen niiden alueiden käyttöoikeuden, joita käyttäjät tarvitsevat työssään.</span><span class="sxs-lookup"><span data-stu-id="2481d-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="2481d-105">Toimintojen käyttöä hallitaan *käyttäjäryhmien* ja *profiilien* avulla.</span><span class="sxs-lookup"><span data-stu-id="2481d-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="2481d-106">Järjestelmänvalvojana voit lisätä ja poistaa käyttäjiä [!INCLUDE[d365fin](includes/d365fin_md.md)] -tilauksesta. Voit myös määrittää käyttäjien oikeuksia käyttäjäryhmien avulla.</span><span class="sxs-lookup"><span data-stu-id="2481d-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="2481d-107">Käyttäjien lisääminen</span><span class="sxs-lookup"><span data-stu-id="2481d-107">Adding Users</span></span>

<span data-ttu-id="2481d-108">Käyttäjiä voi lisätä [!INCLUDE[d365fin](includes/d365fin_md.md)] online -versioon sen jälkeen, kun yrityksen Office 365:n järjestelmänvalvoja on ensin luonut käyttäjät Office 365:n hallintaportaalissa.</span><span class="sxs-lookup"><span data-stu-id="2481d-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="2481d-109">Lisätietoja on kohdassa [Käyttäjien lisääminen Office 365 for Businessiin](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="2481d-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="2481d-110">Tämän jälkeen järjestelmänvalvoja voi määrittää käyttöoikeudet kullekin käyttäjälle ja käyttäjäryhmälle.</span><span class="sxs-lookup"><span data-stu-id="2481d-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="2481d-111">Lisätietoja on kohdassa [Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="2481d-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

<span data-ttu-id="2481d-112">Käyttäjän tehokkaimmat käyttöoikeudet SUPER-käyttöoikeusjoukko.</span><span class="sxs-lookup"><span data-stu-id="2481d-112">The most powerful permissions that a user can have is the SUPER permission set.</span></span> <span data-ttu-id="2481d-113">Jokaisella yrityksellä on oltava ainakin yksi käyttäjä, jolla on tämä käyttöoikeusjoukko. Parhaan käytännön mukaista on kuitenkin antaa jokaiselle käyttäjälle hänen [!INCLUDE[prodshort](includes/prodshort.md)]in käyttötarpeitaan vastaavat käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="2481d-113">Each company must have at least one user with this permission set, but it is a best practice to give each user permissions that match their work needs in [!INCLUDE[prodshort](includes/prodshort.md)] and not more than that.</span></span> <span data-ttu-id="2481d-114">Tämä auttaa varmistamaan, että käyttäjillä on vain niiden tietojen käyttöoikeus, joita he tarvitsevat esimerkiksi työssään.</span><span class="sxs-lookup"><span data-stu-id="2481d-114">This helps ensure that users only have access to data that is relevant to their work, for example.</span></span>  

> [!TIP]
> <span data-ttu-id="2481d-115">On parhaan käytännön mukaista varmistaa, että Office 365:n järjestelmänvalvojalla on myös [!INCLUDE[prodshort](includes/prodshort.md)]in SUPER-käyttöoikeusjoukko, koska se helpottaa hallintatehtäviä, kuten integraation määrittämistä muiden sovellusten kanssa.</span><span class="sxs-lookup"><span data-stu-id="2481d-115">It's a best practice to make sure that the Office 365 administrator also has the SUPER permission set in [!INCLUDE[prodshort](includes/prodshort.md)] because that makes many administrative tasks easier, including setting up integration with other apps.</span></span>

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="2481d-116">Paikallisten käyttöönottojen käyttäjät</span><span class="sxs-lookup"><span data-stu-id="2481d-116">Users of on-premises deployments</span></span>

<span data-ttu-id="2481d-117">Järjestelmänvalvoja voi valita käyttäjille [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen paikallisten käyttöönottojen eri tunnistetietojen mekanismeista.</span><span class="sxs-lookup"><span data-stu-id="2481d-117">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="2481d-118">Kun olet luonut käyttäjän, annat eri tietoja riippuen tunnistetiedoista, joita käytät tietyssä [!INCLUDE[server](includes/server.md)] -ilmentymässä.</span><span class="sxs-lookup"><span data-stu-id="2481d-118">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="2481d-119">Lisätietoja on [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen kehittäjän ja ITPro-sisällön järjestelmänvalvojan osan [Todennus ja tunnistetietotyypit](/dynamics365/business-central/dev-itpro/administration/users-credential-types) -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="2481d-119">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="2481d-120">Profiilit</span><span class="sxs-lookup"><span data-stu-id="2481d-120">Profiles</span></span>

<span data-ttu-id="2481d-121">Kaikilla yrityksen henkilöille, joilla on [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeus, on määritetty *profiili*, jonka mahdollistaa *roolikeskuksen* käytön.</span><span class="sxs-lookup"><span data-stu-id="2481d-121">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="2481d-122">Profiilit ovat niiden [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjien kokoelmia, jotka jakavat saman roolikeskuksen.</span><span class="sxs-lookup"><span data-stu-id="2481d-122">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="2481d-123">Roolikeskus on [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen aloituskohta ja kotisivu. Sen avulla tärkeimpien tehtävien aloitus on nopeaa ja se sisältää paljon tietoja työstä, mukaan lukien työn suorituskykyilmaisimet.</span><span class="sxs-lookup"><span data-stu-id="2481d-123">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2481d-124">Et voi lisätä, muokata tai poistaa profiileja nykyisessä [!INCLUDE[d365fin](includes/d365fin_md.md)] online -versiossa.</span><span class="sxs-lookup"><span data-stu-id="2481d-124">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

### <a name="CreateProfile"></a> <span data-ttu-id="2481d-125">Profiilin luonti</span><span class="sxs-lookup"><span data-stu-id="2481d-125">Create a profile</span></span>

1.  <span data-ttu-id="2481d-126">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Profiililuettelo** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="2481d-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profile List**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="2481d-127">Avaa **Uusi profiilikortti** -sivu valitsemalla **Profiililuettelo**-sivulla **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="2481d-127">On the **Profile List** page, choose the **New** action to open the **New Profile Card** page.</span></span>  

3.  <span data-ttu-id="2481d-128">Anna **Profiilin tunnus** -kentässä nimi, joka kuvaa käyttäjien tarkoitettua roolia.</span><span class="sxs-lookup"><span data-stu-id="2481d-128">In the **Profile ID** field, enter a name that describes the intended role of the users.</span></span>  

4.  <span data-ttu-id="2481d-129">Kirjoita **Kuvaus**-kenttään profiilitunnuksen kuvaus, esimerkiksi **Tilausten käsittelijä**.</span><span class="sxs-lookup"><span data-stu-id="2481d-129">In the **Description** field, enter a description of the Profile ID, for example, **Order Processor**.</span></span>  

5.  <span data-ttu-id="2481d-130">Määritä **Roolikeskuksen tunnus** -kenttäään profiiliin liitettävä roolikeskus.</span><span class="sxs-lookup"><span data-stu-id="2481d-130">Set the **Role Center ID** field to the Role Center that you want to assign to the profile.</span></span>  

<span data-ttu-id="2481d-131">Olemassa olevan profiilin muokkaaminen tapahtuu samalla tavalla. Ainoa ero on, että **Profiililuettelo**-sivulla valitaan olemassa oleva profiili **Uusi**-toiminnon sijaan.</span><span class="sxs-lookup"><span data-stu-id="2481d-131">The procedure for modifying an existing profile is the same, except you select an existing profile on the **Profile List** page instead of choosing the **New** action.</span></span>  


### <a name="copy-a-profile"></a><span data-ttu-id="2481d-132">Profiilin kopioiminen</span><span class="sxs-lookup"><span data-stu-id="2481d-132">Copy a profile</span></span>
<span data-ttu-id="2481d-133">Profiilin kopioiminen voi säästää aikaa, jos haluat käyttää profiilissa samanlaisia asetuksia, ja haluat muuttaa vain joitakin asetuksia.</span><span class="sxs-lookup"><span data-stu-id="2481d-133">Copying a profile can save you time if you want to use similar settings on a profile and you only want to change a few settings.</span></span>

1.  <span data-ttu-id="2481d-134">Avaa kopioitava profiili ja valitse sitten **Kopioi profiili** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="2481d-134">Open the profile that you want to copy, and then choose the **Copy Profile** action.</span></span>

2.  <span data-ttu-id="2481d-135">Syötä **Uuden profiilin tunnus** -kenttään sen profiilin nimi, jonka haluat kopioida.</span><span class="sxs-lookup"><span data-stu-id="2481d-135">In **New Profile ID** field, enter a name for the profile that you want to copy.</span></span>

3.  <span data-ttu-id="2481d-136">Määritä **Uuden profiilin alue** -kenttään jokin seuraavista arvoista:</span><span class="sxs-lookup"><span data-stu-id="2481d-136">Set the **New Profile Scope** field to one of the following:</span></span>

    - <span data-ttu-id="2481d-137">**Järjestelmä**, kun haluat määrittää uuden profiilin kaikkien sovellusta käyttävien vuokraajatietokantojen käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="2481d-137">**System** to make the new profile available to all tenant databases that use the application.</span></span>
    - <span data-ttu-id="2481d-138">**Vuokraaja**, kun haluat määrittää profiilin vain nykyisen vuokraajatietokannan käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="2481d-138">**Tenant** to make the new profile available to just the current tenant database.</span></span>
4. <span data-ttu-id="2481d-139">Valitse **OK**-painike, kun olet valmis.</span><span class="sxs-lookup"><span data-stu-id="2481d-139">Choose the **OK** button when done.</span></span>

### <a name="ExportImportProfile"></a><span data-ttu-id="2481d-140">Profiilien vienti ja tuonti</span><span class="sxs-lookup"><span data-stu-id="2481d-140">Export and import profiles</span></span>

<span data-ttu-id="2481d-141">Voit viedä profiileja XML-tiedostoina [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietokantaan ja tuoda niitä tietokannasta.</span><span class="sxs-lookup"><span data-stu-id="2481d-141">You can export and import profiles as XML files to and from the a [!INCLUDE[d365fin](includes/d365fin_md.md)] database.</span></span> <span data-ttu-id="2481d-142">Profiilin vieminen ja tuominen voi säästää aikaa, kun määrität käyttöliittymää. Voit käyttää aiemmin luotua profiilimääritystä sen sijaan, että määrittäisit profiilin alusta alkaen.</span><span class="sxs-lookup"><span data-stu-id="2481d-142">Exporting and importing a profile can save you time when configuring the user interface because you reuse an existing profile configuration instead of having to configure a profile from scratch.</span></span> <span data-ttu-id="2481d-143">Jos profiili on määritetty [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietokannassa ja haluat käyttää sen tai osan samasta profiilimäärityksestä uudelleen toisessa tietokannassa, voit viedä profiilin XML-tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="2481d-143">If you have a profile that is configured in a [!INCLUDE[d365fin](includes/d365fin_md.md)] database and you would like to reuse all or some of the same profile configurations in another database, you can export the profile to an XML file.</span></span> <span data-ttu-id="2481d-144">Tämän jälkeen voit tuoda profiilin XML-tiedoston toiseen tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="2481d-144">Then, you can import the profile XML file into the other database.</span></span>

-   <span data-ttu-id="2481d-145">Voit viedä profiilin joko valitsemalla **Vie profiilit** -toiminto **Profiililuettelo**- tai **Profiilikortti**-sivulla tai etsimällä sen ja avaamalla **Vie profiilit** -sivun.</span><span class="sxs-lookup"><span data-stu-id="2481d-145">To export a profile, you can either choose the **Export Profiles** action from the **Profile List** or **Profile Card** page or you can search for and open the **Export Profiles** page.</span></span> <span data-ttu-id="2481d-146">Tallenna XML-tiedosto tietokoneelle tai verkkoon.</span><span class="sxs-lookup"><span data-stu-id="2481d-146">Save the XML file to a location on your computer or network.</span></span>

-   <span data-ttu-id="2481d-147">Voit tuoda profiilin joko valitsemalla **Tuo profiilit** -toiminto **Profiililuettelo**-sivulla tai etsimällä sen ja avaamalla **Tuo profiilit** -sivun.</span><span class="sxs-lookup"><span data-stu-id="2481d-147">To import a profile, you can either choose the **Import Profile** action from the **Profile List** page, or you can search for and open the **Import Profiles** page.</span></span> 

    > [!NOTE]  
    >  <span data-ttu-id="2481d-148">Et voi tuoda profiilia, joka on jo tietokannassa, vaikka XML-tiedosto olisi eriniminen tai sillä olisi eri sisältö.</span><span class="sxs-lookup"><span data-stu-id="2481d-148">You cannot import a profile that already exists in the database, even though the XML file is named differently or has different content.</span></span> <span data-ttu-id="2481d-149">Poista olemassa oleva profiili ennen kuin tuot uuden profiilin.</span><span class="sxs-lookup"><span data-stu-id="2481d-149">You must delete the existing profile before you can import the new profile.</span></span>


## <a name="configuration-and-personalization"></a><span data-ttu-id="2481d-150">Kokoonpano ja mukautus</span><span class="sxs-lookup"><span data-stu-id="2481d-150">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

<span data-ttu-id="2481d-151">Käyttäjät voivat mukauttaa henkilökohtaisen versionsa käyttöliittymää mukauttamalla käyttöliittymää oman kirjautumistunnuksensa osalta.</span><span class="sxs-lookup"><span data-stu-id="2481d-151">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="2481d-152">Järjestelmänvalvoja voi poistaa tämän mukautuksen.</span><span class="sxs-lookup"><span data-stu-id="2481d-152">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="2481d-153">Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="2481d-153">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="2481d-154">Katso myös</span><span class="sxs-lookup"><span data-stu-id="2481d-154">See Also</span></span>  
[<span data-ttu-id="2481d-155">Käyttäjien ja käyttöoikeuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="2481d-155">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="2481d-156">Mukautuksen hallinta järjestelmänvalvojana</span><span class="sxs-lookup"><span data-stu-id="2481d-156">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="2481d-157">Työtilan mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="2481d-157">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  

