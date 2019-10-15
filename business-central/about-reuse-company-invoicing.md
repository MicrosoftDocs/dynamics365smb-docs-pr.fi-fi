---
title: Invoicing- ja Business Central -sovellusten käyttäminen | Microsoft Docs
description: Ratkaisu, jonka avulla voi käyttää Microsoft Invoicingia, kun olet rekisteröitynyt Dynamics 365 Business Centraliin.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Office 365
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 354babea367b80cdb0eae4078f6111d44583df9e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300759"
---
# <a name="using-the-same-office-365-account-in-included365finincludesd365fin_long_mdmd-and-microsoft-invoicing"></a><span data-ttu-id="57745-103">Saman Office 365 -tilin käyttäminen [!INCLUDE[d365fin](includes/d365fin_long_md.md)]:ssä ja Microsoft Invoicingissa</span><span class="sxs-lookup"><span data-stu-id="57745-103">Using the same Office 365 Account in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="57745-104">Kun rekisteröidyt [!INCLUDE[d365fin](includes/d365fin_md.md)]:n kokeiluversioon, voit siirtyä 30 päivän arviointivaiheeseen, aloittaa tilauksen tai lopettaa [!INCLUDE[d365fin](includes/d365fin_md.md)]:n käytön.</span><span class="sxs-lookup"><span data-stu-id="57745-104">When you sign up for a trial with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="57745-105">Kaikissa näissä tapauksissa Office-portaaliin kirjautumisen jälkeen näkyvissä voi olla **Microsoft Invoicing** -ruutu, jota voi napsauttaa.</span><span class="sxs-lookup"><span data-stu-id="57745-105">In all cases, if you sign in to the Office Portal, you might see a tile called **Microsoft Invoicing** and click it.</span></span> <span data-ttu-id="57745-106">Se sisältyy Office 365 Business Premium -tilaukseen, joten kaikki Office-portaalin käyttäjät eivät näe ruutua.</span><span class="sxs-lookup"><span data-stu-id="57745-106">This is part of the Office 365 Business Premium subscription, so not everyone will see that tile in the Office Portal.</span></span>  

