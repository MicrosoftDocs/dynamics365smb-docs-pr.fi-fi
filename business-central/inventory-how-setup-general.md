---
title: Yleisten varastotietojen määrittäminen
description: 'Kuvaus siitä, miten fyysisen varaston ja varaston hallinta voidaan määrittää.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, stock'
ms.search.form: '30, 456, 461'
ms.date: 07/28/2021
ms.author: edupont
---
# <a name="set-up-general-inventory-information"></a><a name="set-up-general-inventory-information"></a>Yleisten varastotietojen määrittäminen

Yleiset varastoasetukset määritetään **Varastonhallinnan asetukset** -sivulla.

## <a name="to-set-up-general-inventory-information"></a><a name="to-set-up-general-inventory-information"></a>Yleisten varastotietojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastonhallinnan asetukset** ja valitse sitten vastaava linkki.
2. Täytä **Varastonhallinnan asetukset** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Lisätietoja kustannuslaskentakentistä, **Automaattisesta kustannusten kirjaamisesta**, **Oletetusta kustannusten kirjaamisesta KP:oon** ja **Oletuskustannuslaskentamenetelmästä** on kohdassa [Varaston kustannusten täsmäyttäminen pääkirjanpitoon](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Suunnittelun tiedot: varaston kustannuslaskelma](design-details-inventory-costing.md) ja [Suunnittelun tiedot: oletettu kustannuskirjaus](design-details-expected-cost-posting.md). Lisätietoja yleisestä kustannuslaskennasta on kohdassa [Varastokustannusten hallinta](finance-manage-inventory-costs.md).  

Jos haluat sisällyttää fyysisen varastoinnin käsittelyajan ostorivin toimituksen lupaamisen laskentaan, voit määrittää sen oletusarvoksi varastolle ja sijainnille **Varastonhallinnan asetukset** -sivulla. Lisätietoja on kohdassa [Toimituksen lupaamisen päivämäärän laskeminen](sales-how-to-calculate-order-promising-dates.md).  

> [!NOTE]
> **Automaattinen kustannusten oikaisu** -kentän arvona on oletusarvoisesti *Aina*, jotta varaston arvot ovat aina oikeat kirjanpidossa, mikä puolestaan pitää myynti- ja tuottotilastot ajan tasalla. Kustannusten muutokset saapuvista merkinnöistä, kuten ostoista tai tuotannosta, kohdistetaan niihin liittyviin lähteviin tietoihin, kuten myynteihin tai siirtoihin. Tämä on hyödyllistä uusille [!INCLUDE[prod_short](includes/prod_short.md)] -asiakkaille ja pienille yrityksille, joilla on suhteellisen alhaiset varastotransaktiotasot.
>
> Yrityksen kasvaessa ja varastotasojen kasvaessa tämä voi kuitenkin hidastaa järjestelmän suorituskykyä. Jos haluat vähentää suorituskykyä kirjauksen aikana, valitse ajan asetus, joka määrittää, kuinka kauas taaksepäin käsittelypäivämäärästä lähtien saapuva tapahtuma voi aiheuttaa liittyvien lähtevien arvotapahtumien muuttamisen.
>
> Vaihtoehtoisesti voit muuttaa kustannuksia säännöllisin väliajoin Muuta kust.-nimike tapahtumat -eräajon avulla. Voit myös poistaa automaattisen kustannusten kirjaamisen käytöstä tai määrittää **Automaattinen kustannusten oikaisu** -kentän arvoksi *Ei koskaan*. Molemmissa tapauksissa näyttöön tulee ilmoitus, josta voit käynnistää avustetun asennusoppaan, jonka avulla voit ajoittaa tehtäviä työjonoon. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Varastonhallinnan määrittäminen](inventory-setup-inventory.md)  
[Rakennetiedot: Arvostusmenetelmät](design-details-costing-methods.md)  
[Varaston hallinta](inventory-manage-inventory.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
