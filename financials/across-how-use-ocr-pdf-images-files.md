---
title: "PDF-tiedostojen muuntaminen sähköisiksi laskuiksi OCR:n avulla| Microsoft Docs"
description: "Kuvaa, miten PDF- tai kuvatiedostot voidaan muuntaa sähköisiksi Financials-asiakirjoiksi OCR-palvelun avulla."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 020aeed82d6147641936dee2d7b860791c76d2ee
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a>Toimintaohje: Käytä OCR:ää muuntamaan PDF- ja kuvatiedostoja sähköisiksi asiakirjoiksi
Ulkoinen OCR (Optical Character Recognition) -palvelu voi luoda liikekumppaneilta vastaanotetuista PDF- tai kuvatiedostoista sähköisiä asiakirjoja, jotka voit muuntaa tiedostotietueiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Esimerkiksi kun saat PDF-muodossa laskun toimittajalta, voit lähettää sen OCR-palveluun **Saapuvat asiakirjat** -ikkunasta. Tämä kuvataan ensimmäisessä menettelytavassa.

Jos et halua lähettää tiedostoa **Saapuneet asiakirjat** -ikkunasta, voit lähettää sen OCR-palveluun sähköpostitse. Sitten, kun saat sähköisen tiedoston takaisin, liittyvä saapuvan asiakirjan tietue luodaan automaattisesti. Tämä kuvataan toisessa menettelytavassa.

Jonkin sekunnin kuluttua saat tiedoston takaisin OCR-palvelusta sähköisenä laskuna, jonka voit muuntaa toimittajan ostolaskuksi. Tämä kuvataan kolmannessa menettelytavassa.

Koska OCR perustuu optiseen tunnistukseen, OCR-palvelu tulkitsee todennäköisesti PDF- tai kuvatiedostojesi merkit väärin, kun se käsittelee ensimmäistä kertaa esimerkiksi tietyn toimittajan asiakirjoja. Se ei ehkä tulkitse yrityksen logoa toimittajan nimeksi, tai se voi tulkita tositteen kokonaissumman väärin sen asettelun vuoksi. Voit välttää näiden virheiden aiheuttamat seuraukset korjaamalla virheet **Saapuneet asiakirjat** -ikkunan erillisessä versiossa. Sitten korjaukset lähettää takaisin OCR-palveluun opettamaan se tulkitsemaan merkkejä oikein seuraavalla kerralla, kun se käsittelee PDF- tai kuva-asiakirjaa samalta toimittajalta. Lisätietoja on osassa "OCR-palvelun kouluttaminen välttämään virheet".

Tiedostojen liikenne OCR-palvelun kanssa sisään ja ulos käsitellään erillisinä työjonotapahtumana, jotka luodaan automaattisesti, kun otat liittyvän palveluyhteyden käyttöön. Lisätietoja on kohdassa [Toimintaohje: Saapuvien asiakirjojen määrittäminen](across-how-setup-income-documents.md).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-window"></a>Voit lähettää PDF- tai kuvatiedoston OCR-palveluun **Saapuvat asiakirjat** -ikkunasta
1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Saapuvat asiakirjat** ja valitse sitten aiheeseen liittyvä linkki.
2. Luo uuden saapuvan asiakirjan tietueen ja liittää tiedoston. Lisätietoja on kohdassa [Toimintaohje: Saapuvien asiakirjatietueiden luominen](across-how-create-income-document-records.md).  
3. Valitse **Saapuneet asiakirjat** -ikkunassa vähintään yksi rivi ja valitse sitten **Lähetä työjonoon** -toiminto.

    **OCR-tila**-kentän arvoksi tulee **Valmis**. Liitetty PDF- tai kuvatiedosto lähetetään OCR-palvelun aikataulun mukaan Työjonosta edellyttäen, että virheitä ei ole.
4. Vaihtoehtoisesti voit valita **Saapuneet asiakirjat** -ikkunassa vähintään yhden rivin ja valita sitten **Lähetä OCR-palveluun** -toiminto.

