# Feladatnapló — Színpaletta és Kezdőlap (Hero, Navbar) Fejlesztése

- **Dátum:** 2026-09-18
- **Felelős / Tanuló:** Zsombi
- **Téma:** 18. A mi fejlesztőstúdiónk (MySoftware)
- **Érintett Git ág / fájlok:** `README.md`, `src/css/index.css`, `src/html/index.html`, `src/html/example.html`, `src/images/`, `docs/zsombi/2026-09-18_szinpaletta.md`

---

## 1. Elvégzett feladatok

### Színskála megtervezése és bevezetése
- Kidolgoztam a MySoftware egységes, sötét tónusú színpalettáját:
  - **Main background:** Ink Black (`#11100E`) — Teljes oldal háttere
  - **Elevated surface:** Charcoal (`#211F1C`) — Kiemelt felületek, header, kártyák
  - **Main light / text:** Warm Bone (`#F4EBDD`) — Fő szöveg és címsorok
  - **Brand color:** Signal Coral (`#FF5A45`) — Elsődleges márka szín, CTA gombok
  - **Coral dark / hover:** Brick (`#9E392D`) — Gombok lebegtetési (hover) állapota
  - **Special accent:** Acid Chartreuse (`#D8F34A`) — Különleges kiemelések, badge-ek
  - **Muted text:** Stone (`#9B9388`) — Másodlagos szövegek, metaadatok
  - **Light border:** Sand (`#D8CDBD`) — Finom szegélyek és elválasztó vonalak
- Rögzítettem a színskálát a projekt központi `README.md` fájljában (hex és RGB értékekkel, leírással).
- Definiáltam a színeket a `src/css/index.css` fájlban CSS változóként (`:root`).
- Létrehoztam egy önálló bemutató mintafájlt (`src/html/example.html`) beágyazott stílussal.

### Fejléc és navigáció kialakítása (`src/html/index.html`)
- A stúdió logóját (`src/images/logo.png`) elhelyeztem a navigációs sávban (`<header> <nav>`), kezdőlapra mutató linkkel (`<a href="index.html">`).
- Megfelelő méretezést adtam a logónak (`height: 45px; width: auto;`), így nem nyújtja el a fejlécet.
- Kialakítottam a flexbox alapú navigációs menüt a relatív linkekkel (`index.html`, `tema.html`, `muhely.html`).

### Hero szekció felépítése és arculata
- Létrehoztam a főoldali Hero blokkot (`.hero-banner`), amely két oszlopos elrendezésben jeleníti meg a tartalmat:
  - **Bal oldal:** Kiemelő címke (`.hero-tag`), figyelemfelkeltő stúdiócím (`h2`), bemutató szöveg (`p`) és cselekvésre ösztönző gomb (`.hero-btn`).
  - **Jobb oldal:** Nagyméretű, reprezentatív banner kép (`src/images/herobanner.png`) finom lekerekítéssel.
- Beállítottam a Hero szekció kártyaszerű megjelenését (`var(--elevated-surface)` háttér, `var(--light-border)` szegély, lekerekítés és tágas belső térközök).
- Megszüntettem az inline CSS használatát, minden szabályzat tisztán a `src/css/index.css` stíluslapba került, 12. évfolyamos tananyagnak megfelelő szabványos tulajdonságokkal (`display: flex`, `justify-content`, `align-items`, `gap`).

---

## 2. Tapasztalatok és mit tanultam közben
- **CSS változók (`:root`) gyakorlati haszna:** Egy helyen módosítható az egész weboldal színharmóniája anélkül, hogy minden egyes szelektorban kézzel kellene hex kódokat cserélni.
- **Flexbox igazítás a Hero szekciónál:** A `justify-content: space-between` és az `align-items: center` segítségével a szöveg és a kép természetesen, szimmetrikusan igazodik egymáshoz, elkerülve a túlzott és merev margókat.
- **Képméretezés arányossága:** A reszponzivitás érdekében a képekhez fix pixelméret mellett `max-width: 50%` és `height: auto` szükséges, így kisebb képernyőkön sem lógnak ki a konténerből.

---

## 3. Társi ellenőrzés (Peer review)
- **Ellenőrző csapattag:** Bando / Kincsi
- **Megjegyzések / észrevételek:** A színskála és a kezdőlap Hero/Navbar elrendezése elkészült, a stíluslap letisztult.
- **Állapot:** Elfogadásra benyújtva

---

## 4. Következő teendő
- [ ] A csapat többi tagjával (Bando, Kincsi) egyeztetni a stíluslap használatát a `tema.html` és `muhely.html` oldalakon.
- [ ] A főoldal további szekcióinak (`#bemutatkozas`, `#celkozonseg`, `#szolgaltatasok`) szöveges kidolgozása.
