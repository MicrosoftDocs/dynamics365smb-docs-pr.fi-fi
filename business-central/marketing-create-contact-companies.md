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
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: aaeb98aa5e3c48a92be71546be33b1494a751cb9
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795058"
---
# <a name="creating-contacts"></a>Kontaktien luominen
Yrityksen työntekijät tapaavat säännöllisesti mahdollisia asiakasyrityksiä, ja tapaamiset johtavat usein liikesuhteisiin. Kun uusi kontakti luodaan, nämä tiedot on tallennettava yhteydenpidon jatkamista varten.

Tehokkaan yhteydenpidon varmistamiseksi yrityksestä on määritettävä mahdollisimman paljon tietoja. Kun yritys liitetään esimerkiksi sopivaan toimialaryhmään, nämä yritykset sisällytetään kaikkeen soveltuvaan yhteydenpitoon. Voit määrittää myös liikesuhteen, joka kontaktiin on muodostettu. Kontakti voi olla esimerkiksi prospekti, pankki tai alihankkija.

> [!NOTE]
> Voit määrittää **Kontaktin kortti** -sivun **Tyyppi**-kentässä kontaktiksi henkilön tai yrityksen yleensä sen perusteella, tiedätkö yhteyshenkilön nimen kortin luontihetkellä. Molemmissa tyypeissä on samanlaiset toiminnot. Poikkeuksena ovat mahdollisesti määritettävät lisätietotyypit. Voit muuttaa kentän arvoa myöhemmin. Vaihtoehtoisesti voit hallita, mitä tietoja henkilön ja liittyvän yrityksen välillä jaetaan, **Kontaktienhallinnan asetukset** -sivun **Periytyminen**-pikavälilehdessä.

Voit luoda kontaktin jokaiselle uudelle henkilölle tai yritykselle (esimerkiksi asiakkaalle, toimittajalle, mahdolliselle asiakkaalle, pankille, lakiasiantoimistolle ja konsultille), jonka kanssa yrityksesi on vuorovaikutuksessa.

Kontaktin voi luoda kahdella tavalla:
 * Manuaalisesti.
 * Aiemmin luodusta asiakkaasta, toimittajasta tai pankkitilistä.

## <a name="to-create-a-contact-manually"></a>Kontaktin luominen manuaalisesti
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kontaktit** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Valitse **Nro**-kenttään kontaktin numero.

    Jos olet määrittänyt kontakteille numerosarjan **Kontaktienhallinnan asetukset**-sivulla, voit lisätä seuraavan saatavilla olevan kontaktinumeron Enter-näppäimellä.  
