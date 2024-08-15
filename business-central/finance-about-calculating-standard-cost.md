---
title: Tietoja standardikustannuksen laskemisesta
description: Vakiokustannusjärjestelmässä varaston yksikkökustannus määritetään kohtuullisten aiempien tai odotettujen kustannusten perusteella.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 5841
ms.author: bholtorf
ms.date: 10/10/2023
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="about-calculating-standard-cost"></a>Tietoja standardikustannuksen laskemisesta

Useat tuotantoyritykset valitsevat vakiokustannusten perustaksi arvostuksen. Tämä pätee myös yrityksiin, jotka tekevät vain kevyitä tuotantotöitä, kuten kokoonpanoa ja varustelua. Vakiokustannusjärjestelmässä varastoyksikkö määritetään kohtuullisten aiempien tai odotettujen kustannusten perusteella. Tällöin aiempien ja arvioitujen kustannusten tarkastelut muodostavat vakiokustannusten perustan. Nämä kustannukset jäädytetään, kunnes niiden muutosta koskeva päätös on tehty. Tuotteen todelliset tuotantokustannukset voivat erota arvioiduista vakiokustannuksista. Todellisia kustannuksia vertaillaan tietyn nimikkeen vakiokustannuksiin johdon hallintotarkoituksia varten, ja *erot* tunnistetaan ja analysoidaan.  

Vakiokustannuksia voidaan ylläpitää nimikkeiden osalta, jotka täydennetään ostojen, kokoonpanon ja tuotannon kautta. Kunkin täydennysmenetelmän vakiokustannukset voivat sisältää seuraavat elementit.  

|Täydennysjärjestelmä|Vakiokustannuksen elementit|  
|--------------------------|----------------------------|  
|**Osto**|Välittömät materiaalikustannukset ja yleismateriaalikustannukset tarvittaessa.|  
|**Kokoonpano**|Välittömät materiaalikustannukset, välittömät tai kiinteän työn kustannukset ja yleiskustannukset.|  
|**Tuotantotilaus**|Välittömät materiaalikustannukset, työkustannukset, alihankintakustannukset ja yleiskustannukset.|  

## <a name="set-up-standard-costs"></a>Vakiokustannusten määrittäminen

Vakiokustannukset on muodostettava jokaiselle kustannuselementille, koska kokoonpannun tai tuotetun nimikkeen vakiokustannukset koostuvat useista kustannuselementeistä, joita ovat materiaalien, kapasiteetin (työvoima) ja alihankkijan kustannukset (välittömät ja yleiset).  

Nimikkeitä käsittelevällä yrityksellä, joka käyttää vakiokustannuksia, on kaksinkertainen kirjanpitotehtävä:  

- valmiin nimikkeen vakiokustannusten arvioiminen ja määrittäminen nimikekorttiin.  
- tuotannon kustannuselementtien todellisten kustannusten tallentaminen ja kohdistaminen sekä erojen asianmukainen selvitys.  

Kaikki komponentin kustannukset on laskettava yhteen, jotta valmiin nimikkeen välittömät kustannukset voidaan määrittää. Koottu tai valmistettu nimike voi sisältää osakokoonpanoja, jotka voivat myös sisältää useita osia.  

Seuraavat keskeiset kustannukset muodostavat valmiiksi käsitellyn nimikkeen välittömän kokonaiskustannuksen:  

- Materiaalikulut  
- Kapasiteettikustannus  
- Alihankintakustannukset ainoastaan tuotetuille nimikkeille.  

### <a name="material-costs"></a>Materiaalikulut

Materiaalikustannuksia ovat osakokoonpanoihin ja ostettuun raaka-aineeseen liittyvät kustannukset. Materiaaliyksikön kustannukset voivat koostua välittömistä ja välillisistä kustannuselementeistä.  

- Välittömät materiaalikustannukset edustavat ostettujen raaka-aineiden tai osakokoonpanon käsittelykustannusten laskutettua summaa.  
- Välilliset kustannukset (tai *yleiskustannukset*) voivat koostua esimerkiksi tuotetun valmiin nimikkeen varastointikustannuksista.  

