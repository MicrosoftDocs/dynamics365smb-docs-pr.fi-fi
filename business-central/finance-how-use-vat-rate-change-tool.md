---
title: ALV-prosenttimuutosten hallinta
description: 'Lue, miten ALV-prosentin muutostyökalua käytetään Dynamics 365 Business Centralissa ALV-prosentin muuttamiseen paikallisen lainsäädännön mukaiseksi.'
author: andregu
ms.topic: conceptual
ms.reviewer: bholtorf
ms.workload: na
ms.search.keywords: 'VAT, VAT rate, posting, tax, value-added tax'
ms.search.form: '550,'
ms.date: 06/16/2021
ms.author: andregu
---

# <a name="managing-vat-rate-changes"></a>ALV-prosenttimuutosten hallinta

ALV-prosentit voivat muuttua paikallisen lainsäädännön mukaan. Kaikki ALV-muutokset vaikuttavat [!INCLUDE[prod_short](includes/prod_short.md)]in tietoihin riippumatta siitä, laskeeko vai nouseeko ALV-prosentti vai poistetaanko se. ALV on yhdistetty moniin [!INCLUDE[prod_short](includes/prod_short.md)]in entiteetteihin, kuten asiakkaisiin, toimittajiin, nimikkeisiin, resursseihin, nimikelukuihin ja pääkirjanpitotileihin. ALV-prosentit muuttuvat yleensä tiettynä päivänä, johon mennessä esimerkiksi ALV-asetukset ja kirjausryhmät on muutettu, sillä näin voidaan varmistaa, että uusia myynti- ja ostotilauksia luotaessa käytetään uutta ALV-prosenttia.

## <a name="changing-vat-rates"></a>ALV-prosenttien muuttaminen

Paras tapa hallita ALV-prosenttimuutosta on kirjata ja sulkea avoimet tilaukset ja muut asiakirjat ennen ALV-prosentin muutospäivää. Tällä tavoin voidaan varmistaa, muutos ei vaikuta niihin. Tämä on selkein toimintatapa, jonka ansiosta uusissa tilauksissa ja asiakirjoissa voidaan käyttää uutta ALV-prosenttia.

Ehdotettu tapa hallita ALV-prosenttimuutosta

1. Kirjaa ja sulje avoimet tilaukset, päiväkirjat ja muut asiakirjat kokonaan ennen vaihtopäivämäärää. Voit odottaa vaihtopäivän jälkeistä aikaa, kunhan uusia rivejä ei lisätä ja varmistat, että voimaantulopäivä on ennen vaihtopäivämäärää.  
2. Luo uudet ALV-asetukset.  
3. Tee ALV-vaihto entiteeteissä (esimerkiksi ne asiakkaat, toimittajat ja nimikkeet, joita se koskee).  
4. Luo ALV-prosentin vaihtopäivänä uutta prosenttia käyttävät uudet asiakirjat.  


> [!NOTE]  
> ALV-prosentin muutostyökalua päivitetään parhaillaan. Jäljempänä mainittavat toiminnot eivät vastaa ympäristön toimintoja. Päivitys on valmis 1. heinäkuuta 2020 mennessä, eikä se ole säännöllinen kuukausipäivitys. Kaikki ympäristöt päivitetään sen sijaan automaattisesti (hotfix). Kun tämä päivitys on valmis, sanomaa ei enää näytetä.  

## <a name="the-vat-rate-change-tool"></a>ALV-prosentin muutostyökalua

ALV-prosentin muutostyökalu auttaa jossain määrin päätietojen, päiväkirjojen ja tilausten ALV-prosenttien muuntamisessa. Se on kätevää, jos haluat helpottaa päätietojen ALV:n muuntoa tai jos joitakin tilauksia ei voi sulkea ennen vaihtopäivää ja niitä käsitellään pitkään, myös ALV-prosentin muutospäivän jälkeen. ALV-prosentin muutostyökaluun liittyy tiettyjä rajoituksia.

