---
title: Tietokannan käyttötarkoituksen hallinta Business Centralissa | Microsoft Docs
description: Tietokannan käyttötarkoituksen muuttaminen raportteja, API-sivuja ja kyselyjä varten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/30/2020
ms.author: jswymer
ms.openlocfilehash: b46786b60d7c5799b056c49188785bd595db57ff
ms.sourcegitcommit: 866f0e6ed9df3397072b9df838e31c3a1f4b626d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2020
ms.locfileid: "3333906"
---
# <a name="managing-database-access-intent"></a><span data-ttu-id="3006d-103">Tietokannan käyttötarkoituksen hallinta</span><span class="sxs-lookup"><span data-stu-id="3006d-103">Managing Database Access Intent</span></span> 

<span data-ttu-id="3006d-104">Superkäyttäjä ja järjestelmänvalvoja voivat muuttaa tietokannan käyttötarkoitusta raporteissa, API-tyyppisillä sivuilla ja kyselyissä. Näin parannetaan palvelun suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="3006d-104">As a super user or administrator, you can change the database access intent on reports, pages of the type API, and queries to improve performance of the service.</span></span>

## <a name="overview"></a><span data-ttu-id="3006d-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="3006d-105">Overview</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="3006d-106">voidaan määrittää käyttämään ensisijaisen (vain luku) tietokannan vain luku -replikoita.</span><span class="sxs-lookup"><span data-stu-id="3006d-106">can be set up to use read-only replicas of the primary (read-write) database.</span></span> <span data-ttu-id="3006d-107">Tietokannan replikan käyttäminen vähentää ensisijaisen tietokannan työkuormaa.</span><span class="sxs-lookup"><span data-stu-id="3006d-107">Using the database replica reduces the load on the primary database.</span></span> <span data-ttu-id="3006d-108">Joissakin tapauksissa se parantaa myös tietojen tarkastelemisen suorituskykyä asiakasohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="3006d-108">In some cases, it will also improve the performance when viewing data in the client.</span></span> <span data-ttu-id="3006d-109">Replikat ovat hyödyllisiä objekteille, kuten raporteille, kyselyille ja API-sivuille, joita käytetään vain tietojen tarkastelemiseen tietojen muokkaamisen sijaan.</span><span class="sxs-lookup"><span data-stu-id="3006d-109">Replicas are beneficial for objects, like reports, queries, and API pages, that are used for viewing data only, not modifying data.</span></span>

