---
title: Dimensiot| Microsoft Docs
description: "Dimensioiden käyttäminen tietojen analysoimisessa."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7552ee2b3398c203a7f3295f3203c83914fbb15f
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="dimensions"></a>Dimensiot
Voit yksinkertaistaa asiakirjojen, kuten myyntitilausten, analysointia dimensioiden avulla. Dimensiot ovat tapahtumia luokittelevia määritteitä ja arvoja, joita voi seurata ja analysoida. Dimensioiden avulla voit esimerkiksi ilmaista, mistä projektista tai osastosta tapahtuma on lähtöisin.  

Jos käytät dimensioita, sinun ei esimerkiksi tarvitse määrittää erillisiä kirjanpitotilejä kullekin osastolle ja projektille. Tämä mahdollistaa monipuolinen analysoinnin ilman monimutkaisen tilikartan luontia.  

Voit myös esimerkiksi määrittää *Osasto*-nimisen dimension ja käyttää sitä myyntiasiakirjojen kirjaamisen yhteydessä. Voit sitten käyttää BI-työkaluja, jos haluat selvittää, mitä nimikkeitä kukin osasto myy.
Mitä useampia dimensioita käytät, sitä yksityiskohtaisempia raportteja voit käyttää liiketoimintapäätösten apuna. Yksittäisessä myyntitapahtumassa voi esimerkiksi olla useita dimensiotietoja, kuten  

* tili, jolle nimikkeen myynti on kirjattu  
* nimikkeen myyntipaikka
* nimikkeen myyjä
* nimikkeen ostaneen asiakkaan tyyppi.  

Voit määrittää itse, kuinka monta dimensiota haluat luoda ja kuinka montaa arvoa haluat dimensioissa käyttää.  

**Huomautus**: Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]-kokemuksen mukauttaminen](ui-experiences.md).

## <a name="using-dimensions"></a>Dimensioiden käyttäminen
Voit lisätä asiakirjaan, kuten esimerkiksi myyntitilaukseen, dimension tiedot sekä yksittäiseen asiakirjariviin että itse asiakirjaan. Voit antaa esimerkiksi **Myyntitilaus**-ikkunassa kahden ensimmäisen pikadimension dimension arvot yksittäisillä myyntiriveillä.. Voit myös lisätä lisää dimension tietoja valitsemalla **Dimensiot**-painikkeen.  

Jos käsittelet sen sijaan päiväkirjaa, voit lisätä dimension tietoja tapahtumaan samalla tavalla, jos olet määrittänyt pikadimensiot kentiksi suoraan päiväkirjan riveille.  

Voit määrittää tileille tai tilityypeille oletusdimensioita, jolloin dimensiot tai dimensioiden arvot täytetään automaattisesti.  

## <a name="dimension-sets"></a>Dimensioyhdistelmät
Dimensioyhdistelmä on dimensioarvojen yksilöllinen yhdistelmä. Se tallennetaan dimensioyhdistelmän tapahtumiksi tietokantaan. Kukin dimensioyhdistelmän tapahtuma edustaa yksittäistä dimensioarvoa. Dimensioyhdistelmä tunnistetaan yhteisellä dimensioyhdistelmän tunnuksella, joka määritetään jokaiselle yhdistelmään kuuluvalle tapahtumalle.  

Kun luot päiväkirjarivin, asiakirjaotsikon tai asiakirjarivin, voit määrittää dimensioarvojen yhdistelmän. Sen sijaan, että tallentaisit jokaisen dimensioarvon erikseen tietokantaan, dimensioyhdistelmä määritetään päiväkirjan rivillä, asiakirjaotsikossa tai asiakirjan rivillä dimensioyhdistelmän tunnuksen avulla.  

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Dimensioiden määrittäminen](finance-setup-dimensions.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  

