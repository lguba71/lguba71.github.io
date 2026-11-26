---
layout: post
title: "Műszaki bizonytalanság: mikor szabad továbblépni egy projektben?"
description: "Hogyan kezeljük a nyitott műszaki kérdéseket, hogy a feltételezések ne váljanak költséges konstrukciómódosításokká?"
date: 2026-11-26 12:00:00 +0100
lang: hu
permalink: /hu/jegyzetek/muszaki-bizonytalansag-mikor-szabad-tovabblepni-egy-projektben/
categories: [Magyar szakmai jegyzetek]
tags: [projektvezetés, műszaki bizonytalanság, célgép, tervezés, döntési kapu, műszaki ellenőrzés]
comments: false
toc: true
---

*Hogyan kezeljük a nyitott műszaki kérdéseket, mielőtt egy hibás feltételezésből költséges konstrukciómódosítás lesz?*

Egy célgép- vagy automatizálási projektben ritkán ismerünk minden műszaki részletet már a tervezés kezdetén. Nem biztos, hogy pontosan ismerjük a dinamikus terheléseket. Nem tudjuk, hogy egy megfogó megfelelően működik-e olajos alkatrészekkel. Kérdéses lehet egy beszállító gyártási képessége, egy szerkezeti elem merevsége vagy több részegység együttes működése. Ezek önmagukban nem feltétlenül jelentenek problémát. A mérnöki tervezés természetes részei. A nehézség akkor kezdődik, amikor a projekt halad előre, a nyitott kérdések viszont megválaszolatlanok maradnak.

Elindul a részlettervezés. Kiadjuk a gyártási rajzokat. Megrendeljük a hosszú szállítási idejű alkatrészeket. Megkezdődik a szerelés. Egy korábban még viszonylag egyszerűen kezelhető bizonytalanság ekkor már jelentős költséget és késést okozhat. A kérdés tehát nem az, hogy minden bizonytalanságot meg tudunk-e szüntetni. Hanem az, hogy

**Melyik kérdésre, milyen biztosítékra és mikorra van szükségünk ahhoz, hogy felelősen továbbengedhessük a projektet.**

## A kockázat és a műszaki bizonytalanság nem ugyanaz

A két fogalom szorosan kapcsolódik egymáshoz, de nem teljesen azonos. Tegyük fel, hogy egy kritikus hajtómű szállítása 30% valószínűséggel 10 napot késhet. Ebben az esetben egy ismert lehetséges eseménnyel és becsült következménnyel számolhatunk. Egyszerű várható időhatás:

**E = P × I = 0,30 × 10 = 3 nap**

Ez nem jelenti azt, hogy a projekt ténylegesen három napot fog késni. Az érték egy egyszerű valószínűségi becslés, amelynek hatása a projektütemezésére a kritikus úttól és az időtartalékoktól is függhet.

Most nézzünk egy másik helyzetet. Kiválasztottunk egy lineáris vezetéket, de nem tudjuk, hogy a dinamikus merevsége elegendő-e a számított terheléshez. Itt nem feltétlenül tudunk megbízható valószínűséget rendelni a meghibásodáshoz. Lehet, hogy a modellünk hiányos, vagy a valós üzemi viselkedésről nincs elegendő információnk. Ez a műszaki bizonytalanság. A gyakorlatban a kockázat és a bizonytalanság gyakran együtt jelenik meg. A különbségtétel azonban fontos, mert nem ugyanazzal a módszerrel kezeljük őket.

Egy becsülhető kockázathoz tartalékot, megelőző intézkedést vagy alternatív tervet rendelhetünk. Egy hiányzó műszaki ismeret megszerzéséhez viszont számításra, vizsgálatra, mérésre vagy kísérletre lehet szükség.

## A műszaki bizonytalanság négy típusa

Célgép- és automatizálási projektekben célszerű legalább négy területet megkülönböztetni.

| Terület | Tipikus kérdés |
|---|---|
| Követelmények | Pontosan minek kell megfelelnie a gépnek? |
| Konstrukció | Működni fog a választott műszaki megoldás? |
| Gyártás | A tervezett alkatrész stabilan és gazdaságosan előállítható? |
| Integráció | A külön-külön megfelelő részegységek együtt is teljesítik a követelményeket? |

Egy egyszerű példa jól mutatja, miért fontos ez a különbség. A vevő azt mondja, hogy a gép legyen gyors. Ez nem megfelelően meghatározott követelmény.

- Húsz vagy negyven darabot kell percenként gyártani?

- Mennyi a megengedett selejt?

- Mi történik termékváltáskor?

- Milyen rendelkezésre állást kell teljesíteni?

