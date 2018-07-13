---
title: "Henkilökohtaisia tietoja koskeviin pyyntöihin vastaaminen"
description: "Tietojen kohteen pyyntöihin on vastattava."
author: bholtorf
ms.service: dynamics365-business-central
ms.author: bholtorf
ms.custom: na
ms.date: 05/25/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: b90577cbab4167894fe79a3e8e8a0c61ce8c70e9
ms.contentlocale: fi-fi
ms.lasthandoff: 06/28/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Henkilökohtaisia tietoja koskeviin pyyntöihin vastaaminen  
Tietojen kohteet voivat pyytää erilaisia henkilökohtaisia tietoja koskevia toimintoja. Esimerkiksi yleisen tietosuoja-asetuksen (GDPR) ansiosta, EU-alueella asuvilla on oikeus pyytää henkilökohtaisten tietojensa vientiä, poistamista ja muokkaamista. Tätä kutsutaan *tietojen kohteen pyynnöksi*. Jos olet luokitellut tietojen luottamuksellisuuden ja olet varma, että ne ovat oikein, järjestelmänvalvoja voi vastata pyyntöihin **käyttäjien, käyttäjäryhmien ja käyttöoikeuksien hallinnan** roolikeskuksen **Tietosuoja**-kohdan määritysten avulla. Jos käytössä on Windows-asiakasohjelma, järjestelmänvalvoja voi käyttää **IT-päällikkö**-roolikeskusta. Lisätietoja tietojen luokittelusta ja tietojen luottamuksellisuuden luokittelusta [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]ssa on kohdissa [Tietojen luokitteleminen](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) ja [Tietojen luottamuksellisuuden luokitteleminen](admin-classifying-data-sensitivity.md).  

## <a name="types-of-requests"></a>Pyyntöjen tyypit

Seuraavassa taulukossa on esimerkkejä pyyntötyypeistä, joihin voit vastata.

> [!Note]
> Tarjoamme mahdollisuuden vastata tämän tyyppisiin pyyntöihin ja henkilökohtaisten tietojen käyttöoikeuden. Käyttäjän vastuulle jää kuitenkin varmistaa, että henkilökohtaiset ja luottamukselliset tiedot tallennetaan ja luokitellaan asianmukaisesti.

