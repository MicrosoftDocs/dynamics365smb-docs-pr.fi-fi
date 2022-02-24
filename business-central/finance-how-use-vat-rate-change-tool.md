---
title: Käytä ALV-kannan muutostyökalua | Microsoft-dokumentit
description: Käytä ALV-kannan muutostyökalua
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 04/01/2020
ms.author: andregu
ms.openlocfilehash: 76c6f8902e9661f4f4dbbbf70487a53bf286edb2
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183162"
---
# <a name="use-the-vat-rate-change-tool"></a>Käytä ALV-kannan muutostyökalua

## <a name="understanding-the-vat-rate-conversion-process"></a>Tietoja ALV-prosentin muutosprosessista  
ALV-prosentin muutostyökalu suorittaa päätietojen, päiväkirjojen ja tilauksien ALV-prosenttimuunnoksia eri tavoilla. Valitut perustiedot ja kirjauskansiot päivitetään uuden yleisen tuotteen kirjausryhmän tai ALV-tuotteen kirjausryhmän toimesta. Jos tilaus on kokonaan tai osittain toimitettu, toimitetut nimikkeet säilyvät nykyisessä tuotteen kirjausryhmässä tai tuotteen ALV-kirjausryhmässä. Uusi tilausrivi luodaan lähettämättömiä kohteita varten ja päivitetään nykyisen ja uuden ALV- tai yleisen tuotekirjausryhmän mukaan. Lisäksi nimikekulujen määritykset, varaukset ja nimikkeiden seurantatiedot päivitetään tämän mukaisesti.  

Työkalu ei tee muutoksia seuraavissa tilanteissa:

* Myynti- tai ostotilaukset ja laskut, jossa toimitukset on kirjattu. Nämä asiakirjat kirjataan käyttämällä nykyistä ALV-prosenttia.  
* Asiakirjat, joissa kirjattuja ennakkomaksulaskuja. Olet ehkä tehnyt ennakkomaksuja tai vastaanottanut niitä laskuista, joita ei ole tehty valmiiksi ennen ALV-prosentin muutostyökalun käyttämistä. Tässä tapauksessa erääntyvän ALV:n ja ennakkomaksuissa maksetun ALV:n välillä on ero, kun lasku on valmis. ALV-prosentin muutostyökalu ohittaa nämä asiakirjat ja ne täytyy päivittää manuaalisesti.  
* Suora toimitukset tai erikoistilaukset.  
* Varaston integroinnin sisältävät myynti- tai ostotilaukset, jos ne on osittain toimitettu tai vastaanotettu.  
* Huoltosopimukset.  

### <a name="to-prepare-vat-rate-change-conversions"></a>Suorita ALV-kurssimuutoksen muunnokset  
Ennen ALV:n muutostyökalun määrittämistä sinun on tehtävä seuraavat valmistelut.

* Jos sinulla on eri kursseja käyttäviä tapahtumia, ne on erotettava eri ryhmiin joko luomalla jokaiselle kurssille uusi pääkirjanpitotili tai ryhmittelemällä tapahtumat kurssin mukaan tietosuodattimien avulla.  
* Jos luot uusia kirjanpitotilejä, sinun on luotava myös uusia yleisiä kirjausryhmiä.  
* Vähentääksesi muunnettavien asiakirjojen määrää, kirjaa niin monta asiakirjaa kuin mahdollista ja vähennä kirjaamattomat asiakirjat minimiin.  
* Tietojen varmuuskopiointi.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Määritä ALV-prosentin muutostyökalu  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-prosentin muutos** ja valitse sitten liittyvä linkki.  
2. Valitse **Päätiedot**-, **Päiväkirjat**- ja **Asiakirjat**-pikavälilehdissä kirjausryhmän arvo tarvittavien kenttien asetusluettelosta. Kullekin ryhmälle voidaan valita, muunnetaanko tuotteen ALV-kirjausryhmät vai yleiset tuotteen kirjausryhmät vai muunnetaanko molemmat arvot, jos ne ovat käytettävissä päätietokohteessa. Joillakin alueilla voit myös asettaa suodattimen, joka muuntaa vain arvon alijoukon, esimerkiksi KP-tilit. 

