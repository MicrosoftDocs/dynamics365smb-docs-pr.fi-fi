---
title: Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten
description: Tietoja fyysisen varaston poiminta-asiakirjojen käyttämisestä poimintatietojen luomista ja käsittelyä varten ennen fyysisen varaston toimituksen kirjaamista.
author: bholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '7335, 7339, 7345,'
---
# <a name="pick-items-for-warehouse-shipment"></a><a name="pick-items-for-warehouse-shipment"></a><a name="pick-items-for-warehouse-shipment"></a>Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten

[!INCLUDE[prod_short](includes/prod_short.md)]issa nimikkeet poimintaan ja toimitukseen on käytettävissä neljä tapaa, jotka käsitellään seuraavassa taulukossa.

|Tapa|Lähtevien käsittely|Vaadi poiminta|Vaadi toimitus|Monimutkaisuustaso (lisätietoja on kohdassa [Varastoinninhallinnan yleiskatsaus](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Poiminnan ja toimituksen kirjaaminen tilausriviltä|||Ei määritettyä fyysisen varaston toimintaa.|  
|B|Poiminnan ja toimituksen kirjaaminen varaston poiminta-asiakirjasta|Otettu käyttöön||Perus: tilauksittain.|  
|S|Poiminnan ja toimituksen kirjaaminen fyysisen varastoinnin toimitusasiakirjasta||Otettu käyttöön|Perus: useiden tilausten konsolidoitu vastaanoton ja toimituksen kirjaus.|  
|P|Poiminnan kirjaaminen fyysisen varastoinnin poiminta-asiakirjasta ja toimituksen kirjaaminen fyysisen varastoinnin toimitusasiakirjasta|Otettu käyttöön|Otettu käyttöön|Lisäasetukset|  

Lisätietoja on kohdassa [Fyysisen varaston lähtevä työnkulku](design-details-outbound-warehouse-flow.md).

Tässä artikkelissa viitataan taulukon menetelmään D. Lisätietoja nimikkeiden toimittamisesta on kohdassa [Nimikkeiden toimittaminen](warehouse-how-ship-items.md).

Jos fyysisen varastoinnin poiminnan käsittely ja fyysisen varastoinnin toimituksen käsittely on määritetty sijainnissa pakolliseksi, fyysisen varaston poiminta-asiakirjojen avulla voidaan ja käsitellä poimintatietoja ennen fyysisen varastoinnin toimituksen kirjaamista.  

Fyysisen varastoinnin poiminta-asiakirjaa ei voi luoda tyhjästä. Poiminnat ovat sellaisen työnkulun osa, jossa tilausta käsittelevä henkilö luo ne push-menetelmänä tai varastotyöntekijä luo ne pull-menetelmänä:

- Push-menetelmässä käytetään **Luo poiminta** -toimintoa **Fyysisen varaston toimitus** -sivulla. Poimittavat rivit valitaan ja poiminnat valmistellaan määrittämällä esimerkiksi, mistä varastopaikoista otetaan ja mihin asetetaan sekä kuinka monta yksikköä käsitellään. Varastopaikat on voitu määrittää valmiiksi fyysisen varaston sijainnissa tai resurssissa.
- Pull-menetelmässä käytetään **Fyysisen varaston toimitus** -sivun **Vapauta**-toimintoa mahdollistamaan nimikkeiden hyllytys. Varastontyöntekijä voi sitten käyttää **Poimintatyökirja**-sivulla **Hae f. varastoinnin asiakirjat** -toimintoa määritettyjen poimintojen noutamiseen.

> [!NOTE]  
> Poiminta myyntitilausta varten kokoonpantujen nimikkeiden fyysisen varastoinnin toimitukseen tehdään samoin kuin tavallisissa fyysisen varastoinnin poiminnoissa toimitusta varten, mitä on käsitelty tässä artikkelissa. Toimitettavaa määrää varten poimittavien rivien määrä voi kuitenkin olla monta yhteen, koska poimittavana on komponentteja eikä kokoonpantu nimike.  
>
> Fyysisen varastoinnin poimintarivit luodaan kokoonpanotilauksen **Jäljellä oleva määrä** -kentässä olevalle arvolle; kyseinen kokoonpanotilaus on linkitetty toimitettavaan myyntitilausriviin. Kaikki komponentit kerätään yhtenä toimintona. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden käsitteleminen fyysisen varastoinnin toimituksissa](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).  
>  
> Lisätietoja kokoonpanotilausten komponenttien poiminnasta, mukaan lukien tilanteissa, joissa kokoonpanon nimikkeet eivät liity myyntitoimitukseen, on kohdassa [Poiminta tuotantoon, kokoonpanoon tai projekteihin fyysisen varastoinnin laajennetuissa määrityksissä](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a><a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a><a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Poiminta-asiakirjojen joukkoluonti poimintatyökirjan avulla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poimintatyökirja** ja valitse sitten vastaava linkki.  

2. Valitse **Hae f. varastoinnin asiakirjat** -toiminto.  

    Luettelo sisältää kaikki toimitukset, jotka on vapautettu poimintaan. Tämä koskee myös poimintoja, joiden poimintaohjeet on jo luotu. Tässä luettelossa ei ole asiakirjoja, joiden poimintarivit on kokonaisuudessaan poimittu ja rekisteröity.  
3. Valitse toimitukset, joille haluat valmistella poiminnan.

    > [!NOTE]  
    >  Jos sellainen toimitus- tai poiminta-asiakirja yritetään valita, jonka kaikille riveillä on jo luotu ohjeet, avautuva sanoma ilmoittaa, ettei mitään käsiteltävää ole. Jo luotujen fyysisen varastoinnin poimintaohjeiden yhdistäminen yhdeksi poimintaohjeeksi edellyttää, että fyysisen varastoinnin yksittäiset poiminnat poistetaan ensin.

4. Järjestä rivit täyttämällä **Järjestämistapa**-kenttä.  

    > [!NOTE]  
    >  Rivien lajittelu työkirjassa ei automaattisesti toteudu samanlaisena poimintaohjeessa. Käytössä on kuitenkin samat järjestämis- ja varastopaikan luokittelumahdollisuudet. Työkirjassa suunnittu rivijärjestys on helppo luoda uudelleen poimintaohjeita luotaessa tai niitä järjestettäessä.

5. Täytä **Käsiteltävä määrä** -kenttä joko manuaalisesti ja käyttämällä **Täytä autom. käsitelt. määrä** -toiminto.  

    Sivulla näkyy määrät, jotka ovat saatavana laiturointivarastopaikoissa. Näistä tiedoista on hyötyä suunniteltaessa työtehtäviä laiturointitilanteissa. [!INCLUDE[prod_short](includes/prod_short.md)] ehdottaa aina ensin poimimista laiturointivarastopaikasta.
6. Rivejä voi tarvittaessa muokata. Poimintaa voi tehostaa myös poistamalla rivejä. Jos esimerkiksi useilla riveillä on nimikkeitä, joita ovat laiturointivarastopaikoissa, kaikkien rivien poiminta voidaan luoda. Laituroidut nimikkeet toimitetaan muiden toimituksessa olevien nimikkeiden kanssa, ja tällä tavoin laiturointivarastopaikkoihin tulee tilaa uusille saapuville nimikkeille.  

    > [!NOTE]  
    >  Poistettavat rivit poistetaan vain työkirjasta. Niitä ei poisteta poiminnan valintaluettelosta.  

7. Valitse **Luo poiminta** -toiminto. **Luo poiminta** -sivu avautuu, ja luotavaan poimintaan voidaan lisätä muita tietoja. Poimintarivien yhdistäminen määritetään valitsemalla jokin seuraavista vaihtoehdoista.  

    |Asetus|Kuvaus|
    |-|-|
    |Per f.var. Asiakirja|Luo erilliset poiminta-asiakirjat työkirjan riveille, joilla on sama varastolähdeasiakirja.|
    |Per asiak./toimit./sijainti|Luo erilliset poiminta-asiakirjat kullekin asiakkaalle (myyntitilaukset), toimittajalle (ostopalautustilaukset) ja sijainnille (siirtotilaukset).|
    |Per nimike|Luo erilliset poiminta-asiakirjat kullekin nimikkeelle poimintatyökirjassa.|
    |Per lähtöalue|Luo erilliset poiminta-asiakirjat kullekin alueelle, josta nimikkeitä otetaan.|
    |Per lokero|Luo erilliset poiminta-asiakirjat kullekin varastopaikalle, josta nimikkeitä otetaan.|
    |Per eräpäivä|Luo erilliset varastopoiminta-asiakirjat lähdeasiakirjoille, joilla on sama eräpäivä.|

    Määrittää, miten poimintarivit luodaan tekemällä valinta seuraavista vaihtoehdoista.

    |Asetus|Kuvaus|
    |-|-|
    |Maks. Ei. poimintarivejä|Luo poiminta-asiakirjat, joista jokaisessa on enintään määritetty määrä rivejä.|
    |Maks. Ei. poiminnan lähdeasiakirjoja|Luo poiminta-asiakirjat, joista jokainen kattaa enintään määritetyn määrän lähdeasiakirjoja.|
    |Määritetty käyttäjätunnus|Luo poiminta-asiakirjat vain työkirjan riveille, jotka on liitetty valittuun varastotyöntekijään.|
    |Järjestämistapa poimintariveille|Rivien lajittelu luodussa poiminta-asiakirjassa tekemällä valinnan käytettävistä olevista vaihtoehdoista.|
    |Aseta erottelusuodatin|Piilottaa poiminnan erottelurivit, kun suurempi mittayksikkö muunnetaan pienemmäksi mittayksiköksi ja poimitaan kokonaan.|
    |Älä täytä käsiteltävää määrää|Jättää luotavien poimintarivien Käsiteltävä määrä -kentän tyhjäksi.|
    |Tulosta poiminta|Tulostaa poiminta-asiakirjat, kun ne luodaan. Tulostus on mahdollista myös luoduista poiminta-asiakirjasta.|

8. Valitse **OK**. [!INCLUDE [prod_short](includes/prod_short.md)] luo valintojen mukaisen poiminnan.  

## <a name="to-pick-items-for-a-warehouse-shipment"></a><a name="to-pick-items-for-a-warehouse-shipment"></a><a name="to-pick-items-for-a-warehouse-shipment"></a>Fyysisen varastoinnin toimituksen nimikkeiden poimiminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston poiminnat** ja valitse sitten vastaava linkki.  

    Jos sinun pitää käsitellä tiettyä poimintaa, valitse poiminta luettelosta tai etsi sinulle määritetyt poiminnat suodattamalla luetteloa. Avaa poiminnan kortti.  
2. Jos **Määritetty käyttäjätunnus** -kenttä on tyhjä, syötä tunnus tarvittaessa itse.  
3. Poimi nimikkeet.  

    Jos fyysinen varasto on määritetty käyttämään varastopaikkoja, nimikkeen ottopaikkoja ehdotettaessa käytetään nimikkeen oletusvarastopaikkoja. Ohjeissa on ainakin kaksi erillistä otto- ja asetustoimintojen riviä.  

    Jos fyysinen varasto on määritetty käyttämään ohjattua hyllytystä ja poimintaa, parhaat poiminnan varastopaikat lasketaan varastopaikan luokittelun avulla. Kyseisiä varastopaikkoja ehdotetaan poimintarivillä. Ohjeissa on ainakin kaksi erillistä otto- ja asetustoimintojen riviä.  

    * Ensimmäisellä rivillä, jolla **Toiminnon tyyppi** -kentässä on **Ota**, ilmaistaan, millä poiminta-alueella nimikkeet sijaitsevat. Jos yhdellä vastaanottorivillä toimitetaan suuri määrä nimikkeitä, nimikkeet on ehkä poimittava useista varastopaikoista, joten kullakin varastopaikalla on Ota-rivi.
    * Seuraava rivi, jonka **Toiminnon tyyppi** -kentässä lukee **Aseta**, osoittaa, minne nimikkeet on asetettava fyysisessä varastossa. Tällä rivillä olevaa aluetta ja varastopaikkaa ei voi muuttaa.

    > [!NOTE]
    > Jos yhden rivin nimikkeet on poimittava useasta varastopaikasta tai asetettava useaan varastopaikkaan esimerkiksi siksi, että määritetty varastopaikka on täynnä, käytä **Rivit**-pikavälilehden **Jaa rivi** -toimintoa. Toiminto luo rivin jäljellä olevalle käsiteltävälle määrälle.

4. Kun nimikkeet on poimittu ja asetettu toimitusalueelle tai toimituksen varastopaikkaan, valitse **Rekisteröi poiminta** -toiminto.  

Nimikkeet voidaan nyt tuoda toimitusalueelle ja toimitus voidaan kirjata, mukaan lukien liittyvä lähdeasiakirja, **F.var. toimitus** -sivulla. Lisätietoja on kohdassa [Nimikkeiden toimittaminen](warehouse-how-ship-items.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/pick-ship-items-warehouse/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
