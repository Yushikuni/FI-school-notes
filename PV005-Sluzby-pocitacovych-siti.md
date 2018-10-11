## 1. odpovědník
Každý z odpovědníků předmětu Služby počítačových sítí musím od jeho otevření úspěšně složit do
- tří týdnů

Základní informace o počítačových službách FI pro začínající studenty najdu v materiálu
- https://www.fi.muni.cz/tech/zaciname-s-fi.pdf

Dostupné technické informace jsou na webu FI ve složce
- https://www.fi.muni.cz/tech/

Jednosměrnou šifrovací funkcí (bez možnosti dešifrování) je v is.muni.cz uloženo heslo
- primární

E-mailová adresa každého uživatele is.muni.cz má internetovou doménu
- mail.muni.cz

Fakultní login (přihlašovací jméno) je tvořen z
- příjmení uživatele

Přímý vstup do Fakultní administrativy FI je na adrese
- https://fadmin.fi.muni.cz/

Každý student FI má e-mailovou adresu
- login@fi.muni.cz

Které heslo je typicky náročnější uhodnout?
- correct horse battery staple

Která z činností je v počítačové síti FI povolena?
- stahování záznamů přednášek

## 2. odpovědník
Masarykova univerzita je připojena k celosvětové síti provozované sdružením
- CESNET

Standardy a další dokumenty popisující internetové protokoly lze najít pod názvem
- RFC (Request For Comments)

RFC2045 https://www.ietf.org/rfc/rfc2045.txt nahrazuje nebo je nahrazen RFC1521?
- nahrazuje

Hyper Text Coffee Pot Control Protocol (HTCPCP/1.0) popisuje RFC
- RFC 2324

Protokol IP (Internet Protocol) zaručuje či nezaručuje, že se datové bloky přenesou všechny, ve správném pořadí, bez duplicit a se správným obsahem?
- nezaručuje

Protokol TCP (Transmission Control Protocol) zaručuje či nezaručuje, že se datové bloky přenesou všechny, ve správném pořadí, bez duplicit a se správným obsahem?
- zaručuje

IP směrovač (router) musí mít (vyberte nejsprávnější odpověď, vezměte v úvahu pouze technologie, které byly zmíněny na přednášce)
- alespoň dva síťové adaptéry

IP směrovač má
- minimálně dvě adresy

Protokol CSMA/CD (Carrier Sense Multiple Access / Collision Detection) zajistí, že
- vysílající před vyslání poslechne, zda je klid, a pak vysílá. Poslouchá během vysílání, zda slyší to, co sám vyslal.

Co je kolize v CSMA/CD?
- dva nebo více vysílajících vysílá současně

Jak rozpozná vysílající v CSMA/CD kolizi?
- že slyší na médiu něco jiného, než co sám vyslal.

Jak dlouho se v CSMA/CD čeká po zjištění kolize před dalším pokusem o vysílání?
- náhodný čas

MAC (Media Access Control) adresa (tj. ethernetová adresa) je tvořena
- šesti bajty

IP adresa v4 (verze 4) je
- číselná

IP adresa v4 má délku
- 4 bajty

V zápisu IP adresy v4 jsou bajty vyšších řádů
- vlevo

V IP adrese v4 je v bajtech vyšších řádů
- adresa sítě

## 3. odpovědník
Dynamicky se IP adresy v lokální síti (např. po připojení do WiFi sítě) přidělují protokolem
- Dynamic Host Configuration Protocol (DHCP)

MAC adresa cíle v lokální síti se zjišťuje protokolem
- ARP Address Resolution Protocol

Adresa v doménovém tvaru má nejvyšší doménu
- vpravo

Proces dotazování při převodu adresy v doménovém tvaru na IP adresu začíná (není-li adresa v cache počítače nebo nameserveru)
- u kořenového nameserveru

Adresu kořenového nameserveru
- má každé zařízení uloženou už z výroby

Správce spravuje informace o počítačích v doméně manuálně v
- primárním nameserveru

IP směrovač ve směrovací tabulce po svém zapnutí má
- pouze informace o přímo připojených sítích ručně zadané správcem

IP směrovač se učí tj. doplňuje do směrovací tabulky další informace
- posloucháním směrovacích tabulek od jiných směrovačů

IP směrovač svoji směrovací tabulku ostatním směrovačům v síti poskytuje
- všesměrovým vysíláním 

Který protokol je vhodnější pro (on-line) přenos videa a zvuku?
- UDP (User Datagram Protocol), který je nespolehlivý (tj. nezaručuje doručení všech datových bloků)

Služba 'ping' pro ověření dostupnosti počítače konkrétní adresy používá protokol
- ICMP (Internet Control Message Protocol)

Konkrétní stroj je adresovaný IP adresou. Čím se však v komunikačním protokolu rozliší aplikační služba, kterou po stroji požaduji?
- předáním čísla portu

## 4. odpovědník
E-maily se od odesílatele k příjemci doručují protokolem
- Simple Mail Transfer Protocol (SMTP)

Přístup k dopisům doručeným do poštovní schránky neposkytuje protokol
- Simple Mail Transfer Protocol (SMTP)

Dle RFC 822 (Internet Message Protocol) obsahuje internetová zpráva hlavičky a tělo. Čím je odděleno tělo od hlaviček?
- prázdným řádkem

Smí mít jedna položka z hlaviček obsah na více řádcích?
- ano, pokračovací řádek musí mít v prvním sloupci bílé místo (mezeru)

Jaký je správný zápis adresy v hlavičce?
- Ferda Mravenec <ferda@mraveniste.cz>

Jaký je správný zápis adresy v hlavičce?
- ferda@mraveniste.cz (Ferda Mravenec)

Ve fyzickém těle dopisu smí být
- pouze text

Primární a sekundární adresáti dopisu jsou popsáni v hlavičkách
- To a Cc

Způsob kódování binárních dat do textové podoby Base64
- převádí tři bajty s libovolným obsahem na čtyři bajty s textem

MIME (Multipurpose Internet Mail Extensions) zavádí symbolické označení typu obsahu souboru. Pro soubor obsahující obrázek ve formátu PNG se použije označení
- image/png

Určení použitého kódování uloženého textu se specifikuje v MIME hlavičce
- Content-Type: text/html; charset=utf8

Není-li v hlavičkách dopisu s tělem obsahujícím text s diakritikou specifikován charset
- je to katastrofa

Zacyklení při doručování dopisu se pozná podle
- množství hlaviček Received
