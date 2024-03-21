---
title: Puuttuvien asetusarvojen käsitteleminen
description: Lisätietoja täyden synkronoinnin epäonnistumisen estämisestä yhdistettyjen kenttien erilaisten asetusten vuoksi. Tämä prosessi edellyttää kehittäjän apua.
author: brentholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.date: 12/12/2023
ms.service: dynamics-365-business-central
---

# Puuttuvien asetusarvojen käsitteleminen
> [!NOTE]
> Vuoden 2022 1. julkaisuaallossa voit luoda omia asetusten yhdistämismäärityksiä. Lisätietoja on kohdassa [Asetusten yhdistämismääritysten mukauttaminen Microsoft Dataversen avulla](/dynamics365/business-central/dev-itpro/administration/administration-custom-option-mapping). Uudet ominaisuudet edellyttävät, että järjestelmänvalvoja ottaa käyttöön asetuksen **Ominaisuuden päivitys: Liitä Dataversen asetusjoukkoihin ilman koodia** **Ominaisuuksien hallinta** - sivulla. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management).

Tämä artikkeli on tarkoitettu tekniselle yleisölle. Siinä kuvatut prosessit edellyttävät kehittäjän apua.

[!INCLUDE[prod_short](includes/cds_long_md.md)] sisältää kolme asetusjoukkokenttää, joissa on Asetus-tyyppiä oleviin [!INCLUDE[prod_short](includes/prod_short.md)] -kenttiin yhdistettävät arvot automaattista synkronointia varten. Synkronoinnin aikana muut kuin yhdistetyt asetukset ohitetaan ja puuttuvat asetukset liitetään liittyvään [!INCLUDE[prod_short](includes/prod_short.md)] -tauluun ja lisätään **Dataverse-asetuksen yhdistäminen** -järjestelmätauluun myöhemmin tapahtuvaa manuaalista käsittelemistä varten. Voit esimerkiksi lisätä puuttuvat asetukset tuotteeseen ja päivittää sitten yhdistämismäärityksen.

**Integrointitaulukon yhdistämismääritys** -sivulla on kolme kenttää, jotka sisältävät vähintään yhden yhdistetyn asetusarvon. Täyden synkronoinnin jälkeen **Dataverse-asetuksen yhdistäminen** -sivu sisältää kolmen kentän muut kuin yhdistetyt asetukset.

|         Tietue             | Asetusarvo | Asetusarvon otsikko |
|----------------------------|--------------|----------------------|
| Maksuehdot: NET30       | 1            | Netto 30               |
| Maksuehdot: 2%10NET30   | 2            | 2 % 10; Netto 30        |
| Maksuehdot: NET45       | 3            | Netto 45               |
| Maksuehdot: NET60       | 4            | Netto 60               |
| Toimitusehto: FOB       | 1            | FOB                  |
| Toimitusehto: NOCHARGE  | 2            | Ei veloitusta            |
| Kuljetusliike: AIRBORNE   | 1            | Lentoposti             |
| Kuljetusliike: DHL        | 2            | DHL                  |
| Kuljetusliike: FEDEX      | 3            | FedEx                |
| Kuljetusliike: UPS        | 4            | UPS                  |
| Kuljetusliike: POSTALMAIL | 5            | Posti          |
| Kuljetusliike: FULLLOAD   | 6            | Täysi kuorma            |
| Kuljetusliike: WILLCALL   | 7            | Noutoasiakas            |

