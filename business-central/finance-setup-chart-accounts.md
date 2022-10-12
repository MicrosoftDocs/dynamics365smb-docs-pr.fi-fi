---
title: Tilikartan valmistelutoimien määrittäminen tai muuttaminen (sisältää videon)
description: Tilikartta näyttää ne kirjanpidon tilit, joihin on tallennettu taloustietoja. Voit muuttaa oletustilejä tilikartassa ja lisätä uusia tilejä.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.search.form: 16, 17, 18, 118, 386, 391
ms.date: 01/21/2022
ms.author: edupont
ms.openlocfilehash: 15eca1f6bc4a75ca6758e5be351d4a459226ac5b
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606692"
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>Tilikartan määrittäminen tai muuttaminen

Tilikartta näyttää ne kirjanpidon tilit, joihin on tallennettu taloustietoja. [!INCLUDE[prod_short](includes/prod_short.md)] sisältää tilikartan, joka on valmis tukemaan liiketoimintaasi. Voit kuitenkin muuttaa oletustilejä ja lisätä uusia tilejä.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Lisää tai muuta tilejä

Voit avata kunkin tilin pääkirjanpidon (KP) tilin tilikartasta ja lisätä tai muuttaa asetuksia. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Tarvittaessa voit käyttää useita rivejä KP-tilin nimeä varten. Valitse **KP-tilikortti**-sivun **Tili**-ryhmässä **Lisätekstit** ja täytä sitten vähintään yhteen riviin tilin nimi ja kopioitava teksti.  

**Summa**-tyyppisten tilien osalta sinun täytyy täyttää **Summausväli**-kenttä. **Loppusumma**-tilien osalta Sisennä-toiminto täyttää tämän kentän automaattisesti. Kun olet määrittänyt kaikki tilit, valitse **Prosessi**-toiminto ja valitse sitten **Sisennä tilikartta**.  

> [!IMPORTANT]
> Jos olet syöttänyt määritelmiä **Summausväli**-kentässä **Loppusumma**-tileille ennen sisentämistä, sinun täytyy syöttää ne uudestaan, koska Sisennys-toiminto korvaa kaikki arvot **Loppusumma**-kentässä.

## <a name="delete-accounts"></a>Poista tilejä

Voit poistaa pääkirjanpitotilin. Ennen sen poistamista seuraavien on kuitenkin toteuduttava:  

* Tilin saldon tulee olla nolla.  
* **Salli KP-tilin poisto ennen** -kenttä on määritettävä **Pääkirjanpidon asetukset** -sivulla. Tilillä ei saa olla tapahtumakirjauksia kyseisenä päivänä tai sen jälkeen.  
* Jos **Tarkista KP-tilin käyttö** -kenttä on valittu **Pääkirjanpidon asetukset** -sivulla, tiliä ei voi käyttää kirjausryhmässä tai kirjauksen asetuksissa.  

[!INCLUDE[prod_short](includes/prod_short.md)] estää tilikartassa tarvittavia tietoja sisältävän pääkirjanpitotilin poistamisen.  

## <a name="block-deletion-of-gl-accounts"></a>Estä KP-tilien poisto

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Vuoden 2022 2. julkaisuaalto sisältää ylimääräisen suojauksen, ettei KP-tilejä poistetaan vahingossa edes sellaisissa skenaarioissa, joissa kriteerit täyttyvät.  

**Pääkirjanpidon asetukset** -sivulle lisättiin uusi **Estä KP-tilien poisto** -kenttä. Kun arvoksi on määritetty *Kyllä*, kenttä toimii lisätarkistuksena. Tämä tarkoittaa sitä, että KP-tilejä ja kirjanpitotapahtumia ei voi poistaa **Tarkista, voidaanko KP-tili poistaa tämän jälkeen** -kenttään määritetyn päivämäärän jälkeen. Jos haluat poistaa tällaisen tilin, kentän arvoksi on määritettävä ensin *Ei* **Pääkirjanpidon asetukset** -sivulla, johon käyttäjällä on oltava oikeudet.  

Paras käytäntö on määrittää **Estä KP-tilien poisto** -kentän arvoksi *Kyllä* ja **Tarkista, voidaanko KP-tili poistaa tämän jälkeen** -kentän arvoksi esimerkiksi päivämäärä, johon mennessä taloustiedot on tallennettava.  

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Tietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Talousraporttien käsitteleminen](bi-how-work-account-schedule.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Sulje tuloslaskelmatilit ranskalaisessa versiossa](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Tulosta tuloslaskelmat australialaisessa versiossa](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Tulosta tuloslaskelmat uusiseelantilaisessa versiossa](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Määritä ja sulje tuloslaskelmasaldot espanjalaisessa versiossa](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Tilikartan sisentäminen ja vahvistaminen espanjalaisessa versiossa](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
