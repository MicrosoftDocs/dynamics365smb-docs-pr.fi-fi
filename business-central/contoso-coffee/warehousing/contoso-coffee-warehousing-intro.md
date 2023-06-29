---
title: Contoso Coffeen esittely
description: 'Yleiskuvaus tilanteista, joissa Contoso Coffee -demotietojen avulla opit käyttämään Business Centralin varastointiominaisuuksia.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-warehousing"></a><a name="introduction-to-contoso-coffee-warehousing"></a>Contoso Coffeen fyysisen varastoinnin esittely

Contoso Coffee on kuvitteellinen yritys, joka tuottaa kuluttajille ja yrityksille kahvinkeittimiä. **Contoso Coffee** -sovellukset Business Centralille lisäävät demotietoja, joiden avulla voit opetella käyttämään varastointiominaisuuksia Business Centralissa. Voit määrittää fyysisen varastoinnin ominaisuuksia monella eri tavalla, katso [Yleiskuvaus erilaisista määritysvaihtoehdoista](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

Sovellus sisältää kolme sijaintia, jotka on optimoitu eri skenaarioita varten:

- **HOPEINEN**  

  Tämä sijainti on määritetty käyttämään varastopaikkoja. Se voidaan helposti määrittää tukemaan perus- tai lisätietoja. 

- **KELTAINEN**  

  Tässä sijainnissa käytetään varastoinnin lisäkonfiguraatiota, mutta se ei käytä varastopaikkoja. Se voidaan määrittää uudelleen tukemaan perusmäärityksiä.

- **VALKOINEN**  

  Tässä sijainnissa käytetään kehittynyttä fyysisen varastoinnin konfiguraatiota, jossa on ohjatut hyllytykset ja poiminnat, joiden avulla nimikkeet liikkuvat koko fyysisessä varastossa.

## <a name="set-up-contoso-coffee-warehousing-data"></a><a name="set-up-contoso-coffee-warehousing-data"></a>Contoso Coffeen varastointitietojen määrittäminen

Contoson Coffeen varastoinnin esittelytietojen käyttäminen edellyttää, että asennat asianomaiseen yritykseen [!INCLUDE [prod_short](../../includes/prod_short.md)] -ratkaisussa kaksi sovellusta:  

- **Contoso Coffee Demo Dataset**  

    Tämä sovellus tarjoaa demotietoja perussovellukselle.  
- **Contoso Coffee Demo Dataset (maatunnus)**  

    Tämä sovellus lisää maakohtaisen sisällön perussovelluksen päälle.

Lisää sovellukset tyhjään yritykseen maksulliseen tilaukseen tai kokeiluversion osana. Voit esimerkiksi luoda uuden yrityksen, jolla ei ole näytetietoja **Luo uusi yritys** -asennustoiminnon avulla, jonka voit avata **Yritykset**-luettelosta. Lisää sitten sovellukset [Marketplacesta](../../ui-extensions-install-uninstall.md#install), jos niitä ei ole vielä **Laajennusten hallinta** -sivulla.  

Kun asianmukaiset sovellukset on asennettu, siirry [Contoso Coffeen varastoinnin esittelytiedot](https://businesscentral.dynamics.com/?page=4761) -sivulle [!INCLUDE [prod_short](../../includes/prod_short.md)] ja muuta oletusasetuksia tarpeidesi mukaan. Asetukset kuvaillaan seuraavassa taulukossa:  

|Kenttä  |Kuvaus  |
|---------|---------|
|**Aloitusvuosi** |Määrittää ensimmäisen vuoden, jota haluat käyttää Contoso Coffee -demotiedoissa. Yrityksen asetuksista riippuen vuosi on joko kalenterivuosi tai tilikausi.|
|**Sijainti Lokero**  |Sijainti, jota käytetään perussijaintiskenaarioissa.|
|**Sijainnin edistynyt logistiikka**  |Sijainti, jota käytetään logistiikan perusskenaarioissa.|
|**Sijaintiohjattu hyllytys ja poiminta**  |Sijainti, jota käytetään logistiikan lisäskenaarioissa.|
|**Sijainti Kuljetuksessa**  |Siirtoskenaarioiden kuljetuksessa-sijainnissa käytettävä sijainti.|
|**Asiakasnro**  |Asiakas, jota käytetään myyntitoimintojen perusskenaarioissa ja yksinkertaisissa skenaarioissa.|
|**Toimittajanro**  |Toimittaja, jota käytetään kaikissa ostotoimintojen skenaarioissa.|
|**Päänimikenro**  |Nimike, jota käytetään kaikissa myyntitoimintojen skenaarioissa.|
|**Nimikkeen 1 nro**  |Kaikissa skenaarioissa käytettävä päänimike.|
|**Nimikkeen 2 nro**  |Kaikissa skenaarioissa käytettävä lisänimike.|
|**Asiakkaan kirjausryhmä**|Määrittää liiketoimintakoodin kotimaan asiakkaille. Liiketoimintakoodeja käytetään, kun tapahtumia kirjataan. |
|**Asiakkaan yleinen liiketoiminnan kirjausryhmä**|Määrittää liiketoimintakoodin kotimaan asiakkaille. Liiketoimintakoodeja käytetään, kun tapahtumia kirjataan. |
|**Toimittajan kirjausryhmä**|Määrittää liiketoimintakoodin kotimaan asiakkaille ja toimittajille. Liiketoimintakoodeja käytetään, kun tapahtumia kirjataan. |
|**Toimittajan yleinen liiketoiminnan kirjausryhmä**|Määrittää liiketoimintakoodin kotimaan asiakkaille ja toimittajille. Liiketoimintakoodeja käytetään, kun tapahtumia kirjataan. |
|**Kotimaa – ALV-liiketoiminnan kirjausryhmä**|Määrittää liiketoiminnan ALV-koodin asiakkaille ja toimittajille ALV:n kirjaamista varten, jos ALV on käytössä.|
|**Jälleenmyynti – Varaston kirjausryhmä**    |Määrittää koodin nimikkeille, joita tulee käyttää kirjattaessa uudelleenmyyntiä.|
|**Vähittäismyynti – Tuotteen yleinen kirjausryhmä**    |Määrittää koodin nimikkeille, joita tulee käyttää kirjattaessa vähittäismyyntiä.|
|**Tuotteen ALV-kirjausryhmä**    |Määrittää tuotteen ALV-koodin nimikkeille ALV:n kirjaamista varten, jos ALV on käytössä.|
|**Hintakerroin**     |Määrittää kertoimen, jolla hinta muunnetaan USD/EUR-valuutasta paikalliseksi valuutaksi. *1* tarkoittaa, että hinta on sama summa kaikissa valuutoissa. Korkeampaa numeroa käytetään, kun hinta saadaan paikallisena valuuttana. |
|**Pyöristystarkkuus**  |Määrittää, miten lasketun kulutuksen määrät pyöristetään, kun ne syötetään kulutuspäiväkirjan riveille. Määrät, jotka ovat pienempiä kuin 0,5, pyöristetään alaspäin. Määriä, jotka ovat yhtä suuria tai suurempia kuin 0,5, pyöristetään ylöspäin.|

Kun olet valmis, valitse **Luo demotiedot** -toiminto. Tietojen lisääminen pohjana olevaan tietokantaan kestää muutaman minuutin, mutta sitten olet valmis suorittamaan erilaisia skenaarioita.  

> [!IMPORTANT]
> Jos käytät skenaarioita, haluat ehkä varmistaa, että käyttäjä on lisätty valittujen sijaintien osalta. Lisätietoja on kohdassa [Varastotyöntekijöiden määrittäminen](../../warehouse-how-to-set-up-warehouse-employees.md).

## <a name="scenarios"></a><a name="scenarios"></a>Esimerkkitilanteet

Contoso Coffeen varastoinnin esittelytiedot tukevat tällä hetkellä seuraavia testi- ja harjoitteluskenaarioita:

1.  [Vaihekuvaus: Saapuva ja lähtevä työnkulku fyysisen varaston perusmäärityksissä](warehouse-basic-flow-putaway-pick.md)
2.  [Vaihekuvaus: Saapuva ja lähtevä työnkulku fyysisen sekavaraston perusmäärityksissä](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Vaihekuvaus: Saapuva ja lähtevä työnkulku edistyneessä fyysisen varaston määrityksessä, jossa on ohjattu hyllytys ja poiminta](warehouse-directed-flow.md)

Lue kunkin skenaarion vaiheet asianomaisessa artikkelissa.  

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Varaston määrittäminen](../../inventory-setup-inventory.md) 
[Tietoja sijaintien määrittämisestä](../../inventory-how-setup-locations.md) 
[Varastointi](../../warehouse-manage-warehouse.md) 
[Suunnittelutiedot](../../design-details-warehouse-overview.md) 
