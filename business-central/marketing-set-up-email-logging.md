---
title: Sähköpostin lokiinkirjauksen määrittäminen | Microsoft Docs
description: Lisätietoja siitä, miten myyjien ja asiakkaiden sähköpostivuorovaikutukset voidaan muuttaa todellisiksi myyntimahdollisuuksiksi.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 08/26/2019
ms.author: bholtorf
ms.openlocfilehash: e42618be17ff4f9bfe0d54a88e70d5a1841568c1
ms.sourcegitcommit: 8d9f08304b2f3b5504332bc626383797564ac5e3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/26/2019
ms.locfileid: "1920464"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><span data-ttu-id="31324-103">Myyjien ja yhteyshenkilöiden välisten sähköpostiviestien seuraaminen</span><span class="sxs-lookup"><span data-stu-id="31324-103">Track Email Message Exchanges Between Salespeople and Contacts</span></span>
<span data-ttu-id="31324-104">Saat enemmän hyötyä myyjien ja olemassa olevien tai potentiaalisten asiakkaiden välisestä viestinnästä, jos seuraat sähköpostiviestejä ja muunnat ne toiminnallisiksi mahdollisuuksiksi.</span><span class="sxs-lookup"><span data-stu-id="31324-104">Get more out of the communications between salespeople and your existing or potential customers by tracking email exchanges, and then turning them into actionable opportunities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="31324-105">-sovellusta voi käyttää yhdessä Exchange Onlinen kanssa. Näin voit seurata saapuvia ja lähteviä viestejä.</span><span class="sxs-lookup"><span data-stu-id="31324-105">can work with Exchange Online to keep a log of the inbound and outbound messages.</span></span> <span data-ttu-id="31324-106">Voit tarkastella ja analysoida kunkin viestin sisältöä **Vuorovaikutuslokin tapahtumat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="31324-106">You can view and analyze the contents of each message on the **Interaction Log Entries** page.</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085401]

## <a name="setting-up-included365finincludesd365fin_mdmd-to-log-email-messages"></a><span data-ttu-id="31324-107">Määritetään [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellus sähköpostiviestien kirjaamista varten</span><span class="sxs-lookup"><span data-stu-id="31324-107">Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)] to Log Email Messages</span></span>
<span data-ttu-id="31324-108">Aloita sähköpostien kirjaaminen seuraavien kahden helpon vaiheen avulla:</span><span class="sxs-lookup"><span data-stu-id="31324-108">Get started with email logging in two easy steps:</span></span>

