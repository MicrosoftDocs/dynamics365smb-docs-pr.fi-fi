---
title: Kassavirtaennusteiden tekeminen käyttäen KP-raporttimalleja
description: Tässä vaihekuvauksessa kuvataan, kuinka KP-raporttimallin avulla voit tehdä kassavirtaennusteita Business Centralissa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: e0da9a5cab5c36bd5403bca3731ce46bb67316c3
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438500"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a>Vaihekuvaus: tehdään kassavirtaennusteita käyttäen KP-raporttimalleja

Tässä vaihekuvauksessa kuvataan, kuinka KP-raporttimallin avulla voit tehdä kassavirtaennusteita. KP-raporttimallit suorittavat laskutoimituksia, joita ei voi tehdä suoraan kassavirtakaavioihin. KP-raporttimalleissa voidaan määrittää välisummat kassavirtavastaanottoja ja suorituksia varten. Nämä välisummat voidaan sisällyttää uusiin kokonaissummiin, joita voidaan sitten käyttää kassavirtaennusteita tehtäessä.  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta

Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

- Uuden kassavirran KP-raporttimallin nimen määrittäminen.  
- Uuden KP-raporttimallin rivien määrittäminen.  
- Uuden sarakkeen asettelun määrittäminen.  
- Sarakeasettelun määritys KP-raporttimalliin.  
- Tarkastellaan ja tulostetaan kassavirtaennustetta.  

### <a name="prerequisites"></a>Vaatimukset

Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Kassavirran rivit on rekisteröity  

## <a name="roles"></a>Roolit

Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:  

- Valvoja  

## <a name="story"></a>Taustatietoja

Ken on CRONUS -päällikkö, joka tekee kuukausittaisia kassavirtaennusteita. Hän sisällyttää ennusteeseen rahoituksen, myynnin, oston ja käyttöomaisuuden ja esittelee ennusteen talousjohtaja Saaralle liiketoiminnan kuva selkeyttämiseksi.  

## <a name="setting-up-a-new-account-schedule-name"></a>Uuden KP-raporttimallin nimen määrittäminen

KP-raporttimalli koostuu kassavirran KP-raporttimallin nimestä, jossa on sarja rivejä ja sarakeasettelu.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Uuden KP-raporttimallin nimen määrittäminen  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KP-raporttimallit** ja valitse sitten vastaava linkki.  
2. Valitse **KP-raporttimallien nimet** -sivulla **Uusi**-toiminto ja luo uuden kassavirran KP-raporttimallin nimi.  
3. Syötä **Nimi**-kenttään **Ennuste**.  
4. Kirjoita **Kuvaus**-kenttään **Kassavirtaennuste**.  
5. Älä täytä **Sarakeasettelun oletusarvo**- ja **Analyysinäkymän nimi** -kenttiä.  

## <a name="setting-up-account-schedule-lines"></a>Uuden KP-raporttimallin rivien määrittäminen

Kun KP-raporttimallin nimi on määritetty, Ken määrittää jokaisen rivin, joka näkyy kassavirran KP-raporttimallissa. Ken määrittää rivit, jotka voidaan näyttää raporteissa niiden rivien lisäksi, jotka on tarkoitettu vain laskentaan.  

### <a name="to-set-up-account-schedule-lines"></a>Määritä KP-raporttimallin rivit  

1. Valitse **KP-raporttimallien nimet** -sivulla luomasi uuden **Ennusteen** KP-raporttimallin nimi ja valitse sitten **Muokkaa KP-raporttimallia** -toiminto.  
2. Anna **KP-raporttimallien nimet** -sivulla kukin rivi seuraavassa taulukossa esitetyllä tavalla.  

    > [!TIP]  
    >  Käyttämällä **Lisää kassavirtatilit** -toimintoa, voit nopeasti merkitä kassavirtatilit kassavairtatilikartallta ja kopioida ne KP-raporttimallin riveille.  

    | Rivinro | Kuvaus              | Summaustyyppi            | Summausväli | Rivityyppi   | Summatyyppi | Näytä |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Avoimet myyntitilaukset        | Kassavirran tapahtumatilit | 20       |Nettomuutos | Nettosumma  | Kyllä  |
    | R10     | Vuokraus                  | Kassavirran tapahtumatilit | 30       |Nettomuutos | Nettosumma  | Kyllä  |
    | R10     | Rahoitussaatavat         | Kassavirran tapahtumatilit | 40       |Nettomuutos | Nettosumma  | Kyllä  |
    | R10     | Käyttöomaisuuden luovutus    | Kassavirran tapahtumatilit | 50       |Nettomuutos | Nettosumma  | Kyllä  |
    | R10     | Yksityissijoitukset      | Kassavirran tapahtumatilit | 60       |Nettomuutos | Nettosumma  | Kyllä  |
    | R10     | Sekalaiset vastaanotot   | Kassavirran tapahtumatilit | 70       |Nettomuutos | Nettosumma  | Kyllä  |
    | R10     | Avoimet huoltotilaukset      | Kassavirran tapahtumatilit | 80       |Nettomuutos | Nettosumma  | Kyllä  |
    | R20     | Kassaanmaksu yhteensä      | Kaava                  | R10      |Nettomuutos | Nettosumma  | Kyllä  |
    | R20     | Kassaanmaksu yhteensä      | Kaava                  | R10      |Nettomuutos | Nettosumma  | Kyllä  |
    | R30     | Ostovelat                 | Kassavirran tapahtumatilit | 1010     |Nettomuutos | Nettosumma  | Kyllä  |
    | R30     | Avoimet ostotilaukset     | Kassavirran tapahtumatilit | 1020     |Nettomuutos | Nettosumma  | Kyllä  |
    | R30     | Henkilöstökulut          | Kassavirran tapahtumatilit | 1030     |Nettomuutos | Nettosumma  | Kyllä  |
    | R30     | Käyttökustannukset            | Kassavirran tapahtumatilit | 1040     |Nettomuutos | Nettosumma  | Kyllä  |
    | R30     | Rahoituskulut            | Kassavirran tapahtumatilit | 1050     |Nettomuutos | Nettosumma  | Kyllä  |
    | R30     | Sijoitukset              | Kassavirran tapahtumatilit | 1070     |Nettomuutos | Nettosumma  | Kyllä  |
    | R30     | Yksityinen kulutus     | Kassavirran tapahtumatilit | 1090     |Nettomuutos | Nettosumma  | Kyllä  |
    | R30     | Erääntyvä ALV                  | Kassavirran tapahtumatilit | 1100     |Nettomuutos | Nettosumma  | Kyllä  |
    | R30     | Muut kulut           | Kassavirran tapahtumatilit | 1110     |Nettomuutos | Nettosumma  | Kyllä  |
    | R40     | Kassasuoritukset yhteensä | Kaava                  | R30      |Nettomuutos | Nettosumma  | Kyllä  |
    | R50     | Ylijäämä                  | Kaava                  | R20+R40  |Nettomuutos | Nettosumma  | Kyllä  |
    | R60     | Kassavirtavarat          | Kassavirran tapahtumatilit | 2100     |Nettomuutos | Nettosumma  | Kyllä  |
    | R70     | Kassavirta yhteensä          | Kaava                  | R50+R60  |Nettomuutos | Nettosumma  | Kyllä  |

    > [!NOTE]
    > Rivinumeroa R10 käytetään saamistilien summien sitouttamiseen. Rivinumeroa R20 käytetään laskemaan kaikkien käteiskuittien summa. Rivinumeroa R30 käytetään ostovelkatilien summien sitouttamiseen. Rivinumeroa R40 käytetään laskemaan kaikkien käteiskassasuoritusten summa. Rivinumeroa R50 käytetään laskemaan käteisylijäämän summa. Rivinumeroa R60 käytetään sitouttamaan käyttövaroja. Rivinumeroa R70 käytetään laskemaan ennustettu kassavirta.

