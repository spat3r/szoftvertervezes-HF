szoftvertervezes-HF

Feladatunk: 11. Két féléves diplomaterv első féléve után a beadott dolgozat kiküldése tanszéki kollégák/bírálók részére (konzulens).

# Elsődleges Aktorok

## Hallgató
A **Hallgató** olyan személy, aki az Egyetemmel hallgatói jogviszonyban van és  teljesítette a Szakdolgozat-készítés vagy Diplomatervezés tárgyakhoz tartozó mérföldköveket.

## Szakvezető
Az Egyetemen a szak vezetéséért és ügyiért felelős munkatárs, a Tanszéki kollégák közül kerül ki.
## Tanszékvezető
Az Egyetemen a Tanszék vezetéséért és ügyiért felelős munkatárs, a Tanszéki kollégák közül kerül ki.

## Tanszéki kolléga
Az Egyetem egy munkatársa.

## Tanszéki ügyintéző
A Tanszéki ügyekért felelős Tanszéki kolléga
# Másodlagos Aktorok
## Címtár
Az Egyetem belső rendszere, amely a Hallgatók bejelentkeztetésére szolgál, illetve tárolja a legfontosabb adataikat.

## Ügy
Iktatott, bármilyen üzleti cselekmény. Az Egyetemen végbemenő, hivatalos cselekmények és tevékenységek.

## Diplomaterv Kiírás
Természetes nyelven megfogalmatzott dokumentum. Rögzíti a hallgató Diplomatervezés vagy Szakdolgozat-készítés tárgy keretében elkészítendő feladatával kapcsolatban több információt.
- Egy rövid leírását a témával kapcsolatban.
- Dolgozat elkészítése során elvégzendő feladatokat.
- A Konzulens és a Tanszék vagy Szakvezető hitelesítét.

## Bírálat
Természetes nyelven megfogalmatzott dokumentum. Rögzíti a hallgató Diplomatervezés vagy Szakdolgozat-készítés tárgy keretében elkészített feladatának szakmai szempontok szerinti értékelését.
- A Bírálatnak értékelnie kell, hogy a kiírásban megadott feladatok milyen mértékben és minőségben készültek el.
- A Bírálatot a Bírálati sablon alapján szükséges elkészíteni.
- A Bírálatnak szakmailag kell értékelnie a dolgozatban vázolt eredményeket.
- A Bírálatnak formai szempontból kell értékelni a dolgozat összeállítását.

## Bíráló
A Szakdolgozat vagy Diplomaterv értékelésére felkért, a munka elkészítésétől jól elhatárolható személy. A bírálónak legalább olyan szintű ISCED besorolású végzettséggel kell rendelkezzen, mint amit az általa bírált mű sikeres megvédésével el lehet érni.



# Use Case-ek

## UC1: Dolgozat feltöltése
- Aktorok: Hallgató
- Előfeltételek:
  - A **Hallgató** be van jelentkezve.
  - Van érvényes témakiírása (tehát volt adatlap, konzulens stb.)
- Elsődleges forgatókönyv:
  1. A **Hallgató** kiválasztja a fájl feltöltése funkciót.
  2. A **Rendszer** megjeleníti a Feltöltési felületet.
  3. A **Hallgató** behúzza a feltölteni kívánt fájlt vagy Böngésző fájlfeltöltő funkciójával kiválasztja feltöltendő fájlt
  4. A **Rendszer** ellenőrzi a fájl nevét, kiterjesztését és a méretét.
  5. A **Hallgató** megerősíti a feltöltést a mentés gombra kattintással.
  6. A **Rendszer** iktatja a feltöltött dokumentumot.

Alternatív forgatókönyv:
- 4/a A **Rendszer** jelzi, hogy a kiválasztott fájl neve nem megfelelő formátumú. A use case a 2. lépéssel folytatódik.
- 4/b A **Rendszer** jelzi, hogy a kiválasztott fájl kiterjesztése nem megfelelő. A use case a 2. lépéssel folytatódik.
- 4/c A **Rendszer** jelzi, hogy a kiválasztott fájl mérete nem megfelelő. A use case a 2. lépéssel folytatódik.


## UCX: Feltöltés iktatása

## UCX: Dolgozat leadása
- Aktor: Hallgató
- Előfeltétel:
  - Feltöltötte a **Hallgató** a dolgozatot és az iktatásra került.
  > :memo: **Note:** Legyen menthető a rendszerben egy átmeneti állapot a végleges leadás előtt. (A **Rendszer** ne adja le automatikusan a dolgozatot. Kelljen a hallgatónak azzal hitelesíteni-e, hogy rányom a leadás gombra)
  - A **Hallgató** a megfelelő oldalon van.
  - Kiválasztotta a **Hallgató** a záróvizsga tárgyát
  > :memo: **Note:** Dipterv1 leadása után nincs zv vagy dipterv 2 után, tehát nem vonatkozik ide a Követelmények 12 §
- Elsődleges forgatókönyv:
  1. A **Hallgató** kiválasztja a dolgozat leadása funkciót.
  2. A **Rendszer** iktatja, hogy a dolgozat leadásra kerül.
  3. A **Rendszer** értesíti a **Hallgató** belső konzulensét.
  4. A Rendszernek elérhetővé kell tennie a Szakvezető számára az ügyet.  
  > :memo: **Note:** Látja e a Szakvezető az iktatások alapján az iktatás tárgyát?  
  > :memo: **Note:** Minden iktatás során az ügyben érintetteket értesítse az iktató aktor.  
  > :memo: **Note:** Az érintett aktorok számára legyen elérhető felület ahol az értesítéseiket látják
- Alternatív forgatókönyv:




## UCX: Leadás iktatása




