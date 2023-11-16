---
title: Kustannuslaskennan määrittäminen
description: 'Ennen kuin alat käsitellä kustannuslaskentaa, sinun täytyy suorittaa asetustehtävät. Jokaisella kustannustapahtumalla täytyy olla määritettynä sekä kustannustyyppi ja joko kustannuspaikkakoodi tai kustannuskohde.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1100, 1112, 1113, 1122'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="setting-up-cost-accounting"></a>Kustannuslaskennan määrittäminen

Ennen kuin alat käsitellä kustannuslaskentaa, sinun täytyy suorittaa asetustehtävät.

## <a name="balances-between-cost-type-cost-center-and-cost-object"></a>Kustannustyypin, kustannuspaikan ja kustannusobjektin saldot

Kun määrität kustannuslaskennan, sinun on varmistettava, että kaikki tapahtumat on liitetty sekä kustannustyyppiin että kustannuspaikkaan ja kustannuskohteeseen. Tämä tarkoittaa, että jokaisella kustannustapahtumalla täytyy olla määritettynä sekä kustannustyyppi ja joko kustannuspaikkakoodi tai kustannuskohde. Tämä sääntö varmistaa, että kukin kustannustapahtuma näkyy joko kustannuspaikassa tai kustannuskohteessa, mutta ei koskaan molemmissa.  

Näin luot seuraavan kirjanpitolaskutoimituksen:  

*Kustannustyypin saldo* = *Kustannuspaikan saldo* + *Kustannuskohteen saldo*  

Kun tulostat Kustannustyyppikaavion, kustannuspaikkakaavion ja kustannuskohteiden raporttikaavion, voit analysoida tämän suhteen.

## <a name="setting-up-cost-types"></a>Kustannustyyppien määrittäminen

Kustannustyyppikartta vastaa pääkirjanpidon tilikarttaa. Voit määrittää kustannustyyppikaavion seuraavilla tavoilla:  

- Kustannustyyppien kaavioiden rakenne vastaa pääkirjanpidon tuloslaskelmatilejä. Sitten voit siirtää kirjanpidon tilikartan kustannustyyppikaavioon. Siirron jälkeen voit tehdä tarvittavat muutokset.  
- Luo uusi kustannustyyppien kaavio tai lisää uudet kustannustyypit aiemmin luotuun kustannustyyppien kaavioon. Sinun on luotava jokainen uusi kustannustyyppi erikseen.  

### <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Siirrä pääkirjanpidon tilikartta kustannustyyppikaavioon

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kustannustyyppikartta** ja valitse sitten vastaava linkki.  
2. Valitse **Hae kustannustyypit tilikartasta** -toiminto. Vahvista siirto valitsemalla valintaikkunassa **Kyllä**. Funktio käyttää tilikarttaa kustannustyyppikaavion luontiin.  

    Kustannustyyppikaavio sisältää nyt kaikki pääkirjanpidon tuloslaskelmat, mukaan lukien otsikot ja välisummat. Voit tarvittaessa muuttaa kustannustyyppejä. Voit esimerkiksi poistaa kustannustyyppien kaksoiskappaleet.  

    > [!IMPORTANT]  
    >  **Rekisteröi kustannustyypit tilikartassa** -toiminto päivittää tilikartan ja kustannustyyppukaavion välisen suhteen. **Nro**-kenttä on täytetty ja vahvistettu, että jokaiselle KP-tilille on liitetty vain yksi kustannuslaji. Toiminto suoritetaan automaattisesti ennen KP-tapahtumien siirtämistä kustannuslaskentaan.  

### <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a>Uuden kustannustyypin määrittäminen Kustannustyyppikartta-sivulla

1. Avaa **Kustannustyyppikartta**-sivu muokkaustilassa.  
2. Täytä kentät tarvittaessa ohjeiden mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Voit määrittää ja ylläpitää kustannustyyppejä joko **Kustannustyypin kortti**- tai **Kustannustyyppikartta**-sivulla. Tässä toimenpiteessä määrität kustannustyypit **Kustannustyyppikartta**-sivulla.

3. Kun olet luonut kaikki kustannustyypit, valitse **Sisennä kustannustyypit** -toiminto. Valitse valintaikkunassa **Kyllä**.  
4. Linkitä uusi kustannustyyppi vastaavalle pääkirjanpidon tilille.  

    > [!IMPORTANT]  
    >  Jos olet antanut määritelmiä **Loppusumma**-rivien **Summausväli**-kentissä ennen **Sisennä kustannustyypit** -toiminnon suorittamista, määritelmät on annettava uudelleen, koska toiminto korvaa kaikki **Loppusumma**-kenttien arvot.  