Ha húsz darab/perces teljesítményre tervezzük a gépet, majd a projekt előrehaladott állapotában kiderül, hogy negyven darab/perc a valódi elvárás, az nem egyszerű paramétermódosítás. Ez érintheti a hajtásokat, a mozgatott tömegeket, a megfogót, a gépvázat, a vezérlést és a biztonsági megoldásokat is. Ezt a bizonytalanságot nem végeselemes analízissel vagy prototípussal kell először kezelni, hanem a követelmények egyértelmű tisztázásával.

Más a helyzet akkor, amikor a követelmény ismert, de nem tudjuk, hogy a konstrukciónk megfelel-e neki. Ott már valóban indokolt lehet egy számítás, szimuláció vagy célzott próba.

**A helyes vizsgálati módszer kiválasztásához először azt kell tudni, milyen jellegű kérdésre keressük a választ.**

## A bizonytalanság ára a projekt előrehaladtával nő

Egy koncepció módosítása gyakran viszonylag kevés ráfordítást igényel. Ugyanez a módosítás a részletes CAD-modell elkészülése után már több munkát jelenthet. Gyártás után új alkatrészekre, szerelés után bontásra és újraépítésre lehet szükség. Az összefüggés szemléletesen:

**C(koncepció) &lt; C(részlettervezés) < C(gyártás után)**

Ez nem minden esetben érvényes költségtörvény, hanem gyakori projektgazdasági tendencia. Különösen igaz a nehezen módosítható vagy hosszú átfutású részegységekre. Tegyük fel, hogy egy kritikus golyós orsó szállítási ideje nyolc hét. A rendelés leadása után a konstrukció módosítása már jelentős költséget és késést okozhat. A rendelés ezért egy fontos elköteleződési pont (commitment point). A kapcsolódó műszaki kérdéseket még a rendelés előtt kell megfelelő bizonyossággal tisztázni. Ez nem jelenti azt, hogy a projekt minden nyitott kérdését azonnal meg kell válaszolnunk. A cél az, hogy az adott döntéshez szükséges információ rendelkezésre álljon, mielőtt a hibás döntés visszafordítása túl költségessé válik.

## Nem a naptári dátum, hanem a bizonyíték számít

Sok projektben találkozunk olyan mérföldkövekkel, mint:

- Concept Freeze

- Design Freeze

- Manufacturing Release

- FAT Readiness

Ezek hasznosak, de önmagukban a naptárba beírt dátumok még nem igazolják a műszaki készültséget. Például a Design Freeze nem attól indokolt, hogy elérkezett a kijelölt nap. Akkor van valódi jelentősége, ha az előírt követelmények teljesülését alátámasztó bizonyítékok rendelkezésre állnak. Ilyenek lehetnek a lezárt követelmények, meghatározott interfészek, ellenőrzött terhelési esetek, tűréslánc-vizsgálatok, gyárthatósági egyeztetések és a kritikus komponensek jóváhagyása. Fontos különbség van aközött, hogy:

**„A CAD-modell 100%-ban elkészült.”**

és aközött, hogy:

**„A konstrukció gyártásra kiadható műszaki állapotban van.”**

Lehet teljes a geometria, de egy fontos terhelési eset még nincs ellenőrizve, a hajtás kiválasztása bizonytalan, vagy a beszállító még nem igazolta egy kritikus méret gyárthatóságát. A CADkészültség tehát nem azonos a műszaki igazoltsággal. A projektvezetési mérföldkövekhez ezért érdemes egyértelmű elfogadási feltételeket rendelni.

## Mennyi bizonyíték elegendő?

Nem minden döntéshez szükséges ugyanolyan részletességű vizsgálat. Egy egyszerű burkolatrögzítéshez többnyire nincs szükség teljes fizikai prototípusra. Egy nagy tömegű, dinamikusan mozgó mechanizmusnál viszont egy durva becslés nem feltétlenül elegendő. A bizonyítékok érettségét szemléltetésként öt szintbe sorolhatjuk:

| Szint | A rendelkezésre álló bizonyíték |
|---|---|
| L0 | Feltételezés, mérnöki megérzés |
| L1 | Előzetes mérnöki becslés |
| L2 | Részletes számítás vagy szimuláció |
| L3 | Fizikai komponens- vagy részrendszerpróba |
| L4 | Integrált, rendszerszintű vizsgálat |

Ez egy szemléltető besorolás, nem általános szabványos minősítési rendszer. A cél nem az, hogy minden kérdéshez a legmagasabb szintű igazolás készüljön. Az ellenőrzés mélységének arányban kell állnia a bizonytalansággal és egy hibás döntés következményeivel. Néha a számítás a legjobb eszköz. Máskor egy néhány órás fizikai teszt lényegesen értékesebb.

## Példa: egy megfogó kiválasztása

Tegyük fel, hogy egy célgéphez olyan kétpofás megfogót választunk, amelynek egy 8 kg tömegű alkatrészt kell mozgatnia.

