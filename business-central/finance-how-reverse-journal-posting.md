---
title: Kirjauksen kumoaminen kirjaamalla palautustapahtuma| Microsoft Docs
description: Jos olet tehnyt virheellisen kirjauksen yleiseen päiväkirjaan, Peruuta tapahtuma -toiminnolla kumottu kirjaus luo oikean kirjausketjun.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 808459f9c77d797c58a5956a5641c97bc398734e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306210"
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a>Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen
Voit kumota virheellisen kirjauksen päiväkirjaan valitsemalla tapahtuman luomalla peruutustapahtuman (alkuperäistä tapahtumaa vastaava tapahtuma, jossa summakentässä on vastakkainen etumerkki), jossa on sama asiakirjanumero ja kirjauspäivämäärä kuin alkuperäisessä tapahtumassa. Kun olet peruuttanut tapahtuman, lisää tapahtuma korjattuna.

Vain yleisen päiväkirjan riviltä kirjatut tapahtumat voi peruuttaa. Tapahtuman voi peruuttaa vain kerran.

Voit kumota vastaanoton tai toimituksen kirjauksen ennen niiden kirjaamista laskutettuina käyttämällä kirjatun asiakirjan **Kumoa**-toimintoa. Voit kumota **Nimike**-tyypin määriä.

Jos olet tehnyt virheellisen negatiivisen määräkirjauksen, kuten kirjannut ostotilaukselle väärän määrän vastaanotetuksi mutta ei laskutetuksi, voit kumota kirjauksen.

Jos olet tehnyt virheellisen positiivisen määräkirjauksen, kuten kirjannut myyntitoimitukselle tai ostopalautustoimitukselle väärän määrän toimitetuksi mutta ei laskutetuksi, voit kumota kirjauksen.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Pääkirjanpidon tapahtuman päiväkirjakirjauksen peruuttaminen
Tapahtumia voi peruuttaa kaikista **Tapahtumakirjaukset**-sivuilta. Seuraava menettely perustuu **Pääkirjanpidon tapahtumat** -sivuun.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon tapahtumat** ja valitse sitten liittyvä linkki.
2. Valitse ensin peruutettava tapahtuma ja sitten **Peruuta tapahtuma** -toiminto. Huomaa, että sen on oltava peräisin päiväkirjan kirjauksesta.
3. Valitse **Peruuta tapahtumat** -sivulla käsiteltävä tapahtuma ja valitse sitten **Peruuta**-toiminto.
4. Valitse vahvistusviestissä **Kyllä**.

## <a name="to-post-a-negative-entry"></a>Negatiivisen tapahtuman kirjaaminen  
**Korjaus**-kentän avulla voit kirjata tilille negatiivisen debetin kreditin sijaan tai negatiivisen kreditin debetin sijaan. Tämä kenttä näkyy oletusarvoisesti kaikissa kirjauskansioissa, jotta lainsäädännölliset vaatimukset täytetään. **Debet-summa**- ja **Kredit-summa**-kentät sisältävät sekä alkuperäisen että korjatun tapahtuman. Kentät eivät vaikuta tilin saldoon.  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten liittyvä linkki  
2.  Valitse haluttu erän nimi **Erän nimi** -kentässä.  
3.  Lisää tiedot asianmukaisiin kenttiin.  
4.  Valitse **Korjaus**-valintaruutu sen kirjauskansion rivillä, jonka haluat ottaa käyttöön negatiivisia tapahtumia varten.  
5.  Kirjaa kirjauskansio valitsemalla **Kirjaa**-toiminto ja valitsemalla sitten **Kyllä**-painike.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Kirjatun ostovastaanoton määrän kirjauksen kumoaminen  
Seuraavaksi kerrotaan, miten kirjattu vastaanotto kumotaan. Vaiheet ovat samankaltaisia kirjatuissa toimituksissa.

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut ostovastaanotot** ja valitse sitten liittyvä linkki.  
2.  Avaa kirjattu vastaanotto, jonka haluat kumota.  
3.  Valitse kumottavat rivit.  
4.  Valitse **Peruuta vast.otto** -toiminto.

Korjaava rivi lisätään valitun kuittirivin alle. Jos määrä vastaanotettiin fyysisen varastoinnin vastaanottona, korjaava rivi lisätään kirjattuun fyysisen varastoinnin vastaanottoon.  

**Vastaanotettu määrä** ja **Vast.otettu laskuttamaton määrä** -kenttien arvoiksi liittyvällä ostotilauksella asetetaan nolla.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Kirjatun palautustoimituksen määrän kirjauksen kumoaminen ja tekeminen uudelleen
Seuraavaksi kerrotaan, miten kirjattu palautustoimitus kumotaan ja ostopalautus kirjataan sitten uudelleen uudella määrällä.

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut palautustoimitukset** ja valitse sitten liittyvä linkki.  
2.  Avaa kumottava kirjattu palautustoimitus.
3. Valitse kumottavat rivit.  

4.  Valitse **Peruuta palautustoimitus** -toiminto.  

    Ohjelma syöttää korjaavan rivin kirjatulle asiakirjalle ja **Toimitettu palautusmäärä** ja **Pal.määrä toimitettu ei laskutettu** -kentät palautustilauksella asetetaan nollaksi.  

    Palaa nyt ostopalautustilaukseen ja tee kirjaus uudelleen.  

5.  Kirjoita muistiin numero, joka on **Kirjattu palautustoimitus** -sivun **Palautustilauksen nro** -kentässä.  
6.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostopalautustilaus** ja valitse sitten liittyvä linkki.  
7.  Avaa kyseinen palautustilaus ja valitse **Avaa uudelleen** -toiminto.  
8.  Korjaa tapahtuma **Määrä**-kentässä ja kirjaa ostopalautustilaus uudelleen.  

## <a name="see-also"></a>Katso myös
[Kokoonpanon kirjauksen kumoaminen](assembly-how-to-undo-assembly-posting.md)  
[Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
