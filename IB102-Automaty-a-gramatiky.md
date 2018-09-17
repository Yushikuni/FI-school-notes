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
- unární operace definována pro všechny i
- N0 = přirozená čísla s 0
- N = přirozená čísla od 1...N
- např.
  *u0 = epsilon
  ui+1 = u.ui*
- konkrétní příklad:
  *u = ba
  u0 = epsilon
  u<sup>1</sup> = u . u<sup>0</sup> = ba . epsilon = ba
  u2 = u . u1 = ba . ba = baba
  .
  .
  .
  *
