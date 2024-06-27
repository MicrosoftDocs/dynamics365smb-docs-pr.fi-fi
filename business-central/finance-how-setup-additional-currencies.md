---
title: Lisävaluuttojen määrittäminen
description: 'Pääkirjanpito määritetään käyttämään paikallista valuuttaa (PVA) ja toinen valuutta määritetään lisävaluutaksi, jolle määritetään ajantasainen vaihtokurssi.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'multiple currencies, foreign exchange rates'
ms.search.form: '5, 16,118, 483, 495'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Lisäraportointivaluutan määrittäminen

Yritysten toimiessa yhä useammassa maassa tai useammalla alueella niiden on entistä tärkeämpää pystyä tarkistamaan ja raportoimaan taloustiedot useana valuuttana.

> [!NOTE]  
> Jos etsit [!INCLUDE[prod_short](includes/prod_short.md)]issa reaaliajassa tietoa valuuttakurssien (FX) hinnoista tai historiallisista hinnoista, löydät sen nimityksellä valuutta. Tämän artikkelin lisäksi on myös artikkeli [Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md).

Pääkirjanpito määritetään käyttämään paikallista valuuttaa (PVA), mutta voit määrittää sen käyttämään myös toista valuuttaa, jolle määritetään ajantasainen vaihtokurssi. Jos määrität toisen valuutan lisäraportointivaluutaksi (LVA), [!INCLUDE[prod_short](includes/prod_short.md)] tallentaa summat automaattisesti sekä PVA:na että lisäraportointivaluuttana (LVA) kuhunkin KP-tapahtumaan sekä muihin tapahtumiin, kuten ALV-tapahtumiin.

> [!Warning]
> LVA-ominaisuutta ei pidä käyttää rahoituslaskelmakäännösten perustana, ellet ymmärrä sen rajoituksia. Sillä ei voi kääntää ulkomaisten tytäryritysten tilinpäätöksiä osana yrityksen konsolidointia. LVA:ta voidaan käyttää vain toista valuttaa käyttävien raporttien valmisteluun siten, että kyseinen valuutta on kuin yrityksen PVA.
>
> Sinulla voi olla esimerkiksi suuri määrä myyntisaamisia Ison-Britannian puntina (GBP), ja olet määrittänyt LVA:n GBP:ksi. Tässä skenaariossa myyntisaamisten summia, jotka käyttävät GBP:tä, ei oikaista valuuttakurssivoitoiksi/tappioiksi LVA:ssa, vaan ainoastaan myyntisaamisten summat, jotka ovat eri valuutoissa. Tämä tarkoittaa sitä, että jos ilmoitat tilinpäätöksen LVA:n avulla, se voi johtaa liian pieniin tai liian suuriin avoimiin saldoihin myyntisaamisissa.

## Raporttien ja summien näyttäminen LVA:na

LVA:n käyttäminen voi helpottaa yrityksen raportointiprosessia seuraavissa tapauksissa:

- Yritys toimii EU:n ulkopuolella ja suuri osa sen liiketoimista tapahtuu EU:ssa toimivien yritysten kanssa. Tässä tapauksessa EU:n ulkopuolisen yrityksen kannattaa ehkä raportoida euroina, jotta sen talousraportit olisivat helpommin EU-liikekumppanien käytettävissä.
- Yritys haluaa esittää raporttinsa oman paikallisen valuuttansa lisäksi myös laajemmin kansainvälisesti käytetyssä valuutassa.

Useat talousraportit perustuvat kirjanpitotapahtumiin. Raportin tiedot voidaan näyttää LVA:na valitsemalla kyseisen KP-raportin **Vaihtoehdot**-pikavälilehdessä **Näytä summat lisäraportointivaluuttana** -valintaruutu.

## Muutetaan vaihtokursseja

Koska vaihtokurssit vaihtelevat jatkuvasti, järjestelmän LVA-arvot on tarkistettava jaksoittain. Jos muutoksia ei tehdä, ulkomaanvaluutoista (tai lisävaluutoista) muunnetut summat voivat olla harhaanjohtavia, kun ne kirjataan pääkirjanpitoon PVA:na. Lisäksi päivittäiset tapahtumat, jotka on kirjattu ennen päivittäisen vaihtokurssin lisäämistä sovellukseen, on päivitettävä, kun päivittäinen vaihtokurssi on lisätty. **Muuta vaihtokursseja** -eräajon avulla voidaan muuttaa kirjattujen asiakas-, toimittaja- ja pankkitilitapahtumien vaihtokursseja. Sen avulla voi myös päivittää KP-tapahtumien LVA-summia. Lisätietoja on kohdassa [Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md).

## LVA:n määritys

Määritä LVA seuraavalla tavalla:

