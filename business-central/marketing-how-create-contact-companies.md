---
title: Kontaktiyritysten luominen| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten luodaan kontakti kullekin sellaiselle uudelle yritykselle tai mahdolliselle yritykselle, joiden kanssa olet vuorovaikutuksessa tai joihin sinulla on liikesuhde.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: ff585f1a96d509ef317aaaf3671bc91ca46a430a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "796412"
---
# <a name="create-contacts"></a><span data-ttu-id="74aea-103">Kontaktien luominen</span><span class="sxs-lookup"><span data-stu-id="74aea-103">Create Contacts</span></span>
<span data-ttu-id="74aea-104">Voit luoda kontaktin jokaiselle uudelle yritykselle (esimerkiksi asiakkaalle, toimittajalle, mahdolliselle asiakkaalle, pankille, lakiasiantoimistolle ja konsultille), jonka kanssa yrityksesi on vuorovaikutuksessa.</span><span class="sxs-lookup"><span data-stu-id="74aea-104">You can create a contact for each new company you interact with, for example, a customer, vendor, prospective customer, bank, law firm, consultant, and so on.</span></span>

<span data-ttu-id="74aea-105">Kontaktin voi luoda joko alusta alkaen tai aiemmin luodusta asiakkaasta, toimittajasta tai pankkitilistä.</span><span class="sxs-lookup"><span data-stu-id="74aea-105">There are two ways to create a contact: from scratch or from an existing customer, vendor, or bank account.</span></span>

## <a name="create-a-company-contact-from-scratch"></a><span data-ttu-id="74aea-106">Yrityksen kontaktin luominen alusta alkaen</span><span class="sxs-lookup"><span data-stu-id="74aea-106">Create a company contact from scratch</span></span>
1. <span data-ttu-id="74aea-107">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Kontaktit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="74aea-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="74aea-108">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="74aea-108">Choose the **New** action.</span></span>
3. <span data-ttu-id="74aea-109">Syötä **Nro**-kenttään kontaktin numero.</span><span class="sxs-lookup"><span data-stu-id="74aea-109">In the **No. field**, enter a number for the contact.</span></span>

    <span data-ttu-id="74aea-110">Jos olet määrittänyt kontakteille numerosarjan **Kontaktienhallinnan asetukset**-sivulla, voit myös painaa Enter-näppäintä, jolloin ohjelma syöttää seuraavan saatavilla olevan kontaktinumeron.</span><span class="sxs-lookup"><span data-stu-id="74aea-110">Alternatively, if you have set up a number series for contacts on the **Marketing Setup** page, you can press the Enter key to select the next available contact number.</span></span>  
4. <span data-ttu-id="74aea-111">Määritä **yrityksen** **tyyppi**.</span><span class="sxs-lookup"><span data-stu-id="74aea-111">Set **Type** to **Company**.</span></span>
5. <span data-ttu-id="74aea-112">Täytä tarvittaessa muut kentät.</span><span class="sxs-lookup"><span data-stu-id="74aea-112">Fill in the other fields as required.</span></span>

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a><span data-ttu-id="74aea-113">Yrityksen kontaktin luominen asiakkaasta, toimittajasta tai pankkitilistä</span><span class="sxs-lookup"><span data-stu-id="74aea-113">To create a company contact from a customer, vendor, or bank account</span></span>
<span data-ttu-id="74aea-114">Jos olet jo määrittänyt useita asiakkaita, toimittajia ja pankkitilejä ohjelmassa, voit luoda kontakteja olemassa olevien tietojen pohjalta.</span><span class="sxs-lookup"><span data-stu-id="74aea-114">If you have already set up a number of customers, vendors, and bank accounts, you can create contacts on the basis of the existing data.</span></span> <span data-ttu-id="74aea-115">Kun luot kontaktin tällä tavalla, kontaktin tiedot synkronoidaan asiakkaan, toimittajan tai pankkitilin tietojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="74aea-115">When you create a contact this way, the contact information is synchronized with the customer, vendor, or bank account information.</span></span>

