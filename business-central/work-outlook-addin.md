---
title: Business Centralin käyttäminen Outlookin kanssa
description: 'Tämä palvelu integroituu kattavasti Microsoft 365:n kanssa, joten voit hallita kaikkea yrityksen asiakkaiden ja toimittajien kanssa tapahtuvaa viestintää suoraan Outlookissa.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'SMTP, mail, Microsoft 365'
ms.date: 04/21/2022
ms.author: jswymer
---
# <a name="use-business-central-as-your-business-inbox-in-outlook"></a>Business Central -sovelluksen käyttäminen yrityssähköpostina Outlookissa

[!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa apuohjelman, jonka avulla voit hallita liiketoiminnallisia vuorovaikutuksia asiakkaiden ja toimittajien kanssa suoraan Microsoft Outlookista. [!INCLUDE[prod_short](includes/prod_short.md)]in Outlook-apuohjelman avulla voit tarkastella asiakkaisiin ja toimittajiin liittyviä taloustietoja sekä luoda ja lähettää talousasiakirjoja, kuten tarjouksia ja laskuja.

[!INCLUDE[prod_short](includes/prod_short.md)] -apuohjelma koostuu kahdesta erillisestä apuohjelmista, jotka sisältävät seuraavat ominaisuudet:

- Kontaktien tiedot

   Tämä apuohjelma tarjoaa [!INCLUDE[prod_short](includes/prod_short.md)]in asiakas- tai toimittajatiedot Outlookin sähköposteissa ja kalenteritapaamisissa. Sen avulla voit myös luoda ja lähettää [!INCLUDE[prod_short](includes/prod_short.md)]in liiketoiminta-asiakirjoja, kuten myyntitarjouksia ja laskuja kontaktille.

- Asiakirjanäkymä

   Kun sähköpostin tekstissä lähetetään liiketoiminta-asiakirja, tämä apuohjelma antaa sähköpostiviestistä suoran linkin varsinaiseen liiketoiminta-asiakirjaan [!INCLUDE[prod_short](includes/prod_short.md)]issa.

## <a name="get-started"></a>Aloitus

1. Ensimmäinen asia on saada [!INCLUDE[prod_short](includes/prod_short.md)] -apuohjelma asennettua Outlookiin. Järjestelmänvalvoja on saattanut jo asentaa apuohjelman puolestasi. Jos et ole varma, tarkista asia järjestelmänvalvojalta tai katso seuraava vaihe ja tarkista, onko se asennettu.

    Jos apuohjelmaa ei ole asennettu puolestasi, lisätietoja on ohjeaiheessa [Apuohjelman asentaminen omaan käyttöön](admin-outlook.md#install). 

2. Kun apuohjelma on asennettu, voit käyttää **[!INCLUDE[prod_short](includes/prod_short.md)]** -apuohjelmaa mistä tahansa Outlookin uudesta tai olemassa olevasta sähköpostiviestistä tai kalenteritapaamisesta.

    Aloita kirjautumalla Outlookiin ja avaamalla sähköpostiviesti. Jos käytät Outlook-sovellusta, siirry sitten valintanauhaan ja etsi **[!INCLUDE[prod_short](includes/prod_short.md)]**.  Jos käytät Outlookia verkossa, Etsi sähköpostiviestin ylä- tai alareunasta ![Outlookin Business Central -apuohjelman kuvake.](media/outlook-business-central-icon.png) Voit myös siirtyä Lisää toimintoja -kohtaan ![Näytä lisää sähköpostitoimintoja Outlookissa.](media/outlook-more-actions-button.png) -painikkeen.

    ![Business Central -apuohjelmien käyttäminen Outlookissa.](media/outlook-business-central-addin.png)

   Jos olet asentanut lisäohjelman itse ja valinnut, että saat näytesähköpostin, tarkista Saapuneet-kansiosta tervetulosähköposti. Tämä sähköpostiviesti sisältää tietoja, joiden avulla pääset alkuun.

Kun käytät ensimmäistä kertaa apuohjelmaa, [!INCLUDE[prod_short](includes/prod_short.md)] -apuohjelman ruudussa sinua saatetaan pyytää kirjautumaan sisään. Valitse tässä tapauksessa **Kirjaudu sisään** ja kirjaudu Business Centraliin noudattamalla näyttöön tulevia ohjeita.

> [!TIP]
> Jos käytät uusia Outlookia verkossa, voit kiinnittää **[!INCLUDE[prod_short](includes/prod_short.md)]in** aina näkyviin sen sijaan, että sinun tarvitsee mennä Lisää toimintoja -painikkeeseen, jolloin voit tarkastella kontaktin tietoja samalla, kun selaat eri sähköposteja.

Lisätietoja on kohdassa [Outlook-verkkoversion apuohjelmien käyttäminen](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

## <a name="work-with-contacts-and-documents-using-the-contact-insights-add-in"></a>Kontaktien ja asiakirjojen käsitteleminen kontaktin Kontaktin tiedot -apuohjelman avulla

Oletetaan, että saat sähköpostiviestin asiakkaalta, joka haluaa tarjouksen tietyistä nimikkeistä. Voit avata [!INCLUDE[prod_short](includes/prod_short.md)] -apuohjelman suoraan Outlookissa, jossa lähettäjä tunnistetaan asiakkaaksi ja yrityksen asiakaskortti avataan. Tässä koontinäytössä näytetään asiakkaan yleiskuvauksen tiedot. Koontinäytössä voit myös siirtyä tiettyjen asiakirjojen lisätietoihin. Voit siirtyä tarkastelemaan myös asiakkaan myyntihistoriaa. Jos kyseessä on uusi yhteyshenkilö, voit luoda uuden asiakkaan [!INCLUDE[prod_short](includes/prod_short.md)]issa Outlookista poistumatta.  

Apuohjelmassa voit luoda myyntitarjouksen ja lähettää sen takaisin asiakkaalle ilman, että poistut Outlookista. Kaikki myyntitarjouksessa tarvitsemasi tiedot ovat käytettävissä Outlookin yrityssähköpostissa. Kun tiedot on syötetty, voit kirjata tarjouksen ja lähettää sen sähköpostitse. [!INCLUDE[prod_short](includes/prod_short.md)] luo myyntitarjouksen sisältävän .PDF-tiedoston ja liittää sen apuohjelmassa tekemääsi sähköpostiviestin luonnokseen.  

Jos vastaavasti saat sähköpostia toimittajalta, voit käsitellä toimittajia ja ostolaskuja apuohjelman avulla.  

Joskus haluat nähdä enemmän kenttiä kuin lisäohjelmassa on. Näin voi tapahtua esimerkiksi silloin, kun haluat täyttää laskun rivejä. Saat lisää työskentelytilaa, kun avaat apuohjelman erillisellä sivulla. Se on yhä osa Outlookia, mutta käytettävissä on enemmän tilaa. Muutokset tallennetaan automaattisesti samalla, kun syötät asiakirjan tietoja ponnahdusikkunaan. Seuraavissa osissa on perustietoja tehtävistä, joiden avulla saat yleisen käsityksen siitä, miten sitä käytetään.

> [!TIP]
> Tehtävät selittävät, kuinka apuohjelmaa käytetään sähköpostiviestissä. Voit kuitenkin tehdä saman Outlook-kalenteritapaamisista.

### <a name="look-up-a-business-contact-when-composing-an-email"></a>Työyhteyshenkilön haku sähköpostiviestin kirjoittamisen yhteydessä

1. Luo uusi sähköpostiviesti
2. Etsi **[!INCLUDE[prod_short](includes/prod_short.md)]** valintanauhasta ja valitse **Yhteystietojen tiedot**. Jos käytät Outlookia verkossa, valitse sähköpostiviestin alareunasta ![Outlookin Business Central -apuohjelman kuvake.](media/outlook-business-central-icon.png) > **Kontaktien tiedot**
3. Etsi ja valitse näyttöön tulevassa **[!INCLUDE[prod_short](includes/prod_short.md)]** -apuohjelmaruudussa haluamasi kontakti.

    Ruudussa näkyy kontaktin yleiskuvaus, ja kontakti lisätään sähköpostin **Vastaanottaja**-riville.

### <a name="view-and-change-the-contact-details-or-switch-company"></a>Yhteystietojen tarkasteleminen ja muuttaminen tai yrityksen vaihtaminen

[!INCLUDE[prod_short](includes/prod_short.md)] -apuohjelmaruudun yläosassa olevassa toimintopalkissa on useita toimintoja, joiden avulla saat kaivautua syvemmälle kontaktin yksityiskohtiin ja muuttaa asioita.

![Business Central -apuohjelman toimintopalkki Outlookissa.](media/outlook-addin-action-bar.png)

Voit esimerkiksi avata täydelliset kontaktitiedot niin kuin ne näkisit [!INCLUDE[prod_short](includes/prod_short.md)]issa. Jos työskentelet useamman kuin yhden [!INCLUDE[prod_short](includes/prod_short.md)] -yrityksen kanssa, voit helposti vaihtaa yritysten välillä.

### <a name="track-incoming-documents"></a>Saapuvien asiakirjojen seuranta

Ehkä käytät **Saapuvat asiakirjat** -luetteloa [!INCLUDE[prod_short](includes/prod_short.md)]issa, kun haluat seurata asiakirjoja, joita toimittajat lähettävät, kuten ostolasku, joka täytyy maksaa. Jos teet näin, voit helposti luoda Saapuvat asiakirjat -tietueita Outlook-apuohjelmasta ja sisällyttää sähköpostin liitteet.

1. Kun vastaanotat liitteen sisältävän toimittajan sähköpostin, valitse ![Outlookissa Business Central -apuohjelman kuvake.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Kontaktien tiedot**.  

2. Valitse apuohjelman toimintopalkissa **Näytä lisää toimintoja** ja valitse **Lähetä saapuviin asiakirjoihin...** -toiminto.  

### <a name="create-and-send-new-document-to-a-contact"></a>Uuden asiakirjan luominen ja lähettäminen kontaktille

1. Valitse valintanauhassa tai sähköpostiviestin alaosassa ![Outlookin Business Central -apuohjelman kuvake.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]** > **Uusi** ja valitse luotavan asiakirjan tyyppi, esimerkiksi **Myyntitarjous**.
2. Tee muutokset asiakirjaan **[!INCLUDE[prod_short](includes/prod_short.md)]** -lisäosan ruudussa.
3. Kun asiakirja on valmis lähetettäväksi kontaktille, valitse toimintopalkissa **Näytä lisää toimintoja** ja valitse **Lähetä sähköpostilla** -toiminto.

### <a name="attach-files-to-records"></a>Liitä tiedostoja tietueisiin

Sähköpostisi Saapuneet-kansio toimii usein saapuvien tiedostojen lähteenä, kun työnkulkuja käynnistetään tai niiden esto poistetaan. Tiedostot voivat sisältää esimerkiksi PDF-laskun maksuja, valokuvia tavaroista tai Word-asiakirjan vaatimuksia. Kun työskentelet Outlookissa Business Centralin tietueiden, kuten toimittajien, asiakkaiden, ostolaskujen tai myyntitilausten, parissa, voit liittää nämä tiedostot tietueisiin.

Voit liittää tiedostoja muutamalla eri tavalla. Yksi tapa on ladata tiedostoja laitteesta. Toinen tapa on lähettää sähköpostiin liitettyjä tiedostoja. Oletetaan esimerkiksi, että saat sähköpostiviestin, jossa on yhteyshenkilön tiedostot. Lisäosa näyttää automaattisesti kontaktitietueen, joka vastaa sähköpostin lähettäjää. Sieltä voit navigoida kontaktin asiakirjaan, kuten uusimpaan myyntitilaukseen. Kun olet tunnistanut tilauksen, johon sähköposti liittyy, voit nopeasti ladata tiedostot sähköpostista kyseiseen tilaukseen.

![Näyttää, miten sähköpostista lisätään liitteitä Business Centralin tietueisiin.](media/outlook-attach-files.png)

Kun asiakirja on liitetty, työtoverit voivat ladata ja tarkastella tiedostoa minkä tahansa Business Central -asiakkaan **Liitteet**-tietoruudussa. He voivat myös avata tiedoston kohteessa OneDrive ja jakaa ja tehdä yhteistyötä osastonsa kanssa.

#### <a name="how-to-attach-a-file"></a>Tiedoston liittäminen

1. Avaa sähköpostiviesti, valitse ![Outlookin Business Central -apuohjelman kuvake.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Kontaktien tiedot**.
2. Valitse apuohjelman toimintopalkissa **Näytä lisää toimintoja** > **Liitteet**.

    **Liitetyt asiakirjat** -sivu avautuu, ja näyttöön tulee luettelo asiakirjoista, jotka on jo liitetty tietueeseen.
3. Valitse **Liitetyt tiedostot...** ja valitse sitten jokin seuraavista vaihtoehdoista:

   - Lataa sähköpostiin liitetyt tai valitut tiedostot valitsemalla **Liitä sähköpostista**.
   - Valitse **Lataa tiedostosta**, jos haluat ladata yhden tai useita tiedostoja laitteesta.

> [!NOTE]
> Et voi liittää tiedostoja kaikkiin tietueisiin. Tämä ominaisuus on käytettävissä tietueissa, jotka käyttävät **Liitteet**-tietoruutua, kuten toimittajaa, asiakasta, ostolaskua tai myyntitilausta.

## <a name="view-a-document-from-an-email-using-the-document-view-add-in"></a>Asiakirjan tarkasteleminen sähköpostiviestistä Asiakirjanäkymä-apuohjelman avulla

Olipa kyseessä sähköpostiviesti, jonka olet lähettänyt tai vastaanottanut, voit näyttää minkä tahansa [!INCLUDE[prod_short](includes/prod_short.md)] -asiakirjan, kuten myyntitarjouksen, suoraan Outlookissa. Sieltä voit tehdä muutoksia ja navigoida liittyviin tietoihin &mdash; aivan kuten [!INCLUDE[prod_short](includes/prod_short.md)]issa.

Jos käytät Outlook-sovellusta, valitse vain sähköpostiviestin yläosassa **Asiakirjan linkki**. Jos kyseessä on Outlook verkossa, etsi asiakirjan viitelinkki sähköpostiviestistä. Viitelinkin teksti sisältää asiakirjanumeron, joka perustuu [!INCLUDE[prod_short](includes/prod_short.md)]-ohjelman käyttämiin numerosarjoihin. Esimerkiksi myyntitarjouksen linkki voisi olla esimerkiksi **Sales Quote S-QUO1000**.  

> [!TIP]
> Alkaen vuoden 2022 julkaisuaallosta 1, asiakirjat avautuvat uuteen selainikkunaan kaikilla ominaisuuksilla, jotka ovat tuttuja kohteesta [!INCLUDE [prod_short](includes/prod_short.md)]. Voit siirtyä asiakirjasta luetteloon ja takaisin, avata luetteloita Excelissä, lähettää asiakirjat tulostettavaksi sekä suorittaa tai esikatsella liittyviä raportteja. Myös kaikki tutut pikanäppäimet ovat saatavilla, kun avaat asiakirjoja Outlookista.  


## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Business Centralin hakeminen omaan mobiililaitteeseen](install-mobile-app.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Rahoitus](finance.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Outlookin vähimmäisvaatimukset](product-requirements.md#outlook)  
[Apuohjelmien käyttäminen Outlookin verkkoversiossa](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