Ostettujen nimikkeiden materiaalikustannusten määrittäminen välillisiin ja välittömiin kustannuksiin riippuu kyseiselle nimikkeelle valitusta arvostusmenetelmästä. Kummankin arvostusmenetelmän kustannustiedot määritetään nimikkeen kortissa. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

Hukkatavaran kustannus tuotannossa on toinen kokonaismateriaalikustannusten laskennassa huomioon otettava tekijä. Kun tietty määrä raaka-ainetta hukataan nimikkeen kokoonpanossa tai tuotannossa, tämän nimikkeen tuotannossa tarvittavien komponenttien määrä yleensä kasvaa. Se taas lisää päänimikkeen tuotannossa tarvittavien komponenttien materiaalikustannuksia. Materiaalien hukkakustannus voidaan määrittää joko tuotannon tuoterakenteessa tai reitityksessä.  

Tuotetun nimikkeen materiaalikustannukset voidaan esittää kahdella vakiokustannusten laskentaperustetta vastaavalla tavalla:  

|Kustannusten laskentaperuste|Materiaalikustannusten laskenta|  
|----------------------------|-------------------------------|  
|Yksitasoinen|Tuotettu nimike vastaa kyseisen nimikkeen tuotannon tuotantorakenteen kaikkien ostettujen tai osakokoonpantujen nimikkeiden kokonaiskustannusta.|  
|Vyörytystaso tai monitasoinen|Tuotettu nimike on kyseisen nimikkeen tuotantorakenteen kaikkien osakokoonpanojen materiaalikustannusten ja kyseisen nimikkeen tuotannon tuotantorakenteen kaikkien ostettujen nimikkeiden summa.|  

### <a name="capacity-costs"></a>Kapasiteettikustannukset

Kapasiteetin kustannuksia ovat kustannukset, jotka liittyvät sisäisen työn ja koneen kustannuksiin. Määritä nämä kustannukset kullekin resurssille (kokoonpanon hallinnassa) ja työlle tai kuormitusryhmälle reitityksessä (tuotannossa). Kuten materiaalien kanssa, voit tunnistaa kapasiteettikustannusten väliliset ja välittömät elementit. Esimerkiksi tuotantosolun välittömät kustannukset voivat olla tietyn toiminnon suorituksesta muodostuvat tuotantokustannukset. Tuotantosolun epäsuoriin kustannuksiin voi kuulua joitain yleisiä tehdaskuluja, esimerkiksi valaistus ja lämmitys. Kuten materiaalikustannusten kanssa, voit ilmaista kapasiteetin yleiskustannukset välillisenä kustannusprosenttina tai kiinteänä yleiskustannuksena.  

Kapasiteettikustannusten asetukset koostuvat seuraavista elementeistä:  

- Resurssin välilliset ja välittömät yksikkökustannukset.  
- Kiinteä tai suora resurssikäyttötyyppi.  

Tuotettujen nimikkeiden kapasiteettikustannusten asetukset koostuvat seuraavista elementeistä:  

- Kuormitusryhmän tai tuotantosolun välittömät ja välilliset yksikkökustannukset.  
- Ajan ja erän koon asetukset.  

Tuotantoyrityksen on muodostettava koneen ja tuotantosolujen suorituksessa tarvittavat vakioaikapalkat kapasiteetin vakiokustannusten laskentaa varten. Toiminnon suorituksen kokonaisaika koostuu yleensä asennus- ja suoritusajasta sekä odotus- ja siirtoajasta.  

Jokaiselle koneelle/tuotantosolulle määritetään kunkin aikatyypin kustannukset yksittäistä reititystä kohti.  

> [!NOTE]  
>  On tärkeää huomata, että ajoajan kustannukset kohdistetaan jokaiseen tuotettavaan nimikeyksikköön ja asetuskustannukset kohdistetaan jokaiseen erään. Sen vuoksi kunkin toiminnon reitityksen asetusajan kustannukset on jaettava eräkoon mukaan. Eräkoko määritetään **nimikekortti**-sivulla **Täydennys**-pikavälilehtikentässä.  

