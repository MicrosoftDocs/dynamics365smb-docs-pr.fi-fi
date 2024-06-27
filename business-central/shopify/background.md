---
title: Tehtävien suorittaminen taustalla ja toistuvasti
description: Määritä tietojen synkronointi Business Centralin ja Shopifyn välillä taustalla.
ms.date: 05/26/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
ms.custom: bap-template
---

# <a name="run-tasks-in-the-background"></a>Tehtävien suorittaminen taustalla

On tehokasta suorittaa joitakin tehtäviä samanaikaisesti ja automatisoidusti. Voit suorittaa tällaisia tehtäviä taustalla ja määrittää aikataulun myös silloin, kun haluat, että kyseiset tehtävät suoritetaan automaattisesti. Voit suorittaa tehtäviä taustalla kahdessa tilassa:

- Manuaalisesti käynnistyvät tehtävät ajoitetaan heti **Työjonon tapahtumien** avulla.
- Toistuvat tehtävät ajoitetaan **Työjonotapahtumiin**.

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Tehtävien suorittaminen taustalla tietyn myymälän osalta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kauppa** ja valitse vastaava linkki.
2. Valitse kauppa, jolle haluat suorittaa synkronoinnin taustalla avataksesi **Shopify-ostoskortti**-sivun.
3. Ota **Salli synkronointi taustalla** -valitsin käyttöön.

Nyt kun synkronointitoiminto käynnistyy, edustalla suoritettavan tehtävän sijaan se pyytää odottamaan. Kun se on valmis, voit siirtyä seuraavaan toimintoon. Tehtävä luodaan **Työjonotapahtumana**, ja se alkaa heti.

## <a name="to-schedule-recurring-tasks"></a>Toistuvien tehtävien ajoittaminen

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
|**Synkronoi yritykset**|Raportti 30114 Shopifyn synkronoidut yritykset (yritystenvälinen)|
|**Synkronoi maksut**|Raportti 30105 Shopifyn synkronoidut maksut|
|**Synkronoi luettelot**|Raportti 30115 Shopifyn synkronoidut luettelot|
|**Synkronoi luettelohinnat**|Raportti 30116 Shopifyn synkronoidut luettelohinnat (yritystenvälinen)|

> [!NOTE]
> Osa elementeistä voi päivittyä usean tehtävän mukaan. Esimerkiksi silloin, kun tuot tilauksia **Shopify-ostoskortti** -sivun asetuksen mukaan, järjestelmä voi myös tuoda ja päivittää asiakkaan ja/tai tuotteen tietoja. Muista käyttää samaa työjonon luokkaa ristiriitojen välttämiseksi.
>
> Määritä suodattimet **Raporttipyyntösivu**-toiminnon avulla. Voit esimerkiksi määrittää, että tuot tilauksia vain, kun niiden tila on **Kokonaan maksettu**.

Muita tehtäviä, joita voi olla hyödyllistä automatisoida myyntiasiakirjojen edelleenkäsittelyssä:

- Raportti 297 Eräkirjaa myyntilaskut
- Raportti 296 Eräkirjaa myyntitilaukset

Voit käyttää **Shopify-tilausnro**-kenttää -kentästä tuotujen Shopify-myyntiasiakirjojen yksilöimiseksi.

Saat lisätietoja myyntitilausten kirjaamisesta erään siirtymällä kohtaan [Työjonotapahtuman luonti myyntitilausten eräkirjausta varten](../ui-batch-posting.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).

## <a name="to-check-the-status-of-synchronization"></a>Synkronoinnin tilan tarkasteleminen

**Liiketoimintajohtajan** roolikeskuksen **Shopify-aktiviteetit**-osassa on useita pinoja, joiden avulla on helppo määrittää, onko Shopify-yhdistimessä ongelmia.

- **Yhdistämättömät asiakkaat**: Shopify-asiakas tuodaan mutta ei linkitetä vastaavaan asiakastapahtumaan [!INCLUDE [prod_short](../includes/prod_short.md)]issa.
- **Yhdistämättömät tuotteet** – Shopify-tuote tuodaan mutta ei linkitetä vastaavaan nimiketapahtumaan [!INCLUDE [prod_short](../includes/prod_short.md)]issa.
- **Käsittelemättömät tilaukset**: Shopify-tilaukset tuodaan mutta myyntiasiakirjoja ei luotu [!INCLUDE [prod_short](../includes/prod_short.md)]issa; syynä oli usein yhdistämättömät tuotteet tai asiakkaat.
- **Käsittelemättömät toimitukset**: Shopifysta peräisin olevia kirjattuja myyntitoimituksia ei synkronoida Shopifyn kanssa.
- **Toimitusvirheet**: Shopify-yhdistin ei voinut synkronoida kirjattuja myyntitoimituksia Shopifyn kanssa.
- **Synkronointivirheet**: Shopify-synkronointiin liittyviä epäonnistuneita työjonotapahtumia.

## <a name="see-also"></a>Katso myös

[Shopify-yhdistimen käytön aloittaminen](get-started.md)  
