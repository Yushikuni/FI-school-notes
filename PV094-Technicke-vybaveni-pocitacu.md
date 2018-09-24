# Technické vybavení počítačů

## 1. přednáška - 17. 09. 2018

**Konzultační hodiny**
- Út: 11:00 - 12:30
- Čt: 10:00 - 11:30

**Zkouška:**
- pouze písemná
- 8 otázek, otevřená forma
- maximum 16 bodů, alespoň 8 bodů na E
- 70 minut čistého času

### Základní pojmy
**Počítač:**
- stroj na zpracování informací
- pracuje pomocí předem vytvořeného programu
- počítač narozdíl od kalkulačky je schopen akceptovat data a vyhodnotit je

**Informace:**
- data, která se strojově zpracovávají
- ve smyslu filozofickém *vše, co nám nebo něčemu podává vědění*

**Program:**
- algoritmus zapsaný v programovacím jazyce, který řeší nějaký konkrétní úkol
- na úrovni technického vybavení počítače chápeme program spíše jako posloupnost instrukcí

**Instrukce:**
- předpis k provedení činnosti realizovatelný přímo technickým vybvením počítače
- příkladem toho jsou přičtení jedničky, uložení hodnoty do paměti či načtění hodnoty z operační paměť

**Hardware (technické vybavení počítače):**
- souhrnný název pro veškerá fyzická zařízení, kterými je počítač vybaven

**Software (programové vybavení počítače):**
- souhrnný název pro veškeré programy, které mohou na počítači pracovat
- software je možno rozdělit na:
  - *systémový software* = operační systémy, ovladače zařízení, utility pro správu systému
  - *aplikační software* = textové editory, grafické editory, grafické hry, databázové systémy

**Firmware:**
- programové vybavení, které tvoří součást technického vybavení
- až na výjimky nemůže být uživatelem modifikováno
. při modifikaci je třeba být opatrný (například update na novější BIOS, který může být však spjat pouze s určitým typem základní desky)
- chytré řešení od GIGABYTE (dva BIOSy, jeden jako záložní)
- např. BIOS

**Řadič:**
- jinak zvaný jako *controller*
- zařízení převádějící příkazy v symbolické formě (instrukce) na posloupnost signálů ovládajících připojené zařízení
- zařízení, které řídí činnosti jiného zařízení

**Sběrnice:**
- soustava vodičů, která umožňuje přenos signálu mezi jednotlivými částmi počítače
- pomocí těchto vodičů mezi sebou jednotlivé části počítače komunikují a přenášejí data
- existují mnohé druhy a řady sběrnic, jako například adresová, datová či rozšiřující sběrnice (slouží tedy k osazení rozšiřujících periférií, jako jsou třeba karty grafické)

**Integrovaný obvod:**
- elektronická součástka realizující určité množství obvodových prvků neoddělitelně spojených na povrchu nebo uvnitř určitého spojitého tělesa, aby se dosáhlo ucelené funkce elektronického obvodu

**Vstupní/výstupní zařízení (I/O devices):**
- zařízení určená pro vstup a výstup dat
- např. disky (pevné, pružné), páskové mechaniky, monitor, scanner, ploter, tiskárna etc.

**BIOS (ROM BIOS):**
- z celého anglického _**B**asic **I**nput **O**utput **S**ystem_
- programové vybavení v paměti ROM (EPROM, EEPROM, Flash)
- zajišťuje nejzákladnější funkce (např. zavedení OS)

### Jednotky informace

**bit:**
- 1 bit (binary digit - dvojková číslice):
- základní jednotka informace
- označuje se malým písmenem *b*
- může nabývat pouze hodnot *0* a *1*
- poskytuje množství informace potřebné k rozhodnutí mezi dvěma možnostmi

**Byte:**
- jednotka odpovídající 8 bitům

**Word:**
- jednotka informace
- platí 1 W = 2 B = 16 b
- občas se užívá i *doubleword* (1W = 32 b)

