---
title: Kulutuksen eräkirjaus
description: Jos materiaalinottotapa on Manuaalinen, komponentit tulee kirjata manuaalisesti kulutuspäiväkirjaa käyttämällä.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000846, 99000850
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 09129dc65ad61e632d7b5f5e3d22b47ae32d95bd
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516716"
---
# <a name="batch-post-production-consumption"></a>Tuotannon kulutuksen eräkirjaus

Jos materiaalinottotapa on **Manuaalinen**, komponentit tulee kirjata manuaalisesti kulutuspäiväkirjaa käyttämällä.  

>[!NOTE]
> Jos olet lisännyt valintamerkin sijaintikortin **Vaadi poiminta** -kenttään osoittamaan, että sijainti vaatii varaston poimintakäsittelyä, sinun ei tarvitse käyttää tätä eräajoa. [!INCLUDE[prod_short](includes/prod_short.md)] käsittelee kulutusta, kun varaston poiminta kirjataan. Lisätietoja on kohdassa [Tuotantopoiminta perusvarastointimäärityksissä](warehouse-how-to-pick-for-production.md#pick-for-production-in-basic-warehouse-configurations).  

Voit myös määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in kirjaamaan (*materiaalioton*) komponentit automaattisesti, kun aloitat tai päätät tuotantotilauksia. Lisätietoja on kohdassa [Komponenttien materiaalinoton ottaminen käyttöön toiminnan tuotoksen mukaan](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Vähintään yhden tuotantotilausrivin kulutuksen kirjaaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kulutuspäiväkirja** ja valitse sitten vastaava linkki.  
2. Täytä kentät tuotantotilauksen tiedoilla ja kulutustiedoilla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Käytä **Laskenta perustuu** -toimintoa luomaan päiväkirjarivejä tuotantotilauksista todellisen tuotoksen (raportoitujen, valmiiden tavaroiden määrän) vai oletetun tuotoksen (valmiiden tavaroiden määrän, jonka oletat tuottavasi) perusteella.

    > [!NOTE]
    > Jos sijaintikortti määritettiin edellyttämään fyysisen varaston poiminnan käsittelyä, vain jo varastotoiminnolla poimitut määrät voidaan antaa **Määrä**-kentässä **Kulutuskirjauskansio**-sivulla minkä tahansa lasketun määrän sijaan. Lisätietoja on kohdassa [Tuotanto- tai kokoonpanopoiminta laajennetuissa varastointimäärityksissä](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

3. Kirjaa kulutus valitsemalla **Kirjaa**-toiminto. Liittyviä varastoja vähennetään.

## <a name="see-also"></a>Katso myös

[Tuotanto](production-manage-manufacturing.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
