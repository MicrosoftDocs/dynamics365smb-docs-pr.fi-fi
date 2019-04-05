---
title: Siirron tulokset | Microsoft Docs
description: Tässä ohjeaiheessa käsitellään mitä tapahtuu, kun pääkirjanpidon tapahtumat siirretään kustannustapahtumiin.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 0e17ff5ad60014cba6ce866c9ddae848b1239167
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795830"
---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="f332e-103">Tulokset siirrettäessä pääkirjanpidon tapahtumat kustannustapahtumiin</span><span class="sxs-lookup"><span data-stu-id="f332e-103">Results of Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="f332e-104">Kun pääkirjanpidon tapahtumia siirretään kustannustapahtumiin, [!INCLUDE[d365fin](includes/d365fin_md.md)] luo yhteyksiä tapahtumiin **KP-tapahtuma**-, **Kustannustapahtuma**- ja **Kustannusrekisteri**-taulukossa. Tämä mahdollistaa pääkirjanpidon tapahtumien ja kustannustapahtumien välisten yhteyksien jäljittämisen.</span><span class="sxs-lookup"><span data-stu-id="f332e-104">During the transfer of general ledger entries to cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates connections in the entries in the **G/L Entry** table, the **Cost Entry** table, and the **Cost Register** table to make it possible to trace the connections between cost entries and general ledger entries.</span></span>  

## <a name="general-ledger-entries"></a><span data-ttu-id="f332e-105">Pääkirjanpidon tapahtumat</span><span class="sxs-lookup"><span data-stu-id="f332e-105">General Ledger Entries</span></span>  
<span data-ttu-id="f332e-106">[!INCLUDE[d365fin](includes/d365fin_md.md)] täyttää kaikkien kustannuslaskentaan siirrettävien pääkirjanpidon tapahtumien kustannusten **Tapahtumanro**-kentän.</span><span class="sxs-lookup"><span data-stu-id="f332e-106">For each general ledger entry that is transferred to cost accounting, [!INCLUDE[d365fin](includes/d365fin_md.md)] fills the cost **Entry No.** field.</span></span>  

## <a name="cost-entries"></a><span data-ttu-id="f332e-107">Kustannustapahtumat</span><span class="sxs-lookup"><span data-stu-id="f332e-107">Cost Entries</span></span>  
<span data-ttu-id="f332e-108">[!INCLUDE[d365fin](includes/d365fin_md.md)] tallentaa vastaavan pääkirjanpidon tapahtuman jokaisen kustannustapahtuman numeron **Kustannustapahtuma**-ikkunan **KP-tapahtuman nro** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f332e-108">For each cost entry, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the corresponding general ledger entry in the **G/L Entry No.** field in the **Cost Entry** table.</span></span>  

<span data-ttu-id="f332e-109">[!INCLUDE[d365fin](includes/d365fin_md.md)] tallentaa yhdistettyjen kustannustapahtumien pääkirjanpidon viimeisen tapahtuman tapahtumanumeron (tapahtuma, jonka numero on kaikkein suurin).</span><span class="sxs-lookup"><span data-stu-id="f332e-109">For combined cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the last general ledger entry, which is the entry with the highest entry number.</span></span>  

<span data-ttu-id="f332e-110">**Kustannustapahtuma**-taulukon **KP-tili**-kentässä on KP-tilin numero, jolta kustannustapahtuma on peräisin.</span><span class="sxs-lookup"><span data-stu-id="f332e-110">The **G/L Account** field in the **Cost Entry** table contains the number of the general ledger account that the cost entry came from.</span></span>  

<span data-ttu-id="f332e-111">[!INCLUDE[d365fin](includes/d365fin_md.md)] siirtää yksittäisten kustannustapahtumien kirjaustekstin pääkirjanpidon tapahtumasta **Kuvaus**-tekstikenttään.</span><span class="sxs-lookup"><span data-stu-id="f332e-111">For single cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfers the posting text from the general ledger entry to the **Description** text field.</span></span> <span data-ttu-id="f332e-112">Tekstikenttä osoittaa, että yhdistetyt tapahtumat siirretään yhdistettyinä tapahtumina.</span><span class="sxs-lookup"><span data-stu-id="f332e-112">For combined entries, the text field shows these entries are transferred as combined entries.</span></span> <span data-ttu-id="f332e-113">Esimerkiksi vuoden 2013 lokakuun yhdistetyn tapahtuman teksti voi olla **Yhdistetyt tapahtumat, lokakuu 2013**.</span><span class="sxs-lookup"><span data-stu-id="f332e-113">For example, for a combined entry for the month of October in 2013, the text can be **Combined Entries, October 2013**.</span></span>  

## <a name="cost-register"></a><span data-ttu-id="f332e-114">Kustannusrekisteri</span><span class="sxs-lookup"><span data-stu-id="f332e-114">Cost Register</span></span>  
<span data-ttu-id="f332e-115">**Kustannusrekisteri**-taulukkoon [!INCLUDE[d365fin](includes/d365fin_md.md)] luo merkinnän lähteen siirtämisestä pääkirjanpidosta.</span><span class="sxs-lookup"><span data-stu-id="f332e-115">In the **Cost Register** table, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates an entry with the source transfer from general ledger.</span></span> <span data-ttu-id="f332e-116">Tapahtuma kirjaa siirrettyjen pääkirjanpidon tapahtumien ensimmäisen ja viimeisen tapahtumanumeron sekä luotujen kustannustapahtumien ensimmäisen ja viimeisen tapahtumanumeron.</span><span class="sxs-lookup"><span data-stu-id="f332e-116">The entry records the first and last entry numbers of the general ledger entries that are transferred, in addition to the first and last entry numbers of the cost entries that are created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f332e-117">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f332e-117">See Also</span></span>  
[<span data-ttu-id="f332e-118">Kustannustapahtumien siirtäminen ja kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="f332e-118">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)   
