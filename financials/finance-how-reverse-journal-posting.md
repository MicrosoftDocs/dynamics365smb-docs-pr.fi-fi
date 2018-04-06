---
title: Kirjauksen kumoaminen kirjaamalla palautustapahtuma| Microsoft Docs
description: "Jos olet tehnyt virheellisen kirjauksen yleiseen päiväkirjaan, Peruuta tapahtuma -toiminnolla kumottu kirjaus luo oikean kirjausketjun."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 08/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 66fcd6282f02d5789b12b79467ec177817422c5c
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="reverse-postings"></a>Kirjausten peruuttaminen
Voit kumota virheellisen kirjauksen päiväkirjaan valitsemalla tapahtuman luomalla peruutustapahtuman (alkuperäistä tapahtumaa vastaava tapahtuma, jossa summakentässä on vastakkainen etumerkki), jossa on sama asiakirjanumero ja kirjauspäivämäärä kuin alkuperäisessä tapahtumassa. Kun olet peruuttanut tapahtuman, lisää tapahtuma korjattuna.

Vain yleisen päiväkirjan riviltä kirjatut tapahtumat voi peruuttaa. Tapahtuman voi peruuttaa vain kerran.

Lisätietoja yleisestä päiväkirjasta tehtävistä kirjauksista on kohdassa [Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md).

Jos olet tehnyt virheellinen negatiivisen määräkirjauksen, kuten kirjannut ostotilaukselle väärän määrän vastaanotetuksi mutta ei laskutetuksi, voit kumota kirjauksen.

Jos olet tehnyt virheellinen positiivisen määräkirjauksen, kuten kirjannut ostopalautustilaukselle väärän määrän toimitetuksi mutta ei laskutetuksi, voit kumota kirjauksen.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Pääkirjanpidon tapahtuman päiväkirjakirjauksen peruuttaminen
Tapahtumia voi peruuttaa kaikista **Tapahtumakirjaukset**-ikkunoista. Seuraava menettely perustuu **Pääkirjanpidon tapahtumat** -ikkunaan.
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Pääkirjanpidon tapahtumat** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse ensin peruutettava tapahtuma ja sitten **Peruuta tapahtuma** -toiminto. Huomaa, että sen on oltava peräisin päiväkirjan kirjauksesta.
3. Valitse **Peruuta tapahtumat** -ikkunassa käsiteltävä tapahtuma ja valitse sitten **Peruuta**-toiminto.
4. Valitse vahvistusviestissä **Kyllä**.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Kirjatun ostovastaanoton määrän kirjauksen kumoaminen  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kirjatut ostovastaanotot** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Avaa kirjattu vastaanotto, jonka haluat kumota.  
3.  Valitse kumottavat rivit.  
4.  Valitse **Peruuta vast.otto** -toiminto.

    Korjaava rivi lisätään valitun kuittirivin alle.  

    Jos määrä vastaanotettiin fyysisen varastoinnin vastaanottona, korjaava rivi lisätään kirjattuun fyysisen varastoinnin vastaanottoon.  

    **Vastaanotettu määrä** ja **Vast.otettu laskuttamaton määrä** -kenttien arvoiksi liittyvällä ostotilauksella asetetaan nolla.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Kirjatun palautustoimituksen määrän kirjauksen kumoaminen ja tekeminen uudelleen

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kirjatut palautustoimitukset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Avaa kumottava kirjattu palautustoimitus.
3. Valitse kumottavat rivit.  

4.  Valitse **Peruuta palautustoimitus** -toiminto.  

    Ohjelma syöttää korjaavan rivin kirjatulle asiakirjalle ja **Toimitettu palautusmäärä** ja **Pal.määrä toimitettu ei laskutettu** -kentät palautustilauksella asetetaan nollaksi.  

    Palaa nyt ostopalautustilaukseen ja tee kirjaus uudelleen.  

5.  Kirjoita muistiin numero, joka on **Kirjattu palautustoimitus** -ikkunan **Palautustilauksen nro** -kentässä.  
6.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostopalautustilaus** ja valitse sitten aiheeseen liittyvä linkki.  
7.  Avaa kyseinen palautustilaus ja valitse **Avaa uudelleen** -toiminto.  
8.  Korjaa tapahtuma **Määrä**-kentässä ja kirjaa ostopalautustilaus uudelleen.  

## <a name="to-post-a-negative-entry"></a>Negatiivisen tapahtuman kirjaaminen  
**Korjaus**-kentän avulla voit kirjata tilille negatiivisen debetin kreditin sijaan tai negatiivisen kreditin debetin sijaan. Tämä kenttä näkyy oletusarvoisesti kaikissa kirjauskansioissa, jotta lainsäädännölliset vaatimukset täytetään. **Debet-summa**- ja **Kredit-summa**-kentät sisältävät sekä alkuperäisen että korjatun tapahtuman. Kentät eivät vaikuta tilin saldoon.  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten aiheeseen liittyvä linkki  
2.  Valitse haluttu erän nimi **Erän nimi** -kentässä.  
3.  Lisää tiedot asianmukaisiin kenttiin.  
4.  Valitse **Korjaus**-valintaruutu sen kirjauskansion rivillä, jonka haluat ottaa käyttöön negatiivisia tapahtumia varten.  
5.  Kirjaa kirjauskansio valitsemalla **Kirjaa**-toiminto ja valitsemalla sitten **Kyllä**-painike.

## <a name="see-also"></a>Katso myös
[Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

