---
title: "Tallennettujen asetusten käyttäminen raporteissa ja niiden muokkaaminen | Microsoft Docs"
description: "Ohjeaiheessa kerrotaan ennalta määritetyistä asetuksista ja suodattimista, joilla raportti mukautetaan ja luodaan oikeita tietoja."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9e5f7417579a5ba0629032cf9fa664e0060b9cbf
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="saved-settings-on-reports"></a>Raporttien tallennetut asetukset
Ajetusta raportista riippuen näkyviin voi tulla sivu, jolla voi määrittää tietyt luodun raportin tietojen muuttamisessa tarvittavat asetukset ja suodattimet. Sivua kutsutaan raporttipyyntösivuksi. Raportti voi sisältää vähintään yhdet *tallennetut asetukset*, joita voidaan käyttää pyyntösivun raportissa. *Tallennetut asetukset* ovat periaatteessa ennalta määritettyjä asetuksia ja suodattimia. Tallennettujen asetusten käyttäminen on nopea ja helppo tapa oikeiden tietojen sisältämien raporttien luomista varten.

Voit tarkastella raportin käytettävissä olevia tallennettuja asetuksia raporttipyyntösivun **Tallennetut asetukset** -osassa.  

## <a name="to-apply-saved-settings-to-a-report"></a>Tallennettujen asetusten käyttäminen raportissa
1. Avaa raportti.

   Näkyviin tulee raporttipyyntösivu.    
2. Määritä sivun **Tallennetut asetukset** -osan **Nimi**-kenttään ne tallennetut asetukset, joita haluat käyttää.

   **Tallennetut asetukset** -osa näkyy vain, jos raportti on suoritettu aiemmin tai jos asetukset on tallennettu aiemmin. **Viimeksi käytetyt asetukset ja suodattimet** -kirjaus on aina saatavilla. Nämä asetukset ovat valinnan ja suodattimen arvot, joita käytettiin viimeksi raportin ajon yhteydessä.

## <a name="administer-saved-report-settings-for-users"></a>Käyttäjille tallennettujen raporttiasetusten hallinta
Jos sinulla on tarvittavat oikeudet, voit tarkastella, luoda ja muokata yrityksen kaikkien käyttäjien raporttien tallennettuja asetuksia. Voit määrittää raportin tallennetut asetukset yksittäisille käyttäjille tai yrityksen kaikille käyttäjille.

Voit hallita tallennettuja asetuksia sivun 1506 **Raporttien asetukset** -kohdassa. Avaa tämä sivu valitsemalla ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoittamalla **Raportin asetukset** ja valitsemalla sitten aiheeseen liittyvä linkki.

**Raporttiasetukset**-sivulla voit luoda uudet asetukset alusta alkaen tai kopioida aiemmin määritetyt asetukset ja muokata niitä. Voit muokata asetusten valintoja ja suodattimia valitsemalla **Muokkaa**-toiminnon.

**Huomautukset:**

* Raporttien tallennettujen asetusten ominaisuus on käytettävissä vain, kun pyyntösivun SaveValues-ominaisuuden arvoksi on määritetty Kyllä. SaveValues-ominaisuuden ominaisuus määritetään kehitysympäristössä.
* Jos luot tallennetut asetukset kaikille käyttäjille, ja niillä on sama nimi kuin tietyn käyttäjän aiemmin tallennetuilla asetuksilla, käyttäjä ei voi käyttää kaikille tarkoitettua asetusjoukkoa.  Käyttäjä näkee raportin pyyntösivun Tallennetut asetukset -kentässä kaksi tallennettujen asetusten vaihtoehtoa, joilla on sama nimi. Valitusta vaihtoehdosta riippumatta järjestelmä käyttää käyttäjän omia asetuksia.

## <a name="see-also"></a>Katso myös
[Suoritettavan raportin aikatauluttaminen](ui-schedule-report.md)  

