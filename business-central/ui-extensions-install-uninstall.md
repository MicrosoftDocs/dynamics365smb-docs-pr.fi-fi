---
title: Sovellusten asentaminen ja asennusten poistaminen
description: Lisätietoja sovellusten ja laajennusten asentamisesta ja asennusten poistamisesta Business Centralissa.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'app, add-in, manifest, customize, install, uninstall'
ms.search.form: '2500, 20350'
ms.date: 09/22/2022
ms.author: solsen
---

# Laajennusten (sovellusten) asentaminen ja asennusten poistaminen Business Centralissa

Voit muuttaa [!INCLUDE[prod_short](includes/prod_short.md)]ia asentamalla sovelluksia, jotka esimerkiksi sisältävät lisätoimintoja, muuttavat toimintaa tai antavat uusien verkkopalveluiden käyttöoikeuden. Lisätietoja on kohdassa [Business Centralin mukauttaminen laajennusten avulla](ui-extensions.md).

> [!NOTE]
> Jos haluat asentaa AppSourcen sovelluksia tai poistaa niitä tai lisätä vuokraajakohtaisia sovelluksia, sinulla on oltava vaaditut käyttöoikeudet. Sinun täytyy olla jäsen joko EXTEND. MGT. - ADMIN -käyttäjäryhmässä tai sinulla on oltava EXTEND. MGT. - ADMIN -käyttöoikeudet. Jos olet järjestelmänvalvoja, voit määrittää käyttäjäryhmiä ja käyttöoikeuksia yrityksesi muille käyttäjille.
>
> Jos haluat käyttää laajennuksen mahdollistamaa toimintoa, kuten avata sivuja, suorittaa raportteja tai valita toimintoja, sinulla on oltava käyttöoikeuksien joukko, joka on asennettu laajennuksen osana.

Jos haluat käyttää laajennuksen mahdollistamaa toimintoa, kuten avata sivuja, suorittaa raportteja tai valita toimintoja, sinulla on oltava käyttöoikeuksien joukko, joka on asennettu laajennuksen osana.

## <a name="install"></a>Laajennuksen asentaminen

