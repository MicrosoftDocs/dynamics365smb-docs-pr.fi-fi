---
title: Viivästyskuluehtojen määrittäminen
description: Lue, miten voit määrittää Business Centralin niin, että voit ilmoittaa asiakkaille lisäkuluista lähettämällä viivästyskululaskuja.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge
ms.date: 12/03/2020
ms.author: edupont
ms.openlocfilehash: aba5ca8eb9425c11c7f8a55a08a153ee18821632
ms.sourcegitcommit: 06bfb3aa59de50d983175e68e681b9d206423242
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/04/2020
ms.locfileid: "4671982"
---
# <a name="set-up-finance-charge-terms"></a><span data-ttu-id="99fab-103">Viivästyskuluehtojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="99fab-103">Set Up Finance Charge Terms</span></span>

<span data-ttu-id="99fab-104">Jos asiakas ei suorita maksua eräpäivään mennessä, voit antaa ohjelman laskea viivästyskulut automaattisesti ja lisätä ne asiakkaan tilin erääntyneisiin summiin.</span><span class="sxs-lookup"><span data-stu-id="99fab-104">When a customer does not pay by the due date, you can have finance charges calculated automatically and add them to the overdue amounts on the customer's account.</span></span> <span data-ttu-id="99fab-105">Voi antaa asiakkaille tiedon lisätyistä kuluista lähettämällä viivästyskululaskuja.</span><span class="sxs-lookup"><span data-stu-id="99fab-105">You can inform customers of the added charges by sending finance charge memos.</span></span> <span data-ttu-id="99fab-106">Ensin jokaista viivästyskulun laskentaa kuvaamaan täytyy määrittää koodi.</span><span class="sxs-lookup"><span data-stu-id="99fab-106">But first, you must set up a code that represents each finance charge calculation.</span></span> <span data-ttu-id="99fab-107">Sitten tämä koodi voidaan syöttää asiakaskortin Viivästyskuluehtojen koodi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="99fab-107">Then you can enter this code in the Fin. Charge Terms Code field on customer cards.</span></span>  

## <a name="finance-charge-terms"></a><span data-ttu-id="99fab-108">Viivästyskuluehdot</span><span class="sxs-lookup"><span data-stu-id="99fab-108">Finance charge terms</span></span>

<span data-ttu-id="99fab-109">Kullekin viivästyskululaskelmalle on määritettävä viivästyskuluehdot ja määritettävä ehdot asiakkaalle **Asiakas**-sivun **Viivästyskuluehtojen koodi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="99fab-109">You must set up finance charge terms for each finance charge calculation, and then assign the terms to the customer in the **Fin. Charge Terms Code** field on the **Customer** page.</span></span>

<span data-ttu-id="99fab-110">Viivästyskulut voidaan laskea käyttämällä joko keskimääräinen päiväsaldo- tai erääntyvä saldo -menetelmää.</span><span class="sxs-lookup"><span data-stu-id="99fab-110">Finance charges can be calculated using either the average daily balance or the balance due methods.</span></span>

* <span data-ttu-id="99fab-111">Keskimääräinen päiväsaldo</span><span class="sxs-lookup"><span data-stu-id="99fab-111">Average daily balance</span></span>  
  
  <span data-ttu-id="99fab-112">Maksun erääntymispäivien määrä otetaan huomioon:</span><span class="sxs-lookup"><span data-stu-id="99fab-112">The number of days the payment is overdue is taken into account:</span></span>  
  <span data-ttu-id="99fab-113">*Keskimääräinen päiväsaldo -menetelmä* - *viivästyskulu* = *erääntynyt summa* x *(päiviä erääntynyt / korkojakso)* x *(korkoprosentti/100)*</span><span class="sxs-lookup"><span data-stu-id="99fab-113">*Average Daily Balance method* - *Finance Charge* = *Overdue Amount* x *(Days Overdue / Interest Period)* x *(Interest Rate/100)*</span></span>

* <span data-ttu-id="99fab-114">Erääntyvä saldo</span><span class="sxs-lookup"><span data-stu-id="99fab-114">Balance due</span></span>  
  
  <span data-ttu-id="99fab-115">Viivästyskulu on prosenttiosuus erääntyneestä summasta:</span><span class="sxs-lookup"><span data-stu-id="99fab-115">The finance charge is a percentage of the overdue amount:</span></span>  
  <span data-ttu-id="99fab-116">*Erääntyvä saldo -menetelmä* - *viivästyskulu* = *erääntynyt summa* x *(korkoprosentti / 100)*</span><span class="sxs-lookup"><span data-stu-id="99fab-116">*Balance Due method* - *Finance Charge* = *Overdue Amount* x *(Interest Rate / 100)*</span></span>

