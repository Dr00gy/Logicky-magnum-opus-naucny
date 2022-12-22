# Předmluva
Tento dokument je výcuc z prezentací pana M, které jsou vlastně výcucem ze skript. Ostatní dokumenty byly moc špatné, tak jsem se rozhodl udělat vlastní.

# Značení
číslo) Kapitola <br />
písmenko) Podkapitola <br />
🔴 Nejasnosti a hnusy (hlavně u otázek)<br />
🔵 Přímo věci ze zkoušek <br />
🟣 Jazyk logiky <br />

Spolu související části z kapitol budou zlinkovány. :) <br /><br />

## 1) Základy
### a) Co je vlastně logika?
Logika je věda o správném usuzování. Je to nástroj, který ověřuje platnost argumentů.

**Úsudek / argument / výrok:** na základě předpokladů / premis můžeme usoudit, zda je závěr pravdivý. Závěr je nutně pravdivý, když jsou všechny premisy pravdivé.

Zabýváme se deduktivně platnými úsudky. Logické vyplývání závěru:
$P_1...P_n\models Z$ <br /><br /><br />



### b) Logické vyplyvání, tedy, pravda / nepravda
Závěr bude logicky vyplývat, pokud v úsudku nikdy nebudou pravdivé všechny předpoklady a zároveň nepravdivý závěr = správná logická forma. Pro správnou logickou formu taktéž potřebujeme, aby všechny nutné předpoklady byly uvedené:

Předpoklad: Číslo 7 je prvočíslo <br />
◻️◻️◻️ <br />
Závěr: Číslo 7 je dělitelné 1 a samo sebou <br /><br />
(mimochodem, takto budou dál zobrazovány úsudky, jen bez označení předpokladů a závěrů) <br /><br />
*Logika je jako AI, odvozuje si skutečnosti jen z toho, co ví. Logika nebere v úvahu souvislost, mezi "být prvočíslem" a "být dělitelný 1 a sám sebou". Musí se ji vše strčit "pod nos".* <br />

$P_1...P_n\models Z$ <br />
(pokud toto má pravdivé premisy a nepravidvý závěr, tak jde o spor) <br /><br />

**Reflexivita:** Pokud je jeden z předpokladů závěrem, tak závěr logicky vyplývá. <br /><br />

Ve výrokové logice (VL), formule (složený výrok, např. "A") výrokově logicky vyplývá z množiny formulí "M" (značíme: $M\models A$), jestliže A je pravdivá v každém modelu množiny M (jednička na konci řádku v pravdivostní tabulce, tedy pravda). <br />
Při všech ohodnoceních, kdy jsou pravdivé předpoklady, je pravdivý i závěr. Tedy, závěr je pravdivý ve všech modelech předpokladů. <br />

Logické vyplývání dokazujeme nepřímo sporem: předpokládáme, že úsudek není platný (premisy pravdivé a závěr nepravdivý) a pak se k tomu zkoušíme dostat. Pokud nalezneme spor, úsudek je platný. <br />
V přímém způsobu nepředpokládáme opak (tedy, že úsudek je neplatný). Můžeme např. přes pravdivostní tabulku (i pokud dokazujeme tautologičnost). <br />

Všechny úsudky se stejnou logickou formou jako nějaký platný úsudek jsou platné. Tedy, za proměnné (např. p, q, r) můžeme dosadit jiné proměnné a nic to nezmění. <br /> $(p \cap q) \supset r$ <br /><br /><br />



### c) Platnost / správnost
Úsudek může být platný a zároveň jeho závěr nepravdivý - avšak jedna premisa úsudku bude nutně nepravdivá. Úsudek je logicky platný pokud ve všech interpretacích, kde máme pravdivé premisy, máme pravdivý i závěr. <br />

Správnost úsudku je dána logickou strukturou. <br /><br />

