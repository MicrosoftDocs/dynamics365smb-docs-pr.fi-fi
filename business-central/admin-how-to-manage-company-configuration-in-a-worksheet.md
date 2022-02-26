---
title: Yrityksen määrittämisen hallinta työkirjassa
description: Määritykset-työkirja on keskitetty sijainti, jossa voit suunnitella, seurata ja tehdä yrityksen määrityksiä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 34d21b0daca39c1b7895800a5f7fbc48485c6c20
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437960"
---
# <a name="manage-company-configuration-in-a-worksheet"></a>Yrityksen määrittämisen hallinta työkirjassa
Määritykset-työkirja on keskitetty sijainti, jossa voit suunnitella, seurata ja tehdä määrityksiä. Voit luoda taulukon kunkin yrityksen osalta, jonka kanssa toimit tai luoda perusmäärityskirjan, jonka avulla voidaan määrittää useita samankaltaisia yrityksiä.  

Kokoonpanopaketin valmistelun ensimmäinen vaihe on sellaisen yrityksen valinta, jonka olet jo luonut ja muokannut omia tarpeitasi varten. Tämä yritys toimii määritysten pohjana, kun määrität kokoonpanoja uusille yrityksille. Työkirjassa määritetään taulukot, joita määritysten halutaan hallitsevan ja käsittelevän. Koska useimmilla taulukoilla [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa on suhteita tai riippuvuuksia muihin taulukoihin, tulisi liittyvät taulukot myös sisällyttää tarpeen mukaan. Nämä taulukot toimivat yhdessä rakenteena, jonka ympärille muodostetaan uusi yritys. Seuraavat vaiheet opastavat kokoonpanosi paketoinnissa ja asentamisessa.  

Voit helpottaa työsi seurantaa ja tarkastusta käyttämällä **Määrityspaketin taulukko** -tietoruutua nähdäksesi lisätietoja tietueista. Voit tarkkailla taulukoiden suhteita **Määritykseen liittyvä taulukko** -tietoruudussa.  

Seuraavissa ohjeissa näytetään, miten voit lisätä ja mukauttaa kokoonpanosi taulukoiden tietoja.  

## <a name="to-open-the-configuration-worksheet"></a>Avaa määritystyökirja  
1.  Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa yritys, joka on määrityksen pohjana, ja avaa sitten sen RapidStart Servicesin käyttöönottajien roolikeskus.  
2.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Määritystyökirja** ja valitse sitten liittyvä linkki.  

## <a name="to-add-a-table-to-the-worksheet"></a>Taulukon lisääminen työkirjaan  
1.  Valitse **Määritä työkirja** -sivulla **Muokkaa luetteloa** -toiminto.  
2.  Valitse ensimmäisen rivin **Rivityyppi**-kentässä **Taulukko**.  
4.  Valitse **Taulukon tunnus** -kentässä taulukko, johon haluat lisätä määrityksesi.  
5.  Kirjoita **Sivun tunnus** -kenttään taulukkoon liittyvän sivun tunnus. Tämä arvo on täytetty automaattisesti vakiomuotoisissa taulukoissa. Mukautetuille taulukoille on annettava tunnus.
6.  Kirjoita **Viite**-kenttään sen dokumentaatiosivun, kuten ohjeiden, URL-osoite, jolla taulukon määrittämisen parhaat käytännöt tai ohjeet ovat.  
7.  Lisää liittyviä taulukoita valitsemalla **Hae liittyvät taulukot** -toiminto.  

    > [!NOTE]  
    > Liittyviä taulukoita ei lisätä **Hae liittyvät taulukot** -toimintoon, jos jompikumpi seuraavista on tosi:
    > - Suhde on ehdollinen.  
    > Esimerkki: Jos saat liittyvät taulukot **Asiakas**-taulukolle, tällöin **Sijainti**-taulukkoa ei lisätä, koska se liittyy **Asiakas**-taulukkoon vain ehdollisesti, jos **Asiakas**-taulukon **Sijaintikoodi**-kenttä täytetään.  
    > - Liittyvä taulukko on suodatettu.  
    > Esimerkki: liittyvän taulukon kentässä on WHERE-lause. Syy tähän on se, että liittyvien suhteiden tiedot on tallennettu **Kenttä**-järjestelmän taulukkoon, joka ei ole täysin sovelluksen käytettävissä.  
    > Lisää tällaiset taulukot manuaalisesti tämän toimenpiteen vaiheen 4 ohjeiden mukaisesti.  

8.  Muokkaa taulukkoluetteloita valitsemalla taulukko, jonka haluat poistaa ja valitsemalla sitten **Poista**-toiminto.  
9. Toista vaiheet jokaiselle taulukolle, jonka haluat lisätä määritykseen.  
10. Voit poistaa taulukkotietojen kaksoiskappaleet, joita voi syntyä **Hae liittyvät taulukot** -toiminnossa, valitsemalla **Poista rivien kaksoiskappaleet** -toiminto. Tämä poistaa päällekkäisiä taulukoita, joilla on sama pakettikoodi.  

## <a name="to-add-multiple-tables-to-the-configuration-worksheet"></a>Useiden taulukoiden lisääminen määritystyökirjaan.  
1. Valitse **Hae taulukot** -toiminto. **Nouda määritystaulukot** -eräajon sivu avautuu.  
2. Määritä **Asetukset**-pikavälilehdessä määritykseen lisättävien taulukoiden tyypit seuraavassa taulukossa kuvatulla tavalla.

    |Asetus|Description|  
    |----------------------------------|---------------------------------------|  
    |**Sisällytä vain tietoja sisältävät**|Valitse valintaruutu sisällyttääksesi vain ne taulukot, jotka sisältävät tietoja. Saatat haluta sisällyttää taulukon, jossa jo määritetään ratkaisusi tukemat tavalliset maksuehdot.|  
    |**Sisällytä liittyvät taulukot**|Merkitse valintaruutu sisällyttääksesi kaikki liittyvät taulukot. Katso tämän toimenpiteen vaiheesta 3 liittyvien taulukoiden osajoukon lisääminen.|  
    |**Sisällytä dimensiotaulukot**|Merkitse valintaruutu sisällyttääksesi dimensiotaulukot.|  
    |**Sisällytä vain lisensoidut taulukot**|Valitse valintaruutu sisällyttääksesi vain taulukot, joita voit käyttöoikeutesi (jonka alaisena luot työkirjaa) mukaan käyttää.|

3. Määritä **Objekti**-pikavälilehdessä asianmukaiset suodattimet sen mukaan, minkätyyppiset taulukot haluat sisällyttää ja jättää pois.  
4. Valitse **OK**-painike. [!INCLUDE[prod_short](includes/prod_short.md)] -taulukot lisätään työkirjaan. Jokaisen luettelon tapahtumalla on rivi, jonka tyyppi on **Taulukko**.  
5. Voit poistaa taulukkotietojen kaksoiskappaleet, joita voi syntyä **Hae taulukot** -toiminnossa, valitsemalla **Poista rivien kaksoiskappaleet** -toiminto. Tämä poistaa päällekkäisiä taulukoita, joilla on sama pakettikoodi.  
6. Voit lisätä taulukoita työkirjoihin, jotka liittyvät valitsemaasi taulukkoon. Tarkasta **Liittyvät taulukot**-tietoruudun tiedot nähdäksesi, puuttuuko taulukoita. Voit lisätä tiettyyn taulukkoon liittyvät taulukot valitsemalla taulukon luettelosta ja valitsemalla sitten **Hae liittyvät taulukot** -toiminto.  

    > [!NOTE]  
    > Liittyviä taulukoita ei lisätä **Hae liittyvät taulukot** -toimintoon, jos jompikumpi seuraavista on tosi:
    > - Suhde on ehdollinen.  
    > Esimerkki: Jos saat liittyvät taulukot **Asiakas**-taulukolle, tällöin **Sijainti**-taulukkoa ei lisätä, koska se liittyy **Asiakas**-taulukkoon vain ehdollisesti, jos **Asiakas**-taulukon **Sijaintikoodi**-kenttä täytetään.  
    > - Liittyvä taulukko on suodatettu.  
    > Esimerkki: liittyvän taulukon kentässä on WHERE-lause. Syy tähän on, että suhteisiin liittyvät tiedot on tallennettu **Kenttä**-virtuaalitaulukkoon ja ne eivät ole suorituskyvystä johtuen käytettävissä sivulla kuten määritystyökirja.  
    > Lisää tällaiset monimutkaisia suhteita sisältävät liittyvät taulukot manuaalisesti kohdan [Taulukon lisääminen työkirjaan](admin-how-to-manage-company-configuration-in-a-worksheet.md#to-add-a-table-to-the-worksheet) vaiheen 4 ohjeiden mukaisesti.

7. Poista taulukoita taulukkoluettelon taulukoita valitsemalla taulukko, jonka haluat poistaa, ja valitsemalla sitten **Poista**-toiminto.  

Seuraavan menettelyn avulla voit määrittää, mitä taulukon kenttiä haluat sisällyttää. Kun olet tehnyt tämän määrityksen, voit viedä taulukon Exceliin ja käyttää taulukkorakennetta mallina asiakkaan tietojen keräämistä varten. Lisätietoja on ohjeaiheessa [Asiakastietojen siirtämisen valmisteleminen](admin-use-templates-to-prepare-customer-data-for-migration.md).  

## <a name="to-specify-a-set-of-fields-and-records-for-a-configuration-table"></a>Määritä joukko kenttiä ja tietueita konfiguraatiotaulukolle  
1. Valitse määritystaulukkoluettelosta taulukko ja valitse sitten **Muokkaa luetteloa** -toiminto.  
2. Valitse taulukko, jonka kentän tiedot haluat määrittää, ja valitse sitten **Kentät**-toiminto.  
3. Jos haluat valita vain sisällytettävät kentät, valitse **Tyhjennä sisällytetty** -toiminto. Jos haluat lisätä kaikki kentät, valitse **Aseta sisällytetty** -toiminto.  
4. Jos haluat määrittää, että kentän tietoja ei tule vahvistaa, poista **Tarkista kenttä** -valintaruudun valinta.  
5. Valitse **OK**-painike.  
6. Voit suodattaa tietyn joukon tietueita kuuluvaksi määritystyökirjaan valitsemalla **Suodattimet**-toiminnon ja määrittämällä soveltuvat suodatinarvot.

Voit luoda taulukoiden toiminta-alueita ja ryhmiä laittaaksesi samankaltaiset toiminnot yhteen. Haluat ehkä luoda määrityksen tilikartan määrityksen yhteydessä kirjaustaulukkoryhmän. Yleensä alueita käytetään ryhmittämään joukko taulukoita, jotka vastaavat toiminta-aluetta. Kukin alue voi sisältää ryhmiä. Ryhmällä voidaan järjestää taulukoita, joilla on yhteinen tarkoitus.  

Seuraavassa kuvaillaan, miten luodaan alue- ja ryhmänimityksiä ensimmäisen taulukkoluettelon luonnin jälkeen. Kun olet lisännyt nämä luokat, voit jatkaa ja lisätä ja muokata taulukoita luettelossa.  

## <a name="to-categorize-and-group-functionality-in-the-worksheet"></a>Luokittele ja ryhmitä toiminnot laskentataulukkoon  
1. Lisää alueen alussa uusi rivi työkirjaan.  
2. Valitse **Rivityyppi**-kentässä **Alue**. Kirjoita **Nimi**-kenttään alueen nimi.  
3. Lisää taulukoiden ryhmittelyn alussa uusi rivi työkirjaan.  
4. Valitse **Rivityyppi**-kentässä **Ryhmä**. Kirjoita **Nimi**-kenttään alueen nimi. Ryhmän nimet sisennetään automaattisesti.  
5. Siirrä taulukoita asianmukaiseen luokkaan valitsemalla siirrettävä taulukko ja valitsemalla sitten **Siirrä ylös**- tai **Siirrä alas** -toiminto. Voit myös poistaa työkirjan rivin ja lisätä taulukon uudelleen tarvittavaan sijaintiin.  

Jotkut [!INCLUDE[prod_short](includes/prod_short.md)] -taulukot ovat vakiomuotoisia, ja niiden tiedot eivät todennäköisesti muutu toteutusten välillä. Näin ollen asiakkaan kohdistuksen avustamiseksi voit poistaa nämä taulukot työkirjoista sen jälkeen, kun olet sisällyttänyt ne määrityspakettiin. Kun taulukot on lisätty, ne säilyvät määrityspaketin osina.  

## <a name="to-remove-a-standard-table-in-the-worksheet"></a>Siirrä vakiotaulukko työkirjassa  
Kun olet lisännyt kaikki tarvittavat taulukot kokoonpanopakettiin, määritä, mitkä taulukot eivät edellytä asiakkaan toimia.  
1.  Valitse taulukot ja poista ne valitsemalla **Poista**-toiminto.  

    > [!NOTE]  
    >  Taulukot säilytetään paketissa, vaikka ne poistetaan työkirjasta.  

## <a name="to-review-and-customize-existing-database-data"></a>Aiemmin luotujen tietokantatietojen tarkistaminen ja mukauttaminen
Kun luot kokoonpanonpaketin ratkaisua varten, voit tarkastella ja mukauttaa käytettävissä olevia tietokannan tietoja vastaamaan asiakkaan tarpeita. Tietokannan taulukolla on oltava siihen liittyvä sivu.  

## <a name="to-customize-data-in-the-database"></a>Mukauta tiedot tietokantaan  

1.  Etsi **Määritystyökirja** -sivulta taulukot, joiden tietoja haluat tarkastella tai muokata.  

    > [!NOTE]  
    >  Varmista, että jokaiseen taulukkoon on määritetty sivun tunnus. Tämä arvo on täytetty automaattisesti vakiomuotoisissa [!INCLUDE[prod_short](includes/prod_short.md)] -taulukoissa. Mukautetuille taulukoille tunnus on kuitenkin annettava.  

2.  Valitse **Tietokantatiedot**-toiminto.  

     Sivun [!INCLUDE[prod_short](includes/prod_short.md)] -sivu avautuu.  

3.  Tarkastele käytettävissä olevia tietoja Muokkaa sitä tarpeen mukaan poistamalla epäolennaiset tietueet tai lisäämällä uusia.

## <a name="see-also"></a>Katso myös  
[Yrityksen konfiguroinnin määrittäminen](admin-set-up-company-configuration.md)  
[Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]