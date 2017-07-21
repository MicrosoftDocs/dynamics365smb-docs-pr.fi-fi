---
title: "Toistuvien maksujen tekstin yhdistämisen tiliin määrittäminen | Microsoft Docs"
description: "Linkitä maksujen teksti tiettyihin tileihin siten, että maksut kirjataan tileille, kun kirjaat maksujen täsmäytyskirjauskansion."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: deb05c6294edeb892606154b38de2aa406abf6a2
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Toimintaohje: toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi
**Tekstin yhdistäminen tiliin** -ikkunassa, joka avataan **Maksujen täsmäytyskirjauskansio** -ikkunasta, voit määrittää maksujen tekstin kohdistukset ja tietyt debet-, kredit- ja kirjanpidon vastatilit siten, että nämä maksut kirjataan tietyille tileille, jotta nämä maksut kirjataan tietyille tileille, kun kirjaat maksun täsmäytyksen päiväkirjan.

> [!NOTE]  
>   Tämä ohjeaihe koskee myös **Linkitä teksti tiliin** -toiminnon käyttämistä saapuvasta asiakirjatietueesta avustettaessa niiden sähköisten asiakirjojen muuntamista, jotka on vastaanotettu ulkoisista palveluista [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakirjoiksi. Lisätietoja on kohdassa [Toimintaohje: Käytä OCR:ää muuntamaan PDF- ja kuvatiedostoja sähköisiksi asiakirjoiksi](across-how-use-ocr-pdf-images-files.md).   

Vastaava toiminto on käytettävissä, kun maksujen täsmäytyskirjauskansion rivien ylimääräisiä summia täsmäytetään ad hoc. Lisätietoja on kohdassa [Toimintaohje: Niiden maksujen täsmäyttäminen, joita ei voi kohdistaa automaattisesti](receivables-how-reconcile-payments-cannot-apply-auto.md).

Maksuja, jotka perustuvat tekstistä tiliin yhdistämiseen, ei käytetä avoimiin tapahtumiin vaan ne kirjataan tietyille tileille pankkitilitapahtumien lisäksi. Näin ollen tekstin ja tilin välinen yhdistäminen sopii toistuviin saatuihin tuloihin tai kuluihin, kuten usein tapahtuvat auton polttoaineen ostot tai pankin kulut ja korko, jotka tapahtuvat pankin tiliotteessa säännöllisesti ja jotka eivät tarvitse niihin liittyvää liiketoiminta-asiakirjaa. Lisätietoja on tämän ohjeaiheen “Esimerkki – tekstin ja tilin yhdistäminen polttoaineen kuluissa” -osassa.

> [!NOTE]  
>   Täsmäytyksen päiväkirjarivien maksut asetetaan kirjattaviksi tekstistä tilien yhdistäminen -asetuksen mukaan, jos automaattinen kohdistus -toiminto voi tarjota kohdistuksen varmuudeksi vain **Pieni** tai **Keskisuuri**. Jos automaattisen sovellusfunktion avulla saadaan vastaavuus Suuri, maksu kohdistetaan automaattisesti yhteen tai useaan avoimeen tapahtumaan tai hyvityslaskuun, eikä maksua kirjata määritetyille tileille **Tekstin yhdistäminen tiliin** -ikkunassa. Toisin sanoen kohdistuksen **Suuri**-vastaavuus kumoaa tekstistä tiliin yhdistämisen.

Maksun täsmäytyksen päiväkirjarivillä, jossa maksu on asetettu kirjatuksi tekstistä tiliin yhdistäminen -asetuksen mukaisesti, **Vastaavuuden luotettavuus** -kentässä on **Suuri – tekstin ja tilin välinen yhdistäminen**, ja **Tilityyppi**- sekä **Tilinumero**-kenttä. sisältävät yhdistetyt tilit.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksujen täsmäytyskirjauskansio** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa maksun täsmäytyksen päiväkirja. Lisätietoja on kohdassa [Toimintaohje: Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).
3. Valitse **Linkitä teksti tiliin** -toiminto. **Tekstin yhdistäminen tiliin** -ikkuna avautuu.
4. Syötä **Tekstin linkitys** -kenttään mikä tahansa teksti, joka näkyy maksuissa, jotka haluat kirjata tietyille tileille kohdistamatta avoimeen tapahtumaan. Koodissa voi olla enintään 50 merkkiä.

    > [!NOTE]  
>   Jos muita maksuja tai saapuvia asiakirjoja, joissa on kyseinen linkitettävä teksti, ei ole, tekstin yhdistäminen tiliin tapahtuu, vaikka maksun tai saapuvan asiakirjan tekstistä vain osa on linkitettävänä tekstinä.
5. **Toimittajan nro** -kenttään syötetään sen toimittajan numero, jolle yhdistettävää tekstiä sisältävät saapuvat asiakirjat luodaan tai johon maksut kirjataan. Lisätietoja on kohdassa [Toimintaohje: Käytä OCR:ää muuntamaan PDF- ja kuvatiedostoja sähköisiksi asiakirjoiksi](across-how-use-ocr-pdf-images-files.md).      
6. Syötä **Debet-tilin numero** -kenttään tili johon tekstin linkityksen sisältävät maksut kirjataan, jos ne ovat saapuvia maksuja. Saapuvien maksujen arvon merkki **Tiliotteen summa** -kentässä on positiivinen.
7. Syötä **Kredit-tilin numero** -kenttään tili johon tekstin linkityksen sisältävät maksut kirjataan, jos ne ovat lähteviä maksuja. Lähtevien maksujen arvon merkki **Tiliotteen summa** -kentässä on negatiivinen.
8. Määritä **Saldon lähteen tyyppi** -kenttään, kirjataanko maksu kirjanpitotilille vai asiakkaan tai toimittajan tilille.
9. Määritä **Saldon lähteen numero** -kenttään **Saldon lähteen tyyppi** -kentän valinnan mukaisesti tili, jolle maksu kirjataan.
10. Toista vaiheet 4-8 kaikkien niiden maksujen tekstien osalta, joille haluat yhdistää tilit suoraa kirjausta varten soveltamatta.

Seuraavan kerran, kun tuot pankin tiliotetiedoston tai valitset **Kohdista automaattisesti** -toiminnon **Maksujen täsmäytyskirjauskansio** -ikkunassa, tietyn yhdistystekstin sisältävät päiväkirjan rivit sisältävät yhdistetyt tilit **Tilityyppi**- ja **Tilinumero**-. -kentät. **Vastaavuuden luotettavuus** -kenttä sisältää **Suuri - Tekstin yhdistäminen tiliin** -tekstin. Tämä on edellytys sille, että automaattinen kohdistustoiminto antaa vastaavuudeksi **Matala** tai **Keskisuuri**.

## <a name="example-text-to-account-mapping-for-fuel-expense"></a>Esimerkki: Tekstin ja tilin yhdistäminen polttoaineen kuluun
Kirjataksesi aina Shell-huoltoasemilla kertyneet polttoainekulut kirjanpitoon polttoaineelle (tili 8510), täytä rivi **Tekstin yhdistäminen tiliin** -ikkunassa seuraavasti.

| Tekstin linkitys | Debet-tilin Nro | Kredit-tilin Nro | Saldo Lähdetyyppi | Saldo Lähteen nro |
| --- | --- | --- | --- | --- |
| Hylly |TYHJÄ |8510 |KP-tili |TYHJÄ |

> [!TIP]  
>   Lisätietoja kenttien ja sarakkeiden käsittelemisestä on ohjeaineessa [[!INCLUDE[d365fin](includes/d365fin_long_md.md)]in käyttäminen](ui-work-product.md). Lisätietoja tiettyjen sivujen löytämisestä on kohdassa [Haku](ui-search.md).

## <a name="see-also"></a>Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[Toimintaohje: Envestnet Yodlee -pankkisyötepalvelun määrittäminen](bank-how-setup-bank-statement-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

