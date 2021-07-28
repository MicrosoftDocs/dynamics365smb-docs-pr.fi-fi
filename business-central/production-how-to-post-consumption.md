---
title: Kulutuksen eräkirjaus
description: Jos materiaalinottotapa on Manuaalinen, komponentit tulee kirjata manuaalisesti kulutuspäiväkirjaa käyttämällä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2f31c7f48e88a44eb3f437827b6b24f255180d9a
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6440426"
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
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
