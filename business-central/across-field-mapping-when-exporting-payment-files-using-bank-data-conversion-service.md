---
title: Pankin maksutiedostojen viennissä käytettävät kentän yhdistämismääritykset | Microsoft Docs
description: Kun viet maksutiedostoja AMC Banking 365 Fundamentals -laajennuksen avulla, vietävät tiedot paljastuvat palveluntarjoajalle.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f705334d42d27e22d9108a410ab91a213c725a4d
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437750"
---
# <a name="field-mapping-when-exporting-payment-files-using-the-amc-banking-365-fundamentals-extension"></a>Kentien yhdistäminen, kun maksutiedostoja viedään AMC Banking 365 Fundamentals -laajennuksen avulla
Kun viet maksutiedostoja AMC Banking 365 Fundamentals -laajennuksen avulla, vietävät tiedot paljastuvat palveluntarjoajalle. Palveluntarjoaja vastaa näiden tietojen tietosuojasta. Lisätietoja AMC Banking 365 Fundamentals -laajennuksesta on kohdassa [AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md).  

> [!CAUTION]  
>  Kun viet maksutiedostoja AMC Banking 365 Fundamentals -laajennuksen avulla, joitakin yritystietoja paljastuu palveluntarjoajalle. Palveluntarjoaja, AMC Consult A/S, vastaa näiden tietojen tietosuojasta. Lisätietoja on kohdassa [AMC:n tietosuojakäytäntö](https://go.microsoft.com/fwlink/?LinkId=510158).  

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)]in yleisessä versiossa asetetaan ja yhdistetään yleiset palvelut pankkitietojen muuntamiseen mihin tahansa pankkisi vaatimaan muotoon. Pohjois-Amerikan versioissa samaa palvelua voi käyttää maksutiedostojen lähettämiseen sähköisenä rahansiirtona (EFT), esimerkkinä usein käytetty ACH-verkko (Automated Clearing House), joskin prosessi on hieman erilainen.

Seuraavassa taulukossa on luettelo kentistä [!INCLUDE[prod_short](includes/prod_short.md)]:ssä, joista voit viedä tietoja.  

