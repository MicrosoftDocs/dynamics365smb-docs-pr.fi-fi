---
title: Työ- ja huoltotuntien määrittäminen | Microsoft Docs
description: Voit määrittää yrityksesi normaalit huoltotunnit. Huoltotuntien avulla lasketaan huoltotilausten ja -tarjousten vastauspäivämäärä ja -aika osalta ja vastausaikavaroitusten lähettäminen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6aaf78756f091d70a1a33532afbafb14a5b29bc7
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877277"
---
# <a name="set-up-work-hours-and-service-hours"></a>Työ- ja huoltotuntien määrittäminen
Tavallisesti huoltohallintojärjestelmässä seurataan resurssin tunteja ja huoltotilauksen tilaa kuormituksen ja huollon tarpeiden ennustamista varten. [!INCLUDE[d365fin](includes/d365fin_md.md)]in sisäiset työkalut voi mukauttaa tallentamaan tällaisia tietoja.  
  
Kun olet määrittänyt yrityksen oletushuoltotunnit, voit laskea huoltotilausten vastausajat tai lähettää varoituksia hälytyksiä huoltokutsun saapuessa. Hälytystoiminto otetaan käyttöön yhdessä työn aikataulutuksen kanssa.   
  
Huoltotilausta käsiteltäessä tilan päivittäminen antaa mahdollisuuden seurata edistymistä. Huoltotilauksen tila kuvastaa kaikkien huoltotilauksessa olevien huoltonimikkeiden korjauksen tilaa. Lisätietoja on kohdassa [Tietoja huoltotilauksesta ja korjauksen tilasta](service-order-repair-status.md). 

## <a name="to-set-up-default-service-hours"></a>Oletushuoltotuntien määrittäminen  
**Oletus huoltotunnit** -sivua käytetään määrittämään yrityksesi tavallisia huoltotunteja. Ohjelma käyttää huoltotunteja silloin, kun se laskee vastauspäivämäärää ja -aikaa huoltotilausten ja -tarjousten osalta ja kun se lähettää vastausajan varoituksia. Ohjelma käyttää huoltosopimuksissa oletushuoltotunteja, ellei sopimukselle määritetä erityishuoltotunteja.  
  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Oletushuoltotunnit** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  Jos **Oletus huoltotunnit** -sivun rivit jätetään tyhjiksi, ohjelma käyttää oletuksena 24 tuntia kaikkina kalenterityöpäivinä.  
  
## <a name="to-set-up-work-hour-templates"></a>Työtuntimallien määrittäminen
**Työtuntimalli**-sivua käytetään määrittämään malleja, jotka sisältävät yrityksen tavalliset työtunnit. Malleja voi luoda esimerkiksi kokoaikaisille teknikoille ja osa-aikaisille teknikoille. Työtunnin malleja voi käyttää silloin, kun lisäät kapasiteettia resursseille.  
  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Työtuntimallit** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> Kun kunkin päivän työtunnit on annettu, **Yhteensä per viikko** -kentän arvo lasketaan automaattisesti.  

## <a name="to-set-up-contract-specific-service-hours"></a>Sopimuskohtaisten huoltotuntien määrittäminen  
**Huoltotunnit**-sivua voidaan käyttää erityisten huoltotuntien määrittämiseen huoltosopimuksen omistavalle asiakkaalle. Ohjelma käyttää huoltotunteja silloin, kun se laskee vastauspäivämäärää ja -aikaa huoltotilauksiin ja tarjouksiin, jotka kuuluvat kyseiseen huoltosopimukseen.  
  
Jos huoltosopimukselle ei määritetä erityisiä huoltotunteja, ohjelma käyttää huoltosopimusten oletusarvoisia huoltotunteja.  
  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltosopimukset** ja valitse sitten liittyvä linkki.  
2. Avaa huoltosopimus, jolle haluat määrittää huoltotunnit, ja valitse **Huoltotunnit**.  
4. Voit määrittää oletushuoltotunteihin perustuvat huoltotunnit valitsemalla **Kopioi oletushuoltotunnit** -toiminto.  
5. Muokkaa huoltotuntitapahtumien kenttiä. Lisää tai poista tapahtumat sopimuksen huoltotuntien määrittämistä varten. Huomaa, että kentät **Päivä**, **Aloitusaika** ja **Lopetusaika** tarvitaan jokaiselle riville.  
6. Jos haluat huoltotuntien olevan voimassa tietystä päivästä alkaen, anna päivä **Aloituspvm**-kenttään.  
7. Jos haluat huoltotuntien olevan voimassa loma-aikoina, valitse **Voimassa loma-aikoina** -kentän valintaruutu.  

## <a name="see-also"></a>Katso myös  
[Tietoja kohdistuksen tilasta ja korjauksen tilasta](service-allocation-status-and-repair-status.md)  
[Huoltohallinnon määrittäminen](service-setup-service.md)  
[Tietoja huoltotilauksen ja korjauksen tilasta](service-order-repair-status.md)  
