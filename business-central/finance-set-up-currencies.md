---
title: Valuuttojen määrittäminen
description: Määritä kukin valuutta, jos käytät ostamiseen ja myymiseen muuta valuuttaa kuin paikallista valuuttaa (PVA) tai jos kirjaat KP-tapahtumia eri valuuttoina.
author: edupont04
ms.topic: conceptual
ms.search.keywords: multiple currencies
ms.search.form: 5, 118
ms.date: 03/15/2022
ms.author: edupont
ms.openlocfilehash: f36d255c555c9ac83205a675bc7647cb02e0b3c2
ms.sourcegitcommit: 521735f8e27d8bff2d2dfbe94d240c09dcdaec29
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/15/2022
ms.locfileid: "8419601"
---
# <a name="set-up-currencies"></a>Valuuttojen määrittäminen

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Voit käyttää ulkoista palvelua ja päivittää ajantasaiset valuutan vaihtokurssit **Valuutat**-luettelossa. Lisätietoja on kohdassa [Valuutanvaihdon kurssipalvelun määrittäminen](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).  

[!INCLUDE [finance-currencies-lcy](includes/finance-currencies-lcy-note.md)]

## <a name="currencies"></a><a name="curr"></a>Valuutat

Seuraavassa taulukossa kuvataan **Valuutat**-luettelon kentät.

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

### <a name="available-currency-functions"></a>Käytettävissä olevat valuuttafunktiot

Seuraavassa taulukossa esitellään päätoiminnot **Valuutat**-sivulla.  

