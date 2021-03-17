---
title: Automaattinen maksujen soveltamisen sääntöjen määrittäminen
description: Määritä Maksusovelluksen säännöt -sivulla säännöt, jotka hallinnoivat sitä, kuinka maksuja/pankkitapahtumia sovelletaan automaattisesti niihin liittyviin avoimiin kirjanpitotapahtumiin, kun käytät Sovella automaattisesti -toimintoa Maksujen täsmäytyskirjauskansio -sivulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a0aad6bce483dba6edf7c6d5ab37033475413d4b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392597"
---
# <a name="set-up-rules-for-automatic-application-of-payments"></a>Automaattinen maksujen soveltamisen sääntöjen määrittäminen

**Maksun sovellussäännöt** -sivulla määritetään sääntöjä, jotka määrittävät, miten maksuteksti (pankkitapahtumassa) kohdistetaan automaattisesti seuraavien kahden prosessin avointen tapahtumien tekstiin:

- Määritä säännöt, jotka hallinnoivat sitä, kuinka maksuja/pankkitapahtumia sovelletaan automaattisesti niihin liittyviin avoimiin (maksamattomiin) laskuihin, hyvityslaskuihin tai muihin kirjanpitotapahtumiin, kun käytät **Sovella automaattisesti** -toimintoa **Maksujen täsmäytyskirjauskansio** -sivulla. Lisätietoja on kohdassa [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).

- Täsmäytä pankkitapahtumat automaattisesti niihin liittyviin sisäisiin pankkitilitapahtumiin valitsemalla **Täsmäytä automaattisesti** -toiminto **Pankkitilin täsmäytys** -sivulla. Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen](bank-how-reconcile-bank-accounts-separately.md).

Voit asettaa uuden maksun sovellussäännön valitsemalla minkä tyyppisten tietojen maksujen täsmäytyskirjauskansion rivillä tulee vastata tietoja yhdessä tai useammassa avoimessa tapahtumassa, ennen kuin liittyvä maksu yhdistetään automaattisesti avoimiin tapahtumiin. Jokaisen automaattisen sovelluksen laatu näkyy käytetyn maksun kohdistussäännön mukaan arvona **Matalasta** **Korkeaan** **Vastaavuuden luotettavuus** -kentässä **Maksujen täsmäytyskirjauskansio** -sivulla sen maksusovellussäännön mukaisesti, jota käytettiin.

Jokainen **Maksusovelluksen säännöt** -sivun rivi edustaa maksun kohdistussääntöä. Sääntöjä sovelletaan **Lajittelujärjestys**-kentän määrittämässä järjestyksessä. Jos samanaikaisesti käytetään useita sääntöjä, käytetään vastaavuuden luotettavuutta korkeimmalle lajitellusta säännöstä.

Automaattinen sovellustoiminto perustuu priorisoituun kohdistusehtoon. Toiminto yrittää ensimmäiseksi kohdistaa prioriteettijärjestyksessä tekstin viiteen **Liittyvät osapuolet** -kenttään kirjauskansion rivillä, jolla on tekstiä pankkitilissä, nimessä tai asiakkaiden tai toimittajien nimissä, ja joissa maksamattomat asiakirjat edustavat avoimia tapahtumia. Tämän jälkeen funktio yrittää kohdentaa tekstin kentissä **Tapahtumateksti** ja **Lisätietoja tapahtumasta** kirjauskansion rivillä, jolla on tekstiä kentissä **Ulkoisen asiakirjan nro** ja **Asiakirjan nro** avoimissa tapahtumissa. Lopuksi funktio yrittää täsmätä kirjauskansion rivin **Tiliotteen summa** -kentän summan avointen tapahtumien summan kanssa.

> [!NOTE]
> Tekstin kohdistus on mahdollista vain yli neljä merkkiä sisältäville teksteille.

Kohdistustietojen lisäksi seuraavaa sovelletaan maksumäärän etumerkkiin:

- Negatiivisille määrille täsmäytys tehdään ensin asiakkaan laskuja edustavia avoimia tapahtumia vastaan ja sitten toimittajan hyvityslaskuja vastaan.
- Positiivisille määrille täsmäytys tehdään ensin toimittajan laskuja edustavia avoimia tapahtumia vastaan ja sitten asiakkaan hyvityslaskuja vastaan.

## <a name="to-set-up-a-payment-application-rule"></a>Maksun sovellussäännön asettaminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Maksujen sovellussäännöt** ja valitse sitten liittyvä linkki.
2. Määritä uusi tai muokattu maksun sovellussääntö täyttämällä rivin kentät seuraavassa taulukossa kuvatulla tavalla.

