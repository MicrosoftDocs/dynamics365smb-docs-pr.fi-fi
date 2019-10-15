---
title: Kontaktiyritysten luominen| Microsoft Docs
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f4bf8e694a7b034eb601c3bf39bd420ff61ab73a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309314"
---
# <a name="create-contacts"></a>Kontaktien luominen
Tapaat säännöllisesti muiden yritysten työntekijöitä, jotka voivat kehittyä liikesuhteiksi, kuten asiakassuhteeksi. Kun tällainen uusi kontakti luodaan, kontaktin korttiin on tallennettava mahdollisimman paljon tietoja, jotta yhteydenpitoa voidaan jatkaa.

Voit luoda yhteyshenkilön, jonka tyyppi on esimerkiksi **Yritys**, jos suhde ei ole yksityishenkilö vaan entiteetti, kuten alihankkija tai pankki. Voit myös luoda yhteyshenkilön, jonka tyyppi on **Henkilö.** Toiminto on suunnilleen sama molemmille tyypeille. Niitä voi myös muuttaa suhteiden muuttuessa.

Kun yhteyshenkilökortti muunnetaan esimerkiksi asiakaskortiksi, yhteyshenkilö tai yhteyshenkilön yrityksestä tulee asiakkaan nimi. Yhteyshenkilökortti säilytetään. Näiden kahden kortin tiedot synkronoidaan ja linkitetään toisiinsa.

## <a name="person-or-company"></a>Henkilö tai yritys
Voit päättää määrittää kontaktin henkilönä tai yrityksenä yleensä sen perusteella, tiedätkö yhteyshenkilön nimen kortin luontihetkellä. Se tehdään täyttämällä **Tyyppi**-kenttä **Kontaktin kortti** -sivulla. Voit ylläpitää kontaktin kortteja myös sekä yritykselle että ainakin yhdelle yrityksen työntekijälle. Tämä tehdään automaattisesti, kun täytät **Yrityksen nimi** -kentän **Henkilö**-tyypin kontaktin kortissa.

Molemmissa tyypeissä on samanlaiset toiminnot. Poikkeuksena ovat tyypin mukaan määritettävät lisätietotyyppivaihtoehdot. Voit esimerkiksi määrittää vastuualueet henkilölle ja toimialaryhmä yritykselle. Tämä ilmaistaan käyttöliittymässä himmentämällä kentät ja toiminnot, jotka eivät ole käytettävissä. Voit muuttaa **Tyyppi**-kentän arvoa myöhemmin. Vaihtoehtoisesti voit hallita, mitä tietoja henkilön ja henkilöön liittyvän yrityksen välillä jaetaan, **Kontaktienhallinnan asetukset** -sivun **Periytyminen**-pikavälilehdessä. Lisätietoja on kohdassa [Kontaktien määrittäminen](marketing-setup-contacts.md).

## <a name="to-create-a-contact-manually"></a>Kontaktin luominen manuaalisesti
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kontaktit** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Valitse **Nro**-kenttään kontaktin numero.

    Jos olet määrittänyt kontakteille numerosarjan **Kontaktienhallinnan asetukset**-sivulla, voit lisätä seuraavan saatavilla olevan kontaktinumeron Enter-näppäimellä.  
