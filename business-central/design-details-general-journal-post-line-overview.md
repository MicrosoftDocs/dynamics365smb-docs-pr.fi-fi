---
title: "Yleisen päiväkirjarivin yleiskuvaus | Microsoft Docs"
description: "Tässä ohjeaiheessa esitellään koodiyksikköön 12, **Yleinen päiväkirja - rivin kirjaus**, tehdyt muutokset. Se on pääkirjanpidon kirjauksen tärkeä sovellusobjekti ja ainoa paikka, jossa lisätään pääkirja-, ALV-, asiakas- ja toimittajatapahtumia."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2667b5d6d11172736a5dd6c3f7c810d42e3f2501
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="general-journal-post-line-overview"></a><span data-ttu-id="7902c-103">Yleisen päiväkirjan kirjausrivin yleiskuva</span><span class="sxs-lookup"><span data-stu-id="7902c-103">General Journal Post Line Overview</span></span>
<span data-ttu-id="7902c-104">Koodiyksikkö 12, **Yleinen päiväkirja - rivin kirjaus**, on pääkirjanpidon kirjauksen tärkeä sovellusobjekti ja ainoa paikka, jossa lisätään pääkirja-, ALV- sekä asiakkaan ja toimittajan reskontratapahtumia.</span><span class="sxs-lookup"><span data-stu-id="7902c-104">Codeunit 12, **Gen. Jnl.-Post Line**, is the major application object for general ledger posting and is the only place to insert general ledger, VAT, and customer and vendor ledger entries.</span></span> <span data-ttu-id="7902c-105">Tätä koodiyksikköä käytetään myös Käytä-, Peruuta kohdistus- ja Peruuta-toiminnoissa.</span><span class="sxs-lookup"><span data-stu-id="7902c-105">This codeunit is also used for all Apply, Unapply and Reverse operations.</span></span>  
  
<span data-ttu-id="7902c-106">Vaikka koodiyksikköä on parannettu jokaisessa versiossa yli kymmenen vuoden ajan, sen arkkitehtuuri on pysynyt olennaisilta osiltaan samana.</span><span class="sxs-lookup"><span data-stu-id="7902c-106">While the codeunit has been improved in each release over the last ten years, its architecture remained essentially unchanged.</span></span> <span data-ttu-id="7902c-107">Koodiyksiköstä tuli suuri noin 7 600 rivien kanssa.</span><span class="sxs-lookup"><span data-stu-id="7902c-107">The codeunit became very large, with approximately 7,600 code lines.</span></span> <span data-ttu-id="7902c-108">Tässä [!INCLUDE[d365fin](includes/d365fin_md.md)] -versiossa arkkitehtuuria on muutettu ja koodiyksiköstä on tehty yksinkertaisempi ja ylläpidettävämpi.</span><span class="sxs-lookup"><span data-stu-id="7902c-108">With this release of [!INCLUDE[d365fin](includes/d365fin_md.md)], the architecture is changed and the codeunit has been made simpler and more maintainable.</span></span> <span data-ttu-id="7902c-109">Tässä ohjeessa esitellään muutokset ja tiedot, joita tarvitset päivitystä varten.</span><span class="sxs-lookup"><span data-stu-id="7902c-109">This documentation introduces the changes and provides information that you will need for upgrade.</span></span>  
  
## <a name="old-architecture"></a><span data-ttu-id="7902c-110">Vanha arkkitehtuuri</span><span class="sxs-lookup"><span data-stu-id="7902c-110">Old Architecture</span></span>  
<span data-ttu-id="7902c-111">Vanhassa arkkitehtuurissa oli seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="7902c-111">The old architecture had the following features:</span></span>  
  
