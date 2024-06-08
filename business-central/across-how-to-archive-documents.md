---
title: Myyntien ja myyntiasiakirjojen arkistointi
description: 'Voit arkistoida myynti-ja ostotilauksia, tarjouksia, palautustilauksia ja puitetilauksia.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/26/2024
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
ms.service: dynamics-365-business-central
---
# Asiakirjojen arkistoiminen

Voit arkistoida myynti-ja ostotilauksia, tarjouksia, palautustilauksia ja puitetilauksia. Jos käytössä projektinhallinnan ominaisuuksia, projekteja voidaan myös arkistoida. Asiakirjoja ja projekteja voidaan arkistoida useita kertoja, jolloin kullakin kerralla tallennetaan erilainen arkistoitu versio.

Jos kyse on myyntiasiakirjoista, joiden alkuperäinen versio on vielä olemassa eikä sitä ole kirjattu, voit korvata sen arkistoidulla versiolla **Palauta**-toiminnolla. 

> [!NOTE]
> Vain myyntiasiakirjoja ja projekteja voidaan palauttaa. Toiminto ei ole käytettävissä arkistoiduissa ostoasiakirjoissa.

Jos kyse on arkistoiduista asiakirjoista, joiden alkuperäinen versio on poistettu, voit käyttää sisällön uudelleen kopioimalla tiedot esimerkiksi **Kopioi asiakirjasta** -toiminnolla  

## Asiakirjojen automaattisen arkistoinnin määrittäminen

Arkistointi voidaan automatisoida luomaan uusi versio arkistoidusta asiakirjasta, kun joku tekee seuraavat asiat:

* Asiakirjan tai projektin muuttaminen tai poistaminen.
* Asiakirjan tulostaminen, lataaminen tai sähköpostitse lähettäminen.
* Tarjouksen muuntaminen tilaukseksi tai laskuksi.
* Kirjaa tilauksen.

Seuraavat vaiheet käsittelevät myyntiasiakirjojen automaattisen arkistoinnin määrittämistä **Myyntien ja myyntisaamisten asetukset** -sivulla. Vaiheet ovat samanlaiset ostoasiakirjoissa ja projekteissa. Ostotilauksissa käytetään **Ostojen ja ostovelkojen asetukset** -sivua. Projekteissa käytetään **Projektiasetukset**-sivua.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntien ja myyntisaamisten asetukset** ja valitse sitten vastaava linkki.
2. Valitse **Arkistointi** -pikavälilehdessä, otetaanko automaattinen arkistointi käyttöön kaikille myyntiasiakirjatyypeille. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Seuraavassa taulukossa kuvataan **Arkistoi tarjoukset**-kentän vaihtoehdot.

|Asetus|Kuvaus|
|------|-----------|
|**Ei koskaan**| Älä arkistoi myyntitarjouksia, kun ne poistetaan.|
|**Kysymys**|Kysy käyttäjältä myyntitarjousten arkistoinnista tarjousten poistamisen yhteydessä.|
|**Aina**|Arkistoi myyntitarjoukset automaattisesti poistamisen yhteydessä.|

## Myyntitilauksen arkistointi manuaalisesti

Seuraavassa kuvataan, miten myyntitilaus arkistoidaan manuaalisesti. Vaiheet ovat samanlaiset kaikissa arkistoitavissa asiakirjoissa ja projekteissa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Avaa myyntitilaus, jonka haluat arkistoida.  
3. Valitse **Arkistoi asiakirja** -toiminto.

Myyntitilaus on arkistoitu. Voit tarkastella sitä **Arkistoidut myyntitilaukset** -sivulla.

## Kirjaamattomien myyntiasiakirjan tai projektin palauttaminen arkistosta

Seuraavaksi käsitellään menetelmä, jolla arkistoitu myyntitilaus palautetaan alkuperäiseen myyntitilaukseen. Asiakirjan palauttaminen on mahdollista vain, jos alkuperäistä asiakirjaa ei ole kirjattu. Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille sekä projekteille.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilausarkistot** ja valitse sitten vastaava linkki.
2. Valitse palautettava arkistoitu myyntitilaus tai sen versio ja valitse sitten **Palauta**-toiminto.  

Alkuperäisen myyntitilauksen tai projektin sisältö korvataan arkistoidulla versiolla.

## Arkistoitujen versioiden poistaminen

Säilytyskäytännön avulla voidaan tyhjentää arkistoidut versiot, joita ei enää tarvita. Säilytyskäytäntöjen avulla järjestelmänvalvojat voivat määrittää, kuinka kauan he haluavat säilyttää tietoja. He voivat esimerkiksi määrittää käytännön, joka poistaa tiedot vanhentumispäivämäärän jälkeen. Lisätietoja on kohdassa [Säilytyskäytäntöjen määrittäminen](admin-data-retention-policies.md).

Arkistoitujen asiakirjojen ja projektien säilytyskäytäntöjen luomista varten kannattaa ottaa huomioon seuraavat seikat:

* Jos alkuperäistä asiakirjaa ei ole poistettu, [!INCLUDE [prod_short](includes/prod_short.md)] ei poista arkistoituja versioita. Arkistoitu versio ei vanhene niin kauan kuin alkuperäinen on olemassa.
* Kun määrität säilytyskäytännön, voit määrittää käytännön poistamaan kaikki arkistoidut versiot uusinta lukuun ottamatta. Versioita voi olla esimerkiksi 10 ja haluat säilyttää viimeisimmän kopion. 
* [!INCLUDE [prod_short](includes/prod_short.md)] Central laskee asiakirjojen vanhentumispäivämäärän viimeisimmän arkistoidun version päivämäärän perusteella.

## Katso myös

[Asiakirjarivien seuraaminen](across-how-to-track-document-lines.md)  
[Myynti](sales-manage-sales.md)  
[Yrityksen yleiset toiminnot](ui-across-business-areas.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
