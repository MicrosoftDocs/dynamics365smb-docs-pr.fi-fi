---
title: Tietojen kopioiminen ja liittäminen
description: Kopioi kentät ja rivit Business Central -sivuilta ja liitä ne toisaalle.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, keyboarding
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: aca14f68e0e1923addbc1cf61926ff5078d6b078
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194569"
---
# <a name="copy-and-paste-faq"></a>Kopioimisen ja liittämisen usein kysytyt kysymykset
Voit kopioida yhden rivin tai useita rivejä (tietueita) luettelosta tai yhden kentän sivulta ja liittää kopioidut kohteet samalle sivulle, toiselle sivulle tai ulkoiseen asiakirjaan (kuten Microsoft Exceliin tai Outlook-sähköpostiin). Jos haluat kopioida, paina näppäimiä CTRL+C (cmd+C macOS-käyttöjärjestelmässä). Jos haluat liittää, paina näppäimiä CTRL+V (cmd+V macOS-käyttöjärjestelmässä).

Kopioimiseen ja liittämiseen on useita muita pikanäppäimiä nopeaa tietojen syöttämistä varten. Lisätietoja on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#CopyRows).

Tässä artikkelissa on vastauksia kopioimiseen ja liittämiseen liittyviin yleisiin kysymyksiin.  

## <a name="what-can-i-copy-and-paste"></a>Mitä voin kopioida ja liittää?
- Voit kopioida yhden rivin tai useita rivejä [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa samaan luetteloon tai mihin tahansa luetteloon, jossa on samat sarakkeet.
- Kopioi yksi rivi tai useita rivejä [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa ja liitä ne Exceliin tai muihin sovelluksiin.
- Kopioi yksi rivi tai useita rivejä Excelissä ja liitä ne [!INCLUDE[d365fin](includes/d365fin_md.md)] -luetteloon.
- Kopioi yksittäisen kentän arvo [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa ja liitä se mihin tahansa.

## <a name="does-copy-and-paste-work-with-tiles"></a>Voiko kopioimista ja liittämistä käyttää ruutujen kanssa?
Kyllä mutta vain yksi valittu ruutu.

## <a name="how-do-i-copy-a-row"></a>Miten rivi kopioidaan?
Kopioi yksi rivi valitsemalla se ja painamalla sitten näppäinyhdistelmää Ctrl+C.

Jos haluat kopioida enemmän rivejä, tee seuraavat toiminnot:
- Käytä toisen rivin kohdalla pikanäppäimiä Ctrl+napsautus tai Vaihto+napsautus ja valitse rivi tai kaikki välissä olevat rivit. Lisätietoja hiiren ja näppäimistön yhdistelmistä rivien valitsemisessa on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#CopyRows) .
- Valitse ![Näytä enemmän vaihtoehtoja](media/show-more-options-icon.png "Näytä enemmän vaihtoehtoja kuvakkeen") ensimmäisessä sarakkeessa. Valitse **Valitse lisää**, valitse sitten kopioitavien rivien kohdalla oleva valintaruutu ja paina näppäinyhdistelmää Ctrl+C.

## <a name="how-do-i-paste-rows"></a>Miten liitän rivejä?
Valitse tyhjä rivi, jossa kohdistus on jossakin solussa, ja paina sitten näppäinyhdistelmää Ctrl+V.

Jos haluat korvata olemassa olevia rivejä, valitse rivit ja paina sitten näppäinyhdistelmää Ctrl+V. Tässä tapauksessa voit liittää vain yhtä monta riviä kuin valitsit.

> [!NOTE]
> Liitettävää luetteloa on voitava muokata.

<!-- Rows are pasted directly where your cursor is located. If you paste into an empty line, any existing subsequent lines will be moved after the pasted lines. If you paste into an existing line or lines, this will be overwritten.-->

## <a name="can-i-paste-rows-into-an-outlook-email"></a>Voinko liittää rivejä Outlook-sähköpostiviestiin?
Kyllä. Tämä liitetään muotoiltuna taulukkona, joka säilyttää [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa nähnyt sisennykset, numeerisen tasauksen ja värit.

## <a name="in-which-lists-can-i-copy-and-paste-rows"></a>Missä luetteloissa voin kopioida ja liittää rivejä?
Voit kopioida rivejä kaikissa luetteloissa, esimerkiksi työkirjoissa, tietoruuduissa ja sivuun upotetuissa luetteloissa (esimerkiksi myyntitilauksen rivit). Jos rivejä halutaan liittää, luettelon on oltava muokattavissa.

Joillakin sivuilla sovelluksen rakenne voi estää rivien liittämisen. Ota yhteyttä järjestelmänvalvojaan tai sovelluksen kehittäjään, jos haluat muuttaa sivun [Editable-ominaisuutta](/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) tai lähdetaulukon [PasteIsValid-ominaisuutta](/dynamics365/business-central/dev-itpro/developer/properties/devenv-pasteisvalid-property).

## <a name="on-which-clients-is-copy-and-paste-available"></a>Missä asiakasohjelmissa kopioiminen ja liittäminen on käytettävissä?
Kopioiminen ja liittäminen ovat käytettävissä [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen selaimessa Windows 10 -käyttöjärjestelmässä.

## <a name="what-is-the-maximum-number-of-rows-that-can-be-copied"></a>Mikä on kopioitavien rivien enimmäismäärä?
Voit kopioida niin monta riviä kuin näkymässä on. Jos esimerkiksi haluat kopioida kaikki sivun 1 000 riviä, siirry ensin sivun alaosaan ja odota, kunnes rivit näkyvät. Aloita kopioiminen vasta sitten. Vain laitteen muisti voi rajoittaa kopioitavien rivien enimmäismäärää.

## <a name="must-i-have-the-exact-same-number-of-columns-when-pasting-rows"></a>Onko sarakkeita oltava täsmälleen sama määrä, kun rivejä liitetään?
Kyllä. Jos kopioit [!INCLUDE[d365fin](includes/d365fin_md.md)]ista, Excelistä tai toisesta taulukkolähteestä, [!INCLUDE[d365fin](includes/d365fin_md.md)]iin liitettävien rivien määrän on oltava täsmälleen sama kuin sarakkeiden määrä.

## <a name="why-do-i-get-errors-when-pasting-rows"></a>Milloin rivien liittämisen yhteydessä voi tulla virhesanomia?
Jos liittäminen tehdään [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellukseen, jokainen rivi tarkistetaan. Näin varmistetaan, että kaikkien sarakkeiden arvot ovat sallittuja. Jos sarakkeessa on arvo, joka ei ole sallittu, liittäminen pysäytetään ja näyttöön tulee virhesanoma. Tämän voi välttää varmistamalla ennen liittämistä, että sarakkeissa on sallitut arvot.


## <a name="see-also"></a>Katso myös .
[Aputoiminnot](ui-accessibility.md)  
[Käytön aloittaminen](product-get-started.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Usein kysytyt kysymykset](across-faq.md)  
