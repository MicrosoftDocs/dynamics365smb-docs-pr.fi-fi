---
title: "Mukautusten hallinta Financialsin järjestelmänvalvojana | Microsoft Docs"
description: "Lisätietoja käyttöliittymän mukauttamisesta omaan työskentelytapaan sopivaksi."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 854dddab2d958e128309aa201b53234d87d2c049
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="managing-personalization-as-an-administrator"></a>Mukautuksen hallinta järjestelmänvalvojana
<!--NAV in the Web client-->
Käyttäjät voivat mukauttaa työtilansa omien mieltymystensä mukaiseksi. Järjestelmänvalvojana voit ohjata ja hallita mukauttamista poistamalla sivujen mukautusmahdollisuus käyttäjiltä ja poistamalla käyttäjien mahdollisesti tekemät mukautukset.

## <a name="disable-personalization-for-a-profile"></a>Profiilin mukauttamisen poistaminen
Voit estää sivujen mukauttamisen kaikilta tiettyyn profiiliin kuuluvilta käyttäjiltä.
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Profiilit** ja valitse sitten aiheeseen liittyvä linkki.
2.  Valitse luettelossa muokattava profiili.
3. Valitse **Poista mukauttaminen käytöstä** -valintaruutuja valitse sitten **OK**.

## <a name="clear-user-personalizations"></a>Käyttäjän mukautusten tyhjentäminen

Mukautetun sivun muutosten tyhjentäminen palauttaa sivun mukautuksia edeltävän alkuperäisen asettelun. Käyttäjien sivulle tekemät mukautukset voi tyhjentää kahdella tavalla: käyttämällä **Poista käyttäjän mukautus** -sivua tai käyttämällä **Käyttäjän mukautuskortti** -sivua.

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Käyttäjän mukautusten tyhjentäminen Poista käyttäjän mukautus -sivun avulla

Voit tyhjentää **Poista käyttäjän mukautus** -sivulla mukautukset kultakin käyttäjältä sivukohtaisesti.

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Poista käyttäjän mukautus** ja valitse sitten aiheeseen liittyvä linkki.

    Sivulla on luettelo kaikista mukautetuista sivuista ja käyttäjästä, jolle se kuuluu.

    >[!NOTE]
    > **Vanha mukautus** -sarakkeiden valintamerkki ilmaisee, että mukautus tehtiin [!INCLUDE[d365fin](includes/d365fin_md.md)]in vanhassa versiossa, jossa mukautusta käsiteltiin eri tavalla kuin nyt. Mukautus estetään näiden sivujen mukautusta yrittäviltä käyttäjiltä, elleivät he ensin valitse sivun lukituksen poistamista. Lisätietoja on kohdassa [Sivun mukauttamisen estäminen lukitsemalla](ui-personalization-locked.md).

2. Valitse ensin poistettava tapahtuma ja sitten **Poista**-toiminto.

    Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Käyttäjän mukautusten tyhjentäminen Käyttäjän mukautuskortti -sivun avulla

Voit tyhjentää **Käyttäjän mukautuskortti** -sivulla tietyn käyttäjän kaikki mukautukset. Tämä edellyttää taulukon 2000000072 **Profiili** kirjoitusoikeuksia.

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Käyttäjän mukautus** ja valitse sitten aiheeseen liittyvä linkki.

    **Käyttäjän mukautus** -sivulla on luettelo kaikista käyttäjistä, joilla mahdollisesti on mukautettuja sivuja. Jos käyttäjä ei löydy luettelosta, kyseisellä käyttäjällä ei ole mukautettuja sivuja.

2. Valitse ensin käyttäjä luettelossa ja sitten **Muokkaa**-toiminto.

3.  Valitse **Toiminnot**-välilehdessä **Tyhjennä mukautetut sivut**.

    Käyttäjä näkee muutokset kirjautuessaan sisään seuraavan kerran.

## <a name="see-also"></a>Katso myös
[Työtilan mukauttaminen](ui-personalization-user.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttökokemuksen mukauttaminen](ui-experiences.md)  

