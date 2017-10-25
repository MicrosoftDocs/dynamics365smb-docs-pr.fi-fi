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
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9dea8be0f5b0200f97082dc25dbaa2483ad6c735
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="1c819-103">Käyttöomaisuuden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1c819-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="1c819-104">Ennen käyttöomaisuuserien käsittelyä on määritettäviä muutamia toimintoja:</span><span class="sxs-lookup"><span data-stu-id="1c819-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="1c819-105">käyttöomaisuuden vakuuttaminen, kunnossapito ja poistaminen</span><span class="sxs-lookup"><span data-stu-id="1c819-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="1c819-106">kustannusten ja muiden arvojen kirjaaminen pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="1c819-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="1c819-107">Seuraavassa taulukossa on linkkejä lisätietoihin.</span><span class="sxs-lookup"><span data-stu-id="1c819-107">The table below has links to more information.</span></span> <span data-ttu-id="1c819-108">Kun olet määrittänyt nämä toiminnot, voit aloittaa erilaisten aktiviteettien käytön.</span><span class="sxs-lookup"><span data-stu-id="1c819-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="1c819-109">Lisätietoja on kohdassa [Käyttöomaisuus](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="1c819-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="1c819-110">Voit tallentaa käyttöomaisuustapahtumat **Käyttöomaisuuden KP-päiväkirja**- tai **Käyttöomaisuuspäiväkirja**-ikkunaan sen mukaan, koskevatko tapahtumat talousraportointia vai sisäistä hallintaa.</span><span class="sxs-lookup"><span data-stu-id="1c819-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="1c819-111">Käyttöomaisuuden ohje sisältää tietoja vain **Käyttöomaisuuden KP-päiväkirja** -ikkunan käyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="1c819-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="1c819-112">Kun otat käyttöomaisuusaktiviteetin käyttöön **Poistokirjakortti**-ikkunan **KP-integrointi**-osassa, **Käyttöomaisuuden KP-päiväkirja** -ikkunaa käytetään kyseisen aktiviteetin tapahtumien kirjaamisessa.</span><span class="sxs-lookup"><span data-stu-id="1c819-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

> [!NOTE]  
>  <span data-ttu-id="1c819-113">Tämä toiminto edellyttää, että kokemukseksi on valittu **Suite**.</span><span class="sxs-lookup"><span data-stu-id="1c819-113">This functionality requires that the experience is set to **Suite**.</span></span> <span data-ttu-id="1c819-114">Lisätietoja on ohjeaiheessa [Financials-kokemuksen mukauttaminen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="1c819-114">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>  

<span data-ttu-id="1c819-115">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="1c819-115">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="1c819-116">Toiminta</span><span class="sxs-lookup"><span data-stu-id="1c819-116">To</span></span> | <span data-ttu-id="1c819-117">Katso</span><span class="sxs-lookup"><span data-stu-id="1c819-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="1c819-118">Määritä oletusarvoiset KP-tilit, kohdistusavaimet, päiväkirjamallit ja -erät käyttöomaisuuden kirjaamista varten. Määritä myös käyttöomaisuuden luokat ja alaluokat, kuten Aineellinen ja Aineeton.</span><span class="sxs-lookup"><span data-stu-id="1c819-118">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="1c819-119">Toimintaohje: Käyttöomaisuuden yleisten tietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1c819-119">How to: Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="1c819-120">Luo poistokirjat, määritä eri poistotavat, integroi pääkirjanpidon kanssa ja ota käyttöön tapahtumien monistaminen useissa poistokirjoissa.</span><span class="sxs-lookup"><span data-stu-id="1c819-120">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="1c819-121">Toimintaohje: Käyttöomaisuuden poiston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1c819-121">How to: Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="1c819-122">Voit ottaa käyttöön käyttöomaisuuden vakuutuksen määrittämällä vakuutuksen tiedot ja sopimuskohtaisen vakuutuskortin sekä valmistelemalla päiväkirjat vakuutuskustannusten kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="1c819-122">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="1c819-123">Toimintaohje: Käyttöomaisuuden vakuutuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1c819-123">How to: Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="1c819-124">Voit ottaa käyttöomaisuuden kunnossapidon määrittämällä yleiset kunnossapitotiedot, kunnossapidon kirjaustilit ja kunnossapitotyön tyypit.</span><span class="sxs-lookup"><span data-stu-id="1c819-124">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="1c819-125">Toimintaohje: Käyttöomaisuuden kunnossapidon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1c819-125">How to: Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="1c819-126">Lisätietoja käyttöomaisuuden erilaisista poistotavoista.</span><span class="sxs-lookup"><span data-stu-id="1c819-126">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="1c819-127">Poistotavat</span><span class="sxs-lookup"><span data-stu-id="1c819-127">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="1c819-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1c819-128">See Also</span></span>
[<span data-ttu-id="1c819-129">Käyttöomaisuus</span><span class="sxs-lookup"><span data-stu-id="1c819-129">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="1c819-130">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="1c819-130">Finance</span></span>](finance.md)  
<span data-ttu-id="1c819-131">[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)</span><span class="sxs-lookup"><span data-stu-id="1c819-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="1c819-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1c819-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

