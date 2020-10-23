---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0c1131d4517f71a2ad43d0ec1830fc2a486124e3
ms.sourcegitcommit: 428f180604e5afcf94fa0e92a0615f58c88e13cd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3959662"
---
<span data-ttu-id="ed415-101">Voit käyttää automaattisia tilikoodeja automaattisen tilin kirjausryhmän luonnin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="ed415-101">To use automatic account codes, you must create an automatic account posting group.</span></span>  

## <a name="to-set-up-automatic-account-posting-groups"></a><span data-ttu-id="ed415-102">Automaattisten tilin kirjausryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ed415-102">To set up automatic account posting groups</span></span>  

1. <span data-ttu-id="ed415-103">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](../../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Autom. tiliryhmät** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ed415-103">Choose the ![Lightbulb that opens the Tell Me feature](../../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Auto. Acc. Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ed415-104">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="ed415-104">Choose the **New** action.</span></span>  
3. <span data-ttu-id="ed415-105">Täytä **Yleinen**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ed415-105">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ed415-106">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ed415-106">Field</span></span>|<span data-ttu-id="ed415-107">Description</span><span class="sxs-lookup"><span data-stu-id="ed415-107">Description</span></span>|  
    |-----------|-----------------|  
    |<span data-ttu-id="ed415-108">**Nro**</span><span class="sxs-lookup"><span data-stu-id="ed415-108">**No.**</span></span>|<span data-ttu-id="ed415-109">Anna automaattiselle tilin kirjausryhmälle yksilöivä aakkosnumeerinen numero.</span><span class="sxs-lookup"><span data-stu-id="ed415-109">Enter a unique alphanumeric number for the automatic account posting group.</span></span>|  
    |<span data-ttu-id="ed415-110">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="ed415-110">**Description**</span></span>|<span data-ttu-id="ed415-111">Anna automaattisen tilin kirjausryhmän kuvaus.</span><span class="sxs-lookup"><span data-stu-id="ed415-111">Enter a description for the automatic account posting group.</span></span>|  

4. <span data-ttu-id="ed415-112">Täytä **Automaattinen tilirivi** -pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="ed415-112">On the **Automatic Acc. Line** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ed415-113">Kenttä</span><span class="sxs-lookup"><span data-stu-id="ed415-113">Field</span></span>|<span data-ttu-id="ed415-114">Description</span><span class="sxs-lookup"><span data-stu-id="ed415-114">Description</span></span>|  
    |-----------|-----------------|  
    |<span data-ttu-id="ed415-115">**Kohdistusprosentti**</span><span class="sxs-lookup"><span data-stu-id="ed415-115">**Allocation Percentage**</span></span>|<span data-ttu-id="ed415-116">Anna lähderivin summan kohdistettava prosentti.</span><span class="sxs-lookup"><span data-stu-id="ed415-116">Enter the percentage of the source line amount that is to be allocated.</span></span>|  
    |<span data-ttu-id="ed415-117">**KP-tilinro**</span><span class="sxs-lookup"><span data-stu-id="ed415-117">**G/L Account No.**</span></span>|<span data-ttu-id="ed415-118">Anna kirjanpitotilin numero, jolle kohdistus kirjataan.</span><span class="sxs-lookup"><span data-stu-id="ed415-118">Enter the general ledger account number to which the allocation should be posted.</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="ed415-119">**Kokonaissaldo**-kentässä lasketaan yhteen kirjausryhmän automaattisten tilirivien **Kohdistusprosentti**-kentän arvot.</span><span class="sxs-lookup"><span data-stu-id="ed415-119">The **Total Balance** field totals the **Allocation Percentage** field for automatic account lines in a posting group.</span></span> <span data-ttu-id="ed415-120">Jos kirjausryhmän kokonaiskohdistusprosentti ei ole nolla, nimikkeen kirjauksen yhteydessä näytetään virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="ed415-120">If the total allocation percent for a posting group does not balance to zero, an error message will be displayed when the item is posted.</span></span>  

5. <span data-ttu-id="ed415-121">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="ed415-121">Choose the **OK** button.</span></span>  
