---
title: Pinon toiminnon visuaalisien signaalien mukauttaminen | Microsoft Docs
description: Määritä värillinen mittari pinoruudussa mukautettuna pinon toiminnon visuaalisena signaalina.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 04/01/2019
ms.author: solsen
redirect_url: admin-how-set-up-colored-indicator-on-cues
ms.openlocfilehash: f79f1a65ee17d8ca46a8ecf1cd9d49c5246bef63
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248109"
---
# <a name="set-up-a-colored-indicator-on-cues"></a><span data-ttu-id="17e50-103">Pinojen värillisen ilmaisimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="17e50-103">Set Up a Colored Indicator on Cues</span></span>
<span data-ttu-id="17e50-104">Voit määrittää pinot, jotka näkyvät roolikeskuksessa, kun haluat sisällyttää ilmaisimen, joka vaihtaa väriä pinojen arvojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="17e50-104">You can set up Cues that appear on the Role Center to include an indicator that changes color based on the data values in the Cues.</span></span>

<span data-ttu-id="17e50-105">Ilmaisin näkyy värillisenä palkkina pinon ruudun yläreunassa.</span><span class="sxs-lookup"><span data-stu-id="17e50-105">The indicator appears as a colored bar along the top border of the Cue tile.</span></span> <span data-ttu-id="17e50-106">Se antaa visuaalisen signaalin pinon toiminnan tilasta, joka voi ilmaista suotuisia tai epäsuotuisia olosuhteita ja kehottaa käyttäjää toimimaan.</span><span class="sxs-lookup"><span data-stu-id="17e50-106">It provides a visual signal of the status of the Cue's activity, which can indicate favorable or unfavorable conditions to prompt the user to take action.</span></span> <span data-ttu-id="17e50-107">Esimerkiksi, jos pino näyttää myyntilaskujen jatkuvan, voit määrittää ilmaisimen näkymään vihreänä (hyvä), kun jatkuva myyntilaskujen määrä on alle 10, ja se muuttuu punaiseksi (epäsuotuisa) kun summa on yli 20.</span><span class="sxs-lookup"><span data-stu-id="17e50-107">For example, if a Cue displays ongoing sales invoices, you can set up the indicator to appear green (favorable) when total number of ongoing sales invoices is below 10, and appears red (unfavorable) when the total is greater than 20.</span></span>

<span data-ttu-id="17e50-108">**Pinon asetukset** -sivulla voi määrittää ilmaisimet kaikille pinoille, jotka ovat saatavilla yhtiön tietokannassa.</span><span class="sxs-lookup"><span data-stu-id="17e50-108">From the **Cue Setup** page, you set up indicators for all the Cues that are available in the company database.</span></span>

<span data-ttu-id="17e50-109">Jotta voit määrittää ilmaisimen, sinun on määritettävä korkeintaan kaksi raja-arvoa, jotka määrittävät kolme arvoaluetta (matala, keskisuuri ja korkea), joihin voit käyttää eri värejä (tai tyyliä).</span><span class="sxs-lookup"><span data-stu-id="17e50-109">To set up the indicator, you specify up to two threshold values that define three ranges of data values (low, middle, and high) to which you can apply a different color (or style).</span></span>

## <a name="to-set-up-colored-indicators-on-cues"></a><span data-ttu-id="17e50-110">Värillisten ilmaisinten määrittäminen pinoissa</span><span class="sxs-lookup"><span data-stu-id="17e50-110">To set up colored indicators on Cues</span></span>
1. <span data-ttu-id="17e50-111">Valitse **Toimenpiteet**-kohdan roolikeskuksessa **Määritä pinot**.</span><span class="sxs-lookup"><span data-stu-id="17e50-111">Under **Activities** on your Role Center, choose **Set Up Cues**.</span></span>  
   <span data-ttu-id="17e50-112">**Pinon asetukset** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="17e50-112">The **Cue Setup** page appears.</span></span> <span data-ttu-id="17e50-113">Sivulla on lueteltu ilmaisimet, jotka on tällä hetkellä asetettu pinoissa.</span><span class="sxs-lookup"><span data-stu-id="17e50-113">The page lists the indicators that are currently setup up on Cues.</span></span>
2. <span data-ttu-id="17e50-114">Voit muokata ilmaisinta muokkaamalla kenttiä ja muokkaamalla esimerkiksi eri rajojen arvoja.</span><span class="sxs-lookup"><span data-stu-id="17e50-114">To modify an indicator, edit the fields and modify, for example, the values for the different thresholds.</span></span>  

<span data-ttu-id="17e50-115">Seuraava taulukko sisältää värit, jotka vastaavat **Matalan alueen tyyli**-, **Keskialueen tyyli**- ja **Korkean alueen tyyli** -kenttää.</span><span class="sxs-lookup"><span data-stu-id="17e50-115">The following table lists the colors that correspond to the options of the **Low Range Style**, **Middle Range Style**, and **High Range Style** fields.</span></span>

| <span data-ttu-id="17e50-116">Asetus</span><span class="sxs-lookup"><span data-stu-id="17e50-116">Option</span></span> | <span data-ttu-id="17e50-117">Väri</span><span class="sxs-lookup"><span data-stu-id="17e50-117">Color</span></span> |
| --- | --- |
| <span data-ttu-id="17e50-118">**Ei mitään**</span><span class="sxs-lookup"><span data-stu-id="17e50-118">**None**</span></span> |<span data-ttu-id="17e50-119">Ei väriä (sama väri kuin pinon ruutu)</span><span class="sxs-lookup"><span data-stu-id="17e50-119">No color (same color as the Cue tile)</span></span>|
| <span data-ttu-id="17e50-120">**Suotuisa**</span><span class="sxs-lookup"><span data-stu-id="17e50-120">**Favorable**</span></span> |<span data-ttu-id="17e50-121">Vihreä</span><span class="sxs-lookup"><span data-stu-id="17e50-121">Green</span></span> |
| <span data-ttu-id="17e50-122">**Epäsuotuisa**</span><span class="sxs-lookup"><span data-stu-id="17e50-122">**Unfavorable**</span></span> |<span data-ttu-id="17e50-123">Punainen</span><span class="sxs-lookup"><span data-stu-id="17e50-123">Red</span></span> |
| <span data-ttu-id="17e50-124">**Epäselvä**</span><span class="sxs-lookup"><span data-stu-id="17e50-124">**Ambiguous**</span></span> |<span data-ttu-id="17e50-125">Keltainen</span><span class="sxs-lookup"><span data-stu-id="17e50-125">Yellow</span></span> |
| <span data-ttu-id="17e50-126">**Alataso**</span><span class="sxs-lookup"><span data-stu-id="17e50-126">**Subordinate**</span></span> |<span data-ttu-id="17e50-127">Harmaa</span><span class="sxs-lookup"><span data-stu-id="17e50-127">Gray</span></span> |

## <a name="see-also"></a><span data-ttu-id="17e50-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="17e50-128">See Also</span></span>
<span data-ttu-id="17e50-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="17e50-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
