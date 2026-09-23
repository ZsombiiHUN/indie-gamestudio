# Feladatnapló — Főoldal bővítése és névváltás

- **Dátum:** 2026-09-23
- **Felelős / Tanuló:** Zsombi
- **Téma:** 18. A mi fejlesztőstúdiónk (MySoftware)
- **Érintett Git ág / fájlok:** `main` | `src/html/index.html`, `src/css/index.css`, `src/html/tema.html`, `src/html/muhely.html`, `src/html/example.html`, `README.md`, `docs/zsombi/`

---

## 1. Elvégzett feladatok

- A főoldalra három játékötletet bemutató kártya került képpel, rövid leírással és a `tema.html` oldalra mutató Részletek linkkel.
- A játékképeknél feltüntettük, hogy ChatGPT-vel készült illusztrációk; a Munkáink oldal készítője Marcell.
- Kitöltöttük a Célközönség és Cél, valamint a Mit vállalunk az iskolában? részt rövid szöveggel és felsorolással.
- A csapattagok helykitöltő bemutatkozását a feladatnaplók és a Műhely oldal alapján konkrét feladatokra, gyakorolt eszközökre és következő célokra cseréltük.
- Egyszerű kártyastílust és mobilnézethez médiafeltételt adtunk a főoldalhoz; a csapattagok szövege 16 px méretű lett.
- A korábbi stúdiónevet MySoftware-re cseréltük az oldalcímekben, képleírásokban, láblécekben, a README-ben és a projektjegyzetekben. A GitHub-tárhely címe változatlan.

## 2. Tapasztalatok és ellenőrzés

- A `flex-wrap` segítségével a játékkártyák keskeny nézetben egymás alá kerülnek. A médiafeltétel a navigációt és a hero részt is átrendezi.
- Böngészőben 390 és 1280 px szélességnél ellenőriztük a főoldalt: nem volt vízszintes túlcsordulás. A három játékkép betöltődött, és mindhárom Részletek link a `tema.html` oldalra mutatott.
- A `git diff --check` nem jelzett formázási hibát; a korábbi stúdiónévre végzett szövegkeresés nem talált találatot a projektfájlokban.

## 3. Társi ellenőrzés

- **Ellenőrző csapattag:** Még nem történt társi ellenőrzés.
- **Állapot:** Társi ellenőrzésre vár.

## 4. Következő teendő

- [ ] A csapattagokkal ellenőrizni a bemutatkozások szövegét és a játékötletek készítőinek feltüntetését.
- [ ] A Műhely oldalra felvenni a munkafolyamatot, saját képernyőképet, HTML/CSS-részletet és forráslistát a projektfüzet szerint.
