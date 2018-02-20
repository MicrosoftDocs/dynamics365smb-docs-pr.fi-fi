---
title: Kontaktiyritysten luominen| Microsoft Docs
description: "Tässä ohjeaiheessa kerrotaan, miten luodaan kontakti kullekin sellaiselle uudelle yritykselle tai mahdolliselle yritykselle, joiden kanssa olet vuorovaikutuksessa tai joihin sinulla on liikesuhde."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ed0f75f1e0ee8a282b58458e4fed3b4eef7c46fb
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="create-contact-companies"></a><span data-ttu-id="fe97d-103">Kontaktiyritysten luominen:</span><span class="sxs-lookup"><span data-stu-id="fe97d-103">Create Contact Companies</span></span>
<span data-ttu-id="fe97d-104">Voit luoda kontaktin jokaiselle uudelle yritykselle (esimerkiksi asiakkaalle, toimittajalle, mahdolliselle asiakkaalle, pankille, lakiasiantoimistolle ja konsultille), jonka kanssa yrityksesi on vuorovaikutuksessa.</span><span class="sxs-lookup"><span data-stu-id="fe97d-104">You can create a contact for each new company you interact with, for example, a customer, vendor, prospective customer, bank, law firm, consultant, and so on.</span></span>

<span data-ttu-id="fe97d-105">Kontaktin voi luoda joko alusta alkaen tai aiemmin luodusta asiakkaasta, toimittajasta tai pankkitilistä.</span><span class="sxs-lookup"><span data-stu-id="fe97d-105">There are two ways to create a contact: from scratch or from an existing customer, vendor, or bank account.</span></span>

<span data-ttu-id="fe97d-106">Ennen uuden kontaktin luomista kannattaa ehkä tarkistaa asetukset **Kontaktienhallinnan asetukset** -ikkunasta.</span><span class="sxs-lookup"><span data-stu-id="fe97d-106">Before creating a contact, you may want to check the settings in the **Marketing Setup** window.</span></span> <span data-ttu-id="fe97d-107">Lisätietoja on kohdassa [Kontaktien hallinnan määrittäminen](marketing-setup-marketing.md).</span><span class="sxs-lookup"><span data-stu-id="fe97d-107">For more information, see [Setting Up Relationship Management](marketing-setup-marketing.md).</span></span>

## <a name="create-a-company-contact-from-scratch"></a><span data-ttu-id="fe97d-108">Yrityksen kontaktin luominen alusta alkaen</span><span class="sxs-lookup"><span data-stu-id="fe97d-108">Create a company contact from scratch</span></span>
1. <span data-ttu-id="fe97d-109">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kontaktit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="fe97d-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="fe97d-110">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="fe97d-110">Choose the **New** action.</span></span>
3. <span data-ttu-id="fe97d-111">Syötä **Nro**-kenttään kontaktin numero.</span><span class="sxs-lookup"><span data-stu-id="fe97d-111">In the **No. field**, enter a number for the contact.</span></span>

    <span data-ttu-id="fe97d-112">Jos olet määrittänyt kontakteille numerosarjan **Kontaktienhallinnan asetukset**-ikkunassa, voit myös painaa Enter-näppäintä, jolloin ohjelma syöttää seuraavan saatavilla olevan kontaktinumeron.</span><span class="sxs-lookup"><span data-stu-id="fe97d-112">Alternatively, if you have set up a number series for contacts in the **Marketing Setup** window, you can press the Enter key to select the next available contact number.</span></span>  
4. <span data-ttu-id="fe97d-113">Määritä **yrityksen** **tyyppi**.</span><span class="sxs-lookup"><span data-stu-id="fe97d-113">Set **Type** to **Company**.</span></span>
5. <span data-ttu-id="fe97d-114">Täytä tarvittaessa muut kentät.</span><span class="sxs-lookup"><span data-stu-id="fe97d-114">Fill in the other fields as required.</span></span>

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a><span data-ttu-id="fe97d-115">Yrityksen kontaktin luominen asiakkaasta, toimittajasta tai pankkitilistä</span><span class="sxs-lookup"><span data-stu-id="fe97d-115">To create a company contact from a customer, vendor, or bank account</span></span>
<span data-ttu-id="fe97d-116">Jos olet jo määrittänyt useita asiakkaita, toimittajia ja pankkitilejä ohjelmassa, voit luoda kontakteja olemassa olevien tietojen pohjalta.</span><span class="sxs-lookup"><span data-stu-id="fe97d-116">If you have already set up a number of customers, vendors, and bank accounts, you can create contacts on the basis of the existing data.</span></span> <span data-ttu-id="fe97d-117">Kun luot kontaktin tällä tavalla, kontaktin tiedot synkronoidaan asiakkaan, toimittajan tai pankkitilin tietojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="fe97d-117">When you create a contact this way, the contact information is synchronized with the customer, vendor, or bank account information.</span></span>

