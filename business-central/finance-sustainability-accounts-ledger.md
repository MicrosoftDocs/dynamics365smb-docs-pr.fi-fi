---
title: Kestävyystilien tilikartta ja kirjanpito
description: 'Tutustu kestävyystilikartan, -luokat- ja alaluokkien hallintaan sekä kestävyystapahtumien yksityiskohtiin.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Kestävyystilien tilikartta ja kirjanpito 

## Kestävyystilien tilikartta  

**Kestävyystilikartta** (CoSA) muodostaa perustavan rakenteen luettelon, jota käytetään kaikkien päästötietojen tallentamiseen. Se toimii kehyksenä, joka luokittelee ja järjestää kestävyystilit niiden määritteiden, kuten laajuuden tai muiden ryhmittymien, perusteella. Jokaiselle tilille määritetään yleensä yksilöivä koodi tai numero, jota on helppo viitata ja seurata. Tilit ovat rakenteeltaan samat kuin perinteisellä **tilikartalla**, mutta ne on räätälöity erityisesti kestävyyteen liittyvien tietojen ja muuttujien seurantaa varten organisaatiossa. 
 
Käyttäjät voivat lisätä **Tililuokat** ja **Alakategoriat** määrittääkseen, miten järjestelmä toimii, valitsemalla erityiset päästöt seurantaa, päästötekijöitä, kaavoja ja vastaavia määrityksiä varten.  

>[!NOTE]
>GHG (Greenhouse gases) -standardeihin perustuvien päästöalueisiin tutustumista varten on kolme päästöaluetta:  
>- **Vaikutusalueen 1 päästöt**: näihin kuuluvat kiinteistä ja liikkuvista polttolähteistä sekä tahattomista hajapäästöistä johtuvat päästöt. 
>- **Vaikutusalueen 2 päästöt**: näihin kuuluvat epäsuorat päästöt, jotka aiheutuvat palveluntarjoajilta ostetun energian muodostamisesta. 
>- **Vaikutusalueen 3 päästöt**: näihin kuuluvat laaja kirjo päästöjä ostetuista tavaroista ja palveluista sekä pääomahyödykkeistä, polttoaineeseen ja energiaan liittyvistä toiminnoista, alku- ja loppupään kuljetuksista, syntyvästä jätteestä, liikematkoista ja työntekijöiden työmatkoista jne. 

**Kestävyystilikartassa** (CoSA) voi tehdä esimerkiksi seuraavia toimintoja:  

-   Voit tarkastella kestävyyskirjanpitotapahtumat- ja saldot näyttäviä raportteja. 
-   Voita avata **kestävyystilikortin** asetusten lisäämistä tai muuttamista varten.  
-   Katso tilin luokka ja alaryhmä.   
-   Yksittäisen tilin kunkin päästön erillisten saldojen tarkastelu. 
-   Lisää yksi tai useampi **dimensio** jokaiseen tiliin ja aseta dimensiosuodatus. 
    
Voit lisätä, muuttaa tai poistaa **Kestävyystilejä**. Erojen estämiseksi et voi poistaa **Kestävyystiliä**, jos tiliin liittyy yksi tai useampia tapahtumia.  

### Lisää tai muuta tilejä  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kestävyystilikartta** ja valitse sitten vastaava linkki. 
2. **Kestävyystilikartta** (CoSA) -sivulla voit avata jokaisen **Kestävyystilin** ja lisätä tai muuttaa asetuksia. Lue lyhyt kuvaus siirtämällä kohdistin kentän päälle. 

**Summa**-tyyppisten tilien osalta sinun täytyy täyttää **Summausväli**-kenttä. **Loppusumma**-tilien osalta Sisennä-toiminto täyttää tämän kentän automaattisesti. Kun olet määrittänyt kaikki tilit, valitse **Sisennä kestävyystilikartta** -toiminto tehdäksesi sen.  

>[!IMPORTANT]
>Jos olet syöttänyt määritelmiä **Summausväli**-kentässä **Loppusumma**-tileille ennen sisentämistä, sinun täytyy syöttää ne uudestaan, koska Sisennys-toiminto korvaa kaikki arvot **Loppusumma**-kentässä.  

### Poista tilejä  

Voit poistaa **kestävyystilin**. Varmista kuitenkin ennen sen poistamista, että tiliin liittyy yksi tai useampia tapahtumia, sillä Business Central estää sinua poistamasta **kestävyystiliä** tässä tilanteessa.  

