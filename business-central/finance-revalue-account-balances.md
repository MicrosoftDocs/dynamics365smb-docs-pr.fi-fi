---
title: Pääkirjanpitotilin saldojen uudelleenarvostus
description: Tietoja pääkirjanpitotilin saldojen uudelleenarvostuksesta ennen tilinpäätösten tuottamista.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/14/2024
ms.custom: bap-template
ms.search.form: null
ms.service: dynamics-365-business-central
---

# <a name="revalue-general-ledger-account-balances"></a>Pääkirjanpitotilin saldojen uudelleenarvostus

Jos pääkirjanpitotilejä (KP) käytetään rekisteröimään taseen nimikkeitä ulkomaanvaluuttoina, tilin saldot on arvostettava uudelleen ennen lopullisten tilipäätösten tuottamista. Valuuttakurssit muuttuvat usein ja uudelleenarvostus auttaa tarkentamaan tilinpäätöksiä.

## <a name="set-up-revaluations"></a>Uudelleenarvostusten määrittäminen

Jokainen uudelleenarvostukseen sisällytettävä tili määritetään **KP-tilin kortti**-sivulla. Valittavissa on, kirjataanko uudelleenarvostuksen muutokset realisoituneille vai ei-realisoituneiden voittojen ja tappioiden tileille. Voittojen ja tappioiden kirjaaminen valuuttakurssin muutoksen aikana noudattaa tavanomaista kirjausrutiinia. Se tehdään esimerkiksi kullekin **Valuutat**-sivun määritykselle. Lisätietoja vaihtokurssin muutoksista on kohdassa [Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md).

Virheet voidaan minimoida määrittämällä **Lähdevaluutan kirjaus** -kentässä tarkistuksen valuutoille, joiden kirjaaminen yksittäisille KP-tileille sallitaan:

* Kaikki valuutat (tyhjä)
* Useat valuutat
* Sama valuutta
* Paikallinen valuutta

## <a name="run-a-revaluation"></a>Uudelleenarvostuksen suorittaminen

Ulkomaanvaluutan summien uudelleenarvostus paikallisena valuuttana KP-tilin saldoihin tehdään käynnistämällä eräajo käyttämällä **KP-valuutan uudelleenarvostus** -toimintoa **Tilikartta**-sivulla. Eräajo luo muutostapahtumat valitussa päiväkirjassa. Tapahtumia kirjattaessa voidaan muuttaa tilin paikallisen valuutan (PVA) saldoa. Aina paikallisena valuuttana näytettävissä KP-tilin saldoissa näkyy nyt muutokset valuuttoihin, joissa tapahtumat kirjattiin. Tämä uudelleenarvostus mahdollistaa aiempaa tarkempien tilinpäätösten tuottaminen entistä vaivattomammin.

Jos käytössä on lisäraportointivaluutta (LVA), KP-uudelleenarvostustapahtumissa on LVA-summa. Summa vastaa vain näiden tapahtumien LVA-summaa eikä KP-tilin LVA-saldoa. Jos LVA-kurssia muutetaan muutosten kirjaamisen jälkeen, kaikkia KP-tapahtumia on muutettava suorittamalla valuutan vaihtokurssin muutos vielä kerran.

> [!IMPORTANT]
> KP-tilin uudelleenarvostus ei ehkä vastaa kaikkia uudelleenarvostusta edellyttävien tapahtuma- ja resurssirekisteröintien vaatimuksia. Tämä on tilanne esimerkiksi rahoitusinstrumenttien, arvopaperien ja vuokratun omaisuuden kohdalla sekä silloin, jos niitä käytetään tietyissä tapahtumissa tai resursseissa tai jos tapahtumia ja resursseja on runsaasti. Tämän ominaisuuden mahdollisesti käytöstä kannattaa keskustella tilintarkastajan käytöstä. Kyse voi olla tilanteesta, jossa tilillä saa esimerkiksi käyttää useita valuuttoja tai kullakin seurattavalla resurssilla on oltava erillinen tili.

