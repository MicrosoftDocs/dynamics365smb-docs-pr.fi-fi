---
title: Liiketoiminnan kontaktien luominen
description: Määrittää tehtävät luomaan kontakteja ja määrittämään liikesuhteet.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 01/05/2021
ms.author: edupont
ms.openlocfilehash: 42645a038c3937644fe90ce895ee454e1d1b5d5c
ms.sourcegitcommit: fe6943d410f5dca4e8b2986f95501009ae982d98
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/05/2021
ms.locfileid: "4827041"
---
# <a name="create-contacts"></a>Kontaktien luominen
Kun luot liiketoiminnan kontaktin johonkuhun toisessa yrityksessä, lisää heidät yhteyshenkilönä [!INCLUDE[prod_short](includes/prod_short.md)]iin. Lisää sitten kontakteista tai kontaktien yrityksestä tietoja, jotka voivat olla hyödyllisiä tulevissa yhteyksissä. **Kontaktin kortti** -sivulla voit luoda seuraavanlaisia kontaktityyppejä:

* **Henkilö** - Yleensä olet ollut suorassa kosketuksessa jonkun kanssa ja sinulla on heidän yhteystietonsa.
* **Yritys** - Esimerkiksi yhteyshenkilö ei ole yksityishenkilö vaan entiteetti, kuten alihankkija tai pankki. 

Kunkin kontaktityypin kannalta merkitykselliset tiedot eroavat toisistaan, joten käytettävissä olevat kentät ja toiminnot ovat erilaisia. Voit esimerkiksi määrittää vastuualueet henkilölle ja toimialaryhmä yritykselle. 

Voit myös muuttaa **Tyyppi**-kentän arvoa myöhemmin. Vaihtoehtoisesti voit käyttää **Kontaktienhallinnan asetukset**-sivun **Periytyvyys**-pikavälilehden kenttiä määrittääksesi jaettavat tiedot henkilön ja yrityksen välillä. Lisätietoja on kohdassa [Kontaktien määrittäminen](marketing-setup-contacts.md).

Kun yhteyshenkilö muunnetaan esimerkiksi asiakkaaksi, yhteyshenkilö tai yhteyshenkilön yrityksestä tulee asiakkaan nimi. Kontaktin tietueet säilytetään, ja voit linkittää kontaktin ja asiakkaan niin, että heidän tietonsa synkronoidaan eteenpäin.

## <a name="to-create-a-contact-manually"></a>Kontaktin luominen manuaalisesti
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yhteyshenkilöt** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Valitse **Nro**-kenttään kontaktin numero.

    Jos olet määrittänyt kontakteille numerosarjan **Kontaktienhallinnan asetukset**-sivulla, voit lisätä seuraavan saatavilla olevan kontaktinumeron **Enter**-näppäimellä.  
