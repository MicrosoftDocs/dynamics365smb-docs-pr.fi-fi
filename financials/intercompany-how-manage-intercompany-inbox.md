---
title: "Saapuvien ja lähtevien konsernitapahtumien käsitteleminen| Microsoft Docs"
description: "Konsernikumppaneilta vastaanotetut konsernitapahtumat näkyvät konsernin Saapuneet-kansiossa, jossa voit käsitellä niitä manuaalisesti tai automaattisesti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: abeb3ee24434ca3549e7ed88ecfae54cc395002d
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>Konsernin Saapuneet- ja Lähtevät-kansion hallinta
Kaikki konsernikumppaneilta sähköisesti vastaanotetut konsernitapahtumat näkyvät konsernin Saapuneet-kansiossa.  

## <a name="organizing-the-inbox"></a>Saapuneet-kansion järjestäminen  
 Saapuneet-ikkunan yläosassa näkyvien suodatinkenttien avulla voit määrittää, mitkä tapahtumat ikkunassa näkyvät. Jos esimerkiksi haluat tarkastella vain tietyn kumppanin luomia tapahtumia, voit antaa suodattimia **Tapahtuman lähde**- ja **Konsernikumppanin koodi** -suodattimissa.  

### <a name="transaction-source"></a>Tapahtuman lähde  
Tapahtumalle tehtävissä olevat toimet määräytyvät sen mukaan, onko tapahtuma  

- konsernikumppanin luoma  
- konsernikumppanin hylkäämä ja palauttama.  

Voit suodattaa **Näytä tapahtuman lähde** -kentän avulla **Konsernin Saapuneet-kansion tapahtumat** -ikkunaa siten, että vain yksi näistä tapahtumatyypeistä näkyy ikkunassa. (Voit käyttää suodatusperusteena myös konsernikumppania tai **Rivitoiminto**-kentän sisältöä.)  

#### <a name="created-by-intercompany-partner"></a>Konsernikumppanin luoma  
 Kumppanin luoman uuden tapahtuman vastaanottaja voi

- hyväksyä tapahtuman  
- hylätä tapahtuman (palauttaa tapahtuman kumppanille)  
- peruuttaa tapahtuman (poistaa tapahtuman palauttamatta sitä kumppanille).  

#### <a name="returned-from-intercompany-partner"></a>Konsernikumppanin palauttama  
 Jos konsernikumppani hylkää tapahtuman, ainoa mahdollinen vaihtoehto on tapahtuman peruuttaminen Saapuneet-kansiossa. Tämän jälkeen sinun täytyy luoda korjausrivejä tai peruuttaa päiväkirja tai asiakirja omassa yrityksessä.  

## <a name="re-creating-inbox-entries"></a>Saapuneet-kansion tapahtumien luominen uudelleen  
 Jos olet hyväksynyt tapahtuman Saapuneet-kansiossa ja kirjaamisen asemesta poistanut asiakirjan tai päiväkirjan, voit luoda tapahtuman uudelleen Saapuneet-kansioon ja hyväksyä sen toistamiseen.  

## <a name="getting-an-overview-of-intercompany-transactions-for-a-period"></a>Konsernin tapahtumien jaksokohtaisen yleiskuvauksen tarkasteleminen  
 Voit tarkastella kaikkien sellaisten tapahtumien yleiskuvausta, jotka olet lähettänyt ja vastaanottanut tietyn jakson aikana. **Konsernin tapahtumat** -raportissa mainitaan kaikki konsernin KP-tapahtumat, asiakastapahtumat ja toimittajatapahtumat.

 > [!NOTE]  
 > Jos konsernikumppanit ovat samassa tietokannassa, tapahtumien siirtämiseen ei tarvita tiedostoa eikä sähköpostia. Katso **Konsernikumppani**-ikkunan **Siirron tyyppi** -kenttä. <br /><br />
Voit määrittää järjestelmän ohittamaan Saapuneet- ja Lähtevät-kansiot valitsemalla **Tapahtumien automaattinen hyväksyntä** -valintaruudun **Konsernikumppani**-ikkunassa ja **Tapahtumien automaattinen lähetys** -valintaruudun **Konsernin asetukset** -ikkunassa.

