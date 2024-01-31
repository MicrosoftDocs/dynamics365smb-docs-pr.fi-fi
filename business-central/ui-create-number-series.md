---
title: Numerosarjojen luominen
description: 'Katso, miten määritetään numerosarjat, jotka määrittävät yksilölliset tunnuskoodit Business Central -sovelluksen tileille ja asiakirjoille.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'numbers, numbering'
ms.search.form: '456, 457, 458, 459, 460, 461, 21, 22, 26, 27, 31'
ms.date: 03/24/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Numerosarjojen luominen

Jokaiselle yritykselle on määritettävä yksilölliset tunnuskoodit esimerkiksi pääkirjanpidon tilejä, asiakas- ja toimittajatilejä, laskuja ja muita asiakirjoja varten. Numerointi ei ole tärkeää pelkästään tunnistamisen kannalta. Hyvin suunniteltu numerointijärjestelmä helpottaa myös yrityksen hallittavuutta ja analysointia ja voi vähentää tietojen syötössä tapahtuvien virheiden määrää.

> [!Important]
> Numerosarjoissa ei oletusarvoisesti sallita aukkoja, koska lainsäädäntö edellyttää, että rahoitustapahtumien täsmällinen historia on oltava käytettävissä tilintarkastuksessa, minkä vuoksi järjestyksen on oltava katkeamaton ilman poistettuja numeroita.
> 
> Jos haluat sallia aukot tietyissä numerosarjoissa, varmista ensin tilintarkistajalta tai talouspäälliköltä, että noudatat maan tai alueen lakisääteisiä vaatimuksia. Lisätietoja on kohdassa [Numerosarjojen aukot](#gaps-in-number-series).

> [!NOTE]  
> On suositeltavaa käyttää niitä numerosarjan koodeja, jotka on mainittu CRONUS-esittely-yrityksen **Numerosarjaluettelo**-sivulla. Koodit, kuten *O-LASKU+*, eivät ehkä avaudu heti, mutta [!INCLUDE[prod_short](includes/prod_short.md)]issa on tiettyjä oletusasetuksia, jotka perustuvat näihin numerosarjan koodeihin.

Numerointijärjestelmä luodaan määrittämällä koodeja kullekin perustietotyypille tai asiakirjalle. Voit määrittää koodin esimerkiksi asiakkaiden, myyntilaskujen ja yleisten päiväkirjojen numerointia varten. Kun olet määrittänyt koodin, sinun on määritettävä vähintään yksi numerosarjarivi. Numerosarjarivit sisältävät erilaisia tietoja, kuten sarjan ensimmäisen ja viimeisen numeron sekä alkupäivämäärän. Voit määrittää yhtä numerosarjakoodia kohti useita numerosarjarivejä, joilla kullakin on eri alkupäivämäärä. Numerosarjoja käytetään peräkkäin kulloisestakin alkupäivämäärästä alkaen.

> [!NOTE]
> Numerosarjan luvun enimmäispituus on 20 merkkiä. Joissakin tilanteissa [!INCLUDE[prod_short](includes/prod_short.md)] liittää lukuun järjestelmän muodostaman tunnuksen. Jos esimerkiksi asiakirjojen, kuten laskuja, käytetään tapahtumien, kuten maksujen, kohdistamiseen, [!INCLUDE[prod_short](includes/prod_short.md)] luo tunnukset kohdistetuille tapahtumille. Tunnus koostuu numerosarjan luvusta ja kuusimerkkisestä järjestelmän määrittämästä tunnuksesta, kuten -12345. Jos käsiteltävissä olevissa pankki- tai pankkisiirtokirjauskansioissa tai kassapäiväkirjoissa odotetaan olevan yli 9 999 asiakirjaa, kyseisten asiakirjatyyppien numerosarjoihin on määritettävä alle 14 merkkiä.

Numerosarjat määritetään yleensä lisäämään seuraava peräkkäinen numero automaattisesti luotuihin uusiin kortteihin tai asiakirjoihin. Voit kuitenkin määrittää myös numerosarjoja, joissa uuden numeron voi antaa manuaalisesti. Se määritetään **Manuaaliset nrot** -valintaruudussa.

Jos haluat käyttää useita numerosarjakoodeja yhdelle perustietotyypille (esimerkiksi silloin, kun haluat eri numerosarjoja eri nimikeluokille), voit käyttää numerosarjasuhteita.

## Numerosarjojen aukot
Kaikki [!INCLUDE[prod_short](includes/prod_short.md)]issa luotavat tietueet eivät ole rahoitustapahtumia, joissa on käytettävä peräkkäisiä numeroita. Esimerkiksi asiakaskortit, myyntitarjoukset ja varastotoiminnot ovat tietueita, joille määritetään numerosarjan mukainen numero mutta joita tilintarkastus ei koske ja/tai jotka voidaan poistaa. Tällaisissa numerosarjoissa **Salli välit numeroissa** -valintaruudun voi valita **Nrosarjojen rivit** -sivulla. Tämän asetuksen voi muuttaa myös numerosarjan luomisen jälkeen. Lisätietoja on kohdassa [Uuden numerosarjan luominen](ui-create-number-series.md#to-create-a-new-number-series).

## Nro-kentän toiminta asiakirjoissa ja korteissa

Myynti-, osto- ja siirtoasiakirjojen ja korttien **Nro** -kenttä voidaan täyttää automaattisesti esimääritetystä numerosarjasta, tai voit lisätä sen manuaalisesti. Tietyissä olosuhteissa **Nro** -kenttä on näkymätön sen muokkaamisen estämiseksi.  

**Nro**-kenttä voidaan täyttää kolmella tavalla:

1. Jos asiakirjantyypillä tai kortilla on vain yksi numerosarja, ja **Oletusnrot**-kenttä on valittu mutta **Manuaaliset nrot** -kenttää ei ole valittu kyseiselle numerosarjalle, kenttä täytetään automaattisesti sarjan seuraavalla numerolla. **Nro**-kenttä -kenttä ei näy kortissa tai asiakirjassa.  

    Vaikka määriteltäisiin malleja, joissa on useita numerosarjoja asiakkaille, jos **Myyntien ja myyntisaamisten asetukset** -sivulla määritetty numerosarja määritetään tällä tavalla, **Nro** -kenttä on näkymätön asiakaskortissa riippumatta siitä, mitä mallia käytät. Sama pätee muun tyyppisiin kortteihin ja asiakirjoihin.  

    > [!NOTE]  
    > Jos numerosarja ei toimi esimerkiksi siksi, että sen numerot ovat loppuneet, tällöin **Nro**-kenttä on näkyvissä ja voit kirjoittaa numeron manuaalisesti tai ratkaista ongelmat **Nrosarja**-sivulla.

2. Jos asiakirjatyypillä tai kortilla on useita numerosarjoja eikä nykyisen kohdistetun numerosarjan **Oletusnrot**-valintaruutua ole valittu, **Nro**-kenttä näkyy ja voit valita käytettävän numerosarjan **Nrosarja**-sivulla. Sarjan seuraava numero lisätään sitten **Nro** -kentässä.

3. Jos asiakirjatyypin tai kortin numerosarjaa ei ole määritetty tai jos numerosarjoille on valittu **Manuaaliset nrot** -kenttä, **Nro**-kenttä näkyy ja numerot on annettava manuaalisesti. Voit kirjoittaa enintään 20 merkkiä, sekä numeroita että kirjaimia.

Kun uuden asiakirjan tai kortin, jolla on jo numerosarja, vastaava **Numerosarja-asetukset**-sivu avautuu. Voit määrittää tällä sivulla kyseisen asiakirjatyypin tai kortin numerosarjan, ennen kuin jatkat muiden tietojen antamista.

> [!NOTE]  
> Jos manuaalinen numerointi on otettava käyttöön esimerkiksi uusissa korteissa, jotka luoneessa tietojen siirtoprosessissa **Nro**-kenttä on oletusarvoisesti piilotettu, siirry **Varastonhallinnan asetukset** -sivulle ja valitse **Nimikenrot**-kenttä. Voit nyt avata ja määrittää liittyvien numerosarjojen asetuksiksi **Manuaaliset nrot**.

## Uuden numerosarjan luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nrosarja** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.  
3. Täytä tarvittavat uuden rivin kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Valitse **Rivit**-toiminto.  
5. Määritä vaiheessa 2 luodun numerosarjan varsinainen käyttö ja sisältö täyttämällä **Nrosarjan rivit** -sivun kentät.  
6. Toista vaihe 5 niin monta kertaa kuin käytät numerosarjoja eri tavoin. **Aloituspvm**-kenttä määrittää, mikä numerosarjan rivi on aktiivinen.  

> [!TIP]
> Jos haluat, että käyttäjät voivat määrittää numeroita manuaalisesti, kun he rekisteröivät uuden asiakkaan tai toimittajan, valitse **Manuaaliset nrot** -kenttä itse numerosarjassa. Jos haluat estää manuaaliset numerot, tyhjennä kenttä.

Voit määrittää numerosarjoja niille malleille, jotka määrität myynti- ja ostohenkilöstön useimmin tuotteeseen [!INCLUDE [prod_short](includes/prod_short.md)] lisäämille erilaisille asiakas- ja toimittajatyypeille. Määritä tällöin asianmukaiset numerosarjat, linkitä ne suhteiden avulla ja lisää sitten kulloisenkin suhteen ensimmäinen numerosarja kulloiseenkin määrityssivuun. Kun käyttäjä luo asiakkaan, hän valitsee asianmukaisen mallin, ja uusi asiakas saa numeron, joka on määritetty kyseiseen malliin määritetystä numerosarjasta.  

## Numerosarjojen suhteiden luonti

Jos tietylle perustiedolle tai tapahtumalle on luotu useampia numerosarjoja, näiden koodien välille voidaan luoda suhteita. Tämä toiminto auttaa koodien valinnassa kun käytetään numeroa. Kun määrität suhteen usean numerosarjan välille, liität kaikki toisiinsa liittyvät sarjat yhteen numerosarjan koodiin. Sitten voit syöttää tämän koodin kenttään **Numerointi**-pikavälilehdessä jollakin asianosaisista määrityssivuilta (esim. **Myyntien ja myyntisaamisten asetukset**).  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nrosarja** ja valitse sitten vastaava linkki.
2. Valitse numerosarjoja sisältävä rivi, jolle haluat luoda suhteita. Valitse sitten **Suhteet**.
3. Kirjoita **Sarjakoodi**-kenttään sen numerosarjan koodi, johon haluat luoda suhteen vaiheessa 2 valitusta sarjasta.
4. Lisää rivi kullekin valittuun numerosarjaan liitettävälle koodille.
5. Sulje sivu.

Kun tarvitset numeron voit käyttää niitä suhteita, joita on luotu numerosarjojen valitsemiseksi.

## Numerosarjan käyttökohteen määrittäminen

Seuraavaksi selitetään, miten myyntialueen numerosarja määritetään. Myös muut alueet määritetään vastaavasti.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myynnit ja saatavat** ja valitse sitten vastaava linkki.
2. Valitse **Myynnit ja myyntisaamiset** -sivun **Numerosarja**-pikavälilehdessä sopiva numerosarja kullekin myyntikortille tai -asiakirjalle.

Valitulla numerolla täytetään kyseisen kortin tai asiakirjan **Nro**-kenttä numerosarjarivillä tehtyjen asetusten mukaisesti.  

## Katso myös

[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
