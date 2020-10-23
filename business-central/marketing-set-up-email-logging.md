---
title: Sähköpostin lokiinkirjauksen määrittäminen | Microsoft Docs
description: Lisätietoja siitä, miten myyjien ja asiakkaiden sähköpostivuorovaikutukset voidaan muuttaa todellisiksi myyntimahdollisuuksiksi.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: f02e78e0b5c7d7f6d3c22cd12e37bdaf74f4b90f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923618"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><span data-ttu-id="ab8fc-103">Myyjien ja yhteyshenkilöiden välisten sähköpostiviestien seuraaminen</span><span class="sxs-lookup"><span data-stu-id="ab8fc-103">Track Email Message Exchanges Between Salespeople and Contacts</span></span>

<span data-ttu-id="ab8fc-104">Saat enemmän hyötyä myyjien ja olemassa olevien tai potentiaalisten asiakkaiden välisestä viestinnästä, jos seuraat sähköpostiviestejä ja muunnat ne toiminnallisiksi mahdollisuuksiksi.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-104">Get more out of the communications between salespeople and your existing or potential customers by tracking email exchanges, and then turning them into actionable opportunities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ab8fc-105">-sovellusta voi käyttää yhdessä Exchange Onlinen kanssa. Näin voit seurata saapuvia ja lähteviä viestejä.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-105">can work with Exchange Online to keep a log of the inbound and outbound messages.</span></span> <span data-ttu-id="ab8fc-106">Voit tarkastella ja analysoida kunkin viestin sisältöä **Vuorovaikutuslokin tapahtumat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-106">You can view and analyze the contents of each message on the **Interaction Log Entries** page.</span></span>

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a><span data-ttu-id="ab8fc-107">Yleisten kansioiden ja sääntöjen määrittäminen sähköpostin lokiinkirjausta Exchange Onlinessa</span><span class="sxs-lookup"><span data-stu-id="ab8fc-107">Set up Public Folders and Rules for Email Logging in Exchange Online</span></span>

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

<span data-ttu-id="ab8fc-108">Seuraavaksi [!INCLUDE[prodshort](includes/prodshort.md)] yhdistetään Exchange Onlineen.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-108">Next, you connect [!INCLUDE[prodshort](includes/prodshort.md)] with Exchange Online.</span></span>

## <a name="setting-up-d365fin-to-log-email-messages"></a><span data-ttu-id="ab8fc-109">Määritetään [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellus sähköpostiviestien kirjaamista varten</span><span class="sxs-lookup"><span data-stu-id="ab8fc-109">Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)] to Log Email Messages</span></span>

<span data-ttu-id="ab8fc-110">Aloita sähköpostien kirjaaminen seuraavien kahden helpon vaiheen avulla:</span><span class="sxs-lookup"><span data-stu-id="ab8fc-110">Get started with email logging in two easy steps:</span></span>

