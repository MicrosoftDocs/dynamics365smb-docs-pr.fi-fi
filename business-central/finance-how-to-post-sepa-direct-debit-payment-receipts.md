---
title: SEPA-suoraveloitusmaksujen kirjaaminen | Microsoft Docs
description: Kun pankki on käsitellyt onnistuneesti suoraveloitusperinnän, voit siirtyä kirjaamaan maksukuitit kyseiselle myyntilaskuille.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: c75f68ddc4112c5956b175162687737464454c45
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302061"
---
# <a name="post-sepa-direct-debit-payment-receipts"></a>SEPA-suoraveloitusmaksujen kirjaaminen
Kun pankki on käsitellyt onnistuneesti suoraveloitusperinnän, voit siirtyä kirjaamaan maksukuitit kyseiselle myyntilaskuille. Lisätietoja on kohdassa [SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  

Voit kirjata suoraan maksun suoraan **Suoraveloitusperinnät**- tai **Suoraveloitusperintätapahtumat**-sivulta. Vaihtoehtoisesti voit siirtää työn toiselle käyttäjälle valmistelemalla siihen liittyvät päiväkirjarivit.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a>Suoraveloitusmaksukuitin kirjaaminen suoraveloitusperinnän sivulta  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Suoraveloitusperinnät** ja valitse sitten liittyvä linkki.  
2. Valitse rivi suoraveloitusperinnälle, joka on viety pankkitiedostoon ja jonka pankki on käsitellyt onnistuneesti. Lisätietoja on kohdassa [SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  
3. Valitse **Kirjaa maksukuitit** -toiminto.  
4. Täytä **Kirjaa suoraveloitusperintä**-sivun kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Suoraveloitusperinnän nro**|Määritä suoraveloitusperintä, johon haluat kirjata maksukuitin.|  
    |**Yleisen päiväkirjan malli**|Määritä, mitä yleisen päiväkirjan mallia käytit maksukuitin kirjaamiseen, kuten kassakuittien malli.|  
    |**Yleisen päiväkirjan erän nimi**|Määritä, mitä yleistä päiväkirjaerää käytit maksukuitin kirjaamiseen.|  
    |**Luo vain päiväkirja**|Merkitse tämä valintaruutu, jos et halua kirjata maksukuittia, kun valitset **OK**-painikkeen. Maksukuitti valmistellaan määritetyssä päiväkirjassa eikä sitä kirjata ennen kuin joku kirjaa kyseisen päiväkirjarivin.|  

5. Valitse **OK**-painike.  

## <a name="see-also"></a>Katso myös  
 [Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md)   
 [Myynti](sales-manage-sales.md)