|Valikko|Toiminto|Kuvaus|
|-------------|--------------|------------------------------|
|**Käsittely**|**Ehdota tilejä**|Käytä muiden valuuttojen tilejä. Useimmin käytetyt tilit lisätään.|
||**Muuta maksutoleranssia**|Muuta suurinta maksutoleranssia, maksutoleranssiprosenttia tai molempia. Tiedot suodatetaan valuutan mukaan. Lisätietoja on kohdassa [Maksutoleranssi ja maksualennustoleranssi](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Vaihtokurssit**|Näytä käyttämiesi valuuttojen päivitetyt vaihtokurssit.|
||**Muuta vaihtokursseja**|Muuta pääkirjanpidon, asiakkaan, toimittajan ja pankkitilin tapahtumien kirjaukset ja saldot muuttuneen vaihtokurssin mukaisiksi, jos vaihtokurssi on muuttunut tapahtumien kirjauksen jälkeen.|
||**Vaihtokurssin muutosrekisteri**|Tarkastele **Muuta vaihtokursseja** -eräajon suorituksen tuloksia. Ohjelma luo rivin jokaiselle valuutalle tai valuuttayhdistelmälle sekä kirjausryhmälle, joka sisältyy muutokseen.|
|**Vaihtokurssipalvelut**|**Vaihtokurssipalvelut**|Tarkastele tai muokkaa niiden asetuksia palveluille, jotka on määritetty noutamaan päivitetyt vaihtokurssit käytettäessä **Päivitä valuutan vaihtokurssit** -toimintoa.|
||**Päivitä valuutan vaihtokurssit**|Nouda uusimmat valuuttojen vaihtokurssit palveluntarjoajalta.|
|**Raportit**|**Valuuttasaldo**|Tämä raportti näyttää kaikkien asiakkaiden ja toimittajien saldot valuutoissa ja paikallisessa valuutassa (PVA). Raportti näyttää kaksi PVA-saldoa. Toinen on ulkomaan valuuttasaldo muunnettuna PVA:ksi tapahtumahetken vaihtokurssia käyttäen. Toinen on ulkomaan valuuttasaldo muunnettuna PVA:ksi työpäivän vaihtokurssia käyttäen.|

## <a name="lcy-and-other-currencies"></a>PVA ja muut valuutat

[!INCLUDE [finance-currencies-lcy-def](includes/finance-currencies-lcy-def.md)]

## <a name="rounding-currencies"></a>Valuuttojen pyöristys

Kahden erilaisen pyöristysominaisuuden avulla voit hallita valuuttoja, joissa ei käytetä desimaaleja, sekä välttää tarpeettomien desimaalien käyttöä ulkomaanvaluutoissa:

- yksikkösumman pyöristys  

- summan pyöristys.  

Näitä ominaisuuksia voi käyttää yhdessä tai erikseen. Lisäksi niitä voi käyttää laskun pyöristyksen kanssa.

Summan ja yksikkösumman pyöristysominaisuudet vaikuttavat vain ulkomaanvaluuttana oleviin summiin, eivät vastaaviin paikallisena valuuttana oleviin summiin. Nämä kaksi ominaisuutta ei tuota mitään kirjauksia pääkirjanpidon tileille. Näin ollen pääkirjanpitotiliä ei ole määritettävä kirjausryhmissä tai muualla.

### <a name="unit-amount-rounding"></a>yksikkösumman pyöristys

Yksikkösumman pyöristysominaisuus ohjaa nimikkeiden ja resurssien ulkomaanvaluuttana olevien myyntihintojen pyöristystä myynti- ja ostoriveillä. Säännöt määritetään erikseen jokaiselle valuutalle **Valuutat**-luettelon **Yksikkösumman pyörist.tarkkuus** -kentässä.

Yksikkösumman pyöristysominaisuutta käytetään automaattisesti aina, kun myyntiriville syötetään nimikkeen tai resurssin numero. Jos lasku on tarkoitettu asiakkaalle, johon liittyy valuutan koodi, nimikkeen tai resurssin hinta muunnetaan asiakkaan valuutaksi. Hinta pyöristetään valuutan yksikkösumman pyöristystarkkuuden mukaan.

### <a name="amount-rounding"></a>summan pyöristys.

Summan pyöristysominaisuus ohjaa ulkomaavaluuttana olevien summien pyöristystä yleisen päiväkirjan riveillä sekä myynti- ja ostoriveillä. Säännöt määritetään erikseen jokaiselle valuutalle **Valuutat**-luettelon **Summan pyöristystarkkuus** -kentässä.

Ulkomaanvaluuttana olevat summat pyöristetään, kun yleisen päiväkirjan rivit sekä myynti- ja ostorivit täytetään ja kirjataan.

## <a name="exchange-rates"></a>Vaihtokurssit

Voit rekisteröidä jokaisen ulkomaanvaluutan vaihtokurssit ja määrittää, mistä päivämääristä alkaen kurssit ovat voimassa. Jokaiselle ulkomaanvaluutalle voi syöttää esimerkiksi päivittäiset, kuukausittaiset tai neljännesvuosittaiset vaihtokurssit.

Voit palauttaa historialliset vaihtokurssit viitetarkoituksia varten **Valuutan vaihtokurssit** -sivulla. Kun vaihtokurssit täytyy päivittää, voit käyttää **Päivitä vaihtokurssit** -painiketta hakeaksesi ajankohtaiset vaihtokurssit ulkoiselta palveluntarjoajalta.

## <a name="general-ledger-accounts"></a>Kirjanpitotilit

Et voi linkittää valuutan koodeja kirjanpitotileihin, koska kirjanpitotilien summat ovat paikallisena valuuttana. Jos pankkilaina on Yhdysvaltojen dollareina ja talletus tehdään Ruotsin kruunuina, tilejä voi seurata määrittämällä pankkitilit käyttämään sekä Yhdysvaltojen dollareita että Ruotsin kruunuja. Voit linkittää tilit kirjausryhmien avulla vastaaviin kirjanpitotileihin. Pääkirjanpidon summien arvo näkyy paikallisena valuuttana.

Voit syöttää valuutan koodin yleisen päiväkirjan riville ja kirjata rivin kirjanpitotilille. Oikeaa vaihtokurssia käytetään muunnettaessa summa paikalliseksi valuutaksi ennen sen kirjaamista kirjanpitotilille.  

## <a name="example-of-a-receivable-currency-transaction"></a>Esimerkki saamisen valuuttatapahtumasta

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="see-also"></a>Katso myös

[Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md)  
[Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md)  