> [!NOTE]
> Uudelleenarvostus ei mahdollista tapahtumien kohdistamista tai kohdistamisen peruuttamista, mikä on mahdollista asiakas- ja toimittajatapahtumissa. Saldon muutokset tehdään valuuttakohtaisesti.

## <a name="revaluate-accounts-vs-customer-and-vendor-exchange-rate-adjustments"></a>Tilien uudelleenarvostuksen vertailu asiakkaan ja toimittajan vaihtokurssin muutoksiin

Uudelleenarvostus yksinkertaistaa KP-tilin saldojen muuttamista. Tämä ominaisuus uudelleenarvostaa saldo valuutta- ja KP-tili-kohtaisesti, mikä vastaa muutosten tekemistä pankkitileihin linkitettyihin KP-tileihin. Jos KP-tiliä käytetään useiden resurssien seuraamiseen, kannattaa harkita sen sijaan toimittaja- tai asiakastilin käyttämistä.

> [!NOTE]
> KP-tilin uudelleenarvostus ei ehkä vastaa kaikkia uudelleenarvostusta edellyttävien tapahtuma- ja resurssirekisteröintien vaatimuksia. Tämä on tilanne esimerkiksi rahoitusinstrumenttien, arvopaperien ja vuokratun omaisuuden kohdalla sekä silloin, jos niitä käytetään tietyissä tapahtumissa tai resursseissa tai jos tapahtumia ja resursseja on runsaasti. Tämän ominaisuuden mahdollisesti käytöstä kannattaa keskustella tilintarkastajan käytöstä. Kyse voi olla tilanteesta, jossa tilillä saa esimerkiksi käyttää useita valuuttoja tai kullakin seurattavalla resurssilla on oltava erillinen tili.

Seuraavat esimerkit osoittavat, mikä ero on KP-tilin ja toimittajatilin käyttämisessä kahden ulkomaanvaluuttaa käyttävän rahavaran seuraamiseen.

**Käytä KP-tiliä** Jos yhtä KP-tiliä käytetään seuraamaan joko useita resursseja (kuten lainoja tai käyttöomaisuutta) samana valuuttana tai saman resurssien yksittäisiä osatapahtumia, joissa on sama valuutta, KP-uudelleenarvostuksessa tulee yksi tapahtuma kussakin valuutan uudelleenarvostuksessa. Tämän vuoksi yksittäisiin resursseihin tai saman resurssin yksittäisiin tapahtumiin liittyviä muutoksia ei voi seurata.

**Käytä toimittajatiliä** Jos useita resursseja määritetään toimittajiksi ja niihin kirjataan tapahtumia joka samana tai eri valuuttana, valuutta- ja toimittajakohtainen muutos saadaan. Tai jos **Tapahtumakohtainen kirjaus** otetaan käyttöön vaihtopainikkeella **Muuta valuutan vaihtokurssia** -työjonotapahtumassa, kullekin erilliselle toimittajatapahtumalle saadaan muutostapahtuma.

Tämä ero tärkeää arvioitaessa, vastaako KP-uudelleenarvostus ominaisuutena raportointitarpeita.

> [!TIP]
> Kirjanpitäjältä tai tilintarkastajalta kannattaa kysyä, minkä tyyppinen tili soveltuu omaan liiketoimintaan. [AppSourcessa](https://appsource.microsoft.com/en-us/marketplace/apps?page=1&product=dynamics-365-business-central) saattaa myös olla liiketoimintaskenaarioihin juuri sopiva [!INCLUDE [prod_short](includes/prod_short.md)]iin tarkoitettu sovellus.

## <a name="see-also"></a>Katso myös

[Summien tarkistaminen kirjanpitotileillä](finance-review-accounts.md)  
[Tietoja pääkirjanpidosta ja tilikartasta](finance-general-ledger.md)  
