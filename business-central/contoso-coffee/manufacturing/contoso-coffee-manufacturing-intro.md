---
title: Contoso Coffeen tuotannon esittely
description: 'Yleiskuvaus tilanteista, joissa Contoso Coffee -demotietojen avulla opit käyttämään Business Centralin tuotanto-ominaisuuksia.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-manufacturing" />Contoso Coffeen tuotannon esittely

Contoso Coffee on kuvitteellinen yritys, joka tuottaa kuluttajille ja yrityksille kahvinkeittimiä. **Contoso Coffee** -sovellukset Business Centralille lisäävät demotietoja, joiden avulla voit opetella käyttämään tuotanto-ominaisuuksia Business Centralissa.  

Sovellus sisältää neljä tuotetta, jotka on optimoitu eri skenaarioita varten:

- **SP-SCM1009 Airpot**  

  Tämä tuote on tuoterakenne, jossa on alikokoonpano **Reititys**. Käytä sitä vakiotuotantovirtojen osoittamiseen. Siihen on määritetty vaihtoehtoisia reitityksiä, joita voidaan käyttää osoittamaan eri skenaarioita, joihin liittyy alihankkijoita. Arvostusmenetelmä on *Vakio*.  

- **SP-SCM1011 Airpot Duo**  

  Tämä tuote edellyttää nimikeseurantaa, ja siinä on komponentti, joka edellyttää myös nimikeseurantaa. Arvostusmenetelmä on *Määrätty*.  

- **SP-SCM1004 Autodrip**  

  Tämä tuote on tuoterakenne, jossa on alikokoonpano **Reititys**. On suositeltavaa osoittaa sen avulla eri materiaalin ottotavat sekä komponenteille että operaatioille. Arvostusmenetelmä on *Vakio*.

- **SP-SCM1006 AutoDripLite**

  Tällä tuotteella on kolme eri varianttia ja kolme tuoterakennetta, jotka voidaan liittää varastointiyksiköihin. Tuote käyttää haamutuoterakenteen käsitettä. Arvostusmenetelmä on *Vakio*.

Kaikkien skenaarioiden tuotanto toiminnot käyttävät sijaintia *NORTH*.  

