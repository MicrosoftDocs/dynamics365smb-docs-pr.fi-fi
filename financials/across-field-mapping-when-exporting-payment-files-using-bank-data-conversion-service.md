---
title: "Pankin maksutiedostojen viennissä käytettävät kentän yhdistämismääritykset | Microsoft Docs"
description: "Kun viet maksutiedostoja pankkitietojen muuntopalvelun avulla, vietävät tiedot paljastetaan pankkitietojen muuntopalvelun tarjoajalle."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: aa3569037e79f79b0a644511361901d0844e58a3
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="field-mapping-when-exporting-payment-files-using-bank-data-conversion-service"></a>Kenttien vastaavuuksien määrittäminen vietäessä maksutiedostot käyttämällä pankkitietojen muuntopalvelua
Kun viet maksutiedostoja pankkitietojen muuntopalvelun avulla, vietävät tiedot paljastetaan pankkitietojen muuntopalvelun tarjoajalle. Palveluntarjoaja vastaa näiden tietojen tietosuojasta. Lisätietoja pankkitietojen muuntopalvelun toiminnasta on ohjeaiheessa [Tietoja tiedonvaihto-kehyksestä](across-about-the-data-exchange-framework.md).  

> [!CAUTION]  
>  Kun viet maksutiedostoja pankkitietojen muuntopalvelun avulla, joitakin yritystietoja paljastetaan palvelun tarjoajalle. Palveluntarjoaja, AMC Consult A/S, vastaa näiden tietojen tietosuojasta. Lisätietoja on kohdassa [AMC:n tietosuojakäytäntö](http://go.microsoft.com/fwlink/?LinkId=510158).  

Seuraavassa taulukossa on [!INCLUDE[d365fin](includes/d365fin_md.md)] -kentät, joista tiedot voidaan viedä palveluntarjoajalle.  

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
|Lähettäjän pankin nimi – tiet. muunto|Pankin nimi - Tietojen muuntaminen|Pankkitili|Lähettäjän pankkitilin nimi, jota pankkitietojen muuntopalvelu on pyytänyt, ja joka on määritetty pankkitilin kortissa|  

## <a name="see-also"></a>Katso myös  
[Tiedonsiirron määrittäminen](across-set-up-data-exchange.md)  
[Sähköinen tiedonsiirto](across-data-exchange.md)
[Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md)   
[Suorita maksut pankkitietojen muunnospalvelulla tai SEPA-hyvityksen siirrolla](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   

