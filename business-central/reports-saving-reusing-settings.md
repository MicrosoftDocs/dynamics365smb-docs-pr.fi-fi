---
title: "Tallennettujen asetusten käyttäminen raporteissa ja niiden muokkaaminen | Microsoft Docs"
description: "Ohjeaiheessa kerrotaan ennalta määritetyistä asetuksista ja suodattimista, joilla raportti mukautetaan ja luodaan oikeita tietoja."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 9fd086831c0d145570d87c33c62a003c166aca87
ms.contentlocale: fi-fi
ms.lasthandoff: 11/22/2018

---
# <a name="managing-saved-settings-on-reports"></a>Raporttien tallennettujen asetusten hallinta
Raportteja ajettaessa käyttäjä saa tyypillisesti näkyviin sivun, jolla voi määrittää tietyt luodun raportin tietojen muuttamisessa tarvittavat asetukset ja suodattimet. Sivua kutsutaan raporttipyyntösivuksi. Raportti voi sisältää vähintään yhdet *tallennetut asetukset*, joita voidaan käyttää pyyntösivun raportissa. *Tallennetut asetukset* ovat periaatteessa ennalta määritettyjä asetuksia ja suodattimia. Tallennettujen asetusten käyttäminen on nopea ja helppo tapa oikeiden tietojen sisältämien raporttien luomista varten. Lisätietoja siitä, miten tallennettuja asetuksia käytetään kohdassa [Tallennettujen asetusten käyttäminen](ui-work-report.md#SavedSettings).

Jos sinulla on tarvittavat oikeudet, voit tarkastella, luoda ja muokata yrityksen kaikkien käyttäjien raporttien tallennettuja asetuksia. Voit määrittää raportin tallennetut asetukset yksittäisille käyttäjille tai yrityksen kaikille käyttäjille.

<!-- 
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a>Kaikkien käyttäjien tallennettujen asetusten luominen ja muokkaaminen
Voit hallita tallennettuja asetuksia sivun **1560 Raporttien asetukset** -kohdassa. Sivun voi avata kahdella tavalla:
-   Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raportin asetukset** ja valitse sitten liittyvä linkki.
-   Avaa raportti, valitse haku **Käytetyt oletusarvot:** -ruudun vierestä, valitse **Valitse koko luettelosta**.

Sivulla näkyvät kaikki olemassa olevat kaikkien käyttäjien tallennusasetukset. Jos sarakkeessa **Määritetty** on käyttäjänimi, vain kyseinen käyttäjä voi käyttää liittyvään raporttiin tallennettuja asetuksia. Jos valintamerkki on **Jaa kaikkien käyttäjien kanssa** -sarakkeessa, kaikki käyttäjät voivat käyttää tallennettuja asetuksia raporttia varten.

**Raporttiasetukset** -sivulla voit:
-   Valita **Uusi** luodaksesi alusta uuden tallennetun tapahtuma-asetuksen.
-   Valita tallennettujen asetusten tapahtuman luettelosta ja valita **Kopioi** luodaksesi kopion.
-   Valita tallennettujen asetusten tapahtuman luettelosta **Muokkaa** muokataksesi tallennettujen asetusten merkintää.


> [!Important]
> Harkita minkä nimen annat tallennettujen asetusten merkinnälle. Jos luot tallennettujen asetusten merkinnän kaikille käyttäjille, ja annat sille saman nimen kuin tietyn käyttäjän aiemmin tallennetuilla merkinnöillä, jotka on määritelty vain tietylle käyttäjälle, kyseinen käyttäjä ei voi käyttää kaikille tarkoitettua asetusmerkintäjoukkoa.  Käyttäjä näkee **Tallennetut asetukset** -kentässä kaksi tallennettujen asetusten merkintää, joilla on sama nimi. Valitusta vaihtoehdosta riippumatta järjestelmä käyttää käyttäjän omia asetusmerkintöjä.

> [!NOTE]
> Raporttien tallennettujen asetusten ominaisuus on käytettävissä vain [SaveValues-ominaisuudessa](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property), joissa arvoksi on määritetty `Yes`. **SaveValues** -ominaisuus määritetään kehitysympäristössä.  

## <a name="see-also"></a>Katso myös
[Raporttien käsittely](ui-work-report.md)  

