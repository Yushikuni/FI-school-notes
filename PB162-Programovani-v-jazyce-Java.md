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
}```

