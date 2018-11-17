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

## 5. odpovědník
Původní varianta protokolu HTTP se dnes nazývá
- 0,9

Při použití metody GET a HTTP/1.0 nebo novějšího posílá klient
- prázdné tělo požadavku, jen hlavičky

V HTTP/1.0 a 1.1 jsou hlavičky od těla odděleny
- prázdným řádkem

CGI program, zpracovávající požadavek metodou POST čte prohlížečem zaslané parametry metody POST
- ze standardního vstupu

Pokud jako první řádek HTTP požadavku uvede klient "GET /", jedná se o protokol verze
- 0,9

Požaduje-li klient URL http://server.cz/cgi-bin/skript.cgi/x.html?a=b, bude mít skript.cgi v proměnné PATH_INFO hodnotu
- /x.html

Požaduje-li klient URL http://server.cz/cgi-bin/skript.cgi/x.html?a=b, bude mít skript.cgi v proměnné QUERY_STRING hodnotu
- a=b

Požaduje-li klient URL http://server.cz/cgi-bin/skript.cgi/x.html?a=b, bude mít skript.cgi v proměnné SCRIPT_NAME hodnotu
- /cgi-bin/skript.cgi

Stavový kód tvaru 2xx obvykle znamená
- úspěšné provedení požadavku

Stavový kód tvaru 3xx obvykle znamená
- neúspěšné provedení požadavku, připadně s odkazem na alternativní URL

Stavový kód tvaru 4xx obvykle znamená
- chybu v klientově požadavku

Stavový kód tvaru 5xx obvykle znamená
- interní chybu serveru

Preferuje-li klient dokumenty v českém jazyce, dá to najevo v HTTP hlavičce Accept-Language: s hodnotou
- cs, *

Informace o znakové sadě, ve které je předávaný dokument, by se přednostně měla uvádět
- v HTTP hlavičce Content-Type

Architektura SSL neumožňuje
- rozumně realizovat virtuální HTTPS servery na téže IP adrese

SSL certifikát je
- veřejný klíč HTTP serveru a jeho jméno, dohromady podepsané tajným klíčem certifikační autority

IPv6 adresa má délku
- 128 bitů

Link-local adresy mají prefix fe80::/10. Jaká je numericky nejvyšší link-local adresa:
- febf:­ffff:­ffff:­ffff:­ffff:­ffff:­ffff:­ffff

Pro zpětnovazebné rozhraní se v IPv6 používá adresa
- ::1

IPv6 definuje právě následující způsoby přenosu:
- unicast, multicast, anycast

Jaký je nejkratší zápis IPv6 adresy 3ffe:­ffff:0273:0000:0042:0000:0000:5fdc?
- 3ffe:­ffff:273:0:42::5fdc

Používáme-li adresu ve formátu EUI-64, je lokální část adresy
- stejně dlouhá jako nelokální část adresy

## 6. odpovědník
Výhodou síťového modelu pracovní skupina NENÍ
- Škálovatelnost

Řadičem domény může být
- Počítač s Windows Server 2016 povýšený jako řadič domény

Alternativní síťová konfigurace se používá,
- když je nastavené získávání IP adresy z DHCP serveru, v případě, že DHCP server neodpoví nebo nepřidělí adresu

Co platí o Alternativní konfiguraci sítě ve Windows?
- Využije se, pokud je nakonfigurována a počítač nedostane konfiguraci od DHCP serveru.

Které tvrzení platí o IP?
- IP je primárně zodpovědné za adresování a směrování paketů mezi počítači.

Které tvrzení platí o TCP?
- TCP poskytuje spojovanou spolehlivou komunikaci po síti.

Které z následujících tvrzení platí o ARP
- ARP je protokol v síťové vrstvě, mapuje IP adresy na MAC adresy.

Co je platná maska podsítě:
- 255.255.255.240

Které tvrzení správně popisuje IPv4adresu:
- 192.168.0.108 je příklad IP adresy třídy C.

Jak vypadá adresa nakonfigurovaná procesem Automatic Private IP Addressing (APIPA)?
- 169.254.x.y

