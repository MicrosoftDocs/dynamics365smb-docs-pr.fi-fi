---
title: Shopify- ja Business Central-synkronoinnin vianetsintä
description: Tietoja siitä, mitä tehdä, jos jokin menee pieleen Shopifyn ja Business Centralin välisen tietojen synkronoinnin aikana
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 01ff5ab1c5e6f132098f914f6bfe97e097cc88b0
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768132"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Shopify- ja Business Central-synkronoinnin vianetsintä

On mahdollista joutua tilanteisiin, joissa sinun on tehtävä vianmääritys. Tällä sivulla määritellään vaiheet joidenkin yleisten mahdollisten skenaarioiden vianmääritykseen.

## <a name="logs"></a>Lokit

Jos synkronointitehtävä epäonnistuu, voit ottaa lokiin kirjaamisen käyttöön ottamalla **ota loki käyttöön** -vaihtonäppäimen käyttöön **Shopify-ostoskortissa**. Käynnistä synkronointitehtävä manuaalisesti ja tarkastele lokia.

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-lokitapahtumat** ja valitse sitten vastaava linkki.
2. Valitse liittyvä lokitapahtuma ja avaa **Shopify-lokitapahtuma**-ikkuna.
3. Tarkastele pyyntöä, tilakoodia ja kuvausta sekä vastausta.

Muista poistaa loki käytöstä, jotta vältytään negatiivisilta tehokkuusvaikutuksilta ja tietokannan koon kasvulta.

**Shopify-lokitapahtumat**-ikkunassa voit laukaista kaikkien sellaisten lokitapahtumien poistamisen, jotka ovat vanhempia kuin seitsemän päivää.

## <a name="data-capture"></a>Tiedonkeruu

**Loki aktivoitu** -asetuksista huolimatta jotkin Shopifyn vastaukset kirjataan aina lokiin, jonka voit tarkistaa tai ladata **Tiedonkeruuluettelo**-ikkunan avulla.

Valitse **Haettu Shopify-data** -toiminto jollakin seuraavista sivuista:

- **Shopify-tilaus**
- **Shopify-tilauksen täyttäminen**
- **Shopify-tilausten toimituskulut**
- **Shopify-tilaustapahtumat**
- **Shopify-maksut**
- **Shopify-maksutapahtumat**
- **Shopify-tapahtumat**

## <a name="reset-sync"></a>Palauta synkronointi

Parhaan suorituskyvyn takaamiseksi yhdistin tuo vain edellisen synkronoinnin jälkeen luodut tai muutetut asiakkaat, tuotteet ja tilaukset. **Shopify-ostoskortissa** on toimintoja, joiden avulla voi muuttaa viimeisimmän synkronoinnin päivämäärää ja aikaa tai nollata sen kokonaan. Tämä toiminto varmistaa sen, että kun synkronointi suoritetaan, kaikki tiedot synkronoidaan eikä vain viimeisimmän synkronoinnin jälkeen tehtyjä muutoksia.

Tämä toiminto koskee vain synkronointia Shopifysta [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan ja voi olla hyödyllinen, jos haluat palauttaa poistetut tiedot, kuten tuotteet, asiakkaat tai poistetut tilaukset.

## <a name="update-the-access-token"></a>Käyttöoikeustunnuksen päivitys

Jos [!INCLUDE[prod_short](../includes/prod_short.md)] ei pysty muodostamaan yhteyttä Shopify-tiliisi, yritä nollata käyttöoikeustietue.

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat saada käyttöoikeustunnuksen avataksesi **Shopify-ostoskortti**-sivun.
3. Syötä koodi **Koodi**-kenttään.  
4. Valitse **pyynnön käyttöoikeus** -toiminto.
5. Jos ohjelma pyytää Kirjautumaan Shopify-tilillesi.

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
