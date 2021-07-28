---
title: Tietoja standardikustannuksen laskemisesta
description: Vakiokustannusjärjestelmässä varaston yksikkökustannus määritetään kohtuullisten aiempien tai odotettujen kustannusten perusteella.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 3ef1aac08230477afefafee6afcaf05ac9c9cfff
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/30/2021
ms.locfileid: "6323200"
---
# <a name="about-calculating-standard-cost"></a>Tietoja standardikustannuksen laskemisesta
Useat tuotantoyritykset valitsevat vakiokustannusten perustaksi arvostuksen. Tämä pätee myös yrityksiin, jotka tekevät vain kevyitä tuotantotöitä, kuten kokoonpanoa ja varustelua. Vakiokustannusjärjestelmässä varastoyksikkö määritetään kohtuullisten aiempien tai odotettujen kustannusten perusteella. Tällöin aiempien ja arvioitujen kustannusten tarkastelut muodostavat vakiokustannusten perustan. Nämä kustannukset jäädytetään, kunnes niiden muutosta koskeva päätös on tehty. Tuotteen todelliset tuotantokustannukset eroavat väistämättä arvioiduista vakiokustannuksista. Todellisia kustannuksia vertaillaan tietyn nimikkeen vakiokustannuksiin johdon hallintotarkoituksia varten, ja *erot* tunnistetaan ja analysoidaan.  

Vakiokustannuksia voidaan ylläpitää nimikkeiden osalta, jotka täydennetään ostojen, kokoonpanon ja tuotannon kautta. Kunkin täydennysmenetelmän vakiokustannukset voivat sisältää seuraavat elementit.  

|Täydennysjärjestelmä|Vakiokustannuksen elementit|  
|--------------------------|----------------------------|  
|**Osto**|Välittömät materiaalikustannukset ja yleismateriaalikustannukset, jos tarpeen.|  
|**Kokoonpano**|Välittömät materiaalikustannukset, välittömät tai kiinteän työn kustannukset ja yleiskustannukset.|  
|**Tuotantotilaus**|Välittömät materiaalikustannukset, työkustannukset, alihankintakustannukset ja yleiskustannukset.|  

## <a name="setting-up-standard-costs"></a>Vakiokustannusten määrittäminen  
Vakiokustannukset on muodostettava jokaiselle kustannuselementille, koska kokoonpannun tai tuotetun nimikkeen vakiokustannukset koostuvat useista kustannuselementeistä, joita ovat materiaalien, kapasiteetin (työvoima) ja alihankkijan kustannukset (välittömät ja yleiset).  

Nimikkeitä käsittelevällä yrityksellä, joka käyttää vakiokustannuksia, on kaksinkertainen kirjanpitotehtävä:  

-   valmiin nimikkeen vakiokustannusten arvioiminen ja määrittäminen nimikekorttiin.  
-   tuotannon kustannuselementtien todellisten kustannusten tallentaminen ja kohdistaminen sekä erojen asianmukainen selvitys.  

Kaikki komponentin kustannukset on laskettava yhteen, jotta valmiin nimikkeen välittömät kustannukset voidaan määrittää. Koottu tai valmistettu nimike voi sisältää osakokoonpanoja, jotka voivat myös sisältää useita osia.  

Seuraavat keskeiset kustannukset muodostavat valmiiksi käsitellyn nimikkeen välittömän kokonaiskustannuksen:  

-   Materiaalikulut  
-   Kapasiteettikustannus  
-   Alihankintakustannukset ainoastaan tuotetuille nimikkeille.  

### <a name="material-costs"></a>Materiaalikustannukset  
 Materiaalikustannuksia ovat osakokoonpanoihin ja ostettuun raaka-aineeseen liittyvät kustannukset. Materiaaliyksikön kustannukset voivat koostua välittömistä ja välillisistä kustannuselementeistä.  

-   Välittömät materiaalikustannukset edustavat ostettujen raaka-aineiden tai osakokoonpanon käsittelykustannusten laskutettua summaa.  
-   Välilliset kustannukset (tai *yleiskustannukset*) voivat koostua esimerkiksi tuotetun valmiin nimikkeen varastointikustannuksista.  

Ostettujen nimikkeiden materiaalikustannusten määrittäminen välillisiin ja välittömiin kustannuksiin riippuu kyseiselle nimikkeelle valitusta arvostusmenetelmästä. Kummankin arvostusmenetelmän kustannustiedot määritetään nimikkeen kortissa. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

Hukkatavaran kustannus tuotannossa on kokonaismateriaalikustannusten laskennassa huomioon otettava lisätekijä. Kun tietty määrä raaka-ainetta hukataan nimikkeen kokoonpanossa tai tuotannossa, tämän nimikkeen tuotannossa tarvittavien komponenttien määrä yleensä kasvaa. Se taas lisää päänimikkeen tuotannossa tarvittavien komponenttien materiaalikustannuksia. Materiaalien hukkakustannus voidaan määrittää joko tuotannon tuoterakenteessa tai reitityksessä.  

Tuotetun nimikkeen materiaalikustannukset voidaan esittää kahdella vakiokustannusten laskentaperustetta vastaavalla tavalla:  

|Kustannusten laskentaperuste|Materiaalikustannusten laskenta|  
|----------------------------|-------------------------------|  
|Yksitasoinen|Tuotettu nimike vastaa kyseisen nimikkeen tuotannon tuotantorakenteen kaikkien ostettujen tai osakokoonpantujen nimikkeiden kokonaiskustannusta.|  
|Vyörytystaso tai monitasoinen|Tuotettu nimike on kyseisen nimikkeen tuotantorakenteen kaikkien osakokoonpanojen materiaalikustannusten ja kyseisen nimikkeen tuotannon tuotantorakenteen kaikkien ostettujen nimikkeiden summa.|  

### <a name="capacity-costs"></a>Kapasiteettikustannukset  
Kapasiteetin kustannuksia ovat kustannukset, jotka liittyvät sisäisen työn ja koneen kustannuksiin. Määritä nämä kustannukset kullekin resurssille (kokoonpanon hallinnassa) ja työlle tai kuormitusryhmälle reitityksessä (tuotannossa). Kuten materiaalien kanssa, voit tunnistaa kapasiteettikustannusten väliliset ja välittömät elementit. Esimerkiksi tuotantosolun välitön kustannukset voivat olla tietyn toiminnon suorituksesta muodostuvat tuotantokustannukset. Tuotantosolun epäsuoriin kustannuksiin voi kuulua joitain yleisiä tehdaskuluja, kuten valaistus, lämmitys jne. Kuten materiaalikustannusten kanssa, voit ilmaista kapasiteetin yleiskustannukset välillisenä kustannusprosenttina tai kiinteänä yleiskustannuksena.  

Kapasiteettikustannusten asetukset koostuvat seuraavista elementeistä:  

-   Resurssin välilliset ja välittömät yksikkökustannukset.  
-   Kiinteä tai suora resurssikäyttötyyppi.  

Tuotettujen nimikkeiden kapasiteettikustannusten asetukset koostuvat seuraavista elementeistä:  

-   Kuormitusryhmän tai tuotantosolun välittömät ja välilliset yksikkökustannukset.  
-   Ajan ja erän koon asetukset.  

Tuotantoyrityksen on muodostettava koneen ja tuotantosolujen suorituksessa tarvittavat vakioaikapalkat kapasiteetin vakiokustannusten laskentaa varten. Toiminnon suorituksen kokonaisaika koostuu yleensä asennus- ja suoritusajasta sekä odotus- ja siirtoajasta.  

Jokaiselle koneelle/tuotantosolulle määritetään kunkin aikatyypin kustannukset yksittäistä reititystä kohti.  

> [!NOTE]  
>  On tärkeää huomata, että ajoajan kustannukset kohdistetaan jokaiseen tuotettavaan nimikeyksikköön ja asetuskustannukset kohdistetaan jokaiseen erään. Sen vuoksi kunkin toiminnon reitityksen asetusajan kustannukset on jaettava eräkoon mukaan. Eräkoko määritetään nimikekortin **Tilaaminen**-pikavälilehden kentässä.  

Jos haluat määrittää määritysajan reitityksen suunnittelulle mutta et sisällyttää tätä kulua vakiokustannusten laskentaan, tyhjennä **Tuotannon asetukset** -sivun **Kust. sisältävät asetuksen** -kentän valinta.  

Yksitasoisena tämä on valmiin tuotantonimikkeen tuotannossa tarvittava työkustannus. Se määritetään tuotantonimikkeen reitityksessä. Monitasoisena tämä on päänimikkeen tuoterakenteeseen sisällytettyjen yksittäisten tuotettujen nimikkeiden kapasiteettikustannus.  

### <a name="subcontractor-costs"></a>Alihankkijan kustannukset  
Alihankkijan kustannuksia ovat yrityksen ulkopuolisille toimittajille tai alihankkijoille toimittamiin palveluihin liittyvät kustannukset. Alihankkijan kustannukset voivat koostua materiaali- ja kapasiteettikustannusten tavoin sekä välittömistä että yleisistä kustannuksista. Välittömiä alihankkijan kustannuksia ovat tuotettujen palveluiden todelliset yksikkökohtaiset kulut. Yleiset alihankkijan kustannukset esimerkiksi voivat olla esimerkiksi alihankintatilaukseen liittyvän yrityksen aiheuttamat kuljetus- ja/tai käsittelykustannukset.  

Koska alihankinta on ulkoistettua kapasiteettia, alihankintapalveluiden kustannukset (välittömät ja välilliset) määritetään alihankintatoimintoa edustavalle toimintosolukortille.  

## <a name="updating-standard-costs"></a>Vakiokustannusten päivittäminen  
Päivitä tai laske kokoonpanon nimikkeiden standardikustannukset käyttäen funktiota nimikekortista.  

Vakiokustannusten päivittäminen tai laskeminen koostuu yleensä seuraavista tehtävistä:  

1.  Päivitetään kustannuksia osa- ja kapasiteettitasolla. Lisätietoja on **Ehdota nimikkeen vakiokust.**- ja **Ehdota kapasiteetin vakiokustannusta** -eräajoissa.  
2.  Nimikkeiden kokoonpanon ja tuotannon kokonaiskustannusten laskeminen konsolidoimalla ja vyöryttämällä osa- ja kapasiteettikustannukset. Lisätietoja on kohdassa [Kokoonpanon nimikkeen vakiokustannusten laskeminen](inventory-how-work-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  Otetaan edellisten eräajojen aikana syötetyt vakiokustannukset käyttöön. Vakiokustannukset eivät tule voimaan, ennen kuin ne on otettu käyttöön. Lisätietoja on **Ota käyttöön vakiokustannusten muutokset** -eräajossa.  
4.  Otetaan muutokset käyttöön nimikkeen kortin **Yksikkökustannus**-kentän päivittämistä ja varaston uudelleenarvostuksen suorittamista varten. Lisätietoja on kohdassa [Varaston uudelleenarvostus](inventory-how-revalue-inventory.md).

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: arvostusmenetelmät](design-details-costing-methods.md)   
 [Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)   
 [Vakiokustannusten päivittäminen](finance-how-to-update-standard-costs.md)   
 [Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]