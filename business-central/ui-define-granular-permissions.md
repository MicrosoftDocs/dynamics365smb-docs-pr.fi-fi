---
title: Määritä hajautetut käyttöoikeudet
description: 'Tässä artikkelissa kuvataan, kuinka määritellään yksityiskohtaiset käyttöoikeudet ja määritetään kullekin käyttäjälle käyttöoikeusjoukot, joita he tarvitsevat työnsä suorittamiseen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
ms.service: dynamics-365-business-central
---

# Määritä käyttöoikeudet käyttäjille ja ryhmille

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

[!INCLUDE[prod_short](includes/prod_short.md)]-suojausjärjestelmä ohjaa, mitä objekteja käyttäjä voi käyttää kussakin tietokannassa tai ympäristössä yhdessä käyttäjän käyttöoikeuden kanssa. Voit määrittää kaikille käyttäjälle, voivatko he lukea, muokata tai syöttää tietoja tietokantaobjekteissa. Lisätietoja on kohdan [Tietosuoja](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) sovelluksen [!INCLUDE[prod_short](includes/prod_short.md)] kehitys- ja hallintosisällössä.

Ennen kuin määrität käyttöoikeuksia käyttäjille ja käyttäjäryhmille, sinun täytyy määrittää, ketkä voivat kirjautua sisään luomalla käyttäjiä heidän käyttöoikeutensa mukaisesti. Katso lisätietoja kohdasta [Luo käyttäjiä lisenssien mukaan](ui-how-users-permissions.md).

