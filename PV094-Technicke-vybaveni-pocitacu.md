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

### __Základní pojmy__
**Počítač**
- stroj na zpracování informací
- pracuje pomocí předem vytvořeného programu
- počítač narozdíl od kalkulačky je schopen akceptovat data a vyhodnotit je

**Informace**
- data, která se strojově zpracovávají
- ve smyslu filozofickém *vše, co nám nebo něčemu podává vědění*

**Program**
- algoritmus zapsaný v programovacím jazyce, který řeší nějaký konkrétní úkol
- na úrovni technického vybavení počítače chápeme program spíše jako posloupnost instrukcí

**Instrukce**
- předpis k provedení činnosti realizovatelný přímo technickým vybvením počítače
- příkladem toho jsou přičtení jedničky, uložení hodnoty do paměti či načtění hodnoty z operační paměť

**Hardware (technické vybavení počítače**
- souhrnný název pro veškerá fyzická zařízení, kterými je počítač vybaven

**Software (programové vybavení počítače)**
- souhrnný název pro veškeré programy, které mohou na počítači pracovat
- software je možno rozdělit na:
  - systémový software = operační systémy, ovladače zařízení, utility pro správu systému
  - aplikační software = textové editory, grafické editory, grafické hry, databázové systémy

**Firmware**
- programové vybavení, které tvoří součást technického vybavení
- až na výjimky nemůže být uživatelem modifikováno
. při modifikaci je třeba být opatrný (například update na novější BIOS, který může být však spjat pouze s určitým typem základní desky)
- chytré řešení od GIGABYTE (dva BIOSy, jeden jako záložní)
- např. BIOS

**Řadič**
- jinak zvaný jako controller
- zařízení převádějící příkazy v symbolické formě (instrukce) na posloupnost signálů ovládajících připojené zařízení
- zařízení, které řídí činnosti jiného zařízení

**Sběrnice**
- soustava vodičů, která umožňuje přenos signálu mezi jednotlivými částmi počítače
- pomocí těchto vodičů mezi sebou jednotlivé části počítače komunikují a přenášejí data
- existují mnohé druhy a řady sběrnic, jako například adresová, datová či rozšiřující sběrnice (slouží tedy k osazení rozšiřujících periférií, jako jsou třeba karty grafické)

**Integrovaný obvod**
- elektronická součástka realizující určité množství obvodových prvků neoddělitelně spojených na povrchu nebo uvnitř určitého spojitého tělesa, aby se dosáhlo ucelené funkce elektronického obvodu

**Vstupní/výstupní zařízení (I/O devices)**
- zařízení určená pro vstup a výstup dat
- např. disky (pevné, pružné), páskové mechaniky, monitor, scanner, ploter, tiskárna etc.

**BIOS (ROM BIOS)**
- z celého anglického **B**asic **I**nput **O**utput **S**ystem
- programov vybaavení v paměti ROM (EPROM, EEPROM, Flash)
- zajišťuje nejzákladnější funkce (např. zavedení OS)

### __Jednotky informace__

**bit**
- 1 bit (binary digit - dvojková číslice):
- základní jednotka informace
- označuje se malým písmenem *b*
- může nabývat pouze hodnot *0* a *1*
- poskytuje množství informace potřebné k rozhodnutí mezi dvěma možnostmi

**Byte**
- jednotka odpovídající 8 bitům

**Word**
- jednotka informace
- platí 1 W = 2 B = 16 b
- občas se užívá i doubleword (1W = 32 b)

### Paměť

**Pamět**
- zařízení sloužící k uchování informací (binárně kódovaných dat)
- kapacita paměti - množství informací, které lze do paměti uložit, udává se v bytech
- zpravidla se užívají předpony (kilo-, mega-, giga-, tera-)
- 1kB = 1024 B (2<sup>10</sup> B)
- bývá rozdělena na buňky jednoznačně identifikovatelné svým číslem (adresa paměti)
- nejmenší adresovatelná jednotka - velikost buňky, která má svou vlastní adresu
  - velikost je variabilní, zpravidla bývá 1 byte (v dnešní době)
  - pružné disky však měli nejmenší adresovatelnou jednotku 1 sektor (čili 512 bytů), čtení a zápis probíhal pouze v sektorech

**Rozdělení paměťi**
- Vnitřní (operační) - slouží k uchování momentálně zpracovaných dat a programů, realizuje se polovodičovými součástkami
- Vnější (periferní) - slouží k dlouhodobějšímu uchování dat, realizuje se na principu magnetického (či optického) záznamu dat)
- vnější paměťi jsou pomalejší, ale za to mají větší kapacitu

