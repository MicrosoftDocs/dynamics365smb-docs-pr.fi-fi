---
title: "SEPA-suoraveloitusperintätapahtumien vieminen| Microsoft Docs"
description: "Luo suoraveloitusperintä, joka sisältää tietoja asiakkaan pankkitilistä, kyseessä olevista myyntilaskuista ja suoraveloitusvaltakirjasta."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 9790f75e9be5ec96a57320e96dd0cd38d567c16f
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="create-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon
Jos haluat ohjata pankin siirtämään maksusumman asiakkaan pankkitililtä yrityksesi tilille, luo suoraveloitusperintätapahtuma, joka säilyttää tiedot asiakkaan pankkitilistä, kyseisestä myyntilaskuista ja suoraveloitusvaltakirjasta. Syntyvästä suoraveloitusperintämerkinnästä viet sitten XML-tiedoston, jonka lähetät tai lataat verkkopankkiin käsittelyä varten. Kaikista maksuista, joita pankki ei voinut käsitellä, tiedotetaan sinulle pankin toimesta. Sinun täytyy sitten manuaalisesti hylätä kyseessä olevat suoraveloitusmerkinnät.  

> [!NOTE]  
>  Kun maksut kerätään SEPA-suoraveloituksen avulla, myyntilaskun valuutan on oltava EURO.  

### <a name="to-create-a-direct-debit-collection"></a>Suoraveloitusperinnän luominen  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Suoraveloitusperinnät** ja valitse sitten liittyvä linkki.  
2. Valitse **Suoraveloitusperinnät**-sivun **Koti**-välilehden **Uusi**-ryhmässä **Luo suoraveloitusperintä**.  
3. Täytä **Luo suoraveloitusperintä**-sivun kentät seuraavassa taulukossa kuvatulla tavalla.  

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

     Suoraveloitusperintä lisätään **Suoraveloitusperinnät**-sivulle ja vähintään yksi suoraveloitusperintätapahtuma luodaan.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Suoraveloitusperintätapahtuman vieminen pankkitiedostoon  
1. Valitse **Suoraveloitusperinnät**-sivun **Kotisivu**-välilehden **Käsittely**-ryhmässä **Suoraveloitusperintätapahtumat**.  
2. Valitse **Suoraveloitusperintätapahtumat**-sivulla merkintä, jonka haluat viedä, ja valitse sitten **Koti**-välilehden **Käsittely**-ryhmässä **Luo suoraveloitustiedosto**.  
3. Tallenna vientitiedosto paikkaan, josta lähetät tai lataat sen verkkopankkiisi.  

     **Suoraveloitusperintätapahtumat**-sivun **Suoraveloitusperinnän tila** -kentän arvoksi muutetaan Tiedosto luotu. **Suoraveloitusvaltakirjat**-sivun **Debet-laskuri**-kentän arvoa nostetaan yhdellä.  

Jos vietyä tiedostoa ei voi käsitellä, esimerkiksi sen vuoksi, että asiakkaan pankkitilillä ei ollut riittävästi varoja, voit hylätä suoraveloitusperintämerkinnän. Jos pankki käsitteli vientitiedoston onnistuneesti, kyseessä olevien myyntilaskujen erääntyneet maksut kerätään automaattisesti kyseisiltä asiakkailta. Tässä tapauksessa voit sulkea perinnän.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Suoraveloitusperintätapahtuman hylkääminen  

* Valitse **Suoraveloitusperintätapahtumat**-sivulla tapahtuma, jonka käsittely ei onnistunut, ja valitse sitten **Kotisivu**-välilehden **Käsittely**-ryhmässä **Hylkää tapahtuma**.  

     **Suoraveloitusperintätapahtumat**-sivun **Tila**-kentän arvoksi muutetaan **Hylätty**.  

### <a name="to-close-a-direct-debit-collection"></a>Suoraveloitusperinnän sulkeminen  
*  Valitse **Suoraveloitusperintätapahtumat**-sivulla tapahtuma, jonka käsittely ei onnistunut, ja valitse sitten **Kotisivu**-välilehden **Käsittely**-ryhmässä **Sulje kokoelma**.  

     Liittyvä suoraveloitusperintä suljetaan.  

Voit nyt siirtyä kirjaamaan mukana olevien myyntilaskujen maksukuitit. Voit tehdä tämän, kun yleensä kirjaat maksukuitteja, kuten **Maksurekisteröinti**-sivulla, tai voit kirjata liittyvät maksukuitit suoraan **Suoraveloitusperintätapahtumat**-sivulta. Lisätietoja on kohdassa [SEPA-suoraveloitusmaksujen kirjaaminen](finance-how-to-post-sepa-direct-debit-payment-receipts.md).  

## <a name="see-also"></a>Katso myös  
[SEPA-suoraveloituksen määrittäminen](finance-how-to-set-up-sepa-direct-debit.md)  
[SEPA-suoraveloitusmaksujen kirjaaminen](finance-how-to-post-sepa-direct-debit-payment-receipts.md)  
[Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md)  

