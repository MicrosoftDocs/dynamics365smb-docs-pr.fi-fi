---
title: "Sekin asettelun määrittäminen| Microsoft Docs"
description: Voit suunnitella ja tulostaa sekkisi eri muodoissa standardinmukaisia vaatimuksia noudattaen.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 743cf7ecbed4157dc9283a97baa956e69ec0c6b5
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

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
| 10401 |Sekki (talonki/talonki/sekki) |Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/talonki/sekki. |
| 10411 |Sekki (talonki/sekki/talonki) |Tämä raportti on suunniteltu tulostamaan sekit muodossa sekki/talonki/sekki. |

Kun olet määrittänyt sekkien asettelut, voit tulostaa sekit **Maksupäiväkirja**-sivulla. Lisätietoja on kohdassa [Sekkien käyttäminen](payables-how-work-checks.md).

## <a name="see-also"></a>Katso myös
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Pankkitilien hallinta](bank-manage-bank-accounts.md)   
[Kauden lopun prosessien viimeisteleminen](year-how-complete-period-end-processes.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

