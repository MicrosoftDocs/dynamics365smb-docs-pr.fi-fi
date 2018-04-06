---
title: Kontaktien kanssa tapahtuvien vuorovaikutusten hallinta| Microsoft Docs
description: "Voit hallita kaikenlaista viestintää tai vuorovaikutusta yrityksesi ja kontaktiesi välillä, kuten kirjeenvaihtoa, puheluja ja kokouksia."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74028404f5bc7c466b9bf7c0769e78804fd6114f
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="managing-interactions-with-contacts"></a><span data-ttu-id="cc3a4-103">Kontaktien kanssa tapahtuvien vuorovaikutusten hallinta</span><span class="sxs-lookup"><span data-stu-id="cc3a4-103">Managing Interactions With Contacts</span></span>
<span data-ttu-id="cc3a4-104">[!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa kaikentyyppinen yhteydenpito yrityksesi ja kontaktiesi välillä on vuorovaikutusta.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], interactions are all types of communications between your company and your contacts.</span></span> <span data-ttu-id="cc3a4-105">Yhteydenpito voi tapahtua esimerkiksi kirjeitse, faksitse, sähköpostitse, puhelimitse jne.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-105">For example, communications can be by letter, fax, email, telephone, meetings, and so on.</span></span>

<span data-ttu-id="cc3a4-106">Asiakkuudenhallinnan alueella voit tallentaa kaikki vuorovaikutukset, joita sinulla on kontaktiesi kanssa, jotta voit seurata kontakteihin suuntaamiasi markkinointi- ja myyntiponnistuksia, ja jatkossa parantaa liiketoiminnallista vuorovaikutustasi näiden kontaktien kanssa.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-106">The relationship management area enables you to record all the interactions you have with your contacts in order to keep track of the sales and marketing efforts you have directed at your contacts and to improve your future business interactions with them.</span></span> <span data-ttu-id="cc3a4-107">Sovelluksen määrittäminen niin, että se tallentaa vuorovaikutukset, sisältää seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="cc3a4-107">Setting up your application to record interactions consists of these tasks:</span></span>

* <span data-ttu-id="cc3a4-108">Vuorovaikutusmallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="cc3a4-108">Setting up interaction templates</span></span>  
* <span data-ttu-id="cc3a4-109">Vuorovaikutusten luominen kontakteille ja segmenteille</span><span class="sxs-lookup"><span data-stu-id="cc3a4-109">Creating interactions on contacts or segments</span></span>  
* <span data-ttu-id="cc3a4-110">Tallennettujen vuorovaikutusten tarkasteleminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="cc3a4-110">View and manage recorded interactions</span></span>  

##  <a name="setting-up-interaction-templates"></a><span data-ttu-id="cc3a4-111">Vuorovaikutusmallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="cc3a4-111">Setting up Interaction Templates</span></span>
<span data-ttu-id="cc3a4-112">Ennen kun voit luoda ja tallentaa vuorovaikutuksia, sinun täytyy määrittää vuorovaikutusmallit.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-112">Before you can create and record interactions, you must set up interaction templates.</span></span> <span data-ttu-id="cc3a4-113">Ennen vuorovaikutusten luomista on määritettävä, mihin vuorovaikutusmalleihin ne perustuvat.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-113">When creating interactions, you must specify the interaction templates they are based on.</span></span> <span data-ttu-id="cc3a4-114">Vuorovaikutusmalli on malli, joka määrittää vuorovaikutuksen perusominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-114">An interaction template is a model that defines the basic characteristics of an interaction.</span></span>
<span data-ttu-id="cc3a4-115">Voit määrittää vuorovaikutusmallin **Vuorovaikutusmallit**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-115">You set up an interaction template in the **Interaction Templates** window.</span></span>  

## <a name="creating-interactions"></a><span data-ttu-id="cc3a4-116">Vuorovaikutusten luominen</span><span class="sxs-lookup"><span data-stu-id="cc3a4-116">Creating Interactions</span></span>
<span data-ttu-id="cc3a4-117">Vuorovaikutuksia voi tallentaa kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="cc3a4-117">There are two ways of recording interactions:</span></span>

