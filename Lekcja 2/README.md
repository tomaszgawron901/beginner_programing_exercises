Hi, I am Tomek

# Na tej lekcji :
* Utworzysz nowy projekt C#
* Dowiesz się jak pobierć znaki z klawiatury i wypisywać informacje na konsolę
* 

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
Jak sama nazwa wskazuje pobiera ci znaki aż do napotkania znaku końca lini (czyli '\n', a w konsoli do kliknięcia antera).

Do wypisywania na konsoli używasz *Console.WriteLine()* lub *Console.Write()*.
Różnica jest taka że WriteLine dodaje na końcu stringa znak przejścia do następnej lini, a Write nie.
*Jak ci się numdzi to możesz poczytać co robi Console.Read(), Console.ReadKey*
![i6](/Lekcja%202/asstes/i6.png)

**WAŻNE! Pobierając znaki za pomocą Console.ReadLine() pobierasz STRING.**
Czyli jeżeli chcesz pobrać np liczbę całkowitą to musisz pobrany ciąg znaków(**string**) zamienić na **int** za pomocą funkcji *Parse()* tak jak poniżej
![i7](/Lekcja%202/asstes/i7.png)

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
var d  = 1.0d;  // double
var d0 = 1.0;   // double
var d1 = 1e+3;  // double
var d2 = 1e-3;  // double
var f  = 1.0f;  // float
var m  = 1.0m;  // decimal
var i  = 1;     // int
var ui = 1U;    // uint
var ul = 1UL;   // ulong
var l  = 1L;    // long
```
