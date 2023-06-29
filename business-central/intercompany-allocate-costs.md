---
title: Kustannusten kohdistaminen konsernikumppaneille | Microsoft Docs
description: 'Tietoja siitä, miten asiakkaiden ja toimittajien ALV-asetukset ohjaavat ALV:n laskemista.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="allocate-costs-to-intercompany-partners"></a><a name="allocate-costs-to-intercompany-partners"></a>Kustannusten kohdistaminen konsernikumppaneille
Kun käytät konsernin kirjauksia asiakirjojen siirtoon konsernikumppanien välillä, ALV:hen liittyvät asetukset (pääasiassa liiketoiminnan ALV-kirjausryhmä), jotka on määritetty (konsernikumppaniin liittyville) asiakas- tai toimittajatileille, määrittävät, lasketaanko ALV ja miten se lasketaan ja rekisteröidään. Voit myös tehdä kustannusten jakoja suoraan ostotilauksesta kumppaniyrityksiin. Jos esimerkiksi rekisteröit ostolaskun ulkopuoliselle toimittajalle ja haluat jakaa osan kustannuksista tai kaikki kustannukset yhdelle tai useammalle konsernikumppanille.

Kustannuksia voi kohdistaa yhdelle tai useammalle konsernikumppanille seuraavasti:

* **Konsernin yleiset päiväkirjat** - Nämä päiväkirjat ovat hyödyllisiä silloin, kun palvelu ostetaan. Esimerkiksi silloin, kun emoyritys palkkaa palvelun määrittämään tietokonejärjestelmiä kahdelle tytäryhtiölle. Lasku lähetetään emoyhtiölle, mutta kustannukset kohdistetaan konsernikumppaneille. Lisätietoja on kohdassa [Konsernin asiakirjojen ja päiväkirjojen käsitteleminen](intercompany-how-work-documents-journals.md).
* Ostotilaukset ja laskut – Ostoasiakirjojen käyttäminen on hyödyllistä silloin, kun esimerkiksi käyttökulujen ostotoiminnot on keskitetty yhteen yritykseen ja kohdistettu sitten konsernikumppaneille.

## <a name="to-allocate-costs-using-an-intercompany-general-journal"></a><a name="to-allocate-costs-using-an-intercompany-general-journal"></a>Kustannusten kohdistaminen konsernin yleisen päiväkirjan avulla
Voit lisätä rivin konsernin yleiseen päiväkirjaan noudattamalla seuraavia vaiheita. 

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin yleinen päiväkirja** ja valitse sitten vastaava linkki.
2. Lisää tarvittaessa **Ulkoisen asiakirjan nro** -kenttään toimittajan laskun asiakirjanumero.
3. Valitse **Asiakirjatyyppi**-kentässä **Lasku**.
4. Valitse **Tilityyppi**-kentässä **Toimittaja**.
5. Valitse **Tilinro**-kentässä toimittaja.
6. Syötä **Summa**-kenttään negatiivinen summa, joka on sama kuin laskun summa.
7. Valitse **Vastatilin tyyppi** -kentässä **KP-tili**.
8. Valitse **Vastatilin nro** -kentässä käytettävä vastatili.
9. Voit kohdistaa kustannukset konsernikumppaneille seuraavasti:
   1. Luo uusi rivi.
   2. Jätä **Asiakirjatyyppi**-kenttä tyhjäksi, valitse vaihtoehto, joka jättää kentän tyhjäksi.
   3. Syötä **Asiakirjan nro** -kenttään numero, joka poikkeaa **Ulkoisen asiakirjan nro** -kentän numerosta. Kustannusten kohdistusta pidetään eri tapahtumana.
   4. Valitse **Tilityyppi**-kentässä **Konsernikumppani**.
   5. Valitse **Tilinro**-kentässä konsernikumppani, jolle kustannus kohdistetaan.
   6. Valitse **Vastatilin tyyppi** -kentässä **KP-tili**.
   7. Valitse **Vastatilin nro** -kentässä KP-tili, jolle haluat kirjata konsernikumppanilta saamasi summan.
   1. Syötä **Summa**-kenttään konsernikumppanille kohdistettavan laskun summa.
   1. Valitse **Konsernikumppanin KP-tilinro** -kentässä KP-tili, jolle haluat kirjata konsernikumppanille maksamasi summan. 
   1. Täytä tarvittavat jäljellä olevat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Toista nämä vaiheet kaikkien niiden konsernikumppanien osalta, joiden tulisi jakaa kustannukset.