<span data-ttu-id="57745-107">Jos yrität käyttää Microsoft Invoicingia, saat ilmoituksen, jonka mukaan et voi käyttää Microsoft Invoicingia, koska tiliä käytetään [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="57745-107">If you access Microsoft Invoicing, you will see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="57745-108">Saat samanlaisen ilmoituksen, jos asennat Invoicingin mobiilisovelluksen.</span><span class="sxs-lookup"><span data-stu-id="57745-108">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="57745-109">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="57745-109">Workaround</span></span>
<span data-ttu-id="57745-110">Invoicing ja [!INCLUDE[d365fin](includes/d365fin_md.md)] jakavat saman alustan.</span><span class="sxs-lookup"><span data-stu-id="57745-110">Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)] have a shared platform.</span></span> <span data-ttu-id="57745-111">Tämän vuoksi sinut tunnistetaan nykyiseksi [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjäksi, kun Invoicing valitaan Office-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="57745-111">That means that you are recognized as an existing user of [!INCLUDE[d365fin](includes/d365fin_md.md)] when you click Invoicing in the Office Portal.</span></span> <span data-ttu-id="57745-112">Syynä on se, että Invoicing ei voi käyttää samaa yritystä kuin [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="57745-112">The reason is that Invoicing cannot use the same company as [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="57745-113">Tämän vuoksi sinun on kirjauduttava [!INCLUDE[d365fin](includes/d365fin_md.md)]:een ja nimettävä aiemmin luotu yritys uudelleen. Seuraavaksi sinun on luotava uusi yritys, jota voit käyttää Invoicingissa.</span><span class="sxs-lookup"><span data-stu-id="57745-113">So you will have to sign in to [!INCLUDE[d365fin](includes/d365fin_md.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="57745-114">Mitään tietoja ei siirretä tai korvata tätä ratkaisua käytettäessä.</span><span class="sxs-lookup"><span data-stu-id="57745-114">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="57745-115">Yrityksen nimeäminen uudelleen</span><span class="sxs-lookup"><span data-stu-id="57745-115">To rename your company</span></span>
1. <span data-ttu-id="57745-116">Kirjaudu [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="57745-116">Sign in to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
2. <span data-ttu-id="57745-117">Valitse oikeassa yläkulmassa **Asetukset**-kuvake ![Asetukset](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") ja valitse sitten **Omat asetukset**.</span><span class="sxs-lookup"><span data-stu-id="57745-117">In the top right corner, choose the **Settings** icon ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center"), and then choose **My Settings**.</span></span>
3. <span data-ttu-id="57745-118">Valitse toinen yritys **Yritys**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="57745-118">In the **Company** field, choose a different company.</span></span>
4. <span data-ttu-id="57745-119">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yritykset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="57745-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.</span></span>  
5. <span data-ttu-id="57745-120">Valitse **Omat yritykset** -sivulla **Muokkaa luetteloa**.</span><span class="sxs-lookup"><span data-stu-id="57745-120">On the **Companies** page, choose **Edit List**.</span></span>  
6. <span data-ttu-id="57745-121">Vaihda *Oma yritys* -merkinnän nimi.</span><span class="sxs-lookup"><span data-stu-id="57745-121">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="57745-122">Odota useita minuutteja.</span><span class="sxs-lookup"><span data-stu-id="57745-122">Wait a number of minutes.</span></span> <span data-ttu-id="57745-123">Taustalla olevaan tietokantaa tehdä muutoksia, ja kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="57745-123">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
7.  <span data-ttu-id="57745-124">Kun järjestelmä on taas valmis, valitse **Luo uusi yritys** -painike.</span><span class="sxs-lookup"><span data-stu-id="57745-124">When the system is ready again, choose the **Create New Company** button.</span></span>  
8.  <span data-ttu-id="57745-125">Määritä avautuvassa valintaikkunassa nimeksi *Oma yritys* ja valitse **Tuotanto - Vain määritystiedot** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="57745-125">In the dialog that appears, specify the name as *My Company*, and choose the **Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="57745-126">Myös tämä toiminto kestää useita minuutteja.</span><span class="sxs-lookup"><span data-stu-id="57745-126">This again takes a number of minutes.</span></span> <span data-ttu-id="57745-127">Kun prosessi on valmis, voi käyttää Invoicingia Office 365 Business Premiumin osana.</span><span class="sxs-lookup"><span data-stu-id="57745-127">When the process completes, you will be able to access Invoicing as part of your Office 365 Business Premium experience.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="57745-128">Mitä tiedoille tapahtuu?</span><span class="sxs-lookup"><span data-stu-id="57745-128">What about my data?</span></span>
<span data-ttu-id="57745-129">Kun nimeät alkuperäisen oman yrityksen uudelleen, tietokantataulukot, joihin aiemmin luodut [!INCLUDE[d365fin](includes/d365fin_md.md)]:n tiedot on tallennettu, nimetään uudelleen mutta itse tietoihin ei kosketa.</span><span class="sxs-lookup"><span data-stu-id="57745-129">When you rename the original My Company, the database tables that store your existing [!INCLUDE[d365fin](includes/d365fin_md.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="57745-130">Jos käytät sekä Invoicingia että [!INCLUDE[d365fin](includes/d365fin_md.md)]:tä, tiedot tallennetaan kahteen eri säilöön (kahteen yritykseen).</span><span class="sxs-lookup"><span data-stu-id="57745-130">If you use both Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="57745-131">Mitään ei jaeta, joten kummankin yrityksen asiakkaita ja nimikkeitä on hallittava erikseen.</span><span class="sxs-lookup"><span data-stu-id="57745-131">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="57745-132">Katso myös</span><span class="sxs-lookup"><span data-stu-id="57745-132">See Also</span></span>
[<span data-ttu-id="57745-133">Usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="57745-133">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="57745-134">Hallinta</span><span class="sxs-lookup"><span data-stu-id="57745-134">Administration</span></span>](admin-setup-and-administration.md)  
