---
title: Pääkirjanpidon tapahtumien siirtäminen kustannustapahtumiin | Microsoft Docs
description: Voit siirtää pääkirjanpidon tapahtumat kustannustapahtumiin.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: c6eace42d460432df8ab4b72964408469fa0b563
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305847"
---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Pääkirjanpidon tapahtumien siirtäminen kustannustapahtumiin
Voit siirtää pääkirjanpidon tapahtumat kustannustapahtumiin.  

Ennen kuin suoritat prosessin pääkirjanpidon merkintöjen siirtämiseksi kustannusmerkintöihin, sinun täytyy laatia siirto manuaalisen korjauksen kirjaamisen välttämiseksi.  

## <a name="to-prepare-the-transfer"></a>Valmistele siirto  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Kustannuslaskennan asetukset** ja valitse sitten liittyvä linkki.  
2.  Varmista **Kustannuslaskennan asetukset** -sivulla, että **KP-siirron alkamispäivämäärä** -kenttään on määritetty oikea arvo.  
3.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Kustannustyyppikartta** ja valitse sitten liittyvä linkki.  
4.  Varmista **Kustannustyyppikortti** -sivulla, että kunkin kustannustyypin **KP-tilien väli** -kenttä on linkitetty oikein, jotta tapahtumat voidaan ottaa pääkirjanpidosta.  
5.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Tilikartta** ja valitse sitten liittyvä linkki.  
6.  Tarkista, että kunkin käsiteltävän pääkirjanpidon tilin **KP-tilin kortti** -sivulla, että **Kustannustyypin numero** -kenttä on linkitetty oikein kustannuslajiin. Lisätietoja on kohdassa [Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md).  
7.  Tarkista, että kaikilla kyseessä olevilla pääkirjanpidon tapahtumilla on dimensioarvot, jotka vastaavat kustannuspaikkaa ja kustannuskohdetta.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Siirrä pääkirjanpidon tapahtumat kustannustapahtumiin  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirrä KP-tapahtumat kustannuslaskentaan** ja valitse sitten liittyvä linkki.  
2.  Aloita siirto valitsemalla **Kyllä**. Prosessi siirtää kaikki pääkirjanpidon tapahtumat, joita ei ole jo siirretty.  

    Siirron aikana prosessi luo yhteyksiä tapahtumiin **Kustannustapahtuma** -taulukossa ja **Kustannusrekisteri** -taulukossa. Tämä mahdollistaa kustannustapahtumien lähteen jäljittämisen.  

## <a name="see-also"></a>Katso myös  
[Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md)   
[Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md)   
