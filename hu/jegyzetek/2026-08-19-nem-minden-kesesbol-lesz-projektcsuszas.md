---
layout: post
title: "Nem minden késésből lesz projektcsúszás"
description: "Mit érdemes ellenőrizni, mielőtt egy célgép-, készülék- vagy automatizálási projektet elkezdünk kapkodva gyorsítani?"
date: 2026-08-19 22:00:00 +0200
lang: hu
permalink: /hu/jegyzetek/nem-minden-kesesbol-lesz-projektcsuszas/
categories: [Magyar szakmai jegyzetek]
tags: [projektvezetés, célgép, készülék, kritikus út, projektcsúszás, változáskezelés]
comments: false
toc: true
---

Egy célgép-, készülék- vagy automatizálási projekt ritkán fut pontosan úgy, ahogy az első ütemtervben szerepel.

Késhet egy beszállító.  
Tovább tarthat a mechanikai tervezés.  
Módosulhat egy interfész.  
Csúszhat egy gyártási tétel.  
Később érkezhet egy villamos komponens.  
Vagy egyszerűen kiderülhet, hogy a kiinduló feltételezés túl optimista volt.

Ilyenkor gyakori az első reakció:

**„A projekt csúszik. Valahogy hozzuk be.”**

Ez érthető reakció, de nem mindig jó projektvezetési logika.

A fontos kérdés ugyanis nem az, hogy valamelyik feladat késik-e.

Hanem az, hogy:

**a késés valóban módosítja-e a projekt várható befejezési dátumát?**

Ez a kettő nem ugyanaz.

## A kritikus út szerepe

A kritikus út az a feladatsor, amely meghatározza a projekt minimális átfutási idejét.

A példában egy félautomata szerelőállomás fő tevékenységei így néznek ki:

| ID | Tevékenység | Időtartam | Előfeltétel |
|---|---|---:|---|
| A | Követelmények lezárása | 2 nap | - |
| B | Mechanikai koncepció | 4 nap | A |
| C | Villamos koncepció | 3 nap | A |
| D | Mechanikai részlettervezés | 8 nap | B |
| E | Villamos részlettervezés | 5 nap | C |
| F | Gyártás | 10 nap | D |
| G | Vásárolt alkatrészek beszerzése | 12 nap | B |
| H | Mechanikai szerelés | 4 nap | F, G |
| I | Villamos szerelés | 3 nap | E, H |
| J | PLC-programozás és integráció | 5 nap | I |
| K | FAT | 2 nap | J |

A kritikus út ebben a példában:

```text
A → B → D → F → H → I → J → K
```

A kritikus úton lévő tevékenységek időtartama:

```text
Követelmények lezárása (A) = 2 nap
Mechanikai koncepció (B) = 4 nap
Mechanikai részlettervezés (D) = 8 nap
Gyártás (F) = 10 nap
Mechanikai szerelés (H) = 4 nap
Villamos szerelés (I) = 3 nap
PLC-programozás és integráció (J) = 5 nap
FAT (K) = 2 nap
```

A teljes időtartam ezen az útvonalon:

```text
2 + 4 + 8 + 10 + 4 + 3 + 5 + 2 = 38 nap
```

Ez a projekt minimális átfutási ideje:

```text
T_P = 38 munkanap
```

Ha ezen az útvonalon egy feladat egy nappal késik, és nincs más beavatkozás, akkor a projekt vége is egy nappal későbbre kerül.

Ezért egy célgép- vagy készülékprojektben nem elég tudni, hogy melyik feladat van késésben.

Azt is látni kell:

- melyik feladat melyik másiktól függ,
- mi a legkorábbi kezdés és befejezés,
- hol van időtartalék,
- mely feladatok vannak a kritikus úton,
- és melyek azok, amelyek közel kritikusak.

A közel kritikus feladatok különösen veszélyesek. Ezek még nem feltétlenül határozzák meg a végdátumot, de kevés tartalékuk van. Egy újabb kisebb késés után gyorsan kritikus feladattá válhatnak.

Ezért a projektcsúszás kezelésének első lépése nem a gyorsítás.

Hanem a helyzet tisztázása.

## Késés és projektcsúszás nem ugyanaz

Egy projektben sok feladat fut egymás mellett vagy egymás után. Vannak olyan feladatok, amelyek közvetlenül meghatározzák a végdátumot, és vannak olyanok, amelyek rendelkeznek valamennyi időtartalékkal.

Ha egy nem kritikus feladat késik, de még belefér az időtartalékába, akkor a projekt vége nem feltétlenül csúszik.

