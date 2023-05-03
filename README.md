# szoftvertervezes-HF

Feladatunk: 11. Két féléves diplomaterv első féléve után a beadott dolgozat kiküldése tanszéki kollégák/bírálók részére (konzulens).

## Elsődleges Aktorok

### Hallgató
A Hallgató olyan személy, aki az Egyetemmel hallgatói jogviszonyban van és  teljesítette a Szakdolgozat-készítés vagy Diplomatervezés tárgyakhoz tartozó mérföldköveket.

### Szakvezető
Szakvezető leírása

### Tanszékvezető
Tanszékvezető leírása

### Tanszéki kolléga
pl. konzulens, belső, szigorúan xd

### Tanszéki ügyintéző

## Másodlagos Aktorok
### Címtár
rövid leírás arról, hogy ez mi

### Ügy
rövid leírás arról, hogy ez mi

### Diplomaterv Kiírás
rövid leírás arról, hogy ez mi

### Bírálat
rövid leírás arról, hogy ez mi

### Bíráló
A Szakdolgozat vagy Diplomaterv értékelésére felkért, a munka elkészítésétől jól elhatárolható személy. A bírálónak legalább olyan szintű ISCED besorolású végzettséggel kell rendelkezzen, mint amit az általa bírált mű sikeres megvédésével el lehet érni.



## Use Case-ek

### UC1: Dolgozat feltöltése
- Aktorok: Hallgató
- Előfeltételek:
  - A Hallgató be van jelentkezve
  - Van érvényes témakiírása (tehát volt adatlap, konzulens stb.)
- Elsődleges forgatókönyv:
  1. A Hallgató kiválasztja a fájl feltöltése funkciót.
  2. A Rendszer megjeleníti a Feltöltési felületet.
  3. A Hallgató behúzza a feltölteni kívánt fájlt vagy Böngésző fájlfeltöltő funkciójával kiválasztja feltöltendő fájlt
  4. A Rendszer ellenőrzi a fájl nevét, kiterjesztését és a méretét.
  5. A Hallgató megerősíti a feltöltést a mentés gombra kattintással.
  6. A Rendszer iktatja a feltöltött dokumentumot.

Alternatív forgatókönyv:
- 4/a A Rendszer jelzi, hogy a kiválasztott fájl neve nem megfelelő formátumú. A use case a 2. lépéssel folytatódik.
- 4/b A Rendszer jelzi, hogy a kiválasztott fájl kiterjesztése nem megfelelő. A use case a 2. lépéssel folytatódik.
- 4/c A Rendszer jelzi, hogy a kiválasztott fájl mérete nem megfelelő. A use case a 2. lépéssel folytatódik.


### UCX: Feltöltés iktatása

### UCX: Dolgozat leadása
- Aktor: Hallgató
- Előfeltétel:
  - Feltöltötte a hallgató a dolgozatot és az iktatásra került.
  > :memo: **Note:** Legyen menthető a rendszerben egy átmeneti állapot a végleges leadás előtt. (A rendszer ne adja le automatikusan a dolgozatot. Kelljen a hallgatónak azzal hitelesíteni-e, hogy rányom a leadás gombra)
  - A Hallgató a megfelelő oldalon van.
  - Kiválasztotta a hallgató a záróvizsga tárgyát
  > :memo: **Note:** Dipterv1 leadása után nincs zv vagy dipterv 2 után, tehát nem vonatkozik ide a Követelmények 12 §
- Elsődleges forgatókönyv:
  1. A Hallgató kiválasztja a dolgozat leadása funkciót.
  2. A Rendszer iktatja, hogy a dolgozat leadásra kerül.
  3. A Rendszer értesíti a Hallgató belső konzulensét.
  4. A Rendszernek elérhetővé kell tennie a Szakvezető számára az ügyet.  
  > :memo: **Note:** Látja e a Szakvezető az iktatások alapján az iktatás tárgyát?  
  > :memo: **Note:** Minden iktatás során az ügyben érintetteket értesítse az iktató aktor.  
  > :memo: **Note:** Az érintett aktorok számára legyen elérhető felület ahol az értesítéseiket látják
- Alternatív forgatókönyv:




### UCX: Leadás iktatása




### UCX: Bíráló rögzítése
- Aktor: Konzulens ( \<extend> Tanszéki kolléga)
- Előfeltétel:
  - A Hallgatónak van érvényes témakiírása.

- Elsődleges forgatókönyv:
  1. A Konzulens kiválasztja a “Hallgatók adminisztrálása” funkciót.
  2. A Rendszer megjeleníti a konzultált hallgatókat
  3. A Konzulens kiválaszt egy Hallgatót
  4. A Rendszer megjeleníti a hallgatóhoz köthető adatlapot.
  5. A Konzulens kiválasztja a bíráló rögzítése funkciót.
  6. A Rendszer megjeleníti a bíráló rögzítése funkciót.
  7. A Konzulens megadja a bíráló információit és elérhetőségét (név, email cím, legmagasabb végzettség).
  8. A Rendszer ellenőrzi a végzettséget és az emailcímet.

- Alternatív forgatókönyv:
  - 5/a A Rendszer jelzi, hogy a kiválasztott hallgatóhoz már van bíráló rendelve.
  > :memo: **Note:** Ebben az esetben csak a tanszékvezető módosíthatja az adatokat.

  - 8/a A Rendszer jelzi, hogy a megadott email cím nem megfelelő. A use case a 7. ponttól folytatódik.
  - 8/b A Rendszer jelzi, hogy a megadott végzettség nem megfelelő. A use case a 7zo. ponttól folytatódik.



### UCX: Leadott dolgozat jóváhagyása
- Aktor: Konzulens ( <extend> Tanszéki kolléga)
- Előfeltétel:
  - A Dolgozat leadása iktatásra került.
- Elsődleges forgatókönyv:
  1. A Konzulens kiválasztja a “Leadott dolgozatok adminisztrálása” funkciót.
  2. A Rendszer megjeleníti az elérhető, leadott dolgozatokat
  3. A Konzulens kiválasztja egy Hallgató leadott dolgozatát
  4. A Rendszer megjeleníti a hallgatóhoz köthető adatlapot, ahol ott van a dolgozat is.
  5. A konzulens kiválasztja a megerősítés funkciót.
  6. A rendszer iktatja a megerősítés
  7. A rendszer továbbítja a dolgozatot a tanszéki kollégáknak és a jegyzett bírálónak


- Alternatív forgatókönyv:
  - 5/a A Konzulens kiválasztja az elutasítás funkciót. A Rendszer iktatja az elutasítást. A Rendszer értesíti a hallgatót az elutasításról. A use case a Dolgozat feltöltésével folytatódik.

### UCX: Jóváhagyás iktatása

### UCX: Leadott dolgozat bírálatra továbbítása
- Aktor: Konzulens ( <extend> Tanszéki kolléga)
- Előfeltétel:
  - A dolgozat 
- Elsődleges forgatókönyv:

- Alternatív forgatókönyv:
