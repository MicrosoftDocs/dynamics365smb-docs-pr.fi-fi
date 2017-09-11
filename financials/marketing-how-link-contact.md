---
title: "Kontaktien linkittäminen asiakkaisiin ja toimittajiin| Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten kontakti linkitetään saman yrityksen asiakkaaseen, toimittajaan tai pankkitiliin yhteisten tietojen synkronointia varten."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f5bbadb37a40dbc7b06668d940d2be9569aaa8e8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-link-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="d2104-103">Toimintaohje: Kontaktien linkittäminen asiakkaisiin, toimittajiin ja pankkitileihin</span><span class="sxs-lookup"><span data-stu-id="d2104-103">How to: Link Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="d2104-104">Jos kontakti ja joko asiakas, toimittaja tai pankkitili ovat samassa yrityksessä, voit linkittää nämä kaksi objektia.</span><span class="sxs-lookup"><span data-stu-id="d2104-104">If you have contact and either a customer, vendor, or bank account for the same company, you can link the two entities.</span></span> <span data-ttu-id="d2104-105">Kahden objektin linkittäminen mahdollistaa yhteisten tietojen synkronoimisen. Tällöin ne ovat samat molemmissa paikoissa.</span><span class="sxs-lookup"><span data-stu-id="d2104-105">Linking the two entities enables you to synchronize data that is common so that it is the same in both places.</span></span>

## <a name="link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a><span data-ttu-id="d2104-106">Kontaktin linkittäminen olemassa olevaan asiakkaaseen, toimittajaan tai pankkitiliin</span><span class="sxs-lookup"><span data-stu-id="d2104-106">Link a Contact to an Existing Customer, Vendor, or Bank Account</span></span>
1. <span data-ttu-id="d2104-107">Avaa kontakti, jonka haluat linkittää.</span><span class="sxs-lookup"><span data-stu-id="d2104-107">Open the contact that you want to link.</span></span>
2. <span data-ttu-id="d2104-108">Valitse **Linkitä olemassa olevan kanssa** -toiminto ja valitse sitten **Asiakas**, **Toimittaja** tai **Pankki**.</span><span class="sxs-lookup"><span data-stu-id="d2104-108">Choose the **Link with existing** action, and then choose **Customer**, **Vendor**, or **Bank**.</span></span>
3. <span data-ttu-id="d2104-109">Valitse asiakas, toimittaja tai pankkitili, johon linkitetään.</span><span class="sxs-lookup"><span data-stu-id="d2104-109">Select the customer, vendor, or bank account to link to.</span></span>

   <span data-ttu-id="d2104-110">Määritä **Nykyiset pääkentät** -kohdassa kentät, jotka tulee priorisoida, jos kontaktille, toimittajalle tai tilille yhteisissä kentissä esiintyy ristiriitaisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="d2104-110">In the **Current Master Fields**, you specify which fields should prioritize in case of conflicting information in fields common to the contact and customer, vendor, or account.</span></span> <span data-ttu-id="d2104-111">Jos esimerkiksi myyntihenkilön koodi on erilainen kontaktilla ja asiakkaalla, voit päättää käyttää kontaktin tietoja valitsemalla **Kontakti** -kohdan.</span><span class="sxs-lookup"><span data-stu-id="d2104-111">For example, if the salesperson code is different in the contact than the customer, you can decide, by selecting **Contact**, to use the information in the contact.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2104-112">Katso myös</span><span class="sxs-lookup"><span data-stu-id="d2104-112">See Also</span></span>
[<span data-ttu-id="d2104-113">Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa</span><span class="sxs-lookup"><span data-stu-id="d2104-113">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="d2104-114">Kontaktien luonti ja hallinta</span><span class="sxs-lookup"><span data-stu-id="d2104-114">Creating and Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="d2104-115">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d2104-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

