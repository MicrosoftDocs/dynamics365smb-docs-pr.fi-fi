---
title: Käyttöoikeuden hallinta suojausryhmien avulla
description: 'Tässä artikkelissa kuvataan, miten käyttöoikeuksia määritetään suojausryhmien avulla.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# <a name="control-access-to-business-central-using-security-groups" />Business Centralin käyttöoikeuden hallinta suojausryhmien avulla

Suojausryhmien avulla järjestelmänvalvojien on helpompi hallita käyttöoikeuksia. Esimerkiksi [!INCLUDE [prod_short](includes/prod_short.md)] onlinessa ne ovat uudelleenkäytettäviä Dynamics 365-sovelluksiin, kuten SharePoint Online, CRM Online, ja [!INCLUDE [prod_short](includes/prod_short.md)]. Järjestelmänvalvojat lisäävät [!INCLUDE [prod_short](includes/prod_short.md)]-suojausryhmiin käyttöoikeuksia ja lisätessään käyttäjiä ryhmään käyttöoikeudet koskevat kaikkia jäseniä. Järjestelmänvalvoja voi esimerkiksi luoda [!INCLUDE [prod_short](includes/prod_short.md)]-suojausryhmän, joka antaa myyjille mahdollisuuden luoda ja kirjata myyntitilauksia. Voit myös antaa ostajien tehdä saman ostotilauksille.

## <a name="business-central-online-and-on-premises" />Business Central Online- ja paikalliset versiot

Voit käyttää suojausryhmiä [!INCLUDE [prod_short](includes/prod_short.md)]-ohjelman online-ja paikallinen-versioissa. Luo versiostasi riippuen ryhmiä jollakin seuraavista tavoista:

* Käytä verkkoversiossa Azure Active Directory -suojausryhmiä. Saat lisätietoja ryhmän luomisesta valitsemalla [Suojausryhmän luominen, muokkaaminen tai poistaminen Microsoft 365 -hallintakeskuksessa](/microsoft-365/admin/email/create-edit-or-delete-a-security-group).
* Käytä paikallisesti Windows Active Directory -ryhmiä. Saat lisätietoja siirtymällä kohtaan [Luo ryhmätili Active Directoryssä](/windows/security/operating-system-security/network-security/windows-firewall/create-a-group-account-in-active-directory).

