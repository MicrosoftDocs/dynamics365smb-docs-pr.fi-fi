---
title: "Pankkitilien määrittäminen| Microsoft Docs"
description: "Voit täsmäyttää pankkitilit Financialsissa pankin tiliotteiden avulla."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f46e95e24ef39a93bc93cfda1b9c575b07273566
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-set-up-bank-accounts"></a><span data-ttu-id="336aa-103">Toimittajan pankkitilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="336aa-103">How to: Set Up Bank Accounts</span></span>
<span data-ttu-id="336aa-104">[!INCLUDE[d365fin](includes/d365fin_md.md)] seuraa pankkitapahtumia pankkitilien avulla.</span><span class="sxs-lookup"><span data-stu-id="336aa-104">You use bank accounts in the [!INCLUDE[d365fin](includes/d365fin_md.md)] to keep track of your banking transactions.</span></span> <span data-ttu-id="336aa-105">Tilit voidaan määrittää käyttämään paikallista valuuttaa tai ulkomaan valuuttaa.</span><span class="sxs-lookup"><span data-stu-id="336aa-105">Accounts can be denominated in your local currency or in a foreign currency.</span></span> <span data-ttu-id="336aa-106">Kun olet määrittänyt pankkitilit, voit myös käyttää Sekin tulostus -vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="336aa-106">After you have set up bank accounts, you can also use the check printing option.</span></span>

## <a name="to-set-up-bank-accounts"></a><span data-ttu-id="336aa-107">Pankkitilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="336aa-107">To set up bank accounts</span></span>
1. <span data-ttu-id="336aa-108">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Pankkitilit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="336aa-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="336aa-109">Valitse **Pankkitilit**-ikkunassa **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="336aa-109">In the **Bank Accounts** window, choose the **New** action.</span></span>
3. <span data-ttu-id="336aa-110">Täytä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="336aa-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a><span data-ttu-id="336aa-111">Pankkitilin määrittäminen pankkitiedostojen tuontia tai vientiä varten</span><span class="sxs-lookup"><span data-stu-id="336aa-111">To set up your bank account for import or export of bank files</span></span>
<span data-ttu-id="336aa-112">**Pankkitilin kortti** -ikkunan **Siirto**-pikavälilehden kentät liittyvät pankkisyötteiden ja -tiedostojen tuontiin ja vientiin.</span><span class="sxs-lookup"><span data-stu-id="336aa-112">Fields on the **Transfer** FastTab in the **Bank Account Card** window are related to import and export of bank feeds and files.</span></span> <span data-ttu-id="336aa-113">Lisätietoja on kohdassa [Toimintaohje: Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md) ja [Toimintaohje: Envestnet Yodlee -pankkisyötepalvelun määrittäminen](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="336aa-113">For more information, see [How to: Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) and [How to: Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

1. <span data-ttu-id="336aa-114">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Pankkitilit** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="336aa-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="336aa-115">Avaa sen pankkitilin kortti, josta viet tai johon tuot pankkitiedostot.</span><span class="sxs-lookup"><span data-stu-id="336aa-115">Open the card for a bank account that you will export or import bank files for.</span></span>
3. <span data-ttu-id="336aa-116">Täytä **Siirto**-pikavälilehdessä tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="336aa-116">On the **Transfer** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="336aa-117">Eri tiedostojen vientipalvelut ja niiden tiedostomuodot edellyttävät erilaisia asetuksia **Pankkitilin kortti** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="336aa-117">Different file export services and their formats require different setup values in the **Bank Account Card** window.</span></span> <span data-ttu-id="336aa-118">Saat ilmoituksen virheellisistä tai puuttuvista asetusarvoista, kun yrität viedä tiedoston.</span><span class="sxs-lookup"><span data-stu-id="336aa-118">You will be informed about wrong or missing setup values as you try to export the file.</span></span> <span data-ttu-id="336aa-119">Lue huolellisesti kenttien lyhyet kuvaukset tai katso lisätietoja liittyvien toimenpiteiden ohjeaiheista.</span><span class="sxs-lookup"><span data-stu-id="336aa-119">So read the short descriptions of the fields carefully or refer to the related procedure topics.</span></span> <span data-ttu-id="336aa-120">Esimerkiksi maksutiedoston vienti pohjoisamerikkalaiseen sähköiseen rahansiirtoon (EFT-toiminto) edellyttää, että sekä **Viimeinen maksuosoitusehdotusnumero**-</span><span class="sxs-lookup"><span data-stu-id="336aa-120">For example, exporting a payment file for North American electronic funds transfer (EFT) requires that both the **Last Remittance Advice No.**</span></span> <span data-ttu-id="336aa-121">ja **Siirtonro**-kentät</span><span class="sxs-lookup"><span data-stu-id="336aa-121">field and the **Transit No.**</span></span> <span data-ttu-id="336aa-122">on täytetty.</span><span class="sxs-lookup"><span data-stu-id="336aa-122">field are filled in.</span></span> <span data-ttu-id="336aa-123">Lisätietoja on kohdassa [Toimintaohje: Maksujen vieminen pankkitiedostoon](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="336aa-123">For more information, see [How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a><span data-ttu-id="336aa-124">Toimittajan pankkitilien määrittäminen pankkitiedostojen vientiä varten</span><span class="sxs-lookup"><span data-stu-id="336aa-124">To set up vendor bank accounts for export of bank files</span></span>
<span data-ttu-id="336aa-125">**Toimittajan pankkitilin kortti** -ikkunan **Siirto**-pikavälilehden kentät liittyvät pankkisyötteiden ja -tiedostojen vientiin.</span><span class="sxs-lookup"><span data-stu-id="336aa-125">Fields on the **Transfer** FastTab in the **Vendor Bank Account Card** window are related to export of bank feeds and files.</span></span> <span data-ttu-id="336aa-126">Lisätietoja on kohdassa [Toimintaohje: Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md) ja [Toimintaohje: Maksujen vienti pankkitiedostoon](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="336aa-126">For more information, see [How to: Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) and [How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

1. <span data-ttu-id="336aa-127">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Toimittajat** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="336aa-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="336aa-128">Avaa sen toimittajan kortti, jonka pankkitiliin viet maksujen pankkitiedostot.</span><span class="sxs-lookup"><span data-stu-id="336aa-128">Open the card for a vendor whose bank account you will export payment bank files to.</span></span>
3. <span data-ttu-id="336aa-129">Valitse **Pankkitilit**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="336aa-129">Choose the **Bank Accounts** action.</span></span>
3. <span data-ttu-id="336aa-130">Täytä tarvittaessa **Toimittajan pankkitilin kortti** -ikkunan **Siirto**-pikavälilehden kentät.</span><span class="sxs-lookup"><span data-stu-id="336aa-130">In the **Vendor Bank Account Card** window, on the **Transfer** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="336aa-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="336aa-131">See Also</span></span>
[<span data-ttu-id="336aa-132">Pankkitoiminnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="336aa-132">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="336aa-133">Pankkitilien hallinta</span><span class="sxs-lookup"><span data-stu-id="336aa-133">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
<span data-ttu-id="336aa-134">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="336aa-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

