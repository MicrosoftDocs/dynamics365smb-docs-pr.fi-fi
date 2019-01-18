---
title: "Rakennetiedot – Nimikeseurannan saatavuus | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten voit varmistaa, että tilauksen käsittelevä henkilö voi luottaa sarja- tai eränumeroiden saatavuuteen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: fcdfc219f94462048474acdef259f671e1c8a402
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="design-details-item-tracking-availability"></a><span data-ttu-id="1ddb0-103">Rakennetiedot: Nimikkeen seurannan saatavuus</span><span class="sxs-lookup"><span data-stu-id="1ddb0-103">Design Details: Item Tracking Availability</span></span>
<span data-ttu-id="1ddb0-104">**Nimikkeen seurantarivit**- ja **Nimikeseurannan yhteenveto** -sivuilla on dynaamista saatavuustietoa sarja- tai eränumeroista.</span><span class="sxs-lookup"><span data-stu-id="1ddb0-104">The **Item Tracking Lines** and **Item Tracking Summary** pages provide dynamic availability information for serial or lot numbers.</span></span> <span data-ttu-id="1ddb0-105">Tämän tarkoituksena on kasvattaa käyttäjien läpinäkyvyyttä lähtevissä asiakirjoissa, kuten myyntitilaukset, näyttämälle heille, mitkä sarjanumerot tai kuinka monta yksikköä eränumeroita tällä hetkellä on kirjattuna toisiin avoimiin asiakirjoihin.</span><span class="sxs-lookup"><span data-stu-id="1ddb0-105">The purpose of this is to increase transparency for users on outbound documents, such as sales orders, by showing them which serial numbers or how many units of a lot number are currently assigned on other open documents.</span></span> <span data-ttu-id="1ddb0-106">Tämä poistaa kaksoiskohdistuksen aiheuttamaa epävarmuutta ja vahvistaa tilausten käsittelijöiden luottamusta siihen, että nimikkeen seurantanumerot ja kirjaamattomien myyntitilausten luvatut päivämäärät voidaan toteuttaa.</span><span class="sxs-lookup"><span data-stu-id="1ddb0-106">This reduces uncertainty that is caused by double allocation and instills confidence in order processors that the item tracking numbers and dates that they are promising on unposted sales orders can be fulfilled.</span></span> <span data-ttu-id="1ddb0-107">Katso lisätiedot kohdasta [Rakennetiedot: Nimikkeen seurantarivit -sivu](design-details-item-tracking-lines-window.md).</span><span class="sxs-lookup"><span data-stu-id="1ddb0-107">For more information, see [Design Details: Item Tracking Lines Page](design-details-item-tracking-lines-window.md).</span></span>  

<span data-ttu-id="1ddb0-108">Kun **Nimikkeen seurantarivit** -sivu avataan, saatavuustiedot haetaan **Nimiketapahtuma**- ja **Varaustapahtuma**-taulukosta ilman päivämääräsuodatinta.</span><span class="sxs-lookup"><span data-stu-id="1ddb0-108">When you open the **Item Tracking Lines** page, availability data is retrieved from the **Item Ledger Entry** table and the **Reservation Entry** table, with no date filter.</span></span> <span data-ttu-id="1ddb0-109">Kun valitset **Sarjanro**- tai **Eränro**-kentän, **Nimikeseurannan yhteenveto** -sivu avautuu. Sivulla näkyvät nimikkeen seurantatiedot **Varaustapahtuma**-taulukossa.</span><span class="sxs-lookup"><span data-stu-id="1ddb0-109">When you choose the **Serial No.** field or the **Lot No.** field, the **Item Tracking Summary** page opens and shows a summary of the item tracking information in the **Reservation Entry** table.</span></span> <span data-ttu-id="1ddb0-110">Tämä yhteenveto sisältää nimikkeen seurantarivin jokaisen sarja- tai eränumeron seurantatiedot.</span><span class="sxs-lookup"><span data-stu-id="1ddb0-110">The summary contains the following information about each serial or lot number on the item tracking line:</span></span>  

