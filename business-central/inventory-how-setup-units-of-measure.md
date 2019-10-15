---
title: Nimikkeen mittayksikön määrittäminen| Microsoft Docs
description: Voit määrittää nimikkeelle useita mittayksiköitä, joten voit kohdistaa mittayksiköt nimikkeeseen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 10/01/2019
ms.author: SorenGP
ms.openlocfilehash: 672ddb851b14accf4df3f88bbc0badd775319a68
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309794"
---
# <a name="set-up-item-units-of-measure"></a>Nimikkeen mittayksikön määrittäminen
Voit määrittää useita mittayksiköitä, jotka on määritetty kohteelle niin, että voit kohdistaa nimikkeen mittayksiköt seuraaviin tarkoituksiin:

- Määritä perusmittayksikkö nimikkeen nimikekortilla määrittämään, miten se tallennetaan varastoon. Perusmittayksikkö toimii myös muuntamisen perustana vaihtoehtoisille mittayksiköille.
- Määritä vaihtoehtoiset mittayksiköt osto-, tuotanto- tai myyntiasiakirjojoille määrittääksesi, kuinka monta perusmittayksikön yksikköä käsittelet kerrallaan kyseisissä prosesseissa. Voi esimerkiksi ostaa nimikkeen kuormalavoihin ja käyttää tuotannossa vain yksittäisiä kappaleita.

Jos nimike varastoidaan yhtä mittayksikköä ja tuotetaan toista mittayksikköä käyttäen, ohjelma voi laskea komponenttien oikean määrän **Päivitä tuotantotilaus** -eräajon aikana luomalla tuotantoerän mittayksikköä käyttävän tuotantotilauksen. Tuotantoerän mittayksikön laskentaa voidaan tarvita esimerkiksi, kun nimike varastoidaan kappaleina mutta tuotetaan tonneina. Lisätietoja on kohdassa [Tuotantoerän mittayksiköiden käyttäminen](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).

## <a name="to-set-up-a-unit-of-measure"></a>Mittayksikön määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa nimikkeen kortti, jolle haluat määrittää vaihtoehtoisen mittayksikön.
3. Valitse **Mittayksiköt**-toiminto. Näyttöön tulee **Nimikkeen mittayksiköt** -sivu.
4. Jos nimikekortin **Perusmittayksikkö**-kenttä on täytetty, kyseinen mittayksikkö on jo määritetty.
5. Valitse **Uusi**-toiminto. Uusi tyhjä rivi lisätään.
6. Syötä mittayksikön nimi **Koodi**-kentässä. Vaihtoehtoisesti voit valita kenttään tietokannassa olevat mittayksikön koodit.
7. Määritä **Määrä mittayksikköä kohti** -kentässä, kuinka monta perusmittayksikön yksikköä uusi mittayksikkö sisältää.
8. Toista vaiheet 5-7 määrittääksesi kaikki vaihtoehtoiset mittayksiköt, joita haluat käyttää tälle nimikkeelle eri prosesseissa.

Voit nyt käyttää vaihtoehtoisia mittayksiköitä osto-, tuotanto- ja myyntiasiakirjoissa. Lisätietoja on kohdassa Oletusmittayksiköiden koodien antaminen osto- ja myyntitapahtumille tai Tuotantoerän mittayksikön käyttäminen.

## <a name="to-set-up-unit-of-measure-translations"></a>Mittayksikön käännösten määrittäminen
Kun myyt nimikkeitä ulkomaisille asiakkaille, voit haluta määrittää mittayksikön asiakkaan kielellä. Tällä tavalla voi tehdä sen jälkeen kun tarpeelliset mittayksiköiden käännökset on määritetty.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Mittayksikkö** ja valitse sitten liittyvä linkki.
2. Valitse koodi, jonka käännökset haluat määrittää, ja valitse sitten **Käännökset** -toiminto.
3. Valitse **Kielikoodi**-kentässä alanuolipainike, jolloin näyttöön tulee luettelo saatavilla olevista kielikoodeista. Valitse kielikoodi, jolle haluat syöttää käännöksen, ja kopioi sitten koodi kenttään valitsemalla OK.
4. Syötä **Kuvaus**-kenttään asianmukainen teksti.
5. Toista vaiheet 2–4 niiden mittayksikön koodien ja kielien osalta, joille haluat antaa käännöksen.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Oletusmittayksikön koodien määrittäminen myynti- ja ostotapahtumille
Jos ostat tai myyt tavallisesti eri yksiköissä kuin perusmittayksiköissä, voit määrittää erillisiä mittayksiköitä ostoille ja myynneille. Tehdäksesi näin **Nimikkeen mittayksiköt** -sivulla tulee määrittää mittayksiköitä.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa sen nimikkeen kortti, jolle haluat määrittää myynnin tai oston oletusmittayksikön koodin.
3. Avaa myynnin osalta **Laskutus**-pikavälilehden **Myynnin mittayksikkö** -kentässä **Nimikkeen mittayksiköt** -sivu.
4. Avaa oston osalta **Täydennys**-pikavälilehden **Oston mittayksikkö** -kentässä **Nimikkeen mittayksiköt** -sivu.
5. Valitse myynnin tai oston oletusmittayksiköksi määritettävä koodi ja valitse sitten **OK**.

## <a name="see-also"></a>Katso myös
[Tuotantoerän mittayksiköiden käyttäminen](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Varaston hallinta](inventory-manage-inventory.md)  
[Ostojen hallinta](purchasing-manage-purchasing.md)  
[Myynnin hallinta](sales-manage-sales.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
