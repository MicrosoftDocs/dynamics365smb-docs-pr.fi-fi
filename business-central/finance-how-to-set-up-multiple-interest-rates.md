---
title: "Useiden korkoprosenttien määrittäminen"
description: "Voit laskea viivästyskulut useilla korkoprosenteilla tietylle jaksolle. Koron laskeminen on samanlaista kaikille viivästyskuluille. Ainoa ero on tietyn jakson korkoprosentti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0af01fe46f6b7df1149825c35a9fc0cc19482403
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-multiple-interest-rates"></a><span data-ttu-id="6347b-104">Useiden korkoprosenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6347b-104">Set Up Multiple Interest Rates</span></span>
<span data-ttu-id="6347b-105">Useita korkoprosentteja käytetään kauppatapahtumien viivästyneissä maksuissa eri jaksoilla.</span><span class="sxs-lookup"><span data-stu-id="6347b-105">Multiple interest rates are used for different periods for delayed payments in trade transactions.</span></span> <span data-ttu-id="6347b-106">Esimerkiksi valtio määrittää asiakkaalta perittävän enimmäiskoron.</span><span class="sxs-lookup"><span data-stu-id="6347b-106">For example, a government specifies the maximum interest to be levied for a consumer.</span></span> <span data-ttu-id="6347b-107">Tätä korkoprosenttia voidaan muuttaa kahdesti vuoden aikana. Ajankohdat ovat 1.1. ja 1.7.</span><span class="sxs-lookup"><span data-stu-id="6347b-107">This interest rate can be changed twice a year on 01 January and 01 July.</span></span> <span data-ttu-id="6347b-108">Yritysten välinen (B2B) korkoprosentti sovitaan osapuolten kesken. Tämän asiakasryhmän korkoprosentille ei ole määritetty enimmäistasoa.</span><span class="sxs-lookup"><span data-stu-id="6347b-108">The interest rate between businesses (B2B) is agreed by the parties and there is no limit to that customer group.</span></span> <span data-ttu-id="6347b-109">Ilmoitettu korkoprosentti on yleensä neljä prosenttia enemmän kuin pankin normaali korko.</span><span class="sxs-lookup"><span data-stu-id="6347b-109">The announced rate is usually four percent more than the normal bank interest.</span></span>

<span data-ttu-id="6347b-110">Kun luot viivästyskuluehdot ja muistutusehdot viivästysmaksulle, voit määrittää useita korkoprosentteja. Viivästysmaksu siis lasketaan eri kausille eri korkoprosentin mukaan.</span><span class="sxs-lookup"><span data-stu-id="6347b-110">When you create finance charge terms and reminder terms, for delayed payment penalty, you can specify multiple interest rates so that the penalty fee is calculated from different interest rates in different periods.</span></span> <span data-ttu-id="6347b-111">Lisätietoja on kohdassa [Avointen saldojen perintä](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="6347b-111">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>

## <a name="to-set-up-multiple-interest-rates"></a><span data-ttu-id="6347b-112">Useiden korkoprosenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6347b-112">To set up multiple interest rates</span></span>  
1.  <span data-ttu-id="6347b-113">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Viivästyskuluehdot** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="6347b-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6347b-114">Valitse **Viivästyskuluehdot**-ikkunassa pakollinen rahoitusehto ja valitse sitten **Korkoprosentit**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="6347b-114">In the **Finance Charge Terms** window, select the required finance term, and then choose the **Interest Rates** action.</span></span>  
3.  <span data-ttu-id="6347b-115">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="6347b-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="6347b-116">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="6347b-116">Choose the **OK** button.</span></span>  
5.  <span data-ttu-id="6347b-117">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Muistutusehdot** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="6347b-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="6347b-118">Valitse **Muistutusehdot**-ikkunassa pakollinen muistutusehto ja valitse sitten **Tasot**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="6347b-118">In the **Reminder Terms** window, select the required reminder term, and then choose the **Levels** action.</span></span>  
7.  <span data-ttu-id="6347b-119">Valitse **Muistutustasot**-ikkunassa **Laske korko** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="6347b-119">In the **Reminder Levels** window, select the **Calculate Interest** field.</span></span>  

<span data-ttu-id="6347b-120">Kun viivästyskululasku lähetetään, laskussa näkyvät viivästyskulut ja eri korkoprosentit tietyille ajanjaksoille.</span><span class="sxs-lookup"><span data-stu-id="6347b-120">When you issue a finance charge memo, the memo shows the finance charges with multiple interest rates for a specific time period.</span></span> <span data-ttu-id="6347b-121">Lasku sisältää myös asiakkaan ja laskun lähettäneen yrityksen yhteystiedot, lisäsumman ja kokonaissumman.</span><span class="sxs-lookup"><span data-stu-id="6347b-121">The memo also contains the contact details of the customer, the company issuing the memo, the additional amount, and the total amount.</span></span> <span data-ttu-id="6347b-122">Laskun alkutapahtuma näkyy lihavoituna.</span><span class="sxs-lookup"><span data-stu-id="6347b-122">The opening entry on the memo is displayed in bold.</span></span> <span data-ttu-id="6347b-123">Viivästyskulut lasketaan useilla korkoprosenteilla tietylle ajanjaksolle. Ne tulostetaan laskuun alkutapahtuman jälkeen.</span><span class="sxs-lookup"><span data-stu-id="6347b-123">The finance charges are calculated with multiple interest rates for a specific time period and are printed after the opening entry of the memo.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6347b-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6347b-124">See Also</span></span>  
[<span data-ttu-id="6347b-125">Avointen saldojen perintä</span><span class="sxs-lookup"><span data-stu-id="6347b-125">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="6347b-126">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6347b-126">Setting Up Finance</span></span>](finance-setup-finance.md)

