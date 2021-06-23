---
title: Yleisen päiväkirjarivin yleiskuvaus | Microsoft Docs
description: Tässä ohjeaiheessa esitellään codeunitön 12, **Yleinen päiväkirja - rivin kirjaus**, tehdyt muutokset. Se on pääkirjanpidon kirjauksen tärkeä sovellusobjekti ja ainoa paikka, jossa lisätään pääkirja-, ALV-, asiakas- ja toimittajatapahtumia.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 1f6060eb7672b332fb570eb13fe027a3b58e6594
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215251"
---
# <a name="general-journal-post-line-overview"></a><span data-ttu-id="59774-103">Yleisen päiväkirjan kirjausrivin yleiskuva</span><span class="sxs-lookup"><span data-stu-id="59774-103">General Journal Post Line Overview</span></span>

<span data-ttu-id="59774-104">Codeunit 12, **Yleinen päiväkirja - rivin kirjaus**, on pääkirjanpidon kirjauksen tärkeä sovellusobjekti ja ainoa paikka, jossa lisätään pääkirja-, ALV- sekä asiakkaan ja toimittajan reskontratapahtumia.</span><span class="sxs-lookup"><span data-stu-id="59774-104">Codeunit 12, **Gen. Jnl.-Post Line**, is the major application object for general ledger posting and is the only place to insert general ledger, VAT, and customer and vendor ledger entries.</span></span> <span data-ttu-id="59774-105">Tätä codeunitia käytetään myös Käytä-, Peruuta kohdistus- ja Peruuta-toiminnoissa.</span><span class="sxs-lookup"><span data-stu-id="59774-105">This codeunit is also used for all Apply, Unapply and Reverse operations.</span></span>  
  
<span data-ttu-id="59774-106">Microsoft Dynamics NAV 2013 R2:n codeunit uusittiin, koska siitä oli tullut hyvin suuri, noin 7 600 koodiriviä.</span><span class="sxs-lookup"><span data-stu-id="59774-106">In Microsoft Dynamics NAV 2013 R2, the codeunit was redesigned because it had become very large, with approximately 7,600 code lines.</span></span> <span data-ttu-id="59774-107">Arkkitehtuuri muutettiin ja codeunitista tehtiin yksinkertaisempi ja ylläpidettävämpi.</span><span class="sxs-lookup"><span data-stu-id="59774-107">The architecture was changed and the codeunit has been made simpler and more maintainable.</span></span> <span data-ttu-id="59774-108">Tässä ohjeessa kuvaillaan muutokset ja tiedot, joita tarvitset päivitystä varten.</span><span class="sxs-lookup"><span data-stu-id="59774-108">This documentation describes the changes and provides information that you will need for upgrade.</span></span>  
  
## <a name="old-architecture"></a><span data-ttu-id="59774-109">Vanha arkkitehtuuri</span><span class="sxs-lookup"><span data-stu-id="59774-109">Old Architecture</span></span>  
<span data-ttu-id="59774-110">Vanhassa arkkitehtuurissa oli seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="59774-110">The old architecture had the following features:</span></span>  
  
* <span data-ttu-id="59774-111">Yleisten muuttujien käyttö oli laajaa, mikä lisäsi piilotettujen virheiden mahdollisuutta, jos muuttujia käytettiin väärässä laajuudessa.</span><span class="sxs-lookup"><span data-stu-id="59774-111">There was extensive use of global variables, which increased the possibility of hidden errors due to use of variables with the wrong scope.</span></span>  
* <span data-ttu-id="59774-112">Moni proseduuri oli pitkä (yli 100 riviä), mikä lisäsi myös ns. Cyclomatic Complexityn suuruutta (paljon CASE, REPEAT, IF -lauseita) ja teki koodista erittäin vaikean lukea ja ylläpitää.</span><span class="sxs-lookup"><span data-stu-id="59774-112">There were many long procedures (with more than 100 code lines) that also had high cyclomatic complexity (that is, a lot of CASE, REPEAT, IF nested statements), which made the code very difficult to read and maintain.</span></span>  
* <span data-ttu-id="59774-113">Useita proseduureja, joita käytettiin vain paikallisesti ja jotka oli tarkoitettu vain paikallisesti käytettäviksi, ei ollut merkitty paikallisiksi.</span><span class="sxs-lookup"><span data-stu-id="59774-113">Several procedures that were only used locally and were only meant to be used locally were not marked as local.</span></span>  
* <span data-ttu-id="59774-114">Suurimmalla osalla proseduureista ei ole parametreja eikä käytettyjä yleisiä muuttujia.</span><span class="sxs-lookup"><span data-stu-id="59774-114">Most procedures had no parameters and used global variables.</span></span> <span data-ttu-id="59774-115">Osa käytti parametreja ja korvasi yleisiä muuttujia paikallisilla.</span><span class="sxs-lookup"><span data-stu-id="59774-115">Some used parameters and overrode global variables with locals.</span></span>  
* <span data-ttu-id="59774-116">Kirjanpitotilien hakujen koodikuvioita ja kirjanpito- ja ALV-tapahtumien luontia ei ole standardoitu ja ne vaihtelevat paikasta toiseen.</span><span class="sxs-lookup"><span data-stu-id="59774-116">Code patterns for searching the general ledger accounts and creating general ledger and VAT entries was not standardized and varied from place to place.</span></span> <span data-ttu-id="59774-117">Lisäksi oli paljon päällekkäisiä koodeja sekä asiakas- ja toimittajakoodien välisiä symmetriakatkoksia.</span><span class="sxs-lookup"><span data-stu-id="59774-117">In addition, there was a lot of code duplication and broken symmetry between customer and vendor code.</span></span>  
* <span data-ttu-id="59774-118">Suuri osa codeunitin 12 koodista, noin 30 prosenttia, liittyy maksualennus- ja toleranssilaskelmiin, vaikka useissa maissa tai alueilla näitä ominaisuuksia ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="59774-118">A large part of the code in codeunit 12, approximately 30 percent, related to payment discount and tolerance calculations, although these features are not needed in many countries or regions.</span></span>  
* <span data-ttu-id="59774-119">Kirjaus, kohdista, peruuta kohdistus, peruuta, maksualennus ja toleranssi sekä vaihtokurssin muutos on liitetty yhteen codeunitissa 12 yleisten muuttujien pitkää listaa käyttäen.</span><span class="sxs-lookup"><span data-stu-id="59774-119">Posting, Apply, Unapply, Reverse, Payment Discount and Tolerance, and Exchange Rate Adjustment were married together in codeunit 12 using a long list of global variables.</span></span>  
  
