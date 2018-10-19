---
title: "Myyntiasiakirjojen myöhästyvien maksujen ennustaminen | Microsoft Docs"
description: "Käytä ennakoivaa malliamme, kun haluat ennustaa, suoritetaanko laskun maksu ajoissa."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer, payment, invoice, sales, invoice, quote
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 960c8bcd172602a8ab5ea8f3774740bd63fe8ff6
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="the-late-payment-prediction-extension"></a>Myöhästyneen maksun ennusteen laajennus  
Tehokas myyntisaamisten hallinta on tärkeää yrityksen taloudellisen tilanteen yleiskuvan kannalta. Myöhästyneen maksun ennusteen laajennus voi auttaa avointen myyntisaamisten vähentämisessä ja perintästrategian tarkentamisessa ennustamalla, maksetaanko myyntilaskut ajoissa. Jos maksun ennustetaan olevan myöhässä, voit esimerkiksi muuttaa asiakkaan maksuehtoja tai maksutapaa.

## <a name="what-are-predictions-based-on"></a>Mihin ennusteet perustuvat?  
Myöhästyneen maksun ennusteen laajennus käyttää ennakoivaa mallia, joka on kehitetty Azure Machine Learning Studiossa. Sen kehittämisessä käytettiin tietoja, jotka vastaavat pienten ja keskikokoisten yritysten tietoja. Vaikka ennakoiva malli on jo kehitetty käsittelemään tietoja ja se on arvioitu, malli oppii lisää organisaatiosi tietojen avulla. Mitä enemmän käytät mallia ja syötät siihen tietoja, sitä tarkempia ennusteista tulee. Oletusarvoisesti laajennus arvioi mallin ja päivittää ennusteet viikoittan. Voit kuitenkin päivittää ennusteet aina halutessasi valitsemalla **Päivitä ennuste** -toiminnon **Asiakastapahtumat**-ikkunassa.  

> [!Note]
> Microsoft käyttää joka viikko hieman laskenta-aikaa, kun malli arvioidaan ja ennusteet päivitetään. Sen lisäksi, että ennusteita päivitetään manuaalisesti, laskenta-aikaa kuluttavat muut toiminnot silloin, kun mallia kehitetään (kehitystä saatetaan tehdä, jos tietoja on lisätty äskettäin) ja kun mallia arvioidaan (eli tarkastellaan mallin laatua).

## <a name="getting-started"></a>Aloitusopas
Laajennus on [!INCLUDE[d365fin](includes/d365fin_md.md)]:n ilmainen osa. Azure Machine Learning -tilaus on myös saatavana. Tilaus sisältää 30 minuuttia laskenta-aikaa kuukaudessa. Jos tarvitset enemmän, voit luoda oman ennakoivan mallin ja käyttää sitä tämän sijaan. Lisätietoja on myöhemmin tämän ohjeaiheen _Oman ennakoivan mallin luominen_ -osassa.  

Kun avaat kirjatun myyntiasiakirjan, ikkunan yläosaan tulee ilmoitus. Jos haluat käyttää myöhästyneen maksun ennusteen laajennusta, voit suostua sen käyttöön valitsemalla ilmoituksen **Ota käyttöön** -kohdan. Vaihtoehtoisesti voit määrittää laajennuksen manuaalisesti. Näin voit tehdä esimerkiksi silloin, jos kadut ilmoituksen ohittamista.  

Voit ottaa laajennuksen käyttöön manuaalisesti seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Palvelun yhteydet** ja valitse sitten liittyvä linkki.  
2. Valitse **Myöhästyneen maksun ennusteen asetus** -vaihtoehto ja täytä tarvittavat kentät.

## <a name="viewing-all-payment-predictions"></a>Kaikkien maksujen ennusteiden tarkasteleminen
Jos otat käyttöön laajennuksen, **Maksut, joiden on ennustettu olevan myöhässä** -ruutu on käytettävissä **liiketoimintajohtajan** roolikeskuksessa. Ruudussa on niiden maksujen määrä, joiden ennustetaan olevan myöhässä. Sen avulla voit avata **Asiakastapahtumat**-ikkunan, jossa on lisätietoja kirjatuista laskuista. Kiinnitä huomiota seuraaviin kolmeen sarakkeeseen:  

