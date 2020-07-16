---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 06/25/2020
ms.author: edupont
ms.openlocfilehash: 8c5f4205128d52ec88f432cea7ece98e0310546d
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528008"
---
Ennen sähköpostin lokiinkirjauksen määrittämistä Exchange Onlineen on valmisteltava [yleiset kansiot](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019). Se voidaan tehdä [Exchangen hallintakeskuksessa](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019) tai käyttämällä [Exchange-palvelimen hallintaliittymää](/powershell/exchange/exchange-management-shell?view=exchange-ps).  

> [!TIP]
> Jos haluat käyttää [Exchange-palvelimen hallintaliittymää](/powershell/exchange/exchange-management-shell?view=exchange-ps), [BCTech-säilöön](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging) on julkaistu mallikomentosarja, joka voi toimia mallina komentosarjan määrittämisessä.

Seuraavassa on luettelossa keskeiset vaiheet sekä linkkejä lisätietoihin.  

- Yleisten kansioiden järjestelmänvalvojan roolin luonti seuraavan taulukon tietojen perusteella:

  |Ominaisuus        |Arvo                     |
  |----------------|--------------------------|
  |Name            |Yleisten kansioiden hallinta |
  |Valitut roolit  |Yleiset kansiot            |
  |Valitut jäsenet|Sen käyttäjätilin sähköposti, jota Business Central käyttää sähköpostin lokiinkirjaustyön suorittamiseen|

  Lisätietoja on kohdassa [Rooliryhmien hallinta](/exchange/permissions/role-groups?view=exchserver-2019).

- Uuden yleisen kansioin postilaatikon luonti seuraavan taulukon tietojen perusteella:

  |Ominaisuus        |Arvo                     |
  |----------------|--------------------------|
  |Name            |Julkinen postilaatikko            |

  Lisätietoja on kohdassa [Yleisen kansion postilaatikon luonti Exchange Serverissa](/exchange/collaboration/public-folders/create-public-folder-mailboxes).  

- Uusien yleisten kansioiden luominen

  - Luo juuritasolle uusi yleinen kansio, jonka nimi on *Email Logging*, jolloin kansion täydellinen polku on ```\Email Logging\```
  - Luo kaksi alikansiota, jolloin kansioiden täydelliseksi poluksi tulee
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  Lisätietoja on kohdassa [Yleisen kansion luonti](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019).

- Sähköpostin käyttöönotto yleisessä *Queue*-kansiossa

  Lisätietoja on kohdassa [Sähköpostin käyttöönotto tai käytöstäpoistaminen yleisessä kansiossa](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019)

- Sähköpostin käyttöönoton sähköpostien lähettämiseen yleiseen *Queue*-kansioon käyttämällä Outlookia tai Exchange-palvelimen hallintaliittymää

  Lisätietoja on kohdassa [Luvan antaminen anonyymeille käyttäjille sähköpostin lähettämiseen yleiseen kansioon, jossa sähköposti on otettu käyttöön](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder)

- Määritä sähköpostin lokiinkirjauksen käyttäjä kummankin yleisen kansion, *Queue* ja *Storage*, omistajaksi käyttämällä Outlookia tai Exchange-palvelimen hallintaliittymää seuraavan taulukon tietojen perusteella:

  |Ominaisuus        |Arvo                     |
  |----------------|--------------------------|
  |Käyttäjä            |Sen käyttäjätilin sähköposti, jota Business Central käyttää sähköpostin lokiinkirjaustyön suorittamiseen|
  |Käyttöoikeustaso|Omistaja                     |

  Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen yleiseen kansioon](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

- Kahden postityönkulkusäännön luonti seuraavan taulukon tietojen perusteella

  |Tarkoitus  |Name |Ehdot                        |Toiminto                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |Saapuvan sähköpostin sääntö |Lokin sähköposti lähetetty tälle organisaatiolle|*Lähettäjä* sijaitsee *organisaation ulkopuolella* ja *vastaanottaja* sijaitsee *organisaation sisäpuolella*|Piilokopion lähettäminen yleiselle *Queue*-kansiolle määritetylle sähköpostitilille|
  |Lähtevän sähköpostin sääntö | Lokin sähköposti lähetetty tästä organisaatiosta |*Lähettäjä* sijaitsee *organisaation sisäpuolella* ja *vastaanottaja* sijaitsee *organisaation ulkopuolella*|Piilokopion lähettäminen yleiselle *Queue*-kansiolle määritetylle sähköpostitilille|
  
  Lisätietoja on kohdassa [Postityönkulkusääntöjen hallinta Exchange Onlinessa](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) ja [Postityönkulkusäännön toiminnot Exchange Onlinessa](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-action).

> [!NOTE]
> Jos Exchange-palvelimen hallintaliittymään tehdään muutoksia, muutokset tulevat näkyviin Exchangen hallintakeskuksessa viiveen jälkeen. Myös Exchangeen tehdyt muutokset ovat käytettävissä [!INCLUDE[prodshort](prodshort.md)]issa viiveen jälkeen.
