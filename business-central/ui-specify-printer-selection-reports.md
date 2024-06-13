---
title: Oletuskirjoittimen määrittäminen
description: 'Lue lisää eri tavoista määrittää tulostimet, joita käytetään oletusarvoisesti tulostustyöhön.'
author: jswymer
ms.topic: how-to
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.search.keywords: 'online printing, email printing, cloud printing, Universal Print'
ms.search.form: '2650, 2750, 2752, 2753, 2754, 8900,'
ms.date: 02/09/2023
ms.author: jswymer
---
# <a name="specify-a-default-printer"></a><a name="default"></a>Oletuskirjoittimen määrittäminen

Kun tulostimet on määritetty Business Centralin avulla, voit määrittää, mitä tulostinta haluat käyttää oletusarvoisesti. Raporteissa ja muissa tulostustöissä oletusarvoisesti käytettävät tulostimet voidaan määrittää muutamalla eri tavalla. Oletustulostin on kätevä, jos käytössä on raportteja, joissa on käytettävä eri tulostinta sen vuoksi, miten ne on sijoitettu yrityksessä tai mitä tulostusominaisuuksia niissä on.

> [!IMPORTANT]
> Ainoat tulostimet, joita voit määrittää oletustulostimiksi, ovat **Microsoft Print to PDF**- ja pilvitulostimet, jotka on jo määritetty käytettäviksi Business Centralin yhteydessä, kuten sähköpostitulostimet ja Universal Print -tulostimet. Pilvipohjaiset tulostimet määritetään tavallisesti järjestelmänvalvojan toimesta. Lisätietoja on kohdassa [Tulostimen asetukset ja hallinta](admin-printer-setup-overview.md).   

## <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Tulostimen määrittäminen kaikkien tulostustöiden oletustulostimeksi

**Tulostimen hallinta** -sivulla tulostimen voi määrittää kaikkien tulostustöiden oletustulostimeksi. Tulostimen voi määrittää oletustulostimeksi joko itselle tai kaikille käyttäjille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tulostimien hallinta** ja valitse sitten vastaava linkki.

    > [!TIP]
    > **Tulostimen hallinta** -sivun voi avata myös valitsemalla **Tulostimen hallinta** **Tulostimen valinnat** -sivulla.  
2. Valitse tulostin luettelossa **Tulostimen hallinta**-sivulla. Valitse sitten **Hallinta** ja lopuksi **Määritä oletustulostimeksi** tai **Määritä kaikkien käyttäjien oletustulostimeksi**.

> [!NOTE]
> Kun oletustulostin määritetään **Tulostimen hallinta** -sivulla, **Tulostimen valinnat** -sivulle lisätään merkintä.

## <a name="set-a-default-printer-for-specific-reports"></a>Oletustulostimen määrittäminen tietyille raporteille

**Tulostimen valinnat** -sivulla voidaan määrittää tulostin, jota raportti oletusarvoisesti käyttää. Oletustulostimet määritetään käyttäjätilin perusteella. Oletustulostin voidaan määrittää vain itselle, toiselle käyttäjälle tai kaikille käyttäjille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tulostimien valinta** ja valitse sitten liittyvä linkki. Vaihtoehtoisesti voit valita **Tulostimen hallinta** -sivulla tulostimen ja valita sitten **Tulostinvalinnat**-toiminnon.
2. Valitse **Uusi**-toiminto, jos haluat lisätä tulostinvalinnan tiettyä raporttia varten.
3. Täytä tarvittavat kentät.

Määritetty raportti on nyt määritetty tulostamaan halutulle tulostimelle oletusarvoisesti.

> [!NOTE]
> Kun kyseinen raportti tulostetaan, voit valita toisen tulostimen käyttämällä raportin pyyntösivun **Tulosta**-kenttää.

> [!NOTE]
> Jos et määritä raporttia tietylle tulostimelle **Tulostinvalinnat**-sivulla, se tulostetaan yrityksen oletustulostimeen **Tulostimen hallinta** -sivun määritysten mukaisesti.

Sinä tai järjestelmänvalvoja voitte käyttää myös **Tulostinvalinnat**-sivua käyttäjien ja raporttien muiden tulostusvaihtoehtojen määrittämisessä. Seuraava taulukko sisältää niiden arvojen yhdistelmät, joiden avulla määritetään raportin eri tulostusasetukset.

|Vastaanottaja                                                 |Määritä seuraavat arvot                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Tulosta raportti tiettyyn tulostimeen kaikille käyttäjille |Määritä arvot **Raportin tunnus**- ja **Tulostimen nimi** -kenttiin ja jätä **Käyttäjän tunnus** -kenttä tyhjäksi.|
|Tulosta kaikki raportit tiettyyn tulostimeen tietylle käyttäjälle|Määritä arvot **Käyttäjän tunnus**- ja **Tulostimen nimi** -kenttiin ja jätä **Raportin tunnus** -kenttä tyhjäksi. Tämä merkintä toimii samoin kuin **Määritä oletustulostimeksi** -toiminto **Tulostuksen hallinta** -sivulla.|
|Kaikki raporttien oletustulostimen määrittäminen kaikille käyttäjille|Määritä arvo **Tulostimen nimi** -kenttään ja jätä **Käyttäjän tunnus**- ja **Raportin tunnus** -kentät tyhjiksi. Tämä merkintä toimii samoin kuin **Määritä oletustulostimeksi kaikille käyttäjille** -toiminto **Tulostuksen hallinta** -sivulla.|
|Tulosta tietty raportti käyttäjän oletustulostimeen|Määritä arvo **Raportin tunnus** -kenttään ja jätä **Tulostimen nimi**- ja **Käyttäjän tunnus** -kentät tyhjiksi.|
|Tulosta tietty raportti tiettyyn tulostimeen tietylle käyttäjälle|Määritä arvot kaikkiin kolmeen kenttään.|

> [!NOTE]
> Yksityiskohtaiset tulostinvalinnat ohittavat yleisemmät tulostinvalinnat. Esimerkiksi tulostinvalinta, jossa on arvot **Käyttäjän tunnus**-, **Raportin tunnus**- ja **Tulostimen nimi** -kentissä, ohittaa tulostinvalinnan, jossa **Käyttäjän tunnus**- tai **Raportin tunnus** -kentät ovat tyhjät.

## <a name="choosing-the-printer-when-running-a-report"></a>Tulostimen valitseminen raporttia suoritettaessa

Sen sijaan, että käytät oletustulostinta raporttia suoritettaessa, voit ohittaa tämän asetuksen pyyntösivulla. Valitse vain avattavasta **Tulostin**-valikosta, mitä tulostinta haluat käyttää tässä raportin luonnissa.

## <a name="sizing-print-jobs"></a>Tulostustöiden mitoitus

Pilvitulostus on suunniteltu kohtuullisen kokoisia asiakirjoja varten. Useimmissa pilvipalveluissa, kuten PrintNode- ja HP ePrint -palveluissa, on enintään 10 megatavua työtä kohti. Jos haluat tulostaa suurempia raportteja, ne täytyy ehkä jakaa useisiin tulosteisiin.

## <a name="see-also"></a>Katso myös

[Tulostimen hallinta](admin-printer-setup-overview.md)  
[Yleistulostuksen tulostimien määrittäminen](admin-printer-setup-universal-print.md)  
[Sähköpostitulostuksen määrittäminen](admin-printer-setup-email.md)  
[Raportin tulostaminen](ui-work-report.md#PrintReport)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eräajojen ajaminen](ui-how-run-batch-jobs.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