5. Täytä jäljellä olevat kentät tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Kontaktin luominen asiakkaana, toimittajana tai pankkitilinä.
Jos sinulla on asiakkaita, toimittajia ja pankkitilejä, joille haluat luoda kontaktikortit, voit luoda kontakteja aiemmin luoduista tiedoista käyttämällä **Luo kontakteja** -erätöinä. Kun luot kontaktin tällä tavalla, kontaktin tiedot synkronoidaan myöhemmin liittyvän asiakkaan, toimittajan tai pankkitilin tietojen kanssa. Lisätietoja on kohdassa [Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

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
> Tämän voi tehdä myös toisin päin eli asiakkaan, toimittajan tai pankkitilin voi kontaktista. Lisätietoja on kohdassa [Kontaktin luominen asiakkaana, toimittajana tai pankkitilinä](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-employee-or-bank-account-from-a-contact"></a>Asiakkaan, toimittajan, työntekijän tai pankkitilin luominen yhteyshenkilöstä
Jos yrityksellä, jolle haluat luoda yhteyshenkilön, on asiakas, toimittaja, työntekijä tai pankkitili, voit käyttää **Luo**-toimintoa. Kun luot kontaktin tällä tavalla, kontaktin tiedot synkronoidaan myöhemmin liittyvän asiakkaan, toimittajan, työntekijän tai pankkitilin tietojen kanssa. Lisätietoja on kohdassa [Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Ennen kontaktien luontia asiakkaiden, toimittajien, työntekijöiden tai pankkitilien liikesuhteen koodi on määritettävä **Kontaktienhallinnan asetukset** -sivun **Vuorovaikutukset**-pikavälilehdessä. Lisätietoja on kohdassa [Kontaktien määrittäminen](marketing-setup-contacts.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yhteyshenkilöt** ja valitse sitten liittyvä linkki.
2. Valitse kontakti, jonka haluat luoda asiakkaana, toimittajana, työntekijänä tai pankkitilinä.
3. Valitse **Luo**-toiminto ja valitse sitten **Asiakas**, **Toimittaja**, **Pankki** tai **Työntekijä**.
4. Valitse **OK**-painike.

Yhteystiedot siirretään kontaktikortista uuteen asiakas-, toimittaja-, työntekijä- tai pankkitilikorttiin. Haluat ehkä lisätä tiettyjä tietoja jokaiseen korttiin, kuten laskutus- ja maksutiedot. Lisätietoja on esimerkiksi kohdassa [Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account"></a>Kontaktin linkittäminen olemassa olevaan asiakkaaseen, toimittajaan, työntekijään tai pankkitiliin
Jos kontakti ja joko asiakas, toimittaja, työntekijä tai pankkitili ovat samassa yrityksessä, voit linkittää nämä kaksi objektia ja synkronoida tiedot.

1. Avaa kontakti, jonka haluat linkittää.
2. Valitse **Linkitä olemassa olevan kanssa** -toiminto ja valitse sitten **Asiakas**-, **Toimittaja**-, **Pankki**- tai **Työntekijä**-toiminto.
3. Valitse avautuvalla sivulla linkitettävä asiakas, toimittaja, työntekijä tai pankkitili.
4. Määritä **Nykyiset pääkentät** -kentässä kentät, jotka priorisoidaan, jos kontaktille, toimittajalle, työntekijälle tai pankkitilille yhteisissä kentissä esiintyy ristiriitaisia tietoja. Jos esimerkiksi myyjän koodi on erilainen kontaktille ja asiakkaalle, voit valita toisen säilyttämisen kontaktikortissa valitsemalla **Kontakti**.
5. Valitse **OK**-painike.

## <a name="to-remove-a-link-between-a-contact-and-an-existing-customer-vendor-employee-or-bank-account"></a>Kontaktin linkin poistaminen olemassa olevasta asiakkaasta, toimittajasta, työntekijästä tai pankkitilistä

Jos olet linkittänyt kontaktin ja asiakkaan, toimittajan, työntekijän tai pankkitilin virheellisesti, poista entiteettien välinen linkki, jotta tietoja ei enää synkronoida.

1. Avaa kontakti, jossa on väärä linkki.  
2. Valitse **Liikesuhteet**-toiminto.  
3. Valitse avautuvalla sivulla asiakas, toimittaja, työntekijä tai pankkitili, josta linkki poistetaan.  
4. Valitse **Poista**-toiminto.  

> [!NOTE]  
> Älä käytä **Liikesuhteet**-ikkunaa aiemmin luotujen suhteiden muuttamiseen. Poista sen sijaan suhde ja käytä **Linkitä olemassa olevan kanssa** -toimintoa. Lisätietoja on [Kontaktin linkittäminen aiemmin luotuun asiakkaaseen, toimittajaan tai pankkitiliin](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account) -osassa.

## <a name="synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts"></a>Kontaktien synkronoiminen asiakkaiden, toimittajien, työntekijöiden ja pankkitilien kanssa
Jos jotkin kontakteistasi ovat myös asiakkaita, toimittajia, työntekijöitä tai pankkitilejä, voit synkronoida ne sitten kontaktin tietojen kanssa ja saada seuraavat edut:

* Sinun tarvitsee päivittää tiedot vain yhteen paikkaan. Jos esimerkiksi muutat kontaktin puhelinnumeroa, puhelinnumero päivitetään automaattisesti asiakkaalle, toimittajalle, työntekijälle tai pankkitilille.
* Jos olet määrittänyt kontakteille numerosarjan, kun luot asiakkaan, myyjän, työntekijän tai pankkitilikortin, kontakti luodaan automaattisesti.
* Voit luoda kontaktista myyntitarjouksia ja -tilauksia sekä ostotarjouksia ja -tilauksia.
* Voit saada tallentaa vuorovaikutuksia, kuten tilausten tai puitetilausten tulostaminen, myynnin huoltotilauksen luominen ja sähköpostin lähettäminen.
* Jos poistat asiakkaaseen, toimittajaan, työntekijään tai pankkitiliin linkitetyn kontaktin, vain kontakti poistuu ohjelmasta. Asiakas, toimittaja, työntekijä tai pankkitili säilytetään.
* Jos poistat asiakkaaseen, toimittajaan, työntekijään tai pankkitiliin linkitetyn kontaktin, vain kontakti säilytetään.

> [!NOTE]  
> Tietyt tiedot, kuten laskutus- ja kirjaustiedot, eivät ole käytettävissä kontakteille. Kun luot kontakteja asiakkaina, toimittajina, työntekijöinä tai pankkitilinä, haluat ehkä lisätä ne manuaalisesti.

Tietojen synkronointi asiakkaiden, toimittajien, työntekijöiden tai pankkitilien välillä voidaan ottaa käyttöön kolmella tavalla:

* Luomalla yhteyshenkilöitä asiakkaista, toimittajista, työntekijöistä tai pankkitileistä. Katso [Kontaktin luominen asiakkaasta, toimittajasta tai pankkitilistä](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Luomalla asiakkaita, toimittajia, työntekijöitä tai pankkitilejä kontakteista. Katso [Asiakkaan, toimittajan tai pankkitilin luominen yhteyshenkilöstä](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Linkittämällä kontakteja aiemmin luotuihin asiakkaisiin, toimittajiin, työntekijöihin tai pankkitileihin kontaktikortista. Katso [Kontaktin linkittäminen olemassa olevaan asiakkaaseen, toimittajaan tai pankkitiliin](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="to-view-which-customer-vendor-employee-or-bank-account-a-contact-is-related-to"></a>Tarkistetaan, mihin asiakkaaseen, toimittajaan, työntekijään tai pankkitiliin yhteyshenkilö liittyy
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yhteyshenkilöt** ja valitse sitten liittyvä linkki.
2. Valitse yhteyshenkilön rivi. Valitse **Liittyvät tiedot** -toiminto ja valitse sitten **Asiakas/toimittaja/pankkitili/työntekijä**-toiminto.

## <a name="see-also"></a>Katso myös
[Kontaktien hallinta](marketing-contacts.md)  
[Kontaktien määrittäminen](marketing-setup-contacts.md)  
[Business Centralin käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]