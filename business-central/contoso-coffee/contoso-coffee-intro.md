---
title: Johdatus Contoso Coffee -demotietoihin
description: 'Yleiskuvaus tilanteista, joissa Contoso Coffee -demotietojen avulla opit käyttämään Business Centralin ominaisuuksia.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-demo-data"></a><a name="introduction-to-contoso-coffee-demo-data"></a>Johdatus Contoso Coffee -demotietoihin

Contoso Coffee on kuvitteellinen yritys, joka tuottaa kuluttajille ja yrityksille kahvinkeittimiä. **Contoso Coffee** -sovellukset Business Centralille lisäävät demotietoja, joiden avulla voit opetella käyttämään ominaisuuksia Business Centralissa.  


## <a name="set-up-contoso-coffee-data"></a><a name="set-up-contoso-coffee-data"></a>Contoso Coffee -tietojen määrittäminen

Contoson Coffee -esittelytietojen käyttäminen edellyttää, että asennat asianomaiseen yritykseen [!INCLUDE [prod_short](../includes/prod_short.md)] -ratkaisussa kaksi sovellusta:  

- **Contoso Coffee Demo Dataset**  

    Tämä sovellus tarjoaa demotietoja perussovellukselle.  
- **Contoso Coffee Demo Dataset (maatunnus)**  

    Tämä sovellus lisää maakohtaisen sisällön perussovelluksen päälle.

Lisää sovellukset tyhjään yritykseen maksulliseen tilaukseen tai kokeiluversion osana. Voit esimerkiksi luoda uuden yrityksen, jolla ei ole näytetietoja **Luo uusi yritys** -asennustoiminnon avulla, jonka voit avata **Yritykset**-luettelosta. Lisää sitten sovellukset [Marketplacesta](../ui-extensions-install-uninstall.md#install), jos niitä ei ole vielä **Laajennusten hallinta** -sivulla.  

Sen jälkeen tulisi täyttää:
 - [Tuotannon asetusten](manufacturing/contoso-coffee-manufacturing-intro.md) laatiminen [tuotantoskenaarioiden](#manufacturing-scenarios) käyttöä varten
 - [Varastoinnin asetusten](warehousing/contoso-coffee-warehousing-intro.md) laatiminen [varastoinnin skenaarioiden](#warehousing-scenarios) käyttöä varten

## <a name="manufacturing-scenarios"></a><a name="manufacturing-scenarios"></a>Tuotantoskenaariot

Contoso Coffee -esittelytiedot tukevat tällä hetkellä seuraavia testi- ja harjoittelutuotantoskenaarioita:

1. [Uuden tuotannon tuoterakenteen ja tuoterakenneversion luominen](manufacturing/create-new-production-bom-version.md)  
2. [Uuden reitityksen luominen](manufacturing/create-new-routing.md)  
3. [Luo sitovasti suunniteltu tuotantotilaus muuta sitä](manufacturing/create-firm-planned-production-order-change.md)  
4. [Yhdistä automaattinen ja manuaalinen materiaalinotto](manufacturing/combine-automatic-manual-flushing.md)  
5. [Käytä tilauksen suunnittelua tarjonnan luomiseksi ja varaamiseksi](manufacturing/order-planning-create-reserve-supply.md)  
6. [Alihankintatoiminnon määrittäminen ja käsitteleminen](manufacturing/set-up-process-subcontracting-operation.md)  
7. [Määritä uusi kapasiteetti](manufacturing/set-up-new-capacity.md)  
8. [Nimikevarianttien, joille on määritetty eri tuoterakenteet, kysyntäennuste](manufacturing/variants.md)  

Lue kunkin skenaarion vaiheet asianomaisessa artikkelissa.  

> [!IMPORTANT]
> Tuotannon vaihekuvaukset edellyttävät, että käyttäjäkokemukseksi on asetettu *Premium* **Yritystiedot**-sivulla.

## <a name="warehousing-scenarios"></a><a name="warehousing-scenarios"></a>Varastointiskenaariot

Contoso Coffee -esittelytiedot tukevat tällä hetkellä seuraavia testi- ja harjoitteluvarastointiskenaarioita:

1.  Määrittää oletusvarastopaikat, vastaanoton ja hyllytyksen sekä varaston hyllytyksen, poiminnan ja toimituksen varaston poiminnan kanssa tilausjärjestyksessä [Saapuvien ja lähtevien työnkulkujen esittely varaston peruskokoonpanoissa](warehousing/warehouse-basic-flow-putaway-pick.md)
2.  Vastaanota ja hyllytä useampia saapuvia tilauksia kerralla fyysisen varastoinnin vastaanoton avulla, toimita useampia tilauksia kerralla fyysisen varastoinnin toimituksen avulla, poiminta ja fyysisen varastoinnin poiminnat [Tulevan ja lähtevän virran esittely sekavarastokokoonpanoissa](warehousing/warehouse-mixed-flow-receive-pick-ship.md) -toiminnon avulla
3.  Määritä nimikkeen mittayksikön sallitut varastopaikat, käyttäjän laituroiminen vähentämään tavaroiden fyysistä liikkumista, optimoi nimikkeiden sijoittaminen varastopaikkatäydennyksiin, irtotavaran suuri mittayksikkö pienempiin, jakaa poiminta fyysisen varastoinnin työntekijä- ja poimintatyökirjalla [Saapuvien ja lähtevien virtojen esittely edistyneessä varastokokoonpanossa, jossa on ohjattu hyllytys ja poiminta](warehousing/warehouse-directed-flow.md)

Lue kunkin skenaarion vaiheet asianomaisessa artikkelissa.
   
## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Tuotanto](../production-manage-manufacturing.md)  
[Varastointi](../warehouse-manage-warehouse.md)  

