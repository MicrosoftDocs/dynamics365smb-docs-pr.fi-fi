---
title: Näytä taulukon tiedot
description: Lue miten voit tarkastella tietokantataulukoiden tietoja Business Centralissa.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 8700
ms.date: 08/23/2022
ms.author: jswymer
---

# <a name="viewing-table-information"></a><a name="viewing-table-information"></a>Näyttää taulukon tiedot

**8700-taulukon tiedot** -sivulla on tietoja kaikkien [!INCLUDE[prod_short](includes/prod_short.md)]-järjestelmän ja -liiketoimintataulukoiden tietueiden lukumäärästä ja siitä, kuinka paljon tietoja kukin taulukko sisältää.

Näistä tiedoista on hyötyä suorituskykyongelmien vianmäärityksessä, sillä se näyttää tietojen koon jakautumisen eri taulukoissa.

## <a name="viewing-table-information-1"></a><a name="viewing-table-information-1"></a>Näyttää taulukon tiedot

Avaa tämä sivu valitsemalla ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Taulukon tiedot** ja valitse sitten vastaava linkki.

Seuraavassa taulukossa kuvataan kunkin taulukon tiedot:

|Sarake|Kuvaus|
|------|-----------|
|Yrityksen nimi|Sen yrityksen nimi, jos sellainen on, johon taulukko kuuluu.|
|Taulukon nimi|Taulukon nimi.|
|Taulukon nro|Taulukon tunnus.|
|Nro tietuetta|Taulukkoon tallennettujen tietueiden kokonaismäärä.|
|Tietueen koko|Tietueiden keskimääräinen koko kilotavuina/tietueessa. Arvo lasketaan seuraavan kaavan avulla: 1024 (koko)/(Tietueiden tietuetta). |
|Koko (kt)|Taulukon viemän tilan kokonaismäärä tietokannasta. Tämä arvo on tietojen koko- ja indeksin koko -kenttien arvojen summa.|
|Tietojen koko (kt)|Miten paljon taulukon tiedot vievät tilaa tietokannasta.|
|Indeksin koko (kt)|Miten paljon taulukon indeksit (avaimet) vievät tilaa tietokannasta.|
|Tiivistys|Pakkauksen, **rivin**, **sivun** tai **ei mitään** -taulukon tyyppi, jota käytetään tietokannan taulukossa. Lisätietoja on kohdassa [Tietojen tiivistys](/sql/relational-databases/data-compression/data-compression?).|

> [!NOTE]
> Jos poistat taulukon tietoja, [!INCLUDE[prod_short](includes/prod_short.md)] aloittaa useita prosesseja taustalla varmistaakseen, että kaikki tiedot siivotaan tietokannassa. Taulukon tiedot -sivun arvot eivät päivity, ennen kuin nämä prosessit on suoritettu loppuun, mikä voi kestää jonkin aikaa. Odotusaikojen määrä voi vaihdella tietokannan koon mukaan.

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Sivujen tarkistaminen](across-inspect-page.md)  
[Suorituskykyartikkelit kehittäjille](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
