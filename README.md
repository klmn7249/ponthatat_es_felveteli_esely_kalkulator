# ponthatat_es_felveteli_esely_kalkulator

🔢 Számold ki, hogy mennyi az esélye annak, hogy felvesznek egyetemre a 2026 szeptemberében induló képzésekre!

==========================================
1. Súlyozott regresszió (WLS)
A modell az elmúlt évek felvételi aránya (felvett/összes jelentkező) és a ponthatár közötti összefüggést tanulják meg. A λ paraméterrel a régebbi évek kisebb súlyt kapnak.

Ponthatár ≈ a × (felvett ÷ összes) + b
ahol a és b a historikus adatokból számított együtthatók
2. Bootstrap bizonytalanság
Mivel kevés adatponton alapul a regresszió, a modell 5000-szer véletlenszerűen újramintavételezi az adatokat, és minden alkalommal kiszámítja az egyenest. Így megkapjuk, hogy mennyire ingadoznak az együtthatók.

3. Monte Carlo szimuláció (500 000 forgatókönyv)
Minden forgatókönyvben véletlenszerűen választ:

Egy felvett számot (normál eloszlás, a becsült érték ± bizonytalanság alapján)
Egy aktivitási arányt (87–98%, a visszalépések/törlések hatása)
Egy regressziós egyenest (a bootstrap mintából)
Egy véletlen zajt (a historikus illeszkedési hiba alapján)
A 500 000 ponthatár-becslés eloszlásából kapjuk meg a valószínűségi intervallumokat és a felvételi esélyeket.

4. Korlátok és fenntartások

A modell csak a historikus trendet látja — váratlan intézményi döntések (nagy keretszám-változás) torzíthatják az eredményt
Minél kevesebb év adata áll rendelkezésre, annál nagyobb a bizonytalanság
A sorrend-változtatások és törlések hatása becsült (87–98% aktív marad)
Az érettségi közös hatása kiesik a számításból, mert mindenkit egyformán érint
A kalkulátor tájékoztató jellegű — nem helyettesíti a felvi.hu hivatalos adatait
==========================================

*A számítás tájékoztató jellegű, ezért annak eredményei lehet, hogy nem tükrözik a valóságot. A SZÁMÍTÁSOKÉRT NEM VÁLLALUNK FELELŐSSÉGET!*