Tömeg: m=8 kg

Gyorsulás: a = 15 m/s²

Az ebből származó tehetetlenségi erő nagysága:

**F = m × a = 8 × 15 = 120 N**

Ha erre a terhelési összetevőre 2-es méretezési tényezőt alkalmazunk:

**Freq = 2 × 120 = 240 N**

Tegyük fel továbbá, hogy a két pofa súrlódással tartja a munkadarabot, és a szorítóerő pofánként azonos. Az egyszerűsített modell szerint:

**Fhold = 2 × μ × N**

ahol μ a súrlódási tényező, N pedig egy pofa normálerője.

Ha a becsült súrlódási tényező: **μ = 0,12**

akkor:

**N ≥ 240 / (2 × 0,12) = 1000 N/pofa**

Ezzel megkaptunk egy első méretezési értéket. De mi történik, ha a munkadarab olajos felületű, és a tényleges súrlódási tényező csak μ = 0,05?

**N ≥ 240 / (2 × 0,05) = 2400 N/pofa**

A szükséges szorítóerő több mint kétszeresére nőtt.

Ez már a megfogó kiválasztását és akár az egész koncepciót is megváltoztathatja. A számítás egyszerűsített, és nem helyettesíti a teljes megfogási biztonság igazolását. A valós terhelési irányokat, gravitációs hatásokat, gyorsulási csúcsokat, kontakt geometriát és egyéb követelményeket is ellenőrizni kell. A projektvezetési tanulság azonban egyértelmű. A kritikus bizonytalanság ebben a példában nem a tömeg vagy a gyorsulás, hanem a súrlódási viselkedés. Ennek csökkentésére célravezető lehet egy gyors fizikai próba a valódi munkadarabbal, pofa anyagával és jellemző felületi állapottal. Nem kell feltétlenül teljes gépprototípust építeni.

**Olyan minimális vizsgálatot érdemes készíteni, amely közvetlenül a döntést befolyásoló bizonytalanságra ad választ.**

Különösen akkor, ha a megfogót néhány napon belül meg kell rendelni.

## A vizsgálat nemcsak költség, hanem információ is

A mérnöki elemzéseket és próbákat gyakran kizárólag költségként kezeljük. Pedig egy jól megválasztott vizsgálat gazdasági értéke abban is megjelenik, hogy elkerülhetővé tesz egy rossz döntést. Nézzünk egy egyszerű példát amikor két konstrukció közül választunk.

Az A változat alapára 10 millió Ft, de 30% valószínűséggel további 4 millió Ft átalakítási költséget okoz. A várható költség:

**EA = 10 + 0,30 × 4 = 11,2 millió Ft**

A B változat költsége 11 millió Ft, és az adott probléma szempontjából lényegesen kisebb kockázatú.

A rendelkezésre álló adatokkal tehát B tűnik kedvezőbbnek. Van azonban egy 100 000 Ft-os teszt, amely nagy megbízhatósággal segíthet eldönteni, hogy A esetében fennáll-e az átalakítás szükségessége. Ha tökéletes információval rendelkeznénk, probléma nélkül A-t, probléma esetén B-t választhatnánk. A várható költség ebben az elméleti esetben:

**Einfo = 0,70 × 10 + 0,30 × 11 = 10,3 millió Ft**

A tökéletes információ legnagyobb várható gazdasági értéke:

**11 − 10,3 = 0,7 millió Ft**

Vagyis az információ akár 700 000 Ft várható értéket is jelenthet a vizsgált döntési helyzetben. Ez elméleti felső korlát. Egy valódi teszt nem feltétlenül ad tökéletes információt, és a vizsgálat költségét, tévedési lehetőségeit, valamint időhatását is figyelembe kell venni. A lényeg azonban nem maga a számítás. Hanem az, hogy

**egy jókor elvégzett vizsgálat nemcsak ellenőriz, hanem egy költséges döntést is megalapozhat.**

## Nem minden kérdést kell azonnal lezárni

A másik véglet az, amikor a projekt túl sok elemzés miatt nem tud előre haladni. Még egy szimuláció. Még egy pontosítás. Még egy számítás. A további vizsgálat akkor indokolt, ha várhatóan érdemben megváltoztathatja a döntést, vagy szükséges a megfelelő műszaki bizonyíték megszerzéséhez. Ha például a konstrukció megfelelő tartalékkal rendelkezik, a modell ismert, és egy újabb elemzés várhatóan nem módosítaná a választott megoldást, akkor a további részletezés nem feltétlenül értékteremtő. Ugyanez érvényes az alternatív koncepciókra is. Nem szükséges mindig az első héten véglegesen kiválasztani egyetlen megoldást. Ha két konstrukció közötti döntést egy kétnapos próba megalapozhatja, célszerű lehet mindkettőt fenntartani addig, amíg az eredmény megérkezik. Ez nem döntésképtelenség. A különbség az, hogy tudjuk, milyen információra várunk, mikor kapjuk meg, és meddig halasztható a döntés a projekt veszélyeztetése nélkül.

