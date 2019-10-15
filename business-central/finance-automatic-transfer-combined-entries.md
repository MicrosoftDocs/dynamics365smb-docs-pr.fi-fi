---
title: Automaattinen siirto ja yhdistetyt tapahtumat | Microsoft Docs
description: Kustannuslaskennassa voi siirtää pääkirjanpitotapahtumat kustannustyyppiin yhdistetyn kirjauksen avulla. Voit määrittää, jos kustannustyyppi vastaanottaa yhdistettyjä tapahtumia **Yhdistä tapahtumat** -kentässä kustannustyypin määrityksessä. Seuraavassa taulukossa kuvaillaan eri asetukset.
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
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 0c07e470c1df8b9d9b5e7f7c833ff83b3c61be69
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306434"
---
# <a name="automatic-transfer-and-combined-entries"></a>Automaattinen siirto ja yhdistetyt tapahtumat
Voit siirtää kustannuslaskennassa pääkirjanpitotapahtumat kustannustyyppiin yhdistetyn kirjauksen avulla. Voit määrittää, jos kustannustyyppi vastaanottaa yhdistettyjä tapahtumia **Yhdistä tapahtumat** -kentässä kustannustyypin määrityksessä. Seuraavassa taulukossa kuvaillaan eri asetukset.  

|Yhdistä tapahtumat|Kuvaus|  
|---------------------|-----------------|  
|Ei mitään|Kukin pääkirjanpidon tapahtuma siirretään yksitellen vastaavaan kustannustyyppiin.|  
|Päivä|Kirjanpitotapahtumat, joilla on sama kirjauspäivämäärä, siirretään vastaavaan kustannustyyppiin yhtenä tapahtumana.|  
|Kuukausi|Saman kalenterikuukauden aikana kaikki pääkirjanpidon tapahtumat siirretään yhtenä tapahtumana vastaavaan kustannustyyppiin.|  

> [!IMPORTANT]  
>  Jos olet valinnut **Automaattinen siirto kirjanpidosta** -valintaruudun **Kustannuslaskennan asetukset** -sivulla, [!INCLUDE[d365fin](includes/d365fin_md.md)] päivittää kustannuslaskennan jokaisen kirjanpidon kirjauksen jälkeen. Yhdistetyt tapahtumat eivät ole mahdollisia.  

## <a name="see-also"></a>Katso myös  
 [Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md)   
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
