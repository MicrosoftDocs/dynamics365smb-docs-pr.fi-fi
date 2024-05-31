---
title: Käyttäjien henkilökohtaisia tietoja koskeviin pyyntöihin vastaaminen
description: 'Tässä artikkelissa kerrotaan, miten henkilötietopyyntöihin vastataan.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/25/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Käyttäjien henkilökohtaisia tietoja koskeviin pyyntöihin vastaaminen

Tietojen kohteet voivat pyytää erilaisia henkilökohtaisia tietoja koskevia toimintoja. Esimerkiksi joidenkin tietosuojalakien ja -asetusten nojalla heillä on oikeus pyytää henkilötietojensa vientiä, poistamista ja muuttamista. Näitä kutsuja kutsutaan *Tietoaihe pyynnöiksi*. Jos olet luokitellut tietojen luottamuksellisuuden ja olet varma, että ne ovat oikein, järjestelmänvalvoja voi vastata pyyntöihin **IT-päällikkö**-roolikeskuksen **Tietosuoja**-välilehden vaihtoehtojen avulla.

## Pyyntöjen tyypit

Seuraavassa taulukossa on esimerkkejä pyyntötyypeistä, joihin järjestelmänvalvojat voivat vastata.

> [!Note]
> Tarjoamme mahdollisuuden vastata tämän tyyppisiin pyyntöihin ja henkilökohtaisten tietojen käyttöoikeuden. Käyttäjän vastuulle jää kuitenkin varmistaa, että henkilökohtaiset ja luottamukselliset tiedot tallennetaan ja luokitellaan asianmukaisesti.

|Pyynnön tyyppi|Kuvaus ja ehdotettu vastaus|
|-----|-----|
|Siirrettävyyttä koskevat pyynnöt|Tietojen kohde voi tehdä tietojen siirrettävyyttä koskevan pyynnön. Sinun täytyy viedä tietojen kohteen henkilökohtaiset tiedot järjestelmistä ja antaa ne jäsennellysti ja yleisesti käytetyssä muodossa. Voit vastata näihin pyyntöihin viemällä henkilökohtaiset tiedot Excel-tiedostoon tai RapidStart-määrityspakettiin **tietosuojatyökalun** avulla. Excelin avulla voit muokata henkilökohtaisia tietoja ja tallentaa ne yleisesti käytössä olevassa konekielisessä muodossa, kuten .csv- tai .xml-muodossa. RapidStart-määrityspakettien avulla voit määrittää päätietotaulukot ja niiden henkilökohtaisia tietoja sisältävät liittyvät taulukot. <br><br> **Huomautus:** Tietoja vietäessä on määritettävä luottamuksellisuuden vähimmäistaso. Vienti sisältää vähimmäistason sitä ylempien tasojen tiedot. Esimerkiksi jos viet tiedot, jotka on luokiteltu henkilökohtaisiksi, tuontiin kuuluvat myös tiedot, jotka luokitellaan luottamuksellisiksi. <br><br>Kun viedään tietojen kohteeseen liittyviä tietoja, **Tietosuojatyökalu** tietojen kohteen ja tietojen kohteeseen liittyvien tietojen suoria suhteita. **Tietosuojatyökalu** ei automaattisesti vie tietojen kohteeseen epäsuorasti liittyviä tietoja tai muita tietoja. Esimerkiksi Kontakti-taulukko liittyy suoraan Kontaktiprofiilin vastaukset -taulukkoon, joka edelleen liittyy suoraan Profiilikysymykset-tietoihin. Jos haluat viedä myös Profiilikysymykset-taulukon tiedot, sinun on lisättävä tämä taulukko manuaalisesti rivinä, jonka **Tietosuojatyökalu** luo asianmukaisten suodattamien avulla.|
|Poistopyynnöt|Tietojen kohde voi pyytää henkilökohtaisten tietojensa poistamista. Henkilökohtaiset tiedot voi poistaa useilla eri tavoilla mukautusominaisuuksien avulla. Käyttäjän on kuitenkin tehtävä päätös ja toteutus. Joissakin tapauksissa saatat haluta muokata tietojasi suoraan. Esimerkiksi yhteyshenkilö voidaan poistaa ja tämän jälkeen suorittaa Poista peruutettu vuorovaikutus -eräajo yhteyshenkilön vuorovaikutusten poistamiseksi. <br><br> **Huomautus:** Jos **Myyntien ja myyntisaamisten asetukset**- tai **Ostojen ja ostovelkojen asetukset** -sivujen **Salli asiakirjan poisto ennen** -kenttään on määritetty päivämäärä, saatat joutua muuttamaan päivämäärää, jotta voit poistaa kirjatut myynti- ja ostotositteet, joiden kirjauspäivämäärä on sama tai sitä aikaisempi.|
|Korjauspyynnöt|Tietojen kohde voi pyytää virheellisten henkilökohtaisten tietojen korjaamista. Sen voi tehdä usealla tavalla. Joissakin tapauksissa voit viedä luettelot Exceliin, joukkomuokata useita tietueita nopeasti ja tuoda sitten päivitetyt tiedot. Lisätietoja on kohdassa [Liiketoimintatietojen vieminen Exceliin](about-export-data.md). Voit muokata henkilökohtaisia tietoja sisältäviä kenttiä myös manuaalisesti. Tiedot voivat olla esimerkiksi asiakaskortin asiakasta koskevia tietoja. Tietueet, kuten yleinen-, asiakas-ja verotapahtumat, ovat kuitenkin tärkeitä. Jos liiketoimintatapahtumatietueisiin tallennetaan henkilökohtaisia tietoja, tietojen muokkaamisessa kannattaa käyttää mukautusominaisuuksia.|

