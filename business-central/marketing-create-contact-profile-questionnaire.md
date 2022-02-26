---
title: Profiilien avulla voit luokitella kontaktisi
description: Tietoja profiilikyselyjen määrittämisestä. Kyselyjen avulla voidaan luokitella liiketoimintakontakteja.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 06/22/2021
ms.openlocfilehash: 6ce13672651a5b6b65712928b764ad11b3db514d
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588524"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Liiketoimintakontaktien luokittelu profiilikyselyiden avulla
Voit määrittää kyselyprofiileja niille kyselyille, joita haluat käyttää, kun syötät tietoja kontaktiesi profiileista. Jokaisessa kyselyssä voit määrittää eri kysymykset, jotka aiot esittää kontakteillesi.  

Voit saada ohjelman vastaamaan automaattisesti joihinkin kysymyksiin kontakti-, asiakas- tai toimittajatietojen pohjalta.  

## <a name="to-add-a-profile-questionnaire"></a>Profiilikyselyjen lisääminen
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kyselyn asetukset** ja valitse sitten vastaava linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Kysymyksien lisääminen profiilikyselyyn
1.  Valitse haluttu profiilikysely. Valitse sitten **Muokkaa kyselyn asetuksia** -toiminto.  
2.  Valitse ensimmäisellä tyhjällä rivillä **Tyyppi**-kenttä, valitse **Kysymys** ja kirjoita kysymys **Kuvaus**-kenttään. Täytä rivin muut kentät.  
3.  Napsauta seuraavalla tyhjällä rivillä **Tyyppi**-kenttää, valitse **Vastaus** ja kirjoita vastaus **Kuvaus**-kenttään.  
4.  Valitse **Priority**-kentässä prioriteetti. Määritä **Arvosta**- ja **Arvoon**-kenttiin pisteväli. Kontaktit, jotka saavat pisteitä määritetyltä väliltä, saavat vastauksen.  

Toista nämä vaiheet ja syötä kaikki profiilikyselyn kysymykset ja vastaukset.

Kun olet luonut kyselyn, sinun on luotava kontaktin luokituksia luokitellaksesi kontaktisi. Voit myös määrittää automaattisesti kysymyksiä, jotka on luokiteltu kontaktikortin tietojen perusteella.  

> [!NOTE]
> Jos syötät kysymyksen, johon ohjelma vastaa automaattisesti, napsauta <STRONG>Rivi</STRONG>, <STRONG>Kysymyskortti</STRONG>, niin voit syöttää ne kriteerit, joita ohjelma käyttää vastatessaan kysymykseen automaattisesti.

## <a name="the-automatic-classification-of-contacts"></a>Kontaktien automaattinen luokittelu
Voit saada ohjelman luokittelemaan kontaktisi automaattisesti asiakkaan, toimittajan tai kontaktitietojen mukaan, kun määrittelet automaattisesti vastattuja profiilikysymyksiä **Profiilikyselyjen asetukset** -sivulla.  

> [!NOTE]
> Asiakastietoihin perustuva luokittelu voidaan liittää vain sellaisiin kontakteihin, jotka on tallennettu asiakkaina, ja toimittajatietoihin perustuva luokittelu voidaan liittää vain sellaisiin kontakteihin, jotka on tallennettu toimittajina. Automaattista luokittelua ei päivitetä automaattisesti. Haluat siten ehkä päivittää profiilikyselyjäsi, sen jälkeen kun olet päivittänyt ne asiakas-, toimittaja- tai kontaktitiedot, joille profiilikysely perustuu.  

Kun olet määrittänyt automaattisesti vastattuja profiilikysymyksiä, jos liität niistä koostuvan profiilikyselyn kontaktiin, [!INCLUDE[prod_short](includes/prod_short.md)] liittää kontaktiin automaattisesti oikeat vastaukset.  

## <a name="example"></a>Esimerkki

Voit luokitella kontaktisi sen mukaan, kuinka paljon he ostivat sinulta:

|Vastaus|Pätee seuraaviin|
|--- |--- |
|A|kontaktit, jotka ovat ostaneet vähintään 500 000 PVA|
|B|kontaktit, jotka ovat ostaneet 100 000 - 499 999 PVA|
|S|kontaktit, jotka ovat ostaneet enintään 99 999 PVA|

Jotta voisit tehdä tämän, täytä **Profiilikyselyjen asetukset** -sivu seuraavalla tavalla:

| Tyyppi     | Kuvaus        | Automaattinen luokittelu     | Arvosta | Arvoon |
|----------|--------------------|------------------------------|------------|----------|
| Kysymys | ABC-luokittelu | Lisää rasti napsauttamalla |            |          |
| Vastaus   | L                  |                              | 500,000    |          |
| Vastaus   | B                  |                              | 100,000    | 499,999  |
| Vastaus   | S                  |                              |            | 99 999   |

Täytä sitten **Profiilikyselyn yksityiskohdat** -sivu seuraavalla tavalla:

| Kenttä                         | Arvo         |
|-------------------------------|---------------|
| Asiakkaan luokituskenttä | Myynti (PVA)   |
| Luokittelutapa         | Määritetty arvo |

Kun määrität sen profiilikyselyn, jossa tämä kysymys on, kontaktiin, sovellus lisää automaattisesti asianomaisen vastauksen tälle kontaktille kontaktikortin profiiliriveille.

## <a name="see-also"></a>Katso myös

[Kontaktien luominen](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]