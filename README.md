# ObjectiveProgrammingLab1
Programowanie obiektowe lab1

[**1 Typy zmiennych w języku Java**](https://github.com/UniversityOfRzeszow/ObjectiveProgrammingLab2/blob/master/README.md#1-typy-zmiennych-w-języku-java)

[**2 Konstrukcja wyrażeń warunkowych w języku JAVA**](https://github.com/UniversityOfRzeszow/ObjectiveProgrammingLab2/blob/master/README.md#2-konstrukcja-wyrażeń-warunkowych-w-języku-java)

* [2.1 Instrukcja warunkowa `if`](https://github.com/UniversityOfRzeszow/ObjectiveProgrammingLab2/blob/master/README.md#21-instrukcja-warunkowa-if)
* [2.2 Instrukcja warunkowa `if-else`](https://github.com/UniversityOfRzeszow/ObjectiveProgrammingLab2#22-instrukcja-warunkowa-if-else)
* [2.3 Rozbudowana instrukcja warunkowa `else-if`](https://github.com/UniversityOfRzeszow/ObjectiveProgrammingLab2#23-rozbudowana-instrukcja-warunkowa-else-if)
* [2.4 Konstrukcja warunkowa – operator trójargumentowy](https://github.com/UniversityOfRzeszow/ObjectiveProgrammingLab2#24-konstrukcja-warunkowa--operator-trójargumentowy)
* [2.5 Instrukcja wielokrotnego wyboru](https://github.com/UniversityOfRzeszow/ObjectiveProgrammingLab2#25-instrukcja-wielokrotnego-wyboru)

[**3 Konstrukcje pętli**](https://github.com/UniversityOfRzeszow/ObjectiveProgrammingLab2/blob/master/README.md#1-typy-zmiennych-w-języku-java)

* [*3.1 Pętla `while`*](https://github.com/UniversityOfRzeszow/ObjectiveProgrammingLab2#31-pętla-while)
* [*3.2 Pętla `do-while`*](https://github.com/UniversityOfRzeszow/ObjectiveProgrammingLab2#32-pętla-do-while)
* [*3.3 Pętla iteracyjna `for`*](https://github.com/UniversityOfRzeszow/ObjectiveProgrammingLab2#33-pętla-iteracyjna-for)
* [*3.4 Pętla iteracyjna `for-each`*](https://github.com/UniversityOfRzeszow/ObjectiveProgrammingLab2#34-pętla-iteracyjna-for-each)
* [*3.5 Instrukcje `break` i `continue`*](https://github.com/UniversityOfRzeszow/ObjectiveProgrammingLab2#35-instrukcje-break-i-continue)

# 1 Typy zmiennych w języku Java

Java jest językiem silnie typowanym, co oznacza, że każda wartość w języku Java ma dobrze określony typ. Istnieją dwa rodzaje typów: typy obiektowe i typy proste (prymitywne). Typy obiektowe definiowane są przez klasy – i jest bez znaczenia, czy są to klasy które sami zaimplementowaliśmy, czy klasy pochodzące z jakichś bibliotek, np. bibliotek Java SE. Typy proste to typy wbudowane w język, traktowane w specyficzny sposób. Jest 8 typów prostych; są to: `char`, `boolean`, `byte`, `short`, `int`, `long`, `float` oraz `double`.
	Typ `char` reprezentuje pojedynczy znak (np. literę). Zmienne typu char mają wartości odpowiadające dowolnemu znakowi kodowania UTF-16.
	Typ `boolean` reprezentuje wartość typu logicznego. Zmienna typu boolean może przyjmować jedną z dwu wartości: `true` albo `false`.
	Pozostałe typy proste to typy numeryczne. Typy: `byte`, `short`, `int` i `long` to `typy` całkowitoliczbowe tj. typy reprezentujące liczby całkowite. Zmienna typu byte może przyjmować wartości z zakresu od -128 do 127. Zmienna typu `short` z zakresu od -32768 do 32767, typu `int` z zakresu od -2147483648 do 2147483647 a typu `long` z zakresu od -9223372036854775808 do 9223372036854775807.
	Typy `float` oraz double reprezentują liczby zmiennoprzecinkowe. Typ float reprezentuje wartości pojedynczej precyzji a typ double liczby podwójnej precyzji.
	Bodaj najpopularniejszym typem obiektowym obok typu `Object` jest typ `String`. Jest to typ reprezentujący ciąg znaków.

Przykład:

```java 
String a="Typ łańcuchowy";
```

Pewnym specyficznym rodzajem typu obiektowego jest tablica. Typ tablicowy to typ definiujący sekwencję elementów pewnego ustalonego typu. Typ tablicowy oznaczamy umieszczając nawiasy kwadratowe za typem elementów tablicy. Przykładowo, typ tablicowy elementów typu `int` to `int[]` a elementów typu String to `String[]`.
Przykład:

```java
int[] vector;
int[] preinitializedVector = new int[] { 1, 2, 3, 4 };
int[][] twoDimMatrix = new int[][] { { 1, 2, 3 }, { 4, 5, 6 } };
String[] arrayName = {"Ala", "Ela", "Ula", "Ola"};
```

# 2 Konstrukcja wyrażeń warunkowych w języku JAVA


## 2.1 Instrukcja warunkowa `if`

```java
if( warunek ) {
  kod wykonywany warunkowo
}
```


## 2.2 Instrukcja warunkowa `if-else`

```java
if( warunek ) {
  kod wykonywany warunkowo
} else {
  kod wykonywany alternatywnie
}
```

Przykład:

```java
void isPositive(int x) {
 if( x > 0 ) {
    System.out.println("liczba " + x + " jest dodatnia");
  } else {
    System.out.println("liczba " + x + " jest ujemna");
  }
}
```

## 2.3 Rozbudowana instrukcja warunkowa `else-if`

```java
if( warunek ) {
  kod wykonywany warunkowo
} else if ( warunek_drugi ) {
  kod wykonywany gdy spełniony jest drugi warunek
} else {
  kod wykonywany alternatywnie
}
```

Przykład:

```java
void isPositive(int x) {
 if( x > 0 ) {
    System.out.println("liczba " + x + " jest dodatnia");
} else if( x == 0 ) {
    System.out.println("liczba " + x + " jest równa zero");
  } else {
    System.out.println("liczba " + x + " jest ujemna");
  }
}
```

## 2.4 Konstrukcja warunkowa – operator trójargumentowy
```java
warunek ? wartość pierwsza : wartość druga
```
Przykład:

Kod:

```java
public String isEven(int x) {
if(x % 2 == 0)
   return "parzysta";
else
   return "nieparzysta";
}
```

jest równoważny kodowi

```java
public String isEven(int x) {
  return x % 2 == 0 ? "parzysta" : "nieparzysta";
}
```

## 2.5 Instrukcja wielokrotnego wyboru 

```java
switch (wyrażenie wyboru) {
  case wartość_wyboru:
    ciąg instrukcji dla danego wariantu
  case inna_wartość_wyboru:
    ciąg instrukcji dla danego wariantu
  default:
    ciąg instrukcji dla wariantu domyślnego
}
```

Przykład:

```java
public void oddOrEven(int x) {
  switch (x % 2) {
    case 0:
      System.out.println(x + " jest liczbą parzystą");
      break;
    case 1:
      System.out.println(x + " jest liczbą nieparzystą");
      break;
    default:
      System.out.println("nieprzewidziana sytuacja");
  }
}
```

gdzie polecenie brak oznacza, że po spełnieniu warunku i wejściu do danego bloku case, pozostałe bloki nie będą już sprawdzane, zatem kod zawarty w nich na pewno się nie wykona.


# 3 Konstrukcje pętli

## 3.1 Pętla `while`

```java
while( {warunek_pętli} ) {
  ciało pętli
}
```

Przykład:

```java
public void lowerThan(int num) {
  int x = 0;

while( x < num ) {
    System.out.println(x);
    x = x + 1;
  }
}
```

Uwaga: 
Pętla while może nie wykonać kodu w niej zawartego ani raz jeśli warunek początkowy (pierwszy warunek sprawdzany przez pętle nie jest spełniony). 

## 3.2 Pętla do-while 

```java
do {
  ciało pętli
} while ( warunek_pętli );
```

Przykład:

```java
public void lowerThan(int num) {
  int x = 0;
  
  while( x < num ) {
    System.out.println(x);
  
    x = x + 1;
  }
}
```

Uwaga: 
Pętla `do-while` wykona się przynajmniej raz, gdyż warunek sprawdzany jest po wykonaniu ciała pętli.

## 3.3 Pętla iteracyjna `for` 

```java
for(deklaracje_zmiennych; warunek_pętli; instrukcje_inkrementacji) {
  ciało pętli
}
```

Przykład:

```java
public void lowerThan(int num) {
  for( int x = 0 ; x < num ; x++ )  // x++ to x=x+1
    System.out.println(x);
}

public void decrementValue(int num) {
  for( int x = num ; x >= 0 ; x-- ) // x-- to x=x-1
    System.out.println(x);
}
```

Uwaga: 
Pętla for podobnie jak pętla `while` może nie wykonać kodu w niej zawartego ani raz jeśli warunek początkowy (pierwszy warunek sprawdzany przez pętle nie jest spełniony). 

Dodatkowo:

```java
for( ; warunek pętli ; ) {
  ciało pętli
}

jest odpowiednikiem pętli:

while( {warunek pętli} ) {
  ciało pętli
}
```



## 3.4 Pętla iteracyjna `for-each`

Pętla używana do poruszania się po tablicach i kolekcjach danych.

```java
for (deklaracja_zmiennej_pętli : kolekcja lub tablica) {
  ciało pętli
}
```


Przykład:

```java
int[] myArray = { 1, 3, 5, 7, 11 };
    
for (int arrayElem : myArray) {
  System.out.print(arrayElem + " ");
}
```

## 3.5 Instrukcje `break` i `continue`

Instrukcja `BREAK` służy do natychmiastowego przerwania wykonania pętli lub ciągu instrukcji w instrukcji wyboru `SWITCH`. Wykonanie instrukcji `BREAK` powoduje skok do pierwszej instrukcji za przerwaną pętlą czy instrukcją wyboru. Instrukcja ta jest zazwyczaj stosowana do przerwania wykonania w instrukcji wyboru `SWITCH` o której piszę w kolejnym artykule. Użycie w innym celu jest niezalecane i raczej dość rzadko spotykane.

Instrukcja `CONTINUE` może być użyta wewnątrz pętli i służy do przerwania wykonania danej iteracji pętli - tylko wykonanie bieżącej iteracji jest przerwane, nie zaś wykonanie całej pętli, tak jak to ma miejsce w przypadku instrukcji `BREAK`.
W przypadku umieszczenia instrukcji `BREAK` lub `CONTINUE` w pętli zagnieżdżonej w innej pętli mają one skutek tylko dla pętli w której bezpośrednio się znajdują, ale możliwe jest wskazanie – poprzez etykietę – pętli bardziej zewnętrznej. Przykładowo, uruchomienie programu:

```java
public static void main(String[] args) {
  outerLoop:
  for (int j = 0; ; j += 100) {
    for (int i = 0; i < 5; i++) {
      if ((i + j) % 2 == 1)
        continue;
 
      if (j > 100)
        break outerLoop; // przerywa wykonanie także pętli zewnętrznej
 
      System.out.println(i + j + " jest liczbą parzystą");
    }
  }
}
```

skutkuje wyświetleniem sekwencji:

```
0 jest liczbą parzystą
2 jest liczbą parzystą
4 jest liczbą parzystą
100 jest liczbą parzystą
102 jest liczbą parzystą
104 jest liczbą parzystą
```

Instrukcja `CONTINUE` z powyższego przykładu nie została oznaczona żadną etykietą, dlatego dotyczy ona wewnętrznej pętli `FOR`. Instrukcja `BREAK` z etykietą outerLoop powoduje natomiast przerwanie wykonania obydwu pętli, jako że etykietą tą została oznaczona pętla zewnętrzna.
Zadania do wykonania w ramach konspektu:

### Zadanie 1. 
Napisz program obliczający wyróżnik delta i pierwiastki trójmianu kwadratowego.

### Zadanie 2. 
Napisz kalkulator obliczający: sumę, różnicę, iloczyn, iloraz, potęgę, pierwiastek, oraz wartości funkcji trygonometrycznych dla zadanego kąta. Użyj biblioteki Math np. `Math.Sin(2.5)`. Proszę pamiętać, że wartości kąta podawane do funkcji mierzone są miarą łukową. Wyniki działania algorytmów wyświetlaj na konsoli. Do obsługi menu proszę użyć konstrukcji `switch-case` oraz pętli `while`.

### Zadanie 3. 
Napisz program umożliwiający wprowadzanie 10-ciu liczb rzeczywistych do tablicy. Następnie utwórz następujące funkcjonalności używając pętli `for`:

* Wyświetlanie tablicy od pierwszego do ostatniego indeksu.
* Wyświetlanie tablicy od ostatniego do pierwszego indeksu.
* Wyświetlanie elementów o nieparzystych indeksach.
* Wyświetlanie elementów o parzystych indeksach.

Wyniki działania algorytmów wyświetlaj na konsoli. Dla wyboru powyższych funkcjonalności programu utwórz odpowiednie menu. Do obsługi menu użyć rozbudowanej konstrukcji `else-if` oraz pętli `do-while`.

### Zadanie 4. 
Napisz program umożliwiający wprowadzanie 10-ciu liczb. Dla wprowadzonych liczb wykonaj odpowiednie algorytmy:

* oblicz sumę elementów tablicy,
* oblicz iloczyn elementów tablicy,
* wyznacz wartość średnią,
* wyznacz wartość minimalną,
* wyznacz wartość maksymalną.

Wyniki działania algorytmów wyświetlaj na konsoli. Utwórz odpowiednie menu. 

### Zadanie 5. 
Napisz program wyświetlający liczby od 20-0, z wyłączeniem liczb `{2,6,9,15,19}`. Do realizacji zadania wyłączenia użyj instrukcji `continue`;

### Zadanie 6.
Napisz program, który w nieskończoność pyta użytkownika o liczby całkowite. Pętla nieskończona powinna się zakończyć gdy użytkownik wprowadzi liczbę mniejszą od zera. Do opuszczenia pętli nieskończonej użyj instrukcji `break`. Pętle nieskończoną realizuje się następującymi konstrukcjami:

```java
while(true)	
  { ciało pętli }
```
 lub    
```java
for(;;) 
  { ciało pętli }
```
       

### Zadanie 7.  
Napisz program umożliwiający wprowadzanie n liczb oraz sortujący te liczby metodą bąbelkową lub wstawiania. Wyniki wyświetlaj na konsoli.





###### Opracował dr inż. Wojciech Kozioł
