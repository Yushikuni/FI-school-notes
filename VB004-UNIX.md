## Osmičkový popis práv
-----------

| Bitový zápis | Význam |
| ----- | ------ |
| 4000 | SUID bit |
| 2000 | SGID bit |
| 1000 | sticky bit |
| 0400 | r pro vlastníka |
| 0200 | w pro vlastníka |
| 0100 | x pro vlastníka |
| 0040 | r pro skupinu vlastníků |
| 0020 | w pro skupinu vlastníků |
| 0010 | x pro vlastníků |
| 0004 | r pro ostatní |
| 0002 | w pro ostatní |
| 0001 | x pro ostatní |

### Příklady:

**rwxrwxrwx	(0777)**<br/>
Tato kombinace znamená, že jsou nastavena práva pro čtení, zápis a spuštění pro vlastníka (7), skupinu (7) i ostatní (7). Jednotlivé hodnoty práv se sčítají, čili (4 + 2 + 1 = 7, což odpovídá nastavenému rwx)

**r-xrw-r--	(0564)**<br/>
Pro jednotlivé části si vysvětlíme:
- r + x = 5
- r + w = 6
- r = 4

**r-srw-r-- (4564)**<br/>
Malé S (s) v části pro práva vlastníka určuje, že je nastaven SUID bit, který změnil hodnotu na začátku z 0 na 4. Jednotlivá “s” se vstahují vždy k právu execute (x) a nahrazují tedy pouze x, nikoliv třeba w či r.

**r-Srw-r--	(4464)**<br/>
Velké S (S) v části pro práva vlastníka určuje, že je nastaven SUID bit, který změnil hodnotu na začátku z 0 na 4. **Avšak** velká písmena se nezapočítávají do jednotlivých hodnot trojic bitů pro vyjádření práv, mění pouze hodnotu první trojice bitů, proto je zde 4 namísto 5 v druhé trojici bitů, reprezentující práva vlastníka.

**r-xrw-r-t	(1565)**<br/>
Malé T (t) reprezentuje sticky bit. Uvádí se vždy u práv pro ostatní.

**r-xrw-r-T (1564)**<br/>
Velké T (T) funguje naprosto stejně jako S u SUID či SGID, ovlivňuje tedy hodnotu první trojice bitů, ale neovlivňuje hodnotu trojice bitů pro ostatní.

**r-sr-Sr-x (6545)**<br/>
SUID a SGID nám nastavili prvního hodnotu na 6 (4 + 2).


## Vybrané příklady z laboratoře
-----------
23)
```shell
PV004LAB=$HOME/pv004lab
KLIC=548dc
UKOL=pro

ROOTDIR=$PV004LAB/ukol_${UKOL}_$KLIC

test "$ROOTDIR" = "/home/xuser1/pv004lab/ukol_pro_548dc" && echo ano

mkdir $ROOTDIR
cd $ROOTDIR

echo 'ROOTDIR=$PV004LAB/ukol_${UKOL}_$KLIC' > 48c6e
```

26)
1. Vytvoř si kliknutím ty adresáře
2. Přemísti se do adresáře a
3. Použij echo $SMAZANO
4. Pokud vypíše prázdný řádek, pak je v pohodě, jinak vymaž obsah $SMAZANO pomocí příkazu unset SMAZANO
5. Napiš příkaz: grep lock * > /dev/null || { SMAZANO=$PWD; rm $SMAZANO/`ls | grep smaz | grep -v nesmaz`; };
6. Napiš příkaz set > promene_be5
7. Napiš příkaz unset SMAZANO
8. Opakuj krom 5 - 7 pro adresáře b a c

33)

```shell
#!/bin/bash
option="${1}"
filepath="${2}"
pattern="${3}"
[ -z "$option" ] && echo "Empty parameter" >&2 && exit 1;
case "$option" in
   verze|-v) echo "verze 23b"
   ;;
   celkem|-a)
   if [ ! -f "$filepath" ];
      then echo "Error" >&2 && exit 1;
   else wc -l < "$filepath";
   fi
   ;;
   vybrane|-s)
   if [ ! -f "$filepath" ] || [ -z "$pattern" ];
      then echo "Error" >&2 && exit 1;
   else grep "$pattern" "$filepath"|wc -l;
   fi
   ;;
   nevybrane|-r)
   if [ ! -f "$filepath" ] || [ -z "$pattern" ];
      then echo "Error" >&2 && exit 1;
   else grep -v "$pattern" "$filepath"|wc -l;
   fi
   ;;
   *) echo "Error" >&2 && exit 1;
   ;;
esac
```

34)

```shell
#!/bin/bash
for var in "$@"
do
   mv "$var" "${var%.077}.e2f"
done
```

35)

```
#!/bin/bash
if [ "$#" -ne "4" ]
then
   echo "Error" >&2 && exit 1;
else
   echo "ok 97e1c2733a0db9322259" && exit 0;
fi
```

36)
```
#!/bin/bash

source="${1}"
shift
touch "$source"

counter=1

for arg
do
   content=`cat $arg`
   filename=`basename $arg`
   echo "-- ${counter}. $filename 439b5a77728742dd14ff" >> "$source"
   echo "$content" >> "$source"
   counter=$((counter+1))
done
```

71)
```
:1,$s/^\([^:]*\):\([^:]*\):\([^:]*\):\([^:]*\):\(.*\)$/\4:\2:\1:\3:\5/
:x
```
ajó tak tak se to dělá, stačí kliknout na tušku :D že mě to nenapadlo, stejně jako s těma blbýma závorkama ve cvičení 5 :D
