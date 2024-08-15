---
title: Ennusta myyntiasiakirjojen myöhästyvät maksut
description: 'Tämä artikkelissa selitetään, miten voit käyttää ennakoivaa malliamme, kun haluat ennustaa, maksaako asiakas laskun ajoissa.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customer, payment, invoice, sales, invoice, quote'
ms.search.form: '1950, 1951,'
ms.date: 07/11/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="the-late-payment-prediction-extension"></a>Myöhästyneen maksun ennusteen laajennus

Tehokas myyntisaamisten hallinta on tärkeää yrityksen taloudellisen tilanteen yleiskuvan kannalta. Laajennus auttaa perintästrategian tarkentamisessa ennustamalla, onko odotettavissa myöhästyviä maksuja. Jos maksun ennustetaan olevan myöhässä, voit esimerkiksi muuttaa asiakkaan maksuehtoja tai maksutapaa.

## <a name="get-started"></a>Aloittaminen

Kun avaat kirjatun myyntiasiakirjan, sivun yläosaan tulee ilmoitus. Jos haluat käyttää myöhästyneen maksun ennusteen laajennusta, suostu sen käyttöön valitsemalla ilmoituksen **Ota käyttöön** -kohdan. Vaihtoehtoisesti voit määrittää laajennuksen manuaalisesti. Näin voit tehdä esimerkiksi silloin, jos kadut ilmoituksen ohittamista.

Voit ottaa laajennuksen käyttöön manuaalisesti seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myöhästyneen maksun ennusteen asetukset** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.

> [!NOTE]
> Jos päätät ottaa laajennuksen käyttöön manuaalisesti, ota huomioon, että [!INCLUDE[prod_short](includes/prod_short.md)] ei mahdollista tätä, jos mallin laatu on heikko. Mallin laatu osoittaa, miten tarkkoja mallin ennusteista tulee. Useat tekijät voivat vaikuttaa mallin laatuun. Tietoja ei esimerkiksi ole riittävästi tai tiedoissa ei ollut riittävästi muunnoksia. Voit tarkastella tällä hetkellä käytössä olevan mallin laatua **Myöhästyneen maksun ennusteen asetus** -sivulla. Voit myös määrittää mallin laadulle vähimmäisrajan.

## <a name="view-all-payment-predictions"></a>Kaikkien maksujen ennusteiden tarkasteleminen

Jos otat käyttöön laajennuksen, **Maksut, joiden on ennustettu olevan myöhässä** -ruutu on käytettävissä **liiketoimintajohtajan** roolikeskuksessa. Ruudussa on niiden maksujen määrä, joiden ennustetaan olevan myöhässä. Sen avulla voit avata **Asiakastapahtumat**-sivun, jossa on lisätietoja kirjatuista laskuista. Kiinnitä huomiota seuraaviin kolmeen sarakkeeseen:  

* **Myöhästynyt maksu** - Osoittaa, onko laskun maksun ennustettu olevan myöhässä.
* **Ennusteen luotettavuus** - Osoittaa, miten luotettava ennuste on. **Suuri** tarkoittaa, että ennusteen luotettavuus on 90 %, **normaali** 80–90 % ja **pieni** alle 80 %.
* **Ennusteen luotettavuus-%** - Osoittaa luottamusluokituksen todellisen prosenttiosuuden. Tämä sarake on oletusarvoisesti piilotettu, mutta voit lisätä sen halutessasi. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

> [!TIP]
> Asiakastapahtumien sivulla näkyy tietoruutu. **Asiakkaan tiedot** -osan tiedot voivat olla hyödyllisiä, kun tarkastelet ennusteita. Kun valitset luettelosta laskun, osassa näkyvät asiakkaan tiedot. Sen avulla voit myös tehdä toimintoja heti. Jos esimerkiksi asiakas jättää usein maksamatta, voit avata tietoruudussa asiakkaan kortin ja estää asiakasta ostamasta tulevaisuudessa.  

## <a name="design-details"></a>Rakennetiedot

