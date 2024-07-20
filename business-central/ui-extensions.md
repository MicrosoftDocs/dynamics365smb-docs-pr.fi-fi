---
title: Business Central Onlinen mukauttaminen sovellusten avulla
description: Lisätietoja toimintojen lisäämisestä ja Business Central -sovelluksen mukauttamisesta sovellusten asentamisen avulla on tässä artikkelissa.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: solsen
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '2500, 2502, 20350, 20353'
ms.date: 06/27/2024
ms.service: dynamics-365-business-central
---
# <a name="customizing-business-central-online-using-apps"></a>Business Central Onlinen mukauttaminen sovellusten avulla

Voit muuttaa [!INCLUDE[prod_short](includes/prod_short.md)] onlinea asentamalla sovelluksia, jotka sisältävät lisätoimintoja, muuttavat toimintaa tai mahdollistavat esimerkiksi uusien verkkopalveluiden käyttämisen. Nämä sovellukset ovat niin sanottuja *laajennuksia*, koska ne *laajentavat* [!INCLUDE [prod_short](includes/prod_short.md)]ia.

## <a name="manage-apps"></a>Sovellusten hallinta

Kun käynnistät [!INCLUDE[prod_short](includes/prod_short.md)]in ensimmäisen kerran, se sisältää joitakin valmiiksi asennettuja sovelluksia. Ajan kuluessa käytettävissä on yhä enemmän sovelluksia. Voit ottaa niitä käyttöön tarpeen mukaan.

Microsoft tarjoaa esimerkiksi sovelluksen, joka mahdollistaa integroinnin PayPal Payments Standard -ohjelman kanssa. Tämä laajennus asennetaan oletusarvoisesti. Mutta lisäosa, joka tarjoaa integroinnin toiseen maksupalveluun, voi kuitenkin tulla. Tällöin voit asentaa uuden laajennuksen ja valita, mitä käytetään.  

Jos haluat käyttää sovellusta, sinun on määritettävä sen mukana tulevat käyttöoikeuksien joukot.

Jos haluat asentaa AppSourcen sovelluksia tai poistaa niitä tai lisätä vuokraajakohtaisia laajennuksia, sinulla on oltava vaaditut käyttöoikeudet. Sinun on oltava **D365 Extension Mgt.** -käyttäjäryhmän jäsen tai sinulla on oltava **EXTEN. MGT. - ADMIN** -käyttöoikeuksien joukko. Jos olet järjestelmänvalvoja, voit määrittää käyttäjäryhmiä ja käyttöoikeuksia yrityksesi muille käyttäjille. Katso lisätietoja kohdasta [Luo käyttäjiä lisenssien mukaan](ui-how-users-permissions.md).  

> [!IMPORTANT]  
> [!INCLUDE [prod_short](includes/prod_short.md)] on-premises -sovelluksessa ei voi ladata vuokraajakohtaisia laajennuksia tai asentaa AppSource-sovelluksia **Laajennusten hallinta** -sivulla. AppSource-sovelluksia ei voi asentaa paikallisesti esimerkiksi Docker-pohjaisissa käyttöönotoissa.

Sovelluksia hallitaan **Laajennusten hallinta** -sivulla. Tämä sivu löytyy kotisivulta. Vaihtoehtoisesti voit valita **Etsi sivua tai raporttia** -kuvakkeen ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") oikeassa yläkulmassa. Syötä **Laajennus** ja valitse sitten liittyvä linkki. Lisätietoja on kohdassa [Sovellusten asentaminen ja asennusten poistaminen](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Jos sinulla on mielestäsi sovelluksen käyttöoikeus muttet löydä sen toimintoja, tarkista **Laajennusten hallinta** -sivu. Jos sovellusta ei mainita sivulla, voit asentaa sen seuraavassa osassa kerrotulla tavalla.  

