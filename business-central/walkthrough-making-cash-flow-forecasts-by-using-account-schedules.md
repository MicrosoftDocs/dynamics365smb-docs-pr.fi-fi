---
title: Kassavirtaennusteiden tekeminen talousraporttien avulla
description: 'Tässä vaihekuvauksessa kuvataan, kuinka talousraporttien avulla voit tehdä kassavirtaennusteita Business Centralissa.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/18/2022
ms.author: edupont
---
# <a name="walkthrough-making-cash-flow-forecasts-using-financial-reports" />Vaihekuvaus: Kassavirtaennusteiden tekeminen talousraporttien avulla

Tässä vaihekuvauksessa kuvataan, kuinka talousraporttien ominaisuuden avulla voit tehdä kassavirtaennusteita. Talousraportit suorittavat laskutoimituksia, joita ei voi tehdä suoraan kassavirtakaavioihin. Talousraporttien avulla voidaan määrittää välisummat kassavirtavastaanottoja ja suorituksia varten. Nämä välisummat voidaan sisällyttää uusiin kokonaissummiin, joita voidaan sitten käyttää kassavirtaennusteita tehtäessä.  

## <a name="about-this-walkthrough" />Tietoja tästä vaihekuvauksesta

Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

- Uuden kassavirran talousraportin nimen määrittäminen.  
- Talousraportin rivien määrittäminen.  
- Uuden sarakemäärityksen määrittäminen.  
- Sarakemäärityksen liittäminen talousraporttiin.  
- Tarkastellaan ja tulostetaan kassavirtaennustetta.  

### <a name="prerequisites" />Vaatimukset

Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Kassavirtatyökirja ja rekisteröidyt rivit  

## <a name="roles" />Roolit

Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:  

- Valvoja  

## <a name="story" />Taustatietoja

Ken on CRONUS -päällikkö, joka tekee kuukausittaisia kassavirtaennusteita. Ken sisällyttää ennusteisiin rahoituksen, myynnin, oston ja käyttöomaisuuden ja esittelee ne talousjohtaja Saralle liiketoimintanäkemysten tarjoamiseksi.  

## <a name="setting-up-a-new-financial-report-name" />Uuden talousraportin nimen määrittäminen

Talousraportin nimi on nimi, joka annetaan määritettyjen rivien joukon ja sarakemäärityksen sisältävälle kassavirtaennusteelle.  

### <a name="set-up-a-new-financial-report-name" />Uuden talousraportin nimen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.  
2. Valitse **Talousraportit**-sivulla **Uusi** uuden kassavirran talousraportin nimen luomiseksi.  
3. Syötä **Nimi**-kenttään **Ennuste**.  
4. Kirjoita **Kuvaus**-kenttään **Kassavirtaennuste**.  
5. Jätä **Rivimääritys**- ja **Sarakemääritys**-kentät tyhjiksi.

## <a name="setting-up-row-definition-lines" />Rivimäärityksen rivien määrittäminen

Kun talousraportin nimi on määritetty, Ken määrittää kassavirran talousraportin kunkin rivin. Ken määrittää rivit, jotka näytetään raporteissa niiden rivien lisäksi, jotka on tarkoitettu vain laskentaan.  

### <a name="set-up-row-definition-lines" />Rivimäärityksen rivien määrittäminen

1. Valitse **Talousraportit**-sivulla uusi luotu **Ennuste**-talousraportti ja valitse sitten **Muokkaa rivimääritystä'** -toiminto.  
2. Anna **Rivimääritys**-sivulla kukin rivi seuraavassa taulukossa esitetyllä tavalla.  

    > [!TIP]  
    > **Lisää kassavirtatilit** -toiminnon avulla voit nopeasti merkitä haluamasi kassavirtatilit kassavirtatilikartalla ja kopioida ne rivimäärityksen riveille.  

    | Rivinro | Kuvaus              | Summaustyyppi            | Yhteensä | Rivityyppi   | Summatyyppi | Näyttäminen |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Myyntisaamiset              | Kassavirran tapahtumatilit | 10       |Nettomuutos | Nettosumma  | Kyllä  |
    | R10     | Avoimet myyntitilaukset        | Kassavirran tapahtumatilit | 20       |Nettomuutos | Nettosumma  | Kyllä  |
    | R10     | Vuokraus                  | Kassavirran tapahtumatilit | 30       |Nettomuutos | Nettosumma  | Kyllä  |
    | R10     | Rahoitussaatavat         | Kassavirran tapahtumatilit | 40       |Nettomuutos | Nettosumma  | Kyllä  |
    | R10     | Käyttöomaisuuden luovutus    | Kassavirran tapahtumatilit | 50       |Nettomuutos | Nettosumma  | Kyllä  |
    | R10     | Yksityissijoitukset      | Kassavirran tapahtumatilit | 60       |Nettomuutos | Nettosumma  | Kyllä  |
    | R10     | Sekalaiset vastaanotot   | Kassavirran tapahtumatilit | 70       |Nettomuutos | Nettosumma  | Kyllä  |
    | R10     | Avoimet huoltotilaukset      | Kassavirran tapahtumatilit | 80       |Nettomuutos | Nettosumma  | Kyllä  |
    | R20     | Kassakuitit yhteensä      | Kaava                  | R10      |Nettomuutos | Nettosumma  | Kyllä  |
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

