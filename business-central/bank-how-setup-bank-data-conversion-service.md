---
title: "Pankkitietojen muunnon määrittäminen| Microsoft Docs"
description: "Voit määrittää pankkitilien tapahtumia seurattavaksi sekä tuoda tai viedä pankkisyötteitä, kuten Yodlee."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 10/02/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: f46d085eac89743c095b5fd7d73353a5ff248f65
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-the-bank-data-conversion-service"></a>Pankkitietojen muuntopalvelun määrittäminen
Yleiset palvelut on yhdistetty [!INCLUDE[d365fin](includes/d365fin_md.md)]iin ja valmis otettavaksi käyttöön. Sen avulla maksutiedot muunnetaan mihin tahansa pankkisi vaatimaan tietomuotoon. Tätä kutsutaan [!INCLUDE[d365fin](includes/d365fin_md.md)]issa pankkitietojen muuntopalveluksi.

Voit viedä maksurivit **Maksupäiväkirja**-sivulta tiedostoon tai tietovirtaan, joka ladataan pankkiin automaattista käsittelyä varten. Sähköisiä maksuja ei siis tarvitse tehdä yksitellen. Lisätietoja on kohdassa [Maksujen vieminen pankkitiedostoon](payables-how-export-payments-bank-file.md).

Voit tuoda tiliotetiedostot **Maksujen täsmäytyskirjauskansio** -sivulle muuntamalla pankin lähettämän tiedoston pankkitietojen muuntopalvelussa tietovirraksi, jonka [!INCLUDE[d365fin](includes/d365fin_md.md)] voi tuoda. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Tiliotteet voi tuoda pankkitietojen muuntopalvelun lisäksi myös Envestnet Yodlee -pankkisyötepalvelun avulla. Lisätietoja on kohdassa [Envestnet Yodlee -pankkisyötepalvelun määrittäminen](bank-how-setup-bank-statement-service.md).

Pankkitiedostojen tuontia ja vientiä varten on määritettävä oma pankkitili ja toimittajien pankkitilit. Lisätietoja on kohdassa [Pankkitilien määrittäminen](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> Pankkitietojen muuntopalvelu saattaa rajoittaa rivimäärää, joka voidaan viedä yhdessä tiedostossa. Näyttöön tulee virhesanoma, jos raja ylitetään. On suositeltavaa, että tiliotetiedostot sisältävät enintään 1 000 riviä, koska pankkitietojen muuntopalvelun käsittelyaika saattaa muuten kasvaa merkittävästi.

## <a name="to-sign-your-company-up-for-the-bank-data-conversion-service"></a>Yrityksen määrittäminen pankkitietojen muuntopalvelun käyttäjäksi
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitiet. muuntopalvelun asetukset** ja valitse sitten liittyvä linkki.  
2. **Pankkitiet. muuntopalvelun asetukset** -sivu avautuu ja siinä on kolme esitäytettyä kenttää sisältäen pankkitietojen muuntopalvelun tarjoajan asiaankuuluvat URL-osoitteet.

    > [!NOTE]  
    >   CRONUS Finland Oy -esittelytietokannassa Käyttäjänimi- ja Salasana-kenttä esitäytetään kirjautumisen esittelytiedoilla, jotka vaihdat yrityksen todellisiksi tiedoiksi, kun rekisteröidyt pankkitietojen muunnospalveluun.
3. Valitse **Rekisteröitymisen URL-osoite** -kentässä selaimen painike palveluntarjoajan rekisteröitymissivun avaamiseksi.  
4. Kirjoita pankkitietojen palvelujen tarjoajan rekisteröitymissivu, kirjoita yrityksesi rekisteröitymistä vastaava käyttäjänimi ja salasana ja suorita rekisteröitymisprosessi palveluntarjoajan ohjeiden mukaisesti.

    Yrityksesi on nyt rekisteröitynyt pankkitietojen muuntopalveluun. Jatka antamalla käyttäjänimi ja salasana, jotka olet määrittänyt palvelulle vastaavissa [!INCLUDE[d365fin](includes/d365fin_md.md)]in määrityskentissä.

5. Kirjoita **Pankkitiet. muuntopalvelun asetukset** -sivulla **Käyttäjänimi**-kenttään sama arvo, jonka kirjoitit kirjautumisnimeksi palveluntarjoajan sivulla vaiheessa 4.
6. Kirjoita **Salasana**-kenttään sama arvo, jonka kirjoitit **Salasana**-kenttään palveluntarjoajan sivulla vaiheessa 4.

> [!NOTE]  
> Sisäänkirjaustiedot salataan automaattisesti.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Tällä hetkellä tuettujen pankin tietomuotojen luettelon tarkastelu tai päivitys
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitiet. muuntopalvelun asetukset** ja valitse sitten liittyvä linkki.
2. Valitse **Pankkitiet. muuntopalvelun asetukset** -sivulla **Pankin nimi - tietojen muuntoluettelo** -toiminto, jolloin avautuu muuntopalvelun tukemien pankin tietomuotojen luettelo.
3. Valitse **Pankin nimi - tietojen muuntamisen luettelo** -sivulla **Päivitä pankkien nimien luettelo** -toiminto.

Pankkitietojen muuntopalvelun tukemien pankin tietomuotojen luettelo on nyt päivitetty. Tämä on luettelo pankin nimistä suodatettuna maan/alueen mukaan, jotka voit valita **Pankin nimi - tietojen muuntaminen** -kentän **Pankkitilin kortti** -sivulla.

> [!NOTE]  
>   Tuettujen pankin tietomuotojen päivitys tapahtuu myös silloin, kun valitset tai kirjoitat arvon **Pankin nimi - tietojen muuntaminen** -kenttään pankkitilillä.

Olet on nyt kirjautunut pankkitietojen muuntopalveluun. Jatka kirjautumistietojen käyttämistä jokaisella pankkitilillä, joka tulee käyttämään palvelua.

## <a name="see-also"></a>Katso myös
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Pankkitilien hallinta](bank-manage-bank-accounts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

