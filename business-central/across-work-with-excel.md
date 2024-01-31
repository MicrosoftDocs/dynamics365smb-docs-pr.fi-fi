---
title: Näyttäminen ja muokkaaminen Excelissä Business Centralista (sisältää videon)
description: 'Lisätietoja sivujen avaamisesta Microsoft Excelissä, jotta tietoja voi analysoida paremmin Business Centralissa.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: 1480
ms.search.keywords: 'accountant, accounting, financial report'
ms.date: 04/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Näyttäminen ja muokkaaminen Excelissä Business Centralista

Jos sinulla on riveille ja sarakkeisiin sijoittava tietueluettelo, kuten asiakas-, myyntitilaus- tai laskuluettelo, voit tuoda luettelon Microsoft Exceliin ja tarkastella sitä siellä. Sivusta riippuen Excelissä tarkastelemiseen on kaksi vaihtoehtoa. Kumpikin vaihtoehto on käytettävissä **Jaa**-kuvakkeesta ![Jaa sivu toisessa sovelluksessa.](media/share-icon.png) sivun yläreunassa. Voit valita sivulla joko **Avaa Excelissä**- tai **Muokkaa Excelissä** -toiminnon. Tässä artikkelissa selitetään nämä kaksi toimintoa.

## Avaa Excelissä

**Avaa Excelissä** -toiminnon avulla voit tehdä muutoksia tietueisiin Excelissä, mutta et voi julkaista muutoksia takaisin [!INCLUDE[prod_short](includes/prod_short.md)]iin. Muutokset voi tallentaa vain Excel-tiedostoon vaikuttamatta [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman tietoihin.

- Tätä toimintoa käytettäessä Excel noudattaa sivulla olevia näytettäviä tietueita, jotka rajoittavat suodattimia. Excel-työkirjassa on samat rivit ja sarakkeet, jotka näkyvät [!INCLUDE[prod_short](includes/prod_short.md)]in sivulla.

- Tätä toimintoa voi käyttää sekä Windows- että Mac-käyttöjärjestelmässä.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

> [!IMPORTANT]
> Paikallisessa [!INCLUDE[prod_short](includes/prod_short.md)]:ssa **Avaa Excelissä** -toiminto on oletusarvoisesti käytettävissä. Jos kuitenkin [!INCLUDE[prod_short](includes/prod_short.md)] määrität paikallisesti muokkausta varten tietoja Excelissä, **Avaa Excelissä-toiminnon** korvaa **Muokkaa Excelissä** -toiminto.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)] 

