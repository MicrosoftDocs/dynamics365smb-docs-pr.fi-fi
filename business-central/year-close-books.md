---
title: Kirjojen sulkeminen
description: 'Tutustu prosesseihin, jolla tilikauden tai -jakson kirjat suljetaan, ja mitä tapahtuu, kun kirjat suljetaan vuoden lopussa.'
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
m.search.form: 100
ms.date: 08/05/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="closing-the-books"></a>Kirjojen sulkeminen
Kun olet varmistanut, että kaikki tilit ovat ajan tasalla, ja kohdistanut kustannukset ja tulot, voit sulkea tilikauden tai kirjanpitojakson kirjat.

Sinun ei tarvitse sulkea vuotta, mutta se helpottaa järjestelmän käyttöä, koska voit hyödyntää käteviä suodatusvaihtoehtoja. Tapahtumatietojen menettämisestä ei myöskään tarvitse huolehtia, sillä suljetun tilikauden kaikki tiedot säilyvät myös sulkemisen jälkeen.

## <a name="closing-book-process"></a>Tilinpäätöskirjan käsittely
Kirjan sulkemisprosessi sisältää seuraavat päätehtävät:

1. Kirjanpitojakson sulkeminen.

    Tilikausi koostuu **Kirjanpitojaksot**-sivulla olevista avoimista kausista. Tyypillisesti tilikausi koostuu 12:sta kuukauden mittaisesta kaudesta, mutta tilikauden voi määrittää myös toisin.

    Lisätietoja on kohdassa [Kirjanpitojakson päättäminen](year-close-account-periods.md).
2. Edellisen vuoden tapahtumien rekisteröinti.

    Tilikautta suljettaessa on määritettävä erinäisiä hallinnallisia tapahtumia (kuten ennakkoon maksetut ja jaksotetut nimikkeet). Näitä tapahtumia kutsutaan oikaiseviksi tapahtumiksi. Näiden tapahtumien kirjaamista varten ei ole erityissääntöjä, ja niillä (kuten muillakin tapahtumilla) on rasti **Edellisen vuoden tapahtuma -** kentässä, jos ne kirjataan suljetun tilikauden päivämääränä. Vaikka tilikausi on suljettu, voit silti kirjata tilikaudelle KP-tapahtumia.
3. Saldojen siirtäminen tuloslaskelmatileiltä taseeseen.

    Kun tilikausi on suljettu ja kaikki edellisen vuoden tapahtumat on kirjattu, tuloslaskelmatilit on suljettava ja vuoden nettotuotto on siirrettävä taseeseen oman pääoman tilille. Käytä tätä tarkoitusta varten Sulje tuloslaskelma -eräajoa. Eräajo käsittelee kaikki Tuloslaskelma-tyyppiset kirjanpitotilit ja luo niiden saldojen vastatapahtumat. Nämä tapahtumat sijoitetaan päiväkirjaan, josta ne voi kirjata. Eräajo kirjaa ne automaattisesti vain silloin, kun käytetään lisäraportointivaluuttaa. Käytettäessä lisäraportointivaluuttaa eräajo tekee kirjaukset suoraan pääkirjanpitoon.

    Lisätietoja on kohdassa [Tuloslaskelman sulkeminen](year-close-income-statement.md).
4. vuositilinpäätöstapahtuman kirjaaminen yhdessä kompensoivien pääomatilin tapahtumien kanssa.

    Kun Sulje tuloslaskelma -eräajo on valmis, voit kirjata ajon luomat tapahtumat. Jos et määrittänyt eräajoon jakamattoman voiton tiliä, syötä rivi, jolla on vastakirjaus, joka kirjaa nettotulon oikeaan yleiseen kirjanpitotili taseeseen oman pääoman alla. Kirjaa lopulta päiväkirja.

    Lisätietoja on kohdassa [Vuoden lopun tilinpäätöstapahtuman kirjaaminen](year-how-post-year-end-close-entry.md).

## <a name="what-happens-when-you-close"></a>Sulkemisen yhteydessä tapahtuvat asiat

Kun suljet tilikauden vuoden lopussa, järjestelmä siirtää voiton laskennallisesta voitosta jakamattoman voiton tilille. Järjestelmä myös merkitsee tilikauden suljetuksi ja kaikki myöhemmät suljetun vuoden tapahtumat edellisen vuoden tapahtumiksi.

Järjestelmä luo sitten tilinpäätöstapahtuman, mutta tapahtumaa ei kirjata automaattisesti. Saat mahdollisuuden tehdä kompensoivat pääomatilitapahtumat tai -tapahtumat, joiden avulla voit päättää, miten tilinpäätöstapahtuma kohdistetaan. Esimerkiksi jos yrityksessä on useita osastoja, voit antaa järjestelmän luoda yksittäisen tilinpäätöstapahtuman kaikille osastoille ja tehdä sitten kompensoivan tapahtuman kunkin osaston pääomatilille.

Voit tehdä kirjauksia edelliselle tilikaudelle myös tuloslaskelmatilien sulkemisen jälkeen suorittamalla Sulje tuloslaskelma -eräajon myöhemmin uudelleen.

## <a name="see-also"></a>Katso myös

[Kirjanpitojaksojen ja tilikausien käsitteleminen](finance-accounting-periods-and-fiscal-years.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
