---
title: Projektiresurssien ja -nimikkeiden kulutuksen tai käytön tallentaminen
description: Tässä ohjeaiheessa kerrotaan, miten projektien nimikkeiden tai resurssien kulutus tai käyttö tallennetaan projektinhallinnan helpottamiseksi.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.search.form: 89, 92, 201, 1007, 1014
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 01af14b826f2974cf9e4d3b5b351a46dd973665d
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8131279"
---
# <a name="record-consumption-or-usage-for-jobs"></a>Projektien kulutuksen tai käytön kirjaaminen

**Projektin suunnittelurivit** -sivulla voi tarkastella ja tallentaa projektin eri osien käyttötietoja, jotka päivitetään automaattisesti, kun muokkaat ja siirrät tietoja projektin ja projektipäiväkirjan tai projektin laskujen välillä. Tämä edellyttää, että projektissa on määritetty käyttöön **Käytä käyttölinkkiä** -kohta. Lisätietoja on kohdassa [Projektien määrittäminen](projects-how-setup-jobs.md).  

Voit syöttää esimerkiksi tyyppiä **Budjetti** oleville suunnitteluriveille resurssin määrän ja osoittaa, mikä määrä siirretään projektipäiväkirjaan. Jos suunnittelurivin tyyppi on **Laskutettava**, voit syöttää resurssin määrän ja määrittää laskulle siirrettävän määrän. Lisätietoja asiakkaan laskuttamisesta on kohdassa [Projektien laskuttaminen](projects-how-invoice-jobs.md). Vertaamalla alkuperäistä, jäljellä olevaa tai kirjattua määrää voit tarkastella käyttötietoja nopeasti. Lisätietoja budjetoitujen arvojen arvioinnista suunnittelun aikana on kohdassa [Projektibudjettien hallinta](projects-how-manage-budgets.md).  

Seuraavassa kuvataan, miten projektipäiväkirjan todelliset (budjetoidut) määrät ja kustannukset tallennetaan. Vaihtoehtoisesti voit käyttää ostoasiakirjoja projektin oston tallentamisessa. Lisätietoja on kohdassa [Projektin tarvikkeiden hallinta](projects-how-manage-project-supplies.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Käytön kirjaaminen Budjetti-tyypin projektin suunnitteluriville

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2. Valitse soveltuva projekti ja valitse sitten **Projektin suunnittelurivit** -toiminto.
3. Valitse projektin suunnittelurivin tyyppi, joka on **Budjetti** tai **Sekä budjetti että laskutettava** ja jolle haluat kirjata käytön.  

    > [!NOTE]
    > Voit myös tallentaa käytön **Laskutettava**-tyypin projektin suunnitteluriville. Yleensä tätä riviä käytetään laskujen luomisessa, mutta voit myös siirtää sen päiväkirjaan. Lisätietoja on kohdassa [Projektien laskuttaminen](projects-how-invoice-jobs.md) <!--However, when you do that, a job planning line of type **Budget** is created to match the billable line. For more information, see [Manage Job Budgets](projects-how-manage-budgets.md).-->

4. Kirjoita **Päiväkirjaan siirrettävä määrä** -kenttään määrä, jonka haluat siirtää laskuun. Oletusmäärä on **Määrä**-kenttään syöttämäsi arvo.

    **Jäljellä oleva määrä** -kentässä näkyy määrä, joka on jäljellä projektin valmiiksi suorittamista ja päiväkirjaan siirtämistä varten.  
5. Valitse **Luo projektipäiväkirjan rivit** -toiminto.

    > [!TIP]
    > Jos tähän projektiin on tarkoitus lisätä enemmän projektiin suunnittelurivejä, tee tämä määritys vasta, kun olet lisännyt kaikki projektin suunnittelurivit.
6. Täytä **Projektin siirron projektisuunnittelurivi** -sivulla kenttiä tarpeen mukaan ja valitse sitten **OK**-painike. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Valitse **Avaa projektipäiväkirja** -toiminto.  
8. Valitse **Projektipäiväkirja**-sivulla asianmukainen rivi ja valitse sitten **Kirjaa**-toiminto.
9. Tarkista **Projektin suunnittelurivit** -sivulla kirjattu käyttö **Määrä**-, **Jäljellä oleva määrä**- ja **Päiväkirjaan siirrettävä määrä** -kentän avulla.  
10. Kirjaa lisäkäyttö toistamalla vaiheet 3–8.  

## <a name="to-create-job-journal-lines-manually"></a>Luo projektipäiväkirjan rivit manuaalisesti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Valitse **Erän nimi** -kentässä asianmukaisen projektipäiväkirjan erä.  
3. Kirjoita uudelle riville asiakirjan numero, projektinumero, projektin tehtävän numero, tyyppi ja kulutettavan tyypin määrä.  
4. Kun projektipäiväkirjan rivit ovat valmiit, valitse **Kirjaa**-toiminto.  

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Projektin käytön arvioiden tarkasteleminen ja päivitysten kirjaaminen

Voit katsella projektin käyttöä projektin valmistumiseen asti yhden vaiheen avulla. Tämä tapahtuu käyttämällä **Laske projektin jäljellä oleva käyttö** -eräajoa kaikissa tehtävissä projektin alusta loppuun.  

Näin voit seurata ja vertailla alkuperäisiä arvioita todellisiin tuloksiin. Voit myös tehdä tarvittaessa muutoksia tai uusia tapahtumia. Olet esimerkiksi saattanut arvioida projektin kestoksi 10 tuntia, mutta aikaa on kulunut jo 15 tuntia. Voit lisätä viisi tuntia aiemmin luotuun päiväkirjariviin tai luoda uuden rivin, jolla nämä viisi tuntia raportoidaan ylityönä, joka on toinen työtyyppi. Sitten lasketaan oikeat kustannukset ja hinta, jotka voidaan kirjata päiväkirjaan.  

> [!NOTE]  
>   Nimiketapahtumat luovat nimiketapahtumia ja vähentävät varastomäärää. **Kirjaa varaston kustannus KP:oon** -eräajo siirtää kustannuksen varastosta pääkirjanpitoon. Resurssitapahtumat luovat resurssitapahtumia.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Valitse asianmukaisen projektin päiväkirja ja valitse sitten **Laske jäljellä oleva käyttö** -toiminto.  
3. Anna **Laske projektin jäljellä oleva käyttö** -sivulla päiväkirjaan lisättävä asiakirjan numero ja kirjauspäivämäärä. Valitse sitten **OK**-painike.  
4. Päivitä tarvittavat muutokset päiväkirjaan.  
5. Valitse **Kirjaa**.



## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Projektitapahtuman suunnittelurivien tarkasteleminen

Kun olet kirjannut projektipäiväkirjan rivit, näkyvissä ovat suunnittelurivit, jotka liittyvät kirjattuihin projektitapahtumiin.

> [!NOTE]  
> Tämä edellyttää sitä, että projektin **Käytä käyttölinkkiä** -valintaruutu on valittuna. Lisätietoja on kohdassa [Projektien määrittäminen](projects-how-setup-jobs.md).  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Valitse asianmukaisen projektin päiväkirja ja valitse sitten **Tapahtumakirjaukset**-toiminto.  
3. Valitse **Projektitapahtumat**-sivulla **Näytä linkitetyt projektin suunnittelurivit** -toiminto.

## <a name="see-also"></a>Katso myös
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
