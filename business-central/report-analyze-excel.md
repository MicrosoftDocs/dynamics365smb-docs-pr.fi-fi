---
title: 'Raporttitietojen analysointi Excelillä ja XML:llä'
description: 'Tutustu Excelin ja XML:n käyttöön raportin tietojoukon analysoimisessa.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.date: 03/16/2022
ms.author: jswymer
---
# <a name="analyzing-report-data-with-excel-and-xml"></a><a name="analyzing-report-data-with-excel-and-xml"></a>Raporttitietojen analysointi Excelillä ja XML:llä

[!INCLUDE[2021_releasewave2](includes/2021_releasewave2.md)]

Kehittäjänä tai edistynein käyttäjänä kannattaa tarkastaa kulloistakin raportin tietojoukkoa varten luodut tiedot, kun luot uusia raportteja tai muokkaat olemassa olevia raportteja. Tämän ominaisuuden tukemiseksi voit viedä raportin tietojoukon raakatietoina Excel-työkirjaan tai XML-tiedostoon&mdash;suoraan. Tämän jälkeen voit esimerkiksi suorittaa tiedoille Excelissä ad-hoc-analyysin ja diagnosoida ongelmat.

## <a name="get-started"></a><a name="get-started"></a>Aloitus

Voit viedä tietojoukon Excel-työkirjaan tai XML-tiedostoon avaamalla raportin asiakasohjelmassa ja valitsemalla sitten pyyntösivulla **Lähetä kohteeseen** > **Microsoft Excel -asiakirja (vain tiedot)** tai **XML-asiakirja**. Tiedosto ladataan laitteellesi.

## <a name="more-about-excel-data-only"></a><a name="more-about-excel-data-only"></a>Lisätietoja Excelistä (vain tiedot)

**Microsoft Excel -asiakirja (vain tiedot)** -vaihtoehto vie raportin tulokset ja ehdot, jonka perusteella ne luotiin&mdash;mutta ei sisällä raportin asettelua. Excel-tiedosto sisältää koko tietojoukon raakatietoina riveille ja sarakkeisiin järjestettyinä. Kaikki raportin tietojoukon tietosarakkeet sisällytetään riippumatta siitä, käytetäänkö niitä raportin asettelussa.

Kun sinulla on Excel-tiedosto, voit aloittaa tietojen analysoinnin. Voit esimerkiksi suodattaa tiedot ja käyttää Power Pivotia niiden näyttämiseen.

Aina kun viet tuloksia, uusi työkirja luodaan. Käyttämällä **Microsoft Excel -asiakirja (vain tiedot)** -asetusta voit suorittaa saman raportin ja käyttää muotoilumuutoksia uudelleen. Power Pivotia varten voit esimerkiksi suorittaa raportin uudelleen toiselle ajanjaksolle, kopioida tulokset työkirjaan ja päivittää sitten työkirjan. Myös [AppSource](https://appsource.microsoft.com/) sisältää raportointisovelluksia.

> [!NOTE]
> Et voi viedä raporttia, jossa on enemmän kuin 1 048 576 riviä tai 16 384 saraketta. Kun Business Central on paikallinen, vietyjen rivien enimmäismäärä saattaa olla vielä pienempi. Business Central Server sisältää määritysasetuksen nimeltä **Exceliin lähetettävien tietorivien sallittu enimmäismäärä**, jonka tarkoitus on laskea enimmäisarvon rajaa. Katso lisätietoja kohdassa [Business Central Serverin määrittäminen](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) tai ota yhteyttä järjestelmänvalvojaan.

## <a name="for-administrators"></a><a name="for-administrators"></a>Järjestelmänvalvojille

- **Microsoft Excel Asiakirja (vain tiedot)** otettiin käyttöön valinnaisena ominaisuutena vuoden 2021 julkaisuaallossa 1, päivitys 18.3. Jos haluat antaa käyttäjille pääsyn tähän ominaisuuteen käytettäessä vuoden 2021 julkaisuaaltoa 1, ota käyttöön **Tallenna raportin tietojoukko Microsoft Excel -asiakirjaan** -ominaisuuden päivitys **Ominaisuuksien hallinnassa**. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management). Vuoden 2021 julkaisuaallossa 2 tästä ominaisuudesta tuli pysyvä, joten sinun ei tarvitse ottaa sitä käyttöön.

- Valinnan **Microsoft Excel -asiakirja (vain tiedot)** käyttämiseen käyttäjätili tarvitsee luvan **Salli raportin tietojoukon vientitoiminto Exceliin**. Tämä lupa voidaan antaa käyttäjille määrittämällä heille joko käyttöoikeusjoukko **Vianetsintätyökalut** tai **Vie raportti Exceliin**. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md)  

## <a name="for-developers-and-advanced-users"></a><a name="for-developers-and-advanced-users"></a>Kehittäjille ja kokeneille käyttäjille

**Microsoft Excel -asiakirja (vain tiedot)** -asetus vie kaikki sarakkeet, mukaan lukien sarakkeet, joissa on suodattimia tai muotoiluohjeita muita arvoja varten. Tässä muutamia kiinnostavia kohtia:

- Kentän binaaritietoja, kuten kuvaa, ei viedä.

  Binaaritietoja sisältävissä sarakkeissa kenttiin tulee teksti **Binaaritiedot ({0} tavua)**, jossa **{0}** ilmaisee tavujen määrän.
- Business Central 2021:n julkaisuaallosta 2 alkaen Excel-tiedosto sisältää myös **Raportin metatiedot** -työkirjan.

  Tämä työkirja näyttää suodattimet, joita on sovellettu raporttiin ja raportin yleisiin ominaisuuksiin, kuten nimeen, tunnisteeseen ja laajennustietoihin. Suodattimet näkyvät **Suodatin (DataItem::Table::FilterGroupNo::FieldName)** -sarakkeessa. Tämän sarakkeen suodattimet sisältävät raportin pyyntösivulle määritettyjä suodattimia. Se sisältää myös AL-koodissa, esimerkiksi [DataItemLink -ominaisuutta](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) ja [DataItemTableView -ominaisuutta](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property) käyttäen määritettyjä suodattimia.

Lisätietoja raportin rakenteesta on kohdassa [Raportin yleiskatsaus](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Raporttien käyttö](ui-work-report.md)  
[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
[Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