> [!NOTE]  
>   <span data-ttu-id="74aea-116">Ennen kuin voit luoda kontaktiyrityksiä tällä tavalla, asiakkaiden, toimittajien ja pankkitilien liikesuhteen koodi on määritettävä **Kontaktienhallinnan asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="74aea-116">Before you can create contact companies this way, you must specify a business relation code for customers, vendors, and bank accounts on the **Marketing Setup** page.</span></span> <span data-ttu-id="74aea-117">Jos luot kontakteja pankkitileistä, määritä myös pankkitilien numerosarjat **Pääkirjanpidon asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="74aea-117">If you will be creating contacts from a bank accounts, you must also specify numbers series for bank accounts on the **General Ledger Setup** page.</span></span>

1. <span data-ttu-id="74aea-118">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä jokin seuraavista sen perusteella, missä haluat luoda kontakteja, ja valitse liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="74aea-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter one of the following, depending on from where you want to create contacts, and then choose the related link.</span></span>
   * <span data-ttu-id="74aea-119">**Luo kontakteja asiakkaista**</span><span class="sxs-lookup"><span data-stu-id="74aea-119">**Create Contacts from Customers**</span></span>
   * <span data-ttu-id="74aea-120">**Luo kontakteja toimittajista**</span><span class="sxs-lookup"><span data-stu-id="74aea-120">**Create Contacts from Vendors**</span></span>
   * <span data-ttu-id="74aea-121">**Luo kontakteja pankkitileistä**</span><span class="sxs-lookup"><span data-stu-id="74aea-121">**Create Contacts from Bank Accounts**</span></span>
2. <span data-ttu-id="74aea-122">Valitse avautuvalla erätyön sivulla **Asiakas**-, **Toimittaja**- tai **Pankkitili**-osa ja määritä suodattimet, jos haluat luoda kontakteja tietyistä asiakkaista, toimittajista tai pankkitileistä.</span><span class="sxs-lookup"><span data-stu-id="74aea-122">In the batch job page that opens, in the **Customer**, **Vendor**, or **Bank Account** section, set filters if you want to create contacts from specific customers, vendors, or bank accounts.</span></span>
3. <span data-ttu-id="74aea-123">Aloita yhteystietojen luominen valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="74aea-123">Choose the **OK** button to start creating contacts.</span></span>

    <span data-ttu-id="74aea-124">Ohjelma liittää uusiin kontakteihin seuraavat kontaktinumerot numerosarjasta.</span><span class="sxs-lookup"><span data-stu-id="74aea-124">The next contact numbers in the number series are assigned to the new contacts.</span></span> <span data-ttu-id="74aea-125">Uusiin kontakteihin liitetään **Kontaktienhallinnan asetukset** -sivulla määritettyjen toimittajien suhde.</span><span class="sxs-lookup"><span data-stu-id="74aea-125">The business relation for vendors that is specified on the **Marketing Setup** page is assigned to the newly created contacts.</span></span>

> [!TIP]  
>   <span data-ttu-id="74aea-126">Voit luoda kontaktista myös asiakkaan, toimittajan tai pankkitilin.</span><span class="sxs-lookup"><span data-stu-id="74aea-126">You can also create a customer, vendor, or bank account from a contact.</span></span> <span data-ttu-id="74aea-127">Lisätietoja on kohdassa [Asiakkaan, toimittajan tai pankkitilin luominen kontaktista](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="74aea-127">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="74aea-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="74aea-128">See Also</span></span>
[<span data-ttu-id="74aea-129">Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa</span><span class="sxs-lookup"><span data-stu-id="74aea-129">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="74aea-130">Liikesuhteiden liittäminen kontaktiin</span><span class="sxs-lookup"><span data-stu-id="74aea-130">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="74aea-131">Toimialaryhmien liittäminen kontaktiin</span><span class="sxs-lookup"><span data-stu-id="74aea-131">Assign Industry Groups to a Contact</span></span>](marketing-industry-groups.md#AssignIndustryGroupContact)  
[<span data-ttu-id="74aea-132">Postitusryhmien liittäminen kontaktiin</span><span class="sxs-lookup"><span data-stu-id="74aea-132">Assign Mailing Groups to a Contact</span></span>](marketing-mailing-groups.md#AssignMailGroupContact)  
[<span data-ttu-id="74aea-133">Kontaktihenkilöiden luominen</span><span class="sxs-lookup"><span data-stu-id="74aea-133">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="74aea-134">Business Central -sovelluksen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="74aea-134">Working with Business Central</span></span>](ui-work-product.md)
