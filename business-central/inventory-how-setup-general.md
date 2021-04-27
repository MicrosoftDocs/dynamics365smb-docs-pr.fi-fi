---
title: Yleisten varastonhallinnan asetusten määrittäminen
description: Kuvaus siitä, miten fyysisen varaston ja varaston hallinta voidaan määrittää.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1430123f433cfc101e0ae94ce0598d9c0cdd58b2
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785796"
---
# <a name="set-up-general-inventory-information"></a><span data-ttu-id="6eec2-103">Yleisten varastotietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6eec2-103">Set Up General Inventory Information</span></span>

<span data-ttu-id="6eec2-104">Yleiset varastoasetukset määritetään **Varastonhallinnan asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="6eec2-104">You specify your general inventory setup on the **Inventory Setup** page.</span></span>

## <a name="to-set-up-general-inventory-information"></a><span data-ttu-id="6eec2-105">Yleisten varastotietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6eec2-105">To set up general inventory information</span></span>

1. <span data-ttu-id="6eec2-106">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastonhallinnan asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="6eec2-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="6eec2-107">Täytä **Varastonhallinnan asetukset** -sivulla tarvittavat kentät.</span><span class="sxs-lookup"><span data-stu-id="6eec2-107">On the **Inventory Setup** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="6eec2-108">Lisätietoja kustannuslaskentakentistä, **Automaattisesta kustannusten kirjaamisesta**, **Oletetusta kustannusten kirjaamisesta KP:oon** ja **Oletuskustannuslaskentamenetelmästä** on kohdassa [Varaston kustannusten täsmäyttäminen pääkirjanpitoon](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Suunnittelun tiedot: varaston kustannuslaskelma](design-details-inventory-costing.md) ja [Suunnittelun tiedot: oletettu kustannuskirjaus](design-details-expected-cost-posting.md).</span><span class="sxs-lookup"><span data-stu-id="6eec2-108">For detailed information about the costing fields, **Automatic Cost Posting**, **Expected Cost Posting to G/L**, and **Default Costing Method**, see [Reconcile Inventory Costs with the General Ledger](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Design Details: Inventory Costing](design-details-inventory-costing.md), and [Design Details: Expected Cost Posting](design-details-expected-cost-posting.md).</span></span> <span data-ttu-id="6eec2-109">Lisätietoja yleisestä kustannuslaskennasta on kohdassa [Varastokustannusten hallinta](finance-manage-inventory-costs.md).</span><span class="sxs-lookup"><span data-stu-id="6eec2-109">For more information about costing in general, see [Managing Inventory Costs](finance-manage-inventory-costs.md).</span></span>  

<span data-ttu-id="6eec2-110">Jos haluat sisällyttää fyysisen varastoinnin käsittelyajan ostorivin toimituksen lupaamisen laskentaan, voit määrittää sen oletusarvoksi varastolle ja sijainnille **Varastonhallinnan asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="6eec2-110">If you want to include warehouse handling time in the order promising calculation on the purchase line, you can set it up as a default for the inventory, on the **Inventory Setup** page, and for your location.</span></span> <span data-ttu-id="6eec2-111">Lisätietoja on kohdassa [Toimituksen lupaamisen päivämäärän laskeminen](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="6eec2-111">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="6eec2-112">**Automaattinen kustannusten oikaisu** -näppäin otetaan oletusarvoisesti käyttöön, jotta varaston arvot ovat aina oikeat kirjanpidossa, mikä puolestaan pitää myynti- ja tuottotilastot ajan tasalla.</span><span class="sxs-lookup"><span data-stu-id="6eec2-112">The **Automatic Cost Adjustment** toggle is turned on by default to ensure that inventory values are always correct in the general ledger, which in turn keeps your sales and profit statistics up to date.</span></span> <span data-ttu-id="6eec2-113">Kustannusten muutokset saapuvista merkinnöistä, kuten ostoista tai tuotannosta, kohdistetaan niihin liittyviin lähteviin tietoihin, kuten myynteihin tai siirtoihin.</span><span class="sxs-lookup"><span data-stu-id="6eec2-113">Cost changes from inbound entries, such as those for purchases or production output, are assigned to the related outbound entries, such as sales or transfers.</span></span> <span data-ttu-id="6eec2-114">Tämä on hyödyllistä uusille [!INCLUDE[prod_short](includes/prod_short.md)] -asiakkaille ja pienille yrityksille, joilla on suhteellisen alhaiset varastotransaktiotasot.</span><span class="sxs-lookup"><span data-stu-id="6eec2-114">This is helpful for new [!INCLUDE[prod_short](includes/prod_short.md)] customers and small businesses with relatively low inventory transaction levels.</span></span> <span data-ttu-id="6eec2-115">Yrityksen kasvaessa ja varastotasojen kasvaessa tämä voi kuitenkin hidastaa järjestelmän suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="6eec2-115">However, as a business grows and inventory levels increase, this can slow down system performance.</span></span> <span data-ttu-id="6eec2-116">Jos haluat vähentää suorituskykyä kirjauksen aikana, valitse ajan asetus, joka määrittää, kuinka kauas taaksepäin käsittelypäivämäärästä lähtien saapuva tapahtuma voi aiheuttaa liittyvien lähtevien arvotapahtumien muuttamisen.</span><span class="sxs-lookup"><span data-stu-id="6eec2-116">To minimize reduced performance during posting, select a time option to define how far back in time from the work date an inbound transaction can occur to potentially trigger adjustment of related outbound value entries.</span></span> <span data-ttu-id="6eec2-117">Vaihtoehtoisesti voit muuttaa kustannuksia säännöllisin väliajoin Muuta kust.-nimike tapahtumat -eräajon avulla.</span><span class="sxs-lookup"><span data-stu-id="6eec2-117">Alternatively, you can manually adjust costs at regular intervals with the Adjust Cost - Item Entries batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="6eec2-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6eec2-118">See Also</span></span>
[<span data-ttu-id="6eec2-119">Varastonhallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6eec2-119">Set Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="6eec2-120">[Rakennetiedot: arvostusmenetelmät](design-details-costing-methods.md)  </span><span class="sxs-lookup"><span data-stu-id="6eec2-120">[Design Details: Costing Methods](design-details-costing-methods.md)  </span></span>  
[<span data-ttu-id="6eec2-121">Varaston hallinta</span><span class="sxs-lookup"><span data-stu-id="6eec2-121">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="6eec2-122">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6eec2-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="6eec2-123">Näytettävien ominaisuuksien muuttaminen</span><span class="sxs-lookup"><span data-stu-id="6eec2-123">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="6eec2-124">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="6eec2-124">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]