* <span data-ttu-id="cc3a4-118">Voit luoda manuaalisesti vuorovaikutuksia, jotka on linkitetty yhteen kontaktiin tai segmenttiin.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-118">You can manually create interactions that are linked to a single contact or to a segment.</span></span> <span data-ttu-id="cc3a4-119">Lisätietoja on kohdassa [Vuorovaikutusten luominen kontakteille ja segmenteille](marketing-how-create-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="cc3a4-119">For more information, see [Create Interactions on Contacts and Segments](marketing-how-create-interactions.md).</span></span>  
* <span data-ttu-id="cc3a4-120">Voit tallentaa vuorovaikutukset automaattisesti, kun teet toimenpiteitä sovelluksessa (esimerkiksi tulostat laskun tai tarjouksen).</span><span class="sxs-lookup"><span data-stu-id="cc3a4-120">You can automatically record interactions when you perform actions in the application, for example, when you print an invoice, or quote.</span></span> <span data-ttu-id="cc3a4-121">Lisätietoja on kohdassa [Kontaktien kanssa tapahtuvien vuorovaikutusten tallentaminen automaattisesti](marketing-auto-record-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="cc3a4-121">For more information, see [Automatically Record Interactions with Contacts](marketing-auto-record-interactions.md).</span></span>

## <a name="viewing-and-managing-recorded-interactions"></a><span data-ttu-id="cc3a4-122">Tallennettujen vuorovaikutusten tarkasteleminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="cc3a4-122">Viewing and managing Recorded Interactions</span></span>
<span data-ttu-id="cc3a4-123">Voit tarkastella kaikkia tallennettuja vuorovaikutuksia, joita ei ole poistettu, **Vuorovaikutuslokin tapahtumat** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-123">You can view all the recorded interactions that have not been deleted in the **Interaction Log Entries** window.</span></span> <span data-ttu-id="cc3a4-124">Voit avata ikkunan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="cc3a4-124">You can open this window by:</span></span>

* <span data-ttu-id="cc3a4-125">**Etsi sivua tai raporttia** -kuvakkeen avulla, kun haluat hakea **Vuorovaikutuslokin tapahtumat** -kohdasta.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-125">Using the **Search for Page or Report** icon to search on **Interaction Log Entries**.</span></span>
* <span data-ttu-id="cc3a4-126">Valitsemalla kontaktin tai segmentin **Vuorovaikutuslokin tapahtumat** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-126">Choosing the **Interaction Log Entries** action on a contact or segment.</span></span>
  <span data-ttu-id="cc3a4-127">**Vuorovaikutuslokin tapahtuma** -ikkuna sisältää manuaalisesti luomasi vuorovaikutukset sekä sovelluksen automaattisesti tallentamat vuorovaikutukset.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-127">The **Interaction Log Entry** window contains the interactions you create manually and the interactions that the application records automatically.</span></span>

<span data-ttu-id="cc3a4-128">Tässä ikkunassa voit</span><span class="sxs-lookup"><span data-stu-id="cc3a4-128">In this window, you can:</span></span>

* <span data-ttu-id="cc3a4-129">tarkastella vuorovaikutusten tilaa</span><span class="sxs-lookup"><span data-stu-id="cc3a4-129">View the status of interactions.</span></span>
* <span data-ttu-id="cc3a4-130">merkitä vuorovaikutukset peruutetuiksi.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-130">Mark interactions as canceled.</span></span>

<span data-ttu-id="cc3a4-131">Voit poistaa vuorovaikutuslokin tapahtumia, jotka on peruutettu.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-131">You can delete interaction log entries that have been canceled.</span></span> <span data-ttu-id="cc3a4-132">Voit poistaa vuorovaikutuslokin tapahtumia valitsemalla ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvakkeen, kirjoittamalla **Poista peruutetut vuorovaikutuslokin tapahtumat** ja valitsemalla sitten liittyvän linkin. Täytä tämän jälkeen tiedot.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-132">To delete interaction log entries, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Canceled Interaction Log Entries**, and then choose the related link, and then fill in the information.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc3a4-133">Katso myös</span><span class="sxs-lookup"><span data-stu-id="cc3a4-133">See Also</span></span>
[<span data-ttu-id="cc3a4-134">Kontaktien hallinta</span><span class="sxs-lookup"><span data-stu-id="cc3a4-134">Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="cc3a4-135">Myyntimahdollisuuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="cc3a4-135">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="cc3a4-136">Financialsin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="cc3a4-136">Working with Financials</span></span>](ui-work-product.md)  

