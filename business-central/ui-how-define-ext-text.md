---
title: Laajennettujen kuvausten määrittäminen ylimääräisiä rivejä lisäämällä
description: Voit laajentaa nimikkeen, KP-tilin ja muiden tietojen kuvauksena käytettävää vakiotekstiä lisäämällä ylimääräisiä rivejä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b54c8c82a17cb5e1a25beca1115571733fddc2f4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784688"
---
# <a name="add-extended-text"></a><span data-ttu-id="cabe9-103">Lisätekstin lisääminen</span><span class="sxs-lookup"><span data-stu-id="cabe9-103">Add Extended Text</span></span>

<span data-ttu-id="cabe9-104">Nimikkeiden, varastointiyksiköiden, pääkirjanpitotilien ja resurssien kuvausta voi laajentaa lisäämällä lisärivejä lisätekstinä.</span><span class="sxs-lookup"><span data-stu-id="cabe9-104">You can extend the description for items, stock-keeping units, general ledger accounts, and resources by adding extra lines as extended text.</span></span> <span data-ttu-id="cabe9-105">Lisärivien käytölle voi määrittää myös ehdot.</span><span class="sxs-lookup"><span data-stu-id="cabe9-105">You can also set up conditions for use of the extra lines.</span></span>  

<span data-ttu-id="cabe9-106">Seuraavassa osassa käsitellään lisätekstin lisäämistä nimikkeen kuvaukseen.</span><span class="sxs-lookup"><span data-stu-id="cabe9-106">The following section describes how to add extended text to a description of an item.</span></span> <span data-ttu-id="cabe9-107">Samat ohjeet koskevat myös varastointiyksiköitä, kirjanpitotilejä ja resursseja.</span><span class="sxs-lookup"><span data-stu-id="cabe9-107">But the same steps apply to stock-keeping units, general ledger accounts, and resources.</span></span>  

## <a name="to-define-extended-text-for-an-description"></a><span data-ttu-id="cabe9-108">Kuvauksen lisätekstin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="cabe9-108">To define extended text for an description</span></span>

1. <span data-ttu-id="cabe9-109">Avaa sen nimikkeen kortti, johon lisäteksti lisätään, ja valitse **Lisäteksti**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="cabe9-109">Open the card for an item that you want to add extended text to, and then choose the **Extended Text** action.</span></span>
2. <span data-ttu-id="cabe9-110">Täytä **Koodi**- ja **Kuvaus**-kentät.</span><span class="sxs-lookup"><span data-stu-id="cabe9-110">Fill in the **Code** and **Description** fields.</span></span>
3. <span data-ttu-id="cabe9-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="cabe9-111">Choose the **New**.</span></span>
4. <span data-ttu-id="cabe9-112">Täytä **Kielikoodi**-kenttä tai valitse **Kaikki kielikoodit** -valintaruutu, jos käytät kielikoodeja.</span><span class="sxs-lookup"><span data-stu-id="cabe9-112">Fill in the **Language Code** field or select the **All Language Codes** check box if you use language codes.</span></span>
5. <span data-ttu-id="cabe9-113">Anna arvot **Aloituspvm**- ja/tai **Lopetuspvm**-kenttään, jos haluat rajoittaa lisätekstin käyttöpäiviä.</span><span class="sxs-lookup"><span data-stu-id="cabe9-113">Fill in the **Starting Date** and **Ending Date** fields if you want to limit the dates on which the extended text is used.</span></span>
6. <span data-ttu-id="cabe9-114">Kirjoita lisäteksti **Teksti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cabe9-114">In the **Text** field, write the extended text.</span></span>
7. <span data-ttu-id="cabe9-115">Valitse asianmukaiset valintaruudut niitä asiakirjatyyppejä varten, joihin haluat lisätekstin tulostuvan.</span><span class="sxs-lookup"><span data-stu-id="cabe9-115">Select relevant check boxes for the document types where you want the extended text printed.</span></span>
8. <span data-ttu-id="cabe9-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="cabe9-116">Close the page.</span></span>

<span data-ttu-id="cabe9-117">Tämän lisätekstin voi lisätä nyt asiakirjoihin.</span><span class="sxs-lookup"><span data-stu-id="cabe9-117">You can now add this extended text to documents.</span></span> <span data-ttu-id="cabe9-118">Seuraavaksi käsitellään tapaa, jolla lisäteksti lisätään myyntilaukseen, mutta lisäteksti määritetään samalla tavalla myös mihin tahansa muuhun asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="cabe9-118">The following procedure explains how to add extended text to a sales order, but the same steps apply to any other document that you specified for the extended text.</span></span>  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a><span data-ttu-id="cabe9-119">Laajennetun nimiketekstin lisääminen myyntitilausriville</span><span class="sxs-lookup"><span data-stu-id="cabe9-119">To add an extended item text on a sales order line</span></span>

1. <span data-ttu-id="cabe9-120">Avaa sen nimikkeen myyntitilaus ja myyntirivi, jolle on määritetty laajennettu teksti.</span><span class="sxs-lookup"><span data-stu-id="cabe9-120">Open a sales order with a sales line for an item that has extended text defined.</span></span> <span data-ttu-id="cabe9-121">Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="cabe9-121">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="cabe9-122">Valitse kyseinen rivi ja valitse sitten **Syötä lisätekstit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="cabe9-122">Select the line in question, and then choose the **Insert Ext. Text** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="cabe9-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="cabe9-123">See Also</span></span>

[<span data-ttu-id="cabe9-124">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="cabe9-124">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="cabe9-125">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cabe9-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]