- RAM (Random Access Memory) - paměť pro čtení i zápis dat
- ROM (Read Only Memory) - paměť pouze pro čtení dat
- existují i další paměti typu PROM, EPROM, EEPROM (označovali se také jako WORM - Write Once Read Many)

- Paměť s přímým přístupem - dovoluje okamžitě přistoupit k místo s libovolnou adresou
- Paměť se sekvenčním přístupem - pro přístup k libovolnému místu s adresou N je třeba přečíst všechna předchozí místa (0 až n-1), příkladem je třeba páska

- Registr - velmi rychlé paměťové místo (o malé kapacitě v jednotkách bytů) umístěné zpravidla uvnitř procesoru

### __Von Neumannovo schéma__
**Operační paměť**
- slouží k ukládání dat, se kterými se pracuje
- uchovává také jednotlivé instrukce programu

**ALU**
- aritmeticko-logická jednotka
- jednotka sloužící k provádění aritmetických a logických operací
- obsahuje sčítačky, násobičky, komparátory
- dá se přidat i rozšíření jako jsou třeba matematický koprocesor

**Řadič**
- řídící jednotka, stará se o činnost veškerých ostatních zařízení
- dostává stavová hlášení z jednotlivých zařízení

**Vstupní a výstupní zařízení**
- slouží k příjmu a výstupu dat

**Princip funkčnosti**
1) prostřednictvím vstupního zařízení se načtou data a program
2) program i data se přes ALU se načte do operační paměťi
3) ALU začne provádět program, mezivýsledky ukládá do operační paměťi
4) výsledek posílá ALU na výstupní zařízení
5) po celou dobu provádění programu kontroluje řadič správné provádění instrukcí
- procesor je zastoupen řadičem a ALU
- v dnešní době už se toto schéma moc nepoužívá, nicméně hlavní myšlenka zůstává zachována (mám program, ten dělá nějakou činnost, dám ho ke zpracování počítači, ten na jeho základě vykonává svou činnost)

### __Historie počítačů__

**0. generace**
- rok 1940
- velký počet skříní
- operace za sekundu v rámci jednotek
- součástka: relé (sepne/nesepne, 1 nebo 0)
- bug = hmyz vletí do relé a omylem sepne obvod, součástka pak nefunguje :D

**1. generace**
- rok 1950
- desítky skříní
- 10 - 1000 operací za sekundu
- součástka: elektronky

- vybudovány podle von Neumannova schématu
- charakteristický diskrétní režim
- neexistují vyšší programovací jazyky
- neexistují operační systémy
- používány především pro vědeckotechnické výpočty
- př. ENIAC I, MARK-I, UNIVAC I, BECM

**2. generace**
- rok 1958
- do 10 skříní
- tisíce operací za sekundu
- součástka: tranzistor

- charakteristický dávkový režim práce (nasadíme dávku práce, program zpracuje postupně sám)
- vznikají první operační systémy
- vznikají vyšší programovací jazyky (Fortran, Cobol, Algol)
- používají se pro vědeckotechnické výpočty a hromadné zpracování dat
- př. UNIVAC, IBM1401, URAL 1

**3. generace**
- rok 1964
- do 5 skříní
- desetitisíce operací za sekundu
- součástka: IO

**3 a 1/2 generace**
- rok 1972
- 1 skříň
- statisíce operací za sekundu
- součástka: IO (LSI, 1 000 - 10 000 logických členů)

**4. generace**
- rok 1981
- 1 skříň
- desítky milipnů operací za sekundu
- součástka IO (VLSI, 100 000+ logických členů)
