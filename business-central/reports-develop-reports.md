---
title: Raporttien asettelujen ja tietojoukkojen kehittäminen
description: Antaa yleiskuvan Business Central -tiedoista.
author: kennieNP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: feature overview
ms.date: 02/03/2022
ms.author: kepontop
---

# <a name="developing-business-central-report-layouts-and-datasets" />Business Central -raporttien asettelujen ja tietojoukkojen kehittäminen

Tuotteessa [!INCLUDE[prod_short](includes/prod_short.md)] raportti koostuu raporttiobjektista, joka määrittää raportin _tietojoukon_ (mitä tietoja on käytettävissä) sekä _raporttiasettelujen_ määrän (miten tiedot esitetään).  

## <a name="developing-report-layouts" />Raporttiasettelujen kehittäminen

Haluatko muokata tuotteeseen [!INCLUDE[prod_short](includes/prod_short.md)] sisältyviä raporttiasetteluja? Asetteluun käytetyn teknologian mukaan tämä voi olla tehtävissä itse (Excel-asettelut ja ehkä myös Word-asettelut) tai siihen tarvitaan kehittäjää (pikselitarkat RDLC-asettelut).

| Tehtävä | Katso |
|--|--|
| Lisätietoja eri asettelutyypeistä (Word, Excel ja RDLC) | [Asettelutyypit (Word, Excel ja RDLC)](ui-manage-report-layouts.md) |
| Tietoja uuden raporttiasettelun luomisesta. | [Uuden asettelun luominen](ui-how-create-custom-report-layout.md) |
| Tietoja [!INCLUDE[prod_short](includes/prod_short.md)] Onlineen asennetuista fonteista, joita voi käyttää raporttiasetteluissa. | [Fonttien käyttö asettelussa](ui-fonts.md) |
| Word-asettelujen käyttö. | [Wordin asettelujen käyttö](ui-how-add-fields-word-report-layout.md) |
| Asettelutiedostojen tuonti/vienti. | [Asettelun tuonti/vienti](ui-how-import-and-export-report-layout.md) |
| Asettelumäärityksen päivittäminen tuotteessa [!INCLUDE[prod_short](includes/prod_short.md)] uudella asettelutiedostolla. | [Asettelun tuonti/vienti](ui-how-import-and-export-report-layout.md) |
| Raportin oletusasettelun muuttaminen. | [Oletusasettelun muuttaminen](ui-how-change-layout-currently-used-report.md) |
<!-- | Excel-asettelujen käyttö | [Excel-asettelujen käyttö](ui-how-add-fields-word-report-layout.md) | -->

## <a name="developing-report-datasets" />Raporttitietojoukkojen kehittäminen

 Jos haluat muuttaa tietojoukkomäärityksiä, jotka määrittävät raportissa käytettävissä olevat tiedot, tarvitset kehittäjän, joka tuntee AL-ohjelmointikielen sekä työkalut raporttiobjektien ja raporttilaajennusten kehittämiseen.

| Tehtävä | Katso |
|--|--|
| Tutustuminen raporttien ohjelmointiin AL:ssä | [Raporttien kehittämisopas](/dynamics365/business-central/dev-itpro/developer/devenv-reports) |
| Kaiken irti ottaminen raporteista | [Raporttien suorituskyvyn hienosäätöopas](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-reports) |

## <a name="see-also" />Katso myös

[Business Intelligencen ja raportoinnin yleiskuva](reports-use-reports.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
