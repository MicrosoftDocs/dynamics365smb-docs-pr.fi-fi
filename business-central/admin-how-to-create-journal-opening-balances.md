---
title: Kirjauskansion alkusaldojen luominen | Microsoft Docs
description: Business Central sisältää useita eräajoja, jotka helpottavat uuden määritetyn yrityksen vanhojen tilien saldojen siirtämistä. Voit helposti siirtää nämä tiedot ja kirjauskansion kirjaukset.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5e1bb8e34e70d1d906850c157107b9b9701c6c50
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779855"
---
# <a name="create-journal-opening-balances"></a>Kirjauskansion alkusaldojen luominen

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää useita eräajoja, jotka helpottavat uuden määritetyn yrityksen vanhojen tilien saldojen siirtämistä. Voit helposti siirtää nämä tiedot asiakkaan kirjauskansioon, toimittajan kirjauskansioon, nimikepäiväkirjaan tai KP-päiväkirjaan.

Ensimmäiseksi luodaan kokoonpanopaketti, johon sisältyvät kyseisten päiväkirjojen asetustaulukot. Seuraavassa toimenpiteessä oletetaan, että tämä vaihe on suoritettu. Lisätietoja on kohdassa [Yrityksen konfiguraation määrittäminen](admin-set-up-company-configuration.md). Näissä ohjeissa kuvataan seuraavat vaiheet, joihin kuuluu yhteistyökumppanin toimittaman paketin käyttöönotto.  

Varmista ennen aloittamista, että käytät järjestelmänvalvojan roolikeskuksen sivua, koska se tarjoaa oikean kontekstin määrittelytyöllesi. Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>Käytä päiväkirjan tapahtumia uuteen yritykseen

1. Määritä uusi yritys ja ota sille käyttöön määrityspaketti. Lisätietoja on kohdassa [Yrityksen määrittämien ohjatun RapidStart-toiminnon avulla](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Uudessa yrityksessä ei ole tietoja kirjauskansion alkusaldoista.  

2. Avaa määritystyökirja ja tuo olemassa olevat tiedot asiakkaista, nimikkeistä, toimittajista ja pääkirjanpidosta. Lisätietoja on ohjeaiheessa [Asiakastietojen siirtäminen](admin-migrate-customer-data.md).  

    Nyt sinulla on perustiedot käytössä. Seuraavaksi lisätään alkusaldot. Seuraavissa vaiheissa kuvataan, miten KP-tileille luodaan päiväkirjarivejä, mutta sama pätee asiakkaiden, toimittajien ja nimikkeiden päiväkirjarivien luomiseen.  
3. Valitse **Luo pääkirjanpidon tilien kirjauskansioiden rivit** -toiminto.  
4. Täytä **Vaihtoehdot**-pikavälilehden tarvittavat kohdat ja määritä suodattimet. Syötä **Päiväkirjan malli** -kenttään nimi.  
5. Valitse **OK**-painike. Tietueet ovat nyt kirjauskansiossa, mutta summat ovat tyhjiä.  
6. Vie päiväkirjataulukko Exceliin ja syötä kirjaus- ja vastatilin tiedot manuaalisesti vanhoista tiedoista.
7. Tuo uuden yrityksen taulukon tiedot ja ota ne käyttöön. Kirjauskansion rivit ovat valmiita kirjausta varten.  
8. Valitse määritystyökirjassa kirjauskansion rivin taulukko ja valitse sitten **Tietokannan tiedot** -toiminto.  
9. Tarkista tiedot ja valitse **Kirjaa**-toiminto.  
10. Toista vaiheet tuodaksesi ja kirjataksesi muut mahdolliset avaussaldot.  

> [!TIP]
> Voit käyttää samoja eräajoja avaussaldojen lisäämiseen aina kun rekisteröit uuden asiakkaan tai toimittajan, jonka kanssa sinulla on ollut liiketoimintaa aiemmin, mutta et ole rekisteröitynyt kohteeseen [!INCLUDE [prod_short](includes/prod_short.md)]. Etsi vain haluamasi tehtävä ja valitse sitten asianmukainen linkki.

## <a name="see-also"></a>Katso myös

[Kokoonpanojen käyttäminen uusissa yrityksissä](admin-apply-configuration-to-new-companies.md)  
[Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]