> [!IMPORTANT]
> Ennen kuin suoritat mitään Contoso Coffeen skenaarioista, kirjaa kaikki nimikepäiväkirja rivit, joilla on alkusaldot. Lisätietoja vaatimuksista on [Contoso Coffee -tietojen määrittäminen](#set-up-contoso-coffee-manufacturing-data) -osiossa.

## <a name="set-up-contoso-coffee-manufacturing-data" />Contoso Coffeen tuotantotietojen määrittäminen

Contoson Coffeen tuotannon esittelytietojen käyttäminen edellyttää, että asennat asianomaiseen yritykseen [!INCLUDE [prod_short](../../includes/prod_short.md)] -ratkaisussa kaksi sovellusta:  

- **Contoso Coffee Demo Dataset**  

    Tämä sovellus tarjoaa demotietoja perussovellukselle.  
- **Contoso Coffee Demo Dataset (maatunnus)**  

    Tämä sovellus lisää maakohtaisen sisällön perussovelluksen päälle.

Lisää sovellukset tyhjään yritykseen maksulliseen tilaukseen tai kokeiluversion osana. Voit esimerkiksi luoda uuden yrityksen, jolla ei ole näytetietoja **Luo uusi yritys** -asennustoiminnon avulla, jonka voit avata **Yritykset**-luettelosta. Lisää sitten sovellukset [Marketplacesta](../../ui-extensions-install-uninstall.md#install), jos niitä ei ole vielä **Laajennusten hallinta** -sivulla.  

Kun asianmukaiset sovellukset on asennettu, siirry [Contoso Coffee -esittelytiedot](https://businesscentral.dynamics.com/?page=4760) -sivulle [!INCLUDE [prod_short](../../includes/prod_short.md)] ja muuta oletusasetuksia tarpeidesi mukaan. Asetukset kuvaillaan seuraavassa taulukossa:  

|Kenttä  |Kuvaus  |
|---------|---------|
|**Aloitusvuosi** |Määrittää ensimmäisen vuoden, jota haluat käyttää Contoso Coffee -demotiedoissa. Yrityksen asetuksista riippuen vuosi on joko kalenterivuosi tai tilikausi.|
|**Tuotantosijainti** |Määrittää varaston, jota haluat käyttää tuotantotoiminnoissa. Oletus arvo on *NORTH*, mutta sitä voi muuttaa tarpeidesi mukaan.|
|**Yritystyyppi**    |Määrittää, onko valitun yrityksen ilmoitettava ALV vai myyntivero. |
|**Kotimaa – Yleinen liiketoiminnan kirjausryhmä**|Määrittää liiketoimintakoodin kotimaan asiakkaille ja toimittajille. Liiketoimintakoodeja käytetään, kun tapahtumia kirjataan. |
|**Kapasiteetti – Tuotteen yleinen kirjausryhmä**    |Määrittää koodin nimikkeille tai resursseille, joita tulee käyttää kirjattaessa kapasiteettia.|
|**Vähittäismyynti – Tuotteen yleinen kirjausryhmä**    |Määrittää koodin nimikkeille tai resursseille, joita tulee käyttää kirjattaessa vähittäismyyntiä.|
|**Raaka – Tuotteen yleinen kirjausryhmä**    |Määrittää koodin nimikkeille tai resursseille, joita tulee käyttää kirjattaessa raaka-aineita. |
|**ALV-perusteen koodi**    |Määrittää olemassa olevan tuotteen ALV-ryhmän, jota käytetään nimikkeille.|
|**Valmis-koodi**    |Määrittää olemassa olevan tuoteryhmän, jota käytetään valmiille nimikkeille.|
|**Hintakerroin**     |Määrittää kertoimen, jolla hinta muunnetaan USD/EUR-valuutasta paikalliseksi valuutaksi. *1* tarkoittaa, että hinta on sama summa kaikissa valuutoissa. Korkeampaa numeroa käytetään, kun hinta saadaan paikallisena valuuttana. |
|**Pyöristystarkkuus**  |Määrittää, miten lasketun kulutuksen määrät pyöristetään, kun ne syötetään kulutuspäiväkirjan riveille. Määrät, jotka ovat pienempiä kuin 0,5, pyöristetään alaspäin. Määriä, jotka ovat yhtä suuria tai suurempia kuin 0,5, pyöristetään ylöspäin.|

Kun olet valmis, valitse **Luo demotiedot** -toiminto. Tietojen lisääminen pohjana olevaan tietokantaan kestää muutaman minuutin, mutta sitten olet valmis suorittamaan erilaisia skenaarioita.  

## <a name="scenarios" />Esimerkkitilanteet

Contoso Coffeen tuotannon esittelytiedot tukevat tällä hetkellä seuraavia testi- ja harjoitteluskenaarioita:

1. [Uuden tuotannon tuoterakenteen ja tuoterakenneversion luominen](create-new-production-bom-version.md)  
2. [Uuden reitityksen luominen](create-new-routing.md)  
3. [Luo sitovasti suunniteltu tuotantotilaus muuta sitä](create-firm-planned-production-order-change.md)  
4. [Yhdistä automaattinen ja manuaalinen materiaalinotto](combine-automatic-manual-flushing.md)  
5. [Käytä tilauksen suunnittelua tarjonnan luomiseksi ja varaamiseksi](order-planning-create-reserve-supply.md)  
6. [Alihankintatoiminnon määrittäminen ja käsitteleminen](set-up-process-subcontracting-operation.md)  
7. [Määritä uusi kapasiteetti](set-up-new-capacity.md)  
8. [Nimikevarianttien, joille on määritetty eri tuoterakenteet, kysyntäennuste](variants.md)  

Lue kunkin skenaarion vaiheet asianomaisessa artikkelissa.  

> [!IMPORTANT]
> Nämä vaihekuvaukset edellyttävät, että käyttäjäkokemukseksi on asetettu *Premium* **Yritystiedot**-sivulla.

## <a name="see-also" />Katso myös

[Tuotanto](../../production-manage-manufacturing.md)  
[Business Centralin tuotantoraportit ja analytiikka](../../production-reports.md)  
