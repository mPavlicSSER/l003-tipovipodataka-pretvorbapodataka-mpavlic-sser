[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=22012630&assignment_repo_type=AssignmentRepo)
# C# tipovi podataka

# TIPOVI PODATAKA U C#

## 1. Uvod
U programiranju se podaci spremaju u memoriju pomoću varijabli.  
Varijabla ima:
- tip podatka  
- ime  
- vrijednost  

Tip podatka određuje:
- koju vrstu podataka varijabla smije sadržavati
- koliko memorije zauzima
- koje operacije su dopuštene

U C# najčešći osnovni tipovi podataka su:
int, float, double, bool, char, string.

---

## 2. Osnovni tipovi podataka

### int
- spremanje cijelih brojeva
- primjer: 17, 0, -25
- primjer koda: 
```csharp
int godine = 17;
```

### double
- spremanje decimalnih brojeva s visokom preciznošću
- koristi decimalnu točku (.)
- primjer: 3.14, 1.82
- primjer koda: 
```csharp
double visina = 1.82;
```

### float
- decimalni broj manje preciznosti
- mora imati slovo f na kraju
- primjer: 1.75f
- primjer koda:
```csharp
 float prosjek = 1.75f;
```

### bool
- logičke vrijednosti (true/false)
- primjer: true, false
- primjer koda: 
```csharp
bool punoljetan = false;
```
### char
- jedan znak, zapisuje se u apostrofima
- primjer: 'A', 'B'
- primjer koda: 
```csharp
char slovo = 'A';
```

### string
- tekst, zapisuje se u navodnicima
- primjer: "Marko"
- primjer koda: 
```csharp
string ime = "Marko";
```
---

## 3. Usporedna tablica tipova

| Tip podatka | Što sprema?                       | Primjer   |
|-------------|---------------------------------- |-----------|
| int         | cijeli broj                       | 25        |
| float       | decimalni broj (manja preciznost) | 2.5f      |
| double      | decimalni broj (veća preciznost)  | 3.14      |
| bool        | logička vrijednost                | true      |
| char        | jedan znak                        | 'A'       |
| string      | tekst                             | "Ana"     |

---

## 4. Pravila zapisivanja

### Cijeli brojevi (int)
✔ 17  
✖ "17" (string)

### Decimalni brojevi (double)
✔ 3.14  
✖ 3,14 (krivo)

### Float
✔ 1.75f  
✖ 1.75

### Bool
✔ true  
✖ "true" (string)

### Char
✔ 'A'  
✖ "A"  
✖ 'AB'

### String
✔ "Pozdrav"  
✖ 'Pozdrav'

---

## 5. Deklaracija i inicijalizacija

Deklaracija:
```csharp
int broj;
```
Inicijalizacija:
```csharp
broj = 25;
```
Deklaracija + inicijalizacija:
```csharp
int broj = 25;
```
---

## 6. Primjer korištenja tipova podataka
```csharp
string ime = "Luka";  
int godine = 17;  
double visina = 1.83;  
float prosjek = 4.50f;  
char ocjena = 'A';  
bool punoljetan = false;
```
```csharp
Ispis:
Ime: Luka  
Godine: 17  
Visina: 1.83  
Prosjek: 4.5  
Ocjena: A  
Punoljetan: False  
```
---

## 7. Najčešće pogreške

- "17" nije int, nego string  
- 'AB' nije ispravan char  
- 1,82 nije ispravno (mora biti 1.82)  
- "false" nije bool  
- 1.75 bez f nije float  

---

#  PARSE METODE U C#

## 1. Uvod
U C# sve vrijednosti koje korisnik unese preko `Console.ReadLine()` dolaze kao **string**.  
Ako želimo raditi s brojevima, decimalama, logičkim vrijednostima ili znakovima, string moramo pretvoriti u određeni tip podatka.

Najčešći način pretvorbe stringa u druge tipove je korištenjem **Parse metoda**.

---

## 2. Što je Parse?
`Parse` je metoda koja pretvara **string → određeni tip podatka**.

Svaki tip podatka ima svoju Parse metodu:
```csharp
int.Parse()
double.Parse()
float.Parse()
bool.Parse()
char.Parse()
```

## 3. Primjeri Parse pretvorbi


### Pretvorba string → int
```csharp
int broj = int.Parse("25");
```

### Pretvorba string → double
```csharp
double visina = double.Parse("1.82");
```

### Pretvorba string → float
```csharp
float prosjek = float.Parse("2.50");
```

### Pretvorba string → bool
```csharp
bool aktivan = bool.Parse("true");
```

### Pretvorba string → char
```csharp
char slovo = char.Parse("A");
```

### Parse i korisnički unos

```csharp
Console.Write("Upiši godine: ");
string g = Console.ReadLine();

int godine = int.Parse(g);
Console.WriteLine("Godine: " + godine);

```
