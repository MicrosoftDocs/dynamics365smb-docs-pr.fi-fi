---
title: Asiakkaan asetusarvojen kerääminen | Microsoft Docs
description: Määrityskyselylomakkeen avulla vähennät toteutuksen kuormitusta virtaviivaistamalla uuden yrityksen määritystehtävän. Voit luoda määrityskyselylomakkeen Business Centralissa ja toimittaa sen asiakkaalle Excel (.xlsx)- tai XML-tiedostona.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 77534395d868b1ea82317c32aaed0e70d222e1e1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911478"
---
# <a name="gather-customer-setup-values"></a>Asiakkaan asetusarvojen kerääminen
Määrityskyselylomakkeen avulla vähennät toteutuksen kuormitusta virtaviivaistamalla uuden yrityksen määritystehtävän. Voit luoda määrityskyselylomakkeen [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa ja toimittaa sen asiakkaalle Excel-tai XML-tiedostona.  

Voit muuttaa kyselyn kaikki oletusarvot vastaamaan paremmin asiakkaan tarpeita.  

> [!TIP]  
>  Lisätietoja toimitusten suunnittelun kenttien asetusarvojen määrittämisestä on ohjeaiheessa [Asetukset - parhaat käytännöt: toimitusten suunnittelu](setup-best-practices-supply-planning.md).  

Kun asiakas täyttää kyselyn, voit tuoda tiedoston asiakkaan uuteen [!INCLUDE[d365fin](includes/d365fin_md.md)] -yritykseen. Voit tarkistaa kyselyn vastaukset asiakkaan kanssa, ennen kuin vastaukset otetaan käyttöön yrityksessä.

## <a name="to-create-a-configuration-questionnaire"></a>Määrityskyselylomakkeen luominen
Kyselylomakkeen avulla voit selvittää kokoonpanon laajuuden ja tarpeet. Voit luoda uuden kyselyn tai muokata olemassa olevaa kyselyä lisäämällä uusia kysymyksiä tai kysymysalueita.  

<!-- A configuration questionnaire has the following structure
* The name of the questionnaire itself
* Question Areas that group questions about a similar subject. For example, you might create a question area that focuses on entering company informtion. Typically, configuration questionnaires have many question groups
* Questions that are closed ended, meaning that the customer must choose an answer, and can choose only one. -->

 Voit luoda kyselyjä vain asetustyypin taulukoille. Voit käyttää työkalua esimerkiksi seuraavien sivujen tietojen määrittämisessä:  

-   Yrityksen tiedot  
-   Käyttöomaisuuden asetukset  
-   Pääkirjanpidon asetukset  
-   Varastonhallinnan asetukset  
-   Kokoonpanon asetukset
-   Tuotannon asetukset  
-   Ostojen ja ostovelkojen asetukset  
-   Kontaktienhallinnan asetukset  
-   Huollon asetukset  
-   Myyntien ja saamisten asetukset  
-   Fyys. varastoinnin asetukset  

> [!NOTE]  
>  Jos haluat nähdä asetustaulukoiden täydellisen luettelon, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, kirjoita **Määritys** ja valitse sitten liittyvä linkki. Määritä tietueiden tietojen siirron laajuus käyttämällä siirtotoimintoa. Lisätietoja on ohjeaiheessa [Asiakastietojen siirtäminen](admin-migrate-customer-data.md).  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Konfiguraatiokysely** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto.   
3. Syötä **Konfiguraatiokyselylomakkeen** -sivun **koodi** -kenttään... 
<!--4. In the **Name** field, enter...
5. Choose the **Question Areas** action. .
6. On the **Config. Question Areas** page, in the **Code** field, enter...
  
    > [!Note]  
    > The code is alphanumeric, and must start with a letter of the alphabet.
7. In the Table ID field, choose the table to which to apply the answer to the question. Your selection will determine the fields that are available for the questions, and thereby the answer selections.
  
    > [!Tip]
    > The list of table objects is long. If you know the name of the table, use **Search** in the upper left to find it in the list.
8. In the **Description** field, enter text that indicates the subject of the question group.
9. In the **No.** field, enter a number to define where the question appears in the sequence of questions.
10. In the **Field ID** field, choose the field the the customer's answer will be applied to. You can choose from the fields on the table you chose in the **Table ID** field.
  
    When you choose a field, [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a suggestion in the **Question** field. You can edit the question if needed.
11. To add more questions to the questionnaire, repeat steps seven through 10.

> [!Tip]
> If at some point you change a question, or add a new one, choose the **Update Questions** action to update the list.

-->

3. Valitse **Kysymysalueet**-toiminto. **Kysymysalueet**-sivu avautuu.  
4. Valitse **Uusi**-toiminto. **Määrityskysymysalue**-sivu avautuu.  
5. Anna **Taulukon tunnus** -kenttään sen taulukon tunnus, johon haluat kerätä tiedot. **Taulukon nimi** -kenttä täytetään automaattisesti.  
6. Valitse **Päivitä kysymykset** -toiminto. Taulukon kukin kenttä lisätään kyselyyn kysymysmerkki nimen jälkeen.

Voit muotoilla otsikon uudelleen tehdäksesi selväksi, kuinka kysymykseen vastataan. Jos kentän nimi on esimerkiksi Nimi, voit muokata sen tilaksi Mikä on kohteen <data being collected>nimi? Voit antaa myös ohjeita **Viite**-kentässä. Ohje voi olla esimerkiksi URL-osoite lisätietoja sisältävälle sivulle.  

Voit myös poistaa kysymyksiä, joita et halua sisällyttää kyselyyn.  

> [!NOTE]  
>  **Vastausvaihtoehto** -kentässä kuvataan asianmukaiset datan tyyppi ja muoto vastaukselle. **Vastaus**-kentässä on käyttäjän antamia tietoja.  
>   
>  Tarvittaessa, voit myös määrittää oletusvastaukset **Vastaus**-kentässä. Näitä arvoja käytetään mukautetun asennuksen oletusarvoina. Kuitenkin henkilö täyttää kyselylomakkeen, voit muokata ja päivittää vastaus.  

## <a name="to-complete-the-configuration-questionnaire"></a>Määrityskyselylomakkeen viimeisteleminen
Käytä määrityskyselylomaketta, kun muotoilet ja dokumentoit yksityiskohtaisen keskustelun asiakkaan erityistarpeista. Käytät sitä myös kerätäksesi asetustietoja asiakkaalta määrittääksesi asianmukaiset [!INCLUDE[d365fin](includes/d365fin_md.md)] -asetustaulukot, kuten pääkirjanpidon, varaston ja asiakkaat.  

> [!NOTE]  
>  Voit myös luoda oman määrityskyselylomakkeen, joka vastaa tarpeitasi.  

1. Avaa yritys, jonka kyselyn haluat viimeistellä.
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Konfiguraatiokysely** ja valitse sitten liittyvä linkki.  
3. Valitse yrityksen kysely ja valitse sitten **Vie Exceliin** -toiminto tai vaihtoehtoisesti **Vie XML-muotoon** -toiminto.
4. Pyydä asiakasta täyttämään määrityskyselylomake antamalla vastaukset Excel-työkirjaan. Jokaiselle kysymyslomaketta varten luodulle kysymysalueelle on olemassa työkirjoja.   
5. Tallenna Excel-työkirja *XML-tietona*. Valitse **Tuo XML-tiedostosta** -toiminto ja valitse asiakkaan vastaukset sisältävä .xml-tiedosto.
6. Valitse **Kysymysalueet**-toiminto, jos haluat aloittaa vastausten tarkistamisen ja kohdistamisen määrityskyselylomakkeeseen.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>Täydennä kyselylomake määritystyökirjasta  
Seuraavassa ohjeessa neuvotaan vaihtoehtoinen tapa käyttää määrityskyselylomaketta. Se olettaa, että määritetty määrityspaketti sisältää kyselyjä.  

1. Kun olet tuonut määrityspaketin, avaa määritysten työkirja.  
2. Valitse jokaiselle kysymysalueen sisältävälle taulukolle **Kysymykset**-toiminto. Kyselylomake-sivu avautuu.  
3. Vastaa kysymyksiin ja valitse **Käytä vastauksia** -toiminto.  
4. Sulje kysely valitsemalla **OK**-painike.

## <a name="to-validate-the-configuration-questionnaire"></a>Määrityskyselylomakkeen tarkistaminen
On tärkeää tarkistaa määrityskyselylomake, ennen kuin se otetaan käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)] -muodossa. Se on myös keino varmistaa, että tietojen muotoilu säilyy Excel-tuonnin aikana.  

