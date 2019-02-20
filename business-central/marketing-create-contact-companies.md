---
title: Kontaktiyritysten luominen| Microsoft Docs
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 9699fc2194befcbca0610bb44d2a86d16d183cc6
ms.contentlocale: fi-fi
ms.lasthandoff: 12/11/2018

---
# <a name="creating-contact-companies"></a>Kontaktiyrityksen luominen
Yrityksen työntekijät tapaavat säännöllisesti mahdollisia asiakasyrityksiä, ja tapaamiset johtavat usein liikesuhteisiin. Kun uusi kontakti luodaan, nämä tiedot on tallennettava yhteydenpidon jatkamista varten.

Tehokkaan yhteydenpidon varmistamiseksi yrityksestä on määritettävä mahdollisimman paljon tietoja. Kun yritys liitetään esimerkiksi sopivaan toimialaryhmään, nämä yritykset sisällytetään kaikkeen soveltuvaan yhteydenpitoon.

Voit määrittää myös liikesuhteen, joka kontaktiin on muodostettu. Kontakti voi olla esimerkiksi prospekti, pankki tai alihankkija.

## <a name="creatinge-contact-companies"></a>Kontaktiyrityksen luominen
Voit luoda kontaktin jokaiselle uudelle yritykselle (esimerkiksi asiakkaalle, toimittajalle, mahdolliselle asiakkaalle, pankille, lakiasiantoimistolle ja konsultille), jonka kanssa yrityksesi on vuorovaikutuksessa.

Kontaktin voi luoda joko alusta alkaen tai aiemmin luodusta asiakkaasta, toimittajasta tai pankkitilistä.

Ennen uuden kontaktin luomista kannattaa ehkä tarkistaa asetukset **Kontaktienhallinnan asetukset** -sivulla. Lisätietoja on kohdassa [Kontaktien hallinnan määrittäminen](marketing-setup-marketing.md).

### <a name="to-create-a-company-contact-from-scratch"></a>Yrityksen kontaktin luominen alusta alkaen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kontaktit** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Syötä **Nro**-kenttään kontaktin numero.

    Jos olet määrittänyt kontakteille numerosarjan **Kontaktienhallinnan asetukset**-sivulla, voit myös painaa Enter-näppäintä, jolloin ohjelma syöttää seuraavan saatavilla olevan kontaktinumeron.  
4. Määritä **yrityksen** **tyyppi**.
5. Täytä tarvittaessa muut kentät.

### <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Yrityksen kontaktin luominen asiakkaasta, toimittajasta tai pankkitilistä
Jos olet jo määrittänyt useita asiakkaita, toimittajia ja pankkitilejä ohjelmassa, voit luoda kontakteja olemassa olevien tietojen pohjalta. Kun luot kontaktin tällä tavalla, kontaktin tiedot synkronoidaan asiakkaan, toimittajan tai pankkitilin tietojen kanssa.

> [!NOTE]  
>   Ennen kuin voit luoda kontaktiyrityksiä tällä tavalla, asiakkaiden, toimittajien ja pankkitilien liikesuhteen koodi on määritettävä **Kontaktienhallinnan asetukset** -sivulla. Jos luot kontakteja pankkitileistä, määritä myös pankkitilien numerosarjat **Pääkirjanpidon asetukset** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä jokin seuraavista sen perusteella, missä haluat luoda kontakteja, ja valitse liittyvä linkki.
   * **Luo kontakteja asiakkaista**
   * **Luo kontakteja toimittajista**
   * **Luo kontakteja pankkitileistä**
2. Valitse avautuvalla erätyön sivulla **Asiakas**-, **Toimittaja**- tai **Pankkitili**-osa ja määritä suodattimet, jos haluat luoda kontakteja tietyistä asiakkaista, toimittajista tai pankkitileistä.
3. Aloita yhteystietojen luominen valitsemalla **OK**.

    Ohjelma liittää uusiin kontakteihin seuraavat kontaktinumerot numerosarjasta. Uusiin kontakteihin liitetään **Kontaktienhallinnan asetukset** -sivulla määritettyjen toimittajien suhde.

