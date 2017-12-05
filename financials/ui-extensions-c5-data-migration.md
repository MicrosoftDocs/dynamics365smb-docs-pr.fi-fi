---
title: "C5-tietojen siirtolaajennuksen käyttäminen | Microsoft Docs"
description: "Voit käyttää tätä laajennusta asiakkaiden, toimittajien, nimikkeiden ja pääkirjanpidon tilien siirtämiseen Microsoft Dynamics C5 2012:sta Financialsiin."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 09/26/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 2d7d533662936116ffa40ded07b68e845fed810b
ms.contentlocale: fi-fi
ms.lasthandoff: 11/10/2017

---

# <a name="the-c5-data-migration-extension-for-dynamics-365-for-finance-and-operations-business-edition"></a>Dynamics 365 for Finance and Operations, Business editionin C5-tietojen siirtolaajennukset
Tämän laajennuksen avulla on helppo siirtää asiakkaita, toimittajia, nimikkeitä ja pääkirjanpidon tilejä Microsoft Dynamcis C5 2012 -versiosta [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan.  
  
> [!Note] 
> [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman yrityksessä ei saa olla tietoja. Kun siirto on käynnistetty, asiakkaiden, toimittajien, nimikkeiden tai tilien luominen ei ole sallittua. Voit luoda niitä siirron valmistuttua.

## <a name="to-migrate-data"></a>Tietojen siirtäminen
Tietojen siirtäminen C5:stä ja tuominen [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmasta edellyttää vain seuraavien vaiheiden suorittamista:  
  
1. Voit viedä tiedot C5:stä käyttämällä **Vie tietokanta** -toimintoa. Pakkaa sitten viennin kansio.  
2. Valitse [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake. Valitse **Tietojen siirto** ja valitse sitten **Tietojen siirto**.  
3. Suorita asetusten ohjatun määrityksen oppaan vaiheet. Varmista, että valitset tietolähteeksi **Tuo Microsoft Dynamcis C5 2012 -versiosta** -kohdan.  

> [!Note] 
> Yritykset lisäävät usein kenttiä, joiden avulla C5 voidaan mukauttaa toimialan vaatimusten mukaisesti. [!INCLUDE[d365fin](includes/d365fin_md.md)] ei siirrä mukautettujen kenttien tietoja. Siirto epäonnistuu myös, jos mukautettuja kenttiä on enemmän kuin 10. 

## <a name="viewing-the-status-of-the-migration"></a>Siirron tilan tarkasteleminen
Voit valvoa siirron onnistumista **Tietojen siirron yleiskuvaus** -sivulla. Sivulla on tietoja esimerkiksi siirrettävien objektien määrästä, siirron tilasta, siirrettyjen nimikkeiden määrästä ja siirron onnistumisesta. Sivulla on tietoja myös virheiden määrästä. Voit tarkastella sivulla virheitä ja mahdollisesti siirtyä sivulta korjaamaan objektin ongelmat. Lisätietoja on tämän aiheen seuraavassa osassa. 

> [!Note] 
> Päivitä sivu, jotta siirron tulokset näkyvät sivulla.

## <a name="correcting-errors"></a>Virheiden korjaaminen
Jos siirrossa tapahtuu virheitä, **Tila**-kentän arvoksi tulee **Valmis (löytyi virheitä)**. **Virheiden määrä** -kenttä osoittaa virheiden määrän. Voit tarkastella virheluetteloa, kun avaat **Tietojen siirron virheet** -sivun valitsemalla seuraavat kohdat:

* Objektin **Virheiden määrä** -kentässä oleva luku. 
* Objekti ja sen jälkeen **Näytä virheet** -toiminto. 

Voit korjata virheen **Tietojen siirron virheet** -sivulla valitsemalla virhesanoman ja valitsemalla sitten **Muokkaa tietuetta**. Näyttöön avautuu sivu, joka sisältää objektin siirretyt tiedot. Kun olet korjannut yhden tai useita virheitä, voit siirtää korjaamasi objektit valitsemalla **Siirrä**. Koko siirtoprosessia ei siis tarvitse käynnistää uudelleen.  

> [!Tip]
> Jos olet korjannut useita virheitä, voit valita useita siirrettäviä rivejä valitsemalla **Valitse lisää** -toiminnon. Jos virheitä ei tarvitse korjata, voit valita ne ja valita sitten **Ohita valinnat**.

> [!Note]
> Jos osa nimikkeistä sisältyy tuoterakenteeseen, siirto on ehkä tehtävä useaan kertaan, jos alkuperäistä nimikettä ei luoda ennen siihen viittaavien varianttien luomista. Jos nimikevariantti luodaan ensin, alkuperäisen nimikkeen viite voi aiheuttaa virhesanoman.  

## <a name="verifying-data-after-migrating"></a>Tietojen tarkistaminen siirron jälkeen 
Jos haluat tarkistaa, että tiedot on siirretty oikein, voit katsoa seuraavia C5:n ja [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman sivuja.

|Microsoft Dynamics C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|Asiakastapahtumat| Yleiset päiväkirjat|
|Toimittajatapahtumat| Yleiset päiväkirjat|
|Nimiketapahtumat| Nimikepäiväkirjat|

Siirrettyjen tietojen erän nimeksi annetaan [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa **C5MIGRATE**. 

## <a name="stopping-data-migration"></a>Tietojen siirron pysäyttäminen
Voit pysäyttää tietojen siirron valitsemalla **Pysäytä kaikki siirrot**. Jos teet näin, kaikki odottavat siirrot pysäytetään.

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[Tervetuloa [!INCLUDE[d365fin](includes/d365fin_md.md)]iin!](index.md)  

