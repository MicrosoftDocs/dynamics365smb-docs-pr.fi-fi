---
title: Kentän yhdistämismääritykset SEPA CAMT -tiedostoja tuotaessa | Microsoft Docs
description: Voit tuoda Euroopan markkinoilla tiliotetiedostot alueellisen SEPA (Single Euro Payments Area) -standardin mukaisessa muodossa.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/06/2023
ms.custom: bap-template
---
# <a name="field-mapping-when-importing-sepa-camt-files" />Kenttien vastaavuuksien määrittäminen tuotaessa SEPA-CAMT-tiedostoja

[!INCLUDE[prod_short](includes/prod_short.md)] tukee SEPA-tiliotteiden (CAMT-muoto) tuontia varten alueellista SEPA (Single Euro Payments Area) -standardia. Lisätietoja on kohdassa [AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md).  

 SEPA CAMT-standardilla itsellään on paikalliset variaatiot. Yleistä tiedonsiirtomääritystä on ehkä tämän vuoksi muokattava, jotta se voidaan mukauttaa standardin paikalliseen versioon. (Tämä määritys on **Tiedonsiirtomääritykset**-sivulla mainittava **SEPA CAMT** -koodi.) Seuraavissa taulukoissa osoitetaan elementin ja kentän välinen yhdistämismääritys taulukoissa 81, 273 ja 274, kun SEPA CAMT toteutetaan [!INCLUDE[prod_short](includes/prod_short.md)]issa.  

 Lisätietoja tietojenvaihtomäärityksen luomisesta tai muuttamisesta on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="camt-data-mapping-to-fields-in-the-general-journal-table-" />CAMT-tietojen kohdistaminen kenttiin yleinen päiväkirja -taulukossa (81)

|Elementin polku|Viestin elementti|Tietotyyppi|Kuvaus|Negatiivisen etumerkin tunniste|Kentän nro|Kentän nimi|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Summa|Desimaali|Rahamäärä käteiskirjauksessa||13|Summa|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Teksti|Ilmaisee, onko tapahtuma kredit- vai debet-tapahtuma|DBIT|13|Summa|  
|Stmt/Ntry/BookgDt/Dt|Pvm|Pvm|Päivämäärä, jolloin kirjaus on tiliöity tilille tilinhallinnoijan kirjoissa||5|Kirjauspvm|  
|Stmt/Ntry/BookgDt/DtTm|DateTime|DateTime|Päivämäärä ja aika, jolloin kirjaus on tiliöity tilille tilinhallinnoijan kirjoissa||5|Kirjauspvm|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Nimi|Teksti|Osallisen nimi, joka on velkaa rahasumman (viimeiselle) perijälle||1221|Maksajan tiedot|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Rakenteeton|Teksti|Rakenteettomassa muodossa olevat tiedot, jotka on toimitettu sen tapahtuman kohdistamiseen/täsmäytykseen nimikkeillä, jotka maksun tulisi selvittää, esimerkiksi myyntireskontrajärjestelmän kaupallisten laskujen.||8|Kuvaus|  
|Stmt/Ntry/AddtlNtryInf|LisätiedotMerkinnästä|Teksti|Lisätietoja merkinnästä||1222|Tapahtuman tiedot|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-table-" />CAMT-tietojen kohdistaminen kenttiin pankkitilin täsmäytys-taulukossa (273)

|Elementin polku|Viestin elementti|Tietotyyppi|Kuvaus|Negatiivisen etumerkin tunniste|Kentän nro|Kentän nimi|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/CreDtTm|CreationDateTime|Pvm|Päivämäärä ja kellonaika, jolloin sanoma luotiin.||3|Tiliotteen pvm|  
|Stmt/Bal/Amt|Summa|Desimaali|Summa, joka on seurasta kaikkien debet- ja kreditkirjausten summasta.||4|Tiliotteen loppusaldo|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-line-table-" />CAMT-tietojen kohdistaminen kenttiin pankkitilin täsmäytysrivi-taulukossa (274)

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

 Elementit **Ntry**-solmussa, jotka on tuotu [!INCLUDE[prod_short](includes/prod_short.md)] -järjestelmään, mutta joita ei ole kohdistettu mihinkään kenttiin, tallennetaan **Kirj. tiedonsiirron sarakemääritys** -taulukkoon. Käyttäjät voivat tarkastella näitä elementtejä **Maksujen täsmäytyskirjauskansio**-, **Maksun kohdistus**- ja **Pankkitilin täsmäytys** -sivuilla valitsemalla **Pankin tiliotteen rivierittely** -toiminnon. Lisätietoja on kohdassa [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]
> CAMT-tiliotteiden tuonnissa [!INCLUDE[prod_short](includes/prod_short.md)] edllyttää jokaisen tapahtuman olevan yksilöllinen, mikä tarkoittaa sitä, että CAMT-tiedoston *Stmt/Ntry/NtryDtls/TxDtls/Refs/EndToEndId*-tunnisteen **Tapahtumatunnus**-kentän tulee olla yksilöivä avoimen tilitäsmäytyksen sisällä. Jos tietoja ei ole olemassa, [!INCLUDE[prod_short](includes/prod_short.md)] jättää maksun huomiotta. Jos samalla pankkitilillä on kirjattu aikaisempi pankin täsmäytys, jolla on sama tapahtumatunnus kuin tämänhetkisessä tuonnissa, nykyistä tapahtumaa ei täsmäytetä automaattisesti, mutta se voidaan silti tuoda.

## <a name="see-also" />Katso myös

[Tiedonsiirron määrittäminen](across-set-up-data-exchange.md)  
[Sähköinen tiedonsiirto](across-data-exchange.md)  
[Käytä AMC Banking 365 Fundamentals -laajennusta](ui-extensions-amc-banking.md)  
[XML-mallien käyttäminen tietojenvaihtomääritysten valmisteluun](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
