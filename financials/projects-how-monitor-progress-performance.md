---
title: 'Toimintaohje: Projektin edistymisen ja suorituskyvyn valvonta| Microsoft Docs'
description: "Tässä artikkelissa kerrotaan, miten projektit budjetoidaan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: fb38a02bbf2dd99ce003d23c4a5f88f0e3cd593a
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-monitor-job-progress-and-performance"></a>Toimintaohje: Projektin edistymisen ja suorituskyvyn valvonta
Projektin edetessä kulutetaan materiaaleja, resursseja ja muita kuluja, ja nämä on kirjattava projektiin. Keskeneräinen työ (KET) on ominaisuus, jonka avulla voit arvioida kirjanpidossa olevien projektien taloudellisen arvon projektin ollessa meneillään. Monissa tapauksissa saatat kirjata projektille kuluja ennen projektin laskuttamista. Kun projektista on kirjattu vain kuluja, rahoituslaskelma on epätarkka. Lisätietoja on kohdassa [Tietoja KET-menetelmistä](projects-understanding-wip.md).

Voit seurata arvoa kirjanpidossa laskemalla KET:n ja kirjaamalla arvon kirjanpitoon.

Voit laskea KET:n seuraavien arvojen perusteella:

* kustannusarvo
* myyntiarvo
* tuloutettavat kustannukset
* valmistumisen prosenttiosuus
* valmis sopimus.

Jos haluat tarkastella tulosta jollakin muulla menetelmällä, voit vaihtaa menetelmää ja laskea KET:n uudelleen. KET:n laskentakertojen määrää ei ole rajoitettu. Ohjelma laskee KET:n mutta ei kirjaa sitä kirjanpitoon. Kun olet laskenut KET:n, voit kirjata sen kirjanpitoon.

## <a name="to-create-a-job-wip-method"></a>Projektin KET-menetelmän luominen
Voit luoda projektin KET-menetelmän, joka kuvastaa organisaatiosi tarpeita. Luonnin jälkeen voit määrittää sen projektin oletusarvoiseksi KET-laskentamenetelmäksi, jota käytetään organisaatiossa.  

**Huomautus**. Kun olet käyttänyt uutta tapaasi luodaksesi KET-tapahtumat, et voi enää poistaa tai muokata tapaa.  

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektin KET-menetelmät** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Sulje ikkuna.   
4. Jos haluat tehdä tästä uudesta menetelmästä oletusmenetelmän, valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektienhallinnan asetukset** ja valitse sitten liittyvä linkki.  
5. Valitse **Oletus KET-menetelmä** -kentässä menetelmä luettelosta.

## <a name="to-define-a-wip-method-for-a-job"></a>Määritä projektin KET-menetelmä
Kun luot uuden projektin, määritä, mihin projektin KET-menetelmään se kohdistetaan. Joissakin tapauksissa käytettävissä oleva projektin KET-menetelmä on määritetty oletusasetukseksi.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektit** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Lisätietoja on kohdassa [Toimintaohje: Projektien luominen](projects-how-create-jobs.md).  
3. Valitse **Projektikortti**-ikkunan **KET-menetelmä**-kentässä KET-menetelmä luettelosta. Vaikka oletusmenetelmä olisi määritetty, voit valita tarvittaessa toisen vaihtoehdon.  

## <a name="to-calculate-wip"></a>Keskeneräisen työn laskeminen
Voit määrittää tasetileille kirjattavan KET-summan kauden lopussa suoritettavaa raportointia varten. Tähän käytetään **Laske projektin KET** -erätyötä.  

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Laske projektin KET** ja valitse sitten liittyvä linkki.  
2. Valitse **Laske KET** -toiminto.
3. Täytä **Laske projektin KET** -ikkunassa tarvittavat kentät.
4. Valitse **OK**-painike.  

**Huomautus**: Eräajo laskee ainoastaan keskeneräisen työn. Sitä ei kirjata pääkirjanpitoon. Nämä toimet edellyttävät, että suoritat **Kirjaa KET kirjanpitoon** -eräajon, kun olet laskenut keskeneräisen työn. Katso lisätietoja seuraavasta menettelystä.

## <a name="to-post-wip"></a>Keskeneräisen työn kirjaaminen
Kun keskeneräinen työ on laskettu, voit kirjata sen tasetileille jakson lopun raportointia varten. Tähän käytetään **Kirjaa projektin KET kirjanpitoon** -erätyötä.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Kirjaa projektin KET kirjanpitoon** ja valitse sitten liittyvä linkki.  
2. Täytä **Kirjaa projektin KET kirjanpitoon** -ikkunassa tarvittavat kentät.  
3. Valitse **OK**-painike.

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Projektin käytön arvioiden tarkasteleminen ja päivitysten kirjaaminen
Voit katsella projektin käyttöä projektin valmistumiseen asti yhden vaiheen avulla. Tämä tapahtuu käyttämällä **Laske projektin jäljellä oleva käyttö** -eräajoa kaikissa tehtävissä projektin alusta loppuun.  

Näin voit seurata ja vertailla alkuperäisiä arvioita todellisiin tuloksiin. Voit myös tehdä tarvittaessa muutoksia tai uusia tapahtumia. Olet esimerkiksi saattanut arvioida projektin kestoksi 10 tuntia, mutta aikaa on kulunut jo 15 tuntia. Voit lisätä viisi tuntia aiemmin luotuun päiväkirjariviin tai luoda uuden rivin, jolla nämä viisi tuntia raportoidaan ylityönä, joka on toinen työtyyppi. Sitten lasketaan oikeat kustannukset ja hinta, jotka voidaan kirjata päiväkirjaan.  

**Huomautus**: Nimiketapahtumat luovat nimiketapahtumia ja vähentävät varastomäärää. **Kirjaa varaston kustannus KP:oon** -eräajo siirtää kustannuksen varastosta pääkirjanpitoon. Resurssitapahtumat luovat resurssitapahtumia.  

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektipäiväkirjat** ja valitse sitten liittyvä linkki.  
2. Valitse asianmukaisen projektin päiväkirja ja valitse sitten **Laske jäljellä oleva käyttö** -toiminto.  
3. Syötä **Laske projektin jäljellä oleva käyttö** -ikkunassa päiväkirjaan lisättävä asiakirjan numero ja kirjauspäivämäärä. Valitse sitten **OK**-painike.  
4. Päivitä tarvittavat muutokset päiväkirjaan.  
5. Valitse **Kirjaa**.

## <a name="to-view-job-ledger-entries"></a>Projektitapahtumien katsominen
Kaikki projekteihin liittyvät tapahtumat on tallennettu projektirekistereihin ja numeroitu järjestyksessä numerosta 1 alkaen. Projektirekisterissä voi saada yleiskuvan kaikista projektitapahtumista.    

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektirekisterit** ja valitse sitten liittyvä linkki.
2. Valitse asianmukainen rekisteri ja valitse sitten **Projektikirjaukset**-toiminto.

**Projektitapahtumat**-ikkunassa voit tarkastella mihin tahansa projektiin liittyviä tapahtumia.  

## <a name="see-also"></a>Katso myös
[Projektien hallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  

