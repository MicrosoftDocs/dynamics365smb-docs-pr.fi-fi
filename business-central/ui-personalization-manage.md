---
title: Roolien sivujen mukauttaminen | Microsoft Docs
description: Lisätietoja profiilin (roolin) käyttöliittymän mukauttamisesta siten, että kaikki käyttäjät, joille kyseinen rooli on määritetty, näkevät mukautetun työtilan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8e3926db3bcc1b34e2f75e6b338a86f2ddc2c20b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783357"
---
# <a name="customize-pages-for-profiles"></a>Profiilien sivujen mukauttaminen
Käyttäjät voivat mukauttaa työtilan muodostavia sivuja omien mieltymystensä mukaisesti. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

Järjestelmänvalvojat voivat mukauttaa profiilin sivuja liittyvän liiketoimintaroolin tai osaston mukaisesti esimerkiksi siten, että kaikki käyttäjät, joille profiili on määritetty, näkevät mukautetun sivuasettelun. Järjestelmänvalvoja mukauttaa sivuja samalla toiminnolla, jota käyttäjät mukauttavat sivuja.

> [!NOTE]
> Tyypillinen profiilin käyttötapa liiketoiminnassa on rooli. Profiilin nimi onkin käyttöliittymässä tämän vuoksi *Profiili (rooli)*.

Sivun mukauttaminen aloitetaan **Profiilit (roolit)** -sivulla, josta järjestelmänvalvojat aloittavat yksittäisten profiilikorttien käyttäjien profiilien hallinnan. Sivun asettelun mukauttamisen lisäksi voi kunkin profiilin **Profiili (rooli)** -sivulla voi hallita useita muita profiilien asetuksia. Lisätietoja on kohdassa [Profiilien hallinta](admin-users-profiles-roles.md).

## <a name="to-customize-pages-for-a-profile"></a>Profiilin sivujen mukauttaminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Profiilit (Roolit)** ja valitse sitten liittyvä linkki.
2. Valitse ensin sen profiilin rivi, jonka sivuja haluat mukauttaa, ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Mukauta sivuja** -toiminto.

    [!INCLUDE[prod_short](includes/prod_short.md)] avaa valitun profiilin uudessa selaimen välilehdessä siten, että **Mukauttaminen**-palkki on aktivoitu. **Mukauttaminen**-palkissa on samat toiminnot kuin käyttäjien käyttämässä **Mukautus**-palkissa.

4. Mukauta sivuja kyseisen roolin tai osaston tarpeiden mukaan samalla tavoin kuin käyttäjä tekee omat mukautuksensa. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

    > [!NOTE]
    > Voit siirtyä mukauttamisen aikana käyttämällä toiminnossa CTRL+napsautus-yhdistelmää, jos nuolenpää osoittaa toiminnon olevan valittuna.

5. Kun olet muuttanut yhden tai usean sivun asettelua, valitse **Mukauttaminen**-palkissa **Valmis**-painike.
6. Sulje selaimen välilehti.

Sivujen mukauttaminen on nyt tallennettu profiiliin.

## <a name="to-view-all-customized-pages-for-a-profile"></a>Kaikkien profiilin mukautettujen sivujen näyttäminen

Saat tarvittaessa yleiskuvan profiiliin mukautetuista sivuista, mikä auttaa suunnittelemaan esimerkiksi sivujen lisämukautuksia tai poistamisia.

- Valitse **Profiili (rooli)** -sivulla **Hallitse mukautettuja sivuja** -toiminto.

**Mukautetut sivut** -sivulla voit poistaa mukautuksia ja tehdä vian määrityksen tarkistamalla mahdolliset ongelmat.  

## <a name="to-delete-all-customizations-for-a-profile"></a>Profiilin kaikkien mukautusten poistaminen
Voit peruuttaa kaikki profiiliin tehdyt mukautukset. Laajennukseen perustuvia mukautuksia ja käyttäjän tekemiä mukautuksia ei poisteta. Voit poistaa kaikki mukautukset toisella toiminnolla. Lisätietoja on kohdassa [Kaikkien käyttäjän tekemien mukautusten poistaminen](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- Valitse mukautetun profiilin **Profiili (rooli)** -sivulla **Poista mukautetut sivut** -toiminto.

Profiilin sivujen asetteluksi palautetaan oletusasettelu.  

## <a name="to-delete-customization-for-specific-pages-for-a-profile"></a>Profiilin tiettyjen sivujen mukautusten poistaminen
Voit poistaa profiilin yksittäisen sivun mukautukset. Laajennukseen perustuvia mukautuksia ja käyttäjän tekemiä mukautuksia ei poisteta. Voit poistaa tietyn sivun mukautukset toisella toiminnolla. Lisätietoja on kohdassa [Tiettyjen sivujen mukautusten poistaminen](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. Valitse **Profiili (rooli)** -sivulla **Hallitse mukautettuja sivuja** -toiminto.
2. Valitse **Mukautetut sivut** -sivulla vähintään yhden poistettavan sivun mukautuksen rivi ja valitse sitten **Poista**-toiminto.

Valitun sivun asettelu muutetaan vastaamaan tekemiäsi muutoksia.

## <a name="see-also"></a>Katso myös

[Työtilan mukauttaminen](ui-personalization-user.md)  
[Profiilien hallinta](admin-users-profiles-roles.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]