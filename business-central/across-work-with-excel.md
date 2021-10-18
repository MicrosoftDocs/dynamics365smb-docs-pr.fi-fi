---
title: Näyttäminen ja muokkaaminen Excelissä Business Centralista
description: Lisätietoja sivujen avaamisesta Microsoft Excelissä, jotta tietoja voi analysoida paremmin Business Centralissa.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 012fedb26c4d98d4014efdb53327c82b8a6877c8
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2021
ms.locfileid: "7587554"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Näyttäminen ja muokkaaminen Excelissä Business Centralista

Jos sinulla on riveille ja sarakkeisiin sijoittava tietueluettelo, kuten asiakas-, myyntitilaus- tai laskuluettelo, voit tuoda luettelon Microsoft Exceliin ja tarkastella sitä siellä. Sivusta riippuen Excelissä tarkastelemiseen on kaksi vaihtoehtoa. Kumpikin vaihtoehto on käytettävissä **Jaa**-kuvakkeesta ![Jaa sivu toisessa sovelluksessa.](media/share-icon.png) sivun yläreunassa. Voit valita sivulla joko **Avaa Excelissä**- tai **Muokkaa Excelissä** -toiminnon. Tässä artikkelissa selitetään näiden kahden toiminnon erot.

## <a name="open-in-excel"></a>Avaa Excelissä

**Avaa Excelissä** -toiminnon avulla voit tehdä muutoksia tietueisiin Excelissä, mutta et voi julkaista muutoksia takaisin [!INCLUDE[prod_short](includes/prod_short.md)]iin. Muutokset voi tallentaa vain Excel-tiedostoon vaikuttamatta [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman tietoihin.

- Tätä toimintoa käytettäessä Excel noudattaa sivulla olevia näytettäviä tietueita, jotka rajoittavat suodattimia. Excel-työkirjassa on samat rivit ja sarakkeet, jotka näkyvät [!INCLUDE[prod_short](includes/prod_short.md)]in sivulla.

- Tätä toimintoa voi käyttää sekä Windows- että Mac-käyttöjärjestelmässä.

- Päivityksestä 18.3 alkaen voit tarkastella myös sivun osissa näkyviä luetteloita, kuten myyntitilauksen rivejä. 

> [!NOTE]
> Paikallisessa [!INCLUDE[prod_short](includes/prod_short.md)]:ssa **Avaa Excelissä** -toiminto on oletusarvoisesti käytettävissä. Jos kuitenkin [!INCLUDE[prod_short](includes/prod_short.md)] määrität paikallisesti muokkausta varten tietoja Excelissä, **Avaa Excelissä-toiminnon** korvaa **Muokkaa Excelissä** -toiminto.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Muokkaa Excelissä

**Muokkaa Excelissä** -toiminto on käytettävissä useimmissa luetteloissa, mutta ei kaikissa. **Muokkaa Excelissä** -toiminnon avulla voit tehdä muutoksia tietueisiin Excelissä ja voit julkaista muutokset takaisin [!INCLUDE[prod_short](includes/prod_short.md)]iin. Kun Excel avautuu, **Excel-apuohjelma** -ruutu näkyy oikealla.

- Tämän toiminnon avulla Excel ottaa huomioon useimmat sivun suodattimet, jotka rajoittavat näytettäviä tietueita, joten Excel-työkirja sisältää lähes samat tietueet ja sarakkeet.

- Voit hakea uusimmat tiedot [!INCLUDE[prod_short](includes/prod_short.md)]ista valitsemalla Excelin apuohjelmaruudussa **Päivitä**.

- Voit vaihtaa käytössä olevaa yritystä. Voit vaihtaa yrityksen valitsemalla **Asetukset**-kuvakkeen ![Excelin apuohjelma-asetukset.](media/cogwheel.png "Excel-apuohjelman asetukset") Excelin apuohjelmaruudussa ja valitsemalla yrityksen **Yritys**-kentästä.  

    > [!IMPORTANT]
    > Kun vaihdat yritystä, varmista, että **Ympäristö**-kenttä ei ole tyhjä. Jos kenttä on tyhjä, määritä siihen jokin käytettävissä olevista asetuksista. Muussa tapauksessa apuohjelma ei toimi oikein.  

Jos apuohjelmaan tehdään muutoksia, yhteyden päivittäminen edellyttää sen lataamista uudelleen. Lataamiseen käytetään ![Excelin apuohjelmavalikko](media/excel-addin-menu.png "Excel-apuohjelmavalikko") -valikko apuohjelman oikeassa yläkulmassa. Jos et voi ladata apuohjelmaa, keskustele järjestelmänvalvojan kanssa. Jos olet järjestelmänvalvoja, katso lisätietoja kohdassa [Excelin Business Central -apuohjelman hankkiminen](admin-deploy-excel-addin.md).

> [!NOTE]
> Apuohjelma toimii verkkosivuston Excelissä (online) mistä tahansa laitteesta niin kauan kuin sitä käytetään tuetussa selaimessa. Se toimii myös Windowsin (PC) Excel-sovelluksessa, mutta ei macOS:ssa.
>
> **Muokkaa Excelissä** -toiminto on käytettävissä paikallisessa [!INCLUDE[prod_short](includes/prod_short.md)] -versiossa vain, jos järjestelmänvalvoja on määrittänyt Excel-apuohjelman. Se on käytettävissä vain WWW-asiakasohjelmassa. Järjestelmänvalvojille on lisätietoja Excel-apuohjelman asentamisesta kohdassa [Excel-apuohjelman määrittäminen Business Central -tietojen muokkaamiseen](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).


<!-- Note for later: here we're immediately jumping to pretty advanced topics like changing company or reloading the addin. Fine to keep them for now. In the future, we will first need to explain in more detail the actual functionality of the addin, primarily these sub-sections:

Refreshing record data in Excel
Editing and publishing back to Business Central
Creating new records from Excel
Crafting your own editable Excel.
Point (4) is where it gets interesting for changing/specifying company, environment and other connection settings-->

### <a name="first-time-sign-in"></a>Ensimmäinen sisäänkirjautuminen

**Muokkaa Excelissä** -toiminto edellyttää, että Business Central -apuohjelma on asennettu Exceliin. Joissakin tapauksissa järjestelmänvalvoja on saattanut määrittää apuohjelman asentumaan automaattisesti puolestasi. Tässä tapauksessa sinun tarvitsee vain kirjautua Business Centraliin **Excel-apuohjelma** -ruudussa käyttäjänimesi ja salasanasi avulla. Muussa tapauksessa **Uusi Office-apuohjelma** -ruutu avautuu. Jos käyttäjä haluaa asentaa apuohjelman, valitse **Luota tähän apuohjelmaan**, joka asentaa apuohjelman suoraan Office-kaupasta.

Jos apuohjelma ei jostain syystä asennu, ota yhteyttä ylläpitäjään tai yritä asentaa se manuaalisesti. Lisätietoja:[ Asenna apuohjelma manuaalisesti omaan käyttöön](admin-deploy-excel-addin.md#install).

## <a name="see-the-differences-between-the-options"></a>Vaihtoehtojen välisiin eroihin tutustuminen
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Rahoituslaskelmien analysointi Microsoft Excel:issä](finance-analyze-excel.md)  
[Business Centralin käyttäminen](ui-work-product.md)  
[Excel-integraation parannukset vuoden 2019 2. julkaisuaallossa](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]