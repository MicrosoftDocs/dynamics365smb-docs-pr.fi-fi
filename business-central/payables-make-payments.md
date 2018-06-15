---
title: "Toimittajille suoritettavien maksujen hallintatehtävien yleiskatsaus| Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan toimittajille tai luotonantajille suoritettavien maksujen hallintatehtävistä, kuten maksurivien kirjaamisesta ja erääntyvän saldon yleiskatsauksen hakemisesta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/26/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 6b912e8f54fd0e3fb4ac4a1eee3c376c209ffe65
ms.contentlocale: fi-fi
ms.lasthandoff: 04/26/2018

---
# <a name="making-payments"></a>Maksujen suorittaminen
Kun suoritat maksut toimittajille tai hyvityksiä työntekijöille, kirjaat liittyvät maksurivit **Maksupäiväkirja**-ikkunaan. Voit etsiä toimittajien erääntyvät maksut **Ehdota toimittajamaksuja** -eräajon avulla. Voit hakea myös toimittajien erääntyvien maksujen yhteenvedon käyttämällä **Toimittaja - Eräänt.yht.veto** -raporttia.

Maksupäiväkirjassa voit tulostaa tietokonesekkejä tai kirjata käsin kirjoitettuja sekkejä. Jos valitset **Tietokonesekki**-vaihtoehdon **Pankkimaksun tyyppi** -kenttään, sekkejä edustavat rivit on tulostettava, ennen kuin maksupäiväkirja voidaan kirjata.

Kun maksut kirjataan, voit viedä ne pankkitiedostoon, jolloin ne voidaan ladata verkkopankkiisi käsittelyä varten.

Kun maksut on tehty pankkiin, kohdista ne liittyviin avoimiin toimittaja- tai työntekijätapahtumiin. Voit tehdä sen manuaalisesti tai tuomalla pankin tiliotetiedoston ja kohdistamalla maksut automaattisesti. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.

| Vastaanottaja | Katso |
| --- | --- |
|Ymmärrä yleiseen päiväkirjaan perustuvan **Maksupäiväkirja**-ikkunan perustoiminnot, joiden avulla voit valmistella kirjaavasi maksut toimittajille tai työntekijöille.|[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)|
|Kirjaa maksut toimittajille ja hyvitykset asiakkaille ja valinnaisesti kohdista maksut liittyviin maksamattomiin laskuihin/hyvityslaskuihin sulkeaksesi ne maksetuiksi.|[Maksujen ja hyvitysten kirjaaminen](payables-how-post-payments-refunds.md)|
| Käytä **Maksupäiväkirja**-ikkunan toimintoa ehdottaaksesi toimittajan maksuja valittujen ehtojen, kuten eräpäivän, alennuskelpoisuuden ja maksuvalmiutesi, mukaan. |[Ehdota toimittajamaksuja](payables-how-suggest-vendor-payments.md) |
| Myönnä sekkejä toimittajan maksuille tai asiakkaan hyvityksille joko tulosteina tai tietokonesekkeinä. Mitätöi sekit ennen kirjaamista tai sen jälkeen. |[Sekkimaksujen suorittaminen](payables-how-work-checks.md) |
|Suorita sähköisiä maksuja viemällä maksut pankkitiedostoon, joka ladataan pankkiin käsiteltäväksi. Tämä tiedosto voi olla Pohjois-Amerikassa myös sähköinen rahansiirtotiedosto (EFT). |[Sähköisten maksujen suorittaminen](payables-how-export-payments-bank-file.md)|
|Suorita sähköiset maksut EU:n SEPA-tilisiirtostandardin mukaisesti.|[Maksujen suorittaminen pankkitietojen muunnospalvelulla tai SEPA-tilisiirrolla](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Maksaa toimittajalle käteisellä tai sekillä ja kirjaa maksu, kun lasku kirjataan. |[Ostolaskujen selvittäminen viipymättä](finance-how-to-settle-purchase-invoices-promptly.md) |
|Hyvitä työntekijöiden liiketoimintaan liittyvät henkilökohtaiset kulut suorittamalla maksu työntekijän pankkitilille.|[Työntekijöiden kulujen kirjaaminen ja hyvittäminen](finance-how-record-reimburse-employee-expenses.md)|
| Varmista lähettämällä toimittaja-, sekki- ja maksutiedot sisältävä tiedosto, että pankki vahvistaa vain tarkistetut sekit ja summat. |[Positive Pay -tiedoston vienti](finance-how-positive-pay.md) |

## <a name="see-also"></a>Katso myös
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