## Tietojen kohteen tietojen käsittelyn rajoittaminen

Tietojen kohde voi pyytää henkilökohtaisten tietojensa käsittelyn tilapäistä lopettamista. Voit noudattaa pyyntöjä ja merkitä kyseiset tietueet estetyiksi tietosuojan vuoksi. Tällöin tietojen käsittely lopetetaan. Kun tietue on merkitty estetyksi, et voi luoda uusia tapahtumia, joissa kyseinen tietue on käytössä. Et voi esimerkiksi luoda asiakkaalle uutta laskua, jos asiakas tai myyjä on estetty. Voit merkitä tietojen kohteen estetyksi avaamalla tietojen kohteen kortin, esimerkiksi asiakkaan, toimittajan tai yhteyshenkilön kortin, ja valitsemalla **Estetty tietosuojan vuoksi** -valintaruudun. Sinun on ehkä valittava **Näytä lisää**, jotta kenttä näkyy.  

## Tietojen kohteen pyyntöjen käsittely kokeiluversiota käytettäessä

Tietyt henkilötiedot ovat osa Microsoft 365 -tiliä, ja vain järjestelmänvalvojat voivat viedä tiedot. Tietojen kohteen pyyntöjen käsittelyprosessi on erilainen [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajan tyypin mukaan.

Jos sinulla on maksettu [!INCLUDE[prod_short](includes/prod_short.md)] -tilaus, käyttäjien tulee kohdistaa tietojen kohteen pyyntö organisaationsa vuokraajien hallinnoijalle. Järjestelmänvalvojilla on järjestelmänvalvojien oikeudet ja työkalut tietojen kohteen pyyntöjen täyttämiseksi.

Jos olet rekisteröitynyt [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan [Kokeiluversiot](https://trials.dynamics.com/)-sivulta ja käytät edelleen kokeiluversiota, käyttäjät voivat ladata ja viedä omia tietojaan [Azure-portaalin Työn ja koulun tietosuojasivulle](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade).

Työpaikkojen ja oppilaitosten tietosuoja -sivulla voit myös sulkea tilisi. On kuitenkin suositeltavaa viedä ja poistaa kaikki tiedot ensin. Tilin poistaminen tarkoittaa, että menetät käyttöoikeuden [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan.

Voit edelleen merkitä henkilöitä estetyiksi tietosuojan vuoksi ja viedä, muokata tai poistaa tapahtumia tässä artikkelissa esitetyllä tavalla.  

## Tietojen vieminen taulukoista, joita ei ole luokiteltu tietojen aiheen mukaan

Jos sinun on vietävä tietoja, joita ei ole luokiteltu siten, että ne viedään automaattisesti, kuten tiedot Profiilin vastaukset -taulukosta, sinun on suoritettava seuraavat toimet:

* Harkitse, onko sinun todella vietävä sellaisia lisätietoja, jotka eivät liity suoraan kontaktiin.
* Lisää taulukko ja suhde manuaalisesti nopeaan aloituspakettiin ja vie se suoraan nopean käynnistyksen paketista. Luomme sinulle nopean aloituksen paketin, jotta voit muokata sitä tällaisissa tilanteissa.

## Alaikäisiä koskevien tietojen käsitteleminen

Jos yhteyshenkilö on niin nuori, ettei hän voi antaa laillista suostumusta alueen lakien mukaan, voit osoitaa tämän valitsemalla **Yhteyshenkilö**-kortin **Alaikäinen**-valintaruudun. Tällöin **Estetty tietosuojan vuoksi** -valintaruutu valitaan automaattisesti. Kun saat alaikäisen vanhemman tai laillisen huoltajan suostumuksen, voit valita **Vanhemman suostumus vastaanotettu** -valintaruudun, jolloin sisällön esto poistetaan. Voit käsitellä alaikäisten henkilökohtaisia tietoja, mutta et voi käyttää Dynamics 365 Salesin profilointitoimintoja.

> [!Note]
> Muutoslokiin voidaan tallentaa erilaisia tietoja, kuten esimerkiksi milloin **Vanhemman suostumus vastaanotettu** -valintaruutu valittiin ja kuka sen valitsi. Järjestelmänvalvoja voi määrittää tämän **Muutoslokin asetukset** -ohjeiden avulla ja myös valitsemalla **Yhteyshenkilö**-kortin **Vanhemman suostumus vastaanotettu -kohdan lokimuutos** -valintaruudun. Lisätietoja on kohdassa [Muutosten kirjaaminen lokiin](across-log-changes.md)  

### Katso myös

<!-- [Classifying Data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Classifying Data Sensitivity](admin-classifying-data-sensitivity.md)  -->
[Liiketoimintatietojen vieminen Exceliin](about-export-data.md)  
[Muutosten kirjaaminen lokiin](across-log-changes.md)  
[Tietojen kohteiden pyynnöt](/microsoft-365/compliance/gdpr-data-subject-requests)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