## <a name="to-import-intercompany-transactions-from-a-file"></a>Konsernitapahtumien tuominen tiedostosta  
Jos konsernikumppani ja oma yritys ovat eri tietokannoissa, voit vastaanottaa konsernin tapahtumia kyseiseltä kumppanilta .xml-tiedostona. Tapahtumat täytyy tämän jälkeen tuoda Saapuneet-kansioon.  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Yrityksen tiedot** ja valitse sitten aiheeseen liittyvä linkki.
2. Tallenna tiedosto sijaintiin, jonka olet määrittänyt **Yrityksen tiedot** -ikkunan **Konsernin Saapuneet-kansion tiedot** -kentässä.  
3. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Konsernin Saapuneet-kansion tapahtumat** ja valitse sitten aiheeseen liittyvä linkki.
4. Valitse **Konsernin Saapuneet-kansion tapahtumat** -ikkunassa **Tuo tapahtumatiedosto** -toiminto.  
5. Valitse avautuvassa ikkunassa tapahtumat sisältävä .xml-tiedosto ja valitse **Avaa**.  

Tapahtumat tuodaan Saapuneet-kansioon. Niitä voi nyt käsitellä.

## <a name="to-process-incoming-intercompany-transactions"></a>Saapuvien konsernitapahtumien käsitteleminen  
Konsernikumppanien sinulle lähettämät konsernin tapahtumat tulevat konsernin Saapuneet-kansioon. Jokainen Saapuneet-kansion tapahtuma täytyy arvioida ja käsitellä erikseen.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Konsernin Saapuneet-kansion tapahtumat** ja valitse sitten aiheeseen liittyvä linkki.  
2. Käsittele rivi valitsemalla **Konsernin Saapuneet-kansion tapahtumat** -ikkunassa ensin rivi ja sitten toiminto, kuten **Hyväksy**.
3. Täytä **Tot. kons. Saap.-kansion toim.** -ikkunassa tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **OK**-painike.  

**Hyväksy**-toiminnolla käsitellyille riveille luodaan yritykseen asiakirja- tai päiväkirjarivit. Avaa kukin asiakirja tai päiväkirja, tee tarvittavat muutokset ja kirjaa ne.  

**Palauta kumppanille** -toiminnolla käsitellyt rivit siirretään Lähtevät-kansioon, josta voit lähettää ne kumppanille.

**Palauttaja: kumppani** -toiminnolla käsitellyille riville on kirjattava korjaus alkuperäiseen, omassa yrityksessä kirjattuun tapahtumaan.

## <a name="to-process-outgoing-intercompany-transactions"></a>Lähtevien konsernitapahtumien käsitteleminen  
Kun kirjaat konsernin päiväkirjan tai asiakirjan tai lähetät konsernin tilausvahvistuksen, tapahtumat lähetetään konsernin Lähtevät-kansioon. Tapahtumien lähettäminen konsernikumppaneille edellyttää, että Lähtevät-kansio avataan ja tapahtumat käsitellään.  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Konsernin Lähtevät-kansion tapahtumat** ja valitse sitten aiheeseen liittyvä linkki.  
2. Käsittele rivi valitsemalla **Konsernin Lähtevät-kansion tapahtumat** -ikkunassa ensin rivi ja sitten toiminto, kuten **Palaa Saapuneet-kansioon**.

**Lähetä konsernikumppanille** -toiminnolla käsitellyt rivit lähetetään kyseisen kumppanin Saapuneet-kansioon.

**Palaa Saapuneet-kansioon**-toiminnolla käsitellyt rivit siirretään Saapuneet-kansioon, jossa voit sitten hyväksyä ne. Omaan yritykseen luoda sitten vastaavat asiakirja- tai päiväkirjarivit.  

**Peruuta**-toiminnolla käsitellyille riville on kirjattava korjaus alkuperäiseen, omassa yrityksessä kirjattuun tapahtumaan.  

## <a name="to-recreate-intercompany-inbox-transactions"></a>Konsernin Saapuneet-kansion tapahtumien luominen uudelleen  
Joskus haluat ehkä luoda tapahtuman uudelleen Saapuneet- tai Lähtevät-kansioon. Jos olet hyväksynyt tapahtuman Saapuneet-kansiossa ja kirjaamisen asemesta poistanut asiakirjan tai päiväkirjan, voit luoda tapahtuman uudelleen Saapuneet-kansioon ja hyväksyä sen toistamiseen.  

Seuraavissa ohjeissa neuvotaan, kuinka Saapuneet-kansion tapahtumia voi luoda uudelleen. Samoja ohjeita voi kuitenkin soveltaa myös Lähtevät-kansioon.

  1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Käsitellyt konsernin Saapuneet-kansion tapahtumat** ja valitse sitten aiheeseen liittyvä linkki.  

  2.  Valitse **Käsitellyt konsernin Saapuneet-kansion tapahtumat** -ikkunassa rivi, jossa on Saapuneet-kansioon uudelleen luotava tapahtuma. Valitse sitten **Luo Saapuneet-kansion tapahtuma uudelleen** -toiminto.  

## <a name="see-also"></a>Katso myös
[Konsernitapahtumien hallinta](intercompany-manage.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

