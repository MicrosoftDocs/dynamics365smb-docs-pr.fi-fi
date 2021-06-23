---
title: Business Central -sovelluksen käyttäminen Outlookin kanssa | Microsoft Docs
description: Tämä palvelu integroituu kattavasti Microsoft 365:n kanssa, joten voit hallita kaikkea yrityksen asiakkaiden ja toimittajien kanssa tapahtuvaa viestintää suoraan Outlookissa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2c8746098081a8f0b961f6ab2efd11c491104acc
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115360"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Business Central -sovelluksen käyttäminen yrityssähköpostina Outlookissa

[!INCLUDE[prod_short](includes/prod_short.md)] esittelee mahdollisuuden hallita liiketoiminnallisia vuorovaikutuksia asiakkaiden ja toimittajien kanssa suoraan Microsoft Outlookista. [!INCLUDE[prod_short](includes/prod_short.md)]in Outlook-apuohjelmien avulla voit tarkastella asiakkaisiin ja toimittajiin liittyviä taloustietoja sekä luoda ja lähettää talousasiakirjoja, kuten tarjouksia ja laskuja.  

## <a name="getting-the-add-in"></a>Apuohjelman hakeminen
Outlookin [!INCLUDE[prod_short](includes/prod_short.md)] -apuohjelman käytön aloittaminen on helppoa. Voit määrittää asetusten ohjatussa määritysoppaassa **Määritä Outlookin yrityssähköposti** itsesi ja organisaation välisen yhteyden, jos yrityksessä on käytössä Microsoft 365. Yksinkertaista Microsoft 365 -käyttäjänimen ja -salasanan määrittämistä pyydettäessä, ja kerro meille, haluatko saada näytesähköpostiviestin. [!INCLUDE[prod_short](includes/prod_short.md)]in apuohjelmat lisätään tämän jälkeen automaattisesti Outlookiin. Lisätietoja on kohdassa [Outlookin vähimmäisvaatimukset](product-requirements.md#outlook).  

Kun sitten avaat Outlookin, näet *Dynamics 365 Business Centralin järjestelmänvalvojan* lähettämän sähköpostiviestin. Uudet apuohjelmat lisätään Outlookin valintanauhaan, ja [!INCLUDE[prod_short](includes/prod_short.md)]in apuohjelmat näkyvät selaimessa heti sähköpostiviestin perustekstin ylä- tai alapuolella. Apuohjelmat päivitetään ajoittain, ja saat ilmoituksen, kun uusi versio on valmiina Outlookissa.  

> [!TIP]
> Jos käytät uutta Outlookia verkossa [!INCLUDE[prod_short](includes/prod_short.md)]in apuohjelmat voivat olla piilotettuina **Lisää toimintoja** -kohdassa. Jos käytät apuohjelmaa usein, voit kiinnittää sen niin, että se näkyy aina heti. Lisätietoja on kohdassa [Outlook-verkkoversion apuohjelmien käyttäminen](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

Jos työskentelet useamman kuin yhden [!INCLUDE[prod_short](includes/prod_short.md)] -yrityksen kanssa, voit helposti vaihtaa yritysten välillä Outlookissa. Valitse apuohjelman toimintopalkista **Lisää toimintoja**, ja sen jälkeen näet vaihtoehdon, jolla voi siirtyä yritysten välillä.  

<!--TEMP-->
> [!NOTE]
> Yritysten välillä siirtyminen edellyttää [!INCLUDE[prod_short](includes/prod_short.md)]in vuoden 2019 2. julkaisuaallon version ta tai uudemman, kuten [julkaisusuunnitelmassa ilmoitettiin](/dynamics365-release-plan/2019wave2/dynamics365-business-central/switch-between-companies-business-inbox-outlook).

Jotkin Microsoft 365:ää käyttävät yritykset rajoittavat käyttäjien oikeuksia ottaa apuohjelmia käyttöön. Varmista tämän vuoksi, että Microsoft 365 -tilauksesi sisältää sähköpostin ja mahdollistaa apuohjelmien käyttämisen. Jos haluat kokeilla apuohjelmaa joka tapauksessa, [voit kokeilla Microsoft 365:ää maksutta](https://www.microsoft.com/microsoft-365/try).  

## <a name="using-the-contact-insights-add-in"></a>Kontaktien tiedot -apuohjelman käyttäminen
Oletetaan, että saat sähköpostiviestin asiakkaalta, joka haluaa tarjouksen tietyistä nimikkeistä. Voit avata [!INCLUDE[prod_short](includes/prod_short.md)] -apuohjelman suoraan Outlookissa, jossa lähettäjä tunnistetaan asiakkaaksi ja yrityksen asiakaskortti avataan. Tässä koontinäytössä näytetään asiakkaan yleiskuvauksen tiedot. Koontinäytössä voit myös siirtyä tiettyjen asiakirjojen lisätietoihin. Voit siirtyä tarkastelemaan myös asiakkaan myyntihistoriaa. Jos kyseessä on uusi yhteyshenkilö, voit luoda uuden asiakkaan [!INCLUDE[prod_short](includes/prod_short.md)]issa Outlookista poistumatta.  

Apuohjelmassa voit luoda myyntitarjouksen ja lähettää sen takaisin asiakkaalle ilman, että poistut Outlookista. Kaikki myyntitarjouksessa tarvitsemasi tiedot ovat käytettävissä Outlookin yrityssähköpostissa.  
Kun tiedot on syötetty, voit kirjata tarjouksen. Tämän jälkeen voit lähettää sen sähköpostitse. [!INCLUDE[prod_short](includes/prod_short.md)] luo myyntitarjouksen sisältävän .PDF-tiedoston ja liittää sen apuohjelmassa tekemääsi sähköpostiviestin luonnokseen.  

Jos vastaavasti saat sähköpostia toimittajalta, voit käsitellä toimittajia ja ostolaskuja apuohjelman avulla.  

Joskus haluat nähdä enemmän kenttiä kuin lisäohjelmassa on. Näin voi tapahtua esimerkiksi silloin, kun haluat täyttää laskun rivejä. Saat lisää työskentelytilaa, kun avaat apuohjelman erillisellä sivulla. Se on yhä osa Outlookia, mutta käytettävissä on enemmän tilaa. Muutokset tallennetaan automaattisesti samalla, kun syötät asiakirjan tietoja ponnahdusikkunaan. Kun asiakirjan tiedot on annettu, voit valita **OK**-painikkeen. Kun apuohjelman kehys valitaan, Outlook päivittää ponnahdusikkunaan tekemäsi muutokset automaattisesti asiakirjaan.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Laskujen luominen kokouksen tapaamisista
Joissakin yrityksissä kaikki laskutettavat tapaamiset kirjataan Outlookin kalenteriin. Voit luoda [!INCLUDE[prod_short](includes/prod_short.md)]issa asiakkaalle laskun suodaan kalenterinimikkeestä: Avaa ensin tapaaminen ja sitten [!INCLUDE[prod_short](includes/prod_short.md)]in apuohjelma. Etsi aiemmin luodut tiedot tai luo lasku tai muu myyntiasiakirja suoraan sovelluksessa.  

## <a name="doing-quick-document-lookup"></a>Asiakirjan pikahaku
[!INCLUDE[prod_short](includes/prod_short.md)]in asiakirjalinkkien apuohjelman avulla voit ottaa sähköpostiviesteissä mainitut asiakirjat nopeasti käyttöön. Apuohjelma on sähköpostiviestin käytettävissä, jos viestin leipätekstin asiakirjanumero tunnistetaan. Apuohjelman avaaminen mahdollistaa asiakirjan nopean käyttämisen.  

Jos vastaanotat esimerkiksi sähköpostiviestin, joka sisältää tekstin *S-QUO100*, [!INCLUDE[prod_short](includes/prod_short.md)] tunnistaa sen myyntitarjoukseksi. Tämän jälkeen voit avata asiakirjan Outlookissa. Valitse Outlookissa **Asiakirjalinkit**-painike, joka on heti sähköpostiviestin leipätekstin yläpuolella. Valitse Outlookin verkkosovelluksessa sähköpostiviestin leipätekstin *S-QUO1001*-teksti.  

Voit muokata Asiakirjalinkit-apuohjelmassa asiakirjaa ja suorittaa sille toimintoja samoin kuin [!INCLUDE[prod_short](includes/prod_short.md)]issa.

## <a name="adding-the-add-ins-manually"></a>Apuohjelmien lisääminen manuaalisesti
Joissakin tapauksissa apuohjelmia ei lisätä automaattisesti Outlookiin. Vaikka sinä tai kollegasi suoritti avustetun asennusoppaan yrityksen puolesta, [!INCLUDE[prod_short](includes/prod_short.md)] ei ehkä näy Outlookissa. Jos tämä ongelma esiintyy, voit lisätä [!INCLUDE[prod_short](includes/prod_short.md)]in apuohjelmat manuaalisesti.  

Tarkista ensin, että voit käyttää apuohjelmia Microsoft 365 -tililläsi. Avaa Outlook selaimessa ja avaa sitten viesti. Valitse **Lisää toimintoja** (...) viestin yläosassa ja valitse sitten luettelon alaosasta **Hae apuohjelmia**. Näyttöön avautuu **Outlookin apuohjelmat** -sivu, jossa voit ottaa käyttöön kohteen [!INCLUDE[prod_short](includes/prod_short.md)] Outlookia varten. Kun siirryt takaisin Outlookiin, [!INCLUDE[prod_short](includes/prod_short.md)]in pitäisi olla käytettävissä.  

Voit varmistaa myös Outlookin työpöytäversiossa, että [!INCLUDE[prod_short](includes/prod_short.md)] on mainittu **Hae apuohjelmia** -sivulla.  

Jos [!INCLUDE[prod_short](includes/prod_short.md)]ia ei voi edelleenkään käyttää, sinun on haettava kummassakin tapauksessa apuohjelman kokoonpanotiedostot. Pyydä lisätietoja Microsoft 365:n järjestelmänvalvojalta.

## <a name="using-other-email-accounts"></a>Muiden sähköpostitilien käyttäminen

Apuohjelmat on suunniteltu Microsoft 365:n kanssa käytettäväksi. Jos käytät paikallista [!INCLUDE[prod_short](includes/prod_short.md)] -versiota, järjestelmänvalvoja tietää, voitko käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in apuohjelmia Outlookissa. Lisätietoja on ohjeaiheessa [Mitä sähköpostiosoitetta voin käyttää [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman kanssa?](/dynamics365/business-central/across-faq#email), ja [Ominaisuudet, jotka vaativat tiettyjä olosuhteita](/dynamics365/business-central/dev-itpro/features-not-implemented-on-premises#features-that-require-specific-circumstances?toc=/dynamics365/business-central/toc.json) -artikkelin ja [Miksei Outlook-apuohjelma toimi käyttäjieni osalta?](/dynamics365/business-central/dev-itpro/faq#why-doesnt-the-outlook-add-in-work-for-my-users?toc=/dynamics365/business-central/toc.json) -osassa yleisen FAQ-sisällön hallintasisällössä.  

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on [Microsoft Learnissa](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

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