---
title: Mukautusten hallinta Business Centralin järjestelmänvalvojana | Microsoft Docs
description: Lisätietoja käyttöliittymän mukauttamisesta omaan työskentelytapaan sopivaksi.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 37cdf2d7dcc46b1286cbb7a5ad620547e364309e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "910860"
---
# <a name="managing-personalization-as-an-administrator"></a>Mukautuksen hallinta järjestelmänvalvojana

 Käyttäjät voivat mukauttaa työtilansa omien mieltymystensä mukaiseksi. Järjestelmänvalvojana ohjaat ja hallitset mukauttamista seuraavasti:

-   Ottamalla koko sovelluksen mukauttamisominaisuuden käyttöön tai poistamalla sen käytöstä (vain paikalliset asetukset.)
-   Ottamalla mukauttamisominaisuuden käyttöön vain tietyn profiilin käyttäjille tai poistamalla sen heiltä käytöstä.
-   Poistamalla käyttäjien mahdollisesti tekemät sivun mukauttamiset.

## <a name="EnablePersonalization"></a>Mukauttamisen ottaminen käyttöön tai poistaminen käytöstä (vain paikallinen versio)

Mukauttamista ei ole oletusarvoisesti otettu asiakasohjelmassa käyttöön. Mukauttaminen otetaan käyttöön tai poistetaan käytöstä muokkaamalla asiakasohjelmien käytössä olevan Business Central Web Server -esiintymän määritystiedostoa (navsettings.json).

1. Voit ottaa mukauttamisen käyttöön lisäämällä seuraavan rivin navsettings.json-tiedostoon:

    ```
    "PersonalizationEnabled": "true"
    ```

    Voit poistaa mukauttamisen käytöstä poistamalla tämän rivin tai muuttamalla sen seuraavaanlaiseksi:

    ```
    "PersonalizationEnabled": "false"
    ```

    Lisätietoja navsettings.json-tiedoston muokkaamisesta on kohdassa [Navsettings.json-tiedoston muokkaaminen suoraan](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).

2. Luo ja lataa sovelluksen symboleja.

    Tämä on valinnainen vaihe, eikä mukauttaminen käyttöönottaminen edellytä sitä. Se kuitenkin varmistaa, että kehittäjien luomia uusia sivuja voidaan mukauttaa.

    1. Luo ensiksi symbolit suorittamalla finsql.exe `generatesymbolreference`-komennolla. Finsql.exe-tiedosto sijaitsee [!INCLUDE[server](includes/server.md)]- ja CSIDE (Dynamics NAV Development Environment) -asennuskansiossa. Voit luoda symbolit avaamalla komentokehotteen, muuttamalla hakemiston, johon tiedosto on tallennettu, ja suorittamalla sitten seuraavan komennon:

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    Esimerkiksi:

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    Lisätietoja on kohdassa [C/SIDE:n ja AL:n suorittaminen rinnakkainen](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).

    2. Määritä [!INCLUDE[nav_server_md](includes/nav_server_md.md)] -esiintymäksi **Ota sovelluksen symboliviittaukset käyttöön palvelimen käynnistyessä** (EnableSymbolLoadingAtServerStartup). Lisätietoja on kohdassa [Business Central Serverin määrittäminen](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).

## <a name="to-disable-personalization-for-a-profile"></a>Profiilin mukauttamisen poistaminen käytöstä

Voit estää sivujen mukauttamisen kaikilta tiettyyn profiiliin kuuluvilta käyttäjiltä.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Profiilit** ja valitse sitten liittyvä linkki.
2. Valitse luettelossa muokattava profiili.
3. Valitse **Poista mukauttaminen käytöstä** -valintaruutuja valitse sitten **OK**.

## <a name="to-clear-user-personalizations"></a>Käyttäjän mukautusten tyhjentäminen

Mukautetun sivun muutosten tyhjentäminen palauttaa sivun mukautuksia edeltävän alkuperäisen asettelun. Käyttäjien sivulle tekemät mukautukset voi tyhjentää kahdella tavalla: käyttämällä **Poista käyttäjän mukautus** -sivua tai käyttämällä **Käyttäjän mukautuskortti** -sivua.

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Käyttäjän mukautusten tyhjentäminen Poista käyttäjän mukautus -sivun avulla

Voit tyhjentää **Poista käyttäjän mukautus** -sivulla mukautukset kultakin käyttäjältä sivukohtaisesti.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poista käyttäjän mukautus** ja valitse sitten liittyvä linkki.

    Sivulla on luettelo kaikista mukautetuista sivuista ja käyttäjästä, jolle se kuuluu.

    >[!NOTE]
    > **Vanha mukautus** -sarakkeiden valintamerkki ilmaisee, että mukautus tehtiin [!INCLUDE[d365fin](includes/d365fin_md.md)]in vanhassa versiossa, jossa mukautusta käsiteltiin eri tavalla kuin nyt. Mukautus estetään näiden sivujen mukautusta yrittäviltä käyttäjiltä, elleivät he ensin valitse sivun lukituksen poistamista. Lisätietoja on kohdassa [Sivun mukauttamisen estäminen lukitsemalla](ui-personalization-locked.md).

2. Valitse ensin poistettava tapahtuma ja sitten **Poista**-toiminto.

    Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Käyttäjän mukautusten tyhjentäminen Käyttäjän mukautuskortti -sivun avulla

Voit tyhjentää **Käyttäjän mukautuskortti** -sivulla tietyn käyttäjän kaikki mukautukset. Tämä edellyttää taulukon 2000000072 **Profiili** kirjoitusoikeuksia.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän mukautus** ja valitse sitten liittyvä linkki.

    **Käyttäjän mukautus** -sivulla on luettelo kaikista käyttäjistä, joilla mahdollisesti on mukautettuja sivuja. Jos käyttäjä ei löydy luettelosta, kyseisellä käyttäjällä ei ole mukautettuja sivuja.

2. Valitse ensin käyttäjä luettelossa ja sitten **Muokkaa**-toiminto.

3. Valitse **Toiminnot**-välilehdessä **Tyhjennä mukautetut sivut**.

    Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.

## <a name="see-also"></a>Katso myös
[Työtilan mukauttaminen](ui-personalization-user.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
