---
title: Maksujen täsmäytys Envestnet Yodlee Bank Feeds -laajennuksella
description: Tässä ohjeaiheessa käsitellään pankkitilit linkittävästä Envestnet Yodlee Bank Feeds -laajennuksesta, joka nopeuttaa maksujen täsmäyttämistä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 946958669f4554869e171286927bf498fe62a7ed
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5394022"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="96f40-103">Envestnet Yodlee Bank Feeds -laajennus</span><span class="sxs-lookup"><span data-stu-id="96f40-103">The Envestnet Yodlee Bank Feeds Extension</span></span>

<span data-ttu-id="96f40-104">Envestnet Yodlee Bank Feeds -palvelun avulla voit täsmäyttää pankkitileille tehdyt maksut nopeasti linkittämällä järjestelmän pankkitilin verkkopankkitiliin.</span><span class="sxs-lookup"><span data-stu-id="96f40-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="96f40-105">Tämä tarkoittaa sitä, että viimeisin tiliote syötetään automaattisesti tai manuaalisesti täsmäytyskirjauskansioon. Sen avulla varmistetaan, että käsittelet aina viimeisimpiä maksuja, sekä minimoidaan virheen mahdollisuus.</span><span class="sxs-lookup"><span data-stu-id="96f40-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="96f40-106">Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Yhdysvalloissa ja Kanadassa.</span><span class="sxs-lookup"><span data-stu-id="96f40-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="96f40-107">Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Business Central -sovelluksen online-versiossa.</span><span class="sxs-lookup"><span data-stu-id="96f40-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="96f40-108">Jos haluat käyttää tätä toimintoa paikallisesti, sinun on hankittava yhteistili Envestnet Yodleelta.</span><span class="sxs-lookup"><span data-stu-id="96f40-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="96f40-109">Envestnet Yodlee Bank Feeds -palvelua tuetaan vain Yhdysvalloissa ja Kanadassa.</span><span class="sxs-lookup"><span data-stu-id="96f40-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="96f40-110">Vain näissä maissa sijaitsevia pankkeja tuetaan, vaikka muiden maiden pankit voivat näkyä Envestnet Yodlee Bank Feeds -pankin valintaikkunassa [!INCLUDE[prod_short](includes/prod_short.md)]:ssa.</span><span class="sxs-lookup"><span data-stu-id="96f40-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="96f40-111">Uuden eurooppalaisen maksupalveludirektiivin vuoksi (PSD2), 4.9.2019 jälkeen tiliotteita ei voi enää tuoda automaattisesti [!INCLUDE[prod_short](includes/prod_short.md)] brittiläisistä pankeista.</span><span class="sxs-lookup"><span data-stu-id="96f40-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="96f40-112">Tutkimme mahdollisuutta ottaa tämä ominaisuus uudelleen käyttöön tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="96f40-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="96f40-113">Envestnet Yodlee Bank Feeds -palvelun edut:</span><span class="sxs-lookup"><span data-stu-id="96f40-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="96f40-114">poistaa manuaalisyöttämisen tarpeen</span><span class="sxs-lookup"><span data-stu-id="96f40-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="96f40-115">parantaa tehokkuutta ja tarkkuutta maksujen täsmäytyksen aikana</span><span class="sxs-lookup"><span data-stu-id="96f40-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="96f40-116">tukee suuria määriä pankkeja</span><span class="sxs-lookup"><span data-stu-id="96f40-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="96f40-117">tarjoaa pankkitapahtumien päivitetyt tiedot [!INCLUDE[prod_short](includes/prod_short.md)]issa</span><span class="sxs-lookup"><span data-stu-id="96f40-117">Allows up-to-date information about bank transactions from within [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
* <span data-ttu-id="96f40-118">tukee manuaalisia ja automaattisia pankkisyötteitä</span><span class="sxs-lookup"><span data-stu-id="96f40-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="96f40-119">mahdollistaa maksujen täsmäytyksen ulkoistamisen kirjanpitäjälle, koska tiliotteet ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="96f40-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

## <a name="available-bank-feeds"></a><span data-ttu-id="96f40-120">Käytettävissä olevat pankkisyötteet</span><span class="sxs-lookup"><span data-stu-id="96f40-120">Available Bank Feeds</span></span>
<span data-ttu-id="96f40-121">Voit tarkistaa, tuetaanko pankkia määrittämällä ja muodostamalla yhteyden Envestnet Yodlee Bank Feeds -palveluun.</span><span class="sxs-lookup"><span data-stu-id="96f40-121">You can check whether a bank is supported by setting up and connecting to the Envestnet Yodlee Bank Feeds service.</span></span> <span data-ttu-id="96f40-122">Pankki näkyy luettelossa, jos sitä tukee Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="96f40-122">The bank will appear on the list if it is supported by Envestnet Yodlee.</span></span>

<span data-ttu-id="96f40-123">Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="96f40-123">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="96f40-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="96f40-124">See Also</span></span>
<span data-ttu-id="96f40-125">[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="96f40-125">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="96f40-126">Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen</span><span class="sxs-lookup"><span data-stu-id="96f40-126">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="96f40-127">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="96f40-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]