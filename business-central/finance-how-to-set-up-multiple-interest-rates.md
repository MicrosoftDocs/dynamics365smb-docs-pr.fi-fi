---
title: Useiden korkoprosenttien määrittäminen
description: Voit laskea viivästyskulut useilla korkoprosenteilla tietylle jaksolle. Koron laskeminen on samanlaista kaikille viivästyskuluille. Ainoa ero on tietyn jakson korkoprosentti.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e6312b1e00b3267c582dac50da616bdccd2a75b7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305978"
---
# <a name="set-up-multiple-interest-rates"></a>Useiden korkoprosenttien määrittäminen
Useita korkoprosentteja käytetään kauppatapahtumien viivästyneissä maksuissa eri jaksoilla. Esimerkiksi valtio määrittää asiakkaalta perittävän enimmäiskoron. Tätä korkoprosenttia voidaan muuttaa kahdesti vuoden aikana. Ajankohdat ovat 1.1. ja 1.7. Yritysten välinen (B2B) korkoprosentti sovitaan osapuolten kesken. Tämän asiakasryhmän korkoprosentille ei ole määritetty enimmäistasoa. Ilmoitettu korkoprosentti on yleensä neljä prosenttia enemmän kuin pankin normaali korko.

Kun luot viivästyskuluehdot ja muistutusehdot viivästysmaksulle, voit määrittää useita korkoprosentteja. Viivästysmaksu siis lasketaan eri kausille eri korkoprosentin mukaan. Lisätietoja on kohdassa [Avointen saldojen perintä](receivables-collect-outstanding-balances.md).

## <a name="to-set-up-multiple-interest-rates"></a>Useiden korkoprosenttien määrittäminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Viivästyskuluehdot** ja valitse sitten liittyvä linkki.  
2.  Valitse **Viivästyskuluehdot**-sivulla pakollinen rahoitusehto ja valitse sitten **Korkoprosentit**-toiminto.  
3.  Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Valitse **OK**-painike.  
5.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muistutusehdot** ja valitse sitten liittyvä linkki.  
6.  Valitse **Muistutusehdot**-sivulla pakollinen muistutusehto ja valitse sitten **Tasot**-toiminto.  
7.  Valitse **Muistutustasot**-sivulla **Laske korko** -kenttä.  

Kun viivästyskululasku lähetetään, laskussa näkyvät viivästyskulut ja eri korkoprosentit tietyille ajanjaksoille. Lasku sisältää myös asiakkaan ja laskun lähettäneen yrityksen yhteystiedot, lisäsumman ja kokonaissumman. Laskun alkutapahtuma näkyy lihavoituna. Viivästyskulut lasketaan useilla korkoprosenteilla tietylle ajanjaksolle. Ne tulostetaan laskuun alkutapahtuman jälkeen.  

## <a name="see-also"></a>Katso myös  
[Avointen saldojen perintä](receivables-collect-outstanding-balances.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)
