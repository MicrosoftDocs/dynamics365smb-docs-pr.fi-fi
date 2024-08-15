---
title: 'Varaustapahtuma-taulukko - Ominaisuudet, jotka päivittävät Varaustapahtuma-taulukon | Microsoft-asiakirjat'
description: 'Tämä antaa ohjeita, jotka auttavat sinua ymmärtämään ja vianetsintään varaustapahtuma-taulukon epäjohdonmukaisuuksia.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Varaustapahtuma-taulukko - Johdatus

Tässä teknisessä valkoisessa paperissa *on ohjeita, jotka auttavat ymmärtämään ja vianetsintään varaustapahtuma-taulukon* (taulukko 337) epäjohdonmukaisuuksia Microsoft Dynamics NAV. Ensimmäinen osa on tämän taulukon tietoja luovien tai muokkaavien toimintojen esittely. Se kattaa myös useita Varaustapahtuma-taulukon *kenttiä*, jotka kannattaa osoittaa näiden ominaisuuksien yhteydessä. Toisessa osassa havainnollistetaan esimerkeillä, miten Varaustapahtuma-taulukon *tapahtumia* luodaan, poistetaan tai muokataan silloin, kun siirtotilauksia käsitellään tai suunnittelutoimintoja suoritetaan.

Varaustapahtuma-taulukkoa *käytetään* käsittelemään ja tallentamaan tietoja, jotka koskevat varausta, nimikeseurantaa ja tilauksen seurantaa.

Kun käsitellään nimikeseurantaa osittaisella kirjauksella, taulukko toimii yhdessä Seurannan määrittely *-* taulukon (Taulukko 336) kanssa. Käyttäjän Nimikkeen seurantarivit **-sivulle syöttämät** tiedot luodaan väliaikaiseen taulukon 336 versioon, ja ne on sidottu taulukkoon 337 ja seurannan määrittelytaulukkoon, kun sivu suljetaan.

Varaustapahtuma-taulukkoon *luodut tiedot määräytyvät* yleisesti ottaen sen mukaan, mitä ominaisuuksia käytät ja mitkä parametrit valitsit nimikkeen kortti. Näitä ovat esimerkiksi seuraavat:

- Tilauksen seurannan menettelytapa
- Varaustapa
- Suoritettavat suunnittelutoiminnot
- Uusintatilaus- ja tuotantotapa
- Nimikkeen tai varastointiyksikön suunnitteluparametrit kortti
- Nimikkeen seurantakoodi

## Ominaisuudet, jotka päivittävät Varaustapahtuma-taulukon

### Tilauksen seurannan menettelytapa

 **Jos nimikkeen Tilauksen seurantatapa** -kentän arvoksi on määritetty Ei mitään, Microsoft Dynamics NAV  varaustapahtuma-taulukkoon *ei luoda varaustapahtumia*, ellei Nettomuutossuunnitelma- tai Uudelleensuunnittelu-, Varaus- tai Nimikeseurantaa suoriteta. Lisäksi ilman tilauksen seurantaa voi olla varaustapahtumia, kun käytetään Tuotanto-tilaus- tai Kokoonpano-tilaukseen -käytäntöjä.

Tilauksen seurantatavan **voi määrittää** Ei mitään, jos et vaadi kysynnän seurantaa lennossa tarjontaa vastaan tai päinvastoin. Tilauksen seurantatoiminto tai suunnittelumoduuli käsittelee tarjonnan seurannan kysyntään verraten. Tilauksen seurantaa ei kannata käyttää yhdessä suunnittelutoimintojen kanssa.

Kun määrität **Tilauksen seurantatapa** -kentän arvoksi Vain seuranta, Microsoft Dynamics NAV  tapahtumat luodaan aina taulukkoon 337 aina, kun nimikkeelle luodaan tilaus, mutta **taulukon 337 Varauksen tilaksi** ei aina ole määritetty vain Seuranta. Harkitse seuraavaa skenaariota:

> [!NOTE]  
> Käsittelypäivämääräksi on asetettu 23.1.2014 (KK/TP/VVV) kaikille esimerkeille. 
  
1. Luo nimike, jonka **Tilauksen seurantatapa** -kentän arvona on Vain seuranta.  
1. Luo ostotilaus. Microsoft Dynamics NAV luo varaustapahtuman, **jonka varaustila** on Ylijäämä, koska ostotilausta ei ole vielä kohdistettu kysyntään.
1. Luo myyntitilaus. Microsoft Dynamics NAV luo nyt uuden varaustapahtuman, jolla on **varauksen seurantatila** .

Vaihe **2 luodun varauksen tila** päivitetään Seuranta-tilaksi, ja Microsoft Dynamics NAV tila päivitetään automaattisesti. Tämä konsepti on nimeltään Dynaaminen seuranta.
 **Määrittämällä nimikkeen Tilauksen seurantatapa** -kentän arvoksi Vain seuranta käyttäjä voi käyttää tilauksen seuranta -ominaisuutta nähdäkseen yleiskuvan siitä, mihin tarjontaan kysyntä on kohdistettu, ja päinvastoin.

> [!NOTE]  
> Seurantatoiminto ei korvaa suunnittelutoimintoa, joka ottaa kaikki nimikkeet, vaatimukset ja tarvikkeet huomioon ja tarjoaa optimaaliset suunnitteluehdotukset asiakaspalvelutasojen optimoimiseksi ja varastotasojen tasapainottamiseksi.

### Varaustapa

Varaus koostuu Varaustapahtuma-taulukon tietueparista *, jolla on* varauksen tila **ja jolla on sama tapahtumanumero.**  Yhdessä tietueessa Positiivinen-kenttä on käytössä ja se osoittaa tarjontaan. Toisen tietueen Positiivinen-kenttä **ei** ole käytössä ja se osoittaa kysyntään. Lähdetyyppi- **, Lähdeviitteen nro**- ja **Lähdetunnus-kentissä** **korostetaan kysynnän ja tarjonnan välistä varauslinkkiä** .

Lähdetyyppi-kentän **tiedot** ovat varaustapahtuman **nro -taulukko.** -kenttä liittyy. Jos kyseessä on esimerkiksi kysyntätapahtuma (negatiivinen), tapahtuma voi olla *Myyntitilaus-taulukko* (taulukko 37) tai *Suunnittelun komponentti*  (taulukko 99000829).

 **Lähdetunnus-kentässä** on lähdetyyppiin viitatun taulukon asiakirjan tunnus.

Lähde **viitenro** Kentässä on viitenumero riville, jonka varaustapahtuman **nro** liittyy. Jos tapahtuma liittyy myynti- tai ostoriviin, päiväkirjariviin tai hankintariviin, tämän kentän tiedot kopioidaan Rivinro-kentästä **.** -kentässä. Jos tapahtuma liittyy Nimiketapahtuma-taulukon *(taulukko 32) tapahtumaan*, tämän kentän tiedot kopioidaan Tapahtumanro-kentästä. **Nimiketapahtuma**-taulukon *kentästä*.

