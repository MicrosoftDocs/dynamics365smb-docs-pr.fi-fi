---
title: Poiminta sisäisissä toiminnoissa laajennetuissa varastomäärityksissä
description: 'Jos sijainnit käyttävät poimintaa ja toimituksia, poimi komponentteja tuotannon, kokoonpanon ja projektin toimintoja varten F.varastoinnin poiminta -sivulla.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/02/2022
ms.author: bholtorf
---
# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a><a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Tuotanto-, kokoonpano- ja projektipoiminta laajennetuissa varastointimäärityksissä

Tuotantoon, projekteihin tai koonpanotilauksiin poimittujen komponenttien hyllytystapa määräytyy sen mukaan, miten fyysinen varasto on määritetty sijaintina. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

Lähtevän virran (poiminta) laajennetuissa fyysisen varastoinnin määrityksissä **Vaadi poiminta** ja **Vaadi toimitus** otetaan käyttöön vaihtopainikkeilla sijainnin **Sijaintikortti**-sivulla.

Kun sijainti määritetään edellyttämään fyysisen varaston poiminnan ja toimituksenkäsittelyä, fyysisen varaston poiminta-asiakirjoilla voi luoda ja käsitellä poimintatietoja ennen komponenttien käytön tai kulutuksen kirjaamista.  

Fyysisen varastoinnin poiminta-asiakirjaa ei voi luoda tyhjästä. Poiminnat ovat sellaisen työnkulun osa, jossa tilausta käsittelevä henkilö luo ne push-menetelmänä tai varastotyöntekijä luo ne pull-menetelmänä:

- Push-menetelmässä käytetään **Luo poiminta** -toimintoa **Tuotantotilaus**-, **Kokoonpanotilaus**- ja **Työkortti**-sivulla. Poimittavat rivit valitaan ja poiminnat valmistellaan määrittämällä esimerkiksi, mistä varastopaikoista otetaan ja mihin asetetaan sekä kuinka monta yksikköä käsitellään. Varastopaikat on voitu määrittää valmiiksi fyysisen varaston sijainnissa tai resurssissa.
- Pull-menetelmässä **tuotantotilaus**, **kokoonpanotilaus** ja **työkortti** vapautetaan fyysiseen varastoon, jolloin nimikkeet ovat poimittavissa. Varastontyöntekijä voi sitten käyttää **Poimintatyökirja**-sivulla **Hae f. varastoinnin asiakirjat** -toimintoa määritettyjen poimintojen noutamiseen.

Lähdeasiakirjojen komponenttien poimiminen tai siirtäminen pull-menetelmällä edellyttää lähdeasiakirjan vapauttamista, jotta poimimiseen ollaan valmiita. Vapauta sisäisten toimintojen lähdeasiakirjat seuraavilla tavoilla.  

|Lähdeasiakirja|Vapautustapa|  
|---------------------|--------------------|  
|Tuotantotilaus|Tilauksen tilaksi muutetaan Vapautettu tai vaihtoehtoisesti vapautettu tuotantotilaus luodaan heti.|  
|Kokoonpanotilaus|Muuta tilaksi Vapautettu.|
|Projektit | Tilaksi vaihdetaan Avoin tai vaihtoehtoisesti luodaan heti projekti, jonka tila on Avoin.|  

## <a name="production"></a><a name="production"></a>Tuotanto

Tuotannon komponentteja voi poimia työkulussa tuotantoon **F.varastoinnin poiminta** -asiakirjojen avulla.

Jos sijainnissa käytetään varastopaikkoja nimikkeiden siirtämiseen avoimiin tuotannon varastopaikkoihin, käytettävissä on seuraavat menetelmät:

