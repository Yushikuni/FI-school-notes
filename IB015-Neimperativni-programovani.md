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