5. Täytä jäljellä olevat kentät tarvittaessa. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Kontaktin luominen asiakkaana, toimittajana tai pankkitilinä.
Jos sinulla on asiakkaita, toimittajia ja pankkitilejä, joille haluat luoda kontaktikortit, voit luoda kontakteja aiemmin luotujen tietojen perusteella käyttämällä **Luo kontakteja** -erätöinä. Kun luot kontaktin tällä tavalla, kontaktin tiedot synkronoidaan myöhemmin liittyvän asiakkaan, toimittajan tai pankkitilin tietojen kanssa. Lisätietoja on kohdassa [Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Ennen aiemmin luotuihin tietoihin perustuvien kontaktien luontia asiakkaiden, toimittajien tai pankkitilien liikesuhteen koodi on määritettävä **Kontaktienhallinnan asetukset** -sivun **Vuorovaikutukset**-pikavälilehdessä. Lisätietoja on kohdassa [Yhteyshenkilöiden määrittäminen](marketing-setup-contacts.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna jokin seuraavista sen perusteella, mistä haluat luoda kontakteja, ja valitse liittyvä linkki.
   * **Luo kontakteja asiakkaista**
   * **Luo kontakteja toimittajista**
   * **Luo kontakteja pankkitileistä**
2. Valitse avautuvalla pyyntösivulla **Asiakas**-, **Toimittaja**- tai **Pankkitili**-osa ja määritä suodattimet, jos haluat luoda kontakteja tietyistä asiakkaista, toimittajista tai pankkitileistä.
3. Aloita yhteystietojen luominen valitsemalla **OK**.

Ohjelma liittää uusiin kontakteihin seuraavat kontaktinumerot numerosarjasta. Uusiin kontakteihin liitetään **Kontaktienhallinnan asetukset** -sivulla määritetty liikesuhde.

> [!TIP]  
> Tämän voi tehdä myös toisin päin eli asiakkaan, toimittajan tai pankkitilin voi kontaktista. Lisätietoja on kohdassa [Kontaktin luominen asiakkaana, toimittajana tai pankkitilinä](marketing-create-contact-companies.md#to-create-a-customer-vendor-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-or-bank-account-from-a-contact"></a>Asiakkaan, toimittajan tai pankkitilin luominen yhteyshenkilöstä
Jos yrityksellä, jolle haluat luoda yhteyshenkilön, on asiakas, toimittaja tai pankkitili, voit käyttää **Luo**-toimintoa. Kun luot kontaktin tällä tavalla, kontaktin tiedot synkronoidaan myöhemmin liittyvän asiakkaan, toimittajan tai pankkitilin tietojen kanssa. Lisätietoja on kohdassa [Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Ennen kontaktien luontia asiakkaiden, toimittajien tai pankkitilien luontia on määritettävä liikesuhteen koodi **Kontaktienhallinnan asetukset** -sivun **Vuorovaikutukset**-pikavälilehdessä. Lisätietoja on kohdassa [Kontaktien määrittäminen](marketing-setup-contacts.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Kontaktit** ja valitse sitten liittyvä linkki.
2. Valitse kontakti, jonka haluat luoda asiakkaana, toimittajana tai pankkitilinä.
3. Valitse **Luo**-toiminto ja valitse sitten **Asiakas**, **Toimittaja** tai **Pankki**.
4. Valitse **OK**-painike.

Yhteystiedot siirretään kontaktikortista uuteen asiakas-, toimittaja- tai pankkitilikorttiin. Haluat ehkä lisätä tiettyjä tietoja jokaiseen korttiin, kuten laskutus- ja maksutiedot. Lisätietoja on esimerkiksi kohdassa [Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Kontaktin linkittäminen olemassa olevaan asiakkaaseen, toimittajaan tai pankkitiliin
Jos kontakti ja joko asiakas, toimittaja tai pankkitili ovat samassa yrityksessä, voit linkittää nämä kaksi objektia siten, että yhteiset tiedot synkronoidaan.

1. Avaa kontakti, jonka haluat linkittää.
2. Valitse **Linkitä olemassa olevan kanssa** -toiminto ja valitse sitten **Asiakas**, **Toimittaja** tai **Pankki**.
3. Valitse avautuvalla sivulla linkitettävä asiakas, toimittaja tai pankkitili.
4. Määritä **Nykyiset pääkentät** -kentässä kentät, jotka priorisoidaan, jos kontaktille, toimittajalle tai tilille yhteisissä kentissä esiintyy ristiriitaisia tietoja. Jos esimerkiksi myyjän koodi on erilainen kontakti- ja asiakaskortissa, voit valita toisen säilyttämisen kontaktikortissa valitsemalla **Kontakti**.
5. Valitse **OK**-painike.

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa
Jos jotkin kontakteistasi ovat myös asiakkaita, toimittajia tai pankkitilejä, voit synkronisoida kontaktin tiedot liittyvän asiakkaan, toimittajan tai pankkitilin kanssa.

Kontaktin synkronoinnista asiakkaan, toimittajan tai pankkitilin kanssa on seuraavat edut.

* Sinun tarvitsee päivittää tiedot vain yhteen paikkaan. Jos esimerkiksi muutat kontaktin puhelinnumeroa, puhelinnumeroon päivitetään automaattisesti sama muutos kuin asiakkaalle, toimittajalle tai pankkitilille.
* Jos olet määrittänyt numerosarjan kontakteille, kun luot asiakas-, toimittaja- tai pankkitilikortin, ohjelma luo automaattisesti kontaktikortin asiakkaalle, toimittajalle tai pankkitilille.
* Voit luoda kontaktista myyntitarjouksia ja -tilauksia sekä ostotarjouksia ja -tilauksia.
* Voit saada ohjelman tallentamaan vuorovaikutuksia, kun teet erilaisia toimenpiteitä (kuten tilausten tai puitetilausten tulostaminen, myynnin huoltotilauksen luominen ja sähköpostin lähettäminen).
* Jos poistat asiakkaaseen, toimittajaan ja/tai pankkitiliin linkitetyn kontaktin, vain kontakti poistetaan. Asiakas, toimittaja tai pankkitili säilytetään.
* Jos poistat asiakkaaseen, toimittajaan tai pankkitiliin linkitetyn kontaktin, vain kontakti säilytetään.

> [!NOTE]  
> Tietyt tiedot, kuten laskutus- ja kirjaustiedot, eivät näy kontaktikortissa. Tämän vuoksi ne halutaan ehkä lisätä manuaalisesti asiakaskortille, toimittajakortille tai pankkitilikortille, kun kontakteja luodaan asiakkaina, toimittajina tai pankkitileinä.

Yleisten tietojen synkronointi liittyvien asiakkaiden, toimittajien tai pankkitilien välillä voidaan ottaa käyttöön kolmella tavalla:

* Luomalla yhteyshenkilöitä asiakkaista, toimittajista tai pankkitileistä. Katso [Kontaktin luominen asiakkaasta, toimittajasta tai pankkitilistä](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Luomalla asiakkaita, toimittajia tai pankkitilejä kontakteista. Katso [Asiakkaan, toimittajan tai pankkitilin luominen yhteyshenkilöstä](marketing-create-contact-companies.md#to-create-a-customer-vendor-or-bank-account-from-a-contact).
* Linkittämällä kontakteja aiemmin luotuihin asiakkaisiin, toimittajiin tai pankkitileihin kontaktikortista. Katso [Kontaktin linkittäminen olemassa olevaan asiakkaaseen, toimittajaan tai pankkitiliin](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-or-bank-account).

## <a name="to-view-which-customer-vendor-or-bank-account-a-contact-is-related-to"></a>Tarkistetaan, mihin asiakkaaseen, toimittajaan tai pankkitiliin yhteyshenkilö liittyy
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kontaktit** ja valitse sitten liittyvä linkki.
2. Valitse yhteyshenkilön rivi. Valitse **Liittyvät tiedot** -toiminto ja valitse sitten **Asiakas/toimittaja/pankkitili**-toiminto.

Liittyvän kortin sivu avautuu.

## <a name="see-also"></a>Katso myös
[Kontaktien hallinta](marketing-contacts.md)  
[Kontaktien määrittäminen](marketing-setup-contacts.md)  
[Business Centralin käyttäminen](ui-work-product.md)
