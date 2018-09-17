# Automaty a gramatiky
------
### Přednáška 1 - 17. 09. 2018

#### Formální jazyk
**abeceda**
- libovolná konečná množina
- značená symbolem velké sigma
- např. {a, b, c, d}, {@, #, %, ...}
- prvek abecedy nazýváme jako *symbol*

**slovo (řetězec)**
- nad abecedou sigma je libovolná konečná posloupnost znaků této abecedy
- sigma = {a, b, c}
- slova zde budou například:
  - u = abba
  - v = a
  - w = cacacaca
  - y = malé epsilon
- prázdnou posloupnost znaků odpovídá prázdné slovo, ozančované jako malé epsilon
- počet znaků v posloupnosti v značíme |v|

**jazyk**
- nad abecedou sigma je libovolná množina slov nad sigma
- např. sigma = {a, b, c}
  - L = {aa, abac, cc}
  - L' = {epsilon}
  - L''' = prázdná množina
- množina všech slov značíme jako sigma na hvězdičku
- množinu všech neprázdných slov značíme jako sigma na plus

#### Operace a relace nad slovy
**zřetězení** je binární operace, označována ., je definována předpisem: *u.v = uv*
- např.
  *abac . bb = abacbb
  aba. (epsilon) = aba
  (epsilon) . aba = aba*
- zřetězení je asociativní, tj. *u.(u.w) = (u.v).v*
  - např.
  *(ab.bac).ac = abbac.ac = abbacac
  ab.(bac.ac) = ab.bacac = abbacac*
- není komutativní

**podslovo**
- u je podslovem v, jestliže existují slova x, y taková, že *v = x.u.y*
- libovolná podposloupnost daného slova
- např.
  *v = baca
  podslova: baca, bac, aca, ba, ac, ca, b, a, c, (epsilon)*

**předpona**
- pokud je x = epsilon, tak slovo *u* je předponou (prefixem)
- pokud je y = epsilon, tak slovo *u* nazýváme příponou (suffixem)

**mocniny**
- unární operace definována pro všechny *i*
- N<sub>0</sub> = přirozená čísla s 0
- N = přirozená čísla od 1...N
- např.
  *u<sup>0</sup> = {epsilon}
  u<sup>i+1</sup> = u.u<sup>i</sup>*
- konkrétní příklad:
  *u = ba
  u<sup>0</sup> = epsilon
  u<sup>1</sup> = u . u<sup>0</sup> = ba . epsilon = ba
  u<sup>2</sup> = u . u<sup>1</sup> = ba . ba = baba*

#### Operace nad jazyky
- výsledkem je vždy jazyk (sjednocení) nad oběma zastoupenými abecedami
- standardní operace: sjednoccení, průnik, rozdíl
- zřetězení jazyků L a K je jazyk L.K = {u.v | u le L, v le K}, zachovává se pořadí
- např.
  *1 =  {0, 1}, 2 = {a, b}
  L = {00, 01}, K = {aa, bb}
  L.K = {00aa, 00bb, 01aa, 01bb}*
- (prázdná množina).L = prázdná množina, ale pozor {(prázdné slovo)}.L = L

**Iterace** jazyka L je jazyk L* = sjednocení Li (i = 0, nekonečno)
*L = {aa, b}*
L* = L0 sjednoceno L1 sjednoceno L2 ...
L* = {epsilon, aa, b, aaaa, aab, baa, bb, aaaaaa, aaaab, ... }*

**Pozitivní iterace**
L+ = L* 

**Doplněk** jazyka L je jazyk co-L = (sigma)* bez L, je pro to třeba znát abecedu
- např.
  *L =  {a, aa}
  sigma = {a} co-L = {epsilon, aaa, aaaa, ...}
  sigma = {a, b} co-L = {epsilon, b, ab, ba, bb} sjednoceno {w in {a, b}* *| |w| more or eq 3*}

**Zrcadlový obraz**
- např.
  *{abacca}<sup>R</sup> = accaba*

#### Uzavřená třída jazyků
- např.
  * sigma = {a}
      L<sub>1</sub> = {epsilon, a, aa, aaa, aaaa...}
      L<sub>2</sub> = {a, aa, aaa, aaaa...}
      L<sub>3</sub> = {aa, aaa, aaaa...}
      L<sub>i</sub> = {a<sup>j</sup> | j more or eq i}
  
  L je uzavřená na: (union), (intersect), L<sup>n</sup> | (n > 0), ., + 
  L není uzavřená na: (diff), L<sup>0</sup>, *, L+, R
  
  L<sub>i</sub> (union) L<sub>j</sub> = L<sub>min(i,j)</sub>
  L<sub>i</sub> (intersect) L<sub>j</sub> = L<sub>max(i,j)</sub>
  L<sub>1</sub> (union) L<sub>2</sub> = {a}
  *
  
#### Aplikace
N = {1, 2, 3, 4...}
sigma = {0, 1, 2, 3, ... , 9}

N = {1, 2, ... , 9} . {0, 1, 2, ... 9}*
N<sup>0</sup> = N . {0}
nebo
N = sigma<sup>+</sup> - {0} . sigma<sup>+</sup>

#### Gramatika
- je popis jazyka pomocí pravidel, podle kterých se vytvářejí všechna sova daného jazyka
- např.
  *<veta> -> <podmetna cast><prisudkova cast>*
- k zadání syntaxe vyšších programovacích jazyků používáme *Backus-Naurova normální formu (BNF)*
- definice: Gramatika je čtveřice (N, sigma, P, S), kde
  - N je neprázdná konečná množina neterminálů
  - sigma je konečná množina terminálů, taková, že N (intersect) sigma = (null) , množinu všech symbolů definujeme jako N (union) sigma
  - P je komečná množina pravidel, pravidlo (alfa, beta) zapisujeme jako alfa -> beta (alfa přepiš na beta)
  - S je počáteční terminál
- např.
  *G = ({s}, {a, b}, P, S)
  P = {S -> a, S -> baS, aS -> bb}
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
Sigma - terminály: a, b, c, .... , 0, 1, ...
N - neterminály, S, A, B, C, ....
