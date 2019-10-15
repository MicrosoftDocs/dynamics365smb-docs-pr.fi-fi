---
title: Liitteiden, linkkien ja muistioiden lisääminen tietueisiin| Microsoft Docs
description: Liitä hyperlinkki asiakirjaan tai sivusto tiettyyn tietueeseen, kuten asiakkaaseen tai asiakirjaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 84d58193fa7ee272b372403d63702348fbfb1f77
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315274"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Korttien ja asiakirjojen liitteiden, linkkien ja muistioiden hallinta

Voit liittää useimpien korttien ja asiakirjojen tietoruudussa tiedostoja, lisätä linkkejä ja kirjoittaa muistioita. Linkkejä ja muistioita voi kirjoittaa myös luettelosivulla sen jälkeen, kun olet valinnut liittyvän rivin.

Jos haluat tarkastella tai muuttaa näitä liitettyjä tietotyyppejä, sinun on avattava ensin tietoruudun **Liitteet**-välilehti. Välilehden otsikon takana oleva luku ilmaisee, kuinka monta liitettyä tiedostoa, linkkiä tai muistiinpanoa kortissa tai asiakirjassa on.

Liitteet, linkit ja muistiot pysyvät liitteinä, kun korttia tai asiakirjaa käsitellään muihin tiloihin, kuten siirtyminen jatkuvasta myyntitilauksesta kirjattuun myyntilaskuun. Huomaa kuitenkin, että järjestelmä ei käsittele mitään liitetyyppiä esimerkiksi tulostettaessa tai tallennettaessa tiedostoon.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Tiedoston liittäminen ostolaskuun
Korttiin tai asiakirjaan liitettävän tiedoston tyypillä ei ole merkitystä, ja se voi sisältää tekstiä, kuvan tai videon. Tämä on kätevää esimerkiksi silloin, kun haluat tallentaa toimittajan laskun PDF-tiedostona liittyvään [!INCLUDE[d365fin](includes/d365fin_md.md)]in ostolaskuun.

> [!NOTE]
> Saapuvat asiakirjat -ominaisuudella liitetyt tiedostot eivät sisälly **Liitteet**-välilehteen. Lisätietoja on kohdassa [Saapuvat asiakirjat](across-income-documents.md).

Seuraava toimenpide perustuu myyntitilaukseen. Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa ja korteissa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten liittyvä linkki.
2. Avaa myyntitilaus, johon haluat liittää tiedoston.
3. Avaa **Liitteet**-välilehti tietoruudussa.
4. Valitse **Asiakirjat**-kentässä arvo, kuten 0.
5. Valitse **Liitetyt asiakirjat** -sivun **Liite**-kentässä **Valitse tiedosto** -painike.
5. Valitse tiedosto haluamastasi sijainnista ja valitse sitten **Avaa**-painike.

Tiedosto on nyt liitetty ostolaskuun.

## <a name="to-add-a-link-from-an-item-card"></a>Linkin lisääminen nimikekortista
Voit lisätä kortista tai asiakirjasta linkin mihin tahansa URL-osoitteeseen tai polkuun. Tämä kätevää esimerkiksi silloin, kun haluat linkittää nimikekortin toimittajan nimikeluetteloon.

Seuraava toimenpide perustuu nimikekorttiin. Vaiheet ovat samanlaiset kaikissa tuetuissa korteissa ja asiakirjoissa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Valitse nimike, josta haluat lisätä linkin, ja valitse sitten tietoruudussa **Liitteet**-välilehti.
3. Valitse **Linkit**-kohdassa **+**-kuvake.
4. Anna linkki **Linkin osoite** -kentässä.

    - Jos haluat linkittää tietokoneessa tai verkossa olevan tiedoston, anna tiedostopolun ja tiedoston koko nimi, kuten **C:\Omat tiedostot\lasku1.doc**.
    - Luo linkki sivustoon antamalla verkko- eli URL-osoite, kuten **www.microsoft.com**.
    - Luo linkki ohjelmaan antamalla ohjelmaan avaava merkkijono. Jos haluat esimerkiksi että uusi tyhjä, tietylle sähköpostitunnukselle osoitettu Outlook-sähköpostiviesti avautuu, anna **mailto:testalias**.  

5. Kirjoita **Kuvaus**-kenttään linkkiä koskevia tietoja.  
6. Valitse **OK**-painike.

Linkki on nyt liitetty nimikekorttiin.  

## <a name="to-write-a-note-on-a-sales-order"></a>Muistion kirjoittaminen myyntitilaukseen
Voit kirjoittaa asiakirjaan tai korttiin muistion, jossa on esimerkiksi ohjeita muille asiakirjan tai kortin käyttäjille. Voit sisällyttää muistioihin tiedostolinkkejä ja URL-osoitteita.

> [!NOTE]
> **Liitteet**-välilehdessä olevat muistiot eivät liity sisäiseen muistiotoimintoon, jota käytetään lähinnä työnkulujen käyttäjien keskinäiseen viestintään. Lisätietoja on kohdassa [Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md).

Seuraava toimenpide perustuu myyntitilaukseen. Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa ja korteissa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Myyntitilaukset** ja valitse sitten liittyvä linkki.
2. Valitse myyntitilaus, johon haluat kirjoittaa muistion, ja valitse sitten tietoruudussa **Liitteet**-välilehti.
3. Valitse **Muistiot**-osassa **+**-kuvake.
4. Kirjoita **Huomautus**-kenttään tekstiä, kuten Tämä on kiireellinen tilaus.
5. Valitse **OK**-painike.

Huomautus on nyt liitetty myyntitilaukseen.

## <a name="see-also"></a>Katso myös  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)  
