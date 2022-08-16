---
title: Projektin projektikortin luominen ja tehtävien määrittäminen
description: Uudelle projektille luodaan projektin tehtävät ja suunnittelurivit sisältävä projektikortti, mikä auttaa edistymisen ja budjettien hallinnassa.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management, task
ms.search.form: 88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020
ms.date: 08/03/2022
ms.author: edupont
ms.openlocfilehash: 8d70c11aa3d467ada4f7aae3a1cf3efa1603bbe4
ms.sourcegitcommit: bb9b2b4e693fa326a13d94e5e83f60e6c7ac5b68
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227470"
---
# <a name="create-jobs"></a>Projektien luominen

Uuden projektin aloittamisen yhteydessä on luotava projektikortti sekä integroidut projektitehtävät ja projektin suunnittelurivit kahteen eri tasoon.  

Ensimmäinen taso koostuu projektitehtävistä. Projektille on luotava vähintään yksi projektitehtävä, koska kirjaukset viittaavat projektitehtävään. Kun projektissa on vähintään yksi projektitehtävä, voit määrittää projektin suunnittelurivejä ja kirjata projektin kulutuksen.

Toinen taso koostuu projektin suunnitteluriveistä, jotka määrittävät yksityiskohtaisesti resurssien ja nimikkeiden käytön sekä erilaiset kirjanpidon kulut.

Tason rakenteen avulla voit jakaa projektin pienemmiksi tehtäviksi ja käyttää tarkempia tietoja budjetoinnissa, tarjouksissa ja rekisteröinnissä. Lisäksi saat sen avulla tietoja projektin etenemisestä. Voit seurata esimerkiksi sitä, miten olet saavuttanut määritetyt välitavoitteet tai oletko saavuttamassa budjettiin määritetyt tavoitteet.

> [!TIP]
> Käynnistä asetusten ohjattu määritys valitsemalla **Uusi projekti** -toiminto **Projektipäällikkö**-roolikeskuksessa. Ohjattu määritys ohjaa vaihe vaiheelta projektin ja integroitujen tehtävien ja suunnittelurivien luomisessa. Seuraavassa kerrotaan, miten vaiheet suoritetaan manuaalisesti. Esimerkki projektin manuaalisesta luomisesta on [videossa: Projektin luonti Dynamics 365 Business Centralissa](https://www.youtube.com/watch?v=VqaPWr7BWmw).

Joskus palvelua vastaanottava osapuoli eroaa laskun maksavasta osapuolesta. **Projektit**-sivulla voit määrittää projektista hyötyvän asiakkaan **Tilausasiakas**-kentissä sekä laskutettavan osapuolen **Laskutusasiakas**-kentissä. Voit antaa myös seuraavat tiedot: 

* Valitse työn suorituspaikka asiakkaan toimitusasiakkaiden osoitteiden luettelosta.
* Lisää ulkoisten viitteiden tietoja yksinkertaistaaksesi projektia koskevaa viestintää.
* Korvaa projektin vakiotalousehdot.

## <a name="to-create-a-job-card"></a>Projektikortin luominen

Luo projektikortti ja luo sitten projektikortille työtehtävä ja projektin suunnittelurivit.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit määrittää projektille muiden projektien tiedot valitsemalla **Kopioi projekti** -toiminnon, täyttämällä tarvittavat kentät ja valitsemalla sitten **OK**-painikkeen.

> [!NOTE]  
> Jos projektissa käytetään aikaraportteja, myös vastuussa oleva henkilö on määritettävä. Tämä henkilö voi hyväksyä työhön liittyvien työntekijätehtävien tuntilomakkeet. Lisätietoja on kohdassa [Aikaraporttien määrittäminen](projects-how-setup-time-sheets.md).

Voit halutessasi merkitä projektin toimintoja estetyiksi **Estetty**-kentän avulla Seuraavassa taulukossa kuvataan tämän kentän vaihtoehtojen vaikutukset.

|Asetus  |Kuvaus  |
|---------|---------|
|Tyhjä |Kaikki toimenpiteet ovat sallittuja.|
|Kirjaus    |Voit käsitellä suunnittelurivejä, mutta projekti on suljettu kirjauksilta. Jos valitset tämän vaihtoehdon, projektin käyttöä tai myyntiä ei voi kirjata.|
|Kaikki  |Kaikki toimenpiteet ovat suljettuja.|

## <a name="to-create-tasks-for-a-job"></a>Luo projektille tehtäviä

Projektin luomisen keskeinen osa on määrittää siihen liittyvät tehtävät. Voit määrittää tehtäviä luomalla yhden rivin tehtävää kohti **Tehtävät**-pikavälilehdessä **Työkortti**-sivulla. Jokaisella projektilla on oltava vähintään yksi tehtävä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.
2. Avaa asianmukaisen projektin projektikortti.
3. Täytä **Tehtävät**-pikavälilehden uuden rivin kentät tarvittaessa.
4. Kun haluat sisentää tehtäviä ja luoda hierarkian, valitse **Tehtävät**-toiminto ja sen jälkeen **Sisennä projektitehtävät** -toiminto.
5. Toista vaiheet 3 ja 4 kaikille projektissa tarvittaville tehtäville.
6. Voit määrittää projektitehtäville muiden projektitehtävien tiedot valitsemalla **Kopioi projektitehtävät kohteesta** -toiminnon, täyttämällä tarvittavat kentät ja valitsemalla sitten **OK**-painikkeen.

## <a name="to-create-planning-lines-for-a-job"></a>Projektin suunnittelurivien luominen

Voit tarkentaa uusia projektitehtäviä projektin suunnitteluriveillä. Suunnitteluriville voi kerätä tiedot, joita haluat seurata projektissa. Voit esimerkiksi seurata projektin tarvitsemia resursseja tai nimikkeitä. Käytettävissä on esimerkiksi tehtävä, jossa asiakkaan toivotaan hyväksyvän projekti. Tehtävä liitetään nimikkeiden suunnitteluriveihin, esimerkiksi asiakastapaamiseen tai resurssin liittämiseen.  

Projektin suunnittelurivin tyyppi voi olla jokin seuraavista tyypeistä.  

| Tyyppi | Kuvaus |
| --- | --- |
| **Budjetti** |Projektin käytön ja kustannusten arviointi, yleensä Aika ja materiaali -tyyppisessä projektissa. Tällaisia suunnittelurivejä ei voi laskuttaa. |
| **Laskutettava** |Asiakkaan arviolaskutus, yleensä kiinteähintainen projekti. |
| **Sekä budjetti että laskutettava** |Budjetoitu käyttö on sama kuin laskutettava käyttö. |

> [!NOTE]
> Kustannustiedot täytetään automaattisesti projektin suunnittelurivien tietojen lisäyksen aikana. Esimerkiksi resurssien ja nimikkeiden kustannus, hinta ja alennus perustuvat resurssin ja nimikkeen tietoihin. 

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.
2. Avaa sopiva työkortti.
3. Valitse projektitehtävä, jonka **Projektitehtävätyyppi**-kentän arvo on **Kirjaus**. Valitse sitten **Projektin suunnittelurivit** -toiminto.  
4. Täytä **Projektin suunnittelurivit** -sivun uuden rivin tarvittavat kentät.
5. Toista vaiheet 3 ja 4 kaikille projektitehtävässä tarvittaville suunnitteluriveille.

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/create-new-job/)

## <a name="see-also"></a>Katso myös

[Projektinhallinta](projects-manage-projects.md)  
[Video: Projektin luonti Dynamics 365 Business Centralissa](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
