---
author: brentholtorf
ms.topic: include
ms.date: 04/23/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Lisää fyysisen varastoinnin tehokkuutta tarkoilla reaaliaikatuilla tiedoilla tekijöistä, jotka voivat vaikuttaa saatavilla oleviin määriin. Esimerkki: 

* Varastotasot
* Sijainnit
* Prosessoinnin vaiheet
* Karanteenissa olevat nimikkeet
* Varaukset

Tietoja nimikkeen saatavuudesta voi käyttää seuraavista lähdeasiakirjoista:

* Myyntitilaukset
* Tuotantotilaukset
* Kokoonpanotilaus
* Projektit

Tiedot huomioivat myös muut saatavuuteen vaikuttavat tekijät. Esimerkiksi erityisvarastopaikat, lukitut varastopaikat ja nimikkeet, jotka eivät ole poimittavissa. Nimikkeet voivat olla esimerkiksi varattuja tai odottavia hyllytys- tai toimitustoimintoja. **Poiminnan yhteenveto** -sivulla voit tarkastella nimikkeitä, joita [!INCLUDE [prod_short](prod_short.md)] ei sisällyttänyt poiminta-asiakirjoihin, ja tehdä tarvittavat toimenpiteet.

> [!NOTE]
> Tämä ominaisuus edellyttää, että **Ohjattu hyllytys ja poiminta** ottaa käyttöön poimintaprosessissa käytettävien sijaintien osalta.

### Esiversioiden määrittäminen

Kun haluat lisätietoja poimittavista ja ei-poimittavista kohteista, ota käyttöön **Näytä yhteenveto (ohjattu hyllytys ja poiminta)** -valinta **F. var.-lähde - luo asiakirja**- tai **F. var.toimitus - luo poiminta** -pyyntösivuilla.

### Määritä poimittavissa oleva määrä

**Käsiteltävä määrä (perus)** -kenttä näyttää **Luo fyysisen varaston poimintayhteenveto** -sivun riveillä, mitkä nimikkeet ja kuinka monta nimikettä [!INCLUDE [prod_short](prod_short.md)] on yrittänyt poimia. **Yhteenveto**-tietoruudussa on lisätietoja.

Yksinkertaisia tutkimuksia varten **Poimittava määrä** antaa tarpeeksi tietoa. Tässä kentässä näkyy, kuinka monta nimikettä on saatavilla. Jos poimittava määrä on odotettua pienempi, tutustu varastopaikan sisältöön.

**Poimittava määrä** on enimmäismäärä, jonka [!INCLUDE [prod_short](prod_short.md)] voi harkita poimivansa. Tämä määrä koostuu poimittavissa olevien varastopaikkojen nimikkeistä. Määrään ei sisälly määriä, jotka ovat suljetuissa tai erityisvarastopaikoissa, tai nimikkeitä, jotka poimitaan fyysisen varastoinnin poiminta-asiakirjoista. Jos poimittava nimike edellyttää nimikeseurantaa, poimittavissa olevaan määrään ei sisällytetä suljettuja erä- tai sarjanumeroita.

Jos poimittava määrä eroaa poimittavien varastopaikkojen määrästä, siitä voi tulla ongelma. Etsi varastopaikan sisällöstä suljettuja varastopaikkoja tai määriä aktiivisista asiakirjoista.

**Määrä fyysisessä varastossa** -kentässä on kokonaismäärä, jonka löydät fyysisestä varastosta, jos teet inventoinnin. Tässä kentässä voidaan porautua fyysisen varastoinnin tapahtumiin. Jos kentässä on määrä, joka on pienempi kuin **Määrä poimittavissa olevissa varastipaikoissa** -kentän määrä, fyysisen varaston ja varaston määrien välillä on virheellinen kohdistus. Käytä tällöin **Nimikepäiväkirja**-sivulla **Laske fyysisen varaston muutos** -toimintoa ja luo sitten fyysisen varaston poiminta uudelleen.

Seuraava kuva kuvaa poiminnassa huomioon otettavan enimmäismäärän.

:::image type="content" source="../media/pickable-qty.png" alt-text="Poiminnassa huomioon otettava enimmäismäärä.":::

**Selite**

