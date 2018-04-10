---
title: Kirjauskansion alkusaldojen luominen | Microsoft Docs
description: "Business Central sisältää useita eräajoja, jotka helpottavat uuden määritetyn yrityksen vanhojen tilien saldojen siirtämistä. Voit helposti siirtää nämä tiedot ja kirjauskansion kirjaukset."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: be45ed1de52c92722d801da344163fdffc2a9073
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="create-journal-opening-balances"></a>Kirjauskansion alkusaldojen luominen
[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää useita eräajoja, jotka helpottavat uuden määritetyn yrityksen vanhojen tilien saldojen siirtämistä. Voit helposti siirtää nämä tiedot asiakkaan kirjauskansioon, toimittajan kirjauskansioon, nimikepäiväkirjaan tai KP-päiväkirjaan.

Ensimmäiseksi luodaan kokoonpanopaketti, johon sisältyvät kyseisten päiväkirjojen asetustaulukot. Seuraavassa toimenpiteessä oletetaan, että tämä vaihe on suoritettu. Lisätietoja on kohdassa [Yrityksen konfiguraation määrittäminen](admin-set-up-company-configuration.md). Näissä ohjeissa kuvataan seuraavat vaiheet, joihin kuuluu yhteistyökumppanin toimittaman paketin käyttöönotto.  

Varmista ennen aloittamista, että olet RapidStart Services -palvelun käyttöönottajan roolikeskuksen sivulla. Tämä sivu tarjoaa määritystyölle juuri oikean kontekstin. Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>Käytä päiväkirjan tapahtumia uuteen yritykseen  
1. Määritä uusi yritys ja ota sille käyttöön määrityspaketti. Lisätietoja on kohdassa [Yrityksen määrittämien ohjatun RapidStart-toiminnon avulla](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Uudessa yrityksessä ei ole tietoja kirjauskansion alkusaldoista.  

2. Avaa määritystyökirja ja tuo olemassa olevat tiedot asiakkaista, nimikkeistä, toimittajista ja pääkirjanpidosta. Lisätietoja on ohjeaiheessa [Asiakastietojen siirtäminen](admin-migrate-customer-data.md).  
3. Valitse esimerkiksi **Luo kirjanpitopäiväkirjan rivit** -toiminto.  
4. Täytä **Vaihtoehdot**-pikavälilehden tarvittavat kohdat ja määritä suodattimet. Syötä **Päiväkirjan malli** -kenttään nimi.  
5. Valitse **OK**-painike. Tietueet ovat nyt kirjauskansiossa, mutta summat ovat tyhjiä.  
6. Vie päiväkirjataulukko Exceliin ja syötä kirjaus- ja vastatilin tiedot manuaalisesti vanhoista tiedoista.
7. Tuo uuden yrityksen taulukon tiedot ja ota ne käyttöön. Kirjauskansion rivit ovat valmiita kirjausta varten.  
8. Valitse määritystyökirjassa kirjauskansion rivin taulukko ja valitse sitten **Tietokannan tiedot** -toiminto.  
9. Tarkista tiedot ja valitse **Kirjaa**-toiminto.  
10. Toista vaiheet tuodaksesi ja kirjataksesi muut mahdolliset avaussaldot.  

## <a name="see-also"></a>Katso myös  
[Kokoonpanojen käyttäminen uusissa yrityksissä](admin-apply-configuration-to-new-companies.md)  
[Yrityksen määrittäminen RapidStart Services -palvelun avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)
