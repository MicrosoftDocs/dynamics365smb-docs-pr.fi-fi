---
title: Fyysisen varaston toimintorivien jakaminen
description: 'Tietoja varastotoimintorivien jakamisesta, jos ehdotetun varastopaikan käytettävissä oleva kapasiteetti ei riitä.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 9314, 9313, 9315, 9330'
---
# <a name="split-warehouse-activity-lines"></a><a name="split-warehouse-activity-lines"></a>Varastotoimintorivien jakaminen

Fyysisen varastoinnin hyllytyksissä, siirroissa ja poiminnoissa sekä varaston hyllytyksissä ja poiminnoissa poimintaa ja hyllytystä varten ehdotetaan varastopaikkoja. Joskus voi käydä niin, että ehdotettu varastopaikka ei ole riittävä tai että ehdotetussa varastopaikassa ei ole tarpeeksi tilaa hyllytettävälle määrälle. Tällöin rivi voidaan jakaa, jolloin yhden rivin nimikkeet voidaan siirtää useisiin varastopaikkoihin tai ne voidaan hakea useista varastopaikoista.  

Seuraavasti toimitaan seuraavien varastointiasiakirjojen osalta:

* Fyysisen varaston hyllytykset
* Fyysisen varaston siirrot
* Fyysisen varaston poiminnat
* Varaston hyllytykset
* Varastosiirrot
* Varaston poiminnat  

## <a name="to-split-warehouse-activity-lines"></a><a name="to-split-warehouse-activity-lines"></a>Jaa fyysisen varaston aktiviteettirivit

1. Avaa fyysisen varastoinnin toimintorivi, jolla yrität käsitellä riittämätöntä määrää.  
2. Anna **Käsiteltävä määrä** -kentässä vähennetty määrä, joka on käsiteltävissä.  
3. Valitse **Rivit**-pikavälilehdessä ensin **Toiminnot**-, sitten **Toiminnot**- ja lopuksi **Jaa rivi** -toiminto. Uusi rivi tulee näkyvin. Rivi on muuten alkuperäisen rivin kopio, mutta sen **Käsiteltävä määrä** -kentässä on alkuperäiseltä riviltä poistettu määrä.  
4. Määritä varastopaikka, jos käytössä on ohjattu hyllytys ja poiminta, alue tai jatka rivin jakamista siihen asti, koko määrää vastaavat varastopaikat löytyvät.  

> [!NOTE]  
> Jos jaat rivit, kun sijainnissa on käytössä ohjattu hyllytys ja poiminta, sinun täytyy tuntea fyysinen varasto hyvin ja pystyä valitsemaan varastopaikka, joka vastaa nimikkeen varastointitarpeita ja joka täyttää fyysisen varastoinnin asiakirjan yleiset vaatimukset. Esimerkiksi poiminta-asiakirjan riviä ei jaeta eikä joitakin nimikkeitä sijoiteta irtotavaravarastoon.  

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