1. Kun haluat kirjata asiakirjan ja kohdistaa kustannukset, valitse **Kirjaa**.  

## <a name="to-allocate-costs-using-a-purchase-document"></a><a name="to-allocate-costs-using-a-purchase-document"></a>Kustannusten kohdistaminen ostoasiakirjan avulla
Seuraavassa kuvataan, miten kustannuksia kohdistetaan ostolaskun avulla. Ostotilausten vaiheet ovat vastaavanlaiset.

> [!NOTE]
> Näiden vaiheiden suorittaminen edellyttää **Ostolasku** -sivun mukauttamista lisäämällä **Konsernikumppanin koodi**-, **Konsernikumppanin viitetyyppi**- ja **Konsernikumppani**-kentät. Lisätietoja on kohdassa, jossa [Sivun mukauttaminen mukautusvalintanauhan avulla](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolasku** ja valitse sitten vastaava linkki.
2. Valitse **Tyyppi**-kentässä **KP-tili**.
   
   KP-tili on ainoa valinta, jota voi käyttää kustannusten kohdistamiseen.  
1. Valitse **Nro**-kenttään kentässä valitse KP-tili, johon kirjataan.
1. Valitse **Konsernikumppanin koodi**-kentässä konsernikumppani, jolle kustannus kohdistetaan.
1. Valitse **Konsernikumppanin viitetyyppi** -kohdassa KP-tili, jota käytetään kohdistuksessa. Tämä tili yhdistää kulun konsernikumppanin tilikartan tiliin.
1. Määrittele **Määrä**-kenttään konsernikumppanilta laskutettujen yksiköiden lukumäärä.
1. Syötä **Välitön yksikkökustannus ilman ALV:tä (tai sis. alv)** -kenttään konsernikumppanilta laskutettavaan nimikkeeseen sisältyvä kustannus.
1. Täytä tarvittavat jäljellä olevat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
1. Kun haluat kirjata ostotilauksen, valitse **Kirjaa**.

## <a name="to-send-the-allocated-costs-to-intercompany-partners"></a><a name="to-send-the-allocated-costs-to-intercompany-partners"></a>Kohdistettujen kustannusten lähettäminen konsernikumppaneille
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Konsernin Lähtevät-kansion tapahtumat** ja valitse sitten vastaava linkki.
2. Valitse lähetettävät rivit ja valitse sitten **Lähetä konsernikumppanille** -toiminto. 
3. Voit kohdistaa kustannukset valitsemalla **Toteuta rivitoiminnot** -toiminnon.

## <a name="calculating-vat-for-cost-distributions"></a><a name="calculating-vat-for-cost-distributions"></a>ALV:n laskeminen kustannusten jaoille
Kun käytät asiakirjaa kustannusten jakamiseen konsernikumppaneille, huomaa kaksi ALV-asetusta: 
* KP-tilin asetukset kulujen osalta:
   * Jos KP-tiliin on määritetty liiketoiminnan tai yleinen liiketoiminnan ALV-kirjausryhmä, laskenta riippuu asiakirjarivin ryhmistä ja tuoteryhmistä.
   * Jos KP-tilille ei ole määritetty liiketoiminnan tai yleistä liiketoiminnan ALV-kirjausryhmää, laskenta riippuu seuraavista:
* Konsernikumppanien kirjausryhmäasetukset
   * Siitä, liitetäänkö konsernikumppaniin asiakasnumeroon, jolla ei ole määritettyjä liiketoiminnan tai yleisiä liiketoiminnan ALV-kirjausryhmiä.
   * Konsernikumppaniin ei liity asiakasnumeroa. Tässä tapauksessa liiketoiminnan yleiset liiketoiminnan ALV-kirjausryhmät ovat tyhjiä, ja ALV-kirjausasetuksissa olevaa riviä käytetään. Tämä on yleensä ryhmä, jossa on määritetty alv 0 %.

> [!NOTE]
> On tärkeää tarkistaa sekä konsernikumppanin asetukset että KP-tilin asetukset (kustannusten jaossa käytetyn kulutilin osalta) ennen kustannusten kohdistamista konsernikumppaneille.

## <a name="see-also"></a><a name="see-also"></a>Katso myös
[Konsernin tietojen määrittäminen](intercompany-how-setup.md)  
[Konsernitapahtumien hallinta](intercompany-manage.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
