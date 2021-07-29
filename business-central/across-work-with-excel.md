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
ms.openlocfilehash: 6bf12f55f6bce843c4ed12f2a40db542367fffde
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443471"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Näyttäminen ja muokkaaminen Excelissä Business Centralista

Jos sinulla on riveille ja sarakkeisiin sijoittava tietueluettelo, kuten asiakas-, myyntitilaus- tai laskuluettelo, voit katsoa tietueita myös Microsoft Excelissä. Sivusta riippuen Excelissä tarkastelemiseen on kaksi vaihtoehtoa. Voit valita sivulla joko **Avaa Excelissä**- tai **Muokkaa Excelissä** -toiminnon. Tässä artikkelissa selitetään näiden kahden toiminnon erot.

## <a name="open-in-excel"></a>Avaa Excelissä

**Avaa Excelissä** -toiminnon avulla voit tehdä muutoksia tietueisiin Excelissä, mutta et voi julkaista muutoksia takaisin [!INCLUDE[prod_short](includes/prod_short.md)]iin. Voit ainoastaan tallentaa muutokset Excel-tiedostoon omassa tietokoneessa.

- Tätä toimintoa käytettäessä Excel noudattaa sivulla olevia näytettäviä tietueita, jotka rajoittavat suodattimia. Excel-työkirjassa on samat rivit ja sarakkeet, jotka näkyvät [!INCLUDE[prod_short](includes/prod_short.md)]in sivulla.

- Tätä toimintoa voi käyttää sekä Windows- että Mac-käyttöjärjestelmässä.

- Päivityksestä 18.3 alkaen voit tarkastella myös sivun osissa näkyviä luetteloita, kuten myyntitilauksen rivejä. Toistaiseksi tämä on valinnainen ominaisuus, joka edellyttää, että otat käyttöön toiminnon **Vie mikä tahansa luettelon osa Exceliin** kohdassa **Ominaisuuksien hallinta**. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management). 

> [!NOTE]
> Paikallisessa [!INCLUDE[prod_short](includes/prod_short.md)]:ssa **Avaa Excelissä** -toiminto on oletusarvoisesti käytettävissä. Jos kuitenkin [!INCLUDE[prod_short](includes/prod_short.md)] määrität paikallisesti muokkausta varten tietoja Excelissä, **Avaa Excelissä-toiminnon** korvaa **Muokkaa Excelissä** -toiminto.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Muokkaa Excelissä

**Muokkaa Excelissä** -toiminnon avulla voit tehdä muutoksia tietueisiin Excelissä ja voit julkaista muutokset takaisin [!INCLUDE[prod_short](includes/prod_short.md)]iin.

- Tämän toiminnon avulla Excel ottaa huomioon useimmat sivun suodattimet, jotka rajoittavat näytettäviä tietueita, joten Excel-työkirja sisältää lähes samat tietueet ja sarakkeet.

- Toimintoa voi käyttää vain Windowsissa eikä se toimi Mac-käyttöjärjestelmässä.

- Voit vaihtaa käytössä olevaa yritystä. Voit vaihtaa yrityksen valitsemalla **Asetukset**-kuvakkeen ![Excelin apuohjelma-asetukset.](media/cogwheel.png "Excel-apuohjelman asetukset") Excelin apuohjelmaruudussa ja valitsemalla yrityksen **Yritys**-kentästä.  

    > [!IMPORTANT]
    > Kun vaihdat yritystä, varmista, että **Ympäristö**-kenttä ei ole tyhjä. Jos kenttä on tyhjä, määritä siihen jokin käytettävissä olevista asetuksista. Muussa tapauksessa apuohjelma ei toimi oikein.  

Jos apuohjelmaan tehdään muutoksia, yhteyden päivittäminen edellyttää sen lataamista uudelleen. Lataamiseen käytetään ![Excelin apuohjelmavalikko](media/excel-addin-menu.png "Excel-apuohjelmavalikko") -valikko apuohjelman oikeassa yläkulmassa. Jos et voi ladata apuohjelmaa, keskustele järjestelmänvalvojan kanssa. Jos olet järjestelmänvalvoja, katso lisätietoja kohdassa [Excel-apuohjelman määrittäminen Business Central -tietojen muokkaamiseen](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> **Muokkaa Excelissä** -toiminto on käytettävissä paikallisessa [!INCLUDE[prod_short](includes/prod_short.md)] -versiossa vain, jos järjestelmänvalvoja on määrittänyt Excel-apuohjelman. Se on käytettävissä vain WWW-asiakasohjelmassa. Järjestelmänvalvojille on lisätietoja Excel-apuohjelman asentamisesta kohdassa [Excel-apuohjelman määrittäminen Business Central -tietojen muokkaamiseen](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Vaihtoehtojen välisiin eroihin tutustuminen
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Rahoituslaskelmien analysointi Microsoft Excel:issä](finance-analyze-excel.md)  
[Business Centralin käyttäminen](ui-work-product.md)  
[Excel-integraation parannukset vuoden 2019 2. julkaisuaallossa](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]