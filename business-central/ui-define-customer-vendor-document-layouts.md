---
title: Asiakirja-asettelujen määrittäminen asiakkaille tai toimittajille
description: 'Asiakirja-asetteluiden avulla voit valvoa asiakkaille ja toimittajille lähetettävien asiakirjojen, kuten laskujen ja tilausten, ulkoasua ja muotoa.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '21, 9650'
ms.date: 04/07/2022
ms.author: edupont
---
# <a name="define-document-layouts-for-customers-and-vendors" />Asiakirja-asettelujen määrittäminen asiakkaille ja toimittajille

Asiakirja-asettelut määrittävät asiakkaille ja toimittajille lähetettävien asiakirjojen ulkoasun raporttiasetteluiden avulla. Business Central sisältää vakioasetteluita. Voit halutessasi myös räätälöidä mukautettuja asetteluita jokaiselle liiketoimintakumppanille. Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md). Voit valita vakiomuotoiset ja mukautetut asiakirja-asettelut asiakas- ja toimittajakorteista valitsemalla **Asiakirja-asettelut**-toiminnon. **Käyttö**-kentän arvo määrittää prosessin, jossa asiakirja-asettelua käytetään. Esimerkiksi asiakkaiden kohdalla voidaan käyttää asiakirja-asetteluiden **Muistutus**-, **Toimitus**- ja **Vahvistus**-tyyppejä.

Asiakirja-asettelut voivat myös säästää aikaa, kun asiakirjoja lähetetään asiakkaan tai toimittajan yhteyshenkilöille sähköpostitse. Voit määrittää jokaiselle asiakkaalle tai yhteyshenkilölle määritetylle asettelulle vähintään yhden yhteyshenkilön sähköpostiosoitteen. Voit esimerkiksi lähettää laskun asiakkaan osto- ja varastoyhteyshenkilöille. Yhteyshenkilön sähköpostiosoitteiden lisääminen on helppoa. Valitse **Asiakirja-asettelut**-sivulla **Valitse sähköpostiosoite yhteyshenkilöistä** -toiminto, jos haluat tehdä valinnan asiakkaalle tai toimittajalle rekisteröityjen yhteyshenkilöiden sähköpostiosoitteiden luettelosta. Voit myös lisätä sähköpostiosoitteita manuaalisesti. Jos syötät useita osoitteita, erottele ne puolipisteellä äläkä lisää välilyöntejä osoitteiden välille.

Ennen kuin voit määrittää, mitä asiakirja-asettelua käytetään mihinkin prosessiin ja mille kontaktille asiakirjan voi lähettää, sinun täytyy ladata kaikki käytettävissä olevat raportit (asiakirjat) **Raporttivalinnat**-sivulta. Voit ladata asiakirjat nopeasti käyttämällä **Kopioi raporttivalinnasta** -toiminnon **Asiakirja-asettelut**-sivulla.

Seuraavien osien vaiheissa kerrotaan, miten myyntiasiakirja-asettelut määritetään **Asiakaskortti**-sivulla. Työvaiheet ovat samat toimittajille **Toimittajakortti**-sivulla.

## <a name="to-load-the-standard-document-layouts-for-sales-documents-for-a-customer" />Vakioasiakirja-asetteluiden lataaminen asiakkaan myyntiasiakirjoja varten

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Avaa asiakkaan **Asiakaskortti**-sivu ja valitse **Asiakirja-asettelut**-toiminto.
3. Valitse **Asiakirjojen asettelu** -sivulla **Kopioi raporttivalinnasta** -toiminto.

**Asiakirja-asettelut**-sivulla näytetään kaikki myyntiasiakirjan käytettävissä olevat asettelut. 

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout" />Valitse myyntiasiakirjan asettelussa käytettävä mukautettu raporttiasettelu

Jos et ole vielä luonut mukautettua raporttiasettelua asiakirjatyypille, luo se nyt. Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakkaat** ja valitse sitten vastaava linkki.
2. Avaa asiakkaan **Asiakaskortti**-sivu ja valitse **Asiakirja-asettelut**-toiminto.
3. Valitse **Asiakirjojen asettelut** -sivulla **Mukautetun asettelun kuvaus** -kenttä siltä raporttiasettelun riviltä, jolle haluat käyttää mukautettua asettelua.
4. Valitse **Mukautetut raporttiasettelut** -sivulta asiakirja-asettelu, jota haluat käyttää kyseisessä myyntiasiakirjatyypissä. Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

## <a name="to-specify-which-contact-will-receive-which-document-layout-for-a-customer" />Määritetään, kuka yhteyshenkilö vastaanottaa minkäkin asiakirja-asettelun asiakkaan kohdalla

Voit säästää aikaa lähettäessäsi asiakirja asiakkaan ja toimittajan yhteyshenkilöille sähköpostitse, jos määrität sähköpostiosoitteet asiakirja-asetteluissa. Voit esimerkiksi aina lähettää asiakastiliotteet kirjanpitäjän yhteyshenkilöille ja myyntitilaukset ostajille tai ostotilaukset toimittajan myyjille.

1. Valitse **Asiakirjan asettelut** -sivulla **Valitse sähköpostiosoite kontakteista** -toiminto siltä raporttiasettelun riviltä, jonka haluat lähettää asiakkaan tietylle kontaktille.
2. Valitse **Yhteyshenkilöt**-sivulla vähintään yksi yhteyshenkilö ja valitse sitten **OK**.

## <a name="see-related-microsoft-training" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/change-documents-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Päivitä mukautetut raporttiasettelut](ui-update-report-layouts.md)  
[Raporttien mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)  
[Raporttien tai asiakirjojen mukautetun asettelun tuonti ja vienti](ui-how-import-and-export-report-layout.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
[Raporttien, eräajojen ja XMLportien käsitteleminen](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
