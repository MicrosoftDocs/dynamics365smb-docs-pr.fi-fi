---
title: "Invoicingin ja Finance and Operations, Business editionin käyttäminen | Microsoft Docs"
description: "Ratkaisu Microsoft Invoicingin käyttämiseen, kun olet rekisteröitynyt Dynamics 365 for Finance and Operations, Business editioniin."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: abceec5b1bc588e2842d0f512240c30eccbf6f8e
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a><span data-ttu-id="9db0f-103">Saman Office 365 -tilin käyttäminen [!INCLUDE[d365fin](includes/d365fin_long_md.md)]:ssä ja Microsoft Invoicingissa</span><span class="sxs-lookup"><span data-stu-id="9db0f-103">Using the same Office 365 Account in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="9db0f-104">Kun rekisteröidyt [!INCLUDE[d365fin](includes/d365fin_md.md)]:n kokeiluversioon, voit siirtyä 30 päivän arviointivaiheeseen, aloittaa tilauksen tai lopettaa [!INCLUDE[d365fin](includes/d365fin_md.md)]:n käytön.</span><span class="sxs-lookup"><span data-stu-id="9db0f-104">When you sign up for a trial with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="9db0f-105">Kaikissa näissä tapauksissa Office-portaaliin kirjautumisen jälkeen näkyvissä voi olla **Business center** -ruutu, jota voi napsauttaa.</span><span class="sxs-lookup"><span data-stu-id="9db0f-105">In all cases, if you log into the Office Portal, you might see a tile called **Business center** and click it.</span></span> <span data-ttu-id="9db0f-106">Se sisältyy Office 365 Business Premium -tilaukseen, joten kaikki Office-portaalin käyttäjät eivät näe ruutua.</span><span class="sxs-lookup"><span data-stu-id="9db0f-106">This is part of the Office 365 Business Premium subscription, so not everyone will see that tile in the Office Portal.</span></span>  

