---
title: Prosessien suorittamiseen tarvittavat pakolliset kentät | Microsoft Docs
description: Tutustu punaisella tähtimerkillä merkittyihin kenttien. Tämä merkintä osoittaa, että ne ovat pakollisia ja ne on täytettävä, jotta prosessit voidaan suorittaa.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: 386025d90301f780f8bf5927de495658a100825f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775273"
---
# <a name="detecting-mandatory-fields"></a><span data-ttu-id="fa95a-103">Pakollisten kenttien havaitseminen</span><span class="sxs-lookup"><span data-stu-id="fa95a-103">Detecting Mandatory Fields</span></span>
<span data-ttu-id="fa95a-104">Kun annat tietoja [!INCLUDE[prod_short](includes/prod_short.md)]in sivuilla, tietyt kentät on merkitty punaisella tähdellä.</span><span class="sxs-lookup"><span data-stu-id="fa95a-104">When you enter data on pages in [!INCLUDE[prod_short](includes/prod_short.md)], certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="fa95a-105">Punainen tähti tarkoittaa, että kenttä on täytettävä, jotta tietty kenttää käyttävä prosessi voidaan suorittaa, kuten kentässä olevaa arvoa käyttävän tapahtuman kirjaus.</span><span class="sxs-lookup"><span data-stu-id="fa95a-105">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>

<span data-ttu-id="fa95a-106">Vaikka kentässä on punainen tähti, et joudu täyttämään kenttää ennen kuin jatkat muihin kenttiin tai suljet sivun.</span><span class="sxs-lookup"><span data-stu-id="fa95a-106">Even though the field contains a red asterisk, you are not forced to fill in the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="fa95a-107">Punainen tähti toimii vain muistutuksena siitä, että sinua estetään suorittamasta tiettyä prosessia.</span><span class="sxs-lookup"><span data-stu-id="fa95a-107">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>

## <a name="examples"></a><span data-ttu-id="fa95a-108">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="fa95a-108">Examples</span></span>
<span data-ttu-id="fa95a-109">**Asiakkaan kortti** -sivulla näkyy punainen tähti **Veroaluekoodi**-kentän **Nimi**-kentässä ja kolme kirjauksen ryhmäkenttää, jotka ilmaisevat, että et voi kirjata myyntitapahtumia asiakkaalle, ellei kenttiä täytetä.</span><span class="sxs-lookup"><span data-stu-id="fa95a-109">On the **Customer Card** page, the red asterisk appears in the **Name** field, in the **Tax Area Code** field, and in the posting group fields to indicate that you cannot post a sales transaction for the customer unless the fields are filled.</span></span>

<span data-ttu-id="fa95a-110">**Nimikkeen kortti** -sivun **Kuvaus**-kentässä näkyvä punainen tähti osoittaa sen, että et voi kirjoittaa nimikettä asiakirjariville, kuten myyntitilaukseen, jos tätä kenttää ole täytetty.</span><span class="sxs-lookup"><span data-stu-id="fa95a-110">On the **Item Card** page, the red asterisk appears in the **Description** field to indicate that you cannot enter the item on a document line, such as a sales order, unless this field is filled.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa95a-111">Katso myös</span><span class="sxs-lookup"><span data-stu-id="fa95a-111">See Also</span></span>
<span data-ttu-id="fa95a-112">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fa95a-112">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]