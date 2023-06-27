---
title: Kenttien lisääminen Wordin raporttiasetteluun
description: Tässä aiheessa kuvaillaan raportin tietojoukon kenttien lisäämistä aiemmin luodun raportin Wordin raporttiasetteluun.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/25/2021
ms.author: jswymer
---

# <a name="work-with-word-layouts"></a>Wordin asettelujen käyttö

Wordin raporttiasettelu määrittää raportin sisällön ja muotoilun, kun raportti on esikatselussa ja tulostettu Business Centralista. Näitä asetteluita luodaan ja muokataan käyttämällä ohjelmaa Microsoft Word.

[![Esimerkki Word-raporttiasetteluasiakirjasta Business Centralille.](media/word-layout.png)](media/word-layout.png#lightbox) 

Kun muokkaat Wordin raporttiasettelua, voit määrittää raportin tietojoukon kentät, jotka sisällytetään raporttiin, sekä sen, miten kentät järjestetään. Voit myös määrittää raportin yleisen muodon, kuten tekstin fontin, koon, reunukset ja taustakuvat. Raportin sisältö järjestetään tavallisesti lisäämällä asetteluun taulukoita.

Voit tehdä yleisiä muotoilu- ja asettelumuutoksia, kuten vaihtaa tekstin fontin sekä lisätä taulukon ja muokata sitä tai poista tietokentän, käyttämällä samoja Wordin perustoimintoja kuin muissakin Word-asiakirjoissa.

Jos olet suunnittelemassa Wordin raporttiasettelua alusta tai lisäämässä uusia tietokenttiä, aloita lisäämällä taulukko, jossa on rivejä ja sarakkeita, jotka ovat lopulta tietokenttiä.

> [!TIP]  
> Näytä taulukon ruudukko siten, että näet taulukon solujen rajat. Muista piilottaa ruudukko, kun lopetat muokkauksen. Voit näyttää tai piilottaa ruudukot valitsemalla taulukon ja valitsemalla **Asettelu**-kohdan alta **Taulukko**-välilehdellä **Näytä ruudukko**.

## <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Fonttien upottaminen Word-asetteluihin yhdenmukaisuuden vuoksi

Upottamalla fontit Word-asiakirjaan voit varmistaa, että raportit näkyvät ja tulostuvat aiotuilla fonteilla riippumatta siitä, missä käyttäjä avaa tai tulostaa raportit. Fonttien upottaminen voi suurentaa merkittävästi Word-tiedostojen kokoa. Lisätietoja fonttien upottamisesta Wordiin on kohdassa [Fonttien upottaminen Wordissa, PowerPointissa tai Excelissä](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

## <a name="adding-data-fields"></a>Tietokenttien lisääminen

Raportin tietojoukko voi sisältää kenttiä, joissa näkyvät otsikot, tiedot ja kuvat. Tässä ohjeaiheessa käsitellään raportin tietojoukon kenttien lisääminen olemassa olevaan raportin Word-raporttiasetteluun. Lisäät kenttiä käyttämällä raportille mukautettua XML-osaa ja lisäämällä sisällön ohjausobjekteja, jotka on yhdistetty raportin tietojoukon kenttiin. Kenttien lisääminen edellyttää, että tunnet jonkin raportin tietojoukon niin, että voit tunnistaa kentät, jotka haluat lisätä asetteluun.  
  
> [!NOTE]  
>  Et voi muuttaa valmiita raporttiasetteluita<!--Onprem. Built-in layouts can only be modified by using the development environment-->.  

### <a name="to-open-the-custom-xml-part-for-the-report-in-word"></a><a name="OpenXMLPart"></a>Mukautetun XML-osan avaaminen raportille Wordissa
  
1. Jos se ei ole jo auki, avaa Word-raportin asettelun asiakirja Wordissa.  
  
     Lisätietoja on kohdassa [Raportin mukautetun asettelun luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).  
  
2. Näytä **Kehittäjä**-välilehti Microsoft Wordin valintanauhassa.  
  
     Oletuksena on, että **Kehittäjä**-välilehti ei ole näkyvissä valintanauhassa. Lisätietoja on kohdassa [Valintanauhan Kehitystyökalut-välilehden näyttäminen](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon).  
  
3. Valitse **Kehittäjä**-välilehdellä **XML-yhdistäminen-ruutu**.  
  
4. Valitse **XML-yhdistäminen**-ruudun avattavassa **Mukautettu XML-osa** -luettelossa tavallisesti luettelon viimeisenä oleva [!INCLUDE[prod_short](includes/prod_short.md)] -raportin mukautettu XML-osa. Mukautetun XML-osan nimen muoto on seuraava:  
  
     `urn:microsoft-dynamics-nav/reports/<report_name>/<ID>`  

     `<report_name>` on raportille määritetty nimi 

     `<ID>` on raportin tunnusnumero.  
  
     Kun valitset mukautetun XML-osan, XML:n yhdistäminen -ruudussa näkyvät otsikot ja kenttäohjausobjektit, jotka ovat käytettävissä raportissa.  
  
### <a name="to-add-a-label-or-data-field"></a>Selitteen tai tietokentän lisääminen
  
1. Aseta kohdistin asiakirjaan, johon haluat lisätä ohjausobjektin.  
  
2. Napsauta hiiren kakkospainikkeella lisättävää ohjausobjektia **XML-yhdistäminen**-ruudussa, valitse **Lisää ohjausobjekti** ja valitse sitten **Tavallinen teksti**.  
  
    > [!NOTE]  
    >  Et voi lisätä kenttää manuaalisesti kirjoittamalla tietojoukon kentän nimen sisällön ohjausobjektiin. Sinun on käytettävä **XML-yhdistäminen**-ruutua kenttien yhdistämiseen.  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list"></a>Tietokenttien toistuvien rivien lisääminen luettelon luomiseksi
  
1. Lisää taulukkoon taulukkorivi, joka sisältää sarakkeen, kullekin kentälle, jonka haluat toistuvan.  
  
   Tämä rivi toimii paikkamerkkinä toistuville kentille.  
  
2. Valitse koko rivi.  
  
3. Napsauta hiiren kakkospainikkeella **XML-yhdistäminen** -ruudussa ohjausobjektia, joka vastaa raportin tietokohdetta, joka sisältää toistettavat kentät ja valitse **Lisää sisällön ohjausobjekti** ja valitse sitten **Toistuva**.  
  
4. Lisää toistuvia kenttiä riviin seuraavasti:  
  
    1. Siirrä osoitin sarakkeeseen.  
  
    2. Napsauta hiiren kakkospainikkeella lisättävää ohjausobjektia **XML-yhdistäminen**-ruudussa, valitse **Lisää ohjausobjekti** ja valitse sitten **Tavallinen teksti**.  
  
    3. Toista työvaiheet a ja b kunkin kentän kohdalla.  
  
## <a name="adding-image-fields"></a>Kuvakenttien lisääminen

Raportin tietojoukko voi sisältää kentän, joka sisältää kuvan, kuten yrityksen logon tai kuvan kohteen. Voit lisätä kuvan raportin tietojoukosta lisäämällä sisällön **Kuva**-ohjausobjektin.  
  
Kuvat kohdistuvat automaattisesti sisällön hallinnan vasempaan yläkulmaan ja niiden koko muuttuu automaattisesti vastaamaan sisällön hallinnan rajoja.  
  
> [!IMPORTANT]  
> Voit lisätä vain kuvia, joiden muotoa Word tukee (esimerkiksi .bmp-, .png- ja .jpeg-tiedostotyypit). Jos lisäät sellaisen kuvan, jota Word ei tue, näyttöön avautuu virhesanoma, kun suoritat raportin [!INCLUDE[prod_short](includes/prod_short.md)] -asiakasohjelmasta.  
  
### <a name="to-add-an-image"></a>Kuvan lisääminen
  
1. Aseta osoitin asiakirjaan, johon haluat lisätä ohjausobjektin.  
  
2. Napsauta hiiren kakkospainikkeella lisättävää ohjausobjektia **XML-yhdistäminen**-ruudussa, valitse **Lisää ohjausobjekti** ja valitse sitten **Kuva**.  
  
3. Voit suurentaa tai pienentää kuvan kokoa vetämällä kahvaa poispäin sisällön ohjausobjektista tai sen keskustaa kohti.  

## <a name="removing-label-and-data-fields"></a><a name="RemoveField"></a> Otsikko- ja tietokenttien poistaminen

Raportin otsikko- ja tietokentät sisältyvät Wordin sisällön ohjausobjekteihin. Seuraavassa kuvassa on esitetty sisällön ohjausobjekti, kun se on valittuna Word-asiakirjassa.  

![Kentän sisällönhallinta Word-raporttiasettelussa.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

Selitteen tai tietokentän nimi näkyy sisällön ohjausobjektissa. Esimerkissä kentän nimi on CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>Selitteen tai tietokentän poistaminen

1. Napsauta poistettavaa kenttää hiiren kakkospainikkeella ja valitse **Poista sisällön hallinta**.  

     Sisällön ohjausobjekti poistetaan, mutta kentän nimi säilyy tekstinä.  

2. Poistaa jäljellä olevan tekstin tarpeen mukaan.

## <a name="custom-xml-part-overview"></a>Mukautetun XML-osan yleiskatsaus

Word-raporttiasettelut on rakennettu *mukautetuista XML-osista*. Raportin mukautettu XML-osa koostuu niitä tieto-osia, sarakkeita ja otsikoita vastaavista elementeistä, jotka muodostavat raportin tietojoukon. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->Mukautettua XML-osaa käytetään yhdistämään tietoja raporttiin, kun raportti suoritetaan.

### <a name="xml-structure-of-custom-xml-part"></a>Mukautetun XML-osan XML-rakenne

Seuraavassa taulukossa on yksinkertaistettu yhteenveto mukautetun XML-osan XML-koodista.  
  
|XML-elementit|Description|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|Otsikko|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|XML-nimitilan määritys. `<reportname>` on raportille määritetty nimi. `<id>` on raportille määritetty tunnus.|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|Sisältää kaikki raportin otsikot.<!--OnPren The element includes labels that are related to columns that have the IncludeCaption Property.--><br />-   Sarakkeisiin liittyvien otsikkoelementtien muoto on `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />-  Otsikkoelementtien muoto on `<LabelName>LabelName</LabelName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />-   Otsikot ovat aakkosjärjestyksessä.|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|Ylimmän tason tietokohde ja sarakkeet. Sarakkeet ovat aakkosjärjestyksessä.<!--OnPrem <br /><br /> The element names and values are determined by the Name Property of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|Tietojen kohteet ja sarakkeet, jotka sisältyvät ylimmän tason tietokohteeseen. Sarakkeet näkyvät aakkosjärjestyksessä vastaavien tietojen kohdassa.|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|Elementin sulkeminen.|  
  
### <a name="custom-xml-part-in-word"></a>Mukautettu XML-osa Wordissa

 Word -ohjelmassa mukautettu XML-osa avataan **XML-yhdistäminen**-ruudussa ja elementit yhdistetään ruudun avulla Word-asiakirjassa. **XML-yhdistäminen**-ruutua voi käyttää **Kehitystyökalut**-välilehdessä. (Lisätietoja on kohdassa [Valintanauhan Kehitystyökalut-välilehden näyttäminen](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon)).  
  
 **XML-yhdistäminen**-ruudun elementit näkyvät rakenteessa, joka vastaa XML-lähdettä. Otsikkokentät ryhmitellään yleisen **Otsikot**-elementin alle, tietokohteet ja sarakkeet järjestetään hierarkkiseen rakenteeseen, joka vastaa XML-tietolähdettä ja sarakkeet ovat aakkosjärjestyksessä. Elementit tunnistetaan niiden sarakkeen nimen perusteella, joka on määritelty raportin tietojoukossa AL-koodissa. Lisätietoja on kohdassa [Raportin tietojoukon määrittäminen](/dynamics365/business-central/dev-itpro/developer/devenv-report-dataset).  
  
 Seuraavassa kuvassa on yksinkertainen mukautettu XML-osa edellisestä osasta Word-asiakirjan **XML-yhdistäminen**-ruudusta.  
  
 ![XML-määritysruudun leike Wordissa.](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")  
  
* Voit lisätä selitteen tai kentän asettelun lisäämällä sisällön ohjausobjektin, joka liittyy **XML-yhdistäminen**-ruudussa olevaan elementtiin.  
  
* Voit luoda toistuvia sarakkeiden rivejä lisäämällä sisällön **Toistuva**-ohjausobjektin ylemmän tason tietokohteelle ja lisätä sen jälkeen sisällön ohjausobjektin sarakkeille.  
  
* Otsikoissa varsinainen luodussa raportissa näkyvä teksti on **Otsikko**-ominaisuuden arvo tietoyksikkötaulukon kentälle (jos otsikko liittyy raportin tietojoukon sarakkeeseen) tai raportin otsikkosuunnittelijan otsikkoon (jos otsikko ei liity tietojoukon sarakkeeseen).  
  
* Raportin suorituksen aikana näkyvä tunnuksen kieli määräytyy raporttiobjektin kieliasetuksen perusteella.  
  
## <a name="see-also"></a>Katso myös

[Raporttien mukautetun asettelun luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