Microsoft ottaa käyttöön ja käyttää ennustavia verkkopalveluja kaikilla alueilla, joissa [!INCLUDE[prod_short](includes/prod_short.md)] on saatavilla. Näiden verkkopalveluiden käyttö sisältyy [!INCLUDE[prod_short](includes/prod_short.md)] -tilaukseen. Lisätietoja on Microsoft Dynamics 365 Business Centralin käyttöoikeusoppaassa. Opas on ladattavissa [Business Centralin](https://dynamics.microsoft.com/business-central/overview/) verkkosivulla.

Verkkopalvelut toimivat kolmessa seuraavassa tilassa:

* Koulutusmalli. Verkkopalvelu kouluttaa mallia annetun tietojoukon perusteella.
* Arviointimalli. Verkkopalvelu tarkistaa, palauttaako malli luotettavat tiedot annetusta tietojoukosta.
* Ennustus. Verkkopalvelu kohdistaa mallin annettuun tietojoukkoon ja tekee ennustuksen.

Näillä verkkopalveluilla ei ole tilaa. Ne siis käyttävät tietoja vain ennusteiden laskemiseen tarvittaessa. Ne eivät tallenna tietoja.

> [!NOTE]  
> Voit käyttää omaa ennakoivaa verkkopalvelua meidän palvelumme sijaan. Lisätietoja on kohdassa [Oman ennustavan verkkopalvelun myöhästyneen maksun ennusteen luominen ja käyttäminen](#AnchorText).

### <a name="data-required-to-train-and-evaluate-the-model"></a>Tiedot, jotka vaaditaan mallin kouluttamista ja arvioimista varten

Jokainen **asiakastapahtumalle**, jolla on liittyvä **kirjattu myyntilasku**:

* Summa paikallisena valuuttana sisältäen veron
* Maksuehdot päivinä, laskutapa on: **eräpäivä** vähennettynä **kirjauspäivällä**
* Onko hyvityslasku kohdistettu

Lisäksi tietueeseessa on koostetut tiedot muista samaan asiakkaaseen liittyvistä laskuista.

- Maksettujen laskujen kokonaismäärä ja -summa
- Myöhässä maksettujen laskujen kokonaismäärä ja -summa
- Maksamattomien laskujen kokonaismäärä ja -summa
- Maksamattomien, myöhässä olevien laskujen kokonaismäärä ja -summa
- Keskimäärin myöhässä päivää
- Suhde: myöhässä maksettujen / maksettujen laskujen määrä
- Suhde: myöhässä maksettujen / maksettujen laskujen summa
- Suhde: maksamattomien, myöhässä olevien / maksamattomien laskujen määrä
- Suhde: maksamattomien, myöhässä olevien / maksamattomien laskujen summa

> [!NOTE]
> Asiakkaan tietoja ei ole lisätty tietojoukkoon.

### <a name="standard-model-and-my-model"></a>Vakiomalli ja oma malli

Myöhästyneen maksun ennusteen laajennus käyttää ennakoivaa mallia, jonka kehittämisessä on käytetty pienten ja keskikokoisten yritysten tietoja edustavia tietoja. Kun käynnistät laskujen kirjaamisen ja maksujen vastaanottamisen, [!INCLUDE[prod_short](includes/prod_short.md)] arvioi, vastaako vakiomalli liiketoimintaprosessiasi.

Jos prosessit eivät vastaa vakiomallia, voit yhä käyttää laajennusta, mutta sinun täytyy hankkia enemmän tietoja. Vain jatkaa [!INCLUDE[prod_short](includes/prod_short.md)]:n käyttämistä.

> [!NOTE]
> Microsoft käyttää joka viikko hieman laskenta-aikaa, kun malli arvioidaan ja sitä koulutetaan lisää.

[!INCLUDE[prod_short](includes/prod_short.md)] suorittaa koulutuksen ja arvioinnin automaattisesti, kun tarpeeksi maksettuja ja myöhässä olevia laskuja on saatavilla. Voit kuitenkin suorittaa sen manuaalisesti milloin haluat.

#### <a name="to-train-and-use-your-model"></a>Mallin kouluttaminen ja käyttäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myöhästyneen maksun ennusteen asetukset** ja valitse sitten liittyvä linkki.  
2. Valitse **Valittu malli** -kentässä **Oma malli**.
3. Valitse **Luo oma malli** -toiminto, jos haluat kouluttaa tietojen mallia.  

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-late-payment-prediction"></a><a name="AnchorText"> </a>Oman ennakoivan verkkopalvelun luominen ja käyttäminen myöhässä olevan maksun ennustetta varten

Jotta [!INCLUDE[prod_short](includes/prod_short.md)] toimii verkossa Microsoft julkaisee mallin ja yhdistää sen Microsoft-tilaukseen. Toisia käyttöönottovaihtoehtoja varten on luotava koneoppimisen resursseja omassa Azure-tilauksessaan. Esimerkkivaiheita: [esimerkkiraportti](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). Tämän tehtävän tarkoituksena on noutaa ohjelmointirajapinnan URI ja ohjelmointirajapinnan avain.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myöhästyneen maksun ennusteen asetukset** ja valitse sitten liittyvä linkki.  
2. Valitse **Käytä omaa Azure-tilausta** -valintaruutu.
3.  **Kirjoita Mallin API-URL- ja API-tunnus Käytä oman yrityksen tilausta -** pikavälilehteen.  

## <a name="see-also"></a>Katso myös

[Liiketoimintakeskuksen mukauttaminen laajennusten avulla](ui-extensions.md)    
[Tervetuloa [!INCLUDE[prod_long](includes/prod_long.md)]](welcome.md)    
[Tekoälyn käyttäminen Microsoftissa Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)    
[Ennusteohjelmointirajapinnan yleiskatsaus](/dynamics365/business-central/dev-itpro/developer/ml-prediction-api-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
