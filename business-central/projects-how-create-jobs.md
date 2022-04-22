---
title: Projektin projektikortin luominen ja tehtävien määrittäminen
description: Uudelle projektille luodaan projektin tehtävät ja suunnittelurivit sisältävä projektikortti, mikä auttaa edistymisen ja budjettien hallinnassa.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management, task
ms.search.form: 88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6996c82ee184db980879ea98a6f2cbdca1b10852
ms.sourcegitcommit: 55f42d2407e109b4924218cb22129467b53deb08
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/08/2022
ms.locfileid: "8557180"
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
>   Jos projektissa käytetään aikaraportteja, myös vastuussa oleva henkilö on määritettävä. Tämä henkilö voi hyväksyä työhön liittyvien työntekijätehtävien tuntilomakkeet. Lisätietoja on kohdassa [Aikaraporttien määrittäminen](projects-how-setup-time-sheets.md).

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

## <a name="create-inventory-and-warehouse-pick-documents-for-a-job"></a>Luo varaston ja fyysisen varaston poiminta-asiakirjat projektille
Jos haluat luoda varaston ja fyysisen varaston poiminta-asiakirjat projekteille, järjestelmänvalvojan on määritettävä **Ominaisuuspäivitys: Ota käyttöön varaston ja fyysisen varaston poiminnat projekteista** -kohta käyttöön **Ominaisuuksien hallinta** -sivulla.

Toiminto lisää **Luo varastopoiminta**- ja **Luo fyysisen varaston poiminta** -toiminnot **projektikorttiin**. Jos haluat luoda tai rekisteröidä poiminta-asiakirjan, käytä **Hyllytys-/poiminta-/siirtorivit**- tai **Rekisteröidyt poimintarivit** -toimintoa.

Voit käyttää toimintoja seuraavien ehtojen perusteella:
* Projektin **tila** on **Avoin**.
* Projektin suunnittelurivin **rivityyppi** on **Budjetti** tai **Sekä budjetti että laskutettava**.
* Projektin suunnittelurivin **tyyppi** on **Nimike**.
* **Vaadi poiminta** -kohta on otettu käyttöön liittyvässä sijainnissa.
* **Ohjattu hyllytys ja poiminta** on poistettu käytöstä.

> [!NOTE] 
> Vaikka asetuksen nimi on **Vaadi poiminta**, voit silti kirjata kulutuksen suoraan projektin päiväkirjariviltä sijainnissa. Jos sijainti on asetettu vaatimaan poimintaprosessia mutta ei toimitusprosessia, sinun tulee käyttää **Varastopoiminta**-sivua poiminnan tietojen järjestämisessä ja tulostamisessa. Voit käyttää sivua myös poiminnan tuloksen syöttämisessä ja kirjaamisessa. Tämä kirjaa nimikkeiden kulutuksen. 
> 
> Jos sijainti on määritetty edellyttämään sekä poiminta- että toimituskäsittelyä eli olet valinnut sekä **Vaadi poiminta**- ja **Vaadi toimitus** -kohdan **Sijaintikortti**-sivulla, voit käsitellä poiminnan **F. varaston poiminta** -sivulla. Fyysisen varaston poiminnat ovat samanlaisia kuin varaston poiminnat. Erona on, että poiminnan tietojen kirjaamisen sijaan poiminta rekisteröidään. Tämä rekisteröinti ei kirjaa kulutusta, vaan se vain määrittää nimikkeet saataville kirjaamista varten. Varastopäällikkönä voit järjestää poimintatiedot poimintatyökirjan avulla ennen yksittäisten fyysisen varastoinnin poimintaohjeiden luontia

## <a name="see-also"></a>Katso myös

[Projektinhallinta](projects-manage-projects.md)  
[Video: Projektin luonti Dynamics 365 Business Centralissa](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]