|<span data-ttu-id="1ddb0-111">Kenttä</span><span class="sxs-lookup"><span data-stu-id="1ddb0-111">Field</span></span>|<span data-ttu-id="1ddb0-112">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="1ddb0-112">Description</span></span>|  
|---------------------------------|---------------------------------------|  
|<span data-ttu-id="1ddb0-113">**Määrä yhteensä**</span><span class="sxs-lookup"><span data-stu-id="1ddb0-113">**Total Quantity**</span></span>|<span data-ttu-id="1ddb0-114">Varastossa tällä hetkellä oleva erä- tai sarjanumeron kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="1ddb0-114">The total quantity of the serial or lot number that is currently in inventory.</span></span>|  
|<span data-ttu-id="1ddb0-115">**Pyydetty määrä yhteensä**</span><span class="sxs-lookup"><span data-stu-id="1ddb0-115">**Total Requested Quantity**</span></span>|<span data-ttu-id="1ddb0-116">Tällä hetkellä kaikissa asiakirjoissa pyydettyjen erä- tai sarjanumeroiden kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="1ddb0-116">The total quantity of the serial or lot number that is currently requested in all documents.</span></span>|  
|<span data-ttu-id="1ddb0-117">**Nykyinen odottava määrä**</span><span class="sxs-lookup"><span data-stu-id="1ddb0-117">**Current Pending Quantity**</span></span>|<span data-ttu-id="1ddb0-118">Määrä, joka on kirjattu nykyiselle **Nimikkeenseurantarivit** -sivulle, mutta ei ole vielä lähetetty tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="1ddb0-118">The quantity that is entered in the current instance of the **Item Tracking Lines** page but is not yet committed to the database.</span></span>|  
|<span data-ttu-id="1ddb0-119">**Saatavilla oleva kokonaismäärä**</span><span class="sxs-lookup"><span data-stu-id="1ddb0-119">**Total Available Quantity**</span></span>|<span data-ttu-id="1ddb0-120">Sarja- tai eränumeron määrä, joka on käyttäjän käytettävissä pyynnöstä.</span><span class="sxs-lookup"><span data-stu-id="1ddb0-120">The quantity of the serial or lot number that is available for the user to request.</span></span><br /><br /> <span data-ttu-id="1ddb0-121">Määrä lasketaan sivun muiden kenttien avulla seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="1ddb0-121">This quantity is calculated from other fields on the page as follows:</span></span><br /><br /> <span data-ttu-id="1ddb0-122">kokonaismäärä – (pyydetty kokonaismäärä + nykyinen odottava määrä).</span><span class="sxs-lookup"><span data-stu-id="1ddb0-122">total quantity – (total requested quantity + current pending quantity).</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="1ddb0-123">Voit tarkastella edellisen taulukon tietoja käyttämällä **Valitse tapahtumat** -toimintoa **Nimikkeen seurantarivit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="1ddb0-123">You can also see the information in the preceding table by using the **Select Entries** function on the **Item Tracking Lines** page.</span></span>  

<span data-ttu-id="1ddb0-124">Saatavuustiedot haetaan tietokannasta vain kerran **Nimikkeen seurantarivit** -sivun avaamisen ja **Päivitä saatavuus** -toiminnon käyttämisen yhteydessä. Näin säilytetään tietokannan suorituskyky.</span><span class="sxs-lookup"><span data-stu-id="1ddb0-124">To preserve database performance, availability data is only retrieved once from the database when you open the **Item Tracking Lines** page and use the **Refresh Availability** function on the page.</span></span>  

## <a name="calculation-formula"></a><span data-ttu-id="1ddb0-125">Laskentakaava</span><span class="sxs-lookup"><span data-stu-id="1ddb0-125">Calculation Formula</span></span>  
<span data-ttu-id="1ddb0-126">Kuten edellisessä taulukossa selvittiin, määritetyn sarja- tai eränumeron saatavuus lasketaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="1ddb0-126">As described in the preceding table, the availability of a given serial or lot number is calculated as follows:</span></span>  

* <span data-ttu-id="1ddb0-127">saatavilla oleva kokonaismäärä = varastossa oleva määrä – (koko kysyntä + määrä, jota ei ole vielä siirretty tietokantaan)</span><span class="sxs-lookup"><span data-stu-id="1ddb0-127">total available quantity = quantity in inventory – (all demands + quantity not yet committed to the database)</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="1ddb0-128">Tämä kaava osoittaa, että sarja- tai eränumeron saatavuuden laskenta ottaa huomioon vain varaston, ei suunniteltuja vastaanottoja.</span><span class="sxs-lookup"><span data-stu-id="1ddb0-128">This formula implies that the serial or lot number availability calculation considers only inventory and ignores projected receipts.</span></span> <span data-ttu-id="1ddb0-129">Näin ollen tarjonta, jota ei ole vielä kirjattu varastoon, ei vaikuta nimikkeen seurannan saatavuuteen, toisin kuin tavallinen nimikkeen saatavuudessa, johon sisällytetään suunnitellut vastaanotot.</span><span class="sxs-lookup"><span data-stu-id="1ddb0-129">Accordingly, supply that is not yet posted to inventory does not affect item tracking availability, as opposed to regular item availability where projected receipts are included.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1ddb0-130">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1ddb0-130">See Also</span></span>  
[<span data-ttu-id="1ddb0-131">Rakennetiedot: nimikkeen seuranta</span><span class="sxs-lookup"><span data-stu-id="1ddb0-131">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)

