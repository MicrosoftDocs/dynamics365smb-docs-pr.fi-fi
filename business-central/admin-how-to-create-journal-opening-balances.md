---
title: Kirjauskansion alkusaldojen luominen | Microsoft Docs
description: Business Central sisältää useita eräajoja, jotka helpottavat uuden määritetyn yrityksen vanhojen tilien saldojen siirtämistä. Voit helposti siirtää nämä tiedot ja kirjauskansion kirjaukset.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 612eb9cfa5c6cd45bf154f4813efa3b349f44841
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "796405"
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
