---
title: Asiakirjojen ja sähköpostien lähettäminen
description: 'Voit määrittää sähköpostiviestin perustekstiin lisättävän sisällön, kuten PayPal-linkin. Voit myös liittää asiakirjoja sähköpostiviesteihin.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'SMTP, mail, Microsoft 365, cover, body, PayPal, layout'
ms.search.form: '41,'
ms.date: 05/01/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Asiakirjojen ja sähköpostien lähettäminen

Voit helposti jakaa tietoja ja asiakirjoja, kuten myynti- ja ostotilauksia ja laskuja, sähköpostitse suoraan [!INCLUDE[prod_short](includes/prod_short.md)]ista ilman sähköpostisovelluksen avaamista.  

Voit lähettää lähes kaikentyyppisiä asiakirjoja PDF-liitteinä. Vaihtoehtoisesti voit määrittää raportin asettelun, joka sisältää asiakirjan tiedot sähköpostin tekstissä sekä tekstin, joka tekee sähköposteista entistä ystävällisempiä, esimerkiksi vakiotervehdyksen. Lisätietoja on kohdassa [Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md).

Laskujen lähettämisen yhteydessä asiakkaiden on helpompi suorittaa maksuja maksupalvelun (esimerkiksi PayPalin) kautta lisäämällä automaattisesti sähköpostissa tietoja ja linkin palveluun. Lisätietoja on kohdassa [Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta](sales-how-enable-payment-service-extensions.md).

Ota sähköpostit käyttöön [!INCLUDE[prod_short](includes/prod_short.md)]issa käynnistämällä ohjattu **Määritä sähköposti** -määritys. Lisätietoja on kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] tukee vain lähteviä sähköpostiviestejä. Et voi vastaanottaa vastauksia sovelluksessa.

## Asiakirjojen lähettäminen sähköpostitse

Tässä kuvataan, miten kirjattu myyntilasku liitetään sähköpostiin PDF-tiedostona ja asiakirjakohtaisen sähköpostiviestin tekstinä. Vaiheet ovat samat muissa asiakirjoissa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntilaskut** ja valitse sitten vastaava linkki.
2. Valitse lasku ja sitten **Tulosta/Lähetä**-toiminto ja valitse **Lähetä sähköpostilla**.
3. Valitse **Sähköposti**-kentässä **Kyllä (Pyydä asetuksia)**. Lisätietoja on kohdassa [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).

    Jos **Sähköposti**-kentän arvoksi on **Lähetä asiakirja kohteeseen** -sivulla määritetty **Kyllä (Pyydä asetuksia)**, **Lähetä sähköposti** -sivu avautuu. Sivun **Vastaanottaja:**-kenttään on esitäytetty kontaktihenkilön tiedot ja asiakirja on liitetty PDF-tiedostona. Voit syöttää tekstin manuaalisesti **Perusteksti**-kenttään tai kenttään voidaan täyttää määrittämäsi asiakirjakohtaisen sähköpostin perusteksti.

4. Valitse **OK**-painike.
5. Syötä **Vastaanottaja:**-kenttään kelvollinen sähköpostiosoite. Oletusarvo on asiakkaan sähköpostiosoite.
6. Kirjoita **Aihe**-kenttään kuvaava aiheteksti. Oletusarvo on asiakkaan nimi ja laskun numero.
7. Luotu lasku on liitetty **Liite**-kenttään oletusarvoisesti PDF-tiedostona.
8. Kirjoita **Runkoteksti**-kenttään lyhyt viesti vastaanottajalle.

    Jos asiakirjakohtainen sähköpostin teksti on määritetty **Raporttivalinta - Myynti** -sivulla, **Perusteksti**-kenttä täytetään automaattisesti. Lisätietoja: [Uudelleenkäytettävien sähköpostitekstien ja -asettelujen määrittäminen](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).
9. Valitse **OK**-painike, kun haluat lähettää sähköpostiviestin.

> [!NOTE]  
> Jos et halua määrittää sähköpostiviestin asetuksia aina, kun lähetät asiakirjan sähköpostitse, valitse **Kyllä (Käytä oletusasetuksia)** -vaihtoehto **Lähetä asiakirja kohteeseen** -sivun **Sähköposti**-kentässä. Tällöin **Lähetä sähköposti** -sivu ei avaudu. Lisätietoja on vaiheessa 4. Lisätietoja on kohdassa [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).  