> [!NOTE]  
>   <span data-ttu-id="fe97d-118">Ennen kuin voit luoda kontaktiyrityksiä tällä tavalla, asiakkaiden, toimittajien ja pankkitilien liikesuhteen koodi on määritettävä **Kontaktienhallinnan asetukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="fe97d-118">Before you can create contact companies this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="fe97d-119">Jos luot kontakteja pankkitileistä, määritä myös pankkitilien numerosarjat **Pääkirjanpidon asetukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="fe97d-119">If you will be creating contacts from a bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

1. <span data-ttu-id="fe97d-120">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake ja kirjoita jokin seuraavista sen mukaan, mistä haluat luoda kontakteja. Valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="fe97d-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter one of the following, depending on from where you want to create contacts, and then choose the related link.</span></span>
   * <span data-ttu-id="fe97d-121">**Luo kontakteja asiakkaista**</span><span class="sxs-lookup"><span data-stu-id="fe97d-121">**Create Contacts from Customers**</span></span>
   * <span data-ttu-id="fe97d-122">**Luo kontakteja toimittajista**</span><span class="sxs-lookup"><span data-stu-id="fe97d-122">**Create Contacts from Vendors**</span></span>
   * <span data-ttu-id="fe97d-123">**Luo kontakteja pankkitileistä**</span><span class="sxs-lookup"><span data-stu-id="fe97d-123">**Create Contacts from Bank Accounts**</span></span>
2. <span data-ttu-id="fe97d-124">Valitse avautuvassa erätyön ikkunassa **Asiakas**-, **Toimittaja**- tai **Pankkitili**-osa ja määritä suodattimet, jos haluat luoda kontakteja tietyistä asiakkaista, toimittajista tai pankkitileistä.</span><span class="sxs-lookup"><span data-stu-id="fe97d-124">In the batch job window that opens, in the **Customer**, **Vendor**, or **Bank Account** section, set filters if you want to create contacts from specific customers, vendors, or bank accounts.</span></span>
3. <span data-ttu-id="fe97d-125">Aloita yhteystietojen luominen valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe97d-125">Choose the **OK** button to start creating contacts.</span></span>

    <span data-ttu-id="fe97d-126">Ohjelma liittää uusiin kontakteihin seuraavat kontaktinumerot numerosarjasta.</span><span class="sxs-lookup"><span data-stu-id="fe97d-126">The next contact numbers in the number series are assigned to the new contacts.</span></span> <span data-ttu-id="fe97d-127">Uusiin kontakteihin liitetään **Kontaktienhallinnan asetukset** -ikkunassa määritettyjen toimittajien suhde.</span><span class="sxs-lookup"><span data-stu-id="fe97d-127">The business relation for vendors that is specified in the **Marketing Setup** window is assigned to the newly created contacts.</span></span>

> [!TIP]  
>   <span data-ttu-id="fe97d-128">Voit luoda kontaktista myös asiakkaan, toimittajan tai pankkitilin.</span><span class="sxs-lookup"><span data-stu-id="fe97d-128">You can also create a customer, vendor, or bank account from a contact.</span></span> <span data-ttu-id="fe97d-129">Lisätietoja on kohdassa [Asiakkaan, toimittajan tai pankkitilin luominen kontaktista](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="fe97d-129">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="fe97d-130">Katso myös</span><span class="sxs-lookup"><span data-stu-id="fe97d-130">See Also</span></span>
[<span data-ttu-id="fe97d-131">Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa</span><span class="sxs-lookup"><span data-stu-id="fe97d-131">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="fe97d-132">Liikesuhteiden liittäminen kontaktiin</span><span class="sxs-lookup"><span data-stu-id="fe97d-132">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="fe97d-133">Toimialaryhmien liittäminen kontaktiin</span><span class="sxs-lookup"><span data-stu-id="fe97d-133">Assign Industry Groups to a Contact</span></span>](marketing-industry-groups.md#AssignIndustryGroupContact)  
[<span data-ttu-id="fe97d-134">Postitusryhmien liittäminen kontaktiin</span><span class="sxs-lookup"><span data-stu-id="fe97d-134">Assign Mailing Groups to a Contact</span></span>](marketing-mailing-groups.md#AssignMailGroupContact)  
[<span data-ttu-id="fe97d-135">Kontaktihenkilöiden luominen</span><span class="sxs-lookup"><span data-stu-id="fe97d-135">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="fe97d-136">Finance and Operations, Business editionin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="fe97d-136">Working with Finance and Operations, Business edition</span></span>](ui-work-product.md)

