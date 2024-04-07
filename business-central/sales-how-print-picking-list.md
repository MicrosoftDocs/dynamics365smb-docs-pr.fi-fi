---
title: Varaston poimintaluettelon tulostaminen myyntitilauksesta
description: 'Voit tulostaa varaston poimintaluettelon suoraan myyntitilauksesta, myynnistä, laskusta ja muista lähtevistä myyntiasiakirjoista.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Tulosta poimintaluettelo

Voit tulostaa varaston poimintaluettelon suoraan myyntitilauksesta tai mistä tahansa muusta asiakirjasta, joka aloittaa tavaroiden lähettämisen.

Tätä raporttia käytetään tyypillisesti yrityksissä, joissa ei ole erillisiä toimintoja varastoinnin hallintaan, joten varastotyöntekijä voi tarkastella tai tulostaa poimintaluetteloa asiaan liittyvällä myyntiasiakirjalla. Yrityksissä, joiden prosessit ovat suuria tai monimutkaisia, toimitus ja poiminta suunnitellaan ja suoritetaan tietyissä varastointiasiakirjoissa. Lisätietoja on kohdassa [Fyysisen varaston lähtevä työnkulku](design-details-outbound-warehouse-flow.md).

## Varaston poimintaluettelon tulostaminen myyntitilauksesta

Seuraava toimenpide perustuu myyntitilaukseen. Vaiheet ovat samanlaiset kaikissa asiakirjoissa, joita voidaan käyttää nimikkeiden toimituksen käynnistämiseen. Yksi esimerkki on siirtotilaus.

1. Valitse ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Avaa myyntitilaus, johon haluat poimia nimikkeitä.  
3. Valitse **Raportti**-toiminto ja valitse sitten **Poimintaluettelo tilauksen mukaan**-toiminto.  
4. Valitse **Tulosta**-painike, jos haluat tulostaa poimintaluettelon, tai valitse **Esikatselu**, jos haluat katsella raporttia näytössä.

Voit myös tallentaa poimintaluettelon asiakirjana, esimerkiksi lähettääksesi sen jollekulle tai lisätäksesi sen liitteenä myyntitilaukseen. Lisätietoja on kohdassa [Korttien ja asiakirjojen liitteiden, linkkien ja muistioiden hallinta](ui-how-add-link-to-record.md).

> [!NOTE]
> Jos käytit myyntitilauksessa **Pura tuoterakenne** -toimintoa, vain asiaan liittyvän kokoonpanonimikkeen komponentit näkyvät raportissa. Lisätietoja on kohdassa [Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md).

## Katso myös

[Varasto](inventory-manage-inventory.md)  
[Lähtevien varastotyönkulku](design-details-outbound-warehouse-flow.md)
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