## Sähköpostin kirjoittaminen ja lähettäminen

Voit luoda nopeasti sähköpostit kontakteille, asiakkaille, toimittajille, myyjille/ostajille ja pankkitileille suoraan kyseisten entiteettien sivuilta. Valitse vain **Käsittele** ja **Lähetä sähköpostiviesti** sähköpostieditorin avaamista varten. Pankkitileille **Lähetä sähköpostiviesti** -toiminto on kohdassa **Toiminnot**.

> [!TIP]
> Jos lähetät usein samankaltaisia sähköpostiviestejä tai haluat lähettää joukkoviestintää esimerkiksi myyntikampanjan mainostamista varten, voit nopeuttaa prosessia käyttämällä Word-malleja sähköpostiviesteissä. Voit luoda mallin sellaisille entiteeteille kuten asiakkaat, toimittajat ja kontaktit, jotka luovat sähköpostiviestin sisällön ja jopa räätälöivät sen vastaanottajan mukaan [!INCLUDE[prod_short](includes/prod_short.md)]in tietojen perusteella. Lisätietoja on kohdassa [Word-mallien käyttäminen joukkoviestinnässä](ui-mail-merge.md).  

### Liitä asiakirja sähköpostiviestiin

Asiakirjoja voi liittää sähköpostiviesteihin usealla eri tavalla.

Jos sinulle on delegoitu sähköpostiskenaario, joka liittyy entiteettiin, jolle lähetät sähköpostiviestin, tai asiakirjaan, jonka lähetät, liite saatetaan liittää viestiin automaattisesti. Tämä johtuu siitä, että sähköpostiskenaariolle on määritetty oletusliite. Voit poistaa liitteen, jos et halua lähettää liitettä viestissä. Lisätietoja on kohdassa [Sähköpostiskenaarioiden määrittäminen sähköpostitileille](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts). 

Voit liittää tiedoston itse sähköpostieditorissa seuraavien toimintojen avulla:

* Valitse tiedosto valitsemalla **Lisää tiedosto**.
* Voit lisätä sähköpostiskenaarioon liittyvän tiedoston manuaalisesti valitsemalla **Lisää tiedostot oletusvalinnasta**.
* Valitse asiakirjaan liitetty tiedosto valitsemalla **Lisää tiedosto lähdeasiakirjasta**. Tiedostot on liitetty joko itse asiakirjaan tai yhteen tai useampaan sen riviin.

## Asiakirjat, jotka on merkitty tulostetuiksi, kun ne lähetetään

Joissakin [!INCLUDE[prod_short](includes/prod_short.md)] -sivuston asia kirjoissa on kenttä, joka määrittää, kuinka monta kertaa asiakirja on tulostettu. Kentän numero <!--"that field?" need a name...--> päivitetään myös, jos lähetät asiakirjan sähköpostitse, koska sille luodaan PDF-tiedosto. Numero päivittyy, vaikka et lähettäisi sähköpostia. <!--guessing this is because emails are technically reports, so the counter bumps up whenever someone creates an email. Need to verify.-->

## Lähetetyt sähköpostit ja lähtevien sähköpostien kansio

[!INCLUDE[prod_short](includes/prod_short.md)] tallentaa lähettämäsi sähköpostit **Lähetetyt**-sivulle. Se antaa sinun lähettää sähköposteja uudelleen tai lähettää ne jollekulle muulle. Jos et löydä sähköpostia lähetetyistä kohteista, etsi se **Sähköpostin Lähtevät-kansio** -sivulta. 

> [!NOTE]
> Järjestelmänvalvoja voi nähdä kaikkien lähettämien viestien luettelon, mutta ei viestien sisältöä, sen mukaan, mitä sähköpostilaajennusta yrityksesi käyttää.

**Sähköpostin Lähtevät-kansioon** on tallennettu luonnoksina tallentamasi sähköpostit ja sähköpostit, joita ei voitu lähettää, esimerkiksi jos sähköpostiosoite oli virheellinen. Viesteille, joita ei voitu lähettää, voit valita **Näytä virhe** tai **tutki virhe** ja tehdä ongelman vianmäärityksen.  

## Katso myös

[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
[Sähköpostin määrittäminen](admin-how-setup-email.md)  
[Lasku – myynti](sales-how-invoice-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
