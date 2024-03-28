---
title: 'Konsolidoi saldot yritykselle, joka on asiakas ja toimittaja'
description: 'Kuvaa, miten konsolidoidaan saldot yritykselle, joka on asiakas ja toimittaja.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '5052, 21, 5050'
ms.date: 10/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Konsolidoi saldot yritykselle, joka on asiakas ja toimittaja
Yritys, jonka kanssa käyt kauppaa, voi olla sekä asiakas että toimittaja. Tällöin voit välttää tarpeettomien maksujen tai kuittien tekemisen ja ehkä säästää transaktiomaksuissa yhdistämällä yrityksen asiakas- ja toimittajasaldot. Konsolidointi vertaa yrityksen saldoja toimittajana ja asiakkaana ja sitten summaa siten, että joko asiakkaan tai toimittajan saldo säilyy sen mukaan, mikä summa on suurempi. 

Kun haluat konsolidoida saldot, sinun on ensin linkitettävä asiakas- ja toimittajayritykset sellaisen kontaktin kautta, jonka tyyppi on **Yritys**. Asiakkaalla tai toimittajalla voi olla vain yksi kontakti, jonka tyyppi on **Yritys**. Lisätietoja on kohdassa [Kontaktien luominen](marketing-create-contact-companies.md).

Kun olet liittänyt yritykset, **Asiakkaan kortti** -sivulla on **Saldo toimittaja** -kenttänä, ja **toimittajan kortti** -sivulla on **saldo asiakkaana** -kenttä.

Vaikka kyseessä ei ole vaatimus, asiakas- ja toimittajayritykset ovat tavallisesti sama oikeushenkilö. 

## Ennen kuin aloitat
Määritä ennen saldojen konsolidointia joitakin asetuksia **Kontaktienhallinnan asetukset** -sivulla. 

* **Vuorovaikutukset**-pikavälilehdessä täytyy määrittää liikesuhdekoodit **Asiakkaat**- ja **Toimittajat**-kenttiin. Tämän tiedon avulla [!INCLUDE[prod_short](includes/prod_short.md)] määrittää kontakteille näytettävän suhteen tyypin. 
* Valinnainen: Ota kaksoiskappaleiden haku käyttöön tai pois käytöstä **Kaksoiskappaleet**-pikavälilehdessä. Oletusarvon mukaan päällekkäisyyksien haku on käytössä. Lisätietoja on kohdassa [Päällekkäisyyksien käsittely](#handling-duplicates). 

## Asiakas- ja toimittajayrityksen linkittäminen kontaktin kautta
Seuraavissa vaiheissa kuvataan, miten asiakas ja toimittaja linkitetään kontaktin kautta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** tai **Toimittaja** ja valitse sitten vastaava linkki.
2. Valitse asiakas tai toimittaja ja valitse sitten **Kontakti**-toiminto.   
3. Valitse yhteyshenkilö ja valitse sitten **Linkitä olemassa olevan kanssa** -toiminto.
4. Valitse sen yksikön tyyppi, jonka kanssa luodaan liikesuhde.
5. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## Luo toimittaja asiakkaasta tai toisin päin
Voit luoda uuden toimittajan aiemmin luodusta asiakkaasta tai uuden asiakkaan toimittajasta. Avaa **Asiakas**- tai **Toimittaja**-sivuilta **Kontakti**-sivu. Valitse **Luo kohteena** -toiminto ja valitse sitten **Asiakas** tai **Toimittaja**. 

## Luo uusi asiakas tai toimittaja ja linkitä ne toimittajan tai asiakkaan kontaktin kautta.
1. Luo uusi asiakas tai toimittaja. Lisätietoja on kohdissa [Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md) ja [Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md).
2. Kun olet määrittänyt asiakkaan tai toimittajan, valitse **Luo**-toimenpide ja valitse sitten joko **Asiakas**- tai **Toimittaja**. 

## Konsolidoi asiakas- ja toimittajasaldot kontaktiyritykselle
Voit konsolidoida asiakas- ja toimittajasaldot yhdeksi nettosummaksi käyttämällä **Maksupäiväkirja**-sivulla **Asiakkaan/toimittajan nettosaldot** -toimintoa. Toiminto luo, muttei kirjaa, maksupäiväkirjan rivit, jotka sisältävät nettosaldot.

> [!NOTE]
> Jos asiakkaan tai toimittajan saldot sisältävät summia, jotka ovat eri valuutoissa, jokaiselle valuutalle luodaan rivi.

## Kopioiden käsitteleminen
Jos otat kaksoiskappaleiden haun käyttöön **Kontaktienhallinnan asetukset** -sivun **Kaksoiskappaleet**-pikavälilehdessä, näyttöön tulee varoitus, kun muutat niiden kenttien arvoja, jotka ovat osa hakumerkkijonojen kaksoiskappaleiden määritystä. Kun kaksoiskappale löytyy, voit tehdä seuraavat toimet:

* Yhdistä päällekkäiset kontaktit yhteen kontaktiin, joka on sama sekä asiakkaalle että toimittajalle, käyttämällä **Kontaktikortti**-sivulla olevaa **Yhdistä**- toimintoa. Yleensä kontaktien yhdistäminen tehdään vain silloin, kun asiakas ja toimittaja ovat sama oikeushenkilö. Lisätietoja on kohdassa [Tietueiden kaksoiskappaleiden yhdistäminen](sales-how-merge-duplicate-records.md). 
* Poista toimittajan tai asiakkaan kontaktin toimittajaliikesuhde ja linkitä toiseen kontaktiin käyttämällä **Linkitä olemassa olevaan** -toimintoa.    

## Katso myös
[Myynti](sales-manage-sales.md)  
[Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md)  
