---
title: KPI-verkkopalvelun määrittäminen ja julkaiseminen KP-raporttimalleja varten
description: Tässä ohjeaiheessa kuvataan, miten KP-raporttimallin KPI-tiedot näytetään tietyissä KP-raporttimalleissa.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 103, 104, 197, 196, 195, 198, 490, 764, 765, 766
ms.date: 06/15/2021
ms.author: bholtorf
ms.openlocfilehash: d8d3e9b37abe5e8d24e1d01eacfdff96df94da45
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514093"
---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>KP-raporttimalleihin perustuvan KPI-verkkopalvelun määrittäminen ja julkaiseminen
Voit määrittää **KP-raporttimallin KPI-verkkopalvelun asetukset** -sivulla, miten KP-raporttimallin KPI-tiedot näytetään ja mihin tiettyihin KP-raporttimalleihin KPI:t perustuvat. Kun valitset **Julkaise verkkopalvelu** -painikkeen, määritellyt KP-raporttimallin KPI-tiedot lisätään julkaistujen verkkopalveluiden luetteloon **Verkkopalvelut**-sivulla.  

> [!NOTE]
> Kun käytät tätä verkkopalvelua, tietojoukkoon ei sisällytetä sulkemispäivämääriä. Tämä vuoksi Power BI:ssä voidaan käyttää suodattimia eri ajanjaksojen analysoimiseksi.

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>KP-raporttimalleihin perustuvan KPI-verkkopalvelun määrittäminen ja julkaiseminen  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KP-raporttimallin KPI-verkkopalvelun asetukset** ja valitse sitten liittyvä linkki.  
2.  Täytä **Yleinen**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Ennustettujen arvojen alku**|Määritä, missä vaiheessa ennustetut arvot näytetään KP-raporttimallin KPI-kuvaajassa.<br /><br /> Ennustetut arvot haetaan pääkirjanpidon budjetista, jonka valitset **KP-budjetin nimi** -kentässä. **Huomautus:** Jos haluat saada ennustettuja lukuja tietyn päivämäärän jälkeen osoittavat KPI-tiedot ja toteutuneet luvut ennen päivämäärää, voit muuttaa **Ensimm. sallittu kirjauspvm** -kenttää **Pääkirjanpidon asetukset** -sivulla. Lisätietoja on kohdassa Ensimm. sallittu kirjauspvm.|  
    |**KP-budjetin nimi**|Määritä sen pääkirjanpidon budjetin nimi, joka tarjoaa ennustettuja arvoja KP-raporttimallin KPI-verkkopalveluun.|  
    |**Jakso**|Määritä ajanjakso, jolle KP-raporttimallin KPI-verkkopalvelu perustuu.|  
    |**Näyttöperuste**|Määritä, millä aikavälillä KP-raporttimallin KPI-tiedot näytetään.|  
    |**Verkkopalvelun nimi**|Määritä KP-raporttimallin KPI-verkkopalvelun nimi.<br /><br /> Tämä nimi näkyy **Palvelun nimi** -kentässä **Verkkopalvelut**-sivulla.|  

    Määritä vähintään yksi KP-raporttimalli, jonka haluat julkaista KPI-verkkopalveluna edellisen taulukon asetusten mukaisesti.  

3.  Täytä **Raporttimallit**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**KP-raporttimallin nimi**|Määritä KP-raporttimalli, jolle KPI-verkkopalvelu perustuu.|  
    |**KP-raporttimallin kuvaus**|Määritä KP-raporttimalli kuvaus, jolle KPI-verkkopalvelu perustuu.|  

4.  Toista vaihe 3 kaikille KP-raporttimalleille, joille haluat KP-raporttimallin KPI-verkkopalvelun perustuvan.  
5.  Tarkastele tai muokkaa valittua KP-raporttimallia valitsemalla **KP-raporttimalli**-välilehdessä **Muokkaa KP-raporttimallia** -toiminnon.  
6.  Voit tarkastella luomiasi KP-raporttimallin KPI-tietoja valitsemalla **KP-raporttimallin KPI-verkkopalvelu** -toiminnon.  
7.  Julkaise KP-raporttimalli KPI-verkkopalveluna valitsemalla **Julkaise verkkopalvelu** -toiminto. Verkkopalvelu lisätään julkaistujen verkkopalveluiden luetteloon **Verkkopalvelut**-sivulla.  

> [!NOTE]  
>  Voit myös julkaista KPI-verkkopalvelun osoittamalla **KP-raporttimallin KPI-verkkopalvelun asetukset** -sivukohdetta **Verkkopalvelut**-sivulla. Lisätietoja on kohdassa [Verkkopalvelun julkaiseminen](across-how-publish-web-service.md).  

## <a name="see-also"></a>Katso myös  
[Business Intelligence](bi.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]