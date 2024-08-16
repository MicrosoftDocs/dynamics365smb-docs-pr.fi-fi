---
title: ALV-raporttien lähettäminen veroviranomaisille
description: 'Tutustu, miten voit laatia raportteja, joissa on luettelo tietyn jakson myynneistä tai myynneistä ja ostoista, sekä lähettää raportti veroviranomaisille.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'VAT, tax, report, EC sales list, statement'
ms.search.form: '321, 322, 323, 474, 475, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 9401'
ms.date: 08/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="report-vat-to-tax-authorities"></a>ALV:n raportointi veroviranomaisille

Tässä artikkelissa kuvataan raportit [!INCLUDE[prod_short](includes/prod_short.md)] , joiden avulla voit lähettää tietoa arvonlisäverosummista (ALV) myyntien ja ostojen osalta alueesi veroviranomaisille. Tietyn maan/alueen mukaan raportit voivat sisältää tiettyjä tietoja tai lähetettävien lisäraporttien tietoja. Tarkista oman maasi tai alueesi artikkelit [Paikalliset toiminnot](about-localization.md) -osasta.  

Käytössä ovat seuraavat sisäiset raportit:

* **EU-myyntiluettelo**-raportti  

    Euroopan unionin (EU:n) myyntiluettelo sisältää arvolisävero- eli ALV-summat, jotka olet kerännyt EU-maissa tai -alueilla sijaitseville ALV-rekisteröidyille asiakkaille suuntautuneesta myynnistä.  
* **VAT-palautus**-raportti  

    ALV-palautusraportti sisältää asiakkaille suuntautuneen myynnin ja toimittajilta tehtyjen ostojen ALV:n arvonlisäveroa käyttävissä maissa ja sitä käyttävillä alueilla.  

Molemmissa tapauksissa (kuten muissakin ALV:hen liittyvissä raporteissa) ALV lasketaan määritettyjen ALV-kirjausasetusten ja ALV-kirjausryhmien perusteella. [!INCLUDE[prod_short](includes/prod_short.md)] näyttää ALV-tapahtumat aina niiden **ALV-päivämäärän** perusteella ensisijaisena raportointipäivänä.  

> [!NOTE]
> Kaikki ALV-liittyvät raportit suoritetaan nyt käyttämällä **ALV-päivämäärää** asianmukaisten tietueiden suodattamiseen. Vaikka määrität **ALV-päivämäärän käytön** arvoksi **älä käytä ALV-päivämäärätoimintoa**, [!INCLUDE[prod_short](includes/prod_short.md)]-ohjelma piilottaa kaikki **ALV-päivämäärän** esiintymät sovelluksessa. **ALV-päivämäärää** käytetään kuitenkin edelleen kaikissa raportointikohteissa, ja se täytetään automaattisesti **kirjauspäivämäärällä**.

