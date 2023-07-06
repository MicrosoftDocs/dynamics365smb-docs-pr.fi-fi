---
title: Ennusta myyntiasiakirjojen myöhästyvät maksut
description: 'Tämä aihe selittää, miten voit käyttää ennakoivaa malliamme, kun haluat ennustaa, suoritetaanko laskun maksu ajoissa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customer, payment, invoice, sales, invoice, quote'
ms.search.form: '1950, 1951,'
ms.date: 12/20/2021
ms.author: bholtorf
---
# <a name="the-late-payment-prediction-extension"></a><a name="the-late-payment-prediction-extension"></a><a name="the-late-payment-prediction-extension"></a>Myöhästyneen maksun ennusteen laajennus

Tehokas myyntisaamisten hallinta on tärkeää yrityksen taloudellisen tilanteen yleiskuvan kannalta. Myöhästyneen maksun ennusteen laajennus voi auttaa avointen myyntisaamisten vähentämisessä ja perintästrategian tarkentamisessa ennustamalla, maksetaanko myyntilaskut ajoissa. Jos maksun ennustetaan olevan myöhässä, voit esimerkiksi muuttaa asiakkaan maksuehtoja tai maksutapaa.

## <a name="getting-started"></a><a name="getting-started"></a><a name="getting-started"></a>Aloitusopas

Kun avaat kirjatun myyntiasiakirjan, sivun yläosaan tulee ilmoitus. Jos haluat käyttää myöhästyneen maksun ennusteen laajennusta, voit suostua sen käyttöön valitsemalla ilmoituksen **Ota käyttöön** -kohdan. Vaihtoehtoisesti voit määrittää laajennuksen manuaalisesti. Näin voit tehdä esimerkiksi silloin, jos kadut ilmoituksen ohittamista.  

Voit ottaa laajennuksen käyttöön manuaalisesti seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myöhästyneen maksun ennusteen asetukset** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.

> [!NOTE]
> Jos päätät ottaa laajennuksen käyttöön manuaalisesti, ota huomioon, että [!INCLUDE[prod_short](includes/prod_short.md)] ei mahdollista tätä, jos mallin laatu on heikko. Mallin laatu osoittaa, miten tarkkoja mallin ennusteista tulee. Useat tekijät voivat vaikuttaa mallin laatuun. Tietoja ei esimerkiksi ole riittävästi tai tiedoissa ei ollut riittävästi muunnoksia. Voit tarkastella tällä hetkellä käytössä olevan mallin laatua **Myöhästyneen maksun ennusteen asetus** -sivulla. Voit myös määrittää mallin laadulle vähimmäisrajan.   

## <a name="viewing-all-payment-predictions"></a><a name="viewing-all-payment-predictions"></a><a name="viewing-all-payment-predictions"></a>Kaikkien maksujen ennusteiden tarkasteleminen

Jos otat käyttöön laajennuksen, **Maksut, joiden on ennustettu olevan myöhässä** -ruutu on käytettävissä **liiketoimintajohtajan** roolikeskuksessa. Ruudussa on niiden maksujen määrä, joiden ennustetaan olevan myöhässä. Sen avulla voit avata **Asiakastapahtumat**-sivun, jossa on lisätietoja kirjatuista laskuista. Kiinnitä huomiota seuraaviin kolmeen sarakkeeseen:  

* **Myöhästynyt maksu** - Osoittaa, onko laskun maksun ennustettu olevan myöhässä.
* **Ennusteen luotettavuus** - Osoittaa, miten luotettava ennuste on. **Suuri** tarkoittaa, että ennusteen luotettavuus on 90 %, **normaali** 80–90 % ja **pieni** alle 80 %.
* **Ennusteen luotettavuus-%** - Osoittaa luottamusluokituksen todellisen prosenttiosuuden. Tämä sarake ei näy oletusarvoisesti, mutta voit lisätä sen halutessasi. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

> [!TIP]
> Asiakastapahtumat-sivun oikeassa reunassa on tietoruutu. **Asiakkaan tiedot** -osan tiedot voivat olla hyödyllisiä, kun tarkastelet ennusteita. Kun valitset luettelosta laskun, osassa näkyvät asiakkaan tiedot. Sen avulla voit myös tehdä toimintoja heti. Jos esimerkiksi asiakas jättää usein maksamatta, voit avata tietoruudussa asiakkaan kortin ja estää asiakasta ostamasta tulevaisuudessa.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a><a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a><a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a>Tietyn myyntiasiakirjan maksun ennusteen tarkasteleminen

Voit ennustaa myöhäiset maksut myös etukäteen. Voit käyttää **Myyntitarjoukset**-, **Myyntitilaukset**- ja **Myyntilaskut**-sivuilla **Ennusta maksu** -toimintoa ja luoda tarkasteltavalle myyntiasiakirjalle ennusteen.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** page you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="design-details"></a><a name="design-details"></a><a name="design-details"></a>Rakennetiedot

