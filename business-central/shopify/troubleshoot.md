---
title: Shopify- ja Business Central-synkronoinnin vianetsintä
description: 'Tietoja siitä, mitä tehdä, jos jokin menee pieleen, kun synkronoit tietoja Shopifyn ja Business Centralin välillä.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
---

# Shopify- ja Business Central-synkronoinnin vianetsintä

On mahdollista joutua tilanteisiin, joissa sinun on tehtävä vianmääritys, kun synkronoidaan tietoja Shopifyn ja [!INCLUDE[prod_short](../includes/prod_short.md)]in välillä. Tämä sivu määrittää joidenkin tyypillisten skenaarioiden vianmääritysvaiheet.

## Tehtävien suorittaminen edustalla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kauppa** ja valitse vastaava linkki.
2. Valitse kauppa, jolle haluat tehdä vianmäärityksen avataksesi **Shopify-ostoskortti**-sivun.
3. Poista **Salli synkronointi taustalla** -valitsin käytöstä.

Nyt kun synkronointitoiminto käynnistetään, tehtävä suoritetaan edustalla. Jos ilmenee virhe, saat virhevalintaikkunan, jossa on **Kopioi tiedot** -linkki. Linkin avulla voit kopioida tietoja tekstieditoriin lisäanalyysia varten.

## Lokit

Jos synkronointitehtävä epäonnistuu, voit ottaa lokiin kirjaamisen käyttöön ottamalla **ota loki käyttöön** -vaihtonäppäimen käyttöön **Shopify-ostoskortti**-sivulla. Voit käynnistää synkronointitehtävän manuaalisesti ja tarkastella lokia.

### Lokiinkirjaamisen ottaminen käyttöön

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kauppa** ja valitse vastaava linkki.
2. Valitse kauppa, jolle haluat tehdä vianmäärityksen avataksesi **Shopify-ostoskortti**-sivun.
3. Ota **Loki käytössä** -valitsin käyttöön.

### Lokien tarkasteleminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-lokitapahtumat** ja valitse sitten vastaava linkki.
2. Valitse liittyvä lokitapahtuma ja avaa sitten **Shopify-lokitapahtuma**-sivu.
3. Tarkastele pyyntöä, tilakoodia ja kuvausta sekä vastausarvoja. Voit ladata pyyntö- ja vastausarvot tiedostoina tekstimuodossa.

Muista myöhemmin sulkea kirjautuminen, jotta suorituskyky ei heikenny ja eikä tietokannan koko kasva.

**Shopify-lokitapahtumat**-sivulla voit laukaista kaikkien lokitapahtumien poistamisen tai sellaisten, jotka ovat vanhempia kuin seitsemän päivää.

## Tiedonkeruu

Osa Shopify-vastauksista kirjataan aina lokiin, riippumatta siitä, onko **Loki aktivoitu** käytössä. Voit tarkastaa tai ladata lokitiedot **Tietojen sieppausluettelo** -sivulta.

Valitse **Haettu Shopify-data** -toiminto jollakin seuraavista sivuista:

- **Shopify-tilaus**
- **Shopify-tilausrivi**
- **Shopify-jakelut**
- **Shopify-tilausten toimituskulut**
- **Shopify-tilaustapahtumat**
- **Shopify-palautus**
- **Shopify-palautusrivi**
- **Shopify-hyvitys**
- **Shopify-hyvitysrivi**
- **Shopify-maksut**
- **Shopify-maksutapahtumat**
- **Shopify-tapahtumat**

## Palauta synkronointi

Parhaan suorituskyvyn takaamiseksi yhdistin tuo vain edellisen synkronoinnin jälkeen luodut tai muutetut asiakkaat, tuotteet ja tilaukset. **Shopify-ostoskortti**-sivulla on toimintoja, joiden avulla voi muuttaa viimeisimmän synkronoinnin päivämäärää ja aikaa tai nollata sen kokonaan. Tämä toiminto varmistaa sen, että kaikki tiedot synkronoidaan eikä vain viimeisimmän synkronoinnin jälkeen tehtyjä muutoksia.

