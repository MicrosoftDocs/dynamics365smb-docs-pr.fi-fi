---
title: Viivästyskuluehtojen määrittäminen
description: 'Lue, miten voit määrittää Business Centralin niin, että voit ilmoittaa asiakkaille lisäkuluista lähettämällä viivästyskululaskuja.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment due, debt, overdue, fee, charge'
ms.search.form: '6, 494'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-finance-charge-terms"></a><a name="set-up-finance-charge-terms"></a><a name="set-up-finance-charge-terms"></a>Viivästyskuluehtojen määrittäminen

Jos asiakas ei suorita maksua eräpäivään mennessä, voit antaa ohjelman laskea viivästyskulut automaattisesti ja lisätä ne asiakkaan tilin erääntyneisiin summiin. Voi antaa asiakkaille tiedon lisätyistä kuluista lähettämällä viivästyskululaskuja. Ensin jokaista viivästyskulun laskentaa kuvaamaan täytyy määrittää koodi. Sitten tämä koodi voidaan syöttää asiakaskortin Viivästyskuluehtojen koodi -kenttään.  

## <a name="finance-charge-terms"></a><a name="finance-charge-terms"></a><a name="finance-charge-terms"></a>Viivästyskuluehdot

Kullekin viivästyskululaskelmalle on määritettävä viivästyskuluehdot ja määritettävä ehdot asiakkaalle **Asiakas**-sivun **Viivästyskuluehtojen koodi** -kentässä.

Viivästyskulut voidaan laskea käyttämällä joko keskimääräinen päiväsaldo- tai erääntyvä saldo -menetelmää.

* Keskimääräinen päiväsaldo  
  
  Maksun erääntymispäivien määrä otetaan huomioon:  
  *Keskimääräinen päiväsaldo -menetelmä* - *viivästyskulu* = *erääntynyt summa* x *(päiviä erääntynyt / korkojakso)* x *(korkoprosentti/100)*

* Erääntyvä saldo  
  
  Viivästyskulu on prosenttiosuus erääntyneestä summasta:  
  *Erääntyvä saldo -menetelmä* - *viivästyskulu* = *erääntynyt summa* x *(korkoprosentti / 100)*

Lisäksi jokainen Viivästyskuluehdot-taulukon ehto on linkitetty alitaulukkoon, Viivästyskuluteksti-taulukkoon. Jokaiselle viivästyskuluehtojen sarjalle voidaan määrittää alku- ja/tai lopputekstiä, joka sisällytetään viivästyskululaskuun.

### <a name="to-set-up-finance-charge-terms"></a><a name="to-set-up-finance-charge-terms"></a><a name="to-set-up-finance-charge-terms"></a>Viivästyskuluehtojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Viivästyskuluehdot** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät.
3. Voit käyttää useita viivästyskuluehtoyhdistelmä, kun määrität kullekin koodin.

    Voit määrittää kullekin viivästyskuluehdolle yksittäisiä ehtoja, joihin voi sisältyä lisämaksuja sekä paikallisena valuuttana että ulkomaan valuuttana. Kullekin **Viivästyskuluehdot**-sivun ehdolle voi määrittää lisämaksuja ulkomaan valuuttana.
4. Valitse **Valuutat**-toiminto.
5. Määritä **Lisäkuluehtojen valuutat** -sivulla kullekin ehdolle valuutan koodi ja lisämaksu.

    > [!NOTE]  
    > Kun luot viivästyskuluja ulkomaan valuuttana, tässä määritettäviä ulkomaan valuutan ehtoja käytetään viivästyskululaskujen luomiseen. Jos ulkomaan valuuttojen viivästyskuluehtoja ei ole määritetty, käytetään **Viivästyskuluehdot**-sivulla määritettyjä PVA:n viivästyskuluehtoja ja ne muunnetaan liittyvään valuuttaan.

    Voit määrittää jokaiselle viivästyskuluehdolle tekstiä, joka tulostetaan ennen viivästyskululaskun tapahtumia (**Aloitusteksti**) tai tapahtumien jälkeen (**Lopputeksti**).  
6. Valitse tilanteen mukaan joko **Aloitusteksti**- tai **Lopetusteksti**-toiminto ja täytä **Viivästyskuluteksti**-sivun tiedot.
7. Voit lisätä liittyviä arvoja automaattisesti viivästyskulutekstiin käyttämällä seuraavia paikkamerkkejä **Teksti**-kentässä.

|Paikkamerkki|Arvo|  
|-----------------|-----------|  
|%1|Viivästyskululaskun otsikon **Asiakirjan pvm** -kentän sisältö|  
|%2|Viivästyskululaskun otsikon **Eräpäivä**-kentän sisältö|  
|%3|Viivästyskuluehtojen **Korko**-kentän sisältö|  
|%4|Viivästyskululaskun otsikon **Jäljellä oleva summa** -kentän sisältö|  
|%5|Viivästyskululaskun otsikon **Korkosumma**-kentän sisältö|  
|%6|Viivästyskululaskun otsikon **Lisämaksu**-kentän sisältö|  
|%7|Muistutuksen kokonaissumma|  
|%8|Viivästyskululaskun otsikon **Valuutan koodi** -kentän sisältö|  
|%9|Viivästyskululaskun otsikon **Kirjauspvm**-kentän sisältö|  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/send-memos-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Avointen saldojen perintä](receivables-collect-outstanding-balances.md)  
[Muistutusehtojen ja -tasojen määrittäminen](finance-setup-reminders.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
