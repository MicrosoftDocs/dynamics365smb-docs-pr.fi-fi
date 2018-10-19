---
title: "Microsoft Flow -integroinnin vianmääritys| Microsoft Docs"
description: "Suorita vianmääritys ja selvitä, miten voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla rakennat automaattisen työkulun."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0818550021bf17e5a269d3e11f8db54b9ff80dfa
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a>Microsoft Flow -integroinnin vianmääritys – pyynnön URL-osoite on liian pitkä
Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja työnkulun osana Microsoft Flow'ssa.  

> [!NOTE]  
>   Sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja Flow-tili.  

Jos olet luomassa Microsoft Flow'n [!INCLUDE[d365fin](includes/d365fin_md.md)] -yhdistimellä, voit saada työnkulun luomisen jälkeen virhesanoman, jonka mukaan pyydetty URL-osoite on liian pitkä. Viesti voi olla esimerkiksi seuraavanlainen: **RequestUriTooLong**.

## <a name="cause"></a>Syy
Työnkulun käynnistyminen edellyttää, että se havaitsee tiedoissa muutoksia. Kun liittimet selvittävät, onko tiedoissa muutoksia, ne vertaavat välimuistiin tallennettuja tietoja lähteestä pyydettyihin uusiin tietoihin.  

Jos tietopyyntö luo liian pitkän URL-osoitteen, pyyntö epäonnistuu. Yleisiä syitä ovat esimerkiksi seuraavat:
- Yleisesti mikä tahansa taulukko, jossa on yli 250 riviä.
- Lähdetaulukot, joissa on useita tuhansia tietueita.

## <a name="workaround"></a>Ratkaisu
Ongelman voi kiertää seuraavasti:
1. Valitse epäonnistuneen työnkulun muokkaus.
2. Laajenna **Näytä lisäasetukset** työnkulun käynnistimessä.
3. Anna **Ohita määrä** -kenttään ohitettavien tietueiden määrä.  
Jos tietolähteenä käyttämässäsi taulukossa on esimerkiksi 4 000 tietuetta, anna ohittavien tietueiden määräksi 4 000.
4. Päivitä työnkulku.

> [!NOTE]  
> Yhdistimestä on tällä hetkellä käytössä beetaversio. Tietojen muutokset tullaan ottamaan huomioon tulevien versioiden päivityksissä.


## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md)  
[Käytön aloittaminen](product-get-started.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  

