---
author: brentholtorf
ms.topic: include
ms.date: 03/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

> [!NOTE]
> Kun yritys kopioidaan ympäristössä, jossa Dataverse- tai Sales-integrointi on otettu käyttöön, [!INCLUDE [prod_short](prod_short.md)] tyhjentää seuraavat asetukset kohdeyritykseen kopioitaessa:
>
> * Dataversen ja Dynamicsin yhteysasetukset varmistavat, että integrointi uudelleenalustaa kohdeyrityksen oikein.
> * Integrointitietueet varmistavat, että kohdeyritys ei osoita tietueisiin, jotka yhdistettiin lähdeyrityksessä.
> * Integroinnin synkronointityöt pysäyttävät synkronoinnin taustatyöt.
> * Mahdollinen synkronointi epäonnistuu, koska ne osoittavat lähdeyrityksen virheisiin ja niitä pidettäisiin kohdeyrityksissä turhina tietoina.