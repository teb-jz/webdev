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
5. [Instrukcje warunkowe](#instrukcje-warunkowe)
    - [Konstrukcja instrukcji warunkowej](#konstrukcja-instrukcji-warunkowej)
    - [Złożone instrukcje warunkowe](#złożone-instrukcje-warunkowe)
    - [Switch](#switch)
    - [Polecenia](#polecenia---instrukcje-warunkowe)
6. [Document object model](#document-object-model)
    - [Pobieranie elementu](#pobieranie-elementu)
    - [Zarządzanie własnościami elementów](#zarządzanie-własnościami-elementów)
    - [Polecenia](#polecenia---document-object-model)

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

# Instrukcje warunkowe

Instrukcje warunkowe w programowaniu służą do warunkowego wykonywania instrukcji, w zależności od tego, czy dany warunek jest spełniony.

## Konstrukcja instrukcji warunkowej

Instrukcja warunkowa jest spełniona, gdy zawarty w niej warunek jest prawdziwy - zwraca wartość logiczną `true`. W przypadku wartości fałszywej - `false`, wskazane instrukcje nie zostaną wykonane.

```js
const condition = true;

if (condition) {

    console.log("Warunek jest spełniony");
}
```

Po słowie kluczowym `if`, wewnątrz nawiasów okrągłych, następuje warunek. Blok kodu, czyli wszystkie instrukcje, które mają zostać wykonane w obrębie instrukcji warunkowej (mają zostać wykonane pod warunkiem), wyznaczają nawiasy klamrowe. Warunkiem może być zmienna lub całe wyrażenie.

> W powyższym przykładzie sprawdzana jest wartość zmiennej condition. Została ona zainicjowana wartością `true` - wartość jest prawdą, co jest równoznaczne ze spełnieniem warunku.

```js
if (condition)
    console.log("Warunek jest spełniony");
```

W przypadku pojedynczej linii kodu, można pominąć nawiasy klamrowe.

## Złożone instrukcje warunkowe

Po instrukcji `if` można dodawać warunki alternatywne za pośrednictwem instrukcji `else if`. Na samym końcu można dodatkowo zdefiniować działanie dla pozostałych przypadków - czyli sytuacji, w której żaden z poprzednich warunków nie został spełniony - `else`.

```js
const number = 2.13;

if (number > 0)
    console.log("Liczba jest dodatnia.")

else if (number < 0)
    console.log("Liczba jest ujemna.")

else
    console.log("Liczba jest równa 0.")
```

## Switch

W przypadku bardzo precyzyjnych warunków instrukcje warunkowe mogą okazać się niewystarczająco czytelne. Alternatywą może być konstrukcja `switch`.

```js
const key = 'b';

switch (key) {

    case 'a':

        console.log("Wprowadzona litera to 'a'.");
        break;

    case 'b':

        console.log("Wprowadzona litera to 'b'.");
        break;

    default:

        console.log("Wprowadzono inną literę.");
        break;
}
```

Po słowie kluczowym `switch` wskazujemy zmienną, której wartość zadecyduje o przeprowadzonych operacjach. W zależności od jej wartości wybierany jest odpowiedni przypadek - `case`. Na końcu umieszczamy przypadek domyślny - `default`. Każdy przypadek kończymy instrukcją `break`.

## Polecenia - instrukcje warunkowe

1. Zadeklarować **zmienną** i zainicjalizować ją wartością liczbową pobraną od użytkownika (`prompt`), sprawdzić czy jest parzysta i w zależnośći od wyniku wyświetlić odpowiedni komunikat (`alert`).
2. Zadeklarować **stałą** i zainicjalizować ją wartością pobraną od użytkownika (`prompt`), sprawdzić czy leży w przedziale *(5; 20]* i w zależnośći od wyniku wyświetlić odpowiedni komunikat (`alert`).
3. Zadeklarować dwie **stałe** i zainicjalizować je wartościmi pobranymi od użytkownika (`prompt`), a następnie wyświetlić ich średnią arytmetyczną (`alert`).
4. Wykorzystując instrukcję `switch`, napisać kalkulator prosty. Skrypt, przy pomocy `prompt`, powinien pobierać trzy wartości od użytkownika. Pierwsza i trzecia będą liczbami – argumentami wybranego działania matematycznego. Druga wartość będzie określała znak operacji (`+`, `-`, `*` lub `/`). Na koniec wyświetlić w informacyjnym oknie dialogowym (`alert`) wynik wybranej operacji.

# Document Object Model

Sposób reprezentacji struktury dokumentu w formie drzewa. Metody **DOM** pozwalają na interakcję z dokumentem, zmianę struktury, stylu czy zawartości.

## Pobieranie elementu

Do odniesienia się do pojedynczych elementów można wykorzystać metody obiektu `document`:
- `querySelector` &ndash; jako parametr podajemy selektor znany z `css`,
- `getElementById` &ndash; parametrem jest **id** elementu.

```html
<div id = "sampleId">Block</div>

<script>
    const e1 = document.querySelector('#sampleId');
    const e2 = document.getElementById('sampleId');

    console.log(e1);
    console.log(e2);
</script>
```

W przypadku zbioru elementów:
- `querySelectorAll` &ndash; jak wyżej, selektor `css`,
- `getElementsByClassName` &ndash; parametrem jest nazwa **klasy** elementów.

```html
<div class = "sampleClass">Block #1</div>
<div class = "sampleClass">Block #2</div>

<script>
    const e1 = document.querySelectorAll('.sampleClass');
    const e2 = document.getElementsByClassName('sampleClass');

    console.log(e1);
    console.log(e2);
</script>
```

## Zarządzanie własnościami elementów

Po pobraniu elementu możemy dowolnie nim zarządzać. Między innymi zmieniać jego zawartość.

```html
<div id = "first">Text</div>
<div id = "second">Text</div>

<script>
    const e1 = document.querySelector("#first");
    const e2 = document.querySelector("#second");

    e1.innerText = "New text";
    e2.innerHTML = "<p>Another text</p>";
</script>
```

Metoda `innerText` pozwala na zmianę lub pobranie tekstu znajdującego się w danym elemencie. `innerHTML` działa podobnie, ale pozwala dodatkowo na prymitywne nadawanie struktury witrynie.

```html
<div>Block</div>

<script>
    const element = document.querySelector("div");

    element.classList.add("className");
</script>
```

Innym przydatnym polem jest `classList`. Pozwala ono na zarządzanie klasami elementu. Posiada metody takie jak `add`, `remove` i `toggle`.

```html
<div>Block</div>

<script>
    const element = document.querySelector("div");

    element.classList.add("className");
</script>
```

Czasami będziemy chcieli nadać jakieś style bezpośrednio, bez wykorzystywania klas.

```html
<div>Block</div>

<script>
    const element = document.querySelector("div");

    element.style.backgroundColor = "grey";
</script>
```

## Polecenia - Document Object Model

1. Przy pomocy okna dialogowego `prompt` pobrać od użytkownika przykładowy tekst i umieścić go na stronie w stworzonym elemencie liniowym `span`. Skorzystać z pola `innerHTML`.
2. Zmodyfikuj polecenie z kalkulatorem prostym tak, by wynik wyświetlał się wewnątrz elementu blokowego `div` na stronie. Element blokowy ma mieć nadaną klasę w zależności od wykonanego działania ("dodawanie", "odejmowanie", "mnozenie", "dzielenie").
3. Przy pomocy okna dialogowego `prompt` pobrać od użytkownika nazwę koloru ("red", "green", "blue", "yellow", "purple") i na jej podstawie zmienić kolor tła elementu `body`. W przypadku podania błędnej wartości kolor ma zmienić się na biały. Zastosować instrukcję `switch`.
