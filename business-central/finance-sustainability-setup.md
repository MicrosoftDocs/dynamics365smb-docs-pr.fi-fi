---
title: Kestävyysmääritys
description: Tutustu kestävyysominaisuuksien määrittämiseen.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="sustainability-setup"></a>Kestävyysmääritys

Jotta kestävyys-moduuli toimisi oikein, on ensin määritettävä perusohjausobjekteja ja -ohjeita, jotka liittyvät kokonaistoimintoihin.  

Määritä kestävyysmoduuli noudattamalla seuraavia vaiheita:  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kestävyyden asetukset** ja valitse sitten vastaava linkki.  
2. Määritä **Yleinen**-pikavälilehdessä tähän moduuliin liittyvät pakolliset kentät:   

|  Kenttä  |  Kuvaus  |  
|--------|--------------| 
| **Päästön mittayksikön koodi** | Määrittää mittayksikön koodin, jota käytetään päästöjen rekisteröintiin. |
| **Päästön desimaalit** | Määrittää desimaalien määrän, joka näkyy päästömäärille. Oletusasetus 2:5 tarkoittaa, että kaikki summat näyttävät vähintään 2 desimaalia ja enintään 5 desimaalia. Voit syöttää myös kiinteän numeron, esimerkiksi 2, eli summat näytetään kahdella desimaalilla. |
| **Maa tai alue pakollinen** | Määrittää, onko maa/alue pakollinen. Voit käyttää tätä kenttää kirjauskansioissa määrittämättä tätä, mutta voit valita sen, jos haluat valvoa käyttäjien täyttävän kentän ennen kirjausta. |
| **Vastuupaikka pakollinen** | Määrittää, onko vastuupaikka pakollinen, koska vastuupaikkaa voidaan käyttää laitoskohtaisten päästöjen mittauksen toimintona. Voit käyttää tätä kenttää kirjauskansioissa määrittämättä tätä, mutta voit valita sen, jos haluat valvoa käyttäjien täyttävän kentän ennen kirjausta. |
| **Estä laskentaperusteen muutos, jos tapahtumakirjauksia on olemassa** | Määrittää, onko laskentaperusteen muutos Tilikategoriassa suljettu kestävyystapahtuman yhteydessä, mikä tarkoittaa, että tämä laskukaava on jo kohdistettu. |
| **Ota käyttöön taustavirheen tarkistus** | Määrittää, onko vastuullisuuspäiväkirjan rivien taustavirheen tarkistus käytössä. |

3.  Määritä **Laskennat**-pikavälilehdessä pakolliset kentät, jotka liittyvät päästöjen laskennassa käytettyihin kaavoihin:  

|  Kenttä  |  Kuvaus  |  
|--------|--------------| 
| **Polttoaineen/sähkön desimaalit** | Määrittää polttoaine-/sähkömäärissä näytettävien desimaalien määrän. Oletusasetus 2:5 tarkoittaa, että kaikki summat näyttävät vähintään 2 desimaalia ja enintään 5 desimaalia. Voit syöttää myös kiinteän numeron, esimerkiksi 2, eli summat näytetään kahdella desimaalilla. |
| **Etäisyyden desimaalit** | Määrittää etäisyysmittauksissa näytettävien desimaalien määrän. Oletusasetus 2:5 tarkoittaa, että kaikki summat näyttävät vähintään 2 desimaalia ja enintään 5 desimaalia. Voit syöttää myös kiinteän numeron, esimerkiksi 2, eli summat näytetään kahdella desimaalilla. |
| **Mukautettu summan desimaalien määrä** | Määrittää desimaalien määrän, joka näkyy mukautetuille määrille. Oletusasetus 2:5 tarkoittaa, että kaikki summat näyttävät vähintään 2 desimaalia ja enintään 5 desimaalia. Voit syöttää myös kiinteän numeron, esimerkiksi 2, eli summat näytetään kahdella desimaalilla. |

4.  Viimeistele viranomaisille raportointiin liittyvä **Raportointi**-pikavälilehden määritys:   

|  Kenttä  |  Kuvaus  |  
|--------|--------------| 
| **Päästöraportoinnin mittayksikön koodi** | Määrittää mittayksikön koodin, jota käytetään raportoitaessa päästöjä, koska eri mittayksikköä voidaan käyttää viranomaisille raportoitaessa. Tämä kenttä ei sovellu vakioraportteihin. |
| **Raportoinnin UOM-kerroin** | Määrittää mittayksikkökertoimen, jota käytetään päästöjen rekisteröintiin, jos käytät eri mittayksikköä raportoidessasi viranomaisille. |
| **Päästön pyöristystarkkuus** | Määrittää sen välin suuruuden, jota käytetään pyöristettäessä päästösummia viranomaisille raportoitaessa. |
| **Päästön pyöristystyyppi** | Määrittää, miten ohjelma pyöristää päästösumman raportoidessaan viranomaisille käyttäen vaihtoehtoja: Lähin, Ylöspäin tai Alaspäin. |

>[!NOTE]
> Versiossa 24.0 [!INCLUDE[prod_short](includes/prod_short.md)] ei tue raportointia millekään viranomaiselle. **Raportointi**-pikavälilehden määrittämiseen liittyvää kenttää käytetään siis tulevia raportointiominaisuuksia varten, mutta kumppanit voivat käyttää sitä myös lokalisoiduissa versioissa.

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)    
[Vastuullisuuden hallinnan yleiskuvaus](finance-manage-sustainability.md)
[Vastuullisuustilien ja -kirjauksenkaavio](finance-sustainability-accounts-ledger.md)
[Päästöjen tallennus](finance-sustainability-journal.md)
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman toiminta](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
