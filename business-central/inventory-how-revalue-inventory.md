---
title: Luo uusia arvotapahtumia varastossa oleville nimikkeille| Microsoft-asiakirjat
description: 'Tässä ohjeaiheessa kerrotaan, miten vähintään yhden varaston nimikkeen arvotapahtumaa nostetaan tai lasketaan kirjaamalla nimikkeen nykyinen laskettu arvo.'
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'costing, inventory cost, value entries'
ms.search.forms: '5803,'
ms.date: 07/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Varaston uudelleenarvostaminen
Jos haluat nostaa tai laskea nimikkeen tai tietyn nimiketapahtuman varastoarvoa, sinun tulee käyttää uudelleenarvostuspäiväkirjaa.

## Varaston uudelleenarvostus
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Uud.arviointipvk.** ja valitse sitten vastaava linkki.
2. Valitse **Laske varaston arvo** -toiminto.
3. Täytä **Laske varaston arvo** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **OK**-painike.
5. Syötä uusi yksikkökustannus **Nimikkeen uudelleenarvostuspäiväkirjat** -sivun **kunkin rivin Yksikkökustannus (uudelleenarvostet.)**  -kenttään. Vaihtoehtoisesti voit syöttää uuden kokonaissumman **Var. arvo (uudell.arvostettu)** -kenttään.

    Asianmukaiset kentät päivitetään automaattisesti.  **Summa-kentässä** näkyy varaston arvon todellinen muutos valitun nimiketapahtuman osalta. Ohjelma laskee **Varaston arvo (laskettu)** -kentän ja **Var. arvo (uudell.arvostettu)** -kentän erotuksen.
6. Kun olet saanut kaikki uudelleenarvostuspäiväkirjan rivit valmiiksi, valitse **Kirjaa**-toiminto.

Kirjaamiasi uudelleenarvostuksia vastaavat uudet arvotapahtumat on nyt luotu. Uudet arvot näkyvät vastaavissa nimikekorteissa.

## Katso myös
[Suunnittelun yksityiskohdat: Uudelleenarvostus](design-details-revaluation.md)    
[Vaihto-omaisuus](inventory-manage-inventory.md)    
[Myynti](sales-manage-sales.md)    
[Osto](purchasing-manage-purchasing.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]