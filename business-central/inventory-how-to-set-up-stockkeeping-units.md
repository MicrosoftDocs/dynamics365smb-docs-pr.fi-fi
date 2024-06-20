---
title: Varastointiyksiköiden määrittäminen
description: Käytä varastointiyksikköjä tallentaaksesi tietoja nimikkeistäsi tietyssä paikassa tai tietyssä variantissa.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/19/2023
ms.custom: bap-template
ms.search.forms: '5704, 5700, 5702, 5701'
ms.service: dynamics-365-business-central
---

# <a name="set-up-stock-keeping-units"></a>Varastointiyksiköiden määrittäminen

Käytä varastointiyksikköjä (SKU:ita) tallentaaksesi tietoja tietyn sijainnin tai variantin nimikkeistä. Niiden avulla voit lisätä nimikettä koskevia erilaisia tietoja tietylle sijainnille, esimerkiksi:

* Varasto tai jakelukeskus
* Saman nimikkeen variantit, kuten eri hyllynumerot ja eri täydennystiedot  

## <a name="to-set-up-a-sku"></a>Varastointiyksiköiden määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastointiyksiköt** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Täytä tarvittavat kentät. Seuraavat kentät ovat pakollisia: **Nimikkeen nro**, **Paikkakoodi**, ja **Varianttikoodi**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Kun olet määrittänyt nimikkeen ensimmäisen varastointiyksikön, **Nimike**-kortin **Varastointiyks. on olemassa** -valintaruutu on valittu.  

Käytä **Luo varastointiyksikkö** -eräajoa, kun haluat luoda nimikkeelle useita varastointiyksiköitä. Lukeaksesi lisätietoja erätöistä, siirry kohtaan [Työjonojen käyttäminen ajoitustehtäviin](admin-job-queues-schedule-tasks.md).  

> [!NOTE]  
> **Varastointiyksikön** kortin tiedoilla on korkeampi prioriteetti kuin **nimikkeen** kortilla.

> [!Warning]
> Jos varastointiyksikkö toimitetaan tuotannon välityksellä, **Vakiokustannus**-kenttää ei käytetä tuotetun nimikkeen todellisten kustannusten laskutuksessa ja oikaisussa. Sen sijaan [!INCLUDE [prod_short](includes/prod_short.md)] käyttää nimikekortin **Vakiokustannus**-kentän arvoa, ja kaikki varianssit lasketaan nimikkeen kustannusjakaumia kohden.<br><br>
> Vaikka voit määrittää SKU:ille tuotannon materiaaliluetteloita ja reitityksiä, yksikkökustannusten kokoaminen ja siihen liittyvä kustannusosuuksien laskelma eivät ole saatavilla SKU:ille. Lisätietoja vakiokustannuksista on kohdassa [Tietoja vakiokustannusten laskemisesta](finance-about-calculating-standard-cost.md)

## <a name="see-also"></a>Katso myös

[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
