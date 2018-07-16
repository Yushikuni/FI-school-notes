### Laboratory:
-----------
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