## UCX: Bíráló rögzítése
- Aktor: Konzulens ( \<extend> Tanszéki kolléga)
- Előfeltétel:
  - A Hallgatónak van érvényes témakiírása.

- Elsődleges forgatókönyv:
  1. A Konzulens kiválasztja a “Hallgatók adminisztrálása” funkciót.
  2. A **Rendszer** megjeleníti a konzultált hallgatókat
  3. A Konzulens kiválaszt egy Hallgatót
  4. A **Rendszer** megjeleníti a hallgatóhoz köthető adatlapot.
  5. A Konzulens kiválasztja a bíráló rögzítése funkciót.
  6. A **Rendszer** megjeleníti a bíráló rögzítése funkciót.
  7. A Konzulens megadja a bíráló információit és elérhetőségét (név, email cím, legmagasabb végzettség).
  8. A **Rendszer** ellenőrzi a végzettséget és az emailcímet.

- Alternatív forgatókönyv:
  - 5/a A **Rendszer** jelzi, hogy a kiválasztott hallgatóhoz már van bíráló rendelve.
  > :memo: **Note:** Ebben az esetben csak a tanszékvezető módosíthatja az adatokat.

  - 8/a A **Rendszer** jelzi, hogy a megadott email cím nem megfelelő. A use case a 7. ponttól folytatódik.
  - 8/b A **Rendszer** jelzi, hogy a megadott végzettség nem megfelelő. A use case a 7. ponttól folytatódik.



## UCX: Leadott dolgozat jóváhagyása
- Aktor: Konzulens ( $<<extend>>$ Tanszéki kolléga)
- Előfeltétel:
  - A Dolgozat leadása iktatásra került.
- Elsődleges forgatókönyv:
  1. A **Konzulens** kiválasztja a “Leadott dolgozatok adminisztrálása” funkciót.
  2. A **Rendszer** megjeleníti az elérhető, leadott dolgozatokat.
  3. A **Konzulens** kiválasztja egy **Hallgató** leadott dolgozatát
  4. A **Rendszer** megjeleníti a hallgatóhoz köthető adatlapot, ahol ott van a dolgozat is.
  5. A **Konzulens** kiválasztja a megerősítés funkciót.
  6. A **Rendszer** iktatja a megerősítést.
  7. A **Rendszer** felveszi feladatként a bírálatra továbbítást.
  8. A **Rendszer** megjeleníti a bírálatra továbbítás funkciót.
  9. A **Konzulens** megerősíti a továbbítás funkciót.
  10. A **Rendszer** a _Leadott dolgozat bírálatra továbbítása_ USE CASE-el folytatja

- Alternatív forgatókönyv:
  - 5/a A Konzulens kiválasztja az elutasítás funkciót. A **Rendszer** iktatja az elutasítást. A **Rendszer** értesíti a hallgatót az elutasításról. A use case a Dolgozat feltöltésével folytatódik.
  - 9/a. A **Konzulens** nem fogadja el a továbbítás funkciót, a USE CASE a 2. ponttal folytatódik.

## UCX: Jóváhagyás iktatása

## UCX: Leadott dolgozat bírálatra továbbítása
- Aktor: Konzulens ( $<<extend>>$ Tanszéki kolléga)
- Előfeltétel:
  - A dolgozat jóváhagyásra került a Konzulens által.
- Elsődleges forgatókönyv:
  1. A **Rendszer** megjeleníti a továbbító felületet.
  > :memo: **Note:** A továbbító felület egy beépített email kliens.
  2. A Konzulens kiválasztja a továbbítás címzettjét. Az elsődleges auto-fill mindig a kijelölt bíráló.
  > :memo: **Note:** A **Bíráló** kiválasztása a UCX-ben már elő van írva.
  3. A **Rendszer** kitölt egy emailt a címzettel és az email törzsét egy szövegsablonnal, amely tartalmazza a határidőket és egyéb szükséges információkat.
  4. A **Rendszer** csatolja a **Hallgató** témakiírását.
  5. A **Rendszer** csatolja a **Hallgató** dolgozatát.
  6. A **Rendszer** csatolja a bírálati űrlapot.
  7. A **Rendszer** megjeleníti az előnézeti felületet.
  8. A **Konzulens** kiválasztja a küldés funkciót.
  9.  A **Rendszer** megjeleníti a küldés megerősítése funkciót.
  10. A **Konzulens** kiválasztja a megerősítése funkciót.
  11. A **Rendszer** továbbítja az üzenetet a címzett számára.
  > :memo: **Note:** Itt hova érkezzen a bouncback, abban az esetben, ha az email-cím ledobna, mert olyan céges levelező rendszerbe ütközik ami nem támogatja a külső üzenetküldést?
  12.  A **Rendszer** értesíti a Konzulenst a továbbítás sikerességéről.
  13. A **Rendszer** iktatja a kiküldött levelet.
  14. A **Rendszer** hozzárendeli a **Bíráló**hoz a bírálás feladatát, amennyiben **Tanszéki Kolléga**.
  15. A **Rendszer** törli a feladatok közül a bírálatra továbbítást.
  16. A **Rendszer** megjeleníti a továbbító felületet.

- Alternatív forgatókönyv:
  - 8/a. A **Konzulens** módosítást eszközöl az emailen, a USE CASE a 7. ponttól folytatódik.
  - 9/a. A **Konzulens** nem fogadja el a megerősítést, a USE CASE a 7. ponttól folytatódik.
  - 12/a. A továbbítás nem sikeres, erről a **Konzulens** értesítésre kerül, a USE CASE a 2. ponttól folytatódik.
  - 14/a. A **Bíráló** nem **Tanszéki kolléga**, a USE CASE a 15. ponttól folytatódik.