Jos haluat tarkastella täydellistä ALV-tapahtumahistoriaa, jokainen ALV:n sisältävä kirjaus luo tapahtuman **ALV-tapahtumat**-sivulla. Näitä tapahtumia käytetään laskettaessa ALV-laskelmasi summaa (maksu tai palautus) tietyltä kaudelta. ALV-tapahtumat nähdäksesi valitse ![Lamppu, joka avaa toisena Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-tapahtumat** ja valitse sitten vastaava linkki.

> [!NOTE]
> Jokaisen [!INCLUDE[prod_short](includes/prod_short.md)] -ympäristön on tarkoitus käsitellä yhden maan tai alueen lakisääteinen raportointi. Esimerkiksi [!INCLUDE[prod_short](includes/prod_short.md)]in hollantilainen versio käsittelee vain Alankomaiden ALV-raportointia, ei muiden maiden tai alueiden raportointia. Vastaavasti Yhdysvaltain [!INCLUDE[prod_short](includes/prod_short.md)]in versio käsittelee 1099-raportointia Yhdysvalloissa, eikä se tue ALV-raportointia muissa maissa tai muilla alueilla, ellei sitä ole tuotu kumppaniekosysteemin laajennuksella tai asiakaskohtaisella koodimuokkauksella.

## <a name="about-the-ec-sales-list-report"></a><a name="ecsaleslist"></a>Tietoja EU-myyntiluettelon raportista

Euroopan unionissa (EU) ja Yhdistyneessä kuningaskunnassa kaikkien tavaroita ja palveluja ALV-rekisteröidyille asiakkaille, myös muiden EU-maiden tai -alueiden asiakkaille, myyvien yritysten on lähetettävä EU-myyntiluettelo-raportin sähköinen versio tulli- ja veroviranomaisilleen. **EU-myyntiluettelo**-raportti toimii vain EU-maiden ja -alueiden kohdalla.

Raportti sisältää yhden rivin kullekin asiakastapahtumalle ja näyttää kokonaissumman tietyntyyppisille tapahtumille. Raportti voi sisältää kolmentyyppisiä tapahtumia:  

* B2B-tuotteet  
* B2B-palvelut  
* B2B-kolmikantakaupan tuotteet  

*B2B*-tuotteet ja -palvelut määrittävät, onko kyse myydystä tavarasta tai palvelusta, jota voi hallita ALV-kirjausasetusten **EU-palvelu**-asetuksella. *B2B-kolmikantakaupan* tuotteet ilmaisevat, onko kyse kaupankäynnistä kolmannen osapuolen kanssa, jolloin niitä voi hallita myyntiasiakirjojen, kuten myyntitilausten, laskujen ja hyvityslaskujen, **EU-kolmikantakauppa**-asetuksella.  

Kun veroviranomainen on tarkistanut raporttisi, hän lähettää sähköpostia yrityksesi yhteyshenkilölle. [!INCLUDE[prod_short](includes/prod_short.md)]issa yhteyshenkilö määritetään **Yritystiedot**-sivulla. Ennen kuin lähetät raportin, varmista, että olet valinnut yhteyshenkilön.  

### <a name="submit-an-ec-sales-list-report"></a>Lähetä EU-myyntiluettelon raportti

[!INCLUDE [finance-ecsaleslist](includes/finance-ecsaleslist.md)]

## <a name="about-the-vat-return-report"></a><a name="vatreturn"></a>Tietoja ALV-palautusraportista

Voit lähettää tällä raportilla osto- ja myyntiasiakirjoissa olevan ALV:n. Näitä asiakirjoja ovat esimerkiksi osto- ja myyntitilaukset, laskut ja hyvityslaskut. Tiedot ovat raportissa samassa muodossa kuin tulli- ja veroviranomaisille tehtävässä yhteenvetoilmoituksessa.  

Tapahtumat voidaan määrittää sisältämään ALV-palautuksia varten seuraavat tiedot:

* Lähetä vain avoimet tapahtumat tai avoimet ja suljetut tapahtumat. Tämä on kätevää esimerkiksi silloin, kun valmistelet lopullista vuositason ALV-palautusta.
* Lähetä vain määritettyjen kausien tapahtumat tai sisällytä myös edellisten kausien tapahtumat. Tämä on kätevää päivitettäessä jo lähetettyä ALV-palautusta, jos esimerkiksi toimittaa lähettää laskun myöhässä.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Veroviranomaisen verkkopalveluun yhdistäminen
[!INCLUDE[prod_short](includes/prod_short.md)] sisältää palveluyhteyden veroviranomaisten sivustoihin. Jos toimit esimerkiksi Isossa-Britanniassa, voit ottaa käyttöön **GovTalk**-palveluyhteyden, jonka kautta voit lähettää EU-myyntiluettelo- ja ALV-palautus-raportit sähköisessä muodossa. Jos haluat lähettää raportin manuaalisesti esimerkiksi syöttämällä tietosi veroviranomaisen verkkosivuille, sitä ei tarvita.   

Jotta voisit ilmoittaa arvonlisäveron viranomaiselle sähköisesti, [!INCLUDE[prod_short](includes/prod_short.md)] on yhdistettävä veroviranomaisen verkkopalveluun. Tämä edellyttää, että luot tilin ALV-viranomaisen kanssa. Kun sinulla on tili, voit ottaa käyttöön [!INCLUDE[prod_short](includes/prod_short.md)]issa tarjotun palveluyhteyden.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Palveluyhteydet** ja valitse sitten sopiva linkki.
2. Täytä vaaditut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > Yhteyden toimivuus kannattaa testata. Sen voi tehdä valitsemalla **Testitila**-valintaruudun sekä valmistelemalla ja lähettämällä ALV-raportin kohdassa [ALV-raportin valmisteleminen ja lähettäminen](#to-prepare-and-submit-a-vat-report) kuvatulla tavalla. Palvelu testaa testitilassa, voiko veroviranomainen vastaanottaa raportin. Raportin tila ilmaisee, onnistuiko testilähetys vai ei. Muista kuitenkin, että tietoja ei ole vielä oikeasti lähetetty. Kun haluat lähettää raportin oikeasti, poista **Testitila**-valintaruudun valinta ja toista sitten lähetysprosessi.

## <a name="to-set-up-vat-reports-in-"></a>ALV-raporttien määrittäminen [!INCLUDE[prod_short](includes/prod_short.md)]issa

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

### <a name="to-set-up-vat-return-periods"></a>ALV-palautusjaksojen määrittäminen

Vaihtoehtoisesti, jos liiketoimintasi ei sijaitse Isossa-Britanniassa, käytä **ALV-palautusjaksot -sivua määrittääksesi ajoitetut ALV-palautukset** . Jos liiketoimintasi sijaitsee Isossa-Britanniassa, katso [Tax Digital -ohjelman tekeminen Isossa-Britanniassa](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md).  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-palautusjaksot** ja valitse sitten vastaava linkki.  
2. Määritä ensimmäinen jakso täyttämällä **ALV-palautusjaksot**-sivun kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)].  
3. Toista vaihe 2 kaikkien niiden kausien osalta, jotka haluat lisätä.  