|Pyynnön tyyppi|Kuvaus ja ehdotettu vastaus|
|-----|-----|
|Siirrettävyyttä koskevat pyynnöt|Tietojen kohde voi tehdä tietojen siirrettävyyttä koskevan pyynnön. Se tarkoittaa, että tietojen kohteen henkilökohtaiset tiedot on vietävä järjestelmästä jäsennetyssä ja yleisesti käytössä olevassa muodossa. Voit vastata näihin pyyntöihin viemällä henkilökohtaiset tiedot Excel-tiedostoon tai RapidStart-määrityspakettiin **tietosuojatyökalun** avulla. Excelin avulla voit muokata henkilökohtaisia tietoja ja tallentaa ne yleisesti käytössä olevassa konekielisessä muodossa, kuten .csv- tai .xml-muodossa. RapidStart-määrityspakettien avulla voit määrittää päätietotaulukot ja niiden henkilökohtaisia tietoja sisältävät liittyvät taulukot. <br><br> **Huomautus:** Tietoja vietäessä on määritettävä luottamuksellisuuden vähimmäistaso. Vienti sisältää vähimmäistason sitä ylempien tasojen tiedot. Esimerkiksi jos haluat viedä tiedot, jotka on luokiteltu henkilökohtaisiksi, tuontiin kuuluvat myös tiedot, jotka luokitellaan luottamuksellisiksi. <br><br>Kun viedään tietojen kohteeseen liittyviä tietoja, **Tietosuojatyökalu** tietojen kohteen ja tietojen kohteeseen liittyvien tietojen suoria suhteita. **Tietosuojatyökalu** ei automaattisesti vie tietojen kohteeseen epäsuorasti liittyviä tietoja tai muita tietoja. Esimerkiksi Kontakti-taulukko liittyy suoraan Kontaktiprofiilin vastaukset -taulukkoon, joka edelleen liittyy suoraan Profiilikysymykset-tietoihin. Jos haluat viedä myös Profiilikysymykset-taulukon tiedot, sinun on lisättävä tämä taulukko manuaalisesti rivinä, jonka **Tietosuojatyökalu** luo asianmukaisten suodattamien avulla.|
|Poistopyynnöt|Tietojen kohde voi pyytää henkilökohtaisten tietojensa poistamista. Henkilökohtaiset tiedot voi poistaa useilla eri tavoilla mukautusominaisuuksien avulla. Käyttäjän on kuitenkin tehtävä päätös ja toteutus. Joissakin tapauksissa tietoja halutaan muokata suoraan. Esimerkiksi yhteyshenkilö voidaan poistaa ja tämän jälkeen suorittaa Poista peruutettu vuorovaikutus -eräajo yhteyshenkilön vuorovaikutusten poistamiseksi. <br><br> **Huomautus:** Jos **Myyntien ja myyntisaamisten asetukset**- tai **Ostojen ja ostovelkojen asetukset** -sivujen **Salli asiakirjan poisto ennen** -kenttään on määritetty päivämäärä, sitä on ehkä muutettava, jotta tulostetut kirjatut myynti- ja ostoasiakirjat voidaan poistaa, koska niiden kirjauspäivämäärä saattaa olla kyseinen päivämäärä tai sitä aiempi päivämäärä.|
|Korjauspyynnöt|Tietojen kohde voi pyytää virheellisten henkilökohtaisten tietojen korjaamista. Sen voi tehdä usealla tavalla. Joissakin tapauksissa voit viedä luettelot Exceliin, joukkomuokata useita tietueita nopeasti ja tuoda sitten päivitetyt tiedot. Lisätietoja on kohdassa [Liiketoimintatietojen vieminen Exceliin](about-export-data.md). Voit muokata henkilökohtaisia tietoja sisältäviä kenttiä myös manuaalisesti. Tiedot voivat olla esimerkiksi asiakaskortin asiakasta koskevia tietoja. Tapahtumatietueet, kuten yleiset tapahtumat, asiakastapahtumat ja verotapahtumat, ovat tärkeitä toiminnanohjausjärjestelmän eheyden kannalta. Jos liiketoimintatapahtumatietueisiin tallennetaan henkilökohtaisia tietoja, tietojen muokkaamisessa kannattaa käyttää mukautusominaisuuksia.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Tietojen kohteen tietojen käsittelyn rajoittaminen
Tietojen kohde voi pyytää henkilökohtaisten tietojensa käsittelyn tilapäistä lopettamista. Voit noudattaa pyyntöjä ja merkitä kyseiset tietueet estetyiksi tietosuojan vuoksi. Tällöin tietojen käsittely lopetetaan. Kun tietue on merkitty estetyksi, et voi luoda uusia tapahtumia, joissa kyseinen tietue on käytössä. Et voi esimerkiksi luoda asiakkaalle uutta laskua, jos asiakas tai myyjä on estetty. Voit merkitä tietojen kohteen estetyksi avaamalla tietojen kohteen kortin, esimerkiksi asiakkaan, toimittajan tai yhteyshenkilön kortin, ja valitsemalla **Estetty tietosuojan vuoksi** -valintaruudun. Sinun on ehkä valittava **Näytä lisää**, jotta kenttä näkyy.  

## <a name="handling-data-subject-requests-while-in-trial"></a>Tietojen kohteen pyyntöjen käsittely kokeiluversiossa
Tietyn tyyppiset henkilötiedot ovat osa omaa Office 365 -tiliäsi. Näiden tietojen vieminen vaatii järjestelmänvalvojan oikeudet, jos saat tietojen kohteen pyynnön, joka koskee tämän tyyppisiä henkilökohtaisia tietoja, joihin sovelletaan yleistä tietosuoja-asetusta (GDPR). Tietojen kohteen pyyntöjen käsittelyprosessi on erilainen [!INCLUDE[d365fin](includes/d365fin_md.md)] -vuokraajan tyypin mukaan.  

