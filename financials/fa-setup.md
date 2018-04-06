---
title: "Käyttöomaisuuden määrittäminen| Microsoft Docs"
description: "Lue käyttöomaisuuden, kuten koneiden tai rakennusten määrittämiseen tarvittavasta tehtäväsarjasta."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6ca21ece631fdd07cb95ffdaaa350506b4a8c9e1
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="ee32a-103">Käyttöomaisuuden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ee32a-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="ee32a-104">Ennen käyttöomaisuuserien käsittelyä on määritettäviä muutamia toimintoja:</span><span class="sxs-lookup"><span data-stu-id="ee32a-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="ee32a-105">käyttöomaisuuden vakuuttaminen, kunnossapito ja poistaminen</span><span class="sxs-lookup"><span data-stu-id="ee32a-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="ee32a-106">kustannusten ja muiden arvojen kirjaaminen pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="ee32a-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="ee32a-107">Seuraavassa taulukossa on linkkejä lisätietoihin.</span><span class="sxs-lookup"><span data-stu-id="ee32a-107">The table below has links to more information.</span></span> <span data-ttu-id="ee32a-108">Kun olet määrittänyt nämä toiminnot, voit aloittaa erilaisten aktiviteettien käytön.</span><span class="sxs-lookup"><span data-stu-id="ee32a-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="ee32a-109">Lisätietoja on kohdassa [Käyttöomaisuus](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="ee32a-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="ee32a-110">Voit tallentaa käyttöomaisuustapahtumat **Käyttöomaisuuden KP-päiväkirja**- tai **Käyttöomaisuuspäiväkirja**-ikkunaan sen mukaan, koskevatko tapahtumat talousraportointia vai sisäistä hallintaa.</span><span class="sxs-lookup"><span data-stu-id="ee32a-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="ee32a-111">Käyttöomaisuuden ohje sisältää tietoja vain **Käyttöomaisuuden KP-päiväkirja** -ikkunan käyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="ee32a-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="ee32a-112">Kun otat käyttöomaisuusaktiviteetin käyttöön **Poistokirjakortti**-ikkunan **KP-integrointi**-osassa, **Käyttöomaisuuden KP-päiväkirja** -ikkunaa käytetään kyseisen aktiviteetin tapahtumien kirjaamisessa.</span><span class="sxs-lookup"><span data-stu-id="ee32a-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

<span data-ttu-id="ee32a-113">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="ee32a-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="ee32a-114">Toiminta</span><span class="sxs-lookup"><span data-stu-id="ee32a-114">To</span></span> | <span data-ttu-id="ee32a-115">Katso</span><span class="sxs-lookup"><span data-stu-id="ee32a-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="ee32a-116">Määritä oletusarvoiset KP-tilit, kohdistusavaimet, päiväkirjamallit ja -erät käyttöomaisuuden kirjaamista varten. Määritä myös käyttöomaisuuden luokat ja alaluokat, kuten Aineellinen ja Aineeton.</span><span class="sxs-lookup"><span data-stu-id="ee32a-116">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="ee32a-117">Käyttöomaisuuden yleisten tietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ee32a-117">Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="ee32a-118">Luo poistokirjat, määritä eri poistotavat, integroi pääkirjanpidon kanssa ja ota käyttöön tapahtumien monistaminen useissa poistokirjoissa.</span><span class="sxs-lookup"><span data-stu-id="ee32a-118">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="ee32a-119">Käyttöomaisuuden poiston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ee32a-119">Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="ee32a-120">Voit ottaa käyttöön käyttöomaisuuden vakuutuksen määrittämällä vakuutuksen tiedot ja sopimuskohtaisen vakuutuskortin sekä valmistelemalla päiväkirjat vakuutuskustannusten kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="ee32a-120">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="ee32a-121">Käyttöomaisuuserän määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ee32a-121">Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="ee32a-122">Voit ottaa käyttöomaisuuden kunnossapidon määrittämällä yleiset kunnossapitotiedot, kunnossapidon kirjaustilit ja kunnossapitotyön tyypit.</span><span class="sxs-lookup"><span data-stu-id="ee32a-122">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="ee32a-123">Käyttöomaisuuden huollon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ee32a-123">Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="ee32a-124">Lisätietoja käyttöomaisuuden erilaisista poistotavoista.</span><span class="sxs-lookup"><span data-stu-id="ee32a-124">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="ee32a-125">Poistotavat</span><span class="sxs-lookup"><span data-stu-id="ee32a-125">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="ee32a-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ee32a-126">See Also</span></span>
[<span data-ttu-id="ee32a-127">Käyttöomaisuus</span><span class="sxs-lookup"><span data-stu-id="ee32a-127">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="ee32a-128">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="ee32a-128">Finance</span></span>](finance.md)  
<span data-ttu-id="ee32a-129">[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)</span><span class="sxs-lookup"><span data-stu-id="ee32a-129">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="ee32a-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ee32a-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

