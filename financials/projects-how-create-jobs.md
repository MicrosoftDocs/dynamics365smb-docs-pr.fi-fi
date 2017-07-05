---
title: 'Toimintaohje: Projektien luominen| Microsoft Docs'
description: Artikkelissa kerrotaan, miten projektin luodaan.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, task
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: c9dcf1c235f3d510cde85502ac6ec40af748893b
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-create-jobs"></a>Toimintaohje: Projektien luominen
Uuden projektin aloittamisen yhteydessä on luotava projektikortti sekä integroidut projektitehtävät ja projektin suunnittelurivit kahteen eri tasoon.  

Ensimmäinen taso koostuu projektitehtävistä. Projektille on luotava vähintään yksi projektitehtävä, koska kirjaukset viittaavat projektitehtävään. Kun projektissa on vähintään yksi projektitehtävä, voit määrittää projektin suunnittelurivejä ja kirjata projektin kulutuksen.

Toinen taso koostuu projektin suunnitteluriveistä, jotka määrittävät yksityiskohtaisesti resurssien ja nimikkeiden käytön sekä erilaiset kirjanpidon kulut.

Tason rakenteen avulla voit jakaa projektin pienemmiksi tehtäviksi ja käyttää tarkempia tietoja budjetoinnissa, tarjouksissa ja rekisteröinnissä. Lisäksi saat sen avulla tietoja projektin etenemisestä. Voit seurata esimerkiksi sitä, miten olet saavuttanut määritetyt välitavoitteet tai oletko saavuttamassa budjettiin määritetyt tavoitteet.

**Huomautus**: **Uusi projekti** -toiminto **Projektipäällikkö**-roolikeskuksessa käynnistää avustetun asennuksen, jonka ohjaa vaihe vaiheelta projektin ja integroitujen tehtävien ja suunnittelurivien luomisessa. Seuraavassa kerrotaan, miten vaiheet suoritetaan manuaalisesti.

**Huomautus**: Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]-kokemuksen mukauttaminen](ui-experiences.md).

## <a name="to-create-a-job-card"></a>Projektikortin luominen
Luo projektikortti ja luo sitten projektikortille työtehtävä ja projektin suunnittelurivit.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektit** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit määrittää projektille muiden projektien tiedot valitsemalla **Kopioi projekti** -toiminnon, täyttämällä tarvittavat kentät ja valitsemalla sitten **OK**-painikkeen.

**Huomautus**: Jos projektissa käytetään aikaraportteja, myös vastuussa oleva henkilö on määritettävä. Tämä henkilö voi hyväksyä työhön liittyvien työntekijätehtävien tuntilomakkeet. Lisätietoja on kohdassa [Toimintaohje: Aikaraporttien määrittäminen](projects-how-setup-time-sheets.md).

## <a name="to-create-tasks-for-a-job"></a>Luo projektille tehtäviä
Projektin luomisen keskeinen osa on määrittää siihen liittyvät tehtävät. Se tehdään lisäämällä **Projektikortti**-ikkunan **Tehtävät**-pikavälilehteen yksi tehtävä riville. Jokaisella projektilla on oltava vähintään yksi tehtävä.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektit** ja valitse sitten liittyvä linkki.
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

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektit** ja valitse sitten liittyvä linkki.
2. Avaa asianmukainen projektikortti.
3. Valitse projektitehtävä, jonka **Projektitehtävätyyppi**-kentän arvo on **Kirjaus**. Valitse sitten **Projektin suunnittelurivit** -toiminto.  
4. Täytä **Projektin suunnittelurivit** -ikkunan uuden rivin tarvittavat kentät.
5. Toista vaiheet 3 ja 4 kaikille projektitehtävässä tarvittaville suunnitteluriveille.

## <a name="see-also"></a>Katso myös
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  