> [!TIP]  
>   Voit luoda kontaktista myös asiakkaan, toimittajan tai pankkitilin. Lisätietoja on kohdassa [Asiakkaan, toimittajan tai pankkitilin luominen kontaktista](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa
Jos jotkin kontakteistasi ovat myös asiakkaita, toimittajia tai pankkitilejä, voit synkronisoida kontaktin tiedot liittyvän asiakkaan, toimittajan tai pankkitilin kanssa. Synkronoimisen avulla kontaktien ja asiakkaiden, toimittajien tai pankkitilien yhteiset tiedot säilyvät samoina.  

Ennen kun synkronisoit kontaktisi asiakkaiden, toimittajien tai pankkitilien kanssa, sinun täytyy määrittää liikesuhdekoodi asiakkaille, toimittajille ja pankkitileille **Kontaktienhallinnan asetukset** -sivulla. Lisätietoja on kohdassa [Kontaktien hallinnan määrittäminen](marketing-setup-marketing.md).

### <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Erilaisia tapoja, joilla kontaktit voidaan synkronoida asiakkaiden, toimittajien ja pankkitilien kanssa
Voit synkronisoida kontaktejasi asiakkaiden, toimittajien ja/tai pankkitilien kanssa kolmella tavalla:

* linkittämällä kontakteja olemassa oleviin asiakkaisiin, toimittajiin ja/tai pankkitileihin kontaktikortilta. Lisätietoja on kohdassa [Kontaktien linkittäminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-how-link-contact.md).
* Luo asiakkaita, toimittajia tai pankkitilejä kontaktista. Lisätietoja on kohdassa [Asiakkaan, toimittajan tai pankkitilin luominen kontaktista](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Kontaktien luominen asiakkaista, toimittajista tai pankkitileistä. Lisätietoja on kohdassa [Yrityskontaktin luominen asiakkaasta, toimittajasta tai pankkitilistä](marketing-how-create-contact-companies.md).

### <a name="consequences-of-synchronization"></a>Synkronoimisen seuraukset
Kontaktin synkronoiminen asiakkaan, toimittajan ja pankkitilin kanssa

* Sinun tarvitsee päivittää tiedot vain yhteen paikkaan. Jos esimerkiksi muutat kontaktin puhelinnumeroa, puhelinnumeroon päivitetään automaattisesti sama muutos kuin asiakkaalle, toimittajalle tai pankkitilille.
* Jos olet määrittänyt numerosarjan kontakteille, kun luot asiakas-, toimittaja- tai pankkitilikortin, ohjelma luo automaattisesti kontaktikortin asiakkaalle, toimittajalle tai pankkitilille.
* Voit luoda kontaktista myyntitarjouksia ja -tilauksia sekä ostotarjouksia ja -tilauksia.
* voit saada ohjelman tallentamaan vuorovaikutuksia, kun teet erilaisia toimenpiteitä (kuten tilausten tai puitetilausten tulostaminen, myynnin huoltotilauksen luominen ja sähköpostin lähettäminen).
* jos poistat asiakkaaseen, toimittajaan ja/tai pankkitiliin linkitetyn kontaktin, vain kontakti poistuu ohjelmasta. Asiakas, toimittaja tai pankkitili säilytetään.
* jos poistat asiakkaaseen, toimittajaan ja/tai pankkitiliin linkitetyn kontaktin, vain kontakti säilytetään.

> [!NOTE]  
>   Jotkin tiedot, kuten laskutus- ja kirjaustiedot, eivät näy kontaktikortilla. Tämän vuoksi ne halutaan ehkä lisätä manuaalisesti asiakaskortille, toimittajakortille tai pankkitilikortille, kun kontakteja luodaan asiakkaina, toimittajina tai pankkitileinä.

## <a name="linking-contacts-with-customers-vendors-and-bank-accounts"></a>Kontaktien linkittäminen asiakkaiden, toimittajien ja pankkitilien kanssa
Jos kontakti ja joko asiakas, toimittaja tai pankkitili ovat samassa yrityksessä, voit linkittää nämä kaksi objektia. Kahden objektin linkittäminen mahdollistaa yhteisten tietojen synkronoimisen. Tällöin ne ovat samat molemmissa paikoissa.

### <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Kontaktin linkittäminen olemassa olevaan asiakkaaseen, toimittajaan tai pankkitiliin
1. Avaa kontakti, jonka haluat linkittää.
2. Valitse **Linkitä olemassa olevan kanssa** -toiminto ja valitse sitten **Asiakas**, **Toimittaja** tai **Pankki**.
3. Valitse asiakas, toimittaja tai pankkitili, johon linkitetään.

   Määritä **Nykyiset pääkentät** -kohdassa kentät, jotka tulee priorisoida, jos kontaktille, toimittajalle tai tilille yhteisissä kentissä esiintyy ristiriitaisia tietoja. Jos esimerkiksi myyntihenkilön koodi on erilainen kontaktilla ja asiakkaalla, voit päättää käyttää kontaktin tietoja valitsemalla **Kontakti** -kohdan.

## <a name="creating-a-customer-vendor-or-bank-account-from-a-contact"></a>Asiakkaan, toimittajan tai pankkitilin luominen kontaktista
   Haluat ehkä tallentaa jotkin aiemmin luoduista kontakteistasi asiakkaina, toimittajina tai pankkitileinä. Kun asiakas, toimittaja tai pankkitili luodaan kontaktista, voit käyttää aiemmin luotuja tietoja. Kun luot asiakkaan, toimittajan tai pankkitilin tällä tavalla, se synkronisoidaan kontaktin kanssa. Synkronoimisen avulla kontaktien ja asiakkaiden, toimittajien tai pankkitilien yhteiset tiedot säilyvät samoina.

   Ennen kuin voit tallentaa kontakteja tällä tavalla, asiakkaiden, toimittajien ja pankkitilien liikesuhteen koodi on määritettävä **Kontaktienhallinnan asetukset** -sivulla. Jos tallennat kontakteja pankkitileinä, määritä myös pankkitilien numerosarjat **Pääkirjanpidon asetukset** -sivulla.

### <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Kontaktin luominen asiakkaana, toimittajana tai pankkitilinä.
   1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kontaktit** ja valitse sitten liittyvä linkki.
   2. Valitse kontakti, jonka haluat luoda asiakkaana, toimittajana tai pankkitilinä.
   3. Valitse **Luo**-toiminto ja valitse sitten **Asiakas**, **Toimittaja** tai **Pankki**.
   4. Vahvista valintasi.

   Yhteystiedot siirretään **Kontakti**-kortilta **Pankkitili** -kortille, **Asiakas** -kortille tai **Toimittaja** -kortille. Haluat ehkä lisätä tiettyjä tietoja jokaiseen korttiin, kuten laskutus- ja maksutiedot.

## <a name="setting-up-business-relations-on-contact-companies"></a>Liikesuhteiden määrittäminen kontaktiyrityksissä
Voit käyttää liikesuhteita, kun haluat osoittaa eri kontaktien, kuten prospektin, pankin, konsultin tai palvelun toimittajan, kanssa olevan liikesuhteen.

Kontaktien liikesuhteiden käyttäminen on kaksivaiheinen prosessi. Ensin määritetään liikesuhteen koodi. Tämä vaihe suoritetaan vain kerran jokaiselle liikesuhteelle. Kun liikesuhteen koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.

> [!NOTE]  
>   Jos aiot synkronisoida kontaktisi ohjelman muissa osissa olevien toimittajien, asiakkaiden tai pankkitilien kanssa, haluat ehkä määrittää niille liikesuhteen.

### <a name="to-define-a-business-relation-code"></a>Liikesuhteen koodin määrittäminen
Liikesuhteen koodi määrittää liikesuhteen luokan tai tyypin. Se voi olla esimerkiksi PANKKI tai LAKI. Liikesuhteen koodeja voi olla useita. Määritä liikesuhde **Liikesuhteet**-sivulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liikesuhteet** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

### <a name="AssignBusRelContact"></a> Liikesuhteiden määrittäminen kontaktille
Liikesuhteita ei voi liittää kontaktihenkilöön, vaan ainoastaan yrityksiin.

1. Avaa kontakti.
2. Valitse **Yritys**-toiminto ja sitten **Liikesuhteet**-toiminto.

    **Kontaktin liikesuhteet** -sivu avautuu.
3. Valitse **Liikesuhteen koodi** -kentässä liikesuhde, jonka haluat määrittää.

Toista nämä vaiheet ja luo niin monta liikesuhdetta kuin haluat. Voit myös liittää liikesuhteita kontaktiluettelosta saman menettelytavan avulla.

Kontaktille liitettyjen liikesuhteiden lukumäärä näkyy **Kontakti**-sivun **Segmentointi**-osan **Liikesuhteiden lkm** -kentässä.

Kun olet liittänyt liikesuhteita kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on ohjeaiheessa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="see-also"></a>Katso myös
[Kontaktihenkilöiden luominen](marketing-create-contact-persons.md)   
[Business Central -sovelluksen käyttäminen](ui-work-product.md)

