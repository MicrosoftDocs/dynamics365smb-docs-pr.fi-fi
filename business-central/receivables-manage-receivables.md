---
title: "Myyntisaamisten hallintatehtävien yleiskatsaus | Microsoft Docs"
description: "Ohjeaiheessa kerrotaan tehtävistä, joilla hallitaan myyntisaamisia ja kohdistetaan maksuja asiakas- ja toimittajatapahtumiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 11/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 2e677a1170be8f55421869ca0308fb31961b58f7
ms.contentlocale: fi-fi
ms.lasthandoff: 11/22/2018

---
# <a name="managing-receivables"></a>Myyntisaamisten hallinta
Säännöllinen vaihe missä tahansa rahoituskierrossa on pankkitilien täsmäyttäminen, mikä edellyttää saapuvien maksujen kohdistamista asiakas- tai toimittajatapahtumiin, jotta myyntilaskut tai ostohyvityslaskut voidaan sulkea maksettuina.

Useimmat asiakkaat yritysympäristöissä maksavat jonkin aikaa toimituksen jälkeen jättäen kirjatun myyntilaskun avoimeksi myyntireskontraosaston suljettavaksi (kohdistettavaksi) kun maksu vastaanotetaan. Jotkin myyntilaskut voidaan kuitenkin maksaa heti esimerkiksi PayPal-maksuna. Tällaiset laskut kohdistetaan välittömästi maksetuiksi kirjaamisen yhteydessä ja siksi ne eivät näy myyntireskontralle käsiteltävinä maksuina. Lisätietoja on esimerkiksi kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).  

[!INCLUDE[d365fin](includes/d365fin_md.md)]issa voi rekisteröidä maksut nopeasti **Maksujen täsmäytyskirjauskansio** -sivulla tuomalla pankin tiliotteen tai syötteen. Maksut kohdistetaan avoimiin asiakas- tai toimittajatapahtumiin maksutekstin ja tapahtumatietojen välisen täsmäytyksen perusteella. Voit tarkastella ja muuttaa täsmäytyksiä ennen päiväkirjan kirjaamista sekä sulkea tapahtumien pankkitilitapahtumia päiväkirjaan kirjauksen aikana. Pankkitili täsmäytetään, kun kaikki maksut on kohdistettu.

On olemassa muita sivuja, joissa voit joko kohdistaa maksuja tai täsmäyttää pankkitilejä:

* **Pankkitilin täsmäytykset** -sivu, jossa voit täsmäyttää pankkitilit vertaamalla oman järjestelmän pankkitilitapahtumia tuodun pankin tiliotteen riveihin. Tässä voit täsmäyttää myös sekkimaksuja. Lisätietoja on kohdassa [Pankkitilien täsmäyttäminen erikseen](bank-how-reconcile-bank-accounts-separately.md). Tässä ei voi kohdistaa maksuja.
* Voit kohdistaa manuaalisesti **Maksurekisteröinti**-sivulla käteisenä, sekkinä tai pankkitapahtumana vastaanotetut maksut maksamattomia myyntiasiakirjoja vastaan. Huomaa, että tämä toiminto on käytettävissä vain myyntiasiakirjoja varten. Tässä ei voi kohdistaa lähteviä maksuja eikä täsmäyttää pankkitilejä.
* **Kassapäiväkirja**-sivulla, jossa vastaanotot kirjataan antamalla manuaalisesti maksurivi soveltuvaan pääkirjaan tai soveltuvalle asiakkaalle tai toiselle tilille. Voit kohdistaa vastaanoton tai hyvityksen yhteen avoimeen tapahtumaan tai useisiin avoimiin tapahtumiin, ennen kuin kirjaat kassapäiväkirjan. Voit tehdä kohdistuksen myös asiakastapahtumista. Tässä ei voi täsmäyttää pankkitilejä.  

Myyntisaamisten hallinnassa kerätään myös avoimet saldot, kuten viivästyskulut, ja lähetetään muistutuksia sekä määritetään pankkitilit sallimaan asiakkaiden maksujen nostamien heidän tileiltään automaattisesti.

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.  

| Toiminta | Katso |
| --- | --- |
| Kohdista maksut avoimiin asiakas- tai toimittajatapahtumiin tuodun pankin tiliotetiedoston tai syötteen perusteella. Täsmäytä pankkitili sitten, kun kaikki maksut on kohdistettu. |[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
|Voit määrittää maksujen tekstin kohdistukset ja tietyt debet-, kredit- ja kirjanpidon vastatilit siten, että nämä maksut kirjataan tietyille tileille, jotta nämä maksut kirjataan tietyille tileille, kun kirjaat maksun täsmäytyksen päiväkirjan.|[Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)|
| Kohdista maksut avoimiin asiakasmaksuihin maksamattomien myyntiasiakirjojen luettelon manuaalisen tapahtuman perusteella. |[Asiakkaan maksujen täsmäyttäminen manuaalisesti maksamattomien myyntiasiakirjojen luettelosta](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Kirjaa asiakkaiden kassaanmaksut tai hyvitykset kassapäiväkirjaan ja kohdista asiakastapahtumat päiväkirjasta tai kirjatuista tapahtumakirjauksista. |[Täsmäytä asiakkaan maksut manuaalisesti](receivables-how-apply-sales-transactions-manually.md) |
| Asiakkaiden muistuttaminen erääntyneistä summista, koron laskeminen ja viivästyskululaskut sekä myyntireskontran hallinta. |[Avointen saldojen perintä](receivables-collect-outstanding-balances.md) |
| Ennusta, milloin myyntiasiakirjan laskut määritetään myöhästyneiksi. | [Myöhästyneen maksun ennusteen laajennus](ui-extensions-late-payment-prediction.md) |
|Asiakkaan suostumuksella voit kerätä maksut suoraan asiakkaan pankkitililtä. Tämä on mahdollista vain euroina.|[Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md)|
|Estä asiakkaan syöttäminen asiakirjoihin tai kirjauksesta esimerkiksi maksukyvyttömyyden vuoksi.|[Asiakkaiden estäminen](receivables-how-block-customers.md)|
|Varmista. että tiedät toimitettujen nimikkeiden kulut määrittämällä lisätyt nimikekulut, kuten nimikkeiden myynnin jälkeen syntyvät rahti-, käsittely-, vakuutus- ja kuljetuskulut.|[Kaupan lisäkustannusten huomiointi nimikekulujen avulla](payables-how-assign-item-charges.md)|
|Määritä toleranssi, jonka mukaan järjestelmä sulkee laskun, vaikka maksu ja mahdolliset alennukset eivät täysin vastaa laskun koko summaa.|[Maksutoleranssien ja maksualennustoleranssien käsitteleminen](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

