---
title: "Henkilökohtaisia tietoja koskeviin pyyntöihin vastaaminen"
description: "Tietojen kohteen pyyntöihin on vastattava."
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.date: 03/13/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 89f53f24f74401ce384b54d04fbeb473aedad96d
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Henkilökohtaisia tietoja koskeviin pyyntöihin vastaaminen  
Tietojen kohteet voivat pyytää erilaisia henkilökohtaisia tietoja koskevia toimintoja. Jos olet luokitellut tietojen luottamuksellisuuden ja olet varma, että ne ovat oikein, järjestelmänvalvoja voi vastata pyyntöihin **käyttäjien, käyttäjäryhmien ja käyttöoikeuksien hallinnan** roolikeskuksen tietojen luokittelun työkirjan avulla. Jos käytössä on Windows-asiakasohjelma, järjestelmänvalvoja voi käyttää **IT-päällikön** roolikeskusta. Lisätietoja tietojen luokittelusta ja tietojen luottamuksellisuuden luokittelusta on kohdissa [Tietojen luokitteleminen](/dynamics-nav/classifying-data) ja [Tietojen luottamuksellisuuden luokitteleminen](admin-classifying-data-sensitivity.md).

Seuraavassa taulukossa on esimerkkejä pyyntötyypeistä, joihin voit vastata.

> [!Note]
> Tarjoamme mahdollisuuden vastata tämän tyyppisiin pyyntöihin ja henkilökohtaisten tietojen käyttöoikeuden. Käyttäjän vastuulle jää kuitenkin varmistaa, että henkilökohtaiset ja luottamukselliset tiedot tallennetaan ja luokitellaan asianmukaisesti.

|Pyynnön tyyppi|Kuvaus ja ehdotettu vastaus|
|-----|-----|
|Siirrettävyyttä koskevat pyynnöt|Tietojen kohde voi tehdä tietojen siirrettävyyttä koskevan pyynnön. Se tarkoittaa, että tietojen kohteen henkilökohtaiset tiedot on vietävä järjestelmästä jäsennetyssä ja yleisesti käytössä olevassa muodossa. Voit vastata näihin pyyntöihin viemällä henkilökohtaiset tiedot Excel-tiedostoon tietosuojatyökalun avulla. Excelin avulla voit muokata henkilökohtaisia tietoja ja tallentaa ne yleisesti käytössä olevassa konekielisessä muodossa, kuten .csv- tai .xml-muodossa. Järjestelmänvalvojat voi myös viedä tietoja RapidStart-määrityspakettien avulla ja määrittää sitten päätietotaulukot ja niiden henkilökohtaisia tietoja sisältävät liittyvät taulukot. |
|Poistopyynnöt|Tietojen kohde voi pyytää henkilökohtaisten tietojensa poistamista. Henkilökohtaiset tiedot voi poistaa useilla eri tavoilla mukautusominaisuuksien avulla. Käyttäjän on kuitenkin tehtävä päätös ja toteutus. Joissakin tapauksissa tietoja halutaan muokata suoraan. Esimerkiksi yhteyshenkilö voidaan poistaa ja tämän jälkeen suorittaa Poista peruutettu vuorovaikutus -eräajo yhteyshenkilön vuorovaikutusten poistamiseksi. <br><br> **Huomautus:** Jos **Myyntien ja myyntisaamisten asetukset**- tai **Ostojen ja ostovelkojen asetukset** -sivujen **Salli asiakirjan poisto ennen** -kenttään on määritetty päivämäärä, sitä on ehkä muutettava, jotta tulostetut kirjatut myynti- ja ostoasiakirjat voidaan poistaa, koska niiden kirjauspäivämäärä saattaa olla kyseinen päivämäärä tai sitä aiempi päivämäärä.|
|Korjauspyynnöt|Tietojen kohde voi pyytää virheellisten henkilökohtaisten tietojen korjaamista. Sen voi tehdä usealla tavalla. Joissakin tapauksissa voit viedä luettelot Exceliin, joukkomuokata useita tietueita nopeasti ja tuoda sitten päivitetyt tiedot. Lisätietoja on kohdassa [Liiketoimintatietojen vieminen Exceliin](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data). Voit muokata henkilökohtaisia tietoja sisältäviä kenttiä myös manuaalisesti. Tiedot voivat olla esimerkiksi asiakaskortin asiakasta koskevia tietoja. Tapahtumatietueet, kuten yleiset tapahtumat, asiakastapahtumat ja verotapahtumat, ovat tärkeitä toiminnanohjausjärjestelmän eheyden kannalta. Jos liiketoimintatapahtumatietueisiin tallennetaan henkilökohtaisia tietoja, tietojen muokkaamisessa kannattaa käyttää mukautusominaisuuksia.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Tietojen kohteen tietojen käsittelyn rajoittaminen
Tietojen kohde voi pyytää henkilökohtaisten tietojensa käsittelyn tilapäistä lopettamista. Voit noudattaa pyyntöjä ja merkitä kyseiset tietueet estetyiksi tietosuojan vuoksi. Tällöin tietojen käsittely lopetetaan. Kun tietue on merkitty estetyksi, et voi luoda uusia tapahtumia, joissa kyseinen tietue on käytössä. Et voi esimerkiksi luoda asiakkaalle uutta laskua, jos asiakas tai myyjä on estetty. Voit merkitä tietojen kohteen estetyksi avaamalla tietojen kohteen kortin, esimerkiksi asiakkaan, toimittajan tai yhteyshenkilön kortin, ja valitsemalla **Estetty tietosuojan vuoksi** -valintaruudun. Sinun on ehkä valittava **Näytä lisää**, jotta kenttä näkyy.

## <a name="handling-data-about-minors"></a>Alaikäisiä koskevien tietojen käsitteleminen
Jos yhteyshenkilö on niin nuori, ettei hän voi antaa laillista suostumusta alueen lakien mukaan, voit osoitaa tämän valitsemalla **Yhteyshenkilö**-kortin **Alaikäinen**-valintaruudun. Tällöin **Estetty tietosuojan vuoksi** -valintaruutu valitaan automaattisesti. Kun saat alaikäisen vanhemman tai laillisen huoltajan suostumuksen, voit valita **Vanhemman suostumus vastaanotettu** -valintaruudun, jolloin sisällön esto poistetaan. Voit käsitellä alaikäisten henkilökohtaisia tietoja, mutta et voi käyttää Microsoft Dynamics 365 for Sales -sovelluksen profilointitoimintoja.

> [!Note]
> Muutoslokiin voidaan tallentaa erilaisia tietoja, kuten esimerkiksi milloin **Vanhemman suostumus vastaanotettu** -valintaruutu valittiin ja kuka sen valitsi. Järjestelmänvalvoja voi määrittää tämän **Muutoslokin asetukset** -ohjeiden avulla ja myös valitsemalla **Yhteyshenkilö**-kortin **Vanhemman suostumus vastaanotettu -kohdan lokimuutos** -valintaruudun. Lisätietoja on kohdassa [Muutosten kirjaaminen lokiin](/dynamics-nav-app/across-log-changes)  

## <a name="see-also"></a>Katso myös
[Tietojen luokitteleminen](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data)  
[Tietojen luottamuksellisuuden luokitteleminen](admin-classifying-data-sensitivity.md)  
[Liiketoimintatietojen vieminen Exceliin](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data)  

