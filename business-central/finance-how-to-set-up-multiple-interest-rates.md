---
title: "Useiden korkoprosenttien määrittäminen"
description: "Voit laskea viivästyskulut useilla korkoprosenteilla tietylle jaksolle. Koron laskeminen on samanlaista kaikille viivästyskuluille. Ainoa ero on tietyn jakson korkoprosentti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0af01fe46f6b7df1149825c35a9fc0cc19482403
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-multiple-interest-rates"></a>Useiden korkoprosenttien määrittäminen
Useita korkoprosentteja käytetään kauppatapahtumien viivästyneissä maksuissa eri jaksoilla. Esimerkiksi valtio määrittää asiakkaalta perittävän enimmäiskoron. Tätä korkoprosenttia voidaan muuttaa kahdesti vuoden aikana. Ajankohdat ovat 1.1. ja 1.7. Yritysten välinen (B2B) korkoprosentti sovitaan osapuolten kesken. Tämän asiakasryhmän korkoprosentille ei ole määritetty enimmäistasoa. Ilmoitettu korkoprosentti on yleensä neljä prosenttia enemmän kuin pankin normaali korko.

Kun luot viivästyskuluehdot ja muistutusehdot viivästysmaksulle, voit määrittää useita korkoprosentteja. Viivästysmaksu siis lasketaan eri kausille eri korkoprosentin mukaan. Lisätietoja on kohdassa [Avointen saldojen perintä](receivables-collect-outstanding-balances.md).

## <a name="to-set-up-multiple-interest-rates"></a>Useiden korkoprosenttien määrittäminen  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Viivästyskuluehdot** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Viivästyskuluehdot**-ikkunassa pakollinen rahoitusehto ja valitse sitten **Korkoprosentit**-toiminto.  
3.  Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Valitse **OK**-painike.  
5.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Muistutusehdot** ja valitse sitten aiheeseen liittyvä linkki.  
6.  Valitse **Muistutusehdot**-ikkunassa pakollinen muistutusehto ja valitse sitten **Tasot**-toiminto.  
7.  Valitse **Muistutustasot**-ikkunassa **Laske korko** -kenttä.  

Kun viivästyskululasku lähetetään, laskussa näkyvät viivästyskulut ja eri korkoprosentit tietyille ajanjaksoille. Lasku sisältää myös asiakkaan ja laskun lähettäneen yrityksen yhteystiedot, lisäsumman ja kokonaissumman. Laskun alkutapahtuma näkyy lihavoituna. Viivästyskulut lasketaan useilla korkoprosenteilla tietylle ajanjaksolle. Ne tulostetaan laskuun alkutapahtuman jälkeen.  

## <a name="see-also"></a>Katso myös  
[Avointen saldojen perintä](receivables-collect-outstanding-balances.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)