### Paměť

**Pamět**
- zařízení sloužící k uchování informací (binárně kódovaných dat)
- kapacita paměti - množství informací, které lze do paměti uložit, udává se v bytech
- zpravidla se užívají předpony (kilo-, mega-, giga-, tera-)
- 1kB = 1024 B (2<sup>10</sup> B)
- bývá rozdělena na buňky jednoznačně identifikovatelné svým číslem (adresa paměti)
- *nejmenší adresovatelná jednotka* - velikost buňky, která má svou vlastní adresu
  - velikost je variabilní, zpravidla bývá 1 byte (v dnešní době)
  - pružné disky však měli nejmenší adresovatelnou jednotku 1 *sektor* (čili 512 bytů), čtení a zápis probíhal pouze v sektorech

**Rozdělení paměťi**
- *Vnitřní (operační)* - slouží k uchování momentálně zpracovaných dat a programů, realizuje se polovodičovými součástkami
- *Vnější (periferní)* - slouží k dlouhodobějšímu uchování dat, realizuje se na principu magnetického (či optického) záznamu dat)
- vnější paměťi jsou pomalejší, ale za to mají větší kapacitu

- _RAM (**R**andom **A**ccess **M**emory)_ - paměť pro čtení i zápis dat
- _ROM (**R**ead **O**nly **M**emory)_ - paměť pouze pro čtení dat
- existují i další paměti typu PROM, EPROM, EEPROM (označovali se také jako *WORM - Write Once Read Many*)

- *Paměť s přímým přístupem* - dovoluje okamžitě přistoupit k místo s libovolnou adresou
- *Paměť se sekvenčním přístupem* - pro přístup k libovolnému místu s adresou N je třeba přečíst všechna předchozí místa (0 až n-1), příkladem je třeba páska

- *Registr* - velmi rychlé paměťové místo (o malé kapacitě v jednotkách bytů) umístěné zpravidla uvnitř procesoru

### Von Neumannovo schéma
**Operační paměť:**
- slouží k ukládání dat, se kterými se pracuje
- uchovává také jednotlivé instrukce programu

**ALU:**
- aritmeticko-logická jednotka
- jednotka sloužící k provádění aritmetických a logických operací
- obsahuje sčítačky, násobičky, komparátory
- dá se přidat i rozšíření jako jsou třeba matematický koprocesor

**Řadič:**
- řídící jednotka, stará se o činnost veškerých ostatních zařízení
- dostává stavová hlášení z jednotlivých zařízení

**Vstupní a výstupní zařízení:**
- slouží k příjmu a výstupu dat

**Princip funkčnosti:**
1) prostřednictvím vstupního zařízení se načtou data a program
2) program i data se přes ALU se načte do operační paměťi
3) ALU začne provádět program, mezivýsledky ukládá do operační paměťi
4) výsledek posílá ALU na výstupní zařízení
5) po celou dobu provádění programu kontroluje řadič správné provádění instrukcí
- procesor je zastoupen řadičem a ALU
- v dnešní době už se toto schéma moc nepoužívá, nicméně hlavní myšlenka zůstává zachována (mám program, ten dělá nějakou činnost, dám ho ke zpracování počítači, ten na jeho základě vykonává svou činnost)

### Historie počítačů

**0. generace:**
- rok 1940
- velký počet skříní
- operace za sekundu v rámci jednotek
- součástka: relé (sepne/nesepne, 1 nebo 0)
- *bug* = hmyz vletí do relé a omylem sepne obvod, součástka pak nefunguje :D

**1. generace:**
- rok 1950
- desítky skříní
- 10 - 1000 operací za sekundu
- součástka: elektronka

- vybudovány podle von Neumannova schématu
- charakteristický diskrétní režim
- neexistují vyšší programovací jazyky
- neexistují operační systémy
- používány především pro vědeckotechnické výpočty
- př. ENIAC I, MARK-I, UNIVAC I, BECM

