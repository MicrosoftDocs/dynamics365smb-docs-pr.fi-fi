---
title: Siirtyminen toiseen yritykseen tai ympäristöön
description: 'Jos käytät useita organisaatioita, voivat ympäristöjä yrityksiä nopeasti.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'environments, companies, tenants, organization'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 04/24/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# <a name="switching-to-another-company-or-environment"></a>Siirtyminen toiseen yritykseen tai ympäristöön

[!INCLUDE [prod_short](includes/prod_short.md)] on saatavilla useissa eri maissa ja eri alueilla. Se tukee monia erityyppisiä organisaatioita. Organisaatiossa voidaan päättää, että [!INCLUDE [prod_short](includes/prod_short.md)] on käytössä useissa *yrityksissä* ja *ympäristöissä*. Tässä artikkelissa on tietoja tärkeistä eroista ja siitä, miten niitä käytetään.

## <a name="about-companies-and-environments"></a>Tietoja yrityksistä ja ympäristöistä

[!INCLUDE [company_environment](includes/company_environment.md)]

> [!TIP]
> Jos siirryt usein yritysten välillä tai työskentelet [!INCLUDE[prod_short](includes/prod_short.md)]issa toisen sovelluksen, kuten Microsoft Teamsin, sisällä, voit helposti unohtaa missä kohdassa olet. Lisäämällä yrityksen nimen sisältävän tunnuksen lisääminen on helppo tarkistaa nopeasti, että olet oikeassa paikassa. Lisätietoja on kohdassa [Yrityksen merkkien näyttäminen](admin-company-information.md#badge).
> 
> Selaimesta riippuen voit myös kiinnittää eri yritykset Suosikit-palkkiin.  

<!--
[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]-->

## <a name="features-for-switching-company-or-environment"></a>Ominaisuudet yrityksen tai ympäristön vaihtamista varten

On olemassa muutamia ominaisuuksia, joiden avulla voit vaihtaa yritystä tai ympäristöä työskentelyn aikana. Seuraavassa taulukossa vertaillaan näitä ominaisuuksia. Niistä kerrotaan tarkemmin seuraavassa osassa.

|Ominaisuus|Vaihda yritystä|Vaihda ympäristöä|Vaihda uuteen selainvälilehteen| Käytettävissä paikallisesti|
|-------|--------------|------------------|-------------------------|----------------------|
|[Yrityksen vaihtaja](#use-the-company-switcher)|![valintamerkki](media/check.png "tarkistus")|![valintamerkki](media/check.png "tarkistus")|![valintamerkki](media/check.png "tarkistus")|![valintamerkki](media/check.png "tarkistus")|
|[Sovelluksen käynnistys](#use-the-app-launcher)||![valintamerkki](media/check.png "tarkistus")|![valintamerkki](media/check.png "tarkistus")||
|[Omat asetukset](#use-my-settings)|![valintamerkki](media/check.png "tarkistus")|||![valintamerkki](media/check.png "tarkistus")|
|[Yritystoiminto](#use-company-hub)|![valintamerkki](media/check.png "tarkistus")|![valintamerkki](media/check.png "tarkistus")|![valintamerkki](media/check.png "tarkistus")||

## <a name="use-the-company-switcher"></a>Käytä yrityksen vaihtajaa

Yrityksen vaihtajan käyttäminen on todennäköisesti nopein ja monipuolisin tapa vaihtaa yritystä. Yrityksen vaihtaja on ruutu, joka on käyttävissä kaikilla sivuilla. Ruutu sisältää yleiskatsauksen kaikkien ympäristöjen kaikista yrityksistä, joiden käyttöoikeus käyttäjällä on. Sen avulla voit vaihtaa suoraan mihin tahansa yritykseen samassa tai uudessa selainvälilehdessä. Tämä on erityisen hyödyllinen ominaisuus silloin, kun työskennellään useissa yrityksissä eri ympäristöissä.

1. Oikeassa yläkulmassa lähellä hakukuvaketta näkyy vakioyrityksen kuvake, esimerkiksi ![yrityksen kuvakkeen käynnistin.](media/ui-experience/company-icon.png "Näyttää yrityksen vaihtajan kuvakkeen, kun käytössä on yksittäinen ympäristö") ja ![company-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Näyttää yrityksen vaihtajan kuvakkeen, kun käytössä on useita ympäristöjä") tai [mukautettu merkki](admin-company-information.md#badge) yritykselle, jota parhaillaan käsitellään. Avaa yrityksen vaihtajan ruutu valitsemalla kuvake.

   :::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Näyttää yrityksen vaihtaja -kuvakkeen Business Central -asiakkaan otsikossa.":::  

   > [!TIP]
   > Voit avata ruudun myös käyttämällä <kbd>Crtl</kbd>+<kbd>O</kbd>-pikanäppäintä.
2. Valitse **Käytettävissä olevat yritykset** -ruudussa yritys, johon haluat vaihtaa, ja valitse sitten **Vaihda**-nuoli. Valitse lopuksi jokin seuraavista vaihtoehdoista:

   |Asetus|Kuvaus|
   |------|-----------|
   |Vaihda|Avaa valitun yrityksen roolikeskuksen auki olevassa selainvälilehdessä. Yrityksestä tulee Business Centralin avaava oletusyritys siihen asti, kunnes vaihdat yritystä tai muutat sitä käyttämällä **Omat asetukset** -kohtaa. |
   |Avaa uudessa välilehdessä|Avaa valitun yrityksen roolikeskuksen uudessa selainvälilehdessä niin, että alkuperäinen yritys avataan toisessa välilehdessä.|
   |Avaa uudessa välilehdessä ja siirry samalle sivulle|Tämä vaihtoehto on aktiivinen vain luettelosivuilla, kuten asiakkaiden, myyntitilausten tai nimikkeiden sivuilla. Se avaa saman luettelon valitulle yritykselle uudessa selainvälilehdessä. |

> [!TIP]
> Päivitä ympäristöjen ja yritysten luettelo painamalla <kbd>F5</kbd>-näppäintä.

## <a name="use-the-app-launcher"></a>Sovelluksen käynnistyksen käyttäminen

Kun olet kirjautunut sisään [!INCLUDE[prod_short](includes/prod_short.md)], käytettävissä olevat ympäristöt ovat käytettävissä tässä ikkunassa Microsoft 365.  

1. Valitse **Sovelluksen käynnistys** -kuvake ![Sovelluksen käynnistys.](media/app-launcher-icon.png "Sovelluksen käynnistimen avulla voi käyttää myös muita ominaisuuksia").
2. Etsi ja valitse [!INCLUDE[prod_short](includes/prod_short.md)] avautuvassa ruudussa. Jos et näe kohtaa [!INCLUDE[prod_short](includes/prod_short.md)], valitse **Kaikki sovellukset**, syötä sitten **Business Central** **Haku**-kenttään.

   :::image type="content" source="media/app-launcher-bc-tile.png" alt-text=" Microsoft 365 -sovelluksen käynnistimessä näkyy Business Central -ruutu.":::  

3. Jos ympäristöjä on enemmän kuin yksi, sinua pyydetään valitsemaan käytettävä ympäristö.

> [!NOTE]
> Sovelluksen käynnistystoiminto ei ole käytettävissä, jos olet kirjautunut Business Centraliin vieraana.

<!--
The following image shows tiles for accessing production and sandbox environments on the Dynamics 365 Home page.

:::image type="content" source="media/app-picker-environments.png" alt-text="The Dynamics 365 Home page showing production and sandbox environments.":::
-->
## <a name="use-my-settings"></a>Omien asetusten käyttäminen

Jos olet kirjautunut [!INCLUDE[prod_short](includes/prod_short.md)]iin, voit vaihtaa nopeasti toiseen yritykseen samassa ympäristössä. Valitsemastasi yrityksestä tulee vaihdon jälkeen oletusyritys, ja se avautuu, kun kirjaudut sisään seuraavan kerran.

1. Valitse oikeassa yläkulmassa **Asetukset**-kuvake ![Asetukset.](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") ja valitse sitten **Omat asetukset** -toiminto.

    > [!TIP]
    > Voit myös avata nopeasti Omat asetukset -sivun <kbd>Alt</kbd>+<kbd>T</kbd>-näppäinyhdistelmällä.

2. Valitse yritys **Omat asetukset** -sivun **Yritys**-kentässä.  
3. Valitse **OK**-painike.

> [!TIP]
> Oletusympäristöön voi siirtyä kätevästi kirjautumisen yhteydessä ilman ympäristön määritystä lisäämällä URL-osoitteen suosikkiluetteloon kirjautumisen jälkeen.

## <a name="use-company-hub"></a>Yritystoiminnon käyttäminen

*Yritystoiminto* on pitkälti erikoistunut roolikeskus, joka tarjoaa yrityksille ja ympäristöille taloudellisen yhteenvedon. Yritystoiminto on saatavilla [laajennuksena](ui-extensions-company-hub.md). Se sisältää koontinäytön ja yhteenvetotiedot jokaisesta yrityksestä, jonka käyttöoikeus käyttäjällä on. Aloitussivu näyttää taloudelliset KPI:t sekä suoran linkin yksittäisiin ympäristöihin ja yrityksiin. Katso lisätietoja kohdasta [Työnhallinta useiden yritysten välillä yritystoiminnossa](company-hub.md).

[![Näyttää yritystoiminnon sivun, jolla on luettelo kaikista yrityksistä.](media/company-hub.png)](media/company-hub.png#lightbox)  

## <a name="see-also"></a>Katso myös

[Uusien yritysten luominen [!INCLUDE[prod_short](includes/prod_short.md)]issa](about-new-company.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Ympäristöt ja yritykset (vain englanniksi)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  
[Yrityksen tiedot](admin-company-information.md)  
[Business Centralin hallintakeskus](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
