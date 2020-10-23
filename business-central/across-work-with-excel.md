---
title: Näyttäminen ja muokkaaminen Excelissä Business Centralista | Microsoft Docs
description: Lisätietoja sivujen avaamisesta Microsoft Excelissä, jotta tietoja voi analysoida paremmin Business Centralissa.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: b25413c8f0479aaccfc67ae96f2870690f993dfa
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927270"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Näyttäminen ja muokkaaminen Excelissä Business Centralista

Jos sinulla on riveille ja sarakkeisiin sijoittava tietueluettelo, kuten asiakas-, myyntitilaus- tai laskuluettelo, voit katsoa tietueita myös Microsoft Excelissä. Sen voi tehdä kahdella tavalla. Voit valita sivulla joko **Avaa Excelissä**- tai **Muokkaa Excelissä** -toiminnon. Toimintojen erot ovat seuraavat:  

## <a name="open-in-excel"></a>Avaa Excelissä

- Tätä toimintoa käytettäessä Excel noudattaa sivulla olevia näytettäviä tietueita, jotka rajoittavat suodattimia. Niinpä Excel-työkirjassa on samat rivit ja sarakkeet, jotka näkyvät [!INCLUDE[prodshort](includes/prodshort.md)]in sivulla.

- Voit tehdä muutoksia tietueisiin Excelissä, mutta et voi julkaista näitä muutoksia takaisin [!INCLUDE[prodshort](includes/prodshort.md)]iin. Voit ainoastaan tallentaa muutokset Excel-tiedostoon omassa tietokoneessa.

- Tätä toimintoa voi käyttää sekä Windows- että Mac-käyttöjärjestelmässä.

> [!NOTE]
> Paikallisessa [!INCLUDE[prodshort](includes/prodshort.md)]:ssa **Avaa Excelissä** -toiminto on oletusarvoisesti käytettävissä. Jos kuitenkin [!INCLUDE[prodshort](includes/prodshort.md)] määrität paikallisesti muokkausta varten tietoja Excelissä, **Avaa Excelissä-toiminnon** korvaa **Muokkaa Excelissä** -toiminto.

## <a name="edit-in-excel"></a>Muokkaa Excelissä

- Tätä toimintoa käytettäessä Excel noudattaa sivulla olevia näytettäviä tietueita, jotka rajoittavat useimpia suodattimia. Niinpä Excel-työkirjassa on lähes samat tietueet ja sarakkeet.

- **Muokkaa Excelissä** -toiminnon etuna on, että voit tehdä muutoksia tietueisiin Excelissä ja julkaista sitten muutokset takaisin [!INCLUDE[prodshort](includes/prodshort.md)]iin.

- Toimintoa voi käyttää vain Windowsissa eikä se toimi Mac-käyttöjärjestelmässä.

- Voit vaihtaa käytössä olevaa yritystä. Se tehdään valitsemalla **Asetukset**-kuvake ![Excel-apuohjelman asetukset](media/cogwheel.png "Excel-apuohjelman asetukset") Excel-apuohjelma-ruudussa ja valitsemalla sitten yritys **Yritys**-kentässä.  

    > [!IMPORTANT]
    > Kun vaihdat yritystä, varmista, että **Ympäristö**-kenttä ei ole tyhjä. Jos kenttä on tyhjä, määritä siihen jokin käytettävissä olevista asetuksista. Muussa tapauksessa apuohjelma ei toimi oikein.  

Jos apuohjelmaan tehdään muutoksia, yhteyden päivittäminen edellyttää sen lataamista uudelleen. Lataamiseen käytetään ![Excelin apuohjelmavalikko](media/excel-addin-menu.png "Excel-apuohjelmavalikko") -valikko apuohjelman oikeassa yläkulmassa.

> [!NOTE]
> **Muokkaa Excelissä** -toiminto on käytettävissä paikallisessa [!INCLUDE[prodshort](includes/prodshort.md)] -versiossa vain, jos järjestelmänvalvoja on määrittänyt Excel-apuohjelman. Se on käytettävissä vain WWW-asiakasohjelmassa. Järjestelmänvalvojille on lisätietoja Excel-apuohjelman asentamisesta kohdassa [Excel-apuohjelman määrittäminen Business Central -tietojen muokkaamiseen](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Vaihtoehtojen välisiin eroihin tutustuminen
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Rahoituslaskelmien analysointi Microsoft Excel:issä](finance-analyze-excel.md)  
[Business Centralin käyttäminen](ui-work-product.md)  
[Excel-integraation parannukset vuoden 2019 2. julkaisuaallossa](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  