**Dataverse-asetuksen yhdistäminen** -sivu perustuu **CRM-tili**-taulun enum-arvoihin. [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksessa tilitaulukon seuraavat kentät yhdistetään asiakas- ja toimittajatietueiden kenttiin:

- **Osoite 1: Kuljetusehdot**, jonka tietojen tyyppi on Enum ja jonka arvot määritetään seuraavasti:

```
enum 5335 "CDS Shipment Method Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "FOB") { Caption = 'FOB'; }
    value(2; "NoCharge") { Caption = 'No Charge'; }
}
```

- **Osoite 1: Toimitustapa**, jonka tietojen tyyppi on Enum ja jonka arvot määritetään seuraavasti:

```
enum 5336 "CDS Shipping Agent Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Airborne") { Caption = 'Airborne'; }
    value(2; "DHL") { Caption = 'DHL'; }
    value(3; "FedEx") { Caption = 'FedEx'; }
    value(4; "UPS") { Caption = 'UPS'; }
    value(5; "PostalMail") { Caption = 'Postal Mail'; }
    value(6; "FullLoad") { Caption = 'Full Load'; }
    value(7; "WillCall") { Caption = 'Will Call'; }
}
```

- **Maksuehdot**, joiden tietojen tyyppi on Enum ja jonka arvot määritetään seuraavasti:

```
enum 5334 "CDS Payment Terms Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Net30") { Caption = 'Net 30'; }
    value(2; "2%10Net30") { Caption = '2% 10; Net 30'; }
    value(3; "Net45") { Caption = 'Net 45'; }
    value(4; "Net60") { Caption = 'Net 60'; }
}
```

Kaikki [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen yllä mainitut enum-arvot yhdistetään [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksen asetusjoukkoihin.

## [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen asetusjoukkojen laajentaminen
1. Luo uusi AL-laajennus.

2. Lisää Enum-laajennus laajennettaville asetuksille. Varmista, että käytät samaa arvoa. 

```
enumextension 50100 "CDS Payment Terms Code Extension" extends "CDS Payment Terms Code"
{
    value(779800001; "Cash Payment") { Caption = 'Cash Payment'; }
    value(779800002; "Transfer") { Caption = 'Transfer'; }
}
```

> [!IMPORTANT]  
> Sinun on käytettävä [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksen samoja asetuksen tunnusten arvoja kuin [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen enum-arvon laajennuksen yhteydessä. Muussa tapauksessa synkronointi epäonnistuu.

> [!IMPORTANT]  
> Älä käytä merkkiä "," enum-arvoissa ja kuvateksteissä. [!INCLUDE[prod_short](includes/prod_short.md)]in suorituspalvelu ei tue sitä tällä hetkellä.

> [!NOTE]
> Uusien asetusarvojen nimien ja otsikoiden kymmenen ensimmäisen merkin on oltava samoja. Esimerkiksi kaksi asetusta, joiden nimet ovat Siirretään 20 työpäivää ja Siirretään 20 kalenteripäivää, aiheuttavat virheen, koska molemmissa on samat 10 ensimmäistä merkkiä (Siirretään). Anna nimiksi esimerkiksi SIIR20 TP ja SIIR20 KP.

## [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksen asetusten yhdistämisen päivittäminen
Nyt voit luoda uudelleen [!INCLUDE[prod_short](includes/cds_long_md.md)] -asetusten ja [!INCLUDE[prod_short](includes/prod_short.md)] -tietueiden välisen yhdistämismäärityksen.

Valitse **Integrointitaulukon yhdistämismääritys** -sivulla rivi **Maksuehdot**-yhdistämistä varten. Valitse sitten **Synkronoi muokatut tietueet** -toiminto. **Dataverse-asetuksen yhdistäminen** -sivulle päivitetään alla olevat lisätietueet.

|         Tietue                 | Asetusarvo   | Asetusarvon otsikko |
|--------------------------------|----------------|----------------------|
| Maksuehdot: NET30           | 1              | Netto 30               |
| Maksuehdot: 2%10NET30       | 2              | 2 % 10; Netto 30        |
| Maksuehdot: NET45           | 3              | Netto 45               |
| Maksuehdot: NET60           | 4              | Netto 60               | 
| **Maksuehdot: CASH PAYME**  | **779800001**  | **Kassamaksu**     |
| **Maksuehdot: TRANSFER**    | **779800002**  | **Siirto**         |

**Maksuehdot**-taulukko [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa sisältää nyt [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelun asetusten uudet tietueet. Seuraavassa taulukossa uudet asetukset ovat lihavoituna. Kursivoidut rivit edustavat kaikkia asetuksia, jotka voidaan nyt synkronoida. Jäljellä olevat rivit kuvaavat asetuksia, joita ei käytetä. Ne ohitetaan synkronoinnin aikana. Voit poistaa ne tai laajentaa Dataverse-asetukset käyttämällä samoja nimiä.)

| Koodi       | Eräpäivän laskenta | Alennuspvm:n laskenta | Alennus-% | Laske maksualen. hyvityslask. | Kuvaus       |
|------------|----------------------|---------------------------|------------|-------------------------------|-------------------|
| 10 PÄIVÄÄ    | 10P                  |                           | 0.         | EPÄTOSI                         | 10 päivää netto       |
| 14 PÄIVÄÄ    | 14D                  |                           | 0.         | EPÄTOSI                         | 14 päivää netto       |
| 15 PÄIVÄÄ    | 15D                  |                           | 0.         | EPÄTOSI                         | 15 päivää netto       |
| 1M(8D)     | 1M                   | 8D                        | 2.         | EPÄTOSI                         | 1 kuukausi / 2 % 8 päivää |
| 2 PÄIVÄÄ     | 2D                   |                           | 0.         | EPÄTOSI                         | 2 päivää netto        |
| *2%10NET30* |                      |                           | 0.         | EPÄTOSI                         |                   |
| 21 PÄIVÄÄ    | 21D                  |                           | 0.         | EPÄTOSI                         | 21 päivää netto       |
| 30 PÄIVÄÄ    | 30D                  |                           | 0.         | EPÄTOSI                         | 30 päivää netto       |
| 60 PÄIVÄÄ    | 60D                  |                           | 0.         | EPÄTOSI                         | 60 päivää netto       |
| 7 PÄIVÄÄ     | 7D                   |                           | 0.         | EPÄTOSI                         | 7 päivää netto        |
| ***CASH PAYME*** |                      |                           | 0.         | EPÄTOSI                         |                   |
| NK         | NK                   |                           | 0.         | EPÄTOSI                         | Nykyinen kuukausi     |
| JV        | 0D                   |                           | 0.         | EPÄTOSI                         | Jälkivaatimuksella  |
| *NET30*      |                      |                           | 0.         | EPÄTOSI                         |                   |
| *NET45*      |                      |                           | 0.         | EPÄTOSI                         |                   |
| *NET60*      |                      |                           | 0.         | EPÄTOSI                         |                   |
| ***TRANSFER*** |                      |                           | 0.         | EPÄTOSI                         |                   |

## Katso myös
[Synkronoitavien taulujen ja kenttien yhdistäminen](admin-how-to-modify-table-mappings-for-synchronization.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]