## Tililuokat   

Käyttäjien on lisättävä **kestävyystilikategoria** kuhunkin **kestävyystiliin**, määritettävä järjestelmän toimintatapa, valittava päästöjen laajuus, erityiset päästöt seurantaa varten, kaavat ja vastaavat kokoonpanot.  

Voit tarkistaa **kestävyystililuokat** noudattamalla seuraavia vaiheita: 

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kestävyystililuokat** ja valitse sitten vastaava linkki. 
2.  **Kestävyystilin luokat** -sivulla voit muokata aiemmin luotua luetteloa tai luoda uuden luokan. Kun haluat luoda uuden luokan, valitse **Uusi**-toiminto.  
3.  Täytä **Koodi**- ja **Kuvaus**-kentät.   
4.  Määritä **Päästöalue**-kenttä ja valitse yksi vaikutusalueen vaihtoehdoista.  
5.  Valitse seurattavat kaasupäästöt. Tällä hetkellä voit käyttää yhtä vaihtoehdoista: **CO2**, **CH4** tai **N2O**. Voit valita minkä tahansa seurattavan yhdistelmän, mutta seurannassa tulee olla vähintään yksi päästö.  
6.  **Laskentaperuste**-kentässä voit valita minkä tahansa kaavoista, joita haluat käyttää, jos et tiedä tarkkaa päästösummaa. Tässä voit määrittää päästölaskennan laskentaperustan (kaava). Voit valita jonkin seuraavista vaihtoehdoista: **Polttoaine/sähkö**, **Etäisyys**, **Asennus** tai **Mukautettu**. 
7.  Jos valitset **Mukautettu**-kaavan, mukautettu kuvaus voidaan määrittää **Mukautettu arvo** -kentässä.  

>[!NOTE]
>Jos tämä tarjottujen kaavojen sarja **Laskentaperuste**-kentässä ei riitä, voit laajentaa tätä kenttää ja lisätä laskelmia järjestelmään, jota käytetään **kestävyyspäiväkirjoissa**.  

Jos käytät **Laskentaperustetta** (kaavoja), on olemassa kuvaus siitä, miten järjestelmä laskee valitsemasi vaihtoehdon perusteella (**EF** on **päästökerroin**, jonka voit määrittää **Kestävyystilin alaryhmä** -sivulla): 

|  Päästön tyyppi  |  Laskentaperuste  |  Kaava         | Kommentti      |
|------------|--------------|------------------------------|---------------------------------|
| **VAIKUTUSALUE 1**  |
| Kiinteät polttolähteet | Polttoaine/sähkö | Päästöt = Polttoaine * EF | _ts., Polttoaine = Kattiloiden, lämmittimien ja lämpöhapettimien polttoaineen määrä..._ |
| Liikkuvat polttolähteet | Polttoaine/sähkö | Päästöt = Polttoaine * EF | _ts., Polttoaine = Maantie- tai ei-maantieajoneuvoihin, rautatieajoneuvoihin käytetyn polttoaineen määrä..._ |
|  |  |  Päästö = Etäisyys * EF | _ts., Etäisyys = Maantie- tai ei-maantieajoneuvojen, rautateiden mittarilukema..._ |
| Hajapäästöt | Asennus | Päästöt = Asennuskerroin * Mukautettu määrä / 100 * Aikakerroin | _ts., Mukautettu määrä = Kokoonpanotappiot, Vuosittainen vuotamisprosentti..._ |
| **VAIKUTUSALUE 2**  |
| Yleishyödylliset palvelut | Polttoaine/sähkö | Päästöt = Sähkö * EF | _ts., Polttoaine/Sähkö = Sähkömäärä, Höyrymäärä, Lämmitysyksikkö..._ |
|  | Mukautettu | Päästöt = Mukautettu määrä * EF | _ts., Mukautettu määrä = Lämpöyksikkö, Tonnitunti..._ |
| **VAIKUTUSALUE 3**  |
| Ostetut tavarat ja palvelut sekä tuotantohyödykkeet | Mukautettu | Päästöt = Mukautettu määrä * EF | _ts., Mukautettu määrä = Kustannus (KP).._ |
| Alkupään kuljetus ja jakelu | Etäisyys | Päästö = Etäisyys * EF |  |
|  | Etäisyys | Päästö = Etäisyys * Kerroin * EF | _Kerroin = Lastin tonnit_ |
| Loppupään kuljetus ja jakelu | Etäisyys | Päästö = Etäisyys * EF |  |
|  | Etäisyys | Päästö = Etäisyys * Kerroin * EF | _Kerroin = Lastin tonnit_ |
| Myytävien tuotteiden toiminnassa ja loppukäsittelyssä syntyvät jätteet | Mukautettu | Päästöt = Mukautettu määrä * EF | _ts., Mukautettu määrä = Jäte_ |
| Liikematkustus ja työntekijöiden työmatkustus | Etäisyys | Päästö = Etäisyys * EF | _ts., Etäisyys = Käytetyn työsuhdeauton mittarilukema, vuokra-auto, juna, lento..._ |
|  | Mukautettu | Päästöt = Mukautettu määrä * EF | _ts., Mukautettu määrä = Hotellimajoitus..._ |
|  | Polttoaine/sähkö | Päästöt = Polttoaine * EF | _ts., Polttoaine = Yrityksen autoon, vuokra-autoon käytetyn polttoaineen määrä..._ |

