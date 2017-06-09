---
title: Ostovelkojen hallinta| Microsoft Docs
description: Ostovelkojen hallinta
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 92b16c52589a07661d9ff080e9ef8a0f6be633f7
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


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

## <a name="see-also"></a>Katso myös
[Osto](purchasing-manage-purchasing.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