> [!NOTE]  
> Kirjaudu sivustoon [AppSource.microsoft.com](https://appsource.microsoft.com/) [!INCLUDE[prod_short](includes/prod_short.md)] onlinessa käyttämäsi sähköpostitilin tiedoilla. Saman sähköpostitilin käyttäminen myös muissa palveluissa ja tuotteissa takaa sujuvan käyttökokemuksen.  

Pääset AppSourceen myös käyttämällä sovellusta [!INCLUDE[prod_short](includes/prod_short.md)]. Tällä hetkellä asennettuna olevat sovellukset näkyvät **Laajennusten hallinta** -sivulla. Voit avata **Microsoft AppSource -sovellukset** -sivun, jossa näkyvät AppSourcessa tällä hetkellä käytettävissä olevat [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukset. Jos valitset **Näytä AppSource** -toiminnon, sinut siirretään sivustolle [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Lisätietoja: [AppSource-sovellusten hallinta](admin-manage-appsource-apps.md).

Kun valitset sovelluksen, voit lukea tietoja sovelluksesta ja hakea lisätietoja käyttämällä sovelluksen Ohje-toimintoa. Kun haluat noutaa sovelluksen, sinun on hyväksyttävä käyttöehdot. Jos noudat sovelluksen AppSource-sivustosta, sinut kirjataan sisään sovellukseen [!INCLUDE[prod_short](includes/prod_short.md)] asennuksen viimeistelemiseksi.  

Sovellus on ehkä määritettävä asennuksen yhteydessä. Se tarkoittaa esimerkiksi **[!INCLUDE[prod_short](includes/prod_short.md)]in PayPal Payments Standard** -laajennuksen käyttämisessä tarvittavan tilin määrittämistä. Muissa sovelluksissa esimerkiksi lisätään kenttiä olemassa olevalle sivulle tai lisätään uusi sivu.

Jos poistat sovelluksen asennuksen ja haluat ottaa sen takaisin käyttöön, voit asentaa sovelluksen uudelleen. Kun poistat sovelluksen asennuksen, tietosi säilyvät. Jos asennat sovelluksen uudelleen, se on edelleen saatavilla. Jotkin sovellukset ovat pakollisia, eikä niitä voi poistaa **Laajennusten hallinta** -sivulla.

Osa on Microsoftin sovelluksia, osa [muiden yritysten](ui-extensions-other.md) sovelluksia. Kaikki sovellukset testataan, ennen kuin ne ovat käyttäjien käytettävissä. Suosittelemme kuitenkin lisätietoihin tutustumista laajennuksen mukana saatavien linkkien avulla ennen sovelluksen asentamista.  

> [!NOTE]  
> Voit pitää silmällä Microsoftin ja muiden toimittajien uusia sovelluksia osoitteessa [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## <a name="apps-and-data-transfer"></a>Sovellukset ja tietojen siirto

Koska seuraavia sovelluksia käytetään viestintään muiden palvelujen kanssa, ne saattavat siirtää tietoja [!INCLUDE[prod_short](includes/prod_short.md)] -ympäristön maantieteellisen alueen ulkopuolelle:

* AMC Banking 365 Fundamentals -laajennus
* Image Analyzer
* Myöhästyneen maksun ennuste
* PayPal Payments Standard
* Myynti- ja varastoennuste
* WorldPay Payments Standard

Sama pätee perussovellukseen, kuten seuraaviin ominaisuuksiin:

* Kassavirtaennuste
* Document Exchange -palvelu
* Dataverse-yhteys
* OCR-palvelu
* Online-kartta
* EU:n ALV-nron tarkistuksen Palvelu

## <a name="connect-your-business"></a>Yhdistä yrityksesi

Vuoden 2022 2. julkaisuaallossa [!INCLUDE [prod_short](includes/prod_short.md)] online -ympäristöt voivat sisältää vähintään yhden sovelluksen **Yhteyssovellukset**- ja **Pankkisovellukset**-sivuilla. Nämä sovellukset voivat muodostaa yhteyden yrityksesi ulkoisiin palveluihin tuottavuuden lisäämiseksi automatisoimalla prosesseja. Voit esimerkiksi muodostaa yhteyden pankkeihin ja tuoda automaattisesti pankkitapahtumia. Sovellukset on helppo asentaa ja määrittää suoraan tällä sivulla. Valitse sovellus, jonka ominaisuuksista ja hinnoittelusta haluat lisätietoja.  

Tarkastele ehdotettujen sovellusten luetteloa valitsemalla **Yhteyssovellukset**-toiminto **Laajennusten hallinta** -sivulla.  

> [!NOTE]
> **Yhteyssovellukset**-sivun ensimmäisenä avaavan henkilön on sallittava laajennukset, jotta ulkoiseen palveluun voidaan muodostaa yhteys. Salli yhteyden muodostaminen kerran tai aina. Jos valitset yhteyden estämisen, etsi vastaavat sovellukset AppSourcesta.

Tämä ulkoinen palvelu luo luettelon liittyvistä sovelluksista maasi tai alueesi perusteella

## <a name="recommended-apps"></a>Suositellut sovellukset

Microsoft-kumppanit ja -jälleenmyyjät voivat luoda sovelluksia, joita he voivat käyttää sellaisten sovellusten luetteloiden laatimiseen, joita he usein suosittelevat asiakkailleen. Jos näin tehdään, ja sovellus on otettu käyttöön vuokraajassasi, sovellukset ovat käytettävissä **Suositellut sovellukset** -sivulla. Siellä voit lukea kustakin sovelluksesta ja päättää, asennetaanko se.

> [!NOTE]
> Jos olet Microsoft-kumppani tai -jälleenmyyjä ja olet kiinnostunut tarjoamaan luettelon suositelluista sovelluksista, katso [Suositellut sovellukset AppSourcesta](/dynamics365/business-central/dev-itpro/administration/recommend-apps) -kohta hallintosisällössä.

## <a name="see-also"></a>Katso myös

[Sovellusten asentaminen ja asennusten poistaminen](ui-extensions-install-uninstall.md)  
[Business Centralin mukauttaminen](ui-customizing-overview.md)  
[Muiden toimittajien Business Central -sovellukset](ui-extensions-other.md)  
[Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md)  
[Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta](sales-how-enable-payment-service-extensions.md)  
[Liiketoiminnan tietojen siirtäminen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[Muiden palveluntarjoajien [!INCLUDE[prod_short](includes/prod_short.md)]in sovellukset](ui-extensions-other.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
