---
title: Yritysten lisääminen yrityksen keskittimeen
description: Opi lisäämään yrityksiä muista Business Central -ympäristöistä yritystoimintoon, jotta voit hallita eri ympäristöjen välisiä töitä.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: accountant, accounting, company hub
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 773731ecc860e7d1ea0d13bbf9e6896a746544be
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927652"
---
# <a name="add-companies-to-your-company-hub"></a>Yritysten lisääminen yritystoimintoon

Yritystoiminnon avulla voit käsitellä työtäsi useiden yritysten välillä eri [!INCLUDE [prodshort](includes/prodshort.md)] -ympäristöissä. Voit lisätä ympäristöjä ja yrityksiä manuaalisesti, jos yritykset eivät näy automaattisesti yritystoiminnossa.  

Aivan yritystoiminnon aloitussivulla on **Asetukset**-valikko, josta voit siirtyä **Ympäristölinkit**-sivulle. Valitse vain **Uusi** ja täytä sitten tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

## <a name="environment-links"></a>Ympäristölinkit

Ympäristölinkki on kortti, jossa määritetään [!INCLUDE [prodshort](includes/prodshort.md)] -ympäristö, jossa vähintään yhden yrityksen isäntä toimii. Kunkin ympäristön kortin tiedot määrität sinä itse, ja voit myös muuttaa niitä tarvittaessa. **Ympäristölinkki**-kenttä on kuitenkin erityisen tärkeä – sitä tarvitaan yrityksen [!INCLUDE [prodshort](includes/prodshort.md)]iin pääsyyn. Tarkista, että linkki on oikein valintanauhan **Testaa yhteys** -toiminnon avulla. Linkki, johon sinun täytyy syöttää pisteitä lisättävän yrityksen isännöimisessä ympäristössä, ja sen täytyy sisältää Azure Active Directory ( Azure AD) -tunnus tai organisaation toimialuenimi. Jos toimialueeksi on määritetty esimerkiksi MyBusiness.com, linkki [!INCLUDE [prodshort](includes/prodshort.md)] -sovellukseen on ```https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1```. Muussa tapauksessa se näyttää suunnilleen tältä: ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```  

Linkkiä käytetään, kun yritys valitaan yritystoiminnossa.  

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Yritystoiminnon luettelossa olevan yrityksen toiminnot":::

> [!TIP]
> Jos käytät [!INCLUDE [prodshort](includes/prodshort.md)] -ohjelman maksutonta kokeiluversiota, voit helposti lisätä yrityksen vuokraajalle. Voit etsiä ympäristölinkin kopioimalla Azure Active Directory -tunnuksen Ohje & tuki -sivun **Vian etsintä** -osiosta. Ympäristön nimi on todennäköisesti oletusarvo, TUOTANTO. Lisää nämä tiedot **Ympäristölinkki**-kenttään, esimerkiksi ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1``` ja valitse sitten **Testaa yhteys**. Arviointiyritys lisätään luetteloon.
>
> Jos olet siirtynyt kolmenkymmenen päivän kokeiluyritykseen, My Companyyn, voit lisätä sen luetteloon valitsemalla **Lataa uudelleen/Lataa uudelleen kaikki yritykset** -toiminnon luettelossa.

## <a name="load-companies"></a>Lataa yritykset

Kun olet lisännyt ympäristösi, yritykset näkyvät automaattisesti. Jos kuitenkin tiedät, että uusi yritys on lisätty ympäristöön, voit päivittää luettelon valitsemalla **Lataa kaikki yritykset uudelleen** -toiminnon. Käytä samaa toimintoa tietojen päivittämiseen yritysten välillä.  

> [!TIP]
> Jotta voisit päivittää yritystoiminnon tiedot, sinun on voitava käyttää niiden yritysten tietoja, joista tiedot ovat peräisin.

## <a name="see-also"></a>Katso myös .

[Työnhallinta useiden yritysten välillä yrityksen keskittimessä](company-hub.md)  
[Ohje- ja tukiresurssit](product-help-and-support.md)  
