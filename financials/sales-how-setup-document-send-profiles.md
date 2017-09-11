---
title: "Myyntiasiakirjojen ensisijaisten lähetystapojen määrittäminen | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten kunkin asiakkaan ensisijainen myyntiasiakirjojen lähetystapa määritetään. Lähetystavaksi voidaan valita esimerkiksi sähköposti, PDF tai sähköinen asiakirja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7f7499e6e501207ed5fd6ebbee5b94d18c1d008e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-document-sending-profiles"></a><span data-ttu-id="05007-103">Toimintaohje: Asiakirjan lähetysprofiilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="05007-103">How to: Set Up Document Sending Profiles</span></span>
<span data-ttu-id="05007-104">Voit määrittää jokaiselle asiakkaalle haluamasi myyntiasiakirjojen lähettämistavan. Näin sinun tarvitse valita lähettämistapaa aina, kun valitset **Kirjaa ja lähetä** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="05007-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="05007-105">**Asiakirjan lähetysprofiilit** -ikkunassa voit määrittää eri lähetysprofiileja, joista voit valita asiakkaan kortin **Asiakirjan lähetysprofiili** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="05007-105">In the **Document Sending Profiles** window, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="05007-106">Valitse **Oletus**-valintaruutu, kun haluat, että asiakirjan lähetysprofiili on kaikkien asiakkaiden oletusprofiili lukuun ottamatta niitä asiakkaita, joiden **Asiakirjan lähetysprofiili** -kenttään on valittu toinen lähetysprofiili.</span><span class="sxs-lookup"><span data-stu-id="05007-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="05007-107">Kun valitset **Kirjaa ja lähetä** -toiminnon myyntiasiakirjassa, näkyviin tulee **Kirjaa ja lähetä vahvistus** -valintaikkuna, jossa näkyy käytetty lähetysprofiili (joka asiakkaalle määritetty profiili tai kaikille asiakkaille yhteinen oletusprofiili).</span><span class="sxs-lookup"><span data-stu-id="05007-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="05007-108">Valintaikkunassa voit muuttaa myyntiasiakirjan lähetysprofiilia.</span><span class="sxs-lookup"><span data-stu-id="05007-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="05007-109">Lisätietoja on ohjeaiheessa [Toimintaohje: Myynnin laskuttaminen](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="05007-109">For more information, see [How to: Invoice Sales](sales-how-invoice-sales.md).</span></span>

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="05007-110">Asiakirjan lähetysprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="05007-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="05007-111">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakirjan lähetysprofiilit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="05007-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="05007-112">Valitse **Asiakirjan lähetysprofiilit** -ikkunassa **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="05007-112">In the **Document Sending Profiles** window, choose the **New** action.</span></span>
3. <span data-ttu-id="05007-113">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="05007-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="05007-114">Lähetysprofiilin määrittäminen asiakaskortilla</span><span class="sxs-lookup"><span data-stu-id="05007-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="05007-115">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakkaan tiliote** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="05007-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="05007-116">Avaa sen asiakkaan kortti, jolle haluat määrittää lähetysprofiilin.</span><span class="sxs-lookup"><span data-stu-id="05007-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="05007-117">Valitse **Asiakirjan lähetyksen profiili** -kentässä profiili, jonka olet määrittänyt edellisessä vaiheessa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="05007-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="05007-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="05007-118">See Also</span></span>
[<span data-ttu-id="05007-119">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="05007-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="05007-120">Myynti</span><span class="sxs-lookup"><span data-stu-id="05007-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="05007-121">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="05007-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

