---
title: Tallennettujen asetusten käyttäminen raporteissa ja niiden muokkaaminen | Microsoft Docs
description: Ohjeaiheessa kerrotaan ennalta määritetyistä asetuksista ja suodattimista, joilla raportti mukautetaan ja luodaan oikeita tietoja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4437d723834a8189a7155d59812c8e2e1f16b933
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778920"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Raporttien ja erätöiden tallennettujen asetusten hallinta
Raportteja ajettaessa käyttäjät näkyvät yleensä sivun, jossa voi valita asetuksia ja määrittää suodattimia, joita tarvitaan luotuun raporttiin sisältyvien tietojen muuttamiseen. Sivua kutsutaan pyyntösivuksi. Raportti voi sisältää vähintään yhdet *tallennetut asetukset*, joita voidaan käyttää pyyntösivun raportissa. *Tallennetut asetukset* ovat periaatteessa ennalta määritettyjä asetuksia ja suodattimia. Tallennettujen asetusten käyttäminen on nopea ja helppo tapa oikeiden tietojen sisältämien raporttien luomista varten. Lisätietoja on kohdassa [Tallennettujen asetusten käyttäminen](ui-work-report.md#SavedSettings).

> [!NOTE]
> Tässä ohjeaiheessa viitataan pääsiassa raportteihin, mutta vastaavat tiedot koskevat myös erätöitä.

Jos sinulla on tarvittavat oikeudet, voit tarkastella, luoda ja muokata yrityksen kaikkien käyttäjien kaikkien raporttien tallennettuja asetuksia. Voit määrittää raportin tallennetut asetukset yksittäisille käyttäjille tai yrityksen kaikille käyttäjille.

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a>Kaikkien käyttäjien tallennettujen asetusten luominen ja muokkaaminen
Voit hallita tallennettuja asetuksia **Raporttien asetukset** -sivulla. Sivun voi avata kahdella tavalla:
-   Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Raporttiasetukset** ja valitse sitten liittyvä linkki.
-   Avaa raportti, valitse **Käytä oletusarvoja kohteesta:** -kentän haku ja valitse sitten **Valitse koko luettelosta** -toiminto.

Sivulla näkyvät kaikkien käyttäjien kaikki aiemmin tallennetut asetukset. Jos **Määritetty kohteelle** -kentässä on käyttäjänimi, vain kyseinen käyttäjä voi käyttää liittyvään raporttiin tallennettuja asetuksia. Jos **Jaettu kaikille käyttäjille** -kentässä on valintamerkki, kaikki käyttäjät voivat käyttää raportin tallennettuja asetuksia.

**Raporttiasetukset** -sivulla voit:
-   luoda täysin uuden asetuksen tallennustapahtuman valitsemalla **Uusi**-toiminnon
-   valitse tallennettujen asetusten tapahtuman luettelosta ja luoda kopion valitsemalla **Kopioi**-toiminnon
-   valita asetusten tallennustapahtuman luettelosta ja muokata asetusten tallennustapahtumaa valitsemalla **Muokkaa**-toiminnon

> [!Important]
> Harkita minkä nimen annat tallennettujen asetusten merkinnälle. Jos luot tallennettujen asetusten merkinnän kaikille käyttäjille, ja annat sille saman nimen kuin tietyn käyttäjän aiemmin tallennetuilla merkinnöillä, jotka on määritelty vain tietylle käyttäjälle, kyseinen käyttäjä ei voi käyttää kaikille tarkoitettua asetusmerkintäjoukkoa.  Käyttäjä näkee **Tallennetut asetukset** -osassa kaksi asetusten tallennustapahtumaa, jolla on sama nimi. Valitusta vaihtoehdosta riippumatta järjestelmä käyttää käyttäjän omaa asetusten tallennustapahtumaa.

> [!NOTE]
> Tallennetut asetukset -ominaisuus on käytössä vain raporteissa, joissa raportin pyyntösivun [SaveValues-ominaisuudeksi](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) on määritetty **Kyllä**. **SaveValues** -ominaisuus määritetään kehitysympäristössä.  

## <a name="see-also"></a>Katso myös
[Raporttien, eräajojen ja XMLportien käsitteleminen](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]