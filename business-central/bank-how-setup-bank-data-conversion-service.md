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
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 98d7215b4d8ae476fbc550ea0057e6f71a00a5fd
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-the-bank-data-conversion-service"></a>Pankkitietojen muuntopalvelun määrittäminen
Yleiset palvelut on yhdistetty [!INCLUDE[d365fin](includes/d365fin_md.md)]iin ja valmis otettavaksi käyttöön. Sen avulla maksutiedot muunnetaan mihin tahansa pankkisi vaatimaan tietomuotoon. Tätä kutsutaan [!INCLUDE[d365fin](includes/d365fin_md.md)]issa pankkitietojen muuntopalveluksi.

Voit viedä maksurivit **Maksupäiväkirja**-ikkunasta tiedostoon tai tietovirtaan, joka ladataan pankkiin automaattista käsittelyä varten. Sähköisiä maksuja ei siis tarvitse tehdä yksitellen. Lisätietoja on kohdassa [Maksujen vieminen pankkitiedostoon](payables-how-export-payments-bank-file.md).

Voit tuoda tiliotetiedostot **Maksujen täsmäytyskirjauskansio** -ikkunaan muuntamalla pankin lähettämän tiedoston pankkitietojen muuntopalvelussa tietovirraksi, jonka [!INCLUDE[d365fin](includes/d365fin_md.md)] voi tuoda. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Tiliotteet voi tuoda pankkitietojen muuntopalvelun lisäksi myös Envestnet Yodlee -pankkisyötepalvelun avulla. Lisätietoja on kohdassa [Envestnet Yodlee -pankkisyötepalvelun määrittäminen](bank-how-setup-bank-statement-service.md).

Pankkitiedostojen tuontia ja vientiä varten on määritettävä oma pankkitili ja toimittajien pankkitilit. Lisätietoja on kohdassa [Pankkitilien määrittäminen](bank-how-setup-bank-accounts.md).

> [!NOTE]  
>   Pankkitietojen muuntopalvelu saattaa rajoittaa rivimäärää, joka voidaan viedä yhdessä tiedostossa. Näyttöön tulee virhesanoma, jos raja ylitetään. On suositeltavaa, että tiliotetiedostot sisältävät enintään 1 000 riviä, koska pankkitietojen muuntopalvelun käsittelyaika saattaa muuten kasvaa merkittävästi.

## <a name="to-sign-your-company-up-for-the-bank-data-conversion-service"></a>Yrityksen määrittäminen pankkitietojen muuntopalvelun käyttäjäksi
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Pankkitiet. muuntopalvelun asetukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. **Pankkitiet. muuntopalvelun asetukset** -ikkuna avautuu ja siinä on kolme esitäytettyä kenttää sisältäen pankkitietojen muuntopalvelun tarjoajan asiaankuuluvat URL-osoitteet.

    > [!NOTE]  
    >   CRONUS Finland Oy -esittelytietokannassa Käyttäjänimi- ja Salasana-kenttä esitäytetään kirjautumisen esittelytiedoilla, jotka vaihdat yrityksen todellisiksi tiedoiksi, kun rekisteröidyt pankkitietojen muunnospalveluun.
3. Valitse **Rekisteröitymisen URL-osoite** -kentässä selaimen painike palveluntarjoajan rekisteröitymissivun avaamiseksi.  
4. Kirjoita pankkitietojen palvelujen tarjoajan rekisteröitymissivu, kirjoita yrityksesi rekisteröitymistä vastaava käyttäjänimi ja salasana ja suorita rekisteröitymisprosessi palveluntarjoajan ohjeiden mukaisesti.

  Yrityksesi on nyt rekisteröitynyt pankkitietojen muuntopalveluun. Jatka antamalla käyttäjänimi ja salasana, jotka olet määrittänyt palvelulle vastaavissa [!INCLUDE[d365fin](includes/d365fin_md.md)]in määrityskentissä.
5. Kirjoita **Pankkitiet. muuntopalvelun asetukset** -ikkunassa **Käyttäjänimi**-kenttään sama arvo, jonka kirjoitit kirjautumisnimeksi palveluntarjoajan sivulla vaiheessa 4.
6. Kirjoita **Salasana**-kenttään sama arvo, jonka kirjoitit **Salasana**-kenttään palveluntarjoajan sivulla vaiheessa 4.

## <a name="to-encrypt-your-login-information"></a>Kirjautumistietojen salaaminen
Suosittelemme, että suojaat **Pankkitiet. muuntopalvelun asetukset** -ikkunaan kirjoittamasi kirjautumistiedot. [!INCLUDE[d365fin](includes/d365fin_md.md)] -palvelimen tiedot voi salata luomalla uusia salausavaimia tai tuomalla aiemmin luotuja salausavaimia, jotka otetaan käyttöön tietokantayhteyden muodostavassa [!INCLUDE[d365fin](includes/d365fin_md.md)] -palvelininstanssissa.

1. Valitse **Pankkitiet. muuntopalvelun asetukset** -ikkunassa **Salauksen hallinta** -toiminto.
2. Ota tietojen salaus käyttöön **Tietojen salauksen hallinta** -ikkunassa.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Tällä hetkellä tuettujen pankin tietomuotojen luettelon tarkastelu tai päivitys
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Pankkitiet. muuntopalvelun asetukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Pankkitiet. muuntopalvelun asetukset** -ikkunassa **Pankin nimi - tietojen muuntoluettelo** -toiminto, jolloin avautuu muuntopalvelun tukemien pankin tietomuotojen luettelo.
3. Valitse **Pankin nimi - tietojen muuntamisen luettelo** -sivulla **Päivitä pankkien nimien luettelo** -toiminto.

Pankkitietojen muuntopalvelun tukemien pankin tietomuotojen luettelo on nyt päivitetty. Tämä on luettelo pankin nimistä suodatettuna maan/alueen mukaan, jotka voit valita **Pankin nimi - tietojen muuntaminen** -kentän **Pankkitilin kortti** -ikkunassa.

> [!NOTE]  
>   Tuettujen pankin tietomuotojen päivitys tapahtuu myös silloin, kun valitset tai kirjoitat arvon **Pankin nimi - tietojen muuntaminen** -kenttään pankkitilillä.

Olet on nyt kirjautunut pankkitietojen muuntopalveluun. Jatka kirjautumistietojen käyttämistä jokaisella pankkitilillä, joka tulee käyttämään palvelua.

## <a name="see-also"></a>Katso myös
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Pankkitilien hallinta](bank-manage-bank-accounts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

