---
title: Useiden korkoprosenttien määrittäminen
description: Voit laskea viivästyskulut useilla korkoprosenteilla tietylle jaksolle. Koron laskeminen on samanlaista kaikille viivästyskuluille. Ainoa ero on tietyn jakson korkoprosentti.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3311747fb6bf6482b708948c3a99c9baf91557f8
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239670"
---
# <a name="set-up-multiple-interest-rates"></a><span data-ttu-id="5c6bc-104">Useiden korkoprosenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5c6bc-104">Set Up Multiple Interest Rates</span></span>
<span data-ttu-id="5c6bc-105">Useita korkoprosentteja käytetään kauppatapahtumien viivästyneissä maksuissa eri jaksoilla.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-105">Multiple interest rates are used for different periods for delayed payments in trade transactions.</span></span> <span data-ttu-id="5c6bc-106">Esimerkiksi valtio määrittää asiakkaalta perittävän enimmäiskoron.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-106">For example, a government specifies the maximum interest to be levied for a consumer.</span></span> <span data-ttu-id="5c6bc-107">Tätä korkoprosenttia voidaan muuttaa kahdesti vuoden aikana. Ajankohdat ovat 1.1. ja 1.7.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-107">This interest rate can be changed twice a year on 01 January and 01 July.</span></span> <span data-ttu-id="5c6bc-108">Yritysten välinen (B2B) korkoprosentti sovitaan osapuolten kesken. Tämän asiakasryhmän korkoprosentille ei ole määritetty enimmäistasoa.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-108">The interest rate between businesses (B2B) is agreed by the parties and there is no limit to that customer group.</span></span> <span data-ttu-id="5c6bc-109">Ilmoitettu korkoprosentti on yleensä neljä prosenttia enemmän kuin pankin normaali korko.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-109">The announced rate is usually four percent more than the normal bank interest.</span></span>

<span data-ttu-id="5c6bc-110">Kun luot viivästyskuluehdot ja muistutusehdot viivästysmaksulle, voit määrittää useita korkoprosentteja. Viivästysmaksu siis lasketaan eri kausille eri korkoprosentin mukaan.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-110">When you create finance charge terms and reminder terms, for delayed payment penalty, you can specify multiple interest rates so that the penalty fee is calculated from different interest rates in different periods.</span></span> <span data-ttu-id="5c6bc-111">Lisätietoja on kohdassa [Avointen saldojen perintä](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="5c6bc-111">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>

## <a name="to-set-up-multiple-interest-rates"></a><span data-ttu-id="5c6bc-112">Useiden korkoprosenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5c6bc-112">To set up multiple interest rates</span></span>  
1.  <span data-ttu-id="5c6bc-113">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Viivästyskuluehdot** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5c6bc-114">Valitse **Viivästyskuluehdot**-sivulla pakollinen rahoitusehto ja valitse sitten **Korkoprosentit**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-114">On the **Finance Charge Terms** page, select the required finance term, and then choose the **Interest Rates** action.</span></span>  
3.  <span data-ttu-id="5c6bc-115">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="5c6bc-116">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-116">Choose the **OK** button.</span></span>  
5.  <span data-ttu-id="5c6bc-117">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutusehdot** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="5c6bc-118">Valitse **Muistutusehdot**-sivulla pakollinen muistutusehto ja valitse sitten **Tasot**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-118">On the **Reminder Terms** page, select the required reminder term, and then choose the **Levels** action.</span></span>  
7.  <span data-ttu-id="5c6bc-119">Valitse **Muistutustasot**-sivulla **Laske korko** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-119">On the **Reminder Levels** page, select the **Calculate Interest** field.</span></span>  

<span data-ttu-id="5c6bc-120">Kun viivästyskululasku lähetetään, laskussa näkyvät viivästyskulut ja eri korkoprosentit tietyille ajanjaksoille.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-120">When you issue a finance charge memo, the memo shows the finance charges with multiple interest rates for a specific time period.</span></span> <span data-ttu-id="5c6bc-121">Lasku sisältää myös asiakkaan ja laskun lähettäneen yrityksen yhteystiedot, lisäsumman ja kokonaissumman.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-121">The memo also contains the contact details of the customer, the company issuing the memo, the additional amount, and the total amount.</span></span> <span data-ttu-id="5c6bc-122">Laskun alkutapahtuma näkyy lihavoituna.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-122">The opening entry on the memo is displayed in bold.</span></span> <span data-ttu-id="5c6bc-123">Viivästyskulut lasketaan useilla korkoprosenteilla tietylle ajanjaksolle. Ne tulostetaan laskuun alkutapahtuman jälkeen.</span><span class="sxs-lookup"><span data-stu-id="5c6bc-123">The finance charges are calculated with multiple interest rates for a specific time period and are printed after the opening entry of the memo.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5c6bc-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5c6bc-124">See Also</span></span>  
[<span data-ttu-id="5c6bc-125">Avointen saldojen perintä</span><span class="sxs-lookup"><span data-stu-id="5c6bc-125">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="5c6bc-126">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5c6bc-126">Setting Up Finance</span></span>](finance-setup-finance.md)
