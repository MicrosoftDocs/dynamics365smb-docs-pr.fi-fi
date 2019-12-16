---
title: Useiden korkoprosenttien määrittäminen
description: Voit laskea viivästyskulut useilla korkoprosenteilla tietylle jaksolle. Koron laskeminen on samanlaista kaikille viivästyskuluille. Ainoa ero on tietyn jakson korkoprosentti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: fd52a1cb3f139f5c21b4c1f0d6ce86f7aac7167c
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882636"
---
# <a name="set-up-multiple-interest-rates"></a>Useiden korkoprosenttien määrittäminen
Useita korkoprosentteja käytetään kauppatapahtumien viivästyneissä maksuissa eri jaksoilla. Esimerkiksi valtio määrittää asiakkaalta perittävän enimmäiskoron. Tätä korkoprosenttia voidaan muuttaa kahdesti vuoden aikana. Ajankohdat ovat 1.1. ja 1.7. Yritysten välinen (B2B) korkoprosentti sovitaan osapuolten kesken. Tämän asiakasryhmän korkoprosentille ei ole määritetty enimmäistasoa. Ilmoitettu korkoprosentti on yleensä neljä prosenttia enemmän kuin pankin normaali korko.

Kun luot viivästyskuluehdot ja muistutusehdot viivästysmaksulle, voit määrittää useita korkoprosentteja. Viivästysmaksu siis lasketaan eri kausille eri korkoprosentin mukaan. Lisätietoja on kohdassa [Avointen saldojen perintä](receivables-collect-outstanding-balances.md).

## <a name="to-set-up-multiple-interest-rates"></a>Useiden korkoprosenttien määrittäminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Viivästyskuluehdot** ja valitse sitten liittyvä linkki.  
2.  Valitse **Viivästyskuluehdot**-sivulla pakollinen rahoitusehto ja valitse sitten **Korkoprosentit**-toiminto.  
3.  Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Valitse **OK**-painike.  
5.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Muistutusehdot** ja valitse sitten liittyvä linkki.  
6.  Valitse **Muistutusehdot**-sivulla pakollinen muistutusehto ja valitse sitten **Tasot**-toiminto.  
7.  Valitse **Muistutustasot**-sivulla **Laske korko** -kenttä.  

Kun viivästyskululasku lähetetään, laskussa näkyvät viivästyskulut ja eri korkoprosentit tietyille ajanjaksoille. Lasku sisältää myös asiakkaan ja laskun lähettäneen yrityksen yhteystiedot, lisäsumman ja kokonaissumman. Laskun alkutapahtuma näkyy lihavoituna. Viivästyskulut lasketaan useilla korkoprosenteilla tietylle ajanjaksolle. Ne tulostetaan laskuun alkutapahtuman jälkeen.  

## <a name="see-also"></a>Katso myös  
[Avointen saldojen perintä](receivables-collect-outstanding-balances.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)
