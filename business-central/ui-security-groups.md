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

# Business Centralin käyttöoikeuden hallinta suojausryhmien avulla

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

Suojausryhmien avulla järjestelmänvalvojat voivat hallita käyttöoikeuksia Dynamics 365 -sovelluksissa, kuten SharePoint Online, CRM Online ja [!INCLUDE [prod_short](includes/prod_short.md)] -verkkoversio. Järjestelmänvalvojat lisäävät suojausryhmiin käyttöoikeuksia ja lisätessään käyttäjiä ryhmään käyttöoikeudet koskevat kaikkia jäseniä. Järjestelmänvalvoja voi esimerkiksi luoda suojausryhmän, joka antaa myyjille mahdollisuuden luoda ja kirjata myyntitilauksia. Voit myös antaa ostajien tehdä saman ostotilauksille.

Luo suojausryhmät Microsoft 365 hallintakeskuksessa tai Azure Active Directoryssa. Tässä artikkelissa kuvataan Microsoft 365 -hallintakeskuksen vaiheet , mutta vaiheet ovat samanlaiset molemmissa.

## Suojausryhmän lisääminen Microsoft 365 -hallintakeskukseen

1. Siirry Microsoft 365 -hallintakeskuksen **Aktiiviset tiimit ja ryhmät** -sivulle.
2. Valitse **Lisää ryhmä**.
3. Valitse ryhmän **suojaus**tyyppi ja valitse sitten **Seuraava**.
4. Ryhmän perusteiden määrittäminen.
5. Valinnainen: voit määrittää ryhmän jäsenet roolienmäärityskäyttöön. Jos haluat lisätietoja määrityksistä, valitse [Roolimääritysten hallinta Azure AD -ryhmien avulla](/azure/active-directory/roles/groups-concept).
6. Avaa ryhmä ja lisää sitten henkilöt ryhmään **Lisää jäseniä** -välilehden avulla.

## Suojausryhmän lisääminen Business Centralissa

Luo suojausryhmä kohteessa [!INCLUDE [prod_short](includes/prod_short.md)] ja linkitä se sitten Microsoft 365 -hallintakeskuksen suojausryhmään. Uusi ryhmä sisältää Microsoft 365 -hallintakeskuksessa lisäämäsi jäsenet.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Suojausryhmät** ja valitse sitten vastaava linkki.
2. Luo uusi ryhmä valitsemalla **Uusi**.
3. Kirjoita **Nimi**-kenttään ryhmän nimi.
4. Kirjoita suojausryhmän nimi täsmälleen sellaisena kuin se näkyy Microsoft 365 -hallintakeskuksessa **AAD-suojausryhmän nimi** -kenttään. [!INCLUDE [prod_short](includes/prod_short.md)] etsii kyseisen ryhmän ja linkittää sen tähän ryhmään.

> [!NOTE]
> Käyttäjät näkyvät **Jäsenet**-kortissa tietoruudussa tai **Suojausryhmän jäsenet** -sivulla vain, jos heidät on lisätty kohteen [!INCLUDE [prod_short](includes/prod_short.md)] käyttäjiksi. Lisätietoja käyttäjien lisäämisestä on kohdassa [Käyttäjien lisääminen tai käyttäjätietojen ja käyttöoikeuksien delegoinnin päivittäminen Business Centralissa](ui-how-users-permissions.md#adduser).  

### Määritä ryhmän käyttöoikeudet

1. Valitse ryhmä **Suojausryhmät** -sivulla ja valitse sitten **Käyttöoikeudet** -toiminto.
1. Määritä käyttöoikeudet seuraavilla tavoilla:
    * Voit määrittää käyttöoikeuksien joukkoja erikseen valitsemalla **Käyttöoikeuksien joukko** -kentässä määritettävät käyttöoikeudet.
    * Voit määrittää useampia käyttöoikeusjoukkoja valitsemalla **Valitse käyttöoikeuksien joukot** -toiminnon ja valitsemalla sitten määritettävät joukot.

## Tarkastele käyttöoikeusryhmän oikeuksia

**Suojausryhmät** -sivulla tietoruudussa näkyvät ryhmälle määritetyt **käyttöoikeuksien joukot**. Jokaisella **Jäsenet**-kortissa olevalla käyttäjällä on kyseiset käyttöoikeudet. **Käyttöoikeuksien joukko suojausryhmän mukaan** -toiminnon avulla määritetty käyttöoikeus määrittää yksityiskohtaisen näkymän. Siellä voit myös tutkia kunkin suojausryhmän yksilöllisiä käyttöoikeuksia.

Käyttöoikeudet ovat käytettävissä myös **Käyttäjät**-sivulla. Tietoruudussa näkyvät valitulle käyttäjälle **Käyttöoikeuksien joukot suojausryhmistä**- ja **Suojausryhmän jäsenyydet** -kortit.

## Suojausryhmät ja käyttäjäryhmät

Jos sinulla on käyttäjäryhmiä, voit muuntaa ryhmät vuokralaisen käyttöoikeusjoukoksi käyttämällä **Käyttäjäryhmän siirto** -asetusten ohjattua määritystä. Voit käynnistää oppaan **Ominaisuuksien hallinta** -sivulla, etsi **Ominaisuus: Muunna käyttäjäryhmän käyttöoikeudet** ja valitse sitten **Kaikki käyttäjät** **Käytössä:** -kentässä. Asetusten ohjattu määritys sisältää seuraavat muunnosvaihtoehdot.

|Asetus  |Kuvaus  |
|---------|---------|
|Määritä käyttäjälle     | Määritä käyttäjäryhmien käyttöoikeudet suoraan ryhmään liitetyille käyttäjille ja poista niiden käyttäjäryhmämääritykset.        |
|Muunna käyttöoikeuksien joukoksi     | Luo uusi käyttöoikeus kunkin käyttäjäryhmän käyttöoikeuksia varten. Uusi käyttöoikeusjoukko määritetään kaikkien käyttäjäryhmien kaikille jäsenille.          |

## Katso myös

[Luo käyttäjät käyttöoikeuksien mukaan](ui-how-users-permissions.md)  
[Business Centralin käytön määrittäminen Teamsissa Microsoft 365 -käyttöoikeuksilla](admin-access-with-m365-license-setup.md)  
[Tutustu ryhmiin ja käyttöoikeuksiin Azure Active Directoryssa](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Active Directory -suojausryhmät](/windows-server/identity/ad-ds/manage/understand-security-groups)  