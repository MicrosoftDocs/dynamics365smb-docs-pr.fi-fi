---
title: Huoltonimikkeiden luominen | Microsoft Docs
description: "Kun vastaanotat rekisteröimättömän nimikkeen huollettavaksi, sen voi rekisteröidä huoltonimikkeeksi."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: acd3305694186793ccc5c305573f62c16a718531
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-service-items"></a>Huoltonimikkeiden luominen
[!INCLUDE[d365fin](includes/d365fin_md.md)]issä huoltonimikkeellä tarkoitetaan huoltoa edellyttävää laitetta tai nimikettä. Kun luot huoltotilauksen, määrität huoltoa tarvitsevat nimikkeet. Voit linkittää huoltonimikkeen tilauksessa varaston tai huoltonimikeryhmän nimikkeeseen.    

Kun vastaanotat huoltoa tarvitsevan nimikkeen, voit rekisteröidä sen huoltonimikkeeksi. Sen voi tehdä usealla tavalla. Voit esimerkiksi luoda huoltonimikkeen **Huoltonimikkeet**-sivulla tai toisen prosessin osana esimerkiksi huoltotilausta käsiteltäessä.   

## <a name="to-create-a-service-item"></a>Huoltonimikkeiden luominen  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltonimikkeet** ja valitse sitten aiheeseen liittyvä linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>Huoltonimikkeiden luominen huoltotilauksissa  
Kun vastaanotat huollettavaksi nimikkeitä, jotka haluat rekisteröidä huoltonimikkeiksi, ne voi luoda huoltonimikkeiksi **Huoltotilaus**- tai **Huoltotarjous**-ikkunassa.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltotilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Valitse **Luo huoltonimike** -toiminto.  

    Numero annetaan huoltonimikkeelle ja huoltonimikekortti luodaan. Se täyttää **Huoltonimikkeen nro** -kentän uuden huoltonimikkeen numerolla.

## <a name="to-create-a-service-item-when-shipping-items"></a>Huoltonimikkeiden luominen nimikkeitä toimitettaessa  
Kun nimikkeitä toimitetaan kirjaamalla joko huoltotilauksia tai huoltolaskuja, ohjelma rekisteröi toimitetut nimikkeet automaattisesti huoltonimikkeiksi, jos seuraava ehto toteutuu: Nimikkeiden tulee kuulua huoltonimikeryhmään, jonka **Luo huoltonimike** -kentässä on valintamerkki. Jos nimikkeille on rekisteröity sarjanumero Nimikkeen seurantarivit -ikkunassa, ohjelma kopioi tämän tiedon automaattisesti huoltonimikekortin **Sarjanro**-kenttään huoltonimikkeiden luonnin yhteydessä.  

Seuraavassa kuvataan, miten huoltonimikkeitä luodaan huoltotilauksissa olevia nimikkeitä toimitettaessa.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltotilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Avaa haluamasi huoltotilaus.  
3. Valitse **Kirjaa**- tai **Kirjaa ja tulosta** -toiminto.  
4. Valitse **Toimitus**- tai **Toimitus ja lasku** -toiminto.  
5. Ohjelma luo automaattisesti huoltonimikkeet tilauksessa oleville nimikkeille, jos ne kuuluvat huoltonimikkeiden luomiseksi määritettyyn huoltonimikeryhmään. Jos **Nimikkeen seurantarivit** -ikkunassa on rekisteröity sarjanumeroita, ne määritetään huoltonimikkeille.  

> [!NOTE]  
>  Jos nimike on tuoterakenne ja olet purkanut tuoterakenteen, puretun tuoterakenteen nimikkeitä käsitellään tavallisen nimikkeen tavoin. Ohjelma luo huoltonimikkeet huoltonimikeryhmää koskevan ehdon ja mahdollisen sarjanumeroehdon mukaan. Jos lisäksi huoltonimike on luotu puretun tuoterakenteen nimikkeelle, joka muodostuu muista tuoterakenteen komponenteista, nämä nimikkeet luodaan puretun tuoterakenteen huoltonimikkeen huoltonimikkeen komponenteiksi.  
>   
>  Jos nimike on tuoterakenne etkä ole purkanut tuoterakennetta, ohjelma luo nimikkeelle huoltonimikkeen huoltonimikeryhmää koskevan ehdon ja mahdollisen sarjanumeroehdon mukaan.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>Aloitusmaksujen syöttäminen huoltonimikkeille
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltotehtävät** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Nimikkeen työkirja** -toiminto.
3. Valitse ensin huoltorivi ja sitten **Toiminnot**. Valitse sitten **Toiminnot** ja lopuksi **Syötä aloitusmaksu** -toiminto.  

    Ohjelma lisää **Kustannus**-tyypin huoltorivin, jolla on aloitusmaksu. Tämä aloitusmaksu koskee valittua huoltonimikettä.

## <a name="see-also"></a>Katso myös  
[Toimintaohje: Huoltonimikkeiden ja huoltonimikkeen komponenttien määrittäminen](service-how-setup-service-items.md)  
[Huoltohallinnon määrittäminen](service-setup-service.md)  
[Service Management](service-service.md)  