Microsoft ottaa käyttöön ja käyttää ennustavia verkkopalveluja kaikilla alueilla, joissa [!INCLUDE[prod_short](includes/prod_short.md)] on saatavilla. Näiden verkkopalveluiden käyttö sisältyy [!INCLUDE[prod_short](includes/prod_short.md)] -tilaukseen. Lisätietoja on Microsoft Dynamics 365 Business Centralin käyttöoikeusoppaassa. Opas on ladattavissa [Business Centralin](https://dynamics.microsoft.com/business-central/overview/) verkkosivulla.

Verkkopalvelut toimivat kolmessa seuraavassa tilassa:

* Koulutusmalli. Verkkopalvelu kouluttaa mallia annetun tietojoukon perusteella.
* Arviointimalli. Verkkopalvelu tarkistaa, palauttaako malli luotettavat tiedot annetusta tietojoukosta.
* Ennustus. Verkkopalvelu kohdistaa mallin annettuun tietojoukkoon ja tekee ennustuksen.

Näillä verkkopalveluilla ei ole tilaa. Ne siis käyttävät tietoja vain ennusteiden laskemiseen tarvittaessa. Ne eivät tallenna tietoja. 

> [!NOTE]  
> Voit käyttää omaa ennakoivaa verkkopalvelua meidän palvelumme sijaan. Lisätietoja on kohdassa [Oman ennustavan verkkopalvelun myöhästyneen maksun ennusteen luominen ja käyttäminen](#AnchorText).

### <a name="data-required-to-train-and-evaluate-the-model"></a><a name="data-required-to-train-and-evaluate-the-model"></a><a name="data-required-to-train-and-evaluate-the-model"></a>Tiedot, jotka vaaditaan mallin kouluttamista ja arvioimista varten

Jokainen **asiakastapahtumalle**, jolla on liittyvä **kirjattu myyntilasku**:

* Summa (LCY), joka sisältää veron
* Maksuehdot päivinä, laskutapa: **eräpäivä** vähennettynä **kirjauspäivällä**.
* Onko hyvityslasku kohdistettu. 

Lisäksi tietueeseen on lisätty koostetut tiedot muista samaan asiakkaaseen liittyvistä laskuista. Tämä sisältää seuraavat:

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

### <a name="standard-model-and-my-model"></a><a name="standard-model-and-my-model"></a><a name="standard-model-and-my-model"></a>Vakiomalli ja oma malli

Myöhästyneen maksun ennusteen laajennus käyttää ennakoivaa mallia, jonka kehittämisessä on käytetty pienten ja keskikokoisten yritysten tietoja vastaavia tietoja. Kun käynnistät laskujen kirjaamisen ja maksujen vastaanottamisen, [!INCLUDE[prod_short](includes/prod_short.md)] arvioi, vastaako vakiomalli liiketoimintaprosessiasi. 

Jos näyttää siltä, että prosessit eivät vastaa vakiomallia, voit yhä käyttää laajennusta, mutta sinun täytyy hakea lisää dataa. Vain jatkaa [!INCLUDE[prod_short](includes/prod_short.md)]:n käyttämistä.
> [!NOTE]
> Microsoft käyttää joka viikko hieman laskenta-aikaa, kun malli arvioidaan ja sitä koulutetaan lisää. 

[!INCLUDE[prod_short](includes/prod_short.md)] suorittaa koulutuksen ja arvioimisen automaattisesti, kun maksettuja ja myöhässä olevia laskuja on riittävästi saatavilla. Halutessasi voit suorittaa nämä manuaalisesti milloin tahansa.

#### <a name="to-train-and-use-your-model"></a><a name="to-train-and-use-your-model"></a><a name="to-train-and-use-your-model"></a>Mallin kouluttaminen ja käyttäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myöhästyneen maksun ennusteen asetukset** ja valitse sitten liittyvä linkki.  
2. Valitse **Valittu malli** -kentässä **Oma malli**.
3. Valitse **Luo oma malli** -toiminto, jos haluat kouluttaa tietojen mallia.  

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-late-payment-prediction"></a><a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-late-payment-prediction"></a><a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-late-payment-prediction"></a><a name="AnchorText"> </a>Oman ennakoivan verkkopalvelun luominen ja käyttäminen myöhässä olevan maksun ennustetta varten

Voit myös luoda oman ennakoivan verkkopalvelun **Dynamics 365 Business Centralin ennakoiva kokeilu** -nimisen julkisen mallin perusteella. Tämä ennakoiva malli on saatavana verkossa Azure AI Galleryssa. Voit käyttää mallia seuraavien vaiheiden avulla:  

1. Avaa selain ja siirry [Azure AI Galleryyn](https://go.microsoft.com/fwlink/?linkid=2086310).  
2. Hae **Dynamics 365 Business Centralin ennakoiva kokeilu** ja avaa malli Azure Machine Learning Studiossa.  
3. Kirjaudu työtilaan Microsoft-tilin avulla ja kopioi malli.  
4. Aja malli ja julkaise se verkkopalveluna.  
5. Kirjoita API:n URL-osoite ja API-avain muistiin. Näitä tunnistetietoja käytetään kassavirran asetuksissa.  
6. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myöhästyneen maksun ennusteen asetukset** ja valitse sitten liittyvä linkki.  
7. Valitse **Käytä omaa Azure-tilausta** -valintaruutu.
8. Syötä **Oman mallin tunnistetiedot** -pikavälilehteen mallin ohjelmointirajapinnan URL-osoite ja avain.  .  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/predict-late-payments-sales-documents/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Azure Machine Learning Studio -dokumentaatio](/azure/machine-learning/classic/)  
[Business Central -sovelluksen mukauttaminen laajennusten avulla](ui-extensions.md)  
[Tervetuloa [!INCLUDE[prod_long](includes/prod_long.md)]iin!](index.md)  
[Tekoälyn käyttäminen Microsoft Dynamics 365 Business Centralissa](/training/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
