---
title: Sijaintien määrittäminen varastopaikkojen käyttämistä varten
description: Varastopaikkat edustavat varastoinnin perusrakennetta ja niitä käytetään ehdotusten tekemiseksi nimikkeiden sijoittelusta ja sijainnista.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="set-up-locations-to-use-bins"></a><a name="set-up-locations-to-use-bins"></a><a name="set-up-locations-to-use-bins"></a>Sijaintien määrittäminen varastopaikkojen käyttämistä varten

Varastopaikkat edustavat varastoinnin perusrakennetta ja niitä käytetään ehdotusten tekemiseksi nimikkeiden sijoittelusta. Kun olet luonut varastopaikat, voit määrittää hyvin tarkkaan sisällön, jonka haluat ohjelman sijoittavan kuhunkin varastopaikkaan, tai varastopaikka voi toimia määrittelemättömänä varastopaikkana, jolla ei ole määritettyä sisältöä.  

A. Jotta voisit käyttää varastopaikan toimintoja sijainnissa, ne on otettava käyttöön **Sijainti**-kortissa Sitten voi suunnitella nimikevirran sijainnissa määrittämällä varastopaikkakoodit määrityskentistä, jotka edustavat eri virtoja.  

> [!NOTE]  
>  Ennen kuin voit määrittää varastopaikkakoodeja sijaintikortissa, on luotava varastopaikkakoodit. Lisätietoja on kohdassa [Varastopaikkojen luominen](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a><a name="to-set-up-a-location-to-use-bins"></a><a name="to-set-up-a-location-to-use-bins"></a>Määritä sijainti käyttääksesi varastopaikkoja

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
2.  Valitse sijainti, jossa haluat käyttää varastopaikkoja.  
3.  Valitse **Muokkaa** -toiminto.  
4.  Valitse **Fyysinen varasto** -pikavälilehdessä **Var.paikka pakollinen** -valintaruutu.  
5.  Jos et käytä ohjattua hyllytystä ja poimintaa sijainnissa, kirjoita **Oletusvar.paikan valinta** -kenttään menetelmä, jolla haluat järjestelmän määrittävän nimikkeelle oletusvarastopaikan.  
6.  Avaa sen sijainnin kortti, johon haluat määrittää varastopaikkoja.
7.  Valitse **Varastopaikat**-pikavälilehdessä varastopaikat, joita haluat käyttää oletuksena vastaanotoille, toimituksille sekä saapuville, lähteville ja avoimille tuotannon varastopaikoille.  
8.  Tähän täyttämäsi varastopaikkakoodit tulevat automaattisesti näkyviin useiden eri fyysisen varastoinnin asiakirjojen otsikoihin (ja sitä myötä myös riveille, ellet muuta niitä). Oletusarvoiset varastopaikat määrittelevät nimikkeiden kaikki alku- ja loppusijoitukset fyysisessä varastossa.  
9.  Jos käytät ohjattua hyllytystä ja poimintaa, valitse varastopaikka fyysisen varastoinnin muutoksille. Varastopaikkakoodi **Muutosvarastopaikan koodi** -kentässä määrittää virtuaalisen varastopaikan, johon tallennetaan eroavaisuudet silloin, kun kirjataan joko varaston nimikepäiväkirjassa havaittuja eroja tai varaston inventoinnin yhteydessä laskettuja eroja.  
10. Täytä **Var.paikkojen periaatteet** -pikavälilehden kentät, jotka ovat olennaisia käytetyn fyysisen varastoinnin kannalta. Tärkeimmät kentät ovat **Var.paikan kapasiteettitapa**, **Salli erottelu** ja **Hyllytysmallin koodi**.  
11. Täytä **F. varastointi** -pikavälilehdessä kentät **Lähtevä f. var. käsittelyaika**, **Saapuva f. var. käsittelyaika** ja  **Peruskalenterin koodi**. Lisätietoja on kohdassa [Peruskalentereiden määrittäminen](across-how-to-assign-base-calendars.md).

## <a name="fill-in-the-consumption-bin"></a><a name="fill-in-the-consumption-bin"></a><a name="fill-in-the-consumption-bin"></a>Kulutuksen varastopaikan täyttäminen

Tämä työnkulkukaavio näyttää, miten tuotantotilauksen osarivien **Varastopaikkakoodi**-kenttä täytetään sijaintiasetusten mukaisesti.

![Varastopaikkojen työnkulkukaavio.](media/binflow.png "BinFlow")  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/configure-bins-location/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