Tegyük fel, hogy a fenti példában a vásárolt alkatrészek beszerzése eredetileg a 18. napon zárulna. A következő mechanikai szerelési lépés azonban csak a 24. napon tudna indulni, mert addigra készül el a gyártott mechanikai alkatrészek másik ága.

Ebben az esetben a beszerzés időtartaléka:

```text
TF_G = 24 - 18 = 6 nap
```

Ha a beszállító négy nap késést jelez, akkor a beszerzés új befejezése:

```text
18 + 4 = 22 nap
```

A szerelés tervezett indulása továbbra is:

```text
24 nap
```

Mivel:

```text
22 < 24
```

a projekt végdátuma még nem változik.

A késés valós, de a projekt még nem csúszott. Csak az időtartalék csökkent:

```text
6 - 4 = 2 nap
```

Ezért veszélyes minden késést automatikusan projektcsúszásként kezelni.

A projektvezetőnek nem egyszerűen a „késő feladatokat” kell figyelnie, hanem a kritikus és közel kritikus feladatokat.

## Amikor a késés már valóban módosítja a projektet

Más a helyzet, ha egy kritikus úton lévő feladat késik.

Tegyük fel, hogy a mechanikai részlettervezés eredetileg 8 napos feladat volt, de valójában 11 nap alatt készül el.

A késés:

```text
11 - 8 = 3 nap
```

Ha ez a feladat a kritikus úton van, akkor változtatás nélkül a projekt új várható átfutása:

```text
T_új = 38 + 3 = 41 nap
```

Itt már nem csak egy feladat késik.

Itt a projekt várható befejezése is későbbre kerül.

Ez az a pont, ahol recovery döntésre van szükség.

## Az első hiba: mindenkit gyorsítani akarunk

Amikor egy projekt nyomás alá kerül, gyakori reakció, hogy mindenki próbáljon gyorsabban dolgozni.

Ez elsőre logikusnak tűnik, de sokszor nem hoz valódi határidőnyereséget.

Ha például egy villamos részlettervezési feladatot gyorsítunk, miközben a projekt vége valójában a mechanikai gyártásra és szerelésre vár, akkor lehet, hogy pénzt és energiát költöttünk, de a projekt végdátuma nem változott.

Ezért nem mindegy, hol avatkozunk be.

A határidő helyreállításához elsősorban ott kell időt nyerni, ahol a projekt vége ténylegesen eldől.

Ez általában a kritikus út.

## Mit kell először ellenőrizni?

Ha egy projektben késés jelenik meg, érdemes egy egyszerű sorrendet követni.

Először azt kell tisztázni, hogy mi történt ténylegesen.

Nem elég annyit mondani, hogy „csúszik a projekt”. Pontosan meg kell nevezni:

- melyik feladat késik,
- mennyit késik,
- mely következő feladatokat érinti,
- volt-e eredetileg időtartaléka,
- és mi az új várható befejezési dátum.

Ezután jön a kulcskérdés:

**kritikus úton van-e a késő feladat?**

Ha nincs, akkor meg kell nézni, mennyi időtartaléka maradt.

Ha a késés még belefér a tartalékba, akkor lehet, hogy nincs szükség drága vagy kockázatos beavatkozásra. Ilyenkor elég lehet szorosabb figyelés, beszállítói egyeztetés vagy a következő kapcsolódó feladatok előkészítése.

Ha viszont a késés kritikus úton van, vagy elfogyasztotta az időtartalékot, akkor valóban helyreállítási döntést kell hozni.

## Forecast: nem ugyanaz, mint a baseline

Projektvezetésben fontos különbség van az eredeti terv és az aktuális előrejelzés között.

Az eredeti, jóváhagyott terv a baseline.

Ez mutatja, mit vállaltunk: milyen határidővel, milyen scope-pal, milyen feltételekkel.

A forecast ezzel szemben az aktuális információk alapján várható befejezés.

Az előbbi példában az eredeti baseline:

```text
T_B = 38 nap
```

A kritikus úton lévő mechanikai részlettervezés késése után az aktuális forecast:

```text
T_F = 41 nap
```

Ez azonban nem jelenti azt, hogy az eredeti baseline-t egyszerűen át kell írni 41 napra.

Ha minden késés után átírjuk az eredeti tervet, elveszítjük az összehasonlítás lehetőségét.

Nem fogjuk látni, mennyire tértünk el az eredeti vállalástól, és azt sem, hogy a recovery intézkedések valóban javítottak-e a helyzeten.

Új baseline csak akkor indokolt, ha maga a projekt tartalma vagy feltételrendszere változik meg érdemben.