Sovelluksia ja laajennuksia hallitaan **Laajennusten hallinta** -sivulla. Tämä sivu löytyy kotisivulta. Vaihtoehtoisesti valitse **Hae sivua tai raporttia** -kuvake ![Lamppu, joka avaa Kerro-toiminnon.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") oikeassa yläkulmassa, syötä **Laajennus** ja valitse sitten liittyvä linkki.  

Uusia sovelluksia on saatavana kaupasta osoitteessa [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Kauppapaikka sisältää kaikki käytettävissä olevat sovellukset, joita [!INCLUDE[prod_short](includes/prod_short.md)] käyttää. Se sisältää myös muiden Microsoft-tuotteiden sovellukset ja sisältöpaketit. Määritä soveltuvat suodattimet, tutustu kunkin laajennuksen tietoihin ja hae laajennus [!INCLUDE[prod_short](includes/prod_short.md)]iin.  

> [!NOTE]  
> Kirjaudu sivustoon [AppSource.microsoft.com](https://appsource.microsoft.com/) [!INCLUDE[prod_short](includes/prod_short.md)]issa käyttämäsi sähköpostitilin tiedoilla. Saman sähköpostitilin käyttäminen myös muissa palveluissa ja tuotteissa takaa sujuvan käyttökokemuksen.  

Pääset AppSourceen myös käyttämällä sovellusta [!INCLUDE[prod_short](includes/prod_short.md)]. Tällä hetkellä asennettuna olevat sovellukset näkyvät **Laajennusten hallinta** -sivulla. Voit avata **Laajennuskauppa**-sivun, jossa näkyvät AppSourcessa tällä hetkellä käytettävissä olevat [!INCLUDE[prod_short](includes/prod_short.md)]in sovellukset. Jos valitset *Lisää sovelluksia* -linkin, sinut siirretään sivustolle [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Kun valitset sovelluksen, voit lukea tietoja sovelluksesta ja hakea lisätietoja käyttämällä sovelluksen Ohje-toimintoa. Kun haluat noutaa sovelluksen, sinun on hyväksyttävä käyttöehdot. Jos noudat sovelluksen AppSource-sivustosta, sinut kirjataan sisään sovellukseen [!INCLUDE[prod_short](includes/prod_short.md)] asennuksen viimeistelemiseksi.  

Sovelluksen asentamisen jälkeen se on ehkä määritettävä. Jotkin sovellukset edellyttävät, että annat tietoja ennen sovelluksen käyttämistä. Kun olet esimerkiksi asentanut **PayPal Payments Standard** -sovelluksen, sähköposti tai kauppiastilin tunnus on määritettävä PayPal-tiliä varten. Jos haluat määrittää sovelluksen tai selvittää tarvitsemasi tiedot, valitse **Asennetut laajennukset** -sivulla **Määritä**-toiminto.  

Muissa sovelluksissa esimerkiksi yksinkertaisesti lisätään kenttiä olemassa olevalle sivulle tai lisätään uusi sivu.

Jos poistat sovelluksen asennuksen ja haluat ottaa sen takaisin käyttöön, voit asentaa sovelluksen uudelleen. Kun poistat käytössäsi olleen sovelluksen asennuksen, tiedot säilytetään. Jos siis asennat sovelluksen uudelleen, tiedot ovat yhä käytettävissäsi. Jotkin sovellukset ovat pakollisia. Niiden sovellusten asennuksen poistaminen **Laajennusten hallinta** -sivulla on estetty. Jos yrität tehdä niin, näyttöön avautuu virhesanoma.

Osa on Microsoftin sovelluksia, osa [muiden yritysten](ui-extensions-other.md) sovelluksia. Kaikki sovellukset testataan, ennen kuin ne ovat käyttäjien käytettävissä. Suosittelemme kuitenkin lisätietoihin tutustumista sovelluksen mukana saatavien linkkien avulla ennen sovelluksen asentamista.

Microsoft tarjoaa seuraavat sovellukset:

* [AMC Banking 365 Fundamentals -laajennus](ui-extensions-amc-banking.md)
* [Ceridian Payroll](ui-extensions-ceridian-payroll.md)
* [Yritystoiminto](ui-extensions-company-hub.md)  
* [Dynamics GP -tietojen siirto](ui-extensions-dynamicsgp-data-migration.md)
* [Envestnet Yodlee Bank Feeds](ui-extensions-yodlee-bank-feeds.md)
* [Olennaiset liiketoimintanäkemykset](ui-extensions-essential-business-insights.md)
* [Kuvan analysointitoiminto](ui-extensions-image-analyzer.md)
* [Älykäs pilvi](ui-extensions-data-replication.md)
* [Älykäs Pilvipohja](ui-extensions-intelligent-cloud.md)  
* [Myöhästyneen maksun ennusteet](ui-extensions-late-payment-prediction.md)
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)
* [QuickBooks-tietojen siirto](ui-extensions-quickbooks-data-migration.md)
* [QuickBooks Online -tietojen siirto](ui-extensions-quickbooks-online-data-migration.md)
* [QuickBooks Payroll -tiedostojen tuonti](ui-extensions-quickbooks-payroll.md)
* [Myynti- ja varastoennuste](ui-extensions-sales-forecast.md)
* [Arvonlisäveroryhmä](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [DK – C5-tietojen siirto](ui-extensions-c5-data-migration.md)
* [DK - Maksut ja täsmäytykset](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK – Verotiedostomuodot](ui-extensions-tax-file-formats-dk.md)
* [Ison-Britannian postinumeroiden GetAddress.io-laajennus](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [US/CA/UK/AU/NZ/ZA - Maksusuositusehdotuksen lähettäminen](ui-extensions-send-remittance-advice.md)

## Laajennuksen määrittäminen
Sovelluksen asentamisen jälkeen se on ehkä määritettävä. Esimerkiksi **Sovelluksen [!INCLUDE[prod_short](includes/prod_short.md)] PayPal Payments Standard** -sovellukselle on määritettävä PayPal-tili. Jos näin on tehtävä, [!INCLUDE[prod_short](includes/prod_short.md)] kysyy käyttäjältä asennuksen valmistuttua, haluaako tämä määrittää sovelluksen heti. Sovellus saattaa vaatia asetukset toimiakseen.

Jos haluat määrittää sovelluksen heti ja se vaaditaan asetuksessa, [!INCLUDE[prod_short](includes/prod_short.md)] avaa vaaditun asetuksen. Asetus voi olla sivu, johon syötetään tietoja, tai asetusten ohjattu määritysopas, joka auttaa vaiheiden suorittamisessa. Jos et tee asetusta kerralla valmiiksi, voit käyttää **_Sovelluksen nimi_ – asetukset** -sivua, jolla sovelluksen asetukset kerrotaan. Pakolliset asetukset osoitetaan **lihavoinnilla**.

## Vuokraajakotaisen laajennuksen (PTE) lataaminen palvelimeen

Lataat PTE:n käyttämällä **Laajennuksen hallinta** -sivua. Valitse **Laajennuksen hallinta** -sivulla **Hallinta** ja valitse sitten **Lataa laajennus palvelimeen**. Valitse **Lataa ja ota käyttöön laajennus** -sivulla ladattava .app-tiedosto. Jatka valitsemalla **Hyväksy**-painike ja sitten **Ota käyttöön**-painike, jolloin PTE-käyttöönottoprosessi aloitetaan.

Jos PTE sisältää rikkovia mallin muutoksia, on mahdollista *pakottaa* sen lataaminen. Voit tehdä sen valitsemalla **Mallin synkronointi tila** -kohdassa **Pakota**-asetuksen. Näyttöön tulee vahvistusikkuna, jonka voi hyväksyä ennen jatkamista.  

## Sovelluksen asennuksen poistaminen

Sovelluksen asennus poistetaan **Laajennuksen hallinta** -sivulla. Jos haluat poistaa sovelluksen, valitse se sivulla ja valitse sitten **Poista asennus** -toiminto. Jos poistat sovelluksen asennuksen ja haluat ottaa sen takaisin käyttöön, voit asentaa sovelluksen uudelleen.

Kun poistat käytössäsi olleen sovelluksen asennuksen, tiedot säilytetään oletusarvoisesti mahdollista sovelluksen uudelleenasennusta varten. Voit myös valita tietojen poistamisen sovelluksen kanssa. Tätä toimintoa ohjataan **Poista laajennuksen tiedot** -kytkimellä. Tämä kytkin on oletusarvoisesti **pois päältä**. Kun yrität kytkeä sovelluksen **Poista laajennuksen tiedot** -kytkentä, avautuu vahvistusvalintaikkuna, jossa päälle kytkeminen edellyttää valintaa **Kyllä**. Kun **Poista laajennuksen tiedot** -kytkin on kytketty päälle, voit poistaa sovelluksen asennuksen, jonka yhteydessä sinua pyydetään vahvistamaan uudelleen, että haluat poistaa sovelluksen asennuksen ja poistaa tiedot.

> [!IMPORTANT]  
> - Saattaa olla muita sovelluksia, joiden toimiminen vaatii poistettavan sovelluksen tai on riippuvainen siitä. Näitä muita sovelluksia kutsutaan *riippuvaisiksi*. Et voi poistaa sovelluksen asennusta, ellei myös sen riippuvaisia poisteta.
> - Kun päätät poistaa sellaisen sovelluksen, jolla on vähintään yksi riippuvainen, avautuu vahvistusvalintaruutu, jossa riippuvaiset näkyvät ja sinulta kysytään, haluatko poistaa sovelluksen ja kaikki sen riippuvaiset. Jatkaaksesi sinun on valittava **Kyllä**.
> - Jos kytket **Poista laajennuksen tiedot** -kytkimen päälle, sovelluksen asennuksen poistaminen poistaa kaikki sovelluksen tiedot **sekä** kaikki riippuvaisten sovellusten tiedot. Toimintoa ei voi kumota.
> - Osa sovelluksista on pakollisia. Niiden asennuksen poistaminen **Laajennusten hallinta** -sivulla on estetty. Jos yrität tehdä niin, näyttöön avautuu virhesanoma.  

## Katso myös

[Business Centralin mukauttaminen](ui-customizing-overview.md)  
[Muiden toimittajien Business Central -laajennukset](ui-extensions-other.md)  
[Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md)  
[Asiakkaan maksujen ottaminen käyttöön PayPalin kautta](sales-how-enable-payment-service-extensions.md)  
[Liiketoiminnan tietojen siirtäminen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Ison-Britannian postinumeroiden GetAddress.io-laajennuksen määrittäminen](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[Muiden palveluntarjoajien [!INCLUDE[prod_short](includes/prod_short.md)]in laajennukset](ui-extensions-other.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]