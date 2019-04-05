---
title: Maksujen täsmäytys Envestnet Yodlee -pankkisyötteiden laajennuksella | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan pankkitilit linkittävästä Envestnet Yodlee -pankkisyötteiden laajennuksesta, joka nopeuttaa maksujen täsmäyttämistä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 02/26/2019
ms.author: sgroespe
ms.openlocfilehash: 36400b3265517c29f68f7eb59d17d968334e0fb1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "796322"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="c11bc-103">Envestnet Yodlee -pankkisyötteiden laajennus</span><span class="sxs-lookup"><span data-stu-id="c11bc-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="c11bc-104">Envestnet Yodlee -pankkisyötepalvelun avulla voit täsmäyttää pankkitileille tehdyt maksut nopeasti linkittämällä järjestelmän pankkitilin verkkopankkitiliin.</span><span class="sxs-lookup"><span data-stu-id="c11bc-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="c11bc-105">Tämä tarkoittaa sitä, että viimeisin tiliote syötetään automaattisesti tai manuaalisesti täsmäytyskirjauskansioon. Sen avulla varmistetaan, että käsittelet aina viimeisimpiä maksuja, sekä minimoidaan virheen mahdollisuus.</span><span class="sxs-lookup"><span data-stu-id="c11bc-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

> [!NOTE]
> <span data-ttu-id="c11bc-106">Tätä toimintoa tuetaan vain Business Centralin verkkoversiossa.</span><span class="sxs-lookup"><span data-stu-id="c11bc-106">This functionality is only supported in the online version of Business Central.</span></span> <span data-ttu-id="c11bc-107">Jos haluat käyttää tätä toimintoa paikallisesti, sinun on hankittava yhteistili Envestnet Yodleelta.</span><span class="sxs-lookup"><span data-stu-id="c11bc-107">To use this functionality on-premise, you must obtain a cobrand account from Envestnet Yodlee.</span></span>

<span data-ttu-id="c11bc-108">Envestnet Yodlee -pankkisyötepalvelu tarjoaa seuraavat edut:</span><span class="sxs-lookup"><span data-stu-id="c11bc-108">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="c11bc-109">poistaa manuaalisyöttämisen tarpeen</span><span class="sxs-lookup"><span data-stu-id="c11bc-109">Removes the need for manual entry.</span></span>
* <span data-ttu-id="c11bc-110">parantaa tehokkuutta ja tarkkuutta maksujen täsmäytyksen aikana</span><span class="sxs-lookup"><span data-stu-id="c11bc-110">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="c11bc-111">tukee suuria määriä pankkeja</span><span class="sxs-lookup"><span data-stu-id="c11bc-111">Supports a large number of banks.</span></span>
* <span data-ttu-id="c11bc-112">tarjoaa pankkitapahtumien päivitetyt tiedot [!INCLUDE[d365fin](includes/d365fin_md.md)]issa</span><span class="sxs-lookup"><span data-stu-id="c11bc-112">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="c11bc-113">tukee manuaalisia ja automaattisia pankkisyötteitä</span><span class="sxs-lookup"><span data-stu-id="c11bc-113">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="c11bc-114">mahdollistaa maksujen täsmäytyksen ulkoistamisen kirjanpitäjälle, koska tiliotteet ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="c11bc-114">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="c11bc-115">Lisätietoja on kohdassa [Envestnet Yodlee -pankkisyötepalvelun määrittäminen](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="c11bc-115">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c11bc-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c11bc-116">See Also</span></span>
<span data-ttu-id="c11bc-117">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="c11bc-117">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="c11bc-118">Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen</span><span class="sxs-lookup"><span data-stu-id="c11bc-118">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="c11bc-119">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c11bc-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
