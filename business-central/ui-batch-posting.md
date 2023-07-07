---
title: Useiden asiakirjojen kirjaaminen samanaikaisesti
description: Opi valitsemaan useita kirjaamattomia asiakirjoja luettelosta Business Centralin välitöntä tai ajoitettua eräkirjausta varten.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: null
ms.reviewer: edupont
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="post-multiple-documents-at-the-same-time"></a>Useiden asiakirjojen kirjaaminen samanaikaisesti

Sen sijaan että yksittäisiä asiakirjoja yksi kerrallaan, voit valita luettelosta useita kirjaamattomia asiakirjoja eräkirjausta varten. Tämä kirjaus voidaan tehdä heti tai se voidaan aikatauluttaa tapahtumaan vaikkapa päivän päätteeksi. Tämä voi olla kätevää, jos vain esimies voi kirjata muiden käyttäjien tekemiä asiakirjoja tai jos halutaan estää järjestelmän suorituskyvyn heikentyminen työaikana tehtävien kirjausten vuoksi.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Useiden ostotilausten kirjaaminen heti

Useita ostotilauksia voi kirjata heti toimimalla seuraavasti. Vaiheet ovat samanlaiset kaikissa osto- ja myyntiasiakirjoissa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.
2. Siirry valitsemaan kaikki kirjattavat tilaukset **Ostotilaukset**-sivulla:
3. Valitse **Nro**-kenttään kolme allekkain olevaa pistettä. Pikavalikko avautuu, ja voit valita **Valitse lisää** -toiminnon.
4. Valitse kaikkien samaan aikaan kirjattavien tilausrivien valintaruudut.
5. Valitse ensin **Kirjaus**-toiminto ja sitten **Kirjaa**-toiminto.
6. Valitse vahvistusviestissä **Kyllä**.

## <a name="to-batch-post-multiple-purchase-orders"></a>Useiden ostotilausten eräkirjaaminen

Ostotilauksia voi eräkirjata toimimalla seuraavasti. Vaiheet ovat samat kaikissa osto- ja myyntiasiakirjoissa, joissa **Eräkirjaus**-toiminto on käytettävissä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.  
2. Siirry valitsemaan kaikki kirjattavat tilaukset **Ostotilaukset**-sivulla:
3. Valitse **Nro**-kenttään kolme allekkain olevaa pistettä. Pikavalikko avautuu, ja voit valita **Valitse lisää** -toiminnon.
4. Valitse kaikkien samaan aikaan kirjattavien tilausrivien valintaruudut.
5. Valitse ensin **Kirjaus**-toiminto ja sitten **Eräkirjaus**-toiminto.
6. Täytä tarvittavat kentät **Eräkirjaa ostotilaukset** -sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Valitse **OK**-painike.
8. Voit tarkastella asiakirjojen eräkirjauksen aikana mahdollisesti esiintyneitä ongelmia avaamalla **Virhesanomarekisteri**-sivun.

> [!NOTE]
> Usean asiakirjan kirjaaminen voi kestää jonkin aikaa ja estää muita käyttäjiä. Harkitse taustakirjauksen käyttöönottoa. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).

## <a name="to-set-up-background-posting-with-job-queues"></a>Taustakirjauksen määrittäminen työjonojen avulla
Työjonot ovat tehokas työkalu taustalla suoritettavien liiketoimintaprosessien ajoittamiseen. Kyse voi olla esimerkiksi useista käyttäjistä, jotka yrittävät kirjata myyntitilauksia, kun vain yksi tilaus voidaan käsitellä kerralla.  

