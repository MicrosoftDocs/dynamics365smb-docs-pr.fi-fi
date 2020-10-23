---
title: Laajennettujen kuvausten määrittäminen ylimääräisiä rivejä lisäämällä
description: Voit laajentaa nimikkeen, KP-tilin ja muiden tietojen kuvauksena käytettävää vakiotekstiä lisäämällä ylimääräisiä rivejä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1dd6c3085c0cb8696b6e7011fbea3c3cd9a1c86e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920445"
---
# <a name="add-extended-text"></a><span data-ttu-id="1f27a-103">Lisätekstin lisääminen</span><span class="sxs-lookup"><span data-stu-id="1f27a-103">Add Extended Text</span></span>

<span data-ttu-id="1f27a-104">Nimikkeiden, varastointiyksiköiden, pääkirjanpitotilien ja resurssien kuvausta voi laajentaa lisäämällä lisärivejä lisätekstinä.</span><span class="sxs-lookup"><span data-stu-id="1f27a-104">You can extend the description for items, stock-keeping units, general ledger accounts, and resources by adding extra lines as extended text.</span></span> <span data-ttu-id="1f27a-105">Lisärivien käytölle voi määrittää myös ehdot.</span><span class="sxs-lookup"><span data-stu-id="1f27a-105">You can also set up conditions for use of the extra lines.</span></span>  

<span data-ttu-id="1f27a-106">Seuraavassa osassa käsitellään lisätekstin lisäämistä nimikkeen kuvaukseen.</span><span class="sxs-lookup"><span data-stu-id="1f27a-106">The following section describes how to add extended text to a description of an item.</span></span> <span data-ttu-id="1f27a-107">Samat ohjeet koskevat myös varastointiyksiköitä, kirjanpitotilejä ja resursseja.</span><span class="sxs-lookup"><span data-stu-id="1f27a-107">But the same steps apply to stock-keeping units, general ledger accounts, and resources.</span></span>  

## <a name="to-define-extended-text-for-an-description"></a><span data-ttu-id="1f27a-108">Kuvauksen lisätekstin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1f27a-108">To define extended text for an description</span></span>

1. <span data-ttu-id="1f27a-109">Avaa sen nimikkeen kortti, johon lisäteksti lisätään, ja valitse **Lisäteksti**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="1f27a-109">Open the card for an item that you want to add extended text to, and then choose the **Extended Text** action.</span></span>
2. <span data-ttu-id="1f27a-110">Täytä **Koodi**- ja **Kuvaus**-kentät.</span><span class="sxs-lookup"><span data-stu-id="1f27a-110">Fill in the **Code** and **Description** fields.</span></span>
3. <span data-ttu-id="1f27a-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="1f27a-111">Choose the **New**.</span></span>
4. <span data-ttu-id="1f27a-112">Täytä **Kielikoodi**-kenttä tai valitse **Kaikki kielikoodit** -valintaruutu, jos käytät kielikoodeja.</span><span class="sxs-lookup"><span data-stu-id="1f27a-112">Fill in the **Language Code** field or select the **All Language Codes** check box if you use language codes.</span></span>
5. <span data-ttu-id="1f27a-113">Anna arvot **Aloituspvm**- ja/tai **Lopetuspvm**-kenttään, jos haluat rajoittaa lisätekstin käyttöpäiviä.</span><span class="sxs-lookup"><span data-stu-id="1f27a-113">Fill in the **Starting Date** and **Ending Date** fields if you want to limit the dates on which the extended text is used.</span></span>
6. <span data-ttu-id="1f27a-114">Kirjoita lisäteksti **Teksti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1f27a-114">In the **Text** field, write the extended text.</span></span>
7. <span data-ttu-id="1f27a-115">Valitse asianmukaiset valintaruudut niitä asiakirjatyyppejä varten, joihin haluat lisätekstin tulostuvan.</span><span class="sxs-lookup"><span data-stu-id="1f27a-115">Select relevant check boxes for the document types where you want the extended text printed.</span></span>
8. <span data-ttu-id="1f27a-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1f27a-116">Close the page.</span></span>

<span data-ttu-id="1f27a-117">Tämän lisätekstin voi lisätä nyt asiakirjoihin.</span><span class="sxs-lookup"><span data-stu-id="1f27a-117">You can now add this extended text to documents.</span></span> <span data-ttu-id="1f27a-118">Seuraavaksi käsitellään tapaa, jolla lisäteksti lisätään myyntilaukseen, mutta lisäteksti määritetään samalla tavalla myös mihin tahansa muuhun asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="1f27a-118">The following procedure explains how to add extended text to a sales order, but the same steps apply to any other document that you specified for the extended text.</span></span>  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a><span data-ttu-id="1f27a-119">Laajennetun nimiketekstin lisääminen myyntitilausriville</span><span class="sxs-lookup"><span data-stu-id="1f27a-119">To add an extended item text on a sales order line</span></span>

1. <span data-ttu-id="1f27a-120">Avaa sen nimikkeen myyntitilaus ja myyntirivi, jolle on määritetty laajennettu teksti.</span><span class="sxs-lookup"><span data-stu-id="1f27a-120">Open a sales order with a sales line for an item that has extended text defined.</span></span> <span data-ttu-id="1f27a-121">Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="1f27a-121">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="1f27a-122">Valitse kyseinen rivi ja valitse sitten **Syötä lisätekstit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="1f27a-122">Select the line in question, and then choose the **Insert Ext. Text** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f27a-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1f27a-123">See Also</span></span>

[<span data-ttu-id="1f27a-124">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1f27a-124">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="1f27a-125">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1f27a-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
