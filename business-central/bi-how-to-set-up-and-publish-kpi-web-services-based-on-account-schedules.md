---
title: KP-raporttimallien KPI-verkkopalvelun määrittäminen ja julkaiseminen | Microsoft Docs
description: Tässä ohjeaiheessa kuvataan, miten KP-raporttimallin KPI-tiedot näytetään tietyissä KP-raporttimalleissa.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 9439cdbc2fbe6f2125ebc2be3e6965ad6ed7265f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752178"
---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>KP-raporttimalleihin perustuvan KPI-verkkopalvelun määrittäminen ja julkaiseminen
Voit määrittää **KP-raporttimallin KPI-verkkopalvelun asetukset** -sivulla, miten KP-raporttimallin KPI-tiedot näytetään ja mihin tiettyihin KP-raporttimalleihin KPI:t perustuvat. Kun valitset **Julkaise verkkopalvelu** -painikkeen, määritellyt KP-raporttimallin KPI-tiedot lisätään julkaistujen verkkopalveluiden luetteloon **Verkkopalvelut**-sivulla.  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>KP-raporttimalleihin perustuvan KPI-verkkopalvelun määrittäminen ja julkaiseminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **KP-raporttimallin KPI-verkkopalvelun asetukset** ja valitse sitten liittyvä linkki.  
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
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]