Jos sinulla on maksettu [!INCLUDE[d365fin](includes/d365fin_md.md)] -tilaus, kohdista tietojen kohteen pyyntö organisaatiosi vuokraajien hallinnoijalle. Järjestelmänvalvojalla on järjestelmänvalvojan oikeudet ja työkalut pyynnön täyttämiseksi.  

Jos olet rekisteröinyt [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen [Kokeilut](https://trials.dynamics.com/)-sivulta, etkä ole siirtynyt tästä kokeiluversiosta maksettuun tilaukseen organisaatiosi vuokraajien järjestelmänvalvojan avulla, voit täyttää tietojen kohteen pyynnön [Azure-portaalin Työpaikkojen ja oppilaitosten tietosuoja -sivulla](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade). Tässä voit viedä ja ladata henkilötietojasi.

Työpaikkojen ja oppilaitosten tietosuoja -sivulla voit myös sulkea tilisi. Kannattaa kuitenkin varmistaa, että olet vienyt ja poistanut kaikki tiedot ensin, koska tilin poistaminen tarkoittaa sitä, menetät mahdollisuuden käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellusta.  

Voit edelleen merkitä henkilöitä estetyiksi tietosuojan vuoksi ja viedä, muokata tai poistaa tapahtumia tässä artikkelissa esitetyllä tavalla.  

## <a name="exporting-data-from-tables-not-classified-by-data-subject"></a>Tietojen vieminen taulukoista, joita ei ole luokiteltu tietojen aiheen mukaan
Jos vietävänä on tietoja (kuten Profiilin vastaukset -taulukon tiedot), joiden luokittelu ei mahdollista automaattista vientiä, toimi seuraavasti: 
-   Varmista, haluatko viedä nämä lisätiedot tai onko ne pakko viedä, jos tiedot eivä tliity kontaktiin eli tiedoilla ja kontaktilla ei ole suoraa suhdetta 
-   Lisää tämä taulukko ja suhde manuaalisesti RapidStart-pakettiin ja vie ne suoraan RapidStart-paketista. RapidStart-paketti on luotu juuri sitä varten, että voit käyttää sitä tämänkaltaisissa tilanteissa.

## <a name="handling-data-about-minors"></a>Alaikäisiä koskevien tietojen käsitteleminen
Jos yhteyshenkilö on niin nuori, ettei hän voi antaa laillista suostumusta alueen lakien mukaan, voit osoitaa tämän valitsemalla **Yhteyshenkilö**-kortin **Alaikäinen**-valintaruudun. Tällöin **Estetty tietosuojan vuoksi** -valintaruutu valitaan automaattisesti. Kun saat alaikäisen vanhemman tai laillisen huoltajan suostumuksen, voit valita **Vanhemman suostumus vastaanotettu** -valintaruudun, jolloin sisällön esto poistetaan. Voit käsitellä alaikäisten henkilökohtaisia tietoja, mutta et voi käyttää Microsoft Dynamics 365 for Sales -sovelluksen profilointitoimintoja.

> [!Note]
> Muutoslokiin voidaan tallentaa erilaisia tietoja, kuten esimerkiksi milloin **Vanhemman suostumus vastaanotettu** -valintaruutu valittiin ja kuka sen valitsi. Järjestelmänvalvoja voi määrittää tämän **Muutoslokin asetukset** -ohjeiden avulla ja myös valitsemalla **Yhteyshenkilö**-kortin **Vanhemman suostumus vastaanotettu -kohdan lokimuutos** -valintaruudun. Lisätietoja on kohdassa [Muutosten kirjaaminen lokiin](across-log-changes.md)  

## <a name="see-also"></a>Katso myös
[Tietojen luokitteleminen](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Tietojen luottamuksellisuuden luokitteleminen](admin-classifying-data-sensitivity.md)  
[Liiketoimintatietojen vieminen Exceliin](about-export-data.md)  
[Muutosten kirjaaminen lokiin](across-log-changes.md)  
[Tietojen kohteiden pyynnöt – GDPR](/microsoft-365/compliance/gdpr-data-subject-requests)  

