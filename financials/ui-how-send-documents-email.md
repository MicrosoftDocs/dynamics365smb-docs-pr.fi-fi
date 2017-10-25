---
title: "Asiakirjakohtaisen sisällön ja sähköpostiviestien liitteiden määrittäminen | Microsoft Docs"
description: "Voit määrittää sähköpostiviestin perustekstiin lisättävän sisällön, kuten PayPal-linkin. Voit myös liittää asiakirjoja sähköpostiviesteihin."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365, cover, body, PayPal, layout
ms.date: 03/30/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: afc73b146ce3c95ea47ac935e826b27f0a18d325
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-send-documents-by-email"></a>Toimintaohje: Asiakirjojen lähettäminen sähköpostitse
Voit kertoa liiketoiminta-asiakirjojen sisällön, kuten esimerkiksi asiakkaiden myyntiasiakirjojen maksutiedot, liiketoimintakumppaneille nopeasti Raporttiasettelu-toiminnolla. Voit määrittää asiakirjakohtaisen sisällön, joka lisätään sähköpostien perustekstiin automaattisesti. Lisätietoja on kohdassa [Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md).

Ota sähköpostit käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa käynnistämällä avustetun **Määritä sähköposti** -asennuksen aloitussivulla.

Voit lähettää käytännössä kaikkia asiakirjatyyppejä sähköpostitse sähköpostiviestien liitteinä suoraan asiakirjan ikkunasta. Liitteen lisäksi voit määrittää asiakirjakohtaisia sähköpostin perustekstejä, jotka sisältävät asiakirjan perustiedot. Niitä edeltää vakioteksti, jossa tervehditään viestin vastaanottajaa ja esitellään kyseessä oleva asiakirja. Voit tarjota asiakkaillesi mahdollisuuden maksaa sähköisesti käyttämällä maksupalvelua, kuten PayPalia. Sähköpostin perustekstiin voi siten lisätä myös PayPal-tiedot ja -hyperlinkin.

Sähköpostin luominen aloitetaan kaikissa tuetuissa asiakirjoissa valitsemalla **Lähetä**-toiminto kirjatuissa asiakirjoissa ja **Kirjaa ja lähetä** -toiminto muissa kuin kirjatuissa asiakirjoissa.

Jos **Sähköposti**-kentän arvoksi on **Lähetä asiakirja kohteeseen** -ikkunassa määritetty **Kyllä (Pyydä asetuksia)**, **Lähetä sähköposti** -ikkuna avautuu. Ikkunan **Vastaanottaja:**-kenttään on esitäytetty kontaktihenkilön tiedot ja asiakirja on liitetty PDF-tiedostona. Voit syöttää tekstin manuaalisesti **Perusteksti**-kenttään tai kenttään voidaan täyttää määrittämäsi asiakirjakohtaisen sähköpostin perusteksti.

Seuraavassa kuvataan, miten sähköpostitse lähetettävien myyntilaskujen asiakirjakohtaisissa sähköpostien perusteksteissä käytettävä **Myyntilasku**-raportti määritetään.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Asiakirjakohtaisen sähköpostin perustekstin määrittäminen myyntilaskuille
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Raporttivalinnat - Myynti** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Raporttivalinta - Myynti** -ikkunan **Käyttö**-kentässä **Lasku**.
3. Valitse **Raportin tunnus** -kentän uudella rivillä esimerkiksi vakioraportti 1306.
4. Valitse **Käytä sähköpostin perustekstinä** -valintaruutu.
5. Valitse ensin **Sähköpostin perustekstin asettelun koodi** -kenttä ja sitten asettelu avattavasta luettelosta.

    Raporttiasettelut määrittävät sähköpostin perustekstin tyylin ja sisällön. Siihen kuuluu myös vakioteksti, joka edeltää asiakirjan perustietoja sähköpostin perustekstissä. Saat kaikki käytettävissä olevat raporttiasettelut näkyviin, jos valitset avattavassa luettelossa **Valitse koko luettelosta** -painikkeen.
6. Voit tarkastella tai muokata asettelua, johon sähköpostin perusteksti perustuu, valitsemalla ensin asettelun **Mukautetut raporttiasettelut** -ikkunassa ja sitten **Muokkaa asettelua** -toiminnon.
7. Jos haluat tarjota asiakkaillesi mahdollisuuden maksaa sähköisesti, voit määrittää liittyvän maksupalvelun, kuten PayPalin. Tämän jälkeen sähköpostin perustekstiin voi lisätä myös PayPal-tiedot ja -hyperlinkin. Lisätietoja on kohdassa [Toimintaohje: Asiakkaan maksujen ottaminen käyttöön PayPalin kautta](sales-how-enable-payment-service-extensions.md).
8. Valitse **OK**-painike.

Kun nyt valitset esimerkiksi **Kirjattu myyntilasku** -ikkunassa **Lähetä**-toiminnon, sähköpostin perusteksti sisältää raportin 1306 asiakirjan tiedot, joita edeltää tyylitelty vakioteksti vaiheessa 5 valitun raporttiasettelun mukaan.

Seuraavassa kerrotaan, miten kirjattu myyntilasku lähetetään sähköpostiviestinä, johon on liitetty asiakirja PDF-tiedostona ja joka sisältää asiakirjakohtaisen sähköpostin perustekstin.

## <a name="to-send-documents-by-email"></a>Asiakirjojen lähettäminen sähköpostitse
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kirjatut myyntilaskut** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse ensin soveltuva kirjattu myyntilasku ja sitten **Lähetä**-toiminto. **Lähetä asiakirja kohteeseen** -ikkuna avautuu.
3. Valitse **Sähköposti**-kentässä **Kyllä (Pyydä asetuksia)**. Lisätietoja on kohdassa [Toimintaohje: Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).
4. Valitse **OK**-painike. **Lähetä sähköposti** -ikkuna avautuu.
5. Syötä **Vastaanottaja:**-kenttään kelvollinen sähköpostiosoite. Oletusarvo on asiakkaan sähköpostiosoite.
6. Kirjoita **Aihe**-kenttään kuvaava aiheteksti. Oletusarvo on asiakkaan nimi ja laskun numero.
7. Luotu lasku on liitetty **Liite**-kenttään oletusarvoisesti PDF-tiedostona. Valitse valintapainike, kun haluat avata tiedoston tai liittää toisen tiedoston.
8. Kirjoita **Runkoteksti**-kenttään lyhyt viesti vastaanottajalle.

    Jos asiakirjakohtainen sähköpostin perusteksti on määritetty **Raporttivalinta - Myynti** -ikkunassa, **Perusteksti**-kenttä täytetään automaattisesti. Lisätietoja on tämän ohjeaiheen Asiakirjakohtaisen sähköpostin perustekstin määrittäminen myyntilaskuille -osassa.
9. Valitse **OK**-painike, kun haluat lähettää sähköpostiviestin.

> [!NOTE]  
>   Jos et halua määrittää sähköpostiviestin asetuksia aina, kun lähetät asiakirjan sähköpostitse, valitse **Kyllä (Käytä oletusasetuksia)** -vaihtoehto **Lähetä asiakirja kohteeseen** -ikkunan **Sähköposti**-kentässä. Tällöin **Lähetä sähköposti** -ikkuna ei avaudu. Lisätietoja on vaiheessa 4. Lisätietoja on kohdassa [Toimintaohje: Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).

## <a name="see-also"></a>Katso myös
[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
[Toimintaohje: Sähköpostin määrittäminen](madeira-how-setup-email.md)  
[Toimintaohje: Myynnin laskutus](sales-how-invoice-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