* **Myöhästynyt maksu** - Osoittaa, onko laskun maksun ennustettu olevan myöhässä.
* **Ennusteen luotettavuus** - Osoittaa, miten luotettava ennuste on. **Suuri** tarkoittaa, että ennusteen luotettavuus on 90 %, **normaali** 80–90 % ja **pieni** alle 80 %.
* **Ennusteen luotettavuus-%** - Osoittaa luottamusluokituksen todellisen prosenttiosuuden. Tämä sarake ei näy oletusarvoisesti, mutta voit lisätä sen halutessasi. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

> [!Tip]
> Asiakastapahtumat-ikkunan oikeassa reunassa on tietoruutu. **Asiakkaan tiedot** -osan tiedot voivat olla hyödyllisiä, kun tarkastelet ennusteita. Kun valitset luettelosta laskun, osassa näkyvät asiakkaan tiedot. Sen avulla voit myös tehdä toimintoja heti. Jos esimerkiksi asiakas jättää usein maksamatta, voit avata tietoruudussa asiakkaan kortin ja estää asiakasta ostamasta tulevaisuudessa.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a>Tietyn myyntiasiakirjan maksun ennusteen tarkasteleminen
Voit ennustaa myöhäiset maksut myös etukäteen. Voit käyttää **Myyntitarjoukset**-, **Myyntitilaukset**- ja **Myyntilaskut**-ikkunoissa **Ennusta maksu** -toimintoa ja luoda tarkasteltavalle myyntiasiakirjalle ennusteen.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** window you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="building-your-own-predictive-model"></a>Oman ennakoivan mallin luominen
Haluatko luoda oman ennakoivan mallin? Voit luoda oman ennakoivan mallin Azure Machine Learning Studion avulla ja käyttää sitä [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä. Sinun on tilattava Azure Machine Learning, jotta voit käyttää omaa mallia. Lisätietoja on kohdassa [Azure Machine Learning Studio -dokumentaatio](https://go.microsoft.com/fwlink/?linkid=861765).  

Microsoft kuitenkin tarjoaa helpomman tavan oman ennakoivan mallin luomista ja käyttämistä varten. Voit jakaa laskujen tiedot ennakoivan kokeilumme kanssa Azure Machine Learning -sovelluksessa. Luomme ja kehitämme ennakoivan mallin tietojesi perusteella. Jos haluat jakaa tiedot, valitse **Myöhästyneen maksun ennusteen asetus** -ikkunassa **Luo oma malli** -toiminto. Tämän jälkeen ennusteet perustuvat Microsoftin mallin sijaan omaan malliisi ja omiin tietoihisi.  

> [!Note]
>   Mallin laatu on tärkeä seikka. Kun ennakoiva kokeilumme käyttää tietojasi ja kehittää mallin, se määrittää mallille laadun arvon prosenttiosuutena. Mallin laatu osoittaa, miten tarkkoja mallin ennusteista tulee. Useat tekijät voivat vaikuttaa mallin laatuun. Tällaisia tekijöitä ovat esimerkiksi se, että tietoja ei ole riittävästi tai tiedoissa ei ollut riittävästi muunnoksia. Voit tarkastella tällä hetkellä käytössä olevan mallin laatua **Myöhästyneen maksun ennusteen asetus** -ikkunassa. Voit myös määrittää mallin laadulle vähimmäisrajan. Mallit, joiden laadun arvo on rajaa pienempi, eivät luo ennusteita.  

### <a name="to-use-your-model-instead-of-ours"></a>Oman mallin käyttäminen Microsoftin mallin sijaan  
Jos luot oman mallin Azure Machine Learning Studio -sovelluksessa ilman [!INCLUDE[d365fin](includes/d365fin_md.md)]:n työkaluja, sinun on annettava tunnistetiedot, jotta [!INCLUDE[d365fin](includes/d365fin_md.md)] voi käyttää mallia. Se sisältää seuraavat vaiheet:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myöhästyneen maksun ennusteen asetus** ja valitse sitten liittyvä linkki.  
2. Valitse **Käytä omaa Azure-tilausta** -valintaruutu.  
3. Valitse **Valittu malli** -kentässä **Oma malli**.  
4. Syötä **Oman mallin tunnistetiedot** -pikavälilehteen mallin ohjelmointirajapinnan URL-osoite ja avain.  

## <a name="see-also"></a>Katso myös  
[Azure Machine Learning Studio -dokumentaatio](https://go.microsoft.com/fwlink/?linkid=861765)  
[Business Central -sovelluksen mukauttaminen laajennusten avulla](ui-extensions.md)  
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)  

