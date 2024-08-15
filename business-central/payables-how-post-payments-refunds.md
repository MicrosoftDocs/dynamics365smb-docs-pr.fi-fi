---
title: Maksujen ja hyvitysten tallentaminen maksupäiväkirjaan
description: 'Tietoja siitä, miten kirjaat maksut toimittajille tai hyvitykset asiakkaille Maksupäiväkirja-sivulla.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment journal, print check, vendor payment, customer refund, refund check, creditor, debt, balance due, AP'
ms.search.form: '256, 233, 624, 1228'
ms.date: 07/17/2024
ms.service: dynamics-365-business-central
---
# Maksujen ja hyvitysten tallentaminen maksupäiväkirjaan

 **Maksupäiväkirjat-sivulle tallennetaan toimittajille suoritetut** maksut ja asiakkaille suoritetut hyvitykset. Kun kirjaat maksupäiväkirjan rivin, maksettu summa kirjataan määritetylle pankkitilille. Sinun on tehtävä sitten todellinen rahan siirto liittyvältä pankkitililtä muutaman vaiheen kautta.  

Maksupäiväkirjat ovat yleisiä päiväkirjoja, joka on tarkoitettu erityisesti maksujen tekemiseen. Voit nopeasti lisätä rivejä manuaalisesti, antaa [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen ehdottaa toimittajamaksuja ja kohdistaa maksun kirjattuihin asiakirjoihin. Vaikka olet tekemässä maksuja, voit syöttää **Asiakirjan summa** -kenttään positiivisen summan. Päiväkirjan rivin asiakirjan tyypistä riippuen summa voidaan muuttaa negatiiviseksi summaksi taustalla olevissa tapahtumissa. Näin päiväkirjan rivien lisääminen manuaalisesti on helpompaa. Jos haluat syöttää negatiivisia summia, voit mukauttaa maksupäiväkirjan niin, että näkyvissä on **Summa**-kenttä. Saat lisätietoja sivujen mukauttamisesta siirtymällä kohtaan [Sivun mukauttamisen aloittaminen mukauttamistoiminnon](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode) avulla.  

- Maksujen kohdistaminen laskuihin tai hyvityslaskuihin

    Jos täytät **Kohdistetaan asiakirjaan nro** -kenttään maksettavan laskun tai hyvityslaskun, kyseinen asiakirja määritetään **maksettavaksi**, kun päiväkirja kirjataan. Tätä asetusta kutsutaan kohdistukseksi." Vaihtoehtona maksun kirjaamisen aikana voit käyttää **Kohdista toimittajatapahtumat**- tai **Kohdista asiakastapahtumat** -sivuja, kun olet tehnyt maksun kirjaamisen. Lue lisätietoja esimerkiksi kohdassa [Toimittajamaksujen täsmäyttäminen maksukirjauskansiolla tai toimittajatapahtumista](payables-how-apply-purchase-transactions-manually.md)  

- Ehdotettujen maksujen hakeminen toimittajille tai työntekijöille

    **Ehdota toimittajamaksuja**- ja **Ehdota työntekijämaksuja** -toiminnot voivat auttaa sinua täyttämään maksupäiväkirjan rivit automaattisesti toimittajien priorisointien ja eräpäivien mukaan. Lisätietoja on kohdassa [Ehdota toimittajamaksuja](payables-how-suggest-vendor-payments.md). Tätä toimintoa käytettäessä **Kohdistetaan asiakirjaan nro** -kenttä täytetään aina.  

- Sekkien tulostaminen ja maksujen lähettäminen sähköisesti pankkiin

    Maksun suorituksen kirjaamisen lisäksi voit käyttää myös **Maksupäiväkirja**-sivua siirtämään maksun pankin lisäkäsittelyä varten. Lisätietoja on kohdissa [Sekkimaksujen suorittaminen](payables-how-work-checks.md) ja [Sähköisten maksujen suorittaminen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## Maksujen tekeminen maksupäiväkirjaan

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten vastaava linkki.
2. Avaa päiväkirjaerä, jota käytät maksuja varten.
3. Jos tiedät, kenelle olet maksamassa, täytä kentät manuaalisesti. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Jos haluat kohdistaa maksun myös laskuun tai hyvityslaskuun, valitse **Kohdistetaan asiakirjaan nro**  **valitse asianmukainen lasku tai hyvityslasku Kohdista toimittajatapahtumat -** sivulta ja valitse **sitten OK-painike** .

    Monet kentät, kuten **Asiakirjan summa** ja **Eräpäivä**, sisältävät nyt valitun asiakirjan tietoja.
5. Vaihtoehtoisesti voit käyttää **Ehdota toimittajamaksuja** -toimintoa. Myös kaikki kohdistustiedot ja summat syötetään päiväkirjariveille. Lisätietoja on kohdassa [Ehdota toimittajamaksuja](payables-how-suggest-vendor-payments.md).
6. Kun kaikki maksupäiväkirjan rivit ovat valmiit, valitse **Kirjaa**-toiminto.

## Palautussekin julkaiseminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten liittyvä linkki.
2. Valitse **Asiakirjatyyppi**-kentässä **Hyvitys**.  
3. Käytä **Ulkoisen asiakirjan nro** -kentässä tätä viitteenä palautussekille (esimerkiksi palautustilauksen numero).  
4. Valitse **Tilityyppi**-kentässä **Asiakas**.  
5. Valitse **Tilinumero** -kentässä asiakkaan tilinumero, jolle palautussekki julkaistaan.  
6. Syötä hyvitettävä summa **Summa**-kenttään.  
7. Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.  
8. Vastatilin **nro** -kentässä, valitse pankkitili, josta sekki tulee.  
9. Valitse **Kohdistetaan asiakirjaan nro** -kentässä hyvitystä vaativat asiakirjat.  
10. Kun kaikki maksupäiväkirjan rivit on täytetty, valitse **Kirjaa/tulosta**-toiminto, valitse **Kirjaa ja tulosta** -toiminto ja valitse sitten **Kyllä**.  
  
## Katso myös

[Sekkimaksujen suorittaminen](payables-how-work-checks.md)  
[Sähköisten maksujen tekeminen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Positive Pay -tiedoston vienti](finance-how-positive-pay.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Työtilan mukauttaminen](ui-personalization-user.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
