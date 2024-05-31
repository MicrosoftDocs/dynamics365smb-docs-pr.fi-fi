---
title: Tietojen syöttäminen Business Centralissa
description: 'Käytettävissä on monia yleisiä ominaisuuksia, jotka helpottavat, nopeuttavat ja täsmentävät tietojen antamista. Perusperiaatteet ja kehittyneet ominaisuudet on kuvattu tässä.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'decimal separator, data entry, focus'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 03/23/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Tietojen antaminen

Käytettävissä on monia yleisiä ominaisuuksia, jotka helpottavat, nopeuttavat ja täsmentävät tietojen antamista. Tässä artikkelissa käsitellään tietojen antamisen perusperiaatteita ja edistyneitä ominaisuuksia.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Tämän artikkelin esimerkeissä käytetään esimerkkitietoja.

## Muokattavien kenttien käsitteleminen

[!INCLUDE[prod_short](includes/prod_short.md)] -kohteen kentissä voi olla erilaisia muokattavia tietoja, kuten tekstiä tai valuuttasummia. Muokattavat kentät näyttävät tavallisesti syöttöruudun, johon voit kirjoittaa tai valita arvon. Ei-muokattavat kentät näkyvät tavallisesti harmaana taustana.   

Joidenkin muokattavien kenttien avulla voit määrittää arvon.  

<!-- TODO: Add illustrations or images of each picker -->
|**Valitsin**        |**Miten se auttaa määrittämään arvon**|
|------------------|------------------------------------|
|Päivämäärävalitsin       |Valitsin näyttää kalenterin, joka perustuu nykyisiin alueellisiin asetuksiin. Sen avulla voit valita yhden päivämäärän.|
|Avattavat valikot          |Avattavat valikot tarjoavat valikoiman kiinteitä arvoja tai viitetietueita toisesta taulukosta|
|Kytkin tai valintaruutu|Joissakin kentissä on helppo valita *Kyllä*- tai *Ei*-arvoja. Valitsinta käytetään määrittämään tämä arvo, ja se näkyy aina valintaruutuna luetteloissa|
|Muokkausapu       |Joissakin kentissä on mukautettuja valitsimia, jotka soveltuvat kyseisen kentän parhaan arvon etsimiseen ja valitsemiseen, esimerkiksi ponnahdusikkunaan|

### Kentän arvon muokkaaminen

Jos haluat muuttaa kentän arvoa, sinun on ensin määritettävä kentän kohdistus. Voit määrittää kohdistuksen tekemällä seuraavat toimet:

- Käytä <kbd>Sarkain</kbd>-näppäintä. Toiminto valitsee koko arvon.
- Napsauta hiiren vasenta näppäintä tai vastaavaa syöttölaitetta. Tämä toimenpide valitsee koko kentän arvon vain, jos kenttä on luettelossa.  

Kun käytät kenttiä käyttöliittymässä, [!INCLUDE[prod_short](includes/prod_short.md)] yleensä suosii koko kentän arvon valitsemista, jotta kyseinen arvo olisi helpompi korvata.

Kun koko kentän arvo on valittuna:
- Voit määrittää uuden arvon korvaamalla arvon kirjoittamalla. Jos kentässä on valitsin, voit aktivoida sen käyttämällä <kbd>Alt</kbd>+<kbd>alanuoli</kbd>-pikanäppäimiä.
- Voit tyhjentää arvon <kbd>Delete</kbd>-näppäimellä tai <kbd>askelpalauttimella</kbd>.

valitse <kbd>F2</kbd>-näppäintä vaihtaaksesi koko kentän arvon valitsemista tai kohdistimen asettamista kentän arvon alapuolelle. Kohdistimen sijoittaminen arvon loppuun helpottaa olemassa olevan arvon liittämistä.

Kun kohdistin näkyy kentän arvon lopussa:
- Lisää arvo kirjoittamalla.
- Voit siirtää kohdistinta arvon sisällä <kbd>koti</kbd>-, <kbd>loppu</kbd>-, <kbd>vasen nuoli</kbd>- ja <kbd>oikea nuoli</kbd> -näppäimillä. Jos muokkaat luettelossa olevaa kenttää, valitse <kbd>vasenta nuolinäppäintä</kbd> uudelleen, kun kohdistin on arvon alussa, ja kohdistus siirtyy edelliseen kenttään. Kun vastaavasti valitset <kbd>oikeaa nuolinäppäintä</kbd> uudelleen, kun kohdistin on arvon lopussa, kohdistus siirtyy seuraavaan kenttään.