## Tilin aliluokat  

Käyttäjien on lisättävä **kestävyystilin alaryhmä** kuhunkin **kestävyystiliin** määrittääkseen päästökertoimia, joita käytetään kaavoissa, mutta se perustuu **kestävyystilikategorian** päästöjen seurannan valintaan.  

Voit tarkistaa **kestävyystilin alaluokat** noudattamalla seuraavia vaiheita:  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kestävyystilin alaluokat** ja valitse sitten vastaava linkki. 
2.  **Kestävyystilin alaluokat** -sivulla voit muokata aiemmin luotua luetteloa tai luoda uuden luokan. Kun haluat luoda uuden luokan, valitse **Uusi**-toiminto.  
3.  Täytä **Koodi**- ja **Kuvaus**-kentät.   
4.  **Kestävyystililuokassa** seurattavien kaasupäästöjen perusteella ja tämän alakategorian liittämiseksi voit täyttää myös yhden tai useamman päästötekijän: 

   - **Päästökerroin CO2** - Määrittää CO2-päästön päästökertoimen.  
   - **Päästökerroin CH4** - Määrittää CH4-päästön päästökertoimen. 
   - **Päästökerroin N2O** - Määrittää N2O-päästön päästökertoimen.  

5.  Jos tämä alaryhmä liittyy uusiutuvaan energiaan, valitse **Uusiutuva energia** -kenttä.   

>[!NOTE]
>**Tuo tiedot**- ja **Tuo kohteesta** -kentät on tarkoitettu mahdolliseen integrointiin ulkoisten järjestelmien kanssa, joita käytetään päästökertoimien keräämiseen, mutta vuoden **2024 1. julkaisuaaltoa** ei voi käyttää oletusarvoisesti ominaisuutena.  

## Vastuullisuustapahtumat  

**Kestävyyskirjaukset** tallentavat kaikkien kirjattujen kestävyystransaktioiden historian ja organisoivat kaikki päästötiedot **kestävyystilikartan** mukaan. Kun käyttäjä kirjaa **kestävyyspäiväkirjan**, kaikki ratkaisevat tiedot tallennetaan sinne. Kaikki aktiiviset raportit on luotu **kestävyyskirjaustapahtumien** perusteella.   

Käyttäjä voi avata tämän tilitapahtuman tietylle tilille käyttämällä **Kestävyystilin kaavio** -sivun **Tapahtumakirjaukset**-toimintoa , tai kun haluat avata kaikki tapahtumat, valitse ![Lamppu, joka avaa Kerro minulle -ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kestävyyskirjaustapahtumat** ja valitse sitten vastaava linkki. Lue lyhyt kuvaus siirtämällä kohdistin kentän päälle.  

>[!IMPORTANT]
>Kun olet kirjannut tiedot kestävyystapahtumiin, et voi poistaa niitä. Jos teit virheen, voit kirjata vastakirjauksen käyttäen samoja yksityiskohtia, mutta käyttämällä summalle negatiivista merkkiä.  

## Katso myös  
[Rahoitus](finance.md)    
[Kestävyyden hallinnan yleiskuvaus](finance-manage-sustainability.md)
[Kestävyyden määritys](finance-sustainability-setup.md)
[Päästöjen tallennus](finance-sustainability-journal.md)
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman toiminta](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
