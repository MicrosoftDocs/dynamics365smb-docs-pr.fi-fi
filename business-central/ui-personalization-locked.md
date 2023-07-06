---
title: Sivun mukauttamisen estäminen lukitsemalla
description: 'Sivun mukauttaminen on ehkä estetty. Lue tästä, miten voit poistaa lukituksen niin, että voit muokata sitä.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="why-a-page-is-locked-from-personalization"></a><a name="why-a-page-is-locked-from-personalization"></a><a name="why-a-page-is-locked-from-personalization"></a>Sivun mukauttamisen estäminen lukitsemalla

Kaksi ehtoa estää sivun mukauttamisen. Sivu on joko lukittu (kuten ![Mukautuksen lukitus.](media/personalization-lock-icon.png "Mukautuksen lukitus") -kuvake ilmaisee) tai se on estetty (kuten ![Mukautuksen esto.](media/personalization-blocked-icon.png "Mukauttaminen estetty") -kuvake ilmaisee).

## <a name="locked-from-personalizing"></a><a name="locked-from-personalizing"></a><a name="locked-from-personalizing"></a>Mukauttaminen estetty lukitsemalla

Jos ![Mukautuksen lukitus.](media/personalization-lock-icon.png "Mukautuksen lukitus") -kuvake on näkyvissä **Mukautetaan**-palkissa, kun avaat sivun, sivun muuttaminen mukauttamalla on tällä hetkellä estetty.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Syitä voi olla kaksi:

1. Olet mukauttanut sivua aiemmin, mutta silloin käytössä oli tuotteen aikaisempi versio. Mukautuksen taustatoimintoja on muutettu sen jälkeen, kun sivua on edellisen kerran mukautettu. Valitettavasti vanhaa ja uutta toimintatapaa ei voi käyttää yhtä aikaa.

2. Tähän saakka olet mukauttanut sivua vain vanhentuneella [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] -ohjelmalla.

### <a name="unlocking-the-page"></a><a name="unlocking-the-page"></a><a name="unlocking-the-page"></a>Sivun lukituksen poistaminen

Jos haluat poistaa sivun lukituksen ja jatkaa sen mukauttamista, valitse ensin ![Mukautuksen lukitus](media/personalization-lock-icon.png "Mukautuksen lukitus") -kuvake ja valitse sitten **Poista lukitus** -toiminto.  

> [!CAUTION]
> Sivun nykyiset mukautukset poistetaan. Sivu voi palautua alkuperäiseen asetteluun ja sinun on aloitettava alusta.  

## <a name="blocked-from-personalizing"></a><a name="blocked-from-personalizing"></a><a name="blocked-from-personalizing"></a>Mukauttaminen estetty

Jos ![Mukautuksen esto](media/personalization-blocked-icon.png "Mukauttaminen estetty") -kuvake on **Mukautetaan**-palkissa, sivulle ei voi tehdä mukautuksia.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked.](media/personalization-blocked.png "Personalize lock") -->

Syynä on se, että käyttäjätiliin tällä hetkellä liitetty roolikeskus tai rooli muokkaa tätä sivua roolin mukaisesti. Pyydä apua järjestelmänvalvojalta. Vaihtoehtoisesti voit yrittää siirtyä roolikeskukseen, jossa on tämän sivun roolimukautus. Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Työtilan mukauttaminen](ui-personalization-user.md)  
[Profiilien sivujen mukauttaminen](ui-personalization-manage.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
