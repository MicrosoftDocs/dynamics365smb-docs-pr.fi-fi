---
title: Sekin asettelun määrittäminen| Microsoft Docs
description: Voit suunnitella ja tulostaa sekkisi eri muodoissa standardinmukaisia vaatimuksia noudattaen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/24/2019
ms.author: edupont
ms.openlocfilehash: f2b7fa01cff36e3aab335f7d5921954343c69b74
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243593"
---
# <a name="define-check-layouts"></a>Sekkien asetteluiden määrittäminen
Voit suunnitella omat sekit, joiden avulla pystyt noudattamaan paikallisten viranomaisten määrittämiä standardeja. Sekkikuvat voidaan tulostaa englannin-, ranskan ja espanjankielisinä.

Sekit suunnitellaan tulostettavaksi sekä Yhdysvaltojen että Kanadan sekkikuvamuodoissa joko muodossa sekki-talonki-sekki tai talonki-talonki-sekki.

## <a name="to-define-check-layouts"></a>Sekkien asetteluiden määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttivalintojen pankkitili** ja valitse sitten liittyvä linkki.
2. Valitse **Raporttivalinta - Pankkitili** -sivun **Käyttö**-kentässä **Sekki**.
3. Valitse jompikumpi seuraavista raportin tunnuksista:

  | Raportin tunnus | Raportin nimi | Kuvaus |
  | --- | --- | --- |
  | 1401 |Sekki |Tämä on oletusraportti. |
  | 10411 |Sekki (talonki/talonki/sekki) |Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/talonki/sekki. |
  | 10412 |Sekki (talonki/sekki/talonki) |Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/sekki/talonki. |
  | 10413 |Kolme sekkiä sivulla |Tämä raportti on suunniteltu tulostamaan kolme sekkiä kullakin sivulla. |

Kun olet määrittänyt sekkien asettelut, voit tulostaa sekit **Maksupäiväkirja**-sivulla. Lisätietoja on kohdassa [Sekkien käyttäminen](payables-how-work-checks.md).

## <a name="see-also"></a>Katso myös
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Pankkitilien hallinta](bank-manage-bank-accounts.md)   
[Kauden lopun prosessien viimeisteleminen](year-how-complete-period-end-processes.md)  
[[!INCLUDE[prodshort](includes/prodshort.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)
