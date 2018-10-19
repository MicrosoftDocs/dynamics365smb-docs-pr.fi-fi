---
title: "Pääkirjanpidon tapahtumien siirtäminen kustannustapahtumiin | Microsoft Docs"
description: "Voit siirtää pääkirjanpidon tapahtumat kustannustapahtumiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 62ed00ef7ca278245b9cdd1a28a4ee70cf9a8f11
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Pääkirjanpidon tapahtumien siirtäminen kustannustapahtumiin
Voit siirtää pääkirjanpidon tapahtumat kustannustapahtumiin.  

Ennen kuin suoritat prosessin pääkirjanpidon merkintöjen siirtämiseksi kustannusmerkintöihin, sinun täytyy laatia siirto manuaalisen korjauksen kirjaamisen välttämiseksi.  

## <a name="to-prepare-the-transfer"></a>Valmistele siirto  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kustannuslaskennan asetukset** ja valitse sitten liittyvä linkki.  
2.  Varmista **Kustannuslaskennan asetukset** -ikkunassa, että **KP-siirron alkamispäivämäärä** -kenttään on määritetty oikea arvo.  
3.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kustannustyyppikartta** ja valitse sitten liittyvä linkki.  
4.  Varmista **Kustannustyyppikortti** -ikkunassa, että kunkin kustannustyypin **KP-tilien väli** -kenttä on linkitetty oikein, jotta tapahtumat voidaan ottaa pääkirjanpidosta.  
5.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.  
6.  Tarkista, että kunkin käsiteltävän pääkirjanpidon tilin **KP-tilin kortti** -ikkunassa, että **Kustannustyypin numero** . Lisätietoja on ohjeaiheessa [Pääkirjanpitotilien ja kustannustyyppien välisen suhteen määrittäminen](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).  
7.  Tarkista, että kaikilla kyseessä olevilla pääkirjanpidon tapahtumilla on dimensioarvot, jotka vastaavat kustannuspaikkaa ja kustannuskohdetta.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Siirrä pääkirjanpidon tapahtumat kustannustapahtumiin  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirrä KP-tapahtumat kustannuslaskentaan** ja valitse sitten liittyvä linkki.  
2.  Aloita siirto valitsemalla **Kyllä**. Prosessi siirtää kaikki pääkirjanpidon tapahtumat, joita ei ole jo siirretty.  

    Siirron aikana prosessi luo yhteyksiä tapahtumiin **Kustannustapahtuma** -taulukossa ja **Kustannusrekisteri** -taulukossa. Tämä mahdollistaa kustannustapahtumien lähteen jäljittämisen.  

## <a name="see-also"></a>Katso myös  
 [Kriteerit pääkirjanpidon tapahtumien siirtämiseksi kustannustapahtumiin](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Automaattinen siirto ja yhdistetyt tapahtumat](finance-automatic-transfer-combined-entries.md)   
 [Siirron tulokset](finance-results-of-the-transfer.md)   
 [Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md)   
 [Pääkirjanpitotilien ja kustannustyyppien välisen suhteen määrittäminen](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

