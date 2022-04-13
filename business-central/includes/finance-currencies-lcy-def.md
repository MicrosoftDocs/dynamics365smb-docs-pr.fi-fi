---
author: edupont04
ms.topic: include
ms.date: 03/15/2022
ms.author: edupont
ms.openlocfilehash: c391e7d6492a722de10801212ccd04a532f8a971
ms.sourcegitcommit: 521735f8e27d8bff2d2dfbe94d240c09dcdaec29
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/15/2022
ms.locfileid: "8419592"
---
Yritysten toimiessa yhä useammassa maassa tai alueella niiden on välttämätöntä pystyä tekemään kauppaa ja raportoimaan taloustiedot useissa valuutoissa. Paikallinen valuutta (PVA) määritetään **Pääkirjanpidon asetukset** -sivulla kuten artikkelissa [Pääkirjanpidon ja tilikartan ymmärtäminen](../finance-general-ledger.md) kuvataan. Kun paikallinen valuutta (PVA) on määritetty, se esitetään tyhjänä valuuttana, joten kun **Valuutta**-kenttä on tyhjä, se tarkoittaa, että valuutta on PVA.  

Seuraavaksi sinun täytyy määrittää valuuttakoodit jokaiselle valuutalle, jota käytät, jos ostat tai myyt muussa valuutassa kuin paikallisessa valuutassa (PVA). Myös pankkitilit voidaan luoda käyttämällä valuuttoja. Pääkirjanpidon tapahtumia voi tallentaa eri valuutoissa, mutta pääkirjanpidon tapahtuma kirjataan aina paikallisessa valuutassa (PVA).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Pääkirjanpito määritetään käyttämään paikallista valuuttaa (PVA), mutta voit määrittää sen käyttämään myös toista valuuttaa, jolle määritetään ajantasainen vaihtokurssi. Kun toinen valuutta määritetään niin sanotuksi lisäraportointivaluutaksi, [!INCLUDE[prod_short](prod_short.md)] tallentaa summat automaattisesti sekä PVA:na että lisäraportointivaluuttana kuhunkin KP-tapahtumaan sekä muihin tapahtumiin, kuten ALV-tapahtumiin. Lisätietoja on kohdassa [Lisäraportointivaluutan määrittäminen](../finance-how-setup-additional-currencies.md). Lisäraportointivaluuttaa käytetään useimmiten taloudelliseen raportointiin omistajille, jotka asuvat muita kuin paikallista valuuttaa (PVA) käyttävissä maissa tai alueilla.  

> [!IMPORTANT]
> Jos haluat käyttää lisäraportointivaluuttaa taloudellisessa raportoinnissa, varmista, että ymmärrät rajoitukset. Lisätietoja on kohdassa [Lisäraportointivaluutan määrittäminen](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Kun kirjaat KP:oon käyttämällä valuutan koodia, esimerkiksi kirjataksesi kulun yleiseen päiväkirjaan käyttämällä valuuttakoodia, tapahtuma muunnetaan PVA:ksi käyttäen kirjauspäivämäärän valuutanvaihtokurssia. KP-tapahtuma ei sisällä tietoja siitä, mitä valuuttaa käytettiin, ja vain sen arvo PVA:ssa. Jos haluat seurata alkuperäistä valuuttaa, esimerkiksi laskua, sinun täytyy käyttää myynti- ja ostoasiakirjoja sekä pankkitilitietoja, jotka tallentavat tapahtumien valuuttakoodin.
