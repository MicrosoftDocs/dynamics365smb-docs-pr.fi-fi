---
title: "Dimensioiden käyttäminen| Microsoft Docs"
description: "Voit käyttää dimensioita tapahtumien luokitteluun esimerkiksi osasto- tai projektikohtaisesti, jonka ansiosta tietojen seuranta ja analysointi helpottuu."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/16/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: b7b69b3419520c482cbe6a84494bbac7ef35bea1
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="working-with-dimensions"></a>Dimensioiden käyttäminen
Voit yksinkertaistaa asiakirjojen, kuten myyntitilausten, analysointia dimensioiden avulla. Dimensiot ovat tapahtumia luokittelevia määritteitä ja arvoja, joita voi seurata ja analysoida. Dimensioiden avulla voit esimerkiksi ilmaista, mistä projektista tai osastosta tapahtuma on lähtöisin.  

Jos käytät dimensioita, sinun ei esimerkiksi tarvitse määrittää erillisiä kirjanpitotilejä kullekin osastolle ja projektille. Tämä mahdollistaa monipuolinen analysoinnin ilman monimutkaisen tilikartan luontia. Lisätietoja on ohjeaiheessa [Business Intelligence](bi.md).

Voit myös esimerkiksi määrittää *Osasto*-nimisen dimension ja käyttää sitä myyntiasiakirjojen kirjaamisen yhteydessä. Voit sitten käyttää BI-työkaluja, jos haluat selvittää, mitä nimikkeitä kukin osasto myy.
Mitä useampia dimensioita käytät, sitä yksityiskohtaisempia raportteja voit käyttää liiketoimintapäätösten apuna. Yksittäisessä myyntitapahtumassa voi esimerkiksi olla useita dimensiotietoja, kuten  

* tili, jolle nimikkeen myynti on kirjattu  
* nimikkeen myyntipaikka
* nimikkeen myyjä
* nimikkeen ostaneen asiakkaan tyyppi.  

> [!NOTE]  
>   Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).

## <a name="analyzing-by-dimensions"></a>Analyysi dimensioittain
Dimensiotoiminnot ovat tärkeä osa liiketoimintatietoja esimerkiksi analyysinäkymiä määritettäessä. Lisätietoja on kohdassa [Toimintaohje: tietojen analysointi dimensioittain](bi-how-analyze-data-dimension.md).

## <a name="dimension-sets"></a>Dimensioyhdistelmät
Dimensioyhdistelmä on dimensioarvojen yksilöllinen yhdistelmä. Se tallennetaan dimensioyhdistelmän tapahtumiksi tietokantaan. Kukin dimensioyhdistelmän tapahtuma edustaa yksittäistä dimensioarvoa. Dimensioyhdistelmä tunnistetaan yhteisellä dimensioyhdistelmän tunnuksella, joka määritetään jokaiselle yhdistelmään kuuluvalle tapahtumalle.  

Kun luot päiväkirjarivin, asiakirjaotsikon tai asiakirjarivin, voit määrittää dimensioarvojen yhdistelmän. Sen sijaan, että tallentaisit jokaisen dimensioarvon erikseen tietokantaan, dimensioyhdistelmä määritetään päiväkirjan rivillä, asiakirjaotsikossa tai asiakirjan rivillä dimensioyhdistelmän tunnuksen avulla.  

## <a name="setting-up-dimensions"></a>Dimensioiden luominen
Voit määrittää päiväkirjojen ja asiakirjojen, kuten myynti- ja ostotilausten, luokitteluun käytettävät dimensiot ja dimension arvot. Dimensiot määritetään **Dimensiot**-ikkunassa, jossa kullekin dimensiolle luodaan yksi rivi. Dimensioita ovat esimerkiksi *Projekti*, *Osasto*, *Alue* ja *Myyjä*.

