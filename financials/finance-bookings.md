---
title: Varausten laskuttaminen Dynamics 365:ssa | Microsoft Docs
description: "Opi, miten voit tehdä massalaskutusta Microsoft Bookingsista Dynamics 365 for Financialsissa."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 06/14/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1f1a1645ba27a3b42d67c11f7472c283ca44dbd1
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365finmdmd"></a><span data-ttu-id="fb6c7-103">Microsoft Bookingsin massalaskutus [!INCLUDE[d365fin](includes/d365fin_md.md)]issa</span><span class="sxs-lookup"><span data-stu-id="fb6c7-103">Bulk Invoicing for Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
<span data-ttu-id="fb6c7-104">Voit tehdä tapaamisten massalaskutusta, jos yrityksesi käyttää Office 365:n Bookings-sovellusta.</span><span class="sxs-lookup"><span data-stu-id="fb6c7-104">If your company uses the Bookings app in Office 365, you can do bulk invoicing for appointments.</span></span> <span data-ttu-id="fb6c7-105">[!INCLUDE[d365fin](includes/d365fin_md.md)]in **Laskuttamattomat varaukset** -sivulla esitetään luettelo yrityksen valmiista varauksista.</span><span class="sxs-lookup"><span data-stu-id="fb6c7-105">The **Uninvoiced Bookings** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a list of the company's completed bookings.</span></span> <span data-ttu-id="fb6c7-106">Tällä sivulla voit valita nopeasti tapaamiset, jotka haluat laskuttaa ja joille haluat luoda luonnoslaskut tarjotuista palveluista.</span><span class="sxs-lookup"><span data-stu-id="fb6c7-106">In this page you can quickly select the appointments that you want to invoice and create draft invoices for the services provided.</span></span>  

## <a name="connect-to-bookings"></a><span data-ttu-id="fb6c7-107">Yhdistäminen Bookings-sovellukseen</span><span class="sxs-lookup"><span data-stu-id="fb6c7-107">Connect to Bookings</span></span>
<span data-ttu-id="fb6c7-108">Jos haluat yhdistää oman [!INCLUDE[d365fin](includes/d365fin_md.md)]in Bookingsiin, sinun on määritettävä Bookings-yritys, Bookingsiin synkronoitavat tiedot, synkronointiväli ja käytettävät mallit.</span><span class="sxs-lookup"><span data-stu-id="fb6c7-108">To connect your [!INCLUDE[d365fin](includes/d365fin_md.md)] with Bookings, you must specify your Bookings company, what to synchronize with Bookings, how often to synchronize, and which templates to use.</span></span> <span data-ttu-id="fb6c7-109">Voit määrittää nämä tiedot **Bookings-synkronoinnin asetukset** -sivulla, jonka voit avata **Exchangen synkronointiasetukset** -sivulta, jonka löydät [Hakutoiminnon](ui-search.md) avulla.</span><span class="sxs-lookup"><span data-stu-id="fb6c7-109">You set up this information in the **Booking Sync. Setup** page, which you can launch from the **Exchange Sync. Setup** page, which you can find through [Search](ui-search.md).</span></span>  

<span data-ttu-id="fb6c7-110">Jos esimerkiksi haluat synkronoida asiakkaat Bookingsin ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in välillä, sinun on määritettävä oletusmalli, jota käytetään uusien asiakkaiden lisäämiseen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin Bookings-yrityksesi asiakkaiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="fb6c7-110">For example, if you want to synchronize customers between Bookings and [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the default template to use to add new customers in [!INCLUDE[d365fin](includes/d365fin_md.md)] based on the customers in your Bookings company.</span></span>  

## <a name="invoice-appointments"></a><span data-ttu-id="fb6c7-111">Laskuta tapaamiset</span><span class="sxs-lookup"><span data-stu-id="fb6c7-111">Invoice Appointments</span></span>
<span data-ttu-id="fb6c7-112">Kun on aika lähettää laskut valmiista varauksista, voit siirtyä **Laskuttamattomat varaukset** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="fb6c7-112">When it is time to send invoices for the completed bookings, you go to the **Uninvoiced Bookings** page.</span></span> <span data-ttu-id="fb6c7-113">Luettelon pituus riippuu tietojen synkronointiaikataulusta.</span><span class="sxs-lookup"><span data-stu-id="fb6c7-113">Depending on how often the information is synchronized, the list is long or short.</span></span> <span data-ttu-id="fb6c7-114">Voit luoda laskut kaikille luettelon varauksille tai yhdelle varaukselle kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="fb6c7-114">You can create invoices for all bookings in the list or one booking at a time.</span></span> <span data-ttu-id="fb6c7-115">Voit valita luettelosta useita tapahtumia ja laskuttaa ainoastaan ne.</span><span class="sxs-lookup"><span data-stu-id="fb6c7-115">You can select one or more entries in the list and invoice those only.</span></span>  

<span data-ttu-id="fb6c7-116">Bookings-tapaamisten laskuttamisen tuki on yksinkertaisempi kuin myyntitarjousten, -tilausten ja -laskujen kanssa työskentelyn täysi työnkulku.</span><span class="sxs-lookup"><span data-stu-id="fb6c7-116">The support for invoicing appointments from Bookings is simpler than the fuller workflow of working with sales quotes, sales orders, and sales invoices.</span></span> <span data-ttu-id="fb6c7-117">Lisätietoja on kohdassa [Toimintaohje: Myynnin laskuttaminen](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="fb6c7-117">For more information, see [How to: Invoice Sales](sales-how-invoice-sales.md).</span></span> <span data-ttu-id="fb6c7-118">Voit myydä palveluitasi [!INCLUDE[d365fin](includes/d365fin_md.md)]in avulla tai käyttää Bookingsia, yrityksesi tarpeista riippuen.</span><span class="sxs-lookup"><span data-stu-id="fb6c7-118">You can choose to sell your services using [!INCLUDE[d365fin](includes/d365fin_md.md)] or choose to use Bookings, depending on your business needs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fb6c7-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="fb6c7-119">See Also</span></span>
[<span data-ttu-id="fb6c7-120">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="fb6c7-120">Finance</span></span>](finance.md)  
[<span data-ttu-id="fb6c7-121">Toimintaohje: Myynnin laskutus</span><span class="sxs-lookup"><span data-stu-id="fb6c7-121">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="fb6c7-122">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fb6c7-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="fb6c7-123">Microsoft Bookings</span><span class="sxs-lookup"><span data-stu-id="fb6c7-123">Microsoft Bookings</span></span>](https://products.office.com/en-us/business/scheduling-and-booking-app)  