Jos haluat määrittää määritysajan reitityksen suunnittelulle mutta et sisällyttää tätä kulua vakiokustannusten laskentaan, tyhjennä **Tuotannon asetukset** -sivun **Kust. sisältävät asetuksen** -kentän valinta.  

Yksitasoisena tämä on valmiin tuotantonimikkeen tuotannossa tarvittava työkustannus. Se määritetään tuotantonimikkeen reitityksessä. Monitasoisena tämä on päänimikkeen tuoterakenteeseen sisällytettyjen yksittäisten tuotettujen nimikkeiden kapasiteettikustannus.  

### <a name="subcontractor-costs"></a>Alihankkijan kustannukset

Alihankkijan kustannuksia ovat yrityksen ulkopuolisille toimittajille tai alihankkijoille toimittamiin palveluihin liittyvät kustannukset. Alihankkijan kustannukset voivat koostua materiaali- ja kapasiteettikustannusten tavoin sekä välittömistä että yleisistä kustannuksista. Välittömiä alihankkijan kustannuksia ovat tuotettujen palveluiden todelliset yksikkökohtaiset kulut. Yleisiä alihankkijan kustannuksia voivat olla esimerkiksi alihankintatilaukseen liittyvän yrityksen aiheuttamat kuljetus- ja/tai käsittelykustannukset.  

Koska alihankinta on ulkoistettua kapasiteettia, alihankintapalveluiden kustannukset (välittömät ja välilliset) määritetään alihankintatoimintoa edustavalle toimintosolukortille.  

## <a name="update-standard-costs"></a>Vakiokustannusten päivittäminen

Päivitä tai laske kokoonpanon nimikkeiden standardikustannukset käyttäen funktiota nimikekortista.  

Vakiokustannusten päivittäminen tai laskeminen koostuu yleensä seuraavista tehtävistä:  