**2. generace:**
- rok 1958
- do 10 skříní
- tisíce operací za sekundu
- součástka: tranzistor

- charakteristický dávkový režim práce (nasadíme dávku práce, program zpracuje postupně sám)
- vznikají první operační systémy
- vznikají vyšší programovací jazyky (Fortran, Cobol, Algol)
- používají se pro vědeckotechnické výpočty a hromadné zpracování dat
- př. UNIVAC, IBM1401, URAL 1

**3. generace:**
- rok 1964
- do 5 skříní
- desetitisíce operací za sekundu
- součástka: IO (integrovaný obvod, SSI v kombinaci MSI)

- začíná se objevovat paralelní zpracování programů (aby počítač mohl zpracovávat data a periférie třeba tisknout výsledky)
- zdokonalují se operační systémy
- vznikají další vyšší programovací jazyky (SIMULA, PL/1, C, Pascal, Prolog)
- př. IBM 360, UNIVAC, SIEMENS, BURROUGHS, CDC

**3 a 1/2 generace:**
- rok 1972
- 1 skříň
- statisíce operací za sekundu
- součástka: IO (LSI, 1 000 - 10 000 logických členů)

**4. generace:**
- rok 1981
- 1 skříň
- desítky milipnů operací za sekundu
- součástka IO (VLSI, 100 000+ logických členů)

### Technologie výroby integrovaných obvodů

**Tranzistor:**
- polovodičová součástka, která má tři elektrody (báze, kolektor, emitor)
- NPN - kolektor je +
- PNP - kolektor je - (je uzemněn)

**TTL:**
- _**T**ransistor **T**ransistor **L**ogic_
- rychlá, ale drahá technologie
- základním stavebním prvkem je bipolární tranzistor (NPN, PNP)
- nevýhoda: velká soustřeba el. energie, velké zahřívání takových obvodů
*insert image of NPN, PNP*
- základní zapojení: invertor (mění 1 na 0 a obráceně)
*insert image of invertor circuit*

- tranzistor lze využít jako spínač (invertor), není však nejlepší
> Na bázi přivedeme vysoký proud, tranzistor sepne, mezi vývodem a negovanou hodnotou je nulové napětí, představuje logickou nulu
> Na bázi přivedeme nízký proud, tranzistor nesepne, toto představuje velký odpor. Podle Ohmova zákona velký odpor znamená velké napětí, což představuje logickou jedničku

**PMOS:**
- _**P**ositive **M**etal **O**xide **S**emiconductor_
- technologie používající unipolární tranzistor MOS
- je řízená elektrickým polem, nikoli elektrickým pole
- má menší příkon, tudíž redukuje nároky na spotřebu elektrické energie
- jedná se však o pomalou a dnes již samosatně nepoužívanou technologie (v kombinaci s NMOS se stále používá)

**NMOS:**
- _**N**egative **M**etal **O**xide **S**emiconductor_
- technologie využícící unipolární tranzistor MOS s negativním vodivostním kanálem
- používala se zhruba do začátku 80. let
- levnější a efektivnější než TTL, rychlejší než PMOS

**CMOS:**
- _**C**omplementary **MOS**_
- technologie spojující v jednom návrhu prvky tranzistorů PMOS i NMOS
- obvody CMOS mají malou spotřebu
- používají se pro výrobu velké části dnešních moderních integrovaných obvodů
- jiné pojmenování elektrod: báze = gate, kolektor = drain, source = emitor
- *PMOS* - šipka vede z báze ven
- *NMOS* - šipka vede směrem dovnitř báze
*insert image of invertor curcuit in CMOS technology*

> Invertor v CMOS využívá dvou tranzistorů NMOS a PMOS, které mají opačnou vodivost. Při přivedení proudu vždy jeden z nich sepne, druhý nesepne a bude zastupovat rezistor. (vytvářet odpor) Malé napětí (sepnutí) na NMOS představuje 0, malé napětí na PMOS představuje 1.

