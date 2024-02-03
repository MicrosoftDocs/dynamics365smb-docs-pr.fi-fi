---
title: Oletusvarastopaikkojen määrittäminen nimikkeille
description: 'Jos käytät sijainnissa varastopaikkoja, voit helpottaa nimikkeiden toimitusta, vastaanottoa ja siirtämistä määrittämällä nimikkeille oletusvarastopaikat.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '7371, 7374, 7379'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="assign-default-bins-to-items"></a>Oletusvarastopaikkojen määrittäminen nimikkeille
Jos käytät sijainnissa varastopaikkoja, voit helpottaa nimikkeiden toimitusta, vastaanottoa ja siirtämistä määrittämällä nimikkeille oletusvarastopaikat. Kun nimikkeelle on määritetty oletusvarastopaikka, ohjelma ehdottaa tätä varastopaikkaa aina, kun aloitat tapahtuman tälle nimikkeelle. Voit määrittää oletusvarastopaikat **Varastopaikan sisältö** -sivulla.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Oletusvarastopaikan määrittäminen nimikkeelle
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Var.p. sisällön luontityökirja** ja valitse sitten vastaava linkki.  
2.  Täydennä varastopaikan koodi ja nimikkeen tiedot kunkin sellaisen varastopaikan osalta, jota haluat käyttää jonkin nimikkeen oletusvarastopaikkana. Varmista, että olet valinnut **Oletus**-kentän.  
3.  Valitse **Luo var.paikan sisältö** -toiminto. Nimikkeelle on nyt määritetty oletusvarastopaikat.  

> [!NOTE]  
>  Kun nimike hyllytetään eikä sille ole määritetty oletusvarastopaikkaa, järjestelmä määrittää oletusvarastopaikaksi varastopaikan, johon nimike hyllytetään.  

## <a name="to-change-the-default-bin-for-an-item"></a>Nimikkeen oletusvarastopaikan muuttaminen
Joskus voi olla tarpeen muuttaa tietyn nimikkeen oletusvarastopaikan määritystä tai määrittää uudelle nimikkeelle oletusvarastopaikka.
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastopaikan sisältö** ja valitse sitten vastaava linkki.  
2.  Valitse **Sijaintisuodatus**-kentässä haluttu sijaintikoodi.  
3.  Etsi nimikkeen nykyinen oletusvarastopaikka ja poista **Oletusvarastopaikka**-valintaruudun valinta.  
4.  Etsi uudeksi varastopaikan sisällöksi haluamasi varastopaikan Varastopaikan sisältö -rivi. Valitse **Oletusvarastopaikka**-valintaruutu.  

> [!NOTE]  
>  Kun nimike hyllytetään ensimmäisen kerran eikä sille ole määritetty oletusvarastopaikkaa, järjestelmä määrittää oletusvarastopaikaksi varastopaikan, johon nimike hyllytetään.  

## <a name="see-also"></a>Katso myös
[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md) 
[Kokoonpanon hallinta](assembly-assemble-items.md)
[[!INCLUDE[prod_short](includes/prod_short.md)]in hallinta](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