Kun käytät varauskäytännön vaihtoehtoa Aina yhdessä tilauksen seurannan kanssa, molemmat ovat yleensä synkronoituina. Kun varaus kuitenkin poistetaan tai tarjonnan vastaanottopäivämäärää siirretään eteenpäin kysynnän eräpäivän jälkeen, tilauksen seuranta poistetaan. Saatat myös havaita virhesanoman, jossa Microsoft Dynamics NAV kysytään, kuinka aiemmin luotujen varausten kanssa tulee tehdä. Esimerkkitilannetta havainnollistetaan seuraavassa esimerkissä:

1. Luo uusi nimike nimeltä COMP. Määritä seuraavat kentät:
  - **Täydennysjärjestelmä**: Osto
  - **Tilauksen seurantatapa**: Vain seuranta
  - **Varaa**: Aina
2. Luo toinen nimike nimeltä FG. Määritä seuraavat kentät:
  - **Täydennysjärjestelmä**: Tuotantotilaus
  - **Tilauksen seurantatapa**: Vain seuranta
  - **Varaa**: Aina
3. Luo toinen nimike nimeltä FG. Määritä seuraavat kentät:
  - **Nimike**: COMP
  - **Määrä per**: 1
4. Hyväksy tuotannon tuoterakenteen nro. Tuoterakenteen naisten sukuelinten silpominen ja liitäminen nimikkeen FG:hen.
5. Luo ostotilaus. Määritä seuraavat kentät:
  - **Nimike**: COMP
  - **Määrä**: 10
  - **Sijaintikoodi**: SININEN
  - **Oletettu vast.ottopvm**: 24.01.2014
6. Luo myyntitilaus. Määritä seuraavat kentät:
  - **Lähetyksen pvm**: 14.02.2014
  - **Sijaintikoodi**: SININEN
  - **Nimike**: COMP
  - **Määrä**: 10

> [!NOTE]  
> Automaattinen varaus on suoritettu osto- ja myyntitilauksen välillä. Lisäksi osto- ja myyntitilausten välille on luotu tilauksen seuranta.

7. Luo manuaalinen vapautettu tuotantotilaus. Määritä seuraavat kentät:
  - **Nimike**: 14.02.2014
  - **Määrä**: 10
  - **Sijainti**: SININEN
  - **Eräpäivä**: 01.02.2014
8. Valitse **Aloitus-välilehden** Prosessi-ryhmässä **Päivitä tuotantotilaus**.
9. Avaa komponenttiluettelo ja etsi Nimikekomponentti.

> [!NOTE]  
> Varausta tai tilausseurantaa Microsoft Dynamics NAV ei luoda. Syy on se, että vaihe 6 luotua myyntitilausta vastaan on jo varaus.

Oletetaan, että liiketoimintasyistä nimikettä tarvitaan kiireellisemmin vapautetussa tuotantotilauksessa, joka on luotu vaihe 7. Seuraavassa peruutamme seuraavaksi varauksen vaihe 6 luodusta myyntitilauksesta ja huomaamme, miten tilauksen seurantaa käsitellään.

10. Etsi Nimikkeen COMP -nimikkeen myyntitilaus vaihe 6:sta ja peruuta varaus.
11. Avaa ostotilaus vaihe 5:stä ja huomaa, että ostotilauksen ja vapautetusta tuotantotilauksesta tarvittavan komponentin välille luodaan nyt tilausseuranta.
12. Luo uudelleen varaus vapautetusta tuotantotilauksesta tarvittavan komponentin ja ostotilauksen tarjonnan välille vaihe 5.

> [!NOTE]  
> Varausta ei luoda uudelleen, mikä tulee tehdä manuaalisesti.

13.  **Muuta ostotilausotsikon Oletettu vast.ottopvm** -kentän arvo 24.1.2014 vaihe 5.2.2014 ja 5.2.2014.

Microsoft Dynamics NAV näyttöön tulee seuraava varoitussanoma:

   Tälle tilaukselle on olemassa varauksia. Nämä varaukset peruutetaan, jos muutos aiheuttaa tietojen ristiriidan. Haluatko jatkaa?

14. Valitse Kyllä. Etsi ostotilauksen varaus- ja tilausseurantatapahtumat.

> [!NOTE]  
> Aiemmin luotu varaus peruutetaan, ja se tulee luoda uudelleen manuaalisesti. Tilaus on kuitenkin dynaaminen, ja se on luotu uudelleen Microsoft Dynamics NAV ostotilauksen ja myyntitilauksen välille. Syy on vapautetun tuotantotilauksen (01.02.2014) kysyntä ennen tarjonnan oletetun vastaanottopäivämäärän päivämäärää.

Tässä kentässä on esimerkki automaattisten varausten ja tilausten seurannan välisestä vuorovaikutuksesta. Esimerkeistä käy ilmi, mitä tapahtuu, kun muutat eräpäiviä, ja virhesanoma, joka käynnistyy silloin, kun varausristiriita ilmenee.

### Laskettu suunnittelu

Suunnittelu, joka tehdään tilauksen suunnittelun, hankintalistan tai suunnittelutyökirjan avulla, luo tapahtumia *Varaustapahtuma-taulukkoon*  **. Varauksen tila** -kentän arvona on Seuranta, Varaus tai Ylijäämä. Aina tulisi olla vastaava pari, jolla on sama Tapahtumanumero. jos tila on Seuranta tai Varaus, Määrä (perus) **-kentässä on positiivinen ja negatiivinen arvo** .  **Lähdetyyppi-kenttä** on kysyntätyyppi eli negatiivisen määrän taulukko 37 ja positiivisen määrän suunnittelutaulukko, esimerkiksi taulukko 246. Lähdetunnus-kenttä **on** SUUNNITTELU.

Jos kysyntää tai tarjontaa ei ole kohdistettu, Microsoft Dynamics NAV  Varaustila-kentän **arvoksi tulee** Ylijäämä. Varaustilaksi voi määrittää esimerkiksi Ylijäämä, jos nykyinen varasto alittaa ennusteeseen linkitetyn varmuusvaraston määrän tai kysynnän.

 *Ei-seurattu suunnitteluelementti* -taulukossa (taulukko 99000855) on tietoja ei-seurattuista määristä, jotka näytetään, kun käyttäjä tekee tilauksen seurantasivulta haun ei-seurattuja määriä varten tai valitsee varoituskuvakkeen suunnittelutyökirjaan. Taulukko sisältää tapahtumia, jotka selittävät ei-seuratun ylijäämämäärän tilauksen seurantaverkossa.