[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa tietokantaobjektien käyttöoikeustasoja on kaksi:

- Käyttöoikeuden mukaiset yleiset käyttöoikeudet, joita kutsutaan myös oikeutuksisi.

  Käyttöoikeuksiin kuuluvat käyttöoikeuksien oletusjoukot. Vuoden 2022 julkaisuaallosta 1 alkaen järjestelmänvalvojat voivat mukauttaa näitä oletusoikeuksia asianmukaisille käyttöoikeustyypeille. Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen käyttöoikeuksien perusteella](ui-how-users-permissions.md#licensespermissions).  

- Yksityiskohtaiset käyttöoikeudet, jotka määritetään kohdassa [!INCLUDE[prod_short](includes/prod_short.md)].

Tässä artikkelissa kuvataan, miten voit määrittää, käyttää ja hakea käyttöoikeuksia sovelluksessa [!INCLUDE [prod_short](includes/prod_short.md)] oletusmääritysten muuttamiseksi.  

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]  
Lisätietoja hallintasisällössä: [Valtuutettu järjestelmänvalvojan käyttöoikeus Business Central Onlineen](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

[!INCLUDE [prod_short](includes/prod_short.md)] online sisältää oletuskäyttäjäryhmät, jotka on määritetty käyttäjille automaattisesti käyttöoikeuden perusteella. Voit muuttaa oletusmäärityksiä muuttamalla tai lisäämällä suojausryhmiä, käyttöoikeuksien joukkoja ja käyttöoikeuksia. Seuraavassa taulukossa on esitelty oletuskäyttöoikeuksien muokkaamiseen liittyvät keskeiset skenaariot.  

|Tehtävä  |Katso  |
|---------|---------|
|Voit helpottaa useiden käyttäjien käyttöoikeuksien hallintaa järjestämällä ne suojausryhmiin ja määrittämällä sitten yhden toiminnon useille käyttäjille yhden käyttöoikeusjoukon tai muuttamaan sitä.| [Käyttöoikeuksien hallinta käyttäjäryhmien avulla](#to-manage-permissions-through-user-groups) |
|Käyttöoikeuksien joukkojen hallinta tiettyjen käyttäjien osalta | [Käyttöoikeusjoukkojen määrittäminen käyttäjälle](#to-assign-permission-sets-to-users) |
|Lisätietoja käyttöoikeuksien joukon määrittämisestä|[Käyttöoikeuksien joukon luominen](#to-create-a-permission-set)|
|Käyttäjän käyttöoikeuksien tarkasteleminen tai vianmääritys|[Yleiskuvan saaminen käyttöoikeuksista](#to-get-an-overview-of-a-users-permissions)|
|Tietoja tietuetason suojauksesta|[Suojaussuodattimet rajoittavat käyttäjän käyttöoikeuden tiettyihin taulukon tietueisiin](#security-filters-limit-a-users-access-to-specific-records-in-a-table)|

> [!NOTE]
> Selkeä tapa määrittää, mitä ominaisuuksia käyttäjällä on oikeus käyttää, on valita asetus **Kokemus**-kentässä **Yritystiedot**-sivulla. Lisätietoja on kohdassa [Näytettävien ominaisuuksien muuttaminen](ui-experiences.md).
>
> Voit myös määrittää ominaisuudet, jotka ovat käyttäjien käytettävissä käyttöliittymässä ja sen, miten he käyttävät niitä sivuilla. Se tehdään profiilien avulla ja nämä määritetään eri käyttäjätyypeille heidän työnsä tai osastonsa mukaisten roolien mukaan. Lisätietoja on kohdissa [Profiilien hallinta](admin-users-profiles-roles.md) ja [[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen](ui-customizing-overview.md).

## Käyttöoikeuksien joukon luominen

> [!NOTE]
> Vuoden 2022 2. julkaisuaallossa helpotettiin käyttöoikeuksien lisäämistä käyttöoikeuksien joukkoon. Käyttöoikeuksien yksittäisen lisäämisen sijaan voit lisätä kokonaisia käyttöoikeuksien joukkoja. Tarvittaessa voit sulkea pois yksittäisiä käyttöoikeuksia niistä. Lisätietoja on kohdassa [Muiden käyttöoikeuksien joukkojen lisääminen](#to-add-other-permission-sets). Jotta tämä olisi mahdollista, korvasimme Käyttöoikeuksien joukko -sivun uudella sivulla. Tärkeimmät erot ovat uudet **Käyttöoikeuksien joukot** ja **Tulokset**-ruutu sekä **Sisällytetyt käyttöoikeudet**-tietoruutu. Jos haluat jatkaa korvatun Käyttöoikeudet-sivun käyttämistä, valitse **Käyttöoikeuksien joukot** -sivulla **Käyttöoikeudet (vanha)** -toiminto.

Ylläpito on myös aiempaa helpompaa. Kun lisäät järjestelmän käyttöoikeuden, käyttäjän määrittämä käyttöoikeuksien joukko päivitetään automaattisesti Microsoftin mahdollisesti näihin käyttöoikeuksiin tekemien muutosten kanssa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöoikeuksien joukot** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat uuden rivin kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **Käyttöoikeudet**-toiminto.
5. Sisällytä **Käyttöoikeuksien joukko** -sivun **Tyyppi**-kenttään objektin käyttöoikeudet tai sulje ne pois seuraavasti:

  Jos haluat sisällyttää käyttöoikeuden, valitse **Sisällytä** ja valitse sitten käyttöoikeustaso **Lukuoikeus**-, **Lisäysoikeus**-, **Muokkausoikeus**-, **Poisto-oikeus** ja **Suoritusoikeus**-kentän avulla. Asetukset kuvaillaan seuraavassa taulukossa.

  |Asetus|Kuvaus|Luokittelu|
  |------|-----------|-------|
  |**Tyhjä**|Käyttäjä voi suorittaa objektille toiminnon.|Pienin|  
  |**Kyllä**|Käyttäjä ei voi suorittaa objektille toimintoa.|Suurin|
  |**Epäsuora**|Käyttäjä voi suorittaa objektille toiminnon, mutta vain toisen sellaisen liittyvän objektin kautta, jonka täydet käyttöoikeudet käyttäjällä on. Lisätietoja on tämän artikkelin kohdassa [Esimerkki - epäsuora käyttöoikeus](#example---indirect-permission) ja kehitys- ja IT-ammattilaisten ohjeiden kohdassa [Käyttöoikeudet - ominaisuus](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property#example---indirect-permission).|Toiseksi korkein|
  
  Jos haluat sulkea pois käyttöoikeuden tai vähintään yhden käyttöoikeustason, valitse **Sulje pois** ja valitse myönnettävä käyttöoikeustaso. Asetukset kuvaillaan seuraavassa taulukossa.

  |Asetus|Kuvaus|
  |------|-----------|-------|
  |**Tyhjä**|Käytä käyttöoikeustasoa joukon käyttöoikeuksien hierarkian perusteella.  |
  |**Sulje pois**|Poista objektin tietty käyttöoikeustaso.|
  |**Vähennä epäsuoraksi**|Muuta käyttöoikeustasoksi Epäsuora, jos jokin käyttöoikeuksien joukko antaa objektin suoran käyttöoikeuden. Valitse tämä asetus esimerkiksi silloin, kun käyttöoikeuksien joukko antaa KP-tapahtumien suoran käyttöoikeuden, mutta et halua käyttäjillä olevan tapahtumien kaikkia käyttöoikeuksia.|
  
  > [!NOTE]
  > Jos käyttöoikeus sisältyy käyttöoikeusjoukkoon ja se on myös poissuljettu käyttöoikeusjoukko, käyttöoikeus ohitetaan.

6. Määritä **Objektin tyyppi**- ja **Objektin tunnus** -kentissä objekti, jolle annetaan käyttöoikeus.

  > [!TIP]
  > Oletusarvot näkyvät uusilla riveillä. Esimerkiksi **Objektin tyyppi** -kentässä on arvo **Taulukon tiedot** ja **Objektin tunnus** -kentässä arvo **0**. Oletusarvot ovat vain paikkamerkkejä, eikä niitä voi käyttää. Valitse objektin tyyppi ja objekti **Objektin tunnus** -kentässä ennen kuin luot toisen uuden rivin.

7. Valinnainen: Jos määrität Taulukon tiedot -tyyppiselle objektille käyttöoikeudet, **Suojaussuodatin**-kentässä voit suodattaa tiedot, joita käyttäjä voi käyttää valitun taulukon kentissä. Voit antaa käyttäjälle esimerkiksi vain niiden tietueiden käyttöoikeuden, joissa on tietoja tietystä asiakkaasta. Lisätietoja on kohdissa [Suojaussuodattimet rajoittavat käyttäjän käyttöoikeutta tiettyihin taulukon tietueisiin](#security-filters-limit-a-users-access-to-specific-records-in-a-table) ja [Suojaussuodattimien käyttäminen](/dynamics365/business-central/dev-itpro/security/security-filters).
8. Valinnainen: Lisää **Käyttöoikeuksien joukot** -ruudussa vähintään yksi käyttöoikeuksien joukko. Lisätietoja on kohdassa [Muiden käyttöoikeuksien joukkojen lisääminen](#to-add-other-permission-sets).

> [!IMPORTANT]
> Käytä harkintaa, kun määrität **Lisäysoikeus**- tai **Muokkausoikeus**-oikeuksia **9001-käyttäjäryhmän jäsenelle** tai **9003-käyttäjäryhmän käyttöoikeusjoukolle**. Kaikki käyttöoikeuksien joukkoon liitetyt käyttäjät voivat mahdollisesti määrittää itsensä muihin käyttäjäryhmiin, mikä puolestaan voi antaa heille tahattomia käyttöoikeuksia.

### Esimerkki - epäsuora käyttöoikeus

Voit määrittää epäsuoran käyttöoikeuden, jos käyttäjä voi käyttää objektia, mutta vain toisen objektin kautta. Käyttäjällä voi olla esimerkiksi oikeus ajaa codeunit 80, myynti kirjattu. Codeunit Myynti kirjattu suorittaa useita tehtäviä, myös muokkaa taulukkoa 37, Ostorivi. Kun käyttäjä kirjaa myyntiasiakirjan Myynti kirjattu -codeunitin avulla, [!INCLUDE[prod_short](includes/prod_short.md)] tarkistaa, onko käyttäjällä oikeus muokata Myyntirivi-taulukkoa. Jos ei, codeunit ei voi suorittaa tehtäviä ja käyttäjä saa virhesanoman. Tällöin codeunitin suorittaminen onnistuu.

Käyttäjällä ei kuitenkaan tarvitse olla Ostorivi-taulukon täysiä käyttöoikeuksia codeunitin suorittamiseksi. Jos käyttäjällä on Myyntirivi-taulukon Epäsuora-käyttöoikeus, Myynti kirjattu -codeunitin suorittaminen onnistuu. Kun käyttäjällä on Epäsuora-käyttöoikeus, käyttäjä voi muokata Myyntirivi-taulukkoa vain suorittamalla Myynti kirjattu -codeunitin tai toisen objektin, jolla on Myyntirivi-taulukon muokkausoikeudet. Käyttäjä voi muokata Ostorivi-taulukkoa vain silloin, kun se tapahtuu tuetulla sovellusalueella. Käyttäjä ei voi suorittaa toimintoa vahingossa tai tahallaan muita menetelmiä käyttäen.

### Toisen käyttöoikeuksien joukon lisääminen

Laajenna käyttöoikeuksien joukkoa lisäämällä siihen muita käyttöoikeuksien joukkoja. Jälkikäteen voit sisällyttää tiettyjä käyttöoikeuksia tai kokonaisia käyttöoikeuksien joukkoja tai sulkea niitä pois kussakin lisäämässäsi joukossa. Näihin käyttöoikeuksiin kuuluvat Laajennus- ja Järjestelmän tyyppi -käyttöoikeuksien joukot, joita muulloin ei sallita. Poikkeukset koskevat vain käyttöoikeuksien joukkoa, jota laajennetaan. Alkuperäistä joukkoa ei muuteta.

Lisää **Käyttöoikeuksien joukko** -sivulla käyttöoikeuksien joukko **Käyttöoikeuksien joukot** -ruutuun. **Tulos**-ruudussa näkyvät kaikki lisätyt käyttöoikeuksien joukot. Jos haluat tutustua käyttöoikeuksiin, jotka sisältyvät lisättyyn joukkoon, valitse Tulos-ruudussa oleva joukko. Käyttöoikeudet näkyvät **Sisällytetyt käyttöoikeudet** -tietoruudussa.

Käytä **Tulos**-ruudun **Sisällytyksen tila** -kenttää, jos haluat tunnistaa käyttöoikeuksien joukot, joista on suljettu pois käyttöoikeuksia tai käyttöoikeuksien joukkoja. Jos poissuljettuja löytyy, tila on **Osittainen**.

Jos haluat nähdä käyttöoikeuksien joukon käyttöoikeuksien yleisnäkymän, valitse **Näytä kaikki käyttöoikeudet** -toiminto. **Laajennetut käyttöoikeudet** -sivulla näkyvät kaikki käyttöoikeudet, jotka on jo liitetty käyttöoikeuksien joukolle, sekä lisättyjen käyttöoikeuksien joukkojen käyttöoikeudet.

Jos haluat sulkea pois kokonaan kaikki käyttöoikeudet käyttöoikeuksien joukosta, valitse **Tulos**-ruudussa rivi ja valitse sitten **Näytä enemmän vaihtoehtoja**. Valitse lopuksi **Sulje pois**. Kun suljet pois käyttöoikeuksien joukon, luodaan rivi Poissuljettu-tyypin **Käyttöoikeuksien joukot** -ruudussa. Jos olet sulkenut pois käyttöoikeuksien joukon, ja haluat sisällyttää sen uudelleen, poista rivi **Käyttöoikeuksien joukot** -ruudussa.

Jos haluat sulkea pois kokonaan tai osittain tietyn käyttöoikeuden lisätyssä joukossa, luo objektille rivi **Käyttöoikeudet**-kohdassa. **Sulje pois** -vaihtoehto näkyy esimerkiksi käyttöoikeustasojen kentissä sekä Lisää käyttöoikeus- ja Muokkaa käyttöoikeutta -kentässä. Jos haluat sallia tietyn käyttöoikeustason, valitse soveltuva vaihtoehto.

Jos käyttöoikeusjoukko jätetään pois, kaikki joukon oikeudet jätetään pois. [!INCLUDE [prod_short](includes/prod_short.md)] laskee käyttöoikeudet seuraavasti:

1. Kaikkien sisällytettyjen käyttöoikeuksien luettelon laskeminen
2. Kaikkien pois suljettujen käyttöoikeuksien luettelon laskeminen
3. Poista pois jätetyt käyttöoikeudet sisällytettyjen käyttöoikeuksien luettelosta (epäsuoran käyttöoikeuden poistaminen on sama kuin Vähennä epäsuoraksi)

## Käyttöoikeuksien joukon kopioiminen

Luo uusi käyttöoikeuksien joukko kopioimalla toinen joukko. Uusi joukko sisältää kaikki käyttöoikeudet ja käyttöoikeuksien joukot kopioimastasi joukosta. Käyttöoikeuksien ja käyttöoikeuksien joukkojen järjestystapa uusissa käyttöoikeuksien joukoissa määrittyy sen mukaan, mitä **Kopiointitoiminto** -kentässä on valittu. Asetukset kuvaillaan seuraavassa taulukossa.

|Asetus  |Kuvaus  |
|---------|---------|
|**Kopiointi viitteenä**     | Alkuperäinen käyttöoikeuksien joukko ja kaikki siihen lisätyt käyttöoikeuksien joukot näkyvät **Tulokset**-ruudussa.       |
|**Jäsentämättömän käyttöoikeuden kopio**  | Kaikki käyttöoikeuksien joukkojen käyttöoikeudet sisältyvät **Käyttöoikeudet-ruudun** jäsentämättömään luetteloon. Käyttöoikeuksia ei ole järjestetty käyttöoikeuksien joukon mukaan.        |
|**Klooni**     | Luo tarkka kopio alkuperäisestä käyttöoikeuksien joukosta.        |

1. Valitse **Käyttöoikeuksien joukot** -sivulla kopioitavan käyttöoikeuksien joukon rivi. Valitse sitten **Kopioi käyttöoikeuksien joukko** -toiminto.
2. Määritä **Kopioi käyttöoikeuksien joukko** -sivulla uuden käyttöoikeuksien joukon nimi.
3. Määritä **Kopiointitoiminto**-kentässä, miten uuden käyttöoikeuksien joukon käyttöoikeus määritetään.
4. Valinnainen: Jos lisäät järjestelmän käyttöoikeuksien joukon, haluat ehkä saada ilmoituksen, jos alkuperäisen käyttöoikeuksien joukon nimeä tai sisältöä muutetaan tulevassa versiossa. Näin voit harkita, tuleeko käyttäjän määrittämää käyttöoikeuksien joukkoa päivittää. Jos haluat saada ilmoituksen, ota käyttöön **Ilmoita muutetusta käyttöoikeuksien joukosta** -vaihtopainike.

> [!NOTE]
> Ilmoitus edellyttää **Järjestelmän alkuperäistä käyttöoikeuksien joukkoa on muutettu** -ilmoituksen käyttöönottoa **Omat ilmoitukset** -sivulla.

## Käyttöoikeuksien luominen tai muokkaaminen toimia tallentamalla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöoikeuksien joukot** ja valitse sitten vastaava linkki.

    Vaihtoehtoisesti voit valita **Käyttäjät**-sivulla **Käyttöoikeuksien joukko** -toiminnon.
2. Valitse **Käyttöoikeuksien joukko** -sivulla **Uusi**-toiminto.
3. Täytä tarvittaessa uuden rivin kentät.
4. Valitse **Käyttöoikeudet**-toiminto.
5. Valitse **Käyttöoikeudet**-sivulla ensin **Kirjausoikeudet**-toiminto ja sitten **Aloita**-toiminto.  
    Tallennus täytyy tehdä joko käyttämällä **Avaa tämä sivu uudessa ikkunassa** (ponnahdusikkuna) -ominaisuutta, jotta **Käyttöoikeudet**-tallennusikkuna on vierekkäin, tai samassa välilehdessä.  
    Tallennusprosessi käynnistyy nyt ja sieppaa kaikki käyttäjän käyttöliittymässä tekemät toiminnot.
6. Siirry niille [!INCLUDE[prod_short](includes/prod_short.md)]in sivulle ja niihin toimintoihin, joita haluat tämän käyttöoikeusjoukon käyttäjien käyttävän. Sinun on tehtävä ne tehtävät, joille haluat tallentaa käyttöoikeudet.
7. Kun tallennus on valmis, palaa **Käyttöoikeudet**-sivulle ja valitse sitten **Lopeta**-toiminto.
8. Lisää tallennetut käyttöoikeudet uuteen käyttöoikeusjoukkoon valitsemalla **Kyllä**.
9. Määritä jokaiselle tallennetun luettelon objektille, saavatko käyttäjät lisätä, muokata tai poistaa tietueita tallennetuissa taulukoissa.

### Käyttöoikeusjoukon vieminen ja tuominen

Jos haluat määrittää käyttöoikeudet nopeasti, voit tuoda toisesta [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajasta viedyt käyttöoikeusjoukot.

Usean vuokraajan ympäristöissä käyttöoikeuksien joukko tuodaan tietylle vuokralaiselle. Toisin sanoen tuonnin laajuus on *vuokralainen*.

1. Valitse Vuokraaja 1:ssä **Käyttöoikeuksien joukot** -sivulla vietävien käyttöoikeuksien joukon rivi tai rivit. Valitse sitten **Vie käyttöoikeuksien joukot** -toiminto.

    Tietokoneen latauskansioon luodaan XML-tiedosto. Oletusarvon mukaan sen nimi on *Export Permission Sets.xml*.

2. Valitse vuokralainen 2:n **Käyttöoikeuksien joukot** -sivulla **Tuo käyttöoikeuksien joukot** -toiminto.
3. Harkitse **Tuo käyttöoikeuksien joukot** -valintaikkunassa, haluatko yhdistää aiemmin luodut käyttöoikeuksien joukot uusien käyttöoikeuksien joukkojen kanssa XML-tiedostoon.

    Jos valitset **Päivitä aiemmin luodut käyttöoikeudet** -valintaruudun, aiemmin luodut käyttöoikeuksien joukot, joilla on sama nimi kuin XML-tiedostossa, yhdistetään tuotuihin käyttöoikeuksien joukkoihin.

    Jos et valitse **Päivitä aiemmin luodut käyttöoikeudet** -valintaruudun, aiemmin luodut käyttöoikeuksien joukot, joilla on sama nimi kuin XML-tiedostossa, ohitetaan tuonnin aikana. Tässä tapauksessa sinulle ilmoitetaan ohitettujen käyttöoikeuksien joukoista.

4. Etsi ja valitse tuotava XML-tiedosto **Tuo**-valintaikkunasivulta ja valitse sitten **Avaa**-toiminto.

Käyttöoikeusien joukot tuodaan.

## Voit poistaa vanhentuneet käyttöoikeudet kaikista käyttöoikeuksien joukoista seuraavasti.

Valitse **Käyttöoikeuksien joukot** -sivulla **Poista vanhentuneet käyttöoikeudet** -toiminto.

## Määritä käyttäjän aikarajoitukset

Järjestelmänvalvojat voivat määrittää ajanjaksot, joina määritetyt käyttäjät voivat kirjata. Järjestelmänvalvojat voivat myös määrittää, kirjataanko järjestelmä lokiin, kuinka kauan käyttäjät ovat kirjautuneena sisään. Vastaavasti järjestelmänvalvojat voivat määrittää käyttäjille vastuupaikkoja. Lisätietoja on kohdassa [Vastuupaikkojen käyttäminen](inventory-responsibility-centers.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjän määritys** ja valitse sitten vastaava linkki.
2. Valitse avautuvalla **Käyttäjäasetukset**-sivulla **Uusi**-toiminto.
3. Anna **Käyttäjätunnus**-kentässä käyttäjän tunnus tai valitse kenttä, jos haluat nähdä kaikki järjestelmässä tällä hetkellä olevat Windows-käyttäjät.
4. Täytä tarvittavat kentät.

## Käyttöoikeuksien hallinta käyttäjäryhmien avulla

Käyttäjäryhmät auttavat hallitsemaan koko yrityksen käyttöoikeuksien joukkoja. [!INCLUDE [prod_short](includes/prod_short.md)] online sisältää oletuskäyttäjäryhmät, jotka on määritetty käyttäjille automaattisesti käyttöoikeuden perusteella. Voit lisätä käyttäjiä käyttäjäryhmään manuaalisesti, ja voit luoda uusia käyttäjäryhmiä aiemmin luotujen käyttäjäryhmien kopioiksi.  

Aloitat luomalla käyttäjäryhmän. Sen jälkeen voit määrittää ryhmälle käyttöoikeuksien ryhmiä, jotka määrittävät, mitä objektia ryhmän käyttäjät voivat käyttää. Kun lisäät käyttäjän ryhmään, ryhmälle määritetyt käyttöoikeusjoukot koskevat käyttäjää.

Käyttäjän käyttäjäryhmän kautta määritetyt käyttöoikeusjoukot pysyvät synkronoituina. Käyttäjäryhmän käyttöoikeuksiin lisätään muutos automaattisesti käyttäjille. Jos poistat käyttäjän käyttäjäryhmästä, asiaan liittyvät käyttöoikeudet peruutetaan automaattisesti.

### Käyttäjien lisääminen käyttäjäryhmään

Seuraavissa ohjeissa selitetään, miten käyttäjäryhmiä luodaan manuaalisesti. Lisätietoja käyttäjäryhmien luomisesta automaattisesti on kohdassa [Käyttäjäryhmän ja kaikkien sen käyttöoikeusjoukkojen kopioiminen](#to-copy-a-user-group-and-all-its-permission-sets).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjäryhmät** ja valitse sitten vastaava linkki.

    1. Vaihtoehtoisesti voit valita **Käyttäjät**-sivulla **Käyttäjäryhmät**-toiminnon.
2. Valitse **Käyttäjäryhmä**-sivulla **Käyttäjäryhmän jäsenet** -toiminto.
3. Valitse **Käyttäjäryhmän jäsenet** -sivulla **Lisää käyttäjät** -toiminto.

### Käyttäjäryhmän ja sen kaikkien käyttöoikeuksien joukkojen kopioiminen

Voit määrittää uuden käyttäjäryhmän nopeasti kopioimalla kaikki käyttöoikeusjoukot aiemmin luodusta käyttäjäryhmästä uuteen käyttäjäryhmään.

> [!NOTE]
> Käyttäjäryhmän jäseniä ei kopioida uuteen käyttäjäryhmään. Heidät on lisättävä myöhemmin manuaalisesti. Lisätietoja on osassa [Käyttäjien lisääminen käyttäjäryhmään](#to-add-users-to-a-user-group).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjäryhmät** ja valitse sitten vastaava linkki.
2. Valitse ensin kopioitava käyttäjäryhmä ja sitten **Kopioi käyttäjäryhmä** -toiminto.
3. Anna **Uuden käyttäjäryhmän koodi** -kentässä ryhmälle nimi ja valitse sitten **OK**-painike.

Uusi käyttäjäryhmä lisätään **Käyttäjäryhmät**-sivulle. Aloita käyttäjien lisääminen. Lisätietoja on osassa [Käyttäjien lisääminen käyttäjäryhmään](#to-add-users-to-a-user-group).  

> [!IMPORTANT]
> Saat vahvistusvirheen, jos yrität kohdistaa käyttäjälle käyttäjäryhmää, joka viittaa poistetussa laajennuksessa määritettyyn käyttöoikeuksien joukkoon. Tämä johtuu siitä, että laajennuksen sovellustunnus vahvistetaan joka kerta, kun siihen viitataan. Jos haluat kohdistaa tämän käyttäjäryhmän käyttäjälle, voit joko asentaa laajennuksen uudelleen, poistaa poistetun laajennutuksen viittaukset käyttöoikeuksien joukosta tai poistaa käyttöoikeuksien joukon käyttäjäryhmästä.

### Käyttöoikeuksien joukkojen määrittäminen käyttäjäryhmille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjäryhmät** ja valitse sitten vastaava linkki.
2. Valitse käyttäjäryhmä, jolle haluat määrittää käyttöoikeuden.  

    Kaikki käyttäjälle jo määritetyt käyttöoikeusjoukot **Käyttöoikeuksien joukot** -tietoruudussa.
3. Avaa **Käyttöoikeuksien joukot**-toiminto, jos haluat avata **Käyttöoikeuksien joukot** -sivun.
4. Täytä **Käyttöoikeuksien joukot** -sivulla uudella rivillä tarvittavat kentät.

### Käyttöoikeuksien joukon määrittäminen **Käyttöoikeuksien joukko käyttäjäryhmän mukaan** -sivulla

Seuraavassa kerrotaan, miten käyttöoikeuksien joukot määritetään käyttäjäryhmälle **Käyttöoikeuksien joukko käyttäjäryhmän mukaan** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.
2. Valitse **Käyttäjät**-sivulla sopiva käyttäjä ja valitse sitten **Käyttöoikeuksien joukko käyttäjäryhmän mukaan** -toiminto.
3. Valitse **Käyttöoikeuksien joukko käyttäjäryhmän mukaan** -sivulla sen käyttöoikeuksien joukon rivin **[käyttäjäryhmän nimi]**-kenttä, joka määritetään käyttäjäryhmälle.
4. Valitse **Kaikki käyttäjäryhmät** -valintaruutu, jos haluat määrittää käyttöoikeuksien joukon kaikille käyttäjäryhmille.

Voit myös määrittää käyttöoikeusjoukkoja suoraan käyttäjälle.

## Käyttöoikeusjoukkojen määrittäminen käyttäjälle

Käyttöoikeusjoukko on joukko tiettyjen tietokantaobjektien käyttöoikeuksia. Kaikille käyttäjille on määritettävä vähintään yksi käyttöoikeusjoukko, ennen kuin he voivat käyttää [!INCLUDE[prod_short](includes/prod_short.md)]ia.  

[!INCLUDE[prod_short](includes/prod_short.md)] -ratkaisu sisältää esimääritettyjä käyttöoikeuksien joukkoja, jotka Microsoft tai oma ratkaisutoimittajasi on lisännyt. Voit myös lisätä uusia käyttöoikeusjoukkoja, jotka on räätälöity organisaatiosi tarpeiden mukaan. Lisätietoja on [Käyttöoikeuksien joukon luominen](#to-create-a-permission-set) -osassa.

> [!NOTE]
> Jos et halua rajoittaa käyttäjän oikeuksia enempää kuin käyttöoikeussopimuksessa on jo määritetty, voit määrittää käyttäjälle erityisen käyttöoikeusjoukon nimeltä SUPER. Tämä käyttöoikeusjoukko varmistaa, että käyttäjä voi käyttää kaikkia lisenssissä määritettyjä objekteja.
>
> Käyttäjällä, jolla on olennainen käyttöoikeus ja SUPER-käyttöoikeusjoukko, on käyttöoikeustoimintoja enemmän kuin käyttäjillä, joilla on tiiminjäsenlisenssi ja SUPER-käyttöoikeusjoukko.

Voit määrittää käyttöoikeusjoukkoja käyttäjille kahdella seuraavalla tavalla:

- **Käyttäjän kortti** -sivulta valitsemalla käyttöoikeusjoukot käyttäjän määrittämistä varten.
- **Käyttöoikeusjoukko**-sivulta valitsemalla käyttäjät, joille käyttöoikeusjoukko on määritetty.

### Käyttäjäoikeuksien joukon määrittäminen käyttäjän kortissa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.
2. Valitse käyttäjä, jolle haluat määrittää käyttöoikeuden.
Kaikki käyttäjälle jo määritetyt käyttöoikeusjoukot **Käyttöoikeuksien joukot** -tietoruudussa.
3. Avaa **Käyttäjän kortti** -sivu valitsemalla **Muokkaa** -toiminto.
4. Täytä **Käyttöoikeuksien joukot** -tietoruudun uudella rivillä tarvittavat kentät. Lisätietoja on kohdassa [Käyttöoikeuksien joukon luominen tai muokkaaminen](ui-define-granular-permissions.md#to-create-a-permission-set).

   Käytä **Yritys**-kenttää, kun haluat käyttää tietylle yritykselle määritettyjä käyttöoikeuksia. Jos jätät kentän tyhjäksi, kenttä koskee kaikkia yrityksiä.

## Käyttöoikeuksien joukon määrittäminen Käyttöoikeuksien joukko käyttäjän mukaan -sivulla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.
2. Valitse **Käyttäjät**-sivulla **Käyttöoikeuksien joukko käyttäjän mukaan** -toiminto.
3. Valitse **Käyttöoikeuksien joukko käyttäjän mukaan** -sivulla sen käyttöoikeuksien joukon rivin **[käyttäjätunnus]**-valintaruutu, joka määritetään käyttäjälle.

    Valitse **Kaikki käyttäjät** -valintaruutu, jos haluat määrittää käyttöoikeuksien joukon kaikille käyttäjille.

## Yleiskuvan saaminen käyttöoikeuksista

Voit tarkastella muiden käyttäjien käyttöoikeuksia vain, jos sinut on liitetty SECURITY- tai SUPER-käyttöoikeuksiin. 

**Voimassa olevat käyttöoikeudet** -sivulla on lisätietoja kunkin käyttöoikeuden lähteestä. Esimerkiksi se, onko lähde käyttöoikeusryhmä vai peritty käyttöoikeus. Sivulla on myös sarake, jossa järjestelmänvalvojat voivat tarkistaa käytettävät suojaussuodattimet. Lisätietoja suojaussuodattimista on kohdassa [Suojaussuodattimet rajoittavat käyttäjän käyttöoikeutta tiettyihin taulukon tietueisiin](#security-filters-limit-a-users-access-to-specific-records-in-a-table).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.
2. Avaa asianmukaisen käyttäjän kortti.
3. Valitse **Voimassa olevat käyttöoikeudet** -toiminto.

    **Käyttöoikeudet**-osassa ovat kaikki tietokantaobjektit, joiden käyttöoikeus käyttäjällä on. Et voi muokata tätä osaa.

    **Käyttöoikeuksien joukon mukaan** -osassa ovat ne määritetyt käyttöoikeuksien joukot, joiden kautta käyttäjälle myönnetään käyttöoikeudet, käyttöoikeuksien joukon lähde ja tyyppi sekä erilaisten käyttöoikeustyyppien hyväksytty laajuus.

    Jokaisella **Käyttöoikeudet**-osan valitun rivin **Käyttöoikeuksien joukon mukaan** -osassa näytetään käyttöoikeuksien joukko tai joukot, joiden kautta käyttöoikeus myönnetään. Tässä osassa voit muokata arvoa kaikissa viidessä käyttöoikeustyyppien kentässä: **luku-**, **lisäys-**, **muokkaus-**, **poisto**- ja **suoritusoikeus**.

    > [!NOTE]  
    > Vain **Käyttäjän määrittämä** -tyyppisiä käyttöoikeuksien joukkoja voi muokata.
    >
    > Rivit, joiden lähde on oikeutus, ovat peräisin tilauslisenssistä. Oikeutuksen käyttöoikeusarvot korvaavat muiden käyttöoikeuksien joukkojen arvot, jos niillä on korkeampi luokitus. Muun kuin oikeuden käyttöoikeuksien joukon arvo, jonka luokitus on korkeampi kuin oikeutuksen liittyvän arvon luokitus, on suluissa. Tämä osoittaa, että se ei ole voimassa, koska oikeutus korvaa sen.
    >
    > Lisätietoja luokituksesta on kohdassa [Käyttöoikeuksien joukon luominen](ui-define-granular-permissions.md#to-create-a-permission-set).  

4. Voit muokata käyttöoikeuksien joukkoa valitsemalla **Käyttöoikeuksien joukon mukaan** -osan asianmukaisen käyttöoikeuksien joukon **Käyttäjän määrittämä** -tyyppisellä rivillä yksi viidestä käyttöoikeustyypin kentästä ja valitse siihen toinen arvo.

5. Voit muokata käyttöoikeuksien joukon yksittäisiä käyttöoikeuksia valitsemalla arvon **Käyttöoikeuksien joukko** -kentässä. **Käyttöoikeudet**-sivu avautuu.

> [!NOTE]  
> Kun muokkaat käyttöoikeuksien joukkoa, muutokset kohdistuvat myös niihin käyttäjiin, joille on määritetty käyttöoikeuksien joukko.

### Suojaussuodattimet rajoittavat käyttäjän käyttöoikeutta tiettyihin taulukon tietueisiin

Sovelluksen [!INCLUDE[prod_short](includes/prod_short.md)] tietuetason suojauksessa käyttäjän käyttöoikeus rajoitetaan taulukon tietoihin suojaussuodattimien avulla. Suojaussuodattimet luodaan taulukon tietojen perusteella. Suojaussuodatin kuvaa sitä taulukon tietuejoukkoa, jonka käyttöoikeus käyttäjällä on. Voit määrittää esimerkiksi, että käyttäjä saa lukea vain tietueita, joissa on tietoja tietystä asiakkaasta. Tällä tavoin käyttäjällä ei ole muiden asiakkaiden tietoja sisältävien tietueiden käyttöoikeutta. Lisätietoja on hallintasisällön kohdassa [Suojaussuodattimien käyttäminen](/dynamics365/business-central/dev-itpro/security/security-filters).

## Käyttöoikeuksien muutosten telemetrian tarkasteleminen

Voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in lähettämään käyttöoikeuksiin tehdyt muutokset Application Insights -resurssiin Microsoft Azuressa. Sitteen Azure Monitorin avulla luot raportteja ja määrität hälytyksiä kerätyille tiedoille. Lisätietoja on [!INCLUDE[prod_short](includes/prod_short.md)]in kehittäjien ja järjestelmänvalvojan ohjeen seuraavissa artikkeleissa:

- [Telemetrian seuranta ja analysointi – Application Insightsin käyttöönotto](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Kentän seurannan telemetrian analysointi](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## Delegoidut järjestelmänvalvojakäyttäjät

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

## Katso myös

[Luo käyttäjät käyttöoikeuksien mukaan](ui-how-users-permissions.md)  
[Profiilien hallinta](admin-users-profiles-roles.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen mukauttaminen](ui-customizing-overview.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Hallinta](admin-setup-and-administration.md)  
[Käyttäjien lisääminen Microsoft 365 for Businessiin](/microsoft-365/admin/add-users/add-users)  
[Turvallisuus ja suojaus Business Centralissa](/dynamics365/business-central/dev-itpro/security/security-and-protection) kohdassa Kehittäjä- ja IT-Pro -ohje  
[Telemetriatunnuksen määrittäminen käyttäjille](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
