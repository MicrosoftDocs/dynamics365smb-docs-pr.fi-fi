---
title: Myyntisaamisten hallintatehtävien yleiskatsaus
description: Ohjeaiheessa kerrotaan tehtävistä, joilla hallitaan myyntisaamisia ja kohdistetaan maksuja asiakas- ja toimittajatapahtumiin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 9e7aa9c7aeb2ac8c84cebf09d5f7eb5287a5b9d7
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/30/2021
ms.locfileid: "6323566"
---
# <a name="managing-receivables"></a>Myyntisaamisten hallinta

Säännöllinen vaihe missä tahansa rahoituskierrossa on pankkitilien täsmäyttäminen, mikä edellyttää saapuvien maksujen kohdistamista asiakas- tai toimittajatapahtumiin, jotta myyntilaskut tai ostohyvityslaskut voidaan sulkea maksettuina.

Useimmat asiakkaat yritysympäristöissä maksavat jonkin aikaa toimituksen jälkeen jättäen kirjatun myyntilaskun avoimeksi myyntireskontraosaston suljettavaksi (kohdistettavaksi) kun maksu vastaanotetaan. Jotkin myyntilaskut voidaan kuitenkin maksaa heti esimerkiksi PayPal-maksuna. Tällaiset laskut kohdistetaan välittömästi maksetuiksi kirjaamisen yhteydessä ja siksi ne eivät näy myyntireskontralle käsiteltävinä maksuina. Lisätietoja on esimerkiksi kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).  

[!INCLUDE[prod_short](includes/prod_short.md)]issa voi rekisteröidä maksut nopeasti **Maksujen täsmäytyskirjauskansio** -sivun avulla tuomalla pankin tiliotteen tai syötteen. Maksut kohdistetaan avoimiin asiakas- tai toimittajatapahtumiin maksutekstin ja tapahtumatietojen välisen täsmäytyksen perusteella. Voit tarkastella ja muuttaa täsmäytyksiä ennen päiväkirjan kirjaamista sekä sulkea tapahtumien pankkitilitapahtumia päiväkirjaan kirjauksen aikana. Pankkitili täsmäytetään, kun kaikki maksut on kohdistettu.

On olemassa muita sivuja, joissa voit joko kohdistaa maksuja tai täsmäyttää pankkitilejä:

* **Pankkitilin täsmäytykset** -sivu, jossa voit täsmäyttää pankkitilit vertaamalla oman järjestelmän pankkitilitapahtumia tuodun pankin tiliotteen riveihin. Tässä voit täsmäyttää myös sekkimaksuja. Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen](bank-how-reconcile-bank-accounts-separately.md). Tässä ei voi kohdistaa maksuja.
* Voit kohdistaa manuaalisesti **Maksurekisteröinti**-sivulla käteisenä, sekkinä tai pankkitapahtumana vastaanotetut maksut maksamattomia myyntiasiakirjoja vastaan. Huomaa, että tämä toiminto on käytettävissä vain myyntiasiakirjoja varten. Tässä ei voi kohdistaa lähteviä maksuja eikä täsmäyttää pankkitilejä.
* **Kassapäiväkirja**-sivulla, jossa vastaanotot kirjataan antamalla manuaalisesti maksurivi soveltuvaan pääkirjaan tai soveltuvalle asiakkaalle tai toiselle tilille. Voit kohdistaa vastaanoton tai hyvityksen yhteen avoimeen tapahtumaan tai useisiin avoimiin tapahtumiin, ennen kuin kirjaat kassapäiväkirjan. Voit tehdä kohdistuksen myös asiakastapahtumista. Tässä ei voi täsmäyttää pankkitilejä.

**Maksujen täsmäytyskirjauskansio** -sivulla käytetään automaattista täsmäytyslogiikkaa, jonka voi määrittää **Maksusovelluksen säännöt** -sivulla. Lisätietoja on kohdassa [Määritä sääntöjä maksujen automaattiselle soveltamiselle](receivables-how-set-up-payment-application-rules.md).  

Myyntisaamisten hallinnassa kerätään myös avoimet saldot, kuten viivästyskulut, ja lähetetään muistutuksia sekä määritetään pankkitilit sallimaan asiakkaiden maksujen nostamien heidän tileiltään automaattisesti.

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.  

| Toiminta | Katso |
| --- | --- |
| Kohdista maksut avoimiin asiakas- tai toimittajatapahtumiin tuodun pankin tiliotetiedoston tai syötteen perusteella. Täsmäytä pankkitili sitten, kun kaikki maksut on kohdistettu. |[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Kohdista maksut asiakastapahtumiin **Maksurekisteröinti**-sivun maksamattomien myyntiasiakirjojen luettelon perusteella. |[Asiakkaan maksujen täsmäyttäminen maksamattomien myyntiasiakirjojen luettelosta](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Kirjaa asiakkaiden kassaanmaksut tai hyvitykset kassapäiväkirjaan ja kohdista asiakastapahtumat päiväkirjasta tai kirjatuista tapahtumakirjauksista. |[Asiakkaan maksujen täsmäyttäminen kassapäiväkirjan avulla tai asiakastapahtumista](receivables-how-apply-sales-transactions-manually.md) |
| Asiakkaiden muistuttaminen erääntyneistä summista, koron laskeminen ja viivästyskululaskut sekä myyntireskontran hallinta. |[Avointen saldojen perintä](receivables-collect-outstanding-balances.md) |
|Asiakkaan suostumuksella voit kerätä maksut suoraan asiakkaan pankkitililtä. Tämä on mahdollista vain euroina.|[Maksujen kerääminen SEPA-suoraveloitusperintänä.](finance-collect-payments-with-sepa-direct-debit.md)|
|Estä asiakkaan syöttäminen asiakirjoihin tai kirjauksesta esimerkiksi maksukyvyttömyyden vuoksi.|[Asiakkaiden estäminen](receivables-how-block-customers.md)|
|Määritä toleranssi, jonka mukaan järjestelmä sulkee laskun, vaikka maksu ja mahdolliset alennukset eivät täysin vastaa laskun koko summaa.|[Maksutoleranssien ja maksualennustoleranssien käsitteleminen](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Ennusta, milloin myyntiasiakirjan laskut määritetään myöhästyneiksi. | [Myöhästyneen maksun ennusteen laajennus](ui-extensions-late-payment-prediction.md) |

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/process-customer-vendor-payments-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]