---
title: "Projektin projektikortin luominen ja tehtävien määrittäminen| Microsoft Docs"
description: "Uudelle projektille luodaan projektin tehtävät ja suunnittelurivit sisältävä projektikortti, mikä auttaa edistymisen ja budjettien hallinnassa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, task
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ece0a95f83868ac2657fdf41330e7d0a9cce37d6
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="create-jobs"></a>Projektien luominen
Uuden projektin aloittamisen yhteydessä on luotava projektikortti sekä integroidut projektitehtävät ja projektin suunnittelurivit kahteen eri tasoon.  

Ensimmäinen taso koostuu projektitehtävistä. Projektille on luotava vähintään yksi projektitehtävä, koska kirjaukset viittaavat projektitehtävään. Kun projektissa on vähintään yksi projektitehtävä, voit määrittää projektin suunnittelurivejä ja kirjata projektin kulutuksen.

Toinen taso koostuu projektin suunnitteluriveistä, jotka määrittävät yksityiskohtaisesti resurssien ja nimikkeiden käytön sekä erilaiset kirjanpidon kulut.

Tason rakenteen avulla voit jakaa projektin pienemmiksi tehtäviksi ja käyttää tarkempia tietoja budjetoinnissa, tarjouksissa ja rekisteröinnissä. Lisäksi saat sen avulla tietoja projektin etenemisestä. Voit seurata esimerkiksi sitä, miten olet saavuttanut määritetyt välitavoitteet tai oletko saavuttamassa budjettiin määritetyt tavoitteet.

> [!NOTE]  
>   **Projektipäällikkö**-roolikeskuksen **Uusi projekti** -toiminto käynnistää avustetun asennuksen, jonka ohjaa vaihe vaiheelta projektin ja integroitujen tehtävien ja suunnittelurivien luomisessa. Seuraavassa kerrotaan, miten vaiheet suoritetaan manuaalisesti.

## <a name="to-create-a-job-card"></a>Projektikortin luominen
Luo projektikortti ja luo sitten projektikortille työtehtävä ja projektin suunnittelurivit.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit määrittää projektille muiden projektien tiedot valitsemalla **Kopioi projekti** -toiminnon, täyttämällä tarvittavat kentät ja valitsemalla sitten **OK**-painikkeen.

> [!NOTE]  
>   Jos projektissa käytetään aikaraportteja, myös vastuussa oleva henkilö on määritettävä. Tämä henkilö voi hyväksyä työhön liittyvien työntekijätehtävien tuntilomakkeet. Lisätietoja on kohdassa [Aikaraporttien määrittäminen](projects-how-setup-time-sheets.md).

## <a name="to-create-tasks-for-a-job"></a>Luo projektille tehtäviä
Projektin luomisen keskeinen osa on määrittää siihen liittyvät tehtävät. Se tehdään lisäämällä **Projektikortti**-ikkunan **Tehtävät**-pikavälilehteen yksi tehtävä riville. Jokaisella projektilla on oltava vähintään yksi tehtävä.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektit** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa asianmukaisen projektin projektikortti.
3. Täytä **Tehtävät**-pikavälilehden uuden rivin kentät tarvittaessa.
4. Kun haluat sisentää tehtäviä ja luoda hierarkian, valitse **Tehtävät**-toiminto ja sen jälkeen **Sisennä projektitehtävät** -toiminto.
5. Toista vaiheet 3 ja 4 kaikille projektissa tarvittaville tehtäville.
6. Voit määrittää projektitehtäville muiden projektitehtävien tiedot valitsemalla **Kopioi projektitehtävät kohteesta** -toiminnon, täyttämällä tarvittavat kentät ja valitsemalla sitten **OK**-painikkeen.

## <a name="to-create-planning-lines-for-a-job"></a>Projektin suunnittelurivien luominen
Voit tarkentaa uusia projektitehtäviä projektin suunnitteluriveillä. Suunnittelurivin avulla voidaan taltioida kaikki tiedot, joita haluat seurata työssä. Voit käyttää suunnittelurivejä lisätäksesi tietoja, muun muassa tiedot siitä, mitä resursseja tarvitaan tai kerätään ja mitä nimikkeitä tarvitaan projektin suorittamisessa. Voit esimerkiksi liittää projektia koskevan asiakkaan hyväksynnän hankkimisessa käytettävän tehtävän nimikkeiden, kuten asiakkaan kanssa käydyn neuvottelun ja resurssin määrittämisen, suunnitteluriveihin.  

Projektin suunnittelurivin tyyppi voi olla jokin seuraavista tyypeistä.  

| Tyyppi | Kuvaus |
| --- | --- |
| **Budjetti** |Projektin käytön ja kustannusten arviointi, yleensä Aika ja materiaali -tyyppisessä projektissa. Tämän tyyppisiä suunnittelurivejä ei voi laskuttaa. |
| **Laskutettava** |Asiakkaan arviolaskutus, yleensä kiinteähintainen projekti. |
| **Sekä budjetti että laskutettava** |Budjetoitu käyttö on sama kuin laskutettava käyttö. |

**Huomautus**. Kustannustiedot täytetään automaattisesti projektin suunnittelurivien tietojen lisäyksen aikana. Esimerkiksi resurssien ja nimikkeiden kustannus, hinta ja alennus perustuvat resurssin ja nimikkeen kortteihin määritettyihin tietoihin.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektit** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa asianmukainen projektikortti.
3. Valitse projektitehtävä, jonka **Projektitehtävätyyppi**-kentän arvo on **Kirjaus**. Valitse sitten **Projektin suunnittelurivit** -toiminto.  
4. Täytä **Projektin suunnittelurivit** -ikkunan uuden rivin tarvittavat kentät.
5. Toista vaiheet 3 ja 4 kaikille projektitehtävässä tarvittaville suunnitteluriveille.

## <a name="see-also"></a>Katso myös
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

