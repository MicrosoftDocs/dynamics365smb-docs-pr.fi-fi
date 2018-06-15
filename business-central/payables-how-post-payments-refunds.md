---
title: "Maksujen kohdistaminen liittyviin asiakirjoihin ja sekä maksujen kirjaaminen | Microsoft Docs"
description: Kuvaa, miten kirjataan maksut toimittajille tai hyvitykset asiakkaille.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 04/30/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 3cad699234d95a849bf48f04c8462afa968789f6
ms.contentlocale: fi-fi
ms.lasthandoff: 05/15/2018

---
# <a name="record-payments-and-refunds"></a>Maksujen ja hyvitysten kirjaaminen
Kirjaat maksut toimittajille tai hyvitykset asiakkaille **Maksupäiväkirja**-ikkunassa. Kun kirjaat maksupäiväkirjan rivin, maksettu summa kirjataan määritetyn järjestelmän pankkitilille. Sinun on tehtävä sitten todellinen rahan siirto liittyvältä pankkitililtä muutaman vaiheen kautta.

Jos täytät **Kohdistetaan asiakirjaan nro** -kenttään maksettavan laskun tai hyvityslaskun, kyseinen asiakirja määritetään maksettavaksi, kun päiväkirja kirjataan. Tätä kutsutaan kohdistukseksi. Vaihtoehtona maksun kirjaamisen aikana voit käyttää **Kohdista toimittajatapahtumat**- tai **Kohdista asiakastapahtumat** -ikkunaa, kun olet tehnyt maksun kirjaamisen. Lisätietoja on esim. ohjeartikkelissa [Toimittajamaksujen täsmäyttäminen manuaalisesti](payables-how-apply-purchase-transactions-manually.md).

**Ehdota toimittajamaksuja** -toiminto voi auttaa sinua täyttämään maksupäiväkirjan rivit automaattisesti toimittajien priorisointien ja eräpäivien mukaan. Lisätietoja on kohdassa [Toimittajamaksujen ehdottaminen](payables-how-suggest-vendor-payments.md). Tätä toimintoa käytettäessä **Kohdistetaan asiakirjaan nro** -kenttä täytetään aina.

Maksun suorituksen kirjaamisen lisäksi voit käyttää myös **Maksupäiväkirja**-ikkunaa siirtämään maksun pankin lisäkäsittelyä varten. Lisätietoja on kohdissa [Sekkimaksujen suorittaminen](payables-how-work-checks.md) ja [Sähköisten maksujen suorittaminen](payables-how-export-payments-bank-file.md).  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksupäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa päiväkirjaerä, joka on varattu maksuja varten.
3. Jos tiedät, kenelle olet maksamassa maksun tai hyvityksen, täytä kentät manuaalisesti. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Voit myös kohdistaa maksun liittyvään laskuun tai hyvityslaskuun valitsemalla **Kohdistetaan asiakirjaan nro** -kentän **Kohdista toimittajatapahtumat** -ikkunassa, valitsemalla asianmukaisen laskun tai hyvityslaskun ja valitsemalla sitten **OK**-painikkeen.

    Monet kentät, kuten **Summa** ja **Eräpäivä**, täytetään nyt valitun asiakirjan tiedoilla.
5. Vaihtoehtoisesti voit käyttää **Ehdota toimittajamaksuja** -toimintoa. Myös kaikki kohdistustiedot ja summat syötetään päiväkirjariveille. Lisätietoja on kohdassa [Toimittajamaksujen ehdottaminen](payables-how-suggest-vendor-payments.md).

    Sanomat opastavat sinua täyttämään pakolliset kentät oikein.
6.  Kun kaikki maksupäiväkirjan rivit ovat valmiit, valitse **Kirjaa**-toiminto.

## <a name="see-also"></a>Katso myös
[Sekkimaksujen suorittaminen](payables-how-work-checks.md)  
[Sähköisten maksujen suorittaminen](payables-how-export-payments-bank-file.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Positive Pay -tiedoston vienti](finance-how-positive-pay.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

