---
title: "Rakennetiedot – Varianssi | Microsoft Docs"
description: "Varianssi on todellisten kustannusten ja vakiokustannuksen välinen ero seuraavan kaavan määrittämällä tavalla."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f01c57c3686764866c9d2a3c25d426e7f9a986a6
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-variance"></a>Rakennetiedot: varianssi
Varianssi on todellisten kustannusten ja vakiokustannuksen välinen ero seuraavan kaavan määrittämällä tavalla.  

 todellinen kustannus – standardikustannus = varianssi  

 Jos todellinen kustannus muuttuu esimerkiksi siksi, että kirjaat nimikekustannuksen myöhemmällä päivämäärällä, tällöin varianssi päivitetään vastaavasti.  

> [!NOTE]  
>  Uudelleenarvostus ei vaikuta varianssin laskentaan, koska uudelleenarvostus vaihtaa vain varaston arvon.  

## <a name="example"></a>Esimerkki  
 Seuraavassa esimerkissä kuvataan sitä, kuinka varianssi lasketaan laskutetuista nimikkeistä. Se perustuu seuraavaan skenaarioon:  

1.  Käyttäjä ostaa nimikkeen hintaan 90,00 (PVA), mutta vakiokustannus on 100,00 (PVA). Näin ollen ostovaihteluksi tulee 10,00 PVA.  
2.  10,00 PVA hyvitetään ostovaihtelutilille.  
3.  Käyttäjä kirjaa nimikekuluksi 20,00 (PVA). Näin ollen todellinen kustannus kasvatetaan arvoon 110,00 PVA ja oston varianssin arvoksi muuttuu 10,00 PVA.  
4.  20,00 PVA veloitetaan ostovaihtelutililtä. Näin ollen netto-ostovaihteluksi tulee 10,00 PVA.  
5.  Käyttäjä määrittää nimikkeen hinnaksi 70,00 (PVA) aiemman 100,00 (PVA):n sijaan. Tämä ei vaikuta erojen laskentaan, ainoastaan varaston arvoon.  

 Seuraavassa taulukossa on tuloksena saatavat arvotapahtumat.  

 ![Ostojen varianssin laskenta](media/design_details_inventory_costing_11_purchase_variance.png "design_details_inventory_costing_11_purchase_variance")  

## <a name="determining-the-standard-cost"></a>Vakiokustannuksen määrittäminen  
 Peruskustannuksia käytetään, kun lasketaan varianssia ja hyödynnettävää määrää. Koska peruskustannus voidaan vaihtaa ajan kuluessa manuaalisista päivityslaskuista johtuen, sinulla tulee olla ajankohta, kun peruskustannus on kiinteä varianssilaskennalle. Tässä kohdassa varastoarvon nousu laskutetaan. Valmistettujen tai koottujen nimikkeiden osalta vakiokustannuksen määrityskohta on kustannuksen muutoshetki.  

 Seuraava taulukko osoittaa, kuinka eri kustannusjaot lasketaan tuotetuille ja kootuille nimikkeille, kun käytät Laske peruskustannukset -toimintoa.  

|Kustannusjakauma|Ostettu nimike|Tuotettu tai koottu nimike|  
|----------------|--------------------|------------------------------|  
|**Vakiokustannus**||Yksitasoiset materiaalikustannukset + Yksitasoiset kapasiteettikustannukset + Yksitasoiset aliurakointikust. + Yksitasoiset kapasit. yleiskust. + Yksitasoiset tehdastuot. yleiskust.|  
|**Yksitasoinen materiaalikust.**|Yksikkökustannus|![Kaava 1](media/design_details_inventory_costing_11_equation_1.png "design_details_inventory_costing_11_equation_1")|  
|**Yksitasoinen kapasiteettikust.**|Ei sovellu|![Kaava 2](media/design_details_inventory_costing_11_equation_2.png "design_details_inventory_costing_11_equation_2")|  
|**Yksitasoinen alihank. kust.**|Ei sovellu|![Kaava 3](media/design_details_inventory_costing_11_equation_3.png "design_details_inventory_costing_11_equation_3")|  
|**Yksitasoinen kap. yleiskust.**|Ei sovellu|![Kaava 4](media/design_details_inventory_costing_11_equation_4.png "design_details_inventory_costing_11_equation_4")|  
|**Yksitasoinen tuotannon yleisk.**|Ei sovellu|(Yksitasoinen materiaalikust. + yksitasoinen kapasiteettikust. + yksitasoinen alihank. kustannus-) * välillinen kustannus % / 100 + yleiskustannus|  
|**Vyörytetty materiaalikust.**|Yksikkökustannus|![Kaava 5](media/design_details_inventory_costing_11_equation_5.png "design_details_inventory_costing_11_equation_5")|  
|**Vyörytetty kapasiteettikust.**|Ei sovellu|![Kaava 6](media/design_details_inventory_costing_11_equation_6.png "design_details_inventory_costing_11_equation_6")|  
|**Vyörytetty alihankkijakust.**|Ei sovellu|![Kaava 7](media/design_details_inventory_costing_11_equation_7.png "design_details_inventory_costing_11_equation_7")|  
|**Vyörytetty kapasiteettiyleiskustannus**|Ei sovellu|![Kaava 8](media/design_details_inventory_costing_11_equation_8.png "design_details_inventory_costing_11_equation_8")|  
|**Vyörytetty tuotannon yleiskust**|Ei sovellu|![Kaava 9](media/design_details_inventory_costing_11_equation_9.png "design_details_inventory_costing_11_equation_9")|  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)   
 [Rakennetiedot: Arvostusmenetelmät](design-details-costing-methods.md) [Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
 [Rahoitus](finance.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