Kun sitten on aika lähettää ALV-palautusjakson ALV-raportti, valitse jakso **ALV-palautusjaksot**-sivulla ja valitse sitten toiminto **Luo ALV-palautus**. Valitse sitten **ALV-palautus**-kortissa toiminto **Ehdota rivejä** seuraavan menettelyn kolmannessa vaiheessa kuvatulla tavalla.  

## <a name="to-prepare-and-submit-a-vat-report"></a>ALV-raportin valmisteleminen ja lähettäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, syötä **EU-myyntiluettelo** tai **ALV-palautus** ja valitse linkit.  
2. Valitse **Uusi** ja täytä sitten tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit luoda raportin sisällön **Ehdota rivejä** -toiminnolla.  

    > [!NOTE]  
    >  Voit tarkastella EU-myyntiluettelo-raportin riveillä olevia tapahtumia ennen raportin lähettämistä. Valitse ensin rivi ja valitse sitten **Näytä ALV-tapahtumat**-toiminto.  

4. Voit tarkistaa ja valmistella raportin lähetystä varten valitsemalla **Vapauta**-toiminnon.  

    > [!NOTE]  
    > [!INCLUDE[prod_short](includes/prod_short.md)] vahvistaa, että raportti on määritetty oikein. Jos tarkistus epäonnistuu, virheet näkyvät **Virheet ja varoitukset** -kohdassa ja voit tehdä näiden tietojen perusteella tarvittavat korjaukset. Jos kyse on [!INCLUDE[prod_short](includes/prod_short.md)]in puuttuvasta asetuksesta, voit yleensä avata korjaukseen tarvittavat tiedot sisältävän sivun napsauttamalla sanomaa.  
5. Raportin voit lähettää **Lähetä** -toiminnolla.  

Kun lähetät raportin, [!INCLUDE[prod_short](includes/prod_short.md)] valvoo palvelua ja pitää kirjaa yhteydenpidosta. **Tila**-kenttä ilmaisee raportin kulun prosessissa. Kun viranomainen on esimerkiksi käsitellyt raporttisi, sen tilaksi tulee **Onnistui**. Jos veroviranomaiselle lähetetyssä raportissa on virheitä, sen tilaksi muutetaan **Epäonnistui**. Voit tarkastella virheitä **Virheet ja varoitukset** -kohdassa, korjata virheet ja lähettää raportin uudelleen. Voit tarkastella luetteloa kaikista EY-myyntiluetteloraporteistasi **EU-myyntiluetteloraportit**-sivulla.  

### <a name="vat-return-statuses"></a>ALV-palautusten tilat

ALV-palautuksilla voi olla eri tiloja seuraavassa taulukossa kuvatulla tavalla.

| Tila | Kuvaus |
|------------|-------------------------|
| Avoin | Kun luot uuden ALV-palautuksen. Voit suorittaa **Ehdota rivejä** -toiminnon. Jos sinun täytyy korjata arvoja, voit suorittaa **Ehdota rivejä** -toiminnon uudelleen. Et voi lähettää ALV-palautusta, jolla on tämä tila. |
| Vapautettu | Tila muuttuu, kun käytät **vapautus**-toimintoa. [!INCLUDE[prod_short](includes/prod_short.md)] näyttää **Virheet ja varoitukset** -pikavälilehden. Et voi tehdä muutoksia tai käyttää **Ehdota rivejä** -toimintoa. Jos haluat tehdä muutoksia, sinun on avattava ALV-palautus uudelleen. |
| Hylätty | Jos lähetys ei onnistunut (esimerkiksi käyttöoikeuksien tarkistus epäonnistui), tilaksi **vaihtuu Hylätty**. Et voi avata uudelleen ALV-palautusta, jolla on tämä tila. |
| Lähetetty | ALV-palautus lähetetään **Lähetä**-toiminnon avulla, tai se merkitään lähetetyksi käyttämällä **merkitse vastaanotetuksi** -toimintoa. |
| Hyväksytty | ALV-palautuksen tila on tämä, jos raportti on merkitty hyväksytyksi Merkitse hyväksytyksi **-** toiminnon avulla. Jos **ALV-palautus**-raportti on merkitty **hyväksytyksi**, voit suorittaa **Laske ja kirjaa ALV-laskelma** -toiminnon. |