Például ha a vevő jelentősen bővíti a scope-ot, új munkadarabtípusokat kér, vagy olyan funkció kerül be, amely az eredeti projektben nem szerepelt, akkor már nem ugyanarról a tervről beszélünk.

De önmagában az, hogy „késtünk három napot”, nem jó ok az alapterv átírására.

## Négy lehetséges helyreállítási irány

Ha a projekt végdátuma tényleg veszélybe került, többféle beavatkozási lehetőség van.

Ezek közül egyik sem ingyenes.

Ha időt nyerünk, akkor általában valahol máshol fizetünk érte: költségben, kockázatban, scope-ban vagy szervezési terhelésben.

### 1. Crashing: több erőforrás, több költség

A crashing azt jelenti, hogy egy kritikus tevékenységet többleterőforrással próbálunk lerövidíteni.

Például több ember dolgozik rajta, külső gyártót vonunk be, túlórát rendelünk el, vagy gyorsított beszerzést választunk.

Ez általában pénzbe kerül.

A kérdés ilyenkor nem csak az, hogy mennyibe kerül a gyorsítás, hanem az is, hogy mennyi időt nyerünk vele.

Például a gyártás normál időtartama:

```text
F = 10 nap
```

Gyorsított időtartama:

```text
F = 8 nap
```

A nyereség:

```text
10 - 8 = 2 nap
```

A normál költség:

```text
600 000 Ft
```

A gyorsított költség:

```text
720 000 Ft
```

A többletköltség:

```text
720 000 - 600 000 = 120 000 Ft
```

Egy megnyert nap költsége:

```text
120 000 / 2 = 60 000 Ft/nap
```

Ez már összehasonlítható más recovery lehetőségekkel.

Egy másik kritikus feladat, például a PLC-programozás gyorsítása lehet:

```text
5 nap → 4 nap
```

A nyereség:

```text
1 nap
```

Ha a többletköltség:

```text
40 000 Ft
```

akkor az egy megnyert napra jutó költség:

```text
40 000 / 1 = 40 000 Ft/nap
```

Tisztán költség alapján először ez tűnik kedvezőbbnek.

De csak akkor, ha a gyorsítás műszakilag lehetséges, és nem növeli elfogadhatatlanul a hibakockázatot.

### A háromnapos késés visszanyerése crashinggel

Az előző példában a kritikus mechanikai részlettervezés miatt 3 nap késés keletkezett:

```text
38 nap → 41 nap
```

Ezt vissza lehet nyerni például két beavatkozással:

```text
PLC-programozás és integráció (J): 5 nap → 4 nap = 1 nap nyereség
Gyártás (F): 10 nap → 8 nap = 2 nap nyereség
```

Összes időnyereség:

```text
1 + 2 = 3 nap
```

Többletköltség:

```text
40 000 + 120 000 = 160 000 Ft
```

Az új forecast így visszakerülhet:

```text
41 - 3 = 38 nap
```

A határidő tehát elvileg tartható.

De nem ingyen.

Ebben a példában a három nap visszanyerésének közvetlen többletköltsége:

```text
160 000 Ft
```

### 2. Fast tracking: párhuzamosítás nagyobb kockázattal

A fast tracking más logika.

Ilyenkor nem feltétlenül több erőforrást használunk, hanem olyan feladatokat végzünk részben párhuzamosan, amelyek eredetileg egymás után következtek volna.

Például a teljes konstrukció lezárása előtt kiadjuk a kritikus alkatrészek rajzait, hogy a gyártás elindulhasson, miközben a kevésbé kritikus részek még véglegesítés alatt vannak.

Ez időt nyerhet.

De új kockázatot hoz létre.

Tegyük fel, hogy részleges rajzkiadással 3 nap nyerhető.

Viszont 20% esély van arra, hogy egy későbbi módosítás miatt 300 000 Ft újragyártási költség keletkezik.

Az egyszerű várható kockázati költség:

```text
EMV = P × C
```

A példában:

```text
EMV = 0,20 × 300 000
```

vagyis:

```text
EMV = 60 000 Ft
```

Ez nem azt jelenti, hogy a fast tracking biztosan 60 000 Ft-ba kerül.

Azt jelenti, hogy a döntés várható pénzügyi kockázata ennyi.

Első látásra ez kedvezőbbnek tűnhet, mint a 160 000 Ft-os crashing.

De további kérdések nélkül nem szabad dönteni:

- mekkora a maximális újragyártási veszteség?
- veszélyezteti-e az újragyártás magát a határidőt?
- biztonsági funkciót érint-e?
- visszafordítható-e a döntés?
- mennyire stabilak az előre kiadott rajzok?
- hogyan kezeljük a verziókat?

