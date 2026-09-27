# 🎓 Egyéni Reflexió és Önértékelés — Pintér Zsombor
> **IKT projektmunka II. — 12. évfolyam (Szoftverfejlesztő és -tesztelő szakma)**  
> **Projekt:** MySoftware (18. téma: A mi fejlesztőstúdiónk)  
> **Oktató:** Czifra Bálint 
> **Dátum:** 2026-09-27  

---

## 👤 Alapadatok

- **Tanuló neve:** Pintér Zsombor
- **Szerepkör a csapatban:** Csapatvezető, Frontend fejlesztő & Git adminisztrátor
- **Fő felelősségi terület és fájlok:**
  - `src/html/index.html` (Kezdőlap szerkezete és tartalma)
  - `src/css/index.css` (Kezdőlap reszponzív elrendezése és komponensei)
  - `src/css/style.css` (Közös arculat, CSS változók, navigáció, lábléc, akadálymentesítés)
  - `README.md` & `README.txt` (Projekt áttekintés és indítási útmutató)
  - `docs/tesztlap.md` (8 átvételi próba és hibajegyzék koordinálása)

---

## 🛠️ 1. Konkrét saját HTML/CSS hozzájárulásom
*(A projektfüzet 25. oldala alapján: nevezz meg legalább egy konkrét komponenst vagy elrendezést, amit te kódoltál, és magyarázd el a technikai döntésedet!)*

- **Az általam készített konkrét elemek és komponensek:**
  1. **Hero Banner (`.hero-banner`):** A főoldali kiemelt bemutató szekció a címmel, szlogennel, cselekvésre ösztönző gombbal (CTA) és a látványos bannerképpel.
  2. **Játékkártyák rácsa (`.games-list`):** A 3 játékot bemutató kártyás szekció az `index.html`-en.
  3. **Akadálymentes billentyűzetfókusz (`:focus-visible`):** A közös stíluslapon létrehozott neonsárga fókuszkeret.

- **Alkalmazott technikai megoldás és indoklás:**
  - **CSS Grid & Flexbox kombinációja a játékkártyáknál:** A kártyarácsot `display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));` szabállyal oldottam meg. Ez automatikusan áttördeli a kártyákat 1, 2 vagy 3 oszlopba a képernyőszélességtől függően anélkül, hogy fix töréspontokat kellene kézzel beégetni. A kártyákon belül pedig `display: flex; flex-direction: column;` és `p { flex-grow: 1; }` beállítást alkalmaztam, így a különböző hosszúságú játékszövegek ellenére az alsó „Részletek →” linkek tökéletesen egy vonalba igazodnak.
  - **CSS változók (`:root`):** A közös arculat színeit változókba szerveztem a `style.css`-ben (`--main-background`, `--elevated-surface`, `--brand-color`, `--special-accent`), így a teljes weboldalon konzisztens maradt a vizuális világ és egyszerűvé vált az utólagos finomhangolás.
  - **`:focus-visible` fókuszstílus:** A sötét felületen az alapértelmezett kék böngészőfókusz szinte láthatatlan volt. Ezért létrehoztam egy 2 px-es, neonsárga (`var(--special-accent)`) keretet 3 px eltolással (`outline-offset: 3px;`), ami a <kbd>Tab</kbd> billentyűvel navigáló felhasználóknak azonnal megmutatja az aktív menüpontot.

---

## 💡 2. Mit tanultam a projekt során?
*(A projektfüzet 25. oldala alapján: írj konkrét szakmai és csapatmunka tapasztalatot!)*

- **Szakmai / Technikai tapasztalat (HTML, CSS, Git, Tesztelés):**
  - **Reszponzivitás 390 px-en:** Megtanultam, hogy a reszponzivitás nem csupán az asztali nézet lezsugorítása. A DevTools emulátorában (iPhone 12/13 — 390 px) szembesültem azzal, hogy egyetlen fix `width: 400px;` vagy hiányzó `max-width: 100%` a képeken azonnal szétnyomja a teljes oldalt és vízszintes görgetősávot okoz. Ennek javítása során mélyebben megértettem a `min-width: 0;`, `clamp()` és `object-fit: cover` szerepét.
  - **Git együttműködés a gyakorlatban:** A csapatban kezelt Git munkafolyamat során megtanultam az `IKT_05` commit üzenet szabvány használatát (`type(scope): description`), a távoli ágak szinkronizálását (`fetch`, `pull`, `push`), valamint a merge és merge conflict kezelésének lépéseit.
  - **Szoftvertesztelés és hibajegyzék:** A `docs/tesztlap.md` kitöltése során a gyakorlatban alkalmaztam a tanult tesztelési alapelveket: a feltárt hibákat (képreszponzivitás, dobozból kicsúszó szövegek) dokumentáltam, és a javításokat független csapattárssal teszteltettem újra.