|Kenttä|Kuvaus|
|-|-|
|**Vastaavuuden luotettavuus**|Määrittää riville määritettävän sovellussäännön luotettavuuden. <br /></br>Tähän kenttään määrittämäsi arvo näkyy **Vastaavuuden luotettavuus** -kentässä **Maksujen täsmäytyskirjauskansio** -sivulla kirjauskansion rivin automaattisen maksusovelluksen laadun mukaan.|
|**Prioriteetti**|Määrittää kohdistussäännön prioriteetin suhteessa muihin kohdistussääntöihin, jotka on määritetty riveinä **Maksujen sovellussäännöt** -sivulla. 1 edustaa korkeinta prioriteettia.|
|**Liittyvän osapuolen vastaavuus**|Määrittää, kuinka paljon tietoja asiakkaasta tai toimittajasta, kuten osoite, kaupungin nimi ja pankkitilin numero, tulee vastata maksujen täsmäytyskirjauskansion rivillä avoimen tapahtuman tietoihin, ennen kuin sovellussääntöä käytetään soveltamaan automaattisesti maksua avoimeen tapahtumaan.|
|**Asiak. nro / Ulk. asiak. nro vastaavuus**|Määrittää, pitääkö maksujen täsmäytyskirjauskansion rivin tekstin vastata avoimen tapahtuman **Asiakirjan nro**- vai **Ulkoisen asiakirjan nro** - kentän arvoa, ennen kuin kohdistussääntö automaattisesti kohdistaa maksun avoimeen tapahtumaan.|
|**Kohdistustoleranssin sis. summa**|Määrittää, kuinka monen asiakkaan tai toimittajan tapahtumanon vastattava summaa, maksutoleranssi mukaan lukien, ennen kuin kohdistussääntöä käytetään automaattisesti kohdistamaan maksu avoimeen tapahtumaan.|
|**Tarkistus vaaditaan**|Määrittää, suositetaanko automaattista maksukohdistusta käyttäjän manuaaliseen tarkistukseen ennen kirjausta. **Tarkistettavat rivit** -kentän valitseminen **Maksujen kohdistuksen kirjauskansio** -sivulla aloittaa ohjatun käyttökokemuksen, jossa voit helposti tarkastella useita kohdistuksia **Maksun kohdistuksen tarkistus** -sivulla.|

Seuraavassa taulukossa kuvataan [!INCLUDE[prod_short](includes/prod_short.md)]in maksujen vakiokohdistuksen säännöt.

> [!Important]
> Maksun kohdistussäännöt saattavat vaihdella [!INCLUDE[prod_short](includes/prod_short.md)]-järjestelmän asennuksessasi.

| Vastaavuuden luotettavuus | Prioriteetti | Liittyvän osapuolen vastaavuus | Asiak. nro / Ulk. asiak. nro Vastaavuus | Kohdistustoleranssin sis. summa |
|------------------|----------|-----------------------|--------------------------------|--------------------------------|
| Korkea             | 1        | Täysin                 | Kyllä – useita                 | Yksi vastaavuus                      |
| Korkea             | 2        | Täysin                 | Kyllä – useita                 | Useita vastaavuuksia               |
| Korkea             | 3        | Täysin                 | Kyllä                            | Yksi vastaavuus                      |
| Korkea             | 4        | Täysin                 | Kyllä                            | Useita vastaavuuksia               |
| Korkea             | 5        | Osittain             | Kyllä – useita                 | Yksi vastaavuus                      |
| Korkea             | 6        | Osittain             | Kyllä – useita                 | Useita vastaavuuksia               |
| Korkea             | 7        | Osittain             | Kyllä                            | Yksi vastaavuus                      |
| Korkea             | 8        | Täysin                 | Ei                             | Yksi vastaavuus                      |
| Korkea             | 9        | Ei                    | Kyllä – useita                 | Yksi vastaavuus                      |
| Korkea             | 10       | Ei                    | Kyllä – useita                 | Useita vastaavuuksia               |
| Keskisuuri           | 1        | Täysin                 | Kyllä – useita                 | Ei huomioida                 |
| Keskisuuri           | 2        | Täysin                 | Kyllä                            | Ei huomioida                 |
| Keskisuuri           | 3        | Täysin                 | Ei                             | Useita vastaavuuksia               |
| Keskisuuri           | 4        | Osittain             | Kyllä – useita                 | Ei huomioida                 |
| Keskisuuri           | 5        | Osittain             | Kyllä                            | Ei huomioida                 |
| Keskisuuri           | 6        | Ei                    | Kyllä                            | Yksi vastaavuus                      |
| Keskisuuri           | 7        | Ei                    | Kyllä – useita                   | Ei huomioida                 |
| Keskisuuri           | 8        | Osittain             | Ei                             | Yksi vastaavuus                      |
| Keskisuuri           | 9        | Ei                    | Kyllä                            | Ei huomioida                 |
| Matala              | 1        | Täysin                 | Ei                             | Ei vastaavuuksia                     |
| Matala              | 2        | Osittain             | Ei                             | Useita vastaavuuksia               |
| Matala              | 3        | Osittain             | Ei                             | Ei vastaavuuksia                     |
| Matala              | 4        | Ei                    | Ei                             | Yksi vastaavuus                      |
| Matala              | 5        | Ei                    | Ei                             | Useita vastaavuuksia               |

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/reconciliation-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös
[Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]