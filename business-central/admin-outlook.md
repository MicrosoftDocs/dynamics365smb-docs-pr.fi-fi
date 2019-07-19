---
title: Business Central -sovelluksen käyttäminen Outlookin kanssa | Microsoft Docs
description: Tämä palvelu integroituu kattavasti Office 365:n kanssa, joten voit hallita kaikkea yrityksen asiakkaiden ja toimittajien kanssa tapahtuvaa viestintää suoraan Outlookissa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 06/28/2019
ms.author: edupont
ms.openlocfilehash: 9248d39ed447f8c590db708567790edfd64da0db
ms.sourcegitcommit: e8abfb78e13f3c29035087b09d7930f2950ab7a3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2019
ms.locfileid: "1717582"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Business Central -sovelluksen käyttäminen yrityssähköpostina Outlookissa
[!INCLUDE[d365fin](includes/d365fin_md.md)] esittelee mahdollisuuden hallita liiketoiminnallisia vuorovaikutuksia asiakkaiden ja toimittajien kanssa suoraan Microsoft Outlookista. [!INCLUDE[d365fin](includes/d365fin_md.md)]in Outlook-apuohjelmien avulla voit tarkastella asiakkaisiin ja toimittajiin liittyviä taloustietoja sekä luoda ja lähettää talousasiakirjoja, kuten tarjouksia ja laskuja.  