Tapahtumat luodaan suunnitteluajon aikana ja ne selvittävät, mistä tilauksen seurantarivien ei-seurattu ylijäämämäärä on peräisin. Ei-seurattu ylijäämä voi olla peräisin seuraavista kohteista:

- Tuotantoennuste
- Puitetilaukset
- Varmuusvaraston määrä
- Uusintatilauspiste
- Enimmäisvarasto
- Uusintatilausmäärä
- Enimmäistilausmäärä
- Vähimmäistilausmäärä
- Tilauskerrannainen
- Vaimennin (% eräkoosta).

Varaustapahtuma-taulukossa *·*, kuten Osto-, Siirto- ja Tuotantotilauksissa, on Suunnittelun **joustavuus** -kenttä. Tässä asetuskentässä määritetään, ottaako suunnittelujärjestelmä näiden toimitustilausten tarjonnan huomioon toimenpideviestien laskennassa. Jos kentässä on vaihtoehto Rajaton, suunnittelujärjestelmä sisällyttää rivin laskiessaan toimenpideviestejä. Jos kentässä on vaihtoehto Ei mitään, rivi on kiinteä, eikä sitä voi muuttaa. Suunnittelujärjestelmä ei sisällytä riviä toimenpideviestien laskentaan. Ominaisuutta hallitaan *Varaustapahtuma-taulukossa* samannimisen kentän avulla.

### Uusintatilaus- ja tuotantotapa

Jos suunnitteluominaisuus toteutetaan sellaiselle nimikkeelle, jonka uusintatilaustavana on Tilaus, Varaustapahtuma-taulukkoon Microsoft Dynamics NAV luodaan tapahtumia *,*  joiden varaustila on Seuranta-sijaan Varaus.

Lähdetyyppi **-** ja **Lähdetunnus-kentät** vastaavat muiden uusintatilaustapojen käsittelyä.  **Varaustapahtuma-taulukon**  *Sidonta-kenttään*  Microsoft Dynamics NAV kuitenkin kirjoitetaan Tilausasiakkaan tilaus.

Sidonta-kenttä **täytetään**, kun halutaan hallita tiettyä kysyntään sidottuja toimitustilauksia, esimerkiksi tuotantotilauksia, jotka on luotu suoraan myyntitilauksesta. Tässä kentässä näkyy Tilaus tilauskohtainen silloin, kun tapahtuma on sidottu erityisesti kysyntään tai tarjontaan (Automaattinen varaus). Kysyntä voi liittyä myynti- tai komponenttitarpeisiin.

### Nimikeseuranta ja prospektin varaustapahtuma

Prospektin varauksen tila voidaan luoda Microsoft Dynamics NAV  *Varaustapahtuma-taulukossa* silloin, kun tilausverkko-objekteja eli Tilauksen seurantaa ei käytetä. Esimerkiksi kulutuspäiväkirjan rivillä komponentille määritellään nimikeseuranta. Jos nimikettä on jo seurattu, Microsoft Dynamics NAV  lisää Prospektin varaustapahtumia voi kuitenkin luoda. Tämä käy ilmi tämän asiakirjan toisessa osassa siirtotilauksiin liittyvässäEXAMPLE 2 -kohdassa.

Kun tarkastelet tai muutat **Nimikkeen seurantarivit** -sivua, Seurannan määrittely - *taulukon (Taulukko 336) ja* Varaustapahtuma-taulukon *kollektiivinen sisältö* esitetään väliaikaisessa taulukossa 336. Tämä varmistaa, että aiempia ja aktiivisia nimikkeen seurantatietoja voi käyttää yhtenä pakettina.

Varaukset jakautuvat kahteen luokkaan: Määrittelemättömiin varauksiin, joissa erä- ja sarjanumeroita ei ole määritetty varaushetkellä, ja Spesifisiin varauksiin, joissa varataan tiettyjä erä- tai sarjanumeroita varastosta.

Ei-pakotettavalle varaukselle Eränro **tai** **Sarjanro** -kenttä on tyhjä Tapahtumanro-kentässä **.** taulukossa 337, joka osoittaa kysyntään (esimerkiksi myyntiin). Varauslogiikan Microsoft Dynamics NAV rakenteen takia, kun nimikeseurannassa olevalle nimikkeelle tehdään ei-määritelty varaus varastoon, tulee kuitenkin valita tietyt nimiketapahtumat, Microsoft Dynamics NAV  joita vastaan varataan.

Koska nimiketapahtumilla on nimikeseurannan tiedot, varaus varaa epäsuoraan tietyt erä- tai sarjanumerot, vaikka käyttäjä ei sitä aikonutkaan. Jos sidonta on myöhästyny, Microsoft Dynamics NAV  se kuitenkin varataan tiettyjä tapahtumia vastaan, mutta käyttää kirjauksessa uudelleenjärjestelymekanismia Microsoft Dynamics NAV .

Lisätietoja Microsoft Dynamics NAV on asiakirjan lopussa olevassa Lisäresurssit-kohdassa luetelluissa teknisissä asiakirjoissa.

### Lähde-alatyyppi-, Peruutettu toimenpideviesti-, Toimenpideviestin muutos- ja Estä peruutus -kentät

Varaustapahtuma-taulukon Lähde-alatyyppi **-,** Peruutettu toimenpideviestin **muutos** **- ja** Estä peruutus - **kentät** *on kuvattu tässä osassa.*  Esimerkkitilanteissa havainnollistetaan Peruutettu toimenpideviesti -, **Toimenpideviestin** muutos **- ja** Peruuta peruutus - **kenttien käyttöä.**   **Toimenpideviestin muutos -** kenttää käytetään tilauksen seurantatavan toiminnolle Seuranta ja Toimenpideviesti.  **Peruuta peruutus -** kenttää käytetään kokoonpano-tilaukseen -ominaisuutta varten vuonna Microsoft Dynamics NAV 2013.

#### Lähteen alatyyppi

Lähteen **alatyyppi -** kenttä ilmaisee, mihin Alatyypin lähteeseen varaustapahtuma liittyy. Jos tapahtuma liittyy osto- tai myyntiriviin, kenttä kopioidaan rivin **Asiakirjatyyppi-kentästä** . Jos kenttä liittyy päiväkirjan riviin, ohjelma kopioi kentän päiväkirjarivin **Tapahtuman tyyppi** -kentästä.

#### Laukkautettu toimenpideviesti

Tukahdutettu **toimenpide msg.** -kenttä tallentaa tiedot silloin, kun aiemmin luotu tarjonta on jo osittain käsitelty, esimerkiksi silloin, kun ostotilaus on jo osittain vastaanotettu tai tuotantotilauksen kulutus on kirjattu sitä vastaan.

