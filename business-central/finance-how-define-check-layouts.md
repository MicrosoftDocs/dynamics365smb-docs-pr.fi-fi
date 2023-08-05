---
title: Sekin asettelun määrittäminen
description: Voit suunnitella ja tulostaa sekkisi eri muodoissa paikallisten viranomaisten säätämiä standardinmukaisia vaatimuksia noudattaen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'print check, customize'
ms.search.form: '374, 404'
ms.date: 06/16/2021
ms.author: edupont
---
# Sekin asettelun valitseminen

Voit suunnitella omat sekit, joiden avulla pystyt noudattamaan paikallisten viranomaisten määrittämiä standardeja. Sekkikuvat voidaan tulostaa englannin-, ranskan ja espanjankielisinä.

Sekit suunnitellaan tulostettavaksi sekä Yhdysvaltojen että Kanadan sekkikuvamuodoissa joko muodossa sekki-talonki-sekki tai talonki-talonki-sekki.

## Sekin asettelun valitseminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttivalintojen pankkitili** ja valitse sitten vastaava linkki.
2. Valitse **Raporttivalinta - Pankkitili** -sivun **Käyttö**-kentässä **Sekki**.
3. Valitse jompikumpi seuraavista raportin tunnuksista:

| Raportin tunnus | Raportin nimi | Kuvaus |
| --- | --- | --- |
| 1401 |Sekki |Tämä on oletusraportti. |
| 10411 |Sekki (talonki/talonki/sekki) |Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/talonki/sekki. |
| 10412 |Sekki (talonki/sekki/talonki) |Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/sekki/talonki. |
| 10413 |Kolme sekkiä sivulla |Tämä raportti on suunniteltu tulostamaan kolme sekkiä kullakin sivulla. |

Kun olet määrittänyt sekkien asettelut, voit tulostaa sekit **Maksupäiväkirja**-sivulla. Lisätietoja on kohdassa [Sekkien käyttäminen](payables-how-work-checks.md).

Voit muuttaa jotakin näistä sekkien oletusasetteluista käyttämällä joko Word- tai RDLC-integrointia. Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

## MICR- ja suojausfonttien käyttäminen
[!INCLUDE[prod_short](includes/prod_short.md)]:n online-versio sisältää valmiiksi asennetut fontit palvelimissa, joita voidaan käyttää sekin asettelujen määrittämisessä. Seuraavassa on esitetty, mitkä fontit ovat käytettävissä, ja siinä on linkit kolmansien osapuolten fonttien toimittajien yksityiskohtaisiin tietoihin.

> [!Important]
> MICR- ja sekki-suojausfontit Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)] on lisensoitu IDAutomation.com, Inc:n fonttipaketissa. Näitä tuotteita saa käyttää vain Microsoft Dynamicsin osana- ja yhteydessä [!INCLUDE[prod_short](includes/prod_short.md)].

Päivityksessä 15.3 ja uudemmissa on asennettu magneettisten merkkien tunnistuksen (MICR) fontteja, jotka ovat käytettävissä. Sekä E-13B- että CMC-7-standardit ovat tuettuja. MICR-fonttien lisäksi käytettävissä on erityisiä suojausfontteja, joiden avulla voidaan luoda tekstiä, nimiä, summia ja valuuttasymboleita: dollari, euro, punta ja jeni, joita on vaikea väärentää, kun sekki on tulostettu.

> [!NOTE]
> Suojaus- ja oikeudellisista syistä mukautettuja fontteja ei voi ladata [!INCLUDE[prod_short](includes/prod_short.md)]-ympäristöön.

### MICR E-13B -määritykset

Seuraavassa on yhteenveto MICR E-13B -fonteista, joista voi olla hyötyä, kun fontteja kalibroidaan sekkiasetteluissa tiettyjen MICR-tulostimien avulla.

![MICR E-13B -määritykset.](media/font_MICR_E-13B_Specifications.png "MICR E-13B -määritykset")

### Erottimen merkit

![Erottimen merkit.](media/font-micr-letters.png "Erottimen merkit")

MICR E-13B -fonttien kokomääritys löytyy toimittajan dokumentaatiosta täältä: (https://www.idautomation.com/micr-fonts/e13b/).

### MICR CMC-7 -määritykset

Seuraavat CMC-7 -fontit ovat käytettävissä [!INCLUDE[prod_short](includes/prod_short.md)] -online-käytössä:

- IDAutomationCMC7
- IDAutomationCMC7n10
- IDAutomationCMC7n25
- IDAutomationCMC7n40

Seuraavassa on yhteenveto MICR CMC-7 -fonteista, joista voi olla hyötyä, kun fontteja kalibroidaan sekkiasetteluissa tiettyjen MICR-tulostimien avulla.

![MICR CMC-7 -määritykset.](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7 -määritykset")

### Erottimen merkit

![Erottimen CMC-7-merkit.](media/font-cmc7-letters.png "Erottimen CMC-7-merkit")

MICR CMC-7 -fonttien kokomääritys löytyy toimittajan dokumentaatiosta täältä: (http://www.idautomation.com/micr-fonts/cmc7/).

### Suojattujen fonttien määritykset

Seuraavassa on yhteenveto sekkisuojausfonteista, joista voi olla hyötyä, kun fontteja kalibroidaan sekkiasetteluissa tiettyjen MICR-tulostimien avulla.

![Suojausfonttien määritysten tarkistaminen.](media/font_check-security-font_Specifications.png "Suojausfonttien määritysten tarkistaminen")

Sekkisuojausfonttien kokomääritys löytyy toimittajan dokumentaatiosta täältä: (https://www.idautomation.com/security-fonts/).

Fontit muihin tarkoituksiin ovat myös saatavilla [!INCLUDE[prod_short](includes/prod_short.md)]. Lisätietoja on kohdassa [Käytettävissä olevat fontit](ui-fonts.md)

## Katso myös

[Raporttien mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)  
[Fontit Business Centralissa](ui-fonts.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)   
[Kauden lopun prosessien viimeisteleminen](year-how-complete-period-end-processes.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]