- Määritä vaihtokurssien muutosmenetelmä kaikille pääkirjanpidon tileille  
- Määritä vaihtokurssien muutosmenetelmä kaikille pääkirjanpidon tileille  
- Määritä vaihtokurssien muutosmenetelmän ALV-tapahtumille  
- Aktivoi LVA.  

### Määritä vaihtokurssien muutosmenetelmä kaikille pääkirjanpidon tileille  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Valuutat** ja valitse sitten vastaava linkki.  
2. Täytä **Valuutat**-sivulla seuraavat kentät LVA:ta varten.  

|Kenttä|Kuvaus|  
|---------------------------------|---------------------------------------|  
|**Realisoitun. KP-voittojen tili**|KP-tili, johon kirjataan PVA:n ja LVA:n välisten valuuttamuutosten vaihtokurssivoitot|  
|**Realisoitun. KP-tapp. tili**|KP-tili, johon kirjataan PVA:n ja LVA:n välisten valuuttamuutosten vaihtokurssihäviöt|  
|**Jäännösvoittojen tili**|KP-tili, jolle ohjelma kirjaa jäännössummat, jotka ovat voittoja, silloin kun tapahtumat kirjataan pääkirjanpidon sovellusalueelle sekä PVA:na että LVA:na|  
|**Jäännöstappioiden tili**|KP-tili, jolle ohjelma kirjaa jäännössummat, jotka ovat häviöitä, silloin kun tapahtumat kirjataan pääkirjanpidon sovellusalueelle sekä PVA:na että LVA:na|

