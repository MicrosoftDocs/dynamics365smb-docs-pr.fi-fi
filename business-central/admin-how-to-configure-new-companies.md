---
title: Uusien yritysten määrittäminen | Microsoft Docs
description: Voit määrittää ja mukauttaa uuden yrityksen, joka on luotu. Tarkentaaksesi käyttöönottoa jatkat kokoonpanon suorittamista kolmessa vaiheessa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: da3fb7a171400736e2b1039368235c898deea163
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779980"
---
# <a name="configure-new-companies"></a>Uusien yritysten määrittäminen
Uusi yritys määritetään ratkaisun käyttöönottoa varten yleensä kolmen vaiheen avulla. Ensimmäisessä vaiheessa tuodaan määrityspaketti, joka on määritystiedot sisältävä .rapidstart-tiedosto. Toisessa vaiheessa muokataan määritystietoja ja käytetään niitä uudessa yrityksessä. Viimeisessä vaiheessa mahdolliset virheet tarkistetaan ja korjataan.  

Seuraavissa ohjeissa oletetaan, että olet luonut ja tallentanut kokoonpanopaketin. Lisätietoja on kohdassa [Määrityspaketin valmisteleminen](admin-how-to-prepare-a-configuration-package.md).  

Seuraavissa ohjeissa oletetaan, että olet alustanut ja avannut uuden yrityksen ja että käytössä on järjestelmänvalvojan roolikeskus.

## <a name="before-you-import-a-configuration-package"></a>Ennen määrityspaketin tuomista
Ennen kuin tuot määrityspaketin, on hyvä tarkistaa, että seuraavat lauseet toteutuvat. Muussa tapauksessa sinä tai asiakkaasi ei voi tuoda määrityspakettia.

* Käyttöoikeus sisältää päivitettävät taulut. Jos et ole varma, **Konfiguroi työkirja** voi auttaa. Jos käyttöoikeus sisältää tauluja, **Käyttöoikeudet sisältävä taulu** -valintaruutu on valittu.  
* Määrityspaketin tuovalla käyttäjällä on voimassa olevat Lisää- ja Muokkaa-oikeudet kaikkiin tauluihin, joita paketti päivittää. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md) 

## <a name="to-import-a-configuration-package"></a>Tuo paketin kokoonpano  
1. Avaa uusi yritys [!INCLUDE[prod_short](includes/prod_short.md)] -tietokannassa.  
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määrityspaketit** ja valitse sitten liittyvä linkki.  
3. Valitse **Tuo paketti** -toiminto.  
4. Siirry kohtaan, jonne määrityspaketin .rapidstart-tiedosto on tallennettu, ja valitse **Avaa**-painike.  
5. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yrityksen tiedot** ja valitse sitten liittyvä linkki. Kirjoita yrityksen tiedot yrityksen tietokorttiin. Sisällytä tietoja, kuten pankin tiedot. Voit myös lisätä yrityksen logon.  

Kaikki taulukot, jotka olet määrittänyt uuden yrityksen sisällyttämistä varten, tuodaan. Voit tässä vaiheessa soveltaa paketin tiedot tietokantaan, tai muuttaa ja muokata taulukkotietoja asiakkaan vaatimusten täyttämiseksi.  

## <a name="to-apply-package-data"></a>Käytä paketin tietoja  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määritystyökirja** ja valitse sitten liittyvä linkki.  
2. Valitse taulukko, jonka tietoja haluat muokata, ja valitse sitten **Käytä tietoja** -toiminto. Vahvista sovellus valitsemalla **Kyllä**-painike.
3. Varmista, että tiedot on nyt tietokannassa ja sovelluksen suoritus onnistui palaamalla **Määritä työkirja** -sivulle ja valitsemalla **Tietokannan tiedot** -toiminto.  

> [!NOTE]  
>  Kun otat tiedot käyttöön, näet ne vain tietokannassa. Se ei enää ole paketissa.  

## <a name="to-modify-and-apply-package-data"></a>Muokkaa ja käytä paketin tietoja  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määritystyökirja** ja valitse sitten liittyvä linkki.  
2. Valitse taulukko, jonka tietoja haluat muokata, ja valitse sitten **Paketin tiedot** -toiminto.  
3. Tee muutokset **Määritä pakettitietueet** -sivulla. Voit esimerkiksi poistaa vaihtoehdot, jotka eivät ole käytettävissä.  
4. Valitse **Käytä tietoja** -toiminto ja sitten **OK**-painike.  
5. Varmista, että tiedot on nyt tietokannassa ja sovelluksen suoritus onnistui palaamalla **Määritä työkirja** -sivulle ja valitsemalla **Tietokannan tiedot** -toiminto.  

## <a name="to-locate-and-identify-a-configuration-error"></a>Etsi ja tunnista määritysvirhe  
Ohjelmassa on tietyn tyyppisiä virheitä, jotka voivat ilmetä, kun tietoja lisätään tietokantaan. Yleisin virhe on vaadittujen liittyvien taulukoiden sisällyttämättä jättäminen. Korjaa tällaiset virheet määritystyökirjassa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määrityspaketit** ja valitse sitten liittyvä linkki.  
2. Valitse tarkistettava paketti ja valitse sitten **Muokkaa**-toiminto.  

    Virheitä sisältävät taulukot näkyvät korostettuna. Pakettivirheiden määrä näkyy **Pakettivirheiden määrä** -kentässä.  

3. Valitse **Pakettivirheiden määrä** -kenttä ja avaa **Määritä pakettitietueet** -sivu, joka sisältää virheelliset tietueet.  

### <a name="to-fix-an-error"></a>Korjaa virhe  
1. Avaa yritys, johon määrityspaketti perustuu.  
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määritystyökirja** ja valitse sitten liittyvä linkki.  
3. Korjaa virheet eli esimerkiksi lisää työkirjaan puuttuvat liittyvät taulukot.  
4. Lisää taulukot nykyiseen kokoonpanpakettiin, tai luo uusi paketti, joka sisältää vain uudet taulukot. Lisätietoja on kohdassa [Määrityspaketin valmisteleminen](admin-how-to-prepare-a-configuration-package.md).  
5. Avaa uusi yritys, jolle määritystä ollaan toteuttamassa.  
6. Tuo määrityspaketti.  

    > [!NOTE]  
    >  Jos tuota saman paketin uudelleen, kaikki aiemmin tekemäsi muutokset voidaan korvata. Tämän vuoksi haluat ehkä lisätä uusia taulukoita uuteen pakettiin ja tuoda sen.  

7. Ota tiedot käyttöön tietokannassa kohdassa [Pakettitietojen muokkaaminen ja käyttäminen](admin-how-to-configure-new-companies.md#to-modify-and-apply-package-data) ohjeiden mukaan.

## <a name="see-also"></a>Katso myös  
[Kokoonpanojen käyttäminen uusissa yrityksissä](admin-apply-configuration-to-new-companies.md)  
[Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]