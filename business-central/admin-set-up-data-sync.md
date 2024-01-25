---
title: Määritä yritykset päätietojen synkronoimiseksi
description: Tietoja yhden tai usean yrityksen määrittämisestä päätietojen synkronoimiseksi.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---

# Päätietojen synkronointiin valmistautuminen

Kun vähintään kaksi yritystä käyttää samoja päätietoja, voit synkronoida tiedot sen sijaan, että lisäsit ne manuaalisesti jokaiseen yritykseen. Tietojen synkronointi on esimerkiksi erityisen hyödyllistä silloin, kun määrität uusia tytäryrityksiä.

Päätietoihin kuuluvat asetukset ja ei-kaupalliset tiedot liiketoimintayksiköistä. Esimerkiksi asiakkaat, toimittajat, nimikkeet ja työntekijät. Tiedot tarjoavat kontekstin liiketoimintatapahtumia varten. Seuraavassa on muutamia esimerkkejä asiakkaan päätiedoista:

* Name
* Tunnistenumero
* Osoite
* Maksuehdot
* Luottoraja

Synkronointi määritetään tytäryrityksissä. Vetomallin avulla tytäryhtiöt hakevat lähdeyritykseltä tiedot, joita ne tarvitsevat asioidakseen niiden kanssa. Kun olet määrittänyt synkronoinnin ja synkronoit tiedot ensimmäisen kerran, olet valmis. Työjonotapahtumat käynnistävät heti tietojen päivittämisen tytäryrityksiin, kun joku muuttaa tietoja lähdeyrityksessä.

## Vain monisuuntainen synkronointi

Voit synkronoida tietoja vetomallilla vain lähdeyrityksestä tytäryrityksiin. Tytäryhtiöt eivät voi työntää tietoja lähdeyritykseen.

> [!NOTE]
> Vaikka se on mahdollista, Microsoft ei suosittele kaksisuuntaisen synkronoinnin määrittämistä. Tämä tarkoittaa sitä, että lähdeyrityksen tiedot synkronoidaan tytäryrityksiin ja tytäryrityksistä lähdeyritykseen. Tietojen synkronoiminen molempiin suuntiin voi aiheuttaa ristiriitoja tai ei-toivottuja korvauksia.

## Ennen kuin aloitat

Seuraavat seikat ovat synkronoinnin määrittämisen vaatimukset.

* Kaikkien yritysten täytyy olla samassa ympäristössä.
* Käyttäjällä, joka määrittää tytäryrityksen, täytyy olla **Essential**-, **Premium**- tai **Perus-ISV**-käyttöoikeus.

> [!NOTE]
> Ryhmän jäsenen ja sisäisen järjestelmänvalvojan käyttöoikeudet antavat sinulle pääsyn tietueisiin, mutta eivät muuta niitä, joten niitä ei voi käyttää synkronoinnin määrittämiseen. Delegoidun järjestelmänvalvojan käyttöoikeus ei anna sinun ajoittaa taustatehtäviä, joten et voi suorittaa asennusta loppuun.

## Määritä lähdeyritys

Ensimmäisten vaiheiden avulla voit määrittää yrityksen, joka on tietolähde, ja ottaa synkronoinnin käyttöön. Tytäryritykset vetävät tietoja lähdeyrityksestä.

