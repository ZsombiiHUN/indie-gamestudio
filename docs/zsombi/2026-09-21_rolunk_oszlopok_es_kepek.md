# Feladatnapló — Kezdőlap Rólunk Szekció (3 oszlop) és Képek Rendszerezése

- **Dátum:** 2026-09-21
- **Felelős / Tanuló:** Zsombi
- **Téma:** 18. A mi fejlesztőstúdiónk (Indie Game Studio)
- **Érintett Git ág / fájlok:** `src/html/index.html`, `src/css/index.css`, `src/images/`, `docs/zsombi/2026-09-21_rolunk_oszlopok_es_kepek.md`

---

## 1. Elvégzett feladatok

### Rólunk (Bemutatkozás) szekció 3 oszlopos kialakítása
- A kezdőlap `#bemutatkozas` szekciójának átalakítása modern, reszponzív 3 oszlopos kártya elrendezésre (`.cards-grid`).
- A csapattagok (Bando, Zsombi, Kincsi) bemutató kártyáinak (`.card`) elkészítése, amelyek tartalmazzák:
  - A profilképet (`.profile-image`)
  - A csapattag nevét (`<h3>`)
  - Szerepkör és feladatleírást (`<p>`)
  - Relatív hivatkozást a kapcsolódó aloldalra (`.card-link` -> `tema.html`, `muhely.html`)
- Reszponzív rácsszerkezet implementálása CSS Grid segítségével (`grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));`), ami automatikusan 3 oszlopban jeleníti meg a kártyákat asztali nézetben, mobilon pedig egymás alá rendezi őket.
- Profilkép formázása és méretezése a stíluslapon (`.profile-image`: fix arányok, lekerekített sarkok, vízszintes középre igazítás és `object-fit: cover`).

### Játékillusztrációk rendszerezése és átnevezése
- A stúdió által készített három játék látványterveinek beillesztése és tiszta, beszédes fájlnevekre való átnevezése a `src/images/` mappában:
  - `starfall-hollow.png` (Starfall Hollow — An atmospheric exploration adventure)
  - `ember-signal.png` (Ember Signal — A story-driven survival mystery)
  - `lanterns-below.png` (Lanterns Below — A cozy mystery beneath the world)
- A korábbi  fájlnevek cseréje tiszta, webes szabványoknak megfelelő formátumra.
- Saját profilkép (`zsombi.png`) integrálása a kezdőlap Rólunk szekciójába.

---

## 2. Tapasztalatok és mit tanultam közben
- **Reszponzív CSS Grid (`repeat(auto-fit, minmax(...))`):** Megtanultuk, hogyan lehet rácsszerkezetet készíteni média lekérdezések (media queries) nélkül, amely a képernyő szélességétől függően dinamikusan és rugalmasan 3, 2 vagy 1 oszlopba rendezi a kártyákat.
- **Képformázás és illeszkedés (`object-fit: cover`):** Segítségével a portréképek és fotók torzulás nélkül jelennek meg fix méretek mellett is.
- **Fájlnevezési konvenciók a webfejlesztésben:** A szóközöket és speciális karaktereket tartalmazó fájlnevek helyett a kisbetűs, kötőjeles elnevezések használata stabilabbá és hivatkozhatóbbá teszi az erőforrásokat a weboldalon.

---

## 3. Társi ellenőrzés (Peer review)
- **Ellenőrző csapattag:** Bando / Kincsi
- **Megjegyzések / észrevételek:** A 3 oszlopos Rólunk szekció reszponzív, a játékokhoz tartozó képek átnevezve készen állnak a munkák (`tema.html`) oldalhoz.
- **Állapot:** Elfogadva

---

## 4. Következő teendő
- [ ] Bando és Kincsi profilképének (`bando.png`, `kincsi.png`) feltöltése és a leírások véglegesítése.
- [ ] A 3 átnevezett játékkép beépítése a `tema.html` oldalra (Munkáink & Csapat).
- [ ] A lábléc és a további szekciók (`#celkozonseg`, `#szolgaltatasok`) kidolgozása.