A fast tracking tehát nem egyszerű „ügyes gyorsítás”.

Ez tudatos kockázatvállalás.

Csak akkor használható felelősen, ha pontosan meghatározzuk, mely elemek elég stabilak az előrehozott kiadáshoz, és hogyan kezeljük a változásokat.

### 3. Műszaki alternatíva: konstrukciós döntéssel időt nyerni

A projektcsúszás néha nem projektvezetési, hanem műszaki döntéssel kezelhető.

Például egy egyedi alkatrész vagy speciális lineáris egység hosszú szállítási ideje miatt csúszna a projekt. Ilyenkor lehet, hogy nem a gyártás gyorsítása a legjobb megoldás, hanem egy standard alternatíva keresése.

Ha egy egyedi egység szállítási ideje:

```text
8 hét
```

egy standard alternatíváé pedig:

```text
2 hét
```

akkor a nyereség első ránézésre jelentős lehet.

Ehhez viszont szükség lehet például:

```text
12 óra konstrukciómódosításra
```

Ez igényelhet új beépítési megoldást, új ellenőrzést, rajzmódosítást vagy kisebb áttervezést.

De ha egy hosszú szállítási idejű elem kiváltható egy gyorsabban elérhető standard megoldással, akkor a projekt egészére nézve ez lehet a legjobb recovery döntés.

Ez különösen célgép- és készülékprojektekben fontos.

Itt a projektvezetés, a konstrukció, a DFM, a beszerzés és a kockázatkezelés nem választható szét teljesen.

Egy jó műszaki alternatíva néha többet ér, mint egy drága gyorsítás.

### 4. Scope-módosítás: csak jóváhagyással

A negyedik lehetőség a scope módosítása.

Ez nem azt jelenti, hogy csendben kihagyunk valamit a projektből.

Azt jelenti, hogy tudatosan megvizsgáljuk: minden funkciónak készen kell-e lennie az első átadáskor, vagy lehet-e bizonyos nem kritikus elemeket későbbi fázisba tenni.

Például egy automatikus riportfunkció további 3 nap programozást igényelhet, miközben a gép alapműködéséhez nem feltétlenül szükséges az első átadáskor.

Ilyenkor lehetséges döntés lehet:

```text
Phase 1:
- gép működőképes
- biztonság validálva
- termelés indítható

Phase 2:
- automatikus riport
- kényelmi funkciók
```

De ez csak akkor korrekt, ha jóváhagyott változásként kezeljük.

A scope nem módosítható csendben azért, hogy a projekt papíron időben elkészüljön.

Ehhez Change Request kell, amely rögzíti:

- mi változik,
- miért változik,
- mi az időhatás,
- mi a költséghatás,
- mi a műszaki hatás,
- milyen új kockázat keletkezik,
- és ki hagyta jóvá.

Ez nem adminisztrációs teher, hanem védelmi eszköz.

Védi a vevőt, a projektcsapatot és a későbbi értelmezést is.

## Amit nem szabad egyszerűen kihagyni

Határidőnyomás alatt könnyű rossz kompromisszumot kötni.

Vannak elemek, amelyeket nem szabad egyszerű schedule-recovery eszközként kezelni.

Ilyen lehet például:

- gépbiztonsági validáció,
- kritikus terhelési próba,
- FAT lényegi része,
- kötelező dokumentáció,
- kockázatos alkatrész elfogadása ellenőrzés nélkül,
- vagy olyan ellenőrzés, amely a későbbi üzembiztonságot érinti.

Ezek kihagyása látszólag időt nyerhet.

Valójában sokszor csak áthelyezi a kockázatot a későbbi üzemeltetésre, a vevői átvételre vagy a garanciális időszakra.

Ez nem valódi projektmentés.

Ez kockázat elrejtése.

## A projekt háromszöge mérnöki környezetben

A klasszikus projektlogika szerint három tényező kapcsolódik össze:

```text
scope - time - cost
```

Ha az egyiket megváltoztatjuk, a másik kettőre is hatunk.

Mérnöki projektekben ehhez még hozzá kell tenni:

```text
quality / risk
```

Mert egy célgép, készülék vagy automatizálási állomás esetében nem elég az, hogy valami határidőre elkészül.

Működnie kell.  
Biztonságosnak kell lennie.  
Gyárthatónak kell lennie.  
Szerelhetőnek kell lennie.  
Dokumentálhatónak kell lennie.  
És hosszabb távon is kezelhető kockázatot kell jelentenie.

Ezért az a mondat, hogy:

**„ugyanazt, ugyanannyi pénzből, ugyanazon minőségben, csak három nappal gyorsabban”**

