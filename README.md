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
&nbsp;&nbsp; E <br /> [Platnost / správnost ve výrokové logice](#g-správnost-vl-v-rezolučce) <br /><br /><br />



### d) Spojitost mezi log. vyplýváním a platností
Logické vyplývání (pravda, nepravda) můžeme dokazovat přes platnost úsudku. Úsudek je platný, pokud je formule pravdivá, ale může být také platný, pokud závěr a jedna premisa je nepravdivá. Neplatný úsudek se skládá z nepravdivého závěru, jen když žádná z premis není nepravdivá. <br /><br /><br />

## 2) VL - výroková logika
### a) Základ
Analyzuje způsoby skládání jednoduchých výroků do výroků složených pomocí logických spojek. Výrok je tvrzení, o němž má smysl prohlásit, zda je pravdivé či nepravdivé. Výrok nemůže být otázka ani rozkaz. Avšak ne všechny oznamovací věty jsou výroky (Francouzský král je holohlavý - nemá smysl se nad tímto zamýšlet, když fracozský král ani neexistuje).<br /><br />
Výroky dělíme na: <br />
*	Jednoduché - žádná vlastní část jednoduchého výroku již není výrokem.
*	Složené - výrok má vlastní část(i), která je/jsou výrokem. Logické spojky a závorky. <br /><br />
Význam jednoduchých výroků redukuje VL na pravdu (1) a nepravdu (0). Výroková logika je tedy algebrou pravdivostních hodnot. Příklady složených výroků: <br /><br />

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
*	Negovaná ekvivalence neboli XOR: "Buď a nebo", "... a nebo...". $\neg(p \equiv q)$ <br /><br /><br />



### b) Sémantika (význam) formulí
* Pravdivostní ohodnocení (valuace) výrokových symbolů - 1 nebo 0, tedy pravda nebo nepravda.
* Pravdivostní funkce - pro každé ohodnocení výrokových symbolů přiřazuje formuli jeji pravdivostní hodnotu. <br />
(popisujeme zde pravdivostní tabulku, respektive, její proměnné a konečnou pravdivostní hodnotu formule na koncci řádku) <br /><br /><br />

### c) Splnitelnost formulí (tautologie, kontradikce, model)
**Model:** Ohodnocení proměnných, kde formule "A" je pravdivá - 1 na konci řádku v pravdivostní tabulce (u cvičení: kroužkujeme proměnné) <br />
**Splnitelná formule:** Má aspoň jeden model. Tautologie je zvláštní případ splnitelné formule. <br />
**Tautologie:** Každé ohodnocení je modelem. <br />
**Nesplnitelná formule / kontradikce:** Nemá ani jeden model. <br />
**Splnitelná množina formulí:** Existuje-li ohodnocení, které je modelem každé formule. [Splnitelnost ve výrokové logice](#f-splnitelnost-vl-v-rezolučce) <br /><br /><br />

### d) Normální formy
Každé formuli přísluší právě jedna pravdivostní funkce (pravdivostní tabulka). Každé jedné takové funkci pak přísluší nekonečně mnoho formulí, které jsou navzájem ekvivalentní (A <=> B, A <=> C, B <=> D, C <=> D, atd.). DŮLEŽITÉ!! Nesmíme plést tyto ekvivalence: <=> (značí úpravu) s $\equiv$ (značí stejné modely / splnitelnost - u otázek na to opět upozorním)!! Platí však A <=> B, právě když formule $A \equiv B$ je tautologie. <br />
**Element:** = literál. Literál je výrokový symbol nebo jeho negace (p, $\neg p$). <br />
**Elementární konjunkce (EK) / disjunkce (ED):** konjunkce / disjunkce literálů (celkem useless). <br />
**Úplná elementární konjunkce (UEK) / disjunkce (UED):** EK nebo ED, kde se každý symbol z množiny vyskytuje jen jednou. Useful jen pro hledání UDNF / UKNF. <br />
**Konjunktivvní (KNF) / disjunktivní normální forma (DNF):** konjunkce elementárních disjunkcí a disjunkce elementárních konjunkcí respectively. <br />
**ÚPLNÁ KONJ. NORMÁLNÍ FORMA (UKNF) / ÚPLNÁ DISJUN. NORMÁLNÍ FORMA (UDNF):** jsou ekvivalentní s původní formulí, ze které je odvozujeme. Tvar disjunkce úplných elementárních konjunkcí a konjunkce úplných element. disjunkcí. Jsou to tzv. kanonické tvary v řádcích pravd. tabulky (1 - UEK, 0 - UED). Každá formule, která není kontradikce má UDNF. Každá formule, která není tautologie má UKNF. <br /><br /><br /> 

### e) Rezoluční metoda ve VL - basics
Nechť I je literál (i), z formule $(A \cup I) \cap (B \cup \neg I)$ odvoď $(A \cup B)$. <br />
Pokud je $(A \cup I) \cap (B \cup \neg(I))$ pravdivá, tak oba disjunkty (také klausule) musí být taky pravdivé (kvůli té konjunkci) $(A \cup I) = 1$  $(B \cup \neg(I)) = 1$ <br />
$(A \cup B)$ je pravdivá v modelu původní formule (díky disjunkcím je funkce pravdivá v jakémkoliv ohodnocení pro I (0, 1). Zachovala se pravdivost, ale není to přechod k ekvivalentní formuli. Důkaz byl proveden pro jakýkoliv model. Platí, že konjunktivní rozšiření formule o náš rezolvent (A U B) nemění pravdivostní funkci formule: $(A \cup I) \cap (B \cup \neg I) \cap (A \cup B)$ <br />

Jinými slovy: Pokud je původní formule pravdivá při nějaké valuaci a pokud je formule vycházející z původní formule pravdivá ve všech možných případech, tak vycházející formule je pravdivá v modelu původní formule. Pravdivostní funkce původní formule se nezmění, pokud vycházející formuli konjunktivně přidáme k té původní formuli. <br />

Konjunktivní normální forma (KNF) se v rezoluční metodě nazývá klauzulární forma. Jednotlivé konjunkty se nazývají klauzule. K prázdné klauzuli na konce rezoluční metody se dostaneme přes přidávání rezolventů (blíže ve 4. prezentaci od pana M). <br />

*	R(f) - konjunktivní rozšíření formule F o všechny rezolventy. Tedy, všechny možné kombinace rezoluce.
*	R0(F) = Ri(F) = R(Ri-1(F)) - rezoluční uzávěr formule F.
*	Platí, že: Ri(F) <=> F <br /><br /><br />

### f) Splnitelnost VL v rezolučce
* Důkaz, že A je kontradikce (nesplnitelná): existuje n takové, že Rn(A) obsahuje prázdnou klauzuli. Tedy, existuje rezoluční proces, který nás dostane k prázdné klauzuli.
* Nepřímý důkaz (naše "normální" rezoluční metoda), že A je tautologie: neg(A) je kontradikce.
* Důkaz, že množina formulí je nesplnitelná: musíme u všech dokázat, že to jsou kontradikce. <br />

Odvodit, co vyplývá z {A1,...,An} znamená odvodit všechny rezolventy. Používané pro AI. Máme formuli, na kterou používáme rezoluční metodu. Každé jeji upravené části odvozují další skutečnosti (cv. 4, příklad 2. v RES). [Splnitelnost v logice - základy](#c-splnitelnost-formulí-tautologie-kontradikce-model) <br /><br /><br />

### g) Správnost VL v rezolučce
* Důkaz správnosti úsudku $A_1...A_n\models Z$ (rezolučkama)
*	Přímý - postupným vytvářením rezolvent odvodíme, že vyplývá.
* Nepřímý - dokážeme že $A_1...A_n \supset Z$ je tautologie, neboli $A_1 \cap ... \cap A_n \supset \neg Z$ je kontradikce - nesplnitelná. <br />
(příklady ve 4. prezentaci od pana M) <br />

* V rezolučce můžeme v každém kroku vypustit jen jednu dvojici literálů.
* 🔴 Můžeme na konci z formule odvodit dvě tautologie, což je v pořádku, protože tautologie vyplývá z jakékoli formule(???).
* Můžeme uvíznout na nekonečné větvi nebo nic neodvodíme. [Platnost / správnost v logice - základy](#c-platnost--správnost) <br /><br /><br />

## Důležité pojmy (so far, nalinkované mezi sebou výše)
* Vyplývání [Logické vyplývání - základy](#b-logické-vyplyvání-tedy-pravda--nepravda)
* Platnost / správnost [Platnost / správnost v logice - základy](#c-platnost--správnost)
* Splnitelnost [Splnitelnost v logice - základy](#c-splnitelnost-formulí-tautologie-kontradikce-model)
* Sémantika [Sémantika ve VL](#b-sémantika-význam-formulí) <br /><br /><br />

## 3) Množiny
### a) Co je množina?
Množina je soubor prvků a je svými prvky plně určena; množinu s prvky a, b, c značíme: {a, b, c}. <br />
Prvkem množiny může být opět množina. Množina také nemusí mít žádné prvky: $\varnothing$. <br />
Příklady množin: $\varnothing$, {a,b}, {b,a},{a,b,a}, {{a,b}}, {a,{b,a}}, { $\varnothing$ , { $\varnothing$ },{{ $\varnothing$ }}} <br />
Množiny jsou identické, právě tehdy a jen tehdy, když mají stejné prvky (princip extenzionality). <br /><br /><br />



### b) Důležité vztahy a operace (a můžeme nahradit čímkoliv, jen nechat závorky a symboly)
*	$a \in$ {a, b}
*	$a \notin$ {{a, b}} ALE {a,b} $\in$ {{a,b}}
*	$\varnothing \in$ { $\varnothing$ , { $\varnothing$ },{{ $\varnothing$ }}}, ale neleží pro žádné a,b,c..
*	{a, b} = {b, a} = {a,b,a} ALE {a,b} $\ne$ {{a, b}} $\ne$ {a, {b, a}}
*	$\varnothing \notin \varnothing$ ALE $\varnothing \subseteq \varnothing$
*	{a} $\subseteq$ {a}
*	$\varnothing \subseteq$ {a} ALE $\varnothing \notin$ {a}
*	{a} $\nsubseteq$ {{a}}

* Podmnožina: $\subseteq$ - A je podmnožinou B, právě když A $\cup$ B = B A ZÁROVEŇ právě když A $\cap$ B = B. V A jsou prvky z B.
* Vlastní podmnožina: $\subset$ - A je vlastní podmnožinou B, právě když A je podmnožinou B, ale A se nerovná B (B má vlastní prvky, které nejsou v A).
* Průnik: $\cap$
* Sjednocení: $\cup$
* Rozdíl: \
* Doplněk (komplement): Doplněk A k M. Nechť A je podmnožinou M, výsledek = M \ A
* Kartézský součin: NOTE! <a,b> se nerovná <b,a>. U n-tic záleží na pořadí a prvky se mohou opakovat (narozdíl od množin)
* Zobecnění: A x ... x A - množina n-tic. Také můžeme značit $A^{n}$.
* Potenční množina: P(A) = {B | B $\subseteq$ A}, značíme také $2^{A}$. Krátce, do potenční množiny libovolné množiny patří: Ø, všechny prvky množiny individuálně a všemožné kombinace prvků mezi sebou v množině. <br />

**Kardinalita / mohutnost:** Mohutnost množiny (také kardinalita množiny) je pojmem teorie množin vyjadřující velikost, počet prvků u konečných, ale i nekonečných množin. Značíme |M|. <br />
|A| = |B| právě když existuje bijekce f (níže): A $\to$ B <br />
|A| menší nebo rovno |B| právě když existuje injekce f (níže): A $\to$ B <br /><br /><br />



### c) Relace a funkce
* Relace mezi množinami A, B je podmnožina Kartézského součinu A x B. Používa n-tice.
* Notace: <a,b> $\in$ R značíme také R(a,b) nebo a R b.
* Můžeme si představit jako tabulku (i v prezentaci), kde řádky jsou jednotlivé n-tice.

Funkce (zobrazení):
* Ve funkci musí být v prním argumentu furt „stejný“ prvek ($a_1$, $a_2$, $a_3$ – $a_1$, $a_2$ nebo $a_3$ se nesmí opakovat) a ke každému takovému prvku existuje nanejvýš prvek druhý (výsledek funkce).
* Množinu M x...x M nazýváme def. obor (doména) funkce f, množinu M pak obor hodnot (range).
* Jako interpretace funkčních symbolů symbolů formulí predikátové logiky 1 (níže v dokumentu) používáme pouze totální funkce.

* Surjekce: Všechny prvky z "pravé" množiny musí být použité a více prvků z "levé množiny" může vést k jednomu prvku zprava.
* Injekce: Všechny prvky z levé množiny musí být použité a více prvků z pravé množiny nemůže vést k jednomu zprava.
* Bijekce: Párování každého prvku s každým z obou množin. <br /><br /><br />

## 4) Predikátová logika 1. řádu (PL1)
### a) Co je PL1?
Jednoduché výroky, kde VL nestačí. "existuje ..", "všechna ..", "žádná .." apod. <br />
*	x - je individuová proměnná. Člen nějakého predikátu ("skupiny").
* Velké písmena (např. P v P(x)) jsou predikátové symboly.
*	Funkční symbol - konstanta (např. "a", O(a)).
*	Každý symbol proměnné (x,y,...) je term.
*	Jsou-li prvky ve funkci termy a f je funkční symbol, tak f($t_1$, $t_2$) je term.
* Atomické formule se skládá z predikátového symbolu, který má v závorce termy (P(x), P(t)).
* Formule - každá atomická formule je formule.

### b) 🟣 Jazyk PL1?
* Všeobecný kvantifikátor: "všichni", "žádní", "nikdo".
* Existenční kv.: "někdo", "něco", "někteří", "existuje".
* POZOR NA DVOJÍ ZÁPOR! Je lepší si větu přeložit do AJ, příklady: 1) "Žádná ryba není inteligentní." -> "No fish is inteligent". Negace bude u vlastnosti inteligence!!, 2) "Všichni vodníci nejsou mokří." -> "All mermen are not wet." Negace bude na začátku formule!! (lehce clunky angličtina nutná pro tuto pomůcku)

<br /><br /><br />

## 5) Aristetolova logika
* Fragmenty predikátové logiky.
* SUBJEKT, a úsudky z nich vytvořené.

*	Všechna S jsou P, SaP
*	Žádné S není P, SeP
*	Některá S jsou P, SiP
*	Některá S nejsou P, SoP <br />

Všechny pojmy S, P jsou zde neprázdné. <br />
Aristetolova logika - logický čtverec might be helpful. <br />
Součástí Aristetol. logiky jsou sylogismy a Vennovy diagramy. <br /><br /><br />

## OTÁZKY!!