## <a name="understanding-the-vat-rate-conversion-process-and-limitations"></a>Tietoja ALV-prosentin muuntoprosessista ja sen rajoituksista

ALV-prosentin muutostyökalu suorittaa päätietojen, päiväkirjojen ja tilauksien ALV-prosenttimuunnoksia eri tavoilla. Valitut perustiedot ja kirjauskansiot päivitetään uuden yleisen tuotteen kirjausryhmän tai ALV-tuotteen kirjausryhmän toimesta. Jos tilaus on kokonaan tai osittain toimitettu, toimitetut nimikkeet säilyvät nykyisessä tuotteen kirjausryhmässä tai tuotteen ALV-kirjausryhmässä. Uusi tilausrivi luodaan lähettämättömiä kohteita varten ja päivitetään nykyisen ja uuden ALV- tai yleisen tuotekirjausryhmän mukaan. Lisäksi nimikekulujen määritykset, nimikkeiden mallimääritykset, varaukset ja nimikkeiden seurantatiedot päivitetään vastaavasti. 

Tilausrivien osalta yksikköhinta päivitetään kaikilla Nimike- ja Resurssi-tyypin riveillä, jos nimikkeen hinta sisältää ALV:n. Muiden rivityyppien osalta voi päättää, päivitetäänkö yksikköhinta.

Työkalu ei tee muutoksia seuraavissa tilanteissa:

* Myynti- tai ostotilaukset ja laskut, jossa toimitukset on kirjattu. Nämä asiakirjat kirjataan käyttämällä nykyistä ALV-prosenttia.  
* Asiakirjat, joissa kirjattuja ennakkomaksulaskuja. Olet ehkä tehnyt ennakkomaksuja tai vastaanottanut niitä laskuista, joita ei ole tehty valmiiksi ennen ALV-prosentin muutostyökalun käyttämistä. Tässä tapauksessa erääntyvän ALV:n ja ennakkomaksuissa maksetun ALV:n välillä on ero, kun lasku on valmis. ALV-prosentin muutostyökalu ohittaa nämä asiakirjat ja ne täytyy päivittää manuaalisesti.  
* Varaston integroinnin sisältävät myynti- tai ostotilaukset, jos ne on osittain toimitettu tai vastaanotettu.  
* Suoratoimitukset.
* Erikoistilaukset. 
* Kokoonpanotilaukset.
* Huoltosopimukset.  
* Hyvityslaskut.
* Palautustilaukset.
* Nimikkeiden hinnat (päätiedot)
* Myyntitietojen hinnat (päätiedot)
* Liiketoiminnan kirjausryhmät asiakkaiden ja toimittajien osalta.

### <a name="to-prepare-vat-rate-change-conversions"></a>Suorita ALV-kurssimuutoksen muunnokset

Ennen ALV:n muutostyökalun määrittämistä sinun on tehtävä seuraavat valmistelut.

* Jos sinulla on eri kursseja käyttäviä tapahtumia, ne on erotettava eri ryhmiin joko luomalla jokaiselle kurssille uusi pääkirjanpitotili tai ryhmittelemällä tapahtumat kurssin mukaan tietosuodattimien avulla.  
* Jos luot uusia kirjanpitotilejä, sinun on luotava myös uusia yleisiä kirjausryhmiä.  
* Vähentääksesi muunnettavien asiakirjojen määrää, kirjaa niin monta asiakirjaa kuin mahdollista ja vähennä kirjaamattomat asiakirjat minimiin.  
* Tietojen varmuuskopiointi.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Määritä ALV-prosentin muutostyökalu

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-prosenttimuutoksen asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **Päätiedot**-, **Päiväkirjat**- ja **Asiakirjat**-pikavälilehdissä kirjausryhmän arvo tarvittavien kenttien asetusluettelosta. Kullekin ryhmälle voidaan valita, muunnetaanko tuotteen ALV-kirjausryhmät vai yleiset tuotteen kirjausryhmät vai muunnetaanko molemmat arvot, jos ne ovat käytettävissä päätietokohteessa. Joillakin alueilla voit myös asettaa suodattimen, joka muuntaa vain arvon alijoukon, esimerkiksi KP-tilit. 
3. Valitse **Hinnat sisältävät ALV:n** -pikavälilehdessä rivityypit tilauksissa, joiden yksikköhinnat haluat päivittää. Nimike-ja Resurssi-tyypin rivien yksikköhinnat päivitetään aina.

