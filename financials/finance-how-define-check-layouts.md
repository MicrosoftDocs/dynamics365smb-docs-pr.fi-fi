---
title: "Toimintaohje: Sekkien asetteluiden määrittäminen| Microsoft Docs"
description: "Lisätietoja Financialsiin sisältyvistä sekkien asetteluista."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 03/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6081b6d09fa75b868138817442d6df4d9a8d0d7f
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-define-check-layouts"></a>Toimintaohje: Sekkien asetteluiden määrittäminen
Voit suunnitella omat sekit, joiden avulla pystyt noudattamaan paikallisten viranomaisten määrittämiä standardeja. Sekkikuvat voidaan tulostaa englannin-, ranskan ja espanjankielisinä.

Sekit suunnitellaan tulostettavaksi sekä Yhdysvaltojen että Kanadan sekkikuvamuodoissa joko muodossa sekki-talonki-sekki tai talonki-talonki-sekki.

## <a name="to-define-check-layouts"></a>Sekkien asetteluiden määrittäminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Raporttivalintojen pankkitili** ja valitse sitten liittyvä linkki.
2. Valitse **Raporttivalinta - Pankkitili** -ikkunan **Käyttö**-kentässä **Sekki**.
3. Valitse jompikumpi seuraavista raportin tunnuksista:

| Raportin tunnus | Raportin nimi | Kuvaus |
| --- | --- | --- |
| 1401 |Sekki |Tämä on oletusraportti. |
| 10401 |Sekki (talonki/talonki/sekki) |Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/talonki/sekki. |
| 10411 |Sekki (talonki/sekki/talonki) |Tämä raportti on suunniteltu tulostamaan sekit muodossa sekki/talonki/sekki. |

Kun olet määrittänyt sekkien asettelut, voit tulostaa sekit **Maksupäiväkirja**-ikkunassa. Lisätietoja on kohdassa [Sekkien käyttäminen](payables-how-work-checks.md).

## <a name="see-also"></a>Katso myös
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Pankkitilien hallinta](bank-manage-bank-accounts.md)   
[Kauden lopun prosessien viimeisteleminen](year-how-complete-period-end-processes.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

