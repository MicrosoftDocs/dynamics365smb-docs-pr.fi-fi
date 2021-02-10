---
title: Myyntiasiakirjojen ensisijaisten lähetystapojen määrittäminen | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten kunkin asiakkaan ensisijainen myyntiasiakirjojen lähetystapa määritetään. Lähetystavaksi voidaan valita esimerkiksi sähköposti, PDF tai sähköinen asiakirja.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1ec87cbf0885b392dc92bbd9a25fca81db38c5a1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758140"
---
# <a name="set-up-document-sending-profiles"></a><span data-ttu-id="11a62-103">Asiakirjan lähetysprofiilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="11a62-103">Set Up Document Sending Profiles</span></span>
<span data-ttu-id="11a62-104">Voit määrittää jokaiselle asiakkaalle haluamasi myyntiasiakirjojen lähettämistavan. Näin sinun tarvitse valita lähettämistapaa aina, kun valitset **Kirjaa ja lähetä** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="11a62-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="11a62-105">**Asiakirjan lähetysprofiilit** -sivulla voi määrittää eri lähetysprofiileja, joista voit valita asiakkaan kortin **Asiakirjan lähetysprofiili** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="11a62-105">On the **Document Sending Profiles** page, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="11a62-106">Valitse **Oletus**-valintaruutu, kun haluat, että asiakirjan lähetysprofiili on kaikkien asiakkaiden oletusprofiili lukuun ottamatta niitä asiakkaita, joiden **Asiakirjan lähetysprofiili** -kenttään on valittu toinen lähetysprofiili.</span><span class="sxs-lookup"><span data-stu-id="11a62-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="11a62-107">Kun valitset **Kirjaa ja lähetä** -toiminnon myyntiasiakirjassa, näkyviin tulee **Kirjaa ja lähetä vahvistus** -valintaikkuna, jossa näkyy käytetty lähetysprofiili (joka asiakkaalle määritetty profiili tai kaikille asiakkaille yhteinen oletusprofiili).</span><span class="sxs-lookup"><span data-stu-id="11a62-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="11a62-108">Valintaikkunassa voit muuttaa myyntiasiakirjan lähetysprofiilia.</span><span class="sxs-lookup"><span data-stu-id="11a62-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="11a62-109">Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="11a62-109">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHH?rel=0]

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="11a62-110">Asiakirjan lähetysprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="11a62-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="11a62-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakirjojen lähetysprofiilit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="11a62-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="11a62-112">Valitse **Asiakirjan lähetysprofiilit** -sivulla **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="11a62-112">On the **Document Sending Profiles** page, choose the **New** action.</span></span>
3. <span data-ttu-id="11a62-113">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="11a62-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="11a62-114">Lähetysprofiilin määrittäminen asiakaskortilla</span><span class="sxs-lookup"><span data-stu-id="11a62-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="11a62-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="11a62-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="11a62-116">Avaa sen asiakkaan kortti, jolle haluat määrittää lähetysprofiilin.</span><span class="sxs-lookup"><span data-stu-id="11a62-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="11a62-117">Valitse **Asiakirjan lähetyksen profiili** -kentässä profiili, jonka olet määrittänyt edellisessä vaiheessa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="11a62-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="11a62-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="11a62-118">See Also</span></span>
[<span data-ttu-id="11a62-119">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="11a62-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="11a62-120">Myynti</span><span class="sxs-lookup"><span data-stu-id="11a62-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="11a62-121">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="11a62-121">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
