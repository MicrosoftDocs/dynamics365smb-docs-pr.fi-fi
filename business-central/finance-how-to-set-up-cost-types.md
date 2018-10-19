---
title: "Kustannustyyppikartan määrittäminen | Microsoft Docs"
description: "Kustannustyyppikaavio on vastaava kuin pääkirjanpidon tilikartta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 37800664c79e501f1cf5dc41c12be6197fcb6bfd
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-cost-types"></a>Kustannustyyppien määrittäminen
Kustannustyyppikartta vastaa pääkirjanpidon tilikarttaa. Voit määrittää kustannustyyppikaavion seuraavilla tavoilla:  

-   Kustannustyyppien kaavioiden rakenne vastaa pääkirjanpidon tuloslaskelmatilejä. Sitten voit siirtää kirjanpidon tilikartan kustannustyyppikaavioon. Siirron jälkeen voit tehdä tarvittavat muutokset.  
-   Luo uusi kustannustyyppien kaavio tai lisää uudet kustannustyypit aiemmin luotuun kustannustyyppien kaavioon. Sinun on luotava jokainen uusi kustannustyyppi erikseen.  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Siirrä pääkirjanpidon tilikartta kustannustyyppikaavioon  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kustannustyyppikartta** ja valitse sitten liittyvä linkki.  
2.  Valitse **Hae kustannustyypit tilikartasta** -toiminto. Vahvista siirto valitsemalla valintaikkunassa **Kyllä**. Funktio käyttää tilikarttaa kustannustyyppikaavion luontiin.  

    Kustannustyyppikaavio sisältää nyt kaikki pääkirjanpidon tuloslaskelmat, mukaan lukien otsikot ja välisummat. Voit tarvittaessa muuttaa kustannustyyppejä. Voit esimerkiksi poistaa kustannustyyppien kaksoiskappaleet.  

    > [!IMPORTANT]  
    >  **Rekisteröi kustannustyypit tilikartassa** -toiminto päivittää tilikartan ja kustannustyyppukaavion välisen suhteen. **Nro**-kenttä on täytetty ja vahvistettu, että jokaiselle KP-tilille on liitetty vain yksi kustannuslaji. Toiminto suoritetaan automaattisesti ennen KP-tapahtumien siirtämistä kustannuslaskentaan.  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-window"></a>Uuden kustannustyypin määrittäminen Kustannustyyppikartta-ikkunassa  
1.  Avaa **Kustannustyyppikartta**-ikkuna muokkaustilassa.  
2.  Täytä kentät tarvittaessa ohjeiden mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Voit määrittää ja ylläpitää kustannustyyppejä joko **Kustannustyypin kortti** -kortissa tai **Kustannustyyppikartta**-ikkunassa. Tässä toimenpiteessä määrität kustannustyypit **Kustannustyyppikartta**-ikkunassa.

3.  Kun olet luonut kaikki kustannustyypit, valitse **Sisennä kustannustyypit** -toiminto. Valitse valintaikkunassa **Kyllä**.  
4.  Linkitä uusi kustannustyyppi vastaavalle pääkirjanpidon tilille.  

    > [!IMPORTANT]  
    >  Jos olet antanut määritelmiä **Loppusumma**-rivien **Summausväli**-kentissä ennen **Sisennä kustannustyypit** -toiminnon suorittamista, määritelmät on annettava uudelleen, koska toiminto korvaa kaikki **Loppusumma**-kenttien arvot.  

## <a name="to-update-cost-types"></a>Päivitä kustannustyypit  
1.  Valitse **Kustannuslaskennan asetukset** -ikkunassa, haluatko kustannustyyppikaavion päivittyvän automaattisesti, kun tilikarttaa muutetaan.  
2.  Voit tehdä **Tasaa KP-tili** -kentässä valinnan seuraavista vaihtoehdoista:  

- **Ei tasausta** - Vastaavaa muutosta ei tehdä kustannustyyppikaaviossa, kun tilikarttaa muutetaan.  
- **Automaattinen** - Vastaava muutos tehdään kustannustyyppikaaviossa, kun muutat tilikartan.  
- **Kysy** - Näkyviin tulee sanoma, jossa kysytään, haluatko tehdä vastaavan muutoksen kustannustyyppien kaaviossa, kun muutat tilikarttaa.  

## <a name="see-also"></a>Katso myös  
[Kustannuslaskenta](finance-manage-cost-accounting.md)  
[Pääkirjanpitotilien ja kustannustyyppien välisen suhteen määrittäminen](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   
[Kustannuspaikkojen ja kustannuskohteiden määrittäminen tilikarttaan](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Kustannustyypin, kustannuspaikan ja kustannusobjektin saldot](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md)   
[Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md)   
[Tietoja kustannuslaskennasta](finance-about-cost-accounting.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

