---
title: "Kentän yhdistämismääritykset SEPA CAMT -tiedostoja tuotaessa | Microsoft Docs"
description: Voit tuoda Euroopan markkinoilla tiliotetiedostot alueellisen SEPA (Single Euro Payments Area) -standardin mukaisessa muodossa.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 6588f01c557b1c0586097766aa8a6f84d545bc6e
ms.contentlocale: fi-fi
ms.lasthandoff: 11/10/2017

---
# <a name="field-mapping-when-importing-sepa-camt-files"></a>Kenttien vastaavuuksien määrittäminen tuotaessa SEPA-CAMT-tiedostoja
[!INCLUDE[d365fin](includes/d365fin_md.md)] tukee SEPA-tiliotteiden (CAMT-muoto) tuontia varten alueellista SEPA (Single Euro Payments Area) -standardia. Lisätietoja on kohdassa [Toimintaohje: Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md).  

 SEPA CAMT-standardilla itsellään on paikalliset variaatiot. Yleistä tiedonsiirtomääritystä on ehkä tämän vuoksi muokattava, jotta se voidaan mukauttaa standardin paikalliseen versioon. (Tämä määritys on **Kirjauksen tiedonsiirtomääritykset** -ikkunassa mainittava **SEPA CAMT** -koodi.) Seuraavissa taulukoissa osoitetaan elementin ja kentän välinen yhdistämismääritys taulukoissa 81, 273 ja 274, kun SEPA CAMT toteutetaan [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.  

 Lisätietoja tietojenvaihtomäärityksen luomisesta tai muuttamisesta on kohdassa [Toimintaohje: Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="camt-data-mapping-to-fields-in-the-general-journal-table-81"></a>CAMT-tietojen kohdistaminen kenttiin yleinen päiväkirja -taulukossa (81)  

|Elementin polku|Viestin elementti|Tietotyyppi|Kuvaus|Negatiivisen etumerkin tunniste|Kentän nro|Kentän nimi|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Summa|Desimaali|Rahamäärä käteiskirjauksessa||13|Summa|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Teksti|Ilmaisee, onko tapahtuma kredit- vai debet-tapahtuma|DBIT|13|Summa|  
|Stmt/Ntry/BookgDt/Dt|Pvm|Pvm|Päivämäärä, jolloin kirjaus on tiliöity tilille tilinhallinnoijan kirjoissa||5|Kirjauspvm|  
|Stmt/Ntry/BookgDt/DtTm|DateTime|DateTime|Päivämäärä ja aika, jolloin kirjaus on tiliöity tilille tilinhallinnoijan kirjoissa||5|Kirjauspvm|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Nimi|Teksti|Osallisen nimi, joka on velkaa rahasumman (viimeiselle) perijälle||1221|Maksajan tiedot|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Rakenteeton|Teksti|Rakenteettomassa muodossa olevat tiedot, jotka on toimitettu sen tapahtuman kohdistamiseen/täsmäytykseen nimikkeillä, jotka maksun tulisi selvittää, esimerkiksi myyntireskontrajärjestelmän kaupallisten laskujen.||8|Kuvaus|  
|Stmt/Ntry/AddtlNtryInf|LisätiedotMerkinnästä|Teksti|Lisätietoja merkinnästä||1222|Tapahtuman tiedot|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-table-273"></a>CAMT-tietojen kohdistaminen kenttiin pankkitilin täsmäytys-taulukossa (273)  

|Elementin polku|Viestin elementti|Tietotyyppi|Kuvaus|Negatiivisen etumerkin tunniste|Kentän nro|Kentän nimi|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/CreDtTm|CreationDateTime|Pvm|Päivämäärä ja kellonaika, jolloin sanoma luotiin.||3|Tiliotteen pvm|  
|Stmt/Bal/Amt|Summa|Desimaali|Summa, joka on seurasta kaikkien debet- ja kreditkirjausten summasta.||4|Tiliotteen loppusaldo|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-line-table-274"></a>CAMT-tietojen kohdistaminen kenttiin pankkitilin täsmäytysrivi-taulukossa (274)  

|Elementin polku|Viestin elementti|Tietotyyppi|Kuvaus|Negatiivisen etumerkin tunniste|Kentän nro|Kentän nimi|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Summa|Desimaali|Rahamäärä käteiskirjauksessa||7|Tiliotteen summa|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Teksti|Ilmaisee, onko tapahtuma kredit- vai debet-tapahtuma|DBIT|7|Tiliotteen summa|  
|Stmt/Ntry/BookgDt/Dt|Pvm|Pvm|Päivämäärä, jolloin kirjaus on tiliöity tilille tilinhallinnoijan kirjoissa||5|Transaktiopvm|  
|Stmt/Ntry/BookgDt/DtTm|DateTime|DateTime|Päivämäärä ja aika, jolloin kirjaus on tiliöity tilille tilinhallinnoijan kirjoissa||5|Transaktiopvm|  
|Stmt/Ntry/ValDt/Dt|Pvm|Pvm|Päivämäärä, jolloin varat tulevat käyttöön tilinomistajalle kredit-tiliöintitapauksessa, tai loppuu olemasta tilinomistajan käytössä Debet-tiliöintitapauksessa.||12|Arvopvm|  
|Stmt/Ntry/ValDt/DtTm|DateTime|DateTime|Päivämäärä ja aika, jolloin varat tulevat käyttöön tilinomistajalle kredit-tiliöintitapauksessa, tai loppuu olemasta tilinomistajan käytössä Debet-tiliöintitapauksessa.||12|Arvopvm|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Nimi|Teksti|Osallisen nimi, joka on velkaa rahasumman (viimeiselle) perijälle||15|Maksajan tiedot|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Rakenteeton|Teksti|Rakenteettomassa muodossa olevat tiedot, jotka on toimitettu sen tapahtuman kohdistamiseen/täsmäytykseen nimikkeillä, jotka maksun tulisi selvittää, esimerkiksi myyntireskontrajärjestelmän kaupallisten laskujen.||6|Kuvaus|  
|Stmt/Ntry/AddtlNtryInf|LisätiedotMerkinnästä|Teksti|Lisätietoja merkinnästä||16|Tapahtuman tiedot|  

 Elementit **Ntry**-solmussa, jotka on tuotu [!INCLUDE[d365fin](includes/d365fin_md.md)] -järjestelmään, mutta joita ei ole kohdistettu mihinkään kenttiin, tallennetaan **Kirj. tiedonsiirron sarakemääritys** -taulukkoon. Käyttäjät voivat tarkastella näitä elementtejä **Maksujen täsmäytyskirjauskansio**-, **Maksun kohdistus**- ja **Pankkitilin täsmäytys** -ikkunassa valitsemalla **Pankin tiliotteen rivierittely** -toiminnon. Lisätietoja on kohdassa [Toimintaohje: Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).  
## <a name="see-also"></a>Katso myös  
[Tiedonsiirron määrittäminen](across-set-up-data-exchange.md)  
[Sähköinen tiedonsiirto](across-data-exchange.md)  
[Toimintaohje: Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md)   
[Toimintaohje: XML-rakenteiden käyttäminen tiedonsiirtomääritysten valmistelussa](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Toimintaohjeet: Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md)  

