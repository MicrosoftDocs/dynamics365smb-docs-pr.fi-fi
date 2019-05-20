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
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 37cdf2d7dcc46b1286cbb7a5ad620547e364309e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250593"
---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="4b972-103">Mukautuksen hallinta järjestelmänvalvojana</span><span class="sxs-lookup"><span data-stu-id="4b972-103">Managing Personalization as an Administrator</span></span>

<span data-ttu-id="4b972-104"> Käyttäjät voivat mukauttaa työtilansa omien mieltymystensä mukaiseksi.</span><span class="sxs-lookup"><span data-stu-id="4b972-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="4b972-105">Järjestelmänvalvojana ohjaat ja hallitset mukauttamista seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4b972-105">As an administrator, you control and manage personalization by:</span></span>

-   <span data-ttu-id="4b972-106">Ottamalla koko sovelluksen mukauttamisominaisuuden käyttöön tai poistamalla sen käytöstä (vain paikalliset asetukset.)</span><span class="sxs-lookup"><span data-stu-id="4b972-106">Enabling or disabling the personalization feature for the entire the application (on-premises installation only).</span></span>
-   <span data-ttu-id="4b972-107">Ottamalla mukauttamisominaisuuden käyttöön vain tietyn profiilin käyttäjille tai poistamalla sen heiltä käytöstä.</span><span class="sxs-lookup"><span data-stu-id="4b972-107">Enabling or disabling the personalization feature for users of a specific profile.</span></span>
-   <span data-ttu-id="4b972-108">Poistamalla käyttäjien mahdollisesti tekemät sivun mukauttamiset.</span><span class="sxs-lookup"><span data-stu-id="4b972-108">Clearing any page personalizations that users have made.</span></span>

## <a name="EnablePersonalization"></a><span data-ttu-id="4b972-109">Mukauttamisen ottaminen käyttöön tai poistaminen käytöstä (vain paikallinen versio)</span><span class="sxs-lookup"><span data-stu-id="4b972-109">To enable or disable personalization (On-Premises Only)</span></span>

<span data-ttu-id="4b972-110">Mukauttamista ei ole oletusarvoisesti otettu asiakasohjelmassa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4b972-110">By default, personalization is not enabled in the client.</span></span> <span data-ttu-id="4b972-111">Mukauttaminen otetaan käyttöön tai poistetaan käytöstä muokkaamalla asiakasohjelmien käytössä olevan Business Central Web Server -esiintymän määritystiedostoa (navsettings.json).</span><span class="sxs-lookup"><span data-stu-id="4b972-111">You enable or disable personalization by modifying the configuration file (navsettings.json) of the Business Central Web Server instance that serves the clients.</span></span>