Voit määrittää myös arvoja dimensioille. Arvot voivat olla esimerkiksi yrityksen osastoja. Dimension arvot voi määrittää tilikartan kaltaisessa hierarkkisessa rakenteessa, jossa tiedot voi jakaa rakeisuustason mukaan ja jossa dimension arvojen osajoukoista voi laskea summat. Voit määrittää tarvitsemasi määrän dimensiota ja dimension arvoja, ja ne ovat yrityksessä kaikkien käytössä.

Voit määrittää myös joitakin globaaleja dimensioita ja pikadimensioita:  

* **Globaaleja dimensioita** käytetään suodattimina esimerkiksi raporteissa ja erätöissä. Käytössä on vain kaksi globaalia dimensiota, joten valitse usein käytetyt dimensiot.
* **Pikadimensiot** ovat käytössä kenttinä päiväkirjan ja asiakirjan riveillä. Voit luoda niitä enintään kuusi.  

### <a name="setting-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Oletusdimensioiden määrittäminen asiakkaille, toimittajille ja muille tileille
Voit määrittää oletusdimension tietylle tilille. Dimensio kopioidaan päiväkirjaan tai asiakirjaan, kun lisäät tilinumeron riville, mutta voit tarvittaessa poistaa koodin rivillä tai muuttaa sitä. Voit määrittää myös dimension, jota tarvitaan tietyn tyyppisen tilitapahtuman kirjaamiseen.  

### <a name="translating-the-names-of-dimensions"></a>Dimensioiden nimien kääntäminen
Dimensiota ja etenkin pikadimensiota luotaessa luodaan itse asiassa mukautettu kenttä tai sarakeotsikko. Jos kyse on kansainvälisestä yrityksestä, voit kääntää dimension nimen. Dimension sisältävät asiakirjat käyttävät tarvittaessa käännettyä nimeä.   

### <a name="example-of-dimension-setup"></a>Esimerkki dimension asetuksista
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
> [!NOTE]  
>   Hierarkian määrittämistä varten koodien on oltava aakkosjärjestyksessä. Myös [!INCLUDE[d365fin](includes/d365fin_md.md)]iin sisältyvät dimension arvojen koodit on otettava tässä huomioon.  

Lisää **OSASTO**-koodiin seuraavat dimension arvot:

| koodi | Name | Dimension arvotyyppi |
| --- | --- | --- |
| HALLINTA |Hallinta |Vakio |
| TUOT |Tuotanto |Vakio |
| MYYNTI |Myynti |Vakio |

Näillä asetuksilla voit sitten lisätä kaksi dimensiota kahtena globaalina dimensiona **Pääkirjanpidon asetukset** -ikkunassa. Niinpä voit käyttää ALUE- ja OSASTO-koodeja pääkirjanpidon tapahtumien suodattamina sekä kaikissa raporteissa ja eräajoissa. Molemmat globaalit dimensiot ovat myös automaattisesti käytettävissä pikadimensioina tapahtumariveillä ja asiakirjojen otsikoissa.  

## <a name="using-dimensions"></a>Dimensioiden käyttäminen
Voit lisätä asiakirjaan, kuten esimerkiksi myyntitilaukseen, dimension tiedot sekä yksittäiseen asiakirjariviin että itse asiakirjaan. Voit antaa esimerkiksi **Myyntitilaus**-ikkunassa kahden ensimmäisen pikadimension dimension arvot yksittäisillä myyntiriveillä. Voit myös lisätä lisää dimension tietoja valitsemalla **Dimensiot**-painikkeen.  

Jos käsittelet sen sijaan päiväkirjaa, voit lisätä dimension tietoja tapahtumaan samalla tavalla, jos olet määrittänyt pikadimensiot kentiksi suoraan päiväkirjan riveille.  

Voit määrittää tileille tai tilityypeille oletusdimensioita, jolloin dimensiot tai dimensioiden arvot täytetään automaattisesti.  

## <a name="see-also"></a>Katso myös
[Business Intelligence](bi.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

