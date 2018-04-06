---
title: Myynti- ja ostoasiakirjojen arkistointi | Microsoft Docs
description: "Voit arkistoida myynti- ja ostotilauksia, tarjouksia, palautustilauksia ja puitetilauksia. Voit myös käyttää arkistoitua asiakirjaa ja luoda uudelleen asiakirjan, josta ne arkistoitiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a>Asiakirjojen arkistointi
Voit arkistoida myynti- ja ostotilauksia, tarjouksia, palautustilauksia ja puitetilauksia. Voit myös käyttää arkistoitua asiakirjaa ja luoda uudelleen asiakirjan, josta ne arkistoitiin.

## <a name="to-set-up-automatic-document-archiving"></a>Asiakirjojen automaattisen arkistoinnin määrittäminen  
Voit määrittää myynti- ja ostotilausten, tarjousten, puitetilausten ja palautustilausten automaattisen arkistoinnin ennen asiakirjojen poistamista.

Seuraavassa kuvataan, miten myyntiasiakirjojen automaattinen arkistointi määritetään. Vaiheet ovat samankaltaiset ostoasiakirjoille.
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntien ja myyntisaamisten asetukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Täytä kentät **Myyntien ja myyntisaamisten asetukset** -ikkunassa seuraavasti.

|Kenttä|Description|
|-----|-----------|
|**Myyntitarjousten arkistointi**|**Ei koskaan**, jos myyntitarjouksia ei arkistoida koskaan poistamisen yhteydessä. **Kysymys**, kun käyttäjältä kysytään myyntitarjousten arkistoinnista tarjousten poistamisen yhteydessä. **Aina**, kun myyntitarjoukset arkistoidaan automaattisesti poistamisen yhteydessä.|
|**Puitemyyntitilausten arkistointi**|Puitemyyntitilaukset arkistoidaan automaattisesti aina poistamisen yhteydessä.|
|**Arkist. tilaukset ja pal.tilaukset**|Myyntitilaukset arkistoidaan automaattisesti aina poistamisen yhteydessä.|

## <a name="to-archive-a-sales-order"></a>Myyntitilauksen arkistointi
Seuraavassa kuvataan, miten myyntitilaus arkistoidaan. Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille.

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Avaa myyntitilaus, jonka haluat arkistoida.  
3.  Valitse **Arkistoi asiakirja** -toiminto.

Myyntitilaus on arkistoitu. Voit tarkastella sitä **Arkistoidut myyntitilaukset** -ikkunassa. Ikkunassa voit myös luoda uudelleen myyntitilauksen, josta se arkistoitiin.

## <a name="to-recreate-a-sales-order-from-the-archive"></a>Myyntitilauksen luominen uudelleen arkistosta
Seuraavassa kuvataan, miten myyntitilaus luodaan uudelleen. Vaiheet ovat samankaltaiset kaikille tilauksille, puitetilauksille, palautustilauksille ja tarjouksille.

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Arkistoidut myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.
2.  Valitse arkistoitu myyntitilaus, joka luodaan uudelleen, ja valitse sitten **Palauta**-toiminto.  

Myyntitilaus luodaan ja lisätään **Myyntitilaukset**-ikkunaan.

## <a name="to-delete-archived-sales-orders"></a>Arkistoitujen myyntitilausten poistaminen
Seuraavassa kuvataan, miten arkistoidut myyntitilaukset poistetaan. Vaiheet ovat samanlaiset muille arkistoiduille myynti- ja ostoasiakirjoille.

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Poista arkistoidut myyntitilausversiot** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Poista arkistoidut myyntitilausversiot** -ikkunassa sopivat suodattimet.  
3.  Valitse **OK**-painike.

## <a name="see-also"></a>Katso myös
[Asiakirjarivien seuranta](across-how-to-track-document-lines.md)  
[Myynti](sales-manage-sales.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

