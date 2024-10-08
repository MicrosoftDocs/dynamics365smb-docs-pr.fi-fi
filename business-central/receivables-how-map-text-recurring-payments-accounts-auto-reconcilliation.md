---
title: Tekstistä tiliin -yhdistämismääritys määrittäminen toistuville maksuille
description: 'Linkitä maksujen teksti tiettyihin tileihin siten, että maksut kirjataan tileille, kun kirjaat maksujen täsmäytyskirjauskansion.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt'
ms.search.form: '1290, 1294, 1287'
ms.date: 03/06/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Toistuvien maksujen tekstin linkittäminen tileihin automaattista täsmäytystä varten

**Tekstin yhdistäminen tiliin** -sivulla, joka avataan **Maksujen täsmäytyskirjauskansio** -sivulta, voit määrittää maksujen tekstin kohdistukset ja tietyt debet-, kredit- ja kirjanpidon vastatilit siten, että nämä maksut kirjataan tietyille tileille, jotta nämä maksut kirjataan tietyille tileille, kun kirjaat maksun täsmäytyksen päiväkirjan.

Vastaava toiminto on käytettävissä, kun maksujen täsmäytyskirjauskansion rivien ylimääräisiä summia täsmäytetään tapauskohtaisesti. Lisätietoja [on kohdassa Sellaisten maksujen täsmäyttäminen, joita ei voi kohdistaa automaattisesti](receivables-how-reconcile-payments-cannot-apply-auto.md).

Maksuja, jotka perustuvat tekstistä tiliin yhdistämiseen, ei käytetä avoimiin tapahtumiin vaan ne kirjataan tietyille tileille pankkitilitapahtumien lisäksi. Tämän mukaisesti tekstitilille -yhdistämismääritys soveltuu toistuviin kassakuitteihin tai kuluihin, kuten autojen polttoaineen tai pankkimaksujen toistuviin ostoihin ja korkoihin, jotka tapahtuvat säännöllisesti pankin tiliotteessa ja jotka eivät tarvitse siihen liittyvää liiketoiminta-asiakirjaa. Lisätietoja on tämän artikkelin Teksti tiliin -yhdistämismääritys kohdassa.

> [!NOTE]  
>   Täsmäytyksen päiväkirjarivien maksut asetetaan kirjattaviksi tekstistä tilien yhdistäminen -asetuksen mukaan, jos automaattinen kohdistus -toiminto voi tarjota kohdistuksen varmuudeksi vain **Pieni** tai **Keskisuuri**. Jos automaattisen sovellusfunktion avulla saadaan vastaavuus Suuri, maksu kohdistetaan automaattisesti yhteen tai useaan avoimeen tapahtumaan tai hyvityslaskuun, eikä maksua kirjata määritetyille tileille **Tekstin yhdistäminen tiliin** -sivulla. Toisin sanoen kohdistuksen **Suuri**-vastaavuus kumoaa tekstistä tiliin yhdistämisen.

Maksun täsmäytyskirjauskansion rivillä, jossa maksu on määritetty kirjatuksi Tekstistä tiliin yhdistäminen -asetuksen mukaisesti, **Vastaavuuden luotettavuus** -kentässä on **Suuri – tekstin ja tilin välinen yhdistäminen**. Lisäksi **Tilityyppi**- sekä **Tilinumero**-kentät sisältävät yhdistetyt tilit.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksujen täsmäytyskirjauskansiot** ja valitse sitten liittyvä linkki.
2. Avaa maksun täsmäytyksen päiväkirja. Lisätietoja on kohdassa [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).
3. Valitse **Linkitä teksti tiliin** -toiminto. **Tekstin yhdistäminen tiliin** -sivu avautuu.
4. Syötä **Tekstin linkitys** -kenttään mikä tahansa teksti, joka näkyy maksuissa, jotka haluat kirjata tietyille tileille kohdistamatta avoimeen tapahtumaan. Koodissa voi olla enintään 50 merkkiä.

    > [!NOTE]  
    >   Jos muita maksuja, joissa on kyseinen linkitettävä teksti, ei ole, tekstin yhdistäminen tiliin tapahtuu, vaikka maksun tekstistä vain osa on linkitettävänä tekstinä.
5. Anna **Toimittajan nro** -kentässä toimittaja, johon maksut kirjataan.
6. Määritä **Saldon lähteen tyyppi** -kenttään, kirjataanko maksu kirjanpitotilille vai asiakkaan tai toimittajan tilille.
7. Määritä **Saldon lähteen numero** -kenttään **Saldon lähteen tyyppi** -kentän valinnan mukaisesti tili, jolle maksu kirjataan.

    > [!NOTE]
    > Älä käytä maksun täsmäytyksessä **Debet-tilin numero**- ja **Kredit-tilin numero** -kenttiä. Niitä käytetään vain saapuvissa asiakirjoissa. Lisätietoja on kohdassa [PDF- ja kuvatiedostojen muuntaminen sähköisiksi asiakirjoiksi OCR-palvelun avulla](across-how-use-ocr-pdf-images-files.md).

8. Toista vaiheet 3-7 kaikkien niiden maksujen tekstien osalta, joille haluat yhdistää tilit suoraa kirjausta varten soveltamatta.

Kun tuot seuraavan kerran pankin tiliotetiedoston tai valitset **Kohdista automaattisesti** -toiminnon **Maksujen täsmäytyskirjauskansio** -sivulla, tietyn yhdistystekstin sisältävät päiväkirjan rivit sisältävät **Tilityyppi**- ja **Tilinumero**-kenttien yhdistetyt tilit. **Vastaavuuden luotettavuus** -kenttä sisältää **Suuri - Tekstin yhdistäminen tiliin** -tekstin. Tämä on edellytys sille, että automaattinen kohdistustoiminto antaa vastaavuudeksi **Matala** tai **Keskisuuri**.

## <a name="example-text-to-account-mapping-for-bank-fees"></a>Esimerkki: Pankkimaksujen Teksti tiliin -yhdistämismääritys

Jos haluat aina kirjata kulut, jotka liittyvät tietyn pankin, Mybankin, pankkikulujen ja -maksujen kirjanpitotilille (tili 60400), täytä rivi **Teksti-tilien-yhdistämiseen** -sivulle seuraavasti.

| Tekstin linkitys | Debet-tilin numero | Kredit-tilin numero | Saldon lähteen tyyppi | Saldon lähteen numero |
| --- | --- | --- | --- | --- |
| MyBank |TYHJÄ |60400|KP-tili |TYHJÄ |

## <a name="see-also"></a>Katso myös

[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
