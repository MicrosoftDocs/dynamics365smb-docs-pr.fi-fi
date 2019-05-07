---
title: Useat sopimukset | Microsoft Docs
description: Asiakkaan kanssa tehtyjen huoltotasosopimusten mukaan saatetaan sama huoltonimike joutua sisällyttämään useaan huoltosopimukseen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: abc62fabc1429c647e0d618193240bd292350fbd
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "918886"
---
# <a name="multiple-contracts"></a>Useita sopimuksia
Asiakkaan kanssa tehtyjen huoltotasosopimusten mukaan sama huoltonimike on ehkä sisällytettävä useaan huoltosopimukseen.  
  
Sisällyttämällä huoltonimikkeen useaan sopimukseen voit tehdä seuraavat toiminnot:  
  
* Tehdä samasta huoltonimikkeestä erilaisia sopimuksia.  
* Huoltaa osat erikseen.  
* Ottaa huomioon huoltonimikkeen eri osien, kuten mekaanisten osien ja ohjelmiston, huollon vaatimat eri taidot.  
* Määrittää huoltonimikkeen eri osien huollolle eri vastausajat ja tiheydet.  
* Ottaa huomioon huoltonimikkeelle tehtävät erilaiset toimenpiteet, kun huoltonimike vaatii erityyppistä huolto eri aikoina.  
* Valita ja määrittää huoltonimikeriville oikean sopimusnumero huoltotilausta luotaessa.  
* Käsitellä huoltonimikkeiden ja huoltotasosopimusten taloudellisia tietoja.  
  
Seuraavassa on esimerkkejä usean sopimuksen käyttämisestä:  
  
## <a name="creating-multiple-contracts-per-service-item"></a>Usean sopimuksen luominen huoltonimikkeelle  
Huoltonimikkeille, jotka on jo rekisteröity saman asiakkaan ei-peruutettuihin sopimuksiin, voidaan luoda manuaalisesti huoltosopimus tai huoltotarjous. Tämä tehdään noudattamalla normaalia huoltosopimusten ja huoltosopimustarjousten luontiprosessia. Lisätietoja on kohdassa [Huoltosopimusten ja huoltosopimustarjousten käyttäminen](service-how-to-create-service-contracts-and-service-contract-quotes.md).  
  
Kun toiseen huoltosopimukseen tai sopimustarjoukseen jo rekisteröity huoltonimike lisätään sopimusriville, ohjelma näyttää varoitussanoman, jossa varoitetaan, että huoltonimike kuuluu jo yhteen tai useaan huoltosopimukseen tai sopimustarjoukseen. Jos sanoma vahvistetaan, järjestelmä kopioi kaikki tarvittavat huoltonimikkeen tiedot juuri luodulle sopimusriville.  
  
## <a name="copying-documents"></a>Asiakirjojen kopioiminen  
Toiseen huoltosopimukseen tai sopimustarjoukseen jo rekisteröidylle huoltonimikkeille voidaan luoda automaattisesti huoltosopimus tai sopimustarjous **Kopioi asiakirja** -toiminnolla.  
  
## <a name="creating-service-orders-for-multiple-contracts"></a>Huoltotilausten luominen usealle sopimukselle  
Useaan voimassa olevaa sopimukseen rekisteröidylle huoltonimikkeelle voidaan luoda huoltotilaus manuaalisesti. Huoltosopimus on voimassa, kun se on allekirjoitettu, eikä se ole vielä vanhentunut.  
  
## <a name="see-also"></a>Katso myös  
[Huoltosopimusten toteuttaminen](service-fulfill-service-contracts.md)  
[Huoltotilausten luominen](service-how-to-create-service-orders.md)  