> [!NOTE]
> Kun olet määrittänyt arvon, Business Central tarkistaa vain, että se on kelvollinen sen jälkeen, kun olet napsauttanut kentän ulkopuolella tai asettanut kohdistuksen toiseen elementtiin, kuten seuraavaan kenttään.  

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]

## Pikanäppäimet

On olemassa useita pikanäppäimiä, joiden avulla voit työskennellä "hiirettä" ja nopeuttaa tietojen syöttöä. Näistä pikanäppäimistä on hyötyä erityisesti suurissa kirjauksissa ja toistuvissa kirjoitustehtävissä.

Lisätietoja pikanäppäimissä on kohdassa [Pikanäppäimet](keyboard-shortcuts.md). Tässä artikkelissa käsitellään muutamia pikanäppäimiä.

## <a name="QuickEntry"></a>Tietojen syöttämisen helpottaminen pikatapahtuman avulla

Pikatapahtuma on näppäimistön avulla tapahtuvaa tietojen antamista varten suunniteltu ominaisuus. Pikatapahtumia voi käyttää kentissä (kuten korttisivuilla) ja luetteloissa (rivit ja sarakkeet). Se on hyödyllistä, kun teet toistuvia kirjoitustehtäviä, jotka edellyttävät monen tietueen luomista peräkkäin. Esimerkkeinä mainittakoon myyntitilausten erä tai uusien nimikkeiden rekisteröinti.

Voit käyttää sarkainnäppäintä siirtyäksesi sivulla kentästä seuraavaan muokattavaan kenttään. Sarkaimen käytön haittapuolena on kuitenkin se, että se siirtyy aina seuraavaan kenttään. <!-- even if the field is non-editable or seldom filled it in.-->Voit muuttaa tätä polkua pikatapahtuman avulla. Pikasyötön avulla voit siirtyä vain haluamillesi kentille <kbd>Enter</kbd>-näppäimellä. Pikasyöttö hyppää ei-muokattavien kenttien ja niiden kenttien, joita et tavallisesti täytä, yli. Olet ehkä jo havainnut tämän toiminnan joillakin sivuilla. Tämä johtuu siitä, että kentät mihin kenttiin Enter-näppäimellä siirrytään ja mitkä ohitetaan, ovat ennalta määritettyjä. Voit mukauttaa pikatapahtumaa mukauttamalla työtilaa ja optimoimalla tietojen antamistavan kullakin sivulla.

### Pikatapahtuman toimintaperiaate

Jokainen kenttää voidaan merkitä joko *pikatapahtumaan sisällytetyksi* tai *pikatapahtumasta poissuljetuksi*. Pikamerkintään sisältyvät kentät sisällytetään polkuun <kbd>Enter</kbd>-näppäimen valinnan jälkeen. Pikamerkinnän ulkopuolelle jäävät kentät eivät ole.

