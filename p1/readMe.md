
# Projekt witryny

## Zawartość
* Witryna napisana w języku *HTML5*, w pliku o nazwie **index** z odpowiednim rozszerzeniem.
* Zastosowany właściwy standard kodowania polskich znaków.
* Zadeklarowany język zawartości witryny - **polski**.
* Tytuł strony widoczny na karcie przeglądarki - **Przykładowa strona**.
* Prawidłowo połączony zewnętrzny arkusz stylów.
* Witryna jest podzielona na semantyczne elementy blokowe.
* U góry witryny znajduje się belka górna zawierająca nagłówek pierwszego stopnia.
* Poniżej leży część główna, a w niej artykuł oraz formularz.
* W artykule jest nagłówek drugiego rzędu, akapit, czteroelementowa lista uporządkowana, pozioma linia oraz kolejny akapit.
* W skład formularza wchodzą dwa pola wejściowe typu liczbowego poprzedzone poprawnie połączonymi etykietami, przycisk i jednowierszowa tabela posiadająca pięć komórek. Wewnątrz drugiej komórki znajduje się znak `+`, a wewnątrz czwartej `=`.

## Wygląd

* Strona powinna w jak największym stopniu przypominać załączoną grafikę.
* Style zdefiniowane w oddzielnym pliku CSS o nazwie **main** i odpowiednim rozszerzeniu.
* Znacznik `body` oraz nagłówek pierwszego i drugiego poziomu mają wyzerowany margines zewnętrzny.
* Znacznik `body`:
    * Krój czcionki: **'Trbuchet MS', sans-serif**.
    * Rozmiar czcionki: *"większy"*.
* Belka górna:
    * Wysokość: *80 pikseli*,
    * Kolor tła: *283618<sub>16</sub>*,
    * Wysokość linii: *80 pikseli*,
    * Wyrównanie tekstu do środka,
    * Biały kolor czcionki.
* Artykuł, formularz - zmiana sposobu obliczania wysokości i szerokości na uwzględniający obramowania i marginesy wewnętrzne - `box-sizing` o odpowiedniej wartości.
* Pole wejściowe, etykieta, przycisk, tabela - szerokość: *150 pikseli*.
* Pole wejściowe, etykieta, przycisk:
    * Blokowy sposób wyświetlania - `display`,
    * dolny margines zewnętrzny: *10 pikseli*.
* Przycisk, tabela - zewnętrzny margines górny: *10 pikseli*.
* Tabela - brak odstępu pomiędzy komórkami - `border-collapse`.
* Komórka:
    * Obramowanie: grubość - *1px*, typ - *ciągłe*.
    * Wyrównanie tekstu do środka,
    * Szerokość: *20 pikseli*.
* Artykuł:
    * Szerokość: *80 procent*,
    * Margines wewnętrzny: *20 pikseli*,
    * Kolor tła: *fefae0<sub>16</sub>*.
* Akapit:
    * Wcięcie tekstu: *25 pikseli*,
    * Wysokość linii: *28 pikseli*.
* Lista - styl punktorów: *wielkie rzymskie liczby*.
* Formularz:
    * Szerokość: *20 procent*,
    * Margines wewnętrzny: *25 pikseli*,
    * Kolor tła: *606c38<sub>16</sub>*,
    * Biały kolor czcionki.

---

Style pozwalające na odpowiednie ułożenie danych elementów należy dobrać samodzielnie - `flex`.

### Oczekiwany wygląd witryny

![Strona](web1.png)

## Działanie

Po wciśnięciu przycisku (zdarzenie `click`) skrypt ma pobrać wartości wprowadzone przez użytkownika do pól wejściowych, przekonwertować je na liczby i dodać je do siebie. Na koniec pierwsza liczba ma zostać wpisana (`innerText`) w pierwszą komórkę tabeli leżącą poniżej przycisku, druga liczba w trzecią komórkę, a wynik w ostatnią.
