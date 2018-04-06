---
title: "Resurssien kohdistuksen määrittäminen | Microsoft Docs"
description: "Lisätietoja tavoista, joilla järjestelmä voi auttaa varmistamaan, että palvelun tarjoamiseen määritetyllä henkilöllä on siihen tarvittavat taidot."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 08/22/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6dc4a059cb3bca46910a4a4be43a5940a5652c8f
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-resource-allocation"></a>Resurssien kohdistamisen määrittäminen
Huoltotehtävän onnistuneen suorittamisen kannalta on tärkeää löytää resurssi, jolla on työn edellyttävät taidot. Voit määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)] helpottamaan työhön vaadittavat taidot omaavan henkilön kohdistamista. [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tätä kutsutaan _resurssien kohdistamiseksi_. Resursseja voi kohdistaa taitojen tai saatavuuden perusteella tai sen perusteella, onko resurssi samalla huoltoalueella kuin asiakas. 

Resurssien kohdistaminen edellyttää seuraavia määrityksiä:  
  
* Huoltonimikkeiden korjaamiseen ja ylläpitämiseen tarvittavat taidot. Ne määritetään huoltonimikkeille ja resursseille.  
* Markkina-alueelle määritettävät alueeksi kutsutut maantieteelliset alueet. Alueita voivat olla esimerkiksi itä, länsi, etelä ja pohjoinen. Alueet määritetään asiakkaille ja toimittajille.  
* Näytetäänkö resurssin taidot ja alueet sekä näytetäänkö varoitus, jos joku valitsee resurssin, jonka ei täytä vaatimuksia tai joka ei ole asiakkaan alueella.  

## <a name="to-set-up-skills"></a>Taitojen määrittäminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Taidot** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a>Taitojen määrittäminen huoltonimikkeille ja resursseille
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltonimikkeet** tai **Resurssit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Avaa huoltonimikkeen tai resurssin kortti ja valitse sitten jokin seuraavista:  
  
    * Valitse huoltonimikkeille **Resurssin taidot**.  
    * Valitse resursseille **Taidot**.  

## <a name="to-set-up-zones"></a>Alueiden määrittäminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Alueet** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a>Alueiden määrittäminen asiakkaille ja resursseille 
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Asiakkaat** tai **Resurssit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Avaa huoltonimikkeen tai resurssin kortti ja valitse sitten jokin seuraavista:  
  
    * Valitse asiakkaille alue **Huoltoalueen koodi** -kentässä.  
    * Valitse resursseille **Huoltoalueet**-toiminto.  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a>Resurssin valinnan yhteydessä näytettävien tietojen määrittäminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huollon asetukset** ja valitse sitten aiheeseen liittyvä linkki. 
2. Valitse **Resurssin taitojen vaihtoehto** -kentässä jokin seuraavassa taulukossa käsiteltävistä vaihtoehdoista.  
  
    |**Vaihtoehto**|**Kuvaus**|  
    |------------|-------------|  
    |Koodi näytetty | Näyttää vain koodin.|  
    |Varoitus näytetään | Näyttää tiedot ja varoituksen, jos valitset resurssin, joka ei täytä vaatimuksia.|  
    |Ei käytetty | Nämä tiedot eivät näy.|  

## <a name="to-update-resource-capacity"></a>Resurssikapasiteetin päivittäminen  
Resurssien kapasiteetti on ehkä muutettava.  
  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Resurssikapasiteetti** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse ensin resurssi ja sitten **Aseta kapasiteetti** -toiminto.  
3. Tee muutokset ja valitse sitten **Päivitä kapasiteetti**.  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a>Nimikkeiden, huoltonimikkeiden tai huoltonimikeryhmien taitojen päivittäminen
Jos haluat muuttaa nimikkeille määritettyjä taitokoodeja (vaikkapa **kpl** eikä **PC**), voit tehdä muutoksen joko nimikkeelle, huoltonimikkeelle tai huoltonimikeryhmän kaikille nimikkeille.  
  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Nimikkeet**, **Huoltonimike** tai **Huoltonimikeryhmä**ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse ensin päivitettävä objekti ja sitten **Resurssin taidot** -toiminto.  
3. Valitse sopiva taitokoodi sen rivin **Taitokoodi**-kentässä, jolla muutettava koodi on.  
4.  Jos nimikkeellä on siihen liittyviä huoltonimikkeitä, näyttöön tulee valintaruutu, jossa on kaksi vaihtoehtoa.  
  
    * Muuta taitokoodit valituksi arvoksi: Valitse tämä vaihtoehto, jos haluat korvata vanhan taitokoodin uudella kaikissa nimikkeeseen liittyvissä huoltonimikkeissä.  
    * Poista taitokoodit tai päivitä niiden suhteet: Valitse tämä vaihtoehto, jos haluat muuttaa vain nimikkeen taitokoodin. Siihen liittyvien huoltonimikkeiden taitokoodit määritetään uudelleen, toisin sanoen **Määritetty kohteesta** -kenttä päivitetään.  
  
## <a name="see-also"></a>Katso myös
[Resurssien kohdistaminen](service-how-to-allocate-resources.md)  
[Työ- ja huoltotuntien määrittäminen](service-how-setup-work-service-hours.md)  
[Vian raportoinnin määrittäminen](service-how-setup-fault-reporting.md)  
[Vakiohuoltokoodien määrittäminen](service-how-setup-service-coding.md)  
 


