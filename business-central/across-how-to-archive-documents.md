---
title: Myynti- ja ostoasiakirjojen arkistointi | Microsoft Docs
description: Voit arkistoida myynti- ja ostotilauksia, tarjouksia, palautustilauksia ja puitetilauksia. Voit myös käyttää arkistoitua asiakirjaa ja luoda uudelleen asiakirjan, josta ne arkistoitiin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 0f2b5a2ce4fd53d9d487d20f7139d7b36c5387b5
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780483"
---
# <a name="archive-documents"></a>Asiakirjojen arkistointi
Voit arkistoida osto- ja myyntitilauksia, tarjouksia, palautustilauksia ja puitetilauksia esimerkiksi siksi, että haluat tallentaa asiakirjan kopion käytettäväksi myöhemmin uudelleen. Voit arkistoida myynti- tai ostoasiakirjan useita kertoja ja tallentaa kullakin kerralla erilaisen arkistoidun version.

Jos kyse on asiakirjoista, joiden alkuperäinen versio on vielä olemassa eikä sitä ole kirjattu, voit korvata alkuperäisen asiakirjan arkistoidulla versiolla **Palauta**-toiminnolla. Tämä on kätevää, jos asiakirjaan halutaan palauttaa aiempi sisältö.

Jos kyse on arkistoiduista asiakirjoista, joiden alkuperäinen versio on poistettu, voit käyttää sisällön uudelleen ainoastaan kopioimalla tiedot esimerkiksi **Kopioi asiakirjasta** -toiminnolla.   

## <a name="to-set-up-automatic-document-archiving"></a>Asiakirjojen automaattisen arkistoinnin määrittäminen  
Voit määrittää myynti- ja ostotilausten, tarjousten, puitetilausten ja palautustilausten automaattisen arkistoinnin ennen asiakirjojen poistamista.

Seuraavassa kuvataan, miten myyntiasiakirjojen automaattinen arkistointi määritetään. Vaiheet ovat samankaltaiset ostoasiakirjoille.
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntien ja myyntisaamisten asetukset** ja valitse sitten liittyvä linkki.
2. Täytä kentät **Myyntien ja myyntisaamisten asetukset** -sivulla seuraavasti.

|Kenttä|Description|
|-----|-----------|
|**Myyntitarjousten arkistointi**|**Ei koskaan**, jos myyntitarjouksia ei arkistoida koskaan poistamisen yhteydessä. **Kysymys**, kun käyttäjältä kysytään myyntitarjousten arkistoinnista tarjousten poistamisen yhteydessä. **Aina**, kun myyntitarjoukset arkistoidaan automaattisesti poistamisen yhteydessä.|
|**Puitemyyntitilausten arkistointi**|Puitemyyntitilaukset arkistoidaan automaattisesti aina poistamisen yhteydessä.|
|**Arkist. tilaukset ja pal.tilaukset**|Myyntitilaukset arkistoidaan automaattisesti aina poistamisen yhteydessä.|

## <a name="to-archive-a-sales-order"></a>Myyntitilauksen arkistointi
Seuraavassa kuvataan, miten myyntitilaus arkistoidaan. Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille.

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.  
2.  Avaa myyntitilaus, jonka haluat arkistoida.  
3.  Valitse **Arkistoi asiakirja** -toiminto.

Myyntitilaus on arkistoitu. Voit tarkastella sitä **Arkistoidut myyntitilaukset** -sivulla.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Kirjaamattomien myyntitilausten palauttaminen arkistosta
Seuraavaksi käsitellään menetelmä, jolla arkistoidun myyntitilauksen sisältö tuodaan takaisin alkuperäiseen myyntitilaukseen. Tämä on mahdollista vain, jos alkuperäistä tiedostoa ei ole kirjattu. Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Arkistoidut myyntitilaukset** ja valitse sitten liittyvä linkki.
2. Valitse palautettava arkistoitu myyntitilaus tai sen versio ja valitse sitten **Palauta**-toiminto.  

Alkuperäisen myyntitilauksen sisältö korvataan valitun arkistoidun version sisällöllä.

## <a name="to-delete-archived-sales-orders"></a>Arkistoitujen myyntitilausten poistaminen
Seuraavassa kuvataan, miten arkistoidut myyntitilaukset poistetaan. Vaiheet ovat samanlaiset muille arkistoiduille myynti- ja ostoasiakirjoille.

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poista arkistoidut myyntitilausversiot** ja valitse sitten liittyvä linkki.  
2.  Valitse **Poista arkistoidut myyntitilausversiot** -sivulla sopivat suodattimet.  
3.  Valitse **OK**-painike.

## <a name="see-also"></a>Katso myös
[Asiakirjarivien seuranta](across-how-to-track-document-lines.md)  
[Myynti](sales-manage-sales.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