**BiCMOS:**
- _**Bi**polar **C**omplementary **M**etal **O**xide **S**emiconductor_
- technologie spojujícíc na jednom čipu prvky bipolární technologie i technologie CMS
- používána zejména firmou Intel k výrobě mikroprocesorů (řada Pentium)

### Základní jednotka
**Obsahuje zpravidla:**
- *základní desku* (mainboard, motherboard) a zařízení na ní integrovaná (síťová, zvuková, grafická karta)
  - občas nevýhodné (grafická karta), protože je třeba na náročnější operace pořídit dodatečné lepší periférie
  - nicméně v případě síťové karty to nemusí být špatné
  - v současné době se snaží výrobci dávat co nejvíce na motherboard
- *procesor:*
  - je třeba, aby byl kompatabilní se základní deskou
- *numerický koprocesor:*
  - původně byl zakomponován ve zvlášním slotu na základní desce
  - aktuálně jej obsahují všechny procesory
- *paměť* (jak vnitřní - operační, tak vnější - diskové jednotky, páskové jednotky)
- *řídící jednotky*
  - původně vnější paměť
  - dříve se jednalo o řadiče, které zodpovídali za řízení pevného disku
  - v současné době jednodušší pro výrobce pevných disků (výrobce vyrobí pevný disk a řídící jednotku a jen zajistí, aby byla kompatabilní s používaným rozhraním)
- *rozšiřující karty*: grafická, zvuková, faxmodemová, síťová karta
- *napájecí zdroj*

### Periférní zařízení
- klávesnice
- zobrazovací jednotka (monitor - na principu katodové trubice, LCD displej)
- myš, trackball (původně), touchpad
- tiskárna
- souřadnicový zapisovač (plotter)
- modem
- scanner
- externí diskové jednotky:
  - CD-ROM, CD-R, CD-RW (liší se možností zápisu)
  - DVD, BD (Blue-Ray disc)
  - magnetooptické disky
  - ZIP, JAZZ (ZIP mají větší kapacitu, JAZZ jsou menší pevné disky)
- zařízení připojitelná ke zvukové kartě (reproduktory, mikrofon, syntetizátor)

## 2. přednáška - 24. 09. 2018