|Määritetty kenttä|Taulun kenttä|Sivupöytä|Kuvaus|  
|------------------|--------------------|-----------|---------------------------------------|  
|Luotonantajan nro|Luotonantajan nro|Pankkitili|Tunniste, jonka pankki on liittänyt yritykseen maksujen keräämiseksi|  
|Lähettäjän pankkitilin numero|Pankkitilin nro / IBAN|Pankkitili|Yrityksen pankkitilin numero (IBAN tai muu), joka on määritetty pankkitilin kortissa|  
|Lähettäjän pankin Clearing-standardi|Pankin Clearing-standardi|Pankkitili|Keskuspankin nimien rekisteri, jota käytetään lähettäjän pankkitiliin|  
|Lähettäjän pankin Clearing-koodi|Pankin Clearing-koodi|Pankkitili|Lähettäjän pankin tunniste, joka liittyy käytettävään pankin nimien rekisteriin|  
|Lähettäjän pankin BIC|SWIFT-koodi|Pankkitili|Lähettäjän pankkitilin SWIFT tunnus|  
|Lähettäjän pankkitilin valuutta|Valuutan koodi|Pankkitili|Lähettäjän pankkitilin valuuttakoodi|  
|Asiakirjan nro|Asiakirjan nro|Yleisen päiväkirjan rivi|Maksurivin asiakirjanumero|  
|Kohdist. ulk. asiak. nro|Kohdist. ulk. asiak. nro|Yleisen päiväkirjan rivi|Maksuriviä vastaavan laskun tai hyvityslaskun ulkoisen asiakirjan numero.|  
|Vastaanottajan tunnus|Tilinro|Yleisen päiväkirjan rivi|Maksurivillä määritetyn asiakkaan tai toimittajan numero|  
|Maksutyyppi|Pankkitietojen muunnon maksutyyppi|Maksutapa|Pankkisiirron tyyppi, kuten kotimainen tai kansainvälinen|  
|Maksuviittaus|Maksuviittaus|Yleisen päiväkirjan rivi|Maksurivin maksuviite|  
|Vastaanottajan osoite|Osoite|Asiakas/Toimittaja|Asiakas- tai toimittajakortissa määritetty vastaanottajan osoite|  
|Vastaanottajan kaupunki|Paikkakunta|Asiakas/Toimittaja|Asiakas- tai toimittajakortissa määritetty vastaanottajan kaupunki|  
|Vastaanottajan nimi|Nimi|Asiakas/Toimittaja|Asiakas- tai toimittajakortissa määritetty vastaanottajan nimi|  
|Vastaanottajan maa-/aluekoodi|Maa-/aluekoodi|Asiakas/Toimittaja|Asiakas- tai toimittajakortissa määritetty vastaanottajan maa- tai aluekoodi|  
|Vastaanottajan postinumero|Postinro|Asiakas/Toimittaja|Asiakas- tai toimittajakortissa määritetty vastaanottajan postinumero|  
|Vastaanottajan pankkitilin numero|Pankkitilin nro / IBAN|Asiakkaan pankkitili / toimittajan pankkitili|Vastaanottajan pankkitilin numero (IBAN tai muu), joka on määritetty asiakkaan tai toimittajan pankkitilin kortissa|  
|Vastaanottajan pankin Clearing-koodi|Pankin Clearing-standardi|Asiakkaan pankkitili / toimittajan pankkitili|Keskuspankin nimien rekisteri, jota käytetään vastaanottajan pankkitiliin|  
|Vastaanottajan pankin Clearing-stan.|Pankin Clearing-koodi|Asiakkaan pankkitili / toimittajan pankkitili|Vastaanottajan pankkitilin tunniste, joka liittyy käytettävään pankin nimien rekisteriin|  
|Vastaanottajan sähköpostiosoite|Sähköposti|Asiakas/Toimittaja|Vastaanottajan sähköpostiosoite|  
|Viesti vastaanottajalle 1|Viesti vastaanottajalle|Yleisen päiväkirjan rivi|Viesti vastaanottajalle, joka on määritetty maksurivillä|  
|Summa|Summa|Yleisen päiväkirjan rivi|Maksurivin summa|  
|Valuutan koodi|Valuutan koodi|Yleisen päiväkirjan rivi|Maksurivin valuuttakoodi|  
|Siirtopäivämäärä|Kirjauspvm|Yleisen päiväkirjan rivi|Maksurivin kirjauspäivä|  
|Laskun summa|Alkuperäinen summa|Asiakas-/toimittajatapahtuma|Tapahtuman summa, johon maksu kohdistetaan.|  
|Laskun päivämäärä|Asiakirjan pvm|Asiakas-/toimittajatapahtuma|Tapahtuman laskupäivämäärä, johon maksu kohdistetaan|  
|Vastaanottajan pankin osoite|Osoite|Asiakkaan pankkitili / toimittajan pankkitili|Vastaanottajan pankkitilin osoite, joka on määritetty asiakkaan tai toimittajan pankkitilin kortissa|  
|Vastaanottajan pankkitilin osoite, joka on määritetty asiakkaan tai toimittajan pankkitilin kortissa|Paikkakunta|Asiakkaan pankkitili / toimittajan pankkitili|Vastaanottajan pankkitilin kaupunki, joka on määritetty asiakkaan tai toimittajan pankkitilin kortissa|  
|Vastaanottajan pankin nimi|Nimi|Asiakkaan pankkitili / toimittajan pankkitili|Vastaanottajan pankkitilin nimi, joka on määritetty asiakkaan tai toimittajan pankkitilin kortissa|  
|Vastaanottajan pankin maa/alue|Maa-/aluekoodi|Asiakkaan pankkitili / toimittajan pankkitili|Vastaanottajan pankkitilin maa tai alue, joka on määritetty asiakkaan tai toimittajan pankkitilin kortissa|  
|Vastaanottajan pankin postinumero|Postinro|Asiakkaan pankkitili / toimittajan pankkitili|Vastaanottajan pankkitilin postinumero, joka on määritetty asiakkaan tai toimittajan pankkitilin kortissa|  
|Lähettäjän pankin osoite|Osoite|Pankkitili|Lähettäjän pankkitilin osoite, joka on määritetty pankkitilin korttiin|  
|Lähettäjän pankin paikkakunta|Paikkakunta|Pankkitili|Lähettäjän pankkitilin kaupunki, joka on määritetty pankkitilin korttiin|  
|Lähettäjän pankin nimi|Nimi|Pankkitili|Lähettäjän pankkitilin nimi, joka on määritetty pankkitilin korttiin|  
|Lähettäjän pankin maa/alue|Maa-/aluekoodi|Pankkitili|Lähettäjän pankkitilin maa tai alue, joka on määritetty pankkitilin korttiin|  
|Lähettäjän pankin postinumero|Postinro|Pankkitili|Lähettäjän pankkitilin postinumero, joka on määritetty pankkitilin korttiin|  
|Yleisen päiväkirjan malli|Päiväkirjan mallin nimi|Yleisen päiväkirjan rivi|Yleisen päiväkirjan malli, jota käytetään maksurivillä|  
|Yleisen päiväkirjan erän nimi|Päiväkirjan erän nimi|Yleisen päiväkirjan rivi|Yleisen päiväkirjan erän nimi, jota käytetään maksurivillä|  
|Lähettäjän pankin nimi – tiet. muunto|Pankin nimi - Tietojen muuntaminen|Pankkitili|Lähettäjän pankkitilin nimi, jota AMC Banking 365 Fundamentals -laajennus on pyytänyt ja joka on määritetty pankkitilin kortissa|  

## <a name="see-also"></a>Katso myös  
[Tiedonsiirron määrittäminen](across-set-up-data-exchange.md)  
[Tietojen vaihtaminen sähköisesti](across-data-exchange.md)
[AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md)   
[Maksujen suorittaminen AMC Banking 365 Fundamentals -laajennuksen tai SEPA-tilisiirron avulla](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]