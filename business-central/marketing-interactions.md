---
title: Kontaktien kanssa tapahtuvien vuorovaikutusten hallinta| Microsoft Docs
description: Voit hallita kaikenlaista viestintää tai vuorovaikutusta yrityksesi ja kontaktiesi välillä, kuten kirjeenvaihtoa, puheluja ja kokouksia.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 7ef4416c695543cb93fcf0bed9501bfa4d04985d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "917187"
---
# <a name="managing-interactions-with-contacts"></a><span data-ttu-id="1d5ca-103">Kontaktien kanssa tapahtuvien vuorovaikutusten hallinta</span><span class="sxs-lookup"><span data-stu-id="1d5ca-103">Managing Interactions With Contacts</span></span>
<span data-ttu-id="1d5ca-104">[!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa kaikentyyppinen yhteydenpito yrityksesi ja kontaktiesi välillä on vuorovaikutusta.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], interactions are all types of communications between your company and your contacts.</span></span> <span data-ttu-id="1d5ca-105">Yhteydenpito voi tapahtua esimerkiksi kirjeitse, faksitse, sähköpostitse, puhelimitse jne.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-105">For example, communications can be by letter, fax, email, telephone, meetings, and so on.</span></span>

<span data-ttu-id="1d5ca-106">Asiakkuudenhallinnan alueella voit tallentaa kaikki vuorovaikutukset, joita sinulla on kontaktiesi kanssa, jotta voit seurata kontakteihin suuntaamiasi markkinointi- ja myyntiponnistuksia, ja jatkossa parantaa liiketoiminnallista vuorovaikutustasi näiden kontaktien kanssa.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-106">The relationship management area enables you to record all the interactions you have with your contacts in order to keep track of the sales and marketing efforts you have directed at your contacts and to improve your future business interactions with them.</span></span> <span data-ttu-id="1d5ca-107">Sovelluksen määrittäminen niin, että se tallentaa vuorovaikutukset, sisältää seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="1d5ca-107">Setting up your application to record interactions consists of these tasks:</span></span>

* <span data-ttu-id="1d5ca-108">Vuorovaikutusmallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1d5ca-108">Setting up interaction templates</span></span>  
* <span data-ttu-id="1d5ca-109">Vuorovaikutusten luominen kontakteille ja segmenteille</span><span class="sxs-lookup"><span data-stu-id="1d5ca-109">Creating interactions on contacts or segments</span></span>  
* <span data-ttu-id="1d5ca-110">Tallennettujen vuorovaikutusten tarkasteleminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="1d5ca-110">View and manage recorded interactions</span></span>  

##  <a name="setting-up-interaction-templates"></a><span data-ttu-id="1d5ca-111">Vuorovaikutusmallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1d5ca-111">Setting up Interaction Templates</span></span>
<span data-ttu-id="1d5ca-112">Ennen kun voit luoda ja tallentaa vuorovaikutuksia, sinun täytyy määrittää vuorovaikutusmallit.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-112">Before you can create and record interactions, you must set up interaction templates.</span></span> <span data-ttu-id="1d5ca-113">Ennen vuorovaikutusten luomista on määritettävä, mihin vuorovaikutusmalleihin ne perustuvat.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-113">When creating interactions, you must specify the interaction templates they are based on.</span></span> <span data-ttu-id="1d5ca-114">Vuorovaikutusmalli on malli, joka määrittää vuorovaikutuksen perusominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-114">An interaction template is a model that defines the basic characteristics of an interaction.</span></span>
<span data-ttu-id="1d5ca-115">Voit määrittää vuorovaikutusmallin **Vuorovaikutusmallit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-115">You set up an interaction template on the **Interaction Templates** page.</span></span>

<span data-ttu-id="1d5ca-116">Kun olet syöttänyt vuorovaikutusmallin tiedot, voit luoda liitteen, kuten Microsoft Word -asiakirjan.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-116">After you have entered information about the interaction template, you can create an attachment, for example, a Microsoft Word document.</span></span> <span data-ttu-id="1d5ca-117">Toista vaiheet ja luo niin monta vuorovaikutusmallia kuin haluat.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-117">Repeat the steps to set up as many interaction templates as you want.</span></span>  

## <a name="creating-interactions"></a><span data-ttu-id="1d5ca-118">Vuorovaikutusten luominen</span><span class="sxs-lookup"><span data-stu-id="1d5ca-118">Creating Interactions</span></span>
<span data-ttu-id="1d5ca-119">Vuorovaikutuksia voi tallentaa kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="1d5ca-119">There are two ways of recording interactions:</span></span>