1. <span data-ttu-id="ab8fc-111">Muodosta yhteys [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellukseen Exchange Onlinen avulla Microsoft 365 -tilauksessa.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-111">Connect [!INCLUDE[d365fin](includes/d365fin_md.md)] with Exchange Online for your Microsoft 365 subscription.</span></span> <span data-ttu-id="ab8fc-112">Exchange Online käsittelee sähköpostiviestisi.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-112">Exchange Online handles your email messages.</span></span> <span data-ttu-id="ab8fc-113">Tämä on helppo tehdä asetusten ohjatun määrityksen oppaan avulla.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-113">We've made this step easy by providing an assisted setup guide.</span></span> <span data-ttu-id="ab8fc-114">Tarvitset vain järjestelmänvalvojan tunnistetiedot Microsoft 365:n järjestelmänvalvojan tiliä varten.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-114">You just need your administrator credentials for your administrator account in Microsoft 365.</span></span> <span data-ttu-id="ab8fc-115">Aloita oppaan käyttäminen siirtymällä **Asetusten ohjattu määritys** -kohtaan ja valitsemalla **Määritä sähköpostin lokiinkirjaus**.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-115">To start the guide, go to **Assisted Setup**, and then choose **Set up email logging**.</span></span>  

2. <span data-ttu-id="ab8fc-116">Varmista, että [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellukseen on määritetty oikeat sähköpostiosoitteet myyjille ja yhteyshenkilöille sen mukaan, ovatko he potentiaalisia vai olemassa olevia asiakkaita.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-116">Make sure that valid email addresses have been entered in [!INCLUDE[d365fin](includes/d365fin_md.md)] for your sales people and contacts, depending on whether they are potential or existing customers.</span></span> <span data-ttu-id="ab8fc-117">Tee tämä avaamalla kunkin asiakkaan tai myyjän **Yhteyshenkilö**- tai **Myyjä/ostaja**-kortti ja tarkistamalla **Sähköposti**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-117">To do that, for each customer or salesperson, open the **Contact** or **Salesperson/Purchaser** card and have a look in the **Email** field.</span></span>

> [!Tip]
> <span data-ttu-id="ab8fc-118">Kun olet tehnyt nämä oppaan vaiheet, voit tarkistaa yhteyden tilan.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-118">After you complete the steps in the guide you can check whether the connection was successful.</span></span> <span data-ttu-id="ab8fc-119">Siirry **Kontaktienhallinnan asetukset** -kohtaan, valitse **Prosessi** ja valitse sitten **Toiminnot**. Valitse lopuksi **Tarkista sähköpostin lokiinkirjauksen asetukset**.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-119">Search for **Marketing Setup**, choose **Process**, then **Functions**, and then **Validate Email Logging Setup**.</span></span>

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a><span data-ttu-id="ab8fc-120">Sähköpostiviestien tarkasteleminen vuorovaikutuslokissa</span><span class="sxs-lookup"><span data-stu-id="ab8fc-120">Viewing Email Message Exchanges in the Interaction Log</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ab8fc-121">luo **Vuorovaikutusloki**-sivulle tapahtuman aina, kun myyjä ja yhteyshenkilö lähettävät sähköpostiviestejä.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-121">creates an entry on the **Interaction Log** page each time a salesperson and a contact exchange an email message.</span></span> <span data-ttu-id="ab8fc-122">Voit tarkastella vuorovaikutuslokia avaamalla **Yhteyshenkilö**- tai **Myyjä/ostaja**-kortin ja valitsemalla sitten **Historia**- ja **Vuorovaikutuslokin tapahtumat** -kohdat.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-122">To view the interaction log, open the **Contact** or **Salesperson Purchaser** card for the person, and then choose **History**, and then choose **Interaction Log Entries**.</span></span> <span data-ttu-id="ab8fc-123">Lokin tapahtumille voi tehdä esimerkiksi seuraavia toimintoja:</span><span class="sxs-lookup"><span data-stu-id="ab8fc-123">There are a few things we can do with each entry in the log, for example:</span></span>

- <span data-ttu-id="ab8fc-124">Voit tarkastella sähköpostiviestin sisältöä valitsemalla **Näytä liitteet** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-124">View the content of the email message that was exchanged by clicking the **Show Attachments** action.</span></span>
- <span data-ttu-id="ab8fc-125">Voit muuttaa sähköpostiviestinnän myyntimahdollisuudeksi. Jos tapahtuma näyttää lupaavalta, voit muuttaa sen mahdollisuudeksi, jonka jälkeen siitä voi kehittyä myyntiä.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-125">Turn an email exchange into a sales opportunity - If an entry looks promising, you can turn it into an opportunity and then manage its progress toward a sale.</span></span> <span data-ttu-id="ab8fc-126">Valitse ensin tapahtuma ja valitse sitten **Luo mahdollisuus**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="ab8fc-126">To do that, choose the entry, and then choose the **Create Opportunity** action.</span></span> <span data-ttu-id="ab8fc-127">Lisätietoja on kohdassa [Myyntimahdollisuuksien hallinta](marketing-manage-sales-opportunities.md).</span><span class="sxs-lookup"><span data-stu-id="ab8fc-127">For more information, see [Managing Sales Opportunities](marketing-manage-sales-opportunities.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ab8fc-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ab8fc-128">See Also</span></span>
[<span data-ttu-id="ab8fc-129">Kontaktienhallinta</span><span class="sxs-lookup"><span data-stu-id="ab8fc-129">Managing Relationships</span></span>](marketing-relationship-management.md)