## <a name="getting-the-add-in"></a>Apuohjelman hakeminen
Outlookin [!INCLUDE[d365fin](includes/d365fin_md.md)] -apuohjelman käytön aloittaminen on helppoa. Voit määrittää asetusten ohjatussa määritysoppaassa **Määritä Outlookin yrityssähköposti** itsesi ja organisaation välisen yhteyden, jos yrityksessä on käytössä Office 365. Sinun on vain annettava Office 365:n käyttäjätunnus ja salasana. [!INCLUDE[d365fin](includes/d365fin_md.md)]in apuohjelmat lisätään tämän jälkeen automaattisesti Outlookiin. Lisätietoja on kohdassa [Outlookin vähimmäisvaatimukset](product-requirements.md#outlook).  

Kun sitten avaat Outlookin, näet Dynamics 365 Business Centralin järjestelmänvalvojan lähettämän sähköpostiviestin. Uudet apuohjelmat lisätään Outlookin valintanauhaan, [!INCLUDE[d365fin](includes/d365fin_md.md)]in apuohjelmat näkyvät Outlook Web Appissa heti sähköpostiviestin perustekstin ylä- tai alapuolella. Apuohjelmat päivitetään ajoittain, ja saat ilmoituksen, kun uusi versio on valmiina Outlookissa.  

Jotkin Office 365:ää käyttävät yrityksen rajoittavat käyttäjien oikeuksia ottaa apuohjelmia käyttöön. Varmista tämän vuoksi, että Office 365 -tilauksesi sisältää sähköpostin ja mahdollistaa apuohjelmien käyttämisen. Jos haluat kokeilla apuohjelma joka tapauksessa, voit [kokeilla Office 365:ää maksutta](https://products.office.com/try).  

## <a name="using-the-contact-insights-add-in"></a>Kontaktien tiedot -apuohjelman käyttäminen
Oletetaan, että saat sähköpostiviestin asiakkaalta, joka haluaa tarjouksen tietyistä nimikkeistä. Voit avata [!INCLUDE[d365fin](includes/d365fin_md.md)] -apuohjelman suoraan Outlookissa, jossa lähettäjä tunnistetaan asiakkaaksi ja yrityksen asiakaskortti avataan. Tässä koontinäytössä näytetään asiakkaan yleiskuvauksen tiedot. Koontinäytössä voit myös siirtyä tiettyjen asiakirjojen lisätietoihin. Voit siirtyä tarkastelemaan myös asiakkaan myyntihistoriaa. Jos kyseessä on uusi asiakas, voit luoda uuden asiakkaan [!INCLUDE[d365fin](includes/d365fin_md.md)]issa Outlookista poistumatta.  

Apuohjelmassa voit luoda myyntitarjouksen ja lähettää sen takaisin asiakkaalle ilman, että poistut Outlookista. Kaikki myyntitarjouksessa tarvitsemasi tiedot ovat käytettävissä Outlookin yrityssähköpostissa.  
Kun tiedot on syötetty, voit kirjata tarjouksen. Tämän jälkeen voit lähettää sen sähköpostitse. [!INCLUDE[d365fin](includes/d365fin_md.md)] luo myyntitarjouksen sisältävän .PDF-tiedoston ja liittää sen apuohjelmassa tekemääsi sähköpostiviestin luonnokseen.  

Jos vastaavasti saat sähköpostia toimittajalta, voit käsitellä toimittajia ja ostolaskuja apuohjelman avulla.  

Joskus haluat nähdä enemmän kenttiä kuin lisäohjelmassa on. Näin voi tapahtua esimerkiksi silloin, kun haluat täyttää laskun rivejä. Saat lisää työskentelytilaa, kun avaat apuohjelman erillisellä sivulla. Se on yhä osa Outlookia, mutta käytettävissä on enemmän tilaa. Muutokset tallennetaan automaattisesti samalla, kun syötät asiakirjan tietoja ponnahdusikkunaan. Kun asiakirjan tiedot on annettu, voit valita **OK**-painikkeen. Kun apuohjelman kehys valitaan, Outlook päivittää ponnahdusikkunaan tekemäsi muutokset automaattisesti asiakirjaan.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Laskujen luominen kokouksen tapaamisista
Joissakin yrityksissä kaikki laskutettavat tapaamiset kirjataan Outlookin kalenteriin. Voit luoda [!INCLUDE[d365fin](includes/d365fin_md.md)]issa asiakkaalle laskun suodaan kalenterinimikkeestä: Avaa ensin tapaaminen ja sitten [!INCLUDE[d365fin](includes/d365fin_md.md)]in apuohjelma. Etsi aiemmin luodut tiedot tai luo lasku tai muu myyntiasiakirja suoraan sovelluksessa.  

## <a name="doing-quick-document-lookup"></a>Asiakirjan pikahaku
[!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakirjalinkkien apuohjelman avulla voit ottaa sähköpostiviesteissä mainitut asiakirjat nopeasti käyttöön. Apuohjelma on sähköpostiviestin käytettävissä, jos viestin leipätekstin asiakirjanumero tunnistetaan. Apuohjelman avaaminen mahdollistaa asiakirjan nopean käyttämisen.  

Jos vastaanotat esimerkiksi sähköpostiviestin, joka sisältää tekstin *S-QUO100*, [!INCLUDE[d365fin](includes/d365fin_md.md)] tunnistaa sen myyntitarjoukseksi. Tämän jälkeen voit avata asiakirjan Outlookissa. Valitse Outlookissa **Asiakirjalinkit**-painike, joka on heti sähköpostiviestin leipätekstin yläpuolella. Valitse Outlookin verkkosovelluksessa sähköpostiviestin leipätekstin *S-QUO1001*-teksti.  

Voit muokata Asiakirjalinkit-apuohjelmassa asiakirjaa ja suorittaa sille toimintoja samoin kuin [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.

## <a name="adding-the-add-ins-manually"></a>Apuohjelmien lisääminen manuaalisesti
Joissakin tapauksissa apuohjelmia ei lisätä automaattisesti Outlookiin. Vaikka sinä tai kollegasi suoritti avustetun asennusoppaan yrityksen puolesta, [!INCLUDE[d365fin](includes/d365fin_md.md)] ei ehkä näy Outlookissa. Jos tämä ongelma esiintyy, voit lisätä [!INCLUDE[d365fin](includes/d365fin_md.md)]in apuohjelmat manuaalisesti.  

Tarkista ensin, että voit käyttää apuohjelmia Office 365 -tililläsi. Avaa vain Outlook selaimessa ja lisää URL-osoitteeseen `/owa/#path=/options/manageapps` osoiterivillä. **Apuohjelmien hallinta** -sivu avautuu, ja voit ottaa [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttöön Outlookissa. Kun siirryt takaisin Outlookiin, [!INCLUDE[d365fin](includes/d365fin_md.md)]in pitäisi olla käytettävissä.  

Voit varmistaa myös Outlookin työpöytäversiossa, että [!INCLUDE[d365fin](includes/d365fin_md.md)] on mainittu **Apuohjelmien hallinta** -sivulla.  

Jos [!INCLUDE[d365fin](includes/d365fin_md.md)]ia ei voi edelleenkään käyttää, sinun on haettava kummassakin tapauksessa apuohjelman kokoonpanotiedostot. Pyydä lisätietoja Office 365:n järjestelmänvalvojalta.

## <a name="see-also"></a>Katso myös

[Käytön aloittaminen](product-get-started.md)  
[Business Central -sovelluksen hakeminen omaan mobiililaitteeseen](install-mobile-app.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Rahoitus](finance.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
