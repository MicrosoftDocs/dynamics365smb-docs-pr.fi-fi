---
title: Valuutan vaihtokurssien päivittäminen
description: Seuraa summia eri valuutoissa valuuttakoodeja käyttäen ja anna Business Centralin auttaa sinua säätämään FX-vaihtokursseja julkaistuille merkinnöille ulkoisen palvelun avulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: multiple currencies, adjust exchange rates, FX rates
ms.date: 07/23/2021
ms.author: edupont
ms.openlocfilehash: 44dd13f986098283d29e58d3e8c4ce0218b4a083
ms.sourcegitcommit: 41876b559872fe7adbfa5b59a6e1a71dc907fb15
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/14/2021
ms.locfileid: "7921056"
---
# <a name="update-currency-exchange-rates"></a>Valuutan vaihtokurssien päivittäminen

Yritysten toimiessa yhä useammassa maassa tai alueella niiden on välttämätöntä pystyä tekemään kauppaa ja raportoimaan taloustiedot useissa valuutoissa. Paikallinen valuutta (PVA) määritetään **Pääkirjanpidon asetukset-** -sivulla kuten artikkelissa [Taloustietojen asetukset](finance-setup-finance.md) kuvataan. Kun paikallinen valuutta (PVA) on määritetty, se esitetään tyhjänä valuuttana, joten kun **Valuutta**-kenttä on tyhjä, se tarkoittaa, että valuutta on PVA.  

Seuraavaksi sinun täytyy määrittää valuuttakoodit jokaiselle valuutalle, jota käytät, jos ostat tai myyt muussa valuutassa kuin paikallisessa valuutassa (PVA). Myös pankkitilit voidaan luoda käyttämällä valuuttoja. Pääkirjanpidon tapahtumia voi tallentaa eri valuutoissa, mutta pääkirjanpidon tapahtuma kirjataan aina paikallisessa valuutassa (PVA).

> [!Important]
> Älä luo paikallisen valuutan koodia sekä **Pääkirjanpidon asetukset**- että **Valuutat**-sivulle. Tämä aiheuttaa sekaannusta valuuttataulukon tyhjän valuutan ja PVA-koodin välillä. Pankkitilejä, asiakkaita tai toimittajia saatetaan vahingossa luoda, ja niille voi tulla tyhjiä valuuttoja tai PVA-koodeja.

Pääkirjanpito määritetään käyttämään paikallista valuuttaa (PVA), mutta voit määrittää sen käyttämään myös toista valuuttaa, jolle määritetään ajantasainen vaihtokurssi. Kun toinen valuutta määritetään niin sanotuksi lisäraportointivaluutaksi, [!INCLUDE[prod_short](includes/prod_short.md)] tallentaa summat automaattisesti sekä PVA:na että lisäraportointivaluuttana kuhunkin KP-tapahtumaan sekä muihin tapahtumiin, kuten ALV-tapahtumiin. Lisätietoja on kohdassa [Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md). Lisäraportointivaluuttaa käytetään useimmiten taloudelliseen raportointiin omistajille, jotka asuvat muita kuin paikallista valuuttaa (PVA) käyttävissä maissa tai alueilla.  

> [!IMPORTANT]
> Jos haluat käyttää lisäraportointivaluuttaa taloudellisessa raportoinnissa, varmista, että ymmärrät rajoitukset. Lisätietoja on kohdassa [Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md).

## <a name="currencies"></a>Valuutat

> [!NOTE]  
> Jos etsit [!INCLUDE[prod_short](includes/prod_short.md)]issa reaaliajassa tietoa valuuttakurssien (FX) hinnoista tai historiallisista hinnoista, löydät sen nimityksellä valuutta. Tämän artikkelin lisäksi on artikkeli [Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md).

Valuuttakoodit määritetään kohdassa **Valuutat**, mukaan lukien lisätiedot ja asetukset, jotka ovat välttämättömiä kunkin valuuttakoodin osalta.

> [!TIP]
> Luo valuutat kansainvälisellä ISO-koodilla, jotta työskentely valuutan kanssa on yksinkertaista tulevaisuudessa.

