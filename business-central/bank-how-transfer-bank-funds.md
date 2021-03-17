---
title: Pankkivarojen siirtäminen| Microsoft Docs
description: Voit siirtää summia pankkitililtä toisille myös muissa valuutoissa kirjaamalla tapahtuman yleiseen päiväkirjaan.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1a0ab7c2a96c278740c07ff243ad785be1d72dd4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388097"
---
# <a name="transfer-bank-funds"></a>Siirrä pankkivarat
Joskus on siirrettävä varoja yhdeltä pankkitililtä kohteessa [!INCLUDE[prod_short](includes/prod_short.md)] toiselle. Se tehdään kirjaamalla tapahtuma **Yleinen päiväkirja** -sivulla. Tehtävä vaihtelee sen mukaan, käytetäänkö pankkitileillä samaa vai eri valuuttaa.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Siirtojen kirjaaminen pankkitileillä, jotka käyttävät samaa valuuttakoodia
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleinen päiväkirja** ja valitse sitten liittyvä linkki.
2. Täytä päiväkirjan rivillä **Kirjauspvm**- ja **Asiakirjan nro** -kentät.
3. Valitse **Tilityyppi**-kentässä **Pankkitili**.
4. Valitse **Tilinro**-kentässä pankkitili, josta haluat siirtää varat.
5. Syötä siirrettävä summa **Summa**-kenttään.
6. Näytä kaikki käytettävissä olevat kentät valitsemalla **Näytä enemmän sarakkeita** -toiminto.
7. Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.
8. Valitse **Vastatilin nro**-kentässä pankkitili, johon haluat siirtää varat.
9. Kirjaa päiväkirja.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Siirtojen kirjaaminen pankkitileillä, joilla on eri valuuttakoodit
Voit siirtää varoja eri valuuttoja käyttävien pankkitilien välillä kirjaamalla kaksi yleisen päiväkirjan riviä.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleinen päiväkirja** ja valitse sitten liittyvä linkki.
2. Luo kaksi päiväkirjan riviä ja täytä **Kirjauspvm**- ja **Asiakirjan nro.** -kentät.
3. Valitse **Tyyppi**-kentän ensimmäisellä rivillä **Pankkitili**.
4. Valitse **Tilinro**-kentässä pankkitili, josta haluat siirtää varat.
5. Syötä **Summa**-kenttään summa pankkitilin valuuttana. Anna kredit-summat miinusmerkkisinä. Anna debet-summat ilman miinusmerkkiä.
6. Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.
7. Valitse **Vastatilin nro**-kentässä pankkitili, johon haluat siirtää varat.
8. Valitse **Tyyppi**-kentän toisella rivillä **Pankkitili**.
9. Valitse **Tilinro**-kentässä pankkitili, johon haluat siirtää varat.
10. Syötä **Summa**-kenttään summa pankkitilin valuuttana. Anna kredit-summat miinusmerkkisinä. Anna debet-summat ilman miinusmerkkiä.
11. Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.  
12. Valitse **Vastatilin nro**-kentässä pankkitili, josta haluat siirtää varat.

    > [!NOTE]  
    > Jos päiväkirjassa käytetyt vaihtokurssit eroavat **Valuutan vaihtokurssit** -sivun kursseista, syötä kolmas rivi vaihtokurssivoittoa tai -tappiota varten. Valitse **KP-tili**-kentässä **Pankkitili**. Syötä **Tilinro**-kenttään valuuttakurssivoittojen ja -tappioiden KP-tilin numero. Syötä valuuttakurssivoitto tai -tappio **Summa**-kenttään. Syötä summa miinusmerkin kanssa, jos kyseessä on kredit, ja ilman miinusmerkkiä, jos kyseessä on debet.
13. Kirjaa päiväkirja.

## <a name="see-also"></a>Katso myös
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]