V jakých profilech se může nacházet Windows 8 Firewall?
- Domain, Private, Public

Co platí o Network Discovery v systému Windows 8?
- Je typicky zakázané v Network Location typu Public.

Máme přidělenou síť od ISP 208.147.66.0/24, rozhodli jsme se ji rozdělit na 4
stejné podsítě, kde každá může obsahovat minimálně 50 stanic.
Která z uvedených podsítí je příkladem jedné z těchto 4 podsítí?
- 208.147.66.192/26

Kolik počítačů můžete mít zapojené v IPv4 síti, jejíž adresa je 172.16.0.0/22
- 1022

Kliknu-li ve Windows 10 po připojení do nové sítě v dialogu "Do you want to allow your PC to be discoverable by other PC's and devices on this network?
na tlačítko "Yes",
bude počítač zapojený v síti typu:
- Private

Vrstva L3 se v TCP/IP modelu nazývá:
- Internet

Na jaké vrstvě ISO/OSI modelu sítě pracuje směrovač (Router)?
- L3 Network

Protokol SMB je:
- Client/Server protokol pro sdílení souborů po síti, ustanovující typicky dlouhodobější spojení.

Povolím-li ve Windows 10 pomocí tlačítka "Turn on media streaming" v Media streaming options v Network and Sharing Center možnost zobrazovat dané zařízení v lokální síti , pak platí, že:
- Počítač je schopen v síti komunikovat jako DLNA server a umožňuje přehrávat např. mp3 soubory v AV zařízení připojené do domácí sítě.

UDP protokol je narozdíl od TCP: 
- Umožňuje rychlejší přenos dat

Počítač v kanceláři ve firemní síti přestal komunikovat s Internetem, z výpisu příkazu ipconfig
zjistím, že má nastavenou IP adresu 169.254.1.1, počítač má nastaveno přidělování adresy z DHCP serveru.
Co je příčinou problému?
- DHCP server není na síti dostupný a vypršela doba platnosti konfigurace síťového rozhraní

UTP kabel v přímém zapojení má na konektoru RJ45 dle číslování pinů konektoru od 1 do 8 (z leva, mám-li zobáček vespod)
na obou stranách kabelu stejné zapojení drátů dle barev:
- 1: bílo oranžový, 2: oranžový, 3: bílo zelený, 4: modrý, 5: bílo modrý, 6: zelený, 7: bílo hnědý, 8: hnědý

DLNA umožňuje:
- Jednoduché sdílení multimédií v domácí síti.

## 7. odpovědník

Kolik nafty standardně neobsahuje nádrž pro motor DUPS?
- 2,5 metrů kubických

Kolik vstupních napájecích větví má STS?
- 2

Proč jsou na počítačových sálech umístěny STS?
- ke zvýšení odolnosti jednozdrojových serverů/spotřeb vůči výpadku

Co se nachází pod dvojitou podlahou v počítačových sálech?
- potrubí dopravující chladící vodu mezi počítačovými sály a strojovnou chlazení

Kde na fakultě se nacházejí STOP tlačítka?
- na recepci

Jak rychle by v praxi stoupala teplota v datacentru FI, pokud by jsme náhle vypli chlazení?
- asi 1 stupeň Celsia za minutu

Proč na fakultě používáme u chladícího systému datacenter nižší teplotní gradient než ten, na který byl systém dimenzovaný?
- chlazení tímto způsobem je energeticky efektivnější

Které tvrzení o režimech strojovny chlazení platí?
- plné strojní chlazení spotřebovává více energie než freecooling

Kolik hran má Kybernetický polygon? (Internet napoví.)
- 7

K čemu slouží požární klapky?
- uzavírají vzduchotechnická potrubí, aby zabránily přívodu vzduchu do místa požáru a šíření požáru do jiných oblastí

Na jakém systému běží fakultní router?
- rackový server a Linux

Umožňuje Raspberry Pi standardně napájení přes PoE (Power over Ethernet)?
- ne

## 8. odpovědník
S mírnou nadsázkou platí, že webová stránka či aplikace je hotová, když…
- …už z ní není co odebrat.