### <a name="to-set-up-product-posting-group-conversion"></a>Määritä tuotteiden ALV-kirjausryhmien muunnos  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-prosentin muutos** ja valitse sitten liittyvä linkki.  
2. Valitse **ALV-prosenttimuutoksen asetukset** -sivulla joko **Tuotteen ALV-kirjausryhmän muunto** tai **Yleisen tuotteen kirjausryhmän muunto** -toiminto.  
3. Anna **Koodista** -kentässä nykyinen kirjausryhmä.  
4. Syötä uusi kirjausryhmä **Koodiin**-kenttään.  

### <a name="to-perform-vat-rate-change-conversion"></a>Suorita ALV-kurssimuutoksen muunnos  
ALV-prosentin muutostyökalun avulla voit hallita muutoksia ALV:n vakiokorvauksesta. Voit tehdä ALV- ja yleisen kirjausryhmän muunnokset muuttaaksesi ALV-prosentetia ja ylläpitääksesi ALV- raportointia. Asetusten mukaan tehdään seuraavat muutokset:  

* ALV-kirjausryhmät ja yleiset kirjauryhmät on muunnettu.  
* Muutokset toteutetaan esimerkiksi pääkirjanpitotileissä, asiakkaissa, toimittajissa, avoimissa asiakirjoissa ja päiväkirjariveillä.  

> [!IMPORTANT]  
>  Testaa muunto ennen ALV-prosentin muutosta. Voit tehdä sen seuraavien ohjeiden mukaisesti, mutta muista poistaa **Suorita muuntaminen**- ja **ALV-prosentin muutostyökalu valmis** -valintaruutujen valinta. Testimuunnoksen aikana **ALV-prosentin muutoslokin tapahtuma** -taulukon **Muunnettu**-kenttä tyhjennetään ja **ALV-prosentin muutoslokin tapahtuma** -taulukon **Muunnospvm** -kenttä on tyhjä. Kun muuntaminen on valmis, voit tarkastella testimuutoksen tulokset valitsemalla **ALV-prosentin muutoslokin tapahtumat**. Tarkista jokainen tapahtuma ennen muuntamista. Tarkista erityisesti tapahtumat, jotka käyttävät vanhaa ALV-prosenttia.     

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-prosentin muutos** ja valitse sitten **ALV-prosentin muutoksen asetukset** -linkki.  
2. Varmista, että olet jo määrittänyt tuotteen ALV-kirjausryhmän muunnoksen tai yleisen tuotteen kirjausryhmän muunnoksen.  
3. Valitse **Suorita muuntaminen** -valintaruutu.  

    > [!IMPORTANT]  
    >  Poista **ALV-prosentin muutostyökalu valmis** -valintaruudun valinta. Valintaruutu merkitään automaattisesti, kun ALV:n määrän muunnos on valmis.  

4. Valitse **Muunna**-toiminto.  
5. Kun muuntaminen on valmis, voit tarkastella muutoksen tulokset valitsemalla **ALV-prosentin muutoslokin tapahtumat** -toiminto.  

> [!IMPORTANT]  
>  Muutoksen jälkeen **ALV-prosentin muutoslokin tapahtuma** -taulukon **Muunnettu**-kenttä on valittuna ja **ALV-prosentin muutoslokin tapahtuma** -taulukon **Muunnospvm** -kentässä näkyy muunnospäivämäärä.  
## <a name="see-also"></a>Katso myös  
[Määritä arvonlisävero](finance-setup-vat.md)  
[Ei-realisoituneen arvonlisäveron määrittäminen](finance-setup-unrealized-vat.md)      
[ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)  
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)  
[Business Centralin paikalliset toiminnot](about-localization.md)