sokszor nem valódi opció.

Valaminek változnia kell.

Több költség.  
Kisebb scope.  
Nagyobb kockázat.  
Műszaki alternatíva.  
Vagy ezek kombinációja.

## Minden beavatkozás után újra kell számolni

Fontos, hogy a kritikus út nem örökre rögzített.

Ha egy kritikus feladatot lerövidítünk, előfordulhat, hogy egy másik ág válik kritikussá.

Például ha a gyártási feladatot jelentősen gyorsítjuk:

```text
F: 10 nap → 4 nap
```

akkor a gyártás befejezése:

```text
14 + 4 = 18 nap
```

Ha a beszerzési ág is a 18. napon fejeződik be, akkor már nem csak a gyártás, hanem a beszerzés is kritikussá válik.

További gyártásgyorsítás ilyenkor már nem biztos, hogy rövidíti a projektet, mert a szerelés továbbra is a beszerzésre vár.

Ezért minden jelentős recovery döntés után újra kell ellenőrizni a hálótervet.

Nem elég egyszer megtalálni a kritikus utat a projekt elején.

A projektkontroll folyamatos tevékenység.

## A recovery nem írja felül a kockázatkezelést

Amikor gyorsítani próbálunk, gyakran új kockázatokat hozunk létre.

Fast tracking esetén például megjelenhet:

- részlegesen jóváhagyott rajzból történő gyártás,
- rajzmódosítás miatti újragyártás,
- verziókeveredés,
- szerelési inkompatibilitás,
- vagy beszállítói egyeztetési hiba.

Ezeket nem elég fejben tartani.

Be kell kerülniük a Risk Registerbe vagy legalább egy egyszerű kockázati listába.

A recovery tehát nem azt jelenti, hogy félretesszük a kockázatkezelést.

Hanem azt, hogy frissítjük.

## Egyszerű döntési sorrend projektcsúszás esetén

Ha egy célgép-, készülék- vagy automatizálási projekt csúszni kezd, érdemes egy következetes sorrendet használni.

1. Mi történt ténylegesen?
2. Melyik feladat érintett?
3. Kritikus úton van?
4. Mennyi időtartaléka volt?
5. Mennyi időtartaléka maradt?
6. Mi az új forecast?
7. Eltér-e a vállalt végdátumtól?
8. Mely kritikus feladat rövidíthető?
9. Van crashing lehetőség?
10. Van fast tracking lehetőség?
11. Van műszaki alternatíva?
12. Módosítható-e a scope?
13. Milyen új kockázat keletkezik?
14. Kell-e Change Request?
15. Mi az új hálóterv?

Ez sokkal jobb módszer, mint az, hogy:

**„mindenki próbáljon gyorsabban dolgozni.”**

## Tanulság

A projektcsúszás kezelésének első lépése nem a kapkodás.

Hanem annak megértése, hogy a késés valóban veszélyezteti-e a végdátumot.

Ehhez három dolgot kell tisztán látni:

```text
kritikus út + időtartalék + aktuális forecast
```

Ha a projekt vége nincs veszélyben, akkor lehet, hogy nincs szükség drága vagy kockázatos gyorsításra.

Ha viszont a végdátum tényleg veszélybe került, akkor a beavatkozást kontrolláltan kell kiválasztani.

Lehet gyorsítani többletköltséggel.  
Lehet párhuzamosítani nagyobb kockázattal.  
Lehet műszaki alternatívát keresni.  
Lehet scope-ot módosítani jóváhagyott változásként.

De mindegyik döntésnek ára van.

A projektvezető feladata nem egyszerűen az, hogy mindenáron védje a határidőt.

Hanem az, hogy a határidő helyreállítása közben ne hozzon létre nagyobb műszaki vagy üzleti problémát annál, mint amit megpróbál megoldani.

## Letölthető segédlet

A témához készül egy részletesebb, kitölthető projektkontroll munkalap is:

**GUBA-HU-PM-01 – Projektcsúszás kezelési vizsgálólap**

A segédlet célja, hogy csúszás esetén strukturáltan végig lehessen nézni:

- melyik feladat csúszott,
- kritikus úton van-e,
- mennyi időtartalék maradt,
- hogyan változik a forecast,
- milyen recovery lehetőségek vannak,
- milyen költség- és kockázati hatásuk van,
- szükséges-e Change Request,
- és milyen új hálótervet kell követni.

A cél nem az, hogy minden késést túladminisztráljunk.

A cél az, hogy a fontos projektmentési döntések ne kapkodásból, hanem átlátható műszaki és üzleti logika alapján szülessenek meg.