Kun suunnittelu suoritetaan, Microsoft Dynamics NAV  merkitsee tämän kentän ja määrittää Varaustapahtuman **tila** -kentän arvoksi *Ylijäämä8. Esimerkkinä käytetään seuraavaa:

1. Avaa Nimike 80001. Määritä seuraavat kentät:
  - **Uusintatilaustapa**: Erä-erästä
  - **Varaa**: Valinnainen
  - **Tilauksen seurantatapa**: Ei mitään
2. Luo myyntitilaus. Määritä seuraavat kentät:
  - **Nimike**: 80001
  - **Sijainti**: Tyhjä/Ei mitään
  - **Määrä**: 10
  - **Lähetyksen pvm**: 15.2.2014
3.  **Avaa hankintalistat** ja suorita **Laske suunnitelma -** eräajo nimikkeen 80001 osalta.
  - **Aloituspvm**: 23.01.2014
  - **Lopetuspvm**: 01.03.2014
4. Suunnitteluehdotus annetaan 10:n määrän täydentämiseksi uudella ostotilauksella ja **eräpäivällä** 15.2.2014.
5. Luo **ostotilaus, jonka** oletettu vast.ottopvm **on 15.2014, valitsemalla** Toiminnot-välilehden **Funktiot-ryhmässä Toteuta toimenpideviesti** .
6. Avaa ostotilaus vaihe 5:stä ja määritä **Vastaanotettava** määrä -arvoksi 2 ja kirjaa vain vastaanotto.
7. Avaa myyntitilaus vaihe 2 ja muuta **lähetyksen päivämääräksi** 10.2.2014.
8.  **Avaa hankintalistat** ja suorita Nimikkeen 80001 Laske suunnitelma **-ajo** .
  - **Aloituspvm**: 23.01.2014
  - **Lopetuspvm**: 01.03.2014
9. Suunnitteluehdotus annetaan 8:n määrän täydentämiseksi uudella ostotilauksella ja **eräpäivällä** 10.2.2014.

Taulukon 337 tilatiedot näkyvät seuraavassa kuvassa.

Taulukon 337 tapahtumanumerolla 28 on varaustilan Seuranta, joka vastaa nimiketapahtumaan 318 kirjattua varastoa, joka sisältää kaksi yksikköä, ja avointa kysyntää Myyntitilaus-taulukossa 37. Seuraavalla Tapahtumanrolla 29 on myös varauksen tilan seuranta ja se linkittää jäljellä olevan 8 yksikön määrän Myyntitilaus-taulukon 37 kysynnän ja Hankintarivi-taulukon 246 ehdotetun tarjonnan välille.

Tapahtumanro 30 on olemassa oleva ostotilaus, joka on vastaanotettu osittain määrällä 2. Tämän seurauksena **Varauksen tila -** kentän arvo on Ylijäämä, ja Microsoft Dynamics NAV se määrittää **Määrä (perus)** -kentän arvoksi *8*  (jäljellä oleva saldo) ja **Vaimennetun toiminnon määritteet.** -kenttä on käytössä.

#### Toimenpideviesti muutos

Toimenpideviestin **muutos** -kentässä näkyy tilauksen seurannan tarjontapuolen muutos, joka saadaan aikaan silloin, kun hyväksyt asiaan liittyvät toimenpideviestit. Tässä kentässä näkyy arvo vain silloin, kun sekä tilausseurannan että toimenpideviestien toiminnot ovat aktiivisia (Tilauksen seuranta -käytännöksi on asetettu Seuranta ja toimenpideviesti). Arvo lasketaan Toimenpideviestitapahtuma-taulukon *tietojen perusteella* (taulukko 99000849). Esimerkkinä käytetään seuraavaa:
1. Avaa nimike 80002. Määritä seuraava kenttä:
 - **Tilauksen seurantatapa**: Seuranta ja toimenpideviesti
2. Luo myyntitilaus. Määritä seuraavat kentät:
  - **Nimike**: 80002
  - **Sijainti**: SININEN
  - **Määrä**: 100
3.  **Avaa Tilauksen suunnittelu** -sivu ja suorita **Laske suunnitelma -** eräajo.
4. Valitse myyntitilaus vaihe 2:sta ja suorita **Tee tilaukset -** eräajo.
5. Muuta **myyntitilauksen määrä-kentän arvo** vaihe 2:sta 100:sta 105:een.
Taulukon 337 tilatiedot näkyvät seuraavassa kuvassa.
6. Tapahtumanumerolla 34 on toimenpideviestin muutos **-kenttä** taulukossa 337 käytössä 5 yksikössä, joiden varaustila on Ylijäämä. Kun myyntitilausta lisättiin 5 vaihe, varaus luotiin, Microsoft Dynamics NAV  koska tarjontaa tarvitaan enemmän.
7.  **Avaa Suunnittelutyökirjat-sivu** ja **valitse** Aloitus-välilehden **Prosessi-ryhmässä**  **Hae toimenpideviestit**. Microsoft Dynamics NAV ehdottaa ostotilausmäärän kasvattamista 100:sta 105:een.

#### Älä salli peruutusta

 **Peruuta peruutus -** kenttä ilmaisee, että varaustapahtuma edustaa myyntitilausrivin ja kokoonpanotilauksen välistä linkkiä. Varausta ei voi poistaa, koska sitä tarvitaan ylläpitämään synkronointia, joka ilmenee, kun nimike kootaan tilaukseen. Esimerkkinä käytetään seuraavaa:

1. Luo ostotilaus. Määritä seuraavat kentät:
  - **Perusmittayksikkö**: PCS
  - Mahdolliset oletuskirjausryhmät
  - **Täydennysjärjestelmä**: Kokoonpano
  - **Kokoonpanotapa**: Tilausten kokoaminen
  - **Tilauksen seurantatapa**: Vain seuranta
2. Luo uusi nimike nimeltä Assemble COMP. Määritä seuraavat kentät:
  - **Perusmittayksikkö**: PCS
  - Mahdolliset oletuskirjausryhmät
  - **Täydennysjärjestelmä**: Osto
  - **Tilauksen seurantatapa**: Vain seuranta
3. Avaa nimikkeen Kokoonpano FG ja **valitse Navigoi-välilehden**  **Kokoonpano-/tuotantoryhmässä** Kokoonpano **ja valitse** sitten Kokoonpanon tuoterakenne **.** Määritä kokoonpanon tuoterakenteessa seuraavat kentät:
  - **Tyyppi**: Nimike
  - **Nro**: Kokoa COMP
  - **Määrä per**: 1 Valitse OK-painike **·** .
