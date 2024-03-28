---
title: Myyntien ja myyntiasiakirjojen arkistointi
description: 'Voit arkistoida myynti-ja ostotilauksia, tarjouksia, palautustilauksia ja puitetilauksia.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/18/2023
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
ms.service: dynamics-365-business-central
---
# Asiakirjojen arkistoiminen

Voit arkistoida myynti-ja ostotilauksia, tarjouksia, palautustilauksia ja puitetilauksia. Voit arkistoida myynti- tai ostoasiakirjan useita kertoja ja tallentaa kullakin kerralla erilaisen arkistoidun version.

Jos kyse on myyntiasiakirjoista, joiden alkuperäinen versio on vielä olemassa eikä sitä ole kirjattu, voit korvata nykyisen asiakirjan arkistoidulla versiolla **Palauta**-toiminnolla. Toiminto toimii vain myyntiasiakirjoissa.

Jos kyse on arkistoiduista asiakirjoista, joiden alkuperäinen versio on poistettu, voit käyttää sisällön uudelleen ainoastaan kopioimalla tiedot esimerkiksi käyttäen **Kopioi asiakirjasta** -toimintoa.  

## Asiakirjojen automaattisen arkistoinnin määrittäminen

Voit määrittää myynti- ja ostotilausten, tarjousten, puitetilausten ja palautustilausten automaattisen arkistoinnin. Kun automaattinen arkistointi on käytössä, arkistoidusta asiakirjasta luodaan uusi versio, kun joku tekee seuraavat asiat:

* Asiakirjan muuttaminen tai poistaminen.
* Asiakirjan tulostaminen, lataaminen tai sähköpostitse lähettäminen.
* Tarjouksen muuntaminen tilaukseksi tai laskuksi.
* Kirjaa tilauksen.

Seuraavassa kuvataan, miten myyntiasiakirjojen automaattinen arkistointi määritetään. Vaiheet ovat samankaltaiset ostoasiakirjoille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntien ja myyntisaamisten asetukset** ja valitse sitten vastaava linkki.
2. Valitse **Arkistointi** -pikavälilehdessä, otetaanko automaattinen arkistointi käyttöön kaikille myyntiasiakirjatyypeille. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Seuraavassa taulukossa kuvataan **Arkistoi tarjoukset**-kentän vaihtoehdot.

|Asetus|Kuvaus|
|------|-----------|
|**Ei koskaan**| Älä arkistoi myyntitarjouksia, kun ne poistetaan.|
|**Kysymys**|Kysy käyttäjältä myyntitarjousten arkistoinnista tarjousten poistamisen yhteydessä.|
|**Aina**|Arkistoi myyntitarjoukset automaattisesti poistamisen yhteydessä.|

## Myyntitilauksen arkistointi manuaalisesti

Seuraavassa kuvataan, miten myyntitilaus arkistoidaan manuaalisesti. Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Avaa myyntitilaus, jonka haluat arkistoida.  
3. Valitse **Arkistoi asiakirja** -toiminto.

Myyntitilaus on arkistoitu. Voit tarkastella sitä **Arkistoidut myyntitilaukset** -sivulla.

## Kirjaamattomien myyntitilausten palauttaminen arkistosta

Seuraavaksi käsitellään menetelmä, jolla arkistoitu myyntitilaus palautetaan alkuperäiseen myyntitilaukseen. Asiakirjan palauttaminen on mahdollista vain, jos alkuperäistä tiedostoa ei ole kirjattu. Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilausarkistot** ja valitse sitten vastaava linkki.
2. Valitse palautettava arkistoitu myyntitilaus tai sen versio ja valitse sitten **Palauta**-toiminto.  

Alkuperäisen myyntitilauksen sisältö korvataan arkistoidulla versiolla.

## Arkistoitujen myyntitilausten poistaminen

Säilytyskäytännön avulla voit tyhjentää arkistoidut asiakirjat, joita et enää tarvitse. Säilytyskäytäntöjen avulla järjestelmänvalvojat voivat määrittää, kuinka kauan he haluavat säilyttää tietoja. He voivat esimerkiksi määrittää käytännön, joka poistaa tiedot vanhentumispäivämäärän jälkeen. Lisätietoja on kohdassa [Säilytyskäytäntöjen määrittäminen](admin-data-retention-policies.md).

Arkistoitujen asiakirjojen säilytyskäytäntöjen luomista varten on syytä ottaa huomioon seuraavat seikat:

* *Jos alkuperäistä asiakirjaa ei ole poistettu, Business Central ei poista arkistoituja versioita. Arkistoitu versio ei vanhene niin kauan kuin alkuperäinen on olemassa.
* Kun määrität säilytyskäytännön, voit määrittää, että käytäntö poistaa kaikki asiakirjan arkistoidut versiot uusinta lukuun ottamatta. Sinulla voi olla esimerkiksi 10 versiota asiakirjasta ja haluat säilyttää viimeisimmän kopion. 
* Business Central laskee asiakirjojen vanhentumispäivämäärän viimeisimmän arkistoidun version päivämäärän perusteella.

## Katso myös

[Asiakirjarivien seuraaminen](across-how-to-track-document-lines.md)  
[Myynti](sales-manage-sales.md)  
[Yrityksen yleiset toiminnot](ui-across-business-areas.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
