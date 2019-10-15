---
title: PDF-tiedostojen muuntaminen sähköisiksi laskuiksi OCR:n avulla| Microsoft Docs
description: Kuvaa, miten PDF- tai kuvatiedostot voidaan muuntaa sähköisiksi asiakirjoiksi OCR-palvelun avulla.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c35ccb10ca67e66697002add56d518f3a7bacc0d
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305162"
---
# <a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a>PDF- ja kuvatiedostojen muuntaminen sähköisiksi asiakirjoiksi OCR-palvelun avulla
Ulkoinen OCR (Optical Character Recognition) -palvelu voi luoda liikekumppaneilta vastaanotetuista PDF- tai kuvatiedostoista sähköisiä asiakirjoja, jotka voit muuntaa tiedostotietueiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Kun esimerkiksi saat PDF-muotoisen laskun toimittajalta, voit lähettää sen OCR-palveluun **Saapuvat asiakirjat** -sivulta. Tämä kuvataan ensimmäisessä menettelytavassa.

Jos et halua lähettää tiedostoa **Saapuneet asiakirjat** -sivulta, voit lähettää sen OCR-palveluun sähköpostitse. Sitten, kun saat sähköisen tiedoston takaisin, liittyvä saapuvan asiakirjan tietue luodaan automaattisesti. Tämä kuvataan toisessa menettelytavassa.

Jonkin sekunnin kuluttua saat tiedoston takaisin OCR-palvelusta sähköisenä laskuna, jonka voit muuntaa toimittajan ostolaskuksi. Tämä kuvataan kolmannessa menettelytavassa.