4. Avaa nimikepäiväkirja ja lisää Koontilaskun COMP-varaston määräksi 10 sijaintia SININEN vastaan ja kirjaa päiväkirjarivi.
5. Luo myyntitilaus. Määritä seuraavat kentät:
  - **Nimike**: Kokoa FG
  - **Sijainti**: SININEN
  - **Määrä**: 1 Taulukon 337 tilatiedot näkyvät seuraavassa kuvassa.

Tapahtumanumerolla 82 varaustilan ylijäämä on 9 yksikköä varaston Kokoonpanon kompon. -kentässä, eikä sillä ole kysyntää. Tapahtumanumero 84 seuraa varaustapahtumia Kokoonpanorivi-taulukon *901 kysynnän* ja nimiketapahtuman 346 tarjonnan välillä.

Tapahtumanumerolla 86 on sitova tilaustilaus ja varauksen tilavaraus. Lisäksi **Peruuta peruutuksen peruutus -** kenttä on käytössä, koska kokoonpanokäytännöksi on määritetty Kokoonpano tilaukseksi nimikkeen Kokoonpano FG osalta. Suunnittelun **joustavuus** -kentän arvoksi määritetään Ei mitään, koska Microsoft Dynamics NAV suunnittelulogiikka ei voi poistaa varausta.

#### Poimittavissa ja varattavissa oleva määrä

Varattu poiminta **ja toimitusmäärä** -kenttä taulukossa 337, joka on versioissa ennen Microsoft Dynamics NAV vuotta 2013, ohjaa nimikkeen saatavuutta hallinnoidussa fyysisessä varastossa. Kaikissa varastoinninhallinnan asennuksissa Microsoft Dynamics NAV nimikemääriä on sekä fyysisen varastoinnin tapahtumina että nimiketapahtumina. Näillä kahdella tapahtumatyypillä on eri tiedot siitä, missä nimikkeitä on ja onko niitä saatavilla. Fyysisen varastoinnin tapahtumat määrittävät nimikkeen saatavuuden varastopaikan ja varastopaikan tyypin mukaan. Jälkimmäistä kutsutaan myös varastopaikan sisällöksi. Nimiketapahtumat määrittävät nimikkeen saatavuuden lähtevien asiakirjojen varauksen perusteella. Poiminta-algoritmissa on erityistoimintoja, joiden avulla lasketaan poimittavissa oleva määrä silloin, kun varastopaikan sisältö yhdistetään varauksiin. Poimintaalgoritmi vähentää muille lähteville asiakirjoille varatut määrät, aiemmin luotujen poiminta-asiakirjojen määrät ja poimitut määrät, joita ei ole vielä toimitettu tai kulutettu. Tulos näkyy **Poimintatyökirja-sivun** Poimittava **saatavilla oleva määrä -kentässä**, jossa kenttä lasketaan dynaamisesti. Arvo lasketaan myös silloin, kun käyttäjä luo fyysisen varastoinnin poimintoja suoraan lähtevistä asiakirjoista, kuten myyntitilauksista, tuotannon kulutuksesta tai lähtevistä siirroista.

*Poimittavissa oleva määrä = poiminnan varastopaikkojen määrä - poimintojen ja siirtojen määrä – (varattu määrä poiminnan varastopaikoista + poimintojen ja siirtojen varattu määrä).*

Seuraavassa esimerkissä on esimerkki siitä, miten poimittavissa olevan määrän arvo on laskettu Microsoft Dynamics NAV:

1. Luo uusi nimike nimeltä F. var. nimike. Määritä seuraavat kentät:
  - **Perusmittayksikkö**: PCS
  - Mahdolliset oletuskirjausryhmät
  - **Täydennysjärjestelmä**: Osto
  - **Varaa-menettely**: Aina
  - **Tilauksen seurantatapa**: Vain seuranta
2. Luo ostotilaus toimittajaa 60000 vastaan. Määritä seuraavat kentät:
  - **Nimike**: F. var. nimike
  - **Sijainti**: VALKOINEN
  - **Määrä**: 100
3. Vapauta ostotilaus ja luo fyysisen varastoinnin vastaanotto.
4. Kirjaa fyysisen varastoinnin vastaanotto ja rekisteröi fyysisen varastoinnin hyllytys määrälle 100.
5. Luo toinen ostotilaus toimittajaa 60000 vastaan. Määritä seuraavat kentät:
  - **Nimike**: F. var. nimike
  - **Sijainti**: VALKOINEN
  - **Määrä**: 10
6. Vapauta ostotilaus ja luo fyysisen varastoinnin vastaanotto.
7. Kirjaa vain fyysisen varastoinnin vastaanotto. Älä rekisteröi fyysisen varastoinnin hyllytystä.
8. Luo myyntitilaus. Määritä seuraavat kentät:
  - **Nimike**: F. var. nimike
  - **Sijainti**: VALKOINEN
  - **Määrä**: 10 Varausmääräksi asetetaan automaattisesti 10, koska Varaa-käytännöksi on määritetty Aina.
9. Luo myyntitilaus. Määritä seuraavat kentät:
  - **Nimike**: F. var. nimike
  - **Sijainti**: VALKOINEN
  - **Määrä**: 100 Varausmääräksi asetetaan automaattisesti 100, koska Varaa-käytännöksi on määritetty Aina.
10. Vapauta ensimmäinen myyntitilaus vaihe 8:sta ja luo fyysisen varastoinnin toimitus.
11. Vapauta fyysisen varastoinnin toimitus ja **valitse** Toiminnot-välilehdessä **Luo poiminta**.
Näyttöön tulee seuraava virhesanoma: *Ei mitään käsiteltävää.*
  Syy on se, että poimittava määrä on nolla. Määrä lasketaan seuraavasti: Varastossa oleva määrä = 110 Poimittavissa oleva määrä = 100

> [!NOTE]  
> Hyllytyksen tai vastaanottovarastopaikan määrä ei ole poimittavissa.
   
   Myyntitilauksille varattu kokonaismäärä on 110 poimittavissa olevaa määrää = 100 - 110 = nolla.

Kun fyysisen varastoinnin hyllytys rekisteröidään vaihe 7, fyysisen varastoinnin poiminta voidaan luoda vaihe 11. Versioissa ennen vuotta Microsoft Dynamics NAV 2013 Varaus poiminta **ja toimitusmäärä** -taulukon 337 kenttään lisätään määrä 10 varaus.

Seuraava kuva on otettu 2009 R2:sta Microsoft Dynamics NAV .

## Siirtotilauksia ja suunnittelua käyttävät kuvat

### Siirtotilaukset

Kun käytetään siirtotilauksia ja nimike toimitetaan, mutta ei kokonaan vastaanotettu, *Varaustapahtuma-taulukossa* on varaustila Ylijäämä. Sijaintikoodi on kohteeseen-sijainti.

