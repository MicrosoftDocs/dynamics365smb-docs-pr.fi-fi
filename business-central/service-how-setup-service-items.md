---
title: "Huoltonimikkeiden ja huoltonimikkeen komponenttien määrittäminen | Microsoft Docs"
description: "Lisätietoja määrityksistä, jotka on tehtävä ennen huoltonimikkeiden käyttöä. Esimerkiksi oletusarvot, kuten vastausaika, sopimusalennusprosentti ja huoltohintaryhmä, on määritettävä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e946bab348aeee1b65b85165b2d9d553736813ba
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-service-items-and-service-item-components"></a>Huoltonimikkeiden ja huoltonimikkeen komponenttien määrittäminen
Huoltonimikkeiden käyttöä varten on määritettävä seuraavat asetukset

* Huoltonimikeryhmät.
* Valinnainen

## <a name="to-set-up-service-item-groups"></a>Huoltonimikeryhmien määrittäminen
Voit määrittää korjaus- ja ylläpitoehtoihin liittyvät nimikeryhmät. Huoltonimikeryhmässä oleville huoltonimikkeille voi määritellä oletusarvoja, kuten vastausajan, sopimusalennus-%:n ja huoltohintaryhmän. Huoltonimikeryhmässä olevien nimikkeiden osalta voi valita, halutaanko, että ne rekisteröidään automaattisesti huoltonimikkeiksi silloin, kun ne myydään.  

Huoltonimikeryhmiä määritetään **Nimike**-kortin nimikkeille ja **Huoltonimike**-kortin huoltonimikkeille.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltonimikeryhmät** ja valitse sitten liittyvä linkki.  
2. Luo uusi huoltonimikeryhmä.  
3. Täytä **Koodi**- ja **Kuvaus**-kentät.  
4. Anna **Oletus sopimusalennus-%** -kenttään oletussopimusalennusprosentti, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.  
5. Anna **Oletus huoltohintaryhmän koodi** -kenttään oletushuoltohintaryhmän koodi, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.  
6. Anna **Oletusvastausaika (tuntia)** -kenttään oletusvastausaika tunneissa, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.  
7. Jos haluat rekisteröidä ryhmän nimikkeen huoltonimikkeiksi silloin, kun ne myydään, valitse **Luo huoltonimike** -kenttä.  

## <a name="to-set-up-service-item-components"></a>Huoltonimikkeen komponenttien määrittäminen
Huoltonimike voi koostua useista komponenteista, jotka voidaan korvata varaosilla nimikettä huollettaessa. Nämä komponentit määritetään **Huoltonimikk. komponenttiluet.** -ikkunassa. Jos lisäksi haluat määrittää komponentteja huoltonimikkeille, jotka ovat tuoterakenteita, tuoterakennenimikkeet voidaan kopioida ja luoda huoltonimikkeen komponentteina.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltonimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa huoltonimike, jolle haluat määrittää komponentteja.  
3. Valitse **Komponentit**-toiminto. Näyttöön tulee **Huoltonimikk. komponenttiluet.** -ikkuna.  
4. Uuden ryhmän lisääminen  
5. Valitse **Tyyppi** -kentässä **Huoltonimike**, jos itse komponentti on rekisteröity huoltonimike. Muutoin valitse **Nimike**.  
6. Valitse **Nro**-kenttään nimike tai huoltonimike, joka on huoltonimikkeen komponentti.  

## <a name="to-set-up-service-item-components-from-a-bom"></a>Huoltonimikkeen komponenttien määrittäminen tuoterakenteista
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltonimikkeet** ja valitse sitten liittyvä linkki.  
2. Avaa huoltonimike, jolle haluat määrittää komponentteja huoltorakenteesta.  
3. Valitse **Komponentit**-toiminto. **Huoltonimikk. komponenttiluet.** -ikkuna avautuu.  
4. Valitse **Kopioi tuoterakenteesta** -toiminto.  

    Jos nimike, johon huoltonimike on linkitetty, on tuoterakenne, ohjelma luo automaattisesti komponentteja kaikille tuoterakenteessa oleville nimikkeille.  

## <a name="to-set-up-a-service-shelf"></a>Huoltohyllyn määrittäminen
Voit määrittää huoltohyllyjä, jotka ilmaisevat, mihin huoltonimikkeet varastoidaan. Huoltohyllyt määritetään huoltonimikkeille **Huoltotilaus**- ja **Huoltonimikkeen työkirja** -ikkunoissa.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltohyllyt** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät.

## <a name="see-also"></a>Katso myös
[Vakiohuoltokoodien määrittäminen](service-how-setup-service-coding.md)   
[Vianmäärityksen määrittäminen](service-how-setup-troubleshooting.md)

