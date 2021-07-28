---
title: Tilikartan määrittäminen
description: Tilikartta näyttää ne kirjanpidon tilit, joihin on tallennettu taloustietoja. Voit muuttaa oletustilejä tilikartassa ja lisätä uusia tilejä.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 506aae83d19c8b04102760017302e83d523f77e8
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/30/2021
ms.locfileid: "6327036"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Tilikartan määrittäminen tai muuttaminen

Tilikartta näyttää ne kirjanpidon tilit, joihin on tallennettu taloustietoja. [!INCLUDE[prod_short](includes/prod_short.md)] sisältää tilikartan, joka on valmis tukemaan liiketoimintaasi.
Voit kuitenkin muuttaa oletustilejä ja lisätä uusia tilejä.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="adding-or-changing-accounts"></a>Tilien lisääminen tai muuttaminen

Voit avata kunkin tilin KP-tilin tilikartasta ja lisätä tai muuttaa asetuksia. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Tarvittaessa voit käyttää useita rivejä KP-tilin nimeä varten. Valitse **KP-tilikortti**-sivun **Tili**-ryhmässä **Lisätekstit** ja täytä sitten vähintään yksi rivi kopioitavalla tekstillä sekä tilin nimi.  

**Summa**-tyyppisten tilien osalta sinun täytyy täyttää **Summausväli**-kenttä. **Loppusumma**-tilien osalta Sisennä-toiminto täyttää tämän kentän automaattisesti. Kun olet määrittänyt kaikki tilit, valitse **Prosessi**-toiminto ja valitse sitten **Sisennä tilikartta**.  

> [!IMPORTANT]
> Jos olet syöttänyt määritelmiä **Summausväli**-kentässä **Loppusumma**-tileille ennen sisentämistä, sinun täytyy syöttää ne uudestaan, koska Sisennys-toiminto korvaa kaikki arvot **Loppusumma**-kentässä.

## <a name="deleting-accounts"></a>Tilien poistaminen

Voit poistaa pääkirjanpitotilin. Ennen sen poistamista seuraavien on kuitenkin toteuduttava:  

* Tilin saldon tulee olla nolla.  
* **Salli KP-tilin poisto ennen** -kenttä on määritettävä **Pääkirjanpidon asetukset** -sivulla. Tilillä ei saa olla tapahtumakirjauksia kyseisenä päivänä tai sen jälkeen.  
* Jos **Tarkista KP-tilin käyttö** -kenttä on valittu **Pääkirjanpidon asetukset** -sivulla, tiliä ei voi käyttää kirjausryhmässä tai kirjauksen asetuksissa.  

[!INCLUDE[prod_short](includes/prod_short.md)] estää tilikartassa tarvittavia tietoja sisältävän pääkirjanpitotilin poistamisen.  

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Tietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[KP-raporttimallien käyttäminen](bi-how-work-account-schedule.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Sulje tuloslaskelmatilit ranskalaisessa versiossa](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Tulosta tuloslaskelmat australialaisessa versiossa](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Tulosta tuloslaskelmat uusiseelantilaisessa versiossa](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Määritä ja sulje tuloslaskelmasaldot espanjalaisessa versiossa](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Tilikartan sisentäminen ja vahvistaminen espanjalaisessa versiossa](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]