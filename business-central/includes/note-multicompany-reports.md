---
ms.service: dynamics-365-business-central
---
> [!NOTE]
> Oli mahdollista saada tietoja eri yrityksistä yhdessä raportissa OData-verkkopalveluiden avulla. Mutta [!INCLUDE [prod_short](prod_short.md)]:n vuoden 2021 2. julkaisuaallosta saakka vain ODataV4 on tuettu, eikä se vie tietoja useista yrityksistä. **$expand**-toimintoa Power BI:ssä, jota saatat kuvitella vaihtoehtoiseksi tavaksi luoda usean yrityksen raportti, ei myöskään voi käyttää. Se luo sarakkeen, jossa on yrityksen nimi, mutta ei täytä sitä yrityksen tiedoilla päivityksen jälkeen.