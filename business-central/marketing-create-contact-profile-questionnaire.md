---
title: Profiilien avulla voit luokitella kontaktisi
description: Tietoja profiilikyselyjen määrittämisestä. Kyselyjen avulla voidaan luokitella liiketoimintakontakteja.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'contacts, profiles'
ms.search.form: '5109, 5110'
ms.author: edupont
ms.date: 05/20/2022
---

# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><a name="use-profile-questionnaires-to-classify-business-contacts"></a><a name="use-profile-questionnaires-to-classify-business-contacts"></a>Liiketoimintakontaktien luokittelu profiilikyselyiden avulla

Voit arvioida prospektin ja tunnistaa parhaat mahdolliset prospektit, joille myyntikampanja kohdistetaan. Voit määrittää kyselyprofiileja niille kyselyille, joita haluat käyttää, kun syötät tietoja kontaktiesi profiileista. Jokaisessa kyselyssä voit määrittää eri kysymykset, jotka kontakteille esitetään. Tällä tavoin voit ryhmitellä kontakteja siten, että kampanjasi kohdistetaan todennäköisemmin oikeille henkilöille kyselyllä määrittämiesi perusteiden perusteella.  

Oikeiden kyselyjen avulla voit arvioida prospekteja ja ryhmitellä ne luokkiin. Voit muodostaa luokittelun perustan käyttämällä olemassa olevia kysymyksiä ja vastauksia ja yhdistelemällä niitä uusien kysymysten ja vastausten kanssa. Arvioinnin jokaiselle vastaukselle määritetään pistearvo. Arvioinnin jokaiselle vastaukselle määritetään pistearvo. Luokille määritettyjen arvovälien (*Arvosta* ja *Arvoon*) mukaan arviointijärjestelmä ryhmittelee kontaktit määrittämiisi luokkiin. Luokkia voivat olla esimerkiksi *ABC-asiakkaat*, *vanhat ja uudet* toimittajat tai *platina-, kulta- tai hopeatason* prospektit.  

Voit saada ohjelman vastaamaan automaattisesti joihinkin kysymyksiin kontakti-, asiakas- tai toimittajatietojen pohjalta.  

## <a name="to-add-a-profile-questionnaire"></a><a name="to-add-a-profile-questionnaire"></a><a name="to-add-a-profile-questionnaire"></a>Profiilikyselyjen lisääminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kyselyn asetukset** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><a name="to-add-questions-to-a-profile-questionnaire"></a><a name="to-add-questions-to-a-profile-questionnaire"></a>Kysymyksien lisääminen profiilikyselyyn

1. Valitse haluttu profiilikysely. Valitse sitten **Muokkaa kyselyn asetuksia** -toiminto.  
2. Valitse ensimmäisellä tyhjällä rivillä **Tyyppi**-kenttä, valitse **Kysymys** ja kirjoita kysymys **Kuvaus**-kenttään. Täytä rivin muut kentät.  

    Vaihtoehtoisesti voit lisätä kysymykseen tietoja.

    1. Valitse kysymyksen rivi, sitten **Rivi**-valikko ja lopuksi **Kysymyksen tiedot**.  

    2. Valitse **Profiilikysymyksen tiedot** -sivun **Luokittelu**-pikavälilehdessä **Autom. kontaktienluokittelu** -kenttä.  

    3. Valitse **Kontaktin luokittelukenttä** -kentässä **Luokittelu**-vaihtoehto.  

    4. Täytä **Vähimmäisvastaus-%-kenttä**. Oletusarvo on **0**.  

        Tässä kentässä on kysymysten lukumäärä (prosenteissa), johon tulee vastata, jotta ohjelma laskisi tämän luokittelun.

    5. Valitse **Toiminnot**-välilehden **Sivu**-ryhmässä **Vastauksen pisteet**. Valitse Toiminnot, Vastauksen pisteet ja syötä pisteet, jotka haluat antaa **Vastauksen pisteet**-sivulla luetelluille vastauksille.

        Jos haluat saada yleiskuvan pisteistä, jotka olet antanut kullekin vastaukselle, valitse **Vastauspisteet**-toiminto.

    6. Jos haluat suorittaa päivityksen, palaa **Profiilikyselyn määritys** -sivulle. Valitse **Toiminnot**-valikon **Funktiot**-ryhmässä **Päivitä luokittelu**.

    **Profiilikyselyn määritys** -sivulla näkyy niiden yhteyshenkilöiden määrä, jotka täyttävät **Kontaktien lkm** -kentässä ja kunkin yhteyshenkilön **Kontaktin kortti** -kortissa näkyvät ehdot.

3. Napsauta seuraavalla tyhjällä rivillä **Tyyppi**-kenttää, valitse **Vastaus** ja kirjoita vastaus **Kuvaus**-kenttään.  
4. Valitse **Priority**-kentässä prioriteetti. Määritä **Arvosta**- ja **Arvoon**-kenttiin pisteväli. Kontaktit, jotka saavat pisteitä määritetyltä väliltä, saavat vastauksen.  

Toista nämä vaiheet ja syötä kaikki profiilikyselyn kysymykset ja vastaukset.

Kun olet luonut kyselyn, voit käyttää sitä kontaktiesi arviointiin ja luokitteluun. Voit myös määrittää automaattisesti kysymyksiä, jotka on luokiteltu kontaktikortin tietojen perusteella.  

> [!NOTE]
> Jos syötät kysymyksen, johon ohjelma vastaa automaattisesti, napsauta **Rivi**, **Kysymyskortti**, niin voit syöttää ne kriteerit, joita ohjelma käyttää vastatessaan kysymykseen automaattisesti.

## <a name="apply-questionnaires-to-contacts"></a><a name="apply-questionnaires-to-contacts"></a><a name="apply-questionnaires-to-contacts"></a>Kyselyjen soveltaminen kontakteihin

Voit soveltaa kyselyjä manuaalisesti kontakteihin. Avaa vain kulloinenkin kontaktikortti ja valitse **Profiili**-toiminto. Kun sitten olet soveltanut haluamasi kyselyt, voit aloittaa luokkien käytön kampanjoissasi.  

## <a name="the-automatic-classification-of-contacts"></a><a name="the-automatic-classification-of-contacts"></a><a name="the-automatic-classification-of-contacts"></a>Kontaktien automaattinen luokittelu

Voit saada ohjelman luokittelemaan kontaktisi automaattisesti asiakkaan, toimittajan tai kontaktitietojen mukaan, kun määrittelet automaattisesti vastattuja profiilikysymyksiä **Profiilikyselyjen asetukset** -sivulla.  

> [!NOTE]
> Asiakastietoihin perustuva luokittelu voidaan liittää vain sellaisiin kontakteihin, jotka on tallennettu asiakkaina, ja toimittajatietoihin perustuva luokittelu voidaan liittää vain sellaisiin kontakteihin, jotka on tallennettu toimittajina. Automaattista luokittelua ei päivitetä automaattisesti. Haluat siten ehkä päivittää profiilikyselyjäsi, sen jälkeen kun olet päivittänyt ne asiakas-, toimittaja- tai kontaktitiedot, joille profiilikysely perustuu.  

Kun olet määrittänyt automaattisesti vastattuja profiilikysymyksiä, jos liität niistä koostuvan profiilikyselyn kontaktiin, [!INCLUDE[prod_short](includes/prod_short.md)] liittää kontaktiin automaattisesti oikeat vastaukset.  

## <a name="example"></a><a name="example"></a><a name="example"></a>Esimerkki

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

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Kontaktien luominen](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