Lähde **viitenro** Kentän arvo lasketaan kirjatussa siirtotoimituksessa olevan nimikkeen viimeisen rivitapahtuman numeron + rivitapahtuman numeron perusteella.

Kun tilauksen seuranta on aktivoitu eikä kysyntää (myyntitilausta tai kulutusta) ole, Microsoft Dynamics NAV  luo taulukkoon 337 kaksi merkintää, joiden varaustila on Ylijäämä. Toinen on Siirtorivi-taulukkoa *5741* vastaan ja toinen Nimiketapahtuma-taulukkoa 32 vastaan.

Tämä näkyy ensimmäisessä esimerkissä.

#### Esimerkki 1

1. Avaa nimikkeet 80003 ja 80004 ja määritä **seurantakäytännöksi**  *Vain* seuranta. Jätä muut kentät oletuksena.
2. Avaa nimikepäiväkirja ja lisää näiden nimikkeiden varastomääräksi 10 sijaintia PUNAINEN vastaan ja kirjaa päiväkirjarivit.
3. Luo siirtotilaus sijainnista PUNAINEN SININEN näille kahdelle nimikkeelle: Nimikkeelle 80003 siirtotilausrivillä 10000 ja Nimikkeelle 80004 toisella rivillä 20000, molemmille 10 yksikölle.
4. Kirjaa vain siirtotilauksen toimitusosa ilman fyysisen varastoinnin toimintoja.
Kirjattu siirtotoimitus näkyy seuraavassa kuvassa.
Taulukon 337 tilatiedot näkyvät seuraavassa kuvassa.
5. Vertaa kirjatun siirtotoimituksen tuloksia taulukon 337 tapahtumiin.

Seuraavassa taulukossa kuvataan, mitä tietyissä kentissä tehdään varaustapahtumaa 40 vastaan.

|Kenttä|Kuvaus|  
|---------------------------------|---------------------------------------|  
|**Varauksen tila**|Ylijäämä nimikkeeksi 80003 määritetään tilausseurannan avulla, mutta kysyntää ei ole.|  
|**Sijaintikoodi**|Kohteeseen-koodin sijainti SININEN.|  
|**Lähdetyyppi**|Siirtorivi-taulukko 5741.|  
|**Lähdetunnus**|Asiakirjan nro siirtotilauksesta 1011.|
|**Lähde viitenro**|Rivinro yhteensä 20000 + Rivinro 10000 vastaan Nimike 80003 = 30000.|

Seuraavien Varaustapahtuma 43:a vastaan olevien kenttien kuvaus on seuraavanlainen.

|Kenttä|Kuvaus|  
|---------------------------------|---------------------------------------|  
|**Varauksen tila**|Ylijäämä nimikkeeksi 80003 määritetään tilausseurannan avulla, mutta kysyntää ei ole.|  
|**Sijaintikoodi**|Kuljetuksessa-sijainnin OMA LOki on sijainti, jossa nimike on.|  
|**Lähdetyyppi**|Nimiketapahtuma-taulukko 32.|  
|**Lähde viitenro**|Avoin nimiketapahtuma numero 322.|

#### Esimerkki 2

Seuraava esimerkki kuvaa, mitä tapahtuu, kun komponentti siirretään sijaintien välillä, mutta samaan aikaan sitä seurataan kysyntätarpeen ja saatavilla olevan tarjonnan välillä. Komponentit siirretään sijainnista PUNAINEN sininen, joka käytetään vapautetun tuotantotilauksen kanssa. Komponentti käyttää Tilauksen seurantaa, Tilauksen suunnittelua ja Nimikeseurantaa.

Tässä esimerkissä korostetaan taulukossa 337 havaittua työnkulkua suhteessa Varaustila-, Sijaintikoodi **-,** Lähdetyyppi- **,** **Lähdetunnus-**, **Lähdeviitteen nro**- ja Sidonta-tyyppiin **·**. **·**

1.  **Määritä Tuotannon asetukset -** sivulla Komponentit sijainnissa **-kentän** arvoksi PUNAINEN.
2. Luo uusi nimikekomponentti. Määritä seuraavat kentät:
  - **Perusmittayksikkö**: PCS
  - Mahdolliset oletuskirjausryhmät
  - **Täydennysjärjestelmä**: Osto
  - **Tuotantotapa**: Varasto-ohjattava
  - **Tilauksen seurantatapa**: Vain seuranta
  - **Nimikkeen seurantakoodi**: LOTALL
3. Kun käytät nimikepäiväkirjaa, suurenna nimikkeen komponentin varaston 100 yksikköä punainen -sijaintia vastaan. Määritä seuraavat eränumerot:
  - Eränumero Erä A, Määrä 30
  - Eränumero Erä B, Määrä 70
4. Luo uusi tuotettu nimike. Määritä seuraavat kentät:
  - **Perusmittayksikkö**: PCS
  - Mahdolliset oletuskirjausryhmät
  - **Täydennysjärjestelmä**: Tuotanto
  - **Tuotantotapa**: Varasto-ohjattava
  - **Tilauksen seurantatapa**: Vain seuranta
5. Luo **tuotannon tuoterakenne**, jossa on 1 määrä nimikekomponenttia kohti.
6. Määritä tuotannon tuoterakenne tuotettua nimikettä vastaan.
7. Luo myyntitilaus. Määritä seuraavat kentät:
  - **Nimike**: Tuotettu
  - **Sijainti**: SININEN
  - **Määrä**: 100
8.  **Valitse myyntitilauksen Toiminnot-välilehden**  **Suunnitelma-ryhmässä** Suunnittelu **,** kun haluat luoda linkitetyn vapautetun tuotantotilauksen myyntitilausta vastaan.
9. Avaa vapautettu tuotantotilaus / komponenttitarve ja huomaa, että sijainti on asetettu PUNAISEKSI.
Syy on se, että Komponentit **sijainnissa**  **-arvo on PUNAINEN tuotannon asetuksissa**  kortti.
Tuotettu nimike saa tuotoksen sijaintia SININEN vastaan.

Taulukon 337 tilatiedot näkyvät seuraavassa kuvassa.

##### Varaustapahtumat, joissa on numerot 55 ja 56

Erän A ja B komponenttitarpeen osalta luodaan tilauksen seurantalinkkejä taulukon 5407 Tuotantotilauksen komponentti kysynnästä taulukon 32 Nimiketapahtuma tarjontaan. Varauksen **tila -** kentässä on kaikkien neljän merkinnän seuranta, joka osoittaa, että nämä dynaamiset tilauksen seurantalinkit tarjonta ja kysyntä välillä.

Taulukon 5407 Tuotantotilauksen komponentti kysyntä on linkitetty vapautetun tuotantotilauksen 101006 lähdetunnukseen. Taulukon 32 Nimiketapahtuma tarjonta on linkitetty Lähdeviitteen nro -kenttään. Ovat nimiketapahtuman numerot 325 ja 326, joissa yksiköt ovat.

