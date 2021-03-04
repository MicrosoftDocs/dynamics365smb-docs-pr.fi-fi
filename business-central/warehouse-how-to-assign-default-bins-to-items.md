---
title: Oletusvarastopaikkojen määrittäminen nimikkeille | Microsoft Docs
description: Jos käytät sijainnissa varastopaikkoja, voit helpottaa nimikkeiden toimitusta, vastaanottoa ja siirtämistä määrittämällä nimikkeille oletusvarastopaikat. Kun nimikkeelle on määritetty oletusvarastopaikka, ohjelma ehdottaa tätä varastopaikkaa aina, kun aloitat tapahtuman tälle nimikkeelle.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f3374929434876cee088f046efc6d5f950671cc8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756315"
---
# <a name="assign-default-bins-to-items"></a>Oletusvarastopaikkojen määrittäminen nimikkeille
Jos käytät sijainnissa varastopaikkoja, voit helpottaa nimikkeiden toimitusta, vastaanottoa ja siirtämistä määrittämällä nimikkeille oletusvarastopaikat. Kun nimikkeelle on määritetty oletusvarastopaikka, ohjelma ehdottaa tätä varastopaikkaa aina, kun aloitat tapahtuman tälle nimikkeelle. Voit määrittää oletusvarastopaikat **Varastopaikan sisältö** -sivulla.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Oletusvarastopaikan määrittäminen nimikkeelle
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Var.p. sisällön luontityökirja** ja valitse sitten liittyvä linkki.  
2.  Täydennä varastopaikan koodi ja nimikkeen tiedot kunkin sellaisen varastopaikan osalta, jota haluat käyttää jonkin nimikkeen oletusvarastopaikkana. Varmista, että olet valinnut **Oletus**-kentän.  
3.  Valitse **Luo var.paikan sisältö** -toiminto. Nimikkeelle on nyt määritetty oletusvarastopaikat.  

> [!NOTE]  
>  Kun nimike hyllytetään eikä sille ole määritetty oletusvarastopaikkaa, järjestelmä määrittää oletusvarastopaikaksi varastopaikan, johon nimike hyllytetään.  

## <a name="to-change-the-default-bin-for-an-item"></a>Nimikkeen oletusvarastopaikan muuttaminen  
Joskus voi olla tarpeen muuttaa tietyn nimikkeen oletusvarastopaikan määritystä tai määrittää uudelle nimikkeelle oletusvarastopaikka.    
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varastopaikan sisältö** ja valitse sitten liittyvä linkki.  
2.  Valitse **Sijaintisuodatus**-kentässä haluttu sijaintikoodi.  
3.  Etsi nimikkeen nykyinen oletusvarastopaikka ja poista **Oletusvarastopaikka**-valintaruudun valinta.  
4.  Etsi uudeksi varastopaikan sisällöksi haluamasi varastopaikan Varastopaikan sisältö -rivi. Valitse **Oletusvarastopaikka**-valintaruutu.  

> [!NOTE]  
>  Kun nimike hyllytetään ensimmäisen kerran eikä sille ole määritetty oletusvarastopaikkaa, järjestelmä määrittää oletusvarastopaikaksi varastopaikan, johon nimike hyllytetään.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]