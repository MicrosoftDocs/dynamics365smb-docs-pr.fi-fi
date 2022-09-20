---
title: Osittaisten toimitusten prosessointi
description: Myyntitilausten toimituksia voi käsitellä Business Centralin osatoimituksilla toimitusneuvonta- ja toimitettava määrä -kenttien avulla.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: shipping advice, partial shipments, partial deliveries, trade, customer sales order
ms.date: 08/12/2022
ms.author: a-reishima
ms.openlocfilehash: f279ce6c22c3e2167006bec315b53297d126929c
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2022
ms.locfileid: "9461253"
---
# <a name="process-partial-shipments"></a>Osittaisten toimitusten prosessointi

Osittaisessa toimituksessa tilausta ei toimiteta kerralla. Esimerkiksi 100 yksikön tilauksesta 40 yksikköä toimitetaan heti ja 60 yksikköä myöhemmin. Ohjelmassa ei ole rajoituksia yhteen tilaukseen tehtyjen toimitusten lukumäärästä.

Ennen kuin voit käyttää osittaisia toimituksia [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan, sinun täytyy kuitenkin määrittää, että asiakas hyväksyy osittaiset toimitukset, määrittämällä **asiakkaan kortti** -sivun **toimitusohje**-kentän. Vaihtoehtoisesti jos asiakas hyväksyy vain kokonaisia toimituksia mutta pyytää tai hyväksyy osittaisen toimituksen tietylle myyntitilaukselle, voit muuttaa **Toimitusohje**-kenttää ennen kirjausta.

[!INCLUDE [prod_short](includes/prod_short.md)] määrittää oletusarvoisesti **Asiakkaan kortti** -sivun kentän **osittaiseksi**, jolloin osittaiset toimitukset sallitaan. Jos kenttää on kuitenkin muutettu **valmiiksi**, **toimitettava määrä** -kenttä on estetty kyseisen asiakkaan myyntitilauksissa.

[!INCLUDE [order-ship-invoice_md](includes/order-ship-invoice.md)]

## <a name="see-also"></a>Katso myös

[Tuotteiden myyminen asiakkaan myyntitilauksen avulla](sales-how-sell-products.md)  
[Nimikkeiden lähettäminen](warehouse-how-ship-items.md)  
[Suoratoimitusten tekeminen](sales-how-drop-shipment.md)  
[Myynti](sales-manage-sales.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Hallinta](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