|Kenttä|Kuvaus|  
|---------------------------------|---------------------------------------|  
|**Koodi**|Valuutan tunnus.|
|**Kuvaus**|Valuutan vapaa tekstikuvaus.|
|**ISO-koodi**|Kansainvälinen kolmikirjaiminen ISO 4217:n mukainen valuuttakoodi.|
|**ISO-numerokoodi**|Valuutan kansainvälinen ISO 4217:n mukainen numeroviite.|
|**Vaihtokurssin pvm**|Vaihtokurssin viimeisin todellinen päivämäärä.|
|**EMU-valuutta**|Määrittää, onko valuutta EMU-valuutta (Euroopan talous- ja rahaliitto), esimerkiksi EUR.|
|**Realisoitun. voittojen tili**|Tili, johon todellinen voitto kirjataan, kun vastaanotat maksuja saamisista tai rekisteröit todellisen valuuttakurssin ostovelkojen maksuille. Esimerkki saamisen valuuttatransaktiosta on tämän taulukon alla olevassa esimerkissä. |
|**Realisoitun. tapp. tili**|Tili, johon todellinen tappio kirjataan, kun vastaanotat maksuja saamisista tai rekisteröit todellisen valuuttakurssin ostovelkojen maksuille. Esimerkki saamisen valuuttatransaktiosta on tämän taulukon alla olevassa esimerkissä. |
|**Toteutumattomien voittojen tili**|Tili, johon teoreettinen voitto kirjataan valuutan muutosta tehtäessä.|
|**Toteutumattomien tappioiden tili**|Tili, johon teoreettinen tappio kirjataan valuutan muutosta tehtäessä.|
|**Summan pyöristystarkkuus**|Joissakin valuutoissa laskusummilla on muita muotoja kuin **Pääkirjanpidon asetukset** -sivulla on määritetty. Jos muutat summan pyöristystarkkuutta valuutalle, kaikki kyseisen valuutan laskusummat pyöristetään päivitetyllä tarkkuudella.|
|**Summan desimaalien määrä**|Joissakin valuutoissa laskusummilla on muita muotoja kuin **Pääkirjanpidon asetukset** -sivulla on määritetty. Jos muutat desimaalien määrää valuutalle, kaikki kyseisen valuutan laskusummat pyöristetään päivitetyllä desimaalimäärällä.|
|**Laskun pyöristystyyppi**|Määrittää tavan, jota käytetään, jos summa on pyöristettävä. Vaihtoehdot ovat **Lähin**, **Ylös** ja **Alas**.|
|**Yksikkösumman pyöristystarkkuus**|Joissakin valuutoissa yksikkösummilla on muita muotoja kuin **Pääkirjanpidon asetukset** -sivulla on määritetty. Jos muutat yksikkösumman pyöristystarkkuutta valuutalle, kaikki kyseisen valuutan yksikkösummat pyöristetään päivitetyllä tarkkuudella.|
|**Desimaalien yksikkömäärä**|Joissakin valuutoissa yksikkösummilla on muita muotoja kuin **Pääkirjanpidon asetukset** -sivulla on määritetty. Jos muutat desimaalien yksikkömäärää valuutalle, kaikki kyseisen valuutan yksikkösummat pyöristetään päivitetyllä desimaalimäärällä.|
|**Kohdistuksen pyöristystarkkuus**|Määrittää sen välin suuruuden, joka sallitaan pyöristyksen erona, kun kohdistat eri valuuttoina ilmoitettuja tapahtumia toisiinsa.|
|**PVA:n muuntamispyöristys. Debet-tili**|Määrittää muunnostiedot. Tiedoissa täytyy olla myös debet-tili, jos haluat syöttää korjausrivejä erojen pyöristystä varten pääkirjanpidoissa Kirjoita muunnoksen **PVA-pyöristysrivit** -toiminnon avulla.|
|**PVA:n muuntamispyöristys. Kredit-tili**|Määrittää muunnostiedot. Tiedoissa täytyy olla myös kredit-tili, jos haluat syöttää korjausrivejä erojen pyöristystä varten pääkirjanpidoissa Kirjoita muunnoksen **PVA-pyöristysrivit** -toiminnon avulla.|
|**Viimeksi muutettu**|Viimeisin valuutan muutoksen päivämäärä.|
|**Viimeksi muokattu**|Muutoksen päivämäärä valuutan asetuksiin.|
|**Maksutoleranssiprosentti**|Tälle valuutalle määritetty maksutoleranssin enimmäisprosentti. Lisätietoja on kohdassa [Maksutoleranssi ja maksualennustoleranssi](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Maksimi maksutoleranssisumma**|Tälle valuutalle määritetty maksutoleranssin enimmäissumma. Lisätietoja on kohdassa [Maksutoleranssi ja maksualennustoleranssi](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Valuuttakerroin**|Ilmaisee valuutan ja paikallisvaluutan välisen suhteen käyttämällä todellista valuuttakurssia.|
|**Realisoitun. KP-voittojen tili**|Määrittää pääkirjanpitotilin, jonne vaihtokurssivoitot lähetetään valuuttamuunnoksia varten paikallisvaluutan (PVA) ja lisäraportointivaluutan välillä. Valuuttakurssivoitot lasketaan, kun Muuta vaihtokursseja -eräajo suoritetaan pääkirjanpidon tilitietojen oikaisua varten. Tämä kenttä ei välttämättä ole näkyvissä oletusarvoisesti. Sen voi hakea mukauttamalla sivua.|
|**Realisoitun. KP-tapp. tili**|Määrittää pääkirjanpitotilin, jonne vaihtokurssitappiot lähetetään valuuttamuunnoksia varten paikallisvaluutan (PVA) ja lisäraportointivaluutan välillä. Valuuttakurssivoitot lasketaan, kun Muuta vaihtokursseja -eräajo suoritetaan pääkirjanpidon tilitietojen oikaisua varten. Tämä kenttä ei välttämättä ole näkyvissä oletusarvoisesti. Sen voi hakea mukauttamalla sivua.|
|**Jäännösvoittojen tili**|Määrittää KP-tilin, jota käytetään jäännösvoittosummien (pyöristyserot) kirjaamista varten silloin, kun pääkirjanpidon sovellusalueella käytetään lisäraportointivaluuttaa. Tämä kenttä ei välttämättä ole näkyvissä oletusarvoisesti. Sen voi hakea mukauttamalla sivua.|
|**Jäännöstappioiden tili**|Määrittää KP-tilin, jota käytetään jäännöstappiosummien (pyöristyserot) kirjaamista varten silloin, kun pääkirjanpidon sovellusalueella käytetään lisäraportointivaluuttaa. Tämä kenttä ei välttämättä ole näkyvissä oletusarvoisesti. Sen voi hakea mukauttamalla sivua.|
|**Maksimi sallittu ALV-ero**|Tämän valuutan ALV-erojen suurin sallittu summa. Lisätietoja on kohdassa [ALV-määrien korjaaminen manuaalisesti myynti- ja ostoasiakirjoissa](finance-work-with-vat.md#correcting-vat-amounts-manually-in-sales-and-purchase-documents). Tämä kenttä ei välttämättä ole näkyvissä oletusarvoisesti. Sen voi hakea mukauttamalla sivua.|
|**ALV-pyöristystyyppi**|Määrittää pyöristystavan ALV-summien oikaisemiseksi manuaalisesti myynti- ja ostoasiakirjoissa. Tämä kenttä ei välttämättä ole näkyvissä oletusarvoisesti. Sen voi hakea mukauttamalla sivua.|

### <a name="example-of-a-receivable-currency-transaction"></a>Esimerkki saamisen valuuttatapahtumasta

Kun saat laskun yritykseltä ulkomaan valuutassa, laskun paikallisen valuutan (PVA) arvo on melko helppo laskea tämän päivän valuuttakurssin perusteella. Laskussa on kuitenkin usein maksuehdot, joiden nojalla voit viivyttää maksua myöhemmälle päivämäärälle, mikä taas tarkoittaa mahdollisesti erilaista valuuttakurssia. Kun vielä pankkien valuuttakurssit eroavat aina virallisista valuuttakursseista, on mahdotonta ennakoida tarkkaa paikallisen valuutan (PVA) summaa, joka tarvitaan laskun kattamiseen. Jos laskun eräpäivä ulottuu seuraavaan kuukauteen, saatat joutua myös uudelleenarvostamaan paikallisen valuutan (PVA) summan kuun lopussa. Valuutan oikaisu on tarpeen, koska laskun summan kattamiseen tarvittava uusi PVA-arvo saattaa olla erilainen, ja yrityksen velka toimittajalle on mahdollisesti muuttunut. Uusi PVA-summa voi olla edellistä summaa suurempi tai pienempi, joten se edustaa voittoa tai tappiota. Koska laskua ei ole kuitenkaan vielä maksettu, voiton tai tappion katsotaan olevan *toteutumaton*. Myöhemmin lasku maksetaan, ja pankki palauttaa maksun todellisen valuuttakurssin mukaisesti. Vasta nyt lasketaan *toteutunut* voitto tai tappio. Tämä toteutumaton voitto tai tappio peruutetaan ja toteutunut voitto tai tappio kirjataan sen sijaan.

Seuraavassa esimerkissä lasku vastaanotetaan 1.1., ja valuuttasumma on 1 000. Valuuttakurssi on 1,123.

|Pvm|Toiminto|Valuuttasumma|Asiakirjan pvm|PVA-summa asiakirjassa|Oikaisukurssi|Toteutumattomien voittojen summa|Maksukurssi|Realisoituneiden tappioiden summa|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Lasku**|1000|1,123|1 123|||||
|1/31|**Muutos**|1000||1 125|1,125|2|||
|2/15|**Maksun peruutuksen muutos**|1000||||-2|||
|2/15|**Maksu**|1000||1 120|||1,120|-3|

Kuukauden lopussa suoritetaan valuutan muuttaminen, jossa muutoksen valuuttakurssiksi on asetettu 1,125, mikä laukaisee toteutumattoman voiton 2.

Maksuhetkellä pankkitapahtumaan rekisteröity todellinen valuuttakurssi näyttää valuuttakurssia 1,120.

Tähän sisältyy toteutumaton tapahtuma, ja siksi se peruutetaan yhdessä maksun kanssa.

Lopuksi maksu rekisteröidään ja todellinen tappio kirjataan realisoituneen tappion tilille.

## <a name="available-currency-functions"></a>Käytettävissä olevat valuuttafunktiot

Seuraavassa taulukossa esitellään päätoiminnot **Valuutat**-sivulla. Osa toiminnoista selitetään seuraavissa osissa.  

|Valikko|Toiminto|Kuvaus|
|-------------|--------------|------------------------------|
|**Käsittely**|**Ehdota tilejä**|Käytä muiden valuuttojen tilejä. Useimmin käytetyt tilit lisätään.|
||Muuta maksutoleranssia|Muuta suurinta maksutoleranssia, maksutoleranssiprosenttia tai molempia. Tiedot suodatetaan valuutan mukaan. Lisätietoja on kohdassa [Maksutoleranssi ja maksualennustoleranssi](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Vaihtokurssit**|Näytä käyttämiesi valuuttojen päivitetyt vaihtokurssit.|
||**Muuta vaihtokursseja**|Muuta pääkirjanpidon, asiakkaan, toimittajan ja pankkitilin tapahtumien kirjaukset ja saldot muuttuneen vaihtokurssin mukaisiksi, jos vaihtokurssi on muuttunut tapahtumien kirjauksen jälkeen.|
||**Vaihtokurssin muutos, rekisteri**|Tarkastele **Muuta vaihtokursseja** -eräajon suorituksen tuloksia. Ohjelma luo rivin jokaiselle valuutalle tai valuuttayhdistelmälle sekä kirjausryhmälle, joka sisältyy muutokseen.|
|**Vaihtokurssipalvelut**|**Vaihtokurssipalvelut**|Tarkastele tai muokkaa niiden asetuksia palveluille, jotka on määritetty noutamaan päivitetyt vaihtokurssit käytettäessä **Päivitä valuutan vaihtokurssit** -toimintoa.|
||**Päivitä valuutan vaihtokurssit**|Nouda uusimmat valuuttojen vaihtokurssit palveluntarjoajalta.|
|**Raportit**|**Valuuttasaldo**|Tämä raportti näyttää kaikkien asiakkaiden ja toimittajien saldot valuutoissa ja paikallisessa valuutassa (PVA). Raportti näyttää kaksi PVA-saldoa. Toinen on ulkomaan valuuttasaldo muunnettuna PVA:ksi tapahtumahetken vaihtokurssia käyttäen. Toinen on ulkomaan valuuttasaldo muunnettuna PVA:ksi työpäivän vaihtokurssia käyttäen.|

## <a name="exchange-rates"></a>Vaihtokurssit

Vaihtokurssit ovat työkalu, jonka avulla lasketaan kunkin valuuttatapahtuman arvo paikallisessa valuutassa (PVA). **Vaihtokurssit**-sivulla on seuraavat kentät:

|Kenttä|Kuvaus|  
|---------------------------------|---------------------------------------|  
|**Aloitustiedot**|Päivämäärä, jolloin valuuttakurssi on pantu toimeen|  
|**Valuutan koodi**|Tähän vaihtokurssiin liittyvä valuutan koodi|  
|**Suhteellinen valuuttakoodi**|Jos tämä valuutta on osa kolmenkeskistä valuuttalaskentaa, liittyvä valuuttakoodi voidaan määrittää tässä|  
|**Vaihtokurssisumma**|Vaihtokurssisumma on rivillä valitulle valuuttakoodille käytettävä kurssi. Normaalisti 1 tai 100|  
|**Suhteellinen vaihtokurssisumma**|Suhteellinen vaihtokurssisumma on rivillä valitulle suhteelliselle valuuttakoodille käytettävä kurssi.|  
|**Muutoksen vaihtokurssisumma**|Muutoksen vaihtokurssisumma on kurssi, jota käytetään valuuttakoodille, joka on valittuna rivillä **Muuta vaihtokursseja** -eräajoa varten|  
|**Suhteellinen vaihtokurssisumman muutos**|Suhteellinen vaihtokurssisumman muutos on kurssi, jota käytetään valuuttakoodille, joka on valittuna rivillä **Muuta vaihtokursseja** -eräajoa varten|  
|**Kiinteä vaihtokurssisumma**|Määrittää, voidaanko valuuttakurssia muuttaa laskuissa ja päiväkirjan riveillä.|  

Yleisesti arvoja **Vaihtokurssisumma**- ja **Suhteellinen vaihtokurssisumma** -kentissä käytetään oletusvaluuttakursseina kaikissa vastedes luotavissa myyntisaamisten ja ostovelkojen asiakirjoissa. Asiakirjalle määritetään valuuttakurssi tämänhetkisen käsittelypäivämäärän mukaan.  

> [!Note]
> Todellinen valuuttakurssi lasketaan tämän kaavan avulla:
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

Muutoksen vaihtokurssisummaa tai suhteellista vaihtokurssisumman muutosta käytetään kaikkein avoimien pankki-, saamis- ja ostovelkatransaktioiden päivittämiseen.  

> [!Note]
> Todellinen valuuttakurssi lasketaan tämän kaavan avulla:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjusting-exchange-rates"></a>Vaihtokurssien muuttaminen

Koska vaihtokurssit vaihtelevat jatkuvasti, järjestelmän lisävaluutta-arvot on tarkistettava jaksoittain. Jos tarkistuksia ei tehdä, ulkomaisista valuutoista (tai lisävaluutoista) muunnetut summat voivat olla harhaanjohtavia, kun ne kirjataan pääkirjanpitoon PVA:na. Lisäksi päivittäiset tapahtumat, jotka on kirjattu ennen päivittäisen vaihtokurssin lisäämistä sovellukseen, on päivitettävä, kun päivittäinen vaihtokurssi on lisätty.

**Muuta vaihtokursseja** -eräajon avulla voi muuttaa manuaalisesti kirjattujen asiakas-, toimittaja- ja pankkitilitapahtumien vaihtokursseja. Sen avulla voi myös päivittää KP-tapahtumien lisäraportointivaluutan summia.  

> [!TIP]
> Voit käyttää palvelua vaihtokurssien päivittämiseen automaattisesti järjestelmässä. Lisätietoja on kohdassa [Valuutanvaihdon kurssipalvelun määrittäminen](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Jos kirjattujen tapahtumien vaihtokursseja ei kuitenkaan silloin muuteta. Voit päivittää kirjattujen tapahtumien vaihtokurssit käyttämällä **Muuta vaihtokursseja** -erätyötä.

### <a name="effect-on-customers-and-vendors"></a>Vaikutus asiakkaisiin ja toimittajiin

Asiakkaan ja toimittajan tileillä eräajo muuttaa valuutan käyttäen sitä vaihtokurssia, joka on kirjauspäivämääränä voimassa eräajossa. Eräajo laskee yksittäisten valuuttasaldojen erot ja kirjaa summat sille kirjanpitotilille, joka on määritetty **Valuutat**-sivun **Ei-realisoit. val.voitt. tili** -kentässä tai **Ei-realisoit. val.voitt. tili** -kentässä. Vastatapahtumat kirjataan automaattisesti ostoreskontran/myyntireskontran tilille pääkirjanpidossa.

Eräajo käsittelee kaikki avoimet asiakas- ja toimittajatapahtumat. Jos tapahtumassa on valuuttaero, eräajo luo uuden, eritellyn asiakas- tai toimittajatapahtuman, josta näkyy muutettu summa asiakas- tai toimittajatapahtumassa.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Asiakas- ja toimittajatapahtumien dimensiot

Muutostapahtumille on määritetty dimensiot asiakas-/toimittajatapahtumilta, ja muutokset on kirjattu dimensioarvojen kombinaatioiden mukaan.

### <a name="effect-on-bank-accounts"></a>Vaikutus pankkitileihin

Pankkitileillä eräajo muuttaa valuutan käyttäen sitä vaihtokurssia, joka on kirjauspäivämääränä voimassa eräajossa. Eräajo laskee eron jokaiselle tilille, jolla on valuuttakoodi ja kirjaa summat sille kirjanpitotilille, joka on määritetty **Valuutat**-sivun **Realisoitun. val.voitt. tili** -kentässä tai **Realisoit. val.tapp. tili** -kentässä. Vastatapahtumat kirjataan automaattisesti niille KP:n pankkitileille, jotka on määritelty pankkitilien postitusryhmissä. Eräajo laskee yhden tapahtuman valuuttaa ja kirjausryhmää kohden.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensiot pankkitilitapahtumilla

Muutostapahtumien pankkitilin KP-tilille ja voitto/tappio tileille määritetään oletusdimensiot.

### <a name="effect-on-gl-accounts"></a>Vaikutus KP-tileihin
Jos kirjaat lisäraportointivaluutan, voit eräajon avulla luoda uusia KP-tapahtumia PVA:n ja lisäraportointivaluutan välillä tapahtuvia kurssimuutoksia varten. Eräajo laskee jokaisen kirjanpitotapahtuman erotuksen ja muuttaa kirjanpitotapahtumaa sen mukaan, mitä **Vaihtokurssin muutos** -kentässä lukee kirjanpitotilin kohdalla.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensiot KP-tilin tapahtumille
Muutostapahtumille on määritetty niiden KP-tilien dimensiot, joille ne on kirjattu.

> [!Important]
> Syötä ennen eräajon käyttämistä vaihtokurssit, joita käytetään ulkomaisen valuutan saldoja muutettaessa. Se tehdään **Valuutan vaihtokurssit** -sivulla.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Valuutanvaihdon kurssipalvelun määrittäminen
Voit pitää valuutan vaihtokurssit ajan tasalla ulkoisen palvelun, kuten FloatRatesin avulla. 

> [!NOTE]
> Useimmat vaihtokurssipalvelut sisältävät tietoja, jotka ovat yhteensopivia kohteen [!INCLUDE[prod_short](includes/prod_short.md)] tuontiprosessin kanssa. Joskus tiedot kuitenkin muotoillaan eri tavalla, ja sinun on mukautettava tuontiprosessia. Voit tehdä näin tiedonsiirtokehyksen avulla lisäämällä oman koodiyksikön. Tarvitset luultavasti kehittäjän apua. Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake, syötä **Valuutanvaihdon kurssipalvelut** ja valitse liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät **Valuutanvaihtokurssipalvelut**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **Käytössä**-tilanvaihtonäppäin ottaaksesi palvelun käyttöön.

> [!NOTE]
> Seuraava video näyttää esimerkin siitä, miten voit muodostaa yhteyden valuutan vaihtokurssipalveluun. Esimerkissä käytetään Euroopan keskuspankkia. Segmentissä, joka kuvaa, miten kenttien yhdistämismääritykset tehdään, **Valuutan koodin pääsolmu** -kohdan **Lähde**-sarakkeen asetus palauttaa vain ensimmäisen löydetyn valuutan. Asetuksen on oltava `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Valuutan vaihtokurssien päivittäminen palvelun avulla
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Valuutat** ja valitse sitten vastaava linkki.
2. Valitse **Päivitä valuutan vaihtokurssit** -toiminto.

**Valuutat**-sivun **Vaihtokurssi**-kentän arvo päivittyy uusimman valuutan vaihtokurssin mukaan.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös
[Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md)  
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