> [!NOTE]
> Kun otat synkronoinnin käyttöön, [!INCLUDE [prod_short](includes/prod_short.md)] luo ja ajoittaa työjonotapahtumat, jotka synkronoivat tiedot. Voi näyttää siltä, että tapahtumat synkronoivat tiedot välittömästi, mutta se ei pidä paikkaansa. Luodut työjonotapahtumat synkronoivat vain kytkettyjä tietueita, ja tässä vaiheessa et ole vielä määrittänyt sitä. Synkronointi aloitetaan sen jälkeen, kun [taulukot ja kentät otetaan käyttöön tai poistetaan käytöstä](#enable-or-disable-tables-and-fields) ja [ne on synkronoitu ensimmäisen kerran](#synchronize-for-the-first-time).

1. Valitse tytäryhtiössä ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Päätietojen hallinnan asetukset** ja valitse sitten vastaava linkki.
1. Määritä **Lähdeyritys**-kentässä yritys, josta muutokset vedetään.
1. Määritä valitsimessa **Ota synkronointi käyttöön**.
1. Kun näyttöön tulee vahvistusdialogi, valitse **OK**. [!INCLUDE [prod_short](includes/prod_short.md)] etsii taulukot ja kentät, jotka ovat saatavilla lähdeyrityksestä.

Seuraava vaihe on taulukoiden ja kenttien ottaminen käyttöön synkronointia varten.

## Taulukoiden ja kenttien ottaminen käyttöön ja poistaminen käytöstä

Jos haluat säästää aikaa, [!INCLUDE [prod_short](includes/prod_short.md)] tarjoaa luettelon taulukoista, joita yritykset usein synkronoivat. Oletusarvoisesti nämä taulukot on otettu käyttöön synkronointia varten. Voit muokata, poistaa käytöstä tai poistaa niitä parhaaksi katsomallasi tavalla. Ajan säästämiseksi, jotkin taulukoiden kentät on jo poistettu käytöstä, koska ne eivät todennäköisesti ole olennaisia tytäryrityksen kannalta.

> [!NOTE]
> Jos lähdeyritykseen on asennettu vähintään kaksi laajennusta, kun tytäryritys määrittää synkronoinnin, **Synkronointitaulukot**-sivulla on laajennuksia sisältäviä taulukoita, ja voit käyttää niiden kenttiä. Jos lähdeyritys lisää laajennuksen synkronoinnin jälkeen, kunkin tytäryrityksen on kuitenkin lisättävä taulukot manuaalisesti. Saat lisätietoja taulukoiden lisäämisestä valitsemalla [Lisää tai poista taulukoita synkronointitaulukoiden luettelosta](#add-or-delete-tables-from-the-synchronization-tables-list). Jos haluat lisä tietoja [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman laajentamisesta, siirry kohtaan [Visual Studio Coden laajennusten kehittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview#developing-extensions-in-visual-studio-code).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Päätietojen hallinnan asetukset** ja valitse sitten vastaava linkki.
1. Valitse **Synkronointitaulukot**-toiminto.
1. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> **Taulukon suodatus** -kenttä on hyödyllinen, kun haluat ohjata taulukon synkronointia. Voit määrittää suodattimia synkronoitaviksi vain silloin, kun tietyt ehdot täyttyvät. Voit esimerkiksi lisätä suodattimia, jotka määrittävät, että synkronoit vain tietyn alueen toimittajat. Tai asiakkaita, jotka käyttävät tiettyä valuuttaa.
>
> Jos tytäryrityksellä on jo tietoja taulukoissa, toinen hyvä tapa määrittää synkronointiehdot on määrittää vastaavuuteen perustuva yhdistäminen. Jos haluat lisätietoja kohdistuksesta, siirry kohtaan [Vastaavuuteen perustuvan yhdistämisen käyttäminen](#use-match-based-coupling).

1. Jos haluat ottaa taulukon kentät käyttöön, valitse taulukko ja valitse sitten **Kentät**-toiminto.
1. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Nopea tapa ottaa useita kenttiä käyttöön tai poistaa ne käytöstä samanaikaisesti on valita ne luettelosta ja käyttää sitten joko **Ota käyttöön**- tai **Poista käytöstä** -toimintoa.

### Käytä vastaavuuteen perustuvaa yhdistämistä

Voit määrittää taulukon synkronoitavat tiedot käyttämällä ehtoihin perustuvia tietueita. Valitse **Perustietojen hallinnan asetukset** -sivulla **Vastaavuuteen perustuva yhdistäminen** -toiminto avataksesi **Valitse yhdistämisehdot** -sivun. Voit määrittää seuraavat kriteerit kohdistusta varten:

* Synkronoidaanko sen jälkeen, kun tietueet on yhdistetty.
* Luodaanko tytäryhtiössä uusi tietue, jos täsmäytyskriteerien avulla löydetään ainutlaatuinen, kohdistamaton vastaavuus. Voit aktivoida tämän ominaisuuden ottamalla käyttöön **Luo uusi, jos ei löydy vastaavuutta** -toiminto.
* Kentät, joita käytetään tietueiden täsmäämiseen ja se, onko vastaavuus kirjainkoon huomioonottava.
* Priorisoi tietueiden hakujärjestystä määrittämällä vastaavuusprioriteetin. [!INCLUDE [prod_short](includes/prod_short.md)] etsii vastaavuutta nousevassa järjestyksessä vastaavuuden prioriteetin perusteella. Tyhjä arvo on sama kuin prioriteetti 0, joka on korkein prioriteetti. Kentät, joiden prioriteetti on 0, otetaan ensin huomioon.

## Synkronoi ensimmäisen kerran

Kun olet valmis, valitse **Päätietojen hallinnan asetukset** -sivulla **Aloita ensimmäinen synkronointi** -toiminto. Valitse **Päätietojen ensimmäinen synkronointi** -sivulla kunkin taulukon synkronointityyppi.

* Jos sekä lähde- että tytäryrityksissä on jo tietueita ja haluat kohdistaa olemassa olevat tietueet, valitse **Käytä vastaavuuteen perustuvaa yhdistämistä** -toimintoa. [!INCLUDE [prod_short](includes/prod_short.md)] vertaa tytäryrityksen tietueita lähdeyrityksen tietueisiin. Kohdistukset perustuvat määrittämiisi kriteereihin. Useille oletustaulukoille [!INCLUDE [prod_short](includes/prod_short.md)] on jo kohdistanut aiemmin luodut tietueet käyttämällä niiden perusavainta, mutta voit halutessasi muuttaa sitä. Voit myös antaa synkronoinnin luoda uusia tietueita tytäryrityksessä lähdeyrityksen tietueisiin, joita tytäryrityksellä ei ole. Jos haluat lisätietoja kohdistuksesta, siirry kohtaan [Vastaavuuteen perustuvan yhdistämisen käyttäminen](#use-match-based-coupling).
* Jos valitset **Suorita täydellinen synkronointi**, synkronointi luo uudet tietueet kaikille lähdeyrityksen tietueille, joita ei ole vielä yhdistetty. Tästä vaihtoehdosta on hyötyä esimerkiksi seuraavissa tilanteissa:

    * Tytäryrityksellä ei ole tietoja taulukossa.
    * Haluat lisätä lähdeyrityksen tietueita ilman kohdistusta.  

Kun olet valinnut käytettävän asetuksen, aloita synkronointi valitsemalla **Aloita kaikki** -toiminto.

Kun synkronointi on käynnissä, **Työn tila** -sarake **Perustietojen ensimmäinen täydellinen synkronointi** -sivulla näyttää kunkin työjonomerkinnän tilan. Päivitä tila painamalla **F5**-näppäintä.

> [!TIP]
> Taulukot synkronoidaan ennalta määritetyssä järjestyksessä. Jos synkronointi on juuttunut taulukkoon, valitse taulukko ja valitse sitten **Käynnistä uudelleen**, jotta saat sen taas toimimaan.

Jos haluat käyttää tietoja, kuten lisättyjen tai muutettujen tietueiden määrää, valitse **Työn tila** -sarakkeesta arvo, kun haluat avata **Näytä - Integroinnin synkronointityöt** -sivun. Lisätyille tietueille voit valita **lisätty**-sarakkeen numeron ja käyttää uusia tietueita koskevia lisätietoja.

## Taulukkojen lisääminen tai poistaminen synkronointitaulukkojen luettelosta

### Taulukon lisääminen

> [!IMPORTANT]
> Vaikka tapahtumatietoja sisältävät taulukot ovat saatavilla luettelossa, kuten taulukoita, jotka sisältävät pääkirjanpidon merkintöjä, niitä ei kannata valita. Synkronointi toimii vain sellaisissa taulukoissa, jotka sisältävät ei-tapahtumatietoja.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Synkronoi taulukot** ja valitse sitten vastaava linkki.
1. Valitse **Uusi** ja valitse sitten lisättävä taulukko.
1. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

### Poista taulukko

> [!NOTE]
> Jos poistat tietueen lähdeyrityksestä, sitä ei poisteta myös tytäryhtiöstä. Tämä auttaa estämään ei-toivotut tietojen menetykset. Tytäryritys voi halutessaan poistaa taulukon.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Synkronoi taulukot** ja valitse sitten vastaava linkki.
1. Valitse **Poista**-toiminto.

## Jaa synkronointiasetukset käyttämällä vie ja tuo -asetusta

Jos määrität useita tytäryhtiöitä, jotka käyttävät samoja tai samankaltaisia synkronointiasetuksia, säästäjät aikaa. Määritä toinen tytäryritys ja vie sen asetukset .xml-tiedostoon. Tiedosto sisältää kaikki asetukset, kuten taulukoiden ja kenttien yhdistämismääritykset ja suodatusehdot. Tämän jälkeen voit tuoda tiedoston seuraavalle tytäryhtiölle. Voit tuoda tai viedä asetukset käyttämällä **Päätietojen hallinnan asetukset** -sivulla **Tuonti**- tai **Vienti**-toimintoja.

## Katso myös

[Päätietojen synkronoinnin hallinta](admin-sync-master-data.md)