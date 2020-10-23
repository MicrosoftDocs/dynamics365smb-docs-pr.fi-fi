---
title: Ostolaskujen selvittäminen viipymättä
description: Jos toimittajalle on maksettava käteisellä tai sekillä, tarvittava kirjaus voidaan tehdä laskua kirjattaessa.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: bac023393d95623a2731ef1b2ada7d30b135063b
ms.sourcegitcommit: 0fb6952376d853a878ed33257e73aadc03b95572
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/07/2020
ms.locfileid: "3968357"
---
# <a name="settle-purchase-invoices-promptly"></a>Ostolaskujen selvittäminen viipymättä

Jos toimittajalle on maksettava käteisellä tai sekillä, voit kirjata maksun kun kirjaat laskun.  

> [!NOTE]  
> Jos maksat ostolaskuja usein käteisellä, sekillä tai pankkisiirrolla, on hyvä idea perustaa tiettyjä maksutapoja joissa on vastatili ja syötä tämä metodi **Maksutapa** -kenttään toimittajakortille. Ohjelma automaattisesti syöttää vastatilin numeron ja laskuotsikon joka kerta kun luot uuden laskun. Lisätietoja on kohdassa [Maksutapojen määrittely](finance-payment-methods.md).  

## <a name="to-settle-purchase-invoices-promptly"></a>Ostolaskujen selvittäminen viipymättä

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Ostolaskut** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3. Jos haluat maksaa käteisellä tai pankkisiirrolla, annan kirjanpidon kassatilin tai pankkitilin numero **Vastatilin nro.** -kenttään.  

> [!IMPORTANT]  
> Kohde **Vasta tilin tyyppi** ja **Vasta. tilin nro.** -kenttiä ei sisällytetä vakiolaskun otsikkoon. Jotta voisit kirjata laskun maksun, sinun täytyy ottaa yhteyttä Microsoft-kumppaniin, joka voi lisätä kentät koodin avulla.  
>
> Tämä mukautus tarvitaan vain, jos et määritä vastatilejä maksutavoille yllä kuvatulla tavalla.

## <a name="see-also"></a>Katso myös

[Ostovelkojen hallinta](payables-manage-payables.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
