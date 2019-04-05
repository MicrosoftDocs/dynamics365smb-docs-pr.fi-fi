---
title: Kontaktien synkronointi asiakkaiden ja toimittajien kanssa| Microsoft Docs
description: Voit muodostaa yhteyden kontaktien, jotka ovat myös asiakkaita, toimittajia tai pankkitilejä, yhteystietoihin tai synkronoida ne, joten tiedot tarvitsee päivittää vain yhdessä paikassa.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 10/01/2018
ms.author: edupont
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: 4785e0644e2cb4c615ed79fbd23bef74d25ca547
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795390"
---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="163e6-103">Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa</span><span class="sxs-lookup"><span data-stu-id="163e6-103">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="163e6-104">Jos jotkin kontakteistasi ovat myös asiakkaita, toimittajia tai pankkitilejä, voit synkronisoida kontaktin tiedot liittyvän asiakkaan, toimittajan tai pankkitilin kanssa.</span><span class="sxs-lookup"><span data-stu-id="163e6-104">If some of your contacts are also customers, vendors, or bank accounts, you can synchronize the contact information with the related customer, vendor, or bank account.</span></span> <span data-ttu-id="163e6-105">Synkronoimisen avulla kontaktien ja asiakkaiden, toimittajien tai pankkitilien yhteiset tiedot säilyvät samoina.</span><span class="sxs-lookup"><span data-stu-id="163e6-105">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>  

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="163e6-106">Erilaisia tapoja, joilla kontaktit voidaan synkronoida asiakkaiden, toimittajien ja pankkitilien kanssa</span><span class="sxs-lookup"><span data-stu-id="163e6-106">Different Ways to Synchronize Contacts with Customers, Vendors and Bank Accounts</span></span>
<span data-ttu-id="163e6-107">Voit synkronisoida kontaktejasi asiakkaiden, toimittajien ja/tai pankkitilien kanssa kolmella tavalla:</span><span class="sxs-lookup"><span data-stu-id="163e6-107">You can synchronize your contacts with customers, vendors, or bank accounts by three methods:</span></span>