<span data-ttu-id="99fab-117">Lisäksi jokainen Viivästyskuluehdot-taulukon ehto on linkitetty alitaulukkoon, Viivästyskuluteksti-taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="99fab-117">Additionally, each term in the Finance Charge Terms table is linked to a subtable, the Finance Charge Text table.</span></span> <span data-ttu-id="99fab-118">Jokaiselle viivästyskuluehtojen sarjalle voidaan määrittää alku- ja/tai lopputekstiä, joka sisällytetään viivästyskululaskuun.</span><span class="sxs-lookup"><span data-stu-id="99fab-118">For each set of finance charge terms, you can define a beginning and/or an ending text to include on the finance charge memo.</span></span>

### <a name="to-set-up-finance-charge-terms"></a><span data-ttu-id="99fab-119">Viivästyskuluehtojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="99fab-119">To set up finance charge terms</span></span>

1. <span data-ttu-id="99fab-120">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Viivästyskuluehdot** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="99fab-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2. <span data-ttu-id="99fab-121">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="99fab-121">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="99fab-122">Voit käyttää useita viivästyskuluehtoyhdistelmä, kun määrität kullekin koodin.</span><span class="sxs-lookup"><span data-stu-id="99fab-122">To use more than one combination of finance charge terms, set up a code for each one.</span></span>

    <span data-ttu-id="99fab-123">Voit määrittää kullekin viivästyskuluehdolle yksittäisiä ehtoja, joihin voi sisältyä lisämaksuja sekä paikallisena valuuttana että ulkomaan valuuttana.</span><span class="sxs-lookup"><span data-stu-id="99fab-123">For each finance charge term, you can specify individual conditions that can include additional fees in both LCY and in foreign currency.</span></span> <span data-ttu-id="99fab-124">Kullekin **Viivästyskuluehdot**-sivun ehdolle voi määrittää lisämaksuja ulkomaan valuuttana.</span><span class="sxs-lookup"><span data-stu-id="99fab-124">You can define additional fees in foreign currencies for each term on the **Finance Charge Terms** page.</span></span>
4. <span data-ttu-id="99fab-125">Valitse **Valuutat**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="99fab-125">Choose the **Currencies** action.</span></span>
5. <span data-ttu-id="99fab-126">Määritä **Lisäkuluehtojen valuutat** -sivulla kullekin ehdolle valuutan koodi ja lisämaksu.</span><span class="sxs-lookup"><span data-stu-id="99fab-126">On the **Currencies for Fin. Chrg. Terms** page, define for each term a currency code and an additional fee.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="99fab-127">Kun luot viivästyskuluja ulkomaan valuuttana, tässä määritettäviä ulkomaan valuutan ehtoja käytetään viivästyskululaskujen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="99fab-127">When you create finance charges in a foreign currency, the foreign currency conditions that you set up here will be used to create finance charge memos.</span></span> <span data-ttu-id="99fab-128">Jos ulkomaan valuuttojen viivästyskuluehtoja ei ole määritetty, käytetään **Viivästyskuluehdot**-sivulla määritettyjä PVA:n viivästyskuluehtoja ja ne muunnetaan liittyvään valuuttaan.</span><span class="sxs-lookup"><span data-stu-id="99fab-128">If there are no foreign currency finance charge conditions set up, the LCY finance charge conditions specified on the **Finance Charge Terms** page will be used and then converted to the relevant currency.</span></span>

    <span data-ttu-id="99fab-129">Voit määrittää jokaiselle viivästyskuluehdolle tekstiä, joka tulostetaan ennen viivästyskululaskun tapahtumia (**Aloitusteksti**) tai tapahtumien jälkeen (**Lopputeksti**).</span><span class="sxs-lookup"><span data-stu-id="99fab-129">For each finance charge term, you can specify text that will be printed before (**Beginning Text**) or after (**Ending Text**) on the entries on the finance charge memo.</span></span>  