**Monotónnost:** Je-li úsudek platný, pak rozšíření množiny předpokladů o další předpoklad nevede ke změně platnosti úsudku. <br />
&nbsp;&nbsp; A <br />
&nbsp;&nbsp; B <br />
&nbsp;&nbsp; C <br />
◻️◻️◻️ <br />
&nbsp;&nbsp; E <br /><br />

Je to samé co: <br /><br />

&nbsp;&nbsp; A <br />
&nbsp;&nbsp; B <br />
&nbsp;&nbsp; C <br />
&nbsp;&nbsp; D <br />
◻️◻️◻️ <br />
&nbsp;&nbsp; E <br /><br /><br />



### d) Spojitost mezi log. vyplýváním a platností
Logické vyplývání (pravda, nepravda) můžeme dokazovat přes platnost úsudku. Úsudek je platný, pokud je formule pravdivá, ale může být také platný, pokud závěr a jedna premisa je nepravdivá. Neplatný úsudek se skládá z nepravdivého závěru, jen když žádná z premis není nepravdivá. <br /><br /><br />

## 2) VL - výroková logika
### a) Základ
Analyzuje způsoby skládání jednoduchých výroků do výroků složených pomocí logických spojek. Výrok je tvrzení, o němž má smysl prohlásit, zda je pravdivé či nepravdivé. Výrok nemůže být otázka ani rozkaz. Avšak ne všechny oznamovací věty jsou výroky (Francouzský král je holohlavý - nemá smysl se nad tímto zamýšlet, když fracozský král ani neexistuje).<br /><br />

Výroky dělíme na: <br />
*	Jednoduché - žádná vlastní část jednoduchého výroku již není výrokem.
*	Složené - výrok má vlastní část(i), která je/jsou výrokem. Logické spojky a závorky. <br /><br />

Význam jednoduchých výroků redukuje VL na pravdu (1) a nepravdu (0). Výroková logika je tedy algebrou pravdivostních hodnot. <br /><br />

Příklady složených výroků: <br />
*	V Praze prší a v Brně je hezky.
*	Není pravda, že v Praze prší. (negace) <br /><br />

🟣 **Dobře utvořena formule:** Formální jazyk je zadán abecedou (množina výchozích symbolů) a gramatikou (množina pravidel, která udávají, jak vytvářet "Dobře Utvořené Formule" - DUF. Můžeme chápat, jako správný "syntax": <br /><br />

*	Výrokové symboly: p, q, r (také příklady atomických formulí)
*	Logické spojky (funktory)
*	Pomocné symboly jako např. závorky
* Neatomická formule: $(p \cap q) \supset r$
* Složená formule: $(A \cap B)$ (A, B jsou neatomické formule) <br /><br />

!! Špatně nezneužíváme priorit a závorek! Negace má větší prioritu než např. konjunkce nebo disjunkce. !! <br /><br />

🟣 **Spojky:**
* Negace: "není pravda, že", ne-sloveso
* Konjunkce: "a" (plachetnice a parníky jsou lodě - NENÍ konjunkce!), "ale", "a zároveň", v predikátové logice (PL) pak spojka pro formalizování existenční kvantif.
* Disjunkce: "nebo"
* Implikace: "jestliže, pak", "když, tak", "je-li, pak", "pokud, pak". První člen je antecedent a druhý konsekvent (nepředpokládá se žádná obsahová souvislost). POZOR: "pouze když, pak" je přehozená implikace! ("Pokud se zlepší stav mého účtu, půjdu na pivo." - $z \supset p$, "Pouze když se zlepší stav mého účtu, půjdu na pivo." - $p \supset z$). POMŮCKA: BEZ PENĚZ DO HOSPODY NELEZ! "Protože" není spojka pro implikaci. V predikátovce je implikace spojka pro formalizovaný všeobecný kvantifikátor.
* Ekvivalence: "Právě tehdy když", "tehdy a jen tehdy" ALE NE "tehdy, když" (to je implikace).
*	Negovaná ekvivalence neboli XOR: "Buď a nebo", "... a nebo...". $\neg(p ≡ q)$ <br /><br /><br />



### b) Sémantika (význam) formulí
