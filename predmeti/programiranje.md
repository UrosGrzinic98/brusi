# Programiranje 

Programer ustvarja nove programe ali sestavne dele programa po dogovorjenih pravilih. Razvijajo programsko opremo. 
 
Programiranju rečemo tudi **kodiranje**.  

Za reševanje določenih problemov uporabljamo **programske jezike**.  

<br>

Vključujejo tudi interdisciplinarna območja kot: 

- **MATEMATIKA** 
- **EKONOMIJA** 
- **UMETNOST**  
- **TEHNIKA** 

<br>

**PROGRAM** izvorna koda določenega programskega jezika. 

Preveden program je zaporedje ukazov v strojni kodi.  
 
<br>

Prevajalnik program ki prevede izvorno kodo nekega programskega jezika v strojno kodo 

**STROJNO KODO** razume računalnik. 

<br>

1 Ukaz izvorne kode lahko pomeni več ukazov v strojni kodi. 

<br>

## Algoritem 

- Je navodilo za reševanje problema 

- Je seznam korakov do končnega rezultata 

- Zapisan v naravnem jeziku, diagramu poteka, psevdo kodi, programskem jeziku 

<br>

**Lastnosti**: ima podatke, vrne rezultat, natančno določen, končen, izvedljiv 

**Izvajalec**: človek, stroj, el. Naprava 

<br><br>

## Razvoj programske opreme

**FAZE**: 

1. Opis problema 
2. Analiza problema 
3. Načrtovanje algoritma 
4. Kodiranje 
5. Preizkušanje, vzdrževanje 

<br> 

**SINTAKSA** – pravila kako more bit sestavljen program, napake odkrije in javi prevajalnik 

**SEMANTIKA** – sintaksa pravilna, napačen program -> nerazumevanje problema, slaba tehnika priprave programa 

**STRUKTURIRANO NAČRTOVANJE** - problem razdelimo na podprobleme in jih rešimo 

**EKSTREMNO NAČRTOVANJE** - pripravimo testne primere in pričakovane rezultate 

**ČIMVEČ PREVERJANJA** – ne moremo preverit če program dela prav, lahko pa ugotovimo, če ne dela prav 

<br>

## Java

- *Programski jezik* 

- Začetek nastajanja **1991** 

- **James Gosling** in sodelavci v **SUN Microsystems** 

- Konkurenca C++ 

<br>

**JRE** – programsko orodje omogoča izvajanje prevedenih javanskih programov 

**JDK** – razvojno orodje za ustvarjalce programske opreme (*JRE included*) 
 
 <br>

**Shranjevanje**: ime.java 

**Preveden program**: ime.class 

**Javac** (**Java Compiler**) - ukaz za predvajanje javanske kode 

**Java** – ukaz za zagon prevedenega program 

<br>

**GLAVNA METODA**: 

```javascript
Public static void main(String[] args){ 
    // code goes here :)
}
```


---

nadaljevanje - treba mergat oz transitionat na lepo

---

#### Nadaljevanje

- `\t` tabulator
- `\n` nova vrstica
- `\'` izpis enojnega narekovaja
- `\''` izpis dvojnega narekovaja
- `\\` izpis backslash-a (leve poševnice)

#### Komentarji

- `//` do konca vrstice se ne upošteva kot program
- `/* vse vrstice tu vmes se ne upoštevajo kot program */`

```javascript
//System.out.println("Danes je "lep"dan");
System.out.println("Danes je lep dan");
/*System.out.println(""-to je dvojni narekovaj);
System.out.println()*/
```
<br>

### Vnašanje podatkov

#### Vnos z argumenti
```javascript
public statuc void main(String[]args)
```

`args` - tabela, ki shranjuje vhodne podatke

```javascript
java imePrograma 1756 2347
```

`imePrograma` - zagon programa
`1756` - prvi podatek
`2347` - drugi podatek

#### Razred scanner

- najprej ga uvozimo: `import java.util.Scanner;`
- v programu:

```javascript
System.out.println("Vpiši podatek");
Scanner podatek = new Scanner(System.in);
String  spremenljivka = podatek.next();
String spremenljivka = podatek.nextLine();
podatek.close();
```

`podatek.next()` je za eno besedo
`podatek.nextLine()` pa za več besed

- kje je podatek?
	- v spremenljivki spremenljivka
	- tip podatka je String (niz)

#### Razred bufferedReader

- `iport java.io.*`
- `public static void main(String[] args) throws IOException`

```javascript
system.out.println("Vpiši podatek");
BufferedReader podatek = new BufferedReader(new InputStreamReader(System.in));
String spremenljivka = podatek.readLine();
podatek.close();
```

<br>

### Generiranje naključnega števila

- `Math.random()` - vrača decimalne vrednosti med0 in 1 (0,999...)
- Kaj vrača spodnji stavek?

```javascript
int x = (int)(Math.random()*7)
```
> nevem
- in naslednji stavek?


```javascript
int x = (int)(Math.random()*6+5)
```
> tudi  nevem

<br>

### Pretvorbe med tipi

- pri vnosu podatkov - ponavadi iz String v int, long, double, float
- med izvajanjem programa - med številskimi tipi ali pri tvorjenju niza številk
- iz String v int
	- `Integer.parseInt(spremelnjivka)`
- iz int v String
	- `Integer.toString(spremelnjivka)`
- iz String v Double
	- `Double.valueOf(spremelnjivka).doubleValue()`
- Double v String
	- `Double.toString(spremelnjivka)`
- ostali tipi (ne String) v int
	- `(int)spremelnjivka`


<br>

### Primerjalni operatorji

- pri preverjanju pogojev (pogojni stavki, zanke)

| znak | pogoj | primer |
|---|---|---|
| `>` | večje  | `a>b` |
| `>=` | večje ali enako | `a>=b` |
| `<` | manjše  | `a<b` |
| `<=` | manjše ali neenako | `a<=b` |
| `==` | enako  | `a==b` |
| `!=` | ni enako | a!=b` |

- če preverjamo več pogojev

| znak | pogoj | primer |
|---|---|---|
| `&&` | IN (AND)| `a==b && b<c` |
| `||` | ALI (OR) | `a==b || b<c` |

<br>

### Pogojni stavek
#### if

- preveri izpolnjenost pogoja ali več pogojev (primerja vrednosti spremenljivk)

> slika logike pogojnega stavka

```javascript
if (pogoj) {
	stavek ali več stavkov
}
```
#### if else

> slika logike if elsa
```javascript
if (pogoj) {
	stavek ali več stavkov
} else {
	stavek ali več stavkov
}
```
#### if else if else

> slika logike if else if elsa
```javascript
if (pogoj) {
	stavek ali več stavkov
} else if (pogoj) {
	stavek ali več stavkov
} else {
	stavek ali več stavkov
}
```

#### if na kratko

```javascript
(pogoj) ? čeJePogojIzpolnjen:čePogojNiIzpolnjen
```

Primer:

```javascript
int a = 5;
int b = 3;
int x = (a>b) ? a:b;
System.out.println(x);
```

#### Switch

- Primerjamo vrednost spremenljivke s konstanto - uporaben, če so vrednosti spremenljivke pričakovane

```javascript
switch (spremenljivka) {
case vrednost1:
	stavki;
break;
case vrednost2:
	stavki;
break;
.
.
.
case vrednostN:
	stavki;
break;
default:
	stavki;
}
```

> to treba malo lepše razložit

> DN: simulacija meta (bacanja) kock - zaženeš program in izpiše pattern od kocke iz * 

```javascript
* *   * *
* *    *
* *   * *
```
>  in tko naprej