Tämä toiminto koskee vain synkronointia Shopifysta [!INCLUDE[prod_short](../includes/prod_short.md)] -toimintoon. Se voi olla hyödyllinen, jos haluat palauttaa poistetut tiedot, kuten tuotteet, asiakkaat tai poistetut tilaukset.

## Käyttöoikeustunnuksen pyytäminen

Jos [!INCLUDE[prod_short](../includes/prod_short.md)] ei pysty muodostamaan yhteyttä Shopify-tiliisi, pyydä käyttöoikeustietuetta Shopifysta. Sinun täytyy ehkä pyytää uusi tunnus, jos suojausavaimiin tai käyttöoikeuksiin (sovelluksen vaikutusalueisiin) tehtiin muutoksia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat saada käyttöoikeustunnuksen avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **pyynnön käyttöoikeus** -toiminto.
4. Jos ohjelma pyytää, kirjaudu Shopify-tilillesi.

**On AccessKey** -valitsin aktivoituu.

## Tarkista ja ota käyttöön käyttöoikeudet, jotka mahdollistavat HTTP-pyyntöjen luomisen muussa kuin tuotantoympäristössä

Toimiakseen oikein Shopify-yhdistinlaajennus tarvitsee oikeuden HTTP-pyyntöjen tekemiseen. Kun testataan eristysympäristöissä, HTTP-pyynnöt on kielletty kaikilta laajennuksilta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Laajennusten hallinta** ja valitse sitten vastaava linkki.
2. Valitse **Shopify-yhdistin** -laajennus.
3. Avaa **Laajennusasetukset**-sivu valitsemalla **Määritä**-toiminto.
4. Varmista, että **Salli HTTPClient-pyynnöt** -valitsin on käytössä.

## Shopify-käyttöoikeustunnuksen kääntäminen

Seuraavissa ohjeissa kuvataan, miten Shopify-liittimen käyttämää käyttötunnussanomaa kierrätetään Shopify-verkkokaupan käyttöä varten.

### Shopifyssa

1. Siirry **Shopify-hallinnasta** kohtaan [Sovellukset](https://www.shopify.com/admin/apps).
2. Valitse **Dynamics 365 Business Central** -sovelluksen riviltä **Poista**.
3. Valitse avautuvassa sanomassa **Poista**.

### [!INCLUDE[prod_short](../includes/prod_short.md)]issa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat kierrättää käyttöoikeustunnuksen avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Pyydä käyttöoikeutta** -toiminto.
4. Kirjaudu pyydettäessä sisään Shopify-tiliisi, tarkista tietosuoja ja käyttöoikeudet ja valitse sitten **Asenna sovellus** -painike.

## Tunnetut ongelmat

### Virhe: myynnin otsikkoa ei ole. Tunnistuskentät ja -arvot: Document Type='Quote',No.='YOUR SHOPIFY STORE'

Laskeakseen hinnat Shopify-yhdistin luo väliaikaisen asiakkaan (kauppakoodin) väliaikaisen myyntiasiakirjan (tarjouksen) ja käyttää vakiohinnan laskentalogiikkaa. Jos kolmannen osapuolen laajennus tilaa väliaikaisen myyntiasiakirjan tapahtumia, otsikko ei välttämättä ole käytettävissä. Microsoft suosittelee, että otat yhteyttä laajennuksen tarjoajaan. Pyydä heitä muuttamaan koodia tilapäisten tietueiden tarkistusta varten. Joissakin tapauksissa riittää, että `IsTemporary`-menetelmä lisätään oikeaan paikkaan riittää. Lisätietoja `IsTemporary`-kohteesta on kohdassa [IsTemporary](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Voit varmistaa, että ongelma aiheutuu kolmannen osapuolen laajennuksesta, käyttämällä **Kopioi tiedot leikepöydälle** -linkkiä virhesanomassa ja kopioimalla sisältö tekstieditoriin. Tiedot sisältävät **AL-kutsupinon**, jossa ylin rivi on virhetilanteessa oleva rivi. Seuraavassa esimerkissä näytetään AL-kutsupino.

AL-kutsupino:

```AL
[Object Name]([Object type] [Object Id]).[Function Name] line [XX] - [Extension Name] by [Publisher] 
...
"Sales Line"(Table 37)."No. - OnValidate"(Trigger) line 98 - Base Application by Microsoft
"Shpfy Product Price Calc."(CodeUnit 30182).CalcPrice line 20 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateTempProduct line 137 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateProduct line 5 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).OnRun(Trigger) line 12 - Shopify Connector by Microsoft
"Shpfy Add Item to Shopify"(Report 30106)."Item - OnAfterGetRecord"(Trigger) line 2 - Shopify Connector by Microsoft
"Shpfy Products"(Page 30126)."AddItems - OnAction"(Trigger) line 5 - Shopify Connector by Microsoft
```

Muista jakaa AL-kutsupinon tiedot laajennuksen toimittajan kanssa.

### Virhe: yleinen. Liiketoiminnan kirjausryhmä täytyy sisältää arvon kohdassa Asiakas: 'SINUN SHOPIFY-KAUPPASI'. Se ei voi olla null eikä tyhjä

Valitse **asiakasmallikoodi**-kenttä **Shopify-ostoskortti**-ikkunassa käyttäen mallia, jossa on **Ylein. liiketoim. kirjausryhmä** täytetty. Asiakasmallia käytetään luomaan asiakkaita ja laskemaan myyntihintoja myyntiasiakirjoissa.

### Virhe: Tietojen tuominen Shopify-kauppaan ei ole käytössä. Ota se käyttöön siirtymällä ostoskorttiin

Ota **Shopify-ostoskortti**-sivulla käyttöön **Salli tietojen synkronointi Shopifyssa** -vaihtoehto käyttöön. Tämä asetus auttaa suojaamaan verkkokauppaa saamasta demotietoja kohteesta [!INCLUDE[prod_short](../includes/prod_short.md)].

### Virhe: Oauth-virhe invalid_request: Shopify-sovellusrajapintasovellusta ei löytynyt haulla api_key

Näyttää siltä, että käytät [upota sovellus](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) -toimintoa, jossa asiakkaan URL-osoite on muotoa: `https://[application name].bc.dynamics.com`. Shopify-yhdistin ei toimi upotettavien sovellusten yhteydessä. Lue lisää kohdasta [Mille Microsoft-tuotteille Shopify-yhdistin on saatavilla?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

### Virhe: sisäinen virhe. Jokin meni vikaan meidän päässämme. Pyyntötunnus: XXXXXXXX-XXXX-XXXX-XXXX-XXXX

Ota yhteyttä Shopify-tukeen 7 päivän kuluessa tämän virheen ilmenemistä ja anna pyynnön tunnus. Saat lisätietoja siirtymällä [Shopifyn tukivaihtoehtoihin](shopify-faq.md#shopify).

### Virhe: Oauth-virheen invalid_request: tililläsi ei ole lupaa myöntää pyydettyä käyttöoikeutta tälle sovellukselle. 

Näyttää siltä, että käyttäjällä, joka pyytää käyttöoikeutta, ei ole oikeuksia hallita sovelluksia (kykyä hallita ja asentaa sovelluksia ja kanavia sekä mahdollisesti hyväksyä sovellusmaksuja). Voit ehkä ratkaista tämän ongelman asentamalla sovelluksen tilin omistajaksi. Vaihtoehtoisesti voit tarkistaa käyttäjän **sovelluksen käyttöoikeudet** [**Käyttäjät ja käyttöoikeudet**](https://www.shopify.com/admin/settings/account) -asetuksista **Shopify-järjestelmänvalvojassa**.  

## Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)
