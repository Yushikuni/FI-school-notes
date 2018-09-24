# Automaty a gramatiky
------
### Přednáška 1 - 17. 09. 2018

#### Formální jazyk
**abeceda**
- libovolná konečná množina
- značená symbolem *Σ*
- např. *{a, b, c, d}, {@, #, %, ...}*
- prvek abecedy nazýváme jako *symbol*

**slovo (řetězec)**
- nad abecedou Σ je libovolná konečná posloupnost znaků této abecedy
  >Σ = {a, b, c}<br/>
  >slova zde budou například:
  >- u = abba
  >- v = a
  >- w = cacacaca
  >- y = ε
- prázdnou posloupnost znaků odpovídá prázdné slovo, ozančované jako *ε*
- počet znaků v posloupnosti v značíme *|v|*
- výskyt znaku *a* ve slově *w* značíme jako #<sub>a</sub>(w)

**jazyk**
- nad abecedou Σ je libovolná množina slov nad Σ
> Σ = {a, b, c}<br/>
> L = {aa, abac, cc}<br/>
> L' = {ε}<br/>
> L''' = prázdná množina
- množina všech slov značíme jako Σ<sup>*</sup>
- množinu všech neprázdných slov značíme jako Σ<sup>+</sup>

#### Operace a relace nad slovy
**zřetězení** je binární operace, označována *.* , je definována předpisem: *u.v = uv*
  > abac . bb = abacbb<br/>
  > aba . ε = aba<br/>
  > ε . aba = aba
- zřetězení je asociativní, tj. *u.(u.w) = (u.v).v*
  > (ab.bac).ac = abbac.ac = abbacac<br/>
  > ab.(bac.ac) = ab.bacac = abbacac<br/>
- není komutativní

**podslovo**
- *u* je podslovem *v*, jestliže existují slova *x*, *y* taková, že *v = x.u.y*
- libovolná podposloupnost daného slova
  > v = baca<br/>
  > podslova: baca, bac, aca, ba, ac, ca, b, a, c, ε

**předpona**
- pokud je *x = ε*, tak slovo *u* je předponou (prefixem)
- pokud je *y = ε*, tak slovo *u* nazýváme příponou (suffixem)

**mocniny**
- unární operace definována pro všechny *i*
- N<sub>0</sub> = přirozená čísla s 0
- N = přirozená čísla od 1...N
  > u<sup>0</sup> = {ε}<br/>
  > u<sup>i+1</sup> = u.u<sup>i</sup>
- konkrétní příklad:
  >u = ba<br/>
  >u<sup>0</sup> = ε<br/>
  >u<sup>1</sup> = u . u<sup>0</sup> = ba . ε = ba<br/>
  >u<sup>2</sup> = u . u<sup>1</sup> = ba . ba = baba

#### Operace nad jazyky
- výsledkem je vždy jazyk ∪ nad oběma zastoupenými abecedami
- standardní operace: sjednoccení, průnik, rozdíl
- zřetězení jazyků *L* a *K* je jazyk *L . K = {u.v | u ∈ L, v ∈ K}*, zachovává se pořadí
  >1 =  {0, 1}, 2 = {a, b}<br/>
  >L = {00, 01}, K = {aa, bb}<br/>
  >L.K = {00aa, 00bb, 01aa, 01bb}
- (prázdná množina) . L = prázdná množina, ale pozor {(prázdné slovo)} . L = L

**Iterace** jazyka L je jazyk L* = ∪ Li (i = 0, nekonečno)
>L = {aa, b}*<br/>
>L* = L0 ∪ L1 ∪ L2 ...<br/>
>L* = {ε, aa, b, aaaa, aab, baa, bb, aaaaaa, aaaab, ... }<br/>

**Pozitivní iterace**
L+ = L* \ ε (L* bez slova ε)

**Doplněk** jazyka L je jazyk co-L = Σ* bez L, je pro to třeba znát abecedu
  >L = {a, aa}<br/>
  >Σ = {a} co-L = {ε, aaa, aaaa, ...}<br/>
  >Σ = {a, b} co-L = {ε, b, ab, ba, bb} ∪ {w ∈ {a, b}* | |w| ≥ 3}

**Zrcadlový obraz**
  >{abacca}<sup>R</sup> = accaba

#### Uzavřená třída jazyků
  >Σ = {a}<br/>
  >>  L<sub>1</sub> = {ε, a, aa, aaa, aaaa...}<br/>
  >>  L<sub>2</sub> = {a, aa, aaa, aaaa...}<br/>
  >>  L<sub>3</sub> = {aa, aaa, aaaa...}<br/>
  >>  L<sub>i</sub> = {a<sup>j</sup> | j ≥ i}
  
  L je uzavřená na: ∪, ∩, L<sup>n</sup> | (n > 0), ., + <br/>
  L není uzavřená na: (diff), L<sup>0</sup>, *, L+, R
  
  >L<sub>i</sub> ∪ L<sub>j</sub> = L<sub>min(i,j)</sub><br/>
  >L<sub>i</sub> ∩ L<sub>j</sub> = L<sub>max(i,j)</sub><br/>
  >L<sub>1</sub> ∪ L<sub>2</sub> = {a}
  
#### Aplikace
>N = {1, 2, 3, 4...}<br/>
>Σ = {0, 1, 2, 3, ... , 9}<br/>

>N = {1, 2, ... , 9} . {0, 1, 2, ... 9}*<br/>
>N<sup>0</sup> = N . {0}<br/>
nebo
>N = Σ<sup>+</sup> - {0} . Σ<sup>+</sup>

#### Gramatika
- je popis jazyka pomocí pravidel, podle kterých se vytvářejí všechna sova daného jazyka
- např.
  *<veta> → <podmetna cast><prisudkova cast>*
- k zadání syntaxe vyšších programovacích jazyků používáme *Backus-Naurova normální formu (BNF)*
- definice: Gramatika je čtveřice (N, Σ, P, S), kde
  - N je neprázdná konečná množina neterminálů
  - Σ je konečná množina terminálů, taková, že N ∩ Σ = (null) , množinu všech symbolů definujeme jako N ∪ Σ
  - P je komečná množina pravidel, pravidlo (alfa, beta) zapisujeme jako alfa → beta (alfa přepiš na beta)
  - S je počáteční terminál
  >G = ({s}, {a, b}, P, S)
  >P = {S → a, S → baS, aS → bb}
  ... doplnit na prtsc ...*
  
**přímé odvození**
- *doplnit def. přímého odvození*

**odvození v _k_ krocích**
- *doplnit*

**Větná forma**
- každý řetěz z množiny V*, který lze odvodit z počátečního neterminálu gramatika

**Věta gramatiky**
- každá větná forma, která obsahuje pouze terminály

#### Konvence zápisu
Σ - terminály: a, b, c, .... , 0, 1, ...
N - neterminály, S, A, B, C, ....

### 2. přednáška - 24. 09. 2018

#### Chomského hierarchie gramatik

Klasifikace podle tvaru přepisovacích pravidel<br />

- typ 0: pravidla v obecném tvaru (frázové gramatiky)
- typ 1: kontextové gramatiky, nemůže obsahovat pravidla, kdy je |a| <= |b| (levá strana musí být kratší než pravá strana), nedovoluje přítomnost zkracovacích pravidel (např. Ab -> A nebo Abc -> aC
- typ 2: bezkontextové gramatiky, na levé straně maximálně jeden terminál
- typ 3: regulární gramatiky 
- *typ 3 je zároveň typ 2, který je zároveň typ 1, který je "překvapivě" i typ 0*
 
#### Automaty
- **def**: Deterministický konečný automat (M) je pětice (Q, sigma, ro, q0, F), kde
  - Q je neprázdná množina stavů
  - (Sigma) je konečná vstupní abeceda
  - (delta) Q x E -> parciální přechodová funkce (nemusí být definovaná pro všechny stavy), např. (delta)(q<sub>0</sub>,a) = q2
  - q0 je počáteční (iniciální stav)
  - F (subset) množina koncových (akceptujících) stavů (dvě kolečka okolo stavu)

**Zápis tabulkou**        <br />
   I a  I b
-----------------
q0 I q2 I q1              <br />
q1 I -  I -               <br />

-> q0
<- q1, q2

**Zápis grafem**
- stavy označujeme do symbolu kruhu
- šipky spojují jednotlivé vztahy, využívají přechodové stavy
 
**Rozšířená přechodová funkce**
- parciální funkce definovaná induktivně vzhledem k délce slova (sigma)^*
- značí se jako (delta) se stříškou
- provádí se většinou rekurzivně pro jednotlivé části posloupnosti 

delta se s (q0, abab) =
1) delta(delta se s(q0, aba), b)
2) delta(delta(delta se s(q0, ab), a) b)
3) delta(delta(delta(delta se s(q0, a), b), a), b)
4) delta(delta(delta(delta(delta se s(q0, epsilon), a), b), a), b)

**Jazyk automatu**
- množina slov, které automat akceptuje a vedou k tomu, že se automat dostane do některého z konečných stavů

Jazyky, pro které existuje nějaký deterministický automat nazýváme *regulární*.
