---
title: "Toimittajille suoritettavien maksujen hallintatehtävien yleiskatsaus| Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan toimittajille tai luotonantajille suoritettavien maksujen hallintatehtävistä, kuten maksurivien kirjaamisesta ja erääntyvän saldon yleiskatsauksen hakemisesta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a>Maksujen suorittaminen
Kun suoritat maksut toimittajille, kirjaat liittyvät maksurivit **Maksupäiväkirja**-ikkunaan. **Ehdota toimittajamaksuja** -eräajon avulla voit etsiä erääntyvät maksut. Voit myös hakea erääntyvien maksujen yhteenvedon käyttämällä **Toimittaja - Eräänt.yht.veto** -raporttia.

Maksupäiväkirjassa voit tulostaa tietokonesekkejä tai kirjata käsin kirjoitettuja sekkejä. Jos valitset **Tietokonesekki**-vaihtoehdon **Pankkimaksun tyyppi** -kenttään, sekkejä edustavat rivit on tulostettava, ennen kuin maksupäiväkirja voidaan kirjata.

Kun maksut kirjataan, voit viedä ne pankkitiedostoon, jolloin ne voidaan ladata verkkopankkiisi käsittelyä varten.

Kun maksut on tehty pankkiin, kohdista ne liittyviin avoimiin toimittajatapahtumiin. Voit tehdä sen manuaalisesti tai tuomalla pankin tiliotetiedoston ja kohdistamalla maksut automaattisesti. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.

| Toiminta | Katso |
| --- | --- |
| Käytä toimintoa ehdottaaksesi toimittajan maksuja valittujen ehtojen, kuten eräpäivän, alennuskelpoisuuden ja maksuvalmiutesi, mukaan. |[Toimintaohje: Toimittajamaksujen ehdottaminen](payables-how-suggest-vendor-payments.md) |
| Myönnä sekkejä maksuille joko tulosteina tai tietokonesekkeinä. Mitätöi sekit ennen kirjaamista tai sen jälkeen. |[Toimintaohje: Sekkien käsitteleminen](payables-how-work-checks.md) |
| Varmista lähettämällä toimittaja-, sekki- ja maksutiedot sisältävä tiedosto, että pankki vahvistaa vain tarkistetut sekit ja summat. |[Toimintaohje: Positive Pay -tiedoston vieminen](finance-how-positive-pay.md) |
|Vie maksut **Maksupäiväkirja**-ikkunasta pankkitiedostoon, joka ladataan pankkiin käsiteltäväksi. Tämä tiedosto voi olla Pohjois-Amerikassa myös sähköinen rahansiirtotiedosto (EFT). |[Toimintaohje: Maksujen vieminen pankkitiedostoon](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a>Katso myös
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

