---
title: Liitteiden, linkkien ja muistioiden lisääminen tietueisiin| Microsoft Docs
description: Liitä hyperlinkki asiakirjaan tai sivusto tiettyyn tietueeseen, kuten asiakkaaseen tai asiakirjaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6aa7018a43db8c663c209894e118518c3de2f7cf
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393879"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Korttien ja asiakirjojen liitteiden, linkkien ja muistioiden hallinta

Voit liittää useimpien korttien ja asiakirjojen tietoruudussa tiedostoja, lisätä linkkejä ja kirjoittaa muistioita. Linkkejä ja muistioita voi kirjoittaa myös luettelosivulla sen jälkeen, kun olet valinnut liittyvän rivin.

Jos haluat tarkastella tai muuttaa näitä liitettyjä tietotyyppejä, sinun on avattava ensin tietoruudun **Liitteet**-välilehti. Välilehden otsikon takana oleva luku ilmaisee, kuinka monta liitettyä tiedostoa, linkkiä tai muistiinpanoa kortissa tai asiakirjassa on.

Liitteet, linkit ja muistiot pysyvät liitteinä, kun korttia tai asiakirjaa käsitellään muihin tiloihin, kuten siirtyminen jatkuvasta myyntitilauksesta kirjattuun myyntilaskuun. Järjestelmä ei kuitenkaan käsittele mitään liitetyyppiä esimerkiksi tulostettaessa tai tallennettaessa tiedostoon.

> [!NOTE]
> Kun toimitat ja laskutat myyntitilauksen tai ostotilauksen osittain, liite liitetään vain kyseisen tilauksen lopulliseen laskuun. Samoin kun laskutat käyttämällä lykkäysominaisuutta, liite liitetään vain asiakirjan pääkirjanpidontapahtumiin, mutta ei lykkäystapahtumiin.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Tiedoston liittäminen ostolaskuun
Korttiin tai asiakirjaan liitettävän tiedoston tyypillä ei ole merkitystä, ja se voi sisältää tekstiä, kuvan tai videon. Tämä on kätevää esimerkiksi silloin, kun haluat tallentaa toimittajan laskun PDF-tiedostona liittyvään [!INCLUDE[prod_short](includes/prod_short.md)]in ostolaskuun.

> [!NOTE]
> Saapuvat asiakirjat -ominaisuudella liitetyt tiedostot eivät sisälly **Liitteet**-välilehteen. Lisätietoja on kohdassa [Saapuvat asiakirjat](across-income-documents.md).

Seuraava toimenpide perustuu ostolaskuun. Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa ja korteissa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten liittyvä linkki.
2. Avaa myyntitilaus, johon haluat liittää tiedoston.
3. Avaa **Liitteet**-välilehti tietoruudussa.
4. Valitse **Asiakirjat**-kentässä arvo, kuten 0.
5. Valitse **Liitetyt asiakirjat** -sivun **Liite**-kentässä **Valitse tiedosto** -toiminto.
5. Valitse tiedosto haluamastasi sijainnista ja valitse sitten **Avaa**-painike.

Tiedosto on nyt liitetty ostolaskuun.

## <a name="to-view-an-attached-file"></a>Tarkastele liitettyä tiedostoa
1. Avaa **Liitteet**-välilehti tietoruudussa.
2. Valitse **Asiakirjat**-kentässä arvo, kuten 1.
3. Valitse **Liitetyt asiakirjat** -sivulla **Esikatselu**-toiminto.
4. Ladatun tiedoston avaaminen.

## <a name="to-save-a-document-as-a-pdf-attachment"></a>Asiakirjan tallentaminen PDF-liitteenä
Kun asiakirja on tallennettava tiedostoksi, voit käyttää **Liitä PDF-tiedostona** -toimintoa ja tallentaa nykyisen asiakirjan sisällön PDF-tiedostoksi, joka on liitetty asiakirjan tietoruutuun. Tämä on hyödyllistä esimerkiksi silloin, kun asiakirjat noudattavat useita vaiheita prosessissa, kuten esimerkiksi myyntiprosessissa ja hyväksynnän työnkulussa, ja haluat viitata edellisen vaiheen tulostukseen.

Seuraava toimenpide perustuu myyntitilaukseen. Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.
2. Valitse ensin myyntitilaus ja valitse sitten **Liitä PDF-tiedostona** -toiminto.

PDF-tiedosto ja sen sisältö myyntitilauksesta lisätään **Liitteet**-välilehteen tietoruudussa.

## <a name="to-add-a-link-from-an-item-card"></a>Linkin lisääminen nimikekortista
Voit lisätä kortista tai asiakirjasta linkin mihin tahansa URL-osoitteeseen tai polkuun. Tämä kätevää esimerkiksi silloin, kun haluat linkittää nimikekortin toimittajan nimikeluetteloon.

Seuraava toimenpide perustuu nimikekorttiin. Vaiheet ovat samanlaiset kaikissa tuetuissa korteissa ja asiakirjoissa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Valitse nimike, josta haluat lisätä linkin, ja valitse sitten tietoruudussa **Liitteet**-välilehti.
3. Valitse **Linkit**-kohdassa **+**-kuvake.
4. Anna linkki **Linkin osoite** -kentässä.

    Linkin on oltava kelvollinen Internet- tai intranet-osoite.

5. Kirjoita **Kuvaus**-kenttään linkkiä koskevia tietoja.  
6. Valitse **OK**-painike.

Linkki on nyt liitetty nimikekorttiin.  

## <a name="to-write-a-note-on-a-sales-order"></a>Muistion kirjoittaminen myyntitilaukseen
Voit kirjoittaa asiakirjaan tai korttiin muistion, jossa on esimerkiksi ohjeita muille asiakirjan tai kortin käyttäjille. Voit sisällyttää muistioihin tiedostolinkkejä ja URL-osoitteita.

> [!NOTE]
> **Liitteet**-välilehdessä olevat muistiot eivät liity sisäiseen muistiotoimintoon, jota käytetään lähinnä työnkulujen käyttäjien keskinäiseen viestintään. Lisätietoja on kohdassa [Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md).

Seuraava toimenpide perustuu myyntitilaukseen. Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa ja korteissa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.
2. Valitse myyntitilaus, johon haluat kirjoittaa muistion, ja valitse sitten tietoruudussa **Liitteet**-välilehti.
3. Valitse **Muistiot**-osassa **+**-kuvake.
4. Kirjoita **Huomautus**-kenttään tekstiä, kuten Tämä on kiireellinen tilaus.
5. Valitse **OK**-painike.

Huomautus on nyt liitetty myyntitilaukseen.

## <a name="see-also"></a>Katso myös  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]