* <span data-ttu-id="163e6-108">linkittämällä kontakteja olemassa oleviin asiakkaisiin, toimittajiin ja/tai pankkitileihin kontaktikortilta.</span><span class="sxs-lookup"><span data-stu-id="163e6-108">Link contacts with existing customers, vendors, or bank accounts from the contact card.</span></span> <span data-ttu-id="163e6-109">Lisätietoja on kohdassa [Kontaktien linkittäminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-how-link-contact.md).</span><span class="sxs-lookup"><span data-stu-id="163e6-109">For more information, see [Link Contacts With Customers, Vendors, and Bank Accounts](marketing-how-link-contact.md).</span></span>
* <span data-ttu-id="163e6-110">Luo asiakkaita, toimittajia tai pankkitilejä kontaktista.</span><span class="sxs-lookup"><span data-stu-id="163e6-110">Create customers, vendors, or bank accounts from the contact.</span></span> <span data-ttu-id="163e6-111">Lisätietoja on kohdassa [Asiakkaan, toimittajan tai pankkitilin luominen kontaktista](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="163e6-111">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>
* <span data-ttu-id="163e6-112">Kontaktien luominen asiakkaista, toimittajista tai pankkitileistä.</span><span class="sxs-lookup"><span data-stu-id="163e6-112">Create contacts from customers, vendors or bank accounts.</span></span> <span data-ttu-id="163e6-113">Lisätietoja on kohdassa [Yrityskontaktin luominen asiakkaasta, toimittajasta tai pankkitilistä](marketing-how-create-contact-companies.md).</span><span class="sxs-lookup"><span data-stu-id="163e6-113">For more information, see [Create a company contact from a customer, vendor, or bank account](marketing-how-create-contact-companies.md).</span></span>

## <a name="consequences-of-synchronization"></a><span data-ttu-id="163e6-114">Synkronoimisen seuraukset</span><span class="sxs-lookup"><span data-stu-id="163e6-114">Consequences of Synchronization</span></span>
<span data-ttu-id="163e6-115">Kontaktin synkronoiminen asiakkaan, toimittajan ja pankkitilin kanssa</span><span class="sxs-lookup"><span data-stu-id="163e6-115">When the contact is synchronized with the customer, vendor, bank account:</span></span>

* <span data-ttu-id="163e6-116">Sinun tarvitsee päivittää tiedot vain yhteen paikkaan.</span><span class="sxs-lookup"><span data-stu-id="163e6-116">You only have to update information in one place.</span></span> <span data-ttu-id="163e6-117">Jos esimerkiksi muutat kontaktin puhelinnumeroa, puhelinnumeroon päivitetään automaattisesti sama muutos kuin asiakkaalle, toimittajalle tai pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="163e6-117">For example, if you modify the phone number on the contact, the phone number is automatically updated with the same modification on the customer, the vendor, or the bank account.</span></span>
* <span data-ttu-id="163e6-118">Jos olet määrittänyt numerosarjan kontakteille, kun luot asiakas-, toimittaja- tai pankkitilikortin, ohjelma luo automaattisesti kontaktikortin asiakkaalle, toimittajalle tai pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="163e6-118">If you have specified a number series for contacts, when you create a customer card, a vendor card, or a bank account card, a contact card is automatically created for the customer, vendor or bank account.</span></span>
* <span data-ttu-id="163e6-119">Voit luoda kontaktista myyntitarjouksia ja -tilauksia sekä ostotarjouksia ja -tilauksia.</span><span class="sxs-lookup"><span data-stu-id="163e6-119">You can create sales quotes and orders, and purchase quotes and orders from the contact.</span></span>
* <span data-ttu-id="163e6-120">voit saada ohjelman tallentamaan vuorovaikutuksia, kun teet erilaisia toimenpiteitä (kuten tilausten tai puitetilausten tulostaminen, myynnin huoltotilauksen luominen ja sähköpostin lähettäminen).</span><span class="sxs-lookup"><span data-stu-id="163e6-120">You can have your interactions recorded when you perform actions such as printing orders, blanket orders, creating sales service orders, sending e-mails, and so on.</span></span>
* <span data-ttu-id="163e6-121">jos poistat asiakkaaseen, toimittajaan ja/tai pankkitiliin linkitetyn kontaktin, vain kontakti poistuu ohjelmasta.</span><span class="sxs-lookup"><span data-stu-id="163e6-121">If you delete a contact linked to a customer, vendor or bank account, only the contact is removed.</span></span> <span data-ttu-id="163e6-122">Asiakas, toimittaja tai pankkitili säilytetään.</span><span class="sxs-lookup"><span data-stu-id="163e6-122">The customer, vendor, or bank account remains.</span></span>
* <span data-ttu-id="163e6-123">jos poistat asiakkaaseen, toimittajaan ja/tai pankkitiliin linkitetyn kontaktin, vain kontakti säilytetään.</span><span class="sxs-lookup"><span data-stu-id="163e6-123">If you delete a customer, vendor, bank account linked to a contact, the contact remains.</span></span>

> [!NOTE]  
>   <span data-ttu-id="163e6-124">Jotkin tiedot, kuten laskutus- ja kirjaustiedot, eivät näy kontaktikortilla.</span><span class="sxs-lookup"><span data-stu-id="163e6-124">Some details, such as invoicing and posting details, do not appear on the contact card.</span></span> <span data-ttu-id="163e6-125">Tämän vuoksi ne halutaan ehkä lisätä manuaalisesti asiakaskortille, toimittajakortille tai pankkitilikortille, kun kontakteja luodaan asiakkaina, toimittajina tai pankkitileinä.</span><span class="sxs-lookup"><span data-stu-id="163e6-125">Therefore, you may want to add them manually on the customer card, vendor card, or bank account card when you create contacts as customers, vendors or bank accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="163e6-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="163e6-126">See Also</span></span>
[<span data-ttu-id="163e6-127">Kontaktien hallinta</span><span class="sxs-lookup"><span data-stu-id="163e6-127">Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="163e6-128">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="163e6-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