> [!NOTE]  
> **Eränro**-kenttä on tyhjä kysyntäriveillä, koska eränumeroita ei ole määritetty julkaistun tuotantotilauksen osariveillä.

##### Varaustapahtuma numerolla 57

Taulukon 37 Myyntirivi myyntikysynnästä luodaan tilauksen seurantalinkki tarjontaan taulukossa 5406, Tuotantotilausrivi. Varauksen **tila -** kentässä on Varaus, ja **Sitova-kentässä** on Tilauskohtainen. Tämä johtuu siitä, että vapautettu tuotantotilaus luotiin erityisesti myyntitilausta varten, ja se tulee säilyttää linkitettynä toisin kuin tilauksen seurantalinkit, joiden seurannan varaustila on Seuranta. Linkit luodaan ja muutetaan dynaamisesti.

> [!NOTE]  
> Sidonta-kentässä **voi** olla *tilauskohtainen* myös silloin, kun uusintatilaustavana käytetään tilausohjattua tilausta ja/tai tilausta.

10. Tässä esimerkkitilanteessa komponentin 100 yksikköä siirretään PUNAINEN-sijainnista SININEN-sijaintiin siirtotilausta käyttämällä.

Valitse toimitukselle Erä A ja Erä B.

Kirjaa avoin kokonaismäärä vain toimitetuksi.

> [!NOTE]  
> Komponentteja voi kuluttaa sijainnissa PUNAINEN, mutta esimerkiksi varaustapahtumien virtojen havainnollistamiseksi yksiköt siirretään manuaalisesti SININEN-sijaintiin.

Taulukon 337 tilatiedot näkyvät seuraavassa kuvassa.

##### Varaustapahtumat, joissa on numerot 55 ja 56

Taulukon 5407 kysyntää kuvaavan komponentin kahden erän tilauksen seurantatapahtumat muutetaan seurannan varaustilasta Ylijäämäksi. Syy on se, että siirtotilauksen lähetykseen on käytetty tarjontoja, joihin ne oli linkitetty ennen, taulukossa 32. Aito ylijäämä, kuten tässä tapauksessa, kuvastaa ylimääräistä tarjontaa tai kysyntää, jota ei seurata. Se on osoitus epätasapainosta tilausverkossa, joka luo suunnittelujärjestelmän toimenpideviestin, ellei sitä ratkaista dynaamisesti.

##### Varaustapahtuman numerot 59-63

Koska komponentin kaksi erää on kirjattu siirtotilaukseen toimitetuiksi, mutta ei vastaanotetuiksi, kaikki asiaan liittyvät positiivisen tilauksen seurantatapahtumat ovat varaustyyppiä Ylijäämä, mikä osoittaa, että niitä ei ole kohdistettu mihinkään kysyntään. Yksi tapahtuma liittyy jokaisen eränumeron osalta taulukkoon 5741, Siirtorivi, ja yksi tapahtuma liittyy nimiketapahtumaan kuljetuksessa-sijainnissa, jossa nimikkeet ovat nyt olemassa.

Taulukko 5741, **Siirtorivi**, on lähdetyyppi. **Lähdetunnus** on Siirtotilausasiakirjan numero 1012 ja **Lähde viitenro.** On 20000 = 10000 + 10000, kuten esimerkissä 1. Sijainti on asetettu SININEN kohteeseen-sijaintikoodille.

Kahdella jäljellä olevalla tapahtumalla, joilla **on varauksen tilan** ylijäämä, on taulukko 32, **Nimiketapahtuma**, Lähdetyyppi- ja **Lähdeviitteen nro -kentässä.** 328 ja 330, mukaan lukien niiden eränumerot, jotka tällä hetkellä sijaitsevat Kuljetuksessa-sijainnissa OUT LOG.

11. Kirjaa avoin siirtotilaus vastaanotetuksi.

Taulukon 337 tilatiedot näkyvät seuraavassa kuvassa.

Tilauksen seurantatapahtumat muistuttavat nyt skenaarion ensimmäistä pistettä, ennen kuin siirtotilaus kirjattiin vain toimitetuksi, paitsi että komponentin tapahtumilla on nyt varaustila Ylijäämä Seurannan sijaan. Tämä johtuu siitä, että komponenttitarve on edelleen PUNAINEN-sijainnissa, mikä kuvastaa sitä, että **tuotantotilauksen komponenttirivin Sijaintikoodi-kentässä** on PUNAINEN niin kuin Komponentit **sijainnissa** -asetuskentässä on määritetty.

Tähän kysyntään aiemmin kohdistettu tarjonta oli siirretty SININEN-sijaintiin, eikä sitä voi nyt seurata kokonaan, ellei tuotantotilausrivin komponenttitarvetta muuteta SININEN-sijainniksi. Tämä tallennetaan kahteen viimeiseen varaustapahtumaan, joissa eränumerot on täytetty, **Lähdetyyppi-kentän** arvo on Taulukko 32 ja **Lähdeviitteen nro.** Kenttää ovat Nimiketapahtumat 333 ja 334.

12. Muuta vapautetun tuotantotilauksen komponenttiluettelon sijainnin komponentin osalta SININEN-tilaksi.

12.  **Avaa kulutuspäiväkirja** ja suorita **Laske kulutus -** eräajo.
Määritä erä A määrä 30 ja erä B määrä 70.

Sulje Nimikkeen seuranta -lomake.

Taulukon 337 tilatiedot näkyvät seuraavassa kuvassa.

##### Varaustapahtumat, joissa on numerot 68 ja 69

Koska komponenttitarve on muutettu SININEN-sijainniksi ja tarjonta on saatavilla nimiketapahtumina SININEN-sijainnissa, näiden kahden eränumeron kaikkia tilauksen seurantatapahtumia seurataan nyt täysin, mikä näkyy seurannan varaustilana. Eränumeroita ei nouteta Eränro-kenttään **.** -kenttä suhteessa vapautetun tuotantotilauksen komponentin kysyntään 5406, **Tuot.til. rivi** -taulukkoon, koska emme määrittäneet eränumeroita vapautetun tuotantotilauksen komponentille.

##### Varaustapahtumat, joissa on numerot 70 ja 71

Tapahtumat, joiden varaustila on Prospekti, luodaan taulukossa 337. Syy on se, että molemmat eränumerot määritetään kulutuspäiväkirjan komponenttia vastaan, mutta päiväkirjaa ei ole kirjattu.

Varaustapahtuma-taulukon **tilausten seurantatapahtumien** luomisen, muokkauksen ja poistamisen tapa on nyt nyt valmis, kun useita ominaisuuksia käytetään yhdessä siirtotilausten kanssa.

