# MySoftware — Indie Játékfejlesztő Stúdió Portfólió
> **IKT projektmunka II. — 12. évfolyam**  
> Választott téma: **18. A mi fejlesztőstúdiónk** (Pályaorientáció és informatika)  
> Oktató: Czifra Bálint

---

## 👥 Csapattagok és szerepkörök

| Név / Becenév | Szerepkör | Fő felelősségi terület |
| :--- | :--- | :--- |
| **Pintér Zsombor** (Zsombi) | Vezető & Frontend fejlesztő | Főoldal (`index.html`), Git tárhely, arculat és közös stílus (`style.css`, `index.css`), integráció, csapatmunka |
| **Fátyol András** (Bando) | Frontend fejlesztő | Műhely és Források oldal (`muhely.html`, `muhely.css`), 4 lépéses munkafolyamat, forrásjegyzék |
| **Kincses Marcell** (Kincsi) | Frontend Fejlesztő | Munkáink és Csapat oldal (`tema.html`, `tema.css`), játékkártyák és látványtervek |

---

## 🚀 Indítási útmutató (Hogyan nyitható meg a weboldal?)

A weboldal tisztán statikus webtechnológiákra (HTML5, CSS3) épül, futtatásához:

1. Töltsd le vagy csomagold ki a projekt mappáját.
2. Nyisd meg az alábbi fájlt bármely modern webböngészőben (Google Chrome, Firefox, Edge, Safari):
   ```
   src/html/index.html
   ```
3. A navigációs menü segítségével mindhárom oldal (`Kezdőlap`, `Munkáink & Csapat`, `Műhely & Források`) közvetlenül elérhető és bejárható.

---

## ✨ Elkészült funkciók

- **Egységes dizájnrendszer:** CSS változókkal felépített, modern sötét tónusú stúdióarculat (Ink Black, Signal Coral, Acid Chartreuse).
- **Háromoldalas felépítés:**
  - `index.html`: Stúdióbemutató (3 mondatos célkitűzés), kiemelt játékok ízelítője, tagok bemutatása készségekkel és célokkal, iskolai vállalásaink.
  - `tema.html`: Részletes bemutató a három tervezett indie játékról (Starfall Hollow, Lanterns Below, Ember Signal) látványtervekkel és készítői tapasztalatokkal.
  - `muhely.html`: A stúdió 4 lépéses fejlesztési folyamata, „Mit tanultunk?” összefoglaló konkrét CSS kódpéldával, valós fejlesztői képernyőképekkel és forrásjegyzékkel.
- **Reszponzivitás:** Flexbox és CSS Grid alapú rugalmas elrendezés, amely asztali (1280 px) és mobil (390 px) nézetben is túlcsordulás és vízszintes görgetés nélkül jelenik meg.
- **Akadálymentesség és szemantika:** Helyes HTML5 szerkezet (`header`, `nav`, `main`, `footer`), kitöltött leíró képcímkék (`alt`), látható billentyűzetfókusz (`:focus-visible`).
- **Verziókövetés:** Git alapú közös munkafolyamat a `main` ágon, részletes feladatnaplókkal kísérve a `docs/` mappában.

---

## ⚠️ Ismert korlátok és technikai határok

- **Backend és adatbázis hiánya:** A projektfüzet követelményeinek megfelelően a honlap kizárólag kliensoldali HTML és CSS technológiákra épül, szerveroldali logikát vagy dinamikus adatbázist nem használ.
- **JavaScript mellőzése:** A kötelező funkciók és animációk (lebegtetési effektek, flexbox rácsok) tisztán CSS3-mal lettek megvalósítva külső script-könyvtárak nélkül.
- **Fiktív játékprojektek:** A bemutatott játékok koncepciók és látványtervek, amelyek a stúdió kreatív portfólióját demonstrálják.

---

## 🎨 Színskála / Színpaletta

A projekt az alábbi egységes színrendszert használja a stíluslapokban (`var(--...)`):

| Szerepkör | Szín elnevezése | Hex kód | RGB | Alkalmazás a projektben |
| :--- | :--- | :--- | :--- | :--- |
| **Main background** | Ink Black | `#11100E` | `rgb(17, 16, 14)` | Alap háttérszín a teljes oldalon |
| **Elevated surface** | Charcoal | `#211F1C` | `rgb(33, 31, 28)` | Kiemelt felületek, fejlécek, láblécek, kártyák és panelek |
| **Main light / text** | Warm Bone | `#F4EBDD` | `rgb(244, 235, 221)` | Fő címsorok és elsődleges szövegtartalom |
| **Brand color** | Signal Coral | `#FF5A45` | `rgb(255, 90, 69)` | Elsődleges márka szín, kiemelt gombok (CTA), logó akcentus |
| **Coral dark / hover** | Brick | `#9E392D` | `rgb(158, 57, 45)` | Márkaszín sötétebb változata, gombok és linkek lebegtetési állapota (hover) |
| **Special accent** | Acid Chartreuse | `#D8F34A` | `rgb(216, 243, 74)` | Különleges kiemelések, figyelemfelkeltő kitűzők (badge) |
| **Muted text** | Stone | `#9B9388` | `rgb(155, 147, 136)` | Tompított szövegek, másodlagos információk, lábléc feliratok |
| **Light border** | Sand | `#D8CDBD` | `rgb(216, 205, 189)` | Szegélyek, kártyakeretek és finom elválasztók |
