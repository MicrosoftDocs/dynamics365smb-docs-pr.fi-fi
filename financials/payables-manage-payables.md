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
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: d59c00f7a00854639250ae587805dece50fd1d78
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="managing-payables"></a>Ostovelkojen hallinta
Keskeinen osa ostoreskontran hoitoa on toimittajille maksamista tai kulujen hyvittämistä työntekijöille. Voit lisätä toiminnoilla erääntyviin ostolaskuihin maksurivejä **Maksupäiväkirja**-ikkunassa. Voit lähettää tapahtumia pankkiin viemällä useita maksupäiväkirjan rivejä tiedostoon ja ladata sitten tiedoston pankkiin. Voit myös maksaa sekeillä ja siirtää sekkejä sähköisinä maksuina.

Toinen tavallinen tehtävä on lähtevien maksujen kohdistaminen liittyviin toimittaja- tai työntekijätapahtumiin, jotta ostolaskut, ostohyvityslaskut tai työntekijätilit voidaan sulkea maksettuina. Voit tehdä tämän **Maksujen täsmäytyskirjauskansio** -ikkunassa tuomalla pankin tiliotteen ja rekisteröimällä maksut. Maksut kohdistetaan avoimiin toimittaja-, asiakas- tai työntekijätapahtumiin täsmäyttämällä maksuteksti ja tapahtumatiedot. Täsmäytykset voi tarkistaa tai niitä voi muuttaa eri tavoilla ennen päiväkirjan kirjaamista. Voit sulkea minkä tahansa kohdistettuun tapahtumakirjaukseen liittyvän avoimen pankkitapahtuman päiväkirjan kirjaamisen yhteydessä. Pankkitili täsmäytetään automaattisesti, kun kaikki maksut on kohdistettu.

Vaihtoehtoisesti voit kohdistaa lähtevät maksut manuaalisesti **Maksupäiväkirja**-ikkunassa tai liittyvistä toimittaja- tai työntekijätapahtumista.

Seuraavassa taulukossa on ostoreskontran tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.

| Toiminta | Katso |
| --- | --- |
| Luo toimittajien maksuja tai työntekijöiden hyvityksiä, valmistele suoritettavat sekkimaksut ja vie maksut pankkitiedostoon kirjauksen yhteydessä. |[Maksujen suorittaminen](payables-make-payments.md) |
| Kohdista toimittajan maksut automaattisesti maksamattomiin ostolaskuihin tuomalla pankin tiliotetiedosto. |[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Kohdista toimittajan maksut maksamattomiin ostolaskuihin manuaalisesti. |[Toimittajamaksujen täsmäyttäminen manuaalisesti](payables-how-apply-purchase-transactions-manually.md) |
|Varmista varaston oikea arvostus määrittämällä lisätyt nimikekulut, kuten nimikkeiden ostamisessa syntyvät rahti-, käsittely-, vakuutus- ja kuljetuskulut.|[Kaupan lisäkustannusten huomiointi nimikekulujen avulla](payables-how-assign-item-charges.md)|

## <a name="see-also"></a>Katso myös
[Osto](purchasing-manage-purchasing.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Kaupan lisäkustannusten huomiointi nimikekulujen avulla](payables-how-assign-item-charges.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

## [!INCLUDE [d365fin](includes/free_trial_md.md)]  
## [!INCLUDE [d365fin](includes/training_link_md.md)]

