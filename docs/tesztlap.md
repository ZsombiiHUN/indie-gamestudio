# 📋 Projekt Tesztlap és Átadási Dokumentáció
> **IKT projektmunka II. — 12. évfolyam**  
> Választott téma: **18. A mi fejlesztőstúdiónk** (Pályaorientáció és informatika)  
> Oktató: Czifra Bálint  
> Projekt neve: **MySoftware**

---

## 👥 A tesztelésben résztvevők és azonosítók

- **Vizsgált csapat:** MySoftware (18. téma)
- **A csapat tagjai:**
  - **Pintér Zsombor** (Kezdőlap, közös arculat, Git adminisztráció)
  - **Fátyol András** (Műhely & Források oldal, folyamatleírás)
  - **Kincses Marcell** (Munkáink & Csapat oldal, játékkártyák)
- **Tesztelési környezet:**
  - Asztali nézet: Google Chrome / Firefox (1920×1080 és 1280×800)
  - Mobil emuláció: DevTools (390×844 — iPhone 12/13/14 viewport)
  - Operációs rendszer: Linux / Windows
- **Tesztelés időpontja:** 2026. szeptember 25–27.

---

## 🔍 I. Rész: A 8 Kötelező Átvételi Próba (Projektfüzet 24. oldal)

Az alábbi táblázat tartalmazza a projektfüzet 24. oldalán előírt 8 hivatalos vizsgálati pontot, az elvárt működést és a vizsgálat végeredményét:

| # | Próba megnevezése | Elvárt eredmény | Tényleges eredmény / Tapasztalat | Minősítés |
| :-: | :--- | :--- | :--- | :---: |
| **1.** | **Indítás** | A kicsomagolt mappából az `index.html` közvetlenül megnyitható bármely böngészőben. | Az `src/html/index.html` dupla kattintással és relatív útvonalról is hiba nélkül betöltődik. | **OK** |
| **2.** | **Navigáció** | Mindhárom oldalról mindhárom oldal elérhető, működő relatív linkekkel és aktív oldal jelöléssel. | A fejrész menüjéből (`Kezdőlap`, `Munkáink & Csapat`, `Műhely & Források`) minden aloldal elérhető oda-vissza. | **OK** |
| **3.** | **Kötelező tartalom** | A 18. témalap mind a 4 minimuma megtalálható az oldalakon (stúdió, 3 játék, tagok céljai, munkafolyamat). | Stúdiónév és arculat megvan; 3 játék bemutatva; tagok készségei és céljai rögzítve; 4 lépéses folyamat leírva. | **OK** |
| **4.** | **Mobil / asztali nézet** | **390 px** és **1280 px** szélességen is olvasható; nincs zavaró vízszintes túlcsordulás / elcsúszás. | Asztali (1280 px) és telefonos (390 px) nézetben sincs vízszintes görgetősáv, a tartalom igazodik. *(Javítás után)* | **OK** |
| **5.** | **Képek és szövegek** | Nincs törött kép, minden kép rendelkezik értelmes `alt` szöveggel, a címsorsorrend logikus (`h1 ➔ h2 ➔ h3`). | Az összes kép betöltődik az `images/` mappából, nincsenek elcsúszott címsorok. *(Javítás után)* | **OK** |
| **6.** | **Billentyűzet** | <kbd>Tab</kbd> billentyűvel bejárható a menü; a fókusz látható; a linkek <kbd>Enter</kbd>-rel működnek. | A navigációs linkek <kbd>Tab</kbd>-bal fókuszálhatók, a neon fókuszkeret (`:focus-visible`) világosan látható. *(Javítás után)* | **OK** |
| **7.** | **Műhely és források** | Tagok feladatai, valós képernyőkép a munkáról, működő kódrészlet és a forráslista megvan. | A csapattagok szerepkörei leírva, 2 db kódolási képernyőkép és CSS kódrészlet elhelyezve, források linkelve. | **OK** |
| **8.** | **Témaspecifikus próba** | A saját témalap átvételi próbája sikerül: kiderül, ki készítette az adott elemet és miben fejlődött közben. | A bemutatott munkáknál és a Műhely oldalon nevesítve vannak a felelősök és az egyéni tapasztalatok. | **OK** |

---

## 🛠️ II. Rész: Hibajegyzék és Újratesztelési Napló (Projektfüzet 24. oldal)

A belső tesztelés során feltárt hibák, a hibajavításért felelős csapattagok és a független társi újratesztelés eredményei:

