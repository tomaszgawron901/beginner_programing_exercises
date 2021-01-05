Hi, I am Tomek

# Na tej lekcji dowiesz się:
* Jak utworzyć nowy projekt C#
* Jak pobierć znaki z klawiatury i wypisywać informacje na konsolę
* Co to literały i po co są potrzebne.
* Co to var
* Jak zadeklarować tablicę zmiennych

# Tworzenie nowego projektu
ok, zaczniemy od stworzenia nowego projektu.

Odpal visual studio i wybierz "Create a new project"
![i1](/Lekcja%202/asstes/i1.png)

W listach zaznacz "C#", "All platforms", "Console". I wybierz "Console App(.NET Core)"
![i2](/Lekcja%202/asstes/i2.png)

Nazwij projekt jak tam chcesz i wybierz lokalizację która ci odpowiada
![i3](/Lekcja%202/asstes/i3.png)

# Zapoznanie się z programem startowym

Tu piszesz swój kod.
![i4](/Lekcja%202/asstes/i4.png)

Tu jednym przyciskiem kompilujesz i uruchamiasz swój program.
![i5](/Lekcja%202/asstes/i5.png)

Na początek tyle ci wystarczy

# Pobieranie i wypisywanie danych na konsoli

Do pobierania ciągu znaków będziesz używać *Console.ReadLine()*.
Jak sama nazwa wskazuje pobiera ci znaki aż do napotkania znaku końca lini (czyli '\n', a w konsoli do kliknięcia entera).

Do wypisywania na konsoli używasz *Console.WriteLine()* lub *Console.Write()*.
Różnica jest taka że WriteLine dodaje na końcu stringa znak przejścia do następnej lini, a Write nie.
*Jak ci się numdzi to możesz poczytać co robi Console.Read(), Console.ReadKey*
```C#
int integerValue = 10;
string stringValue = "Ala ma kota";

Console.WriteLine(integerValue);                 //  Wypisze "10"
Console.WriteLine("Mam "+integerValue+" lat.");  // Wypisze "Mam 10 lat."
Console.WriteLine(stringValue);                  // Wypisze "Ala ma kota"
```

**WAŻNE! Pobierając znaki za pomocą Console.ReadLine() pobierasz STRING.**
Czyli jeżeli chcesz pobrać np liczbę całkowitą to musisz pobrany ciąg znaków(**string**) zamienić na **int** za pomocą funkcji *Parse()* tak jak poniżej
```C#
string line = Console.ReadLine();
int integerValue = int.Parse(line);
integerValue += 10;
Console.WriteLine(integerValue);
```

# Literały w C#
Jeżeli chcesz przypisać wartość jakiejś zmiennej numerycznej musić wartość zakończyć literałem.
Dzięki literałom kompilator wie jakiego typu wartość przypisać.

Przykład przypisania wartości do zmiennych:
```C#
double d  = 1.0d;
double d0 = 1.0; 
double d1 = 1e+3;
double d2 = 1e-3;
float f  = 1.0f;
decimal m  = 1.0m;
int i  = 1;
uint ui = 1U;
ulong ul = 1UL;
long l  = 1L;
```
W C# jest też coś takiego jak **var**. **Var** sprawia że przy deklaracji zmiennej nie musisz pisać jej typu. Kompilator sam się domyśla o co chodzi.
```C#
var d  = 1.0d;
var d0 = 1.0; 
var d1 = 1e+3;
var d2 = 1e-3;
var f  = 1.0f;
var m  = 1.0m;
var i  = 1;
var ui = 1U;
var ul = 1UL;
var l  = 1L;
```

# Tablice
Tablice deklarujesz w taki sposób
```C#
int n = 10;
int[] table1 = new int[n];
float[] table2 = new float[10];
```

# Proste zadanko
Pewna *n* liczba krasnoludów codziennie schodzi do kopalni aby wydobywać złoto.
Krasnoludy mają między sobą ustaloną pewną regułę.
Nie ważne ile złota poszczegulny z krasnoludów wykopał, pod koniec dnia dzielą się w taki sposób aby każdy z nich miał tyle samo.

Twoim zadaniem jest pomóc krasnalom, i napisać program który ułatwi im podział złota.
Program ma zwracać informację o tym ile w sumie złota zebrali, ile średnio złota przypada na jednego krasnala i ile poszczegulny krasnal musi oddać lub otrzymać złota, tak aby było po równo.

## Dane wejścia
* W pierszej lini podajesz liczbę krasnali *n*. Liczba *n* jest typu **int**.
* W kolejnych *n-liniach* podajesz liczbę *z* złota. Liczba *z* jest typu **float**.

**Przykładowe dane wejścia**
```
Podaj liczbę krasnali: 3

Podaj ilość złota krasnala nr.0: 16.6
Podaj ilość złota krasnala nr.1: 12.7
Podaj ilość złota krasnala nr.2: 8.8
```

## Dane wyjścia
* Wypisz sumę zebranego złota.
* Wypisz średnią arytmetyczną zebranego złota.
* Dla każdego krasnala wypisz ile złota zebrał, ile złota musi oddać lub otrzymać (w przypadku gdy zegrał tyle złota że nie musi nic oddawać ani nic otrzymywać poinformuj o tym inne krasnale).

**Przykładowe dane wyjścia**
```
W sumie krasnale mają 38.1 złota.
Średnio krasnale mają 12.7 złota.
Krasnal nr.0 ma 16.6 złota, powinien oddać 3.9000006 złota.
Krasnal nr.1 ma 12.7 złota, to tyle ile powinien mieć
Krasnal nr.2 ma 8.8 złota, powinien otrzymać 3.8999996 złota.
```

# After-party
Ok teraz jak już zrobiłeś zadanie zastanów się nad pewnym problemem.
Po wpisaniu powyższych danych przykładowych program sugeruje że:
* Krasnal nr. 0 powinien mieć 12.6999994 złota.
* Krasnal nr. 1 powinien mieć 12.7 złota.
* Krasnal nr. 2 powinien mieć 12.6999996 złota.

Z czego wynika ten błąd?
[2-minutowy artykół na ten temat](https://docs.microsoft.com/pl-pl/cpp/build/why-floating-point-numbers-may-lose-precision?view=msvc-160)