### Laskettu suunnittelu

Kun käytetään suunnittelutoimintoja eli hankintalistaa, suunnittelutyökirjaa **tai** tilauksen suunnittelua **, Varaustapahtuma-taulukon** 337 varaustapahtumia **saatetaan muokata tai lisätä logiikan** suunnitteluehdotuksen mukaisesti. **·**  Microsoft Dynamics NAV Esimerkki 3 käyttää **tuotetulle nimikkeelle uusintatilaustapaa** tilaus, jossa **on tuotantotavan** tilaus. Komponentti käyttää **uusintatilaustapaa** Kiinteä uusintatilausmäärä.

#### Esimerkki 3

1.  **Tuotannon asetukset**  kortti,Komponentti **sijainnissa** on PUNAINEN aiemmasta esimerkistä.
2. Luo uusi pääelementti Nimike 70061. Määritä seuraavat kentät:
  - **Perusmittayksikkö**: PCS
  - Mahdolliset oletuskirjausryhmät
  - **Täydennysjärjestelmä**: Tuotantotilaus
  - **Tuotantotapa**: Tilausohjattava
  - **Uusintatilaustapa**: Tilaus
  - **Varaa-menettely**: Valinnainen
  - **Tilauksen seuranta**: Ei mitään
3. Luo uusi komponenttinimike 70062. Määritä seuraavat kentät:
  - **Perusmittayksikkö**: PCS
  - Mahdolliset oletuskirjausryhmät
  - **Täydennysjärjestelmä**: Osto
  - **Uusintatilaustapa**: Kiinteä uusintatilausmäärä
  - **Varaa-menettely**: Valinnainen
  - **Tilauksen seurantatapa**: Ei mitään
  - **Varmuusvaraston määrä**: 10
  - **Uusintatilauspiste**: 25
  - **Uusintatilausmäärä**: 50
4. Luo uusi tuotannon tuoterakenne ja määritä Komponenttinimike 70062 niin, että määrä on yksi.
Määritä tuotannon tuoterakenne pääelementti nimikkeelle 70061.
5. Luo myyntitilaus. Määritä seuraavat kentät:
  - **Nimike**: Kiinteä uusintatilausmäärä
  - **Sijainti**: PUNAINEN
  - **Määrä**: 40
  - **Lähetyksen pvm**: 15.2.2014
6.  **Avaa Suunnittelutyökirjat-sivu** ja suorita **Laske uudelleensuunnittelu -** eräajo.
  - **Tuotanto-ohjelmassa/tarvelaskennassa**: käytössä
  - **Aloituspvm**: 23.01.2014
  - **Lopetuspvm**: 01.03.2014
  - Suodata nimikkeille 70061 ja 70062
  - Ei ennustetta

Seuraavat suunnitteluehdotukset annetaan.

Ensimmäinen suunnitteluehdotus on luoda uusi suunniteltu tuotantotilaus, joka vastaa myyntitilauksen avointa kysyntää 40 pääelementti nimikkeen 70061 määrällä 40. Tarkista tilausten seuranta ja Microsoft Dynamics NAV näytä avoin myyntitilaus. Tilauksen seuranta on aktivoitu, koska suunnittelumoduuli luo sen.

Toinen rivi on varaston tuominen Uusintatilauspisteen yläpuolelle (25). Uusintatilausmäärä (50) huomioon ottaen suunnittelulogiikka ehdottaa siis 50 yksikön määrää. Kolmas rivi on varaston tuominen varmuusvarastotasolle (10).

Neljäs rivi on varaston täydentäminen myyntitilauksen toimituksen yhteydessä. Tuolloin Varasto on noin 20 alle Uusintatilauspisteen. Tämän seurauksena suunnittelumoduuli ehdottaa 50 lisäkomponentin ostamista uusintatilausmäärä huomioon ottaen. Tämä on Ei-seurattu määrä, joten Varaustapahtuma-taulukossa *337* tämä merkitään varaustilalla Ylijäämä.

Taulukon 337 tilatiedot näkyvät seuraavassa kuvassa.

Varauksen **tila -** kenttä on Varaus ja Tilauskohtainen sidonta luodaan. Syy on se, että nimikkeen tuotantotapa on Tilausohjattava ja uusintatilaustapa on Tilaus. Jos jommankumman tilaksi on määritetty Tilaus, varauksen tilaksi määritetään Seurannan sijaan Varaus ja Sidonta tilauksesta.

40 yksikön kysyntä lähdetunnusta **vastaan** on myyntitilauksen numero 1005, ja Lähdetyyppi on *Myyntirivi-taulukko* 37. Varaustapahtuma on linjassa suunnitteluehdotuksen Lähde viitenro kanssa. 10000, Lähdetunnus on SUUNNITTELU JA Lähdetyyppi hankintarivi-taulukko *246*. Myyntitilauksen kysynnän ja suunnittelumoduulin ehdottaman tarjonnan välillä on siis tasapaino.

##### Varaustapahtuman numerot 73 ja 74

Laske suunnitelma -eräajon avulla luodaan seuraavat neljä merkintää, joiden varaustilana on Seuranta. Tämä johtuu komponentin uusintatilaustavan Kiinteä uusintatilausmäärä asetuksesta. Komponentille 70062 tarvittavaa tarjontaa täydennetään annetuilla suunnitteluehdotuksilla, Lähdeviitteen nro. 20000 ja 30000, joiden Lähdetunnus on asetettu SUUNNITTELU- ja Lähdetyyppi hankintarivi *-taulukosta* 246. Komponenttitarve luodaan täyttämään kysyntä suhteessa pääelementti Nimikkeeseen 70061 kokonaismäärän (perus) 40 osalta. Kysynnän seurauksena Lähde tuot.til. rivi **-kentän arvo** on 1 0000, ja lähdetyyppi on *Komponenttitarve-taulukko* 99000829.

Varauksen tila ei ole Ylijäämä, koska pääelementti nimikkeen 70061 kysynnän ja Komponenttinimikkeen 70062 tarjonnan välillä on tilauksen seuranta.

##### Varaustapahtuman numerot 75 ja 76

Kahdella viimeisellä tapahtumalla on varaustila Ylijäämä, koska ne ovat Ei-seurattuja määriä, jotka on luotu suunnittelutyökirjassa uusintatilausparametreihin Uusintatilauspiste ja Uusintatilausmäärä.

## Katso myös  
[Rakennetiedot: Nimikeseurannan rakenne](design-details-item-tracking-design.md)  
[Rakennetiedot: Kysynnän ja tarjonnan tasaaminen](design-details-balancing-demand-and-supply.md)  
[Rakennetiedot: varaus, tilauksen seuranta ja toimenpiteiden viestitys](design-details-reservation-order-tracking-and-action-messaging.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]