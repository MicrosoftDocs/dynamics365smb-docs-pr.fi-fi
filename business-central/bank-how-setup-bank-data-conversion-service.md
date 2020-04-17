---
title: Pankkitietojen muunnon määrittäminen| Microsoft Docs
description: Voit määrittää pankkitilien tapahtumia seurattavaksi sekä tuoda tai viedä pankkisyötteitä, kuten Yodlee.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, AMC Banking 365 Fundamentals extension, funds transfer
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: e222e133313147cecd94c8cb7f2644776ee1034a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186258"
---
# <a name="set-up-the-amc-banking-365-fundamentals-extension"></a>Asenna AMC Banking 365 -perusteiden laajennus
Yleiset palvelut on yhdistetty [!INCLUDE[d365fin](includes/d365fin_md.md)]iin ja valmis otettavaksi käyttöön. Sen avulla maksutiedot muunnetaan mihin tahansa pankkisi vaatimaan tietomuotoon. Tähän viitataan kohdassa [!INCLUDE[d365fin](includes/d365fin_md.md)] AMC Banking 365 -perusteiden laajennus.

Voit viedä maksurivit **Maksupäiväkirja**-sivulta tiedostoon tai tietovirtaan, joka ladataan pankkiin automaattista käsittelyä varten. Sähköisiä maksuja ei siis tarvitse tehdä yksitellen. Lisätietoja on kohdassa [Maksujen vieminen pankkitiedostoon](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Voit tuoda tiliotetiedostot **Maksujen täsmäytyskirjauskansio** -sivulle muuntamalla pankin lähettämän tiedoston AMC Banking 365 -perusteiden laajennuksen avulla tietovirraksi, jonka [!INCLUDE[d365fin](includes/d365fin_md.md)] voi tuoda. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Tiliotteet voi tuoda AMC Banking 365 -perusteiden laajennuksen lisäksi myös Envestnet Yodlee Bank Feeds -palvelun avulla. Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).

Pankkitiedostojen tuontia ja vientiä varten on määritettävä oma pankkitili ja toimittajien pankkitilit. Lisätietoja on kohdassa [Pankkitilien määrittäminen](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> AMC Banking 365 -perusteiden laajennus saattaa rajoittaa rivimäärää, joka voidaan viedä yhdessä tiedostossa. Näyttöön tulee virhesanoma, jos raja ylitetään. On suositeltavaa, että tiliotetiedostot sisältävät enintään 1 000 riviä, koska AMC Banking 365 -perusteiden laajennuksen käsittelyaika saattaa muuten kasvaa merkittävästi.

## <a name="to-sign-your-company-up-for-the-amc-banking-365-fundamentals-extension"></a>Yrityksen allekirjoittaminen AMC Banking 365 -perusteiden laajennusta varten
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitiet. muuntopalvelun asetukset** ja valitse sitten liittyvä linkki.  
2. **Pankkitiet. muuntopalvelun asetukset** -sivu avautuu ja siinä on kolme esitäytettyä kenttää sisältäen AMC Banking 365 -perusteiden laajennuksen tarjoajan asiaankuuluvat URL-osoitteet.

    > [!NOTE]  
    >   CRONUS International Ltd. -esittelytietokannassa Käyttäjänimi- ja Salasana-kenttä esitäytetään kirjautumisen esittelytiedoilla, jotka vaihdat yrityksen todellisiksi tiedoiksi, kun rekisteröidyt AMC Banking 365 -perusteiden laajennukseen.
3. Valitse **Rekisteröitymisen URL-osoite** -kentässä selaimen painike palveluntarjoajan rekisteröitymissivun avaamiseksi.  
4. Kirjoita pankkitietojen palvelujen tarjoajan rekisteröitymissivu, kirjoita yrityksesi rekisteröitymistä vastaava käyttäjänimi ja salasana ja suorita rekisteröitymisprosessi palveluntarjoajan ohjeiden mukaisesti.

    Yrityksesi on nyt rekisteröitynyt AMC Banking 365 -perusteiden laajennusta varten. Jatka antamalla käyttäjänimi ja salasana, jotka olet määrittänyt palvelulle vastaavissa [!INCLUDE[d365fin](includes/d365fin_md.md)]in määrityskentissä.

5. Kirjoita **Pankkitiet. muuntopalvelun asetukset** -sivulla **Käyttäjänimi**-kenttään sama arvo, jonka kirjoitit kirjautumisnimeksi palveluntarjoajan sivulla vaiheessa 4.
6. Kirjoita **Salasana**-kenttään sama arvo, jonka kirjoitit **Salasana**-kenttään palveluntarjoajan sivulla vaiheessa 4.

> [!NOTE]  
> Sisäänkirjaustiedot salataan automaattisesti.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Tällä hetkellä tuettujen pankin tietomuotojen luettelon tarkastelu tai päivitys
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitiet. muuntopalvelun asetukset** ja valitse sitten liittyvä linkki.
2. Valitse **Pankkitiet. muuntopalvelun asetukset** -sivulla **Pankin nimi - tietojen muuntoluettelo** -toiminto, jolloin avautuu muuntopalvelun tukemien pankin tietomuotojen luettelo.
3. Valitse **Pankin nimi - tietojen muuntamisen luettelo** -sivulla **Päivitä pankkien nimien luettelo** -toiminto.

AMC Banking 365 -perusteiden laajennuksen tukemien pankin tietomuotojen luettelo on nyt päivitetty. Tämä on luettelo pankin nimistä suodatettuna maan/alueen mukaan, jotka voit valita **Pankin nimi - tietojen muuntaminen** -kentän **Pankkitilin kortti** -sivulla.

> [!NOTE]  
>   Tuettujen pankin tietomuotojen päivitys tapahtuu myös silloin, kun valitset tai kirjoitat arvon **Pankin nimi - tietojen muuntaminen** -kenttään pankkitilillä.

Olet nyt rekisteröitynyt AMC Banking 365 -perusteiden laajennusta varten. Jatka kirjautumistietojen käyttämistä jokaisella pankkitilillä, joka tulee käyttämään palvelua.

## <a name="see-also"></a>Katso myös
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