<span data-ttu-id="3006d-110">Kun objektit suoritetaan, tietokannan käyttötarkoitus määrittää, käytetäänkö vain luku -replikaa (jos se on käytettävissä) vai ensisijaista tietokantaa.</span><span class="sxs-lookup"><span data-stu-id="3006d-110">When objects run, the database access intent determines whether to use a read-only replica, if one is available, or the primary database.</span></span> <span data-ttu-id="3006d-111">Raportit, API-sivut ja kyselyt kehitetään ennalta määritetyn tietokannan käyttötarkoituksen kanssa (katso [DatabaseAccessIntent-ominaisuus](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span><span class="sxs-lookup"><span data-stu-id="3006d-111">Reports, API pages, and queries are developed with a predefined database access intent (see [DatabaseAccessIntent property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span></span>

<span data-ttu-id="3006d-112">**Tietokannan käyttötarkoitusluettelo** -sivulla voit ohittaa objektien ennalta määritetyn tietokannan käyttötarkoituksen objektien suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="3006d-112">The **Database Access Intent List** page lets you override the predefined database access intent for objects when they're run.</span></span>

<span data-ttu-id="3006d-113">Tietokannan termeissä tätä ominaisuutta kutsutaan yleisesti *lukemisen skaalaamiseksi*. Lisätietoja lukemisen skaalaamisesta ja tietokannan käyttötarkoituksesta [!INCLUDE[prodshort](includes/prodshort.md)]:ssä on kohdassa [Lukemisen skaalautumisen käyttäminen paremman suorituskyvyn saavuttamiseksi](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) [!INCLUDE[prodshort](includes/prodshort.md)]:n kehittäjän ja hallinnon ohjeessa.</span><span class="sxs-lookup"><span data-stu-id="3006d-113">In database terms, this feature is commonly known as *read scale-out*. For more information about read-scale out and data access intent in [!INCLUDE[prodshort](includes/prodshort.md)], see [Utilizing Read Scale-Out for Better Performance](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in the [!INCLUDE[prodshort](includes/prodshort.md)] Developer and Administration help.</span></span>

## <a name="to-change-the-database-access-intent"></a><span data-ttu-id="3006d-114">Tietokannan käyttötarkoituksen muuttaminen</span><span class="sxs-lookup"><span data-stu-id="3006d-114">To change the database access intent</span></span>

1. <span data-ttu-id="3006d-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tietokannan käyttötarkoitusluettelo** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3006d-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Database Access Intent List**, and then choose the related link.</span></span>

    <span data-ttu-id="3006d-116">Sivulla on luettelo kaikista raporteista, sivuista ja kyselyistä.</span><span class="sxs-lookup"><span data-stu-id="3006d-116">The page lists all reports, pages, and queries.</span></span> <span data-ttu-id="3006d-117">**Käyttötarkoitus**-sarakkeessa on jokin seuraavista arvoista:</span><span class="sxs-lookup"><span data-stu-id="3006d-117">The **Access Intent** column includes one of the following values:</span></span>

    |<span data-ttu-id="3006d-118">**Asetus**</span><span class="sxs-lookup"><span data-stu-id="3006d-118">**Setting**</span></span>|<span data-ttu-id="3006d-119">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="3006d-119">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="3006d-120">**Oletus**</span><span class="sxs-lookup"><span data-stu-id="3006d-120">**Default**</span></span>|<span data-ttu-id="3006d-121">Osoittaa, että objekti käyttää ennalta määritettyä tietokannan käyttötarkoitusta.</span><span class="sxs-lookup"><span data-stu-id="3006d-121">Indicates that the object uses the predefined database access intent.</span></span>|
    |<span data-ttu-id="3006d-122">**Salli kirjoitus**</span><span class="sxs-lookup"><span data-stu-id="3006d-122">**Allow Write**</span></span>|<span data-ttu-id="3006d-123">Asettaa objektin käyttämään ensisijaista tietokantaa, jolloin käyttäjä voi muokata tietoja.</span><span class="sxs-lookup"><span data-stu-id="3006d-123">Sets the object to use the primary database, allowing the user to modify data.</span></span>|
    |<span data-ttu-id="3006d-124">**Vain luku**</span><span class="sxs-lookup"><span data-stu-id="3006d-124">**Read Only**</span></span>|<span data-ttu-id="3006d-125">Asettaa objektin käyttämään tietokannan replikaa. Tämä tarkoittaa sitä, että käyttäjä voi vain katsella tietoja, ei muuttaa niitä.</span><span class="sxs-lookup"><span data-stu-id="3006d-125">Sets the object to use the database replica, which means that the user can only view data, not change data.</span></span>|

2. <span data-ttu-id="3006d-126">Valitse **Muokkaa luetteloa** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="3006d-126">Choose the **Edit List** action.</span></span>

3. <span data-ttu-id="3006d-127">Muuta **Muokkaa - Tietokannan käyttötarkoitusluettelo** -sivulla **Käyttötarkoitus**-kenttää objekteille.</span><span class="sxs-lookup"><span data-stu-id="3006d-127">On the **Edit - Database Access Intent List** page, change the **Access Intent** field for the objects.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3006d-128">Jos muokattavan objektin, kuten asiakaskortin, tilaksi määritetään **Vain luku**, käytetään yhä ensisijaista tietokantaa käyttötarkoituksesta huolimatta. Näin käyttäjät voivat tehdä muutoksia normaaliin tapaan.</span><span class="sxs-lookup"><span data-stu-id="3006d-128">If an object that is editable, like the Customer Card, is set to **Read Only**, the primary database will still be used, regardless of the access intent, allowing users to make changes as normal.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="3006d-129">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="3006d-129">See Related Training at [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="3006d-130">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3006d-130">See Also</span></span>
[<span data-ttu-id="3006d-131">Liiketoiminnan toiminnallisuus</span><span class="sxs-lookup"><span data-stu-id="3006d-131">Business Functionality</span></span>](across-business-functionality.md)  
[<span data-ttu-id="3006d-132">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="3006d-132">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="3006d-133">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3006d-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="3006d-134">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="3006d-134">Getting Started</span></span>](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
