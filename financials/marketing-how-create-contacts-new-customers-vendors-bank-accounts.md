---
title: Asiakkaan tai toimittajanluominen kontaktista| Microsoft Docs
description: "Voit tallentaa aiemmin luodun kontaktin asiakkaana, toimittajana tai pankkitilinä käyttämällä aiemmin luotuja tietoja ja määrittämällä liikesuhteen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 142c1649438ad31b604767d6b6f35a1caeb3f9e4
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-a-customer-vendor-or-bank-account-from-a-contact"></a><span data-ttu-id="82f43-103">Toimintaohje: Asiakkaan, toimittajan tai pankkitilin luominen kontaktista</span><span class="sxs-lookup"><span data-stu-id="82f43-103">How to: Create a Customer, Vendor, or Bank Account From a Contact</span></span>
<span data-ttu-id="82f43-104">Haluat ehkä tallentaa jotkin aiemmin luoduista kontakteistasi asiakkaina, toimittajina tai pankkitileinä.</span><span class="sxs-lookup"><span data-stu-id="82f43-104">You may want to record some of your existing contacts as customers, vendors, or bank accounts.</span></span> <span data-ttu-id="82f43-105">Kun asiakas, toimittaja tai pankkitili luodaan kontaktista, voit käyttää aiemmin luotuja tietoja.</span><span class="sxs-lookup"><span data-stu-id="82f43-105">Creating a customer, vendor, or bank account from a contact enables you use existing data.</span></span> <span data-ttu-id="82f43-106">Kun luot asiakkaan, toimittajan tai pankkitilin tällä tavalla, se synkronisoidaan kontaktin kanssa.</span><span class="sxs-lookup"><span data-stu-id="82f43-106">When you create a customer, vendor, or bank account this way, it is synchronized with the contact.</span></span> <span data-ttu-id="82f43-107">Synkronoimisen avulla kontaktien ja asiakkaiden, toimittajien tai pankkitilien yhteiset tiedot säilyvät samoina.</span><span class="sxs-lookup"><span data-stu-id="82f43-107">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>

<span data-ttu-id="82f43-108">Ennen kuin voit tallentaa kontakteja tällä tavalla, asiakkaiden, toimittajien ja pankkitilien liikesuhteen koodi on määritettävä **Kontaktienhallinnan asetukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="82f43-108">Before you can record contacts this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="82f43-109">Jos tallennat kontakteja pankkitileinä, määritä myös pankkitilien numerosarjat **Pääkirjanpidon asetukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="82f43-109">If you will be recording contacts as bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a><span data-ttu-id="82f43-110">Kontaktin luominen asiakkaana, toimittajana tai pankkitilinä.</span><span class="sxs-lookup"><span data-stu-id="82f43-110">To create a contact as a customer, vendor, or bank account</span></span>
1. <span data-ttu-id="82f43-111">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kontaktit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="82f43-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="82f43-112">Valitse kontakti, jonka haluat luoda asiakkaana, toimittajana tai pankkitilinä.</span><span class="sxs-lookup"><span data-stu-id="82f43-112">Select the contact you want to create as a customer, vendor, or bank account.</span></span>
3. <span data-ttu-id="82f43-113">Valitse **Luo**-toiminto ja valitse sitten **Asiakas**, **Toimittaja** tai **Pankki**.</span><span class="sxs-lookup"><span data-stu-id="82f43-113">Choose the **Create As** action, and then choose either **Customer**, **Vendor**, or **Bank**.</span></span>
4. <span data-ttu-id="82f43-114">Vahvista valintasi.</span><span class="sxs-lookup"><span data-stu-id="82f43-114">Confirm the subsequent message.</span></span>

<span data-ttu-id="82f43-115">Yhteystiedot siirretään **Kontakti**-kortilta **Pankkitili** -kortille, **Asiakas** -kortille tai **Toimittaja** -kortille.</span><span class="sxs-lookup"><span data-stu-id="82f43-115">The contact information is transferred from the **Contact** card to the **Bank Account** card, the **Customer** card, or the **Vendor** card.</span></span> <span data-ttu-id="82f43-116">Haluat ehkä lisätä tiettyjä tietoja jokaiseen korttiin, kuten laskutus- ja maksutiedot.</span><span class="sxs-lookup"><span data-stu-id="82f43-116">You may want to add specific information to each of the cards, such as invoicing and payment details.</span></span>

## <a name="see-also"></a><span data-ttu-id="82f43-117">Katso myös</span><span class="sxs-lookup"><span data-stu-id="82f43-117">See Also</span></span>
[<span data-ttu-id="82f43-118">Toimintaohjeet: Kontaktiyritysten luominen</span><span class="sxs-lookup"><span data-stu-id="82f43-118">How to: Create Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="82f43-119">Toimintaohjeet: Kontaktihenkilöiden luominen</span><span class="sxs-lookup"><span data-stu-id="82f43-119">How to: Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="82f43-120">Kontaktien hallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="82f43-120">Setting Up Relationship Management</span></span>](marketing-setup-marketing.md)  
[<span data-ttu-id="82f43-121">Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa</span><span class="sxs-lookup"><span data-stu-id="82f43-121">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="82f43-122">Toimintaohje: Kontaktien linkittäminen aiemmin luotuihin asiakkaisiin, toimittajiin tai pankkitileihin</span><span class="sxs-lookup"><span data-stu-id="82f43-122">How to: Link Contacts to Existing Customers, Vendors, or Bank Accounts</span></span>](marketing-how-link-contact.md)  
[<span data-ttu-id="82f43-123">Liikesuhteiden liittäminen kontaktiin</span><span class="sxs-lookup"><span data-stu-id="82f43-123">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="82f43-124">Financialsin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="82f43-124">Working with Financials</span></span>](ui-work-product.md)