5. Täytä jäljellä olevat kentät tarvittaessa. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Kontaktin luominen asiakkaana, toimittajana tai pankkitilinä.
Jos sinulla on asiakkaita, toimittajia ja pankkitilejä, joille haluat luoda kontaktikortit, voit luoda kontakteja aiemmin luotujen tietojen perusteella käyttämällä **Luo kontakteja** -erätöinä. Kun luot kontaktin tällä tavalla, kontaktin tiedot synkronoidaan myöhemmin liittyvän asiakkaan, toimittajan tai pankkitilin tietojen kanssa. Lisätietoja on kohdassa [Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Ennen aiemmin luotuihin tietoihin perustuvien kontaktien luontia asiakkaiden, toimittajien tai pankkitilien liikesuhteen koodi on määritettävä **Kontaktienhallinnan asetukset** -sivun **Vuorovaikutukset**-pikavälilehdessä. Lisätietoja on kohdassa [Kontaktien määrittäminen](marketing-setup-contacts.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna jokin seuraavista sen perusteella, mistä haluat luoda kontakteja, ja valitse liittyvä linkki.
   * **Luo kontakteja asiakkaista**
   * **Luo kontakteja toimittajista**
   * **Luo kontakteja pankkitileistä**
2. Valitse avautuvalla pyyntösivulla **Asiakas**-, **Toimittaja**- tai **Pankkitili**-osa ja määritä suodattimet, jos haluat luoda kontakteja tietyistä asiakkaista, toimittajista tai pankkitileistä.
3. Aloita yhteystietojen luominen valitsemalla **OK**.

Ohjelma liittää uusiin kontakteihin seuraavat kontaktinumerot numerosarjasta. Uusiin kontakteihin liitetään **Kontaktienhallinnan asetukset** -sivulla määritetty liikesuhde.

> [!TIP]  
> Tämän voi tehdä myös toisin päin eli asiakkaan, toimittajan tai pankkitilin voi kontaktista. Lisätietoja on kohdassa [Kontaktin luominen asiakkaana, toimittajana tai pankkitilinä](marketing-create-contact-companies.md#to-create-a-contact-as-a-customer-vendor-or-bank-account).

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

* Linkittämällä kontakteja aiemmin luotuihin asiakkaisiin, toimittajiin tai pankkitileihin kontaktikortista. Katso [Kontaktin linkittäminen olemassa olevaan asiakkaaseen, toimittajaan tai pankkitiliin](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-or-bank-account).
* Luomalla asiakkaita, toimittajia tai pankkitilejä kontakteista. Katso [Kontaktin luominen asiakkaasta, toimittajasta tai pankkitilistä](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Luomalla kontakteja asiakkaina, toimittajina tai pankkitileinä. Katso [Kontaktin luominen asiakkaana, toimittajana tai pankkitilinä](marketing-create-contact-companies.md#to-create-a-contact-as-a-customer-vendor-or-bank-account).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Kontaktin linkittäminen olemassa olevaan asiakkaaseen, toimittajaan tai pankkitiliin
Jos kontakti ja joko asiakas, toimittaja tai pankkitili ovat samassa yrityksessä, voit linkittää nämä kaksi objektia siten, että yhteiset tiedot synkronoidaan.

1. Avaa kontakti, jonka haluat linkittää.
2. Valitse **Linkitä olemassa olevan kanssa** -toiminto ja valitse sitten **Asiakas**, **Toimittaja** tai **Pankki**.
3. Valitse avautuvalla sivulla linkitettävä asiakas, toimittaja tai pankkitili.
4. Määritä **Nykyiset pääkentät** -kentässä kentät, jotka priorisoidaan, jos kontaktille, toimittajalle tai tilille yhteisissä kentissä esiintyy ristiriitaisia tietoja. Jos esimerkiksi myyjän koodi on erilainen kontakti- ja asiakaskortissa, voit valita toisen säilyttämisen kontaktikortissa valitsemalla **Kontakti**.
5. Valitse **OK**-painike.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Kontaktin luominen asiakkaana, toimittajana tai pankkitilinä.
Jos yrityksellä, jolle haluat luoda kontaktin, on asiakas, toimittaja tai pankkitili, voit käyttää **Luo**-toimintoa. Kun luot kontaktin tällä tavalla, kontaktin tiedot synkronoidaan myöhemmin liittyvän asiakkaan, toimittajan tai pankkitilin tietojen kanssa. Lisätietoja on kohdassa [Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Ennen kontaktien luontia asiakkaiden, toimittajien tai pankkitilien luontia on määritettävä liikesuhteen koodi **Kontaktienhallinnan asetukset** -sivun **Vuorovaikutukset**-pikavälilehdessä. Lisätietoja on kohdassa [Kontaktien määrittäminen](marketing-setup-contacts.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Kontaktit** ja valitse sitten liittyvä linkki.
2. Valitse kontakti, jonka haluat luoda asiakkaana, toimittajana tai pankkitilinä.
3. Valitse **Luo**-toiminto ja valitse sitten **Asiakas**, **Toimittaja** tai **Pankki**.
4. Valitse **OK**-painike.

Yhteystiedot siirretään kontaktikortista uuteen asiakas-, toimittaja- tai pankkitilikorttiin. Haluat ehkä lisätä tiettyjä tietoja jokaiseen korttiin, kuten laskutus- ja maksutiedot. Lisätietoja on esimerkiksi kohdassa [Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md).

## <a name="see-also"></a>Katso myös
[Kontaktien hallinta](marketing-contacts.md)  
[Kontaktien määrittäminen](marketing-setup-contacts.md)  
[Business Centralin käyttäminen](ui-work-product.md)
