---
title: "Ostovelkojen hallintatehtävien yleiskatsaus| Microsoft Docs"
description: "Tässä ohjeaiheessa käsitellään ostovelkojen hallintaan liittyviä tehtäviä, kuten maksamista velkojille tai laskujen tai hyvityslaskujen sulkemista kohdistamalla lähtevät maksut tapahtumiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9684a91268927a4f1f4d249fef019c8f6ac00325
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="managing-payables"></a>Ostovelkojen hallinta
Keskeinen osa ostoreskontraa on toimittajien maksaminen. Voit lisätä toiminnoilla erääntyviin ostolaskuihin maksurivejä **Maksupäiväkirja**-ikkunassa. Voit lähettää tapahtumia pankkiin viemällä useita maksupäiväkirjan rivejä tiedostoon ja ladata sitten tiedoston pankkiin. Voit myös maksaa sekeillä ja siirtää sekkejä sähköisinä maksuina.

Toinen tavallinen tehtävä on lähtevien maksujen kohdistaminen liittyviin toimittajatapahtumiin, jotta liittyvät ostolaskut tai ostohyvityslaskut voidaan sulkea maksettuina. Voit tehdä tämän **Maksujen täsmäytyskirjauskansio** -ikkunassa tuomalla pankin tiliotteen ja rekisteröimällä maksut. Maksut kohdistetaan avoimiin toimittaja- tai asiakastapahtumiin täsmäyttämällä maksuteksti ja tapahtumatiedot. Täsmäytykset voi tarkistaa tai niitä voi muuttaa eri tavoilla ennen päiväkirjan kirjaamista. Voit sulkea minkä tahansa kohdistettuun tapahtumakirjaukseen liittyvän avoimen pankkitapahtuman päiväkirjan kirjaamisen yhteydessä. Pankkitili täsmäytetään automaattisesti, kun kaikki maksut on kohdistettu.

Vaihtoehtoisesti voit kohdistaa lähtevät maksut manuaalisesti **Maksupäiväkirja**-ikkunassa tai liittyvistä toimittajatapahtumista.

Seuraavassa taulukossa on ostoreskontran tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.

| Toiminta | Katso |
| --- | --- |
| Luo erääntyvät toimittajan maksut, jotka on priorisoitu maksualennusten ja erääntymismaksujen mukaan. Vaihtoehtoisesti voit viedä maksut pankkitiedostoon kirjaamisen yhteydessä. |[Maksujen suorittaminen](payables-make-payments.md) |
| Kohdista toimittajan maksut automaattisesti maksamattomiin ostolaskuihin tuomalla pankin tiliotetiedosto. |[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Kohdista toimittajan maksut maksamattomiin ostolaskuihin manuaalisesti. |[Toimintaohje: Toimittajamaksujen täsmäyttäminen manuaalisesti](payables-how-apply-purchase-transactions-manually.md) |
|Varmista varaston oikea arvostus määrittämällä lisätyt nimikekulut, kuten nimikkeiden ostamisessa syntyvät rahti-, käsittely-, vakuutus- ja kuljetuskulut.|[Toimintaohje: Kaupan lisäkustannusten huomiointi nimikekulujen avulla](payables-how-assign-item-charges.md)|

## <a name="see-also"></a>Katso myös
[Osto](purchasing-manage-purchasing.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Toimintaohje: Kaupan lisäkustannusten huomiointi nimikekulujen avulla](payables-how-assign-item-charges.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