- **Csapatmunka és együttműködés:**
  - Csapatvezetőként megtanultam, hogy a technikai megvalósítás mellett a legfontosabb a türelmes, támogató kommunikáció. Amikor a csapattársaim elakadtak egy-egy CSS problémával vagy frusztráltak voltak a hibák miatt, nem átvettem tőlük a feladatot, hanem részletes, lépésről lépésre követhető mesterútmutatókat készítettem, magyaráztam el nekik, hogy maguk tudják elvégezni és megérteni a javításokat.
  Itt bele is ütköztünk problémákba, mivel többek közt szemantikus HTMl hibák voltak, amelyet átküldtem listaként csapattársamnak, akinek ezzel a motivácioját lecsökkentettem.

---

## 🚀 3. Legközelebb min javítanék?
*(A projektfüzet 25. oldala alapján: adj meg egy konkrét, fejlesztendő területet példával!)*

- **1. Mobile-First tervezési szemlélet alkalmazása:**  
  Ebben a projektben először a 1280 px-es asztali nézetet készítettem el, és utólag, `@media` lekérdezésekkel szűkítettem a nézetet mobilra. Emiatt több helyen kellett felülírni a margókat és szélességeket a kilógások elkerülésére. Legközelebb mindjárt a 390 px-es mobilnézet felépítésével kezdem a kódolást (Mobile-First), és fokozatosan bővítem asztali méretre, mert ez lényegesen tisztább és kevesebb hibalehetőséget rejtő CSS-t eredményez.

- **2. Szigorúbb belső mérföldkövek (Milestones) a csapattagok felé:**  
  A projekt elején túl későre hagytuk az aloldalak összedolgozását, emiatt a leadás előtti napokra torlódtak a hibajavítások és a tesztelés. Legközelebb már rögzíteni fogunk egy kötelező M1 mérföldkövet (3 oldalas működő váz a 6. órára), hogy a kódok összefésülésére és az alapos peer review-ra több időnk maradjon.

---

## 📋 4. Önellenőrzési táblázat

| Követelmény | Saját értékelésem | Bizonyíték a kódban |
| :--- | :---: | :--- |
| **Szemantika:** Szabályos HTML5 tagek (`header`, `nav`, `main`, `footer`, `section`, `article`). | ✅ Teljes | [src/html/index.html](file:///home/zsombi/projects/school/src/html/index.html) |
| **Címsorok:** Logikus `h1 ➔ h2 ➔ h3` hierarchia, nincs folyószöveg címsorban. | ✅ Teljes | [src/html/index.html#L33-L60](file:///home/zsombi/projects/school/src/html/index.html#L33-L60) |
| **Reszponzivitás:** 390 px és 1280 px között zéró vízszintes görgetősáv. | ✅ Teljes | [src/css/index.css#L100-L150](file:///home/zsombi/projects/school/src/css/index.css#L100-L150) (DevTools tesztelve) |
| **Akadálymentesség:** Képeken értelmes `alt`, a billentyűzetes fókusz neonsárga. | ✅ Teljes | [src/css/style.css#L24-L28](file:///home/zsombi/projects/school/src/css/style.css#L24-L28) (`:focus-visible`) |
| **Munkanaplók és teszt:** Rendszeres naplók a `docs/zsombi/`-ban, tesztlap kitöltve. | ✅ Teljes | [docs/tesztlap.md](file:///home/zsombi/projects/school/docs/tesztlap.md) & [docs/zsombi/](file:///home/zsombi/projects/school/docs/zsombi/) |
| **Leadási csomag:** README és indítási útmutató kész. | ✅ Teljes | [README.md](file:///home/zsombi/projects/school/README.md) |
