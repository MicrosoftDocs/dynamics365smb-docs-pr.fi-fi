---
title: Osittaisten toimitusten prosessointi
description: Myyntitilausten toimituksia voi käsitellä Business Centralin osatoimituksilla toimitusneuvonta- ja toimitettava määrä -kenttien avulla.
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'shipping advice, partial shipments, partial deliveries, trade, customer sales order'
ms.date: 08/12/2022
ms.author: bholtorf
---
# Osittaisten toimitusten prosessointi

Osittaisessa toimituksessa tilausta ei toimiteta kerralla. Esimerkiksi 100 yksikön tilauksesta 40 yksikköä toimitetaan heti ja 60 yksikköä myöhemmin. Ohjelmassa ei ole rajoituksia yhteen tilaukseen tehtyjen toimitusten lukumäärästä.

Ennen kuin voit käyttää osittaisia toimituksia [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan, sinun täytyy kuitenkin määrittää, että asiakas hyväksyy osittaiset toimitukset, määrittämällä **asiakkaan kortti** -sivun **toimitusohje**-kentän. Vaihtoehtoisesti jos asiakas hyväksyy vain kokonaisia toimituksia mutta pyytää tai hyväksyy osittaisen toimituksen tietylle myyntitilaukselle, voit muuttaa **Toimitusohje**-kenttää ennen kirjausta.

[!INCLUDE [prod_short](includes/prod_short.md)] määrittää oletusarvoisesti **Asiakkaan kortti** -sivun kentän **osittaiseksi**, jolloin osittaiset toimitukset sallitaan. Jos kenttää on kuitenkin muutettu **valmiiksi**, **toimitettava määrä** -kenttä on estetty kyseisen asiakkaan myyntitilauksissa.

[!INCLUDE [order-ship-invoice_md](includes/order-ship-invoice.md)]

## Katso myös

[Tuotteiden myyminen asiakkaan myyntitilauksen avulla](sales-how-sell-products.md)  
[Nimikkeiden lähettäminen](warehouse-how-ship-items.md)  
[Suoratoimitusten tekeminen](sales-how-drop-shipment.md)  
[Myynti](sales-manage-sales.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Hallinta](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
