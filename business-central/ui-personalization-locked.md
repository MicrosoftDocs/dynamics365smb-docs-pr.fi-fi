---
title: Syitä, miksi sivun mukauttaminen ei onnistu | Microsoft Docs
description: Lisätietoja syistä, miksi sivua ei voi mukauttaa ja miten sivun lukituksen voi avata mukauttamista varten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 64995372f68ed2804bc165823dacc34ad6a3194d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "911694"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Sivun mukauttamisen estäminen lukitsemalla

Kaksi ehtoa estää sivun mukauttamisen. Sivu on joko lukittu (jonka ![Mukautuksen lukitus](media/personalization-lock-icon.png "Mukautuksen lukitus") ilmaisee) tai se on estetty (jonka ![Mukautuksen esto](media/personalization-blocked-icon.png "Mukautuksen esto") ilmaisee).

## <a name="locked-from-personalizing"></a>Mukauttaminen estetty lukitsemalla

Jos avatun sivun **Mukautetaan**-palkissa on ![Mukautuksen lukitus](media/personalization-lock-icon.png "Mukautuksen lukitus") -kuvake (kuten kuvassa), sivua ei voi tällä hetkellä muuttaa mukauttamalla.

![Mukautuksen lukitus](media/personalization-locked.png "Mukautuksen lukitus")


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Syitä voi olla kaksi:

1. Olet mukauttanut sivua aiemmin, mutta silloin käytössä oli tuotteen aikaisempi versio. Mukautuksen taustatoimintoja on muutettu sen jälkeen, kun sivua on edellisen kerran mukautettu. Valitettavasti vanhaa ja uutta toimintatapaa ei voi käyttää yhtä aikaa.

2. Tähän saakka olet mukauttanut sivua vain [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)]illa.

### <a name="unlocking-the-page"></a>Sivun lukituksen poistaminen

Jos haluat poistaa sivun lukituksen ja jatkaa sen mukauttamista, valitse ensin ![Mukautuksen lukitus](media/personalization-lock-icon.png "Mukautuksen lukitus") ja sitten **Poista lukitus**.  

Ota kuitenkin seuraavat huomioon ennen sivun lukituksen poistamista:

- Sivun nykyiset mukautukset poistetaan. Sivu voi palautua alkuperäiseen asetteluun ja sinun on aloitettava alusta.

- Sivu säilyy [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)]issa nykyisellään eivätkä Business Central -asiakasohjelmassa tehdyt uudet mukautusmuutokset vaikuta siihen. Jatkossa [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)]in ja Business Central -asiakasohjelman mukauttaminen on erotettu täysin toisistaan.

## <a name="blocked-from-personalizing"></a>Mukauttaminen estetty

Jos Mukautetaan-palkissa on ![Mukautuksen esto](media/personalization-blocked-icon.png "Mukautuksen esto") -kuvake, mukauttaminen sivulla on estetty.

![Mukautuksen esto](media/personalization-blocked.png "Mukautuksen esto")

Syynä on se, että käyttäjätiliin tällä hetkellä liitetty roolikeskus tai profiili muokkaa tätä sivua roolin mukaisesti. Pyydä apua järjestelmänvalvojalta tai jos se tuntuu järkevältä, yritä vaihtaa roolikeskukseen, joka sisältää tämän sivun roolin mukauttamisen. (Valitse [**Omat asetukset**](https://businesscentral.dynamics.com?page=9176 "Siirry suoraan Business Centralin käyttäjäasetusten sivulle").)

## <a name="see-also"></a>Katso myös
[Työtilan mukauttaminen](ui-personalization-manage.md)  
[Mukautuksen hallinta](ui-personalization-manage.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
