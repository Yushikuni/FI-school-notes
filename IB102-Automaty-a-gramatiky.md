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
- výsledkem je vždy jazyk (sjednocení) nad oběma zastoupenými abecedami
- standardní operace: sjednoccení, průnik, rozdíl
- zřetězení jazyků *L* a *K* je jazyk *L . K = {u.v | u ∈ L, v ∈ K}*, zachovává se pořadí
  >1 =  {0, 1}, 2 = {a, b}<br/>
  >L = {00, 01}, K = {aa, bb}<br/>
  >L.K = {00aa, 00bb, 01aa, 01bb}
- (prázdná množina) . L = prázdná množina, ale pozor {(prázdné slovo)} . L = L

**Iterace** jazyka L je jazyk L* = sjednocení Li (i = 0, nekonečno)
>L = {aa, b}*<br/>
>L* = L0 sjednoceno L1 sjednoceno L2 ...<br/>
>L* = {ε, aa, b, aaaa, aab, baa, bb, aaaaaa, aaaab, ... }<br/>

**Pozitivní iterace**
L+ = L* 

**Doplněk** jazyka L je jazyk co-L = Σ* bez L, je pro to třeba znát abecedu
  >L = {a, aa}<br/>
  >Σ = {a} co-L = {ε, aaa, aaaa, ...}<br/>
  >Σ = {a, b} co-L = {ε, b, ab, ba, bb} sjednoceno {w in {a, b}* *| |w| more or eq 3*}

**Zrcadlový obraz**
  >{abacca}<sup>R</sup> = accaba

#### Uzavřená třída jazyků
  >Σ = {a}<br/>
  >>  L<sub>1</sub> = {ε, a, aa, aaa, aaaa...}<br/>
  >>  L<sub>2</sub> = {a, aa, aaa, aaaa...}<br/>
  >>  L<sub>3</sub> = {aa, aaa, aaaa...}<br/>
  >>  L<sub>i</sub> = {a<sup>j</sup> | j more or eq i}
  
  L je uzavřená na: (union), (intersect), L<sup>n</sup> | (n > 0), ., + <br/>
  L není uzavřená na: (diff), L<sup>0</sup>, *, L+, R
  
  >L<sub>i</sub> (union) L<sub>j</sub> = L<sub>min(i,j)</sub><br/>
  >L<sub>i</sub> (intersect) L<sub>j</sub> = L<sub>max(i,j)</sub><br/>
  >L<sub>1</sub> (union) L<sub>2</sub> = {a}
  
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
  *<veta> -> <podmetna cast><prisudkova cast>*
- k zadání syntaxe vyšších programovacích jazyků používáme *Backus-Naurova normální formu (BNF)*
- definice: Gramatika je čtveřice (N, Σ, P, S), kde
  - N je neprázdná konečná množina neterminálů
  - Σ je konečná množina terminálů, taková, že N (intersect) Σ = (null) , množinu všech symbolů definujeme jako N (union) Σ
  - P je komečná množina pravidel, pravidlo (alfa, beta) zapisujeme jako alfa -> beta (alfa přepiš na beta)
  - S je počáteční terminál
  >G = ({s}, {a, b}, P, S)
  >P = {S -> a, S -> baS, aS -> bb}
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
