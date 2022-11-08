---
title: Shopify- ja Business Central-synkronoinnin vianetsintä
description: Tietoja siitä, mitä tehdä, jos jokin menee pieleen Shopifyn ja Business Centralin välisen tietojen synkronoinnin aikana
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30118, 30119, 30120,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 37fb8069f6149cc89c1c53f671eafe3788f54ccf
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728354"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Shopify- ja Business Central-synkronoinnin vianetsintä

On mahdollista joutua tilanteisiin, joissa sinun on tehtävä vianmääritys, kun synkronoidaan tietoja Shopifyn ja [!INCLUDE[prod_short](../includes/prod_short.md)]in välillä. Tällä sivulla määritellään vaiheet joidenkin yleisten mahdollisten skenaarioiden vianmääritykseen.

## <a name="logs"></a>Lokit

Jos synkronointitehtävä epäonnistuu, voit ottaa lokiin kirjaamisen käyttöön ottamalla **ota loki käyttöön** -vaihtonäppäimen käyttöön **Shopify-ostoskortti**-sivulla. Voit käynnistää synkronointitehtävän manuaalisesti ja tarkastella lokia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-lokitapahtumat** ja valitse sitten vastaava linkki.
2. Valitse liittyvä lokitapahtuma ja avaa **Shopify-lokitapahtuma**-sivu.
3. Tarkastele pyyntöä, tilakoodia ja kuvausta sekä vastausarvoja.

Muista poistaa loki käytöstä myöhemmin, jotta vältytään negatiivisilta tehokkuusvaikutuksilta ja tietokannan koon kasvulta.

**Shopify-lokitapahtumat**-sivulla voit laukaista kaikkien sellaisten lokitapahtumien poistamisen, jotka ovat vanhempia kuin seitsemän päivää.

## <a name="data-capture"></a>Tiedonkeruu

**Loki aktivoitu** -asetuksista huolimatta jotkin Shopifyn vastaukset kirjataan aina lokiin, jonka voit tarkistaa tai ladata **Tiedonkeruuluettelo**-sivun avulla.

Valitse **Haettu Shopify-data** -toiminto jollakin seuraavista sivuista:

- **Shopify-tilaus**
- **Shopify-tilauksen täyttäminen**
- **Shopify-tilausten toimituskulut**
- **Shopify-tilaustapahtumat**
- **Shopify-maksut**
- **Shopify-maksutapahtumat**
- **Shopify-tapahtumat**

## <a name="reset-sync"></a>Palauta synkronointi

Parhaan suorituskyvyn takaamiseksi yhdistin tuo vain edellisen synkronoinnin jälkeen luodut tai muutetut asiakkaat, tuotteet ja tilaukset. **Shopify-ostoskortti**-sivulla on toimintoja, joiden avulla voi muuttaa viimeisimmän synkronoinnin päivämäärää ja aikaa tai nollata sen kokonaan. Tämä toiminto varmistaa sen, että kun synkronointi suoritetaan, kaikki tiedot synkronoidaan eikä vain viimeisimmän synkronoinnin jälkeen tehtyjä muutoksia.

Tämä toiminto koskee vain synkronointia Shopifysta [!INCLUDE[prod_short](../includes/prod_short.md)] -toimintoon. Se voi olla hyödyllinen, jos haluat palauttaa poistetut tiedot, kuten tuotteet, asiakkaat tai poistetut tilaukset.

## <a name="request-the-access-token"></a>Käyttöoikeustunnuksen pyytäminen

Jos [!INCLUDE[prod_short](../includes/prod_short.md)] ei pysty muodostamaan yhteyttä Shopify-tiliisi, pyydä käyttöoikeustietuetta Shopifysta. Tämä pyyntö saatetaan tarvita, jos suojausavaimia on kierrätetty tai tarvittavat käyttöoikeudet on muutettu.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat saada käyttöoikeustunnuksen avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **pyynnön käyttöoikeus** -toiminto.
4. Jos ohjelma pyytää, kirjaudu Shopify-tilillesi.

**On AccessKey** -valitsin aktivoituu.

### <a name="verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment"></a>Tarkista ja ota käyttöön käyttö oikeudet, jotka mahdollistavat HTTP-pyyntöjen suorittamisen muussa kuin tuotantoympäristössä

Toimiakseen oikein Shopify-yhdistinlaajennus tarvitsee oikeuden HTTP-pyyntöjen tekemiseen. Kun testataan Sandbox-ympäristöissä, HTTP-pyynnöt on kielletty kaikilta laajennuksilta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Laajennusten hallinta** ja valitse vastaava linkki.
2. Valitse **Shopify-yhdistin** -laajennus.
3. Avaa **Laajennusasetukset**-sivu valitsemalla **Määritä**-toiminto.
4. Varmista, että **Salli HTTPClient-pyynnöt** -valitsin on käytössä.

## <a name="rotate-the-shopify-access-token"></a>Shopify-käyttöoikeustunnuksen kääntäminen

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

### <a name="the-gen-bus-posting-group-cannot-be-zero-or-empty-there-must-be-a-value-in-the-customer-field"></a>*Ylein. liiketoim. kirjausryhmä* ei voi olla nolla tai tyhjä; asiakaskentässä täytyy olla arvo

Täytä **asiakasmallikoodi**-kenttä **Shopify-ostoskortti**-ikkunassa käyttäen mallia, jossa on **Ylein. liiketoim. kirjausryhmä** täytetty. Asiakasmallia käytetään paitsi asiakkaiden luomiseen myös myyntihinnan laskemiseen ja myyntiasiakirjojen luonnin yhteydessä.

### <a name="importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it"></a>Tietojen tuominen Shopify-kauppaan ei ole käytössä. Ota se käyttöön siirtymällä ostoskorttiin

Ota **Shopify-ostoskortti**-ikkunassa käyttöön **Salli tietojen synkronointi Shopifyssa** -vaihtoehto käyttöön. Tämä vaihtoehto on tarkoitettu suojaamaan verkkokauppaa saamasta demotietoja kohteesta [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key"></a>Oauth-virhe invalid_request: Shopify-sovellusrajapintasovellusta ei löytynyt haulla api_key

Näyttää siltä, että käytät [upota sovellus](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) -toimintoa, jossa asiakkaan URL-osoite on muotoa: `https://[application name].bc.dynamics.com`. Shopify-yhdistin ei toimi upotettavien sovellusten yhteydessä. Lue lisätietoja kohdasta [Mille Microsoft-tuotteille Shopify-yhdistin on saatavilla](shopify-faq.md#what-microsoft-products-is-the-shopify-connector-available-for).

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)
