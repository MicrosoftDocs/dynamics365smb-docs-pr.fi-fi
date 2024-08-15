---
title: Siirtoero tiliin -ominaisuuden käyttäminen maksujen täsmäytykseen
description: 'Tässä kuvataan, miten käsitellään maksuja, joita ei voi kohdistaa asiakirjaan, esimerkiksi silloin, kun vaihtokurssi aiheuttaa erilaisia summia.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 07/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Täsmäytä maksut, joita ei voi kohdistaa automaattisesti
Saatat joutua joskus käsittelemään pankkitilillesi maksuja, joita ei voi kohdistaa liittyvään avoimeen asiakas-, toimittaja- tai pankkitilitapahtumaan. Syynä voi olla se, että mitään asiakirjaa ei ole siinä [!INCLUDE[prod_short](includes/prod_short.md)] , johon maksu voidaan kohdistaa, tai että asiakirjan [!INCLUDE[prod_short](includes/prod_short.md)] summa poikkeaa transaktiosummasta esimerkiksi valuutan vaihdon vuoksi.  **Kaikki sellaisten maksujen kauppatapahtumat, joita ei ole vielä kohdistettu, näkyvät** Maksun täsmäytyspäiväkirja **-sivulla Ero-kentässä** . Summat mukaan lukien summat, joita ei voi kohdistaa edellä mainitun syyn vuoksi.

Näiden kohdistamattomien maksujen ratkaisutavat:
* Kohdista manuaalisesti
* Käytä tekstistä tiliin yhdistämistä
* Voit siirtää ylimääräisen summan päiväkirjan riville luodaksesi ja kirjataksesi vaaditun tapahtuman, kuten liikasuorituksen hyvityksen.

Maksut, joita ei voi kohdistaa, voivat näkyä maksun täsmäytyspäiväkirjan riveillä seuraavilla tavoilla:

* **Ero**-kentän arvo on sama kuin **Tapahtuman summa** -kentän arvo. Tämä tarkoittaa sitä, että mitään maksun osaa ei voi kohdistaa liittyvään avoimeen asiakas-, toimittaja- tai pankkitapahtumaan.
* **Ero**-kentän arvo on pienempi kuin **Tapahtuman summa** -kentän arvo. Tämä tarkoittaa sitä, että osa maksusta voidaan kohdistaa liittyvään avoimeen asiakas-, toimittaja- tai pankkitapahtumaan. Maksun jäljellä olevaa osaa ei voi kohdistaa, ja se täytyy täsmäyttää manuaalisesti tai kirjaamalla se suoraan tilille.

Voit täsmäyttää tällaiset maksut valitsemalla **Siirrä erotus tilille** -toiminnon ja määrittämällä, mille tilille **Ero**-kentän summa kirjataan, kun teet kirjauksen maksujen täsmäytyskirjauskansioon. Voit tehdä tämän joko **Maksujen täsmäytyskirjauskansio** -sivulta tai avaamaltasi **Maksun kohdistuksen tarkistus** -sivulta valitsemalla arvon **Vastaavuuden luotettavuus** -kentässä tai valitsemalla **Ero**-kentän.

> [!TIP]  
>   Vastaavan toiminnon avulla voit määrittää automaattisen täsmäytyksen toistuville maksuille, joita ei voi kohdistaa liittyviin avoimiin asiakas-, toimittaja- tai pankkitapahtumiin. Lisätietoja on kohdassa [Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

## Sellaisten maksujen täsmäyttäminen, joita ei voi kohdistaa automaattisesti
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksujen täsmäytyskirjauskansiot** ja valitse sitten liittyvä linkki.
2. Avaa maksun täsmäytyksen päiväkirja. Lisätietoja on kohdassa [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).
3. Valitse **Siirrä erotus tilille**. **Siirrä erotus tilille** -sivu avautuu.
4. Määritä **Tilityyppi**-kenttään sen tilin tyyppi, johon maksun summa kirjataan.
5. Määritä **Tilityyppi**-kenttään tili, johon maksun summa kirjataan.
6. Määritä **Kuvaus**-kenttään teksti, joka kuvaa tätä suoran maksun kirjausta. Oletusarvoisesti lisätään maksujen täsmäytyskirjauskansion rivin **Tapahtuman teksti** -kentän teksti.
7. Valitse **OK**-painike.

Jos **Ero**-kentän arvo on sama kuin **Tapahtuman summa** -kentän arvo, kun kirjaat maksujen täsmäytyskirjauskansion, koko päiväkirjan rivin maksu kirjataan suoraan määritetylle vastatilille.

Jos **Ero**-kentän arvo on pienempi kuin **Tapahtuman summa** -kentän arvon, samalla tekstillä ja päivämäärällä luodaan päiväkirjan lisärivi ja ero lisätään **Tapahtuman summa** -kenttään. Alkuperäisen päiväkirjan rivin ero vähennetään **Tapahtuman summa** -kentän arvosta ja maksun kohdistus siihen liittyvään asiakas-, toimittaja- tai pankkitilitapahtumaan säilyy. Kun kirjaat maksun täsmäytyskirjauskansion, yksi maksun osa kirjataan kohdistettuna maksuna. Maksun toinen osa kirjataan suoraan määritetylle tilille.

## Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]