---
title: Laskun pyöristyksen määrittäminen
description: 'Jos laskujen summat on pyöristettävä laskuja luotaessa, voit käyttää automaattista pyöristystoimintoa, joka selitetään seuraavassa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5, 16, 118, 459, 460, 495'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Laskun pyöristyksen määrittäminen
Jos laskujen summat on pyöristettävä laskuja luotaessa, voit käyttää automaattista pyöristystoimintoa. Kun lasku pyöristetään, lisätään lisärivi, joka sisältää pyöristyssumman ja joka kirjataan muiden laskurivien kanssa.

> [!NOTE]  
>  Paikalliset määräykset tai tavat saattavat vaatia laskun pyöristystä tietyllä tavalla (esimerkiksi niin, että summa on jaollinen luvulla 0,05).  

Jos haluat käyttää automaattista laskun pyöristystä, sinun on  

* määritettävä kirjanpitotilit, joille pyöristyserot kirjataan  
* määritettävä laskujen pyöristyksen säännöt paikallista valuuttaa ja ulkomaanvaluuttaa varten  
* aktivoitava toiminto.  

> [!NOTE]  
>  Laskun pyöristysominaisuuksien lisäksi laskujen summien pyöristyksessä voi käyttää yksikkösumman ja summan pyöristysominaisuuksia.  

## KP-tilien määrittäminen laskun kohdistuksen pyöristyseroille
Kun haluat käyttää ohjelman automaattista laskunpyöristystoimintoa, sinun täytyy määrittää se KP-tili (tai ne KP-tilit), joille pyöristyserot kirjataan. Sitä ennen sinun täytyy luoda tuotteen ALV-kirjausryhmät. Lisätietoja on kohdassa [ALV:n määrittäminen](finance-setup-vat.md).  

### KP-tilien määrittäminen laskun kohdistuksen pyöristyseroille  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten vastaava linkki.  
2. Määritä tili **Tilikartta**-sivulla ja anna sen nimeksi esimerkiksi **Laskun pyöristys**. [!INCLUDE[prod_short](includes/prod_short.md)] käyttää tätä tilin nimeä pyöristetyissä laskuissa.  
3. Valitse **Veron ALV-kirjausryhmä**- tai **Tuotteen ALV-kirjausryhmä** -kentässä pyöristettyjen summien kirjausryhmä sen mukaan, onko kyseessä ALV- vai myyntivero. Voit halutessasi määrittää uuden ryhmäkoodin laskun pyöristystä varten.
4. Jätä **Yleinen kirjaustyyppi**- ja joko **Liiketoiminnan veron kirjausryhmä**- tai **Liiketoiminnan ALV-kirjausryhmä** -kenttä tyhjäksi. <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  

Voit nyt määrittää laskun pyöristystilin kirjausryhmille **Toimittajan kirjausryhmät** -sivulla.  <!-- Why only the vendor posting groups? -->

## Ulkomaan valuutan ja paikallisen valuutan pyöristämisen määrittäminen
Ulkomaanvaluutan ja paikallisen valuutan pyöristämissäännöt on määritettävä ennen automaattisen pyöristystoiminnon käyttöä.

### Ulkomaan valuuttojen pyöristyssääntöjen määrittäminen  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Valuutat** ja valitse sitten vastaava linkki.  
2. Avaa **Valuutan kortti** valitsemalla **Valuutat**-sivulla ulkomaanvaluutta ja täytä sitten **Summan pyöristystarkkuus**-, **Yksikkösumman pyöristystarkkuus**-, **Laskun pyöristystarkkuus**- ja **Laskun pyöristystyyppi** -kentät.

### Paikallisen valuutan pyöristyssääntöjen määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset** ja valitse sitten vastaava linkki.  
2. Täytä **Pääkirjanpidon asetukset** -sivun **Yleiset**-pikavälilehdessä **Laskun pyöristystarkkuus**- ja **Laskun pyöristystyyppi** -kentät.  

## Laskun pyöristystoiminnon aktivointi  
Laskun pyöristystoiminto on aktivoitava, jotta voit varmistaa myynti- ja ostolaskujen automaattisen pyöristyksen. Voit aktivoida laskunpyöristyksen erikseen myynti- ja ostolaskuille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntien ja myyntisaamisten asetukset** tai **Ostojen ja ostovelkojen asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **Yleiset**-pikavälilehdessä **Laskun pyöristys** -valintaruutu.  

## Katso myös  
[Myynnin laskutus](sales-how-invoice-sales.md)  
[Ostojen kirjaus](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]