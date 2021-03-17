---
title: Tietokannan lukitusten tarkasteleminen
description: Lue miten voit tarkastella minkä tahansa tietokantalukkojen tietoja suoraan Business Centralin asiakasliittymästä.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 640608b810f3ad9812decc493ad4e35bcc316f98
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388147"
---
# <a name="viewing-database-locks"></a>Tietokannan lukitusten tarkasteleminen

Tietokannan lukitseminen ohjaa useiden käyttäjien samojen tietojen samanaikaista käyttöoikeutta. Voit suojata tapahtuman niin, että muut tapahtumat eivät voi muokata samoja tietoja, jos ensimmäinen tapahtuma asettaa tiedoille lukituksen. Lukitus säilyy tapahtuman valmistumiseen asti.

Käyttäjät eivät ehkä voi suorittaa tapahtumia lukittujen tietojen kanssa. Yleensä lukituksesta lähetetään viesti käyttäjille.

## <a name="to-view-database-locks"></a>Tietokannan lukitusten tarkasteleminen

Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Tietokannan lukitukset** ja valitse sitten aiheeseen liittyvä linkki.

**Tietokannan lukitukset** -sivu sisältää kaikkien nykyisten tietokannan lukitusten tilannevedoksen.

Lisätietoja tietokannan lukituksesta on kohdassa [Tietokannan lukitusten valvonta](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) Business Centralin kehittäjän ja IT-ammattilaisen ohjeessa.

## <a name="see-also"></a>Katso myös

[Tietokannan lukitusten valvonta](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]