6. <span data-ttu-id="99fab-130">Valitse tilanteen mukaan joko **Aloitusteksti**- tai **Lopetusteksti**-toiminto ja täytä **Viivästyskuluteksti**-sivun tiedot.</span><span class="sxs-lookup"><span data-stu-id="99fab-130">Choose the **Beginning Text** or **Ending Text** actions respectively, and fill on the **Finance Charge Text** page.</span></span>
7. <span data-ttu-id="99fab-131">Voit lisätä liittyviä arvoja automaattisesti viivästyskulutekstiin käyttämällä seuraavia paikkamerkkejä **Teksti**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="99fab-131">To automatically insert related values in the resulting finance charge text, enter the following placeholders in the **Text** field.</span></span>

|<span data-ttu-id="99fab-132">Paikkamerkki</span><span class="sxs-lookup"><span data-stu-id="99fab-132">Placeholder</span></span>|<span data-ttu-id="99fab-133">Arvo</span><span class="sxs-lookup"><span data-stu-id="99fab-133">Value</span></span>|  
|-----------------|-----------|  
|<span data-ttu-id="99fab-134">%1</span><span class="sxs-lookup"><span data-stu-id="99fab-134">%1</span></span>|<span data-ttu-id="99fab-135">Viivästyskululaskun otsikon **Asiakirjan pvm** -kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="99fab-135">Content of the **Document Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="99fab-136">%2</span><span class="sxs-lookup"><span data-stu-id="99fab-136">%2</span></span>|<span data-ttu-id="99fab-137">Viivästyskululaskun otsikon **Eräpäivä**-kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="99fab-137">Content of the **Due Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="99fab-138">%3</span><span class="sxs-lookup"><span data-stu-id="99fab-138">%3</span></span>|<span data-ttu-id="99fab-139">Viivästyskuluehtojen **Korko**-kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="99fab-139">Content of the **Interest Rate** field on the related finance charge terms</span></span>|  
|<span data-ttu-id="99fab-140">%4</span><span class="sxs-lookup"><span data-stu-id="99fab-140">%4</span></span>|<span data-ttu-id="99fab-141">Viivästyskululaskun otsikon **Jäljellä oleva summa** -kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="99fab-141">Content of the **Remaining Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="99fab-142">%5</span><span class="sxs-lookup"><span data-stu-id="99fab-142">%5</span></span>|<span data-ttu-id="99fab-143">Viivästyskululaskun otsikon **Korkosumma**-kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="99fab-143">Content of the **Interest Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="99fab-144">%6</span><span class="sxs-lookup"><span data-stu-id="99fab-144">%6</span></span>|<span data-ttu-id="99fab-145">Viivästyskululaskun otsikon **Lisämaksu**-kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="99fab-145">Content of the **Additional Fee** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="99fab-146">%7</span><span class="sxs-lookup"><span data-stu-id="99fab-146">%7</span></span>|<span data-ttu-id="99fab-147">Muistutuksen kokonaissumma</span><span class="sxs-lookup"><span data-stu-id="99fab-147">The total amount of the reminder</span></span>|  
|<span data-ttu-id="99fab-148">%8</span><span class="sxs-lookup"><span data-stu-id="99fab-148">%8</span></span>|<span data-ttu-id="99fab-149">Viivästyskululaskun otsikon **Valuutan koodi** -kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="99fab-149">Content of the **Currency Code** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="99fab-150">%9</span><span class="sxs-lookup"><span data-stu-id="99fab-150">%9</span></span>|<span data-ttu-id="99fab-151">Viivästyskululaskun otsikon **Kirjauspvm**-kentän sisältö</span><span class="sxs-lookup"><span data-stu-id="99fab-151">Content of the **Posting Date** field on the finance charge memo header</span></span>|  

## <a name="see-also"></a><span data-ttu-id="99fab-152">Katso myös .</span><span class="sxs-lookup"><span data-stu-id="99fab-152">See also</span></span>

[<span data-ttu-id="99fab-153">Avointen saldojen perintä</span><span class="sxs-lookup"><span data-stu-id="99fab-153">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="99fab-154">Muistutusehtojen ja -tasojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="99fab-154">Set Up Reminder Terms and Levels</span></span>](finance-setup-reminders.md)  
[<span data-ttu-id="99fab-155">Rahoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="99fab-155">Setting Up Finance</span></span>](finance-setup-finance.md)  