---
title: Käteisasiakkaiden määrittäminen
description: 'Tässä aiheessa kuvataan vaiheet, joita tarvitaan laskun määrittämiseen asiakasnumerolla käteisellä maksavia asiakkaita varten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '21, 22'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-cash-customers"></a>Käteisasiakkaiden määrittäminen

Laskua ei voi luoda ilman asiakasnumeroa. Näin on, vaikka teet käteismyynnin, eikä asiakastilille ole mitään tallennettavaa.  

## <a name="to-set-up-a-cash-customer"></a>Käteisasiakkaiden määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** ja valitse sitten vastaava linkki.  
2. Luo uusi **Asiakkaan** kortti. Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).
3. Valitse **Nro**-kenttään esimerkiksi **Käteismyynti**.  
4. Syötä **Nimi**-kenttään esimerkiksi **Käteismyynti**.  
5. Täytä **Laskutus**-pikavälilehden **Asiakkaan kirjausryhmä**- ja **Ylein. liiketoim. kirjausryhmä** -kentät.  

 Nyt asiakas on määritetty, ja se sisältää riittävästi tietoa laskutusta varten.  

> [!NOTE]  
> Olet voinut valita kirjausryhmän, jota on käytetty myös kotimaisiin luottomyynteihin. Jos haluat ylläpitää erillistä tietoa käteismyynneistä esimerkiksi erityisellä myynti- tai myyntisaamistilillä, voit määrittää tätä varten ylimääräisen kirjausryhmän.  
>
> Myyntisaamistilille täytyy syöttää numero kirjausryhmää varten, vaikka tilin saldo on aina 0 laskun kirjaamisen jälkeen.  

## <a name="see-also"></a>Katso myös

[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Uusien asiakkaiden rekisteröiminen](sales-how-register-new-customers.md)
[Rahoitus](finance.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]
