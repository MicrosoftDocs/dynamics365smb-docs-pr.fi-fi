---
title: Kulujen tai tuottojen kirjaaminen suoraan kirjanpitoon| Microsoft Docs
description: "Liiketoiminnan aktiviteeteille, joihin ei liity asiakirjaa, kuten pienille kuluille tai käteissuorituksille voi luoda liittyvät tapahtumat kirjaamalla päiväkirjarivit Yleinen päiväkirja -ikkunassa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 43065620f34a7ef02e5247e78acf306500f82d90
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-transactions-directly-to-the-general-ledger"></a>Tapahtumien kirjaaminen suoraan pääkirjanpitoon
Useimmat rahoitustapahtumat kirjataan pääkirjanpitoon erityisten yritysasiakirjojen, kuten ostolaskujen ja myyntitilausten välityksellä. Liiketoiminnan aktiviteeteille, joihin ei liity [!INCLUDE[d365fin](includes/d365fin_md.md)]-asiakirjaa, kuten pienille kuluille tai käteissuorituksille voi luoda liittyvät tapahtumat kirjaamalla päiväkirjarivit **Yleinen päiväkirja** -ikkunassa.

Yleiseen päiväkirjaan kirjataan tyypillisesti työntekijöiden liiketoimintaa varten käyttämät ovat varat myöhemmin hyvitettäväksi. Lisätietoja on kohdassa [Toimintaohje: Työntekijöiden kulujen kirjaaminen ja hyvittäminen](finance-how-record-reimburse-employee-expenses.md).

Yleisiä päiväkirjoja käytetään rahoitustapahtumien kirjaamiseen suoraan kirjanpitotileille sekä muille tileille, kuten pankki-, asiakas-, toimittaja- ja työtekijätileille. Yleisen päiväkirjan avulla kirjaaminen luo aina tapahtumia kirjanpitotileille. Näin tapahtuu silloinkin, kun kirjataan esimerkiksi päiväkirjan rivi asiakkaan tilille, koska tapahtuma kirjataan pääkirjanpidon myyntisaamisten tilille kirjausryhmän kautta. Voit mukauttaa yleistä päiväkirjaasi määrittämällä päiväkirjaerän tai -mallin. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

Toisin kuin tapahtumat, jotka on kirjattu asiakirjasta ja edellyttävät hyvityslaskuprosessia, voit peruuttaa yleiseen päiväkirjaan kirjattuja tapahtumia oikein. Lisätietoja on kohdassa [Toimintaohje: Kirjauksien peruuttaminen](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Tapahtumien kirjaaminen suoraan pääkirjanpitoon
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa liittyvä yleisen päiväkirjan erä. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).
3. Täytä tarvittaessa uuden päiväkirjarivin kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Toista vaihe 3 jokaiselle tapahtumalle, jonka haluat kirjata.

    > [!TIP]  
    > Jos haluat syöttää useita tapahtumarivejä yhden vastatilin rivin ylle, esimerkiksi yhdelle pankkitilille, valitse erän rivillä oleva **Ehdota vastasummaa** -valintaruutu **Yleisen päiväkirjan erät** -ikkunassa. Tällöin vastatilin rivin **Summa**-kenttä täytetään automaattisesti arvolla, joka vaaditaan tapahtumien täsmäyttämiseen.
5. Valitse **Kirjaa**-toiminto kirjataksesi tapahtumat määritetyille KP-tileille.

## <a name="see-also"></a>Katso myös
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Toimintaohje: Työntekijöiden kulujen kirjaaminen ja hyvittäminen](finance-how-record-reimburse-employee-expenses.md)  
[Toimintaohje: Kirjausten peruuttaminen](finance-how-reverse-journal-posting.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