## <a name="viewing-communications-with-your-tax-authority"></a>Veroviranomaisen ja yrityksen välisen viestintähistorian tarkastelu

Joissakin maissa ja joillakin alueilla tapahtuu viestinvaihtoa veroviranomaiselle raporttien lähettämisen yhteydessä. Näet ensimmäisen ja viimeisen lähettämäsi tai vastaanottamasi sanoman valitsemalla **Lataa lähetysviesti** ja **Lataa vastausviesti** -toiminnon.  

## <a name="submitting-vat-reports-manually"></a>ALV-raporttien lähettäminen manuaalisesti
Jos raportti lähetetään jollakin muulla tavalla, esimerkiksi viemällä se XML-tiedostoksi ja lataamalla sen veroviranomaisen verkkosivulle, raportointikauden voi sulkea sen jälkeen valitsemalla **Merkitse lähetetyksi**. Kun olet merkinnyt ALV-raportin vapautetuksi, siitä tulee ei muokattava. Jos raporttia on muutettava sen jälkeen, kun se on merkitty vapautetuksi, raportti on ensin avattava uudelleen.

## <a name="vat-settlement"></a>ALV-laskelma
Netto-ALV on jaksoittain maksettava veroviranomaisille. Jos ALV on laskettava usein, voit suorittaa **Laske ja kirjaa ALV-laskelma** -eräajon, joka sulkee avoimet ALV-tapahtumat ja siirtää ostojen ja myynnin ALV-summat ALV-maksutilille.

Kun siirrät ALV-summat maksutilille, ostojen ALV-tilille hyvitetään ja myyntien ALV-tililtä veloitetaan ne summat, jotka on laskettu määritetylle ajalle. Nettosumma hyvitetään (tai veloitetaan, jos ostojen ALV-summa on suurempi) ALV-maksutilille. Voit kirjata maksun välittömästi tai tulostaa ensin testiraportin.  

> [!Note]
> Kun suoritat **Laske ja kirjaa ALV-laskelma** -eräajon mutta et määritä **Liiketoiminnan ALV-kirjausryhmä**- ja **Tuotteen ALV-kirjausryhmä** -asetuksia, kaikkien liiketoiminnan kirjausryhmien ja tuotteen kirjausryhmien koodien tapahtumat sisällytetään.

## <a name="configuring-your-own-vat-reports"></a>Omien ALV-raporttien määrittäminen

Voit käyttää valmista **EU-myyntiluetteloa**. Voit kuitenkin myös luoda omia raportteja, jos sinulla on kehityslisenssi, jonka avulla voit luoda codeuniteja. Ohjeita saat tarvittaessa Microsoft-kumppanilta.  

Seuraavassa taulukossa kuvataan codeunitit, jotka sinun on luotava raporttiasi varten.  

| Codeunit | Mitä raportin on tehtävä |
|----|-----|
|Ehdota rivejä| Hakea tiedot **ALV-tapahtumat**-taulukosta ja näytettävä ne riveinä ALV-raportilla.|
|Sisältö | Hallittava raportin muotoa. On kyse esimerkiksi XML- tai JSON-tiedostosta. Muoto, jota käytetään riippuu veroviranomaisesi verkkopalvelun vaatimuksista. |
|Lähettäminen | Määrittää miten ja milloin ALV-raportti lähetetään veroviranomaisten vaatimusten mukaisesti. |
|Vastauksen käsittelijä | Veroviranomaisen vastauksen käsittely. Viranomainen voi esimerkiksi lähettää sähköpostin yrityksesi yhteyshenkilölle. |
|Peruuta | Aiemmin veroviranomaiselle lähetetyn ALV-raportin peruutussanoman lähettäminen. |  

> [!Note]
> Kiinnitä huomiota raportin koodiyksiköitä luodessasi **ALV-raportin versio** -kentän arvoon. Tässä kentässä on oltava sama versio, joka on tai oli veroviranomaisen vaatimuksena. Voit esimerkiksi kirjoittaa kentän arvoksi **2021** osoittamaan, että raportti noudattaa kyseisenä vuonna voimassa olleita vaatimuksia. Voimassa olevan version saat selville veroviranomaiseltasi.  

## <a name="see-also"></a>Katso myös

[Arvonlisäveron laskelmien ja kirjaustapojen määrittäminen](finance-setup-vat.md)    
[Myynnin ja ostojen ALV:n käsitteleminen](finance-work-with-vat.md)    
[Myynnin määrittäminen](sales-setup-sales.md)    
[Myynnin laskutus](sales-how-invoice-sales.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
