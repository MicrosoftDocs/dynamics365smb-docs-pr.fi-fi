---
title: 'Toimintaohje: Nimikekustannusten muokkaaminen manuaalisesti| Microsoft Docs'
description: 'Toimintaohje: Nimikekustannusten muokkaaminen'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 00b5ac40bd0d3df346618b57173df67daba6c7fc
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>Toimintaohje: Nimikekustannusten muokkaaminen manuaalisesti
Nimikekustannus (varastoarvo) voi muuttua, kun ostat nimikkeen ja myyt sen myöhemmin, koska rahtikulut lisätään ostohintaan nimikkeen myynnin jälkeen. Kustannusten muuttamisella on merkitystä etenkin tilanteissa, jossa tavaroita myydään ennen tavaroiden oston laskuttamista. Jotta oikea varastoarvo on tiedossa, nimikekustannukset on mukautettava säännöllisesti. Näin varmistetaan, että tuottotilastot ovat ajan tasalla ja talouden avaintunnusluvut ovat oikein.

[!INCLUDE[d365fin](includes/d365fin_md.md)]issa nimikkeiden kustannuksia muutetaan automaattisesti aina varastotapahtuman yhteydessä, kuten kirjattaessa nimikkeen ostolaskua.

Toiminnolla voi myös muuttaa manuaalisesti vähintään yhden nimikkeen kustannuksia. Tämä on kätevää esimerkiksi silloin, kun tiedät, että nimikkeen kustannukset ovat muuttuneet jonkin muun syyn kuin nimiketapahtuman vuoksi.

**Huomautus**: Nimikekustannukset oikaistaan vain FIFO-arvostusmenetelmän avulla. Tämä tarkoittaa sitä, että nimikkeen yksikkökustannus on nimikkeen minkä tahansa vastaanoton todellinen arvo ja varaston arvostuksessa oletetaan, että varastoon ensimmäisenä asetetut nimikkeet myydään ensimmäisinä.

Kustannusten muuttamistoiminto käsittelee vain arvotapahtumia, joita ei ole vielä muutettu. Jos toiminto kohtaa tilanteen, jossa muutetut saapuvat kustannukset on siirrettävä niihin liittyviin lähteviin tapahtumiin, luodaan uusia muutosarvotapahtumia, jotka perustuvat alkuperäisten arvotapahtumien tietoihin, mutta sisältävät muutossumman. Kustannusten muuttamistoiminto käyttää muutostapahtumassa alkuperäisen arvotapahtuman kirjauspäivämäärää, ellei päivämäärä ole suljetulla varastokaudella. Siinä tapauksessa ohjelma käyttää seuraavan avoimen varastokauden aloituspäivämäärää. Jos varastokausia ei käytetä, **Pääkirjanpidon asetukset** -ikkunan **Ensimm. sallittu kirjauspvm** -kentässä oleva päivämäärä määrittää, milloin muutostapahtuma kirjataan.

Kaupasta johtuvat varastoarvon muutokset täsmäytetään automaattisesti talouskirjojen kanssa nimiketapahtumia kirjattaessa. Lisätietoja on kohdassa [Lisäasetukset: Varaston täsmäytys](advanced-inventory-reconciliation.md).

## <a name="to-adjust-item-costs-manually"></a>Nimikekustannusten muokkaaminen manuaalisesti
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Muuta kustannuksia - Nimiketapahtumat** ja valitse sitten liittyvä linkki.
2. Määritä **Muuta kustannuksia - Nimiketapahtumat** -ikkunassa nimikkeet, joiden kustannuksia muutetaan.
3. Valitse **OK**-painike.

## <a name="see-also"></a>Katso myös
[Lisäasetukset: Varaston täsmäytys](advanced-inventory-reconciliation.md)  
[Varasto](inventory-manage-inventory.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

