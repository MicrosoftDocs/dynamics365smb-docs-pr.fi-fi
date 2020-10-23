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
ms.openlocfilehash: 424d497154e9fc8023ba38cbd22859c0874124ec
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926020"
---
# <a name="set-up-document-sending-profiles"></a><span data-ttu-id="fbe2a-103">Asiakirjan lähetysprofiilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fbe2a-103">Set Up Document Sending Profiles</span></span>
<span data-ttu-id="fbe2a-104">Voit määrittää jokaiselle asiakkaalle haluamasi myyntiasiakirjojen lähettämistavan. Näin sinun tarvitse valita lähettämistapaa aina, kun valitset **Kirjaa ja lähetä** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="fbe2a-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="fbe2a-105">**Asiakirjan lähetysprofiilit** -sivulla voi määrittää eri lähetysprofiileja, joista voit valita asiakkaan kortin **Asiakirjan lähetysprofiili** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="fbe2a-105">On the **Document Sending Profiles** page, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="fbe2a-106">Valitse **Oletus**-valintaruutu, kun haluat, että asiakirjan lähetysprofiili on kaikkien asiakkaiden oletusprofiili lukuun ottamatta niitä asiakkaita, joiden **Asiakirjan lähetysprofiili** -kenttään on valittu toinen lähetysprofiili.</span><span class="sxs-lookup"><span data-stu-id="fbe2a-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="fbe2a-107">Kun valitset **Kirjaa ja lähetä** -toiminnon myyntiasiakirjassa, näkyviin tulee **Kirjaa ja lähetä vahvistus** -valintaikkuna, jossa näkyy käytetty lähetysprofiili (joka asiakkaalle määritetty profiili tai kaikille asiakkaille yhteinen oletusprofiili).</span><span class="sxs-lookup"><span data-stu-id="fbe2a-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="fbe2a-108">Valintaikkunassa voit muuttaa myyntiasiakirjan lähetysprofiilia.</span><span class="sxs-lookup"><span data-stu-id="fbe2a-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="fbe2a-109">Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="fbe2a-109">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHH?rel=0]

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="fbe2a-110">Asiakirjan lähetysprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fbe2a-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="fbe2a-111">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakirjojen lähetysprofiilit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="fbe2a-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="fbe2a-112">Valitse **Asiakirjan lähetysprofiilit** -sivulla **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="fbe2a-112">On the **Document Sending Profiles** page, choose the **New** action.</span></span>
3. <span data-ttu-id="fbe2a-113">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="fbe2a-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="fbe2a-114">Lähetysprofiilin määrittäminen asiakaskortilla</span><span class="sxs-lookup"><span data-stu-id="fbe2a-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="fbe2a-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="fbe2a-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="fbe2a-116">Avaa sen asiakkaan kortti, jolle haluat määrittää lähetysprofiilin.</span><span class="sxs-lookup"><span data-stu-id="fbe2a-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="fbe2a-117">Valitse **Asiakirjan lähetyksen profiili** -kentässä profiili, jonka olet määrittänyt edellisessä vaiheessa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="fbe2a-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="fbe2a-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="fbe2a-118">See Also</span></span>
[<span data-ttu-id="fbe2a-119">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fbe2a-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="fbe2a-120">Myynti</span><span class="sxs-lookup"><span data-stu-id="fbe2a-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="fbe2a-121">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fbe2a-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