### <a name="to-update-cost-types"></a>Päivitä kustannustyypit

1. Valitse **Kustannuslaskennan asetukset** -sivulla, haluatko kustannustyyppikaavion päivittyvän automaattisesti, kun tilikarttaa muutetaan.  
2. Voit tehdä **Tasaa KP-tili** -kentässä valinnan seuraavista vaihtoehdoista:  

- **Ei tasausta** - Vastaavaa muutosta ei tehdä kustannustyyppikaaviossa, kun tilikarttaa muutetaan.  
- **Automaattinen** - Vastaava muutos tehdään kustannustyyppikaaviossa, kun muutat tilikartan.  
- **Kysy** - Näkyviin tulee sanoma, jossa kysytään, haluatko tehdä vastaavan muutoksen kustannustyyppien kaaviossa, kun muutat tilikarttaa.

## <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Pääkirjanpitotilien ja kustannustyyppien välisen suhteen määrittäminen

Kustannustyypin ja KP-tilin välinen suhde luodaan kustannustyypissä ja KP-tilillä.  

- **Kustannustyyppi**-taulukon **KP-tilien väli** -kenttä osoittaa, mitkä KP-tilit kuuluvat millekin kustannustyypille.  
- **Saldokustannustyypin numero** -kenttä tilikartassa osoittaa, mitkä KP-tilit kuuluvat millekin kustannustyypille.  

Nämä kaksi kenttää täytetään automaattisesti, kun käytät **Hae kustannustyypit tilikartasta** -toimintoa.  

### <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Pääkirjanpitotilien ja kustannustyyppien välinen suhde.

Pääkirjanpitotilien ja kustannustyyppien välissä on olemassa n:1-suhde. Useita pääkirjanpitotilejä voi kuulua yhdelle kustannustyypille, mutta jokainen pääkirjanpitotili kuuluu vain yhdelle kustannustyypille. Seuraava taulukko kuvaa suhteen yksityiskohtia.  

|Suhde|**KP-tilien väli**|**Kustannustyypin numero**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Yksi pääkirjanpidon tilin kullekin kustannustyypille|kirjanpitotili.|Yksi kustannuslaji|  
|Useita kirjanpitotilejä yhdelle kustannustyypille|Kirjanpitotiliväli, kuten 7110–7193 jokaisen kirjanpitotilin kohdalla|Alueen kaikille pääkirjanpidon tileillä on vain yksi kustannustyyppi|  
|Kustannustyypit ilman vastaavia pääkirjanpitotilejä|\<Empty\>||  
|Kirjanpitotilit, joiden tapahtumia ei siirretä||\<Empty\>|  

### <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Kustannustyypit ilman suhdetta pääkirjanpitoon

Kustannuksen tyypillä ei ehkä ole yhteyttä pääkirjanpidon tileille, jos jokin seuraavista ehdoista toteutuu:  

- Operatiivisen kirjanpidon tilit, kuten kortin laskenta ja poistot, ottavat kustannukset vain operatiivisesta kirjanpidosta.  
- Auttavia kustannustyyppejä, kuten [!INCLUDE[prod_short](includes/prod_short.md)] -tietokannassa olevia tyyppejä 9901, 9902 ja 9903, käytetään kredit- ja debet-tileinä kohdistuksissa.  
- Auttava tili, 9920 [!INCLUDE[prod_short](includes/prod_short.md)] -tietokannassa, sisältää todellisia kertymiä, jotka näyttävät kustannusten ja KP-kulujen eron.

## <a name="setting-up-cost-centers"></a>Kustannuspaikkojen määrittäminen

Kustannuspaikat ovat osastoja, jotka vastaavat tuloista ja menoista. Kustannuspaikkakaavio vastaa pääkirjanpidon dimensiotietoja. Voit määrittää kustannuspaikkakaavion seuraavilla tavoilla:  

- Siirrä dimensioarvot pääkirjanpidosta kustannuspaikkakaavioon. Siirron jälkeen voit tehdä tarvittavat muutokset.  
- Luo uusi kustannuspaikan kaavio, joka on riippumaton pääkirjanpidosta, tai lisää uusi kustannuspaikka nykyiseen kustannuspaikan kaavioon. Sinun on luotava kukin kustannuspaikka erikseen.  

### <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Dimensioarvojen siirtäminen pääkirjanpidosta kustannuspaikkakaavioon