### Základní deska
- označována také jako mainboard či motherboard
- tvoří základ celého počítače
- obsahuje zpravidla:
  - procesor
  - patici pro numerický koprocesor (dnes už integrován automaticky)
  - obvody čipové sady (řadič operační paměti, cache paměti, rozšiřující sběrnice, sběrnice USB)
  - operační paměť
  - vyrovnávací cache paměť
  - rozšiřující sběrnice = k rozšíření o další karty
  - ROM BIOS
  - CMOS paměť + akumulátor zálohující CMOS paměť (obsahuje program Setup uchovávající nastavení ke spuštění)
  - hodiny reálného času (řízené krystalem kmitajícím o dané frekvenci
  - řadič klávesnice
  - nastavovací propojky (jumpers) a přepínače (switches), dva kontakty kolmo k základní desce, které se mohou či nemusí propojit, což vede ke zkratování a základní nastavení (frekvence procesoru, časování paměťi)
  - řadič pružných disků
  - rozhraní pevných disků
  - řadič diskového pole (RAID) = spojení vícero disků do jednoho velkého disku
  - řadič USB sběrnice
  - řadič rozrahní IEEE 1394 (FireWire)
  - port A.G.P.
  - grafickou kartu
  - vstupní/výstupní porty (I/O kartu)
  - zvuková karta
  - síťoví karta
  - AMR (**A**udio **M**odem **R**iser) slot

#### Procesor
- integrovaný obvod zajišťující funkce CPU
- tvoří "srdce" a "mozek" celého počítače
- provdí instrukce programu
- sychronní zařízení, pracuje s hodinovým kmitem generovaným krystalem umístěným na základní desce
- do značné míry ovlinuje ovlivňuje výkon celého počítače
- *"čím rychlejší procesor, tím rychlejší počítač"* (ovlivňuje však i rychlost pevného disku, grafické karty apod.)
- většinou umístěn na základní desce  

**Parametry procesoru**
- *frekvence*: počet operací provedených za sekundu
  - jednotka: Hertz [Hz]
  - například 4,77 MHz - 4,3 GHz
  - pokud je základní deska navržena pro různé frekvence procesoru, pak je možno na ní frekvenci nastavit např. pomocí jumpers, switch
  - *overclocking* = nastavení vyšší frekvence, se zachováním korektní funkce procesoru, než je frekvence pro kterou byl procesor vyroben
  - je proto třeba dbát na adekvátní chlazení procesoru
  - v minulosti se základní desky navrhovaly aby pracovaly se stejnou frekvencí jako procesor
  - současné základní desky pracují s různými frekvencemi
- *efektivita mikrokódu*: efektivita, se kterou jsou napsány jednotlivé mikroprogramy provádející jednotlivé instrukce procesoru
  - počet kroků potřebných pro provedení jedno instrukce (např. vynásobení dvou čísel)
- *numerický koprocesor (FPU)*:
  - přítomnost (epřítomnost speciální jednotky pro přímé provádění výpočtů v pohyblivé desetinné čárce
  - je přítomen u všech procesorů Intel80486DX a vyšších (vyjma 80486SX)
- *počet instrukčních kanálů (pipelines)*:
  - udává maximální počet instrukcí proveditelnch v jednom taktu procesoru
  - rozsah: 1 až 4 instrukční kanály
- *šířka slova*:
  - maximální počet bitů, které je možné zpracovat během jediné operace
  - určuje nejvyšší číslo, které může procesor zpracovat v rámci jedné operace
  - větší čísla musí být rozdělena na menší a zpracována po částech
- *šířka přenosu dat*:
  - *doplnit ze slajdů*
- *L1 (interní), L2 a L3 cache paměť*:
  - L1, nejmenší kapacita, ale nejrychlejší
  - např. 0 - 64kB (L1), 0 - 18 MB (L2), 0 - 24,75 MB (L3)
- *počet jader (cores)*:
  - počet jednotek (logických procesorů) vykonávajících zpracování instrukcí a dat
  - procesory Intel podporují *hyperthreading*, což jim umožňuje paralélně zpracovávat instrukce z více zdrojů
- *velikost adresovatelné paměti*:
  - velikost paměti, kterou je procesor schopen adresovat (používat)
  - je dána šířkou adresové sběrnice a způsobem vytváření fyzické adresy
  - např. 1 MB - 256 TB
  - Logická (virtuální) adresa --segmentace--> Lineární adresa --stránkování--> Fyzická adresa

**Procesory Intel**
- *Procesor 4004*:
  - 4bitový procesor určený pro elektronické kalkulátory
- *Procesor 8080*:
  - 8bitový procesor určený pro první 8bitové osobní počítače
- *Procesor 8086*:
  - uveden na trh v letech 1979 až 1980
  - plně 16bitový procesor (šířka slova 16 bitů, šířka přenosu dat 16 bitů)
  - kompatabilní s procesorem 8080
  - používán v prvních počítačích PC a PC/XT
  - vybaven 20bitovou adresovou sběrnicí => velikost adresovatelné paměti 1 MB
  - dodáván v pouzdrech DIP (**D**ual **I**nline **P**acket) se 40 vývody
  - je ekvivalentem cca 29 000 tranistorů
  > Logická adresa, sestávající se z segmentu (16 bitů) a offsetu (16 bitů), vezmou se, posunou o čtyři bity (offset se posouvá doleva) a doplní nulami, následně se sečtou a vznikne 20 bitová fyzická adresa
- *Procesor 8088*:
  - podobný svému předchůdci
  - má pouze 8bitovou datovou sběrnici
  - zaveden z cenových důvodů
  - levnější, ale pomalejší
- *Procesor 80168/80188*:
  - podobné procesorům 8086/8088
  - efektivnější mikrokód
  - nezaznamenal většího rozšíření
- *Procesor 80268*:
  - navržen v roce 1981
  - obsahuje asi 134 000 tranzistorů
  - plně 16 bitový
  - pracuje ve dvou režimech (reálný režim = real mode a chráněný režim = protected mode)
  - chráněný režim chrání data jednoho programu před jinými programy
  - chránený režim používá jinou metodu segmentace
  > Logická adresa, skládá se ze segmentu a RPL se 2 bity na nejnižší pozici vpravo (**R**equested **P**rivilage **L**evel), RPL umožňuje 4 úrovně ochrany, nejvyšší ochranu má R0, dále TI (**T**able **I**ndex) určující zda se používá globální (GDT) či lokální (LDT) tabulka deskriptorů, TI = 0 reprezentuje GDT, TI = 1 reprezentuje LDT, zbývajících 13 bitů odpovídá selektroru (tzv. index)
  > *GDT/LDT*: má 64 bitů, jako ukazatel do ní slouží 13 bitový selektor, může mít 8192 adres, každá adresa má 24 bitů (vč. informací jako práva přístupu, co je obsahem apod.) a nazývá se jako báze segmentu, přičítáme k ní 16 bitový offset (bez posunu) a vzniká 24 bitová fyzická adresa, každý segment má tudíž velikost 64 kB, celková fyzická adresa má velikost 16 MB (24 bitů)
- *Procesor 80386*
  - na trh uveden v roce 1986
  - později prodáván jako název 80386DX)
  - dodáván v zapouzdření PGA se 132 vývody (čtvercové pouzdro)
  - ekvivalent k cca 275 000 tranzistorů
  - plně 32bitový procesorů (šířka slova: 32 bitů, šířka přenosu dat: 32 bitů)
  - pracuje ve třech režimech:
  1) **reálný režim (real mode)**
  - režim podobný reálnému režimu předchozích procesorů
  - používá stejný adresovací mechanismus
  - stejná maximální velikost operační paměti (1MB)
  - stejná velikost jednoho segmentu (64kB)
  2) **chráněný režim (protected mode)**
  - podobný chráněnému režimu 80286
  - používá 32 datovou sběrnici, čili maximální velikost je 4 GB
  3) **virtuální režim (virtual mode)**
  - plně podřízen chráněnému režimu
  - procesor pracuje podobně jako procesory 8086/8088
  - má možnost virtualizovat 1MB operační paměti, který mohl adresovat 8086 a uložit jej kdekoliv do 4 GB operační paměťi
  - *proces segmentace:*
  - *doplnit screen z prezentace*
  > Princip velmi podobný jako u 80286, položky tabulky deskriptorů produkují 32 bitovou bázovou adresu a sčítáme ji s 32 bitovým offsetem, výsledek je 32 bitová lineární adresa. Pokud má procesor vypnuté stránkování, tak se lineární adresa rovná fyzické, jinak se přechází do procesu stránkování
  
  - *proces stránkování:*
  > Vezme se lineární adresa a provádíme další transformaci, rozdělíme lineární adresu na tři části (offset, tabulka, adresář = od nejmenšího k nejvyššímu bitu), adresář má 10 bitů, tabulka má 10 bitů, offset má 12 bitů, první vybereme 10 bitů a identifikuje podle něj bázi tabulky, těchto 20 bitů použijeme k identifikaci začátku tabulky stránek, k této tabulce přidáme 10 bitů tabulky, abychom našli bázi stránky, k těmto 20 bitům přičteme ještě 12 bitů offsetu a vzniká 32 bitová fyzická adresa