> [!NOTE]
> Excelissä sarakkeiden kokonaisluvuissa desimaalierotin on lopussa (kuten piste `.` tai pilkku `,`), vaikka desimaalierotin ei näy Business Centralissa. Desimaalierotin määräytyy laitteen alueasetusten mukaan. Esimerkiksi `10` näkyy Business Centralissa muodossa `10.` ja Excelissä `10,`. Muodon voi vaihtaa Excelissä valitsemalla ensin arvot ja sitten näppäinyhdistelmän <kbd>Ctrl</kbd>+<kbd>1</kbd>. Lisätietoja lukujen muotoilun muuttamista Excelissä on kohdassa [Lukujen muotoileminen](https://support.microsoft.com/office/format-numbers-f27f865b-2dc5-4970-b289-5286be8b994a).


## Muokkaa Excelissä

**Muokkaa Excelissä** -toiminto on käytettävissä useimmissa luetteloissa, mutta ei kaikissa. **Muokkaa Excelissä** -toiminnon avulla voit tehdä muutoksia tietueisiin Excelissä ja voit julkaista muutokset takaisin [!INCLUDE[prod_short](includes/prod_short.md)]iin. Kun Excel avautuu, **Excel-apuohjelma** -ruutu näkyy oikealla.

- Tämän toiminnon avulla Excel ottaa huomioon useimmat sivun suodattimet, jotka rajoittavat näytettäviä tietueita, joten Excel-työkirja sisältää lähes samat tietueet ja sarakkeet.

- Voit hakea uusimmat tiedot [!INCLUDE[prod_short](includes/prod_short.md)]ista valitsemalla Excelin apuohjelmaruudussa **Päivitä**.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

### Ensimmäinen sisäänkirjautuminen

**Muokkaa Excelissä** -toiminto edellyttää, että Business Central -apuohjelma on asennettu Exceliin. Joissakin tapauksissa järjestelmänvalvoja on saattanut määrittää apuohjelman asentumaan automaattisesti puolestasi. Tässä tapauksessa sinun tarvitsee vain kirjautua Business Centraliin **Excel-apuohjelma** -ruudussa käyttäjänimesi ja salasanasi avulla. Muussa tapauksessa **Uusi Office-apuohjelma** -ruutu avautuu. Jos käyttäjä haluaa asentaa apuohjelman, valitse **Luota tähän apuohjelmaan**, joka asentaa apuohjelman suoraan Office-kaupasta.

Jos apuohjelma ei asennu, ota joko yhteyttä ylläpitäjään tai yritä asentaa se manuaalisesti. Lisätietoja:[ Asenna apuohjelma manuaalisesti omaan käyttöön](admin-deploy-excel-addin.md#install).

### Ympäristöjen ja yritysten välinen yhteistyö

Voit vaihtaa käytössä olevaa yritystä. Voit vaihtaa yrityksen valitsemalla **Asetukset**-kuvakkeen ![Excelin apuohjelma-asetukset.](media/cogwheel.png "Excel-apuohjelman asetukset") Excelin apuohjelmaruudussa ja valitsemalla yrityksen **Yritys**-kentästä.  

> [!IMPORTANT]
> Kun vaihdat yritystä, varmista, että **Ympäristö**-kenttä ei ole tyhjä. Jos kenttä on tyhjä, määritä siihen jokin käytettävissä olevista asetuksista. Muussa tapauksessa apuohjelma ei toimi oikein.  

Jos apuohjelmaan tehdään muutoksia, yhteyden päivittäminen edellyttää sen lataamista uudelleen. Lataamiseen käytetään ![Excelin apuohjelmavalikko](media/excel-addin-menu.png "Excel-apuohjelmavalikko") -valikko apuohjelman oikeassa yläkulmassa. Jos et voi ladata apuohjelmaa, keskustele järjestelmänvalvojan kanssa. Jos olet järjestelmänvalvoja, katso lisätietoja kohdassa [Excelin Business Central -apuohjelman hankkiminen](admin-deploy-excel-addin.md).

> [!NOTE]
> Apuohjelma toimii verkkosivuston Excelissä (online) mistä tahansa laitteesta niin kauan kuin sitä käytetään tuetussa selaimessa. Se toimii myös Windowsin (PC) Excel-sovelluksessa, mutta ei macOS:ssa.
>
> **Muokkaa Excelissä** -toiminto on käytettävissä paikallisessa [!INCLUDE[prod_short](includes/prod_short.md)] -versiossa vain, jos järjestelmänvalvoja on määrittänyt Excel-apuohjelman. Se on käytettävissä vain WWW-asiakasohjelmassa. Järjestelmänvalvojille on lisätietoja Excel-apuohjelman asentamisesta kohdassa [Excel-apuohjelman määrittäminen Business Central -tietojen muokkaamiseen](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### Rajoituksia käytettäessä Exceliä verkossa 

Kun **Muokkaa Excelissä** -ohjelmaa käytetään luettelosivuilla, joilla on useita sarakkeita, tuloksena olevassa työkirjassa voi olla liian monta saraketta, jotta tiedostoa voisi tarkastella Excelissä verkossa. [!INCLUDE[prod_short](includes/prod_short.md)] rajoittaa viedyn työkirjan automaattisesti sataan sarakkeeseen, kun OneDrive on määritetty järjestelmän ominaisuuksille. 

## Vaihtoehtojen välisiin eroihin tutustuminen
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## Katso myös

[Rahoituslaskelmien analysointi Microsoft Excelissä](finance-analyze-excel.md)  
[Business Centralin käyttäminen](ui-work-product.md)  
[Excel-integraation parannukset vuoden 2019 2. julkaisuaallossa](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