1. Määritä dimensio kustannuspaikan dimensioksi **Päivitä kustannuslaskennan dimensiot** -sivulla. Vain tämän dimension arvot siirretään.  
2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kustannuspaikkakartta** ja valitse sitten vastaava linkki.  
3. Valitse **Toiminnot**-välilehden **Funktiot**-ryhmässä **Nouda kustannuspaikat dimensiosta**, jolloin dimensioarvot siirretään kustannuspaikkakaavioon. Toiminto siirtää kohdassa 1 määritetyt dimensioarvot.  

    > [!NOTE]  
    >  Voit määrittää **Tasaa kustannuspaikan dimensio** -kentän määrittämään yksisuuntaisen dimensioarvojen synkronoinnin kirjanpidosta kustannuspaikkakaavioon. Et voi määrittää kaavion kustannuspaikkojen synkronointia dimensioarvoihin pääkirjanpidossa.  

Kustannuspaikkakaavio sisältää nyt kaikki pääkirjanpidossa määritetyt dimensioarvot, mukaan lukien otsikot ja välisummat.  

### <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a>Uuden kustannuspaikan luominen Kustannuspaikkakartta-sivulla

Voit määrittää ja ylläpitää kustannuspaikkoja joko **Kustannuspaikan kortti** -kortissa tai **Kustannuspaikkakartta**-sivulla. Tässä toimenpiteessä määrität kustannuspaikat **Kustannuspaikkakartta**-sivulla.  