## <a name="setting-up-a-new-column-layout"></a>Uuden sarakkeen asettelun määrittäminen.

Ennen kuin Ken voi tulostaa kassavirtaennusteen, hänen on luotava sarakeasettelu numeerisille tiedoille. Sarakkeisiin hän määrittää tiedot, jotka hän haluaa käyttää riveiltä.

- Ensimmäisen sarakkeen numero on *C10*, sen otsikko on **Summa**, ja sisältönä on nettomuutos.  
- Toisella sarakkeella on numero *C20* otsikolla **Saldo päivämääränä**, ja se sisältää aikajakson tapahtumat.  
- Kolmannessa sarakkeessa on numero *C30* ja otsikko **Koko vuosi**, ja se sisältää koko tilikauden saldojen nettomuutoksen.  
- Lopuksi hän määrittää sarakeasettelun KP-raporttimallin **ennusteen** oletussarakeasetteluksi.  

## <a name="to-set-up-a-new-column-layout"></a>Määritä uusi sarakkeen asettelu

1. Valitse **KP-raporttimallien nimet** -ikkunassa uusi **Ennuste**-KP-raporttimallin nimi, jonka loit. Valitse **Kotisivu**-välilehden **Käsittely**-ryhmässä **Muokkaa sarakeasetuksia**.

    > [!TIP]
    > Voit etsiä saman toiminnon **KP-raportti malli** -sivulta, jos olet vielä muokkaamassa **ennusteen** KP-raporttimallia siellä.

2. Luo uusi sarakeasettelu nimellä **Kassavirta**.

3. Valitse OK-painike.

4. Syötä kukin rivi täsmälleen seuraavassa taulukossa esitetyllä tavalla.

    |Sarakkeen nro|Sarakkeen otsikko|Saraketyyppi|Tapahtumakirjauksen tyyppi|Summatyyppi|Näytä|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Summa|Nettomuutos|Tapahtumat|Nettosumma|Aina|  
    |C20|Summa päivämäärään|Saldo pvm:ttäin|Tapahtumat|Nettosumma|Aina|  
    |C30|Koko tilikausi|Koko tilikausi|Tapahtumat|Nettosumma|Aina|

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Sarakeasettelun määritys KP-raporttimallin nimeen

Ken on nyt valmis määrittämään sarakeasettelun KP-raporttimallin nimeen.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Määritä sarakeasettelu KP-raporttimallin nimeen.  

1. Valitse **Muokkaa sarakeasettelun asetuksia** -toiminto sillä **KP-raporttimalli**-sivulla, jossa käsittelet **ennusteen** KP-raporttimallia.  
2. Valitse **Sarakeasettelun nimi** -kentässä **Kassavirta**-sarakeasettelu oletussarakeasetteluksi.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Tarkastele ja tulosta kassavirtaennuste

1. Valitse **KP-raporttimallien nimet** -sivulla **Yleiskuvaus** ja tarkastele kassavirtaennustetta.  
2. **KP-raporttimallin yleiskuvaus** -sivulla voit valita summan ja näyttää sitten kassavirran tuotantoennustetapahtumat, joista summa muodostuu. Lisäksi voit tarkastella laskentakaavaa, jota käytetään summan laskemisessa. Voit myös suodattaa määrät dimension ja päivämäärän mukaan.  
3. Tulosta kassavirtaennuste valitsemalla **Tulosta**-toiminto.  

## <a name="see-also"></a>Katso myös

[KP-raporttimallien käyttäminen](bi-how-work-account-schedule.md)  
[Yrityksen kassavirran analysoiminen](finance-analyze-cash-flow.md)  
[Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]