### <a name="new-architecture"></a><span data-ttu-id="59774-120">Uusi arkkitehtuuri</span><span class="sxs-lookup"><span data-stu-id="59774-120">New Architecture</span></span>  
<span data-ttu-id="59774-121">[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa codeunit 12 on saanut seuraavia parannuksia:</span><span class="sxs-lookup"><span data-stu-id="59774-121">In [!INCLUDE[prod_short](includes/prod_short.md)], codeunit 12 has had the following improvements:</span></span>  
  
* <span data-ttu-id="59774-122">Codeunit 12 on jaettu pienempiin osiin (kaikissa alle 100 koodiriviä).</span><span class="sxs-lookup"><span data-stu-id="59774-122">Codeunit 12 has been refactored into smaller procedures (all less than 100 code lines).</span></span>  
* <span data-ttu-id="59774-123">Kirjanpitotilien hakujen vakiomallit on toteutettu käyttämällä kirjausryhmä-taulukoiden apufunktioita.</span><span class="sxs-lookup"><span data-stu-id="59774-123">Standardized patterns for the search of general ledger accounts have been implemented by using helper functions from Posting Group tables.</span></span>  
* <span data-ttu-id="59774-124">Kirjausohjelmakehys on toteutettu tapahtumien aloituksen ja lopetuksen hallintaan sekä eristämään luonti kirjanpidosta ja ALV-tapahtumista, ALV-muutosten keräämiseen ja lisävaluutan summien laskemista varten.</span><span class="sxs-lookup"><span data-stu-id="59774-124">A Posting Engine Framework has been implemented to manage the start and finish of transactions and to isolate the creation to general ledger and VAT entries, the collection of VAT adjustment, and the calculation of additional currency amounts.</span></span>  
* <span data-ttu-id="59774-125">Koodin kopiointi on poistettu.</span><span class="sxs-lookup"><span data-stu-id="59774-125">Code duplication has been eliminated.</span></span>  
* <span data-ttu-id="59774-126">Monet aputoiminnot on siirretty vastaaviin asiakkaan ja toimittajan tapahtumataulukoihin.</span><span class="sxs-lookup"><span data-stu-id="59774-126">Many helper functions have been transferred to corresponding customer and vendor ledger entry tables.</span></span>  
* <span data-ttu-id="59774-127">Yleisten muuttujien käyttö on minimoitu, jotta jokainen toimintosarja käyttää parametreja ja kapseloi oman sovelluslogiikkansa.</span><span class="sxs-lookup"><span data-stu-id="59774-127">The use of global variables has been minimized, so that each procedure uses parameters and encapsulates its own application logic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59774-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="59774-128">See Also</span></span>

[<span data-ttu-id="59774-129">Rakenteen tiedot: Kirjausliittymän rakenne</span><span class="sxs-lookup"><span data-stu-id="59774-129">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="59774-130">Rakenteen tiedot: Kirjausohjelman rakenne</span><span class="sxs-lookup"><span data-stu-id="59774-130">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="59774-131">Rakenteen tiedot: Yleisen päiväkirjan kirjausrivi (Dynamics NAV)</span><span class="sxs-lookup"><span data-stu-id="59774-131">Design Details: General Journal Post Line (Dynamics NAV)</span></span>](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]