| Hiba / Észrevétel leírása | Helye | Javító csapattag | Újratesztelő csapattag | Újratesztelés eredménye és igazolása |
| :--- | :--- | :--- | :--- | :--- |
| **1. Képreszponzivitás hiánya a főoldalon:** A Hero banner képe (`herobanner.png`) és a játékkártyák képei kisebb kijelzőkön kilógtak a konténerből, vízszintes görgetősávot okozva. | `src/html/index.html`<br>`src/css/index.css`<br>`src/css/style.css` | **Pintér Zsombor** | **Fátyol András** | **JAVÍTVA (OK):** Globális `img { max-width: 100%; height: auto; }` hozzáadva, a `.hero-banner` és a képek flexibilis méretezést kaptak. 390 px-en nem lóg ki. |
| **2. Szövegkicsúszás a „Közös munkáink” dobozból:** A fix `1050px` szélesség és a rögzített magasság miatt kisebb képernyőn a szöveg kilógott a doboz keretén kívülre, szétcsúszott a megjelenés. | `src/html/muhely.html`<br>`src/css/muhely.css` | **Fátyol András** | **Pintér Zsombor** | **JAVÍTVA (OK):** A fix szélesség helyett `max-width: 1050px; width: 90%; min-height: 200px;` került beállításra. A szöveg tökéletesen a dobozon belül marad minden felbontáson. |
| **3. A Munkáink oldal (`tema.html`) reszponzivitási hibája:** A játékkártyák egymás mellé kényszerültek flex-wrap nélkül, kisebb kijelzőn összenyomódtak; a globális `div { margin: 10px; }` szétnyomta az elrendezést. | `src/html/tema.html`<br>`src/css/tema.css` | **Kincses Marcell** /<br>**Pintér Zsombor** | **Fátyol András** | **JAVÍTVA (OK):** A `.secondcontainer` `flex-wrap: wrap;` tulajdonságot kapott, törlésre került a destruktív globális margó, a kártyák mobilon egymás alá rendeződnek. |
| **4. Műhely csapattag kártyák túlcsordulása mobilon:** A `.team-member` dobozok `width: 400px;` és `margin: 20px;` beállítása (440 px) miatt a 390 px-es mobil teszten 50 px-es kilógás és oldalgörgetés keletkezett. | `src/css/muhely.css` | **Fátyol András** | **Pintér Zsombor** | **JAVÍTVA (OK):** A kártyák szélessége `width: 100%; max-width: 360px;` szabályozást kapott. 390 px szélességen zéró túlcsordulás. |
| **5. Billentyűzetfókusz hiánya sötét háttéren:** <kbd>Tab</kbd> navigáció során a sötét (`#11100E`) felületen az alapértelmezett böngésző fókuszkeret nem látszott megfelelően. | `src/css/style.css` | **Pintér Zsombor** | **Fátyol András** | **JAVÍTVA (OK):** A `style.css`-be bekerült a `:focus-visible { outline: 2px solid var(--special-accent); outline-offset: 3px; }` szabály, ami éles neonsárga keretet ad. |
| **6. Szemantikai hibák és duplikált azonosítók a Műhelyen:** A kártyák belsejében `<h1>` címkék és ismétlődő `id="team-header"`, `id="team-member-task"` azonosítók szerepeltek. | `src/html/muhely.html` | **Fátyol András** | **Pintér Zsombor** | **JAVÍTVA (OK):** A kártyákon belüli címkék átírva szabályos `<h4>`-re, az azonosítók pedig egyedi osztályokra (`class`) lettek cserélve. |

---

## 📦 III. Rész: Leadási Csomag Ellenőrzése (Checklist)

A projektfüzet 24. oldalán leírt leadási csomag (`csapatnev_tema.zip`) követelményei:

- [x] **3 HTML-fájl:** `index.html`, `tema.html`, `muhely.html` megléte és hibamentes összekapcsolása.
- [x] **style.css:** Közös színváltozók és globális formázás érvényesülése mindhárom oldalon.
- [x] **images mappa:** Minden illusztráció, logó, profilkép és kódképernyőkép helyben, relatív útvonallal elérhető.
- [x] **README.md / README.txt:** Tagok, indítási útmutató, kész funkciók és ismert korlátok rögzítve.
- [x] **Feladatnaplók:** Részletes munkanaplók a `docs/` mappában tagokra lebontva (`docs/zsombi/`, `docs/bando/`, `docs/kincsi/`).
- [x] **Kitöltött tesztlap:** A 8 pontos átvételi próba és a dokumentált hibajegyzék (`docs/tesztlap.md`) elkészült.
- [x] **Tiszta mappából történő indítás:** Új, tiszta mappába kicsomagolva a weboldal az `index.html` megnyitásával hibátlanul fut.

---

## 🎯 IV. Rész: Összegzés és Értékelési Javaslat

A MySoftware csapata a tesztelési folyamatot a tanmenetnek és a szoftvertesztelési irányelveknek megfelelően végezte el. A feltárt megjelenítési, szemantikai és reszponzivitási hibák javításra és független csapattag által újratesztelésre kerültek. 

A projekt a **„Teszt és átadás (15 pont)”** szempont minden feltételét maradéktalanul teljesíti. 