Koska OCR perustuu optiseen tunnistukseen, OCR-palvelu tulkitsee todennäköisesti PDF- tai kuvatiedostojesi merkit väärin, kun se käsittelee ensimmäistä kertaa esimerkiksi tietyn toimittajan asiakirjoja. Se ei ehkä tulkitse yrityksen logoa toimittajan nimeksi, tai se voi tulkita tositteen kokonaissumman väärin sen asettelun vuoksi. Voit välttää näiden virheiden aiheuttamat seuraukset korjaamalla virheet **Saapuneet asiakirjat** -sivun erillisessä versiossa. Sitten korjaukset lähettää takaisin OCR-palveluun opettamaan se tulkitsemaan merkkejä oikein seuraavalla kerralla, kun se käsittelee PDF- tai kuva-asiakirjaa samalta toimittajalta. Lisätietoja on kohdassa [OCR-palvelun kouluttaminen välttämään virheitä](across-how-use-ocr-pdf-images-files.md#to-train-the-ocr-service-to-avoid-errors).

Tiedostojen liikenne OCR-palvelun kanssa sisään ja ulos käsitellään erillisinä työjonotapahtumana, jotka luodaan automaattisesti, kun otat liittyvän palveluyhteyden käyttöön. Lisätietoja on kohdassa [Saapuvien asiakirjojen määrittäminen](across-how-setup-income-documents.md).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a>Voit lähettää PDF- tai kuvatiedoston OCR-palveluun **Saapuvat asiakirjat** -sivulta
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Saapuvat asiakirjat** ja valitse sitten liittyvä linkki.
2. Luo uuden saapuvan asiakirjan tietueen ja liittää tiedoston. Lisätietoja on kohdassa [Saapuvien asiakirjatietueiden luominen](across-how-create-income-document-records.md).  
3. Valitse **Saapuneet asiakirjat** -sivulla vähintään yksi rivi ja valitse sitten **Lähetä työjonoon** -toiminto.

    **OCR-tila**-kentän arvoksi tulee **Valmis**. Liitetty PDF- tai kuvatiedosto lähetetään OCR-palvelun aikataulun mukaan Työjonosta edellyttäen, että virheitä ei ole.
4. Vaihtoehtoisesti voit valita **Saapuneet asiakirjat** -sivulla vähintään yhden rivin ja valita sitten **Lähetä OCR-palveluun** -toiminto.

**OCR-tila**-kentän arvoksi tulee **Lähetetty**, jos virheitä ei löydy.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a>Lähetä PDF- tai kuvatiedosto OCR-palveluun sähköpostitse
Lähetä sähköpostiohjelmasta OCR-palveluntarjoajalle sähköpostiviesti PDF- tai kuvatiedostoliitteen kanssa. Palveluntarjoajan verkkosivusto sisältää sähköpostiosoitteen, jonne viesti lähetetään.

Koska tiedostolla ei ole tulevaa asiakirjatietuetta, uusi tietue luodaan automaattisesti **Saapuvat asiakirjat** -sivulla, kun vastaanotat sähköisen asiakirjan OCR-palvelusta. Lisätietoja on kohdassa [Saapuvien asiakirjatietueiden luominen](across-how-create-income-document-records.md).

> [!NOTE]  
>   Jos käytät Tablet PC:tä tai puhelinta, voit lähettää tiedoston OCR-palvelun heti kun olet ottanut valokuvan asiakirjasta tai voit luoda saapuvan asiakirjan suoraan. Lisätietoja on kohdassa [Saapuvien asiakirjatietueiden luominen valokuva ottamalla](across-how-create-income-document-records.md#to-create-an-incoming-document-record-by-taking-a-photo).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a>Tuloksena olevan vastaanotettavan sähköisen asiakirjan vastaanottaminen OCR-palvelusta.
Työjonotapahtuma, joka määritetään OCR-palvelun käyttöönoton yhteydessä, vastaanottaa **Saapuvat asiakirjat** -sivulle automaattisesti sähköisen asiakirjan, jonka OCR-palvelu luo PDF- tai kuvatiedostosta.

Jos et käytä työjonoa tai haluat vastaanottaa OCR-asiakirjan työjonon aikataulua nopeammin, voit valita **Vastaanota OCR-palvelusta** -painikkeen. Näin saat kaikki asiakirjat, jotka ovat valmiita OCR-palvelussa.

> [!NOTE]  
>   Jos OCR-palvelun määrityksissä vaaditaan käsiteltyjen asiakirjojen manuaalinen vahvistus, **OCR-tila**-kentän arvo on **Odottaa vahvistusta**. Kirjaudu tällöin OCR-palvelun verkkosivustoon seuraavien ohjeiden mukaan ja vahvista OCR-asiakirja.

1. Valitse **OCR-tila**-kentässä **Odottaa vahvistusta** -hyperlinkki.
2. Kirjaudu OCR-palvelun verkkosivustoon OCR-palvelutilin tunnistetietojen avulla. Näitä tunnistetietoja käytetään myös palvelun määrittämisessä. Lisätietoja on kohdassa [OCR-palvelun määrittäminen](across-how-setup-income-documents.md#to-set-up-an-ocr-service).

    Näkyviin tulevat OCR-asiakirjan tiedot, joissa näkyvät sekä PDF- tai kuvatiedoston lähdesisältö että tuloksena olevan OCR-kentän arvot.
3. Voit tarkistaa eri kenttien arvoja ja manuaalisesti muokata tai syöttää niiden kenttien arvoja, jotka OCR-palvelu on merkinnyt epävarmoiksi.
4. Valitse **OK**-painike. OCR-prosessi on valmis ja tuloksena saatava sähköinen asiakirja lähetetään [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Saapuvat asiakirjat** -sivulle työjonon aikataulun mukaisesti.
5. Toista vaihe 4 kaikille varmistettaville OCR-asiakirjoille.

Voit nyt jatkaa asiakirjatietueiden luomista vastaanotetuille sähköisille asiakirjoille [!INCLUDE[d365fin](includes/d365fin_md.md)]issa manuaalisesti tai automaattisesti. Lisätietoja on seuraavassa toimenpiteessä. Voit myös yhdistää uuden saapuvan asiakirjan tietueen aiemmin kirjattuun tai kirjaamattomaan asiakirjaan siten, että lähdetiedostoa on helppo käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]ista. Lisätietoja on kohdassa [Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md).

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a>Ostolaskun luominen OCR-palvelusta vastaanotetusta sähköisestä asiakirjasta
Seuraavassa kuvataan, miten ostolaskutietue luodaan toimittajan laskusta, joka on vastaanotettu sähköisenä asiakirjana OCR-palvelusta. Menettelytapa on sama kuin esimerkiksi silloin, kun yleisen päiväkirjan rivi luodaan kulutositteesta tai myyntipalautustilaus asiakkaasta.

> [!NOTE]  
>   **Kuvaus**- ja **Nro**-kenttä täytetään luoduilla asiakirjariveillä vain, jos OCR-asiakirjasta löytynyt teksti on ensin linkitetty kahteen [!INCLUDE[d365fin](includes/d365fin_md.md)]in kenttään. Voit tehdä tämän yhdistämismäärityksen nimiketyyppisten asiakirjarivien nimikkeen ristiviittauksena. Lisätietoja on kohdassa [Nimikkeen viittausten käyttäminen](inventory-how-use-item-cross-refs.md). Voit käyttää myös Tekstin yhdistäminen tiliin -toimintoa. Lisätietoja on kohdassa [Saapuvan asiakirjan tekstin yhdistäminen tiettyyn toimittajaan, kirjanpitoon tai pankkitiliin](across-how-use-ocr-pdf-images-files.md#to-map-text-on-an-incoming-document-to-a-specific-vendor-account).

1. Valitse ensin saapuvan asiakirjan rivi ja sitten **Luo asiakirja** -toiminto.

[!INCLUDE[d365fin](includes/d365fin_md.md)]iin luodaan ostolasku OCR-palvelusta vastaanotetun toimittajan sähköisen laskun tietojen perusteella. Tiedot lisätään uuteen ostolaskuun sen yhdistämismäärityksen perusteella, jonka olet määrittänyt ristiviittaukseksi tai tekstin ja tilin yhdistämiselle.

Vahvistusvirheet (jotka yleensä liittyvät [!INCLUDE[d365fin](includes/d365fin_md.md)]in vääriin tai puuttuviin perustietoihin) näkyvät **Virheet ja varoitukset** -pikavälilehdessä. Lisätietoja on kohdassa [Virheiden käsitteleminen vastaanotettaessa sähköisiä asiakirjoja](across-how-use-ocr-pdf-images-files.md#to-handle-errors-when-receiving-electronic-documents).

### <a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a>Saapuvan asiakirjan tekstin yhdistäminen tietyn toimittajan tiliin
Saapuvissa asiakirjoissa käytetään yleensä **Linkitä teksti tiliin** -toimintoa, kun määritetään, että OCR-palvelusta vastaanotetun toimittajan laskun tietty teksti on linkitetty tiettyyn toimittajan tiliin. Jatkettaessa mikä tahansa saapuvan asiakirjan kuvauksen osa, joka on olemassa linkitettynä tekstinä, tarkoittaa sitä, että **Nro**-kenttä tuloksena saatavassa asiakirjassa tai päiväkirjariveillä, joiden tyyppi on KP-tili, täytetään kyseisen toimittajan tiedoilla.

Toimittajatiliin tai toiseen KP-tiliin linkittämisen lisäksi myös pankkitiliin voidaan linkittää. Tämä on käytännöllistä esimerkiksi sähköisille asiakirjoille, jotka on jo maksettu, johon haluat luoda yleisen päiväkirjarivin, joka on valmis kirjattavajsu pankkitilille.

1. Valitse ensin saapuvan asiakirjan rivi ja sitten **Tekstin yhdistäminen tiliin** -toiminto. **Tekstin yhdistäminen tiliin** -sivu avautuu.
3. Anna **Tekstin linkitys** -kentässä niihin toimittajalaskuihin sisältyvä teksti, joille haluat luoda ostoasiakirjoja tai päiväkirjarivejä. Koodissa voi olla enintään 50 merkkiä.
4. Anna **Toimittajan nro** -kentässä toimittaja, jolle muodostuva ostoasiakirja tai päiväkirjarivi luodaan.
5. Anna **Debet-tilin numero** -kentässä debet-tyyppinen KP-tili, joka lisätään muodostettavaan ostoasiakirjaan tai muodostettavalle KP-tili-tyyppiselle päiväkirjariville.
6. Anna **Kredit-tilin numero** -kentässä kredit-tyyppinen KP-tili, joka lisätään muodostettavaan ostoasiakirjaan tai muodostettavalle KP-tili-tyyppiselle päiväkirjariville.

    > [!NOTE]
    > Älä käytä saapuvien asiakirjojen yhteydessä **Saldon lähteen tyyppi**- ja **Saldon lähteen numero** -kenttiä. Niitä käytetään vain automaattisessa maksujen täsmäytyksessä. Lisätietoja on kohdassa [Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

7. Toista vaiheet 2–5 kaikkien niiden saapuvien asiakirjojen tekstien osalta, joille haluat luoda automaattisesti asiakirjat.

## <a name="to-handle-errors-when-receiving-electronic-documents"></a>Virheiden käsitteleminen vastaanotettaessa sähköisiä asiakirjoja
1. Valitse **Saapuvat asiakirjat** -sivulla OCR-palvelusta vastaanotetun sähköisen asiakirjan virheitä sisältävä rivi. Virhearvo **OCR-tila**-kentässä osoittaa virheen.
2. Valitse **Muokkaa** -toiminto, jonka jälkeen **Saapuva asiakirja** -sivu avautuu.
3. Valitse **Virheet ja varoitukset** -pikavälilehdessä sanoma ja valitse sitten **Avaa liittyvä tietue** -toiminto.
4. Vääriä tai puutteellisia tietoja sisältävä sivu (kuten toimittajakortti, josta puuttuu kenttäarvo) avautuu.
5. Korjaa virhe/virheet virhesanomassa kuvatulla tavalla.
6. Jatka saapuvan sähköisen asiakirjan käsittelemistä valitsemalla uudelleen **Luo manuaalisesti** -toiminto.
7. Toista vaiheet 5–6 kaikille jäljellä oleville virheille. Tämän jälkeen sähköinen asiakirja voidaan ottaa vastaan.

## <a name="to-train-the-ocr-service-to-avoid-errors"></a>OCR-palvelun kouluttaminen välttämään virheet
Koska OCR perustuu optiseen tunnistukseen, OCR-palvelu tulkitsee todennäköisesti PDF- tai kuvatiedostojesi merkit väärin, kun se käsittelee ensimmäistä kertaa esimerkiksi tietyn toimittajan asiakirjoja. Se ei ehkä tulkitse yrityksen logoa toimittajan nimeksi, tai se voi tulkita kulutositteen kokonaissumman väärin sen asettelun vuoksi. Voit välttää näitä virheitä vastaisuudessa korjaamalla OCR-palvelun vastaanottamat tiedot ja lähettämällä sitten palautteen palveluun.

**OCR-tietojen korjaus** -sivulla, joka avataan **Saapuneet asiakirjat** -sivulta, näkyvät **Rahoituksellisia tietoja** -pikavälilehden kentät kahdessa sarakkeessa. Toinen sarake sisältää muokattavat OCR-tiedot ja toinen vain luku -tilassa olevat OCR-tiedot. Kun valitset **Lähetä OCR-palaute** -painike, **OCR-tietojen korjaus** -sivun sisältö lähetetään OCR-palveluun. Seuraavan kerran, kun palvelu käsittelee kyseisiä tietoja sisältäviä PDF- tai kuvatiedostoja, korjaukset otetaan huomioon, jotta vältetään samat virheet.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvat asiakirjat** ja valitse sitten liittyvä linkki.
2. Avaa saapuva asiakirjatietue, joka sisältää OCR-palvelusta saadut tiedot, jonka haluat korjata.
3. Valitse **Saapuva asiakirja** -sivulla **Korjaa OCR-tiedot** -toiminto.
4. Korvaa **OCR-tietojen korjaus** -sivulla muokattavissa olevassa sarakkeessa kenttien virheelliset tiedot.
5. Voit kumota **OCR-tietojen korjaus** -sivun avaamisesta lähtien tehdyt korjaukset valitsemalla **Palauta OCR-tiedot** -toiminnon.
6. Lähetä korjaukset OCR-palveluun valitsemalla **Lähetä OCR-palaute** -toiminto.
7. Tallenna korjaukset sulkemalla **OCR-tietojen korjaus** -sivu.

**Saapunut asiakirja** -sivun **Rahoituksellisia tietoja** -pikavälilehden kenttiin päivitetään vaiheessa 4 antamasi uudet arvot.

## <a name="see-also"></a>Katso myös
[Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
