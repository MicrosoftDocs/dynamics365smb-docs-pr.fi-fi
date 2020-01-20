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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 137d44db160d0f1e832cc344a779e6bf01a64bbd
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2911129"
---
# <a name="select-a-check-layout"></a>Sekin asettelun valitseminen
Voit suunnitella omat sekit, joiden avulla pystyt noudattamaan paikallisten viranomaisten määrittämiä standardeja. Sekkikuvat voidaan tulostaa englannin-, ranskan ja espanjankielisinä.

Sekit suunnitellaan tulostettavaksi sekä Yhdysvaltojen että Kanadan sekkikuvamuodoissa joko muodossa sekki-talonki-sekki tai talonki-talonki-sekki.

## <a name="to-select-a-check-layout"></a>Sekin asettelun valitseminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Raporttivalintojen pankkitili** ja valitse sitten liittyvä linkki.
2. Valitse **Raporttivalinta - Pankkitili** -sivun **Käyttö**-kentässä **Sekki**.
3. Valitse jompikumpi seuraavista raportin tunnuksista:

| Raportin tunnus | Raportin nimi | Kuvaus |
| --- | --- | --- |
| 1401 |Sekki |Tämä on oletusraportti. |
| 10411 |Sekki (talonki/talonki/sekki) |Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/talonki/sekki. |
| 10412 |Sekki (talonki/sekki/talonki) |Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/sekki/talonki. |
| 10413 |Kolme sekkiä sivulla |Tämä raportti on suunniteltu tulostamaan kolme sekkiä kullakin sivulla. |

Kun olet määrittänyt sekkien asettelut, voit tulostaa sekit **Maksupäiväkirja**-sivulla. Lisätietoja on kohdassa [Sekkien käyttäminen](payables-how-work-checks.md).

Voit muuttaa jotakin näistä sekkien oletusasetteluista käyttämällä joko Word- tai RDLC-integrointia. Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Katso myös
[Raporttien mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)   
[Kauden lopun prosessien viimeisteleminen](year-how-complete-period-end-processes.md)  
[[!INCLUDE[prodshort](includes/prodshort.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)
