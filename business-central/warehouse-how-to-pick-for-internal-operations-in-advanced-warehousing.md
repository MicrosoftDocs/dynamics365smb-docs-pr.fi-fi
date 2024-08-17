---
title: Poiminta sisäisissä toiminnoissa laajennetuissa varastomäärityksissä
description: 'Jos sijainneissasi käytetään poimintaa ja toimitusta, poimi komponentteja tuotantoa, kokoonpanoa ja projektitoimintoja varten F. varastoinnin poiminta -sivulla.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 08/12/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="pick-for-production-assembly-or-projects-in-advanced-warehouse-configurations"></a>Poiminta tuotantoa, kokoonpanoa tai projekteja varten laajennetuissa fyysisen varastoinnin määrityksissä

Komponenttien poimintatapa tuotantoa, projekteja tai kokoonpanotilauksia varten määräytyy sen mukaan, miten fyysinen varastointi on määritetty sijainniksi. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

Käytä lähtevää virtaa (poimintaa) varten laajennetussa fyysisen varastoinnin määrityksessä **sijainnin Sijainti-kortti**  sivulla seuraavia asetuksia:

* Tuotanto Tuot **. kulutus f. var. Valitse Käsittely-kenttä**, F **. var. poiminta (valinnainen)**  tai **F. varastoinnin poiminta (pakollinen)**.
* Kokoonpano, **Asm. Kulutus F. var. Valitse Käsittely-kenttä**, F **. var. poiminta (valinnainen)**  tai **F. varastoinnin poiminta (pakollinen).**
* projektinhallinta **projektin kulutus f. var. Valitse Käsittely-kenttä**, F **. var. poiminta (valinnainen)**  tai **F. varastoinnin poiminta (pakollinen).**

Kun sijainnissa on määritetty pakolliseksi fyysisen varastoinnin poiminnan käsittely, käytä fyysisen varastoinnin poiminta-asiakirjoja luodaksesi ja käsitelläksesi poimintatietoja ennen komponenttien käytön tai kulutuksen kirjaamista.  

Fyysisen varastoinnin poiminta-asiakirjaa ei voi luoda tyhjästä. Poiminnat ovat sellaisen työnkulun osa, jossa tilausta käsittelevä henkilö luo ne push-menetelmänä tai varastotyöntekijä luo ne pull-menetelmänä:

- Push-menetelmässä käytetään **Luo poiminta** -toimintoa **Tuotantotilaus**-, **Kokoonpanotilaus**- ja **Projektikortti**-sivulla. Poimittavat rivit valitaan ja poiminnat valmistellaan määrittämällä esimerkiksi, mistä varastopaikoista otetaan ja mihin asetetaan sekä kuinka monta yksikköä käsitellään. Varastopaikat on voitu määrittää valmiiksi fyysisen varaston sijainnissa tai resurssissa.
- Pull-menetelmässä **tuotantotilaus**, **kokoonpanotilaus** ja **projektikortti** vapautetaan fyysiseen varastoon, jolloin nimikkeet ovat poimittavissa. Varastontyöntekijä voi sitten käyttää **Poimintatyökirja**-sivulla **Hae f. varastoinnin asiakirjat** -toimintoa määritettyjen poimintojen noutamiseen.

Lähdeasiakirjojen komponenttien poimiminen tai siirtäminen pull-menetelmällä edellyttää lähdeasiakirjan vapauttamista, jotta poimimiseen ollaan valmiita. Vapauta sisäisten toimintojen lähdeasiakirjat seuraavilla tavoilla.  

|Lähdeasiakirja|Vapautustapa|  
|---------------------|--------------------|  
|Tuotantotilaus|Tilauksen tilaksi muutetaan Vapautettu tai vaihtoehtoisesti vapautettu tuotantotilaus luodaan heti.|  
|Kokoonpanotilaus|Muuta tilaksi Vapautettu.|
|Projektit | Muuta tilaksi Avoin tai luo projekti, jonka tila on Avoin heti.|  

## <a name="production"></a>Tuotanto

