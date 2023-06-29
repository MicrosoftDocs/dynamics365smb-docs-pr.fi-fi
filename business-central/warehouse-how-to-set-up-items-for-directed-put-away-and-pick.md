---
title: Ohjatun hyllytyksen ja poiminnan määrittäminen
description: Ohjattua hyllytys ja poimintaa antaa toiminnot tehokkaaseen varastointiin.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 11/07/2022
ms.author: bholtorf
---
# <a name="set-up-items-and-locations-for-directed-put-away-and-pick"></a><a name="set-up-items-and-locations-for-directed-put-away-and-pick"></a>Nimikkeiden ja sijaintien määrittäminen ohjattua hyllytystä ja poimintaa varten

Kun otat ohjatun hyllytyksen ja poiminnan käyttöön fyysisen varastoinnin sijainnissa, voit tehostaa fyysistä varastointia uusien toimintojen avulla. Jotta hyötyisit mahdollisimman paljon näistä toiminnoista, anna ohjelmalle nimikkeistä lisätietoja, joiden avulla ohjelma voi laskea tehokkaimman fyysisen varastoinnin aktiviteettien suoritustavan. 

## <a name="to-set-up-an-item-for-directed-put-away-and-pick"></a><a name="to-set-up-an-item-for-directed-put-away-and-pick"></a>Nimikkeen määritys ohjattua hyllytystä ja poimintaa varten

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2. Avaa ohjattua hyllytystä ja poimintaa varten määritettävän nimikkeen kortti.
3. Määritä nimikkeen kortin **F. varastointi** -pikavälilehden kenttien avulla, miten nimikettä käsitellään fyysisessä varastoinnissa.  
4. Valitse **Mittayksiköt**-toiminto.
5. Määritä **Mittayksiköt**-sivulla mittayksiköt, joita nimiketapahtumissa voidaan käyttää määrittämällä nimikkeen mittayksikön korkeus, leveys, pituus, tilavuus ja paino.
6. Valitse **Varastopaikan sisältö** -toiminto.
7. Määritä **Varastopaikan sisältö** -sivulla sijainti ja varastopaikka, johon nimike on liitettävä. **Oletusarvo**-kenttä ei ole käytössä, kun sijainnissa on käytössä ohjattu hyllytys ja poiminta.  

## <a name="to-start-using-directed-put-away-and-pick"></a><a name="to-start-using-directed-put-away-and-pick"></a>Ohjatun hyllytyksen ja poiminnan käytön aloittaminen

Ohjatun hyllytyksen ja poiminnan avulla voit käyttää laajennettuja varastomääritystoimintoja, jotka tehostavat varastointia ja parantavat tietojen luotettavuutta. Jotta voisit käyttää tätä toimintoa, tietyt fyysisen varastoinnin sijainnin parametrit on määritettävä ensin.  

Voidaksesi käyttää ohjattua hyllytystä ja poimintaa, ota käyttöön sijaintikortin toiminnot seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
2. Valitse sijainti, jossa haluat käyttää ohjattua hyllytystä ja poimintaa, ja valitse sitten **Muokkaa**-toiminto.  
3. Valitse **F. varastointi** -pikavälilehdessä **Ohjattu hyllytys ja poiminta** -valintaruutu.  

Sijaintikorttiin ei tarvitse vielä täyttää muita kenttiä, vaan sen voi tehdä vasta myöhemmin asetusprosessissa.  

> [!NOTE]  
> Varastopaikkoja ei voi ottaa käyttöön fyysisessä varastoinnissa, jos sijainnissa on avoimia nimiketapahtumia.  

Seuraava työvaihe on käsiteltävien varastopaikkojen tyypin määrittäminen. Lisätietoja on kohdassa [Varastopaikkojen määrittäminen](warehouse-how-to-set-up-bin-types.md). Varastopaikan tyyppi määrittää, miten ohjelma käyttää tiettyä varastopaikkaa käsitellessään nimikkeiden virtaa varaston läpi. Varastopaikan tyypin voi määrittää sekä alueelle että varastopaikalle.  

Voit myös määrittää fyysisen varastoinnin luokkakoodeja, jos fyysisessä varastossa on nimikkeitä, jotka edellyttävät tietynlaisia varastointiolosuhteita. Fyysisen varastoinnin luokkakoodien avulla ehdotetaan nimikkeen sijoitusta varastopaikkoihin. Määrität varaston luokkakoodit tuoteryhmille, jotka tämän jälkeen määritetään nimikkeille ja varastointiyksiköille tai alueille ja varastopaikoille, jotka täyttävät tarvittavat, varastoluokkakoodien varastointiolosuhteet.  

Seuraavaksi voidaan tarvittaessa määrittää vyöhykkeet. Käyttämällä alueita voidaan vähentää varastopaikkoja määritettäessä täytettävien kenttien määrää, koska alueille luodut varastopaikat perivät useita ominaisuuksia alueelta. Alueet voivat myös helpottaa uusien tai väliaikaisten työntekijöiden toimia fyysisessä varastoinnissa. Huomaa, että varastopaikat ohjaavat työnkulkua, ja siksi on mahdollista käytää varastopaikkoja ja vain yhtä aluetta.  

## <a name="to-set-up-a-zone-in-your-warehouse"></a><a name="to-set-up-a-zone-in-your-warehouse"></a>Alueen määrittäminen fyysiseen varastoon

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
2. Valitse sijainti, johon haluat määrittää alueen, ja avaa sijaintikortti. Valitse sitten **Alueet**-toiminto.  
3. Täytä **Alueet**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Kun muutat jotakin alueen parametria, kaikki tämän jälkeen alueella luodut varastopaikat saavat uuden ominaisuuden, mutta alkuperäisiä varastopaikkoja ei muuteta.  

> [!NOTE]  
> Vaikka et haluaisi käyttää alueita, tarvitset kuitenkin yhden alueen, joka on määrittämätön koodia lukuun ottamatta.  

Seuraava määritysvaihe on varastopaikkojen määritys. Lisätietoja on kohdassa [Sijaintien määrittäminen varastopaikkojen käyttämistä varten](warehouse-how-to-set-up-locations-to-use-bins.md).  

Lisäksi on luotava hyllytysmallit ja laskentajaksot. Lisätietoja on kohdassa [Hyllytysmallien määrittäminen](warehouse-how-to-set-up-put-away-templates.md).  

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
