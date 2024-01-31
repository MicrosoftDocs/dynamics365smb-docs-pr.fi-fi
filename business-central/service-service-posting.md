---
title: Huollon kirjaus
description: Huollon kirjaustoiminnon avulla voit käsitellä asiakirjoja tehokkaasti ja ylläpitää onnistunutta asiakkaiden huoltomenettelyä.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Huollon kirjaus
Huollon kirjaustoiminnon avulla voit käsitellä asiakirjoja tehokkaasti ja ylläpitää onnistunutta asiakkaiden huoltomenettelyä. Tämän ominaisuuden avulla ohjelma voi luoda ja päivittää kirjattuja asiakirjoja, luoda tapahtumia huoltoalueella sekä muissa moduuleissa asianmukaisen päivityksen varmistamiseksi.  

> [!NOTE]  
>  Seuraavassa ohjeessa neuvotaan, miten huoltokirjauksia tehdään riippumatta siitä, miten kohteita käsitellään fyysisessä varastossa.  
>   
>  Jos fyysisen varaston käsittely ei ole pakollista sijainnissa, tee kirjaustoiminnot suoraan **Huoltorivit**-sivulla. Sijainneissa, joissa käytetään fyysisen varaston käsittelyä, kuvatut kirjaustoiminnot (toimitusta ja kulutusta lukuun ottamatta) suoritetaan suoraan muuttuvien fyysisen varaston toimitustoimintojen kautta asetusten perusteella. Lisätietoja on kohdassa [Nimikkeiden poiminta varastopoiminnalla](warehouse-how-to-pick-items-with-inventory-picks.md).  

## Toimitus  
Toimitusvaihtoehdon avulla voit rekisteröidä ohjelmassa nimikkeet ja huoltotilauksen riveille huollon suorituksen jälkeen syötetyt ajat. Ohjelma luo kirjatun toimituksen ja päivittää varastomoduulin ja muut [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman moduulit sen mukaan, mitä nimikkeitä on otettu varastosta ja lähetetty asiakkaalle. Ohjelma tuottaa erityisesti nimiketapahtumia, arvotapahtumia, huoltotapahtumia ja takuutapahtumia.  

Jos sijainti on määritetty niin, että fyysisen varaston käsittely on pakollinen, huoltonimikerivien toimitus ja siirtäminen tapahtuu samalla tavalla kuin muissa lähdeasiakirjoissa. Ainoa ero on, että huoltorivin nimikkeet voidaan käyttää joko ulkoisesti tai sisäisesti, johon tarvitaan kaksi eri vapautustoimintoa.

## Lasku  
Sinun on käytettävä laskutusvalintaa, kun laskutat asiakkaalta huollon. Yleensä **Kirjaa toimitus** -toiminnon avulla rekisteröidyn toimitetun määrän ja **Kirjaa kulutus** -toiminnon avulla rekisteröidyn kulutetun määrän ero on laskutettava määrä. Et voi laskuttaa määrää, jota ei ole toimitettu. Kun suoritat **Kirjaa lasku** -toiminnon, ohjelma luo kirjatun huoltolaskun ja päivittää kirjatut asiakirjat, ennen kuin niistä tehdään lähetetyn laskun määrien mukaisia. Ohjelma luo asianmukaiset tapahtumat, esim. KP-tapahtumat, kuten muissa kirjausprosesseissa.  

## Toimitus ja lasku  
Toimitus- ja laskutusvaihtoehdon avulla voit luoda sekä palvelutoimituksen että laskun samaan aikaan.  

## Toimitus ja kulutus  
Toimita- ja kuluta -vaihtoehdon avulla voit rekisteröidä ja kirjata nimikkeitä, kustannuksia tai tunteja, jotka on käytetty huollossa, mutta joita ei voi sisällyttää asiakkaalle lähetettävään laskuun. Ohjelma ei lähetä laskua, mutta mahdollistaa huoltotoimituksen ja huollon kulutuksen lähettämisen samanaikaisesti, jolloin nähdään, että osa nimikkeistä/tunneista on ollut asiakkaalle ilmaisia. Vastaavia tapahtumia luodaan myös, jotta kulutus voidaan rekisteröidä.  

> [!NOTE]  
>  Huollon kirjausprosessi mahdollistaa osittaisen kirjauksen. Voit luoda myös osittaisen toimituksen tai osittaisen laskun täyttämällä **Toimitettava määrä**- ja  **Laskutettava määrä** -kentät huoltotilausten yksittäisillä huoltoriveillä ennen kirjausta. Huomaa, että laskua ei voi luoda jollekin, jota ei ole toimitettu. Tämä tarkoittaa sitä, että ennen laskutusta on täytynyt rekisteröidä toimitus, tai täytyy valita yhtäaikainen toimitus ja laskutus.  

Kirjauksen jälkeen voit katsella kirjattuja huoltoasiakirjoja niitä vastaavilta sivuilta **Kirjattu huoltotoimitus** ja **Kirjattu huoltolasku**. Luodut kirjatut tapahtumat ovat näkyvissä erilaisissa kirjattuja tapahtumia, kuten **KP-tapahtumia**, **nimiketapahtumia**, **fyysisen varaston tapahtumia**, **huoltotapahtumia**, **projektitapahtumia** ja **takuutapahtumia**, sisältävillä sivuilla.  

## Kirjattujen huoltoasiakirjojen tarkasteleminen  
Kun kirjaat huoltolaskun, huoltotoimituksen tai huollon hyvityslaskun, asiakirjan tiedot siirretään **Kirjattu huoltolasku**-, **Kirjattu huoltotoimitus**- tai **Kirjattu huollon hyvityslasku** -sivulle. Et voi lisätä mitään näille sivuille etkä muuttaa tai poistaa niiltä mitään. Voit tulostaa toimituksen, laskun tai hyvityslaskun näillä sivuilla.  

Seuraavassa ohjeessa käytetään esimerkkinä kirjattua huoltolaskua, mutta samaa menettelyä voidaan käyttää kirjattuihin toimituksiin sekä palvelu- ja hyvityslaskuihin.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjattu huoltolasku** ja valitse sitten vastaava linkki.  
2. Avaa kirjattu huoltolasku, jonka haluat nähdä.  
3. Valitse **Tilastot**-toiminto, jos haluat yleiskuvan kirjatusta laskusta.  

    Avaa **Huoltotilaustilastot**-sivu. Sivulla on muun muassa seuraavat kirjatun asiakirjan tiedot: määrä, summa, ALV, kustannus, tuotto ja asiakkaan luottoraja.

## Katso myös  
[Huoltotilausten kirjaaminen](service-how-to-post-service-orders.md)   
[Huoltotilausten luominen](service-how-to-create-service-orders.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]