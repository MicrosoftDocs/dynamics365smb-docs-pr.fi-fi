---
title: Tilikartan valmistelutoimien määrittäminen tai muuttaminen (sisältää videon)
description: 'Lue, miten voit määrittää tilikartan, jossa näkyvät kirjanpitotilit, joihin on tallennettu taloustietoja.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 12/19/2023
ms.custom: bap-template
---
# Tilikartan määrittäminen tai muuttaminen

Tilikartta näyttää ne kirjanpidon tilit, joihin on tallennettu taloustietoja. [!INCLUDE[prod_short](includes/prod_short.md)] sisältää tilikartan, joka on valmis tukemaan liiketoimintaasi. Voit kuitenkin muuttaa oletustilejä ja lisätä uusia tilejä.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## Lisää tai muuta tilejä

Voit avata kunkin tilin pääkirjanpidon (KP) tilin tilikartasta ja lisätä tai muuttaa asetuksia. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Tarvittaessa voit käyttää useita rivejä KP-tilin nimeä varten. Valitse **KP-tilikortti**-sivun **Tili**-ryhmässä **Lisätekstit** ja täytä sitten vähintään yhteen riviin tilin nimi ja kopioitava teksti.  

**Summa**-tyyppisten tilien osalta sinun täytyy täyttää **Summausväli**-kenttä. **Loppusumma**-tilien osalta Sisennä-toiminto täyttää tämän kentän automaattisesti. Kun olet määrittänyt kaikki tilit, valitse **Prosessi**-toiminto ja valitse sitten **Sisennä tilikartta**.  

> [!IMPORTANT]
> Jos olet syöttänyt määritelmiä **Summausväli**-kentässä **Loppusumma**-tileille ennen sisentämistä, sinun täytyy syöttää ne uudestaan, koska Sisennys-toiminto korvaa kaikki arvot **Loppusumma**-kentässä.

## Poista tilejä

Voit poistaa pääkirjanpitotilin. Ennen sen poistamista seuraavien on kuitenkin toteuduttava:  

* Tilin saldon tulee olla nolla.  
* **Salli KP-tilin poisto ennen** -kenttä on määritettävä **Pääkirjanpidon asetukset** -sivulla. Tilillä ei saa olla tapahtumakirjauksia kyseisenä päivänä tai sen jälkeen.  
* Jos **Tarkista KP-tilin käyttö** -kenttä on valittu **Pääkirjanpidon asetukset** -sivulla, tiliä ei voi käyttää kirjausryhmässä tai kirjauksen asetuksissa.  

[!INCLUDE[prod_short](includes/prod_short.md)] estää tilikartassa tarvittavia tietoja sisältävän pääkirjanpitotilin poistamisen.  

Voit myös määrittää, milloin ihmisten sallitaan poistaa tilejä. Käytössä **Pääkirjanpidon asetukset** -sivu, **Estä pääkirjatilien poistaminen** -valinta toimii yhdessä päivämäärän kanssa **Tarkista KP-tilien poistaminen jälkeen** -kenttä toimimaan ylimääräisenä vahvistuksena. Jos otat käyttöön **Estä KP-tilien poisto** -valinnan, et voi poistaa KP-tilejä, joissa on kirjanpitotapahtumia **Tarkista, voidaanko KP-tili poistaa tämän jälkeen** -kenttään määritetyn päivämäärän jälkeen. Jos haluat poistaa tällaisen tilin, joku, jolla on pääsy **Pääkirjanpidon asetukset** -sivun tulee poistaa käytöstä **Estä KP-tilien poisto** -valinta.  

**Estä KP-tilien poisto** -kentän käyttöönotto on usein paras käytäntö, kuten myös päivämäärän asettaminen **Tarkista KP-tilien poisto jälkeen** -kenttä, esimerkiksi päivämäärä, johon asti säädökset edellyttävät rahoitustietojen tallentamista.  

### Video-opastus

Tämä video näyttää, kuinka voit määrittää, voivatko ihmiset poistaa KP-tilejä ja milloin.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1g3oY]

## Katso myös

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
