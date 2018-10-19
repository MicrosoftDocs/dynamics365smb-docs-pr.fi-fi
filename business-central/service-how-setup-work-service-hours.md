---
title: "Työ- ja huoltotuntien määrittäminen | Microsoft Docs"
description: "Voit määrittää yrityksesi normaalit huoltotunnit. Huoltotuntien avulla lasketaan huoltotilausten ja -tarjousten vastauspäivämäärä ja -aika osalta ja vastausaikavaroitusten lähettäminen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6617cb324873c2c129e4d26907dc43fde1c3c0e6
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-work-hours-and-service-hours"></a>Työ- ja huoltotuntien määrittäminen
Tavallisesti huoltohallintojärjestelmässä seurataan resurssin tunteja ja huoltotilauksen tilaa kuormituksen ja huollon tarpeiden ennustamista varten. [!INCLUDE[d365fin](includes/d365fin_md.md)]in sisäiset työkalut voi mukauttaa tallentamaan tällaisia tietoja.  
  
Kun olet määrittänyt yrityksen oletushuoltotunnit, voit laskea huoltotilausten vastausajat tai lähettää varoituksia hälytyksiä huoltokutsun saapuessa. Hälytystoiminto otetaan käyttöön yhdessä työn aikataulutuksen kanssa.   
  
Huoltotilausta käsiteltäessä tilan päivittäminen antaa mahdollisuuden seurata edistymistä. Huoltotilauksen tila kuvastaa kaikkien huoltotilauksessa olevien huoltonimikkeiden korjauksen tilaa. Lisätietoja on kohdassa [Tietoja huoltotilauksesta ja korjauksen tilasta](service-order-repair-status.md). 

## <a name="to-set-up-default-service-hours"></a>Oletushuoltotuntien määrittäminen  
**Oletus huoltotunnit** -ikkunaa käytetään määrittämään yrityksesi tavallisia huoltotunteja. Ohjelma käyttää huoltotunteja silloin, kun se laskee vastauspäivämäärää ja -aikaa huoltotilausten ja -tarjousten osalta ja kun se lähettää vastausajan varoituksia. Ohjelma käyttää huoltosopimuksissa oletushuoltotunteja, ellei sopimukselle määritetä erityishuoltotunteja.  
  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Oletushuoltotunnit** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  Jos **Oletus huoltotunnit** -ikkunan rivit jätetään tyhjiksi, ohjelma käyttää oletuksena 24 tuntia kaikkina kalenterityöpäivinä.  
  
## <a name="to-set-up-work-hour-templates"></a>Työtuntimallien määrittäminen
**Työtuntimalli** -ikkunaa käytetään määrittämään malleja, jotka sisältävät yrityksen tavalliset työtunnit. Malleja voi luoda esimerkiksi kokoaikaisille teknikoille ja osa-aikaisille teknikoille. Työtunnin malleja voi käyttää silloin, kun lisäät kapasiteettia resursseille.  
  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työtuntimallit** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> Kun kunkin päivän työtunnit on annettu, **Yhteensä per viikko** -kentän arvo lasketaan automaattisesti.  

## <a name="to-set-up-contract-specific-service-hours"></a>Sopimuskohtaisten huoltotuntien määrittäminen  
**Huoltotunnit**-ikkunaa voidaan käyttää erityisten huoltotuntien määrittämiseen huoltosopimuksen omistavalle asiakkaalle. Ohjelma käyttää huoltotunteja silloin, kun se laskee vastauspäivämäärää ja -aikaa huoltotilauksiin ja tarjouksiin, jotka kuuluvat kyseiseen huoltosopimukseen.  
  
Jos huoltosopimukselle ei määritetä erityisiä huoltotunteja, ohjelma käyttää huoltosopimusten oletusarvoisia huoltotunteja.  
  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimukset** ja valitse sitten liittyvä linkki.  
2. Avaa huoltosopimus, jolle haluat määrittää huoltotunnit, ja valitse **Huoltotunnit**.  
4. Voit määrittää oletushuoltotunteihin perustuvat huoltotunnit valitsemalla **Kopioi oletushuoltotunnit** -toiminto.  
5. Muokkaa huoltotuntitapahtumien kenttiä. Lisää tai poista tapahtumat sopimuksen huoltotuntien määrittämistä varten. Huomaa, että kentät **Päivä**, **Aloitusaika** ja **Lopetusaika** tarvitaan jokaiselle riville.  
6. Jos haluat huoltotuntien olevan voimassa tietystä päivästä alkaen, anna päivä **Aloituspvm**-kenttään.  
7. Jos haluat huoltotuntien olevan voimassa loma-aikoina, valitse **Voimassa loma-aikoina** -kentän valintaruutu.  

## <a name="see-also"></a>Katso myös  
[Tietoja kohdistuksen tilasta ja korjauksen tilasta](service-allocation-status-and-repair-status.md)  
[Huoltohallinnon määrittäminen](service-setup-service.md)  
[Tietoja huoltotilauksen ja korjauksen tilasta](service-order-repair-status.md)  