* <span data-ttu-id="7902c-112">Yleisten muuttujien käyttö oli laajaa, mikä lisäsi piilotettujen virheiden mahdollisuutta, jos muuttujia käytettiin väärässä laajuudessa.</span><span class="sxs-lookup"><span data-stu-id="7902c-112">There was extensive use of global variables, which increased the possibility of hidden errors due to use of variables with the wrong scope.</span></span>  
* <span data-ttu-id="7902c-113">Moni proseduuri oli pitkä (yli 100 riviä), mikä lisäsi myös ns. Cyclomatic Complexityn suuruutta (paljon CASE, REPEAT, IF -lauseita) ja teki koodista erittäin vaikean lukea ja ylläpitää.</span><span class="sxs-lookup"><span data-stu-id="7902c-113">There were many long procedures (with more than 100 code lines) that also had high cyclomatic complexity (that is, a lot of CASE, REPEAT, IF nested statements), which made the code very difficult to read and maintain.</span></span>  
* <span data-ttu-id="7902c-114">Useita proseduureja, joita käytettiin vain paikallisesti ja jotka oli tarkoitettu vain paikallisesti käytettäviksi, ei ollut merkitty paikallisiksi.</span><span class="sxs-lookup"><span data-stu-id="7902c-114">Several procedures that were only used locally and were only meant to be used locally were not marked as local.</span></span>  
* <span data-ttu-id="7902c-115">Suurimmalla osalla proseduureista ei ole parametreja eikä käytettyjä yleisiä muuttujia.</span><span class="sxs-lookup"><span data-stu-id="7902c-115">Most procedures had no parameters and used global variables.</span></span> <span data-ttu-id="7902c-116">Osa käytti parametreja ja korvasi yleisiä muuttujia paikallisilla.</span><span class="sxs-lookup"><span data-stu-id="7902c-116">Some used parameters and overrode global variables with locals.</span></span>  
* <span data-ttu-id="7902c-117">Kirjanpitotilien hakujen koodikuvioita ja kirjanpito- ja ALV-tapahtumien luontia ei ole standardoitu ja ne vaihtelevat paikasta toiseen.</span><span class="sxs-lookup"><span data-stu-id="7902c-117">Code patterns for searching the general ledger accounts and creating general ledger and VAT entries was not standardized and varied from place to place.</span></span> <span data-ttu-id="7902c-118">Lisäksi oli paljon päällekkäisiä koodeja sekä asiakas- ja toimittajakoodien välisiä symmetriakatkoksia.</span><span class="sxs-lookup"><span data-stu-id="7902c-118">In addition, there was a lot of code duplication and broken symmetry between customer and vendor code.</span></span>  
* <span data-ttu-id="7902c-119">Suuri osa koodiyksikön 12 koodista, noin 30 prosenttia, liittyy maksualennus- ja toleranssilaskelmiin, vaikka useissa maissa tai alueilla näitä ominaisuuksia ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="7902c-119">A large part of the code in codeunit 12, approximately 30 percent, related to payment discount and tolerance calculations, although these features are not needed in many countries or regions.</span></span>  
* <span data-ttu-id="7902c-120">Kirjaus, kohdista, peruuta kohdistus, peruuta, maksualennus ja toleranssi sekä vaihtokurssin muutos on liitetty yhteen koodiyksikössä 12 yleisten muuttujien pitkää listaa käyttäen.</span><span class="sxs-lookup"><span data-stu-id="7902c-120">Posting, Apply, Unapply, Reverse, Payment Discount and Tolerance, and Exchange Rate Adjustment were married together in codeunit 12 using a long list of global variables.</span></span>  
  
### <a name="new-architecture"></a><span data-ttu-id="7902c-121">Uusi arkkitehtuuri</span><span class="sxs-lookup"><span data-stu-id="7902c-121">New Architecture</span></span>  
<span data-ttu-id="7902c-122">[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa koodiyksikkö 12 on saanut seuraavia parannuksia:</span><span class="sxs-lookup"><span data-stu-id="7902c-122">In [!INCLUDE[d365fin](includes/d365fin_md.md)], codeunit 12 has had the following improvements:</span></span>  
  
* <span data-ttu-id="7902c-123">Koodiyksikkö 12 on jaettu pienempiin osiin (kaikissa alle 100 koodiriviä).</span><span class="sxs-lookup"><span data-stu-id="7902c-123">Codeunit 12 has been refactored into smaller procedures (all less than 100 code lines).</span></span>  
* <span data-ttu-id="7902c-124">Kirjanpitotilien hakujen vakiomallit on toteutettu käyttämällä kirjausryhmä-taulukoiden apufunktioita.</span><span class="sxs-lookup"><span data-stu-id="7902c-124">Standardized patterns for the search of general ledger accounts have been implemented by using helper functions from Posting Group tables.</span></span>  
* <span data-ttu-id="7902c-125">Kirjausohjelmakehys on toteutettu tapahtumien aloituksen ja lopetuksen hallintaan sekä eristämään luonti kirjanpidosta ja ALV-tapahtumista, ALV-muutosten keräämiseen ja lisävaluutan summien laskemista varten.</span><span class="sxs-lookup"><span data-stu-id="7902c-125">A Posting Engine Framework has been implemented to manage the start and finish of transactions and to isolate the creation to general ledger and VAT entries, the collection of VAT adjustment, and the calculation of additional currency amounts.</span></span>  
* <span data-ttu-id="7902c-126">Koodin kopiointi on poistettu.</span><span class="sxs-lookup"><span data-stu-id="7902c-126">Code duplication has been eliminated.</span></span>  
* <span data-ttu-id="7902c-127">Monet aputoiminnot on siirretty vastaaviin asiakkaan ja toimittajan tapahtumataulukoihin.</span><span class="sxs-lookup"><span data-stu-id="7902c-127">Many helper functions have been transferred to corresponding customer and vendor ledger entry tables.</span></span>  
* <span data-ttu-id="7902c-128">Yleisten muuttujien käyttö on minimoitu, jotta jokainen toimintosarja käyttää parametreja ja kapseloi oman sovelluslogiikkansa.</span><span class="sxs-lookup"><span data-stu-id="7902c-128">The use of global variables has been minimized, so that each procedure uses parameters and encapsulates its own application logic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7902c-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7902c-129">See Also</span></span>  
<span data-ttu-id="7902c-130">[Rakenteen tiedot: Kirjausliittymän rakenne](design-details-posting-interface-structure.md) </span><span class="sxs-lookup"><span data-stu-id="7902c-130">[Design Details: Posting Interface Structure](design-details-posting-interface-structure.md) </span></span>  
[<span data-ttu-id="7902c-131">Rakenteen tiedot: Kirjausohjelman rakenne</span><span class="sxs-lookup"><span data-stu-id="7902c-131">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)