## <a name="setting-up-a-new-column-definition" />Uuden sarakemäärityksen määrittäminen

Ennen kuin Ken voi tulostaa kassavirtaennusteen, hänen on luotava sarakemääritys numeerisille tiedoille. Sarakkeisiin Ken määrittää tiedot, jotka hän haluaa käyttää riveiltä.

- Ensimmäisen sarakkeen numero on *C10*, sen otsikko on **Summa**, ja sisältönä on nettomuutos.  
- Toisella sarakkeella on numero *C20* otsikolla **Saldo päivämääränä**, ja se sisältää aikajakson tapahtumat.  
- Kolmannessa sarakkeessa on numero *C30* ja otsikko **Koko vuosi**, ja se sisältää koko tilikauden saldojen nettomuutoksen.  
- Lopuksi Ken määrittää sarakemäärityksen talousraportin **ennusteen** oletusasetukseksi.  

### <a name="set-up-a-new-column-definition" />Uuden sarakemäärityksen määrittäminen

1. Valitse **Talousraportit**-sivulla luomasi uuden **Ennuste**-talousraportin nimi. Valitse **Kotisivu**-välilehden **Käsittely**-ryhmässä **Muokkaa sarakemääritystä**.

2. Luo uusi sarakemääritys nimellä **Kassavirta**.

3. Valitse **OK**-painike.

4. Syötä kukin rivi täsmälleen seuraavassa taulukossa esitetyllä tavalla.

    |Sarakkeen nro|Sarakkeen otsikko|Saraketyyppi|Tapahtumakirjauksen tyyppi|Summatyyppi|Näyttäminen|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Summa|Nettomuutos|Tapahtumat|Nettosumma|Aina|  
    |C20|Summa päivämäärään|Saldo pvm:ttäin|Tapahtumat|Nettosumma|Aina|  
    |C30|Koko tilikausi|Koko tilikausi|Tapahtumat|Nettosumma|Aina|

## <a name="assigning-the-column-definition-to-the-financial-report-name" />Sarakemäärityksen liittäminen talousraportin nimeen

Ken on nyt valmis määrittämään sarakemäärityksen talousraportin nimeen.  

### <a name="assign-the-column-definition-to-the-financial-report-name" />Sarakemäärityksen liittäminen talousraportin nimeen

1. Valitse **Talousraportit**-sivulla **Ennuste**-talousraportti ja valitse sitten **Muokkaa sarakemääritystä'** -toiminto.  
2. Valitse **Nimi**-kentässä **Kassavirta**-sarakemääritys oletussarakemääritykseksi.  

## <a name="view-and-print-the-cash-flow-forecast" />Kassavirtaennusteen tarkasteleminen ja tulostaminen

1. Valitse **Talousraportit**-sivulla **Ennuste**-talousraportti uuden kassavirtaennusteen tarkastelemista varten.  
2. **Talousraportti**-sivulla voit valita summan ja näyttää sitten kassavirran tuotantoennustetapahtumat, joista summa muodostuu. Lisäksi voit tarkastella kaavaa, jota käytetään summan laskemisessa. Voit myös suodattaa määrät dimension ja päivämäärän mukaan.  
3. Tulosta kassavirtaennuste valitsemalla **Tulosta**-toiminto.  

## <a name="see-related-microsoft-trainingtrainingmodulesforecast-cash-flow-dynamics--business-central" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/forecast-cash-flow-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Talousraporttien käsitteleminen](bi-how-work-account-schedule.md)  
[Yrityksen kassavirran analysoiminen](finance-analyze-cash-flow.md)  
[Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
