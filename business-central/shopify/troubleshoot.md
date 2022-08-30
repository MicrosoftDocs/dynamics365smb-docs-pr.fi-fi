---
title: Shopify- ja Business Central-synkronoinnin vianetsintä
description: Tietoja siitä, mitä tehdä, jos jokin menee pieleen Shopifyn ja Business Centralin välisen tietojen synkronoinnin aikana
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 4ccbe8ac97eba568ff82d965f24b86ab58c95f81
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317243"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Shopify- ja Business Central-synkronoinnin vianetsintä

On mahdollista joutua tilanteisiin, joissa sinun on tehtävä vianmääritys, kun synkronoidaan tietoja Shopifyn ja [!INCLUDE[prod_short](../includes/prod_short.md)]in välillä. Tällä sivulla määritellään vaiheet joidenkin yleisten mahdollisten skenaarioiden vianmääritykseen.

## <a name="logs"></a>Lokit

Jos synkronointitehtävä epäonnistuu, voit ottaa lokiin kirjaamisen käyttöön ottamalla **ota loki käyttöön** -vaihtonäppäimen käyttöön **Shopify-ostoskortissa**. Käynnistä synkronointitehtävä manuaalisesti ja tarkastele lokia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-lokitapahtumat** ja valitse sitten vastaava linkki.
2. Valitse liittyvä lokitapahtuma ja avaa **Shopify-lokitapahtuma**-ikkuna.
3. Tarkastele pyyntöä, tilakoodia ja kuvausta sekä vastausta.

Muista poistaa loki käytöstä myöhemmin, jotta vältytään negatiivisilta tehokkuusvaikutuksilta ja tietokannan koon kasvulta.

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

## <a name="request-the-access-token"></a>Käyttöoikeustunnuksen pyytäminen

Jos [!INCLUDE[prod_short](../includes/prod_short.md)] ei pysty muodostamaan yhteyttä Shopify-tiliisi, pyydä käyttöoikeustietuetta Shopifysta. Tämä pyyntö saatetaan tarvita, jos suojausavaimia on kierrätetty tai tarvittavat käyttöoikeudet on muutettu.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat saada käyttöoikeustunnuksen avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **pyynnön käyttöoikeus** -toiminto.
4. Jos ohjelma pyytää, kirjaudu Shopify-tilillesi.

**On AccessKey** -valitsin aktivoituu.

### <a name="verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment"></a>Tarkista ja ota käyttöön käyttö oikeudet, jotka mahdollistavat HTTP-pyyntöjen suorittamisen muussa kuin tuotantoympäristössä

Jotta Shopify -yhdistinlaajennus toimisi oikein, se tarvitsee oikeuden HTTP-pyyntöjen tekemiseen. Kun testataan Sandbox-ympäristöissä, HTTP-pyynnöt on kielletty kaikilta laajennuksilta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Laajennusten hallinta** ja valitse sitten vastaava linkki.
2. Valitse *Shopify-yhdistin* -laajennus.
3. Avaa **Laajennusasetukset**-sivu valitsemalla **Määritä**-toiminto.
4. Varmista, että **Salli HTTPClient-pyynnöt** -valitsin on käytössä.

## <a name="rotate-the-shopify-access-key"></a>Kierrätä Shopify-käyttöoikeusavaimia

Seuraavissa ohjeissa kuvataan, miten Shopify-liittimen käyttämää käyttötunnussanomaa kierrätetään Shopify-verkkokaupan käyttöä varten.

### <a name="in-shopify"></a>Shopifyssa

1. Siirry **Shopify-hallinnasta** kohtaan [Sovellukset](https://www.shopify.com/admin/apps).
2. Valitse **Dynamics 365 Business Central** -sovelluksen riviltä **Poista**.
3. Valitse avautuvassa sanomassa **Poista**.

### <a name="in-prod_short"></a>[!INCLUDE[prod_short](../includes/prod_short.md)]issa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat kierrättää käyttöoikeustunnuksen avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Pyydä käyttöoikeutta** -toiminto.
4. Kirjaudu pyydettäessä sisään Shopify-tiliisi, tarkista tietosuoja ja käyttöoikeudet ja valitse sitten **Asenna sovellus** -painike.

## <a name="known-issues"></a>Tunnetut ongelmat

### <a name="gen-bus-posting-group-must-have-a-value-in-customer-it-cannot-be-zero-or-empty"></a>Yl. Väylä. Kirjausryhmällä on oltava arvo asiakkaassa. Se ei voi olla null eikä tyhjä.

Täytä **asiakasmallikoodi**-kenttä **Shopify-ostoskortti**-ikkunassa käyttäen mallia, jossa on **Ylein. liiketoim. kirjausryhmä** täytetty. Asiakasmallia käytetään paitsi asiakkaiden luomiseen myös myyntihinnan laskemiseen ja myyntiasiakirjojen luonnin yhteydessä.

### <a name="importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it"></a>Tietojen tuominen Shopify-kauppaan ei ole käytössä. Ota se käyttöön siirtymällä ostoskorttiin.

Ota **Shopify-ostoskortti**-ikkunassa käyttöön **Salli tietojen synkronointi Shopifyssa** -vaihtoehto käyttöön.  Tämä vaihtoehto on tarkoitettu suojaamaan verkkokauppaa saamasta demotietoja kohteesta [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
