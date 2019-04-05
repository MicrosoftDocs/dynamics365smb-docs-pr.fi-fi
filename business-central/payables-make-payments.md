---
title: Toimittajille suoritettavien maksujen hallintatehtävien yleiskatsaus| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan toimittajille tai luotonantajille suoritettavien maksujen hallintatehtävistä, kuten maksurivien kirjaamisesta ja erääntyvän saldon yleiskatsauksen hakemisesta.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 02/08/2019
ms.author: edupont
ms.openlocfilehash: f2ff92af7dbf6c751cde795d3546d90c8d76a62b
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795289"
---
# <a name="making-payments"></a>Maksujen suorittaminen

Kun suoritat maksut toimittajille tai asiakkaille tai hyvityksiä työntekijöille, kirjaat liittyvät maksurivit **Maksupäiväkirja**-sivulle. Maksukirjauskansio on yleinen kirjauskansio, joka on tarkoitettu maksujen tekemiseen. Se sisältää useita tehokkaita toimintoja, kuten **Ehdota toimittajamaksuja** -toiminnon, joka etsii toimittajat, joilla on erääntyneitä maksuja, ja **Toimittaja - Eräänt.yht.veto** -raportin, joka näyttää toimittajan erääntyneiden maksujen yleiskatsauksen.  

Voit aloittaa maksujen luomisprosessin toimittajille, asiakkaille ja työntekijöille luetteloista, korteista ja tapahtumista. Jokaisella sivulla on painike, joka aloittaa maksuprosessin ja auttaa täyttämään maksukirjauskansion.  

Maksupäiväkirjassa voit tulostaa tietokonesekkejä tai kirjata käsin kirjoitettuja sekkejä. Jos valitset **Tietokonesekki**-vaihtoehdon **Pankkimaksun tyyppi** -kenttään, sekkejä edustavat rivit on tulostettava, ennen kuin maksupäiväkirja voidaan kirjata.

Kun maksut kirjataan, voit viedä ne pankkitiedostoon, jolloin ne voidaan ladata verkkopankkiisi käsittelyä varten.

Kun maksut on tehty pankkiin, kohdista ne liittyviin avoimiin toimittaja- tai työntekijätapahtumiin. Voit tehdä sen manuaalisesti tai tuomalla pankin tiliotetiedoston ja kohdistamalla maksut automaattisesti. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.

| Vastaanottaja | Katso |
| --- | --- |
|Ymmärrä yleiseen päiväkirjaan perustuvan **Maksupäiväkirja**-sivun perustoiminnot, joiden avulla voit valmistella kirjaavasi maksut toimittajille tai työntekijöille.|[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)|
|Kirjaa maksut toimittajille tai työntekijöille ja hyvitykset asiakkaille. Valinnaisesti voit kohdistaa maksut liittyviin maksamattomiin laskuihin/hyvityslaskuihin ja sulkea ne maksettuina.|[Maksujen ja hyvitysten kirjaaminen](payables-how-post-payments-refunds.md)|
| Käytä **Maksupäiväkirja**-sivun toimintoa ehdottaaksesi toimittajan maksuja valittujen ehtojen, kuten eräpäivän, alennuskelpoisuuden ja maksuvalmiutesi, mukaan. |[Ehdota toimittajamaksuja](payables-how-suggest-vendor-payments.md) |
| Myönnä sekkejä toimittajan maksuille tai asiakkaan hyvityksille joko tulosteina tai tietokonesekkeinä. Mitätöi sekit ennen kirjaamista tai sen jälkeen. |[Sekkimaksujen suorittaminen](payables-how-work-checks.md) |
|Suorita sähköisiä maksuja viemällä maksut pankkitiedostoon, joka ladataan pankkiin käsiteltäväksi. Tämä tiedosto voi olla Pohjois-Amerikassa myös sähköinen rahansiirtotiedosto (EFT). |[Sähköisten maksujen suorittaminen](payables-how-export-payments-bank-file.md)|
|Suorita sähköiset maksut EU:n SEPA-tilisiirtostandardin mukaisesti.|[Maksujen suorittaminen pankkitietojen muunnospalvelulla tai SEPA-tilisiirrolla](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Maksaa toimittajalle käteisellä tai sekillä ja kirjaa maksu, kun lasku kirjataan. |[Ostolaskujen selvittäminen viipymättä](finance-how-to-settle-purchase-invoices-promptly.md) |
| Varmista lähettämällä toimittaja-, sekki- ja maksutiedot sisältävä tiedosto, että pankki vahvistaa vain tarkistetut sekit ja summat. |[Positive Pay -tiedoston vienti](finance-how-positive-pay.md) |

## <a name="see-also"></a>Katso myös
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
