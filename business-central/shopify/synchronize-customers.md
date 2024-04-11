---
title: Asiakkaiden synkronointi
description: Asiakkaiden tuominen tai vieminen Shopifyista tai Shopifyihin
ms.date: 03/25/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
---

# <a name="synchronize-customers-and-companies"></a>Asiakkaiden ja yritysten synkronointi

Kun tuot tilauksen Shopifysta, asiakkaan tietojen hankkiminen on olennaista asiakirjan käsittelemisessä [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa. On olemassa kaksi päävaihtoehtoa ja useita yhdistelmiä:

* Käytä erikoisasiakasta kaikissa tilauksissa.
* Tuo asiakastiedot Shopify-tiedoista. Tämä vaihtoehto on käytettävissä myös silloin, kun asiakkaita viedään Shopifyhyn [!INCLUDE[prod_short](../includes/prod_short.md)]ista.

Shopify mahdollistaa yritystenvälisen ja kuluttajakaupan liiketoiminnan suorittamisen samassa paikassa Shopifyn tehokkaan ja vaivattoman keskitetyn ympäristön avulla. Shopify-yhdistin toimii myös erilaisissa sähköisissä kaupankäynneissä.

Shopifyssa on kaksi yksikköä, asiakas ja yritys, kun taas [!INCLUDE[prod_short](../includes/prod_short.md)]issa on vain asiakasyksikkö, mikä vaikuttaa synkronointiin.

Kuluttajamyynnissä ostaja luodaan Shopifyssa asiakkaana. Asiakas tuodaan sitten [!INCLUDE[prod_short](../includes/prod_short.md)]iin Shopify-asiakkaana ja linkitetään tai muunnetaan asiakkaaksi.

Jos kyseessä on yritystenvälinen toiminta, ostaja luodaan Shopifyssa yritykseen linkitettynä asiakkaana. Asiakas tuodaan [!INCLUDE[prod_short](../includes/prod_short.md)]iin Shopify-asiakkaana ja yritys tuodaan [!INCLUDE[prod_short](../includes/prod_short.md)]iin Shopify-yrityksenä joka linkitetään asiakkaaksi tai muunnetaan asiakkaaksi.

Asiakkaan vienti [!INCLUDE[prod_short](../includes/prod_short.md)]ista Shopifyhyn vaihtelee hieman sen mukaan, mitä halutaan tehdä:

* Asiakkaan vienti kuluttajakaupassa Shopify-asiakkaana.
* Asiakkaan vienti yritys- ja asiakasparina yritystenvälisessä työnkulussa.

## <a name="important-settings-when-importing-dtc-customers-from-shopify"></a>Tärkeät asetukset tuotaessa kuluttajakaupan asiakkaita Shopifysta

Joko tuot asiakkaita Shopifysta joukkona tai yhdessä tilausten tuonnin kanssa käyttämällä seuraavia asetuksia, jotka mahdollistavat prosessin hallinnan:

|Kenttä|Kuvaus|
|------|-----------|
|**Asiakkaan tuonti Shopifysta**|Valitse **Kaikki asiakkaat**, jos aiot tuoda asiakkaita Shopifysta joukkona, joko manuaalisesti käyttämällä **Synkronoi asiakkaat** -toimintoa tai työjonon kautta toistuvia päivityksiä varten. Valinnasta huolimatta asiakastiedot tuodaan aina yhdessä tilauksen kanssa. Näiden tietojen käyttäminen riippuu kuitenkin **Shopifyn asiakasmalleista** ja asetuksista **asiakkaan yhdistämismäärityksen tyyppi** -kentässä.|
|**Asiakkaan yhdistämismäärityksen tyyppi**|Määritä, kuinka haluat yhdistimen suorittavan yhdistämisen.</br></br>- **Sähköpostitse/puhelimitse**, jos haluat yhdistimen käyttävän sähköpostitiliä ja puhelintietoja yhdistämään tuodun Shopify-asiakkaan Business Centralin asiakkaaseen.</br></br>- **Laskutusasiakkaan tiedot** jos halutaan, että yhdistin käyttää laskun vastaanottajan osoitetta yhdistämään tuodun Shopify-asiakkaan aiemmin luotuun Business Centralin asiakkaaseen.</br></br>Valitse **Ota aina oletusasiakas**, jos haluat, että järjestelmä käyttää asiakasta **oletusasiakasnro** -kentässä. |
|**Shopify voi päivittää asiakkaat**| Valitse tämä kenttä, jos haluat, että yhdistin päivittää löydetyt asiakkaat, kun joko **asiakkaan yhdistämismäärityksen tyyppi** -kentässä on valittuna **sähköpostilla/puhelimella** tai **Laskutusasiakkaan tiedoilla**.|
|**Luo tuntemattomat asiakkaat automaattisesti**| Valitse tämä kenttä, jos haluat, että yhdistin luo puutuvat asiakkaat, kun **asiakkaan yhdistämismäärityksen tyyppi** -kentässä on valittuna **sähköpostilla/puhelimella** tai **Laskutusasiakkaan tiedoilla**. Uusi asiakas luodaan käyttämällä tuotuja tietoja ja **asiakasmallin koodia**, joka on määritetty **Shopify-ostoskortti**- tai **Shopify-asiakasmalli**-sivuilla. Huomaa, että Shopify-asiakkaalla täytyy olla vähintään 1 osoite. Shopify-myyntipisteen kautta luoduista tilauksista puuttuvat usein osoitetiedot. Jos tämä asetus ei ole käytössä, asiakas on luotava manuaalisesti ja linkitettävä Shopify-asiakkaaseen.|
|**Asiakas-/yritysmallin koodi**|Tätä kenttää käytetään yhdessä **Tuntemattomien asiakkaiden luominen automaattisesti** -toiminnon kanssa.</br></br> Valitse oletusmalli, jota käytetään automaattisesti luoduille asiakkaille. Varmista, että valitussa mallissa on pakolliset kentät, kuten **Yleinen liiketoiminnan kirjausryhmä**, **Asiakkaan kirjausryhmä**, arvonlisävero (ALV) tai veroihin liittyvät kentät.</br></br>Voit määrittää malleja kullekin maalle tai alueelle **Shopify-asiakasmallit** -sivulla, mikä auttaa laskemaan verot oikein.</br></br>Lisätietoja kohdassa [Verojen määrittäminen](setup-taxes.md).|

### <a name="customer-template-per-countryregion"></a>Asiakasmalli maata tai aluetta kohti

Jotkin asetukset voidaan määrittää maan tai alueen tasolla tai osavaltion/provinssin tasolla. Asetukset voidaan määrittää kohdassa [Toimitus-ja toimitus](https://www.shopify.com/admin/settings/shipping) Shopifyssa.

Voit tehdä seuraavan toimen kullekin asiakkaalle **Shopify-asiakasmallin** avulla:

1. Määritä **oletusasiakasnro**, joka on etusijalla **asiakkaan tuonti Shopifysta** ja **Asiakkaan yhdistämismäärityksen tyyppi** -kentissä olevan valinnan. Sitä käytetään tuodussa myyntitilauksessa.
2. **Määritä asiakasmallin koodi**, jota käytetään puuttuvien asiakkaiden luomisessa, jos **Luo automaattisesti tuntemattomat asiakkaat** on otettu käyttöön. Jos **asiakasmallin koodi** on tyhjä, funktio käyttää **Asiakasmallin koodia**, joka on määritetty **Shopify-ostoskortissa**. Järjestelmä yrittää ensin etsiä oletusosoitteen **Maa-/aluekoodi**-mallin. Jos mallia ei löydy, se käyttää ensimmäistä osoitetta.
3. Joissakin tapauksissa maalle tai alueelle määritetty **asiakasmallin koodi** ei riitä varmistamaan oikeita verolaskelmia (esimerkiksi kun maa tai alue käyttää arvonlisäveroa). Tässä tapauksessa **Veroalueen** sisällyttäminen voi olla hyödyllinen lisäys.
4. **Veroalue**-kenttä sisältää myös **Maakoodi**- ja **Läänin nimi** -parin. Tämä pari on hyödyllinen, kun yhdistimen tarvitsee muuntaa koodi nimeksi tai päinvastoin.

> [!NOTE]  
> Maakoodit ovat ISO 3166-1 alpha-2-maakoodeja. Lisätietoja kohdassa [maakoodi](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="important-settings-when-exporting-dtc-customers-to-shopify"></a>Tärkeät asetukset vietäessä kuluttajakaupan asiakkaita Shopifyhyn

Voit viedä olemassa olevat asiakkaat Shopifyhin joukkona. Kussakin tapauksessa luodaan asiakas ja yksi oletusosoite. Voit hallita prosessia seuraavien asetusten avulla:

|Kenttä|Kuvaus|
|------|-----------|
|**Voi päivittää Shopify-asiakkaat**| Ota vaihtoehto käyttöön, jos haluat luoda päivityksiä myöhemmin Business Central -ohjelmassa Shopifyssa oleville asiakkaille.|

Seuraavat vaatimukset koskevat asiakkaan viemistä:

* Asiakkaalla täytyy olla voimassa oleva sähköpostiosoite.
* Vietäessä asiakkaita, joiden osoitteet sisältävät maakunnan tai osavaltion, on varmistettava, että maiden tai alueiden **ISO-koodi** on täytetty.|
* Jos maa tai alue on valittu asiakaskortissa, varmista kyseinen **ISO-koodi**. Paikallisilla asiakkailla, joilla on tyhjä maa tai alue, Shopify-yhdistin käyttää **Yrityksen tiedot** -kohdassa määritettyä maata tai aluetta.
* Jos asiakkaalla on puhelinnumero, numeron täytyy olla yksilöivä, koska Shopify ei hyväksy toista asiakasta, jolla on sama puhelinnumero.
* Jos asiakkaalla on puhelinnumero, sen täytyy olla E.164-muodossa. Eri muotoja tuetaan, jos ne edustavat numeroa, joka voidaan soittaa kaikkialta maailmasta. Seuraavat muodot ovat kelvollisia:

  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

Kun asiakkaat on luotu Shopifyssa, heille voidaan lähettää suoria kutsuja ja kannustaa näin heitä aktivoimaan tilinsä.

### <a name="populate-customer-information-in-shopify"></a>Asiakastietojen täyttäminen Shopifyssa

Shopifyssa asiakkaalla on etunimi, sukunimi, sähköpostiosoite ja/tai puhelinnumero. Etunimen ja sukunimen voi syöttää [!INCLUDE[prod_short](../includes/prod_short.md)]in asiakaskortista.

|Prioriteetti|Asiakaskortin kenttä|Kuvaus|
|------|------|-----------|
|1|**Yhteyshenkilön nimi**|Korkein prioriteetti, jos **Yhteyshenkilön nimi** -kenttä on täytetty ja **Shopify-kauppakortin** **Yhteystiedot**-kenttä sisältää joko *Etunimi ja sukunimi*- tai *Sukunimi ja etunimi* -vaihtoehdot, jotka määrittävät kuinka arvot jaetaan.|
|2|**Nimi 2**|Jos **Nimi 2** -kenttä on täytetty ja **Shopify-kauppakortin** **Nimi 2 -tiedot**-kenttä sisältää joko *Etunimi ja sukunimi*- tai *Sukunimi ja etunimi* -vaihtoehdot, jotka määrittävät kuinka arvot jaetaan.|
|3|**Nimi**|Alin prioriteetti, jos **Yhteyshenkilön nimi** -kenttä on täytetty ja **Shopify-kauppakortin** **Nimitiedot**-kenttä sisältää joko *Etunimi ja sukunimi*- tai *Sukunimi ja etunimi* -vaihtoehdot, jotka määrittävät kuinka arvot jaetaan.|

Asiakkaalla on Shopifyssa myös oletusosoite. Osoite voi myös sisältää yrityksen ja osoitteen etunimen, sukunimen, sähköpostiosoitteen ja/tai puhelinnumeron lisäksi. Voit täyttää **Yritys**-kentän [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelman asiakaskortin tietojen perusteella.

|Prioriteetti|Asiakaskortin kenttä|Kuvaus|
|------|------|-----------|
|1|**Nimi**|Korkein prioriteetti, jos **Nimilähde**-kentässä **Shopify-ostoskortissa** on *yrityksen nimi*.|
|2|**Nimi 2**|Alin prioriteetti, jos **Nimi 2 lähde** -kentässä **Shopify-ostoskortissa** on *yrityksen nimi*.|

Valitse osoitteissa, joissa käytetään lääniä tai provinssia, valitsemalla **Koodi** tai **Nimi** -ostoskortin **Läänin lähde**-kentässä **Shopify-ostoskortissa**. Tämä koodi määrittää **Lääni**-kentän [!INCLUDE[prod_short](../includes/prod_short.md)]iin tallennettavien tietojen tyypin. Muista alustaa asiakasmalleja maittain tai alueittain niin, että läänin koodi/nimi-kartoitus on valmis. 

## <a name="export-dtc-customers-to-shopify"></a>Kuluttajakaupan asiakkaiden vienti Shopifyhyn

### <a name="initial-sync-of-customers-from-business-central-to-shopify"></a>Asiakkaiden ensimmäinen synkronointi Business Centralista Shopifyhyn

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-asiakkaat** ja valitse vastaava linkki.
2. Valitse **Lisää asiakas** -toiminto.
3. Syötä koodi **Ostoskoodi**-kenttään. Jos **Shopify-asiakkaat**-ikkuna avataan **Ostoskortti**-sivulla, ostoskoodi täytetään automaattisesti.
4. Määritä asiakkaan suodattimet tarpeen mukaan. Suodatusperusteena voidaan käyttää esimerkiksi maa- tai aluekoodia.
5. Valitse **OK**.

Tuloksena olevat asiakkaat osoitteineen luodaan Shopifyssa automaattisesti.

> [!NOTE]  
> Asiakkaiden ensimmäinen synkronointi [!INCLUDE[prod_short](../includes/prod_short.md)]ista Shopifyhyn ei ota huomioon **Voi päivittää Shopify -asiakkaita** -asetuksia.

### <a name="sync-customers"></a>Synkronoi asiakkaat

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse määrättykauppa, jolle haluat synkronoida asiakkaat.
3. Valitse **Synkronoi asiakkaat** -toiminto.

Vaihtoehtoisesti voit käyttää **Käynnistä asiakkaan synkronointi** - toimintoa **Shopify-asiakkaat**-ikkunassa tai hae **Synkronoi asiakkaat** -eräajoa.

Voit ajoittaa tehtävän suoritettavaksi automaattisesti. Lisätietoja on kohdassa [Toistuvien tehtävien ajoittaminen](background.md#to-schedule-recurring-tasks).

## <a name="b2b-companies"></a>Yritystenväliset yritykset

Jos yritystenvälistä kauppaa käytetään Shopifyssa, asiakkaiden lisäksi voidaan luoda myös yrityksiä. Yksi tai usea yksittäinen asiakas voidaan linkittää yritykseen. Lisäksi voidaan määrittää maksuehdot, sijainnit ja luettelot.

## <a name="important-settings-when-importing-b2b-companies-from-shopify"></a>Tärkeät asetukset tuotaessa yritystenvälisiä yrityksiä Shopifysta

Riippumatta siitä, tuodaanko yritykset Shopifysta joukkotuontina tai tilauksia tuotaessa, prosessi hallitaan seuraavan taulukon asetusten avulla.

|Kenttä|Kuvaus|
|------|-----------|
|**Yrityksen tuonti Shopifysta**|Valitse **Kaikki yritykset**, jos aiot tuoda asiakkaita Shopifysta joukkona, joko manuaalisesti käyttämällä **Synkronoi yritykset** -toimintoa tai toistuvien päivitysten työjonon kautta. Valinnasta riippumatta asiakastiedot tuodaan aina yhdessä tilauksen kanssa. Näiden tietojen käyttäminen määräytyy kuitenkin **Shopifyn yritysmallien** ja **Yrityksen yhdistämismäärityksen tyyppi** -kentän asetusten mukaan.|
|**Yrityksen yhdistämismäärityksen tyyppi**|Määritä, miten yhdistimen halutaan suorittavan yhdistämisen.</br></br>- **Sähköpostitse/puhelimitse** jos halutaan, että yhdistin yhdistää tuodut Shopify-yritykset Business Centralin aiemmin luotuun asiakkaaseen pääyhteyshenkilön sähköpostin ja puhelinnumeron avulla.</br></br>- Valitse **Käytä aina oletusyritystä**, jos halutaan järjestelmän käyttävän yritystä **Yrityksen oletusnro** -kentässä. |
|**Shopify voi päivittää yrityksen**| Valitse tämä kenttä, jos halutaan, että yhdistin päivittää löydetyt asiakkaat, kun **Sähköpostitse/puhelimitse**-vaihtoehto valitaan **Yrityksen yhdistämismäärityksen tyyppi** -kentässä.|
|**Luo tuntemattomat yritykset automaattisesti**| Valitse tämä kenttä, jos halutaan, että yhdistin luo uudet asiakkaat, kun **Sähköpostitse/puhelimitse**-vaihtoehto valitaan **Yrityksen yhdistämismäärityksen tyyppi** -kentässä. Uusi asiakas luodaan käyttämällä tuotuja tietoja ja**Shopify-ostoskortti**- ja **Shopify-asiakasmalli**-sivuilla määritettyä **Asiakas- tai yritysmallin koodia**.|
|**Asiakas-/yritysmallin koodi**|Tätä kenttää käytetään yhdessä **Luo tuntemattomat yritykset automaattisesti** -toiminnon kanssa.</br></br>- Valitse oletusmalli, jota käytetään automaattisesti luoduille asiakkaille. Varmista, että mallin pakolliset kentät, kuten **Yleinen liiketoiminnan kirjausryhmä**, **Asiakkaan kirjausryhmä**, **Arvonlisävero (ALV)**, tai muut veroihin liittyvät kentät.</br></br>- Voit määrittää malleja kullekin maalle/alueelle **Shopify-asiakasmallit** -sivulla, josta on hyötyä asianmukaisen veron laskentaan.</br></br>Lisätietoja kohdassa [Verojen määrittäminen](setup-taxes.md).|

> [!NOTE]  
> Yrityksellä on oltava pääyhteyshenkilö. Muussa tapauksessa liitin siirtyy yritykseen.
> Vain vanhin sijainti tuodaan.
> Vain pääyhteyshenkilö tuodaan.

## <a name="important-settings-when-exporting-b2b-companies-to-shopify"></a>Tärkeät asetukset tuotaessa yritystenvälisiä yrityksiä Shopifyhyn

Aiemmin luodut asiakkaat voidaan joukkoviedä Shopifyhyn yrityksenä. Kussakin tapauksessa yritys ja yksi oletussijainti luodaan samoin kuin yksi pääyhteyshenkilö. Myös luettelo voidaan luoda.

|Kenttä|Kuvaus|
|------|-----------|
|**Voi päivittää Shopify-yrityksiä**| Ota tämä vaihtoehto käyttöön, jos Business Centralista halutaan myöhemmin luoda päivityksiä Shopifyssa jo oleville asiakkaille.|
|**Oletuskontaktin käyttöoikeus**| Määritä, mitkä käyttöoikeudet on määritettävä pääyhteyshenkilölle. Valittavana on **Ei mitään**, **Vain tilaus** ja **Sijainnin hallinta**.|
|**Luo luettelo automaattisesti**| Ota tämä vaihtoehto käyttöön, jos halutaan luoda kaikki tuotteet sisältävä luettelo. Luettelo luodaan kullekin tuodulle yritykselle.|

## <a name="export-b2b-company-to-shopify"></a>Yritystenvälisen yrityksen vienti Shopifyhyn

### <a name="initial-sync-of-b2b-companies-from-business-central-to-shopify"></a>Yritystenvälisten yritysten ensimmäinen synkronointi Business Centralista Shopifyhyn

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-yritys** ja valitse liittyvä linkki.
2. Valitse **Lisää yritys** -toiminto.
3. Syötä koodi **Ostoskoodi**-kenttään. Jos **Shopify-yritys**-ikkuna avataan **Ostoskortti**-sivulla, ostoskoodi täytetään automaattisesti.
4. Määritä asiakkaan suodattimet tarpeen mukaan. Suodatusperusteena voidaan käyttää esimerkiksi maa- tai aluekoodia.
5. Valitse **OK**.

Tuloksena oleva yritys ja asiakkaat luodaan automaattisesti Shopifyssa.

> [!NOTE]  
> Yritysten ensimmäinen synkronointi [!INCLUDE[prod_short](../includes/prod_short.md)]ista Shopifyhyn ei ota huomioon **Voi päivittää Shopify-yrityksen** -asetuksia.

### <a name="sync-b2b-company"></a>Yritystenvälisen yrityksen synkronointi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse määrättykauppa, jolle haluat synkronoida asiakkaat.
3. Valitse **Synkronoi yritys** -toiminto.

Vaihtoehtoisesti voidaan käyttää **Aloita yrityksen synkronointi** -toiminto **Shopify-yritys**-sivulla tai hae **Synkronoi yritys** -eräajoa.

Tehtävä voidaan ajoittaa suoritettavaksi automaattisesti. Lisätietoja on kohdassa [Toistuvien tehtävien ajoittaminen](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
