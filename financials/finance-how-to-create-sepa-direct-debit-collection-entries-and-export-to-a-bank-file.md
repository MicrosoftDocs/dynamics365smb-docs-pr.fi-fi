---
title: "SEPA-suoraveloitusperintä | Microsoft Docs"
description: "Luo suoraveloitusperintä ja vie XML-tiedosto, jonka voit lähettää tai ladata verkkopankkiin käsiteltäväksi."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct-debit, collection, payment, sepa
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: ff6fc3af28273545781fc96b811f3c164eaa6fd8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-create-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>Toimintaohjeet: SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon
Jos haluat ohjata pankin siirtämään maksusumman asiakkaan pankkitililtä yrityksesi tilille, luo suoraveloitusperintätapahtuma, joka säilyttää tiedot asiakkaan pankkitilistä, kyseisestä myyntilaskuista ja suoraveloitusvaltakirjasta. Syntyvästä suoraveloitusperintämerkinnästä viet sitten XML-tiedoston, jonka lähetät tai lataat verkkopankkiin käsittelyä varten. Kaikista maksuista, joita pankki ei voinut käsitellä, tiedotetaan sinulle pankin toimesta. Sinun täytyy sitten manuaalisesti hylätä kyseessä olevat suoraveloitusmerkinnät.  

> [!NOTE]  
>  Kun maksut kerätään SEPA-suoraveloituksen avulla, myyntilaskun valuutan on oltava EURO.  

### <a name="to-create-a-direct-debit-collection"></a>Suoraveloitusperinnän luominen  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Suoraveloitusperinnät** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Suoraveloitusperinnät**-ikkunan **Koti**-välilehden **Uusi**-ryhmässä **Luo suoraveloitusperintä**.  
3. Täytä **Luo suoraveloitusperintä** -ikkunan kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Eräpäivästä**|Määritä maksun aikaisin eräpäivä myyntilaskuille, joille haluat luoda suoraveloitusperinnän.|  
    |**Eräpäivään**|Määritä myöhäisin maksun eräpäivä myyntilaskuille, joille haluat luoda suoraveloitusperinnän.|  
    |**Kumppanin tyyppi**|Määrittää, suoritetaanko suoraveloitusperintä asiakkaille, joiden tyyppi on **yritys** vain **henkilö**.|  
    |**Vain asiakkaat, joilla on kelvollinen valtakirja**|Määritä, luodaanko suoraveloitus asiakkaille, joilla on voimassa oleva suoraveloitusvaltakirja. **Huomautus:** Suoraveloitusperintä luodaan, vaikka **Suoraveloitusvaltakirjan tunnus** -kenttää ei olisi täytetty myyntilaskussa.|  
    |**Vain laskut, joilla on kelvollinen valtakirja**|Määritä, luodaanko suoraveloitusperintä vain myyntilaskuille, jos myyntilaskun **Suoraveloitusvaltakirjan tunnus** -kentässä on valittu sallittu suoraveloitusvaltakirja.|  
    |**Pankkitilin nro**|Määritä, mille yrityksen pankkitilille perityt maksut siirretään asiakkaan pankkitililtä.|  
    |**Pankkitilin nimi**|Määrittää pankkitilin nimen, jonka valitset **Pankkitilin nro** -kentässä. Tämä kenttä täytetään automaattisesti.|  

4. Valitse **OK**-painike.  

     Suoraveloitusperintä lisätään **Suoraveloitusperinnät**-ikkunaan ja vähintään yksi suoraveloitusperintätapahtuma luodaan.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Suoraveloitusperintätapahtuman vieminen pankkitiedostoon  
1. Valitse **Suoraveloitusperinnät**-ikkunan **Kotisivu**-välilehden **Käsittely**-ryhmässä **Suoraveloitusperintätapahtumat**.  
2. Valitse **Suoraveloitusperintätapahtumat** -ikkunassa merkintä, jonka haluat viedä ja valitse sitten **Koti**-välilehden **Käsittely**-ryhmässä **Luo suoraveloitustiedosto**.  
3. Tallenna vientitiedosto paikkaan, josta lähetät tai lataat sen verkkopankkiisi.  

     **Suoraveloitusperintätapahtumat**-ikkunan **Suoraveloitusperinnän tila** -kentän arvoksi muutetaan Tiedosto luotu. **SEPA-suoraveloitusvaltakirja**-ikkunan **Debet-laskuri**-kentän arvoa nostetaan yhdellä.  

Jos vietyä tiedostoa ei voi käsitellä, esimerkiksi sen vuoksi, että asiakkaan pankkitilillä ei ollut riittävästi varoja, voit hylätä suoraveloitusperintämerkinnän. Jos pankki käsitteli vientitiedoston onnistuneesti, kyseessä olevien myyntilaskujen erääntyneet maksut kerätään automaattisesti kyseisiltä asiakkailta. Tässä tapauksessa voit sulkea perinnän.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Suoraveloitusperintätapahtuman hylkääminen  
* Valitse **Suoraveloitusperintätapahtumat**-ikkunassa tapahtuma, jonka käsittely ei onnistunut ja valitse sitten **Kotisivu**-välilehden **Käsittely**-ryhmässä **Hylkää tapahtuma**.  

     **Suoraveloitusperintätapahtumat**-ikkunan **Tila**-kentän arvoksi muutetaan **Hylätty**.  

### <a name="to-close-a-direct-debit-collection"></a>Suoraveloitusperinnän sulkeminen  
* Valitse **Suoraveloitusperintätapahtumat**-ikkunassa tapahtuma, jonka käsittely ei onnistunut, ja valitse sitten **Kotisivu**-välilehden **Käsittely**-ryhmässä **Sulje kokoelma**.  

     Liittyvä suoraveloitusperintä suljetaan.  

Voit nyt kirjata kyseisten myyntilaskujen maksukuitit. Voit tehdä tämän, kun yleensä kirjaat maksukuitteja, kuten **Maksurekisteröinti**-ikkunassa, tai voit kirjata liittyvät maksukuitit suoran **Suoraveloitusperintätapahtumat**-ikkunasta. Lisätietoja on kohdassa [SEPA-suoraveloitusmaksujen kirjaaminen](finance-how-to-post-sepa-direct-debit-payment-receipts.md).  

## <a name="see-also"></a>Katso myös  
[Toimintaohje: SEPA-suoraveloituksen määrittäminen](finance-how-to-set-up-sepa-direct-debit.md)   
[Toimintaohje: Kuinka SEPA-suoraveloitusmaksut kirjataan](finance-how-to-post-sepa-direct-debit-payment-receipts.md)   
[Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md)   