Luo sen jälkeen vastaava suojausryhmä [!INCLUDE [prod_short](includes/prod_short.md)]-ohjelmassa ja yhdistä se sitten luotuun ryhmään. Saat lisätietoja siirtymällä [Lisää suojausryhmä Business Centralissa](#add-a-security-group-in-business-central) -kohtaan.

> [!NOTE]
> Jos olet määrittänyt erityisen käyttäjätyypin, jolla on Windows-ryhmän käyttöoikeustyyppi, [!INCLUDE [prod_short](includes/prod_short.md)]-ohjelman paikallisessa versiossa, joka on aiempi kuin vuoden 2023 julkaisuaalto 1:n versio, kun päivität [!INCLUDE [prod_short](includes/prod_short.md)]-ohjelman käyttäjän suojausryhmäksi. Uudella suojausryhmällä on sama nimi kuin Windows-ryhmällä. Suojausryhmä antaa paremman yleiskuvan ryhmän jäsenistä ja niiden käytössä olevista käyttöoikeuksista.

## <a name="add-a-security-group-in-business-central" />Suojausryhmän lisääminen Business Centralissa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Suojausryhmät** ja valitse sitten vastaava linkki.
1. Luo uusi ryhmä valitsemalla **Uusi**.
1. Luo linkki ryhmään seuraavasti:

    * Jos kyseessä on [!INCLUDE [prod_short](includes/prod_short.md)] online, valitse ryhmä **AAD-turvaryhmän nimi** -kentässä.
    * Jos kyseessä on paikallinen [!INCLUDE [prod_short](includes/prod_short.md)], valitse ryhmä **Windows-ryhmän nimi** -kentässä.

> [!NOTE]
> Käyttäjät näkyvät **Jäsenet**-kortissa tietoruudussa tai **Suojausryhmän jäsenet** -sivulla vain, jos heidät on lisätty kohteen [!INCLUDE [prod_short](includes/prod_short.md)] käyttäjiksi. Lisätietoja käyttäjien lisäämisestä on kohdassa [Käyttäjien lisääminen tai käyttäjätietojen ja käyttöoikeuksien delegoinnin päivittäminen Business Centralissa](ui-how-users-permissions.md#adduser).  

### <a name="assign-permissions-to-a-security-group" />Käyttöoikeuksien määrittäminen suojausryhmälle

1. Valitse ryhmä **Suojausryhmät** -sivulla ja valitse sitten **Käyttöoikeudet** -toiminto.
1. Määritä käyttöoikeudet seuraavilla tavoilla:

    * Voit määrittää käyttöoikeuksien joukkoja erikseen valitsemalla **Käyttöoikeuksien joukko** -kentässä määritettävät käyttöoikeudet.
    * Voit määrittää useampia käyttöoikeusjoukkoja valitsemalla **Valitse käyttöoikeuksien joukot** -toiminnon ja valitsemalla sitten määritettävät joukot.

## <a name="review-the-permissions-in-a-security-group" />Tarkastele käyttöoikeusryhmän oikeuksia

**Suojausryhmät** -sivulla tietoruudussa näkyvät ryhmälle määritetyt **käyttöoikeuksien joukot**. Jokaisella **Jäsenet**-kortissa olevalla käyttäjällä on kyseiset käyttöoikeudet. **Käyttöoikeuksien joukko suojausryhmän mukaan** -toiminnon avulla määritetty käyttöoikeus määrittää yksityiskohtaisen näkymän. Siellä voit myös tutkia kunkin suojausryhmän yksilöllisiä käyttöoikeuksia.

Käyttöoikeudet ovat käytettävissä myös **Käyttäjät**-sivulla. Tietoruudussa näkyvät valitulle käyttäjälle **Käyttöoikeuksien joukot suojausryhmistä**- ja **Suojausryhmän jäsenyydet** -kortit.

## <a name="security-groups-and-user-groups" />Suojausryhmät ja käyttäjäryhmät

> [!NOTE]
> Käyttäjäryhmät eivät enää ole saatavilla tulevassa versiossa.

Suojausryhmät muistuttavat hyvin paljon tällä hetkellä saatavilla olevia käyttäjäryhmiä. Käyttäjäryhmät ovat kuitenkin merkityksellisiä vain [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmille. Suojausryhmät perustuvat Azure Active Directoryn tai Windows Active Directoryn ryhmiin sen mukaan, onko käytössä [!INCLUDE [prod_short](includes/prod_short.md)] online vai paikallinen. Ryhmistä on hyötyä ylläpitäjille, koska he voivat käyttää niitä muiden Dynamics 365 -sovellusten kanssa. Jos esimerkiksi myyjät käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa ja SharePointia, järjestelmänvalvojien ei tarvitse luoda ryhmää ja sen jäseniä uudelleen.

### <a name="optional-convert-user-groups-to-permission-sets" />Valinnainen: Muunna käyttöoikeuksien joukot käyttäjäryhmille

Vuoden 2023 julkaisuaalto 1:ssä ja uudemmissa versioissa käyttäjäryhmät voidaan muuntaa käyttöoikeusjoukkona vuokralaiselle. Käyttöoikeus joukot tarjoavat samat toiminnot kuin käyttäjäryhmät. Seuraavassa on muutamia esimerkkejä:

* **Käyttäjät**-tietoruudun avulla voit hallita käyttäjien käyttöoikeuksia.
* Voit porautua käyttöoikeusjoukon nimeen ja lisätä muita käyttöoikeusjoukkoja joukkoon, jota käsittelet. Lue lisätietoja kohdassa [Muiden käyttöoikeuksien joukkojen lisääminen](ui-define-granular-permissions.md#to-add-other-permission-sets).

Muunna ryhmät **Käyttäjäryhmien siirto** -avusteisen asennusoppaan avulla. Voit käynnistää oppaan **Ominaisuuksien hallinta** -sivulla, etsi **Ominaisuus: Muunna käyttäjäryhmän käyttöoikeudet** ja valitse sitten **Kaikki käyttäjät** **Käytössä:** -kentässä. Asetusten ohjattu määritys sisältää seuraavat muunnosvaihtoehdot.

|Asetus  |Kuvaus  |
|---------|---------|
|Määritä käyttäjälle     | Määritä käyttäjäryhmien käyttöoikeudet suoraan ryhmään liitetyille käyttäjille ja poista niiden käyttäjäryhmämääritykset.        |
|Muunna käyttöoikeuksien joukoksi     | Luo uusi käyttöoikeus kunkin käyttäjäryhmän käyttöoikeuksia varten. Uusi käyttöoikeusjoukko määritetään kaikkien käyttäjäryhmien kaikille jäsenille.          |

## <a name="see-also" />Katso myös

[Luo käyttäjät käyttöoikeuksien mukaan](ui-how-users-permissions.md)  
[Business Centralin käytön määrittäminen Teamsissa Microsoft 365 -käyttöoikeuksilla](admin-access-with-m365-license-setup.md)  
[Tutustu ryhmiin ja käyttöoikeuksiin Azure Active Directoryssa](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Active Directory -suojausryhmät](/windows-server/identity/ad-ds/manage/understand-security-groups)  
