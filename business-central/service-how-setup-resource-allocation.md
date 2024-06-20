---
title: Resurssien kohdistuksen määrittäminen | Microsoft Docs
description: 'Lisätietoja tavoista, joilla järjestelmä voi auttaa varmistamaan, että palvelun tarjoamiseen määritetyllä henkilöllä on siihen tarvittavat taidot.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'resource, skill, service, zones'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Resurssien kohdistamisen määrittäminen
Huoltotehtävän onnistuneen suorittamisen kannalta on tärkeää löytää resurssi, jolla on työn edellyttävät taidot. Voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)] helpottamaan työhön vaadittavat taidot omaavan henkilön kohdistamista. [!INCLUDE[prod_short](includes/prod_short.md)]issa tätä kutsutaan _resurssien kohdistamiseksi_. Resursseja voi kohdistaa taitojen tai saatavuuden perusteella tai sen perusteella, onko resurssi samalla huoltoalueella kuin asiakas. 

Resurssien kohdistaminen edellyttää seuraavia määrityksiä:  
  
* Huoltonimikkeiden korjaamiseen ja ylläpitämiseen tarvittavat taidot. Ne määritetään huoltonimikkeille ja resursseille.  
* Markkina-alueelle määritettävät alueeksi kutsutut maantieteelliset alueet. Alueita voivat olla esimerkiksi itä, länsi, etelä ja pohjoinen. Alueet määritetään asiakkaille ja toimittajille.  
* Näytetäänkö resurssin taidot ja alueet sekä näytetäänkö varoitus, jos joku valitsee resurssin, jonka ei täytä vaatimuksia tai joka ei ole asiakkaan alueella.  

## Taitojen määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Taidot** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Taitojen määrittäminen huoltonimikkeille ja resursseille
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltonimikkeet** tai **Resurssit** ja valitse sitten vastaava linkki.  
2. Avaa huoltonimikkeen tai resurssin kortti ja valitse sitten jokin seuraavista:  
  
    * Valitse huoltonimikkeille **Resurssin taidot**.  
    * Valitse resursseille **Taidot**.  

## Alueiden määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Alueet** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Alueiden määrittäminen asiakkaille ja resursseille 
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** tai **Resurssit** ja valitse sitten vastaava linkki.  
2. Avaa huoltonimikkeen tai resurssin kortti ja valitse sitten jokin seuraavista:  
  
    * Valitse asiakkaille alue **Huoltoalueen koodi** -kentässä.  
    * Valitse resursseille **Huoltoalueet**-toiminto.  

## Resurssin valinnan yhteydessä näytettävien tietojen määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltohallinnon asetukset** ja valitse sitten vastaava linkki. 
2. Valitse **Resurssin taitojen vaihtoehto** -kentässä jokin seuraavassa taulukossa käsiteltävistä vaihtoehdoista.  
  
    |**Vaihtoehto**|**Kuvaus**|  
    |------------|-------------|  
    |Koodi näytetty | Näyttää vain koodin.|  
    |Varoitus näytetään | Näyttää tiedot ja varoituksen, jos valitset resurssin, joka ei täytä vaatimuksia.|  
    |Ei käytetty | Nämä tiedot eivät näy.|  

## Resurssikapasiteetin päivittäminen  
Resurssien kapasiteetti on ehkä muutettava.  
  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssin kapasiteetti** ja valitse sitten vastaava linkki.  
2. Valitse ensin resurssi ja sitten **Aseta kapasiteetti** -toiminto.  
3. Tee muutokset ja valitse sitten **Päivitä kapasiteetti**.  

## Nimikkeiden, huoltonimikkeiden tai huoltonimikeryhmien taitojen päivittäminen
Jos haluat muuttaa nimikkeille määritettyjä taitokoodeja (vaikkapa **kpl** eikä **PC**), voit tehdä muutoksen joko nimikkeelle, huoltonimikkeelle tai huoltonimikeryhmän kaikille nimikkeille.  
  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** tai **Huoltonimike** tai **Huoltonimikeryhmä** ja valitse sitten liittyvä linkki.  
2. Valitse ensin päivitettävä objekti ja sitten **Resurssin taidot** -toiminto.  
3. Valitse sopiva taitokoodi sen rivin **Taitokoodi**-kentässä, jolla muutettava koodi on.  
4.  Jos nimikkeellä on siihen liittyviä huoltonimikkeitä, näyttöön tulee valintaruutu, jossa on kaksi vaihtoehtoa.  
  
    * Muuta taitokoodit valituksi arvoksi: Valitse tämä vaihtoehto, jos haluat korvata vanhan taitokoodin uudella kaikissa nimikkeeseen liittyvissä huoltonimikkeissä.  
    * Poista taitokoodit tai päivitä niiden suhteet: Valitse tämä vaihtoehto, jos haluat muuttaa vain nimikkeen taitokoodin. Siihen liittyvien huoltonimikkeiden taitokoodit määritetään uudelleen, toisin sanoen **Määritetty kohteesta** -kenttä päivitetään.  
  
## Katso myös
[Resurssien kohdistaminen](service-how-to-allocate-resources.md)  
[Työ- ja huoltotuntien määrittäminen](service-how-setup-work-service-hours.md)  
[Vian raportoinnin määrittäminen](service-how-setup-fault-reporting.md)  
[Vakiohuoltokoodien määrittäminen](service-how-setup-service-coding.md)  
 



[!INCLUDE[footer-include](includes/footer-banner.md)]