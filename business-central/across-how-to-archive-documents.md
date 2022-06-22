---
title: Myyntien ja myyntiasiakirjojen arkistointi
description: Voit arkistoida myynti-ja ostotilauksia, tarjouksia, palautustilauksia ja puitetilauksia sekä palauttaa alkuperäiset tarvittaessa.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349
ms.date: 03/06/2022
ms.author: bholtorf
ms.openlocfilehash: c81248844f603f80304822c0ce089c666f9be9bc
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950327"
---
# <a name="archive-documents"></a>Asiakirjojen arkistointi
Voit arkistoida myynti-ja ostotilauksia, tarjouksia, palautustilauksia ja puitetilauksia. Asiakirjojen arkistointi mahdollistaa alkuperäisen palauttamisen tarvittaessa. Voit arkistoida myynti- tai ostoasiakirjan useita kertoja ja tallentaa kullakin kerralla erilaisen arkistoidun version.

Jos kyse on myyntiasiakirjoista, joiden alkuperäinen versio on vielä olemassa eikä sitä ole kirjattu, voit korvata nykyisen asiakirjan arkistoidulla versiolla **Palauta**-toiminnolla. 

Jos kyse on arkistoiduista asiakirjoista, joiden alkuperäinen versio on poistettu, voit käyttää sisällön uudelleen ainoastaan kopioimalla tiedot esimerkiksi käyttäen **Kopioi asiakirjasta** -toimintoa.  

## <a name="to-set-up-automatic-document-archiving"></a>Asiakirjojen automaattisen arkistoinnin määrittäminen

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

## <a name="to-archive-a-sales-order"></a>Myyntitilauksen arkistointi

Seuraavassa kuvataan, miten myyntitilaus arkistoidaan. Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Avaa myyntitilaus, jonka haluat arkistoida.  
3. Valitse **Arkistoi asiakirja** -toiminto.

Myyntitilaus on arkistoitu. Voit tarkastella sitä **Arkistoidut myyntitilaukset** -sivulla.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Kirjaamattomien myyntitilausten palauttaminen arkistosta

Seuraavaksi käsitellään menetelmä, jolla arkistoitu myyntitilaus palautetaan alkuperäiseen myyntitilaukseen. Asiakirjan palauttaminen on mahdollista vain, jos alkuperäistä tiedostoa ei ole kirjattu. Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilausarkistot** ja valitse sitten vastaava linkki.
2. Valitse palautettava arkistoitu myyntitilaus tai sen versio ja valitse sitten **Palauta**-toiminto.  

Alkuperäisen myyntitilauksen sisältö korvataan arkistoidulla versiolla.

## <a name="to-delete-archived-sales-orders"></a>Arkistoitujen myyntitilausten poistaminen

Seuraavassa kuvataan, miten arkistoidut myyntitilaukset poistetaan. Vaiheet ovat samanlaiset muille arkistoiduille myynti- ja ostoasiakirjoille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilausarkistot** ja valitse sitten vastaava linkki.  
2. Valitse **Poista vanhemmat versiot** -toiminto ja valitse sitten **Poista arkistoidut myyntitilausversiot** -sivulla asiaankuuluvat suodattimet.  
3. Valitse **OK**-painike.

## <a name="see-also"></a>Katso myös

[Asiakirjarivien seuranta](across-how-to-track-document-lines.md)  
[Myynti](sales-manage-sales.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
