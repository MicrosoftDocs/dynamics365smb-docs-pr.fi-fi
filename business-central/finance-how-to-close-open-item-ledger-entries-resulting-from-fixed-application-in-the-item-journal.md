---
title: Nimikepäiväkirjan kiinteästä kohdistuksesta aiheutuvien avointen nimiketapahtumien sulkeminen | Microsoft Docs
description: Voit luoda **Nimikepäiväkirja**-sivun **Kohdistukset tapahtumista** -kentässä manuaalisesti kiinteän kohdistuksen saapuvan tapahtuman ja lähtevän alkuperäisen tapahtuman välille. Voit korjata esimerkiksi lähtevän tapahtuman tai käsitellä sen palautuksen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 289c0aecbf45bbece3291edeed6e0e72aedb9a6b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924201"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Nimikepäiväkirjan kiinteästä kohdistuksesta aiheutuvien avointen nimiketapahtumien sulkeminen
Voit luoda **Nimikepäiväkirja**-sivun **Kohdistukset tapahtumista** -kentässä manuaalisesti kiinteän kohdistuksen saapuvan tapahtuman ja lähtevän alkuperäisen tapahtuman välille. Voit korjata esimerkiksi lähtevän tapahtuman tai käsitellä sen palautuksen. Lisätietoja on kohdassa Kohdistukset tapahtumista.  

> [!IMPORTANT]  
>  Tällä tavoin tehdyt kiinteät kohdistukset koskevat vain kustannuksia, eivät määrää. Näin ollen kirjattu positiivinen nimiketapahtuma ei sulje käytettyä lähtevää tapahtumaa, ja pysyy itse avoinna. Tämä pätee myös silloin, kun positiivisen tapahtuman kiinteä kohdistus kirjataan negatiiviseen tapahtumaan, jota tavallinen positiivinen tapahtuma ei ole sulkenut, jolloin sekä negatiivinen että positiivinen tapahtuma jäävät avoimiksi.  
>   
>  Tämä tarkoittaa myös sitä, että varastokautta ei voi sulkea, jos tällainen tapahtuma on olemassa.  

Seuraavassa ohjeessa neuvotaan, miten sulkea nämä tapahtumat suorittamalla kaksi korjaavaa kirjausta nimikepäiväkirjaan.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>Sulje avoimet nimiketapahtumat, jotka aiheutuvat nimikepäiväkirjan kiinteästä kohdistuksesta  

1.  Kirjaa **Kohdistukset tapahtumista** -kentässä positiivinen muutos ja vastaava määrä. Tämä sulkee alkuperäisen korjaavan negatiivisen tapahtuman, jossa on kiinteä kohdistus.  
2.  Kirjaa negatiivinen muutos **Kohdistetaan tapahtumaan** -kentässä. Tämä sulkee alkuperäisen korjaavan positiivisen tapahtuman, jossa on kiinteä kohdistus.  

## <a name="see-also"></a>Katso myös  
[ Nimiketapahtumien poistaminen ja uudelleenkohdistaminen](finance-how-to-remove-and-reapply-item-entries.md)  
 [Myynnin palautusten ja peruutusten käsittely](sales-how-process-sales-returns-cancellations.md)   
 [Varastonarvostuksen ja kustannuslaskennan määrittäminen](finance-set-up-inventory-valuation-and-costing.md)   
 [Varaston kustannusten hallinta](finance-manage-inventory-costs.md)   
 [Rakennetiedot: Arvostusmenetelmät](design-details-costing-methods.md)
