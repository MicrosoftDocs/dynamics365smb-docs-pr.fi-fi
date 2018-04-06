---
title: Linkin muodostaminen tietueista ulkoisiin tietoihin tai ohjelmiin | Microsoft Docs
description: "Liitä hyperlinkki asiakirjaan tai sivusto tiettyyn tietueeseen, kuten asiakkaaseen tai asiakirjaan."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a513f6e62c4ef8dcf9e484d0211feb3e857dc0f7
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a>Sivustojen, asiakirjojen tai ohjelmien linkkien lisääminen tietueissa
Voit lisätä tiettyyn tietueeseen, kuten asiakkaaseen, asiakirjaan tai myyntitilaukseen, linkin ulkoiseen asiakirjaan, sivustoon tai ohjelmaan. Voit myös lisätä linkin, joka avaa uuden, tyhjän sähköpostiviestin, joka on osoitettu tietylle vastaanottajalle. Joidenkin tietueiden korttisivulla, kuten asiakas- tai toimittajakorteissa, on **Kotisivu**-kenttä, jossa voit antaa verkko- eli URL-osoitteen. Toisaalla tässä artikkelissa on lisätietoja muiden linkkien sisällyttämisestä.

Kyse voi olla myös esimerkiksi tulostettujen laskujen vastaanottamisesta toimittajalta. Voit skannata ja tallentaa ne .pdf-tiedostoina SharePoint-sivustossa. Tämän jälkeen voit muodostaa [!INCLUDE[d365fin_md](includes/d365fin_md.md)]in ostolaskusta linkin vastaavaan SharePointissa olevaan laskuun. Voit muodostaa linkin nimikekortista vastaavaan sivuun toimittajan online-kuvastossa.

## <a name="to-add-a-link-on-a-record"></a>Linkin lisääminen tietueeseen   

1.  Avaa tietue, johon haluat liittää linkin (esimerkiksi asiakaskortti tai myyntitilaus). Jos haluat liittää linkin tietylle riville, kuten päiväkirjan riville, valitse kyseinen rivi.  

2.  Avaa **Linkit**-toiminnolla **Linkit**-ikkuna, jossa kaikki tietueeseen tällä hetkellä lisätyt linkit näkyvät.

3. Lisää uusi linkki valitsemalla **+uusi**.

4.  Anna **Linkin osoite** -kentässä

    -   Jos haluat linkittää tietokoneessa tai verkossa olevan tiedoston, anna tiedostopolun ja tiedoston koko nimi, kuten **C:Omat tiedostotLasku1.doc**.
    -   Luo linkki sivustoon antamalla verkko- eli URL-osoite, kuten **www.microsoft.com**.
    -   Luo linkki sivustoon antamalla verkko- eli URL-osoite, kuten **www.microsoft.com**.
    -   Luo linkki ohjelmaan antamalla ohjelmaan avaava merkkijono. Jos haluat esimerkiksi käynnistää OneNoten siten, että tietty sivu avautuu, anna **onenote:///C:Omat tiedostottesti.one**. Tai jos haluat että tyhjä, tietylle sähköpostitunnukselle osoitettu Outlook-sähköpostiviesti käynnistyy, anna **mailto:testalias**.  

5.  Kirjoita **Kuvaus**-kenttään linkkiä kuvaavat tiedot.  

6.  Valitse **Tallenna**.  

## <a name="to-delete-a-link-from-a-record"></a>Linkin poistaminen tietueesta  

Poista linkki valitsemalla **Linkit**-ikkunassa ensin **...** ja sitten **Poista**.

Jos poistat yksittäisen tietueen, kuten myyntitilausrivin, myyntitilauksen tai asiakkaan, kaikki tietueeseen liitetyt linkit poistetaan. Jos sen sijaan poistat tietueita käyttämällä eräajoa, kuten **Poista laskutetut myyntitilaukset**, linkit säilyvät tietokantaan tallennettuina. Voit poistaa linkit tietokannasta suorittamalla **Poista orvot tietuelinkit** -koodiyksikön. Voit tehdä valitsemalla ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvakkeen, kirjoittamalla **Poista orvot tietuelinkit** ja valitsemalla sitten aiheeseen liittyvän linkin.   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a>Katso myös  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

