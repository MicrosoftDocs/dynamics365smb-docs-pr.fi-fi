---
title: Validoitujen lokalisointisovellusten kehittäminen
description: Noudata Dynamics 365 Business Centralin lakisääteisiä vaatimuksia validoituna lokalisointisovelluksena.
author: altotovi
ms.date: 04/24/2024
ms.reviewer: solsen
ms.topic: conceptual
ms.author: altotovi
---


# <a name="development-of-validated-localization-apps"></a>Validoitujen lokalisointisovellusten kehittäminen

Tässä artikkelissa kuvataan [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman validoidun lokalisointisovelluksen kehittämiseen liittyvät vaatimukset ja suuntaviivat.

## <a name="what-is-a-validated-localization-app"></a>Mikä on validoitu lokalisointisovellus?

[!INCLUDE[prod_short](includes/prod_short.md)] on saatavilla [maailmanlaajuisesti yli 170 markkina-alueella](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json). Joillakin markkinoilla Microsoft tekee yhteistyötä ISV-kumppaneiden kanssa lokalisoidakseen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmia käyttämällä lokalisointisovelluksia, jotka ovat saatavilla [Microsoft AppSourcessa](https://go.microsoft.com/fwlink/?linkid=2081646). Näillä alueilla lokalisoinnit voivat olla käytettävissä ensisijaisen lokalisointisovellusohjelman kautta. Ensisijaiset lokalisointisovellukset -ohjelma tunnistaa ne sovellukset, jotka on rakennettu Microsoftin erityisten laatuohjeiden mukaisesti. ISV-kumppanit, jotka noudattavat näitä ohjelman vaatimuksia ja ohjeita, voivat hyötyä teknisesti ja kaupallisesti palvellakseen jälleenmyyjiään ja asiakkaitaan.  

Seuraavista osista löydät vaatimuksia ja suuntaviivoja. Voit ottaa yhteyttä ohjelman tiimiin, jos haluat osallistua tähän ohjelmaan ja noudattaa alla olevia vaatimuksia ottamalla meihin yhteyttä [Microsoftin lokalisointitiimin kautta](mailto:d365bcloc@microsoft.com).   

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman validoitu lokalisointi -sovellusaloitetta otetaan parhaillaan käyttöön pilottiohjelmana. Alapuolella olevat vaatimukset ja edut voivat muuttua kumppanin ja asiakkaan palautteen perusteella.  

Validoitu lokalisointi -pilottiohjelman sovellukset sisältävät joukon toimintoja, jotka vastaavat seuraaviin luokkiin kuuluviin paikallisiin sääntelyvaatimuksiin.  

- **Sääntelyvaatimukset** - paikalliset toiminnot, jotka auttavat yrityksiä täyttämään lakisääteiset vaatimukset, kuten veroraportointi, paikalliset verkkolaskutusmuodot, paikalliset yleisesti hyväksytyt kirjanpitoperiaatteet ja muut sääntelyvaatimukset.
- **Kansalliset standardit** – paikalliset toiminnot, jotka käsittelevät paikallisia standardeja, kuten osoitemuodot, kansalliset pankkimuodot ja paikalliset globaalien standardien tulkinnat.
- **Paikallinen kieli** - paikallinen kieli lokalisointisovelluksessa, mutta myös perussovellusta varten, jos tämä kieli ei ole tällä hetkellä [tuettujen kielten](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json) luettelossa.
- **Paikallinen kieli** - paikallinen kieli lokalisointisovelluksessa, mutta myös perussovellusta varten, jos tämä kieli ei ole tällä hetkellä [tuettujen kielten](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json) luettelossa.

> [!NOTE]
> Paikallisia markkinatarpeita tai toimialavaatimuksia ei tulisi sisällyttää ensisijaisiin lokalisointisovelluksiin. Jos sovellukset sisältävät nämä toiminnot, sovelluksia ei voi hyväksyä validoiduiksi lokalisointisovelluksiksi.

> [!NOTE]
> Paikalliset toiminnot ovat hyödyllisiä maan tuottavuusprosessien kannalta ja lisäävät näin liiketoiminnan arvoa, mutta niitä ei tarvita sääntelyn näkökulmasta, kuten tietyt pankki- ja maksumuodot, kustannusraportit, henkilöstöhallinnon toiminnot, palkkasummat ja vastaavat pienemmät tai suuremmat, ja kätevät ominaisuudet on eristettävä muihin sovelluksiin. Jos sovellukset sisältävät nämä toiminnot, niitä ei voi hyväksyä validoiduiksi lokalisointisovelluksiksi.   

## <a name="validated-localization-app-business-requirements"></a>Validoitu lokalisointi -sovelluksen liiketoimintavaatimukset

- Validoidun lokalisointisovelluksen tarjoaja täyttää kaikki CSP-palvelun epäsuoran palveluntarjoajan vaatimukset.  
- Validoidun lokalisointisovelluksen tarjoaja tuo markkinoille minimitarjonnan viidessä maassa/alueella, jotka sisältyvät Dynamics 365 Business Centralin validoituun lokalisointisovellukseen. 
- Validoitu lokalisointi -sovelluksen tarjoajalla on vähintään 10 [!INCLUDE[prod_short](includes/prod_short.md)] online -asiakasta, joilla on tuotantoympäristöt ja jotka käyttävät aktiivisesti Validoitu lokalisointi -sovellusta. 
- Validoidun lokalisointisovelluksen tarjoaja lähettää liiketoimintasuunnitelman vuosittain ohjelman v-tiimille. Näihin kuuluvat suunnitellut markkinointi- ja valmiustoimet, joiden avulla voidaan edistää yhdistettyä tarjontaa soveltuvien maiden/alueiden välillisten jälleenmyyjien kanssa. Suunnitelma voidaan lähettää kunkin vuosineljänneksen alussa [Microsoftin lokalisointitiimille](mailto:d365bcloc@microsoft.com).  
- Validoidut lokalisointisovellukset ovat kaikkien asiakkaiden ja kumppaneiden käytettävissä, jotka haluavat hyötyä siitä.  
- Validoidun lokalisointisovelluksen tarjoaja tuo markkinoille minimitarjonnan viidessä maassa/alueella, jotka sisältyvät Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman validoituun lokalisointisovellukseen. 
- Validoitu lokalisointi -sovelluksen tarjoajalla on vähintään 10 [!INCLUDE[prod_short](includes/prod_short.md)] online -asiakasta, joilla on tuotantoympäristöt ja jotka käyttävät aktiivisesti Validoitu lokalisointi -sovellusta. 
- Validoidun lokalisointisovelluksen tarjoaja lähettää liiketoimintasuunnitelman vuosittain ohjelman v-tiimille. Näihin kuuluvat suunnitellut markkinointi- ja valmiustoimet, joiden avulla voidaan edistää yhdistettyä tarjontaa soveltuvien maiden/alueiden välillisten jälleenmyyjien kanssa. Suunnitelma voidaan lähettää kunkin vuosineljänneksen alussa [Microsoftin lokalisointitiimille](mailto:d365bcloc@microsoft.com).  
- Validoidut lokalisointisovellukset ovat kaikkien asiakkaiden ja kumppaneiden käytettävissä, jotka haluavat hyötyä siitä.  
- Validoidun lokalisointisovelluksen tarjoaja käyttää Microsoftia toistuvasti tuotantovirroissa.

## <a name="validated-localization-app-functional-and-technical-requirements"></a>Validoidun lokalisointisovelluksen toiminnalliset ja tekniset vaatimukset

### <a name="functionality-requirements"></a>Toiminnallisuusvaatimukset

Ensisijaisen lokalisointisovelluksen teknisten vaatimusten täyttämisen lisäksi ensisijaisen lokalisointisovelluksen käyttökelpoinen tuotevalikoima on vähintään:  

- Paikalliset pakolliset ominaisuudet:   
  - Lainsäädännön vaatimukset.   
  - Virallisesti pakolliset toiminnot. 
  - Vain vaakasuuntaiset ominaisuudet (jotka eivät ole toimialakohtaisia).  
  - Soveltuu useimpiin yrityksiin.  
  - Seuraavassa suunnitelmassa:   
    - Yleisimmät lainsäädäntömuutokset. 
    - Jo aiemmin Microsoftin lokalisoinneissa seuratut lokalisoinnit. 
    - Ominaisuusviittaukset – harvoin uusia.  
    - Ei toimittaja-/pankkikohtaisia muotoja, palkka- tai muita vastaavia muotoja. 
    - Ei globaaleja ominaisuuksia, jos Microsoft ei ole luonut niitä. 
- Käännökset: 
  - Lokalisointisovelluksen käännös paikallisille kielille. 
  - Perussovelluksen käännös paikallisille kielille – jos kieltä ei jo [tueta](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).  
  - Lokalisointisovelluksen dokumentaation käännös paikallisille kielille. 
- Vaikka molemmat ovat osa lokalisointia, on suositeltavaa, että kansalliset vakiotoiminnot (paikallinen osa) rakennetaan erillisiksi sovelluksiksi paikallisista sääntelytoiminnoista. 
- Tietyille markkinoille soveltuvalla paikallisella kielellä olevat demotiedot.   
- Kaikki toiminnot on suunniteltava siten, että yksinkertaistettu käyttöliittymä säilyy. Huomaa, että ne on tarkoitettu ensisijaisesti PK-yritysten markkinoille.  
- Vältä uusien ominaisuuksien rakentamista, jos perussovelluksessa on jo samoja tai samankaltaisia toimintoja, kuten sähköinen laskutus, tarkastusvienti, ALV-ominaisuudet, tiedonvaihto ja muut, joissa useimmat toiminnot ovat yhteisiä kaikille maille/alueille, mutta joitain paikallisia sääntöjä tai yritysmuodot, jotka ovat globaalien kehysten tai muotojen laajennuksia. Uusien toimintojen rakentamisen sijaan voit laajentaa aiemmin luotuja ominaisuuksia.  
- Valmistele asetusoppaita (ohjattuja toimintoja) alueille, jotka on määritetty monimutkaisiksi, jotta käyttäjät voivat ottaa lokalisointisovelluksen käyttöön, löytää ja käyttää ensimmäistä käyttökokemusta.  
- Kaikki toiminnot on suunniteltava siten, että yksinkertaistettu käyttöliittymä säilyy. Pidä mielessä, että ne on tarkoitettu ensisijaisesti PK-yritysten markkinoille.  
- Vältä uusien ominaisuuksien rakentamista, jos perussovelluksessa on jo samoja tai samankaltaisia toimintoja, kuten sähköinen laskutus, tarkastusvienti, ALV-ominaisuudet, tiedonvaihto ja muut, joissa useimmat toiminnot ovat yhteisiä kaikille maille/alueille, mutta joitain paikallisia sääntöjä tai yritysmuodot, jotka ovat globaalien kehysten tai muotojen laajennuksia. Uusien toimintojen rakentamisen sijaan voit laajentaa aiemmin luotuja ominaisuuksia.    
- Valmistele asetusoppaita (ohjattuja toimintoja) alueille, jotka on määritetty monimutkaisiksi, jotta käyttäjät voivat ottaa lokalisointisovelluksen käyttöön, löytää ja käyttää ensimmäistä käyttökokemusta.  
- Kumppanien on toimitettava toiminnallinen dokumentaatio lokalisointiin liittyvistä kaikista osa-alueista.  

### <a name="technical-requirements"></a>Tekniset vaatimukset

Seuraavassa on luettelo vaatimuksista, jotka sinun on täytettävä, ennen kuin lähetät Validoitu lokalisointi -sovelluksen vahvistuksen laajennuksena. Tämä luettelo ei muuta [teknistä tarkistusluetteloa](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission) , ja se ainoastaan laajentaa vaatimuksia siellä.  

- Validoidun lokalisoinnin sovellustarjoajien on rakennettava Validoitu lokalisointi -sovellus W1-perussovelluksen perusteella.  
- Validoidun lokalisoinnin sovellustarjoajien on noudatettava Microsoftin elinkaari- ja tukikäytäntöjä.   
- Pakollisen testiautomaation on katettava minimi. 80 % koodista ja kaikkien niiden liiketoimintaprosessien, jotka muuttuvat Validoitu lokalisointi -sovelluksen avulla, on katettava testiautomaatio.  
- Validoidun lokalisointisovelluksen palveluntarjoajien on päivitettävä ja/tai testattava validoitu lokalisointi -sovellus ennen uuden julkaisun virallista käyttöönottoa (vähintään RC:n kanssa ennen uutta julkaisua) vahvistaakseen, että ongelmia ei ole. 
- Kaikkien Validoitu lokalisointi -sovelluksen koodin objektien on oltava englanniksi.   
- Validoidun lokalisoinnin sovellustarjoajien on noudatettava Microsoftin vanhentuneiden objektien ja AL-koodin poiston muutosten ja parhaiden käytäntöjen rikkomista.  
- Validoidun lokalisoinnin sovellustarjoajien on lisättävä uusia tapahtumia, jos markkinat (muut käyttöönottokumppanit tai asiakkaat) sitä vaativat, jos se on järkevässä liiketoiminnallisessa mielessä Microsoftin käytäntöjen ja tapojen mukaisesti. Muussa tapauksessa validoidun lokalisointisovelluksen palveluntarjoajien on vastattava tällaisiin kyselyihin asianmukaisin perustein, miksi siihen ei ole järkevää lisätä liiketoimintaa. 
- Validoidun lokalisoinnin sovellustarjoajien on toimitettava kirjalliset testiskenaariot englanniksi ja otettava Microsoft tarvittaessa käyttöön manuaalisessa testauksessa.  
- Jos validoidut lokalisointisovellukset laajentavat [!INCLUDE[prod_short](includes/prod_short.md)] -tietomallia uusilla taulukoilla ja/tai kentillä, validoidun lokalisointisovelluksen palveluntarjoajan on määritettävä **DataClassification**-ominaisuus oikein.
- Validoidun lokalisoinnin sovellustarjoajien on rakennettava Validoitu lokalisointi -sovellus W1-perussovelluksen perusteella.  
- Validoidun lokalisoinnin sovellustarjoajien on noudatettava Microsoftin elinkaari- ja tukikäytäntöjä.   

> [!NOTE]  
> Voit luoda integroinnin myös silloin, kun on hyödyllistä, että jotkin toiminnot sijoitetaan [!INCLUDE[prod_short](includes/prod_short.md)] -ympäristön ulkopuolelle, ja voit sen sijaan muodostaa yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan käyttämällä esimerkiksi ohjelmointirajapintaliittymää tai verkkopalvelua.

## <a name="see-also"></a>Katso myös

[Tekninen tarkistus](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission)  
[Lokalisoinnin vakioratkaisun kehittäminen](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-localization)  
[Maa- ja aluekohtainen saatavuus ja tuetut kielet](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Mikä on Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman paikallinen toiminto](about-localization.md)  
[Microsoft Dynamics 365:n kansainvälinen saatavuus](/dynamics365/get-started/availability)  
[Vaatimustenmukaisuuden yleiskatsaus](compliance/compliance-overview.md)  
[Dynamics 365:n maantieteellinen saatavuus](https://dynamics.microsoft.com/en-us/availability-reports/georeport/)  
