---
author: brentholtorf
ms.topic: include
ms.date: 03/04/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
Jos yrityksesi toimii useammassa kuin yhdessä maassa tai alueella, on todennäköisesti tärkeää, että voit harjoittaa liiketoimintaa useammassa kuin yhdessä valuutassa. Paikallinen valuutta (PVA) määritetään **Pääkirjanpidon asetukset** -sivulla. Myöhemmin paikallinen valuutta näkyy tyhjänä valuuttana asiakirjoissa ja tapahtumissa. Kun **Valuutta**-kenttä on tyhjä, valuutta on PVA.

Seuraavassa videossa kerrotaan, miten paikallinen valuutta määritetään.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1iM1n]

Seuraavaksi sinun täytyy määrittää valuuttakoodit jokaiselle valuutalle, jota käytät, jos ostat tai myyt muussa valuutassa kuin paikallisessa valuutassa (PVA). Myös pankkitilit voidaan luoda käyttämällä valuuttoja. Pääkirjanpidon tapahtumia voi tallentaa eri valuutoissa, mutta pääkirjanpidon tapahtuma kirjataan aina paikallisessa valuutassa (PVA).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Pääkirjanpito määritetään käyttämään paikallista valuuttaa (PVA), mutta voit määrittää sen käyttämään myös toista valuuttaa, jolle määritetään ajantasainen vaihtokurssi. Kun toinen valuutta määritetään lisäraportointivaluutaksi, [!INCLUDE[prod_short](prod_short.md)] tallentaa summat automaattisesti sekä PVA:na että lisäraportointivaluuttana kuhunkin KP-tapahtumaan sekä muihin tapahtumiin, kuten ALV-tapahtumiin. Lisätietoja on kohdassa [Lisäraportointivaluutan määrittäminen](../finance-how-setup-additional-currencies.md). Lisäraportointivaluuttaa käytetään useimmiten taloudelliseen raportointiin omistajille, jotka asuvat muita kuin paikallista valuuttaa (PVA) käyttävissä maissa tai alueilla.  

> [!IMPORTANT]
> Jos haluat käyttää lisäraportointivaluuttaa taloudellisessa raportoinnissa, varmista, että ymmärrät rajoitukset. Lisätietoja on kohdassa [Lisäraportointivaluutan määrittäminen](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Kun kirjaat pääkirjanpitoon käyttäen ulkomaan valuuttaa, [!INCLUDE [prod_short](prod_short.md)] muuntaa tapahtuman PVA:ksi käyttäen kirjauspäivämäärän valuutan vaihtokurssia. KP-tapahtuma ei sisällä tietoja siitä, mitä valuuttaa käytettiin, ja vain sen arvo PVA:ssa. Voit seurata alkuperäistä valuuttaa käyttämällä myynti- ja ostotositteita ja pankkitilejä, jotka tallentavat valuuttatiedot kirjauksia varten.
