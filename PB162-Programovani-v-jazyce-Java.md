# Programování v jazyce Java
-----
### Java
- jazyk *3. generace (3GL)* - imperativní jazyk vysoké úrovně
- je jazyk *uiverzální* - není určen pro specifickou aplikační oblast
- je jazyk *objektově-orientovaný* - používá volání metod objektů
- ideovým předchůdce Javy je C++
- svým způsobem je Java obdobou C++, je však zbavena mnoha zbytečností a nepříjemností (méně syntaktických konstrukcí)
- rychle se na ní vyvíjejí skriptovací jazyky (např. Ruby, Jython)
- multiplatformní, přenositelnost
- robustní, silně typovaný
- stabilní knihovny a open-source podpora
- přeložený kód běží v rámci *JVM* (_**J**ava **V**irtual **M**achine_)
- zdrojový i přeložený kód je jednoduše přenositelný mezi UNIX, Windows i Mac OS X
- je velmi dobrá pro psaní *vícevláknových aplikací*
- používá *automatické odklízení nepoužitelných objektů* (tzv. garbage collector)
- aktuální verze Java SE je *Java 8*
- nejčastější IDE - NetBeans a IntelliJIDEA
- JDK - samostatné vývojové prostředí
- JRE - pouze běhové prostředí
- dá se použít *JavaDoc* pro vygenerování (HTML, PDF) dokumentace z komentářů

### Hello world!
- každý řádek kódu musí být zakomponován do nějaké třídy

- zdrojové kódy musí být obsaženy v *.java* souboru, zbytek vzniká při překladu
- první funkce spouští *main()* s danými argumenty
```java
public static void main(String[] args) {  
  System.out.println("Hello, world");
}
```

### Packages
- reprezentují složení různých tříd, principiélně velmi podobné modulům v C či modulům v JavaScriptu
- řeší zároveň kolizi mezi jmény tříd až na globální (z hlediska zeměpisného) úrovni
- daná hierarchie jmen domén
- prakticky reprezentuje adresářovou hierarchii
- vkládá se jako první řádek kódu
```java
package cz.muni.fi.pb162.lecture2.package1;
```
- přidávají se klíčovým slovem *import*
```java
import nz.school.package1.M;
```
### Konstruktor
- metoda, paradigma, která se podílí na "dovytvoření" objektu
- volá se pouze při vytváření objektu, stará se o inicializaci
- nemá návratový typ
- konstruktory se mohou volat navzájem
```java
public Person(String name, String nick) {
  this.name = name;
  this.nick = nick;
}
```
- *this* = odkaz na objekt se kterým právě pracujeme
  - v případě, že this následují kulaté úvozovky (jako volání kontruktoru), tak můžeme třeba zavolat:
  ```java
  public Person(String name) {
    this(name, null)
  }
  ```
  - toto umožní přiřazení jména a nastavení přezdívky jako *null*, musí být na prvním řádku metody