Seuraavaksi käsitellään myyntitilausten taustakirjausta. Ostoa koskevat vaiheet ovat samanlaisia.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntien ja myyntisaamisten asetukset** ja valitse sitten vastaava linkki.
2. Valitse **Myyntien ja myyntisaamisten asetukset** -sivulla **Kirjaa työjonolla** -valintaruutu.
3. Valitse **Työjonokategorian koodi** -kenttä ja määritä sitten **MKIRJAUS** -koodi.

    > [!NOTE]
    > Jotkin työt muuttavat samoja tietoja, eikä niitä tulisi käyttää samaan aikaan, koska ne voivat aiheuttaa ristiriitoja. Esimerkiksi myyntiasiakirjojen taustatyöt yrittävät muokata samoja tietoja samaan aikaan. Työjonoluokat auttavat estämään tällaisia ristiriitoja varmistamalla, että kun yksi työ on käynnissä, samaan työjonoluokkaan kuuluvaa työtä ei suoriteta ennen kuin suoritettava työ on valmis. Esimerkiksi projekti, joka kuuluu myyntityöjonoluokkaan, odottaa, kunnes kaikki muut myyntiin liittyvät työt on tehty. Voit määrittää työjonoluokan **Taustakirjaus**-pikavälilehdellä **Myynnin ja saatavien asetukset** -sivulla.
    >
    > [!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa työjonoluokkia myyntejä, ostoja ja pääkirjanpidon kirjauksia varten. On suositeltavaa, että jokin näistä tai luomasi on aina määritetty. Jos kohtaat ristiriidoista johtuvia virhetilanteita, harkitse luokan määrittämistä myynnin, oston ja pääkirjanpidon taustakirjausta varten.

    Jos haluat myös tulostaa kirjattavat myyntiasiakirjat, valitse **Kirjaa ja tulosta työjonolla** -valintaruutu **Myyntien ja myyntisaamisten asetukset** -sivulla.  
    Jos valitset **Raportin tuotostyyppi** -kentässä **PDF**, ostotilaukset, joiden kirjaus onnistui, ovat käytettävissä roolikeskuksen **Saapuneet raportit** -osassa.

    > [!IMPORTANT]  
    > Jos määrität asiakirjat kirjaavan ja tulostavan työn ja tulostimessa avautuu valintaikkuna, kuten tunnistetietojen pyyntö tai tulostimen musteen loppumisesta ilmoittava varoitus, asiakirja kirjataan mutta sitä ei tulosteta. Vastaava työjonotapahtuma aikakatkaistaan lopulta, ja **Tila**-kentän arvoksi määritetään **Virhe**. Näin ollen suosittelemme, että et käytä tulostimen asetuksia, jotka edellyttävät vuorovaikutusta tulostimen näytön valintaruutujen kanssa taustakirjausten yhteydessä.

    Kun kirjaat myyntiasiakirjoja seuraavan kerran, [!INCLUDE [prod_short](includes/prod_short.md)] luo automaattisesti työjonotapahtuman kullekin asiakirjalle ja suorittaa työt taustalla yksi kerrallaan.

4. Varmistaaksesi, että työjono toimii odotetulla tavalla, kirjaa myyntitilaus. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).
    Myyntitilaus lisätään nyt määritettyyn työjonotapahtumaan, joka määrittää, milloin asiakirjat kirjataan. 

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Myynti- tai ostoasiakirjan tilan näyttäminen
Jos työjono ei voi kirjata myyntitilausta, tilaksi muutetaan **Virhe** ja myyntitilaus lisätään niiden myyntitilausten luetteloon, jotka käyttäjän on käsiteltävä manuaalisesti.
1. Valitse asiakirjassa, jonka yritit kirjata taustakirjauksena, **Työjonon tila** -kenttä, jossa on **Virhe**.
2. Tarkastele virhesanomaa ja korjaa ongelma.