1. <span data-ttu-id="31324-109">Muodosta yhteys [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellukseen Exchange Onlinen avulla Office 365 -tilauksessa.</span><span class="sxs-lookup"><span data-stu-id="31324-109">Connect [!INCLUDE[d365fin](includes/d365fin_md.md)] with Exchange Online for your Office 365 subscription.</span></span> <span data-ttu-id="31324-110">Exchange Online käsittelee sähköpostiviestisi.</span><span class="sxs-lookup"><span data-stu-id="31324-110">Exchange Online handles your email messages.</span></span> <span data-ttu-id="31324-111">Tämä on helppo tehdä asetusten ohjatun määrityksen oppaan avulla.</span><span class="sxs-lookup"><span data-stu-id="31324-111">We've made this step easy by providing an assisted setup guide.</span></span> <span data-ttu-id="31324-112">Tarvitset vain järjestelmänvalvojan tunnistetiedot Office 365:n järjestelmänvalvojan tiliä varten.</span><span class="sxs-lookup"><span data-stu-id="31324-112">You just need your administrator credentials for your administrator account in Office 365.</span></span> <span data-ttu-id="31324-113">Aloita oppaan käyttäminen siirtymällä **Asetusten ohjattu määritys** -kohtaan ja valitsemalla **Määritä sähköpostin lokiinkirjaus**.</span><span class="sxs-lookup"><span data-stu-id="31324-113">To start the guide, go to **Assisted Setup**, and then choose **Set up email logging**.</span></span> 
2. <span data-ttu-id="31324-114">Varmista, että [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellukseen on määritetty oikeat sähköpostiosoitteet myyjille ja yhteyshenkilöille sen mukaan, ovatko he potentiaalisia vai olemassa olevia asiakkaita.</span><span class="sxs-lookup"><span data-stu-id="31324-114">Make sure that valid email addresses have been entered in [!INCLUDE[d365fin](includes/d365fin_md.md)] for your sales people and contacts, depending on whether they are potential or existing customers.</span></span> <span data-ttu-id="31324-115">Tee tämä avaamalla kunkin asiakkaan tai myyjän **Yhteyshenkilö**- tai **Myyjä/ostaja**-kortti ja tarkistamalla **Sähköposti**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="31324-115">To do that, for each customer or salesperson, open the **Contact** or **Salesperson/Purchaser** card and have a look in the **Email** field.</span></span>

> [!Tip]
> <span data-ttu-id="31324-116">Kun olet tehnyt nämä oppaan vaiheet, voit tarkistaa yhteyden tilan.</span><span class="sxs-lookup"><span data-stu-id="31324-116">After you complete the steps in the guide you can check whether the connection was successful.</span></span> <span data-ttu-id="31324-117">Siirry **Kontaktienhallinnan asetukset** -kohtaan, valitse **Prosessi** ja valitse sitten **Toiminnot**. Valitse lopuksi **Tarkista sähköpostin lokiinkirjauksen asetukset**.</span><span class="sxs-lookup"><span data-stu-id="31324-117">Search for **Marketing Setup**, choose **Process**, then **Functions**, and then **Validate Email Logging Setup**.</span></span>

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a><span data-ttu-id="31324-118">Sähköpostiviestien tarkasteleminen vuorovaikutuslokissa</span><span class="sxs-lookup"><span data-stu-id="31324-118">Viewing Email Message Exchanges in the Interaction Log</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="31324-119">luo **Vuorovaikutusloki**-sivulle tapahtuman aina, kun myyjä ja yhteyshenkilö lähettävät sähköpostiviestejä.</span><span class="sxs-lookup"><span data-stu-id="31324-119">creates an entry on the **Interaction Log** page each time a salesperson and a contact exchange an email message.</span></span> <span data-ttu-id="31324-120">Voit tarkastella vuorovaikutuslokia avaamalla **Yhteyshenkilö**- tai **Myyjä/ostaja**-kortin ja valitsemalla sitten **Siirry**-, **Historia**- ja **Vuorovaikutuslokin tapahtumat**-kohdat.</span><span class="sxs-lookup"><span data-stu-id="31324-120">To view the interaction log, open the **Contact** or **Salesperson\*Purchaser** card for the person, and then choose **Navigate**, **History**, and then choose **Interaction Log Entries**.</span></span> <span data-ttu-id="31324-121">Lokin tapahtumille voi tehdä esimerkiksi seuraavia toimintoja:</span><span class="sxs-lookup"><span data-stu-id="31324-121">There are a few things we can do with each entry in the log, for example:</span></span>

* <span data-ttu-id="31324-122">Voit tarkastella sähköpostiviestin sisältöä valitsemalla **Näytä liitteet** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="31324-122">View the content of the email message that was exchanged by clicking the **Show Attachments** action.</span></span>
* <span data-ttu-id="31324-123">Voit muuttaa sähköpostiviestinnän myyntimahdollisuudeksi. Jos tapahtuma näyttää lupaavalta, voit muuttaa sen mahdollisuudeksi, jonka jälkeen siitä voi kehittyä myyntiä.</span><span class="sxs-lookup"><span data-stu-id="31324-123">Turn an email exchange into a sales opportunity - If an entry looks promising, you can turn it into an opportunity and then manage its progress toward a sale.</span></span> <span data-ttu-id="31324-124">Valitse ensin tapahtuma ja valitse sitten **Luo mahdollisuus**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="31324-124">To do that, choose the entry, and then choose the **Create Opportunity** action.</span></span> <span data-ttu-id="31324-125">Lisätietoja on kohdassa [Myyntimahdollisuuksien hallinta](marketing-manage-sales-opportunities.md).</span><span class="sxs-lookup"><span data-stu-id="31324-125">For more information, see [Managing Sales Opportunities](marketing-manage-sales-opportunities.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="31324-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="31324-126">See Also</span></span>
[<span data-ttu-id="31324-127">Kontaktienhallinta</span><span class="sxs-lookup"><span data-stu-id="31324-127">Managing Relationships</span></span>](marketing-relationship-management.md)