1. Avaa **Kustannuspaikkakartta**-sivu muokkaustilassa.  
2. Anna kustannuspaikkakoodi **Koodi**-kentässä. Kaikilla kustannuspaikoilla on oltava koodi.  
3. Syötä kustannuspaikan nimi **Nimi**-kenttään.  
4. Määritä kustannuspaikan tarkoitus valitsemalla avattava nuoli **Rivityyppi**-kentässä.  

    - **Summa**-tyyppisten kustannuspaikkojen osalta sinun täytyy täyttää **Summausväli**-kenttä. Määritä kustannuspaikkojen alueet **tai**-operaattorin avulla. Se on pystysuora viiva (**&#124;**).  
    - Jos kustannuspaikan rivityyppi on **Loppusumma**, kenttä täytetään automaattisesti, kun käytössä on sisennystoiminto.  
5. Täytä **Lajittelujärjestys** ja **Kustannuksen alityyppi** -kentät.  
6. Napsauta seuraavaa tyhjää riviä uuden kustannuspaikan määrittämistä varten. Toista sitten vaiheet 2-5.  
7. Kun olet määrittänyt kaikki kustannuspaikat, valitse **Sisennä kustannuspaikat** -toiminto. Valitse **Kyllä**-painike.  

> [!IMPORTANT]  
> Jos olet antanut määritelmiä **Loppusumma**-kustannuspaikkojen **Summausväli**-kenttiin ennen sisennyksen suorittamista, määritelmät on annettava uudelleen. Toiminto korvaa kaikki **Loppusumma**-kentän arvot.

## <a name="setting-up-cost-objects"></a>Kustannuskohteiden määrittäminen

Kustannuskohteet ovat yrityksen projekteja, tuotteita tai palveluja. Kustannuskohdekaavio vastaa pääkirjanpidon dimensiotietoja. Voit määrittää kustannuskohdekaavion seuraavilla tavoilla:  

* Siirrä dimensioarvot pääkirjanpidosta kustannuskohdekaavioon. Siirron jälkeen voit tehdä tarvittavat muutokset.  
* Luo uusi kustannuskohteen kaavio, joka on riippumaton pääkirjanpidosta, tai lisää uusi kustannuskohde nykyiseen kustannuskohteiden kaavioon. Sinun on luotava kukin kustannuskohde erikseen.  

### <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Dimensioarvojen siirtäminen pääkirjanpidosta kustannuskohdekaavioon

1.  Määritä dimensio kustannuskohteen dimensioksi **Päivitä KL-dimensiot** -sivulla. Vain tämän dimension arvot siirretään.  
2.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kustannuskohdekartta** ja valitse sitten vastaava linkki.  
3.  Valitse **Nouda kustannuskohteet dimensiosta** -toiminto, jolla dimensioarvot siirretään kustannuskohdekaavioon. Toiminto siirtää kohdassa 1 määritetyt dimensioarvot.  

    > [!NOTE]  
    >  Voit määrittää **Tasaa kustannuskohteen dimensio** -kentän määrittämään yksisuuntaisen dimensioarvojen synkronoinnin kirjanpidosta kustannuskohdekarttaan. Et voi määrittää kaavion kustannuskohteiden synkronointia dimensioarvoihin pääkirjanpidossa.  

Kustannuskohdekaavio sisältää nyt kaikki pääkirjanpidossa määritetyt dimensioarvot, mukaan lukien otsikot ja välisummat.  

### <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>Uuden kustannuskohteen luominen Kustannuskohdekartta-sivulla

Voit määrittää ja ylläpitää kustannuskohteita joko **Kustannuskohteen kortti** -kortissa tai **Kustannuskohdekartta**-sivulla. Tässä toimenpiteessä määrität kustannuskohteet **Kustannuskohdekartta**-sivulla.  

1.  Avaa **Kustannuskohdekartta**-sivu muokkaustilassa.  
2.  Anna kustannuskohdekoodi **Koodi**-kentässä. Kaikilla kustannuskohteilla on oltava koodi.  
3.  Syötä kustannuskohteen nimi **Nimi**-kenttään.  
4.  Valitse avattava nuoli **Rivityyppi**-kentässä määrittämään kustannuskohteen tarkoitus.  

    * Jos kustannuskohteiden rivityyppi on **Yhteensä**, anna arvo **Summan lähde/kohde** -kenttään. Käytä **tai**-operaattoria, joka on pystysuora viiva (**&#124;**) kustannuskohteiden alueiden määrittämiseen.  
    * Jos kustannuskohteiden rivityyppi on **Loppusumma**, kenttä täytetään automaattisesti, kun käytössä on sisennystoiminto.  
5.  Täytä **Lajittelujärjestys**-kentän tiedot.  
6.  Napsauta seuraavaa tyhjää riviä uuden kustannuskohteen määrittämistä varten. Toista sitten vaiheet 2-5.  
7.  Kun olet määrittänyt kaikki kustannuskohteet, valitse **Sisennä kustannuskohteet** -toiminto. Valitse **Kyllä**-painike.  

> [!IMPORTANT]  
>  Jos olet antanut määritelmiä **Loppusumma**-kustannuskohteiden **Summan lähde/kohde** -kenttiin ennen sisennyksen suorittamista, määritelmät on annettava uudelleen. Toiminto korvaa kaikki **Loppusumma**-kentän arvot.

## <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Kustannuspaikkojen ja kustannuskohteiden määrittäminen tilikarttaan

Voit siirtää kulu- ja tuottotapahtumat automaattisesti pääkirjanpidosta kustannuslaskentaan joko jokaisen pääkirjanpidon kirjauksen tai eräajon yhteydessä. Kun teet siirron, [!INCLUDE[prod_short](includes/prod_short.md)] vain siirtää tapahtumat, jotka on jo linkitetty kustannuspaikkaan tai kustannuskohteeseen. Muodosta mielekäs siirto varmistamalla, että kustannuspaikat ja kustannuskohdeet on asianmukaisesti määritetty.  

### <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Dimension oletusarvojen määrittäminen pääkirjanpitotilejä varten

Voit määrittää kunkin pääkirjanpidon tilin dimension oletusarvot **Oletusdimensio**-taulukossa. Seuraavassa esimerkissä näytetään, miten määritetään, että KP-tilin kirjauksia tehdessä tulee aina olla OSASTO-kustannuspaikka eikä koskaan PROJEKTI-kustannuskohde.  

|**Dimensiokoodi**|**Arvon kirjaaminen**|  
|------------------------------------------|-----------------------------------------|  
|Osaston|Koodi pakollinen|  
|Projektin|Ei koodia|  

### <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Dimensioarvojen määrittäminen yleiskustannuksille ja suorille kustannuksille

 Voit siirtää yleiskustannukset kustannuspaikkaan ja suorat kustannukset kustannuskohteeseen. Seuraavassa taulukossa näytetään dimension asetusarvojen optimaalinen yhdistelmä.  

|Siirrä kohteeseen|Kustannuspaikan kirjaus|Kustannuskohteen kirjaus|  
|-----------------|-------------------------|-------------------------|  
|Kustannuspaikka|Koodi pakollinen|Ei koodia|  
|Kustannuskohde|Ei koodia|Koodi pakollinen|  

> [!NOTE]  
>  Varmista, että kirjanpitoon ennalta määritetty kustannuspaikka ja kustannusobjekti siirretään automaattisesti kustannuslaskentaan, valitsemalla **Tarkista KP-kirjaukset** -valintaruutu Kustannuslaskennan asetukset -sivulla.

## <a name="see-also"></a>Katso myös

[Kustannuslaskenta](finance-manage-cost-accounting.md)  
[Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md)  
[Kustannusten määrittäminen ja kohdistaminen](finance-define-and-allocate-costs.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
