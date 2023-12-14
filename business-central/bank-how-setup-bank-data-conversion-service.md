---
title: Pankkitietojen muuntopalvelun määrittäminen
description: 'Voit määrittää pankkitilien tapahtumia seurattavaksi sekä tuoda tai viedä pankkisyötteitä, kuten Yodlee.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, AMC Banking 365 Fundamentals extension, funds transfer'
ms.search.form: '304, 20106, 20105, 20100, 20101, 20107, 20109'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="set-up-the-amc-banking-365-fundamentals-extension"></a>AMC Banking 365 Fundamentals -laajennuksen määrittäminen
Yleiset palvelut on yhdistetty [!INCLUDE[prod_short](includes/prod_short.md)]iin ja valmis otettavaksi käyttöön. Sen avulla maksutiedot muunnetaan mihin tahansa pankkisi vaatimaan tietomuotoon. Tähän viitataan [!INCLUDE[prod_short](includes/prod_short.md)]issa AMC Banking 365 Fundamentals -laajennuksena.

Voit viedä maksurivit **Maksupäiväkirja**-sivulta tiedostoon tai tietovirtaan, joka ladataan pankkiin automaattista käsittelyä varten. Sähköisiä maksuja ei siis tarvitse tehdä yksitellen. Lisätietoja on kohdassa [Maksujen vieminen pankkitiedostoon](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Voit tuoda tiliotetiedostot **Maksujen täsmäytyskirjauskansio** -sivulle muuntamalla pankin lähettämän tiedoston AMC Banking 365 Fundamentals -laajennuksen avulla tietovirraksi, jonka [!INCLUDE[prod_short](includes/prod_short.md)] voi tuoda. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Tiliotteet voi tuoda AMC Banking 365 Fundamentals -laajennuksen lisäksi myös Envestnet Yodlee Bank Feeds -palvelun avulla. Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).

Pankkitiedostojen tuontia ja vientiä varten on määritettävä oma pankkitili ja toimittajien pankkitilit. Lisätietoja on kohdassa [Pankkitilien määrittäminen](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> AMC Banking 365 Fundamentals -laajennus saattaa rajoittaa rivimäärää, joka voidaan viedä yhdessä tiedostossa. Näyttöön tulee virhesanoma, jos raja ylitetään. On suositeltavaa, että tiliotetiedostot sisältävät enintään 1 000 riviä, koska AMC Banking 365 Fundamentals -laajennuksen käsittelyaika saattaa muuten pidentyä merkittävästi.

## <a name="to-sign-your-company-up-for-the-amc-banking-365-fundamentals-extension"></a>Yrityksen rekisteröiminen AMC Banking 365 Fundamentals -laajennukseen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitiet. muuntopalvelun asetukset** ja valitse sitten vastaava linkki.  
2. **Pankkitiet. muuntopalvelun asetukset** -sivu avautuu ja siinä on kolme esitäytettyä kenttää, jotka sisältävät AMC Banking 365 Fundamentals -laajennuksen tarjoajan tarvittavat URL-osoitteet.

    > [!NOTE]  
    >   CRONUS International Ltd. -esittelytietokannassa Käyttäjänimi- ja Salasana-kenttä esitäytetään kirjautumisen esittelytiedoilla, jotka vaihdetaan yrityksen todellisiksi tiedoiksi, kun rekisteröidyt AMC Banking 365 Fundamentals -laajennukseen.
3. Valitse **Rekisteröitymisen URL-osoite** -kentässä selaimen painike palveluntarjoajan rekisteröitymissivun avaamiseksi.  
4. Kirjoita pankkitietojen palvelujen tarjoajan rekisteröitymissivu, kirjoita yrityksesi rekisteröitymistä vastaava käyttäjänimi ja salasana ja suorita rekisteröitymisprosessi palveluntarjoajan ohjeiden mukaisesti.

    Yrityksesi on nyt rekisteröitynyt AMC Banking 365 Fundamentals -laajennukseen. Jatka antamalla käyttäjänimi ja salasana, jotka olet määrittänyt palvelulle vastaavissa [!INCLUDE[prod_short](includes/prod_short.md)]in määrityskentissä.

5. Kirjoita **Pankkitiet. muuntopalvelun asetukset** -sivulla **Käyttäjänimi**-kenttään sama arvo, jonka kirjoitit kirjautumisnimeksi palveluntarjoajan sivulla vaiheessa 4.
6. Kirjoita **Salasana**-kenttään sama arvo, jonka kirjoitit **Salasana**-kenttään palveluntarjoajan sivulla vaiheessa 4.

> [!NOTE]  
> Sisäänkirjaustiedot salataan automaattisesti.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Tällä hetkellä tuettujen pankin tietomuotojen luettelon tarkastelu tai päivitys
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitiet. muuntopalvelun asetukset** ja valitse sitten vastaava linkki.
2. Valitse **Pankkitiet. muuntopalvelun asetukset** -sivulla **Pankin nimi - tietojen muuntoluettelo** -toiminto, jolloin avautuu muuntopalvelun tukemien pankin tietomuotojen luettelo.
3. Valitse **Pankin nimi - tietojen muuntamisen luettelo** -sivulla **Päivitä pankkien nimien luettelo** -toiminto.

AMC Banking 365 Fundamentals -laajennuksen tukema pankkitietomuotojen luettelo on nyt päivitetty. Tämä on luettelo pankin nimistä suodatettuna maan/alueen mukaan, jotka voit valita **Pankin nimi - tietojen muuntaminen** -kentän **Pankkitilin kortti** -sivulla.

> [!NOTE]  
>   Tuettujen pankin tietomuotojen päivitys tapahtuu myös silloin, kun valitset tai kirjoitat arvon **Pankin nimi - tietojen muuntaminen** -kenttään pankkitilillä.

Olet nyt rekisteröitynyt AMC Banking 365 Fundamentals -laajennukseen. Jatka kirjautumistietojen käyttämistä jokaisella pankkitilillä, joka tulee käyttämään palvelua.

## <a name="see-also"></a>Katso myös
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
