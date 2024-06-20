---
title: Taloudellisten yleiskatsausten käsittely Excelissä
description: 'Lisätietoja raporttien avaamisesta Microsoft Excelissä, jotta analysointi toimii Business Central -sovelluksessa paremmin.'
author: brentholtorf
ms.topic: overview
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: 9027
ms.date: 08/23/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="analyzing-financial-statements-in-microsoft-excel"></a>Rahoituslaskelmien analysointi Microsoft Excelissä

[!INCLUDE [prod_short](includes/prod_short.md)] tarjoaa suorituskykyilmaisimia ja antaa yleiskatsauksia yrityksesi taloudesta. Seuraavassa on esimerkkejä tavoista analysoida KPI:tä ja yleiskatsauksia Excelissä:

* Avaa luettelot Excelissä tietojen analysointia varten. 
* Vie raskaita raportteja, kuten taseita ja tuloslaskelmia, Exceliin, analysoida tietoja ja tulostaa raportit.  

> [!TIP]
> Excelissä näkyvät raportit on suunniteltu siten, että niiden avulla voidaan analysoida kuluvaa vuotta. Tuloslaskelmaraportti on kuitenkin poikkeus. Raportin avulla voit suodattaa tiedot niin, että ne sisältävät aikaisempien vuosien analyysit.

## <a name="getting-the-overview-and-the-details-in-excel"></a>Yleiskuvan ja yksityiskohtien tarkastelu Excelissä

Liiketoimintajohtajan ja kirjanpitäjän roolikeskusten **Raportit**-toiminnon avulla voit valita Excelissä tarkasteltavat tilinpäätökset. Kun valitse raportin, se avautuu Excelissä tai Excel Onlinessa. Apuohjelma yhdistää tiedot [!INCLUDE [prod_short](includes/prod_short.md)]iin. Kirjautumiseen on kuitenkin käytettävä sitä tiliä, jolla [!INCLUDE [prod_short](includes/prod_short.md)]ia käytetään. Seuraavassa taulukossa on luettelo raporteista ja siitä, missä ne ovat saatavilla.  


|Raportti  |Roolikeskus  |
|---------|---------|
|Tase                 | Liiketoimintajohtaja, kirjanpitäjä |
|Tuloslaskelma              | Liiketoimintajohtaja, kirjanpitäjä |
|Kassavirtalaskelma       | Liiketoimintajohtaja, kirjanpitäjä |
|Jakamattoman voiton laskelma| Liiketoimintajohtaja, kirjanpitäjä |
|Kerätty arvonlisävero         | Liiketoimintajohtaja, kirjanpitäjä |
|Asiakkaan tiliotteet           | Liiketoimintajohtaja, kirjanpitäjä |
|Ostovelkojen tilanne         | Kirjanpitäjä |
|Myyntisaatavien tilanne      | Kirjanpitäjä |

Oletetaan, että haluat porautua kassavirtaan. Voit avata liiketoimintajohtajan tai kirjanpitäjän roolikeskuksessa **rahavirtalaskelman** Excelissä; tosiasiassa tarvittavat tiedot viedään luotavaan Excelin työkirjaan ennalta määritetyn mallin mukaisesti. Joissakin selaimissa sinua voidaan pyytää avaamaan tai tallentamaan työkirja.  

Excelissä on välilehti, jossa tiedot on sijoitettu ensimmäiseen työkirjaan. Kaikki viedyt tiedot ovat esillä muissa työkirjoissa, jos satut tarvitsemaan niitä. Voit tulostaa raportin heti tai voit muokata sitä, kunnes käytössä on haluamasi yleiskatsaus ja yksityiskohdat. Voit suodattaa ja analysoida tietoja entistä paremmin [!INCLUDE [prod_short](includes/prod_short.md)]in Excel-apuohjelmalla.  

### <a name="understanding-the-excel-templates"></a>Excel-mallien ymmärtäminen

Esimääritetyt Excel-raportit perustuvat valitun yrityksen tietoihin. Esimerkkiyritys on esimerkiksi määrittänyt tilikarttaan kolme käteistiliä, jotka on lueteltu *Nykyisissä käyttöomaisuuserissä*: 10100 **Sekkitili**, 10200 **Säästötili** ja 10300 **Käteiskassa**. **Tilien alaluokka** -kentän arvoksi on määritetty *Käteinen*, ja niiden yhteenlaskettu summa näkyy *Käteisenä* **Taseen** Excel-raportissa.  

Excel-työkirjan muut taulukot näyttävät raportin taustalla olevat tiedot. Jos haluat tietää, mikä Excel-raporttien ryhmittelyiden perustana on, sinun täytyy ehkä suodattaa [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman luettelot.  

## <a name="the--excel-add-in"></a>[!INCLUDE [prod_short](includes/prod_short.md)]in Excel-apuohjelma

[!INCLUDE [prod_short](includes/prod_short.md)]-kokemus sisältää Excelin apuohjelman. Tilauksen mukaan kirjaudut joko automaattisesti tai sinun on annettava kirjautumistiedot [!INCLUDE [prod_short](includes/prod_short.md)]iin. Lisätietoja on kohdassa [Tarkasteleminen ja muokkaaminen Excelissä Business Centralista](across-work-with-excel.md).  

Apuohjelman ansiosta saat uusimmat tiedot [!INCLUDE [prod_short](includes/prod_short.md)]ista ja voit siirtää muutokset takaisin [!INCLUDE [prod_short](includes/prod_short.md)]iin. Mahdollisuus siirtää tiedostot takaisin tietokantaan ei ole käytöstä tarkasteltavissa Excel-raporteissa.  

## <a name="see-also"></a>Katso myös

[Näyttäminen ja muokkaaminen Excelissä Business Centralista](across-work-with-excel.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Business Centralin käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
