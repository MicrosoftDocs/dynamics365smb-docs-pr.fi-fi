---
title: Tietokannan lukitusten tarkasteleminen
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1153ffc97d0f22c889ff23c5a27a8c0446b17018
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196376"
---
# <a name="viewing-database-locks"></a>Tietokannan lukitusten tarkasteleminen

## <a name="about-locks"></a>Tietoja lukituksista

Tietokannan lukitseminen ohjaa useiden käyttäjien samojen tietojen samanaikaista käyttöoikeutta. Voit suojata tapahtuman niin, että muut tapahtumat eivät voi muokata samoja tietoja, jos ensimmäinen tapahtuma asettaa tiedoille lukituksen. Lukitus säilyy tapahtuman valmistumiseen asti.

Käyttäjät eivät ehkä voi suorittaa tapahtumia lukittujen tietojen kanssa. Yleensä lukituksesta lähetetään viesti käyttäjille.

## <a name="to-view-database-locks"></a>Tietokannan lukitusten tarkasteleminen

Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Tietokannan lukitukset** ja valitse sitten aiheeseen liittyvä linkki.

**Tietokannan lukitukset** -sivu sisältää kaikkien nykyisten tietokannan lukitusten tilannevedoksen.

Lisätietoja tietokannan lukituksesta on kohdassa [Tietokannan lukitusten valvonta](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) Business Centralin kehittäjän ja IT-ammattilaisen ohjeessa.

## <a name="see-also"></a>Katso myös

[Tietokannan lukitusten valvonta](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) 
