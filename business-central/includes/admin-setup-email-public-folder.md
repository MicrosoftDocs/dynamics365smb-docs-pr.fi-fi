---
author: brentholtorf
ms.topic: include
ms.date: 02/15/2022
ms.author: bholtorf
---

> [!NOTE]
> Seuraavissa osissa oletetaan, että sinulla on Exchange Online -järjestelmänvalvojan oikeudet.

Ennen sähköpostin lokiinkirjauksen määrittämistä Office 365:een on valmisteltava [yleiset kansiot](/exchange/collaboration-exo/public-folders/public-folders). Se voidaan tehdä [Exchangen hallintakeskuksessa](/exchange/exchange-admin-center?preserve-view=true) tai käyttämällä [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&?preserve-view=true) -liittymää.

> [!TIP]
> Jos haluat käyttää [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true) -liittymää, [BCTech-säilöön](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging) on julkaistu mallikomentosarja, joka voi toimia mallina komentosarjan määrittämisessä.

Määritä Exchange Online seuraavien vaiheiden avulla ja linkit, joiden avulla saat lisätietoja.

### <a name="create-an-admin-role-group"></a>Järjestelmänvalvojan rooliryhmän luominen

Yleisten kansioiden järjestelmänvalvojan rooliryhmän luonti seuraavan taulukon tietojen perusteella:

|Ominaisuus        |Arvo                     |
|----------------|--------------------------|
|Name            |Yleisten kansioiden hallinta |
|Valitut roolit  |Yleiset kansiot            |
|Valitut käyttäjät  |Sen käyttäjätilin sähköposti, jota Business Central käyttää sähköpostin lokiinkirjaustyön suorittamiseen|

Lisätietoja on kohdassa [Rooliryhmien hallinta Exchange Onlinessa](/exchange/permissions-exo/role-groups).

### <a name="create-a-new-public-folder-mailbox"></a>Uuden yleisen kansion postilaatikon luominen

Uuden yleisen kansioin postilaatikon luonti seuraavan taulukon tietojen perusteella:

|Ominaisuus        |Arvo                     |
|----------------|--------------------------|
|Name            |Julkinen postilaatikko            |

Lisätietoja on kohdassa [Yleisen kansion postilaatikon luonti](/exchange/collaboration-exo/public-folders/create-public-folder-mailbox).

### <a name="create-new-public-folders"></a>Uusien yleisten kansioiden luominen

1. Luo juuritasolle uusi yleinen kansio, jonka nimi on **Email Logging**, jolloin kansion täydellinen polku on `\Email Logging\`.
2. Luo kaksi alikansiota, jolloin kansioiden täydelliseksi poluksi tulee

    - `\Email Logging\Queue\`
    - `\Email Logging\Storage\`

Lisätietoja on kohdassa [Yleisen kansion luonti](/exchange/collaboration-exo/public-folders/create-public-folder).

### <a name="set-public-folder-ownership"></a>Yleisen kansion omistajuuden määrittäminen

Määritä sähköpostin kirjaamisen käyttäjä molempien yleisten kansioiden,*Jono* ja *Tallennustila*, omistajaksi.

Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen yleiseen kansioon](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

### <a name="mail-enable-the-queue-public-folder"></a>Sähköpostin käyttöönotto yleisessä *Queue*-kansiossa

  Lisätietoja on kohdassa [Sähköpostin käyttöönotto tai käytöstäpoistaminen yleisessä kansiossa](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder).

### <a name="mail-enable-sending-emails-to-the-queue-public-folder"></a>Sähköpostin ottaminen käyttöön sähköpostien lähettämiseksi julkiseen *Jono*-kansioon

Sähköpostin käyttöönoton sähköpostien lähettämiseen yleiseen *Queue*-kansioon käyttämällä Outlookia tai Exchange-palvelimen hallintaliittymää.

Lisätietoja on kohdassa [Luvan antaminen anonyymeille käyttäjille sähköpostin lähettämiseen yleiseen kansioon, jossa sähköposti on otettu käyttöön](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?preserve-view=true).

### <a name="create-mail-flow-rules"></a>Sähköpostin työnkulkusääntöjen luominen

Kahden postityönkulkusäännön luonti seuraavan taulukon tietojen perusteella:

|Tarkoitus  |Name |Käytä tätä sääntöä, jos...             |Tee seuraavat toiminnot...                          |
|---------|-----|----------------------------------|---------------------------------------------|
|Saapuvan sähköpostin sääntö |Lokin sähköposti lähetetty tälle organisaatiolle|*Lähettäjä* sijaitsee *organisaation ulkopuolella* ja *vastaanottaja* sijaitsee *organisaation sisäpuolella*|Piilokopion lähettäminen yleiselle *Queue*-kansiolle määritetylle sähköpostitilille|
|Lähtevän sähköpostin sääntö | Lokin sähköposti lähetetty tästä organisaatiosta |*Lähettäjä* sijaitsee *organisaation sisäpuolella* ja *vastaanottaja* sijaitsee *organisaation ulkopuolella*|Piilokopion lähettäminen yleiselle *Queue*-kansiolle määritetylle sähköpostitilille|

Lisätietoja on kohdassa [Postityönkulkusääntöjen hallinta Exchange Onlinessa](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) ja [Postityönkulkusäännön toiminnot Exchange Onlinessa](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

> [!NOTE]
> Jos Exchange-palvelimen hallintaliittymään tehdään muutoksia, muutokset tulevat näkyviin Exchangen hallintakeskuksessa viiveen jälkeen. Myös Exchangeen tehdyt muutokset ovat käytettävissä [!INCLUDE[prod_short](prod_short.md)]issa viiveen jälkeen. Viive voi olla useita tunteja.
