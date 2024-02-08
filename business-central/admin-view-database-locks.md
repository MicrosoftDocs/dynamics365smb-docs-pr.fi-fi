---
title: Tietokannan lukitusten tarkasteleminen
description: Lue miten voit tarkastella asiakkaan tietokantalukkojen tietoja suoraan Business Centralin asiakasliittymästä.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: 9511
ms.date: 06/14/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="viewing-database-locks"></a>Tietokannan lukitusten tarkasteleminen

Tietokannan lukitseminen ohjaa useiden käyttäjien samojen tietojen samanaikaista käyttöoikeutta. Voit suojata tapahtuman niin, että muut tapahtumat eivät voi muokata samoja tietoja, jos ensimmäinen tapahtuma asettaa tiedoille lukituksen. Lukitus säilyy tapahtuman valmistumiseen asti.

Käyttäjät eivät ehkä voi suorittaa tapahtumia lukittujen tietojen kanssa. Yleensä lukituksesta lähetetään viesti käyttäjille.

## <a name="to-view-database-locks"></a>Tietokannan lukitusten tarkasteleminen

Valitse ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Tietokannan lukitukset** ja valitse sitten vastaava linkki.

**Tietokannan lukitukset** -sivu sisältää kaikkien nykyisten tietokannan lukitusten tilannevedoksen.

Lisätietoja tietokannan lukituksesta on kohdassa [Tietokannan lukitusten valvonta](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) Business Centralin kehittäjän ja IT-ammattilaisen ohjeessa.

## <a name="see-also"></a>Katso myös

[Tietokannan lukitusten valvonta](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]
