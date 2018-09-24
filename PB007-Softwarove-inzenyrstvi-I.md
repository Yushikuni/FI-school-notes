# Softwarové inženýrství I
--------
# Přednášky
## Přednáška 1 - 19. 09. 2018

### Softwarové inženýrství
- pojem, který je 50 let starý, vznikl na koferenci NASA
- zabývá se teoriemi, metodami a nástroji k profesionální vývoji softwarů
- zabývá se tím, aby byl systém *cost-effective*, je třeba znát kontext a cílovou klientelu
- protiklad mezi investicí do testování a verifikace (a uspoření nákladů za opravu) vs. nákladnější techniky vývoje 
- software engineering - o softwarů
- system engineering - zahrnuje i hardware

**Historie vývoje**
1) Krabicové produkty
- například operační systémy, slovníky atd.
- typičtější v období 1980+

2) Kustomizované produkty
- vývoj software na míru

3) Online služby
- cloud, mail apod.

**Typy aplikací**
- samostatné desktopové aplikace (krabicové produkty, ale svým způsobem také položky ze Store)
- interaktivní webové aplikace
- počítačové hry (samostatné kvůli vyšším nárokům například na konektivitu)
- vestavěné kontrolní systémy (v rámci hardware, kontrolují ten hardware - například auto či pračku)
- systémy na zpracování dat (první z aplikací, bankovnictví či armáda, hromadné zpracování dat)
- mobilní aplikace
- monitorovací systémy
- IoT systémy (velké sítě propojených zařízení, např. chytré domácnosti)

**Fáze vývoje software**
- softwarový postup - postup aktivit, které proběhnou při vývoji softwaru

1) Specifikace požadavků
- definování požadavků, vazeb a operací
2) Analýza a design (dev)
- analýza - rozmyšlení *co* budeme dělat (např. volba architektury)
- design - rozmýšlíme *jak* budeme dělat (např. jaké zvolíme návrhové vzory)
3) Implementace (dev)
4) Validace a verifikace
- kontrola zda software splňuje to, co zákazník požaduje
5) Evoluce
- modifikace produktu tak, aby reflektoval požadavky zákazníka a trhu (v opačném případě může ustrpnout a zaniknout mezi konkurencí)

### UML v softwarovém vývoji
- vznik v 90. letech, sjednocený
- z anglického *Unified Modeling Language (UML)*
- pomáhá vizualizovat z mnoha pohledů
- externí perspektiva - vztahy v rámci systému, kontext
- strukturní perspektiva - třídy, data, která jsou systémem zpracovávané
- interakční perspektiva - jak spolu třídy komunikují
- perspektiva chování - jakým způsobem se chovají jednotlivé třídy zvlášť

**Oblíbené UML diagramy**
- *Diagram případů užití (Use Case Diagram)* - interakce mezi systémem a okolím
- *Diagram tříd*
- *Sekvenční diagram*
- *Diagram aktivit (Activity diagram)*

### Use Case Diagram
- použití:
- specifikace funkčních požadavků (funkce, které má systém obsahovat)
  - funkční požadavek: měl by umět udělat seznat všech klinik
  - nefunkční požadavek: měl by být naprogramovaný v jazyce Java (toto je specifikace, nikoli požadavek na funkčnost)
- obsahuje:

**Aktér**
- zastupuje entitu, která se systémem pracuje (nachází se vně systému)
- iniciuje aktivitu v diagramu užití
- aktérem může být například i čas
- *generalizace* - dvě či více entit mají velkou část sdílených atributů, ale existuje i odlišné atributy, využívá se pak i dědičnosti

**Use case**
- zpravidla reprezentována slovesnou vazbou (například *zadej objednávku*)
- jedná se o něco, co potřebuje aktér, aby systém udělal
- primární aktor - například student si zapíše kurz
- sekundární aktor - většinou člověk
- vytváříme scénář pro každý use case
  - zpravidla v angličtině, číslování kroků
  - kroky, které se opakují např. v IF či FOR větvení se dávají třeba do 3.2.1 kroku a zanořují se
- *branching* - dá se odskočit z main flow do alternative flow (například kvůli výjimkám)
- dají se generalizovat
- *include* - A include B (B je nutnou částí, bez něj A nefunguje a je součástí A)
- *extend* - B extend A (A je funkční samo o sobě, B však rozšiřuje A)

# Cvičení
## Cvičení 1 - 17. 09. 2018
- celkově 90 bodů, potřeba 50 bodů na E
- cvičení odpovědníky 10x 2 body
- max. 5 bonusových bodů na aktivitu
- UML 2