Kun tiedot on annettu kenttään, vahvista muutokset <kbd>Enter</kbd>-näppäimellä ja siirry samalla seuraavaan kenttään. Jos haluat palata taaksepäin ja siirtyä edelliseen kenttään, paina näppäinyhdistelmää <kbd>Vaihto</kbd>+<kbd>Enter</kbd>. Lisätietoja pikanäppäimistä on kohdassa [Kenttien pikatapahtumien pikanäppäimet](keyboard-shortcuts.md#QuickEntry)

#### Vihjeet ja vinkit

Seuraavassa luettelossa on joitakin hyödyllisiä tietoja pikatapahtumien käyttämisestä.

- Se on käytössä muokattavissa kentissä.
- Sitä voi käyttää myös sarakkeissa ja riveillä.
- Se ei estä sivun muiden osien, kuten toimintojen, käyttämistä, Näitä elementtejä voi edelleen käyttää <kbd>sarkaimella</kbd> ja <kbd>Vaihto</kbd>+<kbd>Sarkain</kbd>-näppäinyhdistelmällä.  
- Pikavälilehtien laajentamista ei edellytetä, jotta pikasyöttö voi toimia. Jos seuraava pikatapahtumakenttä sijaitsee tiivistetyssä pikavälilehdessä, pikavälilehti laajentuu automaattisesti ja kohdistus on valitussa kentässä. [!INCLUDE[prod_short](includes/prod_short.md)] muistaa, että pikavälilehti on laajennettava, kun seuraavan kerran käyt sivulla.  
- Pikasyöttö on käytettävissä riippumatta siitä, ovatko kentät pakollisia vai eivät. Tämän vuoksi kannattaa varmistaa, että pakolliset kentät sisällytetään pikasyöttöön.
- Oletusarvoisesti useimmat kentät sisällytetään automaattisesti pikatapahtumaan. Tämän vuoksi joudutkin luultavasti aluksi sulkemaan kenttiä pois pikatapahtumasta.

### Pikatapahtumakenttien muuttaminen

Voit määrittää kenttiin pikasyötön käyttämällä mukauttamista.

1. Aloita mukauttaminen valitsemalla ![Asetukset.](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") -kuvake ja sitten **Mukauta**-toiminto.
2. Valitse muutettava kenttä. Valitse luettelosta vastaava sarakeotsikko. Valitse sitten **Sisällytä pikasyöttöön** tai **Jätä pois pikasyötöstä** -valinta.

Lisätietoja mukauttamisesta on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

## Pakolliset kentät

Kun annat tietoja sivuilla, tietyt kentät on merkitty punaisella tähtimerkillä. Punainen tähti tarkoittaa, että kenttä on täytettävä tietyn prosessin suorittamiseksi loppuun. Esimerkkinä voidaan kirjata kauppatapahtuma, joka käyttää kentän arvoa.  

Vaikka kenttä on pakollinen, et joudu täyttämään kenttää ennen kuin jatkat muihin kenttiin tai suljet sivun. Punainen tähti toimii vain muistutuksena siitä, että sinua estetään suorittamasta tiettyä prosessia.  

## Tietojen etsiminen kirjoitettaessa

 Kun alat kirjoittaa merkkejä kenttään, näyttöön tulee avattava luettelo, joka sisältää kentän mahdollisia arvoja. Luettelon sisältö muuttuu, kun kirjoitat lisää merkkejä, ja voit valita luettelosta haluamasi vaihtoehdon, kun luettelo on näkyvissä.  

 Monissa kentissä on alanuolipainike, jonka voi valita. Napsauttamalla tätä painiketta saat näyttöön luettelon arvoista, jotka ovat määritettävissä kyseiseen kenttään. Painikkeella on kaksi eri tehtävää kentän tyypin mukaan:  

- Haku - Ohjelma näyttää toisen taulukon tietoja, joita voi syöttää kenttään. Voit valita yhden tiedon kerrallaan.  

- Avattava luettelo - Ohjelma näyttää kentän eri vaihtoehdot. Voit valita vain yhden vaihtoehdoista.  

## Kenttien ja rivien kopioimisen ja liittämisen usein kysytyt kysymykset

Voit kopioida yhden tai useamman rivin luettelosta tai yhden kentän sivulla. Liitä sitten kopioimasi kohde samalle sivulle, toiselle sivulle tai ulkoiseen asiakirjaan. Voit esimerkiksi liittää Microsoft Exceliin tai Outlook-sähköpostiin. Jos haluat kopioida, valitse näppäimistöllä <kbd>Ctrl</kbd>+<kbd>C</kbd> (cmd+C macOS-käyttöjärjestelmässä). Jos haluat liittää, paina näppäimiä <kbd>Ctrl</kbd>+<kbd>V</kbd> tai <kbd>cmd+V</kbd> macOS-käyttöjärjestelmässä.

Kopioi luettelossa kenttä yläpuolella olevan rivin samasta sarakkeesta ja liitä se nykyiselle riville valitsemalla <kbd>F8</kbd>-näppäintä.

Lisätietoja on kohdassa [Kopioinnin ja liittämisen usein kysytyt kysymykset](faq-copy-paste.yml).

## Rivinimikkeiden suodattaminen

Aloita suodatus valitsemalla ![Suodatusruudun kuvake](media/open-filter-pane-icon.png "Suodatinruudun kuvake") luettelon yläosasta tai paina <kbd>Vaihto</kbd>+<kbd>F3</kbd> avataksesi suodatuspaneelin. Voit käyttää suodatinruutua samalla tavoin kuin muitakin luetteloita. Lisätietoja on kohdassa [Suodattaminen](ui-enter-criteria-filters.md#filtering).

Suodatuksesta on apua erityisesti silloin, kun tarkasteltava ja analysoitava asiakirja on pitkä. Kuvittele, että avaat kirjatun myyntilaskun. Sen jälkeen voit suodattaa rivinimikkeet niin, että ne näyttävät kaikki rivinimikkeet, joiden yksittäinen alennus on yli 5 %. Voit myös suodattaa näyttämään vain polkupyörätarvikkeet, joiden nimessä on "Pro".

## <a name="Focus"></a>Kohdistaminen rivinimikkeisiin

Jos käsiteltävissä asiakirjoissa on rivinimikeosia, voit siirtää kohdistuksen vain rivinimikkeisiin. Esimerkkiasiakirjat ovat myyntitilaus- tai laskusivuja. Rivinimikkeet-osa laajenee niin, että se peittää lähes koko työtilan. Se piilottaa sivun muut osat paitsi toiminnot-alueen yläosassa. Saat tällä sijoittelulla hyvän yleiskuvan rivinimikkeistä, ja sinulla on enemmän tilaa niiden käsittelemiseen.

Hyödyt erityisesti, kun työskentelet suurten rivinimikeluetteloiden parissa, ja haluat syöttää tietoja nopeasti. Tämä ominaisuus tarjoaa myös kehittyneitä suodatusominaisuuksia. Kuten muissakin luetteloissa, rivinimikkeiden selaaminen ja etsiminen helpottuu entisestään.

### Kohdituksen Kytkeminen Päälle ja Pois

Jos haluat keskittyä rivikohteisiin, valitse missä tahansa rivikohteen osassa ja valitse sitten ![Kohdistustila-kuvake.](media/focus-mode.png "Tarkennustilan kuvake") oikeassa yläkulmassa tai paina näppäinyhdistelmää <kbd>Ctrl</kbd>+<kbd>Vaihto</kbd>+<kbd>F12</kbd>.

Jos haluat palata normaalinäkymään, valitse ![Tarkennustila-kuvake.](media/focus-mode.png "Tarkennustilan kuvake") tai valitse <kbd>Ctrl</kbd>+<kbd>Vaihto</kbd>+<kbd>F12</kbd> uudelleen.

## Monen tehtävän suorittaminen yhtä aikaa useilla sivuilla

Voit avata kortin tai asiakirjan sivun uudessa ikkunassa. Avaamalla uuden ikkunan voit:

- Työskennellä useiden tehtävien parissa samanaikaisesti
- Hallita käynnissä olevan tehtävän keskeytyksiä, kuten saapuvan puhelun ottamista.
- Pitää keskeneräisen tehtävän ikkunan avoinna samalla, kun aloitat tai suoritat toisen tehtävän toisessa ikkunassa.

Jos haluat avata nykyisen kortin tai asiakirjan uudessa ikkunassa, valitse ![Avaa uusi ikkuna.](media/open-new-window-icon.png "Avaa uudessa ikkunassa -kuvake") oikeassa yläkulmassa tai paina näppäinyhdistelmää <kbd>Alt</kbd>+<kbd>Vaihto</kbd>+<kbd>W</kbd>.

<!--
When working on multiple tasks at a time or when managing interruptions to the current task, such as taking an incoming call, you can open a card or document page in a new window. This allows you to keep a window open for an ongoing task while you start or complete another task in one or more other windows.
-->

> [!NOTE]
> Kun avaat uudessa ikkunassa avatusta kortista tai asiakirjasta muita sivuja, kyseiset sivut avautuvat uudessa ikkunassa, vaikka et valitsisi toimintoa ![Avaa uusi ikkuna.](media/open-new-window-icon.png "Avaa uudessa ikkunassa -kuvake").

> [!NOTE]
> Jos käytössä on Safari-selain, ponnahdusikkunoiden esto voi estää uuden ikkunan avautumisen. Määritä siinä tapauksessa tuotteen URL-osoite sallituksi sivustoksi. Lisätietoja on kohdassa [Safarin asetusten muuttaminen](https://go.microsoft.com/fwlink/?LinkId=2102965).<br /><br />
> Sama voi tapahtua muissakin selaimissa, kuten Firefoxissa. Lisätietoja on kohdassa [Firefoxin ponnahdusikkunoiden eston asetukset](https://go.microsoft.com/fwlink/?LinkId=2116400).  

Toinen tapa tehdä useita toimintoja samanaikaisesti on avata [!INCLUDE[prod_short](includes/prod_short.md)] kahdessa tai useammassa välilehdessä. Kun noudatat tätä tapaa, luo uusi välilehti ja kopioi/liitä alkuperäisen välilehden URL-osoite uuteen välilehteen. Tämä tapa luo uuden istunnon.   

> [!NOTE]
> Älä käytä selaimen **Monista**-toimintoa uuden välilehden luomiseen, koska se voi aiheuttaa toimintoja yhdelle välilehdelle estämään muiden välilehtien toiminnot, koska ne ovat osa samaa istuntoa.

## Määrien antaminen laskutoimituksia käyttämällä

Kun syötät lukuja määräkenttiin, kuten nimikepäiväkirjan rivin **Määrä**-kenttään, voit syöttää summan asemesta kaavan. Seuraavassa on esimerkkejä:  

### Esimerkkejä  

- Jos syötät 19+19, kentän arvoksi lasketaan 38.  

- Jos syötät 41-9, kentän arvoksi lasketaan 32.  

- Jos syötät 12*4, kentän arvoksi lasketaan 48.  

- Jos syötät 12/4, kentän arvoksi lasketaan 3.  

## Negatiivisten lukujen syöttäminen

Voit antaa negatiivisia lukuja kahdella tavalla. Numero -20,5 voidaan syöttää seuraavasti:  

- -20.5  

  tai
- 20,5-  

Kummassakin tapauksessa summa kirjataan arvona -20,5.  

Jos lausekkeen viimeinen merkki on **+** tai **-**, koko lauseke kirjataan kyseisen merkin kanssa. Esimerkiksi **10-20+** johtaa tulokseen 10, ei tulokseen -10.  

## Päivämäärien ja aikojen syöttäminen

Päivämääriä ja aikoja voi määrittää kaikissa päivämääräkentissä. Voit syöttää päivämäärät käyttäen erottimia tai ilman niitä.

> [!NOTE]  
> Päivämäärien ja kellonaikojen antaminen määräytyy **Alue**-asetusten mukaan. Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).  

### Päivämäärien syöttäminen

Voit käyttää joko päivämäärän valitsinta valitaksesi päivämäärän kalenterista, tai antaa päivämäärät manuaalisesti. Tässä osassa käsitellään lyhyesti päivämäärien antamista. Lisätietoja on kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).

Kun päivämäärä annetaan manuaalisesti, voit käyttää kahta, neljää, kuutta tai kahdeksaan numeroa:  

- Kaksi numeroa tulkitaan päiväksi. Ohjelma lisää käsittelypäivämäärän kuukauden ja vuoden.  

- Neljä numeroa tulkitaan päiväksi ja kuukaudeksi. Ohjelma lisää käsittelypäivämäärän vuoden.  

- Jos haluamasi päivämäärä on alueella 01.01.1950 – 31.12.2049, kirjoita vuosi, jossa on kaksi numeroa. Muussa tapauksessa syötä vuosi, jossa on neljä numeroa.

  > [!NOTE]
  > Jos käytössä on paikallinen [!INCLUDE[prod_short](includes/prod_short.md)], kaksinumeroinen vuosiväli voi olla eri. Järjestelmänvalvojat voivat muuttaa aluetta muuttamalla **CalendarTwoDigitYearMax**-asetusta [!INCLUDE[prod_short](includes/prod_short.md)]-palvelimessa. Lisätietoja on kohdassa [Business Central Serverin määrittäminen](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General).

Voit myös syöttää päivämäärän viikonpäivänä, jonka jälkeen tulee viikon numero. Tai voit syöttää vuoden. Esimerkiksi Ma25 tai ma25 tarkoittaa viikon 25 maanantaita.  

Tietyn päivämäärän antamisen sijaan voit antaa jonkin seuraavista koodeista.  

|Koodi|Tulos|  
|--------------|----------------|  
|t|Määrittää kuluvan päivän päivämäärän (tietokoneen järjestelmäpäivämäärä).|  
|j|Määrittää kirjanpitojakson, jossa j tarkoittaa ensimmäistä kirjanpitojaksoa, j2 toista kirjanpitojaksoa ja niin edelleen. |
|k|Määrittää sovelluksessa määritettävän käsittelypäivämäärän. Lisätietoja käsittelypäivämäärän muuttamisesta on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md). Haluat ehkä käyttää käsittelypäivämäärää, jos sellaisia tapahtumia on paljon, joissa on jokin muu kuin tämän päivän päivämäärä.|
|n|Määrittää, että n:n jälkeinen päivämäärä on sulkemispäivämäärä, kuten N31.12.01.|  

## Aikojen syöttäminen

Kun syötät aikoja, voit lisätä minkä tahansa erotinmerkin yksiköiden väliin, mutta se ei ole tarpeen. Minuutteja, sekunteja tai AM/PM-merkintää (aamupäivä/iltapäivä) ei tarvitse kirjoittaa.  

Seuraavassa taulukossa on luettelo eri tavoista, joilla aikoja voi syöttää ja miten niitä tulkitaan:  

|Tapahtuma|Tulkinta|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:5,50|05:30:05.5|  
|053005050|05:30:05.05|  

 Jos et käytä erotinmerkkiä, jokaiselle aikayksikölle tulee syöttää kaksi numeroa.  

## Yhdistettyjen päivämäärien ja aikojen syöttäminen

[!INCLUDE [datetimes](includes/datetimes.md)]

## Keston syöttäminen

Kesto syötetään numerona, jota seuraa sen mittayksikkö.  

Seuraavassa on muutamia esimerkkejä:  

|Kesto|Mittayksikkö**|  
|------------------|-------------------------|  
|2t|2 tuntia|  
|6t 30 m|6 tuntia 30 minuuttia|  
|6,5t|6 tuntia 30 minuuttia|  
|90 m|1 tunti 30 minuuttia|  
|2p 6t 30m|2 päivää 6 tuntia 30 minuuttia|  
|2p 6t 30m 56s 600ms|2 päivää 6 tuntia 30 minuuttia 56 sekuntia 600 tuhannesosasekuntia|  

 Voit syöttää myös numeron, jonka ohjelma muuntaa automaattisesti kestoksi. Syöttämäsi numero muunnetaan kestokenttään määritellyn oletusmittayksikön mukaisesti.  

 Voit tarkastaa, mitä mittayksikköä kestokentässä käytetään, syöttämällä numeron ja katsomalla, mihin mittayksikköön ohjelma muuntaa sen.  

 Numero 5 muunnetaan 5 tunniksi, jos mittayksikkö on tunti.  

## <a name="decimal"></a>Numeeristen näppäimistöjen käyttämän desimaalierottimen asettaminen

Kun syötät tietoja numeronäppäimistön <kbd>desimaalierottimen</kbd> avulla, kenttään syötetty todellinen desimaali erotin määräytyy Business Centralin alueasetuksen mukaan. Useimmat alueet käyttävät piste (.)- tai pilkku (,) -symbolia desimaaliarvojen erottimena, kuten tavallisesti valuuttasummissa. Näppäimistön desimaalinäppäin mukautuu alueeseen. Se on usein eri kuin muun näppäimistön piste- tai pilkkunäppäimet. Määritä alue Business Centralin **Omat asetukset** -sivulla.

Oletetaan esimerkiksi, että käytät numeronäppäimistöä, joka käyttää pistettä (.) <kbd>desimaalierottimen</kbd> näppäimenä. Mutta olet syöttämässä tietoja alueelliselle kielelle, joka käyttää pilkkua (**,**) desimaalierottimena, kuten ranskan (Ranska) kielessä. Haluat siis desimaalit kuten "1.23" syötettävän muodossa "1,23". Tässä tapauksessa voit siirtyä **Omat asetukset** -sivulle ja määrittää **alueen** kohdealuekieleksi **ranska (Ranska)**. Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md#region).

> [!TIP]
> Joskus voi olla tarpeen käyttää desimaalierotinta pisteen (.) syöttämiseen. Oletetaan esimerkiksi, että syötät päivämäärävälin suodattimeen, esimerkiksi `01/01/2022..04/01/2022`tai mikä tahansa, joka edellyttää pistettä. Tämän mahdollistamiseksi valitse numeronäppäimistön <kbd>Alt</kbd>+<kbd>desimaalierotin</kbd>-näppäimiä. Tämä näppäinyhdistelmä vaihtaa desimaalierottimen pisteen syöttämisen ja **Alue**-asetuksessa määritetyn desimaalierottimen välillä.

## Katso myös

[Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen](ui-enter-criteria-filters.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
