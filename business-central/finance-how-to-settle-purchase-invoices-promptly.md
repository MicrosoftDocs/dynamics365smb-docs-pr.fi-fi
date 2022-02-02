---
title: Ostolaskujen selvittäminen viipymättä
description: Jos toimittajalle on maksettava käteisellä tai sekillä, tarvittava kirjaus voidaan tehdä laskua kirjattaessa.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.form: 51, 9308
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: af1dea2cf7ac387f2e0dfa9c2965156768facc3a
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2022
ms.locfileid: "7973412"
---
# <a name="settle-purchase-invoices-promptly"></a>Ostolaskujen selvittäminen viipymättä

Jos toimittajalle on maksettava käteisellä tai sekillä, voit kirjata maksun kun kirjaat laskun.  

> [!NOTE]  
> Jos maksat ostolaskuja usein käteisellä, sekillä tai pankkisiirrolla, on hyvä idea perustaa tiettyjä maksutapoja joissa on vastatili ja syötä tämä metodi **Maksutapa** -kenttään toimittajakortille. Ohjelma automaattisesti syöttää vastatilin numeron ja laskuotsikon joka kerta kun luot uuden laskun. Lisätietoja on kohdassa [Maksutapojen määrittely](finance-payment-methods.md).  

## <a name="to-settle-purchase-invoices-promptly"></a>Ostolaskujen selvittäminen viipymättä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Jos haluat maksaa käteisellä tai pankkisiirrolla, annan kirjanpidon kassatilin tai pankkitilin numero **Vastatilin nro.** -kenttään.  

> [!IMPORTANT]  
> Kohde **Vasta tilin tyyppi** ja **Vasta. tilin nro.** -kenttiä ei sisällytetä vakiolaskun otsikkoon. Jotta voisit kirjata laskun maksun, sinun täytyy ottaa yhteyttä Microsoft-kumppaniin, joka voi lisätä kentät koodin avulla.  
>
> Tämä mukautus tarvitaan vain, jos et määritä vastatilejä maksutavoille yllä kuvatulla tavalla.

## <a name="see-also"></a>Katso myös

[Ostovelkojen hallinta](payables-manage-payables.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]