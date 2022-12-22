# Předmluva
Tento dokument je výcuc z prezentací pana M, které jsou vlastně výcucem ze skript. Ostatní dokumenty byly moc špatné, tak jsem se rozhodl udělat vlastní.

# Značení
číslo) Kapitola <br />
písmenko) Podkapitola <br />
🔴 Nejasnosti a hnusy <br />
🔵 Přímo věci ze zkoušek <br />
🟣 Jazyk logiky <br />

Spolu související části z kapitol budou zlinkovány. :) <br /><br />

## 1) Základy
### a) Co je vlastně logika?
Logika je věda o správném usuzování. Je to nástroj, který ověřuje platnost argumentů.

**Úsudek / argument / výrok:** na základě předpokladů / premis můžeme usoudit, zda je závěr pravdivý. Závěr je nutně pravdivý, když jsou všechny premisy pravdivé.

Zabýváme se deduktivně platnými úsudky. Logické vyplývání závěru:
$P_1...P_n\mid=Z$ <br /><br /><br />



### b) Logické vyplyvání, tedy, pravda / nepravda
Závěr bude logicky vyplývat, pokud v úsudku nikdy nebudou pravdivé všechny předpoklady a zároveň nepravdivý závěr = správná logická forma. Pro správnou logickou formu taktéž potřebujeme, aby všechny nutné předpoklady byly uvedené:

Předpoklad: Číslo 7 je prvočíslo <br />
◻️◻️◻️ <br />
Závěr: Číslo 7 je dělitelné 1 a samo sebou <br /><br />
(mimochodem, takto budou dál zobrazovány úsudky, jen bez označení předpokladů a závěrů) <br /><br />
*Logika je jako AI, odvozuje si skutečnosti jen z toho, co ví. Logika nebere v úvahu souvislost, mezi "být prvočíslem" a "být dělitelný 1 a sám sebou". Musí se ji vše strčit "pod nos".* <br />

$P_1...P_n\mid=Z$ <br />
(pokud toto má pravdivé premisy a nepravidvý závěr, tak jde o spor) <br /><br />

**Reflexivita:** Pokud je jeden z předpokladů závěrem, tak závěr logicky vyplývá. <br /><br />

Ve výrokové logice (VL), formule (složený výrok, např. "A") výrokově logicky vyplývá z množiny formulí "M" (značíme: $M\mid=A$), jestliže A je pravdivá v každém modelu množiny M (jednička na konci řádku v pravdivostní tabulce, tedy pravda). <br />
Při všech ohodnoceních, kdy jsou pravdivé předpoklady, je pravdivý i závěr. Tedy, závěr je pravdivý ve všech modelech předpokladů. <br />

Logické vyplývání dokazujeme nepřímo sporem: předpokládáme, že úsudek není platný (premisy pravdivé a závěr nepravdivý) a pak se k tomu zkoušíme dostat. Pokud nalezneme spor, úsudek je platný. <br />
V přímém způsobu nepředpokládáme opak (tedy, že úsudek je neplatný). Můžeme např. přes pravdivostní tabulku (i pokud dokazujeme tautologičnost). <br />

Všechny úsudky se stejnou logickou formou jako nějaký platný úsudek jsou platné. Tedy, za proměnné (např. p, q, r) můžeme dosadit jiné proměnné a nic to nezmění. <br /><br /><br />



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
