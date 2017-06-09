---
title: "Dimensioiden määrittäminen| Microsoft Docs"
description: "Voit määrittää päiväkirjojen ja asiakirjojen, kuten myynti- ja ostotilausten, luokitteluun käytettävät dimensiot ja dimension arvot."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/28/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0da77c5be3b49f715384752ad61fc072aea8525c
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-dimensions"></a>Dimensioiden luominen
Voit määrittää päiväkirjojen ja asiakirjojen, kuten myynti- ja ostotilausten, luokitteluun käytettävät dimensiot ja dimension arvot. Dimensiot määritetään **Dimensiot**-ikkunassa, jossa kullekin dimensiolle luodaan yksi rivi. Dimensioita ovat esimerkiksi *Projekti*, *Osasto*, *Alue* ja *Myyjä*.

Voit määrittää myös arvoja dimensioille. Arvot voivat olla esimerkiksi yrityksen osastoja. Dimension arvot voi määrittää tilikartan kaltaisessa hierarkkisessa rakenteessa, jossa tiedot voi jakaa rakeisuustason mukaan ja jossa dimension arvojen osajoukoista voi laskea summat. Voit määrittää tarvitsemasi määrän dimensiota ja dimension arvoja, ja ne ovat yrityksessä kaikkien käytössä.

Voit määrittää myös joitakin globaaleja dimensioita ja pikadimensioita:  

* **Globaaleja dimensioita** käytetään suodattimina esimerkiksi raporteissa ja erätöissä. Käytössä on vain kaksi globaalia dimensiota, joten valitse usein käytetyt dimensiot.
* **Pikadimensiot** ovat käytössä kenttinä päiväkirjan ja asiakirjan riveillä. Voit luoda niitä enintään kuusi.  

**Huomautus**: Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]-kokemuksen mukauttaminen](ui-experiences.md).

## <a name="set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Oletusdimensioiden määrittäminen asiakkaille, toimittajille ja muille tileille
Voit määrittää oletusdimension tietylle tilille. Dimensio kopioidaan päiväkirjaan tai asiakirjaan, kun lisäät tilinumeron riville, mutta voit tarvittaessa poistaa koodin rivillä tai muuttaa sitä. Voit määrittää myös dimension, jota tarvitaan tietyn tyyppisen tilitapahtuman kirjaamiseen.  

## <a name="translate-the-names-of-dimensions"></a>Dimensioiden nimien kääntäminen
Dimensiota ja etenkin pikadimensiota luotaessa luodaan itse asiassa mukautettu kenttä tai sarakeotsikko. Jos kyse on kansainvälisestä yrityksestä, voit kääntää dimension nimen. Dimension sisältävät asiakirjat käyttävät tarvittaessa käännettyä nimeä.   

## <a name="example"></a>Esimerkki
Oletetaan, että yritys haluaa seurata tapahtumia organisaatiorakenteen ja maantieteellisen sijainnin perusteella. Määrität tätä tarkoitusta varten kaksi dimensiota **Dimensiot**-ikkunassa:

* **ALUE**  
* **OSASTO**  

| koodi | Name | Koodin otsikko | Suodattimen otsikko |
| --- | --- | --- | --- |
| ALUE |Alue |Aluekoodi |Aluesuodatus |
| OSASTO |Osaston |Osaston koodi |Osastosuodatus |

Lisää **ALUE**-koodiin seuraavat dimension arvot:

| koodi | Name | Dimension arvotyyppi |
| --- | --- | --- |
| 10 |Pohjois- ja Etelä-Amerikka |Alkusumma |
| 20 |Pohjois-Amerikka |Vakio |
| 30 |Tyynimeri |Vakio |
| 40 |Etelä-Amerikka |Vakio |
| 50 |Pohjois- ja Etelä-Amerikka, yhteensä |Loppusumma |
| 60 |Eurooppa |Alkusumma |
| 70 |EU |Vakio |
| 80 |Muu kuin EU |Vakio |
| 90 |Eurooppa, Yhteensä |Loppusumma |

Voit lisätä kahteen päätason maantieteelliseen alueeseen, Pohjois- ja Etelä-Amerikkaan sekä Eurooppaan, alueellisia alaluokkia alueiden sisentämällä dimension arvot. Tällä tavoin voit raportoida aluekohtaisen myynnin tai kulut ja saada kokonaissumman suurille maantieteellisille alueille. Olisit voinut käyttää dimension arvoina myös maita tai alueita – tai maakuntia tai paikkakuntia sen mukaan, mikä on liiketoiminnan kannalta järkevintä.  
**Huomautus**: Hierarkian määrittämistä varten koodien on oltava aakkosjärjestyksessä. Myös [!INCLUDE[d365fin](includes/d365fin_md.md)]iin sisältyvät dimension arvojen koodit on otettava tässä huomioon.  

Lisää **OSASTO**-koodiin seuraavat dimension arvot:

| koodi | Name | Dimension arvotyyppi |
| --- | --- | --- |
| HALLINTA |Hallinta |Vakio |
| TUOT |Tuotanto |Vakio |
| MYYNTI |Myynti |Vakio |

Näillä asetuksilla voit sitten lisätä kaksi dimensiota kahtena globaalina dimensiona **Pääkirjanpidon asetukset** -ikkunassa. Niinpä voit käyttää ALUE- ja OSASTO-koodeja pääkirjanpidon tapahtumien suodattamina sekä kaikissa raporteissa ja eräajoissa. Molemmat globaalit dimensiot ovat myös automaattisesti käytettävissä pikadimensioina tapahtumariveillä ja asiakirjojen otsikoissa.  

Voit aloittaa dimensioiden lisäämisen asiakirjoihin ja päiväkirjoihin näillä asetuksilla. Lisätietoja on kohdassa [Dimensiot](finance-dimensions.md).  

## <a name="see-also"></a>Katso myös
[Dimensiot](finance-dimensions.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

