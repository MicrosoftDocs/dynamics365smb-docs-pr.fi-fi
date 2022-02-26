---
title: Asiakirjojen ja sähköpostien lähettäminen
description: Voit määrittää sähköpostiviestin perustekstiin lisättävän sisällön, kuten PayPal-linkin. Voit myös liittää asiakirjoja sähköpostiviesteihin.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, cover, body, PayPal, layout
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3322199feee09c656b01c7723a8c95396015cde4
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588449"
---
# <a name="send-documents-and-emails"></a>Asiakirjojen ja sähköpostien lähettäminen

Voit helposti jakaa tietoja ja asiakirjoja, kuten myynti- ja ostotilauksia ja laskuja, sähköpostitse suoraan [!INCLUDE[prod_short](includes/prod_short.md)]ista ilman sähköpostisovelluksen avaamista.  

Voit lähettää lähes kaikentyyppisiä asiakirjoja PDF-liitteinä. Vaihtoehtoisesti voit määrittää raportin asettelun, joka sisältää asiakirjan tiedot sähköpostin tekstissä sekä tekstin, joka tekee sähköposteista entistä ystävällisempiä, esimerkiksi vakiotervehdyksen. Lisätietoja on kohdassa [Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md). <!--this topic does not mention how to set up a layout for email. Need to investigate.-->

Laskujen lähettämisen yhteydessä asiakkaiden on helpompi suorittaa maksuja maksupalvelun (esimerkiksi PayPalin) kautta lisäämällä automaattisesti sähköpostissa tietoja ja linkin palveluun. Lisätietoja on kohdassa [Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta](sales-how-enable-payment-service-extensions.md).

Ota sähköpostit käyttöön [!INCLUDE[prod_short](includes/prod_short.md)]issa käynnistämällä ohjattu **Määritä sähköposti** -määritys. Lisätietoja on kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] tukee vain lähteviä sähköpostiviestejä. Et voi vastaanottaa vastauksia sovelluksessa.

## <a name="to-send-documents-by-email"></a>Asiakirjojen lähettäminen sähköpostitse

Tässä kuvataan, miten kirjattu myyntilasku liitetään sähköpostiin PDF-tiedostona ja asiakirjakohtaisen sähköpostiviestin tekstinä. <!--update this-->

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntilaskut** ja valitse sitten vastaava linkki.
2. Valitse lasku ja sitten **Tulosta/Lähetä**-toiminto ja valitse **Lähetä**.
3. Valitse **Sähköposti**-kentässä **Kyllä (Pyydä asetuksia)**. Lisätietoja on kohdassa [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).
    
    Jos **Sähköposti**-kentän arvoksi on **Lähetä asiakirja kohteeseen** -sivulla määritetty **Kyllä (Pyydä asetuksia)**, **Lähetä sähköposti** -sivu avautuu. Sivun **Vastaanottaja:**-kenttään on esitäytetty kontaktihenkilön tiedot ja asiakirja on liitetty PDF-tiedostona. Voit syöttää tekstin manuaalisesti **Perusteksti**-kenttään tai kenttään voidaan täyttää määrittämäsi asiakirjakohtaisen sähköpostin perusteksti.

4. Valitse **OK**-painike.
5. Syötä **Vastaanottaja:**-kenttään kelvollinen sähköpostiosoite. Oletusarvo on asiakkaan sähköpostiosoite.
6. Kirjoita **Aihe**-kenttään kuvaava aiheteksti. Oletusarvo on asiakkaan nimi ja laskun numero.
7. Luotu lasku on liitetty **Liite**-kenttään oletusarvoisesti PDF-tiedostona.
8. Kirjoita **Runkoteksti**-kenttään lyhyt viesti vastaanottajalle.

    Jos asiakirjakohtainen sähköpostin teksti on määritetty **Raporttivalinta - Myynti** -sivulla, **Perusteksti**-kenttä täytetään automaattisesti. Lisätieoja: [Uudelleenkäytettävien sähköpostitekstien ja -asettelujen määrittäminen myynti- ja ostoasiakirjoille](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents).
