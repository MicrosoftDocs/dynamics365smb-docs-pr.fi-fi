---
title: "Maksujen täsmäytys Envestnet Yodlee -pankkisyötteiden laajennuksella | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan pankkitilit linkittävästä Envestnet Yodlee -pankkisyötteiden laajennuksesta, joka nopeuttaa maksujen täsmäyttämistä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: daa014eaa78caa7a317b05ca92ff27c1d1530c06
ms.openlocfilehash: 8b5fab97874815849309aa46a6d44f758cb8dcb2
ms.contentlocale: fi-fi
ms.lasthandoff: 10/17/2017

---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="3b72d-103">Envestnet Yodlee -pankkisyötteiden laajennus</span><span class="sxs-lookup"><span data-stu-id="3b72d-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="3b72d-104">Envestnet Yodlee -pankkisyötepalvelun avulla voit täsmäyttää pankkitileille tehdyt maksut nopeasti linkittämällä järjestelmän pankkitilin verkkopankkitiliin.</span><span class="sxs-lookup"><span data-stu-id="3b72d-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="3b72d-105">Tämä tarkoittaa sitä, että viimeisin tiliote syötetään automaattisesti tai manuaalisesti täsmäytyskirjauskansioon. Sen avulla varmistetaan, että käsittelet aina viimeisimpiä maksuja, sekä minimoidaan virheen mahdollisuus.</span><span class="sxs-lookup"><span data-stu-id="3b72d-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="3b72d-106">Envestnet Yodlee -pankkisyötepalvelu tarjoaa seuraavat edut:</span><span class="sxs-lookup"><span data-stu-id="3b72d-106">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="3b72d-107">poistaa manuaalisyöttämisen tarpeen</span><span class="sxs-lookup"><span data-stu-id="3b72d-107">Removes the need for manual entry.</span></span>
* <span data-ttu-id="3b72d-108">parantaa tehokkuutta ja tarkkuutta maksujen täsmäytyksen aikana</span><span class="sxs-lookup"><span data-stu-id="3b72d-108">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="3b72d-109">tukee suuria määriä pankkeja</span><span class="sxs-lookup"><span data-stu-id="3b72d-109">Supports a large number of banks.</span></span>
* <span data-ttu-id="3b72d-110">tarjoaa pankkitapahtumien päivitetyt tiedot [!INCLUDE[d365fin](includes/d365fin_md.md)]issa</span><span class="sxs-lookup"><span data-stu-id="3b72d-110">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="3b72d-111">tukee manuaalisia ja automaattisia pankkisyötteitä</span><span class="sxs-lookup"><span data-stu-id="3b72d-111">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="3b72d-112">mahdollistaa maksujen täsmäytyksen ulkoistamisen kirjanpitäjälle, koska tiliotteet ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="3b72d-112">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="3b72d-113">Lisätietoja on kohdassa [Toimintaohje: Envestnet Yodlee -pankkisyötepalvelun määrittäminen](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="3b72d-113">For more information, see [How to: Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3b72d-114">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3b72d-114">See Also</span></span>
<span data-ttu-id="3b72d-115">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="3b72d-115">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="3b72d-116">Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen</span><span class="sxs-lookup"><span data-stu-id="3b72d-116">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="3b72d-117">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3b72d-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