Yleinen vahvistustehtävä tarkistaa, että tekstijonoja ei kirjoiteta päivämääräkenttiin. Tämä tarkistustoimenpide on tarpeen, koska kyselyn vastausmuotoa ei vahvisteta automaattisesti **Ota vastaukset käyttöön** -toiminnon suorituksen yhteydessä.  

> [!NOTE]  
>  Yleensä määrityskyselylomakkeen asetusten tarkistaminen on manuaalinen prosessi. Alueellisten muotoilujen ristiriidat voidaan kuitenkin tarkistaa. Lisäksi saadaan virheilmoituksia, jos [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietokannan rakenne ei vastaa siirtotietokannan rakennetta.  

1. Valitse **Määrityskyselylomake**-sivulla asianmukainen kyselylomake ja valitse sitten **Kysymysalueet**-toiminto.  
2. Avaa asianmukainen kysymysalue.  
3. Tarkista jokaisen kysymyksen kohdalla, että **Vastaus**-kentän arvo vastaa **Vastausvaihtoehto**-kentässä määritettyä muotoa. Tarkista, että yrityksen osoite on tekstimuodossa.  
4. Jos löydät virheitä, voit tehdä vianmäärityksen ja tehdä korjaukset Excelissä viemällä kyselylomakkeen ja tuomalla sen takaisin. Vaihtoehtoisesti voit korjata virheet suoraan [!INCLUDE[d365fin](includes/d365fin_md.md)]'ssa, kun arvioit vastauksia **Määrityskysymysalue**-sivulla.  
5. Toista nämä vaiheet kullekin kysymysalueelle.  

Kun tarkistus on tehty, tiedot ovat valmiita käyttöön tietokantaa varten.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Määrityskyselylomakkeen vastausten käyttäminen
Kun olet tuonut määrityskyselylomakkeen tiedot ja vahvistanut ne, voit siirtää tai käyttää asetustietoja vastaaviin taulukoihin [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietokannassa.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Konfiguraatiokysely** ja valitse sitten liittyvä linkki. **Määrityskysely**-sivu avautuu.  
2. Valitse määrityskyselylomake luettelosta ja valitse sitten **Muokkaa luetteloa** -toiminto.  
3. Voit käyttää vastauksia jommalla kummalla tavalla.  

- Käytä koko kyselylomaketta valitsemalla **Ota vastaukset käyttöön** -toiminto.  
- Käytä vastauksia vain tietyssä **kysymysalueessa** valitsemalla **Kysymysalueet**-toiminto. Valitse luettelosta **Kysymysalue** ja valitse sitten **Käytä vastauksia** -toiminto.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>Varmista, että vastaukset on kohdistettu onnistuneesti  
1. Tarkista [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman eri toiminta-alueiden asetussivut. Valitse sivun löytääksesi ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä asetussivun nimi ja valitse sitten liittyvä linkki.  
2. Varmista, että kentät on täytetty oikeilla tiedoilla määrityskyselylomakkeen eri kysymysalueilta.  

Olet nyt määrittänyt asetukset asiakkaan yrityksen tietoihin ja sääntöihin.

## <a name="see-also"></a>Katso myös  
[Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)
