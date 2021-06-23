---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 59376b96dcd6f755040b07784ceca53e157bcf14
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115942"
---
<span data-ttu-id="48fe6-101">Ostoasiakirjoissa ja päiväkirjoissa voit määrittää asiakirjanumeron, joka viittaa toimittajan numerointijärjestelmään.</span><span class="sxs-lookup"><span data-stu-id="48fe6-101">On purchase documents and journals, you can specify a document number that refers to the vendor's numbering system.</span></span> <span data-ttu-id="48fe6-102">Tämän kentän avulla voit tallentaa numeron, jonka toimittaja on määrittänyt tilaukselle, laskulle tai hyvityslaskulle.</span><span class="sxs-lookup"><span data-stu-id="48fe6-102">Use this field to record the number that the vendor assigned to the order, invoice, or credit memo.</span></span> <span data-ttu-id="48fe6-103">Tätä numeroa voi käyttää myöhemmin, jos sinun tarvitsee etsiä kirjattua merkintää tätä numeroa käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="48fe6-103">You can then use the number later if, for some reason, you need to search for the posted entry using this number.</span></span>

<span data-ttu-id="48fe6-104">**Ulkois. asiakirjan nro pakoll.** -kenttä **Ostojen ja ostovelkojen asetukset** -sivulla määrittää, onko ulkoisen asiakirjan numeron syöttäminen seuraavissa tilanteissa pakollista:</span><span class="sxs-lookup"><span data-stu-id="48fe6-104">The **Ext. Doc. No. Mandatory** field in the **Purchases & Payables Setup** page specifies whether it is mandatory to enter an external document number in the following situations:</span></span>

* <span data-ttu-id="48fe6-105">**Toimittajan laskunro** -kentässä **Toimittajan tilausnro**</span><span class="sxs-lookup"><span data-stu-id="48fe6-105">In the **Vendor Invoice No.** field, **Vendor Order No.**</span></span> <span data-ttu-id="48fe6-106">kenttä tai **Toimittajan hyvityslaskunro**</span><span class="sxs-lookup"><span data-stu-id="48fe6-106">field, or the **Vendor Cr. Memo No.**</span></span> <span data-ttu-id="48fe6-107">kenttä ostojen tunnistetiedoissa</span><span class="sxs-lookup"><span data-stu-id="48fe6-107">field on a purchase header</span></span>

* <span data-ttu-id="48fe6-108">Yleisen päiväkirjan rivin **Ulkoisen asiakirjan nro** -kentässä, jossa **Asiakirjatyyppi**-kenttä on *Lasku*, *Hyvityslasku* tai *Viivästyskulu* ja **Tilityyppi** -kenttä on *Toimittaja*.</span><span class="sxs-lookup"><span data-stu-id="48fe6-108">In the **External Document No.** field on a general journal line, where the **Document Type** field is set to *Invoice*, *Credit Memo*, or *Finance Charge Memo*, and the **Account Type** field is set to *Vendor*.</span></span>

<span data-ttu-id="48fe6-109">Jos valitset kentän, laskua, hyvityslaskua tai aiemmin kuvattua yleisen päiväkirjan rivin tyyppiä ei voi kirjata ilman ulkoisen asiakirjan numeroa.</span><span class="sxs-lookup"><span data-stu-id="48fe6-109">If you select this field, it will not be possible to post an invoice, a credit memo, or the type of general journal line described above without an external document number.</span></span>

<span data-ttu-id="48fe6-110">Ulkoisen asiakirjan numero sisältyy kirjattuihin asiakirjoihin, joista voit hakea asianomaisen numeron perusteella.</span><span class="sxs-lookup"><span data-stu-id="48fe6-110">The external document number is included in posted documents where you can search by the relevant number.</span></span> <span data-ttu-id="48fe6-111">Voit myös etsiä käyttämällä ulkoisen asiakirjan numeroa, kun navigoit toimittajatapahtumien merkinnöissä.</span><span class="sxs-lookup"><span data-stu-id="48fe6-111">You can also search using the external document number when navigating on vendor ledger entries.</span></span>

<span data-ttu-id="48fe6-112">Ulkoisen asiakirjan numeroita voi käsitellä myös käyttämällä **Viitteenne**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="48fe6-112">A different way to handle external document numbers is to use the **Your Reference** field.</span></span> <span data-ttu-id="48fe6-113">Jos käytät **Viitteenne**-kenttää, numero sisällytetään kirjattuihin asiakirjoihin, ja voit hakea sen mukaan samalla tavalla kuin haet arvoja **Ulkoisen asiakirjan nro** -kentistä.</span><span class="sxs-lookup"><span data-stu-id="48fe6-113">If you use the **Your Reference** field, the number will be included in posted documents, and you can search by it in the same way as for values from **External Document No.** fields.</span></span> <span data-ttu-id="48fe6-114">Kenttä ei ole kuitenkaan käytettävissä päiväkirjan riveillä.</span><span class="sxs-lookup"><span data-stu-id="48fe6-114">But the field is not available on journal lines.</span></span>
