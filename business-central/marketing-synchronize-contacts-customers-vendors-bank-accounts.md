---
title: Kontaktien synkronointi asiakkaiden ja toimittajien kanssa| Microsoft Docs
description: "Voit muodostaa yhteyden kontaktien, jotka ovat myös asiakkaita, toimittajia tai pankkitilejä, yhteystietoihin tai synkronoida ne, joten tiedot tarvitsee päivittää vain yhdessä paikassa."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 10/01/2018
ms.author: edupont
redirect_url: marketing-create-contact-companies
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 84cb3a6a96826ad5e3d1824ed5182dfcd972d0b3
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Kontaktien synkronoiminen asiakkaiden, toimittajien ja pankkitilien kanssa
Jos jotkin kontakteistasi ovat myös asiakkaita, toimittajia tai pankkitilejä, voit synkronisoida kontaktin tiedot liittyvän asiakkaan, toimittajan tai pankkitilin kanssa. Synkronoimisen avulla kontaktien ja asiakkaiden, toimittajien tai pankkitilien yhteiset tiedot säilyvät samoina.  

Ennen kun synkronisoit kontaktisi asiakkaiden, toimittajien tai pankkitilien kanssa, sinun täytyy määrittää liikesuhdekoodi asiakkaille, toimittajille ja pankkitileille **Kontaktienhallinnan asetukset** -sivulla. Lisätietoja on kohdassa [Kontaktien hallinnan määrittäminen](marketing-setup-marketing.md).

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Erilaisia tapoja, joilla kontaktit voidaan synkronoida asiakkaiden, toimittajien ja pankkitilien kanssa
Voit synkronisoida kontaktejasi asiakkaiden, toimittajien ja/tai pankkitilien kanssa kolmella tavalla:

* linkittämällä kontakteja olemassa oleviin asiakkaisiin, toimittajiin ja/tai pankkitileihin kontaktikortilta. Lisätietoja on kohdassa [Kontaktien linkittäminen asiakkaiden, toimittajien ja pankkitilien kanssa](marketing-how-link-contact.md).
* Luo asiakkaita, toimittajia tai pankkitilejä kontaktista. Lisätietoja on kohdassa [Asiakkaan, toimittajan tai pankkitilin luominen kontaktista](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Kontaktien luominen asiakkaista, toimittajista tai pankkitileistä. Lisätietoja on kohdassa [Yrityskontaktin luominen asiakkaasta, toimittajasta tai pankkitilistä](marketing-how-create-contact-companies.md).

## <a name="consequences-of-synchronization"></a>Synkronoimisen seuraukset
Kontaktin synkronoiminen asiakkaan, toimittajan ja pankkitilin kanssa

* Sinun tarvitsee päivittää tiedot vain yhteen paikkaan. Jos esimerkiksi muutat kontaktin puhelinnumeroa, puhelinnumeroon päivitetään automaattisesti sama muutos kuin asiakkaalle, toimittajalle tai pankkitilille.
* Jos olet määrittänyt numerosarjan kontakteille, kun luot asiakas-, toimittaja- tai pankkitilikortin, ohjelma luo automaattisesti kontaktikortin asiakkaalle, toimittajalle tai pankkitilille.
* Voit luoda kontaktista myyntitarjouksia ja -tilauksia sekä ostotarjouksia ja -tilauksia.
* voit saada ohjelman tallentamaan vuorovaikutuksia, kun teet erilaisia toimenpiteitä (kuten tilausten tai puitetilausten tulostaminen, myynnin huoltotilauksen luominen ja sähköpostin lähettäminen).
* jos poistat asiakkaaseen, toimittajaan ja/tai pankkitiliin linkitetyn kontaktin, vain kontakti poistuu ohjelmasta. Asiakas, toimittaja tai pankkitili säilytetään.
* jos poistat asiakkaaseen, toimittajaan ja/tai pankkitiliin linkitetyn kontaktin, vain kontakti säilytetään.

> [!NOTE]  
>   Jotkin tiedot, kuten laskutus- ja kirjaustiedot, eivät näy kontaktikortilla. Tämän vuoksi ne halutaan ehkä lisätä manuaalisesti asiakaskortille, toimittajakortille tai pankkitilikortille, kun kontakteja luodaan asiakkaina, toimittajina tai pankkitileinä.

## <a name="see-also"></a>Katso myös
[Kontaktien hallinta](marketing-contacts.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