|Kirjain  |Kuvaus  |
|---------|---------|
|J     |Varastopaikat, joiden tyyppi on Poiminta         |
|P     |Varastopaikat, joiden tyyppi on Poiminta, on merkitty erityisvarastopaikoiksi        |
|L     |Varastopaikat, joiden tyyppi on Poiminta, aktiivisissa asiakirjoissa (kuten toisessa poiminnassa)       |
|T     |Varastopaikat, joiden tyyppi on Poiminta ja joiden seuranta on estetty         |
|B     |Varastopaikat, joiden tyyppi on Poiminta ja joiden lähtevä siirto on estetty         |
|O     |Muut varastopaikat         |

### Varaukset

Jos poimittavalle nimikkeelle on varauksia, laskenta jatkuu. Ajatuksena on, että varatulla kysynnällä on korkeampi prioriteetti kuin varaamattomalla kysynnällä, eli ei-varatun kysynnän poiminta ei saa estää poimimista varatulle kysynnälle myöhemmin.

Voit tarkistaa, että määrä kattaa kysynnän, vertaamalla **Poimittava määrä** -tietoruudun arvoa **Yhteenveto**-tietoruudussa **Käsiteltävä määrä (perus)** -kentän arvoon riveillä.

**Varattu määrä yhteensä fyysisessä varastossa** -kentässä on varausten kokonaismäärä. Varatut määrät, jotka on jo poimittu ja jotka ovat valmiita toimituksiin, käyttöön tai kulutukseen, eivät vaikuta saatavuuteen. **Varattu määrä poiminta-/toimituslokeroissa** -kentässä on tämä määrä.

**Saatavilla oleva määrä ilman toimituslokeroa** -kentässä on saatavilla oleva määrä, ei määriä, joiden osalta seuraavat ovat totta:

* Ne on jo poimittu toimituksia varten.
* Ne ovat suljettuja nimike-eriä tai sarjanumeroita.
* Ne ovat suljetuissa varastopaikoissa.
* Ne ovat erityisvarastopaikoissa.

Nämä määrät voivat olla saatavilla, mutta niitä ei ehkä vielä voi poimia. Ne voivat olla vielä vastaanotto-, varastointi- tai laadunvarmistusalueilla. Voit siirtää ne poiminta-alueelle käsittelemällä hyllytyksen tai varaston siirron työkirjaa.

**Saatavilla oleva määrä ilman toimituslokeroa** ja varattu määrä fyysisessä varastossa on poimittavissa oleva määrä ilman, että se vaikuttaa varattuun varastoon.

Seuraava kuva havainnollistaa käytettävissä olevan määrän jakamista varatulle määrälle.

:::image type="content" source="../media/Warehouse_Reservation_Pick.png" alt-text="Enimmäismäärä, joka otetaan huomioon poimintaa varten varauksen yhteydessä.":::

**Selite**

|Kirjain  |Kuvaus  |
|---------|---------|
|J     |Poimittava määrä         |
|TR    |Varattu määrä yhteensä fyysisessä varastossa.         |
|RS    |Varatut määrät, jotka on jo poimittu ja jotka ovat valmiita toimituksiin, käyttöön tai kulutukseen       |
|L     |Saatavilla oleva määrä ilman toimituslokeroa         |
|B     |Erityisten tai suljettujen varastopaikkojen, suljettujen nimike-erien tai sarjanumeroiden määrä         |

Vaikka fyysisessä varastossa on tarpeeksi saatavilla olevaa määrää poiminnan täyttämiseksi kokonaan, se johtaa siihen, että varattu kokonaismäärä on kohdistettu erityisten tai suljettujen varastopaikkojen määriin, mikä estää poiminnan tämän kysynnän osalta. Koska varatulla kysynnällä on korkeampi prioriteetti, [!INCLUDE [prod_short](prod_short.md)] vähentää poimittavaa määrää negatiivisten vaikutusten, kuten poimintakyvyttömyyden, estämiseksi varattuun kysyntään.

### Muut tiedot

Jos nimikkeet vaativat nimikeseurantaa, voit löytää määrän myös suljettujen erien tai sarjanumeroiden osalta, mikä aiheuttaa seuraavat vähennykset:

* Poimittava määrä
* Saatavilla oleva määrä, pois lukien toimituslokero
* Varattu määrä fyysisessä varastossa 

Jos poimit saman nimikkeen usealle lähdeasiakirjalle tai -riville, mikä on tilanne myös sarjanumeroita poimittaessa, muiden rivien poimintojen tiedot näkyvät myös siksi, että ne vähentävät poimittavaa määrää.
