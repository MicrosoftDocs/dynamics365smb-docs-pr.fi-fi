---
title: Käyttöomaisuuden määrittäminen| Microsoft Docs
description: Lue käyttöomaisuuden, kuten koneiden tai rakennusten määrittämiseen tarvittavasta tehtäväsarjasta.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3044d878260dbab4e9d2423398b7654386671638
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380075"
---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="45905-103">Käyttöomaisuuden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="45905-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="45905-104">Ennen käyttöomaisuuserien käsittelyä on määritettäviä muutamia toimintoja:</span><span class="sxs-lookup"><span data-stu-id="45905-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="45905-105">käyttöomaisuuden vakuuttaminen, kunnossapito ja poistaminen</span><span class="sxs-lookup"><span data-stu-id="45905-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="45905-106">kustannusten ja muiden arvojen kirjaaminen pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="45905-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="45905-107">Seuraavassa taulukossa on linkkejä lisätietoihin.</span><span class="sxs-lookup"><span data-stu-id="45905-107">The table below has links to more information.</span></span> <span data-ttu-id="45905-108">Kun olet määrittänyt nämä toiminnot, voit aloittaa erilaisten aktiviteettien käytön.</span><span class="sxs-lookup"><span data-stu-id="45905-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="45905-109">Lisätietoja on kohdassa [Käyttöomaisuus](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="45905-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="45905-110">Voit tallentaa käyttöomaisuustapahtumat **Käyttöomaisuuden KP-päiväkirja**- tai **Käyttöomaisuuspäiväkirja**-sivulla sen mukaan, koskevatko tapahtumat talousraportointia vai sisäistä hallintaa.</span><span class="sxs-lookup"><span data-stu-id="45905-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** pages, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="45905-111">Käyttöomaisuuden ohje sisältää tietoja vain **Käyttöomaisuuden KP-päiväkirja** -sivun käyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="45905-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** page.</span></span>  

<span data-ttu-id="45905-112">Kun otat käyttöomaisuusaktiviteetin käyttöön **Poistokirjakortti**-sivun **KP-integrointi**-osassa, **Käyttöomaisuuden KP-päiväkirja** -sivua käytetään kyseisen aktiviteetin tapahtumien kirjaamisessa.</span><span class="sxs-lookup"><span data-stu-id="45905-112">When you enable a fixed asset activity in the **G/L Integration** section on the **Depreciation Book Card** page, the **Fixed Asset G/L Journal** page is used to post transactions for the activity.</span></span>

<span data-ttu-id="45905-113">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="45905-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="45905-114">Toiminta</span><span class="sxs-lookup"><span data-stu-id="45905-114">To</span></span> | <span data-ttu-id="45905-115">Katso</span><span class="sxs-lookup"><span data-stu-id="45905-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="45905-116">Määritä oletusarvoiset KP-tilit, kohdistusavaimet, päiväkirjamallit ja -erät käyttöomaisuuden kirjaamista varten. Määritä myös käyttöomaisuuden luokat ja alaluokat, kuten Aineellinen ja Aineeton.</span><span class="sxs-lookup"><span data-stu-id="45905-116">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="45905-117">Käyttöomaisuuden yleisten tietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="45905-117">Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="45905-118">Luo poistokirjat, määritä eri poistotavat, integroi pääkirjanpidon kanssa ja ota käyttöön tapahtumien monistaminen useissa poistokirjoissa.</span><span class="sxs-lookup"><span data-stu-id="45905-118">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="45905-119">Käyttöomaisuuden poiston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="45905-119">Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="45905-120">Voit ottaa käyttöön käyttöomaisuuden vakuutuksen määrittämällä vakuutuksen tiedot ja sopimuskohtaisen vakuutuskortin sekä valmistelemalla päiväkirjat vakuutuskustannusten kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="45905-120">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="45905-121">Käyttöomaisuuserän määrittäminen</span><span class="sxs-lookup"><span data-stu-id="45905-121">Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="45905-122">Voit ottaa käyttöomaisuuden kunnossapidon määrittämällä yleiset kunnossapitotiedot, kunnossapidon kirjaustilit ja kunnossapitotyön tyypit.</span><span class="sxs-lookup"><span data-stu-id="45905-122">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="45905-123">Käyttöomaisuuden huollon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="45905-123">Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="45905-124">Lisätietoja käyttöomaisuuden erilaisista poistotavoista.</span><span class="sxs-lookup"><span data-stu-id="45905-124">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="45905-125">Poistotavat</span><span class="sxs-lookup"><span data-stu-id="45905-125">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="45905-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="45905-126">See Also</span></span>
[<span data-ttu-id="45905-127">Käyttöomaisuus</span><span class="sxs-lookup"><span data-stu-id="45905-127">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="45905-128">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="45905-128">Finance</span></span>](finance.md)  
[<span data-ttu-id="45905-129">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="45905-129">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="45905-130">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="45905-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]