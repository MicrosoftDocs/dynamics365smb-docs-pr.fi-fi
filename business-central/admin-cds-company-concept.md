---
title: Yrityksen ja liiketoimintayksikön yhdistämismääritys | Microsoft Docs
description: Yritykset ovat sekä oikeushenkilö- että liiketoimintarakenteita. Niiden avulla suojataan ja visualisoidaan liiketoimintatiedot.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: CDS, Common Data Service, integration, sync
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 4f8e5959098e01cd08134a37ae706aa852d88729
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911654"
---
# <a name="data-ownership-models"></a>Tietojen omistusmallit
[!INCLUDE[d365fin](includes/cds_long_md.md)] edellyttää, että määrität tallennettavien tietojen omistajan. Lisätietoja on Power Apps -dokumentaation kohdassa [Entiteetin omistus](https://docs.microsoft.com/powerapps/maker/common-data-service/types-of-entities#entity-ownership). Kun määrität [!INCLUDE[d365fin](includes/cds_long_md.md)]- ja [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen välisen integroinnin, sinun on valittava synkronoiduille tietueille toinen seuraavista kahdesta omistusmallista:

* Tiimi 
* Henkilö (käyttäjä)

Näille tietueille suoritettavia toimintoja voidaan hallita käyttäjätasolla. Lisätietoja on kohdassa [Käyttäjän ja tiimin entiteetit](https://docs.microsoft.com/powerapps/developer/common-data-service/user-team-entities). Suosittelemme tiimin omistuksen mallia, koska sen avulla on helppo hallita useiden henkilöiden omistusta.

## <a name="team-ownership"></a>Tiimin omistus
[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa yritys on oikeushenkilö- ja yritysentiteetti, jonka avulla liiketoimintatiedot voidaan suojata ja visualisoida. Käyttäjät työskentelevät aina yrityksen kontekstissa. Lähimpänä tätä konseptia [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksessa on liiketoimintaentiteetti. Se ei sisällä oikeushenkilö- tai yritysviittauksia.

Koska liiketoimintayksiköissä ei ole oikeushenkilö- tai yritysviittauksia, et voi pakottaa tietojen synkronointia yrityksen ja liiketoimintayksikön välillä yksi yhteen (1:1) -yhdistämismäärityksen avulla yhteen tai kahteen suuntaan. Jotta synkronointi olisi mahdollista, [!INCLUDE[d365fin](includes/d365fin_md.md)] -yrityksen synkronoinnin käyttöönoton aikana tapahtuu seuraavaa [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksessa:

* Luodaan yritysentiteetti, joka vastaa yritysentiteettiä [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa. Yrityksen nimen jälkiliite on BC Yritys ID. Esimerkiksi Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Luodaan oletusliiketoimintayksikkö, jolla on sama nimi kuin yrityksellä. Esimerkiksi Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Luodaan erillinen omistajatiimi, jolla on sama nimi kuin yrityksellä, ja liitetään se liiketoimintayksikköön. Tiimin nimen alkuliite on BCI -. Esimerkiksi BCI - Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksessa luodut ja sen kanssa synkronoidut tietueet liitetään BCI - omistaja -tiimiin, joka on linkitetty liiketoimintayksikköön.

> [!NOTE]
> Jos nimeät yrityksen uudelleen kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)], automaattisesti luodut yrityksen, liiketoiminnan ja tiimin nimet kohteessa [!INCLUDE[d365fin](includes/cds_long_md.md)] eivät päivity. Koska integroinnissa käytetään vain yritystunnusta, se ei vaikuta synkronointiin. Jos haluat, että nimet vastaavat toisiaan, sinun täytyy päivittää yritys, liiketoimintayksikkö ja tiimi kohteessa [!INCLUDE[d365fin](includes/cds_long_md.md)].

Seuraavassa kuvassa on esimerkki [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksen näiden tietojen asetuksesta.

![Pääliiketoimintayksikkö on yläosassa, tiimit keskellä ja yritykset alaosassa.](media/cds_bu_team_company.png)

Tässä määrityksessä Cronus US -yritykseen liittyvät tietueet omistaa tiimi, joka on linkitetty Cronus US -yrityksen <ID> liiketoimintayksikköön [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksessa. Käyttäjät, jotka voivat käyttää kyseistä liiketoimintayksikköä [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksen liiketoimintayksikön tason näkyvyydeksi määritetyn käyttöoikeusroolin avulla, näkevät nämä tietueet. Seuraavassa esimerkissä näytetään, miten näiden tietueiden käyttöoikeus saadaan tiimien avulla.

* Myyntipäällikön rooli on liitetty Cronus US -myyntitiimin jäsenille.
* Myyntipäällikön roolin omaavat käyttäjät voivat käyttää saman liiketoimintayksikön jäsenten tilitietueita.
* Cronus US -myyntitiimi on linkitetty aiemmin mainittuun Cronus US -liiketoimintayksikköön. Cronus US -myyntitiimin jäsenet voivat nähdä kaikki Cronus US <ID> -käyttäjän omistamat tilit, jos käyttäjä on peräisin Cronus US -yritysentiteetistä [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa.

Kuitenkin 1:1-yhdistämismääritys liiketoimintayksikön, yrityksen ja tiimin välillä on vasta aloituskohta seuraavan kuvan mukaisesti.

![Käyttöoikeusrooli ohjaa tietojen näkyvyyttä.](media/cds_bu_team_company_2.png)

Tässä esimerkissä luodaan uusi EUR (Eurooppa) -pääliiketoimintayksikkö [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksessa sekä Cronus DE (Saksa)- että Cronus ES (Espanja) -yritykselle. EUR-liiketoimintayksikköä ei ole liitetty synkronointiin. Se voi kuitenkin antaa EUR-myyntitiimeille tilin tietojen käyttöoikeuden sekä Cronus DE- että Cronus ES -yrityksessä määrittämällä tietojen näkyvyydeksi **Pää-/aliliiketoimintayksikkö** liittyvässä käyttöoikeusroolissa [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksessa.

Synkronointi määrittää tietueet omistavan tiimin. **Omistava oletustiimi** -kenttä BCI - <ID> -tietueessa ohjaa tätä. Kun BCI - <ID> -tietue on otettu käyttöön synkronointia varten, liittyvä liiketoimintayksikkö ja omistava tiimi luodaan automaattisesti (jos ne eivät vielä ole olemassa) ja **Omistava oletustiimi** -kenttä määritetään. Kun entiteetin synkronointi on otettu käyttöön, järjestelmänvalvojat voivat muuttaa omistavaa tiimiä, mutta tiimi on aina määritettävä.

> [!NOTE]
> Tietueet ovat vain luku -tilassa yrityksen lisäämisen ja tallentamisen jälkeen. Varmista siis, että valitset oikean yrityksen.

## <a name="choosing-a-different-business-unit"></a>Toisen liiketoimintayksikön valitseminen
Voit muuttaa liiketoimintayksikön valintaa, jos käytät ryhmien omistajuus -mallia. Jos käytät henkilön omistajuus -mallia, oletusliiketoimintayksikkö valitaan aina. 

Jos valitset toisen liiketoimintayksikön, esimerkiksi aiemmin [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksessa luodun yksikön, sen alkuperäinen nimi säilytetään. Tämä tarkoittaa sitä, että nimen alkuun ei tule yritystunnusta. Luodaan tiimi, joka käyttää nimeämiskäytäntöjä.

Kun muutat liiketoimintayksikköä, voit valita vain ne liiketoimintayksiköt, jotka ovat yhden tason pääliiketoimintayksikön alapuolella.

## <a name="person-ownership"></a>Henkilön omistus
Jos valitset henkilön omistusmallin, määritä kaikki myyjät, jotka omistavat uusia tietueita. Liiketoimintayksikkö ja tiimi luodaan [Tiimin omistajuus](admin-cds-company-concept.md#team-ownership) -osan mukaisesti.

Oletusliiketoimintayksikköä käytetään, kun henkilön omistajuus -malli valitaan, eikä toista liiketoimintayksikköä voi valita. Oletusliiketoimintayksikköön liitetty ryhmä omistaa tietueita yleisille entiteeteille, kuten tuoteyksikölle, jotka eivät liity tiettyihin myyjiin.

Kun lisäät myyjiä [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä [!INCLUDE[d365fin](includes/cds_long_md.md)] -ohjelman käyttäjiin, [!INCLUDE[d365fin](includes/d365fin_md.md)] lisää käyttäjän oletusryhmään [!INCLUDE[d365fin](includes/cds_long_md.md)] -ohjelmaan. Voit varmistaa, että käyttäjät lisätään tarkastelemalla **Käyttäjät - Common Data Service** -sivun **Oletusryhmänjäsen**-saraketta . Jos käyttäjää ei lisätä, voit lisätä ne manuaalisesti käyttämällä **Lisää sidotut käyttäjät tiimiin** -toimintoa. Lisätietoja on kohdassa [Business Centralin tietojen synkronointi Common Data Servicen avulla](admin-synchronizing-business-central-and-sales.md).

## <a name="see-also"></a>Katso myös
[Tietoja [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-common-data-service.md) -sovelluksesta