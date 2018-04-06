---
title: "Uusien yritysten määrittäminen cmdlet-komennolla | Microsoft Docs"
description: "Saatat haluta ladata ja tuoda määrityspaketin eri tilanteissa ilman käyttäjien osallistumista tai käyttämällä RapidStart Services -käyttöliittymää. Voit tehdä niin käyttämällä Windows PowerShellin cmdlet -komentoa."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ce8bfdb40d8d428f4b02abcbba4498d58d6481be
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a>Uusien yritysten määrittäminen cmdlet-komennolla
Saatat haluta ladata ja tuoda määrityspaketin eri tilanteissa ilman käyttäjien osallistumista tai käyttämällä RapidStart Services -käyttöliittymää. Voit tehdä niin käyttämällä Windows PowerShellin cmdlet -komentoa. Skenaariot, jossa tämä voi olla hyödyllistä, ovat:  

- Useiden [!INCLUDE[d365fin](includes/d365fin_md.md)] -toteutusten tietojen tuonnin suorittaminen.
- Sovelluksen lisäalueiden määrittäminen useille asiakkaille.  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a>Määrityspaketin käyttöönottaminen cmdlet-komennon avulla  

1. Valmistele RapidStart Services -palvelun paketti. Voit esimerkiksi luoda paketin tiettyjen arvojen ja taulukon nimien ja niiden kenttien tuomiseksi, joihin nämä arvot lisätään.  
2. Aseta paketti tietokoneeseen, jossa suoritat cmdlet-komennon.  
3. Avaa [!INCLUDE[d365fin](includes/d365fin_md.md)] -hallintoliittymä.  
4. Kirjoita **Invoke-NAVCodeUnit** ja määritä vastaavat tiedot kuin seuraavassa esimerkissä.  
    ```powershell  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
Cmdlet tuo paketin jokaiseen yritykseen. Käyttäjät voivat alkaa käyttää uutta toimintoa heti.  

## <a name="see-also"></a>Katso myös  
[Uusien yritysten määrittäminen](admin-how-to-configure-new-companies.md)  
[Kokoonpanojen käyttäminen uusissa yrityksissä](admin-apply-configuration-to-new-companies.md)  
[Yrityksen määrittäminen RapidStart Services -palvelun avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)  
[Microsoft Dynamics NAV Windows PowerShell Cmdlet-komennot](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

