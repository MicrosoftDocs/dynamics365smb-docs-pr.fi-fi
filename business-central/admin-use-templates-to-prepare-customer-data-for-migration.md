---
title: "Asiakastietojen siirtämisen valmisteleminen | Microsoft Docs"
description: "Kun olet tuonut ja ottanut käyttöön asetustiedot uuteen tietokantaan, voit aloittaa siirtämään asiakkaan nykyiset päätiedot, kuten nimikkeiden ja asiakkaiden numerot ja nimet. Varmista, että tiedot luodaan nopeasti ja tarkasti uudessa yrityksessä käyttämällä malleja tietojen järjestämiseen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3cfc53c1ea3c8d30f65b2d475a8dab052519e81e
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="prepare-to-migrate-customer-data"></a>Asiakastietojen siirtämisen valmisteleminen
Kun olet tuonut ja ottanut käyttöön asetustiedot uuteen tietokantaan, voit aloittaa siirtämään asiakkaan nykyiset päätiedot, kuten nimikkeiden ja asiakkaiden numerot ja nimet. Varmista, että tiedot luodaan nopeasti ja tarkasti uudessa yrityksessä käyttämällä malleja tietojen järjestämiseen.  

Yleensä voit luoda tietomallit seuraaville päätietotaulukoille:  

-   **Kontakti**  
-   **Asiakas**  
-   **Nimike**  
-   **Toimittaja**  

Voit kuitenkin luoda mallirakenteen ja kohdistaa sen mihin tahansa ohjelman [!INCLUDE[d365fin](includes/d365fin_md.md)] taulukkoon.  

> [!TIP]  
>  Voit myös käyttää tietueita päivittäisiin toimintoihin luodaksesi uusia tietueita, jotka perustuvat malleihin. Nämä tietomallit toimivat vain tuetuissa päätietotaulukoissa. Lisätietoja on esimerkiksi kohdassa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).  

Kun tuot asiakastietoja, kuten nimikkeille, tiedostosta, pakollinen-kenttätiedot, jotka olet määrittänyt, otetaanlinkitetystä tietomallista. Kun luot uuden kohteen, kirjoitat vain yleisiä tietoja, kuten nimi, kuvaus ja hinta ja keräät sitten loput pakolliset kenttätiedot valitusta tietomallista.  

Kun luot uuden päätietotietueen, kuten asiakaskortti, jotkin kentät ovat pakollisia, ja ne on täytettävä. Voit ryhmitellä useimmat pakolliset kentät, kuten kirjausryhmät ja maksuehdot, tehdäksesi päätietotietueiden luomisen entistä helpommaksi ja vakaammaksi. Voit esimerkiksi ryhmitellä taulukon 18 (**Asiakas**) pakolliset kentät tyypiksi **Kotimainen**, **Ulkomainen** tai  **Vienti**.

## <a name="to-select-a-data-template"></a>Valitse tietomalli.
Kun valitset olemassa olevan tietomalliin, sinun tulee arvioida, ovatko uudelle yritykselle luodut mallit riittäviä asiakkaalle. Tarkista annetut kentät ja arvot, jotka määrittävät, mitkä mallit sopivat uudelle yritykselle.  

> [!TIP]  
>  Tietomallien avulla voit luoda myös uusia tilien kortteja nopeasti. Käytä niitä nopeampaa ja vaivattomampaa tietojen luomista varten. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Määritysmallit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Määritä malliluettelo** -ikkunassa luettelosta tietomalli ja valitse sitten **Muokkaa**-toiminto.  

Jos oletusmallit eivät vastaa tarpeitasi, voit luoda uusia malleja tai lisätä olemassa olevaan malliin kenttiä. Jos oletusmallit ovat riittäviä, voit käyttää niitä tai luoda tietueita päätietomallien perusteella.

## <a name="to-create-a-data-template"></a>Tietomallin luominen
Voit luoda uuden tietomallin, jos oletusmallit eivät vastaa uuden yrityksen tarpeita. Jos aiot luoda useita, **Koodi**-kentän kohdalla kannattaa ehkä noudattaa nimeämiskäytäntöjä.

Kukin malli sisältää otsikon ja rivit. Kun olet luonut mallin, voit määrittää, mitä kenttiä käytät aina tietyn tyyppisten tietojen kanssa. Voit luoda erilaisia asiakasmalleja, jotka kohdistetaan eri asiakastyyppeihin. Kun luot asiakkaan mallin avulla, voit käyttää mallitietoja esitäyttääksesi tietyt kentät.

### <a name="to-create-a-data-template-header"></a>Luo tietomallin otsikko
1. Avaa **Määritä malliluettelo**-ikkuna.
2. Valitse **Uusi**-toiminto.
3. Anna **Taulukon tunnus** -kentässä taulukko, jota kyseinen malli koskee. **Taulukon nimi** -kenttä täytetään automaattisesti, kun **Taulukon tunnus** -kentän arvo on määritetty.

### <a name="to-create-a-data-template-line"></a>Luo tietomallin rivi
1. Valitse ensimmäisellä rivillä **Kentän nimi** -kenttä. **Kenttäluettelo**-ikkunassa näkyy luettelo taulukon kentistä.
2. Valitse kenttä ja valitse sitten **OK**-painike. **Kentän seloste** -kenttään täytetään kentän nimi.
3. Anna **Oletusarvo**-kenttään asianmukainen arvo. Joissakin tapauksissa haluat ehkä käyttää arvoa, joka ei ole käytettävissä tietokannassa. Tällöin voit valita tietojen virheettömän käytön valitsemalla **Ohita suhteen tarkistus** -valintaruudun.

    > [!TIP]  
    > Koska **Oletusarvo**-kentällä ei ole hakua vastaaviin [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman kenttäasetuksiin, kopioi ja liitä haluamasi arvo malliin asianmukaiselta sivulta.

    > Valitse **Pakollinen**-valintaruutu. Valintaruutu on vain tiedoksi. Se kertoo, että käyttäjän on syötettävä tiedot kenttään, mutta yrityslogiikkaa ei sovelleta. Esimerkiksi tilausta ei voi laskuttaa ja kirjata, jos kirjausryhmiä ei ole määritetty. Koska kirjausryhmät vaaditaan, voit valita **Pakollinen**-valintaruudun noille kentille.

3. Anna **Viite**-kenttään tarvittavat tiedot kentästä.
4. Valitse **OK**-painike.

## <a name="to-export-to-a-template-in-excel"></a>Mallin vieminen Exceliin
Voit luoda Excel-työkirjan malliksi, joka perustuu olemassa olevan tietokannan taulukon rakenteeseen nopeasti. Mallin avulla voit kerätä yhteen asiakastiedot yhdenmukaisessa muodossa myöhempää tuontia varten [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Määritystyökirja** ja valitse sitten aiheeseen liittyvä linkki.
2. Lisää taulukko luetteloon tai valitse aiemmin luotu taulukko. Lisätietoja on kohdassa [Yrityksen määrittämisen hallinta työkirjassa](admin-how-to-manage-company-configuration-in-a-worksheet.md).
3. Määritä kentät taulukosta, jonka haluat sisällyttää malliin.
4. Valitse **Vie malliin** -toiminto.
5. Nimeä ja tallenna Excel-tiedosto. Excel-työkirja avataan automaattisesti.

Voit nyt lisätä asiakkaan tiedot Excel-työkirjaan. Jos olet vienyt useita taulukoita, jokainen taulukko on omassa työkirjassaan. Tallenna työkirja ennen kuin jatkat seuraavaan vaiheeseen.

> [!NOTE]  
> Voit kohdata seuraavan virheen, kun käytät Excelin englanninkielistä versiota, mutta sinulla on aluekohtaisissa asetuksissa määritettynä muu kuin englannin kieli: Muoto on vanha tai tyyppikirjasto ei kelpaa. Korjaa tämä virhe varmistamalla, että kielipaketti muulle kuin englannin kielelle on asennettu.

## <a name="to-import-from-a-template-in-excel"></a>Excelin mallista tuominen
1. Valitse **Määritä työkirja** -ikkunassa **Tuo mallista** -toiminto.
3. Siirry luomaasi työkirjamalliin ja valitse **Avaa**-toiminto
4. Voit lisätä kerätyt asiakastiedot tietokantaan valitsemalla **Käytä tietoja** -toiminnon.

Kun käytät tietoja mallista Excel-taulukossa taulukkoon, jossa on myös kokoonpanomalli linkitettynä siihen kokoonpanopaketissa, kokoonpanomallin oletusarvokenttiä käytetään myös.

Tietue, jonka tietoja käytetään tällä tavalla on täydellinen, koska se koostuu Excelissä käyttäjän syöttämistä tiedoista sekä määritysmallin mukaisista oletusarvoista.

## <a name="to-create-a-record-from-a-configuration-template"></a>Luo tietue konfiguraatiomallista
Voit käyttää tietorakennetta, joka sisältyy tietomalleihin, muuntaaksesi tiedot malleihin tietokannassa, yksi kerrallaan. Tee tämä käyttämällä **Luo instanssi** -funktiota. Tämä on tietojen siirtoprosessi pienoiskoossa, ja siitä voi olla hyötyä luotaessa prototyyppejä tai käsiteltäessä pienempiä tietojenluontitehtäviä.  

Seuraavissa vaiheissa esitellään, miten nimikekortti luodaan nimiketietomallista. Voit luoda tietueen mistä tahansa tietomallista käyttäen samaa menettelyä.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Määritysmallit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **nimikemalli** ja valitse sitten **Muokkaa**-toiminto. Lisätietoja on Tietomallin luominen -osassa.
3. Valitse **Luo instanssi** -toiminto. Ohjelma luo nimikkeen kortin.  
4. Valitse **OK**-painike.  
5. Voit tarkistaa uuden nimikekortin valitsemalla ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvakkeen, kirjoittamalla **Nimikkeet** ja valitsemalla sitten aiheeseen liittyvän linkin.  
6. Avaa uusi nimikkeen kortti.  
7. Laajenna eri pikavälilehdet ja varmista, että niihin on syötetty oikeat tiedot.  

## <a name="to-use-a-configuration-template-on-a-record"></a>Käytä konfigruointimallia tietueessa
Voit käyttää tietomallia mihin tahansa tietueeseen, joka on [!INCLUDE[d365fin](includes/d365fin_md.md)] ja käyttää tätä tekniikkaa muuttaaksesi tai muokataksesi tietuetta. Kun teet tämän, tietueen aiemmin määritetyt arvot korvataan mallin arvoilla. Näin ollen sinun on oltava huolellinen, kun mallia sovelletaan olemassa oleviin tietueisiin.

> [!WARNING]  
>  **Sovella mallia** -toiminto korvaa nykyisen tietueen tiedot. Jos tätä funktiota käytetään päätietojen siirrossa, se korvaa tuodut tiedot tietueiden luonnin yhteydessä.

Seuraava toimenpide perustuu uuteen asiakaskorttiin.  

1. Luo asiakas. Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).
2. Valitse **Asiakkaan kortti** -ikkunassa **Käytä mallia** -toiminto.  
3. Valitse **Asiakasmallit**-ikkunassa jokin malleista ja valitse sitten **OK**-painike.  

Valitun asiakkaan mallin oletusarvot lisätään asiakaskorttiin.

## <a name="see-also"></a>Katso myös  
[Yrityksen määrittäminen RapidStart Services -palvelun avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)  
[Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md)

