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