**OCR-tila**-kentän arvoksi tulee **Lähetetty**, jos virheitä ei löydy.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a>Lähetä PDF- tai kuvatiedosto OCR-palveluun sähköpostitse
Lähetä sähköpostiohjelmasta OCR-palveluntarjoajalle sähköpostiviesti PDF- tai kuvatiedostoliitteen kanssa. Palveluntarjoajan verkkosivusto sisältää sähköpostiosoitteen, jonne viesti lähetetään.

Koska tiedostolla ei ole tulevaa asiakirjatietuetta, uusi tietue luodaan automaattisesti **Saapuvat asiakirjat** -ikkunassa, kun vastaanotat sähköisen asiakirjan OCR-palvelusta. Lisätietoja on kohdassa [Toimintaohje: Saapuvien asiakirjatietueiden luominen](across-how-create-income-document-records.md).

> [!NOTE]  
>   Jos käytät Tablet PC:tä tai puhelinta, voit lähettää tiedoston OCR-palvelun heti kun olet ottanut valokuvan asiakirjasta tai voit luoda saapuvan asiakirjan suoraan. Lisätietoja on "Saapuvien asiakirjatietueiden luominen ottamalla valokuva"-osassa kohdassa [Toimintaohje: Saapuvien tietueiden luominen](across-how-create-income-document-records.md).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a>Tuloksena olevan vastaanotettavan sähköisen asiakirjan vastaanottaminen OCR-palvelusta.
Työjonotapahtuma, joka määritetään OCR-palvelun käyttöönoton yhteydessä, vastaanottaa **Saapuvat asiakirjat** -ikkunaan automaattisesti sähköisen asiakirjan, jonka OCR-palvelu luo PDF- tai kuvatiedostosta.

Jos et käytä työjonoa tai haluat vastaanottaa OCR-asiakirjan työjonon aikataulua nopeammin, voit valita **Vastaanota OCR-palvelusta** -painikkeen. Näin saat kaikki asiakirjat, jotka ovat valmiita OCR-palvelussa.

> [!NOTE]  
>   Jos OCR-palvelun määrityksissä vaaditaan käsiteltyjen asiakirjojen manuaalinen vahvistus, **OCR-tila**-kentän arvo on **Odottaa vahvistusta**. Kirjaudu tällöin OCR-palvelun verkkosivustoon seuraavien ohjeiden mukaan ja vahvista OCR-asiakirja.

1. Valitse **OCR-tila**-kentässä **Odottaa vahvistusta** -hyperlinkki. Vaihtoehtoisesti voit valita kotisivulla **Odottaa vahvistusta** -ruudun.
2. Kirjaudu OCR-palvelun verkkosivustoon OCR-palvelutilin tunnistetietojen avulla. Näitä tunnistetietoja käytetään myös palvelun määrittämisessä. Lisätietoja on "OCR-palvelun määrittäminen" -osan kohdassa [Toimintaohje: Saapuvan asiakirjan määrittäminen](across-how-setup-income-documents.md).

    Jos siirryt verkkosivustoon **OCR-tila**-kentän avulla, kyseinen asiakirja näytetään heti sisäänkirjautumisen jälkeen. Jos siirryt verkkosivustoon kotisivun ruudun avulla, ensimmäisenä avautuvalla OCR-palvelun sivulla on valittava **Aloita**-painike **Vahvista**-välilehdessä. Vaihtoehtoisesti voit kaksoisnapsauttaa vahvistettavaa asiakirjaa.

    Näkyviin tulevat OCR-asiakirjan tiedot, joissa näkyvät sekä PDF- tai kuvatiedoston lähdesisältö että tuloksena olevan OCR-kentän arvot.
