---
author: brentholtorf
ms.topic: include
ms.date: 04/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

## <a name="best-practices-for-working-with-column-definitions"></a>Sarakemääritysten käytön parhaat käytännöt

Sarakemäärityksiä ei versioida. Kun muutat sarakemääritystä, vanha versio korvataan, kun muutos tallentuu tietokantaan. Seuraavassa luettelossa on joitakin parhaita käytäntöjä sarakemääritysten parissa työskentelemiseen.

- Jos lisäät sarakemääritelmiä, valitse hyvä koodi ja täytä kuvaus-kenttään merkityksellinen teksti samalla kun tiedät, mihin sarakemääritystä käytetään. Näiden tietojen avulla työkaverisi (ja tuleva itsesi) voivat työskennellä talousraportoinnin parissa ja ehkä muuttaa sarakkeen määrittelyä.
- Ennen kuin muutat sarakemääritystä, harkitse kopion ottamista varmuuskopioksi siltä varalta, että muutos ei toimi odotetulla tavalla. Voit joko kopioida määrityksen (antaa sille hyvän nimen) tai viedä sen. Lisätietoja on kohdassa [siirry sarakemääritysten tuomiseen tai viemiseen](#import-or-export-financial-report-column-definitions).
- Jos tarvitset uuden kopion määrityksestä, jonka [!INCLUDE [prod_short](prod_short.md)] tarjoaa, helppo tapa saada sellainen, on luoda uusi yritys, joka sisältää vain asetustietoja. Vie sitten määritys ja tuo se yritykseen, jossa määrityksen päivitystä tarvitaan.
