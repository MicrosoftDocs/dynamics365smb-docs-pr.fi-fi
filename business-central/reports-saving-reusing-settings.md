---
title: Raporttien ja erätöiden tallennettujen asetusten hallinta
description: Kuvaa kuinka järjestelmänvalvoja voi määrittää raportin esimääritettyjä vaihtoehtoja ja suodattimia sekä jakaa kyseiset asetukset yhden tai kaikkien käyttäjien kanssa.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customization, personalization'
ms.date: 12/21/2021
ms.author: edupont
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs" />Raporttien ja erätöiden tallennettujen asetusten hallinta

Raportteja ajettaessa käyttäjät näkyvät yleensä sivun, jossa voi valita asetuksia ja määrittää suodattimia, joita tarvitaan luotuun raporttiin sisältyvien tietojen muuttamiseen. Sivua kutsutaan *pyyntösivuksi*. Raportti voi sisältää vähintään yhdet *tallennetut asetukset*, joita voidaan käyttää pyyntösivun raportissa. *Tallennetut asetukset* ovat periaatteessa ennalta määritettyjä asetuksia ja suodattimia. Tallennettujen asetusten käyttäminen on nopea ja helppo tapa oikeiden tietojen sisältämien raporttien luomista varten. Lisätietoja on kohdassa [Tallennettujen asetusten käyttäminen](ui-work-report.md#SavedSettings).

> [!NOTE]
> Tässä ohjeaiheessa viitataan pääsiassa *raportteihin*, mutta vastaavat tiedot koskevat myös *erätöitä*.

Jos sinulla on tarvittavat oikeudet, voit tarkastella, luoda ja muokata yrityksen kaikkien käyttäjien kaikkien raporttien tallennettuja asetuksia. Voit määrittää raportin tallennetut asetukset yksittäisille käyttäjille tai yrityksen kaikille käyttäjille.

## <a name="manage-saved-settings" />Tallennettujen asetusten hallinta

Voit hallita tallennettuja asetuksia **Raporttien asetukset** -sivulla. Sivun voi avata kahdella tavalla:

- Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raportin asetukset** ja valitse sitten vastaava linkki.
- Valitse raportin pyyntösivulla **Käytä oletusarvoja kohteesta** -kentän haku ja valitse sitten **Valitse koko luettelosta** -toiminto.

    Tämä kenttä näkyy vain, jos olet suorittanut raportin vähintään kerran aiemmin. Luettelossa näkyvät vain asetukset, jotka ovat käytettävissäsi, koska ne ovat omia asetuksiasi tai koska asetukset on jaettu kanssasi.

**Raporttiasetukset** -sivulla näkyvät kaikkien käyttäjien kaikki aiemmin tallennetut asetukset. Jos **Määritetty kohteelle** -kentässä on käyttäjänimi, vain kyseinen käyttäjä voi käyttää liittyvään raporttiin tallennettuja asetuksia. Jos **Jaettu kaikille käyttäjille** -kentässä on valintamerkki, kaikki käyttäjät voivat käyttää raportin tallennettuja asetuksia.  

> [!TIP]
> Kun käyttäjä on suorittanut raportin, joka tukee jaettuja asetuksia, hänen asetuksensa tallennetaan ja lisätään tähän luetteloon. Useimmissa tapauksissa järjestelmänvalvoja voi muokata asetuksia ja jakaa asetukset kaikkien käyttäjien kanssa.
>
> Joissakin tapauksissa asetuksia ei kuitenkaan voi jakaa, eikä järjestelmänvalvoja voi muuttaa niitä. Useimmat erätyöt eivät tue jaettuja asetuksia.  

## <a name="create-or-modify-saved-settings-for-all-users" />Kaikkien käyttäjien tallennettujen asetusten luominen tai muokkaaminen

**Raporttiasetukset** -sivulla voit:

- luoda täysin uuden asetuksen tallennustapahtuman valitsemalla **Uusi**-toiminnon
- valitse tallennettujen asetusten tapahtuman luettelosta ja luoda kopion valitsemalla **Kopioi**-toiminnon
- valita asetusten tallennustapahtuman luettelosta ja muokata asetusten tallennustapahtumaa valitsemalla **Muokkaa**-toiminnon

> [!Important]
> Harkita minkä nimen annat tallennettujen asetusten merkinnälle. Jos luot tallennettujen asetusten merkinnän kaikille käyttäjille, ja annat sille saman nimen kuin tietyn käyttäjän aiemmin tallennetuilla merkinnöillä, jotka on määritelty vain tietylle käyttäjälle, kyseinen käyttäjä ei voi käyttää kaikille tarkoitettua asetusmerkintäjoukkoa.  Käyttäjä näkee **Tallennetut asetukset** -osassa kaksi asetusten tallennustapahtumaa, jolla on sama nimi. Valitusta vaihtoehdosta riippumatta järjestelmä käyttää käyttäjän omaa asetusten tallennustapahtumaa.

> [!NOTE]
> Tallennetut asetukset -mahdollisuus on käytössä vain raporteissa, joissa raportin pyyntösivun [SaveValues-ominaisuudeksi](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) on määritetty **Kyllä**. Kehittäjä määrittää **SaveValues** -ominaisuuden.  

## <a name="see-also" />Katso myös

[Raporttien, eräajojen ja XMLportien käsitteleminen](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
