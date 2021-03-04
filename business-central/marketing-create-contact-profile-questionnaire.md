---
title: Profiilien avulla voit luokitella kontaktisi
description: Liiketoimintakontaktien luokittelu profiilikyselyiden avulla
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 10/01/2020
ms.openlocfilehash: 65c27bee86d273c467709f1e238b996829d73f37
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755440"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Liiketoimintakontaktien luokittelu profiilikyselyiden avulla
Voit määrittää kyselyprofiileja niille kyselyille, joita haluat käyttää, kun syötät tietoja kontaktiesi profiileista. Jokaisessa kyselyssä voit määrittää eri kysymykset, jotka aiot esittää kontakteillesi.  

Voit saada ohjelman vastaamaan automaattisesti joihinkin kysymyksiin kontakti-, asiakas- tai toimittajatietojen pohjalta.  

## <a name="to-add-a-profile-questionnaire"></a>Profiilikyselyjen lisääminen
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kyselyn asetukset** ja valitse sitten liittyvä linkki.  
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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Vastaus</strong></th>
<th><strong>Pätee seuraaviin</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p>kontaktit, jotka ovat ostaneet vähintään 500 000 PVA</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p>kontaktit, jotka ovat ostaneet 100 000 - 499 999 PVA</p></td>
</tr>
<tr class="odd">
<td><p>S</p></td>
<td><p>kontaktit, jotka ovat ostaneet enintään 99 999 PVA</p></td>
</tr>
</tbody>
</table>

Jotta voisit tehdä tämän, täytä **Profiilikyselyjen asetukset** -sivu seuraavalla tavalla:


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tyyppi</strong></th>
<th><strong>Kuvaus</strong></th>
<th><strong>Automaattinen luokittelu</strong></th>
<th><strong>Arvosta</strong></th>
<th><strong>Arvoon</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Kysymys</p></td>
<td><p>ABC-luokittelu</p></td>
<td><p>Lisää rasti napsauttamalla</p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>Vastaus</p></td>
<td><p>L</p></td>
<td><p> </p></td>
<td><p>500,000</p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p>Vastaus</p></td>
<td><p>B</p></td>
<td><p> </p></td>
<td><p>100,000</p></td>
<td><p>499,999</p></td>
</tr>
<tr class="even">
<td><p>Vastaus</p></td>
<td><p>S</p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p>99 999</p></td>
</tr>
</tbody>
</table>

Täytä sitten **Profiilikyselyn yksityiskohdat** -sivu seuraavalla tavalla:
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Kenttä</strong></th>
<th><strong>Arvo</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Asiakkaan luokituskenttä</strong></td>
<td><emphasis>Myynti (PVA)</emphasis></td>
</tr>
<tr>
<td><strong>Luokittelutapa</strong></td>
<td><emphasis>Määritetty arvo</emphasis></td>
</tr>
</tbody>
</table>

Kun määrität sen profiilikyselyn, jossa tämä kysymys on, kontaktiin, sovellus lisää automaattisesti asianomaisen vastauksen tälle kontaktille kontaktikortin profiiliriveille.

## <a name="see-also"></a>Katso myös
[Kontaktien luominen](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]