---
title: Nimikekustannusten muokkaaminen manuaalisesti| Microsoft Docs
description: "Voit muuttaa nimikkeen varastonarvostusta FIFO- tai Keskiarvo-arvostusmenetelmällä, esimerkiksi silloin, kun nimikkeen kustannusten muutoksen syynä on jokin muu kuin tapahtuma."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a1f682b60b7b9ae402c27093f13aa3db2368ed5b
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>Toimintaohje: Nimikekustannusten muokkaaminen manuaalisesti
Nimikekustannus (varastoarvo) voi muuttua, kun ostat nimikkeen ja myyt sen myöhemmin, koska rahtikulut lisätään ostohintaan nimikkeen myynnin jälkeen. Kustannusten muuttamisella on merkitystä etenkin tilanteissa, jossa tavaroita myydään ennen tavaroiden oston laskuttamista. Jotta oikea varastoarvo on tiedossa, nimikekustannukset on mukautettava säännöllisesti. Näin varmistetaan, että tuottotilastot ovat ajan tasalla ja talouden avaintunnusluvut ovat oikein.

[!INCLUDE[d365fin](includes/d365fin_md.md)]issa nimikkeiden kustannuksia muutetaan automaattisesti aina varastotapahtuman yhteydessä, kuten kirjattaessa nimikkeen ostolaskua.

Toiminnolla voi myös muuttaa manuaalisesti vähintään yhden nimikkeen kustannuksia. Tämä on kätevää esimerkiksi silloin, kun tiedät, että nimikkeen kustannukset ovat muuttuneet jonkin muun syyn kuin nimiketapahtuman vuoksi.

Nimikkeen kustannuksia muutetaan FIFO- tai Keskiarvo-arvostusmenetelmälla ohjatussa **Määritä oma yritys** -asetusten määrityksessä tehdyn valinnan mukaan. Lisätietoja on kohdassa [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).  

Jos käytössä on FIFO-arvostusmenetelmä, nimikkeen yksikkökustannus on nimikkeen vastaanoton todellinen arvo. Varastonarvostuksessa käytetään oletusta, että ensin varastoon sijoitetut nimikkeet myydään ensin.

Jos käytät Keskiarvo-arvostusmenetelmää, nimikkeen yksikkökustannus lasketaan kussakin vaiheessa keskimääräisenä yksikkökustannuksena oston jälkeen. Varastonarvostus olettaa, että kaikki vaihto-omaisuus myydään samanaikaisesti.

Kustannusten muuttamistoiminto käsittelee vain arvotapahtumia, joita ei ole vielä muutettu. Jos toiminto kohtaa tilanteen, jossa muutetut saapuvat kustannukset on siirrettävä niihin liittyviin lähteviin tapahtumiin, luodaan uusia muutosarvotapahtumia, jotka perustuvat alkuperäisten arvotapahtumien tietoihin, mutta sisältävät muutossumman. Kustannusten muuttamistoiminto käyttää muutostapahtumassa alkuperäisen arvotapahtuman kirjauspäivämäärää, ellei päivämäärä ole suljetulla varastokaudella. Siinä tapauksessa ohjelma käyttää seuraavan avoimen varastokauden aloituspäivämäärää. Jos varastokausia ei käytetä, **Pääkirjanpidon asetukset** -ikkunan **Ensimm. sallittu kirjauspvm** -kentässä oleva päivämäärä määrittää, milloin muutostapahtuma kirjataan.

Kaupasta johtuvat varastoarvon muutokset täsmäytetään automaattisesti talouskirjojen kanssa nimiketapahtumia kirjattaessa. Lisätietoja on ohjeaiheen [Varasto](inventory-manage-inventory.md) kohdassa Varaston täsmäytys.

## <a name="to-adjust-item-costs-manually"></a>Nimikekustannusten muokkaaminen manuaalisesti
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Muuta kustannuksia - Nimiketapahtumat** ja valitse sitten aiheeseen liittyvä linkki.
2. Määritä **Muuta kustannuksia - Nimiketapahtumat** -ikkunassa nimikkeet, joiden kustannuksia muutetaan.
3. Valitse **OK**-painike.

## <a name="see-also"></a>Katso myös
[Varasto](inventory-manage-inventory.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

