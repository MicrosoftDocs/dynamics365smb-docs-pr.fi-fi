---
title: Käyttäjien ja roolien hallinta | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten Business Central -sovelluksen käyttäjiä ja roolikeskuksia hallitaan.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 10/24/2018
ms.author: edupont
ms.openlocfilehash: 7ecd8a5ad2b321d4d1683047e70ede90c7ce229f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "796002"
---
# <a name="understanding-users-profiles-and-role-centers"></a>Tietoja käyttäjistä, profiileista ja roolikeskuksista

[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa järjestelmänvalvoja lisää käyttäjät ja antaa käyttäjille [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen niiden alueiden käyttöoikeuden, joita käyttäjät tarvitsevat työssään.  

Toimintojen käyttöä hallitaan *käyttäjäryhmien* ja *profiilien* avulla. Järjestelmänvalvojana voit lisätä ja poistaa käyttäjiä [!INCLUDE[d365fin](includes/d365fin_md.md)] -tilauksesta. Voit myös määrittää käyttäjien oikeuksia käyttäjäryhmien avulla.  

## <a name="adding-users"></a>Käyttäjien lisääminen

Käyttäjiä voi lisätä [!INCLUDE[d365fin](includes/d365fin_md.md)] online -versioon sen jälkeen, kun yrityksen Office 365:n järjestelmänvalvoja on ensin luonut käyttäjät Office 365:n hallintaportaalissa. Lisätietoja on kohdassa [Käyttäjien lisääminen Office 365 for Businessiin](https://aka.ms/CreateOffice365Users).

Tämän jälkeen järjestelmänvalvoja voi määrittää käyttöoikeudet kullekin käyttäjälle ja käyttäjäryhmälle. Lisätietoja on kohdassa [Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).  

Käyttäjän tehokkaimmat käyttöoikeudet SUPER-käyttöoikeusjoukko. Jokaisella yrityksellä on oltava ainakin yksi käyttäjä, jolla on tämä käyttöoikeusjoukko. Parhaan käytännön mukaista on kuitenkin antaa jokaiselle käyttäjälle hänen [!INCLUDE[prodshort](includes/prodshort.md)]in käyttötarpeitaan vastaavat käyttöoikeudet. Tämä auttaa varmistamaan, että käyttäjillä on vain niiden tietojen käyttöoikeus, joita he tarvitsevat esimerkiksi työssään.  

> [!TIP]
> On parhaan käytännön mukaista varmistaa, että Office 365:n järjestelmänvalvojalla on myös [!INCLUDE[prodshort](includes/prodshort.md)]in SUPER-käyttöoikeusjoukko, koska se helpottaa hallintatehtäviä, kuten integraation määrittämistä muiden sovellusten kanssa.

### <a name="users-of-on-premises-deployments"></a>Paikallisten käyttöönottojen käyttäjät

Järjestelmänvalvoja voi valita käyttäjille [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen paikallisten käyttöönottojen eri tunnistetietojen mekanismeista. Kun olet luonut käyttäjän, annat eri tietoja riippuen tunnistetiedoista, joita käytät tietyssä [!INCLUDE[server](includes/server.md)] -ilmentymässä. Lisätietoja on [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen kehittäjän ja ITPro-sisällön järjestelmänvalvojan osan [Todennus ja tunnistetietotyypit](/dynamics365/business-central/dev-itpro/administration/users-credential-types) -kohdassa.  

## <a name="profiles"></a>Profiilit

Kaikilla yrityksen henkilöille, joilla on [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeus, on määritetty *profiili*, jonka mahdollistaa *roolikeskuksen* käytön.

Profiilit ovat niiden [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjien kokoelmia, jotka jakavat saman roolikeskuksen. Roolikeskus on [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen aloituskohta ja kotisivu. Sen avulla tärkeimpien tehtävien aloitus on nopeaa ja se sisältää paljon tietoja työstä, mukaan lukien työn suorituskykyilmaisimet.  

> [!NOTE]  
>  Et voi lisätä, muokata tai poistaa profiileja nykyisessä [!INCLUDE[d365fin](includes/d365fin_md.md)] online -versiossa.  

### <a name="CreateProfile"></a> Profiilin luonti

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Profiililuettelo** ja valitse sitten aiheeseen liittyvä linkki.  

2.  Avaa **Uusi profiilikortti** -sivu valitsemalla **Profiililuettelo**-sivulla **Uusi**-toiminto.  

3.  Anna **Profiilin tunnus** -kentässä nimi, joka kuvaa käyttäjien tarkoitettua roolia.  

4.  Kirjoita **Kuvaus**-kenttään profiilitunnuksen kuvaus, esimerkiksi **Tilausten käsittelijä**.  

5.  Määritä **Roolikeskuksen tunnus** -kenttäään profiiliin liitettävä roolikeskus.  

Olemassa olevan profiilin muokkaaminen tapahtuu samalla tavalla. Ainoa ero on, että **Profiililuettelo**-sivulla valitaan olemassa oleva profiili **Uusi**-toiminnon sijaan.  


### <a name="copy-a-profile"></a>Profiilin kopioiminen
Profiilin kopioiminen voi säästää aikaa, jos haluat käyttää profiilissa samanlaisia asetuksia, ja haluat muuttaa vain joitakin asetuksia.

1.  Avaa kopioitava profiili ja valitse sitten **Kopioi profiili** -toiminto.

2.  Syötä **Uuden profiilin tunnus** -kenttään sen profiilin nimi, jonka haluat kopioida.

3.  Määritä **Uuden profiilin alue** -kenttään jokin seuraavista arvoista:

    - **Järjestelmä**, kun haluat määrittää uuden profiilin kaikkien sovellusta käyttävien vuokraajatietokantojen käytettäväksi.
    - **Vuokraaja**, kun haluat määrittää profiilin vain nykyisen vuokraajatietokannan käytettäväksi.
4. Valitse **OK**-painike, kun olet valmis.

### <a name="ExportImportProfile"></a>Profiilien vienti ja tuonti

Voit viedä profiileja XML-tiedostoina [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietokantaan ja tuoda niitä tietokannasta. Profiilin vieminen ja tuominen voi säästää aikaa, kun määrität käyttöliittymää. Voit käyttää aiemmin luotua profiilimääritystä sen sijaan, että määrittäisit profiilin alusta alkaen. Jos profiili on määritetty [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietokannassa ja haluat käyttää sen tai osan samasta profiilimäärityksestä uudelleen toisessa tietokannassa, voit viedä profiilin XML-tiedostoon. Tämän jälkeen voit tuoda profiilin XML-tiedoston toiseen tietokantaan.

-   Voit viedä profiilin joko valitsemalla **Vie profiilit** -toiminto **Profiililuettelo**- tai **Profiilikortti**-sivulla tai etsimällä sen ja avaamalla **Vie profiilit** -sivun. Tallenna XML-tiedosto tietokoneelle tai verkkoon.

-   Voit tuoda profiilin joko valitsemalla **Tuo profiilit** -toiminto **Profiililuettelo**-sivulla tai etsimällä sen ja avaamalla **Tuo profiilit** -sivun. 

    > [!NOTE]  
    >  Et voi tuoda profiilia, joka on jo tietokannassa, vaikka XML-tiedosto olisi eriniminen tai sillä olisi eri sisältö. Poista olemassa oleva profiili ennen kuin tuot uuden profiilin.


## <a name="configuration-and-personalization"></a>Kokoonpano ja mukautus
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

Käyttäjät voivat mukauttaa henkilökohtaisen versionsa käyttöliittymää mukauttamalla käyttöliittymää oman kirjautumistunnuksensa osalta. Järjestelmänvalvoja voi poistaa tämän mukautuksen. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).  

## <a name="see-also"></a>Katso myös  
[Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)  
[Mukautuksen hallinta järjestelmänvalvojana](ui-personalization-manage.md)  
[Työtilan mukauttaminen](ui-personalization-user.md)  
