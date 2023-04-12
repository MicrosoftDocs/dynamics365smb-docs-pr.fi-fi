---
title: Tehtävien suorittaminen taustalla ja toistuvasti
description: Määritä tietojen synkronointi Business Centralin ja Shopifyn välillä taustalla.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
---

# Tehtävien suorittaminen taustalla

On tehokasta suorittaa joitakin tehtäviä samanaikaisesti ja automatisoidusti. Voit suorittaa tällaisia tehtäviä taustalla ja määrittää aikataulun myös silloin, kun haluat, että kyseiset tehtävät suoritetaan automaattisesti. Voit suorittaa tehtäviä taustalla kahdessa tilassa:

- Manuaalisesti käynnistyvät tehtävät ajoitetaan heti **Työjonon tapahtumien** avulla.
- Toistuvat tehtävät ajoitetaan **Työjonotapahtumiin**.

## Tehtävien suorittaminen taustalla tietyn myymälän osalta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kauppa** ja valitse vastaava linkki.
2. Valitse kauppa, jolle haluat suorittaa synkronoinnin taustalla avataksesi **Shopify-ostoskortti**-sivun.
3. Ota **Salli synkronointi taustalla** -valitsin käyttöön.

Nyt kun synkronointitoiminto käynnistetään, se pyytää sinua odottamaan edustalla suoritettavan tehtävän sijaan. Kun se on valmis, voit siirtyä seuraavaan toimintoon. Tehtävä luodaan **Työjonotapahtumana**, ja se alkaa heti.

## Toistuvien tehtävien ajoittaminen

Voit ajoittaa seuraavat toistuvat aktiviteetit suoritettavaksi automaattisesti. Lue lisätietoja tehtävien ajoittamisesta kohdasta [Työjonot](../admin-job-queues-schedule-tasks.md).

|Tehtävä|Objekti|
|------|------------|
|**Synkronoi tilaukset Shopifysta**|Raportti 30104 Shopifysta synkronoidut tilaukset|
|**Käsitellään Shopify-tilauksia**|Raportti 30103 Shopifylla luodut myyntitilaukset|
|**Synkronoi toimitukset Shopifyhin**|Raportti 30109 Shopifyhin synkronoidut toimitukset|
|**Synkronoi tuotteet ja/tai hinnat**|Raportti 30108 Shopifyn synkronoidut tuotteet|
|**Synkronoi varasto**|Raportti 30102 Shopifyhin synkronoidut varastot|
|**Synkronoi kuvat**|Raportti 30107 Shopifyn synkronoidut kuvat|
|**Synkronoi asiakkaat**|Raportti 30100 Shopifyn synkronoidut asiakkaat|
|**Synkronoi maksut**|Raportti 30105 Shopifyn synkronoidut maksut|

> [!NOTE]
> Useat tehtävät voivat päivittää joitakin elementtejä, esimerkiksi silloin, kun tuot tilauksia **Shopify-ostoskortin** asetuksen mukaan, järjestelmä voi myös tuoda ja päivittää asiakkaan ja/tai tuotteen tietoja. Muista käyttää samaa työjonon luokkaa ristiriitojen välttämiseksi.

Muita tehtäviä, joita voi olla hyödyllistä automatisoida myyntiasiakirjojen edelleenkäsittelyssä:

- raportti 497 Eräkirjaa ostolaskut
- raportti 496 Eräkirjaa ostotilaukset

Voit käyttää **Shopify-tilausnro**-kenttää -kentästä tuotujen Shopify-myyntiasiakirjojen yksilöimiseksi.

Saat lisätietoja myyntitilausten kirjaamisesta erään siirtymällä kohtaan [Työjonotapahtuman luonti myyntitilausten eräkirjausta varten](../ui-batch-posting.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).

## Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