3. Voit tarkistaa eri kenttien arvoja ja manuaalisesti muokata tai syöttää niiden kenttien arvoja, jotka OCR-palvelu on merkinnyt epävarmoiksi.
4. Valitse **OK**-painike. OCR-prosessi on valmis ja tuloksena saatava sähköinen asiakirja lähetetään [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Saapuvat asiakirjat** -ikkunaan työjonon aikataulun mukaisesti.

    Jos siirryt verkkosivustoon kotisivun ruudun avulla, kaikki muut varmistettavat OCR-asiakirjat näytetään verkkosivustossa automaattisesti.
5. Toista vaihe 4 kaikille varmistettaville OCR-asiakirjoille.

Voit nyt jatkaa asiakirjatietueiden luomista vastaanotetuille sähköisille asiakirjoille [!INCLUDE[d365fin](includes/d365fin_md.md)]issa manuaalisesti tai automaattisesti. Lisätietoja on seuraavassa toimenpiteessä. Voit myös yhdistää uuden saapuvan asiakirjan tietueen aiemmin kirjattuun tai kirjaamattomaan asiakirjaan siten, että lähdetiedostoa on helppo käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]ista. Lisätietoja on kohdassa [Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md).

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a>Ostolaskun luominen OCR-palvelusta vastaanotetusta sähköisestä asiakirjasta
Seuraavassa kuvataan, miten ostolaskutietue luodaan toimittajan laskusta, joka on vastaanotettu sähköisenä asiakirjana OCR-palvelusta. Menettelytapa on sama kuin esimerkiksi silloin,kun yleisenpäiväkirjan rivi luodaan kulutositteesta.

