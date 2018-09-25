# Neimperativní programování
--------
- cíl předmětu: *Vyvinout se z Pikatchu na Rajchu*
- nemohou se měnit hodnoty proměnných, ale mohou se měnit parametry funkce

### Základní datové typy
**Čísla**
- *Integer* - libovolně velká celá čísla
- *Int* - celá čísla do velikosti slova procesoru
- *Float* - reálná čísla
- *Fractional* - racionální čísla

**Znaky a řetězce**
- *Char* - znak
- *String* - řetězec (totéž co [Char])

**Pravdivostní hodnoty**
- *Bool* - true nebo false

**Víceřádkové definice funkcí**
- na místě formálních parametrů se použijí tzv. vzory
- použije se první vzor, který vyhovuje
- symbol _ vyhovuje libovolnému parametru
- lze použít pro větvení výpočtu

**Prefix a infix**
- *prefixové funkce* - funkce, které stojí před svými parametry (např. *max*, *min*, *succ* či *pred*)
- *infixové funkce* - funkce, které stojí mezi svými parametry (např. *+* či *)*
- aplikace funkcí (zavolání funkce vložením mezery mezi název funkce a funkční hodnoty) má nejvyšší přednost (viz. spodní příklad - jsou naprosto stejné)
```haskell
succ 9 + max 5 4 + 1
(succ 9) + (max 5 4) + 1
```
- prefixové funkce mají přednost před infixovými
```haskell
succ 9 * 10 -- result is 100
succ (9 * 10) -- result is 91
```
- prefixové funkce, které berou dva argumenty, se dají přepsat na infixové pomocí obrácených apostrofů (kvůli čitelnosti)
```haskell
div 92 10
92 `div` 10 -- this is more clear
```

**Odsazování**
- Haskell je *tab sensitive*, namísto něj by se měly používat dvě mezery

**If/else**
- Větvení pomocí if/else je syntakticky podobné imperativním jazykům (nevyužívají se však složené závorky)
- *if* je výraz, čili část kódu, která něco vrací
- else větev je povinná!

### Uspořádané n-tice a seznamy

**N-tice**
- pevně daný počet nějakých hodnot v pevně daném pořadí
- prvek kartézského součinu nosných množin
- používá se, když víme kolik prvků budeme zpracovávat
- syntax
  ```haskell
  ("Hung", "mávicnez10cm")
  ```
**Seznam**
- posloupnost hodnot stejného charakteru (stejného typu)
- může být prázdná, konečná i nekonečná
- každých prvek v seznamu je na nějaké (unikátní) pozici
- používá se, když nevíme kolik prvků budeme zpracovávat
- syntax:
  ```haskell
  [12, 43, -3, 69]
  ```
### Hodnoty a typy

**Typ**
- označení množiny všech hodnot dané kvality
- slouží k popisu datové struktury
- silně typovaný jazyk, každá hodnota má svůj typ
- typy se komponují stejně jako hodnoty
- konkrétní typy:
  - Int - vleze se do jednoho slova
  - Integer
  - Float
  - Char
  - Bool
- složené typy:
  - uspořádané n-tice = (Bool, Int)
  - seznamy [Int], [Char], [[Char]]
- funkcionální typy:
  - Integer -> Bool *("baští" Integer a vrací Bool)*
  - Float -> Float -> Float *("baští" dva Float a vrací Float)*
  - -> znamená transformaci
  - *poslední za šipkou je výstup, všechno ostatní jsou vstupy*
 
**Arita funkce**
- označuje počet parametrů funkce
- nulární (0), unární (1), duální (2), ternární (3)
 
**Polymorfní typy**
- některé funkce nepotebují znát konkrétní typ forálních parametrů, stačí znát jejich strukturu
- typová proměnná se specializuje až při dosazení

**Typové třídy**
- některé funkce nevyžadují konkrétní typ, zároveň nedovolují použití libovolného typu, je třeba omezit třídu typů
- typové třídy:
  - Integral = celočíselné
  - Num = numerické
  - Ord = uspořádané
  - Eq = porovnatelné na rovnost
  - př.
  ```haskell
  Prelude> :t (>)
  (>) :: Ord a => a -> a -> Bool
  ```
  - Bere dva argumenty typu *a*, vrací jeden argument typu *Bool* a oba argumenty *a* musí být uspořádatelné
- => odděluje typové omezení

**Hodnotové konstruktory**
- (,) = hodnotový konstruktor pro uspořádanou dvojici
- (,, ... ,) = hodnotový konstruktor pro uspořádanou n-tici

**Zápis seznamu**
- "ahoj" = ['a', 'h', 'o', 'j'] , jedná se o syntaktickou zkratku



  
  
  