## A nyitott műszaki kérdéseket külön is követni kell

A hagyományos kockázati lista mellé hasznos lehet egy műszaki bizonytalanságokat nyilvántartó táblázat. Nem elegendő például annyit beírni, hogy „megfogó kockázat – közepes”.

Sokkal hasznosabb, ha rögzítjük, hogy pontosan mit nem tudunk, milyen következménye lenne egy hibás feltételezésnek, milyen vizsgálat szükséges, ki felel érte, és mely döntés előtt kell eredményre jutni. Például:

| Nyitott kérdés | Feloldási módszer | Határidő |
|---|---|---|
| Megfelelő-e a megfogó olajos alkatrészhez? | Fizikai megfogási próba | Megfogó rendelése előtt |
| Teljesíthető-e a kritikus furatpozíció? | Beszállítói próbagyártás | Rajzkiadás előtt |
| Teljesül-e a 12 s-os ciklusidő? | Integrált idővizsgálat | Koncepció lezárása előtt |

Ezt kiegészíthetjük felelőssel, státusszal, bizonyítékkal és az elmaradó döntés várható következményével. A feltételezéseket is érdemes külön megjelölni. Például az, hogy „a munkadarab felülete mindig száraz”, nem válik attól igazolt ténnyé, hogy mindenki erre építette a konstrukcióját. Egy dokumentált feltételezés ellenőrizhető. Egy elfelejtett feltételezés viszont később észrevétlenül beépülhet a végleges gépbe.

## Mikor kerül veszélyes állapotba a projekt?

A projekt előrehaladtával természetes, hogy egyre több műszaki döntést véglegesítünk. Ezzel párhuzamosan viszont a fontos bizonytalanságok számának és jelentőségének csökkennie kellene. A legkedvezőtlenebb helyzet akkor alakul ki, amikor már sok pénzt és időt kötöttünk le, miközben a kritikus műszaki kérdések továbbra is nyitottak. Például a gépváz már legyártva, a hajtások megrendelve, a szerelés megkezdődött, de a tényleges dinamikus terhelés vagy egy kritikus interfész működése még nincs igazolva. Egy ilyen projekt nem feltétlenül azért veszélyes, mert sok benne a probléma. Hanem azért, mert a még megválaszolatlan kérdésekre adott válaszok már nehezen és drágán vezethetők át a konstrukción. Ezért a projektvezetésben a bizonytalanságok követését össze kell kapcsolni a döntési és elköteleződési pontokkal.

## Öt kérdés, amelyet érdemes minden kritikus döntés előtt feltenni

Mielőtt kiadunk egy gyártási rajzot, megrendelünk egy drága komponenst vagy lezárunk egy fontos konstrukciós döntést, érdemes végig gondolni:

1. Mit nem tudunk még biztosan?

2. Mi történik, ha a feltételezésünk hibásnak bizonyul?

3. Mikor válik költségessé vagy nehezen visszafordíthatóvá a döntés?

4. Milyen számítás, mérés vagy minimális próba adhat megfelelő bizonyítékot?

5. Milyen eredmény vagy elfogadási feltétel esetén engedhetjük tovább a projektet?

Ez a gondolkodás nem helyettesíti a műszaki tervezést és a kockázatkezelést. Segít viszont abban, hogy a rendelkezésre álló mérnöki kapacitást ne egyenletesen osszuk el minden nyitott kérdés között, hanem azokra fordítsuk, amelyek a következő fontos döntést valóban befolyásolják.

## Összefoglalás

Egy műszaki projektben soha nem lesz minden információ teljesen biztos. Ez önmagában nem probléma. A probléma az, ha nem tudjuk, melyik feltételezés bizonytalan, milyen következménye lehet a tévedésnek, és meddig kell megszereznünk a szükséges bizonyítékot. A hatékony műszaki projektvezetés ezért nem minden kérdés azonnali lezárását jelenti. Hanem azt, hogy

**a kritikus bizonytalanságokat még azelőtt csökkentsük elfogadható szintre, mielőtt az adott döntés visszafordítása túl költségessé válna.**

Egy időben elvégzett számítás, egy jól megválasztott részpróba vagy egy megfelelően előkészített műszaki egyeztetés sokszor többet ér, mint egy későbbi, kapkodva végrehajtott konstrukciómódosítás.

---

**Kapcsolódó jegyzet:** [Nem minden késésből lesz projektcsúszás](/hu/jegyzetek/nem-minden-kesesbol-lesz-projektcsuszas/) – kritikus út, időtartalék és kontrollált újratervezés.