<span data-ttu-id="9db0f-107">Jos Business center -ruutu on käytettävissä, siinä on **Invoicing**-osa.</span><span class="sxs-lookup"><span data-stu-id="9db0f-107">If you do access the Business center, you will see a section called **Invoicing**.</span></span> <span data-ttu-id="9db0f-108">Jos yrität käyttää tätä osaa, saat ilmoituksen, jonka mukaan et voi käyttää Microsoft Invoicingia, koska tiliä käytetään [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä.</span><span class="sxs-lookup"><span data-stu-id="9db0f-108">If you access that section, you will see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="9db0f-109">Saat samanlaisen ilmoituksen, jos asennat Invoicingin mobiilisovelluksen.</span><span class="sxs-lookup"><span data-stu-id="9db0f-109">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="9db0f-110">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="9db0f-110">Workaround</span></span>
<span data-ttu-id="9db0f-111">Invoicing ja [!INCLUDE[d365fin](includes/d365fin_md.md)] jakavat saman alustan.</span><span class="sxs-lookup"><span data-stu-id="9db0f-111">Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)] have a shared platform.</span></span> <span data-ttu-id="9db0f-112">Tämän vuoksi sinut tunnistetaan [!INCLUDE[d365fin](includes/d365fin_md.md)]:n nykyiseksi käyttäjäksi, kun valitset Business center -ruudussa Invoicing.</span><span class="sxs-lookup"><span data-stu-id="9db0f-112">That means that you are recognized as an existing user of [!INCLUDE[d365fin](includes/d365fin_md.md)] when you click Invoicing in the Business center.</span></span> <span data-ttu-id="9db0f-113">Syynä on se, että Invoicing ei voi käyttää samaa yritystä kuin [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9db0f-113">The reason is that Invoicing cannot use the same company as [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="9db0f-114">Tämän vuoksi sinun on kirjauduttava [!INCLUDE[d365fin](includes/d365fin_md.md)]:een ja nimettävä aiemmin luotu yritys uudelleen. Seuraavaksi sinun on luotava uusi yritys, jota voit käyttää Invoicingissa.</span><span class="sxs-lookup"><span data-stu-id="9db0f-114">So you will have to log into [!INCLUDE[d365fin](includes/d365fin_md.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="9db0f-115">Mitään tietoja ei siirretä tai korvata tätä ratkaisua käytettäessä.</span><span class="sxs-lookup"><span data-stu-id="9db0f-115">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="9db0f-116">Yrityksen nimeäminen uudelleen</span><span class="sxs-lookup"><span data-stu-id="9db0f-116">To rename your company</span></span>
1.  <span data-ttu-id="9db0f-117">Kirjaudu [!INCLUDE[d365fin](includes/d365fin_md.md)]:een.</span><span class="sxs-lookup"><span data-stu-id="9db0f-117">Sign in to your [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
2.  <span data-ttu-id="9db0f-118">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Omat yritykset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="9db0f-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Companies**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="9db0f-119">Valitse **Omat yritykset** -ikkunassa **Muokkaa luetteloa** -painike.</span><span class="sxs-lookup"><span data-stu-id="9db0f-119">In the **Companies** window, choose the **Edit List** button.</span></span>  
4.  <span data-ttu-id="9db0f-120">Vaihda *Oma yritys* -merkinnän nimi.</span><span class="sxs-lookup"><span data-stu-id="9db0f-120">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="9db0f-121">Odota useita minuutteja.</span><span class="sxs-lookup"><span data-stu-id="9db0f-121">Wait a number of minutes.</span></span> <span data-ttu-id="9db0f-122">Taustalla olevaan tietokantaa tehdä muutoksia, ja kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="9db0f-122">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
5.  <span data-ttu-id="9db0f-123">Kun järjestelmä on taas valmis, valitse **Luo uusi yritys** -painike.</span><span class="sxs-lookup"><span data-stu-id="9db0f-123">When the system is ready again, choose the **Create New Company** button.</span></span>  
6.  <span data-ttu-id="9db0f-124">Määritä avautuvassa valintaikkunassa nimeksi *Oma yritys* ja valitse **Suite-tuotanto - Vain määritystiedot** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="9db0f-124">In the dialog that appears, specify the name as *My Company*, and choose the **Suite Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="9db0f-125">Myös tämä toiminto kestää useita minuutteja.</span><span class="sxs-lookup"><span data-stu-id="9db0f-125">This again takes a number of minutes.</span></span> <span data-ttu-id="9db0f-126">Kun prosessi on valmis, voi käyttää Invoicingia Office 365 Business Premiumin osana.</span><span class="sxs-lookup"><span data-stu-id="9db0f-126">When the process completes, you will be able to access Invoicing as part of your Office 365 Business Premium experience.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="9db0f-127">Mitä tiedoille tapahtuu?</span><span class="sxs-lookup"><span data-stu-id="9db0f-127">What about my data?</span></span>
<span data-ttu-id="9db0f-128">Kun nimeät alkuperäisen oman yrityksen uudelleen, tietokantataulukot, joihin aiemmin luodut [!INCLUDE[d365fin](includes/d365fin_md.md)]:n tiedot on tallennettu, nimetään uudelleen mutta itse tietoihin ei kosketa.</span><span class="sxs-lookup"><span data-stu-id="9db0f-128">When you rename the original My Company, the database tables that store your existing [!INCLUDE[d365fin](includes/d365fin_md.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="9db0f-129">Jos käytät sekä Invoicingia että [!INCLUDE[d365fin](includes/d365fin_md.md)]:tä, tiedot tallennetaan kahteen eri säilöön (kahteen yritykseen).</span><span class="sxs-lookup"><span data-stu-id="9db0f-129">If you use both Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="9db0f-130">Mitään ei jaeta, joten kummankin yrityksen asiakkaita ja nimikkeitä on hallittava erikseen.</span><span class="sxs-lookup"><span data-stu-id="9db0f-130">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9db0f-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="9db0f-131">See Also</span></span>
[<span data-ttu-id="9db0f-132">Usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="9db0f-132">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="9db0f-133">Asetukset ja hallinto</span><span class="sxs-lookup"><span data-stu-id="9db0f-133">Setup and Administration</span></span>](admin-setup-and-administration.md)  