Tuotannon komponentteja voi poimia työkulussa tuotantoon **F.varastoinnin poiminta** -asiakirjojen avulla.

Jos sijainnissa käytetään varastopaikkoja nimikkeiden siirtämiseen avoimiin tuotannon varastopaikkoihin, käytettävissä on seuraavat menetelmät:

* Jos sijainnissa käytetään ohjattua hyllytystä ja poimintaa, lisätietoja on artikkelissa [Nimikkeiden siirtäminen laajennetuissa fyysisen varaston määrityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md).
* Muita sijainteja koskevia lisätietoja on artikkelissa [Nimikkeiden sisäinen siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

## <a name="assembly"></a>Kokoonpano

Kokoonpanon komponentit voidaan siirtää kokoonpanoalueelle **F.varastoinnin poiminta** -asiakirjojen avulla.

[!INCLUDE [prod_short](includes/prod_short.md)] tukee kokoonpanovirtoja, joiden tyyppi on kokoonpanoa varastoa varten ja kokoonpano tilausten varten. Lisätietoja fyysisen varaston lähtevän virran kokoonpanosta tilausten varten on kohdassa [Kokoonpano tilausta varten -nimikkeiden käsitteleminen fyysisen varastoinnin toimituksissa](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

## <a name="project-management"></a>Projektien hallinta

Poimi projektin komponentteja projektinhallinnan työnkulussa F. varastoinnin poiminta **-asiakirjojen avulla** .

> [!NOTE]
> Project ei tue laajennettuja määrityksiä, joissa ohjattu poiminta **- ja hyllytysvalinta** on käytössä.

## <a name="check-whether-items-are-available-for-picking"></a>Tarkista, ovatko nimikkeet poimittavissa

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Poiminta-asiakirjojen joukkoluonti poimintatyökirjan avulla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poimintatyökirja** ja valitse sitten vastaava linkki.  
2. Valitse **Hae f. varastoinnin asiakirjat** -toiminto.  

    Luettelossa näkyvät vapautetut tuotantotilaukset, projektit ja kokoonpanotilaukset, jotka on välitetty poimintatoimintoon. Tilaukset sisältävät ne, joille poimintaohjeet on jo luotu. Tässä luettelossa ei ole asiakirjoja, joiden poimintarivit on poimittu ja rekisteröity.  
3. Valitse tilaukset, joiden poiminta halutaan valmistella.

    > [!NOTE]  
    > Jos valitussa asiakirjassa on jo ohjeet kaikilla riveillä, [!INCLUDE [prod_short](includes/prod_short.md)] ilmoittaa, ettei mitään käsiteltävää ole. Jo luotujen fyysisen varaston poimintaohjeiden yhdistäminen yhdeksi poimintaohjeeksi tehdään poistamalla ensin yksittäiset fyysisen varaston poiminnat.

4. Järjestä rivit haluamallasi tavalla täyttämällä **Järjestämistapa**-kenttä.  

    > [!NOTE]  
    > Rivien lajittelu työkirjassa ei automaattisesti toteudu samanlaisena poimintaohjeessa. Samat lajittelutyönkalut, myös varastopaikkaluokittelu ovat kuitenkin käytettävissä. Työkirjassa suunnittu rivijärjestys on helppo luoda uudelleen poimintaohjeita luotaessa tai niitä lajiteltaessa.

5. Täytä **Käsiteltävä määrä** -kenttä. Valitse **Täytä autom. käsitelt. määrä** -toiminto tai täytä kentät manuaalisesti.  

    Sivulla näkyy määrät, jotka ovat saatavana laiturointivarastopaikoissa, mikä on kätevää suunniteltaessa työtehtäviä laiturointitilanteissa. [!INCLUDE[prod_short](includes/prod_short.md)] ehdottaa aina ensin poimimista laiturointivarastopaikasta.

6. Rivejä voi tarvittaessa muokata manuaalisesti. Poimintaa voi myös tehostaa poistamalla joitakin rivejä. Jos esimerkiksi useilla riveillä on nimikkeitä, joita ovat laiturointivarastopaikoissa, kaikkien rivien poiminta voidaan luoda. Laituroidut nimikkeet poimitaan muiden lähdeasiakirjassa olevien nimikkeiden kanssa, joten laiturointivarastopaikkoihin tulee tilaa uusille saapuville nimikkeille.

    > [!NOTE]  
    >  Rivit vain kyseisestä työkirjasta, ei poiminnan valintaluettelosta.  

7. Valitse **Luo poiminta** -toiminto. **Luo poiminta** -sivu avautuu, ja sivulla poimintaan voi lisätä muita tietoja.  

    Poimintarivien yhdistäminen määritetään valitsemalla jokin seuraavista vaihtoehdoista.  

    |Asetus|Kuvaus|
    |-|-|
    |Per f.var. Asiakirja|Luo erilliset poiminta-asiakirjat työkirjan riveille, joilla on sama varastolähdeasiakirja.|
    |Per asiak./toimit./sijainti|Luo erilliset poiminta-asiakirjat kullekin asiakkaalle (projektille)|
    |Per nimike|Luo erilliset poiminta-asiakirjat kullekin nimikkeelle poimintatyökirjassa.|
    |Per lähtöalue|Luo erilliset poiminta-asiakirjat kullekin alueelle, josta nimikkeitä otetaan.|
    |Per lokero|Luo erilliset poiminta-asiakirjat kullekin varastopaikalle, josta nimikkeitä otetaan.|
    |Per eräpäivä|Luo erilliset varastopoiminta-asiakirjat lähdeasiakirjoille, joilla on sama eräpäivä.|

    Määritä seuraavien asetusten avulla, miten poiminta-asiakirjat luodaan.  

    |Asetus|Kuvaus|
    |-|-|
    |Maks. Nro poimintarivejä|Luo poiminta-asiakirjat, joista jokaisessa on enintään määritetty määrä rivejä.|
    |Maks. Ei. poiminnan lähdeasiakirjoja|Luo poiminta-asiakirjat, jotka kattavat määritetyn määrän lähdeasiakirjoja.|
    |Määritetty käyttäjätunnus|Luo poiminta-asiakirjat vain työkirjan riveille, jotka on liitetty valittuun varastotyöntekijään.|
    |Järjestämistapa poimintariveille|Rivien lajittelu luodussa poiminta-asiakirjassa tekemällä valinnan käytettävistä olevista vaihtoehdoista.|
    |Aseta erottelusuodatin|Piilottaa poiminnan erottelurivit, kun suurempi mittayksikkö muunnetaan pienemmäksi mittayksiköksi ja poimitaan.|
    |Älä täytä käsiteltävää määrää|Jättää **Käsiteltävä määrä** -kentän tyhjäksi luoduilla poimintariveillä.|
    |Tulosta poiminta|Tulostaa poiminta-asiakirjat, kun ne luodaan. Tulostus on mahdollista myös luoduista poiminta-asiakirjasta.|

8. Valitse **OK**-painike.  

## <a name="to-pick-items-for-a-production-order-assembly-order-or-project"></a>Nimikkeiden poiminta tuotantotilausta, kokoonpanotilausta tai projektia varten

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poiminnat** ja valitse sitten vastaava linkki.  

    Jos tiettyä poimintaa on käsiteltävä, poiminta valitaan luettelosta tai määritetyt poiminnat etsitään suodattamalla luetteloa. Avaa poiminnan kortti.  
2. Jos **Määritetty käyttäjätunnus** -kenttä on tyhjä, syötä tunnus tarvittaessa itse.  
3. Poimi nimikkeet.  

    Jos fyysinen varasto on määritetty käyttämään varastopaikkoja, nimikkeen ottopaikkoja ehdotettaessa käytetään nimikkeen oletusvarastopaikkoja. Ohjeissa on ainakin kaksi erillistä otto- ja asetustoimintojen riviä.  

    Toimintoalueilla, kuten tuotannon varastopaikoissa, voi olla oletusvarastopaikka vaadituille komponenteille. Jos se on olemassa, oletusvarastopaikkakoodi lisätään fyysisen varaston poiminta-asiakirjaan osoittamaan, minne nimikkeet sijoitetaan. Lisätietoja on Tuotanto-varastopaikan koodi-, **Kokoonpanon varastopaikkakoodi**- ja **Projektiin-varastopaikkakoodi**-kenttien työkaluvihjeissä **.** 

    Jos fyysinen varasto on määritetty käyttämään ohjattua hyllytystä ja poimintaa, parhaat poimintavarastopaikat lasketaan varastopaikan luokittelun avulla. Kyseisiä varastopaikkoja ehdotetaan poimintarivillä. Ohjeissa on ainakin kaksi erillistä otto- ja asetustoimintojen riviä.  

    * Ensimmäisellä rivillä, jolla **Toiminnon tyyppi** -kentässä on **Ota**, ilmaistaan, millä poiminta-alueella nimikkeet sijaitsevat. Jos yhdellä vastaanottorivillä toimitetaan suuri määrä nimikkeitä, nimikkeet on ehkä poimittava useista varastopaikoista, joten kullakin varastopaikalla on Ota-rivi.
    * Seuraava rivi, jonka **Toiminnon tyyppi** -kentässä lukee **Aseta**, osoittaa, minne nimikkeet on asetettava fyysisessä varastossa. Tällä rivillä olevaa aluetta ja varastopaikkaa ei voi muuttaa.

    > [!NOTE]
    > Jos yhden rivin nimikkeet on poimittava useasta varastopaikasta tai asetettava useaan varastopaikkaan esimerkiksi siksi, että määritetty varastopaikka on täynnä, käytä **Rivit**-pikavälilehden **Jaa rivi** -toimintoa. Toiminto luo rivin jäljellä olevalle käsiteltävälle määrälle.

      Poimintarivejä voidaan järjestellä erilaisten ehtojen, kuten nimikkeen, hyllynumeron tai eräpäivän, mukaan. Järjestäminen voi auttaa hyllytysprosessin optimoinnissa esimerkiksi seuraavasti:

    * Jos kunkin lähetysrivin Ota- ja Aseta-rivit eivät ole peräkkäiset ja niiden halutaan olevan peräkkäisiä, järjestä rivit valitsemalla **Nimike** **Järjestämistapa**-kentässä.  
    * Jos varastopaikan luokittelut vastaavat fyysisen varaston fyysistä asettelua, työt järjestetään varastopaikkojen sijainnin perusteella käyttämällä **Varastopaikan luokittelu** -järjestämistapaa.

  > [!NOTE]  
  > Rivit on lajiteltu valittujen kriteereiden nousevassa järjestyksessä. Jos järjestelet asiakirjan mukaan, lajittelu tehdään ensin asiakirjatyypin mukaan **F. varastoinnin aktiviteetin lähdeasiakirja** -kentän perusteella. Jos järjestelet määränpään mukaan, lajittelu tehdään ensin kohdetyypin mukaan **F. varastoinnin kohdetyyppi** -kentän perusteella.

4. Kun olet poiminut ja sijoittanut nimikkeet tuotantoon, kokoonpanoon, projektialueeseen tai varastopaikkaan, valitse Rekisteröi poiminta **-** toiminto.  

    Nimikkeet voidaan nyt tuoda kyseiselle alueelle ja poimittujen komponenttien käyttö tai kulutus voidaan kirjata kirjaamalla kulutuspäiväkirja, kokoonpanotilaus tai projektipäiväkirja. Seuraavissa artikkeleissa on lisätietoja:

    * [Yhden vapautetun tuotantotilausrivin kulutuksen ja tuotoksen rekisteröiminen](production-how-to-register-consumption-and-output.md)
    * [Nimikkeiden kokoonpano](assembly-how-to-assemble-items.md)
    * [Projektien kulutuksen tai käytön kirjaaminen](projects-how-record-job-usage.md)

## <a name="flushing-production-components-in-an-advanced-warehouse-configuration"></a>Tuotannon komponenttien materiaaliotto laajennetussa fyysisen varaston määrityksessä

Materiaaliottotavat vaikuttavat komponenttien siirtymiseen tuotantoon. Lisätietoja on kohdassa [Komponenttien materiaalinotto toiminnan tuotoksen mukaan](production-how-to-flush-components-according-to-operation-output.md). Valitun materiaaliottotavan mukaan komponentteja voi poimia tuotantoon seuraavilla tavoilla:

* Käyttämällä **F.varastoinnin poiminta** -asiakirjaa **Manuaalinen**-materiaaliottotapaa käyttävien nimikkeiden poiminnan kirjaamiseen. Kulutus on rekisteröitävä erikseen. Lisätietoja on kohdassa [Tuotannon kulutuksen eräkirjaus](production-how-to-post-consumption.md).
* Käyttämällä **F.varastoinnin poiminta** -asiakirjaa **Poiminta + eteenpäin**- tai **Poiminta + taaksepäin** -materiaaliottotapaa käyttävien nimikkeiden poiminnan kirjaamiseen. Komponentteja kulutetaan automaattisesti, joko muutettaessa tuotantotilauksen tilaa taikka aloitettaessa tai lopetettaessa työvaihetta. Kaikkien pakollisten komponenttien on oltava saatavana. Muutoin kyseisen komponentin materiaalinoton kirjaus lopetetaan.
* Käyttämällä **F. var. siirto** -asiakirjaa viittaamatta lähdeasiakirjaan tai kirjaamalla muulla tavoin **Eteenpäin**- tai **Taaksepäin**-materiaaliottotapaa käyttävien komponenttien varaston siirrot. Komponentteja kulutetaan automaattisesti, joko muutettaessa tuotantotilauksen tilaa taikka aloitettaessa tai lopetettaessa työvaihetta. Kaikkien pakollisten komponenttien on oltava saatavana. Muutoin kyseisen komponentin materiaalinoton kirjaus lopetetaan. Lisätietoja on kohdassa [Nimikkeiden siirtäminen](warehouse-move-items.md).

### <a name="example"></a>Esimerkki

Nimikkeellä SP-SCM1004 on 15 kappaleen tuotantotilaus.. Joiden komponenttiluettelon nimikkeiden materiaaliotto on tehtävä manuaalisesti kulutuspäiväkirjassa. Muiden nimikkeiden poiminta ja materiaaliotto voidaan tehdä automaattisesti käyttämällä **Poiminta + taaksepäin** -materiaaliottotapaa.  

Seuraavissa vaiheissa käsitellään toimintoja, joita eri henkilöt tekevät ja niihin liittyviä vastauksia:  

1. Kaupan työnjohtaja vapauttaa tuotantotilauksen. Nimikkeet, jotka käyttävät **Eteenpäin**-materiaalinottotapaa ja joilla ei ole reitityslinkkiä, vähennetään avoimen tuotannon varastopaikasta.  
2. Tuotannon työnjohtaja valitsee tuotantotilauksessa **Luo fyysisen varaston poiminta** -toiminnon. Fyysisen varaston poiminta-asiakirja luodaan poimimaan nimikkeitä **Manuaalinen**-, **Poiminta + taaksepäin**- ja **Poiminta + eteenpäin**-materiaalinottotavoilla. Nämä nimikkeet on asetettu tuotannon valmisteluvarastopaikkaan.  
3. Varastopäällikkö määrittää poiminnat varastotyöntekijälle.  
4. Varastotyöntekijä poimii nimikkeet soveltuvista varastopaikoista ja asettaa ne tuotannon valmisteluvarastopaikkaan tai fyysisen varastoinnin poiminnan määritettyyn varastopaikkaan. Varastopaikka voi olla tuotantosolun tai kuormitusryhmän varastopaikka.
5. Varastotyöntekijä rekisteröi poiminnan. Määrää siirretään poimintavarastopaikasta ja lisätään kulutusvarastopaikkaan. kaikkien poimittujen nimikkeiden **Poimittu määrä** -kenttä osaluettelossa on päivitetty.

    > [!NOTE]  
    >  Vain poimittu määrä voidaan kuluttaa.  
6. Koneenkäyttäjä tiedottaa tuotantojohtajaa, että loppukohdat ovat lopussa.
7. Tuotannon työnjohtaja käyttää kulutus- tai tuotantopäiväkirjaa kirjaamaan jompaakumpaa **Manuaalinen**-materiaaliottotapaa käyttävien komponentin nimikkeiden kulutuksen kirjaamiseen.
8. Tuotannon työnjohtaja käyttää tuotospäiväkirjaa tai tuotantopäiväkirjaa tuotoksen kirjaamiseen. **Poiminta + eteenpäin**- tai **Poiminta + taaksepäin** -materiaaliottomenetelmää ja reitityslinkkejä käyttävien komponentin nimikkeiden määrä vähennetään tuotannon valmisteluvarastopaikasta.
9. Tuotantopäällikkö vaihtaa tuotantotilauksen tilaksi **Valmis**. Komponentin **Taaksepäin**-materiaaliottomenetelmää käyttävien komponentin nimikkeiden määrä vähennetään avoimesta tuotannon varastopaikasta ja sellaisten **Poiminta + taaksepäin** -materiaaliottomenetelmää käyttävien komponentin nimikkeiden määrä vähennetään tuotannon valmisteluvarastopaikasta, joissa ei ole reitityslinkkiä.  

Seuraavassa kuvassa esitetään, milloin **Bin-koodi** -kenttä osaluettelossa täytetään sijainnin tai koneen/työkeskuksen asetusten mukaisesti.  

:::image type="content" source="media/binflow.png" alt-text="Yleiskatsaus Varastopaikkakoodi-kenttä täyttämisen ajankohdasta ja täyttämistavasta.":::

## <a name="make-to-order-mto-production-components-in-an-advanced-warehouse-configuration"></a>Tilausohjattujen (MTO) komponenttien materiaaliotto laajennetussa fyysisen varaston määrityksessä

Esimerkkitilanteissa, joissa tuotettu nimike koostuu raaka-aineista ja puolivalmiista nimikkeistä, joiden tuotantotapana on **tilausohjautuva**, näiden puolivalmiiden komponenttien fyysisen varastoinnin poiminta lisätään samaan tuotantotilaukseen niin, että **Suunnittelutason koodi** -kenttä on täytetty. Puolivalmiiden nimikkeiden oletetaan olevan heti kulutuksessa, eivätkä ne vaadi poimintaa, joten niitä ei sisällytetä fyysisen varastoinnin poiminta-asiakirjaan. Luodut fyysisen varastoinnin poiminnat sisältävät raaka-aineet vain tuotetun nimikkeen ja puolivalmiiden nimikkeiden osalta.

Jos varastossa on kuitenkin puolivalmiita nimikkeitä, suunnittelujärjestelmä ehdottaa nimikkeiden kulutusta koko määrän tuottamisen asemesta. Esimerkiksi tuotettu nimike vaatii viisi puolivalmista komponenttia, mutta kolme on jo varastossa. Tässä tapauksessa tuotantotilauksen komponenteissa näkyy viisi puolivalmista nimikettä, mutta vain kaksi tuotetaan samassa tuotantotilauksessa erillisenä tuotantotilausrivinä.
Tällaiset asetukset eivät ole yhteensopivia fyysisen varastoinnin poimintojen kanssa, ja tiheydestä riippuen tällaisten puolivalmiiden nimikkeiden tuotantotapa tulee muuttaa **varasto-ohjautuvaksi** tai tuotantotilauksen komponenttirivi tulee jakaa manuaalisesti silloin, kun aiemmin tuotetut puolivalmiit nimikkeet tulee poimia.


## <a name="see-also"></a>Katso myös

- [Varaston hallinta](inventory-manage-inventory.md)  
- [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
- [Kokoonpanon hallinta](assembly-assemble-items.md)  
- [Varastoinninhallinnan yleiskatsaus](design-details-warehouse-management.md)
- [Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
