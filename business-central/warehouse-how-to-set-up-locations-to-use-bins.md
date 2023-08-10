---
title: Sijaintien määrittäminen varastopaikkojen käyttämistä varten
description: Varastopaikkat edustavat varastoinnin perusrakennetta ja niitä käytetään ehdotusten tekemiseksi nimikkeiden sijoittelusta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
---

# <a name="set-up-locations-to-use-bins"></a>Sijaintien määrittäminen varastopaikkojen käyttämistä varten

Varastopaikat edustavat fyysisen varaston perusrakennetta. Ne voivat ehdottaa, minne nimikkeet kannattaa sijoittaa. Kun olet luonut varastopaikat, määrität niiden sisällön tai annat niiden olla määrittelemättömiä varastopaikkoja, joissa ei ole tiettyä sisältöä.

Jos haluat käyttää varastopaikkatoimintoa sijainnissa, aktivoi **Sijainti**-kortissa **Varastopaikat pakollisia** -valintapainike. Kun olet kytkenyt valintapainikkeen päälle, **Varastopaikan koodi**- ja **Alueen koodi** -kentät ovat käytettävissä seuraavissa asiakirjoissa:

* F. var. vast.ot. otsikko
* F. var. vast.ottorivit
* Fyysisen varaston hyllytysrivit
* F. var. toimitusotsikko
* Fyysisen varaston toimitusrivit
* Fyysisen varaston hyllytysrivit

Sitten voi suunnitella nimikevirran sijainnissa määrittämällä varastopaikkakoodit määrityskentistä, jotka edustavat eri virtoja.  

> [!NOTE]  
> Ennen kuin voit määrittää varastopaikkakoodeja sijainnissa, on luotava varastopaikkakoodit. Lisätietoja on kohdassa [Varastopaikkojen luominen](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a>Määritä sijainti käyttääksesi varastopaikkoja

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
2. Valitse sijainti, jossa haluat käyttää varastopaikkoja.  
3. Valitse **Muokkaa** -toiminto.  
4. Valitse **Fyysinen varasto** -pikavälilehdessä **Var.paikka pakollinen** -valintaruutu.  
5. Jos et käytä ohjattua hyllytystä ja poimintaa sijainnissa, kirjoita **Oletusvar.paikan valinta** -kenttään menetelmä, jolla haluat [!INCLUDE [prod_short](includes/prod_short.md)] määrittävän nimikkeelle oletusvarastopaikan.  
6. Avaa sen sijainnin kortti, johon haluat määrittää varastopaikkoja.
7. Valitse **Varastopaikat**-pikavälilehdessä varastopaikat, joita haluat käyttää oletuksena vastaanotoille, toimituksille sekä saapuville, lähteville ja avoimille tuotannon varastopaikoille.  

    Tähän täyttämäsi varastopaikkakoodit tulevat automaattisesti näkyviin useiden eri fyysisen varastoinnin asiakirjojen otsikoihin (ja sitä myötä myös riveille, ellet muuta niitä). Oletusarvoiset varastopaikat määrittelevät nimikkeiden kaikki alku- ja loppusijoitukset fyysisessä varastossa.  
8. Jos käytät ohjattua hyllytystä ja poimintaa, valitse varastopaikka fyysisen varastoinnin muutoksille. Varastopaikkakoodi **Muutosvarastopaikan koodi** -kentässä määrittää virtuaalisen varastopaikan, johon tallennetaan eroavaisuudet varastossa:

    * Kun kirjataan varaston nimikepäiväkirjassa havaittuja eroja
    * eroja, jotka lasketaan silloin, kun rekisteröidään fyysisen varastoinnin inventointi  
9. Valinnainen: täytä **Var.paikkojen periaatteet** -pikavälilehden kentät. Tärkeimmät kentät ovat **Var.paikan kapasiteettitapa**, **Salli erottelu** ja **Hyllytysmallin koodi**.  
10. Täytä **F. varastointi** -pikavälilehdessä kentät **Lähtevä f. var. käsittelyaika**, **Saapuva f. var. käsittelyaika** ja  **Peruskalenterin koodi**. Saat lisätietoja valitsemalla [Peruskalenterien määrittäminen](across-how-to-assign-base-calendars.md).

## <a name="fill-in-the-consumption-bin"></a>Kulutuksen varastopaikan täyttäminen

Seuraava työnkulkukaavio näyttää, miten tuotantotilauksen osarivien **Varastopaikkakoodi**-kenttä täytetään sijaintiasetusten mukaisesti.

:::image type="content" source="media/binflow.png" alt-text="Varastopaikkakoodi-kenttä tuotantotilauksen osariveillä.":::

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/configure-bins-location/)

## <a name="see-also"></a>Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
