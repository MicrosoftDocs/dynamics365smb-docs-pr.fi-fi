---
title: Varoitukset ja virhesanomat
description: 'Tutustu siihen, miten voit tehdä vianmäärityksen ja löytää ratkaisuja virheviesteihin, kun työskentelet Business Centralin kanssa.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-temeplate
---
# Varoitukset ja virhesanomat

Työpäivän aikana voi näkyä ilmoituksia [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa esimerkiksi siitä, että jotain on mennyt pieleen tai että jotain ei voitu kirjata. Ilmoituksen avulla on usein helppo ratkaista asia tai peruuttaa tekemäsi muutokset. Muissa tapauksissa sinulla ei ehkä ole tietoja, joita tarvitset ratkaistaksesi asian. Tässä artikkelissa on vihjeitä siitä, miten voit onnistua.  

## Tuotteen sisäinen käyttäjätuki

[!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman oletusversio sisältää useimpien kenttien, sarakkeiden ja toimintojen kuvaukset, joita voi käyttää, kun valitset nimen. Yhdessä tärkeiden sivujen, kuvailevien kuvatekstien ja ohjetekstien opastusvihjeiden kanssa nämä työkaluvihjeet tai kuvatekstit ovat nykyinen *upotetun käyttäjätuen* toteutus, mikä on tärkeä periaate nykyisessä ohjelmistosuunnittelussa.  

Jos sinulla on kysyttävää jostakin kentästä tai käyttöliittymän jostakin muusta osasta, valitse nimi ja lyhyt kuvaus tulee näkyviin. Valitse *Kysy Copilotilta* -linkki, jos se ei riitä. Voit myös etsiä vastauksia kysymyksiisi tuotteen sisäisestä ohjeruudusta.  

Saadaksesi lisätietoja, katso [Dynamics 365 Business Central -käyttäjäapumalli](/dynamics365/business-central/dev-itpro/user-assistance)n hallinnon sisällössä [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmalle.  

## Ohje- ja tukisivu

[!INCLUDE[prod_short](includes/prod_short.md)]in Ohje-valikosta (kysymysmerkki oikeassa yläkulmassa) pääsee **Ohje ja tuki** -sivulle. Siellä on linkkejä resursseihin, jotka auttavat löytämään vastauksia kysymyksiin. Lisätietoja on kohdassa [Resurssit ohjeelle ja tuelle](product-help-and-support.md).  

## Auta muita

Jos olet järjestelmänvalvoja tai pääkäyttäjä, voit auttaa muita käyttäjiä etsimällä virhesanomia **Virhesanomien rekisteröinti**- tai Hallintokeskus -sivuilta. Monissa tapauksissa varoitus- tai virhesanomassa on kyse asennuksesta tai puutteellisista oikeuksista ja samankaltaisissa kysymyksissä, joissa pääkäyttäjä tai järjestelmänvalvoja voi helposti auttaa. Muissa tapauksissa saatat joutua tarkastamaan sivut syyn selvittämiseksi. Lisätietoja on kohdassa [Teknisten tietojen etsiminen](/dynamics365/business-central/dev-itpro/administration/manage-technical-support#finding-technical-information) [!INCLUDE [prod_short](includes/prod_short.md)] -hallintasisällöstä.  

## Avun saannin nopeuttaminen virhetietoja jakamalla

Ongelmien ratkaiseminen ja käyttökatkosten minimointi hyödyntämällä työtovereiden ja aihealueen asiantuntijoiden osaamista. Jos virhe estää jatkamisen, virheen tiedot on helppo jakaa, kun apua saadaan. 

Näitä tietoja ovat esimerkiksi virhesanoma, virhekoodi ja muut tiedot, joista on apua virheen vianmäärityksessä. Jakamalla virheen tiedot voidaan viestittää tehokkaasti esillä oleva ongelma, mikä auttaa työtovereita antamaan apua.  

Tiedot voidaan kopioida valitsemalla **Jaa-kuvakkeen** vahvistusikkunoissa ja **Jaa tiedot** -valikon virheikkunoissa.  

Virhetietojen kopioinnin lisäksi voidaan valita tietojen jakaminen Microsoft Teamsin kautta valitsemalla **Jaa tiedot Teamsiin** seuraavasti:

* Kopioi virheen tiedot.
* Avaa **Jaa Teamsiin** -ikkuna, jossa kopioidut virheen tiedot liitetään ja määritetään, keneltä halutaan pyytää apua. [!INCLUDE [prod_short](includes/prod_short.md)] lisää linkin sivulla, jossa virhe tapahtui, mikä helpottaa vianmääritystä.

Vaihtoehtoisesti voi jakaa tiedot sähköpostitse valitsemalla **Jaa tiedot sähköpostitse** ja toimimalla seuraavasti:

* Kopioi virheen tiedot.
* Avaa oletussähköpostiohjelma, jossa kopioidut virheen tiedot liitetään ja määritetään, keneltä halutaan pyytää apua. [!INCLUDE [prod_short](includes/prod_short.md)] lisää linkin sivulle, jossa ongelma esiintyi.

## Omaehtoinen apu

Ympäristövirheiden ymmärtämistä, niihin siirtymistä ja niiden ratkaisemista on helpotettu.

[!INCLUDE [prod_short](includes/prod_short.md)] -ympäristön luomissa virhesanomissa on kaikki tekniset tiedot, mukaan lukien kenttien nimet, **Eritelty virhesanoma** -osassa. Valitse tarkistusvirheissä tai virhesanomissa **Kopioi tiedot** -kuvake, sillä näin saadaan tekniset tiedot.

Virhesanomien toiminnot vievät suoraan sivulle, jossa kenttä aiheuttaa virheen. Sivun tai kentän etsimiseen ei siis kulu aikaa. Kun virhesanomassa valitaan toiminto, [!INCLUDE [prod_short](includes/prod_short.md)] siirtää oikeaan sijaintiin ratkaisemaan virheen.

### Vinkki kehittäjille

Jos kehittäjä kutsuu [TestField](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-testfield-joker-joker-errorinfo-method)-menetelmää eikä ErrorInfo-objektia siirretä, [!INCLUDE [prod_short](includes/prod_short.md)] luo automaattisesti linkin sivulle, jossa käyttäjä voi korjata ongelman. [!INCLUDE [prod_short](includes/prod_short.md)] hakee ensin tietueen haku- tai porautumissivun ja etsii sitten kortti- tai hakusivun sekä lisää navigointilinkin kyseiselle korttisivulle. [!INCLUDE [prod_short](includes/prod_short.md)] ei lisää linkkiä seuraavissa tilanteissa:

* Virhe on avoimena olevalla sivulla.
* Käyttäjällä ei ole taustatietueen muokkausoikeutta.

## Katso myös

[Ohje- ja tukiresurssit](product-help-and-support.md)  
[Usein kysytyt kysymykset](across-faq.yml)  
[Kerro, mitä haluat tehdä -toiminnon usein kysytyt kysymykset](ui-search-faq.md)  
[Usein kysyttyjen kysymysten haku ja suodatus](ui-search-filter-faq.yml)  
[Kopioimisen ja liittämisen usein kysytyt kysymykset](faq-copy-paste.yml)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]