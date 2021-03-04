---
title: Resurssien kohdistuksen määrittäminen | Microsoft Docs
description: Lisätietoja tavoista, joilla järjestelmä voi auttaa varmistamaan, että palvelun tarjoamiseen määritetyllä henkilöllä on siihen tarvittavat taidot.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 48d0f9f9e51a0da3f82abdb43e8c4bb6044a5f29
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757990"
---
# <a name="set-up-resource-allocation"></a>Resurssien kohdistamisen määrittäminen
Huoltotehtävän onnistuneen suorittamisen kannalta on tärkeää löytää resurssi, jolla on työn edellyttävät taidot. Voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)] helpottamaan työhön vaadittavat taidot omaavan henkilön kohdistamista. [!INCLUDE[prod_short](includes/prod_short.md)]issa tätä kutsutaan _resurssien kohdistamiseksi_. Resursseja voi kohdistaa taitojen tai saatavuuden perusteella tai sen perusteella, onko resurssi samalla huoltoalueella kuin asiakas. 

Resurssien kohdistaminen edellyttää seuraavia määrityksiä:  
  
* Huoltonimikkeiden korjaamiseen ja ylläpitämiseen tarvittavat taidot. Ne määritetään huoltonimikkeille ja resursseille.  
* Markkina-alueelle määritettävät alueeksi kutsutut maantieteelliset alueet. Alueita voivat olla esimerkiksi itä, länsi, etelä ja pohjoinen. Alueet määritetään asiakkaille ja toimittajille.  
* Näytetäänkö resurssin taidot ja alueet sekä näytetäänkö varoitus, jos joku valitsee resurssin, jonka ei täytä vaatimuksia tai joka ei ole asiakkaan alueella.  

## <a name="to-set-up-skills"></a>Taitojen määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Taidot** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a>Taitojen määrittäminen huoltonimikkeille ja resursseille
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltonimikkeet** tai **Resurssit** ja valitse sitten liittyvä linkki.  
2. Avaa huoltonimikkeen tai resurssin kortti ja valitse sitten jokin seuraavista:  
  
    * Valitse huoltonimikkeille **Resurssin taidot**.  
    * Valitse resursseille **Taidot**.  

## <a name="to-set-up-zones"></a>Alueiden määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Vyöhykkeet** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a>Alueiden määrittäminen asiakkaille ja resursseille 
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Asiakkaat** tai **Resurssit** ja valitse sitten liittyvä linkki.  
2. Avaa huoltonimikkeen tai resurssin kortti ja valitse sitten jokin seuraavista:  
  
    * Valitse asiakkaille alue **Huoltoalueen koodi** -kentässä.  
    * Valitse resursseille **Huoltoalueet**-toiminto.  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a>Resurssin valinnan yhteydessä näytettävien tietojen määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huollon hallinnan asetukset** ja valitse sitten liittyvä linkki. 
2. Valitse **Resurssin taitojen vaihtoehto** -kentässä jokin seuraavassa taulukossa käsiteltävistä vaihtoehdoista.  
  
    |**Vaihtoehto**|**Kuvaus**|  
    |------------|-------------|  
    |Koodi näytetty | Näyttää vain koodin.|  
    |Varoitus näytetään | Näyttää tiedot ja varoituksen, jos valitset resurssin, joka ei täytä vaatimuksia.|  
    |Ei käytetty | Nämä tiedot eivät näy.|  

## <a name="to-update-resource-capacity"></a>Resurssikapasiteetin päivittäminen  
Resurssien kapasiteetti on ehkä muutettava.  
  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Resurssikapasiteetti** ja valitse sitten liittyvä linkki.  
2. Valitse ensin resurssi ja sitten **Aseta kapasiteetti** -toiminto.  
3. Tee muutokset ja valitse sitten **Päivitä kapasiteetti**.  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a>Nimikkeiden, huoltonimikkeiden tai huoltonimikeryhmien taitojen päivittäminen
Jos haluat muuttaa nimikkeille määritettyjä taitokoodeja (vaikkapa **kpl** eikä **PC**), voit tehdä muutoksen joko nimikkeelle, huoltonimikkeelle tai huoltonimikeryhmän kaikille nimikkeille.  
  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet**, **Huoltonimike** tai **Huoltonimikeryhmä** ja valitse sitten liittyvä linkki.  
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
 



[!INCLUDE[footer-include](includes/footer-banner.md)]