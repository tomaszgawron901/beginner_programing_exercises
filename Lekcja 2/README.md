Hi, I am Tomek

# Na tej lekcji :
* Utworzysz nowy projekt C#
* Dowiesz się jak pobierć znaki z klawiatury i wypisywać informacje na konsolę
* 

# Tworzenie nowego projektu
ok, zaczniemy od stworzenia nowego projektu.

Odpal visual studio i wybierz "Create a new project"
![i1](/assets/i1.png)

W listach zaznacz "C#", "All platforms", "Console". I wybierz "Console App(.NET Core)"
![i2](/assets/i2.png)

Nazwij projekt jak tam chcesz i wybierz lokalizację która ci odpowiada
![i3](/assets/i3.png)

# Zapoznanie się z programem startowym

Tu piszesz swój kod.
![i4](/assets/i4.png)

Tu jednym przyciskiem kompilujesz i uruchamiaż swój program.
![i5](/assets/i5.png)

Na początek tyle ci wystarczy

# Pobieranie i wypisywanie danych na konsoli
Do pobierania ciągu znaków będziesz używać Console.ReadLine(). Jak sama nazwa wskazuje pobiera ci znaki aż do napotkania znaku końca lini (czyli '\n', a w konsoli do kliknięcia antera).
Do wypisywania na konsoli używasz Console.WriteLine().
*Byłoby ok jakbyś sobie jeszcze poczytał co robi Console.Read(), Console.ReadKey, Console.Write(). Nie jest ci to na razie potrzebne ale warto znać na przyszłość.*
![i6](/assets/i6.png)

**WAŻNE! Pobierając znaki za pomocą Console.ReadLine() pobierasz STRING. Czyli jeżeli chcesz pobrać np liczbę całkowitą to musisz pobrany ciąg znaków zamienić na INT za pomocą funkcji "Parse" tak jak poniżej**
![i7](/assets/i7.png)