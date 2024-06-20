---
title: Tietojen omistusmallit synkronointia varten
description: Yritykset ovat sekä oikeushenkilö- että liiketoimintarakenteita. Niiden avulla suojataan ja visualisoidaan liiketoimintatiedot.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'CDS, Dataverse, integration, sync'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Tietojen omistusmallit synkronointia varten

[!INCLUDE[prod_short](includes/cds_long_md.md)] edellyttää, että määrität tallennettavien tietojen omistajan. Lisätietoja on Power Apps -dokumentaation kohdassa [Taulukkotyypit](/powerapps/maker/data-platform/types-of-entities). Kun määrität [!INCLUDE[prod_short](includes/cds_long_md.md)]- ja [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen välisen integroinnin, sinun on valittava synkronoiduille tietueille omistajaksi **käyttäjä tai ryhmä**. Näille tietueille suoritettavia toimintoja voidaan hallita käyttäjätasolla. <!--We recommend the Team ownership model because it makes it easier to manage ownership for multiple people.NO LONGER TRUE IN DATAVERSE-->

## Tiimin omistus
[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa yritys on oikeushenkilö- ja yritystaulukko, jonka avulla liiketoimintatiedot voidaan suojata ja visualisoida. Käyttäjät työskentelevät aina yrityksen kontekstissa. Lähimpänä tätä konseptia [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksessa on liiketoimintataulukko. Se ei sisällä oikeushenkilö- tai yritysviittauksia.

Koska liiketoimintayksiköissä ei ole oikeushenkilö- tai yritysviittauksia, et voi pakottaa tietojen synkronointia yrityksen ja liiketoimintayksikön välillä yksi yhteen (1:1) -yhdistämismäärityksen avulla yhteen tai kahteen suuntaan. Jotta synkronointi olisi mahdollista, [!INCLUDE[prod_short](includes/prod_short.md)] -yrityksen synkronoinnin käyttöönoton aikana tapahtuu seuraavaa [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksessa:

* Luodaan yritystaulukko, joka vastaa yritystaulukkoa [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa. Yrityksen nimen jälkiliite on BC Yritys ID. Esimerkiksi Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Luodaan oletusliiketoimintayksikkö, jolla on sama nimi kuin yrityksellä. Esimerkiksi Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Luodaan erillinen omistajatiimi, jolla on sama nimi kuin yrityksellä, ja liitetään se liiketoimintayksikköön. Tiimin nimen alkuliite on BCI -. Esimerkiksi BCI - Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksessa luodut ja sen kanssa synkronoidut tietueet liitetään BCI - omistaja -tiimiin, joka on linkitetty liiketoimintayksikköön.

> [!NOTE]
> Jos nimeät yrityksen uudelleen kohteessa [!INCLUDE[prod_short](includes/prod_short.md)], automaattisesti luodut yrityksen, liiketoiminnan ja tiimin nimet kohteessa [!INCLUDE[prod_short](includes/cds_long_md.md)] eivät päivity. Koska integroinnissa käytetään vain yritystunnusta, se ei vaikuta synkronointiin. Jos haluat, että nimet vastaavat toisiaan, sinun täytyy päivittää yritys, liiketoimintayksikkö ja tiimi kohteessa [!INCLUDE[prod_short](includes/cds_long_md.md)].

Seuraavassa kuvassa on esimerkki [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksen näiden tietojen asetuksesta.

![Pääliiketoimintayksikkö on yläosassa, tiimit keskellä ja yritykset alaosassa.](media/cds_bu_team_company.png)

Tässä määrityksessä Cronus US -yritykseen liittyvät tietueet omistaa tiimi, joka on linkitetty Cronus US -yrityksen liiketoimintayksikköön [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksessa. Käyttäjät, jotka voivat käyttää kyseistä liiketoimintayksikköä [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksen liiketoimintayksikön tason näkyvyydeksi määritetyn käyttöoikeusroolin avulla, näkevät nämä tietueet. Seuraavassa esimerkissä näytetään, miten näiden tietueiden käyttöoikeus saadaan tiimien avulla.

* Myyntipäällikön rooli on liitetty Cronus US -myyntitiimin jäsenille.
* Myyntipäällikön roolin omaavat käyttäjät voivat käyttää saman liiketoimintayksikön jäsenten tilitietueita.
* Cronus US -myyntitiimi on linkitetty aiemmin mainittuun Cronus US -liiketoimintayksikköön. Cronus US -myyntitiimin jäsenet voivat nähdä kaikki Cronus US -käyttäjän omistamat tilit, jos käyttäjä on peräisin Cronus US -yritystaulukosta [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa.

Kuitenkin 1:1-yhdistämismääritys liiketoimintayksikön, yrityksen ja tiimin välillä on vasta aloituskohta seuraavan kuvan mukaisesti.

![Käyttöoikeusrooli ohjaa tietojen näkyvyyttä.](media/cds_bu_team_company_2.png)

Tässä esimerkissä luodaan uusi EUR (Eurooppa) -pääliiketoimintayksikkö [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksessa sekä Cronus DE (Saksa)- että Cronus ES (Espanja) -yritykselle. EUR-liiketoimintayksikköä ei ole liitetty synkronointiin. Se voi kuitenkin antaa EUR-myyntitiimeille tilin tietojen käyttöoikeuden sekä Cronus DE- että Cronus ES -yrityksessä määrittämällä tietojen näkyvyydeksi **Pää-/aliliiketoimintayksikkö** liittyvässä käyttöoikeusroolissa [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksessa.

Synkronointi määrittää tietueet omistavan tiimin. **Omistava oletustiimi** -kenttä BCI -rivillä ohjaa tätä. Kun BCI -tietue on otettu käyttöön synkronointia varten, liittyvä liiketoimintayksikkö ja omistava tiimi luodaan automaattisesti (jos ne eivät vielä ole olemassa) ja **Omistava oletustiimi** -kenttä määritetään. Kun taulukon synkronointi on otettu käyttöön, järjestelmänvalvojat voivat muuttaa omistavaa tiimiä, mutta tiimi on aina määritettävä.

> [!NOTE]
> Tietueet ovat vain luku -tilassa yrityksen lisäämisen ja tallentamisen jälkeen. Varmista siis, että valitset oikean yrityksen.

## Toisen liiketoimintayksikön valitseminen
Voit muuttaa liiketoimintayksikön valintaa, jos käytät ryhmien omistajuus -mallia. Jos käytät henkilön omistajuus -mallia, oletusliiketoimintayksikkö valitaan aina. 

Jos valitset toisen liiketoimintayksikön, esimerkiksi aiemmin [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksessa luodun yksikön, sen alkuperäinen nimi säilytetään. Tämä tarkoittaa sitä, että nimen alkuun ei tule yritystunnusta. Luodaan tiimi, joka käyttää nimeämiskäytäntöjä.

Kun muutat liiketoimintayksikköä, voit valita vain ne liiketoimintayksiköt, jotka ovat yhden tason pääliiketoimintayksikön alapuolella.

## Henkilön omistus
Jos valitset henkilön omistusmallin, määritä kaikki myyjät, jotka omistavat uusia tietueita. Liiketoimintayksikkö ja tiimi luodaan [Tiimin omistajuus](admin-cds-company-concept.md#team-ownership) -osan mukaisesti.

Oletusliiketoimintayksikköä käytetään, kun henkilön omistajuus -malli valitaan, eikä toista liiketoimintayksikköä voi valita. Oletusliiketoimintayksikköön liitetty ryhmä omistaa tietueita yleisille taulukoille, kuten tuotetaulukolle, jotka eivät liity tiettyihin myyjiin.

Kun lisäät myyjiä [!INCLUDE[prod_short](includes/prod_short.md)]:ssä [!INCLUDE[prod_short](includes/cds_long_md.md)] -ohjelman käyttäjiin, [!INCLUDE[prod_short](includes/prod_short.md)] lisää käyttäjän oletusryhmään [!INCLUDE[prod_short](includes/cds_long_md.md)] -ohjelmaan. Voit varmistaa, että käyttäjät lisätään tarkastelemalla **Käyttäjät - Common Data Service** -sivun **Oletusryhmänjäsen**-saraketta. Jos käyttäjää ei lisätä, voit lisätä ne manuaalisesti käyttämällä **Lisää sidotut käyttäjät tiimiin** -toimintoa. Lisätietoja on kohdassa [Business Centralin tietojen synkronointi Dataversen avulla](admin-synchronizing-business-central-and-sales.md).

## Katso myös
[Tietoja [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-common-data-service.md) -sovelluksesta

[!INCLUDE[footer-include](includes/footer-banner.md)]