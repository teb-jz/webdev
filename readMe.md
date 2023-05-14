# Spis treści

1. [Wprowadzenie](#wprowadzenie)
    - [Umieszczanie skryptu na stronie](#umieszczanie-skryptu-na-stronie)
    - [Komunikaty konsoli](#komunikaty-konsoli)
2. [Zmienne](#zmienne)
    - [Zmienne i stałe](#zmienne-i-stałe)
    - [Typy danych](#typy-danych)
    - [Konwersje typów](#konwersje-typów)
3. [Operatory](#operatory)
    - [Operatory arytmetyczne](#operatory-arytmetyczne)
    - [Dodatkowe operatory przypisania](#dodatkowe-operatory-przypisania)
    - [Operatory relacyjne](#operatory-relacyjne)
    - [Operatory logiczne](#operatory-logiczne)
4. [Komunikacja z użytkownikiem](#komunikacja-z-użytkownikiem)
5. [Polecenia](#polecenia)

# Wprowadzenie

**JavaScript** to **hybrydowy język programowania** wykorzystywany między innymi na stronach internetowych.

## Umieszczanie skryptu na stronie

Na stronie można umieścić skrypt na dwa podstawowe sposoby. Wykorzystujemy w tym celu znacznik `<script>`, zazwyczaj na końcu kodu witryny.

```html
<!DOCTYPE html>
<html lang = "en">
<head>
    <meta charset = "UTF-8">
    <title>Document</title>
</head>
<body>

    <p>Lorem ipsum</p>

    <script>
        console.log("Hello world!");
    </script>

</body>
</html>
```

W przypadku niewielkich skryptów, cały kod można umieścić pomiędzy znacznikami `<script>`.

```html
<!DOCTYPE html>
<html lang = "en">
<head>
    <meta charset = "UTF-8">
    <title>Document</title>
</head>
<body>

    <p>Lorem ipsum</p>
    
    <script src = "main.js"></script>

</body>
</html>
```

Zazwyczaj jednak skrypt umieszczamy w oddzielnym pliku o rozszerzeniu `js`, a następnie importujemy, podając jego ścieżkę w atrybucie `src`.

> Jeżeli znacznik `<script>` posiada atrybut `src`, powinien pozostać pusty.

## Komunikaty konsoli

W prostych przypadkach testowania kodu często posługujemy się komunikatami konsoli. Wyróżniamy trzy podstawowe **metody**:

```js
console.log("Informacja");
```
```js
console.warn("Ostrzeżenie");
```
```js
console.error("Błąd");
```

Różnią się one pomiędzy sobą wyglądem w konsoli. Przy ich pomocy można wyświetlać na przykład komunikaty, czy wartości poszczególnych **zmiennych**.

# Zmienne

Zmienna to pewne wydzielone miejsce w pamięci komputera, gdzie mogą być przechowywane dane. Wartością zmiennej może być na przykład liczba lub ciąg znaków. Zmienna musi posiadać nazwę symboliczną, przez którą można odwoływać się do niej w kodzie.

## Zmienne i stałe

```js
let zmienna;
```

Przy **deklarowaniu** zmiennej korzystamy ze słowa kluczowego `let`.

```js
const stala = 3.14;
```

W przypadku stałej, wymaganym słowem kluczowym jest `const`. Wartości stałej nie jesteśmy już w stanie zmienić po jej utworzeniu, zatem musimy od razu ją **zainicjalizować**, korzystając ze znaku przypisania `=`.

```js
let x = 9;

x = 11;
```

Po zadeklarowaniu zmiennej lub stałej, przy kolejnych odołaniach pomijamy słowa kluczowe.

## Typy danych

**JavaScript** cechuje **typowanie dynamiczne**, oznacza to, że nie musimy jawnie wskazywać typu danej zmiennej. Jest on nadawany automatycznie w zależności od przechowywanej przez nią wartości. Podstawowe typy wbudowane oferowane przez język to:

- `Number` - liczba,
- `String` - ciąg/łańcuch znaków, napis,
- `Boolean` - wartość logiczna,
- `Object` - obiekt,
- `Null` - brak wartości,
- `Undefined` - wartość nieokreślona.

## Konwersje typów

Wartości można **konwertować** pomiędzy poszczególnymi typami, dzięki temu mogą zostać inaczej interpretowane. W tym celu posłużą nam funkcje wbudowane:
- `parseInt` - rzutowanie na liczbę zmiennoprzecinkową,
- `parseFloat` - rzutowanie na liczbę całkowitą.

```js
const number = 2.13;
const integer = parseInt(number);
```

# Operatory

**JavaScript** podobnie jak inne języki oferuje szereg różnych operatorów, dzięki którym możemy operować na wartościach.

## Operatory arytmetyczne

|Operator|Opis|Przykład|
|:-:|:--|:-:|
|`+`|Dodawanie|`a + 4`|
|`-`|Odejmowanie|`1 - b`|
|`*`|Mnożenie|`7 * 8`|
|`/`|Dzielenie|`a / 1.5`|
|`%`|Reszta z dzielenia (*modulo*)|`a % 2`|
|`**`|Potęgowanie|`b ** 2`|

## Dodatkowe operatory przypisania

Często będziemy musieli zmieniać wartość danej zmiennej, nadpisując ją inną wartością.

```js
let number = 5
number = number + 2
```

Przykładowo, liczbę możemy nadpisać wartością o 2 większą, przypisując jej nową wartość w postaci sumy jej starej wartości i liczby 2. Taki zapis można skrócić przy pomocy danych operatorów dwuargumentowych:

- `+=`,
- `-=`,
- `*=`,
- `/=`,
- `%=`.
- `**=`.

Oraz jednoargumentowych:
- `++`,
- `--`.

Operator `++` odpowiedzialna jest za zwiększenie wartości zmiennej o *1*. Jest to tak zwana **inkrementacja**. Zmniejszenie wartości o *1* nazywamy **dekrementacją** i oznaczamy przez `--`.

|Operator|Opis|Przykład|
|:-:|:--|:-:|
|`+`|Dodawanie|`a + 4`|
|`-`|Odejmowanie|`1 - b`|
|`*`|Mnożenie|`7 * 8`|
|`/`|Dzielenie|`a / 1.5`|
|`%`|Reszta z dzielenia (*modulo*)|`a % 2`|
|`**`|Potęgowanie|`b ** 2`|

## Operatory relacyjne

**Operatory relacyjne** są wykorzystywane najczęściej jako elementy warunków pętli lub instrukcji warunkowcyh. Zwracają one wartość logiczną.

|Operator|Opis|Przykład|
|:-:|:--|:-:|
|`==`|Równe (wartości)|`a == "4"`|
|`===`|Równe (wartości i typy)|`a === "4"`|
|`!=`|Różne (wartości)|`b != 3`|
|`!==`|Różne (wartości lub typy)|`b !== "−3"`|
|`>`|Większe|`a > b`|
|`>=`|Większe lub równe|`b >= −4`|
|`<`|Mniejsze|`2 < a`|
|`<=`|Mniejsze lub równe|`a <= b`|

## Operatory logiczne

Operatory logiczne używa się do konstruowania warunków złożonych.

|Operator|Opis|Przykład|
|:-:|:--|:-:|
|`&&`|Koniunkcja (i, oraz, *and*)|`a > −4 && a < = 4`|
|`\|\|`|Alternatywa (lub, *or*)|`b === −2 \|\| b === 2`|
|`!`|Negacja (*not*)|`!b`|

# Komunikacja z użytkownikiem

Najprostszym i najbardziej prymitywnym sposobem komunikacji z użytkownikiem są okna dialogowe. Wyróżniamy kilka podstawowych metod:

```js
window.alert("Informacja");
```

Metoda `alert` wyświetla informację.

```js
const value = window.confirm("Potwierdzenie");
```

`confirm` wyświetla tekst, oczekując wybrania jednego z dwóch przycisków. Metoda zwraca wartość logiczną w zależności od wyboru, którą można przypisać na przykład do zmiennej i wykorzystać na dalszym etapie.

```js
const value = window.prompt("Pytanie");
```

Metoda `prompt` wyświetla tekst, oczekując wprowadzenie tekstu, po wciśnięciu przycisku wartość jest zwracana.

> Każda wartość wprowadzona przez użytkownika poprzez klawiaturę jest interpretowana jako ciąg znaków. Jeżeli oczekujemy innej interpretacji należy zastosować zmianę typu.

# Polecenia

1. Zadeklarować **zmienną** i zainicjalizować ją wartością liczbową pobraną od użytkownika (`prompt`), sprawdzić czy jest parzysta i w zależnośći od wyniku wyświetlić odpowiedni komunikat (`alert`).
2. Zadeklarować **stałą** i zainicjalizować ją wartością pobraną od użytkownika (`prompt`), sprawdzić czy leży w przedziale *(5; 20]* i w zależnośći od wyniku wyświetlić odpowiedni komunikat (`alert`).
3. Zadeklarować dwie **stałe** i zainicjalizować je wartościmi pobranymi od użytkownika (`prompt`), a następnie wyświetlić ich średnią arytmetyczną (`alert`).
