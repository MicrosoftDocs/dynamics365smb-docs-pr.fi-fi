---
title: Konsernin Saapuneet- ja Lähtevät-kansion hallinta
description: Konsernikumppaneilta vastaanotetut konsernitapahtumat näkyvät konsernin Saapuneet-kansiossa, jossa voit käsitellä niitä manuaalisesti tai automaattisesti.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.search.form: 600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611
ms.date: 03/09/2022
ms.author: edupont
ms.openlocfilehash: 868f07b2b56ccaefb4c56e26be72c27b941d950c
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522116"
---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>Konsernin Saapuneet- ja Lähtevät-kansion hallinta
Kaikki konsernikumppaneilta sähköisesti vastaanotetut konsernitapahtumat näkyvät konsernin Saapuneet-kansiossa.  

Kuitenkin sen mukaan, miten konsernitapahtumat on määritetty, jotkin tapahtumat replikoidaan automaattisesti asianomaisille konsernikumppaneille. Alkaen vuoden 2022 julkaisuaallosta 1 voit määrittää yrityksen konsernikumppaneilta saatujen konsernin sisäisten tapahtumien automaattista luontia varten, jotka on kirjattu konsernin yleiseen päiväkirjaan. Lisätietoja on kohdassa [Voit täyttää ja kirjata konsernin päiväkirjan seuraavasti](intercompany-how-work-documents-journals.md#to-fill-in-and-post-an-intercompany-journal).  

## <a name="organizing-the-inbox"></a>Saapuneet-kansion järjestäminen  
 Saapuneet-sivun yläosassa näkyvien suodatinkenttien avulla voit määrittää, mitkä tapahtumat näkyvät sivulla. Jos esimerkiksi haluat tarkastella vain tietyn kumppanin luomia tapahtumia, voit antaa suodattimia **Tapahtuman lähde**- ja **Konsernikumppanin koodi** -suodattimissa.  

### <a name="transaction-source"></a>Tapahtuman lähde  
Tapahtumalle tehtävissä olevat toimet määräytyvät sen mukaan, onko tapahtuma  

- konsernikumppanin luoma  
- konsernikumppanin hylkäämä ja palauttama.  

Voit suodattaa **Näytä tapahtuman lähde** -kentän avulla **Konsernin Saapuneet-kansion tapahtumat** -sivua siten, että vain yksi näistä tapahtumatyypeistä näkyy sivulla. (Voit käyttää suodatusperusteena myös konsernikumppania tai **Rivitoiminto**-kentän sisältöä.)  

#### <a name="created-by-intercompany-partner"></a>Konsernikumppanin luoma  
 Kumppanin luoman uuden tapahtuman vastaanottaja voi

- hyväksyä tapahtuman  
- hylätä tapahtuman (palauttaa tapahtuman kumppanille)  
- peruuttaa tapahtuman (poistaa tapahtuman palauttamatta sitä kumppanille).  

#### <a name="returned-from-intercompany-partner"></a>Konsernikumppanin palauttama  
 Jos konsernikumppani hylkää tapahtuman, ainoa mahdollinen vaihtoehto on tapahtuman peruuttaminen Saapuneet-kansiossa. Tämän jälkeen sinun täytyy luoda korjausrivejä tai peruuttaa päiväkirja tai asiakirja omassa yrityksessä.  

## <a name="recreating-inbox-entries"></a>Saapuneet-kansion tapahtumien luominen uudelleen  
 Jos olet hyväksynyt tapahtuman Saapuneet-kansiossa ja kirjaamisen asemesta poistanut asiakirjan tai päiväkirjan, voit luoda tapahtuman uudelleen Saapuneet-kansioon ja hyväksyä sen toistamiseen.  

## <a name="getting-an-overview-of-intercompany-transactions-for-a-period"></a>Konsernin tapahtumien jaksokohtaisen yleiskuvauksen tarkasteleminen  
 Voit tarkastella kaikkien sellaisten tapahtumien yleiskuvausta, jotka olet lähettänyt ja vastaanottanut tietyn jakson aikana. **Konsernin tapahtumat** -raportissa mainitaan kaikki konsernin KP-tapahtumat, asiakastapahtumat ja toimittajatapahtumat.

 > [!NOTE]  
 > Jos konsernikumppanit ovat samassa tietokannassa, tapahtumien siirtämiseen ei tarvita tiedostoa eikä sähköpostia. Katso **Konsernikumppani**-sivun **Siirron tyyppi** -kenttä. <br /><br />
Voit määrittää järjestelmän ohittamaan Saapuneet- ja Lähtevät-kansiot valitsemalla **Tapahtumien automaattinen hyväksyntä** -valintaruudun **Konsernikumppani**-sivulla ja **Tapahtumien automaattinen lähetys** -valintaruudun **Konsernin asetukset** -sivulla. Saapuvat konsernitapahtumat voidaan hyväksyä automaattisesti vain, jos tehtävien ajoitus on käytössä. Lisätietoja on kohdassa [Business Central Serverin määrittäminen – Tehtävien ajoituksen asetukset](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Task).

## <a name="to-import-intercompany-transactions-from-a-file"></a>Konsernitapahtumien tuominen tiedostosta

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Jos konsernikumppani ja oma yritys ovat eri tietokannoissa, voit vastaanottaa konsernin tapahtumia kyseiseltä kumppanilta .xml-tiedostona. Tapahtumat täytyy tämän jälkeen tuoda Saapuneet-kansioon.  

1. Tallenna tiedosto sijaintiin, jonka olet määrittänyt **Konsernin Saapuneet-kansion tiedot** -kentässä konsernitapahtumien asettamisen aikana.  
2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin Saapuneet-kansion tapahtumat** ja valitse sitten vastaava linkki.
3. Valitse **Konsernin Saapuneet-kansion tapahtumat** -sivulla **Tuo tapahtumatiedosto** -toiminto.  
4. Valitse avautuvalla sivulla tapahtumat sisältävä .xml-tiedosto ja valitse **Avaa**.  

Tapahtumat tuodaan Saapuneet-kansioon. Niitä voi nyt käsitellä.

## <a name="to-process-incoming-intercompany-transactions"></a>Saapuvien konsernitapahtumien käsitteleminen  
Konsernikumppanien sinulle lähettämät konsernin tapahtumat tulevat konsernin Saapuneet-kansioon. Jokainen Saapuneet-kansion tapahtuma täytyy arvioida ja käsitellä erikseen.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin Saapuneet-kansion tapahtumat** ja valitse sitten vastaava linkki.  
2. Käsittele rivi valitsemalla **Konsernin Saapuneet-kansion tapahtumat** -sivulla ensin rivi ja sitten toiminto, kuten **Hyväksy**.
3. Täytä **Tot. kons. Saap.-kansion toim.** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **OK**-painike.  

**Hyväksy**-toiminnolla käsitellyille riveille luodaan yritykseen asiakirja- tai päiväkirjarivit. Avaa kukin asiakirja tai päiväkirja, tee tarvittavat muutokset ja kirjaa ne.  

**Palauta kumppanille** -toiminnolla käsitellyt rivit siirretään Lähtevät-kansioon, josta voit lähettää ne kumppanille.

**Palauttaja: kumppani** -toiminnolla käsitellyille riville on kirjattava korjaus alkuperäiseen, omassa yrityksessä kirjattuun tapahtumaan.

## <a name="to-process-outgoing-intercompany-transactions"></a>Lähtevien konsernitapahtumien käsitteleminen  
Kun kirjaat konsernin päiväkirjan tai asiakirjan tai lähetät konsernin tilausvahvistuksen, tapahtumat lähetetään konsernin Lähtevät-kansioon. Tapahtumien lähettäminen konsernikumppaneille edellyttää, että Lähtevät-kansio avataan ja tapahtumat käsitellään.  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin Lähtevät-kansion tapahtumat** ja valitse sitten vastaava linkki.  
2. Käsittele rivi valitsemalla **Konsernin Lähtevät-kansion tapahtumat** -sivulla ensin rivi ja sitten toiminto, kuten **Palaa Saapuneet-kansioon**.

**Lähetä konsernikumppanille** -toiminnolla käsitellyt rivit lähetetään kyseisen kumppanin Saapuneet-kansioon.

**Palaa Saapuneet-kansioon**-toiminnolla käsitellyt rivit siirretään Saapuneet-kansioon, jossa voit sitten hyväksyä ne. Omaan yritykseen luoda sitten vastaavat asiakirja- tai päiväkirjarivit.  

**Peruuta**-toiminnolla käsitellyille riville on kirjattava korjaus alkuperäiseen, omassa yrityksessä kirjattuun tapahtumaan.  

## <a name="to-recreate-intercompany-inbox-transactions"></a>Konsernin Saapuneet-kansion tapahtumien luominen uudelleen  
Joskus haluat ehkä luoda tapahtuman uudelleen Saapuneet- tai Lähtevät-kansioon. Jos olet hyväksynyt tapahtuman Saapuneet-kansiossa ja kirjaamisen asemesta poistanut asiakirjan tai päiväkirjan, voit luoda tapahtuman uudelleen Saapuneet-kansioon ja hyväksyä sen toistamiseen.  

Seuraavissa ohjeissa neuvotaan, kuinka Saapuneet-kansion tapahtumia voi luoda uudelleen. Samoja ohjeita voi kuitenkin soveltaa myös Lähtevät-kansioon.

  1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käsitellyt konsernin Saapuneet-kansion tapahtumat** ja valitse sitten vastaava linkki.  

  2.  Valitse **Käsitellyt konsernin Saapuneet-kansion tapahtumat** -sivulla rivi, jossa on Saapuneet-kansioon uudelleen luotava tapahtuma. Valitse sitten **Luo Saapuneet-kansion tapahtuma uudelleen** -toiminto.  

## <a name="see-also"></a>Katso myös
[Konsernitapahtumien hallinta](intercompany-manage.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
