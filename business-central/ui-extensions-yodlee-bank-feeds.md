---
title: Maksujen täsmäytys Envestnet Yodlee Bank Feeds -laajennuksella | Microsoft Docs
description: Tässä ohjeaiheessa käsitellään pankkitilit linkittävästä Envestnet Yodlee Bank Feeds -laajennuksesta, joka nopeuttaa maksujen täsmäyttämistä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: c97673ceda1765033877318b46d63652ec318ae9
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3789423"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="e00ec-103">Envestnet Yodlee Bank Feeds -laajennus</span><span class="sxs-lookup"><span data-stu-id="e00ec-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="e00ec-104">Envestnet Yodlee Bank Feeds -palvelun avulla voit täsmäyttää pankkitileille tehdyt maksut nopeasti linkittämällä järjestelmän pankkitilin verkkopankkitiliin.</span><span class="sxs-lookup"><span data-stu-id="e00ec-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="e00ec-105">Tämä tarkoittaa sitä, että viimeisin tiliote syötetään automaattisesti tai manuaalisesti täsmäytyskirjauskansioon. Sen avulla varmistetaan, että käsittelet aina viimeisimpiä maksuja, sekä minimoidaan virheen mahdollisuus.</span><span class="sxs-lookup"><span data-stu-id="e00ec-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="e00ec-106">Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Yhdysvalloissa ja Kanadassa.</span><span class="sxs-lookup"><span data-stu-id="e00ec-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="e00ec-107">Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Business Central -sovelluksen online-versiossa.</span><span class="sxs-lookup"><span data-stu-id="e00ec-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="e00ec-108">Jos haluat käyttää tätä toimintoa paikallisesti, sinun on hankittava yhteistili Envestnet Yodleelta.</span><span class="sxs-lookup"><span data-stu-id="e00ec-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="e00ec-109">Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Yhdysvalloissa ja Kanadassa.</span><span class="sxs-lookup"><span data-stu-id="e00ec-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="e00ec-110">Vain näissä maissa sijaitsevia pankkeja tuetaan, vaikka muiden maiden pankit voivat näkyä Envestnet Yodlee Bank Feeds -pankin valintaikkunassa [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa.</span><span class="sxs-lookup"><span data-stu-id="e00ec-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e00ec-111">Uuden eurooppalaisen maksupalveludirektiivin vuoksi (PSD2), 4.9.2019 jälkeen tiliotteita ei voi enää tuoda automaattisesti [!INCLUDE[d365fin](includes/d365fin_md.md)] brittiläisistä pankeista.</span><span class="sxs-lookup"><span data-stu-id="e00ec-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e00ec-112">Tutkimme mahdollisuutta ottaa tämä ominaisuus uudelleen käyttöön tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="e00ec-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="e00ec-113">Envestnet Yodlee Bank Feeds -palvelun edut:</span><span class="sxs-lookup"><span data-stu-id="e00ec-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="e00ec-114">poistaa manuaalisyöttämisen tarpeen</span><span class="sxs-lookup"><span data-stu-id="e00ec-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="e00ec-115">parantaa tehokkuutta ja tarkkuutta maksujen täsmäytyksen aikana</span><span class="sxs-lookup"><span data-stu-id="e00ec-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="e00ec-116">tukee suuria määriä pankkeja</span><span class="sxs-lookup"><span data-stu-id="e00ec-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="e00ec-117">tarjoaa pankkitapahtumien päivitetyt tiedot [!INCLUDE[d365fin](includes/d365fin_md.md)]issa</span><span class="sxs-lookup"><span data-stu-id="e00ec-117">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="e00ec-118">tukee manuaalisia ja automaattisia pankkisyötteitä</span><span class="sxs-lookup"><span data-stu-id="e00ec-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="e00ec-119">mahdollistaa maksujen täsmäytyksen ulkoistamisen kirjanpitäjälle, koska tiliotteet ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e00ec-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

## <a name="available-bank-feeds"></a><span data-ttu-id="e00ec-120">Käytettävissä olevat pankkisyötteet</span><span class="sxs-lookup"><span data-stu-id="e00ec-120">Available Bank Feeds</span></span>
<span data-ttu-id="e00ec-121">Voit tarkistaa, tuetaanko pankkia määrittämällä ja muodostamalla yhteyden Envestnet Yodlee Bank Feeds -palveluun.</span><span class="sxs-lookup"><span data-stu-id="e00ec-121">You can check whether a bank is supported by setting up and connecting to the Envestnet Yodlee Bank Feeds service.</span></span> <span data-ttu-id="e00ec-122">Pankki näkyy luettelossa, jos sitä tukee Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="e00ec-122">The bank will appear on the list if it is supported by Envestnet Yodlee.</span></span>

<span data-ttu-id="e00ec-123">Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="e00ec-123">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e00ec-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e00ec-124">See Also</span></span>
<span data-ttu-id="e00ec-125">[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="e00ec-125">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="e00ec-126">Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen</span><span class="sxs-lookup"><span data-stu-id="e00ec-126">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="e00ec-127">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e00ec-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