> [!NOTE]  
>   **Kuvaus**- ja **Nro**-kenttä täytetään luoduilla asiakirjariveillä vain, jos OCR-asiakirjasta löytynyt teksti on ensin linkitetty kahteen [!INCLUDE[d365fin](includes/d365fin_md.md)]in kenttään. Voit tehdä tämän Nimike-tyyppisille asiakirjariveille nimikeviittauksina tai KP-tili-tyyppisille asiakirja- tai päiväkirjariveille tekstin ja tilin yhdistämismäärityksinä. Lisätietoja on nimikekorttien **Viittaukset**-toiminnon työkaluvihjeessä ja liittyvässä menettelytavassa [Toimintaohje: Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Saapuvissa asiakirjoissa käytetään yleensä **Linkitä teksti tiliin** -toimintoa, kun määritetään, että OCR-palvelusta vastaanotetun toimittajan laskun tietty teksti on linkitetty tiettyyn toimittajan tiliin. Jatkettaessa mikä tahansa saapuvan asiakirjan kuvauksen osa, joka on olemassa linkitettynä tekstinä, tarkoittaa sitä, että **Nro**-kenttä tuloksena saatavassa asiakirjassa tai päiväkirjariveillä, joiden tyyppi on KP-tili, täytetään kyseisen toimittajan tiedoilla.

Toimittajatiliin tai toiseen KP-tiliin linkittämisen lisäksi myös pankkitiliin voidaan linkittää. Tämä on käytännöllistä esimerkiksi sähköisille asiakirjoille, jotka on jo maksettu, johon haluat luoda yleisen päiväkirjarivin, joka on valmis kirjattavajsu pankkitilille.

1. Valitse OCR-palvelusta vastaanotetun toimittajan sähköisen asiakirjan saapuvan asiakirjan rivi.
2. Voit linkittää asiakirjan tekstin toimittajan tiliin (debet-tiliin) valitsemalla **Linkitä teksti tiliin** -toiminnon ja täyttämällä **Teksti tilille -vastaavuusmääritys** -ikkunaan toimittajaa jatkossa koskevat tiedot. Lisätietoja on kohdassa [Toimintaohje: Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).
3. Voit linkittää asiakirjan nimikenumerot toimittajan nimikkeiden kuvauksiin avaamalla kunkin nimikkeen kortin, valitsemalla **Viittaukset**-toiminnon ja määrittämällä sitten nimikkeen ja toimittajan kuvausten väliset viittaukset.
4. Valitse **Saapuvat asiakirjat** -ikkunassa **Luo asiakirja** -toiminto.

[!INCLUDE[d365fin](includes/d365fin_md.md)]iin luodaan ostolasku OCR-palvelusta vastaanotetun toimittajan sähköisen laskun tietojen perusteella.

Vahvistusvirheet (jotka yleensä liittyvät [!INCLUDE[d365fin](includes/d365fin_md.md)]in vääriin tai puuttuviin perustietoihin) näkyvät **Virheet ja varoitukset** -pikavälilehdessä. Lisätietoja on "Virheiden käsitteleminen vastaanotettaessa sähköisiä asiakirjoja" -osassa.

## <a name="to-handle-errors-when-receiving-electronic-documents"></a>Virheiden käsitteleminen vastaanotettaessa sähköisiä asiakirjoja
1. Valitse **Saapuvat asiakirjat** -ikkunassa OCR-palvelusta vastaanotetun sähköisen asiakirjan virheitä sisältävä rivi. Virhearvo **OCR-tila**-kentässä osoittaa virheen.
2. Valitse **Muokkaa** -toiminto, jonka jälkeen **Saapuva asiakirja** -ikkuna avautuu.
3. Valitse **Virheet ja varoitukset** -pikavälilehdessä sanoma ja valitse sitten **Avaa liittyvä tietue** -toiminto.
4. Vääriä tai puutteellisia tietoja sisältävä ikkuna (kuten toimittajakortti, josta puuttuu kenttäarvo) avautuu.
5. Korjaa virhe/virheet virhesanomassa kuvatulla tavalla.
6. Jatka saapuvan sähköisen asiakirjan käsittelemistä valitsemalla uudelleen **Luo manuaalisesti** -toiminto.
7. Toista vaiheet 5–6 kaikille jäljellä oleville virheille. Tämän jälkeen sähköinen asiakirja voidaan ottaa vastaan.

## <a name="to-train-the-ocr-service-to-avoid-errors"></a>OCR-palvelun kouluttaminen välttämään virheet
Koska OCR perustuu optiseen tunnistukseen, OCR-palvelu tulkitsee todennäköisesti PDF- tai kuvatiedostojesi merkit väärin, kun se käsittelee ensimmäistä kertaa esimerkiksi tietyn toimittajan asiakirjoja. Se ei ehkä tulkitse yrityksen logoa toimittajan nimeksi, tai se voi tulkita kulutositteen kokonaissumman väärin sen asettelun vuoksi. Voit välttää näitä virheitä vastaisuudessa korjaamalla OCR-palvelun vastaanottamat tiedot ja lähettämällä sitten palautteen palveluun.

**OCR-tietojen korjaus** -ikkunassa, joka avataan **Saapuneet asiakirjat** -ikkunassa, näkyvät **Rahoituksellisia tietoja** -pikavälilehden kentät kahdessa sarakkeessa. Toinen sarake sisältää muokattavat OCR-tiedot ja toinen vain luku -tilassa olevat OCR-tiedot. Kun valitset **Lähetä OCR-palaute** -painike, **OCR-tietojen korjaus** -ikkunan sisältö lähetetään OCR-palveluun. Seuraavan kerran, kun palvelu käsittelee kyseisiä tietoja sisältäviä PDF- tai kuvatiedostoja, korjaukset otetaan huomioon, jotta vältetään samat virheet.

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Saapuvat asiakirjat** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa saapuva asiakirjatietue, joka sisältää OCR-palvelusta saadut tiedot, jonka haluat korjata.
3. Valitse **Saapuva asiakirja** -ikkunassa **Korjaa OCR-tiedot** -toiminto.
4. Korvaa **OCR-tietojen korjaus** -Ikkunassa muokattavissa olevassa sarakkeessa kenttien virheelliset tiedot.
5. Voit peruuttaa **OCR-tietojen korjaus** -ikkunan avaamisesta lähtien tehdyt korjaukset valitsemalla **Palauta OCR-tiedot** -toiminnon.
6. Lähetä korjaukset OCR-palveluun valitsemalla **Lähetä OCR-palaute** -toiminto.
7. Tallenna korjaukset sulkemalla **OCR-tietojen korjaus** -ikkuna.

**Saapunut asiakirja** -ikkunan **Rahoituksellisia tietoja** -pikavälilehden kenttiin päivitetään vaiheessa 4 syöttämäsi uudet arvot.

## <a name="see-also"></a>Katso myös
[Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

