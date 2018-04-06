---
title: "Sandbox-ympäristön luominen | Microsoft Docs"
description: "Luo tutustumista, oppimista, esittelyä, kehittämistä ja testausta varten sopiva ympäristö."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 08/18/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8451e456d03c9429ff2e04f4e0664ae240f872c2
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="create-a-sandbox-environment"></a><span data-ttu-id="0f693-103">Sandbox-ympäristön luominen</span><span class="sxs-lookup"><span data-stu-id="0f693-103">Create a Sandbox Environment</span></span>
<span data-ttu-id="0f693-104">Sandbox-ympäristö (esiversio) on [!INCLUDE[d365fin](includes/d365fin_md.md)]in tuotantoympäristöön kuulumaton ilmentymä.</span><span class="sxs-lookup"><span data-stu-id="0f693-104">A sandbox environment (Preview) is a non-production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0f693-105">Tuotannosta eristetty Sandbox-ympäristö on paikka, jossa voi turvallisesti tutustua palveluun, opetella sen käyttöä sekä kehittää ja testata sitä ilman, että tuotantoympäristön tiedot ja asetukset vaarantuvat.</span><span class="sxs-lookup"><span data-stu-id="0f693-105">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>

## <a name="to-create-a-sandbox-environment"></a><span data-ttu-id="0f693-106">Sandbox-ympäristön luominen</span><span class="sxs-lookup"><span data-stu-id="0f693-106">To create a sandbox environment</span></span>
<span data-ttu-id="0f693-107">Tarvitse sandbox-ympäristön luontia varten [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilauksen.</span><span class="sxs-lookup"><span data-stu-id="0f693-107">You must have a subscription to [!INCLUDE[d365fin](includes/d365fin_md.md)] to be able to create a sandbox environment.</span></span> <span data-ttu-id="0f693-108">Kutakin tilausta kohden voi olla vain yksi sandbox-ympäristö.</span><span class="sxs-lookup"><span data-stu-id="0f693-108">There can only be one sandbox environment per subscription.</span></span>

1. <span data-ttu-id="0f693-109">Kirjaudu [!INCLUDE[d365fin](includes/d365fin_md.md)]-palvelun tuotantoilmentymään.</span><span class="sxs-lookup"><span data-stu-id="0f693-109">Sign in to your production instance of the [!INCLUDE[d365fin](includes/d365fin_md.md)] service.</span></span>
2. <span data-ttu-id="0f693-110">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sandbox-ympäristö** ja valitse liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="0f693-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
<span data-ttu-id="0f693-111">![Sandbox-ympäristön määrittäminen](./media/across-sandbox/sandbox-environment-setup.png)</span><span class="sxs-lookup"><span data-stu-id="0f693-111">![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png)</span></span>
3. <span data-ttu-id="0f693-112">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="0f693-112">Select **Create**.</span></span>  
  <span data-ttu-id="0f693-113">Selaimeen avautuu uusi välilehti, jossa voi viimeistellä sandbox-ympäristön määrittämisen.</span><span class="sxs-lookup"><span data-stu-id="0f693-113">Another tab in your browser will open for finishing the setup of your sandbox environment.</span></span>
> [!NOTE]  
>  <span data-ttu-id="0f693-114">Jos ponnahdusikkunoiden esto on selaimessa käytössä, vaihda sen asetukset sallimaan financials.dynamics.com-osoitteen URL-osoitteet.</span><span class="sxs-lookup"><span data-stu-id="0f693-114">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.financials.dynamics.com address.</span></span>   

4. <span data-ttu-id="0f693-115">Kun sandbox-ympäristö on valmis, sinut uudelleenohjataan sandbox-ympäristön ohjattuun aloitustoimintoon.</span><span class="sxs-lookup"><span data-stu-id="0f693-115">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<span data-ttu-id="0f693-116">![Sandbox-ympäristön ohjattu aloitustoiminto](./media/across-sandbox/sandbox-wizard.png)</span><span class="sxs-lookup"><span data-stu-id="0f693-116">![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png)</span></span>

5. <span data-ttu-id="0f693-117">Valitse **Lisätietoja**, jos haluat lukea skenaarioista, joita voit kokeilla sandbox-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="0f693-117">Choose **Learn more** to read about scenarios that you can try in a sandbox environment.</span></span> <span data-ttu-id="0f693-118">Valitse sen sijaan **Sulje**, jos haluat jatkaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in sanbox-ilmentymän roolikeskukseen.</span><span class="sxs-lookup"><span data-stu-id="0f693-118">Or, choose **Close** to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>
6. <span data-ttu-id="0f693-119">Roolikeskuksen yläreunaan avautuvassa ilmoituksessa ilmoitetaan, että kyse on sandbox-ympäristöstä.</span><span class="sxs-lookup"><span data-stu-id="0f693-119">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="0f693-120">Ympäristön tyyppi näkyy myös asiakasohjelman otsikkopalkissa.</span><span class="sxs-lookup"><span data-stu-id="0f693-120">You can also see the type of the environment in the title bar of the client.</span></span>
<span data-ttu-id="0f693-121">![Sandbox-ympäristön roolikeskuksen ilmoitus](./media/across-sandbox/sandbox-rolecenter-notification.png)</span><span class="sxs-lookup"><span data-stu-id="0f693-121">![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png)</span></span>  
<span data-ttu-id="0f693-122">Sandbox-ympäristöön on luotu täysin uusi vuokraaja.</span><span class="sxs-lookup"><span data-stu-id="0f693-122">In the sandbox environment, a brand-new tenant has been created.</span></span> <span data-ttu-id="0f693-123">Vuokraajaan on ladattu CRONUS-yrityksen oletusesittelytiedot.</span><span class="sxs-lookup"><span data-stu-id="0f693-123">This tenant is loaded with default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="0f693-124">Mitään tietoja ei kopioida tai muutoin siirretä tuotantoympäristöstä sandbox-ympäristön luonnin aikana.</span><span class="sxs-lookup"><span data-stu-id="0f693-124">No data is copied or otherwise transferred from the production environment during the sandbox creation.</span></span>
7.  <span data-ttu-id="0f693-125">Voit palata koska tahansa **Sandbox-ympäristö**-sivulle ja palauttaa sandbox-ympäristön alkuasetuksiin.</span><span class="sxs-lookup"><span data-stu-id="0f693-125">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>
> [!NOTE]  
>  <span data-ttu-id="0f693-126">Sandbox-ympäristön palauttaminen alkuasetuksiin poistaa sen kokonaan, ja voit luoda sen uudelleen oletusesittelytiedoilla.</span><span class="sxs-lookup"><span data-stu-id="0f693-126">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

8.  <span data-ttu-id="0f693-127">Voit siirtyä tuotanto- ja sandbox-ympäristöjen välillä Business Central -sovellusten käynnistysohjelman avulla.</span><span class="sxs-lookup"><span data-stu-id="0f693-127">To switch between your production and sandbox environments, you can use the Business Central app launcher.</span></span>
<span data-ttu-id="0f693-128">![Sandbox-ympäristön Dynamics 365 -valikko](./media/across-sandbox/sandbox-dynamics365-menu.png)</span><span class="sxs-lookup"><span data-stu-id="0f693-128">![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png)</span></span>

9.  <span data-ttu-id="0f693-129">Järjestelmänvalvoja tai toinen käyttäjä voi rajoittaa tai jopa estää joidenkin käyttäjien mahdollisuutta käyttää sandbox-ympäristöä.</span><span class="sxs-lookup"><span data-stu-id="0f693-129">It is possible for an administrator or another user to limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="0f693-130">Se voidaan tehdä tuotteen vakiotietoturvaominaisuuksilla, kuten käyttäjäkortin, käyttäjäryhmien tai käyttöoikeusjoukkojen avulla.</span><span class="sxs-lookup"><span data-stu-id="0f693-130">This can be done by using the standard security features of the product, such as the User card, User Groups, and Permission Sets.</span></span>

![Sandbox-ympäristön käyttöoikeuksien joukot](./media/across-sandbox/sandbox-permission-sets.png)

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="0f693-132">Sandbox-ympäristön lisätoiminnot</span><span class="sxs-lookup"><span data-stu-id="0f693-132">Advanced functionality in the sandbox environment</span></span>
### <a name="the-in-client-designer"></a><span data-ttu-id="0f693-133">Asiakasohjelman suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="0f693-133">The in-client designer</span></span>
<span data-ttu-id="0f693-134">Sandbox-ympäristössä on otettu käyttöön asiakasohjelman suunnittelutoiminto, ja voit aktivoida sen valitsemalla suunnittelukuvakkeen</span><span class="sxs-lookup"><span data-stu-id="0f693-134">In a sandbox environment, you will find the in-client designer feature enabled, which you can activate by selecting the design icon</span></span> ![Rakennenäkymä](./media/across-sandbox/sandbox-inclient-design-icon.png) <span data-ttu-id="0f693-136">-sivulla.</span><span class="sxs-lookup"><span data-stu-id="0f693-136">on a page.</span></span>

![Asiakasohjelman suunnittelutoiminto](./media/across-sandbox/sandbox-inclient-designer.png)

### <a name="enable-the-advanced-user-experience"></a><span data-ttu-id="0f693-138">Käyttäjäkokemuksen lisätoimintojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="0f693-138">Enable the advanced user experience</span></span>
<span data-ttu-id="0f693-139">[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisätoiminnot (kaikki toiminnot) voi ottaa käyttöön kokeiltavaksi sandbox-ympäristön vuokraajassa määrittämällä **Kokemus**-kentän **Yrityksen tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="0f693-139">It is possible to enable and try the advanced (full) functionality of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

![Sandbox-ympäristön lisäasetukset](./media/across-sandbox/sandbox-advanced.png)

![Sandbox-tuotantoympäristö](./media/across-sandbox/sandbox-production.png)

<span data-ttu-id="0f693-142">Kun olet ottanut lisäasetukset käyttöön sandbox-ympäristön vuokraajassa, voit käyttää kaikkia vakioprofiileja ja -roolikeskuksia.</span><span class="sxs-lookup"><span data-stu-id="0f693-142">After you’ve enabled the advanced functionality in a sandbox tenant, you get access to all the standard Profiles and Role Centers.</span></span> <span data-ttu-id="0f693-143">Voit myös luoda täysin määritetyn arviointiyrityksen. Tämä yritys sisältää esittelytiedot ja tuotteen lisäalueiden käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="0f693-143">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span>

![Sandbox-ympäristön uusi yritys](./media/across-sandbox/sandbox-newcompany.png)


## <a name="see-also"></a><span data-ttu-id="0f693-145">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0f693-145">See Also</span></span>
<span data-ttu-id="0f693-146">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0f693-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