1.  Päivitetään kustannuksia osa- ja kapasiteettitasolla. Lisätietoja on **Ehdota nimikkeen vakiokust.**- ja **Ehdota kapasiteetin vakiokustannusta** -eräajoissa.  
2.  Nimikkeiden kokoonpanon ja tuotannon kokonaiskustannusten laskeminen konsolidoimalla ja vyöryttämällä osa- ja kapasiteettikustannukset. Lisätietoja on kohdassa [Kokoonpanon nimikkeen vakiokustannusten laskeminen](assembly-how-work-assembly-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  Otetaan edellisten eräajojen aikana syötetyt vakiokustannukset käyttöön. Vakiokustannukset eivät tule voimaan, ennen kuin ne on otettu käyttöön. Käytä **Ota käyttöön vakiokustannusten muutokset** -erätyötä, joka päivittää nimikkeiden vakiokustannusten muutokset Vakiokustannustyökirja-taulukossa.  
4.  Otetaan muutokset käyttöön nimikkeen kortin **Yksikkökustannus**-kentän päivittämistä ja varaston uudelleenarvostuksen suorittamista varten. Lisätietoja on kohdassa [Varaston uudelleenarvostus](inventory-how-revalue-inventory.md).

## <a name="use-batch-jobs-to-update-standard-costs"></a>Eräajojen käyttäminen vakiokustannusten päivittämisessä
Alla olevissa osissa on tietoja eräajoista, joita käytetään vakiokustannusten päivittämisessä.
### <a name="suggest-item-standard-cost"></a>Ehdota nimikkeen vakiokust.

 Luo ehdotuksia nimikekorttien vakiokustannuksen kustannusten tai kustannusjakaumien muuttamiseksi. Kun eräajo on suoritettu loppuun, tuloksen voi nähdä Vakiokustannustyökirja-ikkunassa.

> [!NOTE]  
> Eräajo on tarkoitettu vain ostetuille nimikkeille. Jos haluat päivittää nimikkeen jolla on tuotantotilaus tai kokoonpanon tuotantotilaus, sinun tulee ensin täyttää työkirja kaikilla komponenteilla ja suorittaa sitten Vyörytä vakiokustannus -eräajo.

Tämä eräajo luo vain ehdotuksia. Se ei toteuta ehdotettuja muutoksia. Jos olet tyytyväinen ehdotuksiin ja haluat ottaa ne käyttöön eli päivittää ne nimikkeen kortteihin ja lisätä ne uudelleenarvostuspäiväkirjaan, valitse Vakiokustannustyökirja-ikkunassa Ota käyttöön vakiokustannusten muutokset.
#### <a name="options"></a>Asetukset

**Vakiokustannus**: Syötä muuntokerroin jota haluat käyttää kun päivität vakiokustannusta. Voit myös valita pyöristystavan uudelle vakiokustannukselle. Täytä kenttä käyttäen prosenttiosuuden kasvulle desimaalia, esimerkiksi 1,1.

**Välillinen kustannus -%**: Syötä muuntokerroin jota haluat käyttää kun päivität välillistä kustannusprosenttia. Voit myös valita pyöristystavan uudelle välitön kustannus -%:lle. Täytä kenttä käyttäen prosenttiosuuden kasvulle desimaalia, esimerkiksi 1,1.

**Yleiskustannus (arvo)**: Syötä muuntokerroin, jota haluat käyttää, kun päivität yleiskustannuksen arvoa. Voit myös valita pyöristystavan uudelle yleiskustannukselle. Täytä kenttä käyttäen prosenttiosuuden kasvulle desimaalia, esimerkiksi 1,1.

### <a name="suggest-workmach-ctr-std-cost"></a>Ehdota k.ryh./t.sol. vak.kust.

Luo ehdotuksia tuotantosolun, kuormitusryhmän tai resurssikorttien vakiokustannuksen kustannusten tai kustannusjakaumien muuttamiseksi. Kun eräajo on suoritettu loppuun, tuloksen voi nähdä **Vakiokustannustyökirja**-ikkunassa.

Tämä eräajo luo vain ehdotuksia. Se ei toteuta ehdotettuja muutoksia. Jos olet tyytyväinen ehdotuksiin ja haluat ottaa ne käyttöön eli päivittää ne nimikkeen kortteihin ja lisätä ne uudelleenarvostuspäiväkirjaan, valitse **Vakiokustannustyökirja**-ikkunassa **Ota käyttöön vakiokustannusten muutokset**.

Jos eräajon suorituksen jälkeen haluat nähdä sen vaikutuksen tuotantoon tai kokoonpano-osastoihin, voit suorittaa **Vyörytä vakiokustannus** -eräajon päivittääksesi vakiokustannukset tuotantosoluihin, kuormitusryhmiin, kokoonpanoresursseihin, tuotannon tuoterakenteisiin ja kokoonpanon tuoterakenteisiin.
#### <a name="options-1"></a>Asetukset
**Vakiokustannus**: Syötä muuntokerroin jota haluat käyttää kun päivität vakiokustannusta. Voit myös valita **pyöristystavan** uudelle vakiokustannukselle. Täytä kenttä käyttäen prosenttiosuuden kasvulle desimaalia, esimerkiksi 1,1.

**Välillinen kustannus -%**: Syötä muuntokerroin jota haluat käyttää kun päivität välillistä kustannusprosenttia. Voit myös valita pyöristystavan uudelle välitön kustannus -%:lle. Täytä kenttä käyttäen prosenttiosuuden kasvulle desimaalia, esimerkiksi 1,1.

**Yleiskustannus (arvo)**: Syötä muuntokerroin, jota haluat käyttää, kun päivität yleiskustannuksen arvoa. Voit myös valita pyöristystavan uudelle yleiskustannukselle. Täytä kenttä käyttäen prosenttiosuuden kasvulle desimaalia, esimerkiksi 1,1.

### <a name="post-inventory-cost-to-gl"></a>Kirjaa varaston kustannus KP:oon

 Tallentaa varaston määrien muutokset nimiketapahtumiin ja varaston arvojen muutokset arvotapahtumiin, kuten myyntitoimituksiin tai ostojen vastaanottoihin.

Jos et ole valinnut **Automaattinen kustannusten kirjaus** -valintaruutua **Varastonhallinnan asetukset** -ikkunassa, varastokustannuksia ei tallenneta dynaamisesti pääkirjanpitoon ja myytyjen tuotteiden kustannuksia ei lasketa myynnin yhteydessä. Tämän vuoksi kirjaukset pääkirjanpitoon tehdään manuaalisesti suorittamalla **Kirjaa varaston kust. KP:oon** -eräajo, joka päivittää pääkirjanpidon ja mahdollisesti tulostaa raportin kirjatuista arvotapahtumista.

Eräajo käyttää perustana arvotapahtumia. Eräajo laskee kirjattavan arvon käyttämällä arvotapahtumien **Kustannussumma (todellinen)** -kentän ja **KP:oon kirjattu kustannus** -kentän välistä eroa. Jos olet valinnut **Varastonhallinnan asetukset** -ikkunan **Oletettu kust. kirjaus KP:toon** -valintaruudun varastonhallinnan asetuksissa, eräajo kirjaa myös **Kustannussumma (oletettu)**- ja **Olet. kust. kirjattu KP:oon** -kenttien välisen eron.

> [!NOTE]
> Jos et ole valinnut **Varastonhallinnan asetukset** -ikkunassa **Oletettu kust. kirjaus KP:toon** -valintaruutua, raportin viimeisessä osassa ovat arvotapahtumat, jotka ohitettiin, koska ne edustavat oletettuja kustannuksia.

> [!NOTE] 
> Jos eräajossa löytyy dimensioihin tai dimensioiden asetuksiin liittyvä virhe, eräajo ohittaa virheen ja kirjaa tapahtuman pääkirjanpitoon käyttämällä arvotapahtuman dimensioita.

Jos haluat varmistaa, ettei eräajossa ilmene virheitä, voit suorittaa **Kirjaa varaston kustannukset kirjanpitoon - Testaa** -raportin, jossa näkyvät kaikki mahdolliset virheet. Voit korjata nämä virheet ja suorittaa sitten kaikki tapahtumat käsittelevän **Kirjaa varaston kustannus KP:oon** -eräajon ilman virheitä.
 
> [!IMPORTANT]  
> Suorita **Muuta kustannuksia - Nimiketapahtumat** -eräajo, ennen kuin käytät tätä eräajoa. Tällä tavoin varmistat, että pääkirjanpitoon kirjattavat kustannukset ovat ajan tasalla, kun sitten suoritat tämän eräajon.
#### <a name="options-2"></a>Asetukset

|Asetus  |Kuvaus  |
|--------------|---------|
|**Kirjaustapa**|Eräajo voi kirjata varaston arvon pääkirjanpitoon joko kirjausryhmän tai kirjatun tapahtuman mukaan. Jos kirjaat tapahtuman mukaan, saat yksityiskohtaisen määrityksen siitä, miten varasto vaikuttaa pääkirjanpitoon, mutta lisäksi saat useita KP-tapahtumia. Jos kirjaat kirjausryhmän mukaan, eräajo luo pääkirjanpidon tapahtuman kutakin kirjauspäivämäärän ja kirjausryhmän yhdistelmää kohden. Tämä tarkoittaa sitä, että pääkirjanpidon tapahtuma luodaan jokaista kirjauspäivämäärän, yleisen liiketoiminnan kirjausryhmän, yleisen tuotteen kirjausryhmän, varaston kirjausryhmän ja sijaintikoodin yhdistelmää kohden. Lisäksi eräajo luo erilliset pääkirjanpidon tapahtumat eri merkein varustettuja kustannuksia varten.|
|**Asiakirjan nro**|Tähän kenttään voit syöttää asiakirjan numeron, jos olet valinnut Kirjaa varaston kirjausryhmää kohti -vaihtoehdon. Asiakirjan numero näkyy kirjatuissa tapahtumissa.|
|**Kirjaa**|Valitse tämä kenttä, jos haluat eräajon kirjaavan yleiseen kirjanpitoon automaattisesti. Jos varaston kustannusta ei kirjata pääkirjanpitoon, eräajo tulostaa vain testiraportin, joka ilmaisee pääkirjanpitoon kirjattavissa olevat arvot, ja raporttiin tulee näkyviin teksti: **Testiraportti (ei kirjattu)**.|

### <a name="roll-up-standard-cost"></a>Vyörytä vakiokustannus

Vyöryttää kokoonpantujen ja tuotettujen nimikkeiden vakiokustannukset. Näihin vaikuttavat osien vakiokustannusten muutos, jota **Ehdota nimikkeen vakiokust.** -eräajo on ehdottanut. Lisäksi niihin vaikuttaa **Ehdota k.ryh./t.sol. vak.kust.** -eräajon ehdottama tuotantokapasiteetin ja kokoonpanon resurssien vakiokustannusten muutos.

Kun olet suorittanut toisen tai molemmat eräajoista ja toteutat vyörytyksen, kaikki työkirjan vakiokustannuksen muutokset on toteutettu liittyvissä tuotannon tai kokoonpanon tuoterakenteissa ja kustannukset on kohdistettu tuoterakenteen kaikille tasoille.

> [!NOTE] 
> Tämä funktio vyöryttää vain nimikekorttien vakiokustannuksen, ei varastointiyksiköiden vakiokustannusta.

Tämä eräajo luo vain ehdotuksia. Se ei toteuta ehdotettuja muutoksia. Jos olet tyytyväinen ehdotuksiin ja haluat ottaa ne käyttöön eli päivittää ne nimikekortteihin ja syöttää ne **Uudelleenarvostuspäiväkirja**-ikkunaan, voit käyttää **Ota käyttöön vakiokust. muutos** -eräajoa. Voit käyttää tätä eräajoa **Vakiokustannustyökirja**-ikkunassa.
#### <a name="options-3"></a>Asetukset

**Laskentapvm**: Syötä päivämäärä joka kohdistuu tuotannon tuoterakenteen versioon jolle haluat tehdä vyörytyksen.
 
### <a name="implement-standard-cost-change"></a>Ota käyttöön vakiokust. muutos

Päivittää **Nimike**-taulukon vakiokustannusten muutokset **Vakiokustannustyökirja**-taulukon tiedoilla. Vakiokustannuksen muutosten ehdotukset voidaan luoda **Ehdota nimikkeen vakiokust.**- ja/tai **Ehdota k.ryh./t.sol. vak.kust.** --eräajolla, ja niitä voi myös muuttaa. Vakiokustannuksen muutosehdotusten kaikkien kenttien sisällöt siirretään. Kun toteutat vakiokustannuksen muutosehdotuksia, voit nähdä ne nimikkeen kortissa ja/tai tuotantosolun/kuormitusryhmän kortissa. Myös uudelleenarvostuspäiväkirja luodaan, jotta voit päivittää olemassa olevan varaston arvon.
#### <a name="options-4"></a>Vaihtoehdot

**Kirjauspvm**: Syötä pvm, jolloin uudelleenluokittelu tulisi tapahtua.

**Asiakirjan nro**: Syötä uudelleenluokittelupäiväkirjan rivien numerot. Jos nimikepäiväkirjan erän nimelle on olemassa numerosarja asiakirjannumero seuraa tapahtumia jotka uudelleenluokittelupäiväkirjan kirjaaminen luo. Muuten voit syöttää numerot manuaalisesti.

**Nimikepäiväkirjan malli**: Syötä uudelleenluokittelupäiväkirjan mallin nimi.

**Nimikepäiväkirjan erän nimi**: Syötä todellisen uudelleenluokittelupäiväkirjan mallin nimi

Käynnistä eräajo valitsemalla **OK**. Jos et halua suorittaa eräajoa juuri nyt, sulje ikkuna valitsemalla **Peruuta**.

## <a name="see-also"></a>Katso myös

[Rakennetiedot: Kustannuslaskennan menetelmät](design-details-costing-methods.md)  
[Vakiokustannusten päivittäminen](finance-how-to-update-standard-costs.md)  
[Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)  
[Kokoonpanon tuoterakenteiden käyttäminen](assembly-how-work-assembly-boms.md)  
[Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md)  
[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