9. Valitse **OK**-painike, kun haluat lähettää sähköpostiviestin.

> [!NOTE]  
> Jos et halua määrittää sähköpostiviestin asetuksia aina, kun lähetät asiakirjan sähköpostitse, valitse **Kyllä (Käytä oletusasetuksia)** -vaihtoehto **Lähetä asiakirja kohteeseen** -sivun **Sähköposti**-kentässä. Tällöin **Lähetä sähköposti** -sivu ei avaudu. Lisätietoja on vaiheessa 4. Lisätietoja on kohdassa [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).  

## <a name="to-compose-and-send-an-email"></a>Sähköpostin kirjoittaminen ja lähettäminen
Voit luoda nopeasti sähköpostit kontakteille, asiakkaille, toimittajille, myyjille/ostajille ja pankkitileille suoraan kyseisten entiteettien sivuilta. Valitse vain **Käsittele** ja **Lähetä sähköpostiviesti** sähköpostieditorin avaamista varten. Pankkitileille **Lähetä sähköpostiviesti** -toiminto on kohdassa **Toiminnot**.

> [!TIP]
> Jos lähetät usein samankaltaisia sähköpostiviestejä tai haluat lähettää joukkoviestintää esimerkiksi myyntikampanjan mainostamista varten, voit nopeuttaa prosessia käyttämällä Word-malleja sähköpostiviesteissä. Voit luoda mallin sellaisille entiteeteille kuten asiakkaat, toimittajat ja kontaktit, jotka luovat sähköpostiviestin sisällön ja jopa räätälöivät sen vastaanottajan mukaan [!INCLUDE[prod_short](includes/prod_short.md)]in tietojen perusteella. Lisätietoja on kohdassa [Word-mallien käyttäminen joukkoviestinnässä](ui-mail-merge.md).  

## <a name="documents-marked-as-printed-when-they-are-sent"></a>Asiakirjat, jotka on merkitty tulostetuiksi, kun ne lähetetään

Joissakin [!INCLUDE[prod_short](includes/prod_short.md)] -sivuston asia kirjoissa on kenttä, joka määrittää, kuinka monta kertaa asiakirja on tulostettu. Kentän numero <!--"that field?" need a name...--> päivitetään myös, jos lähetät asiakirjan sähköpostitse, koska sille luodaan PDF-tiedosto. Numero päivittyy, vaikka et lähettäisi sähköpostia. <!--guessing this is because emails are technically reports, so the counter bumps up whenever someone creates an email. Need to verify.-->

## <a name="sent-emails-and-your-email-outbox"></a>Lähetetyt sähköpostit ja lähtevien sähköpostien kansio

[!INCLUDE[prod_short](includes/prod_short.md)] tallentaa lähettämäsi sähköpostit **Lähetetyt**-sivulle. Se antaa sinun lähettää sähköposteja uudelleen tai lähettää ne jollekulle muulle. Jos et löydä sähköpostia lähetetyistä kohteista, etsi se **Sähköpostin Lähtevät-kansio** -sivulta. 

> [!NOTE]
> Järjestelmänvalvoja voi nähdä kaikkien lähettämien viestien luettelon, mutta ei viestien sisältöä, sen mukaan, mitä sähköpostilaajennusta yrityksesi käyttää.

**Sähköpostin Lähtevät-kansioon** on tallennettu luonnoksina tallentamasi sähköpostit ja sähköpostit, joita ei voitu lähettää, esimerkiksi jos sähköpostiosoite oli virheellinen. Viesteille, joita ei voitu lähettää, voit valita **Näytä virhe** tai **tutki virhe** ja tehdä ongelman vianmäärityksen.  

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/set-up-email/)

## <a name="see-also"></a>Katso myös

[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
[Sähköpostin määrittäminen](admin-how-setup-email.md)  
[Myynnin laskutus](sales-how-invoice-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