* Jos sijainnissa käytetään ohjattua hyllytystä ja poimintaa, lisätietoja on artikkelissa [Nimikkeiden siirtäminen laajennetuissa fyysisen varaston määrityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md).
* Muita sijainteja koskevia lisätietoja on artikkelissa [Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

## <a name="assembly"></a><a name="assembly"></a>Kokoonpano

Kokoonpanon komponentit voidaan siirtää kokoonpanoalueelle **F.varastoinnin poiminta** -asiakirjojen avulla.

[!INCLUDE [prod_short](includes/prod_short.md)] tukee kokoonpanovirtoja, joiden tyyppi on kokoonpanoa varastoa varten ja kokoonpano tilausten varten. Lisätietoja fyysisen varaston lähtevän virran kokoonpanosta tilausten varten on kohdassa [Kokoonpano tilausta varten -nimikkeiden käsitteleminen fyysisen varastoinnin toimituksissa](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

## <a name="project-management"></a><a name="project-management"></a>Projektinhallinta

Projektin komponentteja voi poimia työnkulussa projektinhallintaan **F.varastoinnin poiminta** -asiakirjojen avulla.

> [!NOTE]
> Projektin suunnittelurivien komponenttien poimintamahdollisuus lisättiin sovellukseen [!INCLUDE[d365fin](includes/d365fin_md.md)] vuoden 2022 2. julkaisuaallossa. Jotta ominaisuutta voi käyttää, järjestelmänvalvojan on otettava käyttöön **Ominaisuuspäivitys: Ota käyttöön varaston ja fyysisen varaston poiminnat projekteista** **Ominaisuuksien hallinta** -sivulla.
>
> Projektit eivät tue laajennettuja määrityksiä, joissa **Ohjattu poiminta ja hyllytys** on otettu vaihtopainikkeella käyttöön.

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a><a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Poiminta-asiakirjojen joukkoluonti poimintatyökirjan avulla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poimintatyökirja** ja valitse sitten vastaava linkki.  

2. Valitse **Hae f. varastoinnin asiakirjat** -toiminto.  

    Luettelo sisältää vapautetun tuotannon, projektit ja kokoonpanotilaukset, jotka siirretty poimintatoimintoon. Tilaukset sisältävät myös ne, joille poimintaohjeet on jo luotu. Tässä luettelossa ei ole asiakirjat, joiden poimintarivit on kokonaisuudessaan poimittu ja rekisteröity.  
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
    |Per asiak./toimit./sijainti|Luo erilliset poiminta-asiakirjat kullekin asiakkaalle (projekteille)|
    |Per nimike|Luo erilliset poiminta-asiakirjat kullekin nimikkeelle poimintatyökirjassa.|
    |Per lähtöalue|Luo erilliset poiminta-asiakirjat kullekin alueelle, josta nimikkeitä otetaan.|
    |Per lokero|Luo erilliset poiminta-asiakirjat kullekin varastopaikalle, josta nimikkeitä otetaan.|
    |Per eräpäivä|Luo erilliset varastopoiminta-asiakirjat lähdeasiakirjoille, joilla on sama eräpäivä.|

    Poiminta-asiakirjojen luonnin määrittäminen tekemällä valinnan seuraavista vaihtoehdoista.  

    |Asetus|Kuvaus|
    |-|-|
    |Maks. Ei. poimintarivejä|Luo poiminta-asiakirjat, joista jokaisessa on enintään määritetty määrä rivejä.|
    |Maks. Ei. poiminnan lähdeasiakirjoja|Luo poiminta-asiakirjat, jotka kattavat määritetyn määrän lähdeasiakirjoja.|
    |Määritetty käyttäjätunnus|Luo poiminta-asiakirjat vain työkirjan riveille, jotka on liitetty valittuun varastotyöntekijään.|
    |Järjestämistapa poimintariveille|Rivien lajittelu luodussa poiminta-asiakirjassa tekemällä valinnan käytettävistä olevista vaihtoehdoista.|
    |Aseta erottelusuodatin|Piilottaa poiminnan erottelurivit, kun suurempi mittayksikkö muunnetaan pienemmäksi mittayksiköksi ja poimitaan kokonaan.|
    |Älä täytä käsiteltävää määrää|Jättää **Käsiteltävä määrä** -kentän tyhjäksi luoduilla poimintariveillä.|
    |Tulosta poiminta|Tulostaa poiminta-asiakirjat, kun ne luodaan. Tulostus on mahdollista myös luoduista poiminta-asiakirjasta.|

8. Valitse **OK**-painike.  

## <a name="to-pick-items-for-a-productions-order-assembly-order-job"></a><a name="to-pick-items-for-a-productions-order-assembly-order-job"></a>Tuotantotilauksen, kokoonpanotilauksen, projektin nimikkeiden poimiminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poiminnat** ja valitse sitten vastaava linkki.  

    Jos tiettyä poimintaa on käsiteltävä, poiminta valitaan luettelosta tai määritetyt poiminnat etsitään suodattamalla luetteloa. Avaa poiminnan kortti.  
2. Jos **Määritetty käyttäjätunnus** -kenttä on tyhjä, syötä tunnus tarvittaessa itse.  
3. Poimi nimikkeet.  

    Jos fyysinen varasto on määritetty käyttämään varastopaikkoja, nimikkeen ottopaikkoja ehdotettaessa käytetään nimikkeen oletusvarastopaikkoja. Ohjeissa on ainakin kaksi erillistä otto- ja asetustoimintojen riviä.  

    Toimintoalueilla, kuten tuotannon varastopaikoissa, voi olla oletusvarastopaikka vaadituille komponenteille. Jos se on olemassa, oletusvarastopaikkakoodi lisätään fyysisen varaston poiminta-asiakirjaan osoittamaan, minne nimikkeet sijoitetaan. Lisätietoja on **Tuotannon valmisteluvarastopaikkakoodi**- **Kokoonpanoon-varastop.koodi**- ja **Projektiin-lokeron koodi** -kenttien työkaluvihjeissä.

    Jos fyysinen varasto on määritetty käyttämään ohjattua hyllytystä ja poimintaa, parhaat poimintavarastopaikat lasketaan varastopaikan luokittelun avulla. Kyseisiä varastopaikkoja ehdotetaan poimintarivillä. Ohjeissa on ainakin kaksi erillistä otto- ja asetustoimintojen riviä.  

    * Ensimmäisellä rivillä, jolla **Toiminnon tyyppi** -kentässä on **Ota**, ilmaistaan, millä poiminta-alueella nimikkeet sijaitsevat. Jos yhdellä vastaanottorivillä toimitetaan suuri määrä nimikkeitä, nimikkeet on ehkä poimittava useista varastopaikoista, joten kullakin varastopaikalla on Ota-rivi.
    * Seuraava rivi, jonka **Toiminnon tyyppi** -kentässä lukee **Aseta**, osoittaa, minne nimikkeet on asetettava fyysisessä varastossa. Tällä rivillä olevaa aluetta ja varastopaikkaa ei voi muuttaa.

    > [!NOTE]
    > Jos yhden rivin nimikkeet on poimittava useasta varastopaikasta tai asetettava useaan varastopaikkaan esimerkiksi siksi, että määritetty varastopaikka on täynnä, käytä **Rivit**-pikavälilehden **Jaa rivi** -toimintoa. Toiminto luo rivin jäljellä olevalle käsiteltävälle määrälle.

4. Kun nimikkeet on poimittu ja asetettu tuotanto-, kokoonpano- tai projektialueelle taikka -varastopaikkaan, valitse **Rekisteröi poiminta** -toiminto.  

    Nimikkeet voidaan nyt tuoda kyseiselle alueelle ja poimittujen komponenttien käyttö tai kulutus voidaan kirjata kirjaamalla kulutuspäiväkirja, kokoonpanotilaus tai projektipäiväkirja. Seuraavissa artikkeleissa on lisätietoja:

    * [Yhden vapautetun tuotantotilausrivin kulutuksen ja tuotoksen rekisteröiminen](production-how-to-register-consumption-and-output.md)
    * [Kokoa nimikkeet](assembly-how-to-assemble-items.md)
    * [Projektien kulutuksen tai käytön kirjaaminen](projects-how-record-job-usage.md)

## <a name="flushing-production-components-in-a-advanced-warehouse-configuration"></a><a name="flushing-production-components-in-a-advanced-warehouse-configuration"></a>Tuotannon komponenttien materiaaliotto laajennetussa fyysisen varaston määrityksessä

Materiaaliottotavat vaikuttavat komponenttien siirtymiseen tuotantoon. Lisätietoja on kohdassa [Komponenttien materiaalinotto toiminnan tuotoksen mukaan](production-how-to-flush-components-according-to-operation-output.md). Valitun materiaaliottotavan mukaan komponentteja voi poimia tuotantoon seuraavilla tavoilla:

* Käyttämällä **F.varastoinnin poiminta** -asiakirjaa **Manuaalinen**-materiaaliottotapaa käyttävien nimikkeiden poiminnan kirjaamiseen. Kulutus on rekisteröitävä erikseen. Lisätietoja on kohdassa [Tuotannon kulutuksen eräkirjaus](production-how-to-post-consumption.md).
* Käyttämällä **F.varastoinnin poiminta** -asiakirjaa **Poiminta + eteenpäin**- tai **Poiminta + taaksepäin** -materiaaliottotapaa käyttävien nimikkeiden poiminnan kirjaamiseen. Komponentteja kulutetaan automaattisesti, joko muutettaessa tuotantotilauksen tilaa taikka aloitettaessa tai lopetettaessa työvaihetta. Kaikkien pakollisten komponenttien on oltava saatavana. Muutoin kyseisen komponentin materiaalinoton kirjaus lopetetaan.
* Käyttämällä **F. var. siirto** -asiakirjaa viittaamatta lähdeasiakirjaan tai kirjaamalla muulla tavoin **Eteenpäin**- tai **Taaksepäin**-materiaaliottotapaa käyttävien komponenttien varaston siirrot. Komponentteja kulutetaan automaattisesti, joko muutettaessa tuotantotilauksen tilaa taikka aloitettaessa tai lopetettaessa työvaihetta. Kaikkien pakollisten komponenttien on oltava saatavana. Muutoin kyseisen komponentin materiaalinoton kirjaus lopetetaan. Lisätietoja on kohdassa [Nimikkeiden siirtäminen](warehouse-move-items.md).

### <a name="example"></a><a name="example"></a>Esimerkki

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

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Varastonhallinnan yleiskatsaus](design-details-warehouse-management.md)
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