### <a name="to-set-up-product-posting-group-conversion"></a>Määritä tuotteiden ALV-kirjausryhmien muunnos

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-prosenttimuutoksen asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **ALV-prosenttimuutoksen asetukset** -sivulla joko **Tuotteen ALV-kirjausryhmän muunto** tai **Yleisen tuotteen kirjausryhmän muunto** -toiminto.  
3. Anna **Koodista** -kentässä nykyinen kirjausryhmä.  
4. Syötä uusi kirjausryhmä **Koodiin**-kenttään.  

### <a name="to-perform-vat-rate-change-conversion"></a>Suorita ALV-kurssimuutoksen muunnos

ALV-prosentin muutostyökalun avulla voit hallita muutoksia ALV:n vakiokorvauksesta. Voit tehdä ALV- ja yleisen kirjausryhmän muunnokset muuttaaksesi ALV-prosentetia ja ylläpitääksesi ALV- raportointia. Asetusten mukaan tehdään seuraavat muutokset:  

* ALV-kirjausryhmät ja yleiset kirjauryhmät on muunnettu.  
* Muutokset toteutetaan esimerkiksi pääkirjanpitotileissä, asiakkaissa, toimittajissa, avoimissa asiakirjoissa ja päiväkirjariveillä.  

> [!IMPORTANT]  
> Testaa muunto ennen ALV-prosentin muutosta. Voit tehdä sen seuraavien ohjeiden mukaisesti, mutta muista poistaa **Suorita muuntaminen**- ja **ALV-prosentin muutostyökalu valmis** -valintaruutujen valinta. Testimuunnoksen aikana **ALV-prosentin muutoslokin tapahtuma** -taulukon **Muunnettu**-kenttä tyhjennetään ja **ALV-prosentin muutoslokin tapahtuma** -taulukon **Muunnospvm** -kenttä on tyhjä. Kun muuntaminen on valmis, voit tarkastella testimuutoksen tulokset valitsemalla **ALV-prosentin muutoslokin tapahtumat**. Tarkista jokainen tapahtuma ennen muuntamista. Tarkista erityisesti tapahtumat, jotka käyttävät vanhaa ALV-prosenttia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-prosentin muutos** ja valitse sitten **ALV-prosenttimuutoksen asetukset** -linkki.  
2. Varmista, että olet jo määrittänyt tuotteen ALV-kirjausryhmän muunnoksen tai yleisen tuotteen kirjausryhmän muunnoksen.  
3. Valitse **Suorita muuntaminen** -valintaruutu.  

    > [!IMPORTANT]  
    >  Poista **ALV-prosentin muutostyökalu valmis** -valintaruudun valinta. Valintaruutu merkitään automaattisesti, kun ALV:n määrän muunnos on valmis.  

4. Valitse **Muunna**-toiminto.  
5. Kun muuntaminen on valmis, voit tarkastella muutoksen tulokset valitsemalla **ALV-prosentin muutoslokin tapahtumat** -toiminto.  

> [!IMPORTANT]  
> Muutoksen jälkeen **ALV-prosentin muutoslokin tapahtuma** -taulukon **Muunnettu**-kenttä on valittuna ja **ALV-prosentin muutoslokin tapahtuma** -taulukon **Muunnospvm** -kentässä näkyy muunnospäivämäärä.  

## <a name="see-also"></a>Katso myös

[Arvonlisäveron määritys](finance-setup-vat.md)  
[Ei-realisoituneen arvonlisäveron määrittäminen](finance-setup-unrealized-vat.md)  
[ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  
[Business Centralin paikalliset toiminnot](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