Copywriter je:
- „Prodavač za psacím stolem“ odpovědný za poutavou podobu textového obsahu. 

Cílem testování použitelnosti je…
- …odhalit překážky, které brání uživatelům splnit úkol na testovaném webu, tj. použít ho k zamýšlenému účelu.

Designová hlavička stránky…
- …pomáhá identifikovat stránku jako součást webu, obsahuje jméno/logo webu s odkazem na titulní stranu, často také vyhledávací políčko a horizontální navigaci.

Většinu času tráví uživatel…
- …na cizích webových stránkách (protože průměrná session je jen pár stránek během několika málo minut).

Z nabízených odpovědí je pro navigaci nejméně podstatné, že…
- …je umístěna horizontálně nebo vertikálně. 

Vyberte nesprávné tvrzení:
- Počet registrovaných domén, celosvětově jich je zhruba 300 mil., odpovídá počtu webů.

Pro psaní textů pro web platí řada doporučení. Vyberte nesprávné:
- Obsah textu je vhodné psát stylem úvod, zápletka, rozuzlení, aby to nejdůležitější bylo uvedeno až v závěru, když má čtenář všechny informace.

Vyberte nesprávné tvrzení o testování použitelnosti:
- Čím více uživatelů otestujeme najednou, tím lépe.

Čím má smysl začít realizaci nového webu?
- Nejdříve analyzovat obsah a vytvořit zadání. 

Co je dobrým cílem při tvorbě grafiky webu?
- Identita (jedinečnost) a důvěryhodnost. 

K čemu nejsou dobré drátěné modely (wireframes)?
- Lze s jejich pomocí rychle web dokončit a spustit.

Vyberte nesprávné tvrzení:
- Dobrý styly textu pro webovou stránku je esej, román anebo vyprávění. 

## 9. odpovědník
Myslíme-li to vážně, po uvedení nového webu do provozu…
- …bychom se měli zaměřit na analýzu, optimalizaci a efektivní propagaci.

Vyberte správné tvrzení (přístupnost):
- Webová stránka bez přímého příkazu uživatele nemanipuluje uživatelským prostředím.

Vyberte správné tvrzení (přístupnost):
- Obsah ani kód webové stránky nepředpokládá, že uživatel již navštívil jinou stránku. Tj. každá stránka "funguje" samostatně.

U dobrých redakčních systémů neplatí:
- Nelze je dále rozšiřovat přidáním modulů (ať už vyvinutých třetí stranou nebo mnou).

Vyberte nejlepší dokončení věty: Uvedením webu do provozu práce nekončí, naopak začíná…
- …analýza, optimalizace a propagace webu. 

Při analýze návštěvnosti sledujeme především…
- …trend vybraných ukazatelů, např. zda se snižuje míra okamžitého opuštění (bounce rate) a zvyšuje průměrná doba návštěvy.

Konverze je...
- …měřitelná akce návštěvníka webu, jejímž vykonáním se stává zákazníkem. 

Vyberte nesprávné tvrzení. Vysoká návštěvnost webu je dobrá...
- …vždy, hlavně když je zadarmo. 

Při použití JavaScriptového měřícího kódu (webového analytického nástroje, např. Google Analytics)…
- …je možné zjistit více údajů než je zaznamenáno v logu webového serveru.

V článku Web Design is Dead autor doporučuje:
- …podřídit design tomu, co v daném kontextu funguje a měřením je ověřeno.

U webu typu blog se záměrem vybudovat komunitu pravidelných čtenářů očekáváme:
- vysoké procento vracejících se návštěvníků 

Tzv. referrer, tj. adresa, ze které se návštěvník dostal na danou webovou stránku,…
- …je (nepovinnou) součástí HTTP požadavku na webový server.

Mezi funkce Google Analytics nepatří možnost:
- zobrazení barevného zvýraznění stránky podle toho, kde na ní návštěvníci klikají (tzv. teplotní mapa)

Mezi funkce Google Analytics nepatří možnost:
- zaznamenávání přístupů i z prohlížečů bez JavaScriptu a cookies

Google Analytics IQ je:
- zkouška a osobní certifikace (Individual Qualification) prokazující znalosti GA.
