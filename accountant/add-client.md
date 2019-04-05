---
title: Asiakkaiden hakeminen Dynamics 365 -kirjanpitäjäkokemukseen | Microsoft Docs
description: Lisätietoja nykyisten asiakkaiden lisäämisestä Dynamics 365:n Accountant Hubiin.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/23/2018
ms.author: edupont
ms.openlocfilehash: c7f0af8d3535f558567cd40c841909cd151ce313
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795844"
---
# <a name="add-clients-to-your-dashboard-in-include-d365acclongincludesd365acclongmdmd"></a>Asiakkaiden lisääminen koontinäyttöön [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)] -sovelluksessa
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Voit lisätä asiakkaan **Asiakkaat**-sivulla, jonka voit avata valitsemalla **Hallitse asiakkaita** -toiminnon valintanauhassa. Valitse vain **Uusi** ja täytä sitten tarvittavat kentät.  

> [!div class="mx-imgBorder"]
> ![Asiakkaan lisääminen](./media/accountant-add-client/manage-client.png)

Kunkin asiakaskortin tiedot määrität sinä itse, ja voit myös muuttaa niitä tarvittaessa. **Asiakkaan URL-osoite** -kenttä on kuitenkin erityisen tärkeä – sitä tarvitaan asiakkaan [!INCLUDE [d365fin](includes/d365fin_md.md)]iin pääsyyn. Valintanauhan **Tarkista asiakkaan URL-osoite** -toiminnon avulla voit tarkistaa, että linkki on annettu oikein. URL-osoite, joka on syötettävä, osoittaa asiakkaan [!INCLUDE [d365fin](includes/d365fin_md.md)] -sovellukseen ja sisältää tämän toimialueen osoitteen. Jos toimialueeksi on määritetty esimerkiksi MyBusiness.com, linkki [!INCLUDE [d365fin](includes/d365fin_md.md)] -sovellukseen on *https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1*.  

> [!NOTE]
>  Ennen toikokuun 2018 päivitystä määritetyn URL-osoitteen alussa olevan asiakkaan yrityksen nimen muoto oli erilainen. Nykyisessä [!INCLUDE [d365fin](includes/d365fin_md.md)] -versiossa muoto on ```https://businesscentral.dynamics.com/clientdomain?redirectedfromsignup=1```, jossa ```clientdomain``` viittaa asiakkaan toimialueeseen.  

Asiakkaan URL-osoitetta käytetään, kun valitset **Siirry yritykseen** -valikkovaihtoehdon [!INCLUDE [d365acc](includes/d365acc_md.md)] -koontinäytössä.  

### <a name="get-invited-to-a-clients-include-d365finlongincludesd365finlongmdmd"></a>Kutsun saaminen asiakkaan [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)] -ympäristöön
[!INCLUDE [d365fin](includes/d365fin_md.md)]ia käyttävä yritys voi kutsua sinut [!INCLUDE [d365fin](includes/d365fin_md.md)] -ympäristöönsä ulkoiseksi kirjanpitäjäksi. Saat kutsun, jos annat heille [!INCLUDE [d365acc](includes/d365acc_md.md)]issa käyttämäsi sähköpostiosoitteen, joka voi olla esimerkiksi <em>me@accountant.com</em>. Asiakkaan järjestelmänvalvoja voi sitten lisätä sinut järjestelmään suorittamalla ohjatun **Kutsu ulkoinen kirjanpitäjä** -toiminnon.  

Saat nyt asiakkaalta sähköpostiviestin, jossa on linkit asiakkaan [!INCLUDE [d365fin](includes/d365fin_md.md)]:een. Ensimmäinen linkki on kutsu, jolla saa yrityksen käyttöoikeuden. Avaa linkki ja hyväksy vaiheet, joilla sinut lisätään asiakkaan [!INCLUDE [d365fin](includes/d365fin_md.md)]:een. Toisen linkin avulla kyseinen asiakas lisätään [!INCLUDE [d365acc](includes/d365acc_md.md)]in koontinäyttöön edellä kuvatulla tavalla.  

Hyväksymällä kutsun kirjaudut sisään ja saat asiakkaan taloustietojen käyttöoikeuden **Kirjanpitäjä**-roolikeskuksesta. Lisätietoja on kohdassa [Kirjanpitäjän käyttökokemukset [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).  

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365acc](includes/d365acc_md.md)]in käytön aloittaminen](get-started.md)  
[[!INCLUDE[d365acc](includes/d365acc_md.md)]in vianmääritys](troubleshooting.md)  
