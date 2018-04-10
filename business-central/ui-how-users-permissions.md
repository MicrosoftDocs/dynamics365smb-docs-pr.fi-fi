---
title: "Käyttöoikeuksien määrittäminen tai muokkaaminen | Microsoft Docs"
description: "Lisätietoja Office 365 -käyttäjien lisäämisestä Business Central -sovellukseen sekä käyttöoikeuksien ja suojausasetusten määrittämisestä."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 03/16/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 6d350a064f134c4c29938005fea966dec7cca142
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="manage-users-and-permissions"></a>Käyttäjien ja käyttöoikeuksien hallinta
Käyttäjiä voi lisätä [!INCLUDE[d365fin](includes/d365fin_md.md)]iin sen jälkeen, kun yrityksen Office 365:n järjestelmänvalvoja on ensin luonut käyttäjät Office 365:n hallintaportaalissa. Lisätietoja on kohdassa [Käyttäjien lisääminen Office 365 for Businessiin](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Kun käyttäjät on luotu Office 365:ssa, heidät voidaan tuoda **Käyttäjät**-ikkunaan **Hae käyttäjät Office 365:stä** -toiminnolla. Käyttäjille määritetään käyttöoikeusjoukot sen mukaan, mitä palvelupaketti on määritetty käyttäjälle Office 365:ssä.

Voit sitten määrittää käyttäjille käyttöoikeusjoukkoja, jotka määrittävät, mitä tietokantaobjekteja siten myös mitä käyttöliittymäelementtejä käyttäjät saavat käyttää ja missä yrityksissä niitä saa käyttää. Voit lisätä käyttäjiä käyttäjäryhmiin. Tämä helpottaa samojen käyttöoikeusjoukkojen määrittämistä useille käyttäjille.

Oikeussarja on joukko tietyn tietokannan objektien käyttöoikeuksia. Kaikille käyttäjille on määritettävä vähintään yksi käyttöoikeusjoukko, ennen kuin he voivat käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]ia. Tietyt ennalta määritetyt käyttöoikeusryhmät ovat valmiina oletusarvoisesti. Voit käyttää näitä käyttöoikeusjoukkoja oletuksena, muokata käyttöoikeuksien oletusjoukkoja tai luoda lisäkäyttöoikeusjoukkoja.

Järjestelmänvalvojat voivat määrittää **Käyttäjäasetukset**-ikkunassa ajanjaksoja, joiden aikana määritetyt käyttäjät voivat tehdä kirjauksia. He voivat myös määrittää, kirjaako järjestelmä ajan, jonka käyttäjät olivat kirjautuneena.

## <a name="to-assign-permissions-to-a-user"></a>Käyttöoikeuksien määrittäminen käyttäjälle
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Valitse käyttäjä, jolle haluat määrittää käyttöoikeuden.
Kaikki käyttäjälle jo määritetyt käyttöoikeusjoukot **Käyttöoikeuksien joukot** -tietoruudussa.
3. Avaa **Käyttäjän kortti** -ikkuna valitsemalla **Muokkaa** -toiminto.
4. Täytä **Käyttöoikeuksien joukot** -tietoruudun uudella rivillä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Käyttäjien ryhmittäminen käyttäjäryhmiin
Voit määrittää käyttäjäryhmiä auttamaan hallitsemaan oikeusryhmät käyttäjäryhmille yrityksessä.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Vaihtoehtoisesti voit valita **Käyttäjät**-ikkunassa **Käyttäjäryhmät**-toiminnon.
3. Valitse **Käyttäjäryhmä**-ikkunassa **Käyttäjäryhmän jäsenet** -toiminto.
6. Valitse **Käyttäjäryhmän jäsenet** -ikkunassa **Lisää käyttäjiä** -toiminto.
7. Voit lisätä uusia käyttöoikeusjoukkoja tai lisäkäyttöoikeusjoukkoja valitsemalla **Käyttäjäryhmät**-ikkunassa **Käyttäjäryhmän käyttöoikeuksien joukot** -toiminnon.
8. Täytä **Käyttäjäryhmän käyttöoikeuksien joukot** -ikkunan uudella rivillä tarvittavat kentät tekemällä valintoja aiemmin luoduista käyttöoikeuksien joukoista.

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Käyttäjäryhmän ja sen kaikkien käyttöoikeuksien joukkojen kopioiminen
Voit määrittää uuden käyttäjäryhmän nopeasti kopioimalla kaikki käyttöoikeusjoukot aiemmin luodusta käyttäjäryhmästä uuteen käyttäjäryhmään.

Käyttäjäryhmän jäseniä ei kopioida uuteen käyttäjäryhmään. Heidät on lisättävä myöhemmin manuaalisesti.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Valitse ensin kopioitava käyttäjäryhmä ja sitten **Kopioi käyttäjäryhmä** -toiminto.
3. Anna **Uuden käyttäjäryhmän koodi** -kentässä ryhmälle nimi ja valitse sitten **OK**-painike.

Uusi käyttäjäryhmä lisätään **Käyttäjäryhmät**-ikkunaan. Aloita käyttäjien lisääminen. Lisätietoja on osassa Käyttäjien ryhmittäminen käyttäjäryhmiin

## <a name="to-set-up-user-time-constraints"></a>Määritä käyttäjän aikarajoitukset
Järjestelmänvalvojat voivat määrittää ajanjaksoja, joiden aikana määritetyt käyttäjät voivat tehdä kirjauksia. He voivat myös määrittää, kirjaako järjestelmä ajan, jonka käyttäjät olivat kirjautuneena. Järjestelmänvalvojat voivat myös määrittää käyttäjille vastuupaikkoja. Lisätietoja on kohdassa [Vastuupaikkojen käyttäminen](inventory-responsibility-centers.md).

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoitta **Resurssienhallinnan asetukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse avautuvassa **Käyttäjäasetukset**-ikkunassa **Uusi**-toiminto.
3. Anna **Käyttäjätunnus**-kentässä käyttäjän tunnus tai valitse kenttä, jos haluat nähdä kaikki järjestelmässä tällä hetkellä olevat Windows-käyttäjät.
4. Täytä tarvittavat kentät.

## <a name="see-also"></a>Katso myös
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Hallinta](admin-setup-and-administration.md)  
[Käytön aloittaminen](product-get-started.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