1. <span data-ttu-id="4b972-112">Voit ottaa mukauttamisen käyttöön lisäämällä seuraavan rivin navsettings.json-tiedostoon:</span><span class="sxs-lookup"><span data-stu-id="4b972-112">To enable personalization, add the following line in the navsettings.json file:</span></span>

    ```
    "PersonalizationEnabled": "true"
    ```

    <span data-ttu-id="4b972-113">Voit poistaa mukauttamisen käytöstä poistamalla tämän rivin tai muuttamalla sen seuraavaanlaiseksi:</span><span class="sxs-lookup"><span data-stu-id="4b972-113">To disable personalization, remove this line or change it to:</span></span>

    ```
    "PersonalizationEnabled": "false"
    ```

    <span data-ttu-id="4b972-114">Lisätietoja navsettings.json-tiedoston muokkaamisesta on kohdassa [Navsettings.json-tiedoston muokkaaminen suoraan](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span><span class="sxs-lookup"><span data-stu-id="4b972-114">For more information about how to modify the navsettings.json file, see [Modify the navsettings.json file directly](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span></span>

2. <span data-ttu-id="4b972-115">Luo ja lataa sovelluksen symboleja.</span><span class="sxs-lookup"><span data-stu-id="4b972-115">Generate and download the application symbols.</span></span>

    <span data-ttu-id="4b972-116">Tämä on valinnainen vaihe, eikä mukauttaminen käyttöönottaminen edellytä sitä.</span><span class="sxs-lookup"><span data-stu-id="4b972-116">This step is optional, and not required to enable personalization.</span></span> <span data-ttu-id="4b972-117">Se kuitenkin varmistaa, että kehittäjien luomia uusia sivuja voidaan mukauttaa.</span><span class="sxs-lookup"><span data-stu-id="4b972-117">However, it ensures that new pages that are created by developers can be personalized.</span></span>

    1. <span data-ttu-id="4b972-118">Luo ensiksi symbolit suorittamalla finsql.exe `generatesymbolreference`-komennolla.</span><span class="sxs-lookup"><span data-stu-id="4b972-118">First, you generate the symbols by running finsql.exe with `generatesymbolreference` command.</span></span> <span data-ttu-id="4b972-119">Finsql.exe-tiedosto sijaitsee [!INCLUDE[server](includes/server.md)]- ja CSIDE (Dynamics NAV Development Environment) -asennuskansiossa.</span><span class="sxs-lookup"><span data-stu-id="4b972-119">The finsql.exe file is located in the installation folder for the [!INCLUDE[server](includes/server.md)] and Dynamics NAV Development Environment (CSIDE).</span></span> <span data-ttu-id="4b972-120">Voit luoda symbolit avaamalla komentokehotteen, muuttamalla hakemiston, johon tiedosto on tallennettu, ja suorittamalla sitten seuraavan komennon:</span><span class="sxs-lookup"><span data-stu-id="4b972-120">To generate the symbols, open a command prompt, change to the directory where the file is store, and the run the following command:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    <span data-ttu-id="4b972-121">Esimerkiksi:</span><span class="sxs-lookup"><span data-stu-id="4b972-121">For example:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    <span data-ttu-id="4b972-122">Lisätietoja on kohdassa [C/SIDE:n ja AL:n suorittaminen rinnakkainen](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span><span class="sxs-lookup"><span data-stu-id="4b972-122">For more information, see [Running C/SIDE and AL Side-by-Side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span></span>

    2. <span data-ttu-id="4b972-123">Määritä [!INCLUDE[nav_server_md](includes/nav_server_md.md)] -esiintymäksi **Ota sovelluksen symboliviittaukset käyttöön palvelimen käynnistyessä** (EnableSymbolLoadingAtServerStartup).</span><span class="sxs-lookup"><span data-stu-id="4b972-123">Configure [!INCLUDE[nav_server_md](includes/nav_server_md.md)] instance to **Enable loading application symbol references at server startup** (EnableSymbolLoadingAtServerStartup).</span></span> <span data-ttu-id="4b972-124">Lisätietoja on kohdassa [Business Central Serverin määrittäminen](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span><span class="sxs-lookup"><span data-stu-id="4b972-124">For more information, see [Configuring Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span></span>

## <a name="to-disable-personalization-for-a-profile"></a><span data-ttu-id="4b972-125">Profiilin mukauttamisen poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="4b972-125">To disable personalization for a profile</span></span>

<span data-ttu-id="4b972-126">Voit estää sivujen mukauttamisen kaikilta tiettyyn profiiliin kuuluvilta käyttäjiltä.</span><span class="sxs-lookup"><span data-stu-id="4b972-126">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>

1. <span data-ttu-id="4b972-127">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Profiilit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4b972-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="4b972-128">Valitse luettelossa muokattava profiili.</span><span class="sxs-lookup"><span data-stu-id="4b972-128">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="4b972-129">Valitse **Poista mukauttaminen käytöstä** -valintaruutuja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b972-129">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="to-clear-user-personalizations"></a><span data-ttu-id="4b972-130">Käyttäjän mukautusten tyhjentäminen</span><span class="sxs-lookup"><span data-stu-id="4b972-130">To clear user personalizations</span></span>

<span data-ttu-id="4b972-131">Mukautetun sivun muutosten tyhjentäminen palauttaa sivun mukautuksia edeltävän alkuperäisen asettelun.</span><span class="sxs-lookup"><span data-stu-id="4b972-131">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="4b972-132">Käyttäjien sivulle tekemät mukautukset voi tyhjentää kahdella tavalla: käyttämällä **Poista käyttäjän mukautus** -sivua tai käyttämällä **Käyttäjän mukautuskortti** -sivua.</span><span class="sxs-lookup"><span data-stu-id="4b972-132">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="4b972-133">Käyttäjän mukautusten tyhjentäminen Poista käyttäjän mukautus -sivun avulla</span><span class="sxs-lookup"><span data-stu-id="4b972-133">To clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="4b972-134">Voit tyhjentää **Poista käyttäjän mukautus** -sivulla mukautukset kultakin käyttäjältä sivukohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="4b972-134">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1. <span data-ttu-id="4b972-135">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poista käyttäjän mukautus** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4b972-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="4b972-136">Sivulla on luettelo kaikista mukautetuista sivuista ja käyttäjästä, jolle se kuuluu.</span><span class="sxs-lookup"><span data-stu-id="4b972-136">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="4b972-137">**Vanha mukautus** -sarakkeiden valintamerkki ilmaisee, että mukautus tehtiin [!INCLUDE[d365fin](includes/d365fin_md.md)]in vanhassa versiossa, jossa mukautusta käsiteltiin eri tavalla kuin nyt.</span><span class="sxs-lookup"><span data-stu-id="4b972-137">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="4b972-138">Mukautus estetään näiden sivujen mukautusta yrittäviltä käyttäjiltä, elleivät he ensin valitse sivun lukituksen poistamista.</span><span class="sxs-lookup"><span data-stu-id="4b972-138">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="4b972-139">Lisätietoja on kohdassa [Sivun mukauttamisen estäminen lukitsemalla](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="4b972-139">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="4b972-140">Valitse ensin poistettava tapahtuma ja sitten **Poista**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="4b972-140">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="4b972-141">Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.</span><span class="sxs-lookup"><span data-stu-id="4b972-141">The user will see the changes the next time they sign-in.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="4b972-142">Käyttäjän mukautusten tyhjentäminen Käyttäjän mukautuskortti -sivun avulla</span><span class="sxs-lookup"><span data-stu-id="4b972-142">To clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="4b972-143">Voit tyhjentää **Käyttäjän mukautuskortti** -sivulla tietyn käyttäjän kaikki mukautukset.</span><span class="sxs-lookup"><span data-stu-id="4b972-143">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="4b972-144">Tämä edellyttää taulukon 2000000072 **Profiili** kirjoitusoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="4b972-144">This requires write permission to Table 2000000072 **Profile**.</span></span>

1. <span data-ttu-id="4b972-145">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän mukautus** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="4b972-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="4b972-146">**Käyttäjän mukautus** -sivulla on luettelo kaikista käyttäjistä, joilla mahdollisesti on mukautettuja sivuja.</span><span class="sxs-lookup"><span data-stu-id="4b972-146">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="4b972-147">Jos käyttäjä ei löydy luettelosta, kyseisellä käyttäjällä ei ole mukautettuja sivuja.</span><span class="sxs-lookup"><span data-stu-id="4b972-147">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="4b972-148">Valitse ensin käyttäjä luettelossa ja sitten **Muokkaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="4b972-148">Select the user from the list, and then choose the **Edit** action.</span></span>

3. <span data-ttu-id="4b972-149">Valitse **Toiminnot**-välilehdessä **Tyhjennä mukautetut sivut**.</span><span class="sxs-lookup"><span data-stu-id="4b972-149">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="4b972-150">Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.</span><span class="sxs-lookup"><span data-stu-id="4b972-150">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b972-151">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4b972-151">See Also</span></span>
[<span data-ttu-id="4b972-152">Työtilan mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="4b972-152">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="4b972-153">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4b972-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4b972-154">Perusasetusten muuttaminen</span><span class="sxs-lookup"><span data-stu-id="4b972-154">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="4b972-155">Näytettävien ominaisuuksien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="4b972-155">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