> [!NOTE]  
> Jäännössummia voi syntyä [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman pyöristäessä PVA:sta LVA:ksi muunnettuja debet- ja kreditsummia.  

Kutakin KP-tiliä varten on määritettävä, miten tilin KP-summat muutetaan PVA:n ja LVA:n välisen vaihtokurssin muuttuessa.  

### Määritä vaihtokurssien muutosmenetelmä kaikille pääkirjanpidon tileille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten vastaava linkki.  
2. Valitse ensin **Tilikartta**-sivulla sopiva tili ja sitten **Muokkaa**-toiminto.  
3. Valitse **KP-tilin kortti** -sivun **Vaihtokurssin muutos** -kentässä sopiva menetelmä.  

    Jos tapahtumat kirjataan LVA:na, **Vaihtokurssin muutos** -kentässä määritetään, kuinka tätä KP-tiliä muutetaan PVA:n ja LVA:n välisen vaihtokurssin muuttuessa. Asetukset kuvaillaan seuraavassa taulukossa.  

    |Kenttä|Kuvaus|  
    |----------------------------------|---------------------------------------|  
    |**Ei muutosta**|KP-tilille ei tehdä vaihtokurssin muutosta. Tämä asetus on oletusarvo.<br /><br /> **HUOMAA:** Valitse tämä vaihtoehto, jos PVA:n ja LVA:n välinen vaihtokurssi on aina kiinteä.|  
    |**Muuta summaa**|PVA muutetaan aina valuuttakurssitappion ja –voiton yhteydessä. Ohjelma kirjaa kaikki vaihtokurssivoitot ja -tappiot KP-tilille ( **Lisävaluutan summa** -kenttä) sekä **Valuutat**-sivun **Realisoitun. KP-voittojen tili**- tai **Realisoitun. KP-tapp. tili** -kentässä voitoille tai tappioille määritetyille tileille.|  
    |**Muuta lisävaluuttasummaa**|LVA muutetaan aina valuuttakurssitappion ja –voiton yhteydessä. Ohjelma kirjaa kaikki vaihtokurssivoitot ja -tappiot KP-tilille ( **Lisävaluutan summa** -kenttä) sekä **Valuutat**-sivun **Realisoitun. KP-voittojen tili**- tai **Realisoitun. KP-tapp. tili** -kentässä voitoille tai tappioille määritetyille tileille.|  

    Vaihtokurssivoitot ja -tappiot kirjataan **Muuta vaihtokursseja** -eräajon suorituksen yhteydessä. Kyseisessä eräajossa etsitään muuttunut vaihtokurssi **Valuutan vaihtokurssit** -sivulta ja selvitetään sitten, onko kyseessä vaihtokurssivoitto vai -tappio, vertaamalla KP-tapahtuman **Summa**- ja **Lisävaluutan summa** -kenttien summia. Eräajo määrittää **Vaihtokurssin muutos** -kentässä valitun vaihtoehdon perusteella, Miten KP-tilien vaihtokurssivoitot tai -tappiot lasketaan ja kirjataan.  

4.  Sulje **KP-tilin kortti** -sivu.  

### Vaihtokurssien muutosmenetelmän määrittäminen ALV-tapahtumille

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **Pääkirjanpidon asetukset** -sivun **ALV:n vaihtokurssin muutos** -kentässä sopiva menetelmä.  
3. Jos tapahtumat kirjataan LVA:na, **ALV:n vaihtokurssin muutos** -kentässä voi määrittää, miten **ALV-kirjausten asetukset** -sivulla ALV-kirjauksille määritettyjä tilejä muutetaan PVA:n ja LVA:n välisen vaihtokurssin muuttuessa.  

    **Muuta vaihtokursseja** -eräajon suorittamisen yhteydessä muuttunut vaihtokurssi määritetään **Valuutan vaihtokurssi** -sivulla ja selvitetään sitten, onko kyseessä vaihtokurssivoitto vai -tappio, vertaamalla ALV-tapahtuman **Summa**- ja **Lisävaluutan summa** -kenttiä. Eräajo määrittää tässä kentässä valitun vaihtoehdon perusteella, kuinka ALV-tilien vaihtokurssivoitot tai -tappiot kirjataan.  

    Valittavana on samat kolme vaihtoehtoa kuin KP-tapahtumissa, mutta tässä tapauksessa muutettavat tapahtumat ovat ALV-tapahtumia: Asetukset kuvaillaan seuraavassa taulukossa.

    |Kenttä|Kuvaus|  
    |----------------------------------|---------------------------------------|  
    |**Ei muutosta**|KP-tilille ei tehdä vaihtokurssin muutosta. Tämä asetus on oletusarvo.|  
    |**Muuta summaa**|PVA muutetaan aina valuuttakurssitappion ja –voiton yhteydessä. Ohjelma kirjaa kaikki vaihtokurssivoitot ja -tappiot KP-tilille ( **Lisävaluutan summa** -kenttä) sekä **Valuutat**-sivun **Realisoitun. KP-voittojen tili**- tai **Realisoitun. KP-tapp. tili** -kentässä voitoille tai tappioille määritetyille tileille.|  
    |**Muuta lisävaluuttasummaa**|LVA muutetaan aina valuuttakurssitappion ja –voiton yhteydessä. Ohjelma kirjaa kaikki vaihtokurssivoitot ja -tappiot KP-tilille ( **Lisävaluutan summa** -kenttä) sekä **Valuutat**-sivun **Realisoitun. KP-voittojen tili**- tai **Realisoitun. KP-tapp. tili** -kentässä voitoille tai tappioille määritetyille tileille.|  

### LVA:n aktivointi  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **Pääkirjanpidon asetukset** -sivulla **Lisäraportointivaluutta**-kenttä ja valitse haluamasi raportoinnin lisävaluutta.  
3. Kun poistut kentästä, [!INCLUDE[prod_short](includes/prod_short.md)] näyttää vahvistussanoman, jossa kuvataan LVA:n valitsemisen (ja aktivoinnin) vaikutus.  
4. Vahvista valuutan aktivointi valitsemalla **Kyllä**.  
5. **Muuta/Lisää. Raportointivaluutta** -eräajo avautuu.

    Tämä eräajo muuttaa olemassa olevien tapahtumien PVA-summat LVA:ksi. Eräajo käyttää oletusvaihtokurssina työpäivänä voimassa olevaa **Valuutan vaihtokurssit** -sivulta kopioitua vaihtokurssia. Jäännössummat, jotka syntyvät, kun PVA muunnetaan LVA:ksi, kirjataan **Valuutat**-sivulla määritetyille jäännösvoittojen ja -tappioiden tileille. Näiden tapahtumien kirjauspäivämäärä ja asiakirjanumero ovat samat kuin alkuperäisessä KP-tapahtumassa. Kun olet kirjannut kaikki nämä jäännöstapahtumat, eräajo kirjaa jakamattoman voiton tilille pyöristystapahtuman kunkin suljetun tilikauden sulkemispäivänä. Näin varmistetaan, että kunkin suljetun vuoden tuloslaskelmatilin loppusaldo on 0 sekä PVA:na että LVA:na.
6. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Suorita eräajo valisemalla **OK**.  

Kun olet suorittanut eräajon, seuraavien olemassa olevien tapahtumien summat ovat sekä PVA:ssa että LVA:ssa:  

- Pääkirjanpidon tapahtumat  
- Nimikkeen kohdistustapahtumat  
- ALV-tapahtumat  
- Projektitapahtumat  
- Arvotapahtumat  
- tuotantotilausrivit  
- tuotantotilaustapahtumat.  

Lisäksi kaikissa samantyyppisissä tulevissa tapahtumissa summat kirjataan sekä PVA:na että LVA:na.  

> [!NOTE]  
> **Lisäraportointivaluutta**-kenttä aktivoituu vasta, kun olet napsauttanut **Muuta lisäraportointivaluuttaa**-eräajon **OK**-painiketta.  

## Katso myös

[Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md)  
[Vuosien ja kausien sulkeminen](year-close-years-periods.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