* <span data-ttu-id="1d5ca-120">Voit luoda manuaalisesti vuorovaikutuksia, jotka on linkitetty yhteen kontaktiin tai segmenttiin.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-120">You can manually create interactions that are linked to a single contact or to a segment.</span></span> <span data-ttu-id="1d5ca-121">Lisätietoja on kohdassa [Vuorovaikutusten luominen kontakteille ja segmenteille](marketing-how-create-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="1d5ca-121">For more information, see [Create Interactions on Contacts and Segments](marketing-how-create-interactions.md).</span></span>  
* <span data-ttu-id="1d5ca-122">Voit tallentaa vuorovaikutukset automaattisesti, kun teet toimenpiteitä sovelluksessa (esimerkiksi tulostat laskun tai tarjouksen).</span><span class="sxs-lookup"><span data-stu-id="1d5ca-122">You can automatically record interactions when you perform actions in the application, for example, when you print an invoice, or quote.</span></span> <span data-ttu-id="1d5ca-123">Lisätietoja on ohjeaiheessa [Kontaktien kanssa tapahtuvien vuorovaikutusten tallennus automaattisesti](marketing-auto-record-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="1d5ca-123">For more information, see [Automatically Record Interactions with Contacts](marketing-auto-record-interactions.md).</span></span>

## <a name="viewing-and-managing-recorded-interactions"></a><span data-ttu-id="1d5ca-124">Tallennettujen vuorovaikutusten tarkasteleminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="1d5ca-124">Viewing and Managing Recorded Interactions</span></span>
<span data-ttu-id="1d5ca-125">Voit tarkastella kaikkia tallennettuja vuorovaikutuksia, joita ei ole poistettu, **Vuorovaikutuslokin tapahtumat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-125">You can view all the recorded interactions that have not been deleted on the **Interaction Log Entries** page.</span></span> <span data-ttu-id="1d5ca-126">Voit avata sivun seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="1d5ca-126">You can open this page by:</span></span>

* <span data-ttu-id="1d5ca-127">**Etsi sivua tai raporttia** -kuvakkeen avulla, kun haluat hakea **Vuorovaikutuslokin tapahtumat** -kohdasta.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-127">Using the **Search for Page or Report** icon to search on **Interaction Log Entries**.</span></span>
* <span data-ttu-id="1d5ca-128">Valitsemalla kontaktin tai segmentin **Vuorovaikutuslokin tapahtumat** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-128">Choosing the **Interaction Log Entries** action on a contact or segment.</span></span>
  <span data-ttu-id="1d5ca-129">**Vuorovaikutuslokin tapahtuma** -sivu sisältää manuaalisesti luomasi vuorovaikutukset sekä sovelluksen automaattisesti tallentamat vuorovaikutukset.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-129">The **Interaction Log Entry** page contains the interactions you create manually and the interactions that the application records automatically.</span></span>

<span data-ttu-id="1d5ca-130">Tällä sivulla voit</span><span class="sxs-lookup"><span data-stu-id="1d5ca-130">In this page, you can:</span></span>

* <span data-ttu-id="1d5ca-131">tarkastella vuorovaikutusten tilaa</span><span class="sxs-lookup"><span data-stu-id="1d5ca-131">View the status of interactions.</span></span>
* <span data-ttu-id="1d5ca-132">merkitä vuorovaikutukset peruutetuiksi.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-132">Mark interactions as canceled.</span></span>

<span data-ttu-id="1d5ca-133">Voit poistaa vuorovaikutuslokin tapahtumia, jotka on peruutettu.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-133">You can delete interaction log entries that have been canceled.</span></span> <span data-ttu-id="1d5ca-134">Voit poistaa vuorovaikutuslokin tapahtumia valitsemalla ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeen, kirjoittamalla **Poista peruutetut vuorovaikutuslokin tapahtumat** ja valitsemalla sitten liittyvän linkin. Täytä tämän jälkeen tiedot.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-134">To delete interaction log entries, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Canceled Interaction Log Entries**, and then choose the related link, and then fill in the information.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d5ca-135">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1d5ca-135">See Also</span></span>
[<span data-ttu-id="1d5ca-136">Kontaktien hallinta</span><span class="sxs-lookup"><span data-stu-id="1d5ca-136">Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="1d5ca-137">Myyntimahdollisuuksien hallinta</span><span class="sxs-lookup"><span data-stu-id="1d5ca-137">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="1d5ca-138">Business Central -sovelluksen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="1d5ca-138">Working with Business Central</span></span>](ui-work-product.md)  