Vaihtoehtoisesti voit tarkistaa **Työjonon lokitapahtumat** -sivulta, onnistuiko myyntitilauksen kirjaus. Lisätietoja on [Valvo työjonoa](#monitor-the-job-queue) -osassa.

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Työjonotapahtuman luonti myyntitilausten eräkirjausta varten

Vaihtoehtoisesti voit lykätä kirjaukset organisaatiolle parhaiten sopivaan ajankohtaan. Yrityksessä saattaa olla esimerkiksi hyödyllistä suorittaa tietyt toiminnot sen jälkeen, kun suurin osa päivän tiedoista on syötetty. Tämä on mahdollista, kun määrität työjonon ajamaan useita eräkirjausraportteja, kuten **Eräkirjaa myyntitilaukset**- ja **Eräkirjaa ostotilaukset** -raportit sekä vastaavat raportit. [!INCLUDE[prod_short](includes/prod_short.md)] tukee kaikkien myynti-, osto- ja huoltoasiakirjojen taustakirjausta.

Seuraavaksi selitetään, miten **Eräkirjaa myyntitilaukset** -raportti määritetään kirjaamaan myyntitilaukset automaattisesti arkipäivisin kello 16.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työjonon tapahtumat** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Valitse **Suoritettavan objektin tyyppi** -kentässä **Raportti**.  
4. Valitse **Suoritettavan objektin tunnus** -kentässä 296, **Eräkirjaa myyntitilaukset**.

   Käytössä on myös seuraavat raportit:
  
   * 900 **Eräkirjaa kokoonpanotilaukset**
   * 497 **Eräkirjaa ostolaskut**
   * 496 **Eräkirjaa ostotilaukset**
   * 498 **Eräkirjaa ostohyvityslaskut**
   * 6665 **Eräkirjaa ostopal.tilaukset**
   * 298 **Eräkirjaa myyntihyvityslaskut**
   * 297 **Eräkirjaa myyntilaskut**
   * 296 **Eräkirjaa myyntitilaukset**
   * 6655 **Eräkirjaa myyntipal.tilaukset**
   * 6005 **Eräkirjaa huollon hyvityslaskut**
   * 6004 **Eräkirjaa huoltolaskut**
   * 6001 **Eräkirjaa huoltotilaukset**

5. Valitse **Raporttipyyntösivu**-valintaruutu.
6. Määritä **Eräkirjaa myyntitilaukset** -pyyntösivulla, mitä myyntitilausten automaattiseen kirjaukseen sisältyy, ja valitse sitten **OK**-painike.

    > [!IMPORTANT]
    > Muista käyttää tiukkoja suodattimia, sillä muutoin [!INCLUDE [prod_short](includes/prod_short.md)] kirjaa kaikki asiakirjat, vaikka ne eivät olisi valmiita. *Vapautettu*-arvon käyttöä suodattimen **Tilan**-kentän arvona ja *tänään*-arvoa **Kirjauspäivämäärä**-kentän arvona kannattaa harkita. Lisätietoja on kohdassa [Lajitteleminen, hakeminen ja suodattaminen](ui-enter-criteria-filters.md).
7. Valitse kaikki valintaruudut **Suorita maanantaisin** -kohdasta **Suorita perjantaisin** -kohtaan.
8. Anna **Aloitusaika**-kentässä arvoksi 16.00.
9. Valitse **Määritä tilaksi valmis** -toiminto.

Määritettyjen suodattimien mukaiset myyntitilaukset kirjataan nyt joka arkipäivä kello 16.

## <a name="monitor-the-job-queue"></a>Valvo työjonoa

Jos määrität taustakirjauksen työjonojen avulla, tee työjonon seuranta tavalliseksi tehtäväksi ongelmien havaitsemiseksi. Voit tarkastella tilaa  **Työjonon tapahtumat** -sivulla. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).  

Järjestelmänvalvojana voit [Application Insightsin](/azure/azure-monitor/app/app-insights-overview) avulla kerätä ja analysoida telemetriaa, jonka avulla voit tunnistaa ongelmia. Lisätietoja on kehittäjien ja järjestelmänvalvojien ohjeessa [Telemetrian seuranta ja analysoiminen](/dynamics365/business-central/dev-itpro/administration/telemetry-overview).  

## <a name="see-also"></a>Katso myös

[Asiakirjojen ja päiväkirjojen kirjaaminen](ui-post-documents-journals.md)  
[Työjonojen käyttäminen ajoitustehtäviin](admin-job-queues-schedule-tasks.md)  
[Kirjattujen asiakirjojen muokkaaminen](across-edit-posted-document.md)  
[Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
