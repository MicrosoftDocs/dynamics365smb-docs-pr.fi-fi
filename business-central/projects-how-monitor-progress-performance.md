---
title: Projektin edistymisen ja suorituskyvyn valvonta
description: Tässä artikkelissa kerrotaan, miten keskeneräisen työn (KET) menetelmä luodaan ja miten KET lasketaan, kun projektien taloudellinen arvo arvioidaan projektin ollessa kesken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.search.form: 89, 92, 1010
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7c816ea6d4fa8f1653000f94e15b74f9b78db8c6
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971808"
---
# <a name="monitor-job-progress-and-performance"></a>Projektin edistymisen ja suorituskyvyn valvonta
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

> [!NOTE]
> Kun olet käyttänyt uutta tapaasi luodaksesi KET-tapahtumat, et voi enää poistaa tai muokata tapaa.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektin KET-menetelmät** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Sulje sivu.   
4. Jos haluat tehdä tästä uudesta menetelmästä oletusmenetelmän, valitse ![Kerro-ominaisuuden avaava hehkulamppu.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektienhallinnan asetukset** ja valitse sitten vastaava linkki.  
5. Valitse **Oletus KET-menetelmä** -kentässä menetelmä luettelosta.

## <a name="to-define-a-wip-method-for-a-job"></a>Määritä projektin KET-menetelmä
Kun luot uuden projektin, määritä, mihin projektin KET-menetelmään se kohdistetaan. Joissakin tapauksissa käytettävissä oleva projektin KET-menetelmä on määritetty oletusasetukseksi.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto. Lisätietoja on kohdassa [Projektien luominen](projects-how-create-jobs.md).  
3. Valitse **Projektikortti**-sivun **KET-menetelmä**-kentässä KET-menetelmä luettelosta. Vaikka oletusmenetelmä olisi määritetty, voit valita tarvittaessa toisen vaihtoehdon.  

## <a name="to-calculate-wip"></a>Keskeneräisen työn laskeminen
Voit määrittää tasetileille kirjattavan KET-summan kauden lopussa suoritettavaa raportointia varten. Tähän käytetään **Laske projektin KET** -erätyötä.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Laske projektin KET** ja valitse sitten vastaava linkki.  
2. Valitse **Laske KET** -toiminto.
3. Täytä **Laske projektin KET** -sivulla tarvittavat kentät.
4. Valitse **OK**-painike.  

> [!NOTE]  
>   Eräajo laskee ainoastaan keskeneräisen työn. Sitä ei kirjata pääkirjanpitoon. Nämä toimet edellyttävät, että suoritat **Kirjaa KET kirjanpitoon** -eräajon, kun olet laskenut keskeneräisen työn. Katso lisätietoja seuraavasta menettelystä.

## <a name="to-post-wip"></a>Keskeneräisen työn kirjaaminen
Kun keskeneräinen työ on laskettu, voit kirjata sen tasetileille jakson lopun raportointia varten. Tähän käytetään **Kirjaa projektin KET kirjanpitoon** -erätyötä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjaa projektin KET kirjanpitoon** ja valitse sitten vastaava linkki.  
2. Täytä **Kirjaa projektin KET kirjanpitoon** -sivulla tarvittavat kentät.  
3. Valitse **OK**-painike.

## <a name="to-calculate-and-post-job-completion-entries"></a>Projektin valmistumistapahtumien laskeminen ja kirjaaminen
Kun olet saanut kaikki projektin toimenpiteet, kuten käytön kirjauksen ja laskutuksen, valmiiksi, projekti on päivitettävä **tilaan** **Valmis**. Tämän jälkeen mahdollinen kirjanpitoon kirjattu KET peruuntuu.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2. Valitse avoin projekti ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Tila**-kentässä **Valmis**.
4. Laske ja kirjaa KET ohjattujen vaiheiden avulla. Vaihtoehtoisesti voit tehdä toiminnot manuaalisesti vaiheiden 5 ja 6 mukaisesti.  
5. Valitse **Laske KET** -toiminto.
6. Täytä **Laske projektin KET** -sivulla tarvittavat kentät.  

     Erätyön luomien projektin KET-tapahtumien vieressä on nyt valintamerkki **Projekti valmis** -kentässä. Valintamerkki osoittaa, että kyseessä ovat valmistumistapahtumat.  
7. Valitse **Kirjaa projektin KET kirjanpitoon** -toiminto.
8. Täytä **Kirjaa projektin KET kirjanpitoon** -sivulla tarvittavat kentät.  

     Erätyön luomien projektin pääkirjanpidon KET-tapahtumien vieressä on nyt valintamerkki **Projekti valmis** -kentässä. Valintamerkki osoittaa, että kyseessä ovat valmistumistapahtumat.

## <a name="to-view-job-ledger-entries"></a>Projektitapahtumien katsominen
Kaikki projekteihin liittyvät tapahtumat on tallennettu projektirekistereihin ja numeroitu järjestyksessä numerosta 1 alkaen. Projektirekisterissä voi saada yleiskuvan kaikista projektitapahtumista.    

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektirekisterit** ja valitse sitten vastaava linkki.
2. Valitse asianmukainen rekisteri ja valitse sitten **Projektikirjaukset**-toiminto.

**Projektitapahtumat**-sivulla voi tarkastella mihin tahansa projektiin liittyviä tapahtumia.  

## <a name="see-also"></a>Katso myös
[Projektien hallinta](projects-manage